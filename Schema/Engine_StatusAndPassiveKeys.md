# Mewgenics Mod Developer Documentation: Engine: Status and Passive Keys

> **Coverage note:** This file documents keys observed in the base game. For undocumented keys found in source files, see [AUDIT_GAPS.md](./AUDIT_GAPS.md). For enum values, see [Enums.md](./Enums.md).

## Engine: Status and Passive Keys

This document lists every confirmed Status and Passive ID found across all game data files. These IDs are used as **dynamic keys** in any Status or Passive Container block (e.g. `statuses`, `passives`, `AddStatusToBasicAttack`, `bonus_passives`). The value paired with each key depends on the context: typically a stack count or duration for statuses, or a boolean/nested object for passives.

> **Note:** With over 1,200 unique IDs, this is the largest system in the game. Granting a character an ID (like `AddStatusToBasicAttack`) gives the character that reactive behaviour permanently.

> **Referenced by:** [`damage_instance` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-damage_instance), [`effects` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-effects), [`bonus_passives` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-bonus_passives), [`temporary_effects` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-temporary_effects), [`Else` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-else), [`ApplyToSource` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytosource), [`Conditional_HasTag` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_hastag), [`Conditional_Enemy` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_enemy), [`Conditional_Ally` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_ally), [`keyword_tooltips` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-keyword_tooltips), [`additional_passives` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-additional_passives), [`RandomStatusFromPool` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-randomstatusfrompool), [`Conditional_Boss` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_boss), [`ApplyToSourceOnKill` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytosourceonkill), [`CanApplyToInanimate` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-canapplytoinanimate), [`Conditional_NotBoss` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_notboss), [`Conditional_HasStatus` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_hasstatus), [`Conditional_GoodRoll` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_goodroll), [`Conditional_Speculative` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_speculative), [`ApplyPassives` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applypassives), [`Conditional_FormulaIsPositive` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_formulaispositive), [`ApplyStatusIfCrit` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applystatusifcrit), [`Conditional_Corpse` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_corpse), [`Conditional_InForm` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_inform), [`Conditional_HealthThreshold` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_healththreshold), [`Conditional_Object` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_object), [`Conditional_PlayerCat` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_playercat), [`CollectsPickupsWithAltEffects` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-collectspickupswithalteffects), [`Conditional_Familiar` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_familiar), [`LateStatusApplication` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-latestatusapplication), [`TakeBonusTurnWithStatus` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-takebonusturnwithstatus), [`TempPassiveWhileHasStatus` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-temppassivewhilehasstatus), [`TimeDelayStatusApplication` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-timedelaystatusapplication), [`post_spawn_statuses` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-post_spawn_statuses), [`ApplyMultipleTimes` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applymultipletimes), [`Conditional_AffectedByElement` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_affectedbyelement), [`Conditional_FirstApplicationThisTurn` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_firstapplicationthisturn), [`Conditional_LastHit` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_lasthit), [`StatusOnBattleEnd` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-statusonbattleend), [`extra_statuses` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-extra_statuses), [`AddStatusToBasicAttack` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-addstatustobasicattack), [`ApplyToRandomPartyMemberIfPossible` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytorandompartymemberifpossible), [`Conditional_BadRoll` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_badroll), [`Conditional_BossOrBig` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_bossorbig), [`Conditional_Buddy` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_buddy), [`Conditional_Displaceable` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_displaceable), [`Conditional_NotAlly` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_notally), [`Conditional_NotBossOrBig` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_notbossorbig), [`Conditional_NotShielded` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_notshielded), [`Conditional_OncePerBattle` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_onceperbattle), [`Conditional_Shielded` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_shielded), [`Math` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-math), [`MeleeRevengeDamage` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-meleerevengedamage), [`OverHealToStatuses` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-overhealtostatuses), [`XIsTargetHealth` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-xistargethealth), [`AlphaStatusOnTurnBegin` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-alphastatusonturnbegin), [`ApplyPassivesToSpawnerWhileAlive` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applypassivestospawnerwhilealive), [`ApplyStatusesNextTurnBegin` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applystatusesnextturnbegin), [`ApplyToOthersWithSharedTagAndFaction` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytootherswithsharedtagandfaction), [`Conditional_ActiveWeather_Any` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_activeweather_any), [`Conditional_Backstab` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_backstab), [`Conditional_CanBeHealed` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_canbehealed), [`Conditional_DebuffRoll` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_debuffroll), [`Conditional_HasCleansableDebuffs` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_hascleansabledebuffs), [`Conditional_LivingPlayerCat` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_livingplayercat), [`Conditional_RandomChance` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_randomchance), [`Conditional_SourceAbilityHasTag` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_sourceabilityhastag), [`Conditional_SourceHasStatus` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_sourcehasstatus), [`PassiveWhileNotTakingTurn` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-passivewhilenottakingturn), [`ReviveNextRound` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-revivenextround), [`StatusGroup` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-statusgroup), [`StatusKillers` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-statuskillers), [`VisualCountDownThenApplyStatus` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-visualcountdownthenapplystatus), [`innate_passives` (Cat_Classes)](./Cat_Classes.md#context-innate_passives), [`passives` (Cat_Mutations)](./Cat_Mutations.md#context-passives), [`AddStatusToBasicAttack` (Cat_Mutations)](./Cat_Mutations.md#context-addstatustobasicattack), [`effects` (Cat_Mutations)](./Cat_Mutations.md#context-effects), [`MeleeRevengeDamage` (Cat_Mutations)](./Cat_Mutations.md#context-meleerevengedamage), [`AddStatusToBasicMeleeAttack` (Cat_Mutations)](./Cat_Mutations.md#context-addstatustobasicmeleeattack), [`StatusOnTookDamage` (Cat_Mutations)](./Cat_Mutations.md#context-statusontookdamage), [`StatusEachTurnBegin` (Cat_Mutations)](./Cat_Mutations.md#context-statuseachturnbegin), [`RandomStatusFromPool` (Cat_Mutations)](./Cat_Mutations.md#context-randomstatusfrompool), [`StatusEachTurnEnd` (Cat_Mutations)](./Cat_Mutations.md#context-statuseachturnend), [`Conditional_RandomChance` (Cat_Mutations)](./Cat_Mutations.md#context-conditional_randomchance), [`StatusEveryXSpellCasts` (Cat_Mutations)](./Cat_Mutations.md#context-statuseveryxspellcasts), [`StatusKilledCharacters` (Cat_Mutations)](./Cat_Mutations.md#context-statuskilledcharacters), [`StatusOnBattleEnd` (Cat_Mutations)](./Cat_Mutations.md#context-statusonbattleend), [`StatusOnEndMove` (Cat_Mutations)](./Cat_Mutations.md#context-statusonendmove), [`StatusOnTookDamageFromAbility` (Cat_Mutations)](./Cat_Mutations.md#context-statusontookdamagefromability), [`Conditional_FirstApplicationThisTurn` (Cat_Mutations)](./Cat_Mutations.md#context-conditional_firstapplicationthisturn), [`Conditional_GoodRoll` (Cat_Mutations)](./Cat_Mutations.md#context-conditional_goodroll), [`PassiveWhenAtFullMana` (Cat_Mutations)](./Cat_Mutations.md#context-passivewhenatfullmana), [`StatusEachRoundEnd` (Cat_Mutations)](./Cat_Mutations.md#context-statuseachroundend), [`StatusEveryXSpellCastsEachTurn` (Cat_Mutations)](./Cat_Mutations.md#context-statuseveryxspellcastseachturn), [`StatusIfDidntMove` (Cat_Mutations)](./Cat_Mutations.md#context-statusifdidntmove), [`StatusIfUnusedMovePoints` (Cat_Mutations)](./Cat_Mutations.md#context-statusifunusedmovepoints), [`StatusOnAllyCatDeath` (Cat_Mutations)](./Cat_Mutations.md#context-statusonallycatdeath), [`StatusOnCastSpell` (Cat_Mutations)](./Cat_Mutations.md#context-statusoncastspell), [`StatusOnDie` (Cat_Mutations)](./Cat_Mutations.md#context-statusondie), [`StatusOnEatFood` (Cat_Mutations)](./Cat_Mutations.md#context-statusoneatfood), [`StatusOnKill` (Cat_Mutations)](./Cat_Mutations.md#context-statusonkill), [`passives` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-passives), [`AddStatusToBasicAttack` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-addstatustobasicattack), [`MeleeRevengeDamage` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-meleerevengedamage), [`ally_rewards` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-ally_rewards), [`effects` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-effects), [`PassiveGroup` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-passivegroup), [`StatusCollector` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statuscollector), [`statuses` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statuses), [`StatusEachTurnEnd` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statuseachturnend), [`StatusOnKill` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusonkill), [`StatusOnTookDamageFromAbility` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusontookdamagefromability), [`keyword_tooltips` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-keyword_tooltips), [`RandomPassivePool` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-randompassivepool), [`Conditional_GoodRoll` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_goodroll), [`Holy` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-holy), [`StatusGroup` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusgroup), [`StatusOnSpawnIn` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusonspawnin), [`StatusOnTookDamage` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusontookdamage), [`TempPassiveUntilSettled` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-temppassiveuntilsettled), [`alternate_energized_effect` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-alternate_energized_effect), [`passive` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-passive), [`statuses_on_enter_form` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statuses_on_enter_form), [`AddStatusToReceivedDamage` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-addstatustoreceiveddamage), [`AddStatusToSpells` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-addstatustospells), [`AddStatusToTrampleDamage` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-addstatustotrampledamage), [`AddStatusToWeapons` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-addstatustoweapons), [`AdventureTokenPassivePool` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-adventuretokenpassivepool), [`Conditional_BadRoll` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_badroll), [`Conditional_HasKnockback` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_hasknockback), [`Conditional_IsPhysicalAttack` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_isphysicalattack), [`Else` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-else), [`FinalBossHitCountdownBoris` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-finalbosshitcountdownboris), [`FinalBossHitCountdownExplosive` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-finalbosshitcountdownexplosive), [`Fire` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-fire), [`ModularPickup` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-modularpickup), [`PassiveWhenDead` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-passivewhendead), [`RandomStatusFromPool` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-randomstatusfrompool), [`StacyMutant_Brace` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_brace), [`StacyMutant_Counter` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_counter), [`StacyMutant_Damage` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_damage), [`StacyMutant_DoubleHead` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_doublehead), [`StacyMutant_Fire` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_fire), [`StacyMutant_Health` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_health), [`StacyMutant_Holy` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_holy), [`StacyMutant_Ice` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_ice), [`StacyMutant_Lightning` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_lightning), [`StacyMutant_Mirror` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_mirror), [`StacyMutant_Speed` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_speed), [`StacyMutant_Thorns` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_thorns), [`StatusAfterXTurns` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusafterxturns), [`StatusEachTurnBeginIfHasStatus` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statuseachturnbeginifhasstatus), [`StatusEachTurnEndForEachTurn` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statuseachturnendforeachturn), [`StatusEachTurnEndIfEnabledAtStartOfTurn` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statuseachturnendifenabledatstartofturn), [`StatusOnDie` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusondie), [`StatusOnEndMove` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusonendmove), [`StatusOnEnemyConfused` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusonenemyconfused), [`StatusOnGainCoins` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusongaincoins), [`StatusOverlappingCharactersAndDie` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusoverlappingcharactersanddie), [`StatusWhenStatusCompletelyRemoved` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statuswhenstatuscompletelyremoved), [`additional_statuses` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-additional_statuses), [`damage_instance` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-damage_instance), [`passives` (Elite_Buffs)](./Elite_Buffs.md#context-passives), [`StatusEachRoundBegin` (Elite_Buffs)](./Elite_Buffs.md#context-statuseachroundbegin), [`effects` (Elite_Buffs)](./Elite_Buffs.md#context-effects), [`MeleeRevengeDamage` (Elite_Buffs)](./Elite_Buffs.md#context-meleerevengedamage), [`StatusEachTurnEnd` (Elite_Buffs)](./Elite_Buffs.md#context-statuseachturnend), [`statuses` (Elite_Buffs)](./Elite_Buffs.md#context-statuses), [`AddStatusToBasicAttack` (Elite_Buffs)](./Elite_Buffs.md#context-addstatustobasicattack), [`StatusEachRoundEnd` (Elite_Buffs)](./Elite_Buffs.md#context-statuseachroundend), [`StatusOnDie` (Elite_Buffs)](./Elite_Buffs.md#context-statusondie), [`StatusOnEnemyCastSpell` (Elite_Buffs)](./Elite_Buffs.md#context-statusonenemycastspell), [`StatusOnKill` (Elite_Buffs)](./Elite_Buffs.md#context-statusonkill), [`self_status_next_fight` (Events_and_Encounters)](./Events_and_Encounters.md#context-self_status_next_fight), [`party_status_next_fight` (Events_and_Encounters)](./Events_and_Encounters.md#context-party_status_next_fight), [`global_effect_next_fight` (Events_and_Encounters)](./Events_and_Encounters.md#context-global_effect_next_fight), [`CharacterTypeGainsStatusAtBattleStart` (Events_and_Encounters)](./Events_and_Encounters.md#context-charactertypegainsstatusatbattlestart), [`StatusRandomEnemiesOnBattleStart` (Events_and_Encounters)](./Events_and_Encounters.md#context-statusrandomenemiesonbattlestart), [`effects` (House_and_Environment)](./House_and_Environment.md#context-effects), [`Else` (House_and_Environment)](./House_and_Environment.md#context-else), [`StatusCharactersOnRoundEnd` (House_and_Environment)](./House_and_Environment.md#context-statuscharactersonroundend), [`ApplyPassives` (House_and_Environment)](./House_and_Environment.md#context-applypassives), [`CharacterTypeGainsStatusAtBattleStart` (House_and_Environment)](./House_and_Environment.md#context-charactertypegainsstatusatbattlestart), [`Conditional_GoodRoll` (House_and_Environment)](./House_and_Environment.md#context-conditional_goodroll), [`RandomStatusFromPool` (House_and_Environment)](./House_and_Environment.md#context-randomstatusfrompool), [`StatusAllCharactersOnSpawn` (House_and_Environment)](./House_and_Environment.md#context-statusallcharactersonspawn), [`StatusCharactersOnRoundStart` (House_and_Environment)](./House_and_Environment.md#context-statuscharactersonroundstart), [`Conditional_Corpse` (House_and_Environment)](./House_and_Environment.md#context-conditional_corpse), [`Conditional_HasTag` (House_and_Environment)](./House_and_Environment.md#context-conditional_hastag), [`Conditional_PartyMember` (House_and_Environment)](./House_and_Environment.md#context-conditional_partymember), [`StatusOnBattleEnd` (House_and_Environment)](./House_and_Environment.md#context-statusonbattleend), [`extra_statuses` (House_and_Environment)](./House_and_Environment.md#context-extra_statuses), [`passives` (Items_and_Equipment)](./Items_and_Equipment.md#context-passives), [`AddStatusToBasicAttack` (Items_and_Equipment)](./Items_and_Equipment.md#context-addstatustobasicattack), [`effects` (Items_and_Equipment)](./Items_and_Equipment.md#context-effects), [`MeleeRevengeDamage` (Items_and_Equipment)](./Items_and_Equipment.md#context-meleerevengedamage), [`StatusOnBattleEnd` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonbattleend), [`StatusEachTurnEnd` (Items_and_Equipment)](./Items_and_Equipment.md#context-statuseachturnend), [`StatusOnBreak` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonbreak), [`Conditional_GoodRoll` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_goodroll), [`StatusOnKill` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonkill), [`StatusOnTookDamage` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusontookdamage), [`StatusOnBattleStart` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonbattlestart), [`StatusEachTurnBegin` (Items_and_Equipment)](./Items_and_Equipment.md#context-statuseachturnbegin), [`AddSelfStatusToBasicAttack` (Items_and_Equipment)](./Items_and_Equipment.md#context-addselfstatustobasicattack), [`AddStatusToAllDamage` (Items_and_Equipment)](./Items_and_Equipment.md#context-addstatustoalldamage), [`StatusAlliesOnBattleStart` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusalliesonbattlestart), [`StatusOnKillEnemy` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonkillenemy), [`AddPassivesToMinions` (Items_and_Equipment)](./Items_and_Equipment.md#context-addpassivestominions), [`ApplyToSource` (Items_and_Equipment)](./Items_and_Equipment.md#context-applytosource), [`StatusOnDie` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusondie), [`StatusOnEndMove` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonendmove), [`Conditional_HasStatus` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_hasstatus), [`Else` (Items_and_Equipment)](./Items_and_Equipment.md#context-else), [`StatusOnTakeHealthOrShieldDamage` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusontakehealthorshielddamage), [`StatusOnTurnEndIfDidntCastAbilityTypes` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonturnendifdidntcastabilitytypes), [`StatusRandomEnemiesOnBattleStart` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusrandomenemiesonbattlestart), [`CatchProjectiles` (Items_and_Equipment)](./Items_and_Equipment.md#context-catchprojectiles), [`Conditional_PartyMember` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_partymember), [`PassiveWhenDead` (Items_and_Equipment)](./Items_and_Equipment.md#context-passivewhendead), [`StatusAllCharactersOnSpawn` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusallcharactersonspawn), [`StatusEveryXSpellCasts` (Items_and_Equipment)](./Items_and_Equipment.md#context-statuseveryxspellcasts), [`StatusIfUnusedMovePoints` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusifunusedmovepoints), [`StatusOnPopCorpse` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonpopcorpse), [`AddStatusToElementDamage` (Items_and_Equipment)](./Items_and_Equipment.md#context-addstatustoelementdamage), [`AddStatusToKnockbackDamage` (Items_and_Equipment)](./Items_and_Equipment.md#context-addstatustoknockbackdamage), [`AddStatusToSpells` (Items_and_Equipment)](./Items_and_Equipment.md#context-addstatustospells), [`ApplyStatusesToRandomEnemiesEachTurn` (Items_and_Equipment)](./Items_and_Equipment.md#context-applystatusestorandomenemieseachturn), [`Conditional_Adjacent` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_adjacent), [`Conditional_BadRoll` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_badroll), [`Conditional_Boss` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_boss), [`Conditional_HasTag` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_hastag), [`Conditional_OncePerBattle` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_onceperbattle), [`PassiveIfWeaponIsUsable` (Items_and_Equipment)](./Items_and_Equipment.md#context-passiveifweaponisusable), [`StatusAfterCastSpell` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusaftercastspell), [`StatusAfterXStacks` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusafterxstacks), [`StatusIfUnusedActPoints` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusifunusedactpoints), [`StatusOnAllyCatDeath` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonallycatdeath), [`StatusOnBackstab` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonbackstab), [`StatusOnBreakItem` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonbreakitem), [`StatusOnCastSpell` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusoncastspell), [`StatusOnGainCoins` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusongaincoins), [`StatusOnSetPieceBreak` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonsetpiecebreak), [`bonus_passives` (Items_and_Equipment)](./Items_and_Equipment.md#context-bonus_passives), [`keyword_tooltips` (Items_and_Equipment)](./Items_and_Equipment.md#context-keyword_tooltips), [`passive` (Items_and_Equipment)](./Items_and_Equipment.md#context-passive), [`AddPassivesToCharmed` (Items_and_Equipment)](./Items_and_Equipment.md#context-addpassivestocharmed), [`AddSelfStatusToWeapons` (Items_and_Equipment)](./Items_and_Equipment.md#context-addselfstatustoweapons), [`AddStatusToBackstabs` (Items_and_Equipment)](./Items_and_Equipment.md#context-addstatustobackstabs), [`AddStatusToFirstSpellEachTurn` (Items_and_Equipment)](./Items_and_Equipment.md#context-addstatustofirstspelleachturn), [`AddStatusToWeapons` (Items_and_Equipment)](./Items_and_Equipment.md#context-addstatustoweapons), [`ApplyPassives` (Items_and_Equipment)](./Items_and_Equipment.md#context-applypassives), [`ApplyToRandomPartyMemberIfPossible` (Items_and_Equipment)](./Items_and_Equipment.md#context-applytorandompartymemberifpossible), [`Conditional_Ally` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_ally), [`Conditional_Corpse` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_corpse), [`Conditional_Enemy` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_enemy), [`Conditional_HasCleansableDebuffs` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_hascleansabledebuffs), [`Conditional_HealthThreshold` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_healththreshold), [`Conditional_ManaThreshold` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_manathreshold), [`Conditional_PlayerCat` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_playercat), [`Conditional_RandomChance` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_randomchance), [`Conditional_Shielded` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_shielded), [`ConvertDamageToScaledStatus` (Items_and_Equipment)](./Items_and_Equipment.md#context-convertdamagetoscaledstatus), [`CritsApplyStatus` (Items_and_Equipment)](./Items_and_Equipment.md#context-critsapplystatus), [`Eternal` (Items_and_Equipment)](./Items_and_Equipment.md#context-eternal), [`GlobalFlowerTrapperAura` (Items_and_Equipment)](./Items_and_Equipment.md#context-globalflowertrapperaura), [`PassiveWhileHasDurability` (Items_and_Equipment)](./Items_and_Equipment.md#context-passivewhilehasdurability), [`PassiveWhileInMonkMeleeStance` (Items_and_Equipment)](./Items_and_Equipment.md#context-passivewhileinmonkmeleestance), [`PassiveWhileShielded` (Items_and_Equipment)](./Items_and_Equipment.md#context-passivewhileshielded), [`RandomStatusFromPool` (Items_and_Equipment)](./Items_and_Equipment.md#context-randomstatusfrompool), [`ReviveNextRound` (Items_and_Equipment)](./Items_and_Equipment.md#context-revivenextround), [`ScaledStatusOnHolyShieldBlock` (Items_and_Equipment)](./Items_and_Equipment.md#context-scaledstatusonholyshieldblock), [`ScaledStatusOnSpendMana` (Items_and_Equipment)](./Items_and_Equipment.md#context-scaledstatusonspendmana), [`StatDependentPassive` (Items_and_Equipment)](./Items_and_Equipment.md#context-statdependentpassive), [`StatusAfterXTurns` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusafterxturns), [`StatusAlliesEachTurn` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusallieseachturn), [`StatusAlliesOnDeath` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusalliesondeath), [`StatusEachRoundEnd` (Items_and_Equipment)](./Items_and_Equipment.md#context-statuseachroundend), [`StatusEachTurnEndForEachTurn` (Items_and_Equipment)](./Items_and_Equipment.md#context-statuseachturnendforeachturn), [`StatusOnCollectPickup` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusoncollectpickup), [`StatusOnDodge` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusondodge), [`StatusOnEatFood` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusoneatfood), [`StatusOnEatPill` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusoneatpill), [`StatusOnEnemyDeath` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonenemydeath), [`StatusOnFallAsleep` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonfallasleep), [`StatusOnHealed` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonhealed), [`StatusOnPickupCoins` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonpickupcoins), [`StatusOnTurnEndIfCastNSpells` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonturnendifcastnspells), [`StatusOnUseBasicAttack` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonusebasicattack), [`StatusWhenAllySpendsMana` (Items_and_Equipment)](./Items_and_Equipment.md#context-statuswhenallyspendsmana), [`TempPassiveUntilSettled` (Items_and_Equipment)](./Items_and_Equipment.md#context-temppassiveuntilsettled), [`damage_instance` (Items_and_Equipment)](./Items_and_Equipment.md#context-damage_instance), [`CharacterTypeGainsStatusAtBattleStart` (Miscellaneous)](./Miscellaneous.md#context-charactertypegainsstatusatbattlestart), [`passives` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passives), [`AddStatusToBasicAttack` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustobasicattack), [`effects` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-effects), [`AddPassivesToMinions` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addpassivestominions), [`StatusOnTookDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusontookdamage), [`StatusEachTurnEnd` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuseachturnend), [`StatusOnBattleEnd` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonbattleend), [`StatusOnKill` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonkill), [`StatusOnStanceSwitch` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonstanceswitch), [`StatusEachTurnBegin` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuseachturnbegin), [`Conditional_Ally` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_ally), [`CritsApplyStatus` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-critsapplystatus), [`MeleeRevengeDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-meleerevengedamage), [`PassiveIfAllArmorEmpty` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passiveifallarmorempty), [`RandomStatusFromPool` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-randomstatusfrompool), [`StatusOnCrit` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusoncrit), [`Conditional_Enemy` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_enemy), [`PassiveIfEmptyFace` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passiveifemptyface), [`PassiveIfEmptyHead` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passiveifemptyhead), [`PassiveIfEmptyNeck` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passiveifemptyneck), [`StatusAlliesOnDeath` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusalliesondeath), [`StatusOnUseAbilityWithTag` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonuseabilitywithtag), [`AddStatusToElementAbilities` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustoelementabilities), [`AddStatusToWeapons` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustoweapons), [`Else` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-else), [`keyword_tooltips` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-keyword_tooltips), [`AddStatusToAllDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustoalldamage), [`AddStatusToBasicMeleeAttack` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustobasicmeleeattack), [`StatusOnCastSpell` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusoncastspell), [`StatusOnOverHealed` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonoverhealed), [`AddPassivesToCharmed` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addpassivestocharmed), [`AddStatusToElementDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustoelementdamage), [`AddStatusToExplosions` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustoexplosions), [`Conditional_FirstApplicationThisTurn` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_firstapplicationthisturn), [`PassiveWhenAtFullMana` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passivewhenatfullmana), [`StatusAlliesOnKill` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusalliesonkill), [`StatusIfUnusedMovePoints` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusifunusedmovepoints), [`StatusOnTurnEndIfCastNSpells` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonturnendifcastnspells), [`StatusOnTurnEndIfManaExact` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonturnendifmanaexact), [`StatusOnTurnEndIfManaOrHealthExact` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonturnendifmanaorhealthexact), [`AddSelfStatusToBasicAttack` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addselfstatustobasicattack), [`Conditional_BadRoll` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_badroll), [`Conditional_HasStatus` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_hasstatus), [`StatusEveryXSpellCasts` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuseveryxspellcasts), [`StatusGroup` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusgroup), [`StatusKilledCharacters` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuskilledcharacters), [`StatusOnAllyCatDeath` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonallycatdeath), [`StatusOnBattleStart` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonbattlestart), [`StatusOnEatFood` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusoneatfood), [`StatusOnGainCoins` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusongaincoins), [`StatusOnHealed` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonhealed), [`StatusOnKillEnemy` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonkillenemy), [`StatusOnTookDamageFromAbility` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusontookdamagefromability), [`statuses` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuses), [`AddPassivesToSummonAbilityMinions` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addpassivestosummonabilityminions), [`AddSelfStatusToWeapons` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addselfstatustoweapons), [`AddStatusToAllDamageAbilities` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustoalldamageabilities), [`AddStatusToFirstBasicAttack` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustofirstbasicattack), [`AddStatusToTrampleDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustotrampledamage), [`ApplyStatusIfCrit` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-applystatusifcrit), [`ApplyStatusesToRandomEnemiesEachTurn` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-applystatusestorandomenemieseachturn), [`ApplyToSource` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-applytosource), [`CatchProjectiles` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-catchprojectiles), [`Conditional_Adjacent` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_adjacent), [`Conditional_Boss` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_boss), [`Conditional_Corpse` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_corpse), [`Conditional_HasTag` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_hastag), [`Conditional_NotBoss` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_notboss), [`Conditional_PartyMember` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_partymember), [`Conditional_Shielded` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_shielded), [`Electric` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-electric), [`Eternal` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-eternal), [`Fire` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-fire), [`Grass` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-grass), [`Gravity` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-gravity), [`Holy` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-holy), [`HolyDamageBlessing` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-holydamageblessing), [`Ice` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-ice), [`LateBloomer` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-latebloomer), [`LightningRod` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-lightningrod), [`NextBattleStatus` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-nextbattlestatus), [`PassiveAtFullHealth` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passiveatfullhealth), [`PassiveGroup` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passivegroup), [`PassiveUntilCastSpell` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passiveuntilcastspell), [`PassiveWhileInMonkMeleeStance` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passivewhileinmonkmeleestance), [`PassiveWhileInMonkRangedStance` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passivewhileinmonkrangedstance), [`PassiveWhilePreviewingMonkRangedStance` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passivewhilepreviewingmonkrangedstance), [`ScaledStatusOnOverMana` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-scaledstatusonovermana), [`ScaledStatusOnSpendMana` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-scaledstatusonspendmana), [`SpecialFriends` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-specialfriends), [`StatusAfterCastSpell` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusaftercastspell), [`StatusAlliesOnBattleStart` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusalliesonbattlestart), [`StatusAlliesOnGainCoins` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusalliesongaincoins), [`StatusAllyWhenAllySpendsMana` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusallywhenallyspendsmana), [`StatusAnyCatAllyWhoKills` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusanycatallywhokills), [`StatusDamagers` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusdamagers), [`StatusEachTurnEndForEachTurn` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuseachturnendforeachturn), [`StatusEachTurnEndPerEnemyKill` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuseachturnendperenemykill), [`StatusEnemiesOnDeath` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusenemiesondeath), [`StatusEveryXTurnBegins` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuseveryxturnbegins), [`StatusKillers` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuskillers), [`StatusOnAnyDeath` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonanydeath), [`StatusOnBreakItem` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonbreakitem), [`StatusOnCollectPickup` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusoncollectpickup), [`StatusOnDealtDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusondealtdamage), [`StatusOnDealtDamageThreshold` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusondealtdamagethreshold), [`StatusOnEndMove` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonendmove), [`StatusOnGainShield` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusongainshield), [`StatusOnHeal` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonheal), [`StatusOnOverMana` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonovermana), [`StatusOnPickupCoins` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonpickupcoins), [`StatusOnPopCorpse` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonpopcorpse), [`StatusOnTookDamageFromEnemyAbility` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusontookdamagefromenemyability), [`StatusOnTriggerTrap` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusontriggertrap), [`StatusOnUseBasicAttack` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonusebasicattack), [`StatusOnUseElementAbility` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonuseelementability), [`StatusPerInjury` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusperinjury), [`StatusWhenAllySpendsMana` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuswhenallyspendsmana), [`TaggedPickupEffectReplacement` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-taggedpickupeffectreplacement), [`AddStatusToKnockbackDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustoknockbackdamage), [`AddStatusToSpells` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustospells), [`AddStatusesIfPersistentWeatherElement` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatusesifpersistentweatherelement), [`AddStatusesToReceivedElementalDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatusestoreceivedelementaldamage), [`Conditional_DoesDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_doesdamage), [`Conditional_GoodRoll` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_goodroll), [`Diabetes` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-diabetes), [`PassiveLevelScaledStatus` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passivelevelscaledstatus), [`RandomPassivePool` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-randompassivepool), [`ScaledStatusOnBleedDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-scaledstatusonbleeddamage), [`ScaledStatusOnLoseShield` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-scaledstatusonloseshield), [`StatusAlliesEachTurn` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusallieseachturn), [`StatusAlliesOnSpendMana` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusalliesonspendmana), [`StatusAlliesScaledByCursedOnDeath` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusalliesscaledbycursedondeath), [`StatusIfBattleAlreadyBegan` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusifbattlealreadybegan), [`StatusOnEatPill` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusoneatpill), [`StatusOnLoseShield` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonloseshield), [`StatusOnTakeHealthDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusontakehealthdamage), [`StatusOnTurnEndIfDidntCastAbilityTypes` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonturnendifdidntcastabilitytypes), [`TakeBonusTurnWithStatus` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-takebonusturnwithstatus), [`TheHunger` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-thehunger)

### Valid Property Keys

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 5118 ||
| [`class`](./Enums.md#enum-class) | Enum | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1200 ||
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 981 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 928 ||
| `int` | Enum / Integer | The Intelligence stat value or modifier. | 401 ||
| [`neck`](./Enums.md#enum-neck) | Enum | The neck equipment item assigned to the unit. | 378 ||
| `lck` | Enum / Integer | The Luck stat value or modifier. | 351 ||
| [`bonus_passives`](Abilities_and_Spells.md#object-bonus_passives) | Object | Grants temporary passive abilities to the caster for the duration of the ability. | 272 ||
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | Contains status effects to add to the basic attack. | 178 ||
| [`Colorless`](Engine_LogicKeys.md#object-colorless) | Object | Specifies the 'Colorless' form within FormChanger, used for boss dialogue. | 140 ||
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 140 ||
| [`move`](./Arrays.md#array-move) | Enum | Specifies the name of the class's default movement ability. | 122 ||
| [`FormChanger`](Characters_and_Bosses.md#object-formchanger) | Object | Defines the unit's form-changing data, including multiple form definitions and their sub-properties. | 106 ||
| [`SpawnOnDeath`](Characters_and_Bosses.md#object-spawnondeath) | Enum / Object | Specifies an object and its faction to spawn when the unit dies. | 81 ||
| `IgnoreSelf` | Boolean / Integer | If set to 1 or true, the damage instance ignores the source unit (does not affect itself). | 75 ||
| [`Tinkerer`](Engine_LogicKeys.md#object-tinkerer) | Object | Form identifier for the Tinkerer boss type. | 70 ||
| [`Hunter`](Engine_LogicKeys.md#object-hunter) | Object | Defines a list of quotes for the Hunter class (vs boss, embark, return early). | 68 ||
| [`Fear`](./Arrays.md#array-fear) | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 59 ||
| [`Medic`](Engine_LogicKeys.md#object-medic) | Object | Defines a list of quotes for the Medic class. | 58 ||
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 54 ||
| [`RandomArmorPickup`](Engine_LogicKeys.md#object-randomarmorpickup) | Number / Object | The amount of random armor pickups spawned. | 43 ||
| [`BasicMelee`](#object-basicmelee) | Object | An object defining properties for a basic melee attack passive. | 42 ||
| [`StatusImmunity`](./Enums.md#enum-statusimmunity) | Array / Enum | A list of status effect names the unit is immune to. | 38 ||
| [`Wood`](#object-wood) | Variable | A variable representing the Wood element or material type. | 38 ||
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 36 ||
| `HealthGain` | Integer | The amount of health restored to the source. | 36 ||
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 36 ||
| [`FormChangeWhileHasStatus`](Characters_and_Bosses.md#object-formchangewhilehasstatus) | Object | Defines a form change condition that activates while the unit has a specific status effect. | 35 ||
| [`StatusOnTookDamage`](Cat_Mutations.md#object-statusontookdamage) | Object | Specifies status effects or actions triggered when the unit takes damage. | 34 ||
| [`AddElementsToBasicAttack`](./Enums.md#enum-addelementstobasicattack) | Enum | Specifies an elemental damage type that is added to the unit's basic attacks. | 32 ||
| [`Jester`](./Arrays.md#array-jester) | Array | An array of dialogue quotes for the Jester class. | 32 ||
| [`MulticlassLevelUp`](./Enums.md#enum-multiclasslevelup) | Enum | Specifies the class that this unit gains a level in when multiclassing. | 32 ||
| [`AddPassivesToMinions`](Items_and_Equipment.md#object-addpassivestominions) | Object | An object containing passives that are granted to all minions spawned by the unit. | 30 ||
| `Charge` | Integer | The number of charge stacks applied. | 30 ||
| `DodgeChance` | Integer | The percentage chance the unit has to dodge incoming attacks. | 30 ||
| [`EliteTint`](./Arrays.md#array-elitetint) | Array | An RGBA tint color (r g b a) applied to elite variants of a unit. | 30 ||
| [`RevengeDamage`](Abilities_and_Spells.md#object-revengedamage) | Object | An object defining the damage and effects that trigger when the unit is attacked. | 30 ||
| `AddCritMultiplier` | Integer | The percentage added to the critical hit damage multiplier. | 28 ||
| [`TransformAbility`](./Enums.md#enum-transformability) | Enum | Specifies the ability that replaces the current ability. | 28 ||
| `knockback` | Enum / Integer | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 27 ||
| `AddBonusRange` | Integer | The number of additional tiles of range added to the unit's abilities. | 26 ||
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 ||
| [`ImmediateAbilityReaction`](Characters_and_Bosses.md#object-immediateabilityreaction) | Array / Enum / Object | Specifies an ability or list of abilities used immediately in reaction to a triggering event. | 26 ||
| `Knockback` | Integer | The number of tiles the target is pushed away from the source on hit. | 26 ||
| [`Paper`](#object-paper) | Variable | A variable representing the Paper element or material type. | 26 ||
| `even_if_dead` | Boolean | If true, the effect triggers even if the unit is dead. | 25 ||
| `Undead` | Integer | If set, flags the unit as undead (e.g., 1) with associated mechanics. | 25 ||
| `Brittle` | Integer | The number of stacks of the Brittle status, or an object defining its properties. | 24 ||
| `MissChance` | Integer | The flat percentage chance that the unit's attacks will miss. | 24 ||
| [`party_status_next_fight`](Events_and_Encounters.md#object-party_status_next_fight) | Object | An object defining status effects to apply to the party at the start of the next fight. | 24 ||
| [`PassiveWhenAffectedByElement`](Cat_Mutations.md#object-passivewhenaffectedbyelement) | Object | An object containing `element` and `passives` that grants the listed passives while the unit is affected by the specified element. | 24 ||
| [`SpawnOnBattleStart`](Elite_Buffs.md#object-spawnonbattlestart) | Enum / Object | Specifies the object that spawns adjacent to the unit at the start of battle. | 24 ||
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 23 ||
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 22 ||
| [`mode`](./Enums.md#enum-mode) | Enum | Specifies the comparison mode (equal, greater, less_or_equal, etc.) used for a conditional check. | 22 ||
| [`StatusOnBreak`](Items_and_Equipment.md#object-statusonbreak) | Object | An object defining statuses or effects applied when an item or object breaks. | 22 ||
| [`threshold`](Items_and_Equipment.md#object-threshold) | Enum / Integer / Object | The health threshold value, either as a formula using X (max health) or a fixed integer. | 22 ||
| [`additional_passives`](Abilities_and_Spells.md#object-additional_passives) | Object | Additional passive abilities applied to the spawned unit. | 20 ||
| [`BossRewards`](Characters_and_Bosses.md#object-bossrewards) | Object | Defines the common and rare item rewards dropped by a boss on defeat. | 20 ||
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 20 ||
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. | 20 ||
| [`MeleeRevengeDamage`](Abilities_and_Spells.md#object-meleerevengedamage) | Object | Defines the damage and effects applied back to a melee attacker upon being hit. | 20 ||
| [`EliteParticle`](./Enums.md#enum-eliteparticle) | Enum | Specifies the particle effect name attached to an elite unit. | 19 ||
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Specifies the loot pool from which to find an item, with an optional chance. | 19 ||
| [`BirdRewards`](Characters_and_Bosses.md#object-birdrewards) | Object | Defines the rewards and statuses applied when a bird allies with the unit. | 18 ||
| [`Buddy`](Characters_and_Bosses.md#object-buddy) | Enum / Object | Specifies a buddy unit that accompanies or is spawned alongside the unit, with optional reclaim and targeting properties. | 18 ||
| [`Coin`](Engine_LogicKeys.md#object-coin) | Integer / Object | The number of coin pickups spawned. | 18 ||
| [`Consumed`](Abilities_and_Spells.md#object-consumed) | Object | An object configuring how the target is consumed (e.g., via swallow), with fields like `instant`, `wet`, `force_contact`, and `struggle_ability`. | 18 ||
| [`SpawnThingOnDamage`](Cat_Mutations.md#object-spawnthingondamage) | Object | Specifies an object that spawns on the tile when the unit takes damage. | 18 ||
| [`StatusOnKill`](Cat_Mutations.md#object-statusonkill) | Object | Specifies status effects or actions triggered when the unit kills an enemy. | 18 ||
| [`AbilityOnBattleStart_Immediate`](./Enums.md#enum-abilityonbattlestart_immediate) | Enum | Specifies the ability triggered instantly at the start of battle. | 17 ||
| `CollectsPickups` | Integer | If set to 1 or greater, the unit collects pickups (e.g., items) on contact. | 17 ||
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 17 ||
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 17 ||
| [`OverrideKnockbackDamage`](./Enums.md#enum-overrideknockbackdamage) | Enum / Integer | A formula or flat value that sets the damage dealt when knockback occurs, overriding default calculations. | 17 ||
| [`RandomMagicMissile`](Abilities_and_Spells.md#object-randommagicmissile) | Integer / Object | The number of random magic missiles fired, or an object defining its properties. | 17 ||
| `rat` | Variable | A variable representing the Rat element or material type. | 17 ||
| [`AddStatusToBasicMeleeAttack`](Cat_Mutations.md#object-addstatustobasicmeleeattack) | Object | An object listing status effects applied by the unit's basic melee attack. | 16 ||
| [`CharacterLightSource`](Characters_and_Bosses.md#object-characterlightsource) | Object | Defines a dynamic light source attached to the unit, including color, glow, and size. | 16 ||
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 16 ||
| [`HealthPickup`](Characters_and_Bosses.md#object-healthpickup) | Object | Defines properties for a health pickup object, such as healing amount and visual frame range. | 16 ||
| `less_or_equal` | Variable | A variable representing a comparison mode for threshold checks (less than or equal). | 16 ||
| `PassiveLevelUpAtCombatEnd` | Integer | The number of times a passive levels up automatically when combat ends. | 16 ||
| [`pyrophina`](#object-pyrophina) | Variable | A variable representing the Pyrophina element or material type. | 16 ||
| [`StatusEachTurnBegin`](Cat_Mutations.md#object-statuseachturnbegin) | Object | Specifies status effects applied to the unit at the start of each of its turns. | 16 ||
| [`StatusEachTurnEnd`](Cat_Mutations.md#object-statuseachturnend) | Object | Specifies status effects applied to the unit at the end of each of its turns. | 16 ||
| [`zaratana`](#object-zaratana) | Variable | A variable representing the Zaratana element or material type. | 16 ||
| [`ApplyToSourceOnKill`](Abilities_and_Spells.md#object-applytosourceonkill) | Object | Contains effects that are applied to the source when it kills the target. | 15 ||
| [`CanApplyToInanimate`](Abilities_and_Spells.md#object-canapplytoinanimate) | Object | An object containing effects that can be applied to inanimate objects. | 15 ||
| `HealthMultiplier` | Float | A multiplier applied to the unit's base health. | 15 ||
| [`Maggot`](#object-maggot) | Object | An object defining properties for the Maggot passive or status. | 15 ||
| [`ReplaceSpawnedObjects`](./Arrays.md#array-replacespawnedobjects) | Array | An array of [original_object replacement_object] pairs for swapping spawned objects. | 15 ||
| [`ChangeCatClass`](./Enums.md#enum-changecatclass) | Enum | Specifies the new class to assign to the unit. | 14 ||
| `EndTurn` | Integer | If set to 1, ends the current unit's turn immediately after this effect. | 14 ||
| `meat` | Variable | A variable representing the Meat element or material type. | 14 ||
| [`PassiveGroup`](Characters_and_Bosses.md#object-passivegroup) | Object | A group of passive abilities that can be randomly assigned. | 14 ||
| [`SpawnOnDowned`](./Enums.md#enum-spawnondowned) | Enum | Specifies the character or object spawned when the unit is downed. | 14 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 14 ||
| [`statuses`](Characters_and_Bosses.md#object-statuses) | Object | Defines the status effects applied when the parent trigger event occurs. | 14 ||
| [`Trample`](./Arrays.md#array-trample) | Integer | The amount of bonus damage dealt when moving through an enemy. | 14 ||
| [`TransformBasicAttack`](./Enums.md#enum-transformbasicattack) | Enum | Specifies the ability that replaces the unit's basic attack. | 14 ||
| [`ApplyPassives`](Abilities_and_Spells.md#object-applypassives) | Object | Specifies the passives or status effects to apply to the unit. | 13 ||
| [`DeathRattleRevive`](Characters_and_Bosses.md#object-deathrattlerevive) | Enum / Object | Specifies an ability or effect that revives the unit upon death, with options for stunning behavior. | 13 ||
| `Flammable` | Integer | The number of stacks of Flammable, or an object defining its properties. | 13 ||
| `SafeDoomed` | Enum / Integer | The number of SafeDoomed stacks applied, or 'level' to scale with character level. | 13 ||
| [`TransformOnDeath`](./Enums.md#enum-transformondeath) | Array / Enum | Specifies the unit or list of units to transform into upon death. | 13 ||
| `AddBonusMeleeRange` | Integer | The number of additional tiles of range added to the unit's melee attacks. | 12 ||
| `AddCorpseHealth` | Integer | The amount of bonus health the unit's corpse has before it can be resurrected. | 12 ||
| `AddMaxHealth` | Integer | The amount added to the unit's maximum health. Negative values reduce max health. | 12 ||
| [`Bionic`](#object-bionic) | Variable | A variable representing the Bionic element or material type. | 12 ||
| [`BonusAbility`](./Enums.md#enum-bonusability) | Enum | Specifies the name of a bonus ability granted. | 12 ||
| [`CritsApplyStatus`](Items_and_Equipment.md#object-critsapplystatus) | Object | An object containing statuses applied to the target when the unit lands a critical hit. | 12 ||
| [`DeadAltAbility`](./Enums.md#enum-deadaltability) | Enum | Specifies an alternative ability used when the unit is dead. | 12 ||
| `Displace` | Integer | If set to 1, the unit is displaced to another location (e.g., teleport). | 12 ||
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 12 ||
| [`EquipTemporaryItem`](./Enums.md#enum-equiptemporaryitem) | Enum | Specifies which temporary item is equipped. | 12 ||
| `IgnoreTiles` | Integer | If set to 1, movement ignores tile-based penalties or restrictions. | 12 ||
| `NoHealthOnlyShield` | Integer | If set (e.g., 1), the unit has no health and only a shield for damage absorption. | 12 ||
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 12 ||
| [`SpawnEachTurn`](Cat_Mutations.md#object-spawneachturn) | Object | Specifies an object that spawns on a random adjacent tile each turn, with optional chance. | 12 ||
| [`ChanceToBreakFree`](Abilities_and_Spells.md#object-chancetobreakfree) | Object | Defines the chance and ability used for a grappled or restrained unit to break free. | 11 ||
| [`DoScreenShake`](Abilities_and_Spells.md#object-doscreenshake) | Integer / Object | If an integer, the number of screen shakes; if an object, defines the duration and intensity of the screen shake. | 11 ||
| [`EliteFlatTint`](./Arrays.md#array-eliteflattint) | Array | An RGB or RGBA tint multiplier applied uniformly to an elite unit's sprite. | 11 ||
| [`Food`](Engine_LogicKeys.md#object-food) | Integer / Object | The number of food pickups spawned. | 11 ||
| `PermanentMadness` | Integer | The number of permanent madness stacks applied. | 11 ||
| [`BoostWeaponDamage`](Items_and_Equipment.md#object-boostweapondamage) | Object | The amount of bonus weapon damage applied, or an object with `damage` and `crit_chance` fields. | 10 ||
| [`BrambleRandomTileEvent`](#object-bramblerandomtileevent) | Object | An object defining the BrambleRandomTileEvent ability or effect. | 10 ||
| `CoinPickup` | Integer | The amount of coins awarded when this pickup is collected. | 10 ||
| `ExtraMovePoints` | Integer | The number of additional movement points granted to this unit. | 10 ||
| `FadeInsteadOfDie` | Integer | If non-zero, the unit fades out instead of dying. | 10 ||
| [`GainCoins`](./Arrays.md#array-gaincoins) | Array / Integer | The amount of coins gained, or a [min, max] range. | 10 ||
| `KnockbackDamageImmuneUntilSettled` | Integer | If non-zero, makes the target immune to damage from knockback until they stop moving. | 10 ||
| `PartialPurge` | Integer | The amount of beneficial status effects removed from the target. | 10 ||
| [`PassiveAtStatThreshold`](Items_and_Equipment.md#object-passiveatstatthreshold) | Object | An object defining passives granted when a unit's stat meets a specified threshold. | 10 ||
| [`Quivered`](./Arrays.md#array-quivered) | Array / Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 10 ||
| `RandomPermanentStat` | Integer | The amount of a random permanent stat change (positive or negative). | 10 ||
| [`ReplaceBasicMove`](./Enums.md#enum-replacebasicmove) | Enum | Specifies an alternative movement ability that replaces the unit's default move. | 10 ||
| [`SpawnOnBattleStartRandomEmptyTile`](Cat_Mutations.md#object-spawnonbattlestartrandomemptytile) | Object | Specifies an object that spawns on a random empty tile at the start of battle. | 10 ||
| [`StatusOnCrit`](Miscellaneous.md#object-statusoncrit) | Object | An object containing statuses applied to the unit when it lands a critical hit. | 10 ||
| `StripStatuses` | Integer | If 1, removes all status effects from the unit at the beginning of its turn. | 10 ||
| `WaterWalk` | Integer | If greater than 0, allows the unit to traverse water tiles as if they were ground. | 10 ||
| `Ammo` | Integer | The amount of ammo to add or remove (negative values subtract). | 9 ||
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 ||
| `Creep` | Variable | A variable representing the Creep element or material type. | 9 ||
| `DeferVaporize` | Integer | If set to 1, the unit's vaporize (instant death) is delayed until the end of the current action. | 9 ||
| `DiminishingHealthRegen` | Integer | The number of diminishing health regen stacks applied. | 9 ||
| [`FormChangeOnElementInfluence`](Characters_and_Bosses.md#object-formchangeonelementinfluence) | Object | Defines the element that triggers a form change, optional visual effects, and the target form. | 9 ||
| `Plant` | Integer | If set to 1, marks the unit as a Plant type, granting associated immunities and interactions. | 9 ||
| `RandomMutation` | Integer | The number of random mutations to apply. | 9 ||
| [`Rot`](./Arrays.md#array-rot) | Array / Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 9 ||
| [`SmallRockBehavior`](Characters_and_Bosses.md#object-smallrockbehavior) | Integer / Object | Defines the damage, knockback, and chain properties of small rocks spawned from this unit when destroyed. | 9 ||
| `SpawnCreep` | Integer | If set to 1, spawns a creep tile under the target. | 9 ||
| `SpellDamageUp` | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 9 ||
| [`StatusCollector`](Characters_and_Bosses.md#object-statuscollector) | Object | Specifies the status effects and their stack counts that the unit collects to trigger transformations. | 9 ||
| [`TransformInXTurns`](Characters_and_Bosses.md#object-transforminxturns) | Object | Defines a delayed transformation after a set number of turns, with optional target object and initiative handling. | 9 ||
| [`TransformOnElementInfluence`](Characters_and_Bosses.md#object-transformonelementinfluence) | Object | Defines the element that triggers a transformation and the object to transform into. | 9 ||
| `AddKnockbackDamage` | Integer | The amount of additional knockback damage applied. | 8 ||
| `AddLevelUpRerolls` | Integer | The number of additional rerolls the unit gets when leveling up. | 8 ||
| [`AddStatusToWeapons`](Characters_and_Bosses.md#object-addstatustoweapons) | Object | Specifies status effects to add to the unit's weapon attacks, with their stack counts. | 8 ||
| `AlphaTurns` | Integer | The number of turns the unit acts first in battle; negative values may indicate last. | 8 ||
| [`AmplifyStatus`](./Enums.md#enum-amplifystatus) | Enum | Specifies the status effect to amplify, or an object with the status and number of stacks to add. | 8 ||
| [`BasicMagicMissile`](#object-basicmagicmissile) | Object | Directs a basic magic missile projectile at the target. | 8 ||
| [`BlacklistPickupType`](./Enums.md#enum-blacklistpickuptype) | Enum | Specifies a pickup type (e.g., food, catnip) that the unit will refuse to pick up. | 8 ||
| `BleedThorns` | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 8 ||
| [`CharmedFly`](#object-charmedfly) | Object | Transforms the unit into a charmed fly that fights for the allies faction. | 8 ||
| [`DisableAbilitiesWithTag`](./Enums.md#enum-disableabilitieswithtag) | Enum | Specifies a tag that disables any ability with that tag on the unit. | 8 ||
| `ExtraWeaponAttacks` | Integer | The number of additional weapon attacks the unit can perform. | 8 ||
| [`ForceSpecificInjury`](./Enums.md#enum-forcespecificinjury) | Enum | Forces the unit to receive an injury to the specified stat. | 8 ||
| [`FormChangeOffMap`](Characters_and_Bosses.md#object-formchangeoffmap) | Object | Specifies the unit's form when off the map and when on the map. | 8 ||
| [`Grappled`](./Arrays.md#array-grappled) | Array / Integer | The number of stacks and probability of applying the Grappled status, in format [stacks, probability] or just stacks. | 8 ||
| [`InnateElement`](./Enums.md#enum-innateelement) | Enum | Specifies the innate elemental type of the unit (e.g., Fire, Ice, Electric). | 8 ||
| `Lucky` | Enum | Indicates the unit's luck modifier or classification. | 8 ||
| [`ManaCostReductionTagged`](Miscellaneous.md#object-manacostreductiontagged) | Object | Reduces the mana cost of abilities with the specified tag by the given reduction amount. | 8 ||
| `NonStackingDivineShield` | Integer | The number of Divine Shield stacks that do not stack with duplicates. | 8 ||
| `NonStackingShield` | Integer | The amount of non-stacking shield granted. | 8 ||
| [`PassiveIfAllArmorEmpty`](Miscellaneous.md#object-passiveifallarmorempty) | Object | Grants the contained passive effects when no armor is equipped in any slot. | 8 ||
| [`PassiveIfEmptyFace`](Miscellaneous.md#object-passiveifemptyface) | Object | Grants the contained passive effects when the face armor slot is empty. | 8 ||
| [`PassiveIfEmptyHead`](Miscellaneous.md#object-passiveifemptyhead) | Object | Grants the contained passive effects when the head armor slot is empty. | 8 ||
| [`PassiveIfEmptyNeck`](Miscellaneous.md#object-passiveifemptyneck) | Object | Grants the contained passive effects when the neck armor slot is empty. | 8 ||
| [`Poison`](./Arrays.md#array-poison) | Array / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 ||
| [`RandomizeAIWeightsEachTurn`](./Arrays.md#array-randomizeaiweightseachturn) | Array | The range of random weights applied to AI actions each turn. | 8 ||
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | A collection of status effects; one is randomly chosen and applied to the target. | 8 ||
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum | Specifies the ability ID that replaces the unit's basic attack. | 8 ||
| [`StatusAlliesOnDeath`](Items_and_Equipment.md#object-statusalliesondeath) | Object | Applies the contained status effects to all allies when the unit dies. | 8 ||
| [`StatusEachRoundBegin`](Elite_Buffs.md#object-statuseachroundbegin) | Object | Applies the contained status effects at the beginning of each round. | 8 ||
| [`StatusEveryXSpellCasts`](Cat_Mutations.md#object-statuseveryxspellcasts) | Object | An object with `stacks` (number of spell casts) and status effects to apply after that many spell casts. | 8 ||
| [`StatusOnCastSpell`](Cat_Mutations.md#object-statusoncastspell) | Object | An object listing status effects applied to the unit whenever it casts a spell. | 8 ||
| [`StatusOnUseAbilityWithTag`](Miscellaneous.md#object-statusonuseabilitywithtag) | Object | Applies the contained status effects when the unit uses an ability with the specified tag. | 8 ||
| `AbilityEnabledOncePerFightAtHealthThreshold` | Integer | The health threshold (absolute or percentage) at which this ability becomes enabled once per fight. | 7 ||
| [`AbilityWhenBuddyDies`](./Enums.md#enum-abilitywhenbuddydies) | Enum | Specifies the ability to cast when a nearby allied unit dies. | 7 ||
| `BramblesOnHit` | Integer | If set to 1, spawns bramble tiles on the target's location on hit. | 7 ||
| [`BrittleDuringElement`](./Enums.md#enum-brittleduringelement) | Enum | Makes the unit brittle while in contact with the specified element. | 7 ||
| [`ChanceToSpitOnDamage`](Characters_and_Bosses.md#object-chancetospitondamage) | Object | Configures the chance to use a spit ability when taking damage, including base chance and per-damage bonus. | 7 ||
| `CharismaUp` | Enum / Integer | The amount of charisma change, or a keyword like 'item_aux'. | 7 ||
| `ContextualHeal` | Integer | The amount of healing applied contextually (e.g., to allies). | 7 ||
| [`DamageNeighborsOnEndMove`](Miscellaneous.md#object-damageneighborsonendmove) | Object | Deals damage and knockback to units on neighboring tiles when the unit finishes moving. | 7 ||
| [`DurabilityTransform`](Items_and_Equipment.md#object-durabilitytransform) | Object | Transforms the item into another when durability reaches specified thresholds. | 7 ||
| [`GainCoinsRange`](Abilities_and_Spells.md#object-gaincoinsrange) | Object | An object with `min` and `max` fields specifying a range for the amount of coins gained. | 7 ||
| [`Ice`](Engine_LogicKeys.md#object-ice) | Object | Applies the Slow status effect to targets hit by ice-element abilities. | 7 ||
| `ManaSteal` | Integer | The amount of mana stolen (negative values may drain instead). | 7 ||
| `MinimumKnockbackFromAllDamage` | Integer | The minimum knockback distance the unit will suffer from any damage source. | 7 ||
| [`OverrideBasicAttack`](./Enums.md#enum-overridebasicattack) | Enum | Replaces the unit's basic attack with the specified ability. | 7 ||
| `OverrideMaxHealth` | Integer | Replaces the unit's maximum health with this value. | 7 ||
| [`PassiveIfStrAuxEquals`](Items_and_Equipment.md#object-passiveifstrauxequals) | Object | Grants the contained passive effects when the unit's specified auxiliary stat equals the given value. | 7 ||
| [`PassiveWhenOnTile`](Items_and_Equipment.md#object-passivewhenontile) | Object | Grants the contained passive effects while the unit is standing on one of the specified tile types. | 7 ||
| [`SetFragileImmune`](./Enums.md#enum-setfragileimmune) | String | Sets the unit's material to the specified type, granting immunity to the Fragile status. | 7 ||
| [`TriggerWerewolfTransform`](./Arrays.md#array-triggerwerewolftransform) | Array / Number | The number of stacks and probability of triggering the werewolf transformation. | 7 ||
| [`Webbed`](./Arrays.md#array-webbed) | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. | 7 ||
| `XIsFreeArmorSlots` | Integer | The number of armor slots that are free (no cost) for the unit. | 7 ||
| `AbilityEnabledPercentEachTurn` | Integer | The percentage chance each turn that this ability is enabled. | 6 ||
| [`AbilityOnBattleStart`](./Enums.md#enum-abilityonbattlestart) | Enum | Casts the specified ability when the battle begins. | 6 ||
| `AddDamage` | Integer | The amount of damage added to all attacks. Negative values reduce damage. | 6 ||
| [`AddDamageToElementDamage`](Cat_Mutations.md#object-adddamagetoelementdamage) | Object | Defines additional damage of a specific element added to the unit's attacks. | 6 ||
| `AddMovement` | Integer | The amount of bonus movement points added to the unit's base movement. | 6 ||
| [`AddStatusToElementAbilities`](Miscellaneous.md#object-addstatustoelementabilities) | Object | Adds the contained status effects to all abilities with the specified element. | 6 ||
| [`AddTemporaryEffectsToBasicAttack`](Cat_Mutations.md#object-addtemporaryeffectstobasicattack) | Object | A container object that lists temporary status effects applied to the unit's basic attack. | 6 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 6 ||
| `BackstabImmunity` | Integer | If greater than 0, prevents the unit from taking extra damage from backstabs. | 6 ||
| `BasicAttackAOEBonus` | Integer | The additional area of effect radius for the basic attack. | 6 ||
| `BasicAttackDamageMultiplier` | Integer | A multiplier applied to the damage of the basic attack. | 6 ||
| [`Bird`](Passives_and_Statuses.md#object-bird) | Enum / Object | The object dropped by this bird unit upon death. | 6 ||
| `BlastResistance` | Integer | The amount of damage reduction against blast-type damage. | 6 ||
| [`BounceRock`](./Enums.md#enum-bouncerock) | Array / Enum | Specifies the rock object to bounce. | 6 ||
| [`CaveFamilyEnrage`](Characters_and_Bosses.md#object-cavefamilyenrage) | Object | Specifies the ability used when the number of family members with a given tag falls below a threshold. | 6 ||
| `ClearStarving` | Integer | The number of stacks of Starving cleared. | 6 ||
| [`Conditional_BadRoll`](Abilities_and_Spells.md#object-conditional_badroll) | Object | An object containing an `odds` value and effects that are applied when a random roll succeeds. | 6 ||
| [`CureDisease`](#object-curedisease) | Object | Attempts to cure the specified disease with the given chance. | 6 ||
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 ||
| [`DefaultMove`](#object-defaultmove) | Object | Defines the default movement ability for the unit. | 6 ||
| [`DelayedAutoRevive`](Characters_and_Bosses.md#object-delayedautorevive) | Object | Configures an automatic revival after a delay, with specified rounds and health percentage. | 6 ||
| [`Divide4OnDeath`](./Enums.md#enum-divide4ondeath) | Enum | The object that spawns in four instances upon this unit's death. | 6 ||
| [`DoDistortionRing`](Abilities_and_Spells.md#object-dodistortionring) | Object | Configuration for a distortion ring visual effect, with speed, intensity, and radius. | 6 ||
| [`Electric`](Engine_LogicKeys.md#object-electric) | Object | Applies a Stun status effect with specified stacks and probability based on variable X. | 6 ||
| `ExtraBasicAttacks` | Integer | The number of additional basic attacks the unit can perform per turn. | 6 ||
| [`Fire`](Characters_and_Bosses.md#object-fire) | Integer / Object | Defines the 'Fire' form, which may be a stack count or an object that applies burn or uses lava attack. | 6 ||
| [`FormChangeWhilePrimingAbility`](Characters_and_Bosses.md#object-formchangewhileprimingability) | Object | Defines the form changes when a specific ability is being primed and when it is not. | 6 ||
| `Fragile` | Integer | The number of stacks of the Fragile status, causing increased damage taken. | 6 ||
| `FreeFirstCast` | Integer | The number of free casts of this ability per battle. | 6 ||
| [`FreePathfindElement`](./Enums.md#enum-freepathfindelement) | Enum | Specifies a terrain element (e.g., Water, Grass) that the unit can pathfind through without penalty. | 6 ||
| [`Hyde`](#object-hyde) | Object | Defines the properties of the Hyde transformation effect. | 6 ||
| [`ItemAuxTransform`](Items_and_Equipment.md#object-itemauxtransform) | Object | Transforms the item into another when its auxiliary value reaches specified thresholds. | 6 ||
| `KaijuKnockbackImmune` | Integer | If 1, the unit is immune to knockback from kaiju sources. | 6 ||
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 6 ||
| `KnockbackImmunity` | Integer | If set to 1, the unit cannot be knocked back. | 6 ||
| [`MoveQuivered`](./Arrays.md#array-movequivered) | Integer | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 6 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 6 ||
| [`PassiveWhenAtFullMana`](Cat_Mutations.md#object-passivewhenatfullmana) | Object | An object listing passive effects that are active only while the unit's mana is full. | 6 ||
| `PermanentConstitution` | Integer | The amount of permanent Constitution stat added or removed. | 6 ||
| `PoisonThorns` | Integer | The number of stacks of Poison applied to melee attackers when they hit this unit. | 6 ||
| [`ReplaceBasicAttackWhenCastable`](./Enums.md#enum-replacebasicattackwhencastable) | Enum | Replaces the basic attack with the specified ability when that ability can be cast. | 6 ||
| [`ReplaceBasicMove_Mutation`](./Enums.md#enum-replacebasicmove_mutation) | Enum | Replaces the unit's basic movement with the specified mutation-based move. | 6 ||
| [`ScatterCoins`](Abilities_and_Spells.md#object-scattercoins) | Object | The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula. | 6 ||
| [`ScatterHeldCoin`](./Arrays.md#array-scatterheldcoin) | Array / Integer | The number of coins scattered, with an optional probability as a second element. | 6 ||
| [`SetBrittleImmune`](./Enums.md#enum-setbrittleimmune) | String | Sets the unit's material to the specified type, granting immunity to the Brittle status. | 6 ||
| `SetDistanceDisplace` | Integer | The fixed distance to displace the target. | 6 ||
| `ShowHiddenThings` | Integer | If nonzero, reveals hidden objects or tiles on the map. | 6 ||
| [`StatusIfUnusedMovePoints`](Cat_Mutations.md#object-statusifunusedmovepoints) | Object | Specifies status effects applied if the unit ends its turn with unused movement points. | 6 ||
| [`StatusKilledCharacters`](Cat_Mutations.md#object-statuskilledcharacters) | Object | An object listing status effects applied to the unit when it kills a character. | 6 ||
| [`StatusOnBattleEnd`](Abilities_and_Spells.md#object-statusonbattleend) | Object | An object containing status effects or passives applied to the unit when the battle ends. | 6 ||
| [`StatusOnEndMove`](Cat_Mutations.md#object-statusonendmove) | Object | Specifies status effects or actions triggered when the unit finishes moving. | 6 ||
| [`StatusOnStanceSwitch`](Miscellaneous.md#object-statusonstanceswitch) | Object | Applies the contained status effects when the unit changes stances. | 6 ||
| [`StatusOnTookDamageFromAbility`](Cat_Mutations.md#object-statusontookdamagefromability) | Object | Specifies status effects triggered when the unit takes damage specifically from an ability (not environmental). | 6 ||
| [`StunImmunity`](Characters_and_Bosses.md#object-stunimmunity) | Integer / Object | If 1, the unit is immune to stun. The optional object configures whether to cleanse stun on apply. | 6 ||
| [`TagGreed`](./Enums.md#enum-taggreed) | Enum | The tag of items that this unit will move towards to collect. | 6 ||
| [`TeamCastAbility`](Abilities_and_Spells.md#object-teamcastability) | Enum / Object | Specifies the ability name for the team to cast, with optional tag restriction and same orientation. | 6 ||
| [`TwisterDisplaceWithDamage`](Abilities_and_Spells.md#object-twisterdisplacewithdamage) | Object | Configuration for a twister displacement that deals damage, with min/max distance and damage value. | 6 ||
| [`YOffset`](./Enums.md#enum-yoffset) | Float | The vertical offset applied to the unit's visual position, used for floating or hovering effects. | 6 ||
| `ally_chance` | Integer | The percentage chance for an ally to catch incoming projectiles. | 5 ||
| `Angel` | Integer | If 1, the unit is an angel type, which may affect behavior like reviving. | 5 ||
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum | The tile type to change the ground tiles under the target to. | 5 ||
| [`CollectsPickupsWithAltEffects`](Abilities_and_Spells.md#object-collectspickupswithalteffects) | Object | Contains alternative effects that are applied when collecting pickups. | 5 ||
| `DamageOrHealConditionally` | Integer | The amount of conditional damage or healing applied, based on certain conditions (e.g., ally or enemy). | 5 ||
| `fetus` | Variable | A variable used in status effect calculations; specific usage depends on context. | 5 ||
| [`FlySwarm`](#object-flyswarm) | Object | Summons a fly swarm with the given chance or intensity percentage. | 5 ||
| [`FlySwarm`](#object-flyswarm) | Object | Summons a fly swarm with the given chance or intensity percentage. | 5 | `50` (Number), `{ ... }` (Object) |
| `HeadArmorPassiveMultiplierBonus` | Integer | A multiplier bonus applied to passive effects granted by head armor. | 5 ||
| `HitExplosion` | Integer | The radius of the explosion triggered on hit. | 5 ||
| `KnockbackDirectionIsFacingDirection` | Enum / Integer | Specifies how to alter knockback direction relative to the unit's facing: 1 (same), flip (opposite), rotate_right. | 5 ||
| `MonkStanceSwitch` | Integer | The number of times to switch monk stance. | 5 ||
| [`MoveTowardsKillers`](Characters_and_Bosses.md#object-movetowardskillers) | Enum / Object | Determines the movement behavior when moving towards units that have killed an ally. | 5 ||
| `NoHealthRegen` | Number | Prevents the unit from regenerating health normally. | 5 ||
| [`ObjectOnHit`](Abilities_and_Spells.md#object-objectonhit) | Enum / Object | Specifies the object to spawn on the hit tile. | 5 ||
| [`ObjectOnHitEmpty`](./Enums.md#enum-objectonhitempty) | Enum | Specifies the object to spawn on hitting an empty cell. | 5 ||
| `RefreshMovePointsIfHit` | Integer | The amount of movement points restored on hit. | 5 ||
| `RepairTrinket` | Integer | The number of stacks of the Repair Trinket status effect to apply. | 5 ||
| `SharkySmellsBlood` | Integer | If 1, the unit is attracted to damaged units and may prioritize them. | 5 ||
| [`SpawnCoinAnywhere`](./Arrays.md#array-spawncoinanywhere) | Array / Integer | The number of coins to spawn. If an array, the second value is the probability of spawning them anywhere. | 5 ||
| [`SpawnRock`](./Arrays.md#array-spawnrock) | Array / Integer | The number of rocks to spawn, or an array with stacks and probability. | 5 ||
| `StartOffMap` | Integer | If 1, the unit begins the encounter off the map. | 5 ||
| [`StatusGroup`](Abilities_and_Spells.md#object-statusgroup) | Object | A container grouping multiple status effects to be applied simultaneously. | 5 ||
| [`StatusOnTurnEndIfDidntCastAbilityTypes`](Items_and_Equipment.md#object-statusonturnendifdidntcastabilitytypes) | Object | Applies the contained status effects at turn end if the unit did not cast an ability of the specified type(s). | 5 ||
| [`Tangled`](Abilities_and_Spells.md#object-tangled) | Array / Integer / Object | The number of stacks of the Tangled status effect applied, or an object defining its properties such as `stacks` and `alt_art`. | 5 ||
| [`TransformItemOnElementInfluence`](Items_and_Equipment.md#object-transformitemonelementinfluence) | Object | Transforms the item into the specified one when influenced by the given element, optionally fully repairing it. | 5 ||
| [`TransformOnDeathImmediately`](Characters_and_Bosses.md#object-transformondeathimmediately) | Enum / Object | The object to transform into immediately upon death, with optional turn handling. | 5 ||
| `UpgradeRandomAbility` | Integer | The number of random abilities upgraded upon effect. | 5 ||
| [`water`](Characters_and_Bosses.md#object-water) | Variable | A variable representing water element intensity or presence. | 5 ||
| [`Water`](Characters_and_Bosses.md#object-water) | Object | Form state for water element, applying a puddle or movement bonus. | 5 ||
| [`XIsLivingAlliesWithTag`](./Enums.md#enum-xislivingallieswithtag) | Enum | Specifies the tag that living allies must have for this passive to affect them. | 5 ||
| [`AbilityAfterEnemyCastSpell_Stackable`](./Enums.md#enum-abilityafterenemycastspell_stackable) | Enum | The ability to cast after an enemy spell, which can stack in effect. | 4 |  |
| [`AbilityReaction`](Characters_and_Bosses.md#object-abilityreaction) | Enum / Object | Specifies the ability used as a reaction when the unit is targeted by an ability. | 4 ||
| [`AbilityWhenTaggedCharacterMovesNear`](Cat_Mutations.md#object-abilitywhentaggedcharactermovesnear) | Object | An object containing `ability`, `tag`, and `range` that triggers the specified ability when a character with the given tag moves within range. | 4 ||
| `AddDamageToBasicAttack` | String | Additional damage added to the basic attack, either as a flat value or formula. | 4 ||
| `AddManaRegen` | Integer | The flat amount of mana regenerated per turn. | 4 ||
| `AddMeleeKnockback` | Integer | The amount of additional knockback dealt by melee attacks. | 4 ||
| [`AddPassivesToCharmed`](Items_and_Equipment.md#object-addpassivestocharmed) | Object | Grants the contained passive effects to units under the charm status. | 4 ||
| [`AddSelfStatusToBasicAttack`](Items_and_Equipment.md#object-addselfstatustobasicattack) | Object | Applies the contained status effects to the unit when it uses its basic attack. | 4 ||
| `AddSpeed` | Integer | The amount of speed added (or subtracted) to the unit. | 4 ||
| [`AddStatusToAllDamage`](Items_and_Equipment.md#object-addstatustoalldamage) | Object | Adds the contained status effects to all damage dealt by the unit. | 4 ||
| [`AddStatusToAllDamageAbilities`](Miscellaneous.md#object-addstatustoalldamageabilities) | Object | Adds the contained status effects to all damaging abilities (spells and attacks). | 4 ||
| [`AddStatusToElementDamage`](Items_and_Equipment.md#object-addstatustoelementdamage) | Object | An object that applies a specific status effect when dealing damage of a specified element. Contains sub-keys for the element and the status to apply. | 4 ||
| `AllyDamageReduction` | Integer | The amount by which damage dealt to allies is reduced. | 4 ||
| [`AllyManaRegenAura`](Miscellaneous.md#object-allymanaregenaura) | Object | An object granting a mana regeneration aura to allies, with sub-keys for stacks and range. | 4 ||
| `AmplifyKnockback` | Integer | The additional distance (in tiles) a unit is knocked back. | 4 ||
| `any` | Variable | A wildcard key that matches any property name, often used for generic or dynamic lookups. | 4 ||
| `AOEPuddle` | Enum | Specifies the pattern or shape of an area-of-effect puddle left on the ground. | 4 | `X-1` (Enum) |
| [`ApplyToConsumed`](Abilities_and_Spells.md#object-applytoconsumed) | Object | Container for effects that are applied to the consumed object. | 4 ||
| [`ArcLightning`](Abilities_and_Spells.md#object-arclightning) | Object | Configuration for arc lightning chain, with stacks, chance, max distance, and enemy-only flag. | 4 ||
| [`AutocastEachRound`](Abilities_and_Spells.md#object-autocasteachround) | Enum / Object | Contains an ability name and optional 'even_if_stunned' flag to autocast each round. | 4 ||
| `BackstabAllDirections` | Integer | If 1, the unit deals backstab damage from all directions. | 4 ||
| [`BaitAura`](Characters_and_Bosses.md#object-baitaura) | Object | The range of the bait aura that draws enemies towards the unit. | 4 ||
| [`BasicStraightShot`](#object-basicstraightshot) | Object | An object defining a basic attack that fires a projectile in a straight line. | 4 ||
| [`BasicTankMelee`](#object-basictankmelee) | Object | An object defining a basic melee attack for a tank-type unit. | 4 ||
| [`BeefyCharmedLeech`](#object-beefycharmedleech) | Object | An object defining a variant of the Maggot familiar, specifically a charmed, larger leech. | 4 ||
| `BreakAtAux` | Integer | The number of auxiliary item uses before this item breaks. | 4 ||
| [`BuffImmunity`](Items_and_Equipment.md#object-buffimmunity) | Integer / Object | If 1, the unit is immune to buffs. An optional object can list buffs to exclude from immunity. | 4 ||
| `bug` | Variable | A variable key likely indicating a known issue or placeholder value. | 4 ||
| `CatchBoomerang` | Integer | If set, allows the ability to catch a boomerang, with the integer representing the number of catches. | 4 ||
| [`ChanceToBackflip`](Cat_Mutations.md#object-chancetobackflip) | Object | An object specifying the ability to use and the percentage chance to perform a backflip dodge when hit. | 4 ||
| [`ChangeTileOnPop`](./Enums.md#enum-changetileonpop) | Enum | The type of tile that appears when this unit is destroyed. | 4 ||
| [`CharmedTinySpider`](#object-charmedtinyspider) | Object | An object defining a charmed variant of the TinySpider familiar. | 4 ||
| [`ClassManaCostReduction`](Cat_Mutations.md#object-classmanacostreduction) | Object | Defines a reduction in mana cost for abilities of a specific class. | 4 ||
| [`CobraReflex`](./Enums.md#enum-cobrareflex) | Enum | Specifies which basic attack or ability grants increased dodge or counterattack chance. | 4 ||
| [`Conditional_PartyMember`](Engine_LogicKeys.md#conditional_partymember) | Object | A conditional block that executes its child actions only if the target is a party member. | 4 ||
| `ConsumablesInfiniteRange` | Integer | If non-zero, consumable items can be used at any range without distance restrictions. | 4 ||
| `CopyBasicAttackEffects` | Integer | If set, the ability copies the effects from the unit's basic attack. | 4 ||
| `CountAsCorpse` | Integer | If 1, the unit counts as a corpse for interactions like raising or necromancy. | 4 ||
| [`CounterAttack`](Cat_Mutations.md#object-counterattack) | Array / Enum / Object | Specifies the ability used when the unit counterattacks after being hit. | 4 ||
| `CreepTile` | Variable | A variable key referencing a tile type that applies a creep or detrimental effect. | 4 ||
| `crow` | Variable | A variable key likely representing a unit or effect related to the crow faction. | 4 ||
| [`DisableAbilities`](./Enums.md#enum-disableabilities) | Enum | Specifies which category of abilities to disable, such as 'all_items' or 'basic_attack'. | 4 ||
| [`DisplayDangerAOE`](./Enums.md#enum-displaydangeraoe) | Enum | The ability whose area of effect is displayed to warn players. | 4 ||
| [`DistanceBonusDamage`](#object-distancebonusdamage) | Object | An object that adds bonus damage based on the distance from the target, with sub-keys for stacks and minimum range. | 4 ||
| [`DownRankAIIfWeaponUsable`](./Enums.md#enum-downrankaiifweaponusable) | Float | A multiplier that reduces the AI's priority to use this ability if the unit has a usable weapon. | 4 ||
| [`ElementalManaCostReduction`](Items_and_Equipment.md#object-elementalmanacostreduction) | Object | An object that reduces the mana cost of spells of specified elements, with sub-keys for element and reduction amount. | 4 ||
| [`EnableWeather`](./Enums.md#enum-enableweather) | Enum | Specifies the weather effect to enable. | 4 ||
| `equal` | Variable | A variable key used in conditional comparisons to check equality. | 4 ||
| [`EquipRandomTemporaryItemFromPool`](./Enums.md#enum-equiprandomtemporaryitemfrompool) | Enum | Specifies the item pool (e.g., 'pills' or 'weapons') from which a random temporary item is equipped. | 4 ||
| `ExplosionIfHitSomething` | Integer | The radius of explosion triggered if the attack hits an entity. | 4 ||
| [`extra_statuses`](Abilities_and_Spells.md#object-extra_statuses) | Object | An object containing additional status effects (with stack counts) applied to the consumed unit. | 4 ||
| `ExtraDispersedTurns` | Integer | The number of additional or fewer turns in the dispersed turn order. | 4 ||
| `FaceArmorPassiveMultiplierBonus` | Integer | A multiplier bonus applied to the effects of face armor passives. | 4 ||
| [`FactionUprising`](./Enums.md#enum-factionuprising) | Enum | Specifies which faction triggers a global uprising event, adding allied units of that faction. | 4 ||
| `Fights` | Number | The number of fights this status or effect persists for. | 4 ||
| [`FragileDuringElement`](./Enums.md#enum-fragileduringelement) | Enum | Specifies an element during which the unit becomes fragile, taking increased damage. | 4 ||
| `FreezePiercing` | Integer | The number of stacks of freeze resistance that are ignored when applying freeze. | 4 ||
| `GrassTile` | Number | The numerical identifier for a grass-type tile. | 4 ||
| [`GroundFlopper`](./Enums.md#enum-groundflopper) | Enum | The movement ability used when this unit is on the ground. | 4 ||
| `HouseFoodRequirementMultiplier` | Integer | A multiplier for the amount of food the house requires; 0 removes the food requirement. | 4 ||
| `IncreaseExplosionDamage` | Integer | The flat amount by which explosion damage is increased. | 4 ||
| [`LateStatusApplication`](Abilities_and_Spells.md#object-latestatusapplication) | Object | Container for status effects that are applied late after the main effect. | 4 ||
| [`LevelUpClassOverride`](./Enums.md#enum-levelupclassoverride) | Enum | Specifies which class the unit gains upon leveling up, overriding the default class. | 4 ||
| [`LoopingSoundWhileAlive`](./Enums.md#enum-loopingsoundwhilealive) | Enum | The looping sound effect played while the unit is alive. | 4 ||
| [`LowerAmbientLight`](Abilities_and_Spells.md#object-lowerambientlight) | Object | If an object, defines the target light amount and transition speed; if a number, sets the ambient light level directly. | 4 ||
| [`LowerAmbientLight`](Abilities_and_Spells.md#object-lowerambientlight) | Object | If an object, defines the target light amount and transition speed; if a number, sets the ambient light level directly. | 4 ||
| `ManaCostReduction` | Integer | The amount or percentage by which ability mana costs are reduced for this unit. | 4 ||
| [`Metronome`](Abilities_and_Spells.md#object-metronome) | Integer / Object | The number of times Metronome triggers, or an object with stacks and banned abilities. | 4 ||
| [`Metronome`](Abilities_and_Spells.md#object-metronome) | Boolean (Flag) / Number / Object | The number of times Metronome triggers, or an object with stacks and banned abilities. | 4 | `(Flag)` (Boolean (Flag)), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `musical` | Variable | A variable key likely related to musical abilities or sound effects. | 4 ||
| `PartialCleanse` | Integer | The number of stacks of temporary status effects to remove from the target. | 4 ||
| [`PassiveAtHealthThreshold`](Items_and_Equipment.md#object-passiveathealththreshold) | Object | An object that grants additional passives when the unit's health meets a specified threshold, with sub-keys for threshold, mode, and passives. | 4 ||
| [`PassiveWhenDead`](Characters_and_Bosses.md#object-passivewhendead) | Object | Passive effects that remain active while the unit is dead. | 4 ||
| `PermanentIntelligence` | Integer | The permanent amount of intelligence added or removed. | 4 ||
| [`PoopWhenHit`](Items_and_Equipment.md#object-poopwhenhit) | Object | Specifies the object (e.g., Poop) spawned when the unit is hit, or an object with `chance` and `object`. | 4 ||
| `PrioritizeFarAwayTargets` | Integer | The weight for AI to prioritize targets based on distance; higher values favor farther targets. | 4 ||
| [`RandomPassivePool`](Characters_and_Bosses.md#object-randompassivepool) | Object | A pool of random passives from which one is chosen for this unit. | 4 ||
| [`RandomSeededStatModifier`](./Arrays.md#array-randomseededstatmodifier) | Array | An array defining a random, seeded modifier to stats, typically in the format [modifier, offset]. | 4 ||
| [`ReflectProjectiles`](Characters_and_Bosses.md#object-reflectprojectiles) | Integer / Object | The percentage chance to reflect projectiles back at the attacker; optionally includes self-damage. | 4 ||
| `RemoveActPoints` | Integer | The number of action points removed from the target. | 4 ||
| [`RepairWeapon`](./Arrays.md#array-repairweapon) | Array / Integer | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 4 ||
| [`ReplaceSpell`](Abilities_and_Spells.md#object-replacespell) | Object | Defines which spell slot to replace and with which ability. | 4 ||
| `SendRock` | Integer | The number of rocks to send as projectiles. | 4 ||
| [`SizeScale`](./Enums.md#enum-sizescale) | Number | The multiplier applied to the unit's visual and hitbox size. | 4 ||
| [`SmartMetronome`](Abilities_and_Spells.md#object-smartmetronome) | Integer / Object | The number of stacks of a buff that increases damage by a percentage, with an optional upgrade flag. | 4 ||
| [`SmartMetronome`](Abilities_and_Spells.md#object-smartmetronome) | Integer / Object | The number of stacks of a buff that increases damage by a percentage, with an optional upgrade flag. | 4 | `20` (Number), `{ ... }` (Object) |
| [`SpawnCatCopyOnBattleStart`](Miscellaneous.md#object-spawncatcopyonbattlestart) | Object | An object that spawns a copy of the unit's cat at the start of battle, with sub-keys for the copy object and chain-prevention tag. | 4 ||
| [`SpawnThingOnDeath`](./Enums.md#enum-spawnthingondeath) | Enum | Specifies the name of an object to spawn upon death. | 4 ||
| [`StatusOnAllyCatDeath`](Cat_Mutations.md#object-statusonallycatdeath) | Object | An object listing status effects applied to the unit when an allied cat dies. | 4 ||
| [`StatusOnEatFood`](Cat_Mutations.md#object-statusoneatfood) | Object | An object listing status effects applied to the unit when it eats food. | 4 ||
| [`StatusOnGainCoins`](Characters_and_Bosses.md#object-statusongaincoins) | Object | Specifies status effects applied when this unit gains coins. | 4 ||
| [`StatusOnHealed`](Items_and_Equipment.md#object-statusonhealed) | Object | An object that applies a status effect to the unit whenever it is healed. | 4 ||
| [`StatusOnOverHealed`](Miscellaneous.md#object-statusonoverhealed) | Object | An object that applies a status effect to the unit whenever it receives overhealing (healing beyond max health). | 4 ||
| [`StatusOnTakeHealthOrShieldDamage`](Items_and_Equipment.md#object-statusontakehealthorshielddamage) | Object | An object that applies a status effect when the unit takes damage to either health or shields. | 4 ||
| [`StatusOnTurnEndIfCastNSpells`](Miscellaneous.md#object-statusonturnendifcastnspells) | Object | An object that applies a status effect at the end of the turn if the unit has cast a specified number of spells. | 4 ||
| [`StatusOnTurnEndIfManaExact`](Miscellaneous.md#object-statusonturnendifmanaexact) | Object | An object that applies a status effect at the end of the turn if the unit's mana is exactly a specified value. | 4 ||
| [`StatusOnTurnEndIfManaOrHealthExact`](Miscellaneous.md#object-statusonturnendifmanaorhealthexact) | Object | An object that applies a status effect at the end of the turn if the unit's mana or health is exactly a specified value. | 4 ||
| [`StatusRandomEnemiesOnBattleStart`](Events_and_Encounters.md#object-statusrandomenemiesonbattlestart) | Object | An object that applies a status effect to a random number of enemies at the start of battle, with sub-keys for count and the status. | 4 ||
| [`SwitchMusic`](Abilities_and_Spells.md#object-switchmusic) | Object | Defines a new song or layer for the background music. | 4 ||
| `TauntAlways` | Integer | If non-zero, the unit is always taunted, forcing it to target the first enemy in range. | 4 ||
| [`TempPassiveWhileHasStatus`](Abilities_and_Spells.md#object-temppassivewhilehasstatus) | Object | An object defining passives temporarily granted to the unit while it has a specific status effect. | 4 ||
| [`TileTrail`](./Enums.md#enum-tiletrail) | Enum | Specifies the type of tile left behind as the unit moves. | 4 ||
| [`TimeDelayStatusApplication`](Abilities_and_Spells.md#object-timedelaystatusapplication) | Object | Container for status effects applied after a specified delay. | 4 ||
| [`ToadJump_BasicMove`](#object-toadjump_basicmove) | Object | An object defining a basic movement ability for a toad-like unit. | 4 ||
| [`Trapper`](Characters_and_Bosses.md#object-trapper) | Object | Specifies a trap-placing ability and its targeting parameters. | 4 ||
| `UncappedMana` | Integer | If non-zero, the unit has no maximum mana limit. | 4 ||
| `Vegan` | Integer | If nonzero, sets the unit as Vegan; can also be an object with localization fields and the `Disorder` class. | 4 ||
| [`WeremanTransformationReceiver`](./Enums.md#enum-weremantransformationreceiver) | Enum | Determines which transformation animation or effect is applied when this unit is turned by a were-creature. | 4 ||
| `AbilityEnabledOncePerRound` | Integer | If set, the ability can only be used once per round. | 3 ||
| [`AbilityEnableIfConsumedCharacterHasTag`](./Enums.md#enum-abilityenableifconsumedcharacterhastag) | Enum | Specifies the tag that a consumed character must have for the ability to be enabled. | 3 ||
| `AbilityInheritsWeaponEffects` | Integer | If set, the ability inherits properties from the unit's weapon, with higher values indicating different inheritance modes. | 3 ||
| `AddEndOfCombatRegen` | Integer | The amount of health regenerated after combat ends. | 3 ||
| `AggroTargetIsCurrentTurn` | Integer | If set to 1, the unit's aggro target is the unit currently taking its turn. | 3 ||
| `AllStatsUpPerDisorder` | Integer | The amount by which all stats increase for each disorder (negative status) the unit has. | 3 ||
| [`ApplyMultipleTimes`](Abilities_and_Spells.md#object-applymultipletimes) | Object | An object containing a `stacks` value that specifies how many times the nested effects are applied. | 3 ||
| [`BaseStatMultiply`](./Enums.md#enum-basestatmultiply) | Float | A multiplier applied to the unit's base stats. | 3 ||
| [`BasicAttackCritChance`](./Enums.md#enum-basicattackcritchance) | Float | A multiplier for the critical hit chance of basic attacks, either as a float or percentage. | 3 ||
| `bishop_hat` | Variable | A variable key referencing a specific item or graphical element (the bishop hat). | 3 ||
| `BoneArmorPassive` | Integer | The number of stacks of bone armor granted, which absorbs damage. | 3 ||
| [`BonusTurnPattern`](./Arrays.md#array-bonusturnpattern) | Array | An array defining the pattern of bonus turns granted to this unit. | 3 ||
| `Bounty` | Integer | The number of bounty stacks applied to enemies, increasing rewards on defeat. | 3 ||
| [`BreakOnElement`](./Enums.md#enum-breakonelement) | Enum | Specifies an element that, when dealt to the unit, causes its armor or item to break. | 3 ||
| [`CanMutateTo`](./Enums.md#enum-canmutateto) | Array / Enum | Specifies the mutation forms this unit can transform into, either a single form or an array of possible forms. | 3 ||
| `CantCatchDiseases` | Integer | The number of stacks that prevent the unit from contracting diseases. | 3 ||
| `CantSpreadDiseases` | Integer | The number of stacks that prevent the unit from spreading diseases. | 3 ||
| [`CatPartsSizeScaleStatus`](Abilities_and_Spells.md#object-catpartssizescalestatus) | Object | Configures scale multipliers for individual cat body parts (body, arms, mouth). | 3 ||
| `ChanceToBlock` | Integer | The percentage chance to block incoming damage. | 3 ||
| [`CharmedTinyTumor`](#object-charmedtinytumor) | Object | An object defining a specific variant of the TinyTumor status, typically with its own graphics scale. | 3 ||
| [`CollideWithConsumed`](./Math_Equations.md) | Equation | Damage formula for collision with consumed objects, e.g., '4+bonus_melee_damage'. | 3 ||
| [`Conditional_Adjacent`](Engine_LogicKeys.md#conditional_adjacent) | Object | An object whose nested keys define statuses or effects applied to or by units that are adjacent to the unit. | 3 ||
| [`Conditional_RandomChance`](Abilities_and_Spells.md#object-conditional_randomchance) | Object | An object containing effects that execute only if a random roll succeeds, with an odds value defined inside. | 3 ||
| [`Conditional_Shielded`](Abilities_and_Spells.md#object-conditional_shielded) | Object | An object containing effects that are only applied if the target has a shield active. | 3 ||
| [`CookedChickenLeg`](#object-cookedchickenleg) | Object | An undefined object; no examples or paths found in the provided context. | 3 ||
| `CopyPassiveSlot` | Integer | An index (0-based) specifying which equipment slot's passive to copy onto this unit. | 3 ||
| `CorpseVaporizer` | Integer | The number of corpses vaporized on hit. | 3 ||
| [`count`](./Arrays.md#array-count) | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 3 ||
| [`CreateGlobalModifiers`](Abilities_and_Spells.md#object-createglobalmodifiers) | Object | Defines global gameplay modifiers to activate. | 3 ||
| `DestroyWeapon` | Integer | The number of weapons destroyed. | 3 ||
| `DestroyWeaponThrow` | Integer | The number of weapons destroyed after being thrown. | 3 ||
| [`DigestDeadBodies`](./Enums.md#enum-digestdeadbodies) | Enum | Specifies the ability or animation used when digesting a dead body. | 3 ||
| [`DoubleStatus`](./Enums.md#enum-doublestatus) | Enum | The name of a status effect whose stacks are doubled when applied. | 3 ||
| [`DropAsFamiliarOnArmorBreak`](./Enums.md#enum-dropasfamiliaronarmorbreak) | Enum | Specifies the familiar type to drop onto the tile when this status holder's armor breaks. | 3 ||
| [`DustOnHit`](Abilities_and_Spells.md#object-dustonhit) | Object | Configuration for a dust object spawned on hit. | 3 ||
| [`EquipPermanentItem`](./Enums.md#enum-equippermanentitem) | Enum | The name of the item to permanently equip to the source. | 3 ||
| `ExtraBasicMoves_Status` | Integer | The number of extra basic moves per turn granted. | 3 ||
| `ForceDisplace` | Integer | The distance the target is forced to displace. | 3 ||
| `ForceMoveTowardsEnemies` | Enum / Integer | Specifies the ability or distance to force the target to move towards enemies. | 3 ||
| [`FormChangeHealthThreshold`](Characters_and_Bosses.md#object-formchangehealththreshold) | Object | Specifies health thresholds that trigger form changes, with form_below for health at or below and form_above for health above. | 3 ||
| [`Holy`](Characters_and_Bosses.md#object-holy) | Enum / Object | Specifies the 'Holy' form within FormChanger, with its own animation suffix and passives. | 3 ||
| `IllusionTint` | Integer | If non-zero, applies an illusionary tint to the unit's sprite. | 3 ||
| [`IncAuxCounterClamped`](Abilities_and_Spells.md#object-incauxcounterclamped) | Object | An object with `change` and `max` properties modifying the auxiliary counter by `change`, clamped to `max`. | 3 ||
| `include_spells` | Boolean | If true, the AI-controlled bonus turn includes spells as available actions. | 3 ||
| `InstantMaxHealthUp` | Integer | The amount of permanent maximum health increase. | 3 ||
| [`KnockOutCoin`](Abilities_and_Spells.md#object-knockoutcoin) | Integer / Object | The number of coins knocked out, with an optional probability or an object with stacks and chance. | 3 ||
| [`Lava_Distortion`](#object-lava_distortion) | Variable | A configuration object for a visual distortion effect, typically defining a movieclip and render settings. | 3 ||
| `Lifesteal` | Integer | The amount of lifesteal stacks applied. | 3 ||
| [`ManaPickup`](Characters_and_Bosses.md#object-manapickup) | Object | The amount of mana stacks and the frame range for the pickup animation. | 3 ||
| `Meteornado` | Integer | The number of Meteornado status stacks applied, or an object defining its visual effects. | 3 ||
| `MimicSpawnerAttacks` | Integer | If positive, the number of attacks mimicked; if -1, mimics all attacks from spawner. | 3 ||
| `MinimumKnockbackFromPhysicalAttacks` | Integer | The minimum knockback distance applied when hit by a physical attack. | 3 ||
| `MoonHeadFinisherEnabler` | Integer | Determines the finisher state for MoonHead abilities; negative values may disable. | 3 ||
| [`MoveAndUseAbilityEachTurnBeginIfPossible`](./Enums.md#enum-moveanduseabilityeachturnbeginifpossible) | Enum | Specifies the name of the ability the unit will move and attempt to use at the start of each of its turns. | 3 ||
| `must_do_damage` | Boolean | If true, the status or effect will only be applied if the attack or ability actually deals damage. | 3 ||
| [`MutateViaAbility`](./Enums.md#enum-mutateviaability) | Enum | Specifies the ability that triggers a mutation form change. | 3 ||
| `NeckArmorPassiveMultiplierBonus` | Integer | A multiplier bonus applied to the passives of the unit's neck armor slot. | 3 ||
| `NextAttackBonusRange` | Integer | The added range for the unit's next basic attack. | 3 ||
| `PermanentDexterity` | Integer | The permanent amount of dexterity added or removed. | 3 ||
| `PermanentSpeed` | Integer | The permanent amount of speed added or removed. | 3 ||
| `Piercing` | Integer | The amount of armor or damage reduction ignored by the attack or ability. | 3 ||
| `PlayBackground` | Integer | Specifies the background index to play. | 3 ||
| `PrioritizeHitDifferentTargets` | Integer | If set to 1, the unit's AI prioritizes hitting different targets rather than focusing one. | 3 ||
| `RangeUp` | Integer | The number of stacks of bonus attack range applied. | 3 ||
| `RepairOnKill` | Integer | The number of charges restored to the ability upon killing a target. | 3 ||
| `RockyArmorPassive` | Integer | The number of stacks of the Rocky Armor status effect granted. | 3 ||
| `RunInXTurns` | Integer | The number of turns after which this unit will flee the battle. | 3 ||
| [`SetCrazyEyeBackgroundWeights`](Abilities_and_Spells.md#object-setcrazyeyebackgroundweights) | Object | An object containing a `weights` array that sets the weighting for which Crazy Eye background variant is displayed. | 3 ||
| [`SetDefaultFacePassive`](./Enums.md#enum-setdefaultfacepassive) | Enum | Specifies the name of the default face passive to be assigned to this unit. | 3 ||
| `SharePickupsWithSpawner` | Integer | If set to 1, pickups collected by this unit are also given to its spawner. | 3 ||
| `SpawnCreepOnHit` | Integer | If set to 1, spawns creep on the tile when this unit takes damage. | 3 ||
| [`SpawnCustomTrap`](./Enums.md#enum-spawncustomtrap) | Enum | Specifies the name of a custom trap blueprint to spawn at the target location. | 3 ||
| `SpawnNeutralWebTrapOnMiss` | Integer | The number of neutral web traps spawned on the tile if the attack misses. | 3 ||
| [`SpawnVolcanoOnBattleStart`](#object-spawnvolcanoonbattlestart) | Object | An object containing parameters (object type, tile, radius) for spawning a volcano effect at the start of battle. | 3 ||
| [`StackingFlowerTrail`](Items_and_Equipment.md#object-stackingflowertrail) | Object | An object defining how a flower trail status stacks (stacks count, stack key) when the unit moves. | 3 ||
| [`StatusAllCharactersOnSpawn`](House_and_Environment.md#object-statusallcharactersonspawn) | Object | Defines status effects applied to all characters when they spawn into the battlefield. | 3 ||
| [`StatusCharactersOnRoundEnd`](#object-statuscharactersonroundend) | Object | An object whose nested keys define statuses or effects applied to characters at the end of each round. | 3 ||
| [`SupportFormChangeInsteadOfRun`](Characters_and_Bosses.md#object-supportformchangeinsteadofrun) | Enum / Object | Specifies a form change to trigger instead of fleeing, either as a passive object with ability details or a direct form name. | 3 ||
| [`tag_filter`](./Enums.md#enum-tag_filter) | Enum | Specifies a tag (e.g., 'crow', 'rock', 'grub_familiar') used to filter which units a status or effect applies to. | 3 ||
| [`TakeBonusTurnWithAIControl`](Abilities_and_Spells.md#object-takebonusturnwithaicontrol) | Object | An object configuring whether the bonus turn happens at the end of the round and whether spells are included. | 3 ||
| `TempInitiativeChange` | Integer | The flat change to the unit's initiative value. | 3 ||
| [`ThornUpX`](#object-thornupx) | Object | An object defining a self-buff status effect, typically with its own animation (e.g., 'spikes'). | 3 ||
| [`TileTrail_Ahead`](./Enums.md#enum-tiletrail_ahead) | Enum | Specifies the type of tile to place one tile ahead of the unit's movement. | 3 ||
| `TriggerGameEnding` | Integer | If set to 1, triggers the game's ending sequence; 0 disables it. | 3 ||
| `TrueShot` | Integer | The number of stacks of a buff that makes the unit's attacks unmissable. | 3 ||
| [`TVOff`](#object-tvoff) | Object | An object defining a self-buff status effect that plays a 'turnOff' animation. | 3 ||
| [`UseAbility_NonStack`](./Enums.md#enum-useability_nonstack) | Enum | Specifies an ability to use on kill that does not stack with itself. | 3 ||
| `VaporizeTarget` | Integer | If non-zero, instantly destroys the target, leaving no corpse. | 3 ||
| [`XIsMultipliedPercentHealth`](./Arrays.md#array-xismultipliedpercenthealth) | Array | The [stacks, probability] for multiplying health by a percentage. | 3 ||
| [`AbilityChargeRefundChance`](Miscellaneous.md#object-abilitychargerefundchance) | Object | An object containing a percentage chance to refund an ability charge, with an advantage softcap. | 2 ||
| [`AbilityEnabledIfHasStatus`](./Enums.md#enum-abilityenabledifhasstatus) | Enum | Specifies the status effect that must be present on the unit for the ability to be enabled. | 2 ||
| [`AbilityHealthThreshold`](Characters_and_Bosses.md#object-abilityhealththreshold) | Object | Defines an ability and conditions for its activation when the unit's health reaches a threshold. | 2 ||
| [`AbilityOnRoundEnd`](Characters_and_Bosses.md#object-abilityonroundend) | Object | Specifies an ability that is automatically executed at the end of each round. | 2 ||
| [`AbsorbBuff`](#object-absorbbuff) | Variable | A visual effect object (e.g., ManaParticle) that plays when mana or a buff is absorbed. | 2 ||
| `AbsorbManaAura` | Integer | The amount of mana absorbed from nearby enemies each turn. | 2 ||
| `AddAllyNeighborsToAbilityRange` | Integer | The number of additional tiles an ability's range is extended to include adjacent allies. | 2 ||
| `AddChaScalingSpellDamage` | Integer | The amount of spell damage added that scales with the unit's Charisma stat. | 2 ||
| [`AddHiddenTag`](./Enums.md#enum-addhiddentag) | Enum | A hidden tag applied to the unit for internal logic and triggers. | 2 ||
| `AddInitiative` | Integer | The amount of bonus or penalty to the unit's turn order initiative value. | 2 ||
| `AddKnockbackToEverything` | Integer | The number of tiles of knockback added to all damage instances. | 2 ||
| `AddLootMultiplier` | Integer | The multiplier added to loot drops from this unit. | 2 ||
| [`AddPassivesToSummonAbilityMinions`](Miscellaneous.md#object-addpassivestosummonabilityminions) | Object | An object whose nested keys define passives applied to minions summoned by abilities. | 2 ||
| [`AddPassiveToSpawnedRocks`](Miscellaneous.md#object-addpassivetospawnedrocks) | Object | An object whose nested keys define passives applied to rocks spawned by the unit. | 2 ||
| `AddRangedCritChance` | Integer | The percentage chance added to critically hit with ranged attacks. | 2 ||
| [`AddSelfStatusToWeapons`](Items_and_Equipment.md#object-addselfstatustoweapons) | Object | An object whose nested keys define status effects applied to the unit's own weapons. | 2 ||
| `AddSpellDamage` | Integer | The flat amount of spell damage added to all spell attacks. | 2 ||
| `AddSpiritBombCharges` | Integer | The number of charges added to the Spirit Bomb ability. | 2 ||
| `AddStartingMana` | Number | The amount of bonus mana the unit starts each battle with. | 2 ||
| [`AddStatusToBasicAttackWithCooldown`](Miscellaneous.md#object-addstatustobasicattackwithcooldown) | Object | An object whose nested keys define statuses applied to basic attacks, subject to a cooldown. | 2 ||
| [`AddStatusToExplosions`](Miscellaneous.md#object-addstatustoexplosions) | Object | An object whose nested keys define statuses applied to explosion damage. | 2 ||
| [`AddStatusToFirstBasicAttack`](Miscellaneous.md#object-addstatustofirstbasicattack) | Object | An object whose nested keys define statuses applied only to the unit's first basic attack. | 2 ||
| [`AddStatusToKnockbackDamage`](Items_and_Equipment.md#object-addstatustoknockbackdamage) | Object | An object whose nested keys define statuses applied to damage caused by knockback. | 2 ||
| [`AddStatusToMeleeDamage`](Miscellaneous.md#object-addstatustomeleedamage) | Object | An object whose nested keys define statuses applied to melee damage. | 2 ||
| [`AddStatusToSpells`](Characters_and_Bosses.md#object-addstatustospells) | Object | Specifies status effects added to all spell attacks used by this unit. | 2 ||
| [`AddStatusToTrampleDamage`](Characters_and_Bosses.md#object-addstatustotrampledamage) | Object | An object whose nested keys define statuses applied to trample damage. | 2 ||
| [`AddTag`](./Enums.md#enum-addtag) | Enum | Specifies a gameplay tag (e.g., 'rock', 'plant') to add to the unit, used for interaction checks. | 2 ||
| [`AddTemporaryEffectsToEquipment`](Miscellaneous.md#object-addtemporaryeffectstoequipment) | Object | An object whose nested keys define temporary status effects added to equipment. | 2 ||
| `AddUnfilledMaxHealth` | Integer | The amount of maximum health added, but not healed (the health bar remains at its current level). | 2 ||
| `AddWeaponScaling` | Integer | The amount of scaling added to damage based on the weapon's stats. | 2 ||
| [`AfterImage`](Abilities_and_Spells.md#object-afterimage) | Object | Specifies the object or skill used to create an afterimage of the unit. | 2 ||
| `AggroTargetIsBuddy` | Integer | If set to 1, the unit's aggro target is its buddy (linked partner). | 2 ||
| `all_items` | Variable | A variable field for specifying all items; no standard examples provided. | 2 ||
| `AllDamageCrits` | Integer | If set to 1, all damage dealt by the unit becomes critical hits. | 2 ||
| `AllDamageImmune_IncludingSpeculative` | Integer | If set to 1, this unit is immune to all damage, including speculative damage. | 2 ||
| `AlliesAvoidTraps` | Integer | If set to 1, allied units will not trigger traps. | 2 ||
| `AllowPassTurn` | Integer | If set to 1, the unit can skip its turn. If 0, it cannot. | 2 ||
| [`AllyBonusAbilityAura`](./Enums.md#enum-allybonusabilityaura) | Enum | Specifies an ability name granted to adjacent allies in an aura, optionally with a square radius. | 2 ||
| `AllyChainKnockback` | Integer | The number of additional tiles of knockback applied to enemies hit by chain knockback effects. | 2 ||
| [`AllyDamageReaction`](./Enums.md#enum-allydamagereaction) | Enum | Specifies the ability to use when an ally takes damage, such as 'attack'. | 2 ||
| [`AllyHealthRegenAura`](Miscellaneous.md#object-allyhealthregenaura) | Object | An object defining an aura that grants health regeneration to allies, typically with 'stacks' and 'range' fields. | 2 ||
| [`AllyMoveAbilityAura`](./Enums.md#enum-allymoveabilityaura) | Enum | Determines the movement ability granted to allies within an aura. | 2 ||
| `AllyMultiplyKnockbackDamage` | Integer | A multiplier for knockback damage dealt to allies. | 2 ||
| `AllyMultiplyKnockbackDistance` | Integer | A multiplier for knockback distance applied to allies. | 2 ||
| `AllyUncappedHPAura` | Integer | The number of stacks granting uncapped maximum health to allies via an aura. | 2 ||
| [`AlternateCraftingPools`](Miscellaneous.md#object-alternatecraftingpools) | Object | An object mapping crafting pool categories to alternate pools for the unit. | 2 ||
| `AlwaysHitDifferentTargets` | Integer | If set to 1, attacks always target different units, never the same target twice. | 2 ||
| `AmplifyNegativeStatus` | Integer | The number of stacks that amplify the intensity of negative statuses on enemies. | 2 ||
| `AmplifyPositiveStatus` | Integer | The number of stacks that amplify the intensity of positive statuses on allies. | 2 ||
| `Antidote` | Float | The multiplier for the number of antidote pickups spawned. | 2 ||
| [`ApplyStatusesToRandomEnemiesEachTurn`](Items_and_Equipment.md#object-applystatusestorandomenemieseachturn) | Object | An object specifying statuses to apply to random enemies each turn, with an optional 'count' field. | 2 ||
| [`ApplyStatusIfCrit`](Abilities_and_Spells.md#object-applystatusifcrit) | Object | Defines effects that are applied only when the attack scores a critical hit. | 2 ||
| [`ApplyToTile`](Abilities_and_Spells.md#object-applytotile) | Object | Defines effects to apply to the target tile. | 2 ||
| [`ArmorBreakOnHit`](Items_and_Equipment.md#object-armorbreakonhit) | Object | An object defining durability loss and chance for armor to break when hit. | 2 ||
| `ArmorDodgeChance` | Integer | The percentage chance to dodge incoming attacks when wearing this armor. | 2 ||
| [`AutocastEachTurn`](./Enums.md#enum-autocasteachturn) | Enum | Specifies the ability automatically cast at the end of each turn. | 2 ||
| [`AutocastEachTurnBegin`](./Enums.md#enum-autocasteachturnbegin) | Enum | Specifies the ability automatically cast at the start of each turn, optionally with chance and polarity. | 2 ||
| `AutoCritLowDamage` | Integer | The amount of damage below which attacks automatically critically strike. | 2 ||
| `AutoEquipConsumables` | Integer | The number of consumables automatically equipped per turn. | 2 ||
| [`BackstabCritChance`](./Enums.md#enum-backstabcritchance) | Float | A multiplier for critical hit chance on backstab attacks. | 2 ||
| `BackstabFront` | Integer | If set to 1, allows backstab bonuses to apply when attacking from the front. | 2 ||
| `BasicAttackCantMiss` | Integer | If nonzero, the unit's basic attack cannot miss. | 2 ||
| `BasicAttackStatusCarefulness` | Integer | The number of stacks of Carefulness applied by basic attacks. | 2 ||
| [`BasicMonkMelee`](#object-basicmonkmelee) | Object | An object defining the basic melee attack for a monk class. | 2 ||
| [`BasicRanged`](#object-basicranged) | Object | An object defining the basic ranged attack for a unit. | 2 ||
| [`BasicSuplex`](#object-basicsuplex) | Object | An object defining the basic suplex ability for a unit. | 2 ||
| [`BodyGuard`](Abilities_and_Spells.md#object-bodyguard) | Object | An object that applies a bodyguard status, optionally linking to a swap ability. | 2 ||
| [`BodyGuard`](Abilities_and_Spells.md#object-bodyguard) | Object | An object that applies a bodyguard status, optionally linking to a swap ability. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `BonusFoodEachBattle` | Integer | The amount of bonus food earned at the end of each battle. | 2 ||
| `BonusHealthRegenBasedOnDex` | Integer | The amount of bonus health regeneration per point of dexterity. | 2 ||
| `BonusRangeBasedOnDex` | Integer | The amount of bonus range per point of dexterity. | 2 ||
| [`BonusToss`](#object-bonustoss) | Object | An object defining a bonus toss ability for the unit. | 2 ||
| [`BonusToss2`](#object-bonustoss2) | Object | An object defining a second bonus toss ability for the unit. | 2 ||
| [`BoobyTrapItems`](Miscellaneous.md#object-boobytrapitems) | Object | An object defining effects to apply when items are thrown or broken. | 2 ||
| [`BoomerCatExplode`](#object-boomercatexplode) | Object | An object defining the explosion ability for a boomerang cat, including its spell template and graphics. | 2 ||
| `BoostAllyStatsOnDeath` | Integer | The number of stacks that boost ally stats when this unit dies. | 2 ||
| `BoostDamageGlobalAura` | Integer | The amount of damage boost applied by a global aura to all allies. | 2 ||
| `BoostHeals` | Integer | The number of stacks that increase healing received or dealt. | 2 ||
| `BoostRangeGlobalAura` | Integer | The amount of range boost applied by a global aura to all allies. | 2 ||
| [`BouncyProjectiles`](Items_and_Equipment.md#object-bouncyprojectiles) | Object | An object with 'max_bounces' and 'max_range' defining projectile bounciness behavior. | 2 ||
| `Bound` | Integer | The number of stacks of the Bound status effect applied to the target. | 2 ||
| `BraceForEachNeighboringEnemy` | Integer | The number of Brace stacks gained for each adjacent enemy. | 2 ||
| `BreakWhenNoShield` | Integer | If 1, the armor breaks when the unit has no shield remaining. | 2 ||
| [`BungaEntrance`](Characters_and_Bosses.md#object-bungaentrance) | Object | Specifies the entrance animation, ability, and conditions for this unit's dramatic battle entrance. | 2 ||
| [`BungaSwipe`](#object-bungaswipe) | Object | An object defining a melee swipe ability with AI and graphics. | 2 ||
| `CancelPrimedAbilities` | Integer | If non-zero, cancels any primed abilities on the target. | 2 ||
| `CanLevelUpWhenDead` | Integer | If 1, allows the unit to gain experience and level up while dead. | 2 ||
| `CanRemoveCursedItems` | Integer | If nonzero, allows the unit to remove cursed items from equipment slots. | 2 ||
| `CanShield` | Integer | If set to 1, this unit can generate shields. | 2 ||
| `CapDamageFromAllies` | Integer | The maximum amount of damage the unit can take from allies per hit. | 2 ||
| `CapMovementAbilityRange` | Integer | The maximum range allowed for movement abilities. | 2 ||
| `CapTechSpent` | Integer | The maximum amount of tech that can be spent on this ability per turn. | 2 ||
| [`CatAPultAnimation`](Miscellaneous.md#object-catapultanimation) | Object | An object specifying the ability and animation used for the CatAPult passive. | 2 ||
| [`CatapultJump`](#object-catapultjump) | Object | An object defining the Catapult Jump ability, a variant of BasicJump. | 2 ||
| [`CatapultJump2`](#object-catapultjump2) | Object | An object defining an upgraded Catapult Jump ability with a different description. | 2 ||
| [`CatchProjectiles`](Items_and_Equipment.md#object-catchprojectiles) | Object | An object defining chance to catch projectiles and optionally apply statuses. | 2 ||
| `CCImmunity` | Integer | If set to 1, this unit is immune to crowd control effects. | 2 ||
| `ChainKnockback` | Integer | If 1, enables knockback to chain to additional targets. | 2 ||
| [`ChanceToBlockAndCounter`](Items_and_Equipment.md#object-chancetoblockandcounter) | Integer / Object | The percentage chance or an object defining chance and conditions to block and counter an attack. | 2 ||
| `ChanceToDisableActionsIfNotCharmed` | Integer | The percentage chance to disable actions of enemies that are not charmed. | 2 ||
| [`ChanceToRevive`](Elite_Buffs.md#object-chancetorevive) | Integer / Object | The percentage chance or an object defining chance, health, and statuses on revival. | 2 ||
| [`ChangeFaction`](./Enums.md#enum-changefaction) | Enum | Specifies the name of the faction to switch the target to. | 2 ||
| `ChangeTauntPriority` | Integer | The amount to adjust the unit's taunt priority, affecting enemy targeting. | 2 ||
| [`ChangeTileOnDeath`](./Enums.md#enum-changetileondeath) | Enum | Specifies the tile type that replaces the current tile when this unit dies. | 2 ||
| [`ChargeFists`](#object-chargefists) | Integer / Object | The number of charge stacks applied to unarmed attacks. | 2 ||
| [`ChargeFists`](#object-chargefists) | Integer / Object | The number of charge stacks applied to unarmed attacks. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`ChargeSpiritBombAura`](./Enums.md#enum-chargespiritbombaura) | Enum | Specifies the ability to charge for spirit bomb aura. | 2 ||
| `CharmAllFlies` | Integer | If 1, charms all fly-type enemies, causing them to become allies. | 2 ||
| [`CharmedDemonKitten`](#object-charmeddemonkitten) | Object | An object defining the Charmed Demon Kitten familiar, a variant of Hyde. | 2 ||
| [`CharmedFlySwarm`](#object-charmedflyswarm) | Object | Specifies the definition for a charmed fly swarm that inherits properties from FlySwarm, with faction set to allies and inheriting faction. | 2 ||
| `CharmedForceAttack` | Integer | If non-zero, forces the charmed target to use its basic attack on a random nearby unit. | 2 ||
| [`CherubimReaction`](Characters_and_Bosses.md#object-cherubimreaction) | Object | Specifies the abilities used when this unit leaves or returns to the battlefield. | 2 ||
| `ClearNegativeEffects` | Integer | The number of negative effects cleared from the target. | 2 ||
| `CoinsAddDamage` | Integer | The amount of damage added based on the number of coins the unit has. | 2 ||
| `CollectPickupsOnBattleEnd` | Integer | The number of pickups automatically collected from corpses on the battlefield when the battle ends. | 2 ||
| `CollideWithThrowTarget` | Integer | Determines whether the thrown object collides with the primary target (0 disables collision). | 2 ||
| [`Conductor`](Passives_and_Statuses.md#object-conductor) | Object | The number of times the Conduct effect is applied. | 2 ||
| `ConductorManaRegen` | Integer | The amount of mana regenerated per turn by the Conductor effect. | 2 ||
| [`ConjureBonusAbility`](Abilities_and_Spells.md#object-conjurebonusability) | Enum / Object | Specifies the name of the bonus ability to conjure. | 2 ||
| [`ConjureBonusAbility`](Abilities_and_Spells.md#object-conjurebonusability) | Enum / Object | Specifies the name of the bonus ability to conjure. | 2 | `random` (Enum), `Mage` (Enum), `{ ... }` (Object) |
| `ConjureCastSpellsForAllies` | Integer | The number of additional spells conjured for allies when casting. | 2 ||
| `ConsumableEffectsMultiplierBonus` | Integer | A multiplier bonus applied to the effects of consumable items. | 2 ||
| `CopyCatPassive_Initializer` | Integer | The number of copies of this passive to initialize. | 2 ||
| [`CopySpells`](Abilities_and_Spells.md#object-copyspells) | Integer / Object | The number of spells copied from the target, or an object specifying `stacks` and whether the copy is `upgraded`. | 2 ||
| [`Counterspell`](#object-counterspell) | Integer / Object | If non-zero, negates the next incoming enemy spell and triggers the configured counterspell effects. | 2 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | Specifies the amount of damage dealt, can be a number or expression. | 2 ||
| `DamageBasedOnMissingHealth` | Integer | The percentage of the target's missing health dealt as additional damage. | 2 ||
| `DamageDistanceAOEFalloff` | Integer | The falloff multiplier applied to AoE damage based on distance from the center of the effect. | 2 ||
| `DamageEnemiesOnHeal` | Integer | The amount of damage dealt to enemies whenever the unit is healed. | 2 ||
| `DamageEnemiesOnKill` | Integer | The amount of damage dealt to enemies whenever the unit kills an enemy. | 2 ||
| [`DamageNeighborsAfterMove`](Elite_Buffs.md#object-damageneighborsaftermove) | Object | Defines the spell damage and effects applied to neighboring tiles after the unit moves. | 2 ||
| [`DamageNeighborTilesWhenCastSpell`](Miscellaneous.md#object-damageneighbortileswhencastspell) | Object | Defines the spell damage and effects applied to neighbor tiles when a spell is cast. | 2 ||
| [`DamageReductionAura`](Miscellaneous.md#object-damagereductionaura) | Object | Defines an aura that reduces incoming damage, with range, ally-only, and stack settings. | 2 ||
| `DamageTrinket` | Integer | The amount of durability damage dealt to the target's equipped trinket. | 2 ||
| `DeathChill` | Integer | The number of Chill stacks applied to the killer upon death. | 2 ||
| [`DeathRattle`](Characters_and_Bosses.md#object-deathrattle) | Enum / Object | Specifies an ability or effect triggered when the unit dies, optionally with a pop_corpse flag. | 2 ||
| `DebuffImmunity` | Integer | If 1, the unit is immune to debuffs. | 2 ||
| `DejaVu` | Integer | The percentage chance or definition for the DejaVu disorder, causing repeated events. | 2 ||
| [`DelayCastAbility`](Abilities_and_Spells.md#object-delaycastability) | Enum / Object | Specifies the name of an ability to cast after a delay. | 2 ||
| `DelayedFury` | Integer | The percentage of Fury damage that is stored and applied after a delay. | 2 ||
| `DemonicGlyph_Bite` | Integer | The weight for the demonic glyph of bite, or its configuration. | 2 ||
| `DemonicGlyph_Summon` | Integer | The weight for the demonic glyph of summon, or its configuration. | 2 ||
| `DemonicGlyphFrames` | Integer | The number of animation frames for the demonic glyph effect. | 2 ||
| [`DepressionAura`](#depressionaura) | Integer | The number of stacks of Depression status applied to nearby enemies each turn; can be an object with range and ally settings. | 2 ||
| [`DiesToElement`](Characters_and_Bosses.md#object-diestoelement) | Enum / Object | Specifies the element that instantly kills this unit, optionally with an instant flag. | 2 ||
| `DieViaAbilityInternally` | Integer | If non-zero, causes the target to die via an internal ability trigger. | 2 ||
| `DirtyClaws` | Integer | The number of additional damage instances from Dirty Claws on attack. | 2 ||
| `DisablePassiveSlot` | Integer | If non-zero, disables the specified passive slot index (0 or 1). | 2 ||
| `DisplaceToOriginalPosition` | Integer | If non-zero, returns the unit to its original position after the effect resolves. | 2 ||
| `DissuadeInstakills` | Integer | If set to 1, this unit cannot be instantly killed. | 2 ||
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 2 ||
| `DoubleCastSpell` | Integer | The number of times the next spell cast is doubled, or a template with name and tooltip. | 2 ||
| `DoubleCastWeapons` | Integer | The number of additional weapon casts per attack. | 2 ||
| [`DoubleLoot`](#object-doubleloot) | Integer / Object | The multiplier for loot drops, where 1 or 2 doubles the loot. | 2 ||
| [`DoubleLoot`](#object-doubleloot) | Integer / Object | The multiplier for loot drops, where 1 or 2 doubles the loot. | 2 | `2` (Number), `1` (Number), `{ ... }` (Object) |
| `DrinkWater` | Integer | The number of water-drink actions performed. | 2 ||
| [`DrMangler`](#object-drmangler) | Object | Defines the Dr Mangler passive, typically increasing damage based on missing health. | 2 ||
| `DukeOfFlies` | Integer | The number of flies spawned when the unit dies. | 2 ||
| [`Dyslexia`](./Arrays.md#array-dyslexia) | Array | An array [minRange maxRange] defining the random range of spell range swap caused by Dyslexia. | 2 ||
| `EachSpellFreeAtFullMana` | Integer | The number of spells that cost no mana when the unit has full mana. | 2 ||
| [`Earth`](Engine_LogicKeys.md#object-earth) | Object | Defines the Earth element effects, including damage value. | 2 ||
| [`ElementalAttunement`](Miscellaneous.md#object-elementalattunement) | Object | Defines the elemental effects (Fire, Ice, etc.) applied by the attunement. | 2 ||
| [`EMP`](Miscellaneous.md#object-emp) | Object | Defines the EMP effect, including spell graphics override for pulsed area damage. | 2 ||
| `Empath` | Integer | The percentage of damage shared with nearby allies from the Empath disorder. | 2 ||
| `EmptyMana` | Integer | If non-zero, sets the unit's mana to empty when applied. | 2 ||
| [`EmptyMind`](#object-emptymind) | Integer / Object | The number of Empty Mind stacks, likely disabling special abilities. | 2 ||
| [`EmptyMind`](#object-emptymind) | Integer / Object | The number of Empty Mind stacks, likely disabling special abilities. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `EnemiesGetPickupsKnockedOut` | Integer | The number of pickups knocked out of enemies when they are defeated. | 2 ||
| `EnergyStorm` | Integer | The period or definition for the Energy Storm, dealing periodic damage in an area. | 2 ||
| [`Enlarge`](#object-enlarge) | Integer / Object | The number of turns the unit is enlarged, increasing its size and stats. | 2 ||
| [`Enlarge`](#object-enlarge) | Integer / Object | The number of turns the unit is enlarged, increasing its size and stats. | 2 | `3` (Number), `{ ... }` (Object) |
| `EquipmentPassiveMultiplierBonus` | Integer | A multiplier bonus applied to passive effects from equipment. | 2 ||
| `EquipmentSetBonusBonus` | Integer | The number of additional set bonuses granted from equipment. | 2 ||
| [`EscapeSequence`](Miscellaneous.md#object-escapesequence) | Object | Defines an escape sequence with safe explosion displacement and random distance displacement. | 2 ||
| [`Eternal`](Items_and_Equipment.md#object-eternal) | Object | Defines the Eternal revival effect, setting stacks and the health percentage restored. | 2 ||
| `ExpireOnSpawnerTurnEnd` | Integer | If set to 1, this unit is removed from battle at the end of its spawner's turn. | 2 ||
| `ExplodeOverkilledEnemies` | Integer | The number of explosions caused by overkilled enemies. | 2 ||
| `ExplosionImmunity` | Integer | If non-zero, grants immunity to explosion damage. | 2 ||
| [`ExtraStatusWhenDealingDamage`](Items_and_Equipment.md#object-extrastatuswhendealingdamage) | Object | Defines additional statuses applied to the target or source when dealing damage, with conditionals. | 2 ||
| `ExtraTrinketUses` | Integer | The number of additional uses granted to trinkets. | 2 ||
| [`FaceLastDamage`](Characters_and_Bosses.md#object-facelastdamage) | Integer / Object | If set to 1, the unit turns to face the direction of the last damage received; an object can specify animation settings. | 2 ||
| `FaceShield` | Integer | If 1, the unit has a face shield that protects it from certain attacks or effects. | 2 ||
| [`FamiliarBonusAbility`](./Enums.md#enum-familiarbonusability) | Enum | Specifies the name of the bonus ability added to familiars. | 2 ||
| `FamiliarSecondaryDamageImmunity` | Integer | If non-zero, grants immunity to secondary damage sources for familiars. | 2 ||
| [`FinalBossShield`](./Enums.md#enum-finalbossshield) | Enum | Specifies the shield ability used by a final boss, or None for no shield. | 2 ||
| [`FindExtraItemFromPoolOnBattleEnd`](./Enums.md#enum-findextraitemfrompoolonbattleend) | Enum | Specifies the item pool from which an extra item is granted at the end of combat. | 2 ||
| [`FindItem`](./Enums.md#enum-finditem) | Enum | The name of the specific item to find and add to the source's inventory. | 2 ||
| `FireStorm` | Integer | The percentage chance or combo definition for the Fire Storm effect. | 2 ||
| `FlatHealWhenDealDamage` | Integer | The flat amount of health healed each time damage is dealt. | 2 ||
| `FlatLeechIfDamaged` | Integer | The flat amount of health leeched when the unit takes damage. | 2 ||
| `FlippedFacingForceAttack` | Integer | If non-zero, forces the unit to attack after flipping its facing direction. | 2 ||
| `FlowerPowerAuraBrace` | Integer | The amount of brace (defense) granted by the Flower Power aura. | 2 ||
| `FlowerPowerAuraStrength` | Integer | The amount of strength (attack) granted by the Flower Power aura. | 2 ||
| `FlowersOnEndTurn` | Integer | The number of flowers spawned on the unit's tile at the end of each turn. | 2 ||
| `FlowersOnHit` | Integer | The number of flowers spawned on the tile upon hitting the target. | 2 ||
| [`FlyDamageIncrease`](Items_and_Equipment.md#object-flydamageincrease) | Object | The number of stacks or alias for damage increase against flying units. | 2 ||
| `Flying` | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 2 ||
| [`FollowUp`](./Enums.md#enum-followup) | Enum | Specifies the name of the follow-up ability triggered after an attack. | 2 ||
| `ForceMoveNonAlliesInRangeTowardsTile` | Integer | The tile range within which non-allied units are forcibly moved towards a specified tile. | 2 ||
| [`ForceMoveTowardsTaggedObject`](Abilities_and_Spells.md#object-forcemovetowardstaggedobject) | Object | An object specifying the `ability` and optional `tag` used to forcibly move the unit towards a tagged object. | 2 ||
| [`FormChangeDuringWeatherElement`](Characters_and_Bosses.md#object-formchangeduringweatherelement) | Object | Specifies a form change that triggers when the weather matches a given element. | 2 ||
| `FrontstabCritChance` | Integer | The percentage chance to critically hit when attacking from the front. | 2 ||
| `FullHealthAllStatsUp` | Integer | The number of AllStatsUp stacks granted when at full health. | 2 ||
| `FullHealthCritChance` | Integer | The additional critical hit chance percentage when at full health. | 2 ||
| `FullHealthManaRegen` | Integer | The amount of mana regenerated per turn while at full health. | 2 ||
| `FullPower` | Integer | The number of stacks applied per turn while at full health or full mana. | 2 ||
| `GainExtraShield` | Integer | The amount of shield gained on turn start. | 2 ||
| `GainManaWhenAnythingDies` | Integer | The amount of mana gained whenever any unit dies. | 2 ||
| `GlobalManaBurnAura` | Integer | The amount of mana burned from all enemies per turn. | 2 ||
| [`GlobalSpawnOnRoundEnd`](#object-globalspawnonroundend) | Object | Specifies the object to spawn globally at the end of each round. | 2 ||
| `GoopWalk` | Integer | If set to 1, this unit can move through goop tiles without being slowed or damaged. | 2 ||
| [`Grass`](Engine_LogicKeys.md#object-grass) | Object | Specifies the status effects applied to allies standing on grass tiles. | 2 ||
| `GrassTileHealing` | Integer | The amount of healing received per turn while on a grass tile. | 2 ||
| [`GravityWell`](Miscellaneous.md#object-gravitywell) | Object | Specifies the damage and effect applied to units pulled into a gravity well. | 2 ||
| `greater` | Variable | Specifies a conditional check for a value being greater than another value. | 2 ||
| [`GrenadeExplode`](#object-grenadeexplode) | Object | Specifies the explosion effect and graphics used when a grenade detonates. | 2 ||
| [`Haunt`](#object-haunt) | Object | Specifies the status effect applied when haunting a target. | 2 ||
| `HealAndOverhealToShield` | Integer | The amount of healing that also converts overhealing into shield. | 2 ||
| `HealAtStart` | Integer | The percentage or amount of health restored at the start of the turn. | 2 ||
| `HealDamagesEnemies` | Integer | If true, healing actions also damage enemies by this amount. | 2 ||
| `HealingAura` | Integer | The amount of healing per turn granted to nearby allies. | 2 ||
| `HealsAlsoRegenMana` | Integer | The percentage or amount of mana regenerated whenever healing is applied. | 2 ||
| `HealsCanRevive` | Integer | The number of times per battle healing can revive a fallen ally. | 2 ||
| `HolyDamageMultiplierBonus` | Integer | The multiplier bonus applied to holy damage. | 2 ||
| `HolyShieldTransferToSpawner` | Integer | If true, holy shield is transferred to the unit that spawned this one on death. | 2 ||
| [`HolyShieldTransferToTaggedMinions`](./Enums.md#enum-holyshieldtransfertotaggedminions) | Enum | Specifies the tag of minions that receive holy shield on the owner's death. | 2 ||
| `HPGainBlock` | Integer | If true, the unit cannot gain health from any source. | 2 ||
| [`IceArmor`](#object-icearmor) | Integer / Object | The number of Ice Armor stacks granting defensive properties. | 2 ||
| [`IceArmor`](#object-icearmor) | Integer / Object | The number of Ice Armor stacks granting defensive properties. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`ImmediateUseDirectionalAbility`](./Enums.md#enum-immediateusedirectionalability) | Enum | Specifies the name of a directional ability to be used immediately by the unit. | 2 ||
| `ImmobilePassive` | Integer | If set to 1, this unit cannot move from its starting position. | 2 ||
| `ImmortalLeeches` | Integer | The number of leech stacks that persist beyond death. | 2 ||
| `IncreaseExplosionSize` | Integer | The number of extra tiles added to the radius of explosions. | 2 ||
| `IncreaseHealingSpellRange` | Integer | The number of extra tiles added to the range of healing spells. | 2 ||
| `IncreaseItemUsesOnEquip` | Integer | The number of extra uses granted to items when equipped. | 2 ||
| `IncreaseSpellRange` | Integer | The number of extra tiles added to the range of spells. | 2 ||
| [`InfiniteRebirth`](Characters_and_Bosses.md#object-infiniterebirth) | Object | Specifies the health and effects for unlimited rebirth upon death. | 2 ||
| `InjuryImmunity` | Integer | The number of turns the unit is immune to injuries. | 2 ||
| `JohnnyCriesForWashers` | Integer | The number of washers (currency) requested by the Johnny NPC. | 2 ||
| [`KaijuWinCon`](./Enums.md#enum-kaijuwincon) | Enum | Determines which kaiju victory condition is active for this unit. | 2 ||
| `KillsHeal` | Integer | The amount or percentage of health restored on kill. | 2 ||
| [`KillsToMeat`](./Enums.md#enum-killstomeat) | Enum | Specifies the type of meat item spawned when killing certain enemies. | 2 ||
| [`LateBloomer`](Miscellaneous.md#object-latebloomer) | Object | Specifies the stats gained after a set number of turns or stacks. | 2 ||
| [`LeaveBehindOnceEachMove`](./Enums.md#enum-leavebehindonceeachmove) | Enum | Specifies the object left behind on the tile once per move. | 2 ||
| `LeechPercent` | Integer | The percentage of damage dealt restored as health. | 2 ||
| `LightningAspectCharge` | Integer | The number of charges gained that enhance the next lightning attack. | 2 ||
| [`LightningRod`](Miscellaneous.md#object-lightningrod) | Object | Specifies the unit tags and conditions that cause lightning strikes. | 2 ||
| `LimitDamage` | Integer | The maximum amount of damage the unit can take from a single hit. | 2 ||
| `LimitHeal` | Integer | If 1, prevents the unit from being healed. | 2 ||
| [`LineOfSightTrueSightAura`](./Enums.md#enum-lineofsighttruesightaura) | Float | The multiplier or chance for line of sight true sight aura to reveal hidden units. | 2 ||
| `LobbedHook` | Integer | The number of hooks that arc over obstacles to pull targets. | 2 ||
| [`LowHealthAllyDodgeChanceAura`](Miscellaneous.md#object-lowhealthallydodgechanceaura) | Object | Specifies the health threshold and dodge chance granted to nearby low-health allies. | 2 ||
| `MagicDamageImmune` | Integer | If set to 1, this unit is immune to magic damage. | 2 ||
| `MakeBasicAttackPassThroughThings` | Integer | If true, basic attacks pass through obstacles and other units. | 2 ||
| `MakeBasicAttackPull` | Integer | If nonzero, the unit's basic attack pulls the target closer. | 2 ||
| `MakeSpellsRequireCharge` | Integer | If true, spells require a charge-up turn before casting. | 2 ||
| `MamaCatAnimations` | Integer | If set to 1, enables special mama cat animations. | 2 ||
| `ManaRegenMultiplierIfManaEmpty` | Integer | The multiplier applied to mana regen when mana is empty. | 2 ||
| [`Math`](Abilities_and_Spells.md#object-math) | Object | An object containing a `stacks` value that determines how many times the nested effects are applied. | 2 ||
| `MaxHPUp` | Integer | The amount of maximum health permanently increased. | 2 ||
| `MegaMinions` | Integer | The number of extra minions spawned or maximum minion count. | 2 ||
| `Metal` | Integer | The number of armor stacks or metal keyword effects. | 2 ||
| `MetalDetector` | Integer | The number of extra metal drops or scrap found per turn. | 2 ||
| `MinimumTech` | Integer | The minimum tech level guaranteed when crafting or upgrading. | 2 ||
| [`MiniVolcanoReaction`](./Enums.md#enum-minivolcanoreaction) | Enum | Specifies the ability triggered when a mini volcano erupts near this unit. | 2 ||
| [`MockingbirdForm`](#object-mockingbirdform) | Object | Specifies the shape-shift ability that transforms the unit into a mockingbird. | 2 ||
| [`ModifyAbility`](#object-modifyability) | Object | Specifies the modifications to an ability's properties, such as cost or type. | 2 ||
| [`MotherTumorSpawnInCapture`](Characters_and_Bosses.md#object-mothertumorspawnincapture) | Object | Specifies the form changes and statuses applied when the mother tumor spawns after capturing a cat or non-cat. | 2 ||
| [`MoveAwayFromDamageSource`](Characters_and_Bosses.md#object-moveawayfromdamagesource) | Object | Specifies the move ability used to flee from the source of damage, or an object with `move_ability`. | 2 ||
| [`MovementReaction`](Characters_and_Bosses.md#object-movementreaction) | Object | Specifies an ability to cast when a unit moves within range, with options for targeting and conditions. | 2 ||
| [`MoveOne`](#object-moveone) | Object | Specifies a forced movement of exactly one tile in a direction. | 2 ||
| `MoveRandomly` | Integer | If true, the unit moves randomly to an adjacent tile each turn. | 2 ||
| [`MoveSpeedMultiplier`](./Enums.md#enum-movespeedmultiplier) | Float | A multiplier for the unit's movement speed. | 2 ||
| [`MoveTowardsDamageSource`](Characters_and_Bosses.md#object-movetowardsdamagesource) | Enum / Object | Determines the movement behavior when moving towards the unit that dealt damage to it. | 2 ||
| [`MoveWhenDamaged`](Cat_Mutations.md#object-movewhendamaged) | Enum / Object | Defines movement behavior when the unit takes damage, such as weights and move ability. | 2 ||
| [`neck_NukeBonus`](#object-neck_nukebonus) | Object | A self-buff ability that grants the Nuke Explosion sub-ability, augmenting the unit's next weapon-based attack with a nuclear detonation. | 2 ||
| [`neck_NukeExplode`](#object-neck_nukeexplode) | Object | A spell template ability representing the nuclear explosion triggered by Nuke Bonus, playing the NukeBlastLarge center particle and no animation. | 2 ||
| [`Necro_SoulDagger_Uncharged`](#object-necro_souldagger_uncharged) | Object | The uncharged state of the Necromancer's Soul Dagger ability, dealing reduced damage or having a weaker effect compared to the charged version. | 2 ||
| [`NextAttackSpecialCrit`](Abilities_and_Spells.md#object-nextattackspecialcrit) | Integer / Object | The number of charges for a special crit on the next attack, or an object defining its bonus properties. | 2 ||
| [`NextBattleStatus`](#object-nextbattlestatus) | Object | A set of status effects (e.g., stat buffs, full heal) automatically applied to the unit at the start of the next battle. | 2 ||
| `NoManaRegen` | Integer | The unit does not naturally regenerate mana per turn. Value indicates the stage or flag enabling this restriction. | 2 ||
| `NoReflection` | Integer | The unit's reflected damage effects are disabled. Value acts as a binary flag. | 2 ||
| [`NubbyToss`](#object-nubbytoss) | Object | An ability or action where the unit throws a stumpy or truncated projectile, typically dealing damage or applying a debuff. | 2 ||
| `NubbyTossPriority` | Integer | Determines the priority order for the Nubby Toss action relative to other available actions. | 2 ||
| [`NukeQuestFinalBossModifications`](Abilities_and_Spells.md#object-nukequestfinalbossmodifications) | Object | Contains modifications for the nuke quest final boss, such as damage_instance effects. | 2 ||
| `NumbingLeeches` | Integer | The number of leeches that apply a numbing effect, reducing the target's output or disabling certain actions. Also the name of a Necromancer passive. | 2 ||
| `OneUseSpellDamageUp` | Integer | Increases spell damage by the specified amount, but the effect is consumed after a single use. Alias for SpellDamageUp. | 2 ||
| `OverhealGainsBothShield` | Integer | Any healing beyond maximum health also grants shield points equal to the overheal amount. Value controls the conversion rate. | 2 ||
| [`OverHealToStatuses`](Abilities_and_Spells.md#object-overhealtostatuses) | Object | Specifies a set of statuses applied to the target based on the amount of over-healing dealt. | 2 ||
| `ParasitesArentCursed` | Integer | Parasites attached to the unit are not considered cursed items, preventing negative curse effects. Value is a binary flag. | 2 ||
| [`passive0`](./Enums.md#enum-passive0) | Enum | Specifies the first passive ability assigned to the unit from a predefined list (e.g., SelfAssured, HotBlooded). | 2 ||
| [`PassiveAfterXKills`](Items_and_Equipment.md#object-passiveafterxkills) | Object | Activates a set of passive effects (e.g., extra attacks, stat boosts) after the unit achieves a certain number of kills defined by the 'stacks' sub-key. | 2 ||
| [`PassiveAtFullHealth`](Miscellaneous.md#object-passiveatfullhealth) | Object | Applies a set of passive effects (e.g., mana cost reduction, extra damage taken) only while the unit is at maximum health. | 2 ||
| [`PassiveAtInjuryThreshold`](Miscellaneous.md#object-passiveatinjurythreshold) | Object | Applies a set of passive effects when the unit's injury level ('injury' sub-key) meets or exceeds the specified 'threshold' using the comparison 'mode'. | 2 ||
| [`PassiveEnergized`](#object-passiveenergized) | Variable | Enables an electrified visual effect (using Particle_Electric particle) on the unit, indicating a charged or energized state. | 2 ||
| [`PassiveIfWeaponIsUsable`](Items_and_Equipment.md#object-passiveifweaponisusable) | Object | Activates a set of passive effects (e.g., Brace) only if the unit's current weapon is in a usable condition (not broken or disabled). | 2 ||
| [`PassiveTar`](#object-passivetar) | Variable | Enables a dripping tar particle effect (using Particle_TarDrip) on the unit, indicating a tar-related passive. | 2 ||
| [`PassiveUntilCastSpell`](Miscellaneous.md#object-passiveuntilcastspell) | Object | Applies a set of passive effects (e.g., healing allies each turn) that remain active until the unit casts a spell. | 2 ||
| [`PassiveUntilGetKill`](Miscellaneous.md#object-passiveuntilgetkill) | Object | Applies a set of passive effects (e.g., Holy Damage Blessing with burn) that remain active until the unit scores a kill. | 2 ||
| [`PassiveWhenTheAlpha`](Miscellaneous.md#object-passivewhenthealpha) | Object | Activates a set of passive effects (e.g., TogglableRoundEndExtraTurn) only while the unit holds the Alpha status on the team. | 2 ||
| [`PassiveWhileHasStatus`](Cat_Mutations.md#object-passivewhilehasstatus) | Object | An object containing `status` and `passives` that grants the listed passives while the unit has the specified status. | 2 ||
| [`PassiveWhileInMonkMeleeStance`](Items_and_Equipment.md#object-passivewhileinmonkmeleestance) | Object | Applies specific passive effects (e.g., Brace, HealthRegenUp) while the unit is in the Monk's melee combat stance. | 2 ||
| [`PassiveWhileInMonkRangedStance`](Miscellaneous.md#object-passivewhileinmonkrangedstance) | Object | Applies specific passive effects (e.g., AddBonusRange, AddSpellDamage) while the unit is in the Monk's ranged combat stance. | 2 ||
| [`PassiveWhileNotHasStatus`](Characters_and_Bosses.md#object-passivewhilenothasstatus) | Object | Specifies a set of passives that are active only when this unit does not have the given status. | 2 ||
| [`PassiveWhilePreviewingMonkRangedStance`](Miscellaneous.md#object-passivewhilepreviewingmonkrangedstance) | Object | Applies specific passive effects (e.g., AddBonusRange) while the unit is previewing the Monk's ranged stance before committing to it. | 2 ||
| [`PassiveWhileWearingMetal`](Miscellaneous.md#object-passivewhilewearingmetal) | Object | Applies a set of passive effects (e.g., AddElementsToWeapon with Electric) while the unit is equipped with metal armor or accessories. | 2 ||
| `PermanentItems` | Integer | The number of equipment slots that are immune to being unequipped or removed, permanently binding items to those slots. | 2 ||
| `PermanentUpgradeRandomActive` | Integer | The number of random active abilities permanently upgraded. | 2 ||
| `Phasing` | Integer | If set to 1, allows the character to phase through solid objects or obstacles. | 2 ||
| [`PlayerCat_ThiefShade2`](#object-playercat_thiefshade2) | Object | A customization or modifier for the Thief Shade ability variant 2, altering its behavior or appearance for the player cat. | 2 ||
| `PoisonMultiplier` | Integer | A multiplier on all poison damage or poison stack application, increasing the potency of poison effects. | 2 ||
| [`Poop`](Events_and_Encounters.md#object-poop) | Object | A deployable object that acts as a hazard or obstacle, spawning a Poop movieclip with its own name and sound effects. | 2 ||
| `PrioritizeAggroTarget` | Integer | A priority weight for targeting the current aggro target. | 2 ||
| `PrioritizePlayerCats` | Integer | A priority weight for targeting player-controlled cats. | 2 ||
| `PrioritizeWeakestEnemy` | Integer | A priority weight for targeting the weakest enemy unit. | 2 ||
| [`ProtectTargetedAllies`](Characters_and_Bosses.md#object-protecttargetedallies) | Object | Specifies the ability used to protect targeted allies, including an optional target filter. | 2 ||
| [`QuakeAreaChance`](Abilities_and_Spells.md#object-quakeareachance) | Object | An object containing a radius and a chance to trigger a quake area effect. | 2 ||
| `Quiver` | Integer | Grants additional ammunition capacity or reload charges for ranged weapon abilities, increasing how many times they can be fired. | 2 ||
| [`RandomDistanceDisplace`](Abilities_and_Spells.md#object-randomdistancedisplace) | Integer / Object | The number of stacks of a random distance displacement effect, or an object with stacks, min_dist, and chance. | 2 ||
| [`RandomKnockback`](Abilities_and_Spells.md#object-randomknockback) | Object | An object defining the minimum and maximum distance in tiles for a random knockback. | 2 ||
| `RandomLightning` | Integer | Chance per turn or action for a random lightning strike to occur, expressed as a percentage (e.g., 50%). | 2 ||
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 ||
| [`RandomTaggedMutation`](./Enums.md#enum-randomtaggedmutation) | Enum | Specifies the tag to filter random mutations by. | 2 ||
| `RangedTrueShot` | Integer | Ranged attacks cannot miss or be dodged, guaranteeing a hit. Value acts as a binary flag. | 2 ||
| [`RatKing`](#object-ratking) | Object | An ability or entity that spawns or controls a group of rats, applying swarm mechanics or empowered rat effects. | 2 ||
| [`ReaperRevenge`](#object-reaperrevenge) | Object | A teleport-based ability that damages the user while applying buffs (e.g., AllStatsUp) upon arrival at the target location. | 2 ||
| `RebukeDamage` | Integer | The amount of damage dealt by a rebuke backlash effect. | 2 ||
| [`red`](Events_and_Encounters.md#object-red) | Object | Configuration for one of the dialog options (label 'EVENT_RED_ANSW'), with a fixed chance and associated animation, in a choice event. | 2 ||
| [`Reflect`](#object-reflect) | Integer / Object | The amount of reflect stacks applied. | 2 ||
| [`RefreshEquipmentAbilityOnElement`](Items_and_Equipment.md#object-refreshequipmentabilityonelement) | Object | Refreshes the cooldown of the unit's equipment ability when the unit's attack matches the specified element (e.g., Electric), displaying a recharge popup. | 2 ||
| `RefreshMoveOnWeaponConnect` | Integer | Grants an extra move action when the unit successfully lands a weapon hit. Value indicates the number of extra moves. | 2 ||
| [`Regurge`](#object-regurge) | Integer / Object | The number of regurgitation triggers. | 2 ||
| [`Regurge`](#object-regurge) | Integer / Object | The number of regurgitation triggers. | 2 | `1` (Number), `{ ... }` (Object) |
| `ReloadOnKill` | Integer | If set, this ability's reload charge is restored on kill (any kill). | 2 ||
| `ReloadOnKillEnemy` | Integer | If set, this ability's reload charge is restored only when killing an enemy. | 2 ||
| `ReloadOnTotalDamageReceived` | Integer | The threshold of total damage received to restore a reload charge. | 2 ||
| `RemoteLeech` | Integer | The amount of remote leech applied to the target on basic attack. | 2 ||
| `RemoveLineOfSightRestrictions` | Integer | Line of sight requirements for targeting are ignored, allowing the unit to target any visible cell regardless of obstacles. | 2 ||
| `RemoveOncePerFightRestriction` | Integer | Abilities or effects with a 'once per fight' limitation can be used multiple times per fight. Value acts as a binary flag. | 2 ||
| `RepairArmorCondition` | Integer | The amount of armor condition restored. | 2 ||
| [`ReplaceBasicAttack_Mutation`](./Enums.md#enum-replacebasicattack_mutation) | Enum | Specifies the mutation-based ability (e.g., FetusSpit) that replaces the unit's standard basic attack. | 2 ||
| [`ReplaceBasicAttackWhenDead`](./Enums.md#enum-replacebasicattackwhendead) | Enum | Specifies the ability (e.g., Haunt) that replaces the unit's basic attack when it is in a dead state. | 2 ||
| [`ReplaceBrain`](Characters_and_Bosses.md#object-replacebrain) | Object | Defines a replacement AI brain and behavior pattern for the mutant. | 2 ||
| [`ReplaceSpellsWhenDead`](./Enums.md#enum-replacespellswhendead) | Enum | Specifies the spell set (e.g., Spook) that replaces the unit's normal spell list when it is in a dead state. | 2 ||
| `ResetArmorShield` | Integer | The amount of armor shield restored. | 2 ||
| `ReturnBoundItemOnBattleEnd` | Integer | If set to 1, items bound to this character are returned to their owner at the end of battle. | 2 ||
| `ReviveOnWin` | Integer | Chance (as a percentage) for the unit to automatically revive after the battle ends, if it was dead at the time of victory. | 2 ||
| [`Robot`](Characters_and_Bosses.md#object-robot) | Integer / Object | If an integer 1, the unit is robotic and affected by electric/energized effects. If an object, contains further robot-specific properties. | 2 ||
| [`robot`](Characters_and_Bosses.md#object-robot) | Variable | Indicates the unit is considered a robotic entity, potentially sharing interactions or restrictions with mechanical/robot-related systems. | 2 ||
| `RobotsInheritArmor` | Integer | Robots summoned or controlled by the unit inherit a percentage of the unit's armor value. Value controls the inheritance amount. | 2 ||
| `RockDetector` | Integer | Grants the ability to detect or sense rock-type objects or terrain within the specified range (e.g., 10 tiles). | 2 ||
| `SafeExplosions` | Integer | Explosions caused by the unit do not damage friendly units. Value acts as a binary flag. | 2 ||
| [`Sandstorm`](#object-sandstorm) | Object | A self-buff ability that creates a sandstorm, applying a status effect (may be 'Sandstorm 1' or an object definition with a specific template). | 2 ||
| [`Sandstorm`](#object-sandstorm) | Object | A self-buff ability that creates a sandstorm, applying a status effect (may be 'Sandstorm 1' or an object definition with a specific template). | 2 | `1` (Number), `{ ... }` (Object) |
| [`ScaledStatusOnLoseShield`](Miscellaneous.md#object-scaledstatusonloseshield) | Object | Applies a scaled status effect (e.g., Thorns proportional to shield lost) when the unit loses shield points. Value includes a 'shield' sub-key for threshold. | 2 ||
| [`ScaledStatusOnOverHealed`](Miscellaneous.md#object-scaledstatusonoverhealed) | Object | An object containing status effect definitions to apply when the unit receives healing that exceeds its maximum health, with the number of stacks scaled by the amount of over-healing. | 2 ||
| [`ScaledStatusOnOverMana`](Miscellaneous.md#object-scaledstatusonovermana) | Object | An object containing status effect definitions to apply when the unit gains mana that exceeds its maximum mana, with the number of stacks scaled by the amount of over-mana. | 2 ||
| [`ScaledStatusOnSpendMana`](Items_and_Equipment.md#object-scaledstatusonspendmana) | Object | An object containing status effect definitions to apply when the unit spends mana, with the number of stacks scaled by the amount of mana spent. | 2 ||
| `ScrambleEverything` | Integer | The percentage chance to scramble all abilities and passives on the target. | 2 ||
| [`SecurityBotProtect`](Characters_and_Bosses.md#object-securitybotprotect) | Object | Specifies the ability and movement used by a security bot to protect allies. | 2 ||
| `SelfStatusCarefulness` | Integer | The carefulness level when applying statuses to self, used to control stacking. | 2 ||
| [`SelfStun`](./Arrays.md#array-selfstun) | Array / Integer | The number of stacks of self-stun applied, with an optional probability as a second element. | 2 ||
| [`SetDefaultFace`](./Enums.md#enum-setdefaultface) | Enum | Specifies the default facial expression, such as 'happy', 'sad', or 'insane'. | 2 ||
| [`SetItemAux`](#object-setitemaux) | Object | Configures an item's auxiliary value by specifying a target slot and a formula for the new value. | 2 ||
| `SetSpellCosts` | Integer | Overrides the cost of all spells to this value. | 2 ||
| [`Shadowstep`](#object-shadowstep) | Object | An object defining the Shadowstep ability, which allows the unit to teleport behind a target before an attack. | 2 ||
| `ShareHealthRegen` | Integer | The amount of health regeneration shared with nearby allies. | 2 ||
| [`SharePickups`](Characters_and_Bosses.md#object-sharepickups) | Object | If 1 or an object with include_coins, makes the unit share pickups with nearby allies. | 2 ||
| [`Shatter`](#object-shatter) | Integer / Object | The amount of damage dealt when a frozen or petrified status is shattered, or a template definition for a Shatter ability. | 2 ||
| [`ShortCircuit`](#object-shortcircuit) | Integer / Object | The number of stacks of the ShortCircuit status effect. | 2 ||
| [`ShortCircuit`](#object-shortcircuit) | Integer / Object | The number of stacks of the ShortCircuit status effect. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `ShoulderCheck` | Integer | The chance (as a percentage) to perform a Shoulder Check, pushing a target back after a melee attack. | 2 ||
| [`ShovingMatch`](./Enums.md#enum-shovingmatch) | Enum | Determines which stat (e.g., 'attack') is used for the Shoving Match shoving contest. | 2 ||
| `SignalFinalBossShieldBroke` | Integer | If set to a non-zero number, signals that the final boss's shield has been broken. | 2 ||
| [`SleepDart2`](#object-sleepdart2) | Object | An object defining the Sleep Dart 2 status, which puts a target to sleep on hit. | 2 ||
| [`SlotMachineRollPool`](Characters_and_Bosses.md#object-slotmachinerollpool) | Object | Defines the weighted pool of possible slot machine roll results. | 2 ||
| `SmallEnemiesIgnoreYou` | Integer | If non-zero, enemies considered 'small' will ignore this unit and not target it. | 2 ||
| [`SmellBlood`](#object-smellblood) | Integer / Object | If non-zero, activates the Smell Blood ability which reveals nearby injured units. | 2 ||
| [`SmellBlood`](#object-smellblood) | Integer / Object | If non-zero, activates the Smell Blood ability which reveals nearby injured units. | 2 | `1` (Number), `{ ... }` (Object) |
| [`SmiteEnemiesWhoKill`](Miscellaneous.md#object-smiteenemieswhokill) | Object | An object defining a smite effect applied to enemies who kill another unit, typically dealing damage and applying a stun. | 2 ||
| [`SparkleBuff`](#object-sparklebuff) | Variable | A variable defining a sparkle particle effect buffer for visual feedback. | 2 ||
| `SpawnBearTrapOnMiss` | Integer | The number of bear traps to spawn on the tile adjacent to the target when the unit misses an attack. | 2 ||
| [`SpawnCatCopyWhenDowned`](Miscellaneous.md#object-spawncatcopywhendowned) | Object | An object defining a cat copy to spawn when the unit is downed, typically a shade or specter. | 2 ||
| [`SpawnExtraThingsOnBattleStart`](Cat_Mutations.md#object-spawnextrathingsonbattlestart) | Object | An object with `object` and `number` (or range) defining what and how many objects to spawn at battle start. | 2 ||
| [`SpawnItemLinkedFamiliar`](Items_and_Equipment.md#object-spawnitemlinkedfamiliar) | Object | An object defining a familiar to spawn that is linked to a specific item, which breaks when the familiar is defeated. | 2 ||
| [`SpawnMeatOnMove`](./Enums.md#enum-spawnmeatonmove) | Enum | Specifies the type of meat object (e.g., 'Food') to spawn on the tile the unit moves from. | 2 ||
| `SpawnNearEnemies` | Integer | The number of units to spawn near each enemy at the start of battle. | 2 ||
| [`SpawnObjectOnPopCorpse`](Items_and_Equipment.md#object-spawnobjectonpopcorpse) | Enum / Object | Specifies an object (as a string or an object with 'object', 'count', 'except_tiny' keys) to spawn on a corpse when it is popped. | 2 ||
| [`SpecialFriends`](Miscellaneous.md#object-specialfriends) | Object | An object containing a set of status effects applied to allied units that are considered 'special friends' (e.g., granted by a passive). | 2 ||
| [`SpecialGodRays`](#object-specialgodrays) | Object | An object defining visual god rays that follow a specific character tag, used for cinematic or boss effects. | 2 ||
| [`SpikeBuff`](#object-spikebuff) | Variable | A variable defining a spike/bramble particle effect buffer for visual feedback. | 2 ||
| `SplittableMove` | Integer | The number of times a move action can be split into smaller segments. | 2 ||
| [`Spook`](#object-spook) | Object | An object defining the Spook status, which causes the affected unit to flee or become frightened. | 2 ||
| `SpreadExtraDebuffs` | Integer | The number of additional debuffs to spread to nearby enemies when applying a debuff. | 2 ||
| `SpreadPainBonus` | Integer | The amount of bonus damage dealt to enemies who are also affected by the Spread Pain effect. | 2 ||
| `SpreadPainBonusCrit` | Integer | The additional critical hit chance against enemies affected by Spread Pain. | 2 ||
| [`StackingDodgeChanceOnTookDamage`](Miscellaneous.md#object-stackingdodgechanceontookdamage) | Object | An object with 'amount' (percent) and 'cap' (percent) defining a stacking dodge chance buff that increases each time the unit takes damage, up to a maximum. | 2 ||
| `StatMinimum` | Integer | The minimum value that a particular stat cannot fall below. | 2 ||
| [`StatsAtLowHealth`](Miscellaneous.md#object-statsatlowhealth) | Object | An object containing a 'threshold' (health value) and stat bonuses (e.g., 'strength', 'speed') that are applied when the unit's health is below the threshold. | 2 ||
| [`StatusAfterCastSpell`](Items_and_Equipment.md#object-statusaftercastspell) | Object | An object containing status effects to apply to the unit immediately after it casts any spell. | 2 ||
| [`StatusAfterXTurns`](Characters_and_Bosses.md#object-statusafterxturns) | Object | Applies a status effect or forces an ability usage after a set number of turns. | 2 ||
| [`StatusAlliesOnBattleStart`](Items_and_Equipment.md#object-statusalliesonbattlestart) | Object | An object containing status effects to apply to all allies at the start of battle. | 2 ||
| [`StatusAlliesOnGainCoins`](Miscellaneous.md#object-statusalliesongaincoins) | Object | An object containing status effects to apply to allies when the unit gains coins, with an optional 'scaled' boolean to scale stacks. | 2 ||
| [`StatusAlliesOnKill`](Miscellaneous.md#object-statusalliesonkill) | Object | An object containing status effects to apply to all allies when any ally kills an enemy. | 2 ||
| [`StatusAlliesOnSpendMana`](Miscellaneous.md#object-statusalliesonspendmana) | Object | An object containing status effects to apply to allies when the unit spends mana. | 2 ||
| [`StatusAlliesScaledByCursedOnDeath`](Miscellaneous.md#object-statusalliesscaledbycursedondeath) | Object | An object containing status effects to apply to allies when the unit dies, with stacks scaled by the number of Cursed stacks the unit had. | 2 ||
| [`StatusAllyWhenAllySpendsMana`](Miscellaneous.md#object-statusallywhenallyspendsmana) | Object | An object with a 'threshold' (mana amount) and status effects to apply to an ally whenever any ally spends at least that much mana. | 2 ||
| [`StatusAnyCatAllyWhoKills`](Miscellaneous.md#object-statusanycatallywhokills) | Object | An object containing status effects to apply to any cat ally who kills an enemy. | 2 ||
| `StatusCarefulness` | Integer | The carefulness level when applying statuses, used to control stacking behavior. | 2 ||
| [`StatusCharactersOnRoundStart`](#object-statuscharactersonroundstart) | Object | An object containing status effects to apply to all characters on the battlefield at the start of each round. | 2 ||
| [`StatusDamagers`](Miscellaneous.md#object-statusdamagers) | Object | An object defining status effects that damage the unit, with parameters for each status. | 2 ||
| [`StatusEachRoundEnd`](Cat_Mutations.md#object-statuseachroundend) | Object | An object listing status effects applied to the unit at the end of each round. | 2 ||
| [`StatusEachTurnEndForEachTurn`](Characters_and_Bosses.md#object-statuseachturnendforeachturn) | Object | Statuses applied at the end of each turn, with the number of turns as nested values. | 2 ||
| [`StatusEachTurnEndPerEnemyKill`](Miscellaneous.md#object-statuseachturnendperenemykill) | Object | An object containing status effects to apply at the end of each turn for each enemy killed during that turn. | 2 ||
| [`StatusEnemiesOnDeath`](Miscellaneous.md#object-statusenemiesondeath) | Object | An object containing status effects to apply to all enemies when the unit dies. | 2 ||
| [`StatusEveryXSpellCastsEachTurn`](Cat_Mutations.md#object-statuseveryxspellcastseachturn) | Object | An object with a 'stacks' value defining status effects applied every X spell casts within a single turn. | 2 ||
| [`StatusEveryXTurnBegins`](Miscellaneous.md#object-statuseveryxturnbegins) | Object | An object with a 'turns' value defining status effects applied every X turns at the start of the turn. | 2 ||
| [`StatusIfDidntMove`](Cat_Mutations.md#object-statusifdidntmove) | Object | An object containing status effects to apply to the unit if it did not move during its turn. | 2 ||
| [`StatusIfUnusedActPoints`](Items_and_Equipment.md#object-statusifunusedactpoints) | Object | An object containing status effects to apply to the unit if it has unused action points at the end of its turn. | 2 ||
| [`StatusKillers`](Abilities_and_Spells.md#object-statuskillers) | Object | An object containing nested conditionals that apply status effects when the unit kills an enemy. | 2 ||
| [`StatusOnAnyDeath`](Miscellaneous.md#object-statusonanydeath) | Object | An object containing status effects to apply whenever any unit (ally or enemy) dies. | 2 ||
| [`StatusOnBackstab`](Items_and_Equipment.md#object-statusonbackstab) | Object | An object containing status effects to apply when the unit performs a backstab attack. | 2 ||
| [`StatusOnBattleEndIfKillThresholdMet`](Miscellaneous.md#object-statusonbattleendifkillthresholdmet) | Object | An object containing a 'kills' threshold and status effects to apply at the end of battle if the unit's kill count meets or exceeds the threshold. | 2 ||
| [`StatusOnBattleStart`](Items_and_Equipment.md#object-statusonbattlestart) | Object | An object containing status effects to apply to the unit at the start of every battle. | 2 ||
| [`StatusOnBreakItem`](Items_and_Equipment.md#object-statusonbreakitem) | Object | An object containing status effects to apply when the unit breaks a weapon or armor item. | 2 ||
| [`StatusOnCollectPickup`](Items_and_Equipment.md#object-statusoncollectpickup) | Object | An object containing status effects to apply when the unit collects a pickup item. | 2 ||
| [`StatusOnDealtDamage`](Miscellaneous.md#object-statusondealtdamage) | Object | An object containing status effects to apply to the unit whenever it deals damage to an enemy. | 2 ||
| [`StatusOnDealtDamageThreshold`](Miscellaneous.md#object-statusondealtdamagethreshold) | Object | Specifies the effects applied when the unit deals damage equal to or exceeding the defined threshold. | 2 ||
| [`StatusOnDie`](Cat_Mutations.md#object-statusondie) | Object | Specifies status effects or actions triggered when the unit dies. | 2 ||
| [`StatusOnEatPill`](Miscellaneous.md#object-statusoneatpill) | Object | Specifies the effects applied when the unit consumes a pill item. | 2 ||
| [`StatusOnGainShield`](Miscellaneous.md#object-statusongainshield) | Object | Specifies the effects applied when the unit gains a shield. | 2 ||
| [`StatusOnHeal`](Miscellaneous.md#object-statusonheal) | Object | Specifies the effects applied when the unit receives healing. | 2 ||
| [`StatusOnKillEnemy`](Items_and_Equipment.md#object-statusonkillenemy) | Object | Specifies the effects applied when the unit kills an enemy. | 2 ||
| [`StatusOnOverMana`](Miscellaneous.md#object-statusonovermana) | Object | Specifies the effects applied when the unit's mana exceeds its maximum. | 2 ||
| [`StatusOnPickupCoins`](Items_and_Equipment.md#object-statusonpickupcoins) | Object | Specifies the effects applied when the unit picks up coins. | 2 ||
| [`StatusOnPopCorpse`](Items_and_Equipment.md#object-statusonpopcorpse) | Object | Specifies the effects applied when the unit pops a corpse. | 2 ||
| [`StatusOnSetPieceBreak`](Miscellaneous.md#object-statusonsetpiecebreak) | Object | Specifies the effects applied when the unit breaks a set piece. | 2 ||
| [`StatusOnSpawnIn`](Characters_and_Bosses.md#object-statusonspawnin) | Object | Applies statuses or actions upon the unit spawning into the battlefield. | 2 ||
| [`StatusOnTookDamageFromEnemyAbility`](Miscellaneous.md#object-statusontookdamagefromenemyability) | Object | Specifies the effects applied when the unit takes damage from an enemy ability. | 2 ||
| [`StatusOnTriggerTrap`](Miscellaneous.md#object-statusontriggertrap) | Object | Specifies the effects applied when the unit triggers a trap. | 2 ||
| [`StatusOnUseBasicAttack`](Items_and_Equipment.md#object-statusonusebasicattack) | Object | Specifies the effects applied when the unit performs a basic attack. | 2 ||
| [`StatusOnUseElementAbility`](Miscellaneous.md#object-statusonuseelementability) | Object | Specifies the effects applied when the unit uses an ability matching the specified element. | 2 ||
| [`StatusPerInjury`](Miscellaneous.md#object-statusperinjury) | Object | Specifies the effects granted per injury the unit has, up to an optional cap. | 2 ||
| [`StatusReplacement`](./Arrays.md#array-statusreplacement) | Array | Specifies status replacements, where the first status is replaced by the second when applied. | 2 ||
| [`StatusThingsKnockedBack`](Miscellaneous.md#object-statusthingsknockedback) | Object | Specifies the effects applied when the unit knocks back another unit. | 2 ||
| [`StatusWhenAllySpendsMana`](Items_and_Equipment.md#object-statuswhenallyspendsmana) | Object | Specifies the effects applied when an ally spends mana. | 2 ||
| `StrengthForEachNeighboringEnemy` | Integer | The amount of strength gained for each adjacent enemy. | 2 ||
| `StrengthInNumbersAura` | Integer | The amount of strength gained per nearby ally within the aura. | 2 ||
| `Study` | Integer | The number of stacks of the Study status applied. | 2 ||
| `SurviveAt1HP` | Integer | If 1, the unit survives a fatal hit with 1 HP instead of dying. | 2 ||
| `SwallowSmallCharacter` | Integer | The percentage chance to swallow a smaller character on hit. | 2 ||
| `SwapHighestAndLowestStat` | Integer | If non-zero, swaps the unit's highest base stat value with its lowest. | 2 ||
| [`Switcheroo`](#object-switcheroo) | Integer / Object | The number of stacks of the Switcheroo status effect. | 2 ||
| [`Switcheroo`](#object-switcheroo) | Integer / Object | The number of stacks of the Switcheroo status effect. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`TaggedPickupEffectReplacement`](Miscellaneous.md#object-taggedpickupeffectreplacement) | Object | Specifies a replacement effect for picking up items with a given tag. | 2 ||
| `TempCounterAttack` | Integer | The number of turns TempCounterAttack lasts, ticking down at the start of the unit's turn. | 2 ||
| `TempCritChanceUp` | Integer | The amount of temporary critical hit chance (in percentage points) added. | 2 ||
| `TempNoManaRegen` | Integer | The number of turns the unit cannot regenerate mana. | 2 ||
| `ThornsDamageImmuneUntilSettled` | Integer | The number of turns the target is immune to thorns damage until it settles. | 2 ||
| `TileDamageImmuneUntilSettled` | Integer | The number of turns the target is immune to tile damage until it settles. | 2 ||
| `TileDamageMultiplier` | Integer | Multiplier for damage dealt to environmental tiles. | 2 ||
| [`TinkererBasicAttackSwitching`](Cat_Classes.md#object-tinkererbasicattackswitching) | Object | Defines the abilities used for the Tinkerer's basic attack switching mechanic. | 2 ||
| [`TowerDefense`](Miscellaneous.md#object-towerdefense) | Object | Specifies the range and damage of the Tower Defense counterattack. | 2 ||
| [`TowerDefenseReflex`](./Enums.md#enum-towerdefensereflex) | Enum | Specifies the ability or attack used when the unit counterattacks in tower defense reflex mode. | 2 ||
| [`TradeLife`](#object-tradelife) | Integer / Object | The amount of health life traded, or a template for a TradeLife ability. | 2 ||
| [`TradeLife`](#object-tradelife) | Integer / Object | The amount of health life traded, or a template for a TradeLife ability. | 2 | `1` (Number), `{ ... }` (Object) |
| [`TrailBlazer`](#object-trailblazer) | Enum / Integer / Object | The number of trail blazer stacks applied, or a string alias like 'mov'. | 2 ||
| [`TrailBlazer`](#object-trailblazer) | Enum / Integer / Object | The number of trail blazer stacks applied, or a string alias like 'mov'. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`TransformOnElementInfluencex`](Characters_and_Bosses.md#object-transformonelementinfluencex) | Object | Transforms into a specified object when influenced by a given element. | 2 ||
| [`TransformWhenBuddyDies`](./Enums.md#enum-transformwhenbuddydies) | Enum | Specifies the form the unit transforms into when its buddy dies. | 2 ||
| `TrapEffectsMultiplier` | Integer | Multiplier for the potency of trap effects triggered by the unit. | 2 ||
| `TriggerDOTStatuses` | Integer | If set to 1, triggers damage over time statuses on the target immediately. | 2 ||
| `triggers_limit` | Integer | The maximum number of times this passive effect can trigger per battle. | 2 ||
| `TrinketActiveEffectsMultiplierBonus` | Integer | Bonus multiplier to the active effects of equipped trinkets. | 2 ||
| `TrinketPassiveMultiplierBonus` | Integer | Bonus multiplier to the passive effects of equipped trinkets. | 2 ||
| `UncappedHP` | Integer | If 1, the unit's maximum HP is not capped by standard limits. | 2 ||
| `UncappedHPBonusStr` | Integer | The amount of strength gained per point of HP exceeding the maximum cap. | 2 ||
| `Uncontrollable` | Integer | If non-zero, the unit becomes uncontrollable by the player. | 2 ||
| `UnlockOrientation` | Integer | If 1, allows the unit to freely rotate or face any direction regardless of movement. | 2 ||
| [`UpgradeLevelUpClassActives`](./Enums.md#enum-upgradelevelupclassactives) | Enum | Specifies the upgrade path for class active abilities on level up. | 2 ||
| [`UpgradeLevelUpClassPassives`](./Enums.md#enum-upgradelevelupclasspassives) | Enum | Specifies the upgrade path for class passive abilities on level up. | 2 ||
| `UpgradeSpawnedPickups` | Integer | The number of times spawned pickups are upgraded in quality. | 2 ||
| [`UpgradeTaggedSpawnsToChampions`](./Enums.md#enum-upgradetaggedspawnstochampions) | Enum | Specifies which tag of spawns are upgraded to champion versions. | 2 ||
| `Vengeful` | Integer | The number of Vengeful stacks, causing retaliation damage when hit. | 2 ||
| `VisualFlySwarm` | Integer | If non-zero, enables the visual fly swarm effect on the unit. | 2 ||
| `WeaponActiveEffectsMultiplierBonus` | Integer | Bonus multiplier to the active effects of the equipped weapon. | 2 ||
| `WeaponCountsAsBasicAttack` | Integer | If non-zero, the weapon's ability counts as a basic attack. | 2 ||
| `WeaponDamageMultiplierBonus` | Integer | Bonus multiplier to weapon damage. | 2 ||
| `WeaponPassiveMultiplierBonus` | Integer | Bonus multiplier to the passive effects of the equipped weapon. | 2 ||
| `WeaponsDontLoseDurability` | Integer | If set to 1, weapons equipped by this unit do not lose durability. | 2 ||
| [`XIsLivingCharactersWithTag`](./Enums.md#enum-xislivingcharacterswithtag) | Enum | Specifies the tag that living characters must have for this passive to affect them. | 2 ||
| `XIsOtherHealsThisTurn` | Integer | If set, tracks other heals this turn for some effect. | 2 ||
| [`XIsSpellStormRampAndReset`](Abilities_and_Spells.md#object-xisspellstormrampandreset) | Integer / Object | If integer 0, resets stacks; if object, contains 'stacks' and 'reset_percent' for spell storm ramp. | 2 ||
| [`XIsTargetHealth`](Abilities_and_Spells.md#object-xistargethealth) | Object | Evaluates a bonus damage formula where X is the target's current health. | 2 ||
| `XIsTimesDamageTaken` | Integer | If set, multiplier for damage taken to apply some effect. | 2 ||
| `Zombie` | Number | The number of stacks or value for the Zombie status. | 2 ||
| `AbilityDamageMultiplier` | Float | Multiplier for all ability damage dealt by the unit. | 1 ||
| `AbilityDisableIfLivingCrow` | Integer | If set, disables the ability if there is a living crow on the field. | 1 ||
| `AbilityEnabledAtHealthThreshold` | Integer | The health percentage threshold at which the ability becomes enabled. | 1 ||
| `AbilityEnabledIfBasicAttackUsedThisTurn` | Integer | If set, ability is enabled only if the unit used a basic attack this turn. | 1 ||
| `AbilityEnabledIfMovementTrapped` | Integer | If set, ability is enabled only when the unit's movement is trapped. | 1 ||
| `AbilityEnabledIfNoAggroTarget` | Integer | If set, ability is enabled only when the unit has no aggro target. | 1 ||
| [`AbilityEnabledIfNotHasStatus`](./Enums.md#enum-abilityenabledifnothasstatus) | Enum | Specifies the status that must be absent for ability to be enabled. | 1 ||
| [`AbilityEnabledIfSpecificItemEquipped`](./Enums.md#enum-abilityenabledifspecificitemequipped) | Enum | Specifies the item that must be equipped for ability to be enabled. | 1 ||
| [`AbilityOnBattleStart_UseAI`](./Enums.md#enum-abilityonbattlestart_useai) | Enum | Specifies the ability the unit will use at the start of battle via AI resolution. | 1 ||
| [`AbilityOnRoundEndOnce`](Items_and_Equipment.md#object-abilityonroundendonce) | Object | Specifies an ability to be used once at the end of the round. | 1 ||
| `AbsorbManaFromOtherSpells` | Integer | If set, this ability absorbs mana from other spells when cast. | 1 ||
| `AcidRain` | Integer | If non-zero, enables the Acid Rain weather effect dealing damage each turn. | 1 ||
| [`AddAdvantageToEvent`](Items_and_Equipment.md#object-addadvantagetoevent) | Object | Specifies additional advantage options to add to a specific event type. | 1 ||
| `AddAllyNeighborsToAttackRange` | Integer | The number of ally-occupied tiles added to the unit's attack range. | 1 ||
| `AddConstitution` | Integer | The amount of constitution added to the unit. | 1 ||
| [`AddElementsToSpells`](./Enums.md#enum-addelementstospells) | Enum | Specifies which element to add to spells. | 1 ||
| `AddExtraTurnsBeforeRun` | Integer | The number of additional turns added before the run ends. | 1 ||
| `AddLevelUpStatMultiplier` | Integer | Multiplier applied to stat gains on level up. | 1 ||
| [`AddPostProcessEffect`](#object-addpostprocesseffect) | Object | Specifies a post-process shader effect to apply to the scene. | 1 ||
| `AddRandomEliteBuff` | Integer | The number of random elite buffs to apply to the unit. | 1 ||
| [`AddStatusesIfPersistentWeatherElement`](Miscellaneous.md#object-addstatusesifpersistentweatherelement) | Object | Specifies statuses applied if the persistent weather matches the given elements. | 1 ||
| [`AddStatusesToReceivedElementalDamage`](Miscellaneous.md#object-addstatusestoreceivedelementaldamage) | Object | An object defining statuses applied to the unit when it takes elemental damage of the specified types. | 1 ||
| [`AddStatusToBackstabs`](Items_and_Equipment.md#object-addstatustobackstabs) | Object | An object defining statuses applied to the target when the unit performs a backstab attack. | 1 ||
| [`AddStatusToFirstSpellEachTurn`](Miscellaneous.md#object-addstatustofirstspelleachturn) | Object | An object defining statuses applied to the target after the first spell cast by the unit each turn. | 1 ||
| [`AddStatusToReceivedDamage`](Characters_and_Bosses.md#object-addstatustoreceiveddamage) | Object | Applies a status effect to the attacker when the unit takes damage. | 1 ||
| [`AddStatusToReceivedDamage_ExcludeStatuses`](Miscellaneous.md#object-addstatustoreceiveddamage_excludestatuses) | Object | An object defining statuses applied to the attacking unit when the owner receives damage, excluding damage from sources carrying the specified statuses. | 1 ||
| [`AddTilesetObjects`](#object-addtilesetobjects) | Object | An object configuring the spawning of decorative debris or objects on the tileset for an effect. | 1 ||
| `Adrenaline` | Integer | The flat amount of Adrenaline (a resource or stat) granted to the unit. | 1 ||
| [`AdvancedTint`](./Arrays.md#array-advancedtint) | Array | An RGBA color array for advanced sprite tinting. | 1 ||
| [`AdventureTokenPassivePool`](Characters_and_Bosses.md#object-adventuretokenpassivepool) | Object | A pool of passive definitions granted to the unit when picked up as an adventure token. | 1 ||
| [`AggroTargetIsGovernedByHitEffect`](Characters_and_Bosses.md#object-aggrotargetisgovernedbyhiteffect) | Object | If set, the aggro target is determined by the unit's hit effect, with a sub-key for enemies_only. | 1 ||
| `AggroTargetIsLastEnemyThatDealtDamage` | Integer | If 1, the unit's aggro target is the last enemy that damaged it. | 1 ||
| `AggroTargetIsLowestHealthEnemyTillItDies` | Integer | If 1, the unit focuses the lowest health enemy until that enemy dies. | 1 ||
| `AggroTargetIsLowestMaxHealthCat` | Integer | If 1, the unit targets the cat ally with the lowest maximum health. | 1 ||
| [`AIControlNextTurn`](Items_and_Equipment.md#object-aicontrolnextturn) | Object | An object that causes the unit to be controlled by the AI on its next turn, with configurable stacks and spell usage. | 1 ||
| `AIFavorLowHealth` | Integer | The AI's favorability weight for targeting low-health units. | 1 ||
| [`AlienBeastDangerZones`](./Arrays.md#array-alienbeastdangerzones) | Array | An array of ability names that mark dangerous zones for the Alien Beast fight. | 1 ||
| `AlienBeastEyeStalks` | Integer | The number of eye stalk segments on the Alien Beast. | 1 ||
| `all_spells` | Variable | A variable representing a collection of every spell definition available in the game. | 1 ||
| `AlliesScrambleSpellAfterCast` | Integer | The number of times an ally's next spell cast will be scrambled (randomly redirected or modified) after the owner casts a spell. | 1 ||
| `AlliesTakeExtraTurn` | Integer | The number of extra turns granted to allies. | 1 ||
| `AllSpellsCostActPoints` | Integer | If 1, all spells require action points instead of mana or other resources. | 1 ||
| `AllSpellsCostCharge` | Integer | The number of charges required to cast any spell, adding a universal charge cost. | 1 ||
| [`AllStatsAura`](Characters_and_Bosses.md#object-allstatsaura) | Object | An aura that grants bonus stacks of all stats to allies within range. | 1 ||
| `AllUnitsExplodeOnDeath` | Integer | The radius of the explosion that triggers when any unit dies. | 1 ||
| [`AlluringDoodieEater`](Items_and_Equipment.md#object-alluringdoodieeater) | Object | An object defining the chance and damage instance for a unit that consumes an alluring doodie. | 1 ||
| [`AllyDodgeChanceAura`](Items_and_Equipment.md#object-allydodgechanceaura) | Object | An object granting allies within a specified range a percentage chance to dodge incoming attacks. | 1 ||
| `AlphaAllStatsUp` | Integer | The amount by which all of the unit's stats are increased if it is the alpha (highest stat total or designated leader). | 1 ||
| `AlphaDodgeChance` | Integer | The dodge chance granted to the alpha (leader) unit. | 1 ||
| [`AlphaStatusOnTurnBegin`](Abilities_and_Spells.md#object-alphastatusonturnbegin) | Object | Specifies status effects applied to the alpha at the start of each turn. | 1 ||
| [`AlternateIdleAnimation`](./Enums.md#enum-alternateidleanimation) | Enum | Specifies the name of an alternative idle animation to play. | 1 ||
| `AlwaysChosenForLevelUp` | Integer | If set to 1, this unit is always presented as a level-up option when gaining a level. | 1 ||
| `AOEBonus` | Integer | The bonus number of additional targets or tiles affected by an area-of-effect ability. | 1 ||
| [`ApplyPassivesToSpawnerWhileAlive`](Abilities_and_Spells.md#object-applypassivestospawnerwhilealive) | Object | An object defining passives that are applied to the spawner while this unit is alive. | 1 ||
| `ApplyShieldToApplierBasedOnMaxHealth` | Integer | The amount of shield applied to the applier based on a fraction of their max health. | 1 ||
| [`ApplyStatusesNextTurnBegin`](Abilities_and_Spells.md#object-applystatusesnextturnbegin) | Object | Specifies a set of statuses to apply to the target at the beginning of their next turn. | 1 ||
| [`ApplyToOthersWithSharedTagAndFaction`](Abilities_and_Spells.md#object-applytootherswithsharedtagandfaction) | Object | Specifies statuses to apply to other units that share a tag and faction with the target. | 1 ||
| [`ApplyToRandomClosestAlly`](Abilities_and_Spells.md#object-applytorandomclosestally) | Object | Specifies statuses to apply to a random ally closest to the target. | 1 ||
| [`Autism`](Miscellaneous.md#object-autism) | Object | An object defining the Autism disorder, including its name, description, class, and stat modifications for innate and learned levels. | 1 ||
| `AvoidDamagingCharmedEnemies` | Integer | If 1, the unit avoids dealing damage to charmed enemies. | 1 ||
| `AwardCoinsOnDeath` | Integer | The amount of coins awarded to the killer when this unit dies. | 1 ||
| `BackstabWeakness` | Float | A multiplier for damage taken from backstab attacks. | 1 ||
| `BalanceStats` | Integer | If set to 1, the unit's stats are balanced (redistributed) towards an average value. | 1 ||
| `BasicAIDangerZone` | Integer | The radius of the danger zone used by the basic AI for area denial. | 1 ||
| [`BasicAttackStatusSwap`](./Arrays.md#array-basicattackstatusswap) | Array | An array of two status IDs; when the unit performs a basic attack, the first status is removed and the second is applied in its place. | 1 ||
| [`BasicButcherMelee`](#object-basicbutchermelee) | Object | An object defining a basic melee attack for the Butcher class. | 1 ||
| [`BasicDruidAbility`](#object-basicdruidability) | Object | An object defining a basic ability for the Druid class. | 1 ||
| [`BasicMagicShortRanged`](#object-basicmagicshortranged) | Object | An object defining a basic short-ranged magical attack. | 1 ||
| [`BasicMedicMelee`](#object-basicmedicmelee) | Object | An object defining a basic melee attack for the Medic class. | 1 ||
| [`BasicMelee_4Hits`](#object-basicmelee_4hits) | Object | An object defining a variant of the basic melee attack that hits the target 4 times. | 1 ||
| [`BasicNecroRanged`](#object-basicnecroranged) | Object | An object defining a basic ranged attack for the Necromancer class. | 1 ||
| [`BasicPsychicPull`](#object-basicpsychicpull) | Object | An object defining a basic psychic ability that pulls a target towards the caster. | 1 ||
| [`BattlefieldUniqueRandomPassive`](Characters_and_Bosses.md#object-battlefielduniquerandompassive) | Object | A pool of unique random passives that can be applied to each battlefield instance. | 1 ||
| [`BBTransformMutant`](#object-bbtransformmutant) | Object | An object defining a transformation spell that turns the unit into a mutant. | 1 ||
| [`BBTransformZealot`](#object-bbtransformzealot) | Object | An object defining a transformation spell that turns the unit into a zealot. | 1 ||
| [`BiggestFood`](Engine_LogicKeys.md#object-biggestfood) | Integer / Object | The number of biggest food pickups spawned. | 1 ||
| `BigSplashDamage` | Integer | The additional tile radius of the splash damage effect applied by an attack. | 1 ||
| `BlackHolePassive` | Integer | If 1, the unit has black hole passive mechanics. | 1 ||
| `BlackHoleSuck` | Integer | The strength of the black hole's pull effect. | 1 ||
| `BlessingOfPeace` | Integer | The number of stacks of the Blessing of Peace status applied to the unit each turn. | 1 ||
| [`BloatEyeMovement2`](#object-bloateyemovement2) | Object | An object defining a movement ability for the Bloat Eye enemy. | 1 ||
| [`BloatEyePassive2`](./Enums.md#enum-bloateyepassive2) | Enum | Specifies the movement ability for the Bloat Eye enemy. | 1 ||
| [`BloatyExplodey`](#object-bloatyexplodey) | Object | An object defining a spell that causes the target to become bloated and explode. | 1 ||
| `BlockAllDamage` | Integer | If 1, the unit blocks all incoming damage. | 1 ||
| `BlockDamageUnderThreshold` | Integer | The maximum amount of damage from a single hit that will be completely blocked. | 1 ||
| `BlockNegativeStatus` | Integer | The percentage chance to completely block the application of a negative status effect. | 1 ||
| `Bloodzerked` | Integer | The number of Bloodzerk stacks applied. | 1 ||
| `BombBehavior` | Integer | If 1, the unit explodes after a set duration or on death. | 1 ||
| [`BombRatTurtle`](#object-bombratturtle) | Integer / Object | The number of bomb rat turtle spawns triggered. | 1 ||
| [`BoneWormShotMed`](#object-bonewormshotmed) | Object | An object defining a medium-range lobbed attack that fires a bone worm projectile. | 1 ||
| [`BonusAbility_DelayedApplication`](./Enums.md#enum-bonusability_delayedapplication) | Enum | Specifies the name of a bonus ability to apply with a delay. | 1 ||
| `BonusDamageBasedOnMana` | Integer | The amount of bonus damage dealt, scaled by the target's current mana. | 1 ||
| `BonusHealthRegenPerDisorder` | Integer | The amount of additional health regenerated per turn for each disorder the unit has. | 1 ||
| `BoostDamageAura` | Integer | The amount of bonus damage granted to allies within the aura's range. | 1 ||
| `BoostRangeAura` | Integer | The amount of bonus range (in tiles) granted to allies within the aura's range. | 1 ||
| `BoostReceivedHealing` | Integer | The amount of bonus healing received from all sources. | 1 ||
| [`BoyDino`](#object-boydino) | Object | An object defining the Boy Dino passive or character definition. | 1 ||
| [`BoyDinoCry`](#object-boydinocry) | Object | An object defining an ability or effect that causes the unit to cry, typically applying a debuff to nearby enemies. | 1 ||
| `BrittleCharismaUp` | Integer | The number of stacks of temporary Charisma gained on kill. | 1 ||
| `BrittleConstitutionUp` | Integer | The number of stacks of temporary Constitution gained on kill. | 1 ||
| `BrittleDexterityUp` | Integer | The number of stacks of temporary Dexterity gained on kill. | 1 ||
| `BrittleIntelligenceUp` | Integer | The number of stacks of temporary Intelligence gained on kill. | 1 ||
| `BrittleLuckUp` | Integer | The number of stacks of temporary Luck gained on kill. | 1 ||
| `BrittleSpeedUp` | Integer | The number of stacks of temporary Speed gained on kill. | 1 ||
| `BrittleStrengthUp` | Integer | The number of stacks of temporary Strength gained on kill. | 1 ||
| [`BungaCheers`](Characters_and_Bosses.md#object-bungacheers) | Object | Defines cheer particle effects and sounds triggered by ally or enemy actions. | 1 ||
| `ButterflySwarm` | Integer | The number of butterflies spawned for the Butterfly Swarm effect. | 1 ||
| `BypassRockKnockback` | Integer | If set to a non-zero number, bypasses normal rock knockback behavior. | 1 ||
| `CanceledQueuedInput` | Integer | If set to a non-zero number, cancels any queued input from the target. | 1 ||
| `CantDodge` | Integer | If set to 1, the unit cannot dodge any incoming attacks. | 1 ||
| `CapBasicAttackDamage` | Integer | The maximum amount of damage that can be dealt by a basic attack. | 1 ||
| `CapReceivedDamage` | Integer | If 1, the unit caps incoming damage to a maximum per hit. | 1 ||
| [`CatGoop`](#object-catgoop) | Object | Defines a specific attack or ability template, including its graphics and targeting parameters. | 1 ||
| [`CatPartsSizeScale`](Items_and_Equipment.md#object-catpartssizescale) | Object | A multiplier for the size of specific cat parts (e.g., head, body). | 1 ||
| [`CaveCatDad`](#object-cavecatdad) | Object | Configures a specific enemy cat type, including its graphics, name, and custom data. | 1 ||
| `CaveWomanBirthControl` | Integer | If true, restricts or controls the spawning of additional units via birth mechanics. | 1 ||
| [`CerberubsAggroTargetBehavior`](Characters_and_Bosses.md#object-cerberubsaggrotargetbehavior) | Object | Defines the default and alert forms used by Cerberubs when changing aggro behavior. | 1 ||
| [`CerberubsStraightReaction`](#object-cerberubsstraightreaction) | Object | Defines a specific attack ability with a straight-line projectile and configurable area of effect. | 1 ||
| `ChampionUpgradeNextMinion` | Integer | The number of champion upgrades applied to the next spawned minion. | 1 ||
| [`chance`](./Enums.md#enum-chance) | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 ||
| `ChanceToAmbush` | Integer | The percentage chance for the unit to ambush an enemy. | 1 ||
| [`ChanceToForceEvent`](Items_and_Equipment.md#object-chancetoforceevent) | Object | Defines the chance and the specific event to force to occur. | 1 ||
| [`ChanceToFormChangeOnAbilityDamage`](Characters_and_Bosses.md#object-chancetoformchangeonabilitydamage) | Object | A chance to transform into a different form when damaged by an ability. | 1 ||
| [`ChangeTileUnderCharacterAtStart`](./Enums.md#enum-changetileundercharacteratstart) | Enum | Specifies the tile type to change the tile under the character to at the start of battle. | 1 ||
| `ChaosBossFlipMidTeleport` | Integer | If set to a non-zero number, causes the chaos boss to flip direction mid-teleport. | 1 ||
| `ChaosBossFormChange` | Integer | If set to a non-zero number, triggers a chaos boss form change. | 1 ||
| [`ChaosBossFormChangeGuide`](Characters_and_Bosses.md#object-chaosbossformchangeguide) | Object | Defines active and passive piece sets and a health threshold for the Chaos boss's form change pattern. | 1 ||
| [`ChaosBossPieces`](Characters_and_Bosses.md#object-chaosbosspieces) | Object | Defines the list of active and passive piece tags for the Chaos boss fight. | 1 ||
| [`ChaosHeadDropIn`](Characters_and_Bosses.md#object-chaosheaddropin) | Object | Defines the tag, spawn ability, and music for the Chaos head's drop-in sequence. | 1 ||
| [`CharacterTypeGainsStatusAtBattleStart`](Engine_LogicKeys.md#object-charactertypegainsstatusatbattlestart) | Object | Defines status effects applied to characters with a specific tag at the start of a battle. | 1 ||
| `CharismaIsMaxStat` | Integer | Treats the Charisma stat as the character's maximum stat for calculations. | 1 ||
| `CharmedFacingForceAttack` | Integer | If set to a non-zero number, the charmed target is forced to attack the direction they are facing. | 1 ||
| [`CharmedLeech`](#object-charmedleech) | Object | Defines a charmed version of the Leech familiar, including its variant and graphics. | 1 ||
| [`CharmedPooter`](#object-charmedpooter) | Object | Defines a charmed version of the Pooter familiar, including its variant, faction, and properties. | 1 ||
| [`CharmedReaper`](#object-charmedreaper) | Object | Defines a charmed version of the Reaper familiar, including its variant, faction, and properties. | 1 ||
| `CharmImmunity` | Integer | If true, the unit is immune to the Charmed status effect. | 1 ||
| `choose_favorite_cat` | Variable | A variable referencing the selection of the player's favorite cat. | 1 ||
| [`Chubs`](#object-chubs) | Object | Defines the Chubs enemy or summon type, including its properties and abilities. | 1 ||
| [`ChubsGoop`](#object-chubsgoop) | Object | Defines the specific attack ability for Chubs, using a straight-shot template with no mana cost. | 1 ||
| [`ChubsRage`](#object-chubsrage) | Object | Defines the self-buff ability for Chubs, typically applying a rage animation and stat increases. | 1 ||
| `ClearDefaultDebris` | Integer | If true, removes all default debris from the battlefield. | 1 ||
| `ClearFinalBossBattlefield` | Integer | If set to a non-zero number, clears the battlefield during the final boss fight. | 1 ||
| `CloneWeaponTemp` | Integer | The number of turns the cloned weapon persists before being removed. | 1 ||
| `CockroachSwarm` | Integer | If true, the unit spawns as a Cockroach Swarm, with its specific mechanics and effects. | 1 ||
| [`CoinTossBounce`](./Enums.md#enum-cointossbounce) | Enum | Specifies the ability triggered when the coin lands on its edge after a bounce. | 1 ||
| [`Conditional_Flying`](Engine_Uncategorized_Resources.md#conditional_flying) | Object | Defines a conditional block that applies effects or actions only to flying units. | 1 ||
| [`Conditional_ManaThreshold`](Engine_LogicKeys.md#conditional_manathreshold) | Object | Defines a conditional block that applies effects only if a unit's mana meets a specified threshold. | 1 ||
| [`Conditional_SourceHasTag`](Engine_LogicKeys.md#conditional_sourcehastag) | Object | Defines a conditional block that applies effects only if the source of the effect has a specified tag. | 1 ||
| [`Conditional_Tiny`](Engine_Uncategorized_Resources.md#conditional_tiny) | Object | Defines a conditional block that applies effects only to tiny-sized units. | 1 ||
| [`ConfusionEffectOnTaggedAbilities`](./Enums.md#enum-confusioneffectontaggedabilities) | Enum | Specifies the type of ability tag (e.g., consumable) that triggers a confusion effect when used. | 1 ||
| [`ConjureSingleUseBonusAbility`](./Enums.md#enum-conjuresingleusebonusability) | Enum | Specifies the bonus ability to conjure for single use (e.g., 'random' for a random one). | 1 ||
| `ConsumablesMeleeRange` | Integer | Causes consumable items to have a melee range instead of their default range. | 1 ||
| [`ConvertDamageToScaledStatus`](Items_and_Equipment.md#object-convertdamagetoscaledstatus) | Object | Converts a portion of incoming damage into a specified status effect with a given number of stacks. | 1 ||
| [`CounterAttackAfterEnemyCastSpell`](./Enums.md#enum-counterattackafterenemycastspell) | Enum | Specifies the ability the unit uses to counterattack after an enemy casts a spell. | 1 ||
| `CounterNextAttacks` | Integer | The number of incoming attacks the unit will counterattack. | 1 ||
| [`CraterCreeperOut`](#object-cratercreeperout) | Object | Defines the specific enemy type Crater Creeper Out, including its graphics and spawn offset. | 1 ||
| `CrowAttackLink` | Integer | If 1, allows this unit's attacks to chain or link to nearby enemies like a crow. | 1 ||
| `CurrentWeaponAddElectricElement` | Integer | The number of turns the current weapon gains the electric element. | 1 ||
| [`CyborgTurns`](Miscellaneous.md#object-cyborgturns) | Object | Defines the number of extra turns controlled by AI and their timing for a Cyborg unit. | 1 ||
| `DamageFromBehindOnly` | Integer | If 1, the unit can only be damaged when attacked from behind. | 1 ||
| [`DamageIfDidntUseSpecificAbility`](Miscellaneous.md#object-damageifdidntusespecificability) | Object | Deals a specified amount of damage if the unit did not use a designated ability on its previous turn. | 1 ||
| `DamageWeapon` | Integer | The amount of durability damage dealt to the equipped weapon. | 1 ||
| [`DarkOneStrike`](#object-darkonestrike) | Object | Defines a specific powerful attack ability for the Dark One enemy. | 1 ||
| [`DeathwormUnderground`](./Enums.md#enum-deathwormunderground) | Enum | Specifies the ability triggered when the Deathworm emerges from underground. | 1 ||
| [`DecoyExplode`](#object-decoyexplode) | Object | Defines the explosion effect for a decoy unit. | 1 ||
| `DecoySwapper` | Integer | If true, the decoy swaps places with the source when spawned. | 1 ||
| `DelayedPain` | Integer | The number of stacks of DelayedPain applied, dealing damage after a delay. | 1 ||
| [`DelayedWindCone`](Abilities_and_Spells.md#object-delayedwindcone) | Object | An object containing parameters for a delayed wind cone, such as damage and distance. | 1 ||
| `DeleteInanimateObjectsChance` | Integer | The percentage chance per tick to delete all inanimate objects on the battlefield. | 1 ||
| `DeleteTraps` | Integer | If true, removes all traps from the map. | 1 ||
| `DemonicGlyph_Bounce` | Integer | The weight for the demonic glyph of bounce, or its configuration. | 1 ||
| `DemonicGlyph_Fire` | Integer | The weight for the demonic glyph of fire, or its configuration. | 1 ||
| `DemonicGlyph_Movement` | Integer | The weight for the demonic glyph of movement, or its configuration. | 1 ||
| `DemonicGlyphStealer` | Integer | If 1, the unit can steal demonic glyphs from other units. | 1 ||
| [`DestroyerShieldBash`](#object-destroyershieldbash) | Object | Defines the shield bash ability for the Destroyer enemy type. | 1 ||
| `DestroyNeckArmor` | Integer | If true, destroys the target's neck armor slot. | 1 ||
| [`Diabetes`](Miscellaneous.md#object-diabetes) | Object | Defines the Diabetes disorder, including its name, description, and associated passive effects. | 1 ||
| [`DiceBehavior`](Characters_and_Bosses.md#object-dicebehavior) | Object | Defines the dice size and knockback damage for the Dice enemy. | 1 ||
| [`DicerArt`](./Arrays.md#array-dicerart) | Array | An array of art offset values for the Dicer enemy. | 1 ||
| [`DiesToPiercingAndSpikes`](Characters_and_Bosses.md#object-diestopiercingandspikes) | Object | Makes the unit take lethal damage from piercing attacks and spike terrain. | 1 ||
| `DieWhenOnlyGolemsLeft` | Integer | If 1, the unit dies when only golem-type allies remain on the field. | 1 ||
| `DieWhenSpawnerDies` | Integer | If 1, the unit dies when its spawner unit dies. | 1 ||
| [`Digest`](#object-digest) | Object | Defines the digestion mechanic, typically applied to units that swallow others. | 1 ||
| [`DinoLegAnimation`](./Enums.md#enum-dinoleganimation) | Enum | Specifies the animation trigger for the dinosaur leg (e.g., 'poop' for the poop animation). | 1 ||
| `DisableSpells` | Integer | If 1, the unit cannot cast spells. | 1 ||
| `Disguised` | Integer | If true, the unit is disguised, appearing as a different faction or model. | 1 ||
| [`DisguisedTrapper`](./Enums.md#enum-disguisedtrapper) | Enum | Specifies the passive used when disguised as a trapper, e.g. FearMelee. | 1 ||
| `DisplayBuddyCatOnSpawn` | Integer | The number of buddy cat objects to display when the unit spawns. | 1 ||
| `DissolveRandomArmorPiece` | Integer | If true, destroys a random armor piece (head, body, neck) on the target. | 1 ||
| `DivineShieldPickup` | Integer | The number of divine shield charges granted on pickup. | 1 ||
| `DodgeChanceWithBlindSpot` | Integer | The percentage chance to dodge attacks while a blind spot condition is active. | 1 ||
| [`DodgeWhenTargeted`](Characters_and_Bosses.md#object-dodgewhentargeted) | Object | An object defining the ability and effects triggered when the unit is targeted for an attack. | 1 ||
| `DoubleCast` | Integer | The number of double-cast stacks, allowing a spell to be cast twice. | 1 ||
| `DoubleCastSpellIfManaCostUnderThreshold` | Integer | If a spell's mana cost is under this threshold, it will be cast twice. | 1 ||
| `DoubleCastSpellsEachTurn_Status` | Integer | The number of turns the unit gains Double Cast for spells each turn. | 1 ||
| `DoubleCastSpellThisTurn` | Integer | If non-zero, grants the unit a double cast effect for spells this turn. | 1 ||
| [`DoubleCastTaggedSpells`](./Enums.md#enum-doublecasttaggedspells) | Enum | Specifies the spell tag (e.g., musical) that causes spells to be cast twice. | 1 ||
| `DoubleReceivedNegativeStatus` | Integer | If true, the unit receives double the stacks of negative status effects applied to it. | 1 ||
| `DoubleReceivedPositiveStatus` | Integer | If true, the unit receives double the stacks of positive status effects applied to it. | 1 ||
| `DrainAllyCatsForFleshGolem` | Integer | The amount of health drained from ally cats to heal the Flesh Golem. | 1 ||
| [`DropAsFamiliarOnTookDamage`](./Enums.md#enum-dropasfamiliarontookdamage) | Enum | Specifies the familiar type to be dropped when the unit takes damage. | 1 ||
| [`DropSoulJarOnDeath`](./Enums.md#enum-dropsouljarondeath) | Enum | Specifies the type of soul jar to be dropped when the unit dies. | 1 ||
| `DuplicateRandomEquippedItem` | Integer | If true, creates a copy of a random equipped item. | 1 ||
| `DustCloudBehavior` | Integer | An integer flag that controls the behavior mode of a dust cloud entity. | 1 ||
| `Dybbuk1HPTracker` | Integer | A flag indicating the unit tracks that it has 1 HP remaining for Dybbuk possession mechanics. | 1 ||
| `DybbukManualExitTag` | Variable | A variable referencing the tag that allows a Dybbuk unit to manually exit its host. | 1 ||
| [`DybbukPossessionFallback`](Characters_and_Bosses.md#object-dybbukpossessionfallback) | Object | An object specifying the fallback form and exit ability used when possession fails. | 1 ||
| [`EatShit`](#object-eatshit) | Object | Defines a specific ability or effect related to consuming or eating feces. | 1 ||
| `ElectricArcs` | Integer | The number of electric arcs emitted by this unit. | 1 ||
| [`element`](./Enums.md#enum-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 1 ||
| [`ElementWeakness`](./Enums.md#enum-elementweakness) | Enum | Determines which element the unit is weak to, e.g. Fire. | 1 ||
| `EliteUpgradeNextMinion` | Integer | The number of elite upgrades applied to the next spawned minion. | 1 ||
| `end_of_round` | Boolean | If true, the effect triggers at the end of the round instead of at the start of the turn. | 1 ||
| `enemies` | Variable | A variable representing the group of enemy units. | 1 ||
| `EnrageOnDamage` | Integer | If set to 1, the unit gains enrage stacks when taking damage. | 1 ||
| [`EnterMount`](./Enums.md#enum-entermount) | Enum | Specifies the name of the mount status to apply to the unit. | 1 ||
| `EraseSpawnCoins` | Integer | If set to 1, the unit erases spawn coins from the map on spawn. | 1 ||
| [`euphoric`](Miscellaneous.md#object-euphoric) | Object | Defines the facial expression configuration for the euphoric emotional state of a unit. | 1 ||
| `EventBounterHunterPassive` | Integer | A flag enabling the event bounty hunter passive behavior. | 1 ||
| `exclude_self` | Boolean | If true, the effect does not apply to the source unit itself. | 1 ||
| [`ExcludeFromEvents`](./Enums.md#enum-excludefromevents) | Enum | Specifies the event type (e.g., Tragedy) that this unit is excluded from participating in. | 1 ||
| `ExhaustionRoundChange` | Integer | The number of rounds added to the exhaustion counter. | 1 ||
| `ExistUntilIdleUpkeep` | Integer | If true, the entity persists until the source unit enters idle upkeep. | 1 ||
| `ExplodeCharacter_DeathBloom` | Integer | The amount of damage dealt by the DeathBloom explosion. | 1 ||
| `ExplodeCharacter_DeathBloom2` | Integer | The amount of damage dealt by the DeathBloom2 explosion. | 1 ||
| `ExtraInjuryOnDeath` | Integer | The number of additional injuries inflicted upon death. | 1 ||
| [`ExtraTurnsPerTaggedUnit`](./Enums.md#enum-extraturnspertaggedunit) | Enum | Specifies the tag of units that grant extra turns when present. | 1 ||
| [`face_EatNeverstone`](#object-face_eatneverstone) | Object | Defines the ability used when the unit eats a Neverstone, typically a self-buff. | 1 ||
| [`face_LeechBrood`](#object-face_leechbrood) | Object | Defines the ability used when the unit activates Leech Brood, typically a self-buff or attack. | 1 ||
| [`FaceAwayLastDamage`](Characters_and_Bosses.md#object-faceawaylastdamage) | Object | An object defining animation overrides for the last damage event when the unit faces away. | 1 ||
| `FactionDisguiseSource` | Integer | If true, the unit adopts the faction of the source unit for disguise. | 1 ||
| `FastKnockback` | Integer | The number of tiles the target is knocked back with fast animation. | 1 ||
| [`FinalBossBeamQueue`](Characters_and_Bosses.md#object-finalbossbeamqueue) | Object | An object defining the queue of beam ability actions for the final boss form. | 1 ||
| [`FinalBossBecomeTheChild`](Characters_and_Bosses.md#object-finalbossbecomethechild) | Object | An object defining the transformation and environment changes when the boss becomes TheChild. | 1 ||
| [`FinalBossHitCountdownBoris`](Characters_and_Bosses.md#object-finalbosshitcountdownboris) | Object | An object defining the countdown status effect properties for the Boris phase, including stacks, icons, and forced abilities. | 1 ||
| [`FinalBossHitCountdownExplosive`](Characters_and_Bosses.md#object-finalbosshitcountdownexplosive) | Object | An object defining the countdown status effect properties for the Explosive phase, including stacks, icons, and forced abilities. | 1 ||
| [`FinalBossHitCountdownHoly`](Characters_and_Bosses.md#object-finalbosshitcountdownholy) | Object | An object defining the countdown status effect properties for the Holy phase, including stacks and icons. | 1 ||
| [`FinalBossPupils`](Characters_and_Bosses.md#object-finalbosspupils) | Object | An object configuring the visual tracking of the final boss's pupils, including radius, head position, and teleport tracking. | 1 ||
| `FinalBossQueueBeam` | Integer | If true, queues the final boss beam attack. | 1 ||
| [`FinalBossShieldHealth`](Characters_and_Bosses.md#object-finalbossshieldhealth) | Object | An object defining the shield health thresholds per visual state for the final boss. | 1 ||
| [`FinalBossSyncAnimations`](Characters_and_Bosses.md#object-finalbosssyncanimations) | Object | An object defining animation synchronization with another character, including form change abilities. | 1 ||
| [`FireArmor`](#object-firearmor) | Integer / Object | The number of Fire Armor stacks providing damage reflection. | 1 ||
| [`FireArmor2`](#object-firearmor2) | Integer / Object | The number of Fire Armor2 stacks (likely a variant). | 1 ||
| [`FireExtinguish_Steam`](#object-fireextinguish_steam) | Variable | Defines the particle effect for steam created when fire is extinguished. | 1 ||
| `FireflySwarm` | Integer | The number of fireflies in the swarm effect. | 1 ||
| `FistOfFateUniqueEnemyTracker` | Integer | Increases the damage tracking counter for unique enemies hit by Fist of Fate. | 1 ||
| `FlingObjectsOnTop` | Integer | The number of objects to fling on top of this unit. | 1 ||
| [`FlushmasterCelebration`](./Enums.md#enum-flushmastercelebration) | Enum | Specifies the celebration animation or effect name used by the Flushmaster. | 1 ||
| [`FlyBuff`](#object-flybuff) | Variable | Defines the visual effect or buff for the Fly familiar. | 1 ||
| `Fog` | Integer | When an integer, the intensity of fog; when an object, defines the fog particle effect. | 1 ||
| `ForceCollectsPickups` | Integer | If true, the unit automatically collects nearby pickups. | 1 ||
| `ForceDodgeEverything` | Integer | If set to 1, the unit will always dodge all incoming attacks. | 1 ||
| [`ForceImmediateMoveAndAttack`](Abilities_and_Spells.md#object-forceimmediatemoveandattack) | Object | An object that forces the unit to instantly move toward the target and perform a specified ability attack. | 1 ||
| `ForceMoveAndAttack` | Integer | If true, forces the target to move and attack its nearest enemy. | 1 ||
| `ForceTransferWeapon` | Integer | If true, forces the weapon to be transferred to the target. | 1 ||
| [`ForceUseAbilityOnTarget`](#object-forceuseabilityontarget) | Object | Defines a chance to force the unit to use a specified ability on the target. | 1 ||
| [`FormChangeWhenBuddyDies`](./Enums.md#enum-formchangewhenbuddydies) | Enum | Specifies the form name the unit changes into when its buddy dies. | 1 ||
| [`FrankBolts`](Passives_and_Statuses.md#object-frankbolts) | Integer / Object | The number of Frank Bolts applied or available. | 1 ||
| `FreeFirstCastAndAfterSpendMana` | Integer | If set to 1, the first cast of the ability and each cast after spending mana costs no resources. | 1 ||
| `FreeFirstCastEachMatch` | Integer | If set to 1, the first cast of the ability each match costs no resources. | 1 ||
| `FreeSpellsAtFullMana` | Integer | The number of spells that cost no mana when mana is full. | 1 ||
| `FrontstabBasicAttackCritChance` | Integer | The percentage chance for basic attacks to critically hit when attacking from the front. | 1 ||
| `FullBlockEverything` | Integer | If set to 1, the unit fully blocks all incoming damage. | 1 ||
| `FullBlockEverythingTo0Damage` | Integer | If set to 1, the unit reduces all incoming damage to 0. | 1 ||
| [`FurnitureStats`](Miscellaneous.md#object-furniturestats) | Object | Defines the Comfort, Stimulation, and Appeal stats of furniture. | 1 ||
| `GasCanBehavior` | Integer | An integer flag that controls the behavior mode of a gas can entity. | 1 ||
| `GasCloudBehavior2` | Integer | An integer flag that controls a secondary behavior mode of a gas cloud entity. | 1 ||
| `GeminiTwin` | Integer | If set to 1, this unit is the twin in a Gemini pair. | 1 ||
| [`GirlDino`](#object-girldino) | Object | Defines the Girl Dino creature or its ability. | 1 ||
| [`GirlDinoCry`](#object-girldinocry) | Object | Defines the cry ability of Girl Dino, typically a self-buff with a cry animation. | 1 ||
| `GiveBoundItemToTarget` | Integer | If true, gives the source's bound item to the target. | 1 ||
| `GlobalFamiliarDamageBoost` | Integer | The amount of damage boost applied to all familiars globally. | 1 ||
| `GlobalFamiliarMoveBoost` | Integer | The amount of movement boost applied to all familiars globally. | 1 ||
| [`GlobalFlowerTrapperAura`](Miscellaneous.md#object-globalflowertrapperaura) | Object | Defines an aura that applies Tangled to enemies with specified stacks and probability. | 1 ||
| `GlobalHealthRegenAura` | Integer | The amount of health regenerated per turn to all units in range. | 1 ||
| `GlobalManaDrainAura` | Integer | The amount of mana drained per turn from all units in range. | 1 ||
| [`GlobalMeleeRevengeDamage`](Items_and_Equipment.md#object-globalmeleerevengedamage) | Object | Defines revenge damage properties (e.g., knockback) when hit by a melee attack. | 1 ||
| [`GlobalSpawnCharacter`](./Enums.md#enum-globalspawncharacter) | Enum | Specifies the name of a character to spawn globally. | 1 ||
| `GoopImmunity` | Integer | If set to 1, the unit is immune to goop status effects. | 1 ||
| `grub_familiar` | Variable | Defines the Grub familiar's properties. | 1 ||
| [`Guillotina2Body`](#object-guillotina2body) | Object | Defines the Guillotina's second body ability or body part. | 1 ||
| [`Guillotina2Head`](#object-guillotina2head) | Object | Defines the Guillotina's second head ability or head part. | 1 ||
| [`Guillotina3Body`](#object-guillotina3body) | Object | Defines the Guillotina's third body ability or body part. | 1 ||
| [`Guillotina3Head`](#object-guillotina3head) | Object | Defines the Guillotina's third head ability or head part. | 1 ||
| `GuillotinaDeathHead` | Integer | If set to 1, the unit spawns a head object upon death via guillotine. | 1 ||
| [`HarpoonTrapPassive`](./Enums.md#enum-harpoontrappassive) | Enum | Specifies the ability name used when the harpoon trap is triggered. | 1 ||
| [`HCHumanDie`](#object-hchumandie) | Object | Defines the human die animation and buff when a human dies. | 1 ||
| [`HealNeighborsEachTurn`](Characters_and_Bosses.md#object-healneighborseachturn) | Object | An object defining the amount and target filtering for healing adjacent units each turn. | 1 ||
| `HealPercentMaxHP` | Integer | The percentage of max HP healed (e.g., 100 for full heal). | 1 ||
| `HealTo` | Integer | The target HP percentage to heal the unit to (e.g., '50%' for half max HP). | 1 ||
| `HeatWave` | Integer | When an integer, the intensity of the heat wave; when an object, defines the visual effects or status properties. | 1 ||
| `HeavyHits` | Integer | The number of Heavy Hits stacks increasing attack impact. | 1 ||
| [`HemBounce`](#object-hembounce) | Object | Defines the Hem's bounce melee attack ability. | 1 ||
| `HiddenDoomed` | Integer | The number of stacks of a hidden doomed status effect applied to the unit. | 1 ||
| [`HideEquipment`](./Enums.md#enum-hideequipment) | Enum | Specifies which equipment slot is visually hidden. | 1 ||
| `HideSomeHudStuff` | Integer | If set to 1, hides certain HUD elements. | 1 ||
| [`HitlerExecute`](Characters_and_Bosses.md#object-hitlerexecute) | Object | An object defining the tag, ability, and health threshold for executing a clone. | 1 ||
| [`HPAltStates`](Characters_and_Bosses.md#object-hpaltstates) | Object | An object defining alternate visual frames based on current HP thresholds. | 1 ||
| `Hypomania` | Integer | When an integer, the stacks of Hypomania; when an object, defines the Hypomania disorder status. | 1 ||
| `IceBlockBehavior` | Integer | An integer flag that controls the behavior mode of an ice block entity. | 1 ||
| [`IDSprout`](#object-idsprout) | Object | Defines the ID Sprout spawn ability. | 1 ||
| `IgnoreDebuffs` | Integer | If true, the effect ignores debuffs on the target. | 1 ||
| [`IncAuxCounterCycle`](Abilities_and_Spells.md#object-incauxcountercycle) | Object | An object containing parameters for incrementing an auxiliary counter with a change and maximum value. | 1 ||
| `IncreaseCumulativeBlastDamage` | Integer | If true, increases the cumulative blast damage counter. | 1 ||
| `IncreaseItemAuxOnKill` | Integer | If true, increases the item's aux counter on kill. | 1 ||
| `InheritSpawnerStats` | Integer | If set to 1, the unit inherits the stats of its spawner. | 1 ||
| [`insane`](Miscellaneous.md#object-insane) | Object | Defines the 'insane' facial expression with eyebrow and mouth positions. | 1 ||
| `InsertIntoBackgroundPlaceholder` | Integer | If set to 1, the unit is inserted into a background placeholder slot. | 1 ||
| `InterchangeDisabler` | Integer | If set to 1, prevents the unit from being interchanged with another unit. | 1 ||
| `InterchangeMoveActPoints` | Integer | If true, swaps the unit's remaining move points and action points. | 1 ||
| `InvertBrainFaction` | Integer | If set to 1, inverts the unit's faction (e.g., allies become enemies). | 1 ||
| `Invulnerable` | Integer | The number of Invulnerable stacks, making the unit immune to damage. | 1 ||
| `JesterLevelUpRerolls` | Integer | The number of additional rerolls granted when leveling up. | 1 ||
| [`JohnnyNeedsWashing`](Characters_and_Bosses.md#object-johnnyneedswashing) | Object | An object specifying the form names for washed and unwashed states. | 1 ||
| [`JohnnyWasher`](./Enums.md#enum-johnnywasher) | Enum | Specifies the ability name used by the washer form to clean Johnny. | 1 ||
| `JudgementDay` | Integer | When an integer, the turn count or damage for Judgement Day; when an object, defines the weather status. | 1 ||
| [`KnockbackIfCrit`](#object-knockbackifcrit) | Object | Defines knockback properties applied when a critical hit occurs. | 1 ||
| [`LegacySpawnSavedCatIfExists`](./Enums.md#enum-legacyspawnsavedcatifexists) | Enum | Specifies the legacy saved cat ID to spawn if it exists in the save data. | 1 ||
| [`LennyCatDies`](#object-lennycatdies) | Object | Defines the ability triggered when Lenny the cat dies. | 1 ||
| [`LimitedTileTrail`](./Enums.md#enum-limitedtiletrail) | Enum | Specifies the type of tile left behind as a trail when the unit moves. | 1 ||
| `LimitSelfKnockbackDamage` | Integer | The maximum amount of damage taken from self-inflicted knockback. | 1 ||
| [`LockOrientationFaceTile`](./Arrays.md#array-lockorientationfacetile) | Array | A tile coordinate [x y] that the unit's orientation is locked to face. | 1 ||
| `LowGravityKnockbackBoost` | Integer | The multiplier or bonus to knockback force under low gravity. | 1 ||
| `LowGravityRangeBoost` | Integer | The increase in attack range under low gravity. | 1 ||
| `MadnessChanceOnTurnBegin` | Integer | The chance (as a multiplier) to inflict Madness status at the start of each turn in the next battle. | 1 ||
| `MakeWeaponUnbreakable` | Integer | If true, makes the equipped weapon unbreakable. | 1 ||
| [`ManaGainRange`](#object-managainrange) | Object | Defines the minimum and maximum mana gained per turn. | 1 ||
| `ManaStealToHealth` | Integer | The amount of mana stolen and converted to health (negative values may drain health). | 1 ||
| `ManglerAttack` | Integer | If true, the attack triggers the Mangler's attack pattern. | 1 ||
| [`ManglerEnrage`](#object-manglerenrage) | Object | Defines the enrage ability of the Mangler monster. | 1 ||
| [`ManglerMonsterDashAttack`](#object-manglermonsterdashattack) | Object | Defines the dash attack ability of the Mangler monster. | 1 ||
| [`ManglerMonsterPassive`](./Enums.md#enum-manglermonsterpassive) | Enum | Specifies the ability name used for the Mangler monster's dash attack. | 1 ||
| `ManglerShuffle` | Boolean | If true, the order of effects in this damage instance is randomized before application. | 1 ||
| [`ManglersMonster`](#object-manglersmonster) | Object | Defines the Mangler monster's properties. | 1 ||
| `MassAttackThis` | Integer | The number of additional targets this attack hits via the Mass Attack mechanic. | 1 ||
| `MaxAccuracy` | Integer | The maximum allowed accuracy percentage for the unit. | 1 ||
| `MaxStartingMana` | Integer | The maximum amount of mana the unit starts with. | 1 ||
| `Meaty` | Integer | The number of Meaty stacks increasing health or size. | 1 ||
| [`MechExplode`](#object-mechexplode) | Object | Defines the explosion ability of a mech unit. | 1 ||
| [`MegaDinoDropController`](Characters_and_Bosses.md#object-megadinodropcontroller) | Object | An object defining the abilities and stable leg count for the Mega Dino's leg drop sequence. | 1 ||
| [`MegaFart`](#object-megafart) | Object | Defines the Mega Fart ability. | 1 ||
| [`MegaGuppy_SummonTheChild`](#object-megaguppy_summonthechild) | Object | Defines the ability to summon the child from Mega Guppy. | 1 ||
| [`MergeDamageInstance`](Abilities_and_Spells.md#object-mergedamageinstance) | Object | Specifies parameters to merge multiple damage instances into one, controlling hit animation and instant pop behavior. | 1 ||
| `MeteorShower` | Integer | The chance (as a percentage) for a meteor shower to occur on a given turn. | 1 ||
| `MimicMetronome` | Integer | The number of random abilities the Metronome effect selects from this unit's ability pool. | 1 ||
| `ModelingClayPassive` | Integer | If set to 1, enables the passive that duplicates the equipped item on the unit. | 1 ||
| [`ModularPickup`](Characters_and_Bosses.md#object-modularpickup) | Object | An object defining the effects and sounds triggered when the unit is picked up. | 1 ||
| [`MonkCatReactionAbilities`](Characters_and_Bosses.md#object-monkcatreactionabilities) | Object | A set of mappings from action types (move, attack, spell, trinket) to the corresponding ability IDs the MonkCat will use for reactions. | 1 ||
| [`MoonHead_KillHands`](#object-moonhead_killhands) | Object | An object defining a targeted status effect applied when MoonHead kills an enemy with its hands. | 1 ||
| [`MoonHeadCrackedVisual`](./Enums.md#enum-moonheadcrackedvisual) | Enum | Specifies the visual state for the character's cracked head appearance. | 1 ||
| [`MotherGrowController`](Characters_and_Bosses.md#object-mothergrowcontroller) | Object | Controls the growth of tumors on The Mother, including the tumor object, damage type, damage amount, and whether it pierces defense when eating damage. | 1 ||
| `MotherTumorDebugForcePass` | Integer | If non-zero, forces the Mother Tumor boss to pass its turn, skipping its normal action. | 1 ||
| [`MotherTumorPassive`](Characters_and_Bosses.md#object-mothertumorpassive) | Object | Defines the passive behavior for a MotherTumor, including the forms considered for pass/receive, the pass and receive animations, and the grow ability. | 1 ||
| [`Mount`](Characters_and_Bosses.md#object-mount) | Object | Defines the entering and ejecting abilities for a mountable unit, along with its death rattle ability. | 1 ||
| [`MoveAfterAnyAttemptedAttack`](Characters_and_Bosses.md#object-moveafteranyattemptedattack) | Object | Defines the movement behavior (weights and abilities) used after any attempted attack. | 1 ||
| [`MoveAwayWhenEnemyAdjacent`](Characters_and_Bosses.md#object-moveawaywhenenemyadjacent) | Object | Defines the movement behavior (move_ability, weights, and whether it triggers once per turn) when an enemy is adjacent. | 1 ||
| `MulticatHeads` | Integer | The number of additional heads the Multicat has. | 1 ||
| `MultiplyCoinsOnBattleStart` | Integer | The multiplier applied to the unit's coin count at the start of battle. | 1 ||
| `MultiplyReceivedHealing` | Integer | The multiplier applied to all healing the unit receives. | 1 ||
| [`MultiSpawnOnDeath`](Characters_and_Bosses.md#object-multispawnondeath) | Object | Specifies the object to spawn and the range of number of objects to spawn on death. | 1 ||
| `MutateAfterXTurns` | Integer | The number of turns after which the character automatically mutates (or transforms). | 1 ||
| `Muted` | Integer | The number of Muted stacks, disabling certain abilities. | 1 ||
| `MuteDemonicGlyphDisplay` | Integer | If set to 1, suppresses the display of demonic glyphs on the character. | 1 ||
| `NextAbilityHeals` | Integer | The number of stacks causing the next ability to heal instead of damage. | 1 ||
| `NextActionLuckUp` | Integer | The number of stacks increasing luck for the next action. | 1 ||
| [`NextBasicAttackCritsThisTurn`](Abilities_and_Spells.md#object-nextbasicattackcritsthisturn) | Object | An object or number configuring the next basic attack to be a critical hit this turn. An object may contain stack, cant_miss, or piercing sub-keys. | 1 ||
| [`NextBattleStatusStacks`](Abilities_and_Spells.md#object-nextbattlestatusstacks) | Object | An object specifying status effects and their stacks to be applied at the start of the next battle. Contains a "fights" counter and nested status keys. | 1 ||
| `NextDamageReduceAndHealAllies` | Integer | The number of stacks reducing next damage and healing nearby allies. | 1 ||
| `NextTurnDoubleRangedDamage` | Integer | The number of stacks doubling ranged damage on the next turn. | 1 ||
| [`NoHead`](#object-nohead) | Object | An object that replaces the unit's head graphics with a headless cat model and sets the enemy name. | 1 ||
| [`NonChampionFlySwarm`](#object-nonchampionflyswarm) | Object | An object defining a fly swarm that only spawns on non-champion units. | 1 ||
| `NonLethal` | Integer | If set to 1, damage dealt by the unit cannot kill enemies; it leaves them at 1 HP. | 1 ||
| [`Nubs`](#object-nubs) | Object | An object defining a visual or mechanical replacement of the unit's limbs with stubs. | 1 ||
| [`NubsGoop`](#object-nubsgoop) | Object | An object defining a lobbed attack that costs 0 mana and fires goop. | 1 ||
| [`ObjectDetector`](Items_and_Equipment.md#object-objectdetector) | Object | An object that grants a chance to detect a specific item (e.g., CharmedDip) when loot is evaluated. | 1 ||
| [`ObjectOnHitFullyEmpty`](./Enums.md#enum-objectonhitfullyempty) | Enum | Specifies the object (e.g., RandomArmorPickup) to spawn on the target when the attacker's inventory is completely empty. | 1 ||
| [`Ornstein`](#object-ornstein) | Object | An object defining a passive or status effect mimicking Ornstein's behavior (e.g., charge attack). | 1 ||
| `OrthogonalAIDangerZone` | Integer | The range (in tiles) for the AI's orthogonal danger zone detection. | 1 ||
| `OverHealToShield` | Integer | The amount of excess healing converted into temporary shield points. | 1 ||
| `OverManaReducesManaCosts` | Integer | If set to 1, any mana the unit has above their maximum reduces the cost of abilities. | 1 ||
| `OverrideMaxMana` | Integer | Sets the unit's maximum mana to this integer value, overriding the default. | 1 ||
| `OverridePalette` | Integer | Forces the unit to use a specific color palette index. | 1 ||
| `PackHunting` | Integer | If set to 1, enables pack hunting behavior for the character. | 1 ||
| [`Paranoia`](./Enums.md#enum-paranoia) | Enum | Specifies the type of paranoid melee attack the unit will use instead of their normal attack. | 1 ||
| [`PassiveLevelScaledStatus`](Miscellaneous.md#object-passivelevelscaledstatus) | Object | An object containing status effects whose values scale with the unit's level, using X as the level variable. | 1 ||
| [`PassiveWhileHasDurability`](Items_and_Equipment.md#object-passivewhilehasdurability) | Object | An object containing passives that are active only while the item has remaining durability. | 1 ||
| [`PassiveWhileNotTakingTurn`](Abilities_and_Spells.md#object-passivewhilenottakingturn) | Object | A nested passive object that is active only while the unit is not currently taking its turn. | 1 ||
| [`PassiveWhileShielded`](Items_and_Equipment.md#object-passivewhileshielded) | Object | An object containing passives that are active only while the unit has a shield. | 1 ||
| `PercentHeal` | Integer | The percentage of max HP healed when this effect triggers. | 1 ||
| `PermanentConfusion` | Number | If set to 1, the unit is permanently confused and cannot be cured. | 1 ||
| `PermanentImmobile` | Integer | The permanent amount of immobility stacks applied. | 1 ||
| `PermanentKitten` | Integer | If set to 1, the unit retains its kitten form permanently instead of aging. | 1 ||
| `PermanentUpgradeRandomActiveOrPassive` | Integer | The number of random active or passive abilities permanently upgraded. | 1 ||
| [`PersistentElement`](./Enums.md#enum-persistentelement) | Enum | Specifies the element type that this status effect permanently imbues (e.g., Holy). | 1 ||
| `PhysicalAttacksMiss` | Integer | If set to 1, all physical attacks against the unit automatically miss. | 1 ||
| `pickup` | Variable | A variable that marks an object as a pickup item that can be collected on the battlefield. | 1 ||
| `plant` | Variable | A variable that marks an object as a plantable item on the battlefield. | 1 ||
| [`PoolMetronome`](Abilities_and_Spells.md#object-poolmetronome) | Object | An object containing a "pool" array of ability names that the Metronome effect can randomly select from. | 1 ||
| `PreEmptiveCounterNextAttacks` | Integer | The number of next incoming attacks that the unit will counter preemptively before they land. | 1 ||
| [`PreventSpecificInjury`](./Enums.md#enum-preventspecificinjury) | Enum | Specifies a body part tag (e.g., 'int' for head) that cannot receive injuries. | 1 ||
| [`QueueUseAbility`](./Enums.md#enum-queueuseability) | Enum | Specifies the ability ID to be used immediately after the current action resolves. | 1 ||
| `RandomKnockbackDirection` | Integer | The number of random directions the target can be knocked back (e.g., 4 selects from 4 cardinal directions). | 1 ||
| [`RandomPermanentStatsDistinct`](#object-randompermanentstatsdistinct) | Object | An object defining a set of stat changes (positive and negative) that are randomly applied as permanent modifications. | 1 ||
| [`RandomWeatherEachFight`](./Arrays.md#array-randomweathereachfight) | Array | An array of weather types from which one is randomly selected at the start of each battle. | 1 ||
| `RealTimePressure_OneUnit` | Integer | The amount of real-time pressure (countdown) applied to the unit each turn. | 1 ||
| [`ReceivedStatusReplacement`](./Arrays.md#array-receivedstatusreplacement) | Array | An array specifying a status that replaces another status when it would be applied (e.g., Sleep becomes SleepParalysis). | 1 ||
| `ReclaimItemOnBreak` | Integer | If set to 1, the item returns to the inventory when it breaks instead of being lost. | 1 ||
| `ReduceManaCostExcludeBrainstorm` | Integer | The number of stacks reducing mana cost, excluding Brainstorm. | 1 ||
| `ReduceSpellCostsPerDisorder` | Integer | The amount of mana cost reduction per disorder the unit has. | 1 ||
| `ReduceSpellCostsPerParasite` | Integer | The amount of mana cost reduction per parasite the unit is hosting. | 1 ||
| `ReformMoonHead` | Integer | If non-zero, triggers the Moon Head's reformation mechanic (e.g., after it eats a cat). | 1 ||
| `RefreshItemAbilities` | Integer | The number of times all item abilities are recharged (cooldowns reset). | 1 ||
| `RefreshNonManaItemAbilities` | Integer | The number of times non-mana item abilities are recharged. | 1 ||
| `RefreshOncePerFightAbilities` | Integer | The number of times abilities limited to once per fight are refreshed. | 1 ||
| `ReloadOnAllyCatDies` | Integer | If set to 1, restores a charge when an allied cat dies. | 1 ||
| `ReloadOnAllyDies` | Integer | If set to 1, restores a charge when any ally dies. | 1 ||
| `ReloadOnAnyDamage` | Integer | If set to 1, restores a charge when any damage is taken. | 1 ||
| `ReloadOnBackstab` | Integer | If set to 1, restores a charge when performing a backstab. | 1 ||
| [`ReloadOnElementalDamageReceived`](./Enums.md#enum-reloadonelementaldamagereceived) | Enum | Specifies the elemental type of damage that, when received, restores a charge. | 1 ||
| `ReloadOnGainCoins` | Integer | If set to 1, restores a charge when coins are gained. | 1 ||
| `ReloadOnGainDivineShield` | Integer | If set to 1, restores a charge when a Divine Shield is gained. | 1 ||
| [`ReloadOnKillTagged`](./Enums.md#enum-reloadonkilltagged) | Enum | Specifies the tag of enemies that, when killed, restore a charge. | 1 ||
| `ReloadOnSpendMana` | Integer | If set to 1, restores a charge when mana is spent. | 1 ||
| `ReloadOnUseAbilityWithManaCost` | Integer | Specifies the amount of mana cost that, when used, restores a charge. | 1 ||
| `RemoteFlatLeech` | Integer | The flat amount of remote leech applied to the target on basic attack. | 1 ||
| [`RemoveAmbientLightEffects`](./Enums.md#enum-removeambientlighteffects) | Float | The fade-out duration in seconds for ambient light effects. | 1 ||
| `RemoveExtraDispersedTurn` | Integer | If set to 1, the unit's turn order is not delayed by the 'Dispersed' status effect. | 1 ||
| [`RemoveGlobalModifiers`](./Arrays.md#array-removeglobalmodifiers) | Array | List of global modifier names to remove upon death. | 1 ||
| `RepairAllCondition` | Integer | If non-zero, fully repairs the condition of all equipped items. | 1 ||
| [`ReplaceBlankTilesOnBattleStart`](./Enums.md#enum-replaceblanktilesonbattlestart) | Enum | Specifies a tile type (e.g., GlassTile) that replaces all blank tiles on the battle grid at the start of combat. | 1 ||
| `RerollEnemy` | Integer | The number of times the target enemy is re-rolled (transformed into a new random enemy). | 1 ||
| `RerollItemsOnBattleEnd` | Integer | If set to 1, all items in the unit's inventory are rerolled to new random items at the end of battle. | 1 ||
| `ReturnDinoLegs` | Integer | If non-zero, returns the Dino Legs ability to the unit after it is consumed. | 1 ||
| `RNGCannonRandomDamage` | Integer | The maximum random damage value for the RNG Cannon attack. | 1 ||
| [`RockyArmorSalvage`](./Enums.md#enum-rockyarmorsalvage) | Float | A multiplier for the percentage of armor value salvaged when the unit takes damage. | 1 ||
| `RunWhenKittensDead` | Integer | If set to 1, causes the character to attempt to flee when all associated kittens are dead. | 1 ||
| [`RunWhenLastPlayerCatIsCharmed`](Characters_and_Bosses.md#object-runwhenlastplayercatischarmed) | Object | Defines the behavior (including mid-turn decision allowance and legacy save key) for fleeing when the last player cat is charmed. | 1 ||
| [`SandStormBuff`](#object-sandstormbuff) | Variable | A variable containing graphical settings (movieclip, render mode) for a sandstorm visual effect on the unit. | 1 ||
| [`ScaldingOrbMoonBossOneShot`](Items_and_Equipment.md#object-scaldingorbmoonbossoneshot) | Object | An object that completes the ScaldingOrb quest and removes the item from the unit's inventory. | 1 ||
| [`ScaledStatusAlliesOnSpendMana`](Items_and_Equipment.md#object-scaledstatusalliesonspendmana) | Object | An object that applies a scaled status (e.g., ManaGain) to adjacent allies whenever the unit spends mana. | 1 ||
| [`ScaledStatusOnBleedDamage`](Miscellaneous.md#object-scaledstatusonbleeddamage) | Object | An object that applies a scaled status (e.g., Charge) on the unit when they take bleed damage. | 1 ||
| [`ScaledStatusOnHolyShieldBlock`](Items_and_Equipment.md#object-scaledstatusonholyshieldblock) | Object | An object that applies a scaled status (e.g., RandomMagicMissile) when the unit blocks an attack with a holy shield. | 1 ||
| [`ScalingAttackAnimation`](Characters_and_Bosses.md#object-scalingattackanimation) | Object | Maps attack animations to damage thresholds; when the unit's attack stat reaches a threshold, the corresponding animation overrides the default. | 1 ||
| `SchizoIllusionAIModifier` | Integer | If non-zero, modifies the AI behavior for schizo illusions. | 1 ||
| `SchrodingerDisorder` | Integer | A percentage chance for the unit to be simultaneously alive and dead (Schrödinger's cat) at the start of battle. | 1 ||
| `Scleroderma` | Integer | If set to 1, the unit's skin becomes hard, reducing damage but also movement. | 1 ||
| [`ScrambleLastUsedSpell`](Abilities_and_Spells.md#object-scramblelastusedspell) | Object | An object containing a "permanent" boolean. If true, permanently scrambles (randomizes) the last used spell. | 1 ||
| [`self_status_next_fight`](Events_and_Encounters.md#object-self_status_next_fight) | Object | An object defining status effects applied to the unit at the start of the next fight. | 1 ||
| [`SelfDamageWhenDealDamage`](Miscellaneous.md#object-selfdamagewhendealdamage) | Object | An object defining the damage the unit takes to itself whenever it deals damage to an enemy. | 1 ||
| [`set_WitchJump`](#object-set_witchjump) | Object | An object that configures the unit's witch jump ability (teleport-like movement). | 1 ||
| [`SetAnimationAlts`](Abilities_and_Spells.md#object-setanimationalts) | Object | Specifies alternative animation names for the target's dying and dead states. | 1 ||
| [`SetFaction`](./Enums.md#enum-setfaction) | Enum | Specifies the faction the unit belongs to (e.g., 'enemies'). | 1 ||
| `ShadowCrit` | Integer | If non-zero, enables the Shadow Crit mechanic, granting bonus critical hit chance or damage from stealth. | 1 ||
| [`ShineBuff`](#object-shinebuff) | Variable | A variable containing graphical settings (movieclip, render mode) for a sparkling visual effect on the unit. | 1 ||
| `ShootHereCommand` | Integer | If non-zero, commands an allied unit to shoot at this unit's target. | 1 ||
| `ShootHereReceiver` | Integer | If non-zero, marks this unit as the receiver of a Shoot Here command. | 1 ||
| [`Shove`](#object-shove) | Object | Configures a knockback ability that pushes the target a set distance. | 1 ||
| [`SkipFirstRounds`](Characters_and_Bosses.md#object-skipfirstrounds) | Object | Determines the number of initial rounds to skip and the chance per round of 'popping' (becoming active). | 1 ||
| [`SleepDart`](#object-sleepdart) | Object | Defines a projectile or targeted ability that applies the Sleep status effect on hit. | 1 ||
| `SleepParalysis` | Variable | The amount of stacks of Sleep Paralysis applied, which prevents the unit from acting while asleep. | 1 ||
| `SmallHitExplosion` | Integer | The number of small explosion VFX to spawn on hit. | 1 ||
| [`SmokeBuff`](#object-smokebuff) | Variable | Defines a visual particle effect (SmokeBuff) for rendering smoke or fog around the unit. | 1 ||
| [`Smough`](#object-smough) | Object | An object defining the Smough ability or template, likely a melee attack or passive with special properties. | 1 ||
| `Snow` | Integer | The number of snow particle instances or the integer value controlling snow intensity for weather effects. | 1 ||
| [`Snow`](#object-snow) | Number / Object | The number of snow particle instances or the integer value controlling snow intensity for weather effects. | 1 | `1` (Number), `{ ... }` (Object) |
| [`SolarFlare`](#object-solarflare) | Object | Defines the Solar Flare weather effect, which applies damage and status effects (burn, blind) to units each turn. | 1 ||
| [`SoundEventOnHit`](./Enums.md#enum-soundeventonhit) | Enum | Specifies the sound event ID to play on hit (e.g., "Batterup_Connect"). | 1 ||
| [`SourceSwapsBackEndOfTurn`](./Enums.md#enum-sourceswapsbackendofturn) | Enum | Specifies the ability ID to use to swap the source unit back at the end of the turn. | 1 ||
| `SpawnCatCloneOnCorpsePopped` | Integer | The number of cat clones spawned when a corpse is popped (destroyed) by the unit. | 1 ||
| `SpawnCreepOnHitKnockback` | Integer | If set to 1, spawns creep on the tile where a hit knocks back an enemy. | 1 ||
| `spawner` | Variable | A variable identifying the unit or object responsible for spawning other entities or effects. | 1 ||
| `SpawnerCatDataReference` | Integer | A reference ID pointing to the spawner cat's data, used by minions to link back to their spawner. | 1 ||
| [`SpawnRandomPickupsOnTaggedUnitKilled`](Items_and_Equipment.md#object-spawnrandompickupsontaggedunitkilled) | Object | Defines a pool of random pickups (items) spawned when a unit with a specific tag is killed, with a count range. | 1 ||
| [`SpawnTilePuddleOnBattleStart`](#object-spawntilepuddleonbattlestart) | Object | Defines a puddle of a specific tile type (e.g., OilTile) that is spawned on the battlefield at the start, with a radius range. | 1 ||
| `SpawnWebTrap` | Integer | The number of web traps to spawn on the target tile. | 1 ||
| [`SpecialBossMultipartInstakill`](./Enums.md#enum-specialbossmultipartinstakill) | Enum | Specifies the boss ID (e.g., "moonboss") whose multipart instakill mechanic is triggered. | 1 ||
| `SpeedUp_WithoutInitiative` | Integer | The number of stacks of Speed Up that do not affect the unit's initiative (turn order) stat. | 1 ||
| `SpellShield` | Integer | The number of stacks of SpellShield, which blocks incoming spells. | 1 ||
| [`SpewerAltGraphics`](Characters_and_Bosses.md#object-speweraltgraphics) | Object | Maps different Spewer liquid types (Normal, Fire, Tar) to their corresponding alternate graphic indices. | 1 ||
| [`SpiderReturn`](#object-spiderreturn) | Object | Defines the Spider Return ability, which teleports the unit back to a previously marked location after attacking. | 1 ||
| `SpitConsumed` | Integer | If non-zero, marks the object consumed by the Spit ability as having been used. | 1 ||
| `SpreadWater` | Integer | If set to 1, causes the character to spread water onto adjacent tiles. | 1 ||
| `sprout` | Variable | A variable associated with plant-based growth or spawning mechanics, likely a seed or sprout identifier. | 1 ||
| `SproutsGrantMovement` | Integer | If set to 1, sprouts on the character grant additional movement (aliases to MovementUp). | 1 ||
| [`StacyMutant_Brace`](Characters_and_Bosses.md#object-stacymutant_brace) | Object | A passive group granting the Brace ability and cosmetic changes. | 1 ||
| [`StacyMutant_Counter`](Characters_and_Bosses.md#object-stacymutant_counter) | Object | A passive group granting a counter attack and a bleed effect on basic attacks. | 1 ||
| [`StacyMutant_Damage`](Characters_and_Bosses.md#object-stacymutant_damage) | Object | A passive group increasing damage and decreasing max health with cosmetic changes. | 1 ||
| [`StacyMutant_DoubleHead`](Characters_and_Bosses.md#object-stacymutant_doublehead) | Object | A passive group granting an extra dispersed turn and cosmetic changes. | 1 ||
| [`StacyMutant_Fire`](Characters_and_Bosses.md#object-stacymutant_fire) | Object | A passive group granting fire immunity and a lava shot basic attack. | 1 ||
| [`StacyMutant_Health`](Characters_and_Bosses.md#object-stacymutant_health) | Object | A passive group increasing max health, reducing speed, and scaling size. | 1 ||
| [`StacyMutant_Holy`](Characters_and_Bosses.md#object-stacymutant_holy) | Object | A passive group granting a divine shield and cosmetic changes. | 1 ||
| [`StacyMutant_Ice`](Characters_and_Bosses.md#object-stacymutant_ice) | Object | A passive group granting ice immunity and an ice breath basic attack. | 1 ||
| [`StacyMutant_Lightning`](Characters_and_Bosses.md#object-stacymutant_lightning) | Object | A passive group granting electric immunity and a lightning dash basic attack. | 1 ||
| [`StacyMutant_Mirror`](Characters_and_Bosses.md#object-stacymutant_mirror) | Object | A passive group granting projectile reflection and random magic missile each turn. | 1 ||
| [`StacyMutant_Speed`](Characters_and_Bosses.md#object-stacymutant_speed) | Object | A passive group increasing speed, reducing damage, and scaling size. | 1 ||
| [`StacyMutant_Thorns`](Characters_and_Bosses.md#object-stacymutant_thorns) | Object | A passive group granting thorns damage and cosmetic changes. | 1 ||
| `StartDead` | Integer | The percentage chance that the character starts the battle already dead. | 1 ||
| `StatBounty` | Integer | The number of stacks of the StatBounty status effect. | 1 ||
| [`StatDependentPassive`](Items_and_Equipment.md#object-statdependentpassive) | Object | An object containing formulas that dynamically modify passive effects based on the unit's stats (e.g., str, dex, int). | 1 ||
| [`StatusAdjacentOnTheirTurnBegin`](Miscellaneous.md#object-statusadjacentontheirturnbegin) | Object | Defines a status effect applied to adjacent units when their turn begins, such as forcing them to move away. | 1 ||
| [`StatusAdjacentOnTheirTurnEnd`](Items_and_Equipment.md#object-statusadjacentontheirturnend) | Object | Defines a status effect applied to adjacent units when their turn ends, such as forcing them to move away. | 1 ||
| [`StatusAfterXStacks`](#object-statusafterxstacks) | Object | Defines a condition that triggers a status effect when a specified stack key reaches a threshold, optionally expiring at turn end. | 1 ||
| [`StatusAlliesEachTurn`](Items_and_Equipment.md#object-statusallieseachturn) | Object | Defines a status effect applied to all allies each turn, with an optional exclusion of the owner and conditional checks. | 1 ||
| [`StatusEachTurnBeginIfHasStatus`](Characters_and_Bosses.md#object-statuseachturnbeginifhasstatus) | Object | Defines a status effect to apply (and optionally consume) at the start of each turn if the character already has a specific status, with a specified animation. | 1 ||
| [`StatusEachTurnEndIfEnabledAtStartOfTurn`](Characters_and_Bosses.md#object-statuseachturnendifenabledatstartofturn) | Object | Defines an ability to force-use at the end of each turn if the character was in the specified form at the start of the turn. | 1 ||
| [`StatusIfBattleAlreadyBegan`](Miscellaneous.md#object-statusifbattlealreadybegan) | Object | Defines a status effect that is applied only if the battle has already started (not on the first turn). | 1 ||
| [`StatusOnDodge`](Items_and_Equipment.md#object-statusondodge) | Object | Defines a status effect applied to the unit each time it successfully dodges an attack. | 1 ||
| [`StatusOnEnemyCastSpell`](Elite_Buffs.md#object-statusonenemycastspell) | Object | Defines a status effect applied to the unit each time an enemy casts a spell. | 1 ||
| [`StatusOnEnemyConfused`](Characters_and_Bosses.md#object-statusonenemyconfused) | Object | Defines an ability to immediately use when an enemy becomes confused. | 1 ||
| [`StatusOnEnemyDeath`](Items_and_Equipment.md#object-statusonenemydeath) | Object | Defines a status effect applied to the unit each time an enemy dies. | 1 ||
| [`StatusOnFallAsleep`](Items_and_Equipment.md#object-statusonfallasleep) | Object | Defines one or more beneficial status effects applied to the unit when it falls asleep. | 1 ||
| [`StatusOnFullMana`](Items_and_Equipment.md#object-statusonfullmana) | Object | Defines a status effect applied to the unit when its mana is full, with an optional once-per-battle conditional. | 1 ||
| [`StatusOnLoseShield`](Miscellaneous.md#object-statusonloseshield) | Object | Defines a status effect applied to the unit each time it loses a shield point. | 1 ||
| [`StatusOnTakeHealthDamage`](Miscellaneous.md#object-statusontakehealthdamage) | Object | Defines a status effect applied to the unit each time it takes health damage, such as a permanent stat reduction. | 1 ||
| [`StatusOverlappingCharactersAndDie`](Characters_and_Bosses.md#object-statusoverlappingcharactersanddie) | Object | Defines a status effect applied to overlapping characters, after which the character dies. | 1 ||
| [`StatusWhenStatusCompletelyRemoved`](Characters_and_Bosses.md#object-statuswhenstatuscompletelyremoved) | Object | Defines a status to apply and an ability to use when a specific status is completely removed from the character. | 1 ||
| `StealDemonicGlyph` | Integer | The number of Demonic Glyphs stolen from the target. | 1 ||
| [`StealEquipment`](./Enums.md#enum-stealequipment) | Enum | Specifies the type of equipment to steal (e.g., "any") from the target. | 1 ||
| `StealthCritChance` | Integer | The percentage chance to critically hit while stealthed. | 1 ||
| `StealthUntilBasicAttack` | Integer | The number of stacks of Stealth that are removed when the unit performs a basic attack. | 1 ||
| `StealTurn` | Integer | The number of turns stolen from the target to grant to the attacker. | 1 ||
| `StevenBolts` | Integer | The number of Steven Bolts (a special resource or charge) the unit has for a unique ability. | 1 ||
| `StrictLimitDamage` | Integer | The amount of damage strict limit applies, capping incoming damage to a fixed value per hit. | 1 ||
| `StripKnockback` | Integer | If non-zero, removes all knockback effects from the unit's attacks or abilities. | 1 ||
| [`SupportDieInsteadOfRun`](Characters_and_Bosses.md#object-supportdieinsteadofrun) | Object | Configures alternative dying and dead animations for support units that die instead of fleeing. | 1 ||
| [`SwapWeapon`](Abilities_and_Spells.md#object-swapweapon) | Object | An object containing a "pool" array of weapon names to randomly swap to. | 1 ||
| [`SwimmingFormChange`](Characters_and_Bosses.md#object-swimmingformchange) | Object | Defines the form names to switch to when in water and when exiting water. | 1 ||
| [`SyncFormsWithBuddy`](Characters_and_Bosses.md#object-syncformswithbuddy) | Object | Specifies the form to revert to if the character has no buddy, ensuring form synchronization. | 1 ||
| `T2CopyCatInternal` | Variable | An internal variable used by the T2 Copy Cat passive to track clone spawning state. | 1 ||
| [`T3HitlerSpawningPhase`](Characters_and_Bosses.md#object-t3hitlerspawningphase) | Object | Defines weighted groups of spawn abilities used during the T3Hitler boss's spawning phase. | 1 ||
| `T3HitlerTriggerInitialSpawns` | Integer | If non-zero, triggers the initial spawn sequence for the T3 Hitler boss. | 1 ||
| [`TagMetronome`](./Enums.md#enum-tagmetronome) | Enum | Specifies a tag (e.g., "musical") used to filter which abilities the Metronome effect can pick. | 1 ||
| [`TakeBonusTurnWithStatus`](Abilities_and_Spells.md#object-takebonusturnwithstatus) | Object | Container for status effects applied when taking a bonus turn. | 1 ||
| `TakeExtraTurnEndOfRound` | Integer | The number of extra turns taken at the end of the round. | 1 ||
| `TakeWeaponFromSpawner` | Integer | If set to 1, the minion inherits the weapon from its spawner. | 1 ||
| `Tall` | Integer | If set to 1, the character occupies a taller hitbox or sprite space. | 1 ||
| [`TallTumorManaBurn`](./Enums.md#enum-talltumormanaburn) | Enum | Specifies the mana burn ability used by the TallTumor. | 1 ||
| `TargetedMetronome` | Integer | The number of random targets hit by the Targeted Metronome effect. | 1 ||
| [`TattersFear`](#object-tattersfear) | Object | Defines a targeted fear ability that causes the target to flee in a random direction. | 1 ||
| `TauntAtFullHealth` | Integer | The number of stacks of Taunt applied to the unit when it is at full health. | 1 ||
| `Taunting` | Integer | The number of stacks of Taunting, which forces enemies to target the unit. | 1 ||
| [`TC_DashReaction`](#object-tc_dashreaction) | Object | Defines a trample dash reaction ability that triggers when a unit dashes, dealing damage to enemies in the path. | 1 ||
| [`TeamBonusAbility`](./Enums.md#enum-teambonusability) | Enum | Specifies the ability ID granted to allies as a team bonus. | 1 ||
| [`TeleportBackAtTurnEnd`](./Enums.md#enum-teleportbackatturnend) | Enum | Specifies the ability ID used to teleport the unit back to its starting position at turn end. | 1 ||
| `TempBackstab` | Integer | The amount of temporary backstab bonus, typically as a percentage. | 1 ||
| `TempBackstabBleed` | Integer | The number of temporary Bleed status stacks applied on a backstab attack. | 1 ||
| `TempBackstabPiercing` | Integer | The amount of temporary piercing added to backstab attacks. | 1 ||
| `TempBackstabPoison` | Integer | The amount of temporary poison stacks applied with backstab attacks. | 1 ||
| `TempBasicAttackBonusAOE` | Integer | The amount of temporary area-of-effect bonus on basic attacks. | 1 ||
| `TempBonusKnockback` | Integer | The number of stacks of temporary bonus knockback distance. | 1 ||
| `TempBonusKnockbackDamage` | Integer | The number of stacks of temporary bonus knockback damage. | 1 ||
| `TempInjuryImmunity` | Integer | The number of stacks of temporary immunity to Injuries. | 1 ||
| `TempManaCostReduction` | Integer | The number of stacks of temporary mana cost reduction. | 1 ||
| `TempMeleeRangeUp` | Integer | The number of tiles added to the unit's melee attack range as a temporary buff. | 1 ||
| `TempPenetrate` | Integer | The amount of temporary penetration applied to attacks. | 1 ||
| `TempPreEmptiveCounterAttack` | Integer | The number of turns of temporary pre-emptive counterattack status. | 1 ||
| [`Terminator2Chase`](./Enums.md#enum-terminator2chase) | Enum | Specifies the movement ability used by Terminator2 when chasing the target. | 1 ||
| [`Terminator2Run`](Characters_and_Bosses.md#object-terminator2run) | Object | Defines the movement ability and movement weights used by Terminator2 when running away. | 1 ||
| [`TerminatorChase`](Characters_and_Bosses.md#object-terminatorchase) | Object | Defines the movement ability and reaction ability used by Terminator1 when chasing a target, plus whether it prioritizes player cats. | 1 ||
| [`TerminatorSkin`](Characters_and_Bosses.md#object-terminatorskin) | Object | Defines the status effect and groups of stacks applied by the Terminator's skin passive. | 1 ||
| [`TheCreator_SpawnCloneTeam`](#object-thecreator_spawncloneteam) | Object | Defines an ability that spawns a team of clones of the original cat, controlled by The Creator. | 1 ||
| [`TheHunger`](Miscellaneous.md#object-thehunger) | Object | Defines the Hunger passive, which applies Madness or other effects each turn, representing a disorder. | 1 ||
| [`ThornUp`](#object-thornup) | Object | Defines a self-buff ability that increases the unit's Thorns damage, reflecting damage back to attackers. | 1 ||
| [`ThrobbingKing2`](#object-throbbingking2) | Object | An object defining the Throbbing King 2 ability, likely a boss attack or passive with pulsing damage or effects. | 1 ||
| [`TickDownStatus`](./Enums.md#enum-tickdownstatus) | Enum | Specifies the name of the status effect whose duration is reduced by one tick. | 1 ||
| [`TileElementDamageImmunity`](./Enums.md#enum-tileelementdamageimmunity) | Enum | Determines which tile element type the character is immune to damage from. | 1 ||
| `TilesMovedToCritChance` | Integer | The number of stacks of a status that grants critical hit chance based on tiles moved. | 1 ||
| `TilesMovedToMana` | Integer | The number of stacks of a status that grants mana based on tiles moved. | 1 ||
| [`TilesMovedToNeighborHeal`](./Enums.md#enum-tilesmovedtoneighborheal) | Enum | Specifies the scaling type for healing neighbors based on tiles moved (e.g., 'level'). | 1 ||
| `TilesMovedToStrength` | Integer | The number of stacks of a status that grants strength based on tiles moved. | 1 ||
| [`TintItem`](Items_and_Equipment.md#object-tintitem) | Object | Defines additive and multiplicative color tint adjustments applied to an item's appearance, with an optional ignore condition. | 1 ||
| `TireBehavior` | Integer | If set to 1, activates special tire-related behavior for the character. | 1 ||
| `TormentorHeal` | Integer | If set to 1, the Tormentor can heal itself. | 1 ||
| [`TormentorRuneAbsorb`](#object-tormentorruneabsorb) | Object | Defines a spell ability that absorbs runes or energy from a target, typically used by the Tormentor enemy. | 1 ||
| `TossTargetIsAggroTarget` | Integer | If set to 1, the toss target is the unit's current aggro target. | 1 ||
| `TossTargetIsBuddy` | Integer | If set to 1, the toss target is the unit's buddy. | 1 ||
| `TossTargetIsNotInWater` | Integer | If set to 1, the toss target must not be in water terrain. | 1 ||
| [`TourettesMeows`](Miscellaneous.md#object-tourettesmeows) | Object | Defines a passive that triggers random vocalizations (hiss, hit, normal) at random cooldown intervals. | 1 ||
| `TowerDefenseStatus` | Integer | The number of stacks of the sentry/tower defense status, granting stationary attack capabilities. | 1 ||
| `TowerDefenseStatus2` | Integer | The number of stacks of the enhanced sentry/tower defense status. | 1 ||
| [`ToxicBubbles`](#object-toxicbubbles) | Variable | A variable defining the visual particle effect for toxic bubbles, used for environmental hazards or attacks. | 1 ||
| [`ToxPuff`](#object-toxpuff) | Object | Defines a self-buff ability that creates a toxic puff visual effect around the unit. | 1 ||
| [`TrackAmountKilledByPlayer`](./Enums.md#enum-trackamountkilledbyplayer) | Enum | Specifies the name of the counter used to track how many of this type the player has killed. | 1 ||
| [`TransformBasicMove`](./Enums.md#enum-transformbasicmove) | Enum | Specifies the name of the basic move to transform into. | 1 ||
| [`TransformEquipment`](Abilities_and_Spells.md#object-transformequipment) | Object | Defines an equipment transformation from one item to another, with 'from' and 'to' sub-keys. | 1 ||
| [`TransformNow`](./Enums.md#enum-transformnow) | Enum | Specifies the name of the form to immediately transform into. | 1 ||
| [`TransformOnStatusThreshold`](Characters_and_Bosses.md#object-transformonstatusthreshold) | Object | Defines the status effect, the stack threshold at which to transform, and the object to transform into. | 1 ||
| `Trapper_Status` | Integer | The number of trap-related status stacks applied. | 1 ||
| [`TrexSwitchTarget`](#object-trexswitchtarget) | Object | Defines a targeted status ability that forces an enemy to switch its target to the caster. | 1 ||
| `TriggerBleedOnBleed` | Integer | If non-zero, causes the unit to trigger additional bleed effects whenever it applies bleed to an enemy. | 1 ||
| `TriggerMotherConsume` | Integer | The number of times the Mother consume effect is triggered. | 1 ||
| `TriggerMotherGrow` | Integer | The number of times the Mother grow effect is triggered. | 1 ||
| `Triskaidekaphobia` | Integer | The threshold number (typically 13) at which a negative effect triggers due to the disorder Triskaidekaphobia. | 1 ||
| [`TT_Thrash`](#object-tt_thrash) | Object | Defines a melee attack ability that uses the thrash animation and deals damage to the target. | 1 ||
| `tumor` | Variable | A variable identifying a tumor growth passive or effect, likely related to status application or visual changes. | 1 ||
| [`TunnelVision`](Items_and_Equipment.md#object-tunnelvision) | Object | If present, grants the TunnelVision status, which modifies crit_chance as defined in its sub-properties. | 1 ||
| `TurnAround` | Integer | The number of times the unit turns around. | 1 ||
| [`TurnControlDelay`](./Enums.md#enum-turncontroldelay) | Float | Specifies the delay in seconds before the unit regains turn control. | 1 ||
| `TurnRight` | Integer | The number of times the unit turns to the right. | 1 ||
| `TutorialBossRiggedFight` | Integer | The turn count at which the tutorial boss fight becomes rigged. | 1 ||
| `TVBotDisableAttack` | Integer | If set to 1, disables the TVBot's ability to attack. | 1 ||
| `TVBotDisableMove` | Integer | If set to 1, disables the TVBot's ability to move. | 1 ||
| `TVBotDisableSpells` | Integer | If set to 1, disables the TVBot's ability to use spells. | 1 ||
| [`TVBotScreen`](Characters_and_Bosses.md#object-tvbotscreen) | Object | Maps TVBot screen channel names to their corresponding form indices. | 1 ||
| `Twister_loop` | Enum | Specifies which loop animation to use for the Twister effect. | 1 ||
| [`TwisterFling`](Characters_and_Bosses.md#object-twisterfling) | Object | Defines the minimum distance, maximum distance, and damage for the TwisterFling ability. | 1 ||
| [`UFO_BigExplode`](#object-ufo_bigexplode) | Object | Defines the visual and template properties for the UFO's large explosion effect. | 1 ||
| [`UltraSmough`](#object-ultrasmough) | Object | Defines the properties for the UltraSmough entity or status. | 1 ||
| `UndoDamage` | Integer | The amount of damage reversed. | 1 ||
| [`UnlimitedDeathRattleRevive`](Characters_and_Bosses.md#object-unlimiteddeathrattlerevive) | Object | Configures an unlimited revive effect, including the ability to use and whether it works even when stunned. | 1 ||
| `UpTireBehavior` | Integer | The behavior type integer for the Tire's upward form. | 1 ||
| [`UseAbility_Madness`](./Enums.md#enum-useability_madness) | Enum | Determines which ability type (e.g., weapon) is forcibly used when Madness triggers. | 1 ||
| [`UseAbilityWhenOutOfStatus`](Characters_and_Bosses.md#object-useabilitywhenoutofstatus) | Object | Defines an ability to execute when the unit no longer has a specified status. | 1 ||
| [`UseAbilityWhenShieldDepleted`](./Enums.md#enum-useabilitywhenshielddepleted) | Enum | The ability to use when the unit's shield is fully depleted. | 1 ||
| [`UseMoveAbilityWithAI`](Abilities_and_Spells.md#object-usemoveabilitywithai) | Object | Defines a move ability to execute with AI-controlled movement weights. | 1 ||
| `UseRandomSpell_Madness` | Integer | The number of random spells cast when Madness triggers. | 1 ||
| `VaporizeDice` | Integer | The number of dice vaporized. | 1 ||
| [`VisualCountDownThenApplyStatus`](Abilities_and_Spells.md#object-visualcountdownthenapplystatus) | Object | Contains a visual countdown sequence that culminates in applying a status effect, optionally forcing an ability use. | 1 ||
| [`WaggleClone`](Abilities_and_Spells.md#object-waggleclone) | Object | Defines a waggle clone ability with health thresholds and object sizes. | 1 ||
| `Wall` | Integer | If 1, the unit is treated as an impassable wall. | 1 ||
| `Wet` | Integer | The number of stacks of the Wet status effect applied. | 1 ||
| [`WhitelistPickupType`](./Enums.md#enum-whitelistpickuptype) | Enum | Specifies the type of pickup that this unit is allowed to collect. | 1 ||
| `WideBackstab` | Integer | The additional width for backstab attacks, in tiles. | 1 ||
| [`Wind`](Engine_LogicKeys.md#object-wind) | Object | Defines the properties for the Wind element, such as knockback amount. | 1 ||
| `Windy` | Integer | The number representing the Windy weather intensity or whether it is active. | 1 ||
| [`Windy`](#object-windy) | Number / Object | The number representing the Windy weather intensity or whether it is active. | 1 | `10` (Number), `1` (Number), `{ ... }` (Object) |
| `WispDodge` | Integer | If 1, the unit gains the Wisp's dodge ability. | 1 ||
| `WobblyCat` | Integer | The chance (as a percentage) or stack count for the WobblyCat disorder. | 1 ||
| `XIsConsumedCharacterMaxHP` | Integer | Specifies the multiplier used to set X to the maximum HP of the consumed character. | 1 ||
| `XIsCountDeaths` | Integer | If set to 1, X is equal to the number of deaths in the match. | 1 ||
| [`XIsCountStatusStacks`](./Enums.md#enum-xiscountstatusstacks) | Enum | Specifies the status field whose stacks are counted to set X. | 1 ||
| [`XIsFormulaLockedUntilComplete`](./Enums.md#enum-xisformulalockeduntilcomplete) | Enum | Specifies a stat (e.g., dex) whose value is locked in and used for X until the ability completes. | 1 ||
| `XIsIncreaseEachTurn` | Integer | Specifies the amount by which X increases each turn. | 1 ||
| `XIsRampAndReset` | Integer | If set to 1, X ramps up over time and resets after use; 0 disables this behavior. | 1 ||
| `XIsRecycleCostReduction` | Integer | Specifies the amount of recycle cost reduction applied to X. | 1 ||
| `ZeroKnockbackDamage` | Integer | If 1, the unit takes no damage from knockback effects. | 1 ||
| [`AcidRain`](#object-acidrain) | Number / Object | If non-zero, enables the Acid Rain weather effect dealing damage each turn. || `2` (Number), `{ ... }` (Object) |
| `Adrenaline` | Integer | The flat amount of Adrenaline (a resource or stat) granted to the unit. || `[1 .5]` (Array), `10` (Number), `1` (Number), `{ ... }` (Object) |
| `Ammo` | Integer | The amount of ammo to add or remove (negative values subtract). || `[1 .5]` (Array), `1` (Number), `6` (Number), `{ ... }` (Object) |
| `Bloodzerked` | Integer | The number of Bloodzerk stacks applied. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`BombRatTurtle`](#object-bombratturtle) | Integer / Object | The number of bomb rat turtle spawns triggered. || `1` (Number), `{ ... }` (Object) |
| `BounceRock` | Array / Enum | Specifies the rock object to bounce. || `[1 .2]` (Array), `LavaBoulder` (Enum), `SmallRock` (Enum) |
| [`ButterflySwarm`](#object-butterflyswarm) | Number / Object | The number of butterflies spawned for the Butterfly Swarm effect. || `2` (Number), `{ ... }` (Object) |
| `ChampionUpgradeNextMinion` | Integer | The number of champion upgrades applied to the next spawned minion. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`CockroachSwarm`](#object-cockroachswarm) | Number / Object | If true, the unit spawns as a Cockroach Swarm, with its specific mechanics and effects. || `1` (Number), `{ ... }` (Object) |
| `CollideWithConsumed` | String | Damage formula for collision with consumed objects, e.g., '4+bonus_melee_damage'. || `5+bonus_melee_damage` (Enum), `4+bonus_melee_damage` (Enum) |
| [`CopySpells`](Abilities_and_Spells.md#object-copyspells) | Integer / Object | The number of spells copied from the target, or an object specifying `stacks` and whether the copy is `upgraded`. || `1` (Number), `{ ... }` (Object) |
| [`Counterspell`](#object-counterspell) | Integer / Object | If non-zero, negates the next incoming enemy spell and triggers the configured counterspell effects. || `1` (Number), `{ ... }` (Object) |
| [`DelayCastAbility`](Abilities_and_Spells.md#object-delaycastability) | Enum / Object | Specifies the name of an ability to cast after a delay. || `HitlerNuke` (Enum), `{ ... }` (Object) |
| [`DelayCastAbility`](Abilities_and_Spells.md#object-delaycastability) | Enum / Object | Specifies the name of an ability to cast after a delay. || `HitlerNuke` (Enum), `{ ... }` (Object) |
| `DoubleCast` | Integer | The number of double-cast stacks, allowing a spell to be cast twice. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `DoubleCastSpell` | Integer | The number of times the next spell cast is doubled, or a template with name and tooltip. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `EliteUpgradeNextMinion` | Integer | The number of elite upgrades applied to the next spawned minion. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`FactionUprising`](#object-factionuprising) | Enum / Object | Specifies which faction triggers a global uprising event, adding allied units of that faction. || `robot` (Enum), `ghost` (Enum), `{ ... }` (Object) |
| [`FireArmor`](#object-firearmor) | Integer / Object | The number of Fire Armor stacks providing damage reflection. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`FireArmor2`](#object-firearmor2) | Integer / Object | The number of Fire Armor2 stacks (likely a variant). || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`FireflySwarm`](#object-fireflyswarm) | Number / Object | The number of fireflies in the swarm effect. || `2` (Number), `{ ... }` (Object) |
| [`FireStorm`](#object-firestorm) | Number / Object | The percentage chance or combo definition for the Fire Storm effect. || `33` (Number), `0` (Number), `{ ... }` (Object) |
| [`Fog`](#object-fog) | Number / Object | When an integer, the intensity of fog; when an object, defines the fog particle effect. || `1` (Number), `{ ... }` (Object) |
| `ForceMoveTowardsEnemies` | Enum / Integer | Specifies the ability or distance to force the target to move towards enemies. || `MoveOne` (Enum), `DumbMove_Impl` (Enum), `1` (Number) |
| `Grappled` | Array / Integer | The number of stacks and probability of applying the Grappled status, in format [stacks, probability] or just stacks. || `[1 .5]` (Array), `[1 .75]` (Array), `1` (Number), `{ ... }` (Object) |
| [`HeatWave`](#object-heatwave) | Array / Number / Object | When an integer, the intensity of the heat wave; when an object, defines the visual effects or status properties. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `HeavyHits` | Integer | The number of Heavy Hits stacks increasing attack impact. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `IgnoreSelf` | Boolean / Integer | If set to 1 or true, the damage instance ignores the source unit (does not affect itself). || `true` (Boolean), `1` (Number) |
| `Invulnerable` | Integer | The number of Invulnerable stacks, making the unit immune to damage. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`JudgementDay`](#object-judgementday) | Number / Object | When an integer, the turn count or damage for Judgement Day; when an object, defines the weather status. || `25` (Number), `{ ... }` (Object) |
| `KnockbackDirectionIsFacingDirection` | Enum / Integer | Specifies how to alter knockback direction relative to the unit's facing: 1 (same), flip (opposite), rotate_right. || `flip` (Enum), `rotate_right` (Enum), `1` (Number) |
| `Meaty` | Integer | The number of Meaty stacks increasing health or size. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`Meteornado`](#object-meteornado) | Number / Object | The number of Meteornado status stacks applied, or an object defining its visual effects. || `1` (Number), `{ ... }` (Object) |
| [`MeteorShower`](#object-meteorshower) | Number / Object | The chance (as a percentage) for a meteor shower to occur on a given turn. || `25` (Number), `{ ... }` (Object) |
| `Muted` | Integer | The number of Muted stacks, disabling certain abilities. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `NextAbilityHeals` | Integer | The number of stacks causing the next ability to heal instead of damage. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `NextActionLuckUp` | Integer | The number of stacks increasing luck for the next action. || `[1 .5]` (Array), `1` (Number), `99` (Number), `{ ... }` (Object) |
| `NextAttackBonusRange` | Integer | The added range for the unit's next basic attack. || `[1 .5]` (Array), `5` (Number), `1` (Number), `{ ... }` (Object) |
| [`NextAttackSpecialCrit`](Abilities_and_Spells.md#object-nextattackspecialcrit) | Integer / Object | The number of charges for a special crit on the next attack, or an object defining its bonus properties. || `1` (Number), `{ ... }` (Object) |
| [`NextBasicAttackCritsThisTurn`](Abilities_and_Spells.md#object-nextbasicattackcritsthisturn) | Object | An object or number configuring the next basic attack to be a critical hit this turn. An object may contain stack, cant_miss, or piercing sub-keys. || `1` (Number), `{ ... }` (Object) |
| `NextDamageReduceAndHealAllies` | Integer | The number of stacks reducing next damage and healing nearby allies. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `NextTurnDoubleRangedDamage` | Integer | The number of stacks doubling ranged damage on the next turn. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `OverrideKnockbackDamage` | Enum / Integer | A formula or flat value that sets the damage dealt when knockback occurs, overriding default calculations. || `str` (Enum), `X*10` (Enum), `5` (Number), `2` (Number), `"max(5+bonus_melee_ability_damage, 1)"` (String) |
| `OverrideKnockbackDamage` | Enum / Integer | A formula or flat value that sets the damage dealt when knockback occurs, overriding default calculations. || `str` (Enum), `3+bonus_melee_ability_damage` (Enum), `2` (Number), `3` (Number), `"max(5+bonus_melee_ability_damage, 1)"` (String) |
| `PermanentImmobile` | Integer | The permanent amount of immobility stacks applied. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`RandomDistanceDisplace`](Abilities_and_Spells.md#object-randomdistancedisplace) | Integer / Object | The number of stacks of a random distance displacement effect, or an object with stacks, min_dist, and chance. || `20` (Number), `{ ... }` (Object) |
| `ReduceManaCostExcludeBrainstorm` | Integer | The number of stacks reducing mana cost, excluding Brainstorm. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `ScatterHeldCoin` | Array / Integer | The number of coins scattered, with an optional probability as a second element. || `[1 .3]` (Array), `[1 .5]` (Array), `1` (Number) |
| `SelfStun` | Array / Integer | The number of stacks of self-stun applied, with an optional probability as a second element. || `[1 .5]` (Array), `1` (Number) |
| [`Shatter`](#object-shatter) | Integer / Object | The amount of damage dealt when a frozen or petrified status is shattered, or a template definition for a Shatter ability. || `15` (Number), `{ ... }` (Object) |
| `SpawnRock` | Array / Integer | The number of rocks to spawn, or an array with stacks and probability. || `[1 .20]` (Array), `1` (Number) |
| `SpellShield` | Integer | The number of stacks of SpellShield, which blocks incoming spells. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `StatBounty` | Integer | The number of stacks of the StatBounty status effect. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Taunting` | Integer | The number of stacks of Taunting, which forces enemies to target the unit. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`TeamCastAbility`](Abilities_and_Spells.md#object-teamcastability) | Enum / Object | Specifies the ability name for the team to cast, with optional tag restriction and same orientation. || `TeamFlex_Impl2` (Enum), `TeamFlex_Impl` (Enum), `{ ... }` (Object) |
| `TempBackstab` | Integer | The amount of temporary backstab bonus, typically as a percentage. || `[1 .5]` (Array), `75` (Number), `1` (Number), `{ ... }` (Object) |
| `TempBonusKnockback` | Integer | The number of stacks of temporary bonus knockback distance. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TempBonusKnockbackDamage` | Integer | The number of stacks of temporary bonus knockback damage. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TempCritChanceUp` | Integer | The amount of temporary critical hit chance (in percentage points) added. || `[1 .5]` (Array), `30` (Number), `1` (Number), `{ ... }` (Object) |
| `TempInitiativeChange` | Integer | The flat change to the unit's initiative value. || `[1 .5]` (Array), `9999` (Number), `1` (Number), `{ ... }` (Object) |
| `TempInitiativeChange` | Integer | The flat change to the unit's initiative value. || `[1 .5]` (Array), `9999` (Number), `1` (Number), `{ ... }` (Object) |
| `TempInjuryImmunity` | Integer | The number of stacks of temporary immunity to Injuries. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TempManaCostReduction` | Integer | The number of stacks of temporary mana cost reduction. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TempPreEmptiveCounterAttack` | Integer | The number of turns of temporary pre-emptive counterattack status. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TilesMovedToCritChance` | Integer | The number of stacks of a status that grants critical hit chance based on tiles moved. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TilesMovedToMana` | Integer | The number of stacks of a status that grants mana based on tiles moved. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TilesMovedToNeighborHeal` | Enum | Specifies the scaling type for healing neighbors based on tiles moved (e.g., 'level'). || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TilesMovedToStrength` | Integer | The number of stacks of a status that grants strength based on tiles moved. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TowerDefenseStatus` | Integer | The number of stacks of the sentry/tower defense status, granting stationary attack capabilities. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TowerDefenseStatus2` | Integer | The number of stacks of the enhanced sentry/tower defense status. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TriggerWerewolfTransform` | Array / Number | The number of stacks and probability of triggering the werewolf transformation. || `[1 .5]` (Array), `[1 .20]` (Array), `.5` (String) |
| `TurnControlDelay` | Number | Specifies the delay in seconds before the unit regains turn control. || `.25` (String) |
| [`VisualFlySwarm`](#object-visualflyswarm) | Number / Object | If non-zero, enables the visual fly swarm effect on the unit. || `1` (Number), `{ ... }` (Object) |

| [`AddDamageToElementDamage`](Cat_Mutations.md#object-adddamagetoelementdamage) | Object | Defines additional damage of a specific element added to the unit's attacks. | 6 |
| `AddLeechesStatus` | Integer | The number of stacks of Leech status applied to the source, healing when dealing damage. | 0 |
| [`AddStatusesIfPersistentWeatherElement`](Miscellaneous.md#object-addstatusesifpersistentweatherelement) | Object | Specifies statuses applied if the persistent weather matches the given elements. | 0 |
| [`AddStatusesToReceivedElementalDamage`](Miscellaneous.md#object-addstatusestoreceivedelementaldamage) | Object | An object defining statuses applied to the unit when it takes elemental damage of the specified types. | 0 |
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | Contains status effects to add to the basic attack. | 178 |
| [`AddStatusToElementDamage`](Items_and_Equipment.md#object-addstatustoelementdamage) | Object | An object that applies a specific status effect when dealing damage of a specified element. Contains sub-keys for the element and the status to apply. | 4 |
| [`AddStatusToTrampleDamage`](Characters_and_Bosses.md#object-addstatustotrampledamage) | Object | An object whose nested keys define statuses applied to trample damage. | 2 |
| `AddWeaponAux` | Integer / String | The amount or expression to add to the source's weapon auxiliary stat. | 0 |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 0 |
| `AlphaCat` | Integer | The number of AlphaCat stacks applied to the source on kill. | 2 |
| [`ApplyPassives`](Abilities_and_Spells.md#object-applypassives) | Object | Specifies the passives or status effects to apply to the unit. | 0 |
| `BigSplashDamage` | Integer | The additional tile radius of the splash damage effect applied by an attack. | 0 |
| `Bleed` | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 |
| `Blind` | Array / Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 6 |
| [`BloodRain`](Engine_GlobalModifierKeys.md#object-bloodrain) | Integer / Object | If non-zero, enables the blood rain visual effect. | 2 |
| `BonusCritChance` | Integer | The flat percentage increase to critical hit chance. | 0 |
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 0 |
| `BonusDamageBasedOnDistance` | Integer | The flat bonus damage added per tile of distance between the source and target. | 0 |
| `BonusKnockbackDamage` | Integer | The extra damage dealt per tile of knockback. | 0 |
| `BrittleCharismaUp` | Integer | The number of stacks of temporary Charisma gained on kill. | 0 |
| `BrittleConstitutionUp` | Integer | The number of stacks of temporary Constitution gained on kill. | 0 |
| `BrittleDexterityUp` | Integer | The number of stacks of temporary Dexterity gained on kill. | 0 |
| `BrittleIntelligenceUp` | Integer | The number of stacks of temporary Intelligence gained on kill. | 0 |
| `BrittleLuckUp` | Integer | The number of stacks of temporary Luck gained on kill. | 0 |
| `BrittleSpeedUp` | Integer | The number of stacks of temporary Speed gained on kill. | 0 |
| `BrittleStrengthUp` | Integer | The number of stacks of temporary Strength gained on kill. | 0 |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 |
| `Burn` | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 1 |
| `CapDamage` | Integer | The maximum amount of damage dealt, capping the total after all modifiers are applied. | 0 |
| `CaptureFamiliar` | Integer | The number of times to attempt to capture the target as a familiar. | 0 |
| `ChanceToBreak` | Integer | Specifies the percentage chance that the item breaks on use. | 0 |
| [`CharacterTypeGainsStatusAtBattleStart`](Engine_LogicKeys.md#object-charactertypegainsstatusatbattlestart) | Object | Defines status effects applied to characters with a specific tag at the start of a battle. | 1 |
| `Charge` | Integer | The number of charge stacks applied. | 0 |
| `Charmed` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 0 |
| [`Cleanse`](#object-cleanse) | Integer / Object | The number of stacks of negative status effects removed from the target. | 2 |
| `CompleteItemQuest` | Enum | Specifies the item quest ID to mark as complete on kill. | 0 |
| [`Conditional_HasStatus`](Abilities_and_Spells.md#object-conditional_hasstatus) | Object | Contains an inner effect block that only executes if the target has the specified status effect. | 0 |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 |
| `ConjureRandomAbilityFromCat` | Integer | The number of random abilities created or given to the cat unit from a pool of cat-themed abilities. | 0 |
| `CrackMoonHead` | Integer | If set, cracks the MoonHead's head, triggering its death sequence. | 0 |
| `CurrentWeaponDamageUp` | Integer | The amount of temporary damage increase to the current weapon. | 0 |
| `DeleteObject` | Integer | If set, deletes the target object from the map. | 0 |
| `DestroyTrinket` | Integer | The number of trinkets destroyed. | 0 |
| [`Die`](Characters_and_Bosses.md#object-die) | Integer / Object | If set, kills the target immediately. | 0 |
| `DieViolently` | Integer | If true, causes the target to die with a violent, explosive visual effect. | 0 |
| `DisableWeapon` | Integer | If set, disables the source's weapon, preventing its use. | 0 |
| `disallow_modifications` | Boolean | If true, the damage instance cannot be modified by external effects (e.g., passives, statuses). | 0 |
| `DisplaceToAbilityTarget` | Integer | If set, displaces the source to the ability's target location. | 0 |
| `DisplaceTowardsSource` | Integer | If set, displaces the target towards the source of the effect. | 0 |
| [`DistanceBonusDamage`](#object-distancebonusdamage) | Object | An object that adds bonus damage based on the distance from the target, with sub-keys for stacks and minimum range. | 0 |
| `DivineShield` | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 0 |
| `DontHealEnemies` | Integer | If true, the healing effect does not affect enemy units. | 0 |
| `Doomed` | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. | 0 |
| `EmptyMana` | Integer | If non-zero, sets the unit's mana to empty when applied. | 0 |
| `EventBounty` | Integer | The number of stacks of Event Bounty applied, increasing event rewards. | 0 |
| `ExplodeCharacter` | Integer | The radius (in tiles) of an explosion centered on the character. | 0 |
| `ExplodeCharacter_NoDie` | Integer | The damage dealt when a character explodes without dying. | 0 |
| `ExplodeCharacter_Party` | Integer | The radius (in tiles) of an explosion centered on the character that also damages party members. | 0 |
| `ExplodeCharacter_PartyBoss` | Integer | The damage dealt to the party boss when it explodes. | 0 |
| `ExplodeCharacter_RockCrusher` | Integer | The number of RockCrusher explosion triggers applied to non-boss characters. | 0 |
| `ExplodeCharacter_RockCrusher_PetrifyBreak` | Integer | The damage dealt when a petrified RockCrusher explodes. | 0 |
| `FaceAway` | Integer | If set, forces the target to face away from the source. | 0 |
| `FaceCamera` | Integer | If non-zero, forces the character to rotate and face the camera. | 0 |
| `FactionConversion` | Integer | Converts the target to the caster's faction. | 0 |
| `Fear` | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 0 |
| `Fights` | Number | The number of fights this status or effect persists for. | 4 |
| `FillMana` | Integer | The amount of mana restored, or an [amount, probability] array. | 0 |
| `FlatAIBonus` | Integer | A flat adjustment to the AI's evaluation score for this action; positive values encourage the AI to use it, negative values discourage it. | 0 |
| `FlatLeech` | Integer | The flat amount of health restored to the source when dealing damage, applied after the hit. | 0 |
| `FloatingRockTrap` | Integer | The number of stacks of Floating Rock Trap applied to the target, dealing damage when stepped on. | 0 |
| `ForceImmediateMove` | Integer | If non-zero, forces the character to move instantly without waiting for normal action order. | 0 |
| `ForceMoveAway` | Integer | The distance to force the target away from the source. | 0 |
| `ForceMoveTowards` | Integer | The number of tiles to force the target to move toward the caster. | 0 |
| `ForceUseAbility_NonStack` | Enum | Forces the unit to use a specific non-stackable ability when the conditional roll is successful. | 0 |
| [`ForceUseAbilityOnTarget`](#object-forceuseabilityontarget) | Object | Defines a chance to force the unit to use a specified ability on the target. | 0 |
| `FullHeal` | Integer | If non-zero, fully restores the target's health. | 0 |
| `GainDisorder` | Enum | Specifies the name of the disorder gained. | 0 |
| `GainDisorderFromPool_PostCast` | Enum | Specifies the pool of disorders the unit can gain after the spell is cast. | 0 |
| `GenericDebuff` | Integer | The number of stacks of a generic, untooltipped debuff applied to the target. | 0 |
| `HealRandomInjury` | Integer | The number of random injuries healed on the target. | 0 |
| `HealthGain` | Integer | The amount of health restored to the source. | 0 |
| `IgnoreDamage` | Integer | If set, the target ignores all damage for the duration. | 0 |
| [`ImmediateUseAbility`](#object-immediateuseability) | Enum / Object | Specifies the name of an ability to be triggered instantly from this effect. | 0 |
| `ImmediateUseAbility_Instant` | Enum | Specifies the name of an ability to use instantly as a passive effect. | 0 |
| `Immobile` | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 |
| `Imprison` | Enum | Specifies the type of unit or object to summon as a prison. | 0 |
| `InnateElement` | Enum | Specifies the innate elemental type of the unit (e.g., Fire, Ice, Electric). | 8 |
| `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 0 |
| [`KnockbackIfCrit`](#object-knockbackifcrit) | Object | Defines knockback properties applied when a critical hit occurs. | 0 |
| `KnockOutClone` | Enum | Specifies the ability ID used to knock out or remove the player's clone unit from battle. | 0 |
| `LaunchOffScreen` | Equation | A formula string that determines the knockback force to launch the unit off-screen. | 0 |
| `LaunchOffScreenInstakill` | Integer | If non-zero, the unit is instantly killed and launched off-screen. | 0 |
| `LeaveBehindRockOnKnockback` | Integer | If non-zero, leaves behind a rock on each tile the target is knocked through. | 0 |
| `Leech` | Integer | The amount of health leeched from the target (heals the attacker). | 6 |
| `LeechPercent` | Integer | The percentage of damage dealt restored as health. | 0 |
| [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 0 |
| `ManaGain` | Enum / Integer | The amount of mana restored to the source, which can be an expression. | 0 |
| [`Marked`](#object-marked) | Array / Integer / Object | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 0 |
| `NonLethal` | Integer | If set to 1, damage dealt by the unit cannot kill enemies; it leaves them at 1 HP. | 0 |
| `OverrideDamage` | Integer | Overrides the damage of the current action to this flat value (can be negative to heal). | 0 |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 5118 |
| `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. | 0 |
| `PermanentDexterity` | Integer | The permanent amount of dexterity added or removed. | 0 |
| `PreEmptiveCounterNextAttacks` | Integer | The number of next incoming attacks that the unit will counter preemptively before they land. | 0 |
| `PurgeAll` | Integer | If non-zero, removes all temporary status effects (buffs, debuffs) from the target. | 0 |
| `RandomBonusDamage` | Integer | The maximum random bonus damage added to the base damage; the actual bonus is a random value between 0 and this number. | 0 |
| `RandomStatDown` | Array / Integer / String | The amount of random stat reduction applied, either as a fixed number, a formula string, or an array of [stacks, probability]. | 0 |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 |
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | A collection of status effects; one is randomly chosen and applied to the target. | 0 |
| `RefreshActPoints` | Integer | The amount of action points restored to the source. | 0 |
| `RefreshMovePoints` | Integer | The amount of movement points restored to the source. | 0 |
| `RefreshWeaponAbility` | Integer | The number of times the weapon's ability is refreshed. | 0 |
| `RemoteFlatLeech` | Integer | The flat amount of remote leech applied to the target on basic attack. | 0 |
| `RemoteLeech` | Integer | The amount of remote leech applied to the target on basic attack. | 0 |
| `RemoveAmbientLightEffects` | Float | The fade-out duration in seconds for ambient light effects. | 0 |
| `RemoveGlobalModifiers` | Array | List of global modifier names to remove upon death. | 0 |
| `RemoveItem` | Enum | Specifies the item ID to remove from the source on kill. | 0 |
| `RemoveKnockback` | Integer | The number of knockback stacks removed from the received damage. | 0 |
| `RemoveMovePoints` | Integer | The number of move points to remove from the target, preventing them from moving. | 0 |
| `RemoveStatus` | Enum | The name of the status effect to remove from the source. | 0 |
| [`RemoveStatusStacks`](Abilities_and_Spells.md#object-removestatusstacks) | Object | An object specifying a status name and the number of stacks to remove from the target. | 0 |
| `RemoveTurnsThisRound` | Integer | The number of turns to remove from the target's turn order this round. | 0 |
| `RepairWeapon` | Array / Integer | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 0 |
| [`Revive`](#object-revive) | Integer / Object | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 2 |
| `Rot` | Array / Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 0 |
| `ScatterRandomPickups` | Integer | The number of random pickups scattered around the target's location. | 0 |
| `SetHealth` | Integer | Sets the target's health to a specific flat value or percentage. | 0 |
| [`SetItemAux`](#object-setitemaux) | Object | Configures an item's auxiliary value by specifying a target slot and a formula for the new value. | 0 |
| `SetKnockback` | Integer | The knockback distance to set for the damage instance, overriding default. | 0 |
| `SetShield` | Integer | Sets the target's shield value to a specific flat amount. | 0 |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 |
| [`ShowFakeDamage`](Abilities_and_Spells.md#object-showfakedamage) | Object | Displays a fake damage number (with optional style) for visual effect without actually changing health. | 0 |
| `ShowText` | String | Specifies the localization key for a popup text displayed on the target. | 0 |
| [`Slow`](Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 |
| `SpawnBearTrap` | Integer | If non-zero, spawns a bear trap on the tile. | 0 |
| `SpawnBearTrapIfHitKills` | Integer | If non-zero, spawns a bear trap at the target's location upon a killing blow. | 0 |
| `SpawnBearTrapOnMiss` | Integer | The number of bear traps to spawn on the tile adjacent to the target when the unit misses an attack. | 0 |
| `SpawnFlames` | `Array` | An array containing the number of flame tiles to spawn and the chance per tile. | 0 |
| `SpawnThingIfHitKills` | Enum | The name of the thing (e.g., a food type) to spawn at the target's location upon a killing blow. | 0 |
| `SpecificInjury` | Enum | The stat (str, spd, int) to which a specific injury is applied, reducing that stat. | 0 |
| `SpeculativeMoveSelfCorpseOffMap` | Integer | If true, attempts to remove the character's corpse from the map, used for speculative AI targeting. | 0 |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 0 |
| `SpeedUp_WithoutInitiative` | Integer | The number of stacks of Speed Up that do not affect the unit's initiative (turn order) stat. | 0 |
| `StackingSandstorm` | Integer | If non-zero, enables the stacking sandstorm mechanic which increases damage per stack. | 0 |
| `StanceSwitchToMelee` | Integer | If set, switches the source to melee stance. | 0 |
| `StanceSwitchToRanged` | Integer | If set, switches the source to ranged stance. | 0 |
| `status` | Enum | Specifies the status effect to apply in a Temporary object. | 0 |
| [`StatusEachRoundEnd`](Cat_Mutations.md#object-statuseachroundend) | Object | An object listing status effects applied to the unit at the end of each round. | 2 |
| `StatusImmunity` | Array / Enum | A list of status effect names the unit is immune to. | 0 |
| [`StatusRandomEnemiesOnBattleStart`](Events_and_Encounters.md#object-statusrandomenemiesonbattlestart) | Object | An object that applies a status effect to a random number of enemies at the start of battle, with sub-keys for count and the status. | 0 |
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 0 |
| `Stun` | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 0 |
| `T2CopyCat` | Integer | The number of T2 Clone copies created or applied to the target cat. | 0 |
| `TakeExtraTurn` | Integer | The number of extra turns granted to the source. | 0 |
| `TempDexterityUp` | Enum | The number of temporary dexterity stacks applied, or a string alias like 'X'. | 0 |
| `TempLuckUp` | Integer | The amount of temporary luck increase. | 0 |
| [`Temporary`](Abilities_and_Spells.md#object-temporary) | Object | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 0 |
| [`TempPassiveUntilSettled`](Characters_and_Bosses.md#object-temppassiveuntilsettled) | Object | An object containing a temporary passive that is applied until the character's position is settled. | 0 |
| [`TempPassiveWhileHasStatus`](Abilities_and_Spells.md#object-temppassivewhilehasstatus) | Object | An object defining passives temporarily granted to the unit while it has a specific status effect. | 0 |
| `TempStrengthUp` | Equation | The number of stacks of temporary Strength Up applied to the unit. | 0 |
| `TempTrampleUntilSettled` | Integer | The number of stacks of temporary Trample applied to the source, allowing movement through enemies until the source ends its turn. | 0 |
| `Trample` | Integer | The amount of bonus damage dealt when moving through an enemy. | 14 |
| `UseAbility_Madness` | Enum | Determines which ability type (e.g., weapon) is forcibly used when Madness triggers. | 0 |
| `UseAbility_NonStack` | Enum | Specifies an ability to use on kill that does not stack with itself. | 0 |
| `Vaporize` | Integer | Removes the target from play, preventing its corpse from being interacted with. | 0 |
| `VaporizeCorpse` | Integer | If set, vaporizes the target's corpse, preventing revival. | 0 |
| `VaporizeCorpseFlipAdvantage` | `Array` | The number of stacks and probability of vaporizing a corpse to gain loot flip advantage. | 0 |
| `VaporizeInanimate` | Integer | If non-zero, instantly destroys inanimate objects (corpses, rocks) as if they were vaporized. | 0 |
| `VisualFX` | Enum | Specifies the name of the visual effect to play. | 0 |
| [`Weakness`](Passives_and_Statuses.md#object-weakness) | Array / Integer / Object | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 4 |
| `WeaponAuxMultiplier` | Number | A multiplier string (e.g., '.5') for the weapon's auxiliary counter on kill. | 0 |
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
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `AddPassivesToMinions`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 36

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Quivered` | Array / Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 10 | `[1 0.1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `PoisonThorns` | Integer | The number of stacks of Poison applied to melee attackers when they hit this unit. | 6 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`tag_filter`](./Enums.md#enum-tag_filter) | Enum | Specifies a tag (e.g., 'crow', 'rock', 'grub_familiar') used to filter which units a status or effect applies to. | 3 ||
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| [`Buddy`](Characters_and_Bosses.md#object-buddy) | Enum / Object | Specifies a buddy unit that accompanies or is spawned alongside the unit, with optional reclaim and targeting properties. || `spawner` (Enum), `Ornstein` (Enum), `{ ... }` (Object) |
| `DivineShield` | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `[1 .5]` (Array), `[1 .33]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`ForceAttack`](Abilities_and_Spells.md#object-forceattack) | Integer / Object | If set to 1, forces the target to perform an attack against a random or specified target. || `1` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer | The amount of health restored to the source. || `3*X` (Enum), `2*X` (Enum), `2` (Number), `1` (Number) |

</details>

---

#### `AddSelfStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Quivered` | Array / Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 10 | `[1 0.1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Bleed` | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. || `head_HitlersToupe` (Enum), `tk_JarOfRadiation` (Enum), `{ ... }` (Object) |
| [`RandomMagicMissile`](Abilities_and_Spells.md#object-randommagicmissile) | Integer / Object | The number of random magic missiles fired, or an object defining its properties. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `AddSelfStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RepairWeapon` | Array / Integer | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. || `[1 .25]` (Array), `6` (Number), `1` (Number) |
| `ChanceToBreak` | Integer | Specifies the percentage chance that the item breaks on use. | 0 ||
| [`RepairWeapon`](./Arrays.md#array-repairweapon) | Array / Integer | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 0 ||

</details>

---

#### `AddStatusToAllDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Blind` | Array / Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 6 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Blind`](./Arrays.md#array-blind) | Array / Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 6 ||
| [`Conditional_HasStatus`](Abilities_and_Spells.md#object-conditional_hasstatus) | Object | Contains an inner effect block that only executes if the target has the specified status effect. | 3 ||
| [`Conditional_HasTag`](Abilities_and_Spells.md#object-conditional_hastag) | Object | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 3 ||
| `must_do_damage` | Boolean | If true, the status or effect will only be applied if the attack or ability actually deals damage. | 3 ||
| `Rot` | Array / Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. || `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `-999999` (Number), `{ ... }` (Object) |
| [`KnockbackIfCrit`](#object-knockbackifcrit) | Object | Defines knockback properties applied when a critical hit occurs. | 0 ||
| `LeaveBehindRockOnKnockback` | Integer | If non-zero, leaves behind a rock on each tile the target is knocked through. | 0 ||
| `NonLethal` | Integer | If set to 1, damage dealt by the unit cannot kill enemies; it leaves them at 1 HP. | 0 ||
| [`Rot`](./Arrays.md#array-rot) | Array / Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 0 ||
| `BonusKnockbackDamage` | Integer | The extra damage dealt per tile of knockback. | 0 ||

</details>

---

#### `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 248

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Poison` | Array / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Blind` | Array / Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 6 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `[1 .15]` (Array), `[1 .2]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Leech` | Integer | The amount of health leeched from the target (heals the attacker). | 6 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Conditional_Ally`](Abilities_and_Spells.md#object-conditional_ally) | Object | Defines effects that apply only if the target is an ally, with an optional else block for non-allies. | 5 ||
| `Immobile` | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| [`Slow`](Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Weakness`](Passives_and_Statuses.md#object-weakness) | Array / Integer / Object | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_Enemy`](Abilities_and_Spells.md#object-conditional_enemy) | Object | An object containing status effects or actions applied only if the target is an enemy. | 3 ||
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 3 ||
| [`Conditional_Adjacent`](Engine_LogicKeys.md#conditional_adjacent) | Object | An object whose nested keys define statuses or effects applied to or by units that are adjacent to the unit. | 2 ||
| [`Conditional_Shielded`](Abilities_and_Spells.md#object-conditional_shielded) | Object | An object containing effects that are only applied if the target has a shield active. | 2 ||
| [`Leeches`](#object-leeches) | Integer / Object | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 2 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `MagicWeakness` | Array / Integer | The amount of magic weakness stacks applied, or an [stacks, probability] array. | 2 | `[1 .1]` (Array), `[1 .5]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `2` (Number), `-5` (Number) |
| [`SoulLink`](#object-soullink) | Integer / Object | The number of soul link stacks applied. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`Conditional_HasTag`](Abilities_and_Spells.md#object-conditional_hastag) | Object | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 1 ||
| [`Conditional_SourceHasTag`](Engine_LogicKeys.md#conditional_sourcehastag) | Object | Defines a conditional block that applies effects only if the source of the effect has a specified tag. | 1 ||
| `Burn` | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Else`](Abilities_and_Spells.md#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ ... }` (Object) |
| [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). || `{ ... }` (Object) |
| [`BounceObject`](Abilities_and_Spells.md#object-bounceobject) | Enum / Object | Specifies the object or projectile to spawn and bounce from the target. || `AllyRotFly` (Enum), `CharmedFlea_Champion` (Enum), `{ ... }` (Object) |
| `BurgleCoin` | Array / Integer | The number of coins stolen from the target, or an array of `[number, probability]`. || `[1 .5]` (Array), `3` (Number), `1` (Number) |
| [`ChangeTile`](Abilities_and_Spells.md#object-changetile) | Enum / Object | Specifies the tile type to change to, or an object defining tile change parameters (tile type and area of effect). || `LavaTile` (Enum), `TallGrassTile` (Enum), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. || `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `[1 .25]` (Array), `[1 .15]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `FlatLeech` | Integer | The flat amount of health restored to the source when dealing damage, applied after the hit. || `X` (Enum), `5` (Number), `2` (Number) |
| `Freeze` | Array / Integer | The amount of freeze stacks applied, or an [stacks, probability] array. || `[1 .01]` (Array), `[1 .20]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`GainDisorderFromPool`](Characters_and_Bosses.md#object-gaindisorderfrompool) | Enum / Object | Specifies a pool of disorders from which one is randomly gained on basic attack, with an optional chance. || `all_disorders` (Enum), `{ ... }` (Object) |
| `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). || `[25 .01]` (Array), `50` (Number), `999` (Number) |
| `Knockback` | Integer | The number of tiles the target is pushed away from the source on hit. || `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`KnockOutCoin`](Abilities_and_Spells.md#object-knockoutcoin) | Integer / Object | The number of coins knocked out, with an optional probability or an object with stacks and chance. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`KnockUpAndAway`](Abilities_and_Spells.md#object-knockupandaway) | Object | Contains parameters for launching the target upward and away from the source, including stacks and distance. || `{ ... }` (Object) |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. || `[1 .5]` (Array), `222` (Number), `2` (Number), `{ ... }` (Object) |
| [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `ManaLeeches` | Integer | The number of mana leech stacks applied. || `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`Marked`](#object-marked) | Array / Integer / Object | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `3` (Number), `{ ... }` (Object) |
| `OverrideChainKnockback` | Integer | The custom number of tiles for chain knockback, overriding the default. || `10` (Number), `3` (Number) |
| `OverrideChainKnockbackDamage` | String | A formula string that overrides the damage dealt by chain knockback (e.g., "3+bonus_melee_ability_damage"). || `3+bonus_melee_ability_damage` (Enum), `0` (Number) |
| `Petrify` | Array / Integer | The amount of petrify stacks applied, or an [stacks, probability] array. || `[1 .1]` (Array), `[1 .20]` (Array), `1` (Number), `{ ... }` (Object) |
| `Possessed` | Integer | The number of possession stacks applied, or a template with name and tooltips. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `PullSourceToTarget` | Integer | The amount of tiles the source is pulled towards the target after the attack. || `1` (Number) |
| `Rot` | Array / Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. || `[1 .1]` (Array), `[1 .5]` (Array), `-999999` (Number), `2` (Number), `{ ... }` (Object) |
| `SpiderInfested` | Integer | The number of spider infestation stacks applied. || `[1 .5]` (Array), `4` (Number), `1` (Number), `{ ... }` (Object) |
| `SplashDamage` | Integer | The radius (in tiles) for splash damage applied to adjacent targets. || `1` (Number), `2` (Number) |
| [`SpreadDisease`](Abilities_and_Spells.md#object-spreaddisease) | Object | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. || `{ ... }` (Object) |
| `Stun` | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `[1 .25]` (Array), `[1 .15]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| [`Tangled`](Abilities_and_Spells.md#object-tangled) | Array / Integer / Object | The number of stacks of the Tangled status effect applied, or an object defining its properties such as `stacks` and `alt_art`. || `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `VisualFXTile` | Enum | Specifies the name of the visual effect to play on the target tile. || `PoisonPoof` (Enum), `FireBlastSmall` (Enum) |
| `Webbed` | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. || `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `AddStatusToBasicMeleeAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Immobile` | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| `Knockback` | Integer | The number of tiles the target is pushed away from the source on hit. || `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`KnockUpAndAway`](Abilities_and_Spells.md#object-knockupandaway) | Object | Contains parameters for launching the target upward and away from the source, including stacks and distance. || `{ ... }` (Object) |
| [`SpreadDisease`](Abilities_and_Spells.md#object-spreaddisease) | Object | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. || `{ ... }` (Object) |
| `Stun` | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `AddStatusToElementDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AddDamageToElementDamage`](Cat_Mutations.md#object-adddamagetoelementdamage) | Object | Defines additional damage of a specific element added to the unit's attacks. | 6 ||
| [`Conditional_Corpse`](Abilities_and_Spells.md#object-conditional_corpse) | Object | Contains an inner effect block that only executes if the target is a corpse. | 2 ||
| [`element`](./Enums.md#enum-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 1 ||
| `Burn` | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Stun` | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `AddStatusToKnockbackDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 ||
| `Stun` | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 0 ||

</details>

---

#### `AddStatusToSpells`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Leech` | Integer | The amount of health leeched from the target (heals the attacker). | 6 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Leech` | Integer | The amount of health leeched from the target (heals the attacker). | 6 ||
| [`Conditional_Enemy`](Abilities_and_Spells.md#object-conditional_enemy) | Object | An object containing status effects or actions applied only if the target is an enemy. | 1 ||
| `LeechPercent` | Integer | The percentage of damage dealt restored as health. | 0 ||

</details>

---

#### `AddStatusToTrampleDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 ||
| [`Cleave`](Abilities_and_Spells.md#object-cleave) | Integer / Object | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`Cleave`](Abilities_and_Spells.md#object-cleave) | Integer / Object | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. | 0 ||

</details>

---

#### `AddStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Leech` | Integer | The amount of health leeched from the target (heals the attacker). | 6 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Cleave`](Abilities_and_Spells.md#object-cleave) | Integer / Object | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `PullSourceToKnockbackImmuneTarget` | Integer | The amount of pull force applied to the source toward a knockback-immune target. || `1` (Number) |

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
| `YOffset` | Number | The vertical offset applied to the unit's visual position, used for floating or hovering effects. | 6 | `-.18` (String), `.25` (String) |
| `Flying` | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `ApplyStatusIfCrit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Purge`](#object-purge) | Integer / Object | The number of status effects to purge from the target. | 2 | `3` (Number), `0` (Number), `{ ... }` (Object) |
| [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). || `{ ... }` (Object) |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. || `[1 .5]` (Array), `222` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `ApplyStatusesToRandomEnemiesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 3 ||
| `Bounty` | Integer | The number of bounty stacks applied to enemies, increasing rewards on defeat. || `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| [`Marked`](#object-marked) | Array / Integer / Object | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `CatchProjectiles`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localized description string for the item or ability. | 5441 | `"PASSIVE_CATCHPROJECTILES_DESC"` (String) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. | 5027 | `"PASSIVE_CATCHPROJECTILES_NAME"` (String) |
| `Quivered` | Array / Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 10 | `[1 0.1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `ally_chance` | Integer | The percentage chance for an ally to catch incoming projectiles. | 5 ||
| [`chance`](./Enums.md#enum-chance) | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 ||
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `CharacterTypeGainsStatusAtBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 981 ||
| `Stealth` | Array / Integer | The number of stealth stacks applied. | 2 | `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_Flying`](Engine_Uncategorized_Resources.md#conditional_flying) | Object | Defines a conditional block that applies effects or actions only to flying units. | 1 ||
| [`Else`](Abilities_and_Spells.md#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Stun` | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `CritsApplyStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Immobile` | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| [`Weakness`](Passives_and_Statuses.md#object-weakness) | Array / Integer / Object | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_HasStatus`](Abilities_and_Spells.md#object-conditional_hasstatus) | Object | Contains an inner effect block that only executes if the target has the specified status effect. | 2 ||
| [`Else`](Abilities_and_Spells.md#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ ... }` (Object) |
| `Fear` | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. || `Coin` (Enum), `SmallRock` (Enum), `{ ... }` (Object) |
| `Stun` | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `ExtraStatusWhenDealingDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_PartyMember`](Engine_LogicKeys.md#conditional_partymember) | Object | A conditional block that executes its child actions only if the target is a party member. | 3 ||
| [`Conditional_Ally`](Abilities_and_Spells.md#object-conditional_ally) | Object | Defines effects that apply only if the target is an ally, with an optional else block for non-allies. | 2 ||

</details>

---

#### `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 73

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 62 ||
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 54 ||
| `knockback` | Enum / Integer | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 24 ||
| `Poison` | Array / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`InnateElement`](./Enums.md#enum-innateelement) | Enum | Specifies the innate elemental type of the unit (e.g., Fire, Ice, Electric). | 8 ||
| [`AddDamageToElementDamage`](Cat_Mutations.md#object-adddamagetoelementdamage) | Object | Defines additional damage of a specific element added to the unit's attacks. | 6 ||
| `Immobile` | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| [`Weakness`](Passives_and_Statuses.md#object-weakness) | Array / Integer / Object | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`AddStatusToElementDamage`](Items_and_Equipment.md#object-addstatustoelementdamage) | Object | An object that applies a specific status effect when dealing damage of a specified element. Contains sub-keys for the element and the status to apply. | 4 ||
| [`damage`](./Arrays.md#array-damage) | Equation | Specifies the amount of damage dealt, can be a number or expression. | 2 ||
| `cant_miss` | Boolean | If true, the damage instance always hits its target regardless of accuracy or evasion. | 1 ||
| `Freeze` | Array / Integer | The amount of freeze stacks applied, or an [stacks, probability] array. || `[1 .1]` (Array), `[1 0.15]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 0 ||
| [`SpreadDisease`](Abilities_and_Spells.md#object-spreaddisease) | Object | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. || `{ ... }` (Object) |
| [`StatusImmunity`](./Enums.md#enum-statusimmunity) | Array / Enum | A list of status effect names the unit is immune to. | 0 ||

</details>

---

#### `PassiveAfterXKills`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 5118 ||
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 ||

</details>

---

#### `PassiveAtHealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 5118 ||
| [`mode`](./Enums.md#enum-mode) | Enum | Specifies the comparison mode (equal, greater, less_or_equal, etc.) used for a conditional check. | 9 ||
| [`threshold`](Items_and_Equipment.md#object-threshold) | Enum / Integer / Object | The health threshold value, either as a formula using X (max health) or a fixed integer. | 9 ||

</details>

---

#### `PassiveAtStatThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 5118 ||
| [`mode`](./Enums.md#enum-mode) | Enum | Specifies the comparison mode (equal, greater, less_or_equal, etc.) used for a conditional check. | 13 ||
| [`threshold`](Items_and_Equipment.md#object-threshold) | Enum / Integer / Object | The health threshold value, either as a formula using X (max health) or a fixed integer. | 13 ||

</details>

---

#### `PassiveGroup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. || `{ ... }` (Object) |
| `CharismaUp` | Enum / Integer | The amount of charisma change, or a keyword like 'item_aux'. || `[1 .5]` (Array), `5` (Number), `-2` (Number), `{ ... }` (Object) |
| [`FormChange`](Abilities_and_Spells.md#object-formchange) | Enum / Object | Specifies the form the target transforms into, either as a string or an object with a `form` field. || `Fighter` (Enum), `Medic` (Enum), `{ ... }` (Object) |
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. || `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `[1 .5]` (Array), `5` (Number), `-2` (Number), `{ ... }` (Object) |

</details>

---

#### `PassiveWhenAffectedByElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 5118 ||
| [`element`](./Enums.md#enum-element) | Array / Enum | Specifies which element(s) the conditional checks against. | 1 ||

</details>

---

#### `PassiveWhenAtFullMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 20 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Flying` | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `PassiveWhenDead`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`StatusEachTurnBegin`](Cat_Mutations.md#object-statuseachturnbegin) | Object | Specifies status effects applied to the unit at the start of each of its turns. | 16 ||
| [`AutocastEachRound`](Abilities_and_Spells.md#object-autocasteachround) | Enum / Object | Contains an ability name and optional 'even_if_stunned' flag to autocast each round. | 4 | `SpiderReturn` (Enum), `{ ... }` (Object) |
| [`AutocastEachRound`](Abilities_and_Spells.md#object-autocasteachround) | Enum / Object | Contains an ability name and optional 'even_if_stunned' flag to autocast each round. | 4 ||
| [`StatusEachRoundEnd`](Cat_Mutations.md#object-statuseachroundend) | Object | An object listing status effects applied to the unit at the end of each round. | 2 ||
| [`AddStatusToTrampleDamage`](Characters_and_Bosses.md#object-addstatustotrampledamage) | Object | An object whose nested keys define statuses applied to trample damage. | 2 ||

</details>

---

#### `PassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 5118 ||
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 6 ||

</details>

---

#### `PassiveWhileInMonkMeleeStance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 20 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `RandomPassivePool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TransformInXTurns`](Characters_and_Bosses.md#object-transforminxturns) | Object | Defines a delayed transformation after a set number of turns, with optional target object and initiative handling. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 35

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 36 | `[1 .5]` (Array), `5` (Number), `1` (Number), `{ ... }` (Object) |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 36 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 20 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Quivered` | Array / Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 10 | `[1 0.1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Bleed` | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `BleedThorns` | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 8 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Poison` | Array / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Blind` | Array / Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 6 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 6 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `MoveQuivered` | Integer | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 6 | `[1 0.1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Immobile` | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| [`Slow`](Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Weakness`](Passives_and_Statuses.md#object-weakness) | Array / Integer / Object | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`BackflipWhenTargeted`](Abilities_and_Spells.md#object-backflipwhentargeted) | Enum / Integer / Object | The number of backflip charges, or an object defining its ability. | 2 | `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 2 | `[1 .5]` (Array), `40` (Number), `10` (Number), `{ ... }` (Object) |
| `MagicWeakness` | Array / Integer | The amount of magic weakness stacks applied, or an [stacks, probability] array. | 2 | `[1 .1]` (Array), `[1 .5]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| [`PoisonLace`](#object-poisonlace) | Integer / Object / String | Integer or fractional string (e.g., 'X/3') specifying the duration or intensity of the PoisonLace effect. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `2` (Number), `-5` (Number) |
| [`Reflect`](#object-reflect) | Integer / Object | The amount of reflect stacks applied. | 2 | `[1 .5]` (Array), `5` (Number), `1` (Number), `{ ... }` (Object) |
| `Burn` | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Infested`](#object-infested) | Integer / Object | The number of stacks of Infested applied. | 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). || `str` (Enum), `20+bonus_melee_damage` (Enum), `-5` (Number), `-4` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Charge` | Integer | The number of charge stacks applied. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `CharismaUp` | Enum / Integer | The amount of charisma change, or a keyword like 'item_aux'. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. || `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. || `[1 .5]` (Array), `-1` (Number), `-2` (Number), `{ ... }` (Object) |
| `DelayedPain` | Integer | The number of stacks of DelayedPain applied, dealing damage after a delay. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `DexterityUp` | Enum / Integer | The amount of dexterity change, or a keyword like 'item_aux'. || `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `DiminishingHealthRegen` | Integer | The number of diminishing health regen stacks applied. || `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `[1 .5]` (Array), `[1 .33]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Drowsy` | Integer | The amount of drowsy stacks applied, or an [stacks, probability] array. || `[1 .5]` (Array), `8` (Number), `1` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`FormChange`](Abilities_and_Spells.md#object-formchange) | Enum / Object | Specifies the form the target transforms into, either as a string or an object with a `form` field. || `passive` (Enum), `Boris` (Enum), `{ ... }` (Object) |
| `Freeze` | Array / Integer | The amount of freeze stacks applied, or an [stacks, probability] array. || `[1 .1]` (Array), `[1 0.15]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `GainCoins` | Array / Integer | The amount of coins gained, or a [min, max] range. || `[3 5]` (Array), `2` (Number), `-5` (Number) |
| `Hex` | Integer | The number of stacks of Hex applied, causing the target to take increased damage from spells. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. || `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `Lifesteal` | Integer | The amount of lifesteal stacks applied. || `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. || `[1 .5]` (Array), `222` (Number), `2` (Number), `{ ... }` (Object) |
| [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `ManaGain` | Enum / Integer | The amount of mana restored to the source, which can be an expression. || `item_aux` (Enum), `X` (Enum), `5` (Number), `2` (Number), `"max(X*3, 0)"` (String), `"max((X-1)*2, 0)"` (String) |
| [`Marked`](#object-marked) | Array / Integer / Object | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `3` (Number), `{ ... }` (Object) |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. || `SmallRock` (Enum), `BeefyCharmedLeech` (Enum), `{ ... }` (Object) |
| `Ostracized` | Integer | The number of stacks of Ostracized applied. || `[1 .5]` (Array), `4` (Number), `1` (Number), `{ ... }` (Object) |
| `PermanentCharisma` | Integer | The amount of permanent Charisma added to the unit's base stats. || `1` (Number), `2` (Number) |
| `PermanentLuck` | Integer | The amount of permanent Luck added to the unit's base stats. || `1` (Number), `2` (Number) |
| `PermanentStrength` | Integer | The amount of permanent bonus strength (physical damage modifier) granted. || `1` (Number), `2` (Number) |
| `Petrify` | Array / Integer | The amount of petrify stacks applied, or an [stacks, probability] array. || `[1 .1]` (Array), `[1 .20]` (Array), `1` (Number), `{ ... }` (Object) |
| `RandomStatDown` | Array / Integer / String | The amount of random stat reduction applied, either as a fixed number, a formula string, or an array of [stacks, probability]. || `[1 .25]` (Array), `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `1` (Number) |
| `Rot` | Array / Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. || `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `-999999` (Number), `{ ... }` (Object) |
| `Scrambled` | Integer | The number of stacks of Scrambled applied. || `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `Sleep` | Array / Integer | The amount of sleep stacks applied, or an [stacks, probability] array. || `[1 .1]` (Array), `[1 .5]` (Array), `8` (Number), `3` (Number), `{ ... }` (Object) |
| `SpawnCoinAnywhere` | Array / Integer | The number of coins to spawn. If an array, the second value is the probability of spawning them anywhere. || `[1 .5]` (Array), `1` (Number) |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `SpellDamageUp` | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. || `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Stun` | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| `Tarred` | Array / Integer | The amount of tarred stacks applied, or an [stacks, probability] array. || `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `TempCounterAttack` | Integer | The number of turns TempCounterAttack lasts, ticking down at the start of the unit's turn. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 31

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 62 ||
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 54 ||
| `knockback` | Enum / Integer | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 3 ||
| [`damage`](./Arrays.md#array-damage) | Equation | Specifies the amount of damage dealt, can be a number or expression. | 2 ||
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 0 ||

</details>

---

#### `StatusAfterCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TempDamageUp` | Integer | The amount of temporary damage increase applied. || `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `TempRangeUp` | Integer | The amount of temporary range increase applied. || `[1 .5]` (Array), `20` (Number), `3` (Number), `{ ... }` (Object) |
| `TempSpellDamageUp` | Integer | The amount of temporary spell damage increase applied. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object | The name of the ability the target is forced to use. || `GirlDinoPoop` (Enum), `TormentorRuneAbsorb` (Enum), `{ ... }` (Object) |

</details>

---

#### `StatusAfterXTurns`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 ||
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. || `head_HitlersToupe` (Enum), `tk_JarOfRadiation` (Enum), `{ ... }` (Object) |

</details>

---

#### `StatusAllCharactersOnSpawn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Poison` | Array / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_Boss`](Abilities_and_Spells.md#object-conditional_boss) | Object | Contains effects that apply only if the target is a boss enemy. | 2 ||
| [`Conditional_PartyMember`](Engine_LogicKeys.md#conditional_partymember) | Object | A conditional block that executes its child actions only if the target is a party member. | 1 ||
| [`Conditional_Tiny`](Engine_Uncategorized_Resources.md#conditional_tiny) | Object | Defines a conditional block that applies effects only to tiny-sized units. | 1 ||
| [`Else`](Abilities_and_Spells.md#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ ... }` (Object) |

</details>

---

#### `StatusAlliesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `2` (Number), `-5` (Number) |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 ||
| [`Conditional_Adjacent`](Engine_LogicKeys.md#conditional_adjacent) | Object | An object whose nested keys define statuses or effects applied to or by units that are adjacent to the unit. | 1 ||
| `exclude_self` | Boolean | If true, the effect does not apply to the source unit itself. | 1 ||

</details>

---

#### `StatusAlliesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 20 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. || `[1 .5]` (Array), `-1` (Number), `-2` (Number), `{ ... }` (Object) |
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. || `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. || `[1 .5]` (Array), `222` (Number), `2` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusAlliesOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Reanimate`](#object-reanimate) | Integer / Object | The percentage chance to reanimate the target. | 4 | `50` (Number), `100` (Number), `{ ... }` (Object) |
| `triggers_limit` | Integer | The maximum number of times this passive effect can trigger per battle. | 2 ||
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `[1 .5]` (Array), `[1 .33]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Freeze` | Array / Integer | The amount of freeze stacks applied, or an [stacks, probability] array. || `[1 .1]` (Array), `[1 0.15]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusEachRoundEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DoDamage`](Abilities_and_Spells.md#object-dodamage) | Object | Contains damage parameters (amount, type, tile targets) to deal damage to the target. || `{ ... }` (Object) |
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object | The name of the ability the target is forced to use. || `GirlDinoPoop` (Enum), `Spit` (Enum), `{ ... }` (Object) |

</details>

---

#### `StatusEachTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 27

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MissChance` | Integer | The flat percentage chance that the unit's attacks will miss. | 24 | `[1 .5]` (Array), `5` (Number), `10` (Number), `{ ... }` (Object) |
| `Quivered` | Array / Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 10 | `[1 0.1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `MoveQuivered` | Integer | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 6 | `[1 0.1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Conditional_BadRoll`](Abilities_and_Spells.md#object-conditional_badroll) | Object | An object containing an `odds` value and effects that are applied when a random roll succeeds. | 5 ||
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `2` (Number), `-5` (Number) |
| [`Revive`](#object-revive) | Integer / Object | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 2 | `50` (Number), `100` (Number), `{ ... }` (Object) |
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 1 ||
| `Burn` | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `BlessingOfPeace` | Integer | The number of stacks of the Blessing of Peace status applied to the unit each turn. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `DoubleCastSpellThisTurn` | Integer | If non-zero, grants the unit a double cast effect for spells this turn. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `FillMana` | Integer | The amount of mana restored, or an [amount, probability] array. || `[1 .10]` (Array), `[1 .25]` (Array), `1` (Number) |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. || `head_HitlersToupe` (Enum), `tk_JarOfRadiation` (Enum), `{ ... }` (Object) |
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. || `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object | The name of the ability the target is forced to use. || `GirlDinoPoop` (Enum), `TormentorRuneAbsorb` (Enum), `{ ... }` (Object) |
| `Wet` | Integer | The number of stacks of the Wet status effect applied. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 57

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 6 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 2 ||
| [`Cleanse`](#object-cleanse) | Integer / Object | The number of stacks of negative status effects removed from the target. | 2 | `0` (Number), `1` (Number), `{ ... }` (Object) |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `2` (Number), `-5` (Number) |
| `Stealth` | Array / Integer | The number of stealth stacks applied. | 2 | `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_BadRoll`](Abilities_and_Spells.md#object-conditional_badroll) | Object | An object containing an `odds` value and effects that are applied when a random roll succeeds. | 1 ||
| [`Conditional_HasCleansableDebuffs`](Abilities_and_Spells.md#object-conditional_hascleansabledebuffs) | Object | An object containing effects that execute only if the unit has cleansable debuffs. | 1 ||
| [`Conditional_ManaThreshold`](Engine_LogicKeys.md#conditional_manathreshold) | Object | Defines a conditional block that applies effects only if a unit's mana meets a specified threshold. | 1 ||
| `Burn` | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `AddWeaponAux` | Integer / String | The amount or expression to add to the source's weapon auxiliary stat. || `-item_aux` (Enum), `2` (Number), `1` (Number), `"-max(min(X+1, item_aux), 0)"` (String) |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Charge` | Integer | The number of charge stacks applied. || `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. || `[1 .5]` (Array), `-1` (Number), `-2` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `[1 .5]` (Array), `[1 .33]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. || `head_HitlersToupe` (Enum), `tk_RoboSucc` (Enum), `{ ... }` (Object) |
| `HealthGain` | Integer | The amount of health restored to the source. || `3*X` (Enum), `2*X` (Enum), `5` (Number), `10` (Number) |
| [`ImmediateUseAbility`](#object-immediateuseability) | Enum / Object | Specifies the name of an ability to be triggered instantly from this effect. || `MoonHandMegaSqueeze` (Enum), `head_ThrobbingCrown` (Enum), `{ ... }` (Object) |
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. || `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `NonStackingDivineShield` | Integer | The number of Divine Shield stacks that do not stack with duplicates. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. || `SmallRock` (Enum), `SkeletonCatFamiliar` (Enum), `{ ... }` (Object) |
| `PermanentMadness` | Integer | The number of permanent madness stacks applied. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `PreEmptiveCounterNextAttacks` | Integer | The number of next incoming attacks that the unit will counter preemptively before they land. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `RandomStatDown` | Array / Integer / String | The amount of random stat reduction applied, either as a fixed number, a formula string, or an array of [stacks, probability]. || `[1 .25]` (Array), `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `1` (Number) |
| `RangeUp` | Integer | The number of stacks of bonus attack range applied. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `SpawnCoinAnywhere` | Array / Integer | The number of coins to spawn. If an array, the second value is the probability of spawning them anywhere. || `[1 .5]` (Array), `1` (Number) |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusEachTurnEndForEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. || `head_HitlersToupe` (Enum), `tk_JarOfRadiation` (Enum), `{ ... }` (Object) |
| [`RandomMagicMissile`](Abilities_and_Spells.md#object-randommagicmissile) | Integer / Object | The number of random magic missiles fired, or an object defining its properties. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusEveryXSpellCasts`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 8 ||
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Charge` | Integer | The number of charge stacks applied. || `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. || `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. || `SmallRock` (Enum), `SkeletonCatFamiliar` (Enum), `{ ... }` (Object) |
| [`RandomMagicMissile`](Abilities_and_Spells.md#object-randommagicmissile) | Integer / Object | The number of random magic missiles fired, or an object defining its properties. || `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `ReduceManaCost` | Integer | The number of stacks reducing mana cost of abilities. || `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `RepairWeapon` | Array / Integer | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. || `[1 .25]` (Array), `99` (Number), `1` (Number) |
| `RepairWeaponCondition` | Integer | The amount of weapon condition restored. || `1` (Number) |
| `SpellDamageUp` | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. || `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusGroup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DexterityUp` | Enum / Integer | The amount of dexterity change, or a keyword like 'item_aux'. || `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Specifies the loot pool from which to find an item, with an optional chance. || `mutant_pool` (Enum), `parasites` (Enum), `{ ... }` (Object) |
| `Freeze` | Array / Integer | The amount of freeze stacks applied, or an [stacks, probability] array. || `[1 .1]` (Array), `[1 0.15]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. || `[1 .5]` (Array), `222` (Number), `2` (Number), `{ ... }` (Object) |
| `SpawnCoinAnywhere` | Array / Integer | The number of coins to spawn. If an array, the second value is the probability of spawning them anywhere. || `[1 .5]` (Array), `1` (Number) |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusIfUnusedMovePoints`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 20 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `MoveQuivered` | Integer | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 6 | `[1 0.1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Charge` | Integer | The number of charge stacks applied. || `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. || `[1 .5]` (Array), `-1` (Number), `-2` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `[1 .5]` (Array), `[1 .33]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer | The amount of health restored to the source. || `3*X` (Enum), `2*X` (Enum), `5` (Number), `10` (Number) |
| `ManaGain` | Enum / Integer | The amount of mana restored to the source, which can be an expression. || `X` (Enum), `item_aux` (Enum), `5` (Number), `2` (Number), `"max(X*3, 0)"` (String), `"max((X-1)*2, 0)"` (String) |

</details>

---

#### `StatusKilledCharacters`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_RandomChance`](Abilities_and_Spells.md#object-conditional_randomchance) | Object | An object containing effects that execute only if a random roll succeeds, with an odds value defined inside. | 2 ||
| [`Conditional_Ally`](Abilities_and_Spells.md#object-conditional_ally) | Object | Defines effects that apply only if the target is an ally, with an optional else block for non-allies. | 1 ||
| `AutoReanimate` | Number | The percentage chance for the unit to automatically reanimate upon death. || `100` (Number), `50` (Number) |
| `AutoReanimate` | Number | The percentage chance for the unit to automatically reanimate upon death. | 0 ||

</details>

---

#### `StatusKillers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 ||
| [`Conditional_Boss`](Abilities_and_Spells.md#object-conditional_boss) | Object | Contains effects that apply only if the target is a boss enemy. | 2 ||
| [`Conditional_NotBoss`](Abilities_and_Spells.md#object-conditional_notboss) | Object | Contains effects that apply only if the target is not a boss enemy. | 2 ||

</details>

---

#### `StatusOnAllyCatDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `[1 .5]` (Array), `[1 .33]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `FillMana` | Integer | The amount of mana restored, or an [amount, probability] array. || `[1 .10]` (Array), `[1 .25]` (Array), `1` (Number) |
| `HealthGain` | Integer | The amount of health restored to the source. || `3*X` (Enum), `2*X` (Enum), `5` (Number), `10` (Number) |

</details>

---

#### `StatusOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 53

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `even_if_dead` | Boolean | If true, the effect triggers even if the unit is dead. | 25 ||
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 6 ||
| [`Conditional_Corpse`](Abilities_and_Spells.md#object-conditional_corpse) | Object | Contains an inner effect block that only executes if the target is a corpse. | 1 ||
| [`Conditional_Shielded`](Abilities_and_Spells.md#object-conditional_shielded) | Object | An object containing effects that are only applied if the target has a shield active. | 1 ||
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Specifies the loot pool from which to find an item, with an optional chance. || `pills` (Enum), `chapter_specific_item` (Enum), `{ ... }` (Object) |
| `GainCoins` | Array / Integer | The amount of coins gained, or a [min, max] range. || `[3 5]` (Array), `5` (Number), `2` (Number) |
| `PermanentStrength` | Integer | The amount of permanent bonus strength (physical damage modifier) granted. || `1` (Number), `2` (Number) |
| `RepairAll` | Integer | The amount of durability restored to all equipped items. || `10` (Number), `1` (Number) |
| `RepairWeapon` | Array / Integer | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. || `[1 .25]` (Array), `99` (Number), `1` (Number) |
| [`TransformWeapon`](Abilities_and_Spells.md#object-transformweapon) | Object | An object with `from` and `to` fields specifying the weapon transformation. || `{ ... }` (Object) |

</details>

---

#### `StatusOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 20 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Craft`](Abilities_and_Spells.md#object-craft) | Object | Specifies the loot pool and slot to craft an item for the source. | 2 | `{ ... }` (Object) |
| [`DestroyEquipmentAndAttachParasite`](Abilities_and_Spells.md#object-destroyequipmentandattachparasite) | Object | Attempts to destroy a random piece of the target's equipment and attach a parasite from the specified pool. || `{ ... }` (Object) |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Specifies the loot pool from which to find an item, with an optional chance. || `chapter` (Enum), `pills` (Enum), `{ ... }` (Object) |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. || `head_HitlersToupe` (Enum), `tk_JarOfRadiation` (Enum), `{ ... }` (Object) |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. || `SmallRock` (Enum), `SkeletonCatFamiliar` (Enum), `{ ... }` (Object) |
| [`RandomMagicMissile`](Abilities_and_Spells.md#object-randommagicmissile) | Integer / Object | The number of random magic missiles fired, or an object defining its properties. || `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`ReviveNextRound`](Abilities_and_Spells.md#object-revivenextround) | Integer / Object | The number of revives granted, or an object defining revive properties. || `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `SafeDie` | Integer | The number of times the unit can survive a fatal hit. || `1` (Number) |
| `Sleep` | Array / Integer | The amount of sleep stacks applied, or an [stacks, probability] array. || `[1 .1]` (Array), `[1 .5]` (Array), `8` (Number), `3` (Number), `{ ... }` (Object) |
| `StealthUntilBasicAttack` | Integer | The number of stacks of Stealth that are removed when the unit performs a basic attack. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusOnBreak`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 22

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`ApplyToRandomPartyMemberIfPossible`](Abilities_and_Spells.md#object-applytorandompartymemberifpossible) | Object | Contains an inner effect block that is applied to a random living party member if one exists. || `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. || `[1 .5]` (Array), `-1` (Number), `-2` (Number), `{ ... }` (Object) |
| `DexterityUp` | Enum / Integer | The amount of dexterity change, or a keyword like 'item_aux'. || `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Specifies the loot pool from which to find an item, with an optional chance. || `chapter` (Enum), `pills` (Enum), `{ ... }` (Object) |
| `HealthGain` | Integer | The amount of health restored to the source. || `3*X` (Enum), `2*X` (Enum), `5` (Number), `10` (Number) |
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. || `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. || `BestBud` (Enum), `SmallRock` (Enum), `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusOnBreakItem`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 36 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`DoDamage`](Abilities_and_Spells.md#object-dodamage) | Object | Contains damage parameters (amount, type, tile targets) to deal damage to the target. || `{ ... }` (Object) |

</details>

---

#### `StatusOnCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Charge` | Integer | The number of charge stacks applied. || `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer | The amount of health restored to the source. || `3*X` (Enum), `2*X` (Enum), `5` (Number), `10` (Number) |

</details>

---

#### `StatusOnCollectPickup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Tech` | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 2 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusOnDie`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_RandomChance`](Abilities_and_Spells.md#object-conditional_randomchance) | Object | An object containing effects that execute only if a random roll succeeds, with an odds value defined inside. | 1 ||
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Specifies the loot pool from which to find an item, with an optional chance. || `pills` (Enum), `chapter_common` (Enum), `{ ... }` (Object) |
| [`RandomMagicMissile`](Abilities_and_Spells.md#object-randommagicmissile) | Integer / Object | The number of random magic missiles fired, or an object defining its properties. || `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `RemoveAmbientLightEffects` | Number | The fade-out duration in seconds for ambient light effects. || `4` (Number), `.5` (String) |
| [`ScatterCoins`](Abilities_and_Spells.md#object-scattercoins) | Object | The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula. || `[1 .5]` (Array), `5` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusOnEatFood`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Cleanse`](#object-cleanse) | Integer / Object | The number of stacks of negative status effects removed from the target. | 2 | `0` (Number), `1` (Number), `{ ... }` (Object) |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `2` (Number), `-5` (Number) |
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. || `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusOnEatPill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 0 ||
| [`RandomPermanentStatsDistinct`](#object-randompermanentstatsdistinct) | Object | An object defining a set of stat changes (positive and negative) that are randomly applied as permanent modifications. | 0 ||

</details>

---

#### `StatusOnEndMove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_FirstApplicationThisTurn`](Abilities_and_Spells.md#object-conditional_firstapplicationthisturn) | Object | Container for effects applied only on the first application of this ability during the turn. | 1 ||
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 1 ||
| `Charge` | Integer | The number of charge stacks applied. || `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `[1 .5]` (Array), `[1 .33]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`ForceAttack`](Abilities_and_Spells.md#object-forceattack) | Integer / Object | If set to 1, forces the target to perform an attack against a random or specified target. || `1` (Number), `{ ... }` (Object) |
| [`ImmediateUseAbility`](#object-immediateuseability) | Enum / Object | Specifies the name of an ability to be triggered instantly from this effect. || `MoonHandMegaSqueeze` (Enum), `head_MagnetoAttract` (Enum), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `SpeedUp_WithoutInitiative` | Integer | The number of stacks of Speed Up that do not affect the unit's initiative (turn order) stat. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`RemoveStatusStacks`](Abilities_and_Spells.md#object-removestatusstacks) | Object | An object specifying a status name and the number of stacks to remove from the target. | 0 ||
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 0 ||
| [`ImmediateUseAbility`](#object-immediateuseability) | Enum / Object | Specifies the name of an ability to be triggered instantly from this effect. | 0 ||
| `Charge` | Integer | The number of charge stacks applied. | 0 ||
| `SpeedUp_WithoutInitiative` | Integer | The number of stacks of Speed Up that do not affect the unit's initiative (turn order) stat. | 0 ||
| [`ForceAttack`](Abilities_and_Spells.md#object-forceattack) | Integer / Object | If set to 1, forces the target to perform an attack against a random or specified target. | 0 ||
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 0 ||

</details>

---

#### `StatusOnGainCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`BackflipWhenTargeted`](Abilities_and_Spells.md#object-backflipwhentargeted) | Enum / Integer / Object | The number of backflip charges, or an object defining its ability. | 2 | `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `[1 .5]` (Array), `[1 .33]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. || `[1 .5]` (Array), `222` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusOnHealed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 36 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. || `SmallRock` (Enum), `SkeletonCatFamiliar` (Enum), `{ ... }` (Object) |

</details>

---

#### `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 40

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 4 ||
| [`Conditional_FirstApplicationThisTurn`](Abilities_and_Spells.md#object-conditional_firstapplicationthisturn) | Object | Container for effects applied only on the first application of this ability during the turn. | 2 ||
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `2` (Number), `-5` (Number) |
| `Stealth` | Array / Integer | The number of stealth stacks applied. | 2 | `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `CharismaUp` | Enum / Integer | The amount of charisma change, or a keyword like 'item_aux'. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. || `[1 .5]` (Array), `-1` (Number), `-2` (Number), `{ ... }` (Object) |
| `DexterityUp` | Enum / Integer | The amount of dexterity change, or a keyword like 'item_aux'. || `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer | The amount of health restored to the source. || `3*X` (Enum), `2*X` (Enum), `5` (Number), `10` (Number) |
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. || `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. || `[1 .5]` (Array), `222` (Number), `2` (Number), `{ ... }` (Object) |
| `RangeUp` | Integer | The number of stacks of bonus attack range applied. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `BrittleCharismaUp` | Integer | The number of stacks of temporary Charisma gained on kill. | 0 ||
| `BrittleConstitutionUp` | Integer | The number of stacks of temporary Constitution gained on kill. | 0 ||
| `BrittleDexterityUp` | Integer | The number of stacks of temporary Dexterity gained on kill. | 0 ||
| `BrittleIntelligenceUp` | Integer | The number of stacks of temporary Intelligence gained on kill. | 0 ||
| `BrittleLuckUp` | Integer | The number of stacks of temporary Luck gained on kill. | 0 ||
| `BrittleSpeedUp` | Integer | The number of stacks of temporary Speed gained on kill. | 0 ||
| `BrittleStrengthUp` | Integer | The number of stacks of temporary Strength gained on kill. | 0 ||
| [`UseAbility_NonStack`](./Enums.md#enum-useability_nonstack) | Enum | Specifies an ability to use on kill that does not stack with itself. | 0 ||

</details>

---

#### `StatusOnKillEnemy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 20 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `[1 .5]` (Array), `[1 .33]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. || `head_HitlersToupe` (Enum), `tk_JarOfRadiation` (Enum), `{ ... }` (Object) |
| `HealthGain` | Integer | The amount of health restored to the source. || `3*X` (Enum), `2*X` (Enum), `5` (Number), `2` (Number) |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. || `[1 .5]` (Array), `222` (Number), `2` (Number), `{ ... }` (Object) |
| `ManaGain` | Enum / Integer | The amount of mana restored to the source, which can be an expression. || `X` (Enum), `item_aux` (Enum), `5` (Number), `2` (Number), `"max(X*3, 0)"` (String), `"max((X-1)*2, 0)"` (String) |

</details>

---

#### `StatusOnPickupCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DexterityUp` | Enum / Integer | The amount of dexterity change, or a keyword like 'item_aux'. || `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `GainCoins` | Array / Integer | The amount of coins gained, or a [min, max] range. || `[3 5]` (Array), `5` (Number), `2` (Number) |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusOnPopCorpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthGain` | Integer | The amount of health restored to the source. || `3*X` (Enum), `2*X` (Enum), `2` (Number), `1` (Number) |
| `RepairWeapon` | Array / Integer | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. || `[1 .25]` (Array), `99` (Number), `1` (Number) |

</details>

---

#### `StatusOnTookDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 46

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 36 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Bleed` | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_HasStatus`](Abilities_and_Spells.md#object-conditional_hasstatus) | Object | Contains an inner effect block that only executes if the target has the specified status effect. | 2 ||
| [`Craft`](Abilities_and_Spells.md#object-craft) | Object | Specifies the loot pool and slot to craft an item for the source. | 2 | `{ ... }` (Object) |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 2 | `[1 .5]` (Array), `5` (Number), `40` (Number), `{ ... }` (Object) |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `2` (Number), `-5` (Number) |
| [`Conditional_HealthThreshold`](Abilities_and_Spells.md#object-conditional_healththreshold) | Object | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 1 ||
| [`Else`](Abilities_and_Spells.md#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ ... }` (Object) |
| `Charge` | Integer | The number of charge stacks applied. || `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. || `[1 .5]` (Array), `-1` (Number), `-2` (Number), `{ ... }` (Object) |
| `DiminishingHealthRegen` | Integer | The number of diminishing health regen stacks applied. || `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `[1 .5]` (Array), `[1 .33]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. || `[1 .5]` (Array), `-1` (Number), `3` (Number), `{ ... }` (Object) |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. || `[1 .5]` (Array), `222` (Number), `2` (Number), `{ ... }` (Object) |
| `MovementUp` | Integer | The amount of movement increase or decrease applied. || `[1 .5]` (Array), `-2` (Number), `1` (Number), `{ ... }` (Object) |
| `RandomInjury` | Integer | The number of random injuries applied. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `TempDamageUp` | Integer | The amount of temporary damage increase applied. || `[1 .5]` (Array), `-1` (Number), `1` (Number), `{ ... }` (Object) |
| `TempMovement` | Enum / Integer | The amount of temporary movement range added, or a string alias like 'mov'. || `[1 .5]` (Array), `1` (Number), `20` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusOnTookDamageFromAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Bleed` | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `DiminishingHealthRegen` | Integer | The number of diminishing health regen stacks applied. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `ExtraBasicAttacks_Status` | Integer | The number of additional basic attacks the unit can perform each turn. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusOnUseBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer | The amount of health restored to the source. || `3*X` (Enum), `2*X` (Enum), `5` (Number), `10` (Number) |

</details>

---

#### `StatusRandomEnemiesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`count`](./Arrays.md#array-count) | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 3 ||
| `Charmed` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. || `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Freeze` | Array / Integer | The amount of freeze stacks applied, or an [stacks, probability] array. || `[1 .1]` (Array), `[1 0.15]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusWhenAllySpendsMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Charge` | Integer | The number of charge stacks applied. || `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `ManaGain` | Enum / Integer | The amount of mana restored to the source, which can be an expression. || `X` (Enum), `item_aux` (Enum), `5` (Number), `2` (Number), `"max(X*3, 0)"` (String), `"max((X-1)*2, 0)"` (String) |
| [`OneUseSpellDamageUp`](#object-oneusespelldamageup) | Array / Number / Object | Increases spell damage by the specified amount, but the effect is consumed after a single use. Alias for SpellDamageUp. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `TakeBonusTurnWithAIControl`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `include_spells` | Boolean | If true, the AI-controlled bonus turn includes spells as available actions. | 3 ||
| `end_of_round` | Boolean | If true, the effect triggers at the end of the round instead of at the start of the turn. | 1 ||

</details>

---

#### `TakeBonusTurnWithStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Stun` | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `TempPassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 3 ||

</details>

---

#### `additional_passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `FillMana` | Integer | The amount of mana restored, or an [amount, probability] array. || `[1 .10]` (Array), `[1 .25]` (Array), `1` (Number) |
| `HealthGain` | Integer | The amount of health restored to the source. || `3*X` (Enum), `2*X` (Enum), `5` (Number), `10` (Number) |
| `PermanentMadness` | Integer | The number of permanent madness stacks applied. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`ReviveNextRound`](Abilities_and_Spells.md#object-revivenextround) | Integer / Object | The number of revives granted, or an object defining revive properties. || `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `SafeDoomed` | Enum / Integer | The number of SafeDoomed stacks applied, or 'level' to scale with character level. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `bonus_passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 138

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 36 | `[1 .5]` (Array), `5` (Number), `1` (Number), `{ ... }` (Object) |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Trample` | Integer | The amount of bonus damage dealt when moving through an enemy. | 14 | `[1 .5]` (Array), `[3 X-8]` (Array), `5` (Number), `9` (Number), `{ ... }` (Object) |
| [`AutocastEachRound`](Abilities_and_Spells.md#object-autocasteachround) | Enum / Object | Contains an ability name and optional 'even_if_stunned' flag to autocast each round. | 4 | `SpiderReturn` (Enum), `{ ... }` (Object) |
| `AlphaDodgeChance` | Integer | The dodge chance granted to the alpha (leader) unit. || `[1 .5]` (Array), `50` (Number), `1` (Number), `{ ... }` (Object) |
| `DownRankAIIfWeaponUsable` | Number | A multiplier that reduces the AI's priority to use this ability if the unit has a usable weapon. || `.001` (String) |
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. || `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| [`XIsSpellStormRampAndReset`](Abilities_and_Spells.md#object-xisspellstormrampandreset) | Integer / Object | If integer 0, resets stacks; if object, contains 'stacks' and 'reset_percent' for spell storm ramp. || `0` (Number), `{ ... }` (Object) |

</details>

---

#### `extra_statuses`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Poison` | Array / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_HasTag`](Abilities_and_Spells.md#object-conditional_hastag) | Object | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 1 ||
| `Burn` | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer | The amount of health restored to the source. || `3*X` (Enum), `2*X` (Enum), `5` (Number), `10` (Number) |
| `Tarred` | Array / Integer | The amount of tarred stacks applied, or an [stacks, probability] array. || `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `party_status_next_fight`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 24

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Bleed` | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Poison` | Array / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Immobile` | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `[1 .5]` (Array), `[1 .33]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`NoHealthRegen`](#object-nohealthregen) | Array / Number / Object | Prevents the unit from regenerating health normally. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`Tangled`](Abilities_and_Spells.md#object-tangled) | Array / Integer / Object | The number of stacks of the Tangled status effect applied, or an object defining its properties such as `stacks` and `alt_art`. || `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Tarred` | Array / Integer | The amount of tarred stacks applied, or an [stacks, probability] array. || `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `Webbed` | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. || `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |

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
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `MissChance` | Integer | The flat percentage chance that the unit's attacks will miss. | 24 | `[1 .5]` (Array), `5` (Number), `10` (Number), `{ ... }` (Object) |
| `Bleed` | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Poison` | Array / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Blind` | Array / Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 6 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Slow`](Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Burn` | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `CharismaUp` | Enum / Integer | The amount of charisma change, or a keyword like 'item_aux'. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. || `[1 .5]` (Array), `-1` (Number), `-2` (Number), `{ ... }` (Object) |
| `DexterityUp` | Enum / Integer | The amount of dexterity change, or a keyword like 'item_aux'. || `[1 .5]` (Array), `-1` (Number), `1` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `[1 .5]` (Array), `[1 .33]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. || `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. || `[1 .5]` (Array), `222` (Number), `2` (Number), `{ ... }` (Object) |
| [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`NoHealthRegen`](#object-nohealthregen) | Array / Number / Object | Prevents the unit from regenerating health normally. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`NoManaRegen`](Passives_and_Statuses.md#object-nomanaregen) | Array / Number / Object | The unit does not naturally regenerate mana per turn. Value indicates the stage or flag enabling this restriction. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`PermanentConfusion`](#object-permanentconfusion) | Array / Number / Object | If set to 1, the unit is permanently confused and cannot be cured. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `ProbeCharmed` | Integer | The number of charm stacks applied by a probe. || `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Rot` | Array / Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. || `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `-999999` (Number), `{ ... }` (Object) |
| `Sleep` | Array / Integer | The amount of sleep stacks applied, or an [stacks, probability] array. || `[1 .1]` (Array), `[1 .5]` (Array), `8` (Number), `3` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `SpiderInfested` | Integer | The number of spider infestation stacks applied. || `[1 .5]` (Array), `4` (Number), `1` (Number), `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Stun` | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| `Tarred` | Array / Integer | The amount of tarred stacks applied, or an [stacks, probability] array. || `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `TempStrengthUp` | Enum | The number of stacks of temporary Strength Up applied to the unit. || `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Webbed` | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. || `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |

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

### Object: `AlphaDodgeChance`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum | Specifies the reference name of another status effect to alias or copy properties from. || `DodgeChance_Status` (Enum) |

### Object: `AlphaStatusOnTurnBegin`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DoubleCastSpellThisTurn` | Integer | If non-zero, grants the unit a double cast effect for spells this turn. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |

### Object: `ApplyPassivesToSpawnerWhileAlive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HideEquipment` | Enum | Specifies which equipment slot is visually hidden. | 2 | `neck` (Enum) |

### Object: `ApplyToRandomPartyMemberIfPossible`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`GainDisorderFromPool`](Characters_and_Bosses.md#object-gaindisorderfrompool) | Enum / Object | Specifies a pool of disorders from which one is randomly gained on basic attack, with an optional chance. | 4 | `all_disorders` (Enum), `{ ... }` (Object) |

### Object: `ApplyToSource`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 12 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer | The amount of health restored to the source. | 12 | `2*X` (Enum), `3*X` (Enum), `3` (Number), `8` (Number) |
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 12 | `[1 .5]` (Array), `4` (Number), `-2` (Number), `{ ... }` (Object) |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 10 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`EvolveAbilityFromPool`](Abilities_and_Spells.md#object-evolveabilityfrompool) | Enum / Object | Specifies the ability pool from which to evolve an ability for the source, optionally upgrading it. | 8 | `Medic` (Enum), `Psychic` (Enum), `{ ... }` (Object) |
| [`FormChange`](Abilities_and_Spells.md#object-formchange) | Enum / Object | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 8 | `Default` (Enum), `passive` (Enum), `{ ... }` (Object) |
| `AddWeaponAux` | Integer / String | The amount or expression to add to the source's weapon auxiliary stat. | 6 | `-item_aux` (Enum), `1` (Number), `2` (Number), `"-max(min(X+1, item_aux), 0)"` (String) |
| `ConstitutionUp` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 6 | `[1 .5]` (Array), `-1` (Number), `-2` (Number), `{ ... }` (Object) |
| `Charge` | Integer | The number of charge stacks applied. | 4 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| [`Cleanse`](#object-cleanse) | Integer / Object | The number of stacks of negative status effects removed from the target. | 4 | `1` (Number), `0` (Number), `{ ... }` (Object) |
| `EquipPermanentItem` | Enum | The name of the item to permanently equip to the source. | 4 | `BoneClub` (Enum), `Kidney` (Enum) |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Specifies the loot pool from which to find an item, with an optional chance. | 4 | `chapter_specific_item` (Enum), `chapter_common` (Enum), `{ ... }` (Object) |
| `FreeSpell` | Integer | The number of stacks of Free Spell applied to the source, allowing the next spells to be cast without mana cost. | 4 | `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 4 | `[1 .5]` (Array), `-4` (Number), `3` (Number), `{ ... }` (Object) |
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 2 | `[1 .5]` (Array), `10` (Number), `4` (Number), `{ ... }` (Object) |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 2 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 2 | `[1 .5]` (Array), `[1 .33]` (Array), `4` (Number), `1` (Number), `{ ... }` (Object) |
| `FindItem` | Enum | The name of the specific item to find and add to the source's inventory. | 2 | `BoneClub` (Enum), `Pearl` (Enum) |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. | 2 | `neck_ChefsApron` (Enum), `head_HitlersToupe` (Enum), `{ ... }` (Object) |
| [`GainCoinsRange`](Abilities_and_Spells.md#object-gaincoinsrange) | Object | An object with `min` and `max` fields specifying a range for the amount of coins gained. | 2 | `{ ... }` (Object) |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 2 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `ManaGain` | Enum / Integer | The amount of mana restored to the source, which can be an expression. | 2 | `X-1` (Enum), `X+2` (Enum), `15` (Number), `10` (Number), `"max((X-1)*2, 0)"` (String), `"max(X*3, 0)"` (String) |
| `MoveQuivered` | Integer | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 2 | `[1 0.1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | `[1 .5]` (Array), `-2` (Number), `6` (Number), `{ ... }` (Object) |
| `Tech` | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 2 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |

### Object: `BlessingOfPeace`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_BLESSINGOFPEACE_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_BLESSINGOFPEACE_DESC"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_BLESSINGOFPEACE_DESC_STACKLESS"` (String) |

### Object: `BounceObject`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `obj` | Array / Enum | Specifies one or more object names to bounce towards the target. | 6 | `SmallLavaRock` (Enum), `chapter_corpse_medium` (Enum) |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 4 | `.5` (String), `.25` (String) |
| `slide` | Integer | The number of tiles the bounced object slides toward the target. | 2 | `10` (Number) |

### Object: `Bounty`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_BOUNTY_NAME"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_BOUNTY_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_BOUNTY_DESC"` (String) |

### Object: `ChangeTile`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `tile` | Array / Enum | Specifies the tile type(s) to change to, either a single tile string or an array of tiles. | 22 | `[TallGrassTile TallFlowerTile BrambleTile]` (Array), `LavaTile` (Enum), `ToxicTile` (Enum) |
| `aoe` | Integer | The radius (in tiles) of the area affected by the tile change. | 4 | `1` (Number) |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 4 | `25` (Number), `.25` (String) |

### Object: `CharismaUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_CHAUP_NAME"` (String) |
| `name_stacks_neg` | String | Localization key for the name of the negative variant (e.g., stat down) of this status effect. || `"KEYWORD_CHADOWN_NAME"` (String) |
| `tooltip_stackless` | Enum | A localization key for the tooltip description of this status effect when it has no stack count. || `none` (Enum) |
| `tooltip_stacks_neg` | String | Localization key for the tooltip description of the negative variant (e.g., stat down) of this status effect. || `"KEYWORD_CHADOWN_DESC"` (String) |
| `tooltip_stacks_pos` | String | Localization key for the tooltip description of the positive variant (e.g., stat up) of this status effect. || `"KEYWORD_CHAUP_DESC"` (String) |

### Object: `Charmed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_CHARMED_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_CHARMED_DESC"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_CHARMED_DESC_STACKLESS"` (String) |

### Object: `Cleanse`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `spell` (Enum) |

### Object: `Cleave`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | `.25` (String) |
| `icon_frame` | Number | The sprite frame index for the buff icon. || `152` (Number) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_CLEAVE_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_CLEAVE_DESC"` (String) |

### Object: `Conditional_Adjacent`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 4 | `[1 .1]` (Array), `[3 .1]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 4 | `"ceil(X/2)"` (Enum), `str` (Enum), `-4` (Number), `3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `effects` | Object | Applies a list of status effects or visual effects to targets. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | |

### Object: `Conditional_Ally`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 10 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 6 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| [`Cleanse`](#object-cleanse) | Integer / Object | The number of stacks of negative status effects removed from the target. | 6 | `1` (Number), `0` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer | The amount of health restored to the source. | 4 | `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 4 | `"ceil(X/2)"` (Enum), `"ceil(X/3)"` (Enum), `10` (Number), `3` (Number) |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 4 | `[1 .5]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `TempSpeedUp` | Enum / Integer | The number of stacks of temporary Speed Up applied to the unit. | 4 | `[1 .5]` (Array), `10` (Number), `4` (Number), `{ ... }` (Object) |
| `BleedThorns` | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 2 | `[1 .5]` (Array), `6` (Number), `3` (Number), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 2 | `[1 .1+.02*cha]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `ManaGain` | Enum / Integer | The amount of mana restored to the source, which can be an expression. | 2 | `X-1` (Enum), `X+2` (Enum), `15` (Number), `10` (Number), `"max((X-1)*2, 0)"` (String), `"max(X*3, 0)"` (String) |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | `[1 .5]` (Array), `-2` (Number), `6` (Number), `{ ... }` (Object) |
| `TempDamageUp` | Integer | The amount of temporary damage increase applied. | 2 | `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 2 | `[1 .5]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |
| `effects` | Object | Applies a list of status effects or visual effects to targets. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | |

### Object: `Conditional_BadRoll`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Number | The probability of the effect occurring, expressed as a decimal or percentage. | 16 | `0.5` (Number), `.16666666` (String), `.1` (String) |
| `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 2 | `[25 .01]` (Array), `25` (Number), `50` (Number) |
| [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 2 | `[1 .1]` (Array), `[1 .5]` (Array), `999` (Number), `3` (Number), `{ ... }` (Object) |
| `effects` | Object | Applies a list of status effects or visual effects to targets. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | |

### Object: `Conditional_Boss`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Stun` | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 6 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 4 | `[1 .5]` (Array), `-1` (Number), `3` (Number), `{ ... }` (Object) |
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 4 | `"ceil(X/2)"` (Enum), `str` (Enum), `25` (Number), `-4` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Charmed` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 4 | `[1 .1+.02*cha]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `Drowsy` | Integer | The amount of drowsy stacks applied, or an [stacks, probability] array. | 4 | `[1 .5]` (Array), `8` (Number), `1` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 2 | `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `effects` | Object | Applies a list of status effects or visual effects to targets. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | |

### Object: `Conditional_Corpse`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Revive`](#object-revive) | Integer / Object | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 13 | `50` (Number), `100` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 4 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 4 | `[1 .1+.02*cha]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `SafeDoomed` | Enum / Integer | The number of SafeDoomed stacks applied, or 'level' to scale with character level. | 4 | `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| `HealRandomInjury` | Integer | The number of random injuries healed on the target. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `RandomMutation` | Integer | The number of random mutations to apply. | 2 | `3` (Number), `1` (Number) |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | `[1 .5]` (Array), `-2` (Number), `6` (Number), `{ ... }` (Object) |
| [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 1 | `[1 .1]` (Array), `[1 .5]` (Array), `999` (Number), `3` (Number), `{ ... }` (Object) |
| `effects` | Object | Applies a list of status effects or visual effects to targets. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | |

### Object: `Conditional_Enemy`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 16 | `[2 .15]` (Array), `[1 .1]` (Array), `4` (Number), `2` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 4 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `Attraction` | Integer | The number of stacks of Attraction applied, drawing enemy units toward the target. | 4 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 4 | `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 4 | `[1 .1]` (Array), `[1 .5]` (Array), `999` (Number), `3` (Number), `{ ... }` (Object) |
| [`Weakness`](Passives_and_Statuses.md#object-weakness) | Array / Integer / Object | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 2 | `"ceil(X/2)"` (Enum), `str` (Enum), `-4` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Burn` | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 2 | `[1 .1]` (Array), `[1 .25]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 2 | `[1 .1+.02*cha]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `Doomed` | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. | 2 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `Hex` | Integer | The number of stacks of Hex applied, causing the target to take increased damage from spells. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`Leeches`](#object-leeches) | Integer / Object | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 2 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| [`Marked`](#object-marked) | Array / Integer / Object | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 2 | `[1 .1]` (Array), `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Poison` | Array / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 2 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |
| `TempDamageUp` | Integer | The amount of temporary damage increase applied. | 2 | `[1 .5]` (Array), `1` (Number), `-1` (Number), `{ ... }` (Object) |
| `Stun` | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `effects` | Object | Applies a list of status effects or visual effects to targets. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | |

### Object: `Conditional_FirstApplicationThisTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `Charge` | Integer | The number of charge stacks applied. | 2 | `[1 .5]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| `FillMana` | Integer | The amount of mana restored, or an [amount, probability] array. | 2 | `[1 .25]` (Array), `[1 .10]` (Array), `1` (Number) |
| `ManaGain` | Enum / Integer | The amount of mana restored to the source, which can be an expression. | 2 | `X-1` (Enum), `X+2` (Enum), `15` (Number), `10` (Number), `"max((X-1)*2, 0)"` (String), `"max(X*3, 0)"` (String) |
| `effects` | Object | Applies a list of status effects or visual effects to targets. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | |

### Object: `Conditional_GoodRoll`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Number | The probability of the effect occurring, expressed as a decimal or percentage. | 72 | `15` (Number), `50` (Number), `.5` (String) |
| `Freeze` | Array / Integer | The amount of freeze stacks applied, or an [stacks, probability] array. | 12 | `[1 .1]` (Array), `[1 0.15]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Specifies the loot pool from which to find an item, with an optional chance. | 10 | `parasites` (Enum), `chapter_specific_item` (Enum), `{ ... }` (Object) |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. | 6 | `cm_RaptorEggSpawn` (Enum), `tk_WeirdEgg_Spawn` (Enum), `{ ... }` (Object) |
| `RandomMutation` | Integer | The number of random mutations to apply. | 6 | `3` (Number), `1` (Number) |
| `ChangeTilesUnder` | Enum | The tile type to change the ground tiles under the target to. | 2 | `LavaTile` (Enum), `DirtTile` (Enum) |
| [`ImmediateUseAbility`](#object-immediateuseability) | Enum / Object | Specifies the name of an ability to be triggered instantly from this effect. | 2 | `cm_Lard_Impl` (Enum), `tk_ButterBean_Mega` (Enum), `{ ... }` (Object) |
| `effects` | Object | Applies a list of status effects or visual effects to targets. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | |

### Object: `Conditional_HasCleansableDebuffs`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GenericBuff` | Integer | A generic buff value applied to the unit. | 2 | `100` (Number), `5` (Number) |
| `PartialCleanse` | Integer | The number of stacks of temporary status effects to remove from the target. | 2 | `1` (Number), `9999` (Number) |
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | A collection of status effects; one is randomly chosen and applied to the target. | 2 | `{ ... }` (Object) |
| `VisualFX` | Enum | Specifies the name of the visual effect to play. | 2 | `MagicMissleBlast` (Enum), `BigMagicMissileBlast` (Enum) |
| `effects` | Object | Applies a list of status effects or visual effects to targets. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | |

### Object: `Conditional_HasStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 12 | `"ceil(X/2)"` (Enum), `str` (Enum), `20` (Number), `10` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Burn` | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 4 | `[2 .15]` (Array), `[1 .1]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| [`Slow`](Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `-1` (Number), `3` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 2 | `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| [`FormChange`](Abilities_and_Spells.md#object-formchange) | Enum / Object | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 2 | `passive` (Enum), `Bully` (Enum), `{ ... }` (Object) |
| `Quivered` | Array / Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 2 | `[1 0.1]` (Array), `[1 .5]` (Array), `1` (Number), `5` (Number), `{ ... }` (Object) |
| `effects` | Object | Applies a list of status effects or visual effects to targets. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | |

### Object: `Conditional_HasTag`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ImmediateUseAbility`](#object-immediateuseability) | Enum / Object | Specifies the name of an ability to be triggered instantly from this effect. | 6 | `HitlerCloneTransform` (Enum), `head_ThrobbingCrown` (Enum), `{ ... }` (Object) |
| `ChangeTilesUnder` | Enum | The tile type to change the ground tiles under the target to. | 4 | `LavaTile` (Enum), `DirtTile` (Enum) |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 4 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| [`Die`](Characters_and_Bosses.md#object-die) | Integer / Object | If set, kills the target immediately. | 4 | `6` (Number), `1` (Number), `{ ... }` (Object) |
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 2 | `"ceil(X/2)"` (Enum), `str` (Enum), `10` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Charmed` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 2 | `[1 .1+.02*cha]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `EventBounty` | Integer | The number of stacks of Event Bounty applied, increasing event rewards. | 2 | `[1 .5]` (Array), `1` (Number), `5` (Number), `{ ... }` (Object) |
| `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 2 | `[25 .01]` (Array), `25` (Number), `50` (Number) |
| [`PopAndSpawn`](Abilities_and_Spells.md#object-popandspawn) | Enum / Object | The object (enemy or entity) to spawn on the target's tile, optionally with visual effects. | 2 | `TheDestroyer` (Enum), `StemCat_HalfHealth` (Enum), `{ ... }` (Object) |
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object | The name of the ability the target is forced to use. | 2 | `GirlDinoPoop` (Enum), `TormentorRuneAbsorb` (Enum), `{ ... }` (Object) |
| `effects` | Object | Applies a list of status effects or visual effects to targets. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | |

### Object: `Conditional_HealthThreshold`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 2 | `"ceil(X/2)"` (Enum), `str` (Enum), `-4` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| [`Die`](Characters_and_Bosses.md#object-die) | Integer / Object | If set, kills the target immediately. | 2 | `6` (Number), `1` (Number), `{ ... }` (Object) |
| `FlatLeech` | Integer | The flat amount of health restored to the source when dealing damage, applied after the hit. | 2 | `X` (Enum), `10` (Number), `1` (Number) |
| `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 2 | `[25 .01]` (Array), `25` (Number), `50` (Number) |
| `effects` | Object | Applies a list of status effects or visual effects to targets. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | |

### Object: `Conditional_ManaThreshold`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RepairTrinket` | Integer | The number of stacks of the Repair Trinket status effect to apply. | 2 | `1` (Number), `99` (Number) |
| `effects` | Object | Applies a list of status effects or visual effects to targets. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | |

### Object: `Conditional_NotBoss`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Doomed` | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. | 4 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `effects` | Object | Applies a list of status effects or visual effects to targets. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | |

### Object: `Conditional_PartyMember`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Charmed` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 4 | `[1 .1+.02*cha]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `effects` | Object | Applies a list of status effects or visual effects to targets. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | |

### Object: `Conditional_Shielded`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cleave`](Abilities_and_Spells.md#object-cleave) | Integer / Object | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. | 4 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 2 | `"ceil(X/2)"` (Enum), `str` (Enum), `-4` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| [`SetItemAux`](#object-setitemaux) | Object | Configures an item's auxiliary value by specifying a target slot and a formula for the new value. | 2 | `{ ... }` (Object) |
| `Stun` | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `effects` | Object | Applies a list of status effects or visual effects to targets. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | |

### Object: `ConstitutionUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_CONUP_NAME"` (String) |
| `name_stacks_neg` | String | Localization key for the name of the negative variant (e.g., stat down) of this status effect. || `"KEYWORD_CONDOWN_NAME"` (String) |
| `tooltip_stackless` | Enum | A localization key for the tooltip description of this status effect when it has no stack count. || `none` (Enum) |
| `tooltip_stacks_neg` | String | Localization key for the tooltip description of the negative variant (e.g., stat down) of this status effect. || `"KEYWORD_CONDOWN_DESC"` (String) |
| `tooltip_stacks_pos` | String | Localization key for the tooltip description of the positive variant (e.g., stat up) of this status effect. || `"KEYWORD_CONUP_DESC"` (String) |

### Object: `Craft`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pool` | Array / Enum | Specifies the name of the pool from which an ability is learned or an item is crafted. | 30 | `pelts` (Enum), `eyes_nonrare` (Enum) |
| `slot` | Enum / Integer | Specifies the equipment slot (e.g., 'head', 'trinket', 'random_empty') where the crafted item is placed. | 28 | `weapon` (Enum), `trinket` (Enum) |
| `temporary` | Boolean | If true, the crafted item is temporary and will be removed after the battle or a set duration. | 8 | `false` (Boolean) |
| `works_with_tech` | Boolean | If true, the craft effect is compatible with tech-based interactions or abilities. | 8 | `true` (Boolean) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `self_buff` (Enum) |

### Object: `CureDisease`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 12 | `30` (Number), `15` (Number) |
| `disease` | Enum | Determines which disease is applied when spreading disease. | 12 | `Pox` (Enum), `Covid` (Enum) |
| `can_apply_to_anything` | Boolean | If true, this disease can be spread to any unit, regardless of type. | 2 | `true` (Boolean) |

### Object: `DelayedPain`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_DELAYEDPAIN_NAME"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_DELAYEDPAIN_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_DELAYEDPAIN_DESC"` (String) |

### Object: `DestroyEquipmentAndAttachParasite`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 8 | `1` (Number), `.75` (String), `.15` (String) |
| `pool` | Array / Enum | Specifies the name of the pool from which an ability is learned or an item is crafted. | 4 | `[AmoebaHat AmoebaNeck AmoebaFace]` (Array), `[FlyHat FlyMask FlyNeck]` (Array), `parasites` (Enum) |

### Object: `DexterityUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_DEXUP_NAME"` (String) |
| `name_stacks_neg` | String | Localization key for the name of the negative variant (e.g., stat down) of this status effect. || `"KEYWORD_DEXDOWN_NAME"` (String) |
| `tooltip_stackless` | Enum | A localization key for the tooltip description of this status effect when it has no stack count. || `none` (Enum) |
| `tooltip_stacks_neg` | String | Localization key for the tooltip description of the negative variant (e.g., stat down) of this status effect. || `"KEYWORD_DEXDOWN_DESC"` (String) |
| `tooltip_stacks_pos` | String | Localization key for the tooltip description of the positive variant (e.g., stat up) of this status effect. || `"KEYWORD_DEXUP_DESC"` (String) |

### Object: `DiminishingHealthRegen`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_DIMINISHREGEN_NAME"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_DIMINISHREGEN_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_DIMINISHREGEN_DESC"` (String) |

### Object: `DistanceBonusDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `min_range` | Integer | The minimum range of the ability. | 8 | `3` (Number), `1` (Number) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 8 | `1` (Number) |

### Object: `DoDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Equation | Specifies the amount of damage dealt, can be a number or expression. | 14 | `8` (Equation), `5` (Equation) |
| `type` | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 14 | `melee` (Enum), `generic_physical` (Enum) |
| `damage_tiles` | Enum | Specifies whether the damage effect applies to tiles; 'all' damages every tile in the area. | 8 | `all` (Enum) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 8 | `{ ... }` (Object) |
| `elements` | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. || `[Fire]` (Array), `[Water]` (Array) |

### Object: `DoubleCastSpellThisTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_DOUBLECASTTHISTURN_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_DOUBLECASTTHISTURN_DESC"` (String) |

### Object: `Drowsy`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_DROWSY_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_DROWSY_DESC"` (String) |

### Object: `Else`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 12 | `"ceil(X/2)"` (Enum), `str` (Enum), `-4` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| [`Cleanse`](#object-cleanse) | Integer / Object | The number of stacks of negative status effects removed from the target. | 4 | `1` (Number), `0` (Number), `{ ... }` (Object) |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 4 | `[2 .15]` (Array), `[1 .1]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| [`FormChange`](Abilities_and_Spells.md#object-formchange) | Enum / Object | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 4 | `passive` (Enum), `Nuke` (Enum), `{ ... }` (Object) |
| [`GainCoinsRange`](Abilities_and_Spells.md#object-gaincoinsrange) | Object | An object with `min` and `max` fields specifying a range for the amount of coins gained. | 4 | `{ ... }` (Object) |
| [`Marked`](#object-marked) | Array / Integer / Object | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 4 | `[1 .1]` (Array), `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. | 4 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `RandomStatDown` | Array / Integer / String | The amount of random stat reduction applied, either as a fixed number, a formula string, or an array of [stacks, probability]. | 4 | `[1 .25]` (Array), `"ceil(X/2)"` (Enum), `"ceil(X/3)"` (Enum), `1` (Number) |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 4 | `"ceil(X/2)"` (Enum), `"ceil(X/3)"` (Enum), `10` (Number), `3` (Number) |
| [`Revive`](#object-revive) | Integer / Object | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 4 | `50` (Number), `100` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 2 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 2 | `[1 .1+.02*cha]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| [`Cleave`](Abilities_and_Spells.md#object-cleave) | Integer / Object | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 2 | `[1 .5]` (Array), `-1` (Number), `-2` (Number), `{ ... }` (Object) |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 2 | `[1 .5]` (Array), `50` (Number), `20` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 2 | `[1 .5]` (Array), `15` (Number), `66` (Number), `{ ... }` (Object) |
| [`DybbukPossessed`](Abilities_and_Spells.md#object-dybbukpossessed) | Object | Contains parameters for the Dybbuk possession status, specifying exit ability and self-punch ability. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 2 | `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| [`ImmediateUseAbility`](#object-immediateuseability) | Enum / Object | Specifies the name of an ability to be triggered instantly from this effect. | 2 | `cm_Lard_Impl` (Enum), `tk_ButterBean_Mega` (Enum), `{ ... }` (Object) |
| `Immobile` | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 2 | `[1 .1]` (Array), `[1 .25]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 2 | `[25 .01]` (Array), `25` (Number), `50` (Number) |
| [`Leeches`](#object-leeches) | Integer / Object | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 2 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 2 | `Maggot` (Enum), `BeefyCharmedLeech` (Enum), `{ ... }` (Object) |
| `PartialCleanse` | Integer | The number of stacks of temporary status effects to remove from the target. | 2 | `1` (Number), `9999` (Number) |
| [`ScatterCoins`](Abilities_and_Spells.md#object-scattercoins) | Object | The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula. | 2 | `[1 .5]` (Array), `5` (Number), `{ ... }` (Object) |
| [`Slow`](Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 2 | `[1 .1]` (Array), `[1 .25]` (Array), `-1` (Number), `3` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | `[1 .5]` (Array), `-2` (Number), `6` (Number), `{ ... }` (Object) |
| `TempSpeedUp` | Enum / Integer | The number of stacks of temporary Speed Up applied to the unit. | 2 | `[1 .5]` (Array), `10` (Number), `4` (Number), `{ ... }` (Object) |
| `Webbed` | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. | 2 | `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`AllyInfested`](Engine_LogicKeys.md#object-allyinfested) | Array / Number / Object | Defines the AllyInfested object, which spawns an infested ally under the player's control. | 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Poison` | Array / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .5]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |

### Object: `Fear`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_FEAR_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_FEAR_DESC"` (String) |

### Object: `ForceAttack`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `immediate` | Boolean | If true, the action (e.g., attack) occurs instantly without waiting for the unit's turn in the initiative order. | 4 | `true` (Boolean) |

### Object: `ForceUseAbilityOnTarget`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `head_MiniMoonArmorAsteroid` (Enum) |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | `25` (Number) |

### Object: `FormChange`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `form` | Enum / Integer | Specifies the name of the form the unit changes into. | 150 | `Rage` (Enum), `"Default"` (Enum), `4` (Number), `1` (Number) |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | `30` (Number) |

### Object: `Freeze`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_FREEZE_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_FREEZE_DESC"` (String) |

### Object: `GainCoinsRange`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer | The maximum amount of coins that can be gained. | 22 | `30` (Number), `3` (Number) |
| `min` | Integer | The minimum amount of coins that will be gained. | 22 | `30` (Number), `15` (Number) |

### Object: `GainDisorderFromPool`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | `.1` (String) |
| `pool` | Array / Enum | Specifies the name of the pool from which an ability is learned or an item is crafted. | 2 | `diseases` (Enum) |

### Object: `Hex`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_HEX_NAME"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_HEX_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_HEX_DESC"` (String) |

### Object: `ImmediateUseAbility`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `wp_NuclearKnifeExplode` (Enum) |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 2 | `true` (Boolean) |

### Object: `IncAuxCounterClamped`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `change` | Integer | The amount to adjust the auxiliary counter by. | 6 | `-2` (Number), `-3` (Number) |
| `max` | Integer | The maximum amount of coins that can be gained. | 6 | `3` (Number) |

### Object: `Infested`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. || `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. || `{ ... }` (Object) |
| `class` | Enum | Specifies the class that this ability belongs to, used for categorization and restrictions. || `Colorless` (Enum) |
| `default_frame` | Number | The default sprite frame used for the character's portrait or body. || `1002` (Number) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"PASSIVE_INFESTED_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| `icon_frame` | Number | The sprite frame index for the buff icon. || `517` (Number) |
| `lefteye` | Number | The sprite frame index for the character's left eye. || `1040` (Number) |
| `lefteyebrow` | Number | The sprite frame index for the character's left eyebrow. || `1022` (Number) |
| `mouth` | Number | The catalog ID for the cat's mouth part. || `1041` (Number) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"PASSIVE_INFESTED_NAME"` (String), `"KEYWORD_INFESTED_NAME"` (String) |
| `palette` | Enum / Integer | Specifies the color palette index for the ability's visuals. || `50` (Number) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `pitch` | String | The sound pitch multiplier for the character's voice or sounds. || `.7` (String) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |
| `righteye` | Number | The sprite frame index for the character's right eye. || `1041` (Number) |
| `righteyebrow` | Number | The sprite frame index for the character's right eyebrow. || `1022` (Number) |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). || `{ ... }` (Object) |
| `texture` | Integer | The catalog ID for the cat's texture. || `1000` (Number) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_INFESTED_DESC"` (String) |
| `value` | Enum | The numeric value or formula associated with the buff. || `1` (Number) |
| `voice` | Enum | Determines which voice set or type is used for the character. || `female2` (Enum) |

### Object: `IntelligenceUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_INTUP_NAME"` (String) |
| `name_stacks_neg` | String | Localization key for the name of the negative variant (e.g., stat down) of this status effect. || `"KEYWORD_INTDOWN_NAME"` (String) |
| `tooltip_stackless` | Enum | A localization key for the tooltip description of this status effect when it has no stack count. || `none` (Enum) |
| `tooltip_stacks_neg` | String | Localization key for the tooltip description of the negative variant (e.g., stat down) of this status effect. || `"KEYWORD_INTDOWN_DESC"` (String) |
| `tooltip_stacks_pos` | String | Localization key for the tooltip description of the positive variant (e.g., stat up) of this status effect. || `"KEYWORD_INTUP_DESC"` (String) |

### Object: `KnockOutCoin`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | `.5` (String) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `1` (Number) |

### Object: `KnockUpAndAway`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 48 | `3` (Number), `-3` (Number) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 44 | `5+bonus_melee_ability_damage` (Enum), `3` (Number), `1` (Number) |
| `displace` | Boolean | If true, the knockback also displaces the target to a different tile. | 4 | `true` (Boolean) |
| `height` | Integer | The height in tiles the target is launched into the air. | 4 | `0` (Number), `2` (Number) |
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Boolean / Integer / Object | Defines damage or effects applied to the caster when using the ability. | 4 | `false` (Boolean) |
| `circular_variance` | Integer | The random variance in the knockback direction, in tiles. | 2 | `2` (Number) |

### Object: `Knockback`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"Knockback"` (Enum) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `None` (Enum) |

### Object: `KnockbackIfCrit`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `knockback` | Enum / Integer | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 2 | `10` (Number) |
| `override_chain_knockback` | Integer | The distance in tiles the unit is knocked back if a critical hit triggers chain knockback. | 2 | `10` (Number) |

### Object: `Leech`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"SETBONUS_LEECH_DESC"` (String) |
| `icon_frame` | Number | The sprite frame index for the buff icon. || `17` (Number) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"SETBONUS_LEECH_NAME"` (String), `"KEYWORD_LIFESTEAL_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` (Number) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_LIFESTEAL2_DESC"` (String) |

### Object: `Leeches`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_LEECHES_NAME"` (String) |
| `name_reference_applier` | String | A localization key for the name displayed to the applier of this status effect. || `"KEYWORD_LEECHES_NAME_APPLIER"` (String) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `lobbed_attack` (Enum) |
| `tooltip_reference_applier` | String | A localization key for the tooltip description displayed to the applier of this status effect. || `"KEYWORD_LEECHES_DESC_APPLIER"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_LEECHES_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_LEECHES_DESC"` (String) |

### Object: `MagicWeakness`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_MAGICWEAKNESS_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_MAGICWEAKNESS_DESC"` (String) |

### Object: `ManaGainRange`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer | The maximum amount of coins that can be gained. | 2 | `4` (Number) |
| `min` | Integer | The minimum amount of coins that will be gained. | 2 | `0` (Number) |

### Object: `ManaLeeches`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_MANALEECHES_NAME"` (String) |
| `name_reference_applier` | String | A localization key for the name displayed to the applier of this status effect. || `"KEYWORD_MANALEECHES_NAME_APPLIER"` (String) |
| `tooltip_reference_applier` | String | A localization key for the tooltip description displayed to the applier of this status effect. || `"KEYWORD_MANALEECHES_DESC_APPLIER"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_MANALEECHES_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_MANALEECHES_DESC"` (String) |

### Object: `Marked`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_MARKED_NAME"` (String) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `targeted_status` (Enum) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_MARKED_DESC"` (String) |

### Object: `ModifyAbility`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 4 | `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 4 | `{ ... }` (Object) |

### Object: `MovementUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_MOVEMENTUP_NAME"` (String) |
| `name_stacks_neg` | String | Localization key for the name of the negative variant (e.g., stat down) of this status effect. || `"KEYWORD_MOVEMENTDOWN_NAME"` (String) |
| `tooltip_stackless_neg` | String | Localization key for the tooltip of the negative variant when not showing stack count. || `"KEYWORD_MOVEMENTDOWN_DESC_STACKLESS"` (String) |
| `tooltip_stackless_pos` | String | Localization key for the tooltip of the positive variant when not showing stack count. || `"KEYWORD_MOVEMENTUP_DESC_STACKLESS"` (String) |
| `tooltip_stacks_neg` | String | Localization key for the tooltip description of the negative variant (e.g., stat down) of this status effect. || `"KEYWORD_MOVEMENTDOWN_DESC"` (String) |
| `tooltip_stacks_pos` | String | Localization key for the tooltip description of the positive variant (e.g., stat up) of this status effect. || `"KEYWORD_MOVEMENTUP_DESC"` (String) |

### Object: `NextBattleStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 4 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `FullHeal` | Integer | If non-zero, fully restores the target's health. | 4 | `1` (Number), `0` (Number) |

### Object: `NoHealthRegen`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_NOHEALTHREGEN_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_NOHEALTHREGEN_DESC"` (String) |

### Object: `NukeQuestFinalBossModifications`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Boolean / Integer / Object | Defines damage or effects applied to the caster when using the ability. | 4 | `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 2 | `{ ... }` (Object) |
| [`splash_damage`](Abilities_and_Spells.md#object-splash_damage) | Object | Defines additional damage or effects applied to nearby targets around the primary target. | 2 | `{ ... }` (Object) |

### Object: `ObjectOnHitCharacter`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum | Specifies the object or unit to be spawned. | 14 | `CharmedLeech` (Enum), `CharmedTinySpider` (Enum) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 10 | `"floor(lck/4)"` (Enum), `1` (Number), `2` (Number) |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 4 | `1` (Number), `.5` (String) |

### Object: `OneUseSpellDamageUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum | Specifies the reference name of another status effect to alias or copy properties from. || `SpellDamageUp` (Enum) |

### Object: `Ostracized`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_OSTRACIZED_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_OSTRACIZED_DESC"` (String) |

### Object: `PassiveWhileNotTakingTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | Contains status effects to add to the basic attack. | 2 | `{ ... }` (Object) |

### Object: `PermanentConfusion`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_CONFUSION_NAME"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_CONFUSION_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_CONFUSION_DESC_STACKLESS"` (String) |

### Object: `Petrify`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_PETRIFY_NAME"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_PETRIFY_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_PETRIFY_DESC"` (String) |
| `tooltip_stacks_singular` | String ||| `KEYWORD_PETRIFY_DESC_SINGULAR` (String) |

### Object: `PoisonLace`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_POISONLACE_NAME"` (String) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `targeted_status` (Enum) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_POISONLACE_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_POISONLACE_DESC"` (String) |

### Object: `Possessed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_POSSESED_NAME"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_POSSESSED_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_POSSESSED_DESC"` (String) |
| `tooltip_stacks_singular` | String ||| `KEYWORD_POSSESSED_DESC_SIGNULAR` (String) |

### Object: `PreEmptiveCounterNextAttacks`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_PREEMTIVECOUNTER_NAME"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_PREEMTIVECOUNTER_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_PREEMTIVECOUNTER_DESC"` (String) |
| `tooltip_stacks_singular` | String ||| `"KEYWORD_PREEMTIVECOUNTER_DESC_STACKLESS"` (String) |

### Object: `ProbeCharmed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_PROBED_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_PROBED_DESC"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_PROBED_DESC_STACKLESS"` (String) |

### Object: `Purge`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `spell` (Enum) |

### Object: `RandomInjury`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number | The sprite frame index for the buff icon. || `58` (Number) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_RANDOMINJURY_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_RANDOMINJURY_DESC"` (String) |

### Object: `RandomMagicMissile`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `full_size` | Boolean || 4 | `true` (Boolean) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `3` (Number), `4` (Number) |
| `icon_frame` | Number | The sprite frame index for the buff icon. || `154` (Number) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_SPARKLE_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_SPARKLE_DESC"` (String) |

### Object: `RandomPermanentStatsDistinct`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). || `[1 -1]` (Array) |

### Object: `RangeUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_RANGEUP_NAME"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_RANGEUP_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_RANGEUP_DESC"` (String) |

### Object: `Reanimate`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `targeted_status` (Enum) |

### Object: `Reflect`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_REFLECT_NAME"` (String) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `self_buff` (Enum) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_REFLECT_DESC"` (String) |
| `tooltip_stacks_singular` | String ||| `"KEYWORD_REFLECT_DESC_STACKLESS"` (String) |

### Object: `RemoveStatusStacks`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 8 | `10` (Number), `1` (Number) |
| `status` | Enum || 8 | `Thorns` (Enum), `DodgeChance_Status` (Enum) |

### Object: `ReplaceSpell`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 8 | `MoonHeadCommandStopHittingYourself` (Enum), `None` (Enum) |
| `slot` | Enum / Integer | Specifies the equipment slot (e.g., 'head', 'trinket', 'random_empty') where the crafted item is placed. | 8 | `3` (Number), `1` (Number) |

### Object: `Revive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `melee_spell` (Enum) |

### Object: `ReviveNextRound`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `revive_health` | Integer || 8 | `100` (Number), `1` (Number) |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 6 | `[1 .5]` (Array), `15` (Number), `5` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 4 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `2` (Number) |
| `DivineShield` | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 2 | `[1 .5]` (Array), `[1 .33]` (Array), `4` (Number), `1` (Number), `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_AUTOREVIVE_NAME"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `KEYWORD_AUTOREVIVE_DESC` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AUTOREVIVE_DESC"` (String) |
| `tooltip_stacks_singular` | String ||| `"KEYWORD_AUTOREVIVE_DESC_SINGULAR"` (String) |

### Object: `Rot`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_ROT_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_ROT_DESC"` (String) |

### Object: `ScatterCoins`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stackable` | Boolean || 4 | `true` (Boolean) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `item_aux` (Enum), `"max(min(X+1, item_aux), 0)"` (String) |

### Object: `Scrambled`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_SCRAMBLED_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_SCRAMBLED_DESC"` (String) |

### Object: `SetItemAux`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `slot` | Enum / Integer | Specifies the equipment slot (e.g., 'head', 'trinket', 'random_empty') where the crafted item is placed. | 6 | `face` (Enum), `head` (Enum) |
| `value` | Enum | The numeric value or formula associated with the buff. | 6 | `item_aux+1` (Enum), `item_aux+2` (Enum) |

### Object: `Shield`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_SHIELD_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `None` (Enum) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_SHIELD_DESC_STACKLESS"` (String) |

### Object: `Sleep`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_SLEEP_NAME"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_SLEEP_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_SLEEP_DESC"` (String) |

### Object: `SoulLink`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_SOULLINK_NAME"` (String) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `targeted_status` (Enum) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_SOULLINK_DESC"` (String) |

### Object: `SpeedUp_WithoutInitiative`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum | Specifies the reference name of another status effect to alias or copy properties from. || `SpeedUp` (Enum) |

### Object: `SpiderInfested`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_SPIDERINFESTED_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_SPIDERINFESTED_DESC"` (String) |

### Object: `SpreadDisease`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `disease` | Enum | Determines which disease is applied when spreading disease. | 26 | `Pox` (Enum), `Toxoplasmosis` (Enum) |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 24 | `30` (Number), `50` (Number) |
| `can_apply_to_anything` | Boolean | If true, this disease can be spread to any unit, regardless of type. | 12 | `true` (Boolean) |

### Object: `StacyMutant_Brace`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 2 | `[1 .5]` (Array), `4` (Number), `10` (Number), `{ ... }` (Object) |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 2 | `{ ... }` (Object) |

### Object: `StacyMutant_Counter`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | Contains status effects to add to the basic attack. | 2 | `{ ... }` (Object) |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 2 | `{ ... }` (Object) |
| [`CounterAttack`](Cat_Mutations.md#object-counterattack) | Array / Enum / Object | Specifies the ability used when the unit counterattacks after being hit. | 2 | `[attack GSScream]` (Array), `CollectiveCounter` (Enum), `YeticatSnowball_Counter` (Enum), `{ ... }` (Object) |

### Object: `StacyMutant_Damage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddDamage` | Integer | The amount of damage added to all attacks. Negative values reduce damage. | 2 | `-1` (Number), `4` (Number) |
| `AddMaxHealth` | Integer | The amount added to the unit's maximum health. Negative values reduce max health. | 2 | `25` (Number), `-25` (Number) |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 2 | `{ ... }` (Object) |

### Object: `StacyMutant_DoubleHead`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 2 | `{ ... }` (Object) |
| `ExtraDispersedTurns` | Integer | The number of additional or fewer turns in the dispersed turn order. | 2 | `1` (Number), `-1` (Number) |

### Object: `StacyMutant_Fire`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 2 | `{ ... }` (Object) |
| `ElementImmune` | Enum | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 2 | `Fire` (Enum), `Creep` (Enum) |
| `ReplaceBasicAttack` | Enum | Specifies the ability ID that replaces the unit's basic attack. | 2 | `BasicButcherMeleeWideSpin` (Enum), `BasicDruidAbilityVersatile` (Enum) |
| [`ReplaceBrain`](Characters_and_Bosses.md#object-replacebrain) | Object | Defines a replacement AI brain and behavior pattern for the mutant. | 2 | `{ ... }` (Object) |

### Object: `StacyMutant_Health`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddMaxHealth` | Integer | The amount added to the unit's maximum health. Negative values reduce max health. | 2 | `25` (Number), `10` (Number) |
| `AddSpeed` | Integer | The amount of speed added (or subtracted) to the unit. | 2 | `4` (Number), `-3` (Number) |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 2 | `{ ... }` (Object) |
| `SizeScale` | Number | The multiplier applied to the unit's visual and hitbox size. | 2 | `1.2` (Number), `1.65` (Number), `.6` (String), `.8` (String) |

### Object: `StacyMutant_Holy`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 2 | `{ ... }` (Object) |
| `DivineShield` | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 2 | `[1 .5]` (Array), `[1 .33]` (Array), `4` (Number), `1` (Number), `{ ... }` (Object) |

### Object: `StacyMutant_Ice`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddMovement` | Integer | The amount of bonus movement points added to the unit's base movement. | 2 | `-1` (Number), `3` (Number) |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 2 | `{ ... }` (Object) |
| `ElementImmune` | Enum | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 2 | `Fire` (Enum), `Creep` (Enum) |
| `ReplaceBasicAttack` | Enum | Specifies the ability ID that replaces the unit's basic attack. | 2 | `BasicButcherMeleeWideSpin` (Enum), `BasicDruidAbilityVersatile` (Enum) |
| [`ReplaceBrain`](Characters_and_Bosses.md#object-replacebrain) | Object | Defines a replacement AI brain and behavior pattern for the mutant. | 2 | `{ ... }` (Object) |

### Object: `StacyMutant_Lightning`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 2 | `{ ... }` (Object) |
| `ElementImmune` | Enum | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 2 | `Fire` (Enum), `Creep` (Enum) |
| `ReplaceBasicAttack` | Enum | Specifies the ability ID that replaces the unit's basic attack. | 2 | `SM_LightningDash` (Enum), `BasicButcherMeleeWideSpin` (Enum) |
| [`ReplaceBrain`](Characters_and_Bosses.md#object-replacebrain) | Object | Defines a replacement AI brain and behavior pattern for the mutant. | 2 | `{ ... }` (Object) |

### Object: `StacyMutant_Mirror`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 2 | `{ ... }` (Object) |
| [`ReflectProjectiles`](Characters_and_Bosses.md#object-reflectprojectiles) | Integer / Object | The percentage chance to reflect projectiles back at the attacker; optionally includes self-damage. | 2 | `25` (Number), `20` (Number), `{ ... }` (Object) |
| [`StatusEachTurnEndForEachTurn`](Characters_and_Bosses.md#object-statuseachturnendforeachturn) | Object | Statuses applied at the end of each turn, with the number of turns as nested values. | 2 | `{ ... }` (Object) |

### Object: `StacyMutant_Speed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddDamage` | Integer | The amount of damage added to all attacks. Negative values reduce damage. | 2 | `-1` (Number), `4` (Number) |
| `AddSpeed` | Integer | The amount of speed added (or subtracted) to the unit. | 2 | `6` (Number), `-3` (Number) |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 2 | `{ ... }` (Object) |
| `SizeScale` | Number | The multiplier applied to the unit's visual and hitbox size. | 2 | `1.1` (Number), `1.3` (Number), `.6` (String), `.8` (String) |

### Object: `StacyMutant_Thorns`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 2 | `{ ... }` (Object) |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 2 | `[1 .5]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |

### Object: `StatusAfterXStacks`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stack_key` | Enum || 4 | `EMPTY_GENERATOR` (String), `FANNY_PACK` (String) |
| [`threshold`](Items_and_Equipment.md#object-threshold) | Enum / Integer / Object | The health threshold value, either as a formula using X (max health) or a fixed integer. | 4 | `3` (Number), `12` (Number) |
| `ExtraBasicMoves_Status` | Integer | The number of extra basic moves per turn granted. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `RefreshActPoints` | Integer | The amount of action points restored to the source. | 2 | `1` (Number) |
| `expires_on_end_turn` | Boolean | If true, the temporary effect expires at the end of the target's turn. | 2 | `true` (Boolean) |

### Object: `StealthUntilBasicAttack`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_STEALTHUNTIL_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_STEALTHUNTIL_DESC"` (String) |

### Object: `Stun`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_STUN_NAME"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_STUN_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_STUN_DESC"` (String) |

### Object: `Tangled`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alt_art` | Enum || 2 | `TangledMeat` (Enum) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `1` (Number) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_TANGLED_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_TANGLED_DESC"` (String) |

### Object: `Tarred`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_TARRED_NAME"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_TARRED_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_TARRED_DESC"` (String) |

### Object: `TempCounterAttack`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_TEMPCOUNTER_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_TEMPCOUNTER_DESC"` (String) |

### Object: `TempDamageUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum | Specifies the reference name of another status effect to alias or copy properties from. || `DamageUp` (Enum) |

### Object: `TempMovement`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum | Specifies the reference name of another status effect to alias or copy properties from. || `MovementUp` (Enum) |

### Object: `TempPassiveUntilSettled`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`MeleeRevengeDamage`](Abilities_and_Spells.md#object-meleerevengedamage) | Object | Defines the damage and effects applied back to a melee attacker upon being hit. | 4 | `{ ... }` (Object) |
| `LimitHeal` | Integer | If 1, prevents the unit from being healed. | 2 | `1` (Number), `0` (Number) |

### Object: `TempRangeUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_TEMPRANGE_NAME"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_TEMPRANGE_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_TEMPRANGE_DESC"` (String) |

### Object: `TempSpellDamageUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum | Specifies the reference name of another status effect to alias or copy properties from. || `SpellDamageUp` (Enum) |

### Object: `TempStrengthUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum | Specifies the reference name of another status effect to alias or copy properties from. || `StrengthUp` (Enum) |

### Object: `Temporary`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 114 | `5` (Number), `-2` (Number) |
| `status` | Enum || 112 | `Trample` (Enum), `Brace` (Enum) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 104 | `3` (Number), `1` (Number) |
| `expires_on_begin_turn` | Boolean || 50 | `true` (Boolean) |
| `expires_on_end_turn` | Boolean | If true, the temporary effect expires at the end of the target's turn. | 42 | `true` (Boolean) |
| `data` | Integer | An integer value used for custom data associated with the temporary effect. | 4 | `2` (Number) |
| `expires_on_appliers_turn` | Boolean | If true, the temporary effect expires at the start of the applier's next turn. | 4 | `true` (Boolean) |
| `expires_on_move` | Boolean | If true, the temporary effect expires when the target moves. | 2 | `true` (Boolean) |

### Object: `TransformWeapon`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `from` | Enum || 4 | `Necro_SoulDagger_Charged` (Enum), `Necro_SoulDagger_Uncharged` (Enum) |
| `to` | Enum || 4 | `Necro_SoulDagger_Charged` (Enum), `Necro_SoulDagger_Uncharged` (Enum) |

### Object: `Webbed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_WEBBED_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_WEBBED_DESC"` (String) |

### Object: `Wet`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_WET_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_WET_DESC"` (String) |

### Object: `XIsSpellStormRampAndReset`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `reset_percent` | Integer || 2 | `50` (Number) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `0` (Number) |

#### `ApplyToSourceOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 15

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AlphaCat` | Integer | The number of AlphaCat stacks applied to the source on kill. | 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`Revive`](#object-revive) | Integer / Object | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 2 | `1` (Number), `50` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| [`EvolveAbilityFromPool`](Abilities_and_Spells.md#object-evolveabilityfrompool) | Enum / Object | Specifies the ability pool from which to evolve an ability for the source, optionally upgrading it. || `Hunter` (Enum), `Fighter` (Enum), `{ ... }` (Object) |
| `HealthGain` | Integer | The amount of health restored to the source. || `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `ManaGain` | Enum / Integer | The amount of mana restored to the source, which can be an expression. || `X` (Enum), `item_aux` (Enum), `5` (Number), `2` (Number), `"max(X*3, 0)"` (String), `"max((X-1)*2, 0)"` (String) |
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. || `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `WeaponAuxMultiplier` | Number ||| `.5` (String) |

</details>

---

#### `Consumed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 23

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`struggle_ability`](./Enums.md#enum-struggle_ability) | Enum | Specifies the name of the ability the consumed unit uses to attempt escape. | 17 ||
| `force_contact` | Boolean | If true, the consumed unit is forced into contact with the consumer. | 15 ||
| `instant` | Boolean | If true, the consumption happens immediately without a timer. | 12 ||
| [`mount_mode`](./Enums.md#enum-mount_mode) | Boolean / Enum | Specifies the mounting mode; values include 'auto' or 'true'. | 12 ||
| `do_not_pop_corpse` | Boolean | If true, the consumed unit's corpse is not popped upon consumption. | 11 ||
| [`drop_on_death`](./Enums.md#enum-drop_on_death) | Boolean / Enum | Determines if and how the consumed unit is dropped on death; values include 'true', 'false', or 'deferred'. | 11 ||
| `wet` | Boolean | If true, the consumed unit is considered wet (e.g., for elemental interactions). | 8 ||
| `drop_on_self_death` | Boolean | If true, the consumed unit is dropped when the consumer dies. | 3 ||
| [`extra_statuses`](Abilities_and_Spells.md#object-extra_statuses) | Object | An object containing additional status effects (with stack counts) applied to the consumed unit. | 3 ||
| `use_placeholder` | Boolean | If true, renders the ability using a temporary placeholder animation instead of the final art. | 3 ||
| [`drop_body_ability`](./Enums.md#enum-drop_body_ability) | Enum | Specifies the ability used to drop the consumed body. | 1 ||
| `kill_on_consume` | Boolean | If true, the consumed unit is killed immediately upon consumption. | 1 ||

</details>

---

### Object: `AcidRain`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha` | String | The alpha transparency value for the particle system (e.g., '0.03'). || `.5` (String) |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. || `amb_acidrain.ogg` (String) |
| `chain` | Boolean | Specifies the ability to chain into and execute. || `AcidSplash` (Enum) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"WEATHER_ACIDRAIN_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. || `{ ... }` (Object) |
| `emit_amount` | Number | The number of particles emitted per burst. || `1` (Number) |
| `emit_box` | Array | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. || `[0 10 10 10 0 10]` (Array) |
| `emit_direction` | Array | The initial direction vector for emitted particles. || `[0 -1 0]` (Array) |
| `emit_rate` | Number | The rate of particle emission per second. || `100` (Number) |
| `emit_spread` | Number | The angle spread for particle emission direction. || `0` (Number) |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. || `true` (Boolean) |
| `force` | Array | The force vector applied to particles. || `[0 -10 0]` (Array) |
| `live_bounds` | Array | The bounds within which particles can exist. || `[-999 999 0 999 -999 999]` (Array) |
| `movieclip` | Array / Enum | Specifies the visual movie clip or sprite asset used for the object. || `AcidRainParticle` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"WEATHER_ACIDRAIN_NAME"` (String) |
| `particle_lifetime` | Number | The duration in seconds particles remain alive. || `5` (Number) |
| `projection_matrix` | Enum | The projection matrix mode for particle rendering (e.g., 'default'). || `default` (Enum) |
| `render_mode` | Enum | The rendering mode for particles (e.g., 'default', 'separate'). || `separate` (Enum) |
| [`scripts`](Miscellaneous.md#object-scripts) | Object | An object containing particle system scripts like forces or collisions. || `{ ... }` (Object) |
| `simulation_space` | Enum | The coordinate space for particle simulation ('local' or 'global'). || `global` (Enum) |
| `size_start` | String | The starting size of particles. || `.5` (String) |
| `speed_scale` | String | A multiplier for particle speed. || `.1` (String) |
| `speed_start` | Number | The initial speed of particles. || `10` (Number) |

### Object: `AddPostProcessEffect`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `requires_framebuffer` | Boolean || 1 | `false` (Boolean) |
| `shader` | Enum || 1 | `shimmervignette` (Enum) |

### Object: `AddTilesetObjects`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`FloatingDebris`](Engine_LogicKeys.md#object-floatingdebris) | Object || 1 | `{ ... }` (Object) |

### Object: `Adrenaline`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_ADRENALINE_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_ADRENALINE_DESC"` (String) |

### Object: `ApplyMultipleTimes`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | A collection of status effects; one is randomly chosen and applied to the target. | 6 | `{ ... }` (Object) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 6 | `X` (Enum), `4` (Number), `8` (Number) |

### Object: `ApplyStatusesNextTurnBegin`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Quivered` | Array / Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 2 | `[1 0.1]` (Array), `[1 .5]` (Array), `1` (Number), `5` (Number), `{ ... }` (Object) |

### Object: `ApplyToConsumed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DeleteObject` | Integer || 6 | `1` (Number) |
| [`Die`](Characters_and_Bosses.md#object-die) | Integer / Object | If set, kills the target immediately. | 2 | `6` (Number), `1` (Number), `{ ... }` (Object) |

### Object: `ApplyToOthersWithSharedTagAndFaction`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Marked`](#object-marked) | Array / Integer / Object | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 2 | `[1 .1]` (Array), `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |

### Object: `ApplyToRandomClosestAlly`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceMoveTowards` | Integer || 2 | `1` (Number) |

### Object: `ApplyToTile`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ObjectOnHit`](Abilities_and_Spells.md#object-objectonhit) | Enum / Object || 4 | `BiggestFood` (Enum), `Bait` (Enum), `{ ... }` (Object) |
| `SpawnBearTrap` | Integer || 4 | `1` (Number) |

### Object: `ArcLightning`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean | If true, the arc lightning effect only chains to enemy units, ignoring allies. | 8 | `false` (Boolean), `true` (Boolean) |
| `max_distance` | Integer || 8 | `3` (Number), `1` (Number) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 8 | `100` (Number) |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | `.5` (String) |
| `ignore_self` | Boolean || 2 | `true` (Boolean) |

### Object: `Bloodzerked`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_BLOODZERK_NAME"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_BLOODZERK_DESC"` (String) |

### Object: `BodyGuard`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `BodyGuardSwap2` (Enum), `BodyGuardSwap` (Enum) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `1` (Number) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_BODYGUARD_NAME"` (String) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `self_buff` (Enum) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_BODYGUARD_DESC"` (String) |

### Object: `BombRatTurtle`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `self_buff` (Enum) |

### Object: `ButterflySwarm`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. || `amb_butterflyswarm.ogg` (String) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"WEATHER_BUTTERFLY_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"WEATHER_BUTTERFLY_NAME"` (String) |

### Object: `CanApplyToInanimate`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 20 | `AllyRotFly` (Enum), `CharmedLeech` (Enum), `{ ... }` (Object) |
| `BreakIntoRocks` | Enum || 8 | `Coin` (Enum), `SmallRock` (Enum) |
| [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 6 | `{ ... }` (Object) |
| `Vaporize` | Integer | Removes the target from play, preventing its corpse from being interacted with. | 6 | `1` (Number), `20` (Number) |
| `GetAggroTarget` | Integer || 4 | `1` (Number) |
| `PreventDeathTransforms` | Integer || 2 | `1` (Number) |
| [`Temporary`](Abilities_and_Spells.md#object-temporary) | Object | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 2 | `{ ... }` (Object) |

### Object: `CastAgainWithStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `OverrideDamage` | Integer || 2 | `25` (Number), `10` (Number) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `1` (Number) |

### Object: `CatPartsSizeScaleStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `arm1` | Number | The catalog ID for the cat's first arm part. | 2 | `1.1` (Number) |
| `arm2` | Number | The catalog ID for the cat's second arm part. | 2 | `1.1` (Number) |
| `body` | Number | The catalog ID for the cat's body part. | 2 | `1.1` (Number) |
| `mouth` | Number | The catalog ID for the cat's mouth part. | 2 | `1.1` (Number) |

### Object: `ChampionUpgradeNextMinion`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_PROMOTE_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_PROMOTE_DESC"` (String) |

### Object: `ChanceToBreakFree`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 22 | `CHuskDrop` (Enum), `LennyDrop` (Enum) |
| `fail_ability` | Enum || 6 | `CHuskDropFail` (Enum), `XXX` (Enum) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 6 | `25` (Number) |

### Object: `ChargeFists`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object | Associates keyword tooltips with the ability, often used for status effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_CHARGEFISTS_NAME"` (String) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `self_buff` (Enum) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_CHARGEFISTS_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_CHARGEFISTS_DESC"` (String) |
| `tooltip_stacks_singular` | String ||| `"KEYWORD_CHARGEFISTS_DESC_SINGULAR"` (String) |

### Object: `CockroachSwarm`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"WEATHER_COCKROACHES_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"WEATHER_COCKROACHES_NAME"` (String) |

### Object: `CollectsPickupsWithAltEffects`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Tech` | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 4 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `CurrentWeaponAddPoison` | Integer || 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 2 | `[1 .5]` (Array), `-4` (Number), `3` (Number), `{ ... }` (Object) |
| `Quivered` | Array / Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 2 | `[1 0.1]` (Array), `[1 .5]` (Array), `1` (Number), `5` (Number), `{ ... }` (Object) |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"` (Enum), `"ceil(X/3)"` (Enum), `10` (Number), `3` (Number) |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 2 | `[1 .5]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |

### Object: `CopySpells`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `1` (Number) |
| `upgraded` | Boolean | If true, the evolved ability is the upgraded version. | 2 | `true` (Boolean) |

### Object: `Counterspell`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `self_buff` (Enum) |

### Object: `CurrentWeaponAddPoison`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_WPOISONLACE_NAME"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_WPOISONLACE_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_WPOISONLACE_DESC"` (String) |

### Object: `DelayCastAbility`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `FetusAirstrike` (Enum) |
| `lingering` | Boolean | If true, the ability effect lingers after the initial cast. | 2 | `true` (Boolean) |
| `relative` | Boolean | If true, the delay is calculated relative to the current turn count rather than as an absolute time. | 2 | `false` (Boolean) |

### Object: `DelayedWind`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 2 | `2` (Number) |

### Object: `DelayedWindCone`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 4 | `10` (Number) |
| `damage` | Equation | Specifies the amount of damage dealt, can be a number or expression. | 2 | `5` (Equation) |

### Object: `DoDistortionRing`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `intensity` | Integer | The strength of the screen shake effect; positive values shake more, negative values may invert direction. | 12 | `-2` (Number), `1` (Number) |
| `radius` | Array / Integer || 12 | `4` (Number), `5` (Number) |
| `speed` | Array / Number | The speed of the projectile or move, can be a value or a range. | 12 | `30` (Number), `-30` (Number) |

### Object: `DoScreenShake`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `intensity` | Integer | The strength of the screen shake effect; positive values shake more, negative values may invert direction. | 20 | `10` (Number), `3` (Number) |
| `time` | Number | The duration in seconds of the screen shake effect. | 20 | `1` (Number), `2` (Number), `.75` (String), `.5` (String) |

### Object: `DoubleCast`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_DOUBLECAST_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_DOUBLECAST_DESC"` (String) |

### Object: `DoubleCastSpell`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_DOUBLECASTSPELL_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_DOUBLECASTSPELL_DESC"` (String) |

### Object: `DoubleLoot`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `self_buff` (Enum) |

### Object: `Drag`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum | Specifies the class that this ability belongs to, used for categorization and restrictions. || `Psychic` (Enum) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"PASSIVE_DRAG_DESC"` (String) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"PASSIVE_DRAG_NAME"` (String) |

### Object: `DustOnHit`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum | Specifies the object or unit to be spawned. | 6 | `GasCloud` (Enum) |

### Object: `EliteUpgradeNextMinion`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_PROMOTE2_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_PROMOTE2_DESC"` (String) |

### Object: `EmptyMind`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_EMPTYMIND_NAME"` (String) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `self_buff` (Enum) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_EMPTYMIND_DESC"` (String) |

### Object: `Enlarge`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Boolean / Integer / Object | Defines damage or effects applied to the caster when using the ability. || `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `spell` (Enum) |

### Object: `FactionUprising`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`extra_statuses`](Abilities_and_Spells.md#object-extra_statuses) | Object || 1 | `{ ... }` (Object) |
| `tag` | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 1 | `bird` (Enum) |

### Object: `FireArmor`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum | Specifies the class that this ability belongs to, used for categorization and restrictions. || `Mage` (Enum) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"PASSIVE_FIREASPECT_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"FireArmor"` (Enum), `"PASSIVE_FIREASPECT_NAME"` (String) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `self_buff` (Enum) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `None` (Enum) |

### Object: `FireArmor2`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"FireArmor2"` (Enum) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `self_buff` (Enum) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `None` (Enum) |

### Object: `FireStorm`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `combo` | Array | A list of particle effect names that are spawned together in sequence. || `[Firestorm_Fire Firestorm_Embers Firestorm_Distortion]` (Array) |

### Object: `FireflySwarm`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"WEATHER_FIREFLY_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"WEATHER_FIREFLY_NAME"` (String) |

### Object: `FlySwarm`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. || `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. || `{ ... }` (Object) |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. || `amb_flyswarm.ogg` (String) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"WEATHER_FLYSWARM_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"WEATHER_FLYSWARM_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. || `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ ... }` (Object) |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). || `{ ... }` (Object) |

### Object: `Fog`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_end` | Number ||| `0` (Number) |
| `alpha_start` | Number ||| `2` (Number) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"WEATHER_FOG_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. || `{ ... }` (Object) |
| `emit_amount` | Number | The number of particles emitted per burst. || `1` (Number) |
| `emit_box` | Array | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. || `[-5 10 0 2 -5 10]` (Array) |
| `emit_direction` | Array | The initial direction vector for emitted particles. || `[0 1 0]` (Array) |
| `emit_rate` | Number | The rate of particle emission per second. || `100` (Number) |
| `emit_spread` | Number | The angle spread for particle emission direction. || `360` (Number) |
| `friction` | Array | A scalar or 3D vector multiplier for velocity reduction applied over time. || `[0 1 0]` (Array) |
| `live_bounds` | Array | The bounds within which particles can exist. || `[-999 999 -999 999 -999 999]` (Array) |
| `movieclip` | Array / Enum | Specifies the visual movie clip or sprite asset used for the object. || `FogParticle` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"WEATHER_FOG_NAME"` (String) |
| `particle_lifetime` | Array | The duration in seconds particles remain alive. || `[3 5]` (Array) |
| `projection_matrix` | Enum | The projection matrix mode for particle rendering (e.g., 'default'). || `default` (Enum) |
| `render_mode` | Enum | The rendering mode for particles (e.g., 'default', 'separate'). || `separate` (Enum) |
| [`scripts`](Miscellaneous.md#object-scripts) | Object | An object containing particle system scripts like forces or collisions. || `{ ... }` (Object) |
| `simulation_space` | Enum | The coordinate space for particle simulation ('local' or 'global'). || `global` (Enum) |
| `size_start` | Array | The starting size of particles. || `[.2 1]` (Array) |
| `speed_start` | String | The initial speed of particles. || `.1` (String) |

### Object: `ForceImmediateMoveAndAttack`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `G3GrabHead` (Enum) |
| `even_if_cant_reach` | Boolean || 2 | `true` (Boolean) |

### Object: `ForceMoveTowardsTaggedObject`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `MoveOneTrample` (Enum), `MoveTwoTrample` (Enum) |
| `tag` | Array / Enum | Specifies the tag(s) to check on the target, used in conditional effects. | 2 | `food` (Enum) |

### Object: `GlobalSpawnOnRoundEnd`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum | Specifies the object or unit to be spawned. | 2 | `NeutralZombieKitten` (Enum), `NeutralTwister` (Enum) |
| `number` | Array / Integer ||| `[1 2]` (Array) |

### Object: `Grappled`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_GRAPPLED_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_GRAPPLED_DESC"` (String) |

### Object: `Grappling`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit_animations`](Characters_and_Bosses.md#object-exit_animations) | Object || 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer | Specifies an animation suffix for partial form changes. | 2 | `Grapple` (Enum) |

### Object: `HealAlliesEachTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exclude_self` | Boolean || 4 | `false` (Boolean) |
| `mana` | Enum / Integer || 4 | `3` (Number), `2` (Number) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `3` (Number), `2` (Number) |

### Object: `HeatWave`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `combo` | Array | A list of particle effect names that are spawned together in sequence. || `[HeatWave_Particles HeatWave_Distortion]` (Array) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"WEATHER_HEATWAVE_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. || `{ ... }` (Object) |
| `hint_persistent_elements` | Array | A list of element types that remain persistent on the ground during this weather. || `[Heat]` (Array) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"WEATHER_HEATWAVE_NAME"` (String), `"KEYWORD_DEHYDRATED_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_DEHYDRATED_DESC"` (String) |

### Object: `HeavyHits`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_HEAVYHITS_NAME"` (String) |
| `tooltip_stackless` | Enum | A localization key for the tooltip description of this status effect when it has no stack count. || `none` (Enum) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_HEAVYHITS_DESC_STACKS"` (String) |

### Object: `HolyDamageBlessing`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Burn` | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |
| `damage_multiplier` | Number || 4 | `3` (Number), `2` (Number) |

### Object: `IceArmor`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum | Specifies the class that this ability belongs to, used for categorization and restrictions. || `Mage` (Enum) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"PASSIVE_ICEASPECT_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"IceArmor"` (Enum), `"PASSIVE_ICEASPECT_NAME"` (String) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `self_buff` (Enum) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `None` (Enum) |

### Object: `IncAuxCounterCycle`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `change` | Integer | The amount to adjust the auxiliary counter by. | 2 | `1` (Number) |
| `max` | Integer | The maximum amount of coins that can be gained. | 2 | `3` (Number) |

### Object: `Invulnerable`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_INVULNERABLE_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_INVULNERABLE_DESC"` (String) |

### Object: `JudgementDay`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"WEATHER_JUDGEMENT_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"WEATHER_JUDGEMENT_NAME"` (String) |

### Object: `KillEnemyOfTypeAtBattleStart`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `enemy_type` | Enum || 2 | `cat` (Enum), `any` (Enum) |
| `fallback_spawn` | Array ||| `[TomTom Kitten CatCaller Mangy]` (Array) |

### Object: `LateStatusApplication`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CurrentWeaponDamageUp` | Integer || 6 | `3` (Number), `1` (Number) |
| `AddWeaponAux` | Integer / String | The amount or expression to add to the source's weapon auxiliary stat. | 2 | `-item_aux` (Enum), `1` (Number), `2` (Number), `"-max(min(X+1, item_aux), 0)"` (String) |

### Object: `LeaveBehind`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum | Specifies the object or unit to be spawned. | 8 | `CharmedMaggot` (Enum), `Twister` (Enum) |

### Object: `Math`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Stun` | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 4 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `1` (Number) |
| [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object | An object of effects that are applied to the source of the ability (the caster). | 2 | `{ ... }` (Object) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `spell` (Enum) |

### Object: `Meaty`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_MEATY_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_MEATY_DESC"` (String) |

### Object: `MergeDamageInstance`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `can_instapop` | Boolean || 2 | `false` (Boolean) |
| `force_no_hit_animation` | Boolean || 2 | `true` (Boolean) |

### Object: `MeteorShower`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"WEATHER_METEORS_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"WEATHER_METEORS_NAME"` (String) |

### Object: `Meteornado`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_in` | String ||| `.2` (String) |
| `alpha_out` | String ||| `.2` (String) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"WEATHER_METEORNADO_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. || `{ ... }` (Object) |
| `emit_amount` | Number | The number of particles emitted per burst. || `1` (Number) |
| `emit_box` | Array | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. || `[0 10 0 5 0 10]` (Array) |
| `emit_direction` | Array | The initial direction vector for emitted particles. || `[0 1 0]` (Array) |
| `emit_rate` | Number | The rate of particle emission per second. || `200` (Number) |
| `emit_spread` | Number | The angle spread for particle emission direction. || `360` (Number) |
| `live_bounds` | Array | The bounds within which particles can exist. || `[-999 999 -999 999 -999 999]` (Array) |
| `movieclip` | Array / Enum | Specifies the visual movie clip or sprite asset used for the object. || `FX_MoonRock` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"WEATHER_METEORNADO_NAME"` (String) |
| `particle_lifetime` | Array | The duration in seconds particles remain alive. || `[.1 3]` (Array) |
| `projection_matrix` | Enum | The projection matrix mode for particle rendering (e.g., 'default'). || `default` (Enum) |
| `render_mode` | Enum | The rendering mode for particles (e.g., 'default', 'separate'). || `separate` (Enum) |
| `rotation` | Array ||| `[0 360]` (Array) |
| `rotation_speed` | Array ||| `[-1000 1000]` (Array) |
| [`scripts`](Miscellaneous.md#object-scripts) | Object | An object containing particle system scripts like forces or collisions. || `{ ... }` (Object) |
| `simulation_space` | Enum | The coordinate space for particle simulation ('local' or 'global'). || `global` (Enum) |
| `size_start` | Array | The starting size of particles. || `[.5 1.5]` (Array) |
| `speed_start` | Number | The initial speed of particles. || `5` (Number) |

### Object: `Metronome`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `1` (Number) |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. || `tk_Metronome` (Enum) |
| `banned_abilities` | Array | A list of ability IDs that are excluded from random selection or usage in the Metronome effect. || `[BatteryNuke WeAreOne Metronome SmartMetronome BecomeEntropy ForbiddenFamine]` (Array) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"ITEM_METRONOME_DESC"` (String) |
| `frame` | Integer | The sprite frame index to display. || `17` (Number) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| `kind` | Enum | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `trinket` (Enum) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"ITEM_METRONOME_NAME"` (String) |
| `rarity` | Enum | Determines the rarity tier of the item, affecting drop rates and item quality. || `rare` (Enum) |
| `set` | Array / Enum | Specifies the set name(s) the item belongs to for set bonuses. || `Jester` (Enum) |
| `tags` | Array / Enum | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). || `[musical]` (Array) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `self_buff` (Enum) |

### Object: `Muted`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_MUTED_NAME"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_MUTED_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_MUTED_DESC"` (String) |
| `tooltip_stacks_singular` | String ||| `"KEYWORD_MUTED_DESC_SINGULAR"` (String) |

### Object: `NextAbilityHeals`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"NextAbilityHeals"` (Enum) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `None` (Enum) |

### Object: `NextActionLuckUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum | Specifies the reference name of another status effect to alias or copy properties from. || `LuckUp` (Enum) |

### Object: `NextAttackBonusRange`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_BONUSRANGE_NAME"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_BONUSRANGE_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_BONUSRANGE_DESC"` (String) |

### Object: `NextAttackSpecialCrit`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crit_multiplier_bonus` | Integer || 2 | `2` (Number) |
| `extra_coins_per_stack` | Integer || 2 | `2` (Number) |
| `luck_increase` | Integer || 2 | `1` (Number) |

### Object: `NextBasicAttackCritsThisTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cant_miss` | Boolean | If true, the damage instance always hits its target regardless of accuracy or evasion. | 2 | `true` (Boolean) |
| `piercing` | Boolean | If true, the damage instance ignores armor or damage reduction effects on the target. | 2 | `true` (Boolean) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `1` (Number) |

### Object: `NextBattleStatusStacks`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MadnessChanceOnTurnBegin` | Integer || 2 | `2` (Number) |
| `fights` | Integer | The number of future battles the status effect will be applied at the start of. | 2 | `9999` (Number) |

### Object: `NextDamageReduceAndHealAllies`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"NextDamageReduceAndHealAllies"` (Enum) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `None` (Enum) |

### Object: `NextTurnDoubleRangedDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_DOUBLERANGEDDMG_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_DOUBLERANGEDDMG_DESC"` (String) |

### Object: `ObjectOnHit`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum | Specifies the object or unit to be spawned. | 4 | `Poop` (Enum) |

### Object: `OverHealToStatuses`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"` (Enum), `"ceil(X/3)"` (Enum), `10` (Number), `3` (Number) |
| `TakeExtraTurn` | Integer | The number of extra turns granted to the source. | 2 | `1` (Number) |
| `stack_scale` | Integer | The scaling factor for how many stacks of the over-heal status are applied. | 2 | `0` (Number) |

### Object: `PoolMetronome`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pool` | Array / Enum | Specifies the name of the pool from which an ability is learned or an item is crafted. || `[Shockwave Ping Telefrag Stasis Reduce Zealot]` (Array) |

### Object: `QuakeAreaChance`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 4 | `50` (Number) |
| `radius` | Array / Integer || 4 | `1` (Number), `0` (Number) |

### Object: `RandomDistanceDisplace`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `min_dist` | Integer | The minimum distance in tiles the target must be displaced by the knockback effect. | 2 | `4` (Number) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `20` (Number) |

### Object: `RandomKnockback`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer | The maximum amount of coins that can be gained. | 4 | `10` (Number), `3` (Number) |
| `min` | Integer | The minimum amount of coins that will be gained. | 4 | `1` (Number) |

### Object: `ReduceManaCostExcludeBrainstorm`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_INSIGHT_NAME"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_INSIGHT_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_INSIGHT_DESC"` (String) |

### Object: `Regurge`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Boolean / Integer / Object | Defines damage or effects applied to the caster when using the ability. || `{ ... }` (Object) |
| [`spawn`](Abilities_and_Spells.md#object-spawn) | Object | Defines what object or unit is spawned when the ability is used. || `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `spawn` (Enum) |

### Object: `RepressedMemoriesMetronome`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pool` | Array / Enum | Specifies the name of the pool from which an ability is learned or an item is crafted. | 4 | `Psychic` (Enum), `Jester` (Enum) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `1` (Number) |

### Object: `Sandstorm`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. || `amb_sandstorm.ogg` (String) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"WEATHER_SANDSTORM_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"WEATHER_SANDSTORM_NAME"` (String) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `self_buff` (Enum) |

### Object: `ScrambleLastUsedSpell`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `permanent` | Boolean || 2 | `true` (Boolean) |

### Object: `SerratedClaws`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_SERRATED_NAME"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_SERRATED_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_SERRATED_DESC"` (String) |

### Object: `SetAnimationAlts`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dead` | Enum | Determines the animation set used when the unit is dead. | 2 | `deadShot` (Enum) |
| `dying` | Enum | Determines the animation set used when the unit is in a dying state. | 2 | `shot` (Enum) |

### Object: `SetCrazyEyeBackgroundWeights`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `weights` | Array / Enum | Specifies the weight array or named preset for the crazy eye background AI. || `[0 0 1]` (Array), `[0 1 0]` (Array) |

### Object: `Shatter`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `melee_attack` (Enum) |

### Object: `ShortCircuit`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_SHORTCIRCUIT_NAME"` (String) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `spell` (Enum) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_SHORTCIRCUIT_DESC"` (String) |

### Object: `SmartMetronome`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `20` (Number) |
| `upgraded` | Boolean | If true, the evolved ability is the upgraded version. | 2 | `true` (Boolean) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `tags` | Array / Enum | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). || `[musical]` (Array) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `self_buff` (Enum) |

### Object: `SmellBlood`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `self_buff` (Enum) |

### Object: `Snow`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `adventure_weather` | Enum | Specifies the weather type on the adventure map, determining visual and gameplay effects. | 1 | `Snow` (Enum) |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. | 1 | `amb_snow.ogg` (String) |
| `prewarm` | Number | The number of seconds the particle system simulates forward before becoming visible. | 1 | `20` (Number) |
| `skybox_frame` | Enum | Determines which skybox background frame is displayed for this weather. | 1 | `day_snow` (Enum) |
| `alpha` | String | The alpha transparency value for the particle system (e.g., '0.03'). || `.5` (String) |
| `combo` | Array | A list of particle effect names that are spawned together in sequence. || `[SnowB SnowM SnowF]` (Array) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"WEATHER_SNOW_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. || `{ ... }` (Object) |
| `emit_amount` | Number | The number of particles emitted per burst. || `1` (Number) |
| `emit_box` | Array | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. || `[0 10 10 10 0 10]` (Array) |
| `emit_direction` | Array | The initial direction vector for emitted particles. || `[0 -1 0]` (Array) |
| `emit_rate` | Number | The rate of particle emission per second. || `200` (Number) |
| `emit_spread` | Number | The angle spread for particle emission direction. || `10` (Number) |
| `hint_persistent_elements` | Array | A list of element types that remain persistent on the ground during this weather. || `[Ice]` (Array) |
| `live_bounds` | Array | The bounds within which particles can exist. || `[-0.5 999 -999 999 -0.5 999]` (Array) |
| `movieclip` | Array / Enum | Specifies the visual movie clip or sprite asset used for the object. || `ParticleTestNoRandom` (Enum) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"WEATHER_SNOW_NAME"` (String) |
| `particle_lifetime` | Number | The duration in seconds particles remain alive. || `7` (Number) |
| `particles` | Array | A list of particle system identifiers used to render the weather effects. || `[Snow]` (Array) |
| `projection_matrix` | Enum | The projection matrix mode for particle rendering (e.g., 'default'). || `default` (Enum) |
| `render_mode` | Enum | The rendering mode for particles (e.g., 'default', 'separate'). || `separate` (Enum) |
| `rotation` | Array ||| `[0 360]` (Array) |
| `rotation_speed` | Array ||| `[-100 100]` (Array) |
| `rotation_speed_end` | Number ||| `0` (Number) |
| [`scripts`](Miscellaneous.md#object-scripts) | Object | An object containing particle system scripts like forces or collisions. || `{ ... }` (Object) |
| `simulation_space` | Enum | The coordinate space for particle simulation ('local' or 'global'). || `global` (Enum) |
| `size_end` | Number ||| `0` (Number) |
| `size_start` | Array | The starting size of particles. || `[.3 .8]` (Array) |
| `speed_start` | Array | The initial speed of particles. || `[2 4]` (Array) |

### Object: `SolarFlare`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Equation | Specifies the amount of damage dealt, can be a number or expression. | 1 | `5` (Equation) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. | 1 | `{ ... }` (Object) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"WEATHER_SOLARFLARE_DESC"` (String) |
| `elements` | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. || `[Fire]` (Array) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"WEATHER_SOLARFLARE_NAME"` (String) |

### Object: `SpawnTilePuddleOnBattleStart`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max_radius` | Number || 1 | `3.5` (Number) |
| `min_radius` | Number || 1 | `1.5` (Number) |
| `tile` | Array / Enum | Specifies the tile type(s) to change to, either a single tile string or an array of tiles. | 1 | `OilTile` (Enum) |

### Object: `SpawnVolcanoOnBattleStart`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum | Specifies the object or unit to be spawned. | 3 | `Sprout` (Enum), `MiniVolcano` (Enum) |
| `max_radius` | Number || 2 | `2.2` (Number) |
| `min_radius` | Number / String || 2 | `1` (Number), `.2` (String) |
| `puddle_tile` | Array / Enum || 1 | `[BrambleTile TallBrambleTile]` (Array), `LavaTile` (Enum) |
| `number` | Array / Integer ||| `[3 5]` (Array) |

### Object: `SpecialGodRays`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Big`](Characters_and_Bosses.md#object-big) | Object || 2 | `{ ... }` (Object) |

### Object: `SpellShield`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"SpellShield"` (Enum) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `None` (Enum) |

### Object: `StatBounty`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_STATBOUNTY_NAME"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_STATBOUNTY_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_STATBOUNTY_DESC"` (String) |

### Object: `StatusCharactersOnRoundEnd`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 1 | `{ ... }` (Object) |
| `FloatingRockTrap` | Integer || 1 | `1` (Number) |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 1 | `[1 .5]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |
| `tag_filter` | Enum || 1 | `rock` (Enum) |

### Object: `StatusCharactersOnRoundStart`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 1 | `{ ... }` (Object) |
| [`Else`](Abilities_and_Spells.md#object-else) | Object | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ ... }` (Object) |
| [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. || `[1 .1]` (Array), `[1 .25]` (Array), `999` (Number), `3` (Number), `{ ... }` (Object) |

### Object: `SwapWeapon`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pool` | Array / Enum | Specifies the name of the pool from which an ability is learned or an item is crafted. || `[TerminatorShotgun TerminatorSniper TerminatorUzi]` (Array) |

### Object: `SwitchMusic`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `new_layer` | Enum || 14 | `battle` (Enum), `map` (Enum) |
| `new_song` | Enum || 12 | `same` (Enum) |
| `crossfade_speed` | Integer | The duration in seconds for the crossfade transition between music tracks. | 2 | `1` (Number) |

### Object: `Switcheroo`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"Switcheroo"` (Enum) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `self_buff` (Enum) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `None` (Enum) |

### Object: `Taunting`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"Taunting"` (Enum) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `None` (Enum) |

### Object: `TeamCastAbility`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `CollectiveSpinImpl` (Enum), `CollectiveCounterImpl` (Enum) |
| `tag_restriction` | Enum | Specifies a tag that the target unit must have for the team cast to trigger. | 4 | `collective` (Enum) |
| `same_orientation` | Boolean | If true, the team cast ability only triggers if the caster and target face the same direction. | 2 | `true` (Boolean) |

### Object: `TempBackstab`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_TEMPBACKSTAB_NAME"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_TEMPBACKSTAB_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_TEMPBACKSTAB_DESC"` (String) |

### Object: `TempBonusKnockback`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_BONUSKNOCKBACK_NAME"` (String) |
| `tooltip_stackless` | Enum | A localization key for the tooltip description of this status effect when it has no stack count. || `None` (Enum) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_BONUSKNOCKBACK_DESC"` (String) |

### Object: `TempBonusKnockbackDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_BONUSKNOCKBACKDAMAGE_NAME"` (String) |
| `tooltip_stackless` | Enum | A localization key for the tooltip description of this status effect when it has no stack count. || `None` (Enum) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_BONUSKNOCKBACKDAMAGE_DESC"` (String) |

### Object: `TempCritChanceUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum | Specifies the reference name of another status effect to alias or copy properties from. || `CritChanceUp` (Enum) |

### Object: `TempInjuryImmunity`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_TEMPIMMUNE_NAME"` (String) |
| `tooltip_stackless` | Enum | A localization key for the tooltip description of this status effect when it has no stack count. || `none` (Enum) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_TEMPIMMUNE_DESC"` (String) |
| `tooltip_stacks_singular` | String ||| `"KEYWORD_TEMPIMMUNE_DESC_SINGULAR"` (String) |

### Object: `TempManaCostReduction`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_TEMPMANAREDUCTION_NAME"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_TEMPMANAREDUCTION_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_TEMPMANAREDUCTION_DESC"` (String) |

### Object: `TempPreEmptiveCounterAttack`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_PRECOUNTER_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_PRECOUNTER_DESC"` (String) |

### Object: `TemporaryItem`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number | The sprite frame index for the buff icon. || `164` (Number) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_TEMPITEM_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_TEMPITEM_DESC"` (String) |

### Object: `TilesMovedToCritChance`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"TilesMovedToCritChance"` (Enum) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `None` (Enum) |

### Object: `TilesMovedToMana`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"TilesMovedToMana"` (Enum) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `None` (Enum) |

### Object: `TilesMovedToNeighborHeal`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"TilesMovedToNeighborHeal"` (Enum) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `None` (Enum) |

### Object: `TilesMovedToStrength`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"TilesMovedToStrength"` (Enum) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `None` (Enum) |

### Object: `TimeDelayStatusApplication`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `delay` | Number || 8 | `1.13333` (Number), `3` (Number), `.1` (String), `.25` (String) |
| [`SwitchMusic`](Abilities_and_Spells.md#object-switchmusic) | Object || 4 | `{ ... }` (Object) |
| [`Cleanse`](#object-cleanse) | Integer / Object | The number of stacks of negative status effects removed from the target. | 2 | `1` (Number), `0` (Number), `{ ... }` (Object) |
| [`CreateGlobalModifiers`](Abilities_and_Spells.md#object-createglobalmodifiers) | Object | Defines global gameplay modifiers to activate. | 2 | `{ ... }` (Object) |
| [`DoScreenShake`](Abilities_and_Spells.md#object-doscreenshake) | Integer / Object || 2 | `1` (Number), `{ ... }` (Object) |
| [`FormChange`](Abilities_and_Spells.md#object-formchange) | Enum / Object | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 2 | `passive` (Enum), `Boris` (Enum), `{ ... }` (Object) |
| `FullHeal` | Integer | If non-zero, fully restores the target's health. | 2 | `1` (Number), `0` (Number) |
| `GlobalSpawnCharacter` | Enum || 2 | `MegaGuppy` (Enum) |
| `PlayBackground` | Integer || 2 | `1` (Number), `0` (Number) |
| `RemoveAmbientLightEffects` | Number | The fade-out duration in seconds for ambient light effects. | 2 | `4` (Number), `.5` (String) |
| `Vaporize` | Integer | Removes the target from play, preventing its corpse from being interacted with. | 2 | `1` (Number), `20` (Number) |

### Object: `TowerDefenseStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_SENTRY_NAME"` (String) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `"KEYWORD_SENTRY_DESC"` (String) |

### Object: `TowerDefenseStatus2`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"KEYWORD_SENTRYPLUS_NAME"` (String) |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_SENTRYPLUS_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_SENTRYPLUS_DESC"` (String) |

### Object: `TradeLife`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bonus_passives`](Abilities_and_Spells.md#object-bonus_passives) | Object ||| `{ ... }` (Object) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `spell` (Enum) |

### Object: `TrailBlazer`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"Trail Blazer"` (String) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `self_buff` (Enum) |
| `tooltip` | Enum | The localization string key used for the tooltip displayed on hover. || `None` (Enum) |

### Object: `TransformEquipment`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `from` | Enum || 2 | `JarOfChaos` (Enum) |
| `to` | Enum || 2 | `JarOfNothing` (Enum) |

### Object: `TwisterDisplaceWithDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Equation | Specifies the amount of damage dealt, can be a number or expression. | 12 | `inherit` (Equation), `1` (Equation) |
| `max_dist` | Integer | The maximum distance in tiles the target can be displaced by the knockback effect. | 12 | `3` (Number), `20` (Number) |
| `min_dist` | Integer | The minimum distance in tiles the target must be displaced by the knockback effect. | 4 | `3` (Number), `2` (Number) |
| `exclude_prefix` | Enum | Specifies a prefix string; units with a matching prefix in their ID are excluded from the displacement effect. | 2 | `Twister` (Enum) |

### Object: `UseMoveAbilityWithAI`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `LEPortFar` (Enum) |
| `move_weights` | Enum | Determines the movement strategy used by the AI when executing this move ability. | 2 | `stay_far_move_far` (Enum) |

### Object: `VisualCountDownThenApplyStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | The name of the ability the source is forced to use, optionally with a chance. | 2 | `neck_ChefsApron` (Enum), `head_HitlersToupe` (Enum), `{ ... }` (Object) |

### Object: `VisualFlySwarm`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. || `amb_flyswarm.ogg` (String) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"WEATHER_TORFLIES_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. || `{ ... }` (Object) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"WEATHER_TORFLIES_NAME"` (String) |

### Object: `WaggleClone`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cWaggle`](Abilities_and_Spells.md#object-cwaggle) | Boolean (Flag) / Object | Defines a clone variant of the Waggle unit with its own graphics and properties. | 2 | `(Flag)` (Boolean (Flag)), `{ ... }` (Object) |
| [`cWaggle2x2`](Abilities_and_Spells.md#object-cwaggle2x2) | Boolean (Flag) / Object | Defines a larger 2x2 tile clone variant of the Waggle unit. | 2 | `(Flag)` (Boolean (Flag)), `{ ... }` (Object) |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `5` (Number) |
| [`cWaggle3x3`](Abilities_and_Spells.md#object-cwaggle3x3) | Boolean (Flag) / Object | Defines an even larger 3x3 tile clone variant of the Waggle unit. || `(Flag)` (Boolean (Flag)), `{ ... }` (Object) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. || `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. || `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ ... }` (Object) |
| `template` | Enum | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `lobbed_attack` (Enum) |

### Object: `Windy`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `adventure_weather` | Enum | Specifies the weather type on the adventure map, determining visual and gameplay effects. | 1 | `Windy` (Enum) |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. | 1 | `amb_windy.ogg` (String) |
| `prewarm` | Number | The number of seconds the particle system simulates forward before becoming visible. | 1 | `5` (Number) |
| `skybox_frame` | Enum | Determines which skybox background frame is displayed for this weather. | 1 | `day_windy` (Enum) |
| `desc` | Enum | Specifies the localized description string for the item or ability. || `"WEATHER_WINDY_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Applies a list of status effects or visual effects to targets. || `{ ... }` (Object) |
| `hint_persistent_elements` | Array | A list of element types that remain persistent on the ground during this weather. || `[Wind]` (Array) |
| `name` | Enum | Specifies the localized name string for the entity, item, or ability. || `"WEATHER_WINDY_NAME"` (String) |
| `particles` | Array | A list of particle system identifiers used to render the weather effects. || `[WindFull]` (Array) |

### Object: `XIsTargetHealth`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 4 | `"ceil(X/2)"` (Enum), `str` (Enum), `-4` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |



---

## Auto-Discovered Objects


### Object: `AbsorbBuff`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_end` | Number | The alpha (opacity) value at the end of the effect's duration or animation. | 1 | `2` |
| `alpha_start` | Number | The alpha (opacity) value at the start of the effect's duration or animation. | 1 | `-1` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1` |
| `emit_box` | Array | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `0 0 0 1 0 0` |
| `emit_direction` | Array | The initial direction vector for emitted particles. | 1 | `0 1 0` |
| `emit_rate` | Number | The rate of particle emission per second. | 1 | `4` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `180` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `true` |
| `live_bounds` | Array | The bounds within which particles can exist. | 1 | `-999 999 -999 999 -999 999` |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `ManaParticle` |
| `ownership` | String | The ownership scope for the effect, such as local to the caster. | 1 | `local` |
| `particle_lifetime` | Array | The duration in seconds particles remain alive. | 1 | `.5 1.5` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `separate` |
| [`scripts`](Miscellaneous.md#object-scripts) | Object | An object containing particle system scripts like forces or collisions. | 1 ||
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global` |
| `size_end` | Number | The size (scalar or 2D vector) of the effect at the end of its animation. | 1 | `.5` |
| `size_start` | Array | The starting size of particles. | 1 | `2 3` |
| `speed_scale` | Number | A multiplier for particle speed. | 1 | `0` |
| `speed_start` | Number | The initial speed of particles. | 1 | `1` |

</details>

### Object: `BBTransformMutant`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `self_buff` |

</details>

### Object: `BBTransformZealot`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `self_buff` |

</details>

### Object: `BasicButcherMelee`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `melee_attack` |

</details>

### Object: `BasicDruidAbility`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| `tags` | Array | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `musical` |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `spell` |

</details>

### Object: `BasicMagicMissile`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `spell` |

</details>

### Object: `BasicMagicShortRanged`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `ranged_attack` |

</details>

### Object: `BasicMedicMelee`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `melee_attack` |

</details>

### Object: `BasicMelee`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `melee_attack` |

</details>

### Object: `BasicMelee_4Hits`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `BasicMelee` |

</details>

### Object: `BasicMonkMelee`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `melee_attack` |

</details>

### Object: `BasicNecroRanged`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `lobbed_attack` |

</details>

### Object: `BasicPsychicPull`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `spell` |

</details>

### Object: `BasicRanged`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `lobbed_attack` |

</details>

### Object: `BasicStraightShot`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `straightshot_attack` |

</details>

### Object: `BasicSuplex`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `SuplexAbility` |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| `tags` | Array | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `cant_be_simulcast` |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `melee_attack` |

</details>

### Object: `BasicTankMelee`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack` |

</details>

### Object: `BeefyCharmedLeech`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Maggot` |

</details>

### Object: `Bionic`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `"SETBONUS_BIONIC_DESC"` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `"SETBONUS_BIONIC_NAME"` |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| `pieces_required` | Number | The number of scrap pieces required to craft this item. | 1 | `3` |

</details>

### Object: `BloatEyeMovement2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `move` |

</details>

### Object: `BloatyExplodey`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `spell` |

</details>

### Object: `BoneWormShotMed`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `lobbed_attack` |

</details>

### Object: `BonusToss`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `throw_attack` |

</details>

### Object: `BonusToss2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `BonusToss` |

</details>

### Object: `BoomerCatExplode`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `spell` |

</details>

### Object: `BoyDino`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||

</details>

### Object: `BoyDinoCry`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `self_buff` |

</details>

### Object: `BrambleRandomTileEvent`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `spell` |

</details>

### Object: `BungaSwipe`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai_ability` | String | Specifies the ability to use as the AI's behavior for this ability. | 1 | `BungaSwipe_ai` |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `melee_attack` |

</details>

### Object: `CatGoop`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `straightshot_attack` |

</details>

### Object: `CatapultJump`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `BasicJump` |

</details>

### Object: `CatapultJump2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `CatapultJump` |

</details>

### Object: `CaveCatDad`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`equipment`](Characters_and_Bosses.md#object-equipment) | Object | A container object defining the character's equipped items (head, face, neck, weapon, etc.). | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||

</details>

### Object: `CerberubsStraightReaction`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `straightshot_attack` |

</details>

### Object: `CharmedDemonKitten`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Hyde` |

</details>

### Object: `CharmedFly`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Fly` |

</details>

### Object: `CharmedFlySwarm`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `FlySwarm` |

</details>

### Object: `CharmedLeech`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Maggot` |

</details>

### Object: `CharmedPooter`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Pooter` |

</details>

### Object: `CharmedReaper`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Reaper` |

</details>

### Object: `CharmedTinySpider`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 2 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 2 | `TinySpider` |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||

</details>

### Object: `CharmedTinyTumor`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `TinyTumor` |

</details>

### Object: `Chubs`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||

</details>

### Object: `ChubsGoop`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `straightshot_attack` |

</details>

### Object: `ChubsRage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `self_buff` |

</details>

### Object: `CookedChickenLeg`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `CookedBigFood` |

</details>

### Object: `CraterCreeperOut`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||

</details>

### Object: `DarkOneStrike`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `spell` |

</details>

### Object: `DecoyExplode`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `spell` |

</details>

### Object: `DefaultMove`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `move` |

</details>

### Object: `DestroyerShieldBash`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `BasicBigMelee` |

</details>

### Object: `Digest`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `DamageConsumedCharactersAbilit` |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Object | Defines damage or effects applied to the caster when using the ability. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `self_buff` |

</details>

### Object: `DrMangler`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||

</details>

### Object: `EatShit`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `tile_targeted_melee_attack` |

</details>

### Object: `FireExtinguish_Steam`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha` | Number | The alpha transparency value for the particle system (e.g., '0.03'). | 1 | `.1` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `200` |
| `emit_box` | Array | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `-.1 .1 .2 .2 -.1 .1` |
| `emit_direction` | Array | The initial direction vector for emitted particles. | 1 | `0 1 0` |
| `emit_radius` | Number | The radius from which particles or effects are emitted. | 1 | `.4` |
| `emit_rate` | Number | The rate of particle emission per second. | 1 | `1` |
| `emit_timespread` | Number | The time spread over which emissions occur, controlling the duration of the emission burst. | 1 | `.75` |
| `emit_timespread_curve` | String | The curve type (e.g., ease_out) that defines how emission rate changes over time. | 1 | `ease_out` |
| `live_bounds` | Array | The bounds within which particles can exist. | 1 | `-999 999 -999 999 -999 999` |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `ParticleDustCloud` |
| `particle_lifetime` | Number | The duration in seconds particles remain alive. | 1 | `1` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `separate` |
| [`scripts`](Miscellaneous.md#object-scripts) | Object | An object containing particle system scripts like forces or collisions. | 1 ||
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global` |
| `size` | Array | The scale factor (size multiplier) of the spawned unit. | 1 | `.5 2` |
| `speed` | Array | The speed of the projectile or move, can be a value or a range. | 1 | `1 3` |

</details>

### Object: `FlyBuff`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_end` | Number | The alpha (opacity) value at the end of the effect's duration or animation. | 1 | `2` |
| `alpha_start` | Number | The alpha (opacity) value at the start of the effect's duration or animation. | 1 | `-1` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1` |
| `emit_box` | Array | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `0 0 0 1 0 0` |
| `emit_direction` | Array | The initial direction vector for emitted particles. | 1 | `0 1 0` |
| `emit_rate` | Number | The rate of particle emission per second. | 1 | `50` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `180` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `true` |
| `live_bounds` | Array | The bounds within which particles can exist. | 1 | `-999 999 -999 999 -999 999` |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `Critter_Fly` |
| `ownership` | String | The ownership scope for the effect, such as local to the caster. | 1 | `local` |
| `particle_lifetime` | Array | The duration in seconds particles remain alive. | 1 | `.5 1.5` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `separate` |
| [`scripts`](Miscellaneous.md#object-scripts) | Object | An object containing particle system scripts like forces or collisions. | 1 ||
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global` |
| `size_end` | Number | The size (scalar or 2D vector) of the effect at the end of its animation. | 1 | `0` |
| `size_start` | Array | The starting size of particles. | 1 | `3 4` |
| `speed_scale` | Number | A multiplier for particle speed. | 1 | `.25` |
| `speed_start` | Number | The initial speed of particles. | 1 | `1` |

</details>

### Object: `GirlDino`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||

</details>

### Object: `GirlDinoCry`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `self_buff` |

</details>

### Object: `GrenadeExplode`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Object | Defines damage or effects applied to the caster when using the ability. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `spell` |

</details>

### Object: `Guillotina2Body`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||

</details>

### Object: `Guillotina2Head`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||

</details>

### Object: `Guillotina3Body`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||

</details>

### Object: `Guillotina3Head`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||

</details>

### Object: `HCHumanDie`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `self_buff` |

</details>

### Object: `Haunt`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `spell` |

</details>

### Object: `HemBounce`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `melee_attack` |

</details>

### Object: `Hyde`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| `arm1` | Number | The catalog ID for the cat's first arm part. | 1 | `1013` |
| `arm2` | Number | The catalog ID for the cat's second arm part. | 1 | `1013` |
| `body` | Number | The catalog ID for the cat's body part. | 1 | `31` |
| `claws` | Number | The sprite frame index for the character's claws. | 1 | `1` |
| `default_face` | String | Specifies the default facial expression for the unit's portrait. | 1 | `angry` |
| `default_frame` | Number | The default sprite frame used for the character's portrait or body. | 1 | `1` |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| `head` | Number | The catalog ID for the cat's head part. | 1 | `62` |
| `leftear` | Number | The sprite frame index for the character's left ear. | 1 | `1013` |
| `lefteye` | Number | The sprite frame index for the character's left eye. | 1 | `1013` |
| `lefteyebrow` | Number | The sprite frame index for the character's left eyebrow. | 1 | `63` |
| `leg1` | Number | The catalog ID for the cat's first leg part. | 1 | `37` |
| `leg2` | Number | The catalog ID for the cat's second leg part. | 1 | `37` |
| `mouth` | Number | The catalog ID for the cat's mouth part. | 1 | `1013` |
| `palette` | Number | Specifies the color palette index for the ability's visuals. | 1 | `59` |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| `pitch` | Number | The sound pitch multiplier for the character's voice or sounds. | 1 | `.9` |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| `rightear` | Number | The sprite frame index for the character's right ear. | 1 | `1013` |
| `righteye` | Number | The sprite frame index for the character's right eye. | 1 | `1013` |
| `righteyebrow` | Number | The sprite frame index for the character's right eyebrow. | 1 | `63` |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||
| `tail` | Number | The catalog ID for the cat's tail part. | 1 | `1004` |
| `texture` | Number | The catalog ID for the cat's texture. | 1 | `1000` |
| `voice` | String | Determines which voice set or type is used for the character. | 1 | `male9` |

</details>

### Object: `IDSprout`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`spawn`](Abilities_and_Spells.md#object-spawn) | Object | Defines what object or unit is spawned when the ability is used. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `spawn` |

</details>

### Object: `Lava_Distortion`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha` | Number | The alpha transparency value for the particle system (e.g., '0.03'). | 1 | `.01` |
| `alpha_end` | Number | The alpha (opacity) value at the end of the effect's duration or animation. | 1 | `0` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1` |
| `emit_box` | Array | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `-.4 .4 0 0 -.4 .4` |
| `emit_direction` | Array | The initial direction vector for emitted particles. | 1 | `0 1 0` |
| `emit_rate` | Number | The rate of particle emission per second. | 1 | `10` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `4` |
| `live_bounds` | Array | The bounds within which particles can exist. | 1 | `-999 999 0 999 -999 999` |
| `material` | String | The material shader name used for rendering the visual effect. | 1 | `distorter` |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `Particle_HeatWaveDistortion` |
| `particle_lifetime` | Array | The duration in seconds particles remain alive. | 1 | `.5 1` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| `render_layer` | String | The render layer on which the effect is drawn (e.g., background, top). | 1 | `sorted_distortions` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `separate` |
| `rotation` | Array | The rotation of the effect, specified as a single value or a random range [min, max] in degrees. | 1 | `0 0` |
| `rotation_speed_end` | Number | The rotation speed (in degrees per second) of the effect at the end of its animation. | 1 | `0` |
| [`scripts`](Miscellaneous.md#object-scripts) | Object | An object containing particle system scripts like forces or collisions. | 1 ||
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global` |
| `size_end` | Number | The size (scalar or 2D vector) of the effect at the end of its animation. | 1 | `3` |
| `size_start` | Number | The starting size of particles. | 1 | `1` |
| `speed_start` | Array | The initial speed of particles. | 1 | `1 2` |

</details>

### Object: `LennyCatDies`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `DamageConsumedCharactersAbilit` |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Object | Defines damage or effects applied to the caster when using the ability. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `self_buff` |

</details>

### Object: `Maggot`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||

</details>

### Object: `ManglerEnrage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `self_buff` |

</details>

### Object: `ManglerMonsterDashAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack` |

</details>

### Object: `ManglersMonster`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||

</details>

### Object: `MechExplode`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Object | Defines damage or effects applied to the caster when using the ability. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `throw_attack` |

</details>

### Object: `MegaFart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `spell` |

</details>

### Object: `MegaGuppy_SummonTheChild`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`spawn`](Abilities_and_Spells.md#object-spawn) | Object | Defines what object or unit is spawned when the ability is used. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `spawn` |

</details>

### Object: `MockingbirdForm`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| `tags` | Array | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `shapeshift` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `self_buff` |

</details>

### Object: `MoonHead_KillHands`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `targeted_status` |

</details>

### Object: `MoveOne`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `move` |

</details>

### Object: `Necro_SoulDagger_Uncharged`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `wp_NecroSoulDagger` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `"ITEM_SOULDAGGER_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `118` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `weapon` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `"ITEM_SOULDAGGER_NAME"` |

</details>

### Object: `NoHead`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| `claws` | Number | The sprite frame index for the character's claws. | 1 | `1` |
| `default_frame` | Number | The default sprite frame used for the character's portrait or body. | 1 | `1000` |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| `head` | Number | The catalog ID for the cat's head part. | 1 | `1036` |
| `leftear` | Number | The sprite frame index for the character's left ear. | 1 | `1005` |
| `lefteye` | Number | The sprite frame index for the character's left eye. | 1 | `1028` |
| `lefteyebrow` | Number | The sprite frame index for the character's left eyebrow. | 1 | `1022` |
| `mouth` | Number | The catalog ID for the cat's mouth part. | 1 | `1042` |
| `palette` | Number | Specifies the color palette index for the ability's visuals. | 1 | `9` |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| `pitch` | Number | The sound pitch multiplier for the character's voice or sounds. | 1 | `.5` |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| `rightear` | Number | The sprite frame index for the character's right ear. | 1 | `1005` |
| `righteye` | Number | The sprite frame index for the character's right eye. | 1 | `1028` |
| `righteyebrow` | Number | The sprite frame index for the character's right eyebrow. | 1 | `1022` |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||
| `texture` | Number | The catalog ID for the cat's texture. | 1 | `1000` |
| `voice` | String | Determines which voice set or type is used for the character. | 1 | `male1` |

</details>

### Object: `NonChampionFlySwarm`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `FlySwarm` |

</details>

### Object: `NubbyToss`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `throw_attack` |

</details>

### Object: `Nubs`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||

</details>

### Object: `NubsGoop`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `lobbed_attack` |

</details>

### Object: `Ornstein`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||

</details>

### Object: `Paper`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `"SETBONUS_PAPER_DESC"` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `"SETBONUS_PAPER_NAME"` |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| `pieces_required` | Number | The number of scrap pieces required to craft this item. | 1 | `3` |

</details>

### Object: `PassiveEnergized`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1` |
| `emit_box` | Array | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `0 0 .3 .3 0 0` |
| `emit_direction` | Array | The initial direction vector for emitted particles. | 1 | `0 1 0` |
| `emit_radius` | Number | The radius from which particles or effects are emitted. | 1 | `.4` |
| `emit_rate` | Number | The rate of particle emission per second. | 1 | `15` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `45` |
| `friction` | Array | A scalar or 3D vector multiplier for velocity reduction applied over time. | 1 | `-.05 -.1 -.05` |
| `live_bounds` | Array | The bounds within which particles can exist. | 1 | `-999 999 -999 999 -999 999` |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `Particle_Electric` |
| `particle_lifetime` | Number | The duration in seconds particles remain alive. | 1 | `.5` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `separate` |
| `rotation` | Array | The rotation of the effect, specified as a single value or a random range [min, max] in degrees. | 1 | `-90 90` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global` |
| `size` | Array | The scale factor (size multiplier) of the spawned unit. | 1 | `.5 1` |
| `size_in` | Number | The size of the effect at the beginning of its intro animation. | 1 | `.1` |
| `speed_start` | Array | The initial speed of particles. | 1 | `0 2` |
| `unlit` | Boolean | If true, the effect is not affected by scene lighting. | 1 | `true` |

</details>

### Object: `PassiveTar`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_in` | Number | The alpha (opacity) value at the start of the effect's intro animation. | 1 | `.2` |
| `alpha_out` | Number | The alpha (opacity) value at the end of the effect's outro animation. | 1 | `.5` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1` |
| `emit_box` | Array | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `0 0 .7 .7 0 0` |
| `emit_direction` | Array | The initial direction vector for emitted particles. | 1 | `0 1 0` |
| `emit_radius` | Number | The radius from which particles or effects are emitted. | 1 | `.4` |
| `emit_rate` | Number | The rate of particle emission per second. | 1 | `4` |
| `force_end` | Array | The final force applied to particles over time, as a scalar or 3D vector. | 1 | `0 -1 0` |
| `force_start` | Array | The initial force applied to particles, as a scalar or 3D vector. | 1 | `0 0 0` |
| `live_bounds` | Array | The bounds within which particles can exist. | 1 | `-999 999 -999 999 -999 999` |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `Particle_TarDrip` |
| `particle_lifetime` | Array | The duration in seconds particles remain alive. | 1 | `1 1.5` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `separate` |
| `rotation` | Number | The rotation of the effect, specified as a single value or a random range [min, max] in degrees. | 1 | `-90` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global` |
| `size` | Number | The scale factor (size multiplier) of the spawned unit. | 1 | `.5` |
| `size_in` | Number | The size of the effect at the beginning of its intro animation. | 1 | `.1` |
| `speed_start` | Number | The initial speed of particles. | 1 | `0` |
| `spurt` | String | The name of the spurt particle effect to play. | 1 | `PassiveTarSplat` |

</details>

### Object: `PlayerCat_ThiefShade2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `PlayerCat` |

</details>

### Object: `RatKing`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||

</details>

### Object: `ReaperRevenge`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Object | Defines damage or effects applied to the caster when using the ability. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `teleport` |

</details>

### Object: `SandStormBuff`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_end` | Number | The alpha (opacity) value at the end of the effect's duration or animation. | 1 | `2` |
| `alpha_start` | Number | The alpha (opacity) value at the start of the effect's duration or animation. | 1 | `-1` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1` |
| `emit_box` | Array | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `0 0 0 1 0 0` |
| `emit_direction` | Array | The initial direction vector for emitted particles. | 1 | `0 1 0` |
| `emit_rate` | Number | The rate of particle emission per second. | 1 | `100` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `180` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `true` |
| `live_bounds` | Array | The bounds within which particles can exist. | 1 | `-999 999 -999 999 -999 999` |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `SandStormParticle` |
| `ownership` | String | The ownership scope for the effect, such as local to the caster. | 1 | `local` |
| `particle_lifetime` | Array | The duration in seconds particles remain alive. | 1 | `.1 1` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `separate` |
| [`scripts`](Miscellaneous.md#object-scripts) | Object | An object containing particle system scripts like forces or collisions. | 1 ||
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global` |
| `size_end` | Number | The size (scalar or 2D vector) of the effect at the end of its animation. | 1 | `0` |
| `size_start` | Array | The starting size of particles. | 1 | `.4 .6` |
| `speed_scale` | Number | A multiplier for particle speed. | 1 | `.25` |
| `speed_start` | Number | The initial speed of particles. | 1 | `1` |

</details>

### Object: `Shadowstep`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `teleport` |

</details>

### Object: `ShineBuff`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_end` | Number | The alpha (opacity) value at the end of the effect's duration or animation. | 1 | `2` |
| `alpha_start` | Number | The alpha (opacity) value at the start of the effect's duration or animation. | 1 | `.5` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1` |
| `emit_box` | Array | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `0 0 0 1 0 0` |
| `emit_direction` | Array | The initial direction vector for emitted particles. | 1 | `0 1 0` |
| `emit_rate` | Number | The rate of particle emission per second. | 1 | `15` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `180` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `true` |
| `live_bounds` | Array | The bounds within which particles can exist. | 1 | `-999 999 -999 999 -999 999` |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `SparkleParticle` |
| `ownership` | String | The ownership scope for the effect, such as local to the caster. | 1 | `local` |
| `particle_lifetime` | Number | The duration in seconds particles remain alive. | 1 | `.5` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `separate` |
| [`scripts`](Miscellaneous.md#object-scripts) | Object | An object containing particle system scripts like forces or collisions. | 1 ||
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global` |
| `size_end` | Number | The size (scalar or 2D vector) of the effect at the end of its animation. | 1 | `.7` |
| `size_start` | Number | The starting size of particles. | 1 | `.5` |
| `speed_scale` | Number | A multiplier for particle speed. | 1 | `.50` |
| `speed_start` | Number | The initial speed of particles. | 1 | `1` |

</details>

### Object: `Shove`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `melee_attack` |

</details>

### Object: `SleepDart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `wp_SleepDart` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `"ITEM_SLEEPDART_DESC"` |
| `durability` | Number | The amount of durability consumed by this ability or required for its use. | 1 | `1` |
| `frame` | Number | The sprite frame index to display. | 1 | `151` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `weapon` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `"ITEM_SLEEPDART_NAME"` |

</details>

### Object: `SleepDart2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `wp_SleepDart` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `"ITEM_SLEEPDART_DESC"` |
| `durability` | Number | The amount of durability consumed by this ability or required for its use. | 1 | `2` |
| `frame` | Number | The sprite frame index to display. | 1 | `151` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `weapon` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `"ITEM_SLEEPDART_NAME"` |

</details>

### Object: `SmokeBuff`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_end` | Number | The alpha (opacity) value at the end of the effect's duration or animation. | 1 | `2` |
| `alpha_start` | Number | The alpha (opacity) value at the start of the effect's duration or animation. | 1 | `-1` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1` |
| `emit_box` | Array | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `0 0 0 1 0 0` |
| `emit_direction` | Array | The initial direction vector for emitted particles. | 1 | `0 1 0` |
| `emit_rate` | Number | The rate of particle emission per second. | 1 | `25` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `100` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `true` |
| `live_bounds` | Array | The bounds within which particles can exist. | 1 | `-999 999 -999 999 -999 999` |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `ParticleSmoke1` |
| `ownership` | String | The ownership scope for the effect, such as local to the caster. | 1 | `local` |
| `particle_lifetime` | Array | The duration in seconds particles remain alive. | 1 | `.5 1` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `separate` |
| [`scripts`](Miscellaneous.md#object-scripts) | Object | An object containing particle system scripts like forces or collisions. | 1 ||
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global` |
| `size_end` | Number | The size (scalar or 2D vector) of the effect at the end of its animation. | 1 | `0` |
| `size_start` | Array | The starting size of particles. | 1 | `1 1.4` |
| `speed_scale` | Number | A multiplier for particle speed. | 1 | `.25` |
| `speed_start` | Number | The initial speed of particles. | 1 | `.001` |

</details>

### Object: `Smough`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||

</details>

### Object: `SparkleBuff`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_end` | Number | The alpha (opacity) value at the end of the effect's duration or animation. | 1 | `2` |
| `alpha_start` | Number | The alpha (opacity) value at the start of the effect's duration or animation. | 1 | `-1` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1` |
| `emit_box` | Array | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `0 0 0 1 0 0` |
| `emit_direction` | Array | The initial direction vector for emitted particles. | 1 | `0 1 0` |
| `emit_rate` | Number | The rate of particle emission per second. | 1 | `50` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `180` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `true` |
| `live_bounds` | Array | The bounds within which particles can exist. | 1 | `-999 999 -999 999 -999 999` |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `SparkleParticle` |
| `ownership` | String | The ownership scope for the effect, such as local to the caster. | 1 | `local` |
| `particle_lifetime` | Array | The duration in seconds particles remain alive. | 1 | `.1 1` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `separate` |
| [`scripts`](Miscellaneous.md#object-scripts) | Object | An object containing particle system scripts like forces or collisions. | 1 ||
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global` |
| `size_end` | Number | The size (scalar or 2D vector) of the effect at the end of its animation. | 1 | `0` |
| `size_start` | Array | The starting size of particles. | 1 | `.4 .6` |
| `speed_scale` | Number | A multiplier for particle speed. | 1 | `1` |
| `speed_start` | Number | The initial speed of particles. | 1 | `.8` |

</details>

### Object: `SpiderReturn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `return` |

</details>

### Object: `SpikeBuff`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_end` | Number | The alpha (opacity) value at the end of the effect's duration or animation. | 1 | `2` |
| `alpha_start` | Number | The alpha (opacity) value at the start of the effect's duration or animation. | 1 | `1` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1` |
| `emit_box` | Array | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `0 0 0 1 0 0` |
| `emit_direction` | Array | The initial direction vector for emitted particles. | 1 | `0 1 0` |
| `emit_rate` | Number | The rate of particle emission per second. | 1 | `4` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `180` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `true` |
| `live_bounds` | Array | The bounds within which particles can exist. | 1 | `-999 999 -999 999 -999 999` |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `Particle_Thorns` |
| `ownership` | String | The ownership scope for the effect, such as local to the caster. | 1 | `local` |
| `particle_lifetime` | Number | The duration in seconds particles remain alive. | 1 | `.5` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `separate` |
| [`scripts`](Miscellaneous.md#object-scripts) | Object | An object containing particle system scripts like forces or collisions. | 1 ||
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global` |
| `size_end` | Number | The size (scalar or 2D vector) of the effect at the end of its animation. | 1 | `.5` |
| `size_start` | Number | The starting size of particles. | 1 | `.3` |
| `speed_scale` | Number | A multiplier for particle speed. | 1 | `.25` |
| `speed_start` | Number | The initial speed of particles. | 1 | `.5` |

</details>

### Object: `Spook`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `spell` |

</details>

### Object: `TC_DashReaction`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai_ability` | String | Specifies the ability to use as the AI's behavior for this ability. | 1 | `TC_DashReaction_AI` |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `trample_dash` |
| [`temporary_effects`](Abilities_and_Spells.md#object-temporary_effects) | Object | Applies temporary status effects on the caster upon using the ability. | 1 ||

</details>

### Object: `TT_Thrash`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `melee_attack` |

</details>

### Object: `TVOff`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `self_buff` |

</details>

### Object: `TattersFear`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `targeted_status` |

</details>

### Object: `TheCreator_SpawnCloneTeam`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`spawn`](Abilities_and_Spells.md#object-spawn) | Object | Defines what object or unit is spawned when the ability is used. | 1 ||
| `tags` | Array | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `summon` |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `spawn` |

</details>

### Object: `ThornUp`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `self_buff` |

</details>

### Object: `ThornUpX`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `self_buff` |

</details>

### Object: `ThrobbingKing2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||

</details>

### Object: `ToadJump_BasicMove`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `jump_attack` |

</details>

### Object: `TormentorRuneAbsorb`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `spell` |

</details>

### Object: `ToxPuff`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `self_buff` |

</details>

### Object: `ToxicBubbles`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1` |
| `emit_box` | Array | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `-.4 .4 0 0 -.4 .4` |
| `emit_direction` | Array | The initial direction vector for emitted particles. | 1 | `0 0 0` |
| `emit_rate` | Array | The rate of particle emission per second. | 1 | `.7 2` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `false` |
| `live_bounds` | Array | The bounds within which particles can exist. | 1 | `-999 999 0 999 -999 999` |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `ToxicBubbleParticle` |
| `particle_lifetime` | Number | The duration in seconds particles remain alive. | 1 | `1.5` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `separate` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global` |
| `size_start` | Array | The starting size of particles. | 1 | `.5 1` |
| `speed_start` | Number | The initial speed of particles. | 1 | `0` |

</details>

### Object: `TrexSwitchTarget`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `targeted_status` |

</details>

### Object: `UFO_BigExplode`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `spell` |

</details>

### Object: `UltraSmough`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | A container object defining the character's artificial intelligence brain and decision weights. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||

</details>

### Object: `Wood`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `"SETBONUS_WOOD_DESC"` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `"SETBONUS_WOOD_NAME"` |
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| `pieces_required` | Number | The number of scrap pieces required to craft this item. | 1 | `3` |

</details>

### Object: `cWaggle`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Waggle` |

</details>

### Object: `cWaggle2x2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | A container object defining a character's move, attack, and spell abilities. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `cWaggle` |

</details>

### Object: `cWaggle3x3`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `cWaggle2x2` |

</details>

### Object: `face_EatNeverstone`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bonus_passives`](Abilities_and_Spells.md#object-bonus_passives) | Object | Grants temporary passive abilities to the caster for the duration of the ability. | 1 ||
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `self_buff` |

</details>

### Object: `face_LeechBrood`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `lobbed_attack` |

</details>

### Object: `neck_NukeBonus`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bonus_passives`](Abilities_and_Spells.md#object-bonus_passives) | Object | Grants temporary passive abilities to the caster for the duration of the ability. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Contains metadata for the ability including name, description, class, and type icon. | 1 ||
| `sub_ability` | String | Specifies a sub-ability that is part of this ability, often used for multi-part abilities. | 1 | `neck_NukeExplode` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `self_buff` |

</details>

### Object: `neck_NukeExplode`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bonus_passives`](Abilities_and_Spells.md#object-bonus_passives) | Object | Grants temporary passive abilities to the caster for the duration of the ability. | 1 ||
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Defines the resource cost (e.g., mana) and other casting requirements. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Defines damage properties, effects, and healing for the ability's direct damage. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 ||
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Object | Defines damage or effects applied to the caster when using the ability. | 1 ||
| [`splash_damage`](Abilities_and_Spells.md#object-splash_damage) | Object | Defines additional damage or effects applied to nearby targets around the primary target. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `spell` |

</details>

### Object: `pyrophina`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BOSS_PYROPHINA_QUOTE_1` | String | Localization key for the first boss quote for Pyrophina. | 1 ||
| `BOSS_PYROPHINA_QUOTE_2` | String | Localization key for the second boss quote for Pyrophina. | 1 ||
| `act` | Number | The act number (game progression stage) in which this encounter or script takes place. | 1 | `2` |
| `arrival_unlock` | String | The name of the cutscene or event that is unlocked upon arrival. | 1 | `npc_houseboss_intro_pyrophina` |
| `frame_label` | String | Specifies the frame or cutscene animation label for the boss encounter. | 1 | `pyrophina` |
| `index` | Number | The index used to order or identify this encounter within its list. | 1 | `1` |
| `initial_cooldown` | Array | A list of possible initial cooldown values (in turns) before the encounter can trigger. | 1 | `0` |
| `initial_cutscene_day` | String | The name of the cutscene that plays on the first day the encounter appears. | 1 | `pyro_intro` |
| `lead_time` | Number | The number of turns before the event activates. | 1 | `7` |
| `level` | String | The level or quest identifier to load. | 1 | `"house_bosses/pyrophina.lvl"` |
| `music` | String | Specifies the name of the music track to play during the encounter. | 1 | `kaiju` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `BOSS_PYROPHINA_NAME` |
| `quotes` | Array | An array of dialogue quotes for the boss cutscene. | 1 ||
| `rematch_cooldown` | Array | The minimum and maximum number of days before a rematch becomes available. | 1 | `3 7` |
| `rematch_cutscene_day` | String | Specifies the cutscene to play on the day of the rematch. | 1 | `house_boss_returns_pyro` |
| `savefile_string` | String | A unique string identifier used to track the save file associated with this encounter. | 1 | `"SAVE_FILE_FIGHT_HOUSEBOSS_PYR` |

</details>

### Object: `set_WitchJump`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 ||
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `BasicJump` |

</details>

### Object: `zaratana`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BOSS_ZARATANA_QUOTE_1` | String | A string for the first quote spoken by the boss Zara Tana. | 1 ||
| `BOSS_ZARATANA_QUOTE_2` | String | A string for the second quote spoken by the boss Zara Tana. | 1 ||
| `act` | Number | The act number (game progression stage) in which this encounter or script takes place. | 1 | `2` |
| `arrival_unlock` | String | The name of the cutscene or event that is unlocked upon arrival. | 1 | `npc_houseboss_intro_zaratana` |
| `frame_label` | String | Specifies the frame or cutscene animation label for the boss encounter. | 1 | `zaratana` |
| `index` | Number | The index used to order or identify this encounter within its list. | 1 | `2` |
| `initial_cooldown` | Array | A list of possible initial cooldown values (in turns) before the encounter can trigger. | 1 | `0` |
| `initial_cutscene_day` | String | The name of the cutscene that plays on the first day the encounter appears. | 1 | `moonboss_intro` |
| `lead_time` | Number | The number of turns before the event activates. | 1 | `7` |
| `level` | String | The level or quest identifier to load. | 1 | `"house_bosses/zaratana.lvl"` |
| `music` | String | Specifies the name of the music track to play during the encounter. | 1 | `kaiju` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `BOSS_ZARATANA_NAME` |
| `quotes` | Array | An array of dialogue quotes for the boss cutscene. | 1 ||
| `rematch_cooldown` | Array | The minimum and maximum number of days before a rematch becomes available. | 1 | `3 7` |
| `rematch_cutscene_day` | String | Specifies the cutscene to play on the day of the rematch. | 1 | `house_boss_returns_zara` |
| `savefile_string` | String | A unique string identifier used to track the save file associated with this encounter. | 1 | `"SAVE_FILE_FIGHT_HOUSEBOSS_ZAR` |

</details>
