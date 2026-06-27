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
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 5118 | `{ . . . }` |
| [`class`](./Enums.md#enum-class) | Enum | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1200 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 981 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 928 | `{ . . . }` |
| [`int`](./Enums.md#enum-int) | Enum / Integer  | The Intelligence stat value or modifier. | 401 | `-1`<br>`-10`<br>`-2` |
| [`neck`](./Enums.md#enum-neck) | Enum | The neck equipment item assigned to the unit. | 378 | `AngelicAura`<br>`AngelicAura_Terminator`<br>`DruidNeck` |
| [`lck`](./Enums.md#enum-lck) | Enum / Integer  | The Luck stat value or modifier. | 351 | `-1`<br>`-2`<br>`-3` |
| [`bonus_passives`](./Miscellaneous.md#object-bonus_passives) | Object  | Grants temporary passive abilities to the caster for the duration of the ability. | 272 | `{ . . . }` |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack) | Object  | Contains status effects to add to the basic attack. | 178 | `{ . . . }` |
| [`Colorless`](./Engine_LogicKeys.md#object-colorless) | Object  | Specifies the 'Colorless' form within FormChanger, used for boss dialogue. | 140 | `{ . . . }` |
| `consumable` | Boolean | If true, the item is consumed on use. Can also specify a number of uses or an item pool. | 140 | `1`<br>`2`<br>`true` |
| [`move`](./Enums.md#enum-move) | Enum  | Specifies the name of the class's default movement ability. | 122 | `BasicJump`<br>`BungaJumpMove`<br>`DefaultMove` |
| [`FormChanger`](./Passives_and_Statuses.md#object-formchanger) | Object  | Defines the unit's form-changing data, including multiple form definitions and their sub-properties. | 106 | `{ . . . }` |
| [`SpawnOnDeath`](./Passives_and_Statuses.md#object-spawnondeath) | Enum / Object  | Specifies an object and its faction to spawn when the unit dies. | 81 | `{ . . . }`<br>`Antidote`<br>`BiggestFood`<br>`FrankPinky` |
| `IgnoreSelf` | Boolean / Integer | If set to 1 or true, the damage instance ignores the source unit (does not affect itself). | 75 | `1`<br>`true` |
| [`Tinkerer`](./Engine_LogicKeys.md#object-tinkerer) | Object  | Form identifier for the Tinkerer boss type. | 70 | `{ . . . }` |
| [`Hunter`](./Engine_LogicKeys.md#object-hunter) | Object  | Defines a list of quotes for the Hunter class (vs boss, embark, return early). | 68 | `{ . . . }` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 59 | `1`<br>`10`<br>`2` |
| [`Medic`](./Engine_LogicKeys.md#object-medic) | Object  | Defines a list of quotes for the Medic class. | 58 | `{ . . . }` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 54 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`RandomArmorPickup`](./Engine_LogicKeys.md#object-randomarmorpickup) | Number / Object  | The amount of random armor pickups spawned. | 43 | `{ . . . }`<br>`4.5`<br>`40` |
| [`BasicMelee`](./Engine_StatusAndPassiveKeys.md#object-basicmelee) | Object  | An object defining properties for a basic melee attack passive. | 42 | `{ . . . }` |
| [`StatusImmunity`](./Arrays.md#array-statusimmunity) | Array / Enum  | A list of status effect names the unit is immune to. | 38 | `Burn`<br>`Poison`<br>`Tarred` |
| [`Wood`](#object-wood) | Variable | A variable representing the Wood element or material type. | 38 ||
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 36 | `1`<br>`10`<br>`100` |
| `HealthGain` | Integer | The amount of health restored to the source. | 36 | `1`<br>`10`<br>`2` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 36 | `1`<br>`2`<br>`3` |
| [`FormChangeWhileHasStatus`](./Passives_and_Statuses.md#object-formchangewhilehasstatus) | Object  | Defines a form change condition that activates while the unit has a specific status effect. | 35 | `{ . . . }` |
| [`StatusOnTookDamage`](./Passives_and_Statuses.md#object-statusontookdamage) | Object  | Specifies status effects or actions triggered when the unit takes damage. | 34 | `{ . . . }` |
| [`AddElementsToBasicAttack`](./Enums.md#enum-addelementstobasicattack) | Enum | Specifies an elemental damage type that is added to the unit's basic attacks. | 32 | `Electric`<br>`Fire`<br>`Gravity` |
| [`Jester`](./Arrays.md#array-jester) | Array | An array of dialogue quotes for the Jester class. | 32 | `[` |
| [`MulticlassLevelUp`](./Enums.md#enum-multiclasslevelup) | Enum | Specifies the class that this unit gains a level in when multiclassing. | 32 | `Butcher`<br>`Druid`<br>`Fighter` |
| [`AddPassivesToMinions`](./Passives_and_Statuses.md#object-addpassivestominions) | Object  | An object containing passives that are granted to all minions spawned by the unit. | 30 | `{ . . . }` |
| `Charge` | Integer | The number of charge stacks applied. | 30 | `1`<br>`2`<br>`3` |
| `DodgeChance` | Integer | The percentage chance the unit has to dodge incoming attacks. | 30 | `10%`<br>`15%`<br>`2%` |
| [`EliteTint`](./Arrays.md#array-elitetint) | Array | An RGBA tint color (r g b a) applied to elite variants of a unit. | 30 | `[.3 .25 .3 .75]`<br>`[.4 .4 .4]`<br>`[.5 .5 .8 1]` |
| [`RevengeDamage`](./Passives_and_Statuses.md#object-revengedamage) | Object  | An object defining the damage and effects that trigger when the unit is attacked. | 30 | `{ . . . }` |
| `AddCritMultiplier` | Integer | The percentage added to the critical hit damage multiplier. | 28 | `100%`<br>`125%`<br>`150%` |
| [`TransformAbility`](./Enums.md#enum-transformability) | Enum | Specifies the ability that replaces the current ability. | 28 | `BerserkDash`<br>`BerserkDash2`<br>`BirthSquirrel` |
| [`knockback`](./Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 27 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| `AddBonusRange` | Integer | The number of additional tiles of range added to the unit's abilities. | 26 | `1`<br>`10`<br>`2` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 | `1`<br>`2`<br>`3` |
| [`ImmediateAbilityReaction`](./Passives_and_Statuses.md#object-immediateabilityreaction) | Array / Enum / Object  | Specifies an ability or list of abilities used immediately in reaction to a triggering event. | 26 | `{ . . . }`<br>`BirthwortReactionShot`<br>`BumbleButt`<br>`CatGoop` |
| `Knockback` | Integer | The number of tiles the target is pushed away from the source on hit. | 26 | `1`<br>`10`<br>`2` |
| [`Paper`](#object-paper) | Variable | A variable representing the Paper element or material type. | 26 ||
| `even_if_dead` | Boolean | If true, the effect triggers even if the unit is dead. | 25 | `true` |
| `Undead` | Integer | If set, flags the unit as undead (e.g., 1) with associated mechanics. | 25 | `1` |
| `Brittle` | Integer | The number of stacks of the Brittle status, or an object defining its properties. | 24 | `1` |
| `MissChance` | Integer | The flat percentage chance that the unit's attacks will miss. | 24 | `10`<br>`15`<br>`20` |
| [`party_status_next_fight`](./Miscellaneous.md#object-party_status_next_fight) | Object  | An object defining status effects to apply to the party at the start of the next fight. | 24 | `{ . . . }` |
| [`PassiveWhenAffectedByElement`](./Passives_and_Statuses.md#object-passivewhenaffectedbyelement) | Object  | An object containing `element` and `passives` that grants the listed passives while the unit is affected by the specified element. | 24 | `{ . . . }` |
| [`SpawnOnBattleStart`](./Passives_and_Statuses.md#object-spawnonbattlestart) | Enum / Object  | Specifies the object that spawns adjacent to the unit at the start of battle. | 24 | `{ . . . }`<br>`BeefyCharmedLeech`<br>`BuffCharmedKitten`<br>`CharmedCultist` |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 23 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 22 | `1`<br>`2`<br>`4` |
| [`mode`](./Enums.md#enum-mode) | Enum | Specifies the comparison mode (equal, greater, less_or_equal, etc.) used for a conditional check. | 22 | `equal`<br>`greater`<br>`greater_or_equal` |
| [`StatusOnBreak`](./Passives_and_Statuses.md#object-statusonbreak) | Object  | An object defining statuses or effects applied when an item or object breaks. | 22 | `{ . . . }` |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Enum / Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 22 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| [`additional_passives`](./Miscellaneous.md#object-additional_passives) | Object  | Additional passive abilities applied to the spawned unit. | 20 | `{ . . . }` |
| [`BossRewards`](./Passives_and_Statuses.md#object-bossrewards) | Object  | Defines the common and rare item rewards dropped by a boss on defeat. | 20 | `{ . . . }` |
| [`Brace`](./Passives_and_Statuses.md#object-brace) | Enum / Integer / Object  | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 20 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 20 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`MeleeRevengeDamage`](./Passives_and_Statuses.md#object-meleerevengedamage) | Object  | Defines the damage and effects applied back to a melee attacker upon being hit. | 20 | `{ . . . }` |
| [`EliteParticle`](./Enums.md#enum-eliteparticle) | Enum | Specifies the particle effect name attached to an elite unit. | 19 | `AbsorbBuff`<br>`FireExtinguish_Steam`<br>`FlyBuff` |
| [`FindItemFromPool`](./Passives_and_Statuses.md#object-finditemfrompool) | Enum / Object  | Specifies the loot pool from which to find an item, with an optional chance. | 19 | `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`BirdRewards`](./Passives_and_Statuses.md#object-birdrewards) | Object  | Defines the rewards and statuses applied when a bird allies with the unit. | 18 | `{ . . . }` |
| [`Buddy`](./Passives_and_Statuses.md#object-buddy) | Enum / Object  | Specifies a buddy unit that accompanies or is spawned alongside the unit, with optional reclaim and targeting properties. | 18 | `{ . . . }`<br>`BoyDino`<br>`CaveCatDad`<br>`Chubs` |
| [`Coin`](./Engine_LogicKeys.md#object-coin) | Integer / Object  | The number of coin pickups spawned. | 18 | `{ . . . }`<br>`1`<br>`70` |
| [`Consumed`](./Passives_and_Statuses.md#object-consumed) | Object  | An object configuring how the target is consumed (e.g., via swallow), with fields like `instant`, `wet`, `force_contact`, and `struggle_ability`. | 18 | `{ . . . }` |
| [`SpawnThingOnDamage`](./Passives_and_Statuses.md#object-spawnthingondamage) | Object  | Specifies an object that spawns on the tile when the unit takes damage. | 18 | `{ . . . }` |
| [`StatusOnKill`](./Passives_and_Statuses.md#object-statusonkill) | Object  | Specifies status effects or actions triggered when the unit kills an enemy. | 18 | `{ . . . }` |
| [`AbilityOnBattleStart_Immediate`](./Enums.md#enum-abilityonbattlestart_immediate) | Enum | Specifies the ability triggered instantly at the start of battle. | 17 | `BrambleRandomTileEvent`<br>`FlowerEventSleep`<br>`Flush` |
| `CollectsPickups` | Integer | If set to 1 or greater, the unit collects pickups (e.g., items) on contact. | 17 | `1`<br>`2` |
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 17 | `{ . . . }` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 17 | `-1`<br>`-2`<br>`-4` |
| [`OverrideKnockbackDamage`](./Enums.md#enum-overrideknockbackdamage) | Enum / Integer | A formula or flat value that sets the damage dealt when knockback occurs, overriding default calculations. | 17 | `"max(5+bonus_melee_ability_damage, 1)"`<br>`0`<br>`2` |
| [`RandomMagicMissile`](./Miscellaneous.md#object-randommagicmissile) | Integer / Object  | The number of random magic missiles fired, or an object defining its properties. | 17 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| `rat` | Variable | A variable representing the Rat element or material type. | 17 ||
| [`AddStatusToBasicMeleeAttack`](./Passives_and_Statuses.md#object-addstatustobasicmeleeattack) | Object  | An object listing status effects applied by the unit's basic melee attack. | 16 | `{ . . . }` |
| [`CharacterLightSource`](./Passives_and_Statuses.md#object-characterlightsource) | Object  | Defines a dynamic light source attached to the unit, including color, glow, and size. | 16 | `{ . . . }` |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 16 | `Creep`<br>`Electric`<br>`Fire` |
| [`HealthPickup`](./Passives_and_Statuses.md#object-healthpickup) | Object  | Defines properties for a health pickup object, such as healing amount and visual frame range. | 16 | `{ . . . }` |
| `less_or_equal` | Variable | A variable representing a comparison mode for threshold checks (less than or equal). | 16 ||
| `PassiveLevelUpAtCombatEnd` | Integer | The number of times a passive levels up automatically when combat ends. | 16 | `1` |
| [`pyrophina`](#object-pyrophina) | Variable | A variable representing the Pyrophina element or material type. | 16 ||
| [`StatusEachTurnBegin`](./Passives_and_Statuses.md#object-statuseachturnbegin) | Object  | Specifies status effects applied to the unit at the start of each of its turns. | 16 | `{ . . . }` |
| [`StatusEachTurnEnd`](./Passives_and_Statuses.md#object-statuseachturnend) | Object  | Specifies status effects applied to the unit at the end of each of its turns. | 16 | `{ . . . }` |
| [`zaratana`](#object-zaratana) | Variable | A variable representing the Zaratana element or material type. | 16 ||
| [`ApplyToSourceOnKill`](./Miscellaneous.md#object-applytosourceonkill) | Object  | Contains effects that are applied to the source when it kills the target. | 15 | `{ . . . }` |
| [`CanApplyToInanimate`](./Miscellaneous.md#object-canapplytoinanimate) | Object  | An object containing effects that can be applied to inanimate objects. | 15 | `{ . . . }` |
| `HealthMultiplier` | Float | A multiplier applied to the unit's base health. | 15 | `.5`<br>`.8`<br>`1.5` |
| [`Maggot`](./Engine_StatusAndPassiveKeys.md#object-maggot) | Object  | An object defining properties for the Maggot passive or status. | 15 | `{ . . . }` |
| [`ReplaceSpawnedObjects`](./Arrays.md#array-replacespawnedobjects) | Array | An array of [original_object replacement_object] pairs for swapping spawned objects. | 15 | `[Boulder AnimatedBoulder]`<br>`[Boulder AnimatedLavaBoulder]`<br>`[Crow Crow2]` |
| [`ChangeCatClass`](./Enums.md#enum-changecatclass) | Enum | Specifies the new class to assign to the unit. | 14 | `Butcher`<br>`Colorless`<br>`Druid` |
| `EndTurn` | Integer | If set to 1, ends the current unit's turn immediately after this effect. | 14 | `1` |
| `meat` | Variable | A variable representing the Meat element or material type. | 14 ||
| [`PassiveGroup`](./Passives_and_Statuses.md#object-passivegroup) | Object  | A group of passive abilities that can be randomly assigned. | 14 | `{ . . . }` |
| [`SpawnOnDowned`](./Enums.md#enum-spawnondowned) | Enum | Specifies the character or object spawned when the unit is downed. | 14 | `CharmedFly`<br>`CharmedKitten`<br>`CharmedSpookie` |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 14 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`statuses`](./Passives_and_Statuses.md#object-statuses) | Object  | Defines the status effects applied when the parent trigger event occurs. | 14 | `{ . . . }` |
| [`Trample`](./Arrays.md#array-trample) | Integer | The amount of bonus damage dealt when moving through an enemy. | 14 | `1`<br>`3`<br>`4` |
| [`TransformBasicAttack`](./Enums.md#enum-transformbasicattack) | Enum | Specifies the ability that replaces the unit's basic attack. | 14 | `AntlerSwipe`<br>`AntlerSwipe2`<br>`Chitter` |
| [`ApplyPassives`](./Miscellaneous.md#object-applypassives) | Object  | Specifies the passives or status effects to apply to the unit. | 13 | `{ . . . }` |
| [`DeathRattleRevive`](./Passives_and_Statuses.md#object-deathrattlerevive) | Enum / Object  | Specifies an ability or effect that revives the unit upon death, with options for stunning behavior. | 13 | `{ . . . }`<br>`DoNothing`<br>`HCHumanDie`<br>`ToxPuff` |
| `Flammable` | Integer | The number of stacks of Flammable, or an object defining its properties. | 13 | `1`<br>`2` |
| [`SafeDoomed`](./Enums.md#enum-safedoomed) | Enum / Integer  | The number of SafeDoomed stacks applied, or 'level' to scale with character level. | 13 | `1`<br>`2`<br>`level` |
| [`TransformOnDeath`](./Arrays.md#array-transformondeath) | Array / Enum  | Specifies the unit or list of units to transform into upon death. | 13 | `BishopHat`<br>`CanCreeperOut`<br>`Carcus` |
| `AddBonusMeleeRange` | Integer | The number of additional tiles of range added to the unit's melee attacks. | 12 | `1`<br>`10`<br>`2` |
| `AddCorpseHealth` | Integer | The amount of bonus health the unit's corpse has before it can be resurrected. | 12 | `-999`<br>`-999999`<br>`100` |
| `AddMaxHealth` | Integer | The amount added to the unit's maximum health. Negative values reduce max health. | 12 | `-25`<br>`10`<br>`2` |
| [`Bionic`](#object-bionic) | Variable | A variable representing the Bionic element or material type. | 12 ||
| [`BonusAbility`](./Enums.md#enum-bonusability) | Enum | Specifies the name of a bonus ability granted. | 12 | `Bloodzerk`<br>`BonusToss`<br>`BonusToss2` |
| [`CritsApplyStatus`](./Passives_and_Statuses.md#object-critsapplystatus) | Object  | An object containing statuses applied to the target when the unit lands a critical hit. | 12 | `{ . . . }` |
| [`DeadAltAbility`](./Enums.md#enum-deadaltability) | Enum | Specifies an alternative ability used when the unit is dead. | 12 | `CarrionShot_Afterlife`<br>`CarrionShot_Afterlife2`<br>`CoffinFlop_Afterlife` |
| `Displace` | Integer | If set to 1, the unit is displaced to another location (e.g., teleport). | 12 | `1` |
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 12 | `[`<br>`[Heat Fire]` |
| [`EquipTemporaryItem`](./Enums.md#enum-equiptemporaryitem) | Enum | Specifies which temporary item is equipped. | 12 | `Bottles`<br>`ButcherHook_Temporary`<br>`FoodBig` |
| `IgnoreTiles` | Integer | If set to 1, movement ignores tile-based penalties or restrictions. | 12 | `1` |
| `NoHealthOnlyShield` | Integer | If set (e.g., 1), the unit has no health and only a shield for damage absorption. | 12 | `1` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 12 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| [`SpawnEachTurn`](./Passives_and_Statuses.md#object-spawneachturn) | Object  | Specifies an object that spawns on a random adjacent tile each turn, with optional chance. | 12 | `{ . . . }` |
| [`ChanceToBreakFree`](./Miscellaneous.md#object-chancetobreakfree) | Object  | Defines the chance and ability used for a grappled or restrained unit to break free. | 11 | `{ . . . }` |
| [`DoScreenShake`](./Miscellaneous.md#object-doscreenshake) | Integer / Object  | If an integer, the number of screen shakes; if an object, defines the duration and intensity of the screen shake. | 11 | `{ . . . }`<br>`1` |
| [`EliteFlatTint`](./Arrays.md#array-eliteflattint) | Array | An RGB or RGBA tint multiplier applied uniformly to an elite unit's sprite. | 11 | `[.05 .05 .05 .75]`<br>`[.6 1 1]`<br>`[1.1 1.1 1.1]` |
| [`Food`](./Shops.md#object-food) | Integer / Object  | The number of food pickups spawned. | 11 | `{ . . . }`<br>`20` |
| `PermanentMadness` | Integer | The number of permanent madness stacks applied. | 11 | `1` |
| [`BoostWeaponDamage`](./Passives_and_Statuses.md#object-boostweapondamage) | Object  | The amount of bonus weapon damage applied, or an object with `damage` and `crit_chance` fields. | 10 | `{ . . . }` |
| [`BrambleRandomTileEvent`](./Engine_StatusAndPassiveKeys.md#object-bramblerandomtileevent) | Object  | An object defining the BrambleRandomTileEvent ability or effect. | 10 | `{ . . . }` |
| `CoinPickup` | Integer | The amount of coins awarded when this pickup is collected. | 10 | `1`<br>`10`<br>`2` |
| `ExtraMovePoints` | Integer | The number of additional movement points granted to this unit. | 10 | `1` |
| `FadeInsteadOfDie` | Integer | If non-zero, the unit fades out instead of dying. | 10 | `1` |
| [`GainCoins`](./Arrays.md#array-gaincoins) | Array / Integer | The amount of coins gained, or a [min, max] range. | 10 | `-5`<br>`1`<br>`2` |
| `KnockbackDamageImmuneUntilSettled` | Integer | If non-zero, makes the target immune to damage from knockback until they stop moving. | 10 | `1` |
| `PartialPurge` | Integer | The amount of beneficial status effects removed from the target. | 10 | `1` |
| [`PassiveAtStatThreshold`](./Passives_and_Statuses.md#object-passiveatstatthreshold) | Object  | An object defining passives granted when a unit's stat meets a specified threshold. | 10 | `{ . . . }` |
| [`Quivered`](./Arrays.md#array-quivered) | Array / Integer | The amount of quivered stacks applied, or an [stacks, probability] array. | 10 | `1`<br>`2`<br>`5` |
| `RandomPermanentStat` | Integer | The amount of a random permanent stat change (positive or negative). | 10 | `-1`<br>`-2`<br>`-3` |
| [`ReplaceBasicMove`](./Enums.md#enum-replacebasicmove) | Enum | Specifies an alternative movement ability that replaces the unit's default move. | 10 | `BasicDashAttackMove`<br>`BasicJump`<br>`BellyFlop_BasicMove` |
| [`SpawnOnBattleStartRandomEmptyTile`](./Passives_and_Statuses.md#object-spawnonbattlestartrandomemptytile) | Object  | Specifies an object that spawns on a random empty tile at the start of battle. | 10 | `{ . . . }` |
| [`StatusOnCrit`](./Passives_and_Statuses.md#object-statusoncrit) | Object  | An object containing statuses applied to the unit when it lands a critical hit. | 10 | `{ . . . }` |
| `StripStatuses` | Integer | If 1, removes all status effects from the unit at the beginning of its turn. | 10 | `1` |
| `WaterWalk` | Integer | If greater than 0, allows the unit to traverse water tiles as if they were ground. | 10 | `1` |
| `Ammo` | Integer | The amount of ammo to add or remove (negative values subtract). | 9 | `-1`<br>`-99999`<br>`1` |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `1`<br>`10`<br>`2` |
| `Creep` | Variable | A variable representing the Creep element or material type. | 9 ||
| `DeferVaporize` | Integer | If set to 1, the unit's vaporize (instant death) is delayed until the end of the current action. | 9 | `1` |
| `DiminishingHealthRegen` | Integer | The number of diminishing health regen stacks applied. | 9 | `1`<br>`2`<br>`3` |
| [`FormChangeOnElementInfluence`](./Passives_and_Statuses.md#object-formchangeonelementinfluence) | Object  | Defines the element that triggers a form change, optional visual effects, and the target form. | 9 | `{ . . . }` |
| `Plant` | Integer | If set to 1, marks the unit as a Plant type, granting associated immunities and interactions. | 9 | `1` |
| `RandomMutation` | Integer | The number of random mutations to apply. | 9 | `1`<br>`3` |
| [`Rot`](./Arrays.md#array-rot) | Array / Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 9 | `-999999`<br>`1`<br>`2` |
| [`SmallRockBehavior`](./Passives_and_Statuses.md#object-smallrockbehavior) | Integer / Object  | Defines the damage, knockback, and chain properties of small rocks spawned from this unit when destroyed. | 9 | `{ . . . }`<br>`0`<br>`5` |
| `SpawnCreep` | Integer | If set to 1, spawns a creep tile under the target. | 9 | `1` |
| `SpellDamageUp` | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. | 9 | `1`<br>`3` |
| [`StatusCollector`](./Passives_and_Statuses.md#object-statuscollector) | Object  | Specifies the status effects and their stack counts that the unit collects to trigger transformations. | 9 | `{ . . . }` |
| [`TransformInXTurns`](./Passives_and_Statuses.md#object-transforminxturns) | Object  | Defines a delayed transformation after a set number of turns, with optional target object and initiative handling. | 9 | `{ . . . }` |
| [`TransformOnElementInfluence`](./Passives_and_Statuses.md#object-transformonelementinfluence) | Object  | Defines the element that triggers a transformation and the object to transform into. | 9 | `{ . . . }` |
| `AddKnockbackDamage` | Integer | The amount of additional knockback damage applied. | 8 | `1`<br>`2`<br>`3` |
| `AddLevelUpRerolls` | Integer | The number of additional rerolls the unit gets when leveling up. | 8 | `1`<br>`2`<br>`3` |
| [`AddStatusToWeapons`](./Passives_and_Statuses.md#object-addstatustoweapons) | Object  | Specifies status effects to add to the unit's weapon attacks, with their stack counts. | 8 | `{ . . . }` |
| `AlphaTurns` | Integer | The number of turns the unit acts first in battle; negative values may indicate last. | 8 | `-1`<br>`1` |
| [`AmplifyStatus`](./Enums.md#enum-amplifystatus) | Enum | Specifies the status effect to amplify, or an object with the status and number of stacks to add. | 8 | `Bleed`<br>`Burn`<br>`Poison` |
| [`BasicMagicMissile`](./Engine_StatusAndPassiveKeys.md#object-basicmagicmissile) | Object  | Directs a basic magic missile projectile at the target. | 8 | `{ . . . }` |
| [`BlacklistPickupType`](./Enums.md#enum-blacklistpickuptype) | Enum | Specifies a pickup type (e.g., food, catnip) that the unit will refuse to pick up. | 8 | `catnip`<br>`food` |
| `BleedThorns` | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 8 | `1`<br>`2`<br>`3` |
| [`CharmedFly`](./Engine_StatusAndPassiveKeys.md#object-charmedfly) | Object  | Transforms the unit into a charmed fly that fights for the allies faction. | 8 | `{ . . . }` |
| [`DisableAbilitiesWithTag`](./Enums.md#enum-disableabilitieswithtag) | Enum | Specifies a tag that disables any ability with that tag on the unit. | 8 | `consumable`<br>`meat`<br>`musical` |
| `ExtraWeaponAttacks` | Integer | The number of additional weapon attacks the unit can perform. | 8 | `1`<br>`2` |
| [`ForceSpecificInjury`](./Enums.md#enum-forcespecificinjury) | Enum | Forces the unit to receive an injury to the specified stat. | 8 | `cha`<br>`int`<br>`lck` |
| [`FormChangeOffMap`](./Passives_and_Statuses.md#object-formchangeoffmap) | Object  | Specifies the unit's form when off the map and when on the map. | 8 | `{ . . . }` |
| [`Grappled`](./Arrays.md#array-grappled) | Array / Integer | The number of stacks and probability of applying the Grappled status, in format [stacks, probability] or just stacks. | 8 | `1`<br>`[1, .50]`<br>`[1, .75]` |
| [`InnateElement`](./Enums.md#enum-innateelement) | Enum | Specifies the innate elemental type of the unit (e.g., Fire, Ice, Electric). | 8 | `Earth`<br>`Electric`<br>`Fire` |
| `Lucky` | Enum | Indicates the unit's luck modifier or classification. | 8 ||
| [`ManaCostReductionTagged`](./Passives_and_Statuses.md#object-manacostreductiontagged) | Object  | Reduces the mana cost of abilities with the specified tag by the given reduction amount. | 8 | `{ . . . }` |
| `NonStackingDivineShield` | Integer | The number of Divine Shield stacks that do not stack with duplicates. | 8 | `1` |
| `NonStackingShield` | Integer | The amount of non-stacking shield granted. | 8 | `12`<br>`16`<br>`3` |
| [`PassiveIfAllArmorEmpty`](./Passives_and_Statuses.md#object-passiveifallarmorempty) | Object  | Grants the contained passive effects when no armor is equipped in any slot. | 8 | `{ . . . }` |
| [`PassiveIfEmptyFace`](./Passives_and_Statuses.md#object-passiveifemptyface) | Object  | Grants the contained passive effects when the face armor slot is empty. | 8 | `{ . . . }` |
| [`PassiveIfEmptyHead`](./Passives_and_Statuses.md#object-passiveifemptyhead) | Object  | Grants the contained passive effects when the head armor slot is empty. | 8 | `{ . . . }` |
| [`PassiveIfEmptyNeck`](./Passives_and_Statuses.md#object-passiveifemptyneck) | Object  | Grants the contained passive effects when the neck armor slot is empty. | 8 | `{ . . . }` |
| [`Poison`](./Arrays.md#array-poison) | Array / Integer | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 | `1`<br>`10`<br>`2` |
| [`RandomizeAIWeightsEachTurn`](./Arrays.md#array-randomizeaiweightseachturn) | Array | The range of random weights applied to AI actions each turn. | 8 | `[` |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 8 | `{ . . . }` |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum | Specifies the ability ID that replaces the unit's basic attack. | 8 | `BasicButcherMeleeWideDoubleSpin`<br>`BasicButcherMeleeWideSpin`<br>`BasicDruidAbilityVersatile` |
| [`StatusAlliesOnDeath`](./Passives_and_Statuses.md#object-statusalliesondeath) | Object  | Applies the contained status effects to all allies when the unit dies. | 8 | `{ . . . }` |
| [`StatusEachRoundBegin`](./Passives_and_Statuses.md#object-statuseachroundbegin) | Object  | Applies the contained status effects at the beginning of each round. | 8 | `{ . . . }` |
| [`StatusEveryXSpellCasts`](./Passives_and_Statuses.md#object-statuseveryxspellcasts) | Object  | An object with `stacks` (number of spell casts) and status effects to apply after that many spell casts. | 8 | `{ . . . }` |
| [`StatusOnCastSpell`](./Passives_and_Statuses.md#object-statusoncastspell) | Object  | An object listing status effects applied to the unit whenever it casts a spell. | 8 | `{ . . . }` |
| [`StatusOnUseAbilityWithTag`](./Passives_and_Statuses.md#object-statusonuseabilitywithtag) | Object  | Applies the contained status effects when the unit uses an ability with the specified tag. | 8 | `{ . . . }` |
| `AbilityEnabledOncePerFightAtHealthThreshold` | Integer | The health threshold (absolute or percentage) at which this ability becomes enabled once per fight. | 7 | `16`<br>`25%`<br>`50%` |
| [`AbilityWhenBuddyDies`](./Enums.md#enum-abilitywhenbuddydies) | Enum | Specifies the ability to cast when a nearby allied unit dies. | 7 | `BoyDinoCry`<br>`ChubsRage`<br>`GirlDinoCry` |
| `BramblesOnHit` | Integer | If set to 1, spawns bramble tiles on the target's location on hit. | 7 | `1` |
| [`BrittleDuringElement`](./Enums.md#enum-brittleduringelement) | Enum | Makes the unit brittle while in contact with the specified element. | 7 | `water` |
| [`ChanceToSpitOnDamage`](./Passives_and_Statuses.md#object-chancetospitondamage) | Object  | Configures the chance to use a spit ability when taking damage, including base chance and per-damage bonus. | 7 | `{ . . . }` |
| `CharismaUp` | Enum / Integer | The amount of charisma change, or a keyword like 'item_aux'. | 7 | `-1`<br>`-2`<br>`1` |
| `ContextualHeal` | Integer | The amount of healing applied contextually (e.g., to allies). | 7 | `1` |
| [`DamageNeighborsOnEndMove`](./Passives_and_Statuses.md#object-damageneighborsonendmove) | Object  | Deals damage and knockback to units on neighboring tiles when the unit finishes moving. | 7 | `{ . . . }` |
| [`DurabilityTransform`](./Passives_and_Statuses.md#object-durabilitytransform) | Object  | Transforms the item into another when durability reaches specified thresholds. | 7 | `{ . . . }` |
| [`GainCoinsRange`](./Miscellaneous.md#object-gaincoinsrange) | Object  | An object with `min` and `max` fields specifying a range for the amount of coins gained. | 7 | `{ . . . }` |
| [`Ice`](./Passives_and_Statuses.md#object-ice) | Object  | Applies the Slow status effect to targets hit by ice-element abilities. | 7 | `{ . . . }` |
| `ManaSteal` | Integer | The amount of mana stolen (negative values may drain instead). | 7 | `-1`<br>`5` |
| `MinimumKnockbackFromAllDamage` | Integer | The minimum knockback distance the unit will suffer from any damage source. | 7 | `1` |
| [`OverrideBasicAttack`](./Enums.md#enum-overridebasicattack) | Enum | Replaces the unit's basic attack with the specified ability. | 7 | `BasicExplosiveShot`<br>`BasicMelee`<br>`BasicMetronome` |
| `OverrideMaxHealth` | Integer | Replaces the unit's maximum health with this value. | 7 | `1`<br>`25` |
| [`PassiveIfStrAuxEquals`](./Passives_and_Statuses.md#object-passiveifstrauxequals) | Object  | Grants the contained passive effects when the unit's specified auxiliary stat equals the given value. | 7 | `{ . . . }` |
| [`PassiveWhenOnTile`](./Passives_and_Statuses.md#object-passivewhenontile) | Object  | Grants the contained passive effects while the unit is standing on one of the specified tile types. | 7 | `{ . . . }` |
| [`SetFragileImmune`](./Enums.md#enum-setfragileimmune) | String | Sets the unit's material to the specified type, granting immunity to the Fragile status. | 7 | `""`<br>`Bionic`<br>`Cardboard` |
| [`TriggerWerewolfTransform`](./Arrays.md#array-triggerwerewolftransform) | Array / Number | The number of stacks and probability of triggering the werewolf transformation. | 7 | `.5`<br>`[1 .15]`<br>`[1 .20]` |
| [`Webbed`](./Arrays.md#array-webbed) | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. | 7 | `1`<br>`2`<br>`[1 .1]` |
| `XIsFreeArmorSlots` | Integer | The number of armor slots that are free (no cost) for the unit. | 7 | `1` |
| `AbilityEnabledPercentEachTurn` | Integer | The percentage chance each turn that this ability is enabled. | 6 | `25%`<br>`33%`<br>`35%` |
| [`AbilityOnBattleStart`](./Enums.md#enum-abilityonbattlestart) | Enum | Casts the specified ability when the battle begins. | 6 | `Flush`<br>`Heathens`<br>`Heathens2` |
| `AddDamage` | Integer | The amount of damage added to all attacks. Negative values reduce damage. | 6 | `-1`<br>`1`<br>`2` |
| [`AddDamageToElementDamage`](./Passives_and_Statuses.md#object-adddamagetoelementdamage) | Object  | Defines additional damage of a specific element added to the unit's attacks. | 6 | `{ . . . }` |
| `AddMovement` | Integer | The amount of bonus movement points added to the unit's base movement. | 6 | `-1`<br>`-2`<br>`1` |
| [`AddStatusToElementAbilities`](./Passives_and_Statuses.md#object-addstatustoelementabilities) | Object  | Adds the contained status effects to all abilities with the specified element. | 6 | `{ . . . }` |
| [`AddTemporaryEffectsToBasicAttack`](./Passives_and_Statuses.md#object-addtemporaryeffectstobasicattack) | Object  | A container object that lists temporary status effects applied to the unit's basic attack. | 6 | `{ . . . }` |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | Specifies an animation suffix for the current form, used to load different sprites. | 6 | `""`<br>`"0"`<br>`"1"` |
| `BackstabImmunity` | Integer | If greater than 0, prevents the unit from taking extra damage from backstabs. | 6 | `1` |
| `BasicAttackAOEBonus` | Integer | The additional area of effect radius for the basic attack. | 6 | `1`<br>`2` |
| `BasicAttackDamageMultiplier` | Integer | A multiplier applied to the damage of the basic attack. | 6 | `0`<br>`33.333334%`<br>`50%` |
| [`Bird`](./Passives_and_Statuses.md#object-bird) | Enum / Object  | The object dropped by this bird unit upon death. | 6 | `{ . . . }`<br>`CookedChickenLeg` |
| `BlastResistance` | Integer | The amount of damage reduction against blast-type damage. | 6 | `2`<br>`3`<br>`4` |
| [`BounceRock`](./Arrays.md#array-bouncerock) | Array / Enum  | Specifies the rock object to bounce. | 6 | `LavaBoulder`<br>`SmallLavaRock`<br>`SmallRock` |
| [`CaveFamilyEnrage`](./Passives_and_Statuses.md#object-cavefamilyenrage) | Object  | Specifies the ability used when the number of family members with a given tag falls below a threshold. | 6 | `{ . . . }` |
| `ClearStarving` | Integer | The number of stacks of Starving cleared. | 6 | `1` |
| [`Conditional_BadRoll`](./Passives_and_Statuses.md#object-conditional_badroll) | Object  | An object containing an `odds` value and effects that are applied when a random roll succeeds. | 6 | `{ . . . }` |
| [`CureDisease`](./Passives_and_Statuses.md#object-curedisease) | Object  | Attempts to cure the specified disease with the given chance. | 6 | `{ . . . }` |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`DefaultMove`](./Engine_StatusAndPassiveKeys.md#object-defaultmove) | Object  | Defines the default movement ability for the unit. | 6 | `{ . . . }` |
| [`DelayedAutoRevive`](./Passives_and_Statuses.md#object-delayedautorevive) | Object  | Configures an automatic revival after a delay, with specified rounds and health percentage. | 6 | `{ . . . }` |
| [`Divide4OnDeath`](./Enums.md#enum-divide4ondeath) | Enum | The object that spawns in four instances upon this unit's death. | 6 | `BiggestFood`<br>`Clot`<br>`MedSlime` |
| [`DoDistortionRing`](./Miscellaneous.md#object-dodistortionring) | Object  | Configuration for a distortion ring visual effect, with speed, intensity, and radius. | 6 | `{ . . . }` |
| [`Electric`](./Passives_and_Statuses.md#object-electric) | Object  | Applies a Stun status effect with specified stacks and probability based on variable X. | 6 | `{ . . . }` |
| `ExtraBasicAttacks` | Integer | The number of additional basic attacks the unit can perform per turn. | 6 | `1`<br>`2` |
| [`Fire`](./Passives_and_Statuses.md#object-fire) | Integer / Object  | Defines the 'Fire' form, which may be a stack count or an object that applies burn or uses lava attack. | 6 | `{ . . . }`<br>`1` |
| [`FormChangeWhilePrimingAbility`](./Passives_and_Statuses.md#object-formchangewhileprimingability) | Object  | Defines the form changes when a specific ability is being primed and when it is not. | 6 | `{ . . . }` |
| `Fragile` | Integer | The number of stacks of the Fragile status, causing increased damage taken. | 6 | `1` |
| `FreeFirstCast` | Integer | The number of free casts of this ability per battle. | 6 | `1`<br>`4` |
| [`FreePathfindElement`](./Enums.md#enum-freepathfindelement) | Enum | Specifies a terrain element (e.g., Water, Grass) that the unit can pathfind through without penalty. | 6 | `Grass`<br>`Water` |
| [`Hyde`](./Engine_StatusAndPassiveKeys.md#object-hyde) | Object  | Defines the properties of the Hyde transformation effect. | 6 | `{ . . . }` |
| [`ItemAuxTransform`](./Passives_and_Statuses.md#object-itemauxtransform) | Object  | Transforms the item into another when its auxiliary value reaches specified thresholds. | 6 | `{ . . . }` |
| `KaijuKnockbackImmune` | Integer | If 1, the unit is immune to knockback from kaiju sources. | 6 | `1` |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 6 | `1`<br>`2`<br>`3` |
| `KnockbackImmunity` | Integer | If set to 1, the unit cannot be knocked back. | 6 | `1` |
| [`MoveQuivered`](./Arrays.md#array-movequivered) | Integer | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 6 | `1`<br>`2`<br>`[1, 0.1]` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | Specifies an animation suffix for partial form changes. | 6 | `""`<br>`"Angry"`<br>`"Belly"` |
| [`PassiveWhenAtFullMana`](./Passives_and_Statuses.md#object-passivewhenatfullmana) | Object  | An object listing passive effects that are active only while the unit's mana is full. | 6 | `{ . . . }` |
| `PermanentConstitution` | Integer | The amount of permanent Constitution stat added or removed. | 6 | `-1`<br>`-2`<br>`1` |
| `PoisonThorns` | Integer | The number of stacks of Poison applied to melee attackers when they hit this unit. | 6 | `1`<br>`2`<br>`3` |
| [`ReplaceBasicAttackWhenCastable`](./Enums.md#enum-replacebasicattackwhencastable) | Enum | Replaces the basic attack with the specified ability when that ability can be cast. | 6 | `BasicSuplex`<br>`Hone`<br>`Hone2` |
| [`ReplaceBasicMove_Mutation`](./Enums.md#enum-replacebasicmove_mutation) | Enum | Replaces the unit's basic movement with the specified mutation-based move. | 6 | `BasicDig`<br>`BasicJump` |
| [`ScatterCoins`](./Miscellaneous.md#object-scattercoins) | Object  | The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula. | 6 | `{ . . . }` |
| [`ScatterHeldCoin`](./Arrays.md#array-scatterheldcoin) | Array / Integer | The number of coins scattered, with an optional probability as a second element. | 6 | `1`<br>`[1 .3]`<br>`[1 .5]` |
| [`SetBrittleImmune`](./Enums.md#enum-setbrittleimmune) | String | Sets the unit's material to the specified type, granting immunity to the Brittle status. | 6 | `""`<br>`AdvancedAlloy`<br>`Alloy` |
| `SetDistanceDisplace` | Integer | The fixed distance to displace the target. | 6 | `5` |
| `ShowHiddenThings` | Integer | If nonzero, reveals hidden objects or tiles on the map. | 6 | `1` |
| [`StatusIfUnusedMovePoints`](./Passives_and_Statuses.md#object-statusifunusedmovepoints) | Object  | Specifies status effects applied if the unit ends its turn with unused movement points. | 6 | `{ . . . }` |
| [`StatusKilledCharacters`](./Passives_and_Statuses.md#object-statuskilledcharacters) | Object  | An object listing status effects applied to the unit when it kills a character. | 6 | `{ . . . }` |
| [`StatusOnBattleEnd`](./Passives_and_Statuses.md#object-statusonbattleend) | Object  | An object containing status effects or passives applied to the unit when the battle ends. | 6 | `{ . . . }` |
| [`StatusOnEndMove`](./Passives_and_Statuses.md#object-statusonendmove) | Object  | Specifies status effects or actions triggered when the unit finishes moving. | 6 | `{ . . . }` |
| [`StatusOnStanceSwitch`](./Passives_and_Statuses.md#object-statusonstanceswitch) | Object  | Applies the contained status effects when the unit changes stances. | 6 | `{ . . . }` |
| [`StatusOnTookDamageFromAbility`](./Passives_and_Statuses.md#object-statusontookdamagefromability) | Object  | Specifies status effects triggered when the unit takes damage specifically from an ability (not environmental). | 6 | `{ . . . }` |
| [`StunImmunity`](./Passives_and_Statuses.md#object-stunimmunity) | Integer / Object  | If 1, the unit is immune to stun. The optional object configures whether to cleanse stun on apply. | 6 | `{ . . . }`<br>`1` |
| [`TagGreed`](./Enums.md#enum-taggreed) | Enum | The tag of items that this unit will move towards to collect. | 6 | `bishop_hat`<br>`food`<br>`pickup` |
| [`TeamCastAbility`](./Miscellaneous.md#object-teamcastability) | Enum / Object  | Specifies the ability name for the team to cast, with optional tag restriction and same orientation. | 6 | `{ . . . }`<br>`Huddle_Impl`<br>`Spin`<br>`TeamFlex_Impl` |
| [`TwisterDisplaceWithDamage`](./Miscellaneous.md#object-twisterdisplacewithdamage) | Object  | Configuration for a twister displacement that deals damage, with min/max distance and damage value. | 6 | `{ . . . }` |
| [`YOffset`](./Enums.md#enum-yoffset) | Float | The vertical offset applied to the unit's visual position, used for floating or hovering effects. | 6 | `-.18`<br>`.25`<br>`.35` |
| `ally_chance` | Integer | The percentage chance for an ally to catch incoming projectiles. | 5 | `100%`<br>`15%` |
| `Angel` | Integer | If 1, the unit is an angel type, which may affect behavior like reviving. | 5 | `1` |
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum | The tile type to change the ground tiles under the target to. | 5 | `DirtTile`<br>`GlassTile`<br>`LavaTile` |
| [`CollectsPickupsWithAltEffects`](./Miscellaneous.md#object-collectspickupswithalteffects) | Object  | Contains alternative effects that are applied when collecting pickups. | 5 | `{ . . . }` |
| `DamageOrHealConditionally` | Integer | The amount of conditional damage or healing applied, based on certain conditions (e.g., ally or enemy). | 5 | `1` |
| `fetus` | Variable | A variable used in status effect calculations; specific usage depends on context. | 5 ||
| [`FlySwarm`](./Engine_StatusAndPassiveKeys.md#object-flyswarm) | Object  | Summons a fly swarm with the given chance or intensity percentage. | 5 | `{ . . . }` |
| [`FlySwarm`](./Engine_StatusAndPassiveKeys.md#object-flyswarm) | Object  | Summons a fly swarm with the given chance or intensity percentage. | 5 | `{ . . . }` |
| `HeadArmorPassiveMultiplierBonus` | Integer | A multiplier bonus applied to passive effects granted by head armor. | 5 | `1`<br>`2` |
| `HitExplosion` | Integer | The radius of the explosion triggered on hit. | 5 | `10`<br>`5`<br>`X` |
| [`KnockbackDirectionIsFacingDirection`](./Enums.md#enum-knockbackdirectionisfacingdirection) | Enum / Integer  | Specifies how to alter knockback direction relative to the unit's facing: 1 (same), flip (opposite), rotate_right. | 5 | `1`<br>`flip`<br>`rotate_right` |
| `MonkStanceSwitch` | Integer | The number of times to switch monk stance. | 5 | `1` |
| [`MoveTowardsKillers`](./Passives_and_Statuses.md#object-movetowardskillers) | Enum / Object  | Determines the movement behavior when moving towards units that have killed an ally. | 5 | `{ . . . }`<br>`ReaperRevenge` |
| `NoHealthRegen` | Number | Prevents the unit from regenerating health normally. | 5 | `1` |
| [`ObjectOnHit`](./Miscellaneous.md#object-objectonhit) | Enum / Object  | Specifies the object to spawn on the hit tile. | 5 | `{ . . . }`<br>`Bait`<br>`BiggestFood`<br>`Carcus` |
| [`ObjectOnHitEmpty`](./Enums.md#enum-objectonhitempty) | Enum | Specifies the object to spawn on hitting an empty cell. | 5 | `AnimalEgg`<br>`AnimalEgg2`<br>`HeadTumor` |
| `RefreshMovePointsIfHit` | Integer | The amount of movement points restored on hit. | 5 | `1` |
| `RepairTrinket` | Integer | The number of stacks of the Repair Trinket status effect to apply. | 5 | `1`<br>`99` |
| `SharkySmellsBlood` | Integer | If 1, the unit is attracted to damaged units and may prioritize them. | 5 | `1` |
| [`SpawnCoinAnywhere`](./Arrays.md#array-spawncoinanywhere) | Array / Integer | The number of coins to spawn. If an array, the second value is the probability of spawning them anywhere. | 5 | `1`<br>`[1 .5]` |
| [`SpawnRock`](./Arrays.md#array-spawnrock) | Array / Integer | The number of rocks to spawn, or an array with stacks and probability. | 5 | `1`<br>`[1, .20]` |
| `StartOffMap` | Integer | If 1, the unit begins the encounter off the map. | 5 | `1` |
| [`StatusGroup`](./Passives_and_Statuses.md#object-statusgroup) | Object  | A container grouping multiple status effects to be applied simultaneously. | 5 | `{ . . . }` |
| [`StatusOnTurnEndIfDidntCastAbilityTypes`](./Passives_and_Statuses.md#object-statusonturnendifdidntcastabilitytypes) | Object  | Applies the contained status effects at turn end if the unit did not cast an ability of the specified type(s). | 5 | `{ . . . }` |
| [`Tangled`](./Miscellaneous.md#object-tangled) | Array / Integer / Object  | The number of stacks of the Tangled status effect applied, or an object defining its properties such as `stacks` and `alt_art`. | 5 | `{ . . . }`<br>`1`<br>`2`<br>`[1, .05]` |
| [`TransformItemOnElementInfluence`](./Passives_and_Statuses.md#object-transformitemonelementinfluence) | Object  | Transforms the item into the specified one when influenced by the given element, optionally fully repairing it. | 5 | `{ . . . }` |
| [`TransformOnDeathImmediately`](./Passives_and_Statuses.md#object-transformondeathimmediately) | Enum / Object  | The object to transform into immediately upon death, with optional turn handling. | 5 | `{ . . . }`<br>`NoHead` |
| `UpgradeRandomAbility` | Integer | The number of random abilities upgraded upon effect. | 5 | `1` |
| [`water`](Characters_and_Bosses.md#object-water) | Variable | A variable representing water element intensity or presence. | 5 ||
| [`Water`](./Passives_and_Statuses.md#object-water) | Object  | Form state for water element, applying a puddle or movement bonus. | 5 | `{ . . . }` |
| [`XIsLivingAlliesWithTag`](./Enums.md#enum-xislivingallieswithtag) | Enum | Specifies the tag that living allies must have for this passive to affect them. | 5 | `dc_crow`<br>`hitler_clone_fetus`<br>`terminator_mini` |
| [`AbilityAfterEnemyCastSpell_Stackable`](./Enums.md#enum-abilityafterenemycastspell_stackable) | Enum | The ability to cast after an enemy spell, which can stack in effect. | 4 | `ThornUp`<br>`ThornUpX` |
| [`AbilityReaction`](./Passives_and_Statuses.md#object-abilityreaction) | Enum / Object  | Specifies the ability used as a reaction when the unit is targeted by an ability. | 4 | `{ . . . }`<br>`AnkyloSpin`<br>`GSOpen`<br>`Gassy_AssBlast` |
| [`AbilityWhenTaggedCharacterMovesNear`](./Passives_and_Statuses.md#object-abilitywhentaggedcharactermovesnear) | Object  | An object containing `ability`, `tag`, and `range` that triggers the specified ability when a character with the given tag moves within range. | 4 | `{ . . . }` |
| `AddDamageToBasicAttack` | String | Additional damage added to the basic attack, either as a flat value or formula. | 4 | `1`<br>`2`<br>`4` |
| `AddManaRegen` | Integer | The flat amount of mana regenerated per turn. | 4 | `1`<br>`2`<br>`3` |
| `AddMeleeKnockback` | Integer | The amount of additional knockback dealt by melee attacks. | 4 | `1`<br>`10`<br>`2` |
| [`AddPassivesToCharmed`](./Passives_and_Statuses.md#object-addpassivestocharmed) | Object  | Grants the contained passive effects to units under the charm status. | 4 | `{ . . . }` |
| [`AddSelfStatusToBasicAttack`](./Passives_and_Statuses.md#object-addselfstatustobasicattack) | Object  | Applies the contained status effects to the unit when it uses its basic attack. | 4 | `{ . . . }` |
| `AddSpeed` | Integer | The amount of speed added (or subtracted) to the unit. | 4 | `-3`<br>`4`<br>`6` |
| [`AddStatusToAllDamage`](./Passives_and_Statuses.md#object-addstatustoalldamage) | Object  | Adds the contained status effects to all damage dealt by the unit. | 4 | `{ . . . }` |
| [`AddStatusToAllDamageAbilities`](./Passives_and_Statuses.md#object-addstatustoalldamageabilities) | Object  | Adds the contained status effects to all damaging abilities (spells and attacks). | 4 | `{ . . . }` |
| [`AddStatusToElementDamage`](./Passives_and_Statuses.md#object-addstatustoelementdamage) | Object  | An object that applies a specific status effect when dealing damage of a specified element. Contains sub-keys for the element and the status to apply. | 4 | `{ . . . }` |
| `AllyDamageReduction` | Integer | The amount by which damage dealt to allies is reduced. | 4 | `0` |
| [`AllyManaRegenAura`](./Passives_and_Statuses.md#object-allymanaregenaura) | Object  | An object granting a mana regeneration aura to allies, with sub-keys for stacks and range. | 4 | `{ . . . }` |
| `AmplifyKnockback` | Integer | The additional distance (in tiles) a unit is knocked back. | 4 | `10`<br>`2` |
| `any` | Variable | A wildcard key that matches any property name, often used for generic or dynamic lookups. | 4 ||
| `AOEPuddle` | Enum | Specifies the pattern or shape of an area-of-effect puddle left on the ground. | 4 | `X-1` |
| [`ApplyToConsumed`](./Miscellaneous.md#object-applytoconsumed) | Object  | Container for effects that are applied to the consumed object. | 4 | `{ . . . }` |
| [`ArcLightning`](./Miscellaneous.md#object-arclightning) | Object  | Configuration for arc lightning chain, with stacks, chance, max distance, and enemy-only flag. | 4 | `{ . . . }` |
| [`AutocastEachRound`](./Passives_and_Statuses.md#object-autocasteachround) | Enum / Object  | Contains an ability name and optional 'even_if_stunned' flag to autocast each round. | 4 | `{ . . . }`<br>`SpiderReturn` |
| `BackstabAllDirections` | Integer | If 1, the unit deals backstab damage from all directions. | 4 | `1` |
| [`BaitAura`](./Passives_and_Statuses.md#object-baitaura) | Object  | The range of the bait aura that draws enemies towards the unit. | 4 | `{ . . . }` |
| [`BasicStraightShot`](./Engine_StatusAndPassiveKeys.md#object-basicstraightshot) | Object  | An object defining a basic attack that fires a projectile in a straight line. | 4 | `{ . . . }` |
| [`BasicTankMelee`](./Engine_StatusAndPassiveKeys.md#object-basictankmelee) | Object  | An object defining a basic melee attack for a tank-type unit. | 4 | `{ . . . }` |
| [`BeefyCharmedLeech`](./Engine_StatusAndPassiveKeys.md#object-beefycharmedleech) | Object  | An object defining a variant of the Maggot familiar, specifically a charmed, larger leech. | 4 | `{ . . . }` |
| `BreakAtAux` | Integer | The number of auxiliary item uses before this item breaks. | 4 | `0` |
| [`BuffImmunity`](./Passives_and_Statuses.md#object-buffimmunity) | Integer / Object  | If 1, the unit is immune to buffs. An optional object can list buffs to exclude from immunity. | 4 | `{ . . . }`<br>`1` |
| `bug` | Variable | A variable key likely indicating a known issue or placeholder value. | 4 ||
| `CatchBoomerang` | Integer | If set, allows the ability to catch a boomerang, with the integer representing the number of catches. | 4 | `1` |
| [`ChanceToBackflip`](./Passives_and_Statuses.md#object-chancetobackflip) | Object  | An object specifying the ability to use and the percentage chance to perform a backflip dodge when hit. | 4 | `{ . . . }` |
| [`ChangeTileOnPop`](./Enums.md#enum-changetileonpop) | Enum | The type of tile that appears when this unit is destroyed. | 4 | `CreepTile`<br>`GlitchTile`<br>`OilTile` |
| [`CharmedTinySpider`](./Engine_StatusAndPassiveKeys.md#object-charmedtinyspider) | Object  | An object defining a charmed variant of the TinySpider familiar. | 4 | `{ . . . }` |
| [`ClassManaCostReduction`](./Passives_and_Statuses.md#object-classmanacostreduction) | Object  | Defines a reduction in mana cost for abilities of a specific class. | 4 | `{ . . . }` |
| [`CobraReflex`](./Enums.md#enum-cobrareflex) | Enum | Specifies which basic attack or ability grants increased dodge or counterattack chance. | 4 | `BasicMonkMelee` |
| [`Conditional_PartyMember`](./Passives_and_Statuses.md#object-conditional_partymember) | Object  | A conditional block that executes its child actions only if the target is a party member. | 4 | `{ . . . }` |
| `ConsumablesInfiniteRange` | Integer | If non-zero, consumable items can be used at any range without distance restrictions. | 4 | `1` |
| `CopyBasicAttackEffects` | Integer | If set, the ability copies the effects from the unit's basic attack. | 4 | `1` |
| `CountAsCorpse` | Integer | If 1, the unit counts as a corpse for interactions like raising or necromancy. | 4 | `1` |
| [`CounterAttack`](./Passives_and_Statuses.md#object-counterattack) | Array / Enum / Object  | Specifies the ability used when the unit counterattacks after being hit. | 4 | `{ . . . }`<br>`BungaSwipe`<br>`CloakerHex`<br>`CollectiveCounter` |
| `CreepTile` | Variable | A variable key referencing a tile type that applies a creep or detrimental effect. | 4 ||
| `crow` | Variable | A variable key likely representing a unit or effect related to the crow faction. | 4 ||
| [`DisableAbilities`](./Enums.md#enum-disableabilities) | Enum | Specifies which category of abilities to disable, such as 'all_items' or 'basic_attack'. | 4 | `all_items`<br>`all_spells`<br>`basic_attack` |
| [`DisplayDangerAOE`](./Enums.md#enum-displaydangeraoe) | Enum | The ability whose area of effect is displayed to warn players. | 4 | `GrenadeExplode`<br>`MoonHead_Blow`<br>`TheChild_Wrath` |
| [`DistanceBonusDamage`](./Passives_and_Statuses.md#object-distancebonusdamage) | Object  | An object that adds bonus damage based on the distance from the target, with sub-keys for stacks and minimum range. | 4 | `{ . . . }` |
| [`DownRankAIIfWeaponUsable`](./Enums.md#enum-downrankaiifweaponusable) | Float | A multiplier that reduces the AI's priority to use this ability if the unit has a usable weapon. | 4 | `.001` |
| [`ElementalManaCostReduction`](./Passives_and_Statuses.md#object-elementalmanacostreduction) | Object  | An object that reduces the mana cost of spells of specified elements, with sub-keys for element and reduction amount. | 4 | `{ . . . }` |
| [`EnableWeather`](./Enums.md#enum-enableweather) | Enum | Specifies the weather effect to enable. | 4 | `KaijuFirestorm`<br>`KaijuMeteornado`<br>`KaijuMeteornadoSolo` |
| `equal` | Variable | A variable key used in conditional comparisons to check equality. | 4 ||
| [`EquipRandomTemporaryItemFromPool`](./Enums.md#enum-equiprandomtemporaryitemfrompool) | Enum | Specifies the item pool (e.g., 'pills' or 'weapons') from which a random temporary item is equipped. | 4 | `pills`<br>`weapons` |
| `ExplosionIfHitSomething` | Integer | The radius of explosion triggered if the attack hits an entity. | 4 | `5` |
| [`extra_statuses`](./Miscellaneous.md#object-extra_statuses) | Object  | An object containing additional status effects (with stack counts) applied to the consumed unit. | 4 | `{ . . . }` |
| `ExtraDispersedTurns` | Integer | The number of additional or fewer turns in the dispersed turn order. | 4 | `-1`<br>`1` |
| `FaceArmorPassiveMultiplierBonus` | Integer | A multiplier bonus applied to the effects of face armor passives. | 4 | `1`<br>`2` |
| [`FactionUprising`](./Enums.md#enum-factionuprising) | Enum | Specifies which faction triggers a global uprising event, adding allied units of that faction. | 4 | `alien`<br>`ghost`<br>`robot` |
| `Fights` | Number | The number of fights this status or effect persists for. | 4 | `1`<br>`3`<br>`99` |
| [`FragileDuringElement`](./Enums.md#enum-fragileduringelement) | Enum | Specifies an element during which the unit becomes fragile, taking increased damage. | 4 | `water` |
| `FreezePiercing` | Integer | The number of stacks of freeze resistance that are ignored when applying freeze. | 4 | `1` |
| `GrassTile` | Number | The numerical identifier for a grass-type tile. | 4 | `15`<br>`80` |
| [`GroundFlopper`](./Enums.md#enum-groundflopper) | Enum | The movement ability used when this unit is on the ground. | 4 | `DefaultMove`<br>`MoveOne` |
| `HouseFoodRequirementMultiplier` | Integer | A multiplier for the amount of food the house requires; 0 removes the food requirement. | 4 | `0` |
| `IncreaseExplosionDamage` | Integer | The flat amount by which explosion damage is increased. | 4 | `1`<br>`2`<br>`3` |
| [`LateStatusApplication`](./Miscellaneous.md#object-latestatusapplication) | Object  | Container for status effects that are applied late after the main effect. | 4 | `{ . . . }` |
| [`LevelUpClassOverride`](./Enums.md#enum-levelupclassoverride) | Enum | Specifies which class the unit gains upon leveling up, overriding the default class. | 4 | `Colorless`<br>`Jester` |
| [`LoopingSoundWhileAlive`](./Enums.md#enum-loopingsoundwhilealive) | Enum | The looping sound effect played while the unit is alive. | 4 | `BigUFO_ambient_looping`<br>`Bomb_FuseLoop`<br>`Twister_loop` |
| [`LowerAmbientLight`](./Miscellaneous.md#object-lowerambientlight) | Object  | If an object, defines the target light amount and transition speed; if a number, sets the ambient light level directly. | 4 | `{ . . . }` |
| [`LowerAmbientLight`](./Miscellaneous.md#object-lowerambientlight) | Object  | If an object, defines the target light amount and transition speed; if a number, sets the ambient light level directly. | 4 | `{ . . . }` |
| `ManaCostReduction` | Integer | The amount or percentage by which ability mana costs are reduced for this unit. | 4 | `-2`<br>`1`<br>`2` |
| [`Metronome`](./Miscellaneous.md#object-metronome) | Integer / Object  | The number of times Metronome triggers, or an object with stacks and banned abilities. | 4 | `{ . . . }`<br>`1`<br>`2` |
| [`Metronome`](./Miscellaneous.md#object-metronome) | Boolean (Flag) / Number / Object  | The number of times Metronome triggers, or an object with stacks and banned abilities. | 4 | `{ . . . }`<br>`1`<br>`2` |
| `musical` | Variable | A variable key likely related to musical abilities or sound effects. | 4 ||
| `PartialCleanse` | Integer | The number of stacks of temporary status effects to remove from the target. | 4 | `1`<br>`9999` |
| [`PassiveAtHealthThreshold`](./Passives_and_Statuses.md#object-passiveathealththreshold) | Object  | An object that grants additional passives when the unit's health meets a specified threshold, with sub-keys for threshold, mode, and passives. | 4 | `{ . . . }` |
| [`PassiveWhenDead`](./Passives_and_Statuses.md#object-passivewhendead) | Object  | Passive effects that remain active while the unit is dead. | 4 | `{ . . . }` |
| `PermanentIntelligence` | Integer | The permanent amount of intelligence added or removed. | 4 | `-1`<br>`1`<br>`2` |
| [`PoopWhenHit`](./Passives_and_Statuses.md#object-poopwhenhit) | Object  | Specifies the object (e.g., Poop) spawned when the unit is hit, or an object with `chance` and `object`. | 4 | `{ . . . }` |
| `PrioritizeFarAwayTargets` | Integer | The weight for AI to prioritize targets based on distance; higher values favor farther targets. | 4 | `1`<br>`10` |
| [`RandomPassivePool`](./Passives_and_Statuses.md#object-randompassivepool) | Object  | A pool of random passives from which one is chosen for this unit. | 4 | `{ . . . }` |
| [`RandomSeededStatModifier`](./Arrays.md#array-randomseededstatmodifier) | Array | An array defining a random, seeded modifier to stats, typically in the format [modifier, offset]. | 4 | `[2 -1]` |
| [`ReflectProjectiles`](./Passives_and_Statuses.md#object-reflectprojectiles) | Integer / Object  | The percentage chance to reflect projectiles back at the attacker; optionally includes self-damage. | 4 | `{ . . . }`<br>`1`<br>`10%`<br>`100%` |
| `RemoveActPoints` | Integer | The number of action points removed from the target. | 4 | `1` |
| [`RepairWeapon`](./Arrays.md#array-repairweapon) | Array / Integer | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 4 | `1`<br>`6`<br>`99` |
| [`ReplaceSpell`](./Miscellaneous.md#object-replacespell) | Object  | Defines which spell slot to replace and with which ability. | 4 | `{ . . . }` |
| `SendRock` | Integer | The number of rocks to send as projectiles. | 4 | `1` |
| [`SizeScale`](./Enums.md#enum-sizescale) | Number | The multiplier applied to the unit's visual and hitbox size. | 4 | `.4`<br>`.6`<br>`.7` |
| [`SmartMetronome`](./Miscellaneous.md#object-smartmetronome) | Integer / Object  | The number of stacks of a buff that increases damage by a percentage, with an optional upgrade flag. | 4 | `{ . . . }`<br>`20` |
| [`SmartMetronome`](./Miscellaneous.md#object-smartmetronome) | Integer / Object  | The number of stacks of a buff that increases damage by a percentage, with an optional upgrade flag. | 4 | `{ . . . }`<br>`20` |
| [`SpawnCatCopyOnBattleStart`](./Passives_and_Statuses.md#object-spawncatcopyonbattlestart) | Object  | An object that spawns a copy of the unit's cat at the start of battle, with sub-keys for the copy object and chain-prevention tag. | 4 | `{ . . . }` |
| [`SpawnThingOnDeath`](./Enums.md#enum-spawnthingondeath) | Enum | Specifies the name of an object to spawn upon death. | 4 | `Boulder`<br>`CharmedDemonKitten`<br>`CharmedFlySwarm` |
| [`StatusOnAllyCatDeath`](./Passives_and_Statuses.md#object-statusonallycatdeath) | Object  | An object listing status effects applied to the unit when an allied cat dies. | 4 | `{ . . . }` |
| [`StatusOnEatFood`](./Passives_and_Statuses.md#object-statusoneatfood) | Object  | An object listing status effects applied to the unit when it eats food. | 4 | `{ . . . }` |
| [`StatusOnGainCoins`](./Passives_and_Statuses.md#object-statusongaincoins) | Object  | Specifies status effects applied when this unit gains coins. | 4 | `{ . . . }` |
| [`StatusOnHealed`](./Passives_and_Statuses.md#object-statusonhealed) | Object  | An object that applies a status effect to the unit whenever it is healed. | 4 | `{ . . . }` |
| [`StatusOnOverHealed`](./Passives_and_Statuses.md#object-statusonoverhealed) | Object  | An object that applies a status effect to the unit whenever it receives overhealing (healing beyond max health). | 4 | `{ . . . }` |
| [`StatusOnTakeHealthOrShieldDamage`](./Passives_and_Statuses.md#object-statusontakehealthorshielddamage) | Object  | An object that applies a status effect when the unit takes damage to either health or shields. | 4 | `{ . . . }` |
| [`StatusOnTurnEndIfCastNSpells`](./Passives_and_Statuses.md#object-statusonturnendifcastnspells) | Object  | An object that applies a status effect at the end of the turn if the unit has cast a specified number of spells. | 4 | `{ . . . }` |
| [`StatusOnTurnEndIfManaExact`](./Passives_and_Statuses.md#object-statusonturnendifmanaexact) | Object  | An object that applies a status effect at the end of the turn if the unit's mana is exactly a specified value. | 4 | `{ . . . }` |
| [`StatusOnTurnEndIfManaOrHealthExact`](./Passives_and_Statuses.md#object-statusonturnendifmanaorhealthexact) | Object  | An object that applies a status effect at the end of the turn if the unit's mana or health is exactly a specified value. | 4 | `{ . . . }` |
| [`StatusRandomEnemiesOnBattleStart`](./Passives_and_Statuses.md#object-statusrandomenemiesonbattlestart) | Object  | An object that applies a status effect to a random number of enemies at the start of battle, with sub-keys for count and the status. | 4 | `{ . . . }` |
| [`SwitchMusic`](./Miscellaneous.md#object-switchmusic) | Object  | Defines a new song or layer for the background music. | 4 | `{ . . . }` |
| `TauntAlways` | Integer | If non-zero, the unit is always taunted, forcing it to target the first enemy in range. | 4 | `1` |
| [`TempPassiveWhileHasStatus`](./Miscellaneous.md#object-temppassivewhilehasstatus) | Object  | An object defining passives temporarily granted to the unit while it has a specific status effect. | 4 | `{ . . . }` |
| [`TileTrail`](./Enums.md#enum-tiletrail) | Enum | Specifies the type of tile left behind as the unit moves. | 4 | `BrambleTile`<br>`CreepTile`<br>`FireTile` |
| [`TimeDelayStatusApplication`](./Miscellaneous.md#object-timedelaystatusapplication) | Object  | Container for status effects applied after a specified delay. | 4 | `{ . . . }` |
| [`ToadJump_BasicMove`](./Engine_StatusAndPassiveKeys.md#object-toadjump_basicmove) | Object  | An object defining a basic movement ability for a toad-like unit. | 4 | `{ . . . }` |
| [`Trapper`](./Passives_and_Statuses.md#object-trapper) | Object  | Specifies a trap-placing ability and its targeting parameters. | 4 | `{ . . . }` |
| `UncappedMana` | Integer | If non-zero, the unit has no maximum mana limit. | 4 | `1` |
| `Vegan` | Integer | If nonzero, sets the unit as Vegan; can also be an object with localization fields and the `Disorder` class. | 4 | `1` |
| [`WeremanTransformationReceiver`](./Enums.md#enum-weremantransformationreceiver) | Enum | Determines which transformation animation or effect is applied when this unit is turned by a were-creature. | 4 | `CaveManTransform`<br>`CaveWomanDropTransform` |
| `AbilityEnabledOncePerRound` | Integer | If set, the ability can only be used once per round. | 3 | `1` |
| [`AbilityEnableIfConsumedCharacterHasTag`](./Enums.md#enum-abilityenableifconsumedcharacterhastag) | Enum | Specifies the tag that a consumed character must have for the ability to be enabled. | 3 | `sp_pill_fire`<br>`sp_pill_normal`<br>`sp_pill_tar` |
| `AbilityInheritsWeaponEffects` | Integer | If set, the ability inherits properties from the unit's weapon, with higher values indicating different inheritance modes. | 3 | `1`<br>`2` |
| `AddEndOfCombatRegen` | Integer | The amount of health regenerated after combat ends. | 3 | `12`<br>`999999` |
| `AggroTargetIsCurrentTurn` | Integer | If set to 1, the unit's aggro target is the unit currently taking its turn. | 3 | `1` |
| `AllStatsUpPerDisorder` | Integer | The amount by which all stats increase for each disorder (negative status) the unit has. | 3 | `1` |
| [`ApplyMultipleTimes`](./Miscellaneous.md#object-applymultipletimes) | Object  | An object containing a `stacks` value that specifies how many times the nested effects are applied. | 3 | `{ . . . }` |
| [`BaseStatMultiply`](./Enums.md#enum-basestatmultiply) | Float | A multiplier applied to the unit's base stats. | 3 | `.25`<br>`.5`<br>`.666` |
| [`BasicAttackCritChance`](./Enums.md#enum-basicattackcritchance) | Float | A multiplier for the critical hit chance of basic attacks, either as a float or percentage. | 3 | `.1`<br>`100%` |
| `bishop_hat` | Variable | A variable key referencing a specific item or graphical element (the bishop hat). | 3 ||
| `BoneArmorPassive` | Integer | The number of stacks of bone armor granted, which absorbs damage. | 3 | `1` |
| [`BonusTurnPattern`](./Arrays.md#array-bonusturnpattern) | Array | An array defining the pattern of bonus turns granted to this unit. | 3 | `[` |
| `Bounty` | Integer | The number of bounty stacks applied to enemies, increasing rewards on defeat. | 3 | `1`<br>`3` |
| [`BreakOnElement`](./Enums.md#enum-breakonelement) | Enum | Specifies an element that, when dealt to the unit, causes its armor or item to break. | 3 | `water` |
| [`CanMutateTo`](./Arrays.md#array-canmutateto) | Array / Enum  | Specifies the mutation forms this unit can transform into, either a single form or an array of possible forms. | 3 | `Hyde`<br>`[Lumpy, Leaper]`<br>`[TumorousMaggot, ChargeyMaggot, SwappyMaggot]` |
| `CantCatchDiseases` | Integer | The number of stacks that prevent the unit from contracting diseases. | 3 | `1` |
| `CantSpreadDiseases` | Integer | The number of stacks that prevent the unit from spreading diseases. | 3 | `1` |
| [`CatPartsSizeScaleStatus`](./Miscellaneous.md#object-catpartssizescalestatus) | Object  | Configures scale multipliers for individual cat body parts (body, arms, mouth). | 3 | `{ . . . }` |
| `ChanceToBlock` | Integer | The percentage chance to block incoming damage. | 3 | `10%` |
| [`CharmedTinyTumor`](./Engine_StatusAndPassiveKeys.md#object-charmedtinytumor) | Object  | An object defining a specific variant of the TinyTumor status, typically with its own graphics scale. | 3 | `{ . . . }` |
| [`CollideWithConsumed`](./Math_Equations.md) | Equation | Damage formula for collision with consumed objects, e.g., '4+bonus_melee_damage'. | 3 | `1+bonus_melee_damage`<br>`4+bonus_melee_damage`<br>`5+bonus_melee_damage` |
| [`Conditional_Adjacent`](./Passives_and_Statuses.md#object-conditional_adjacent) | Object  | An object whose nested keys define statuses or effects applied to or by units that are adjacent to the unit. | 3 | `{ . . . }` |
| [`Conditional_RandomChance`](./Miscellaneous.md#object-conditional_randomchance) | Object  | An object containing effects that execute only if a random roll succeeds, with an odds value defined inside. | 3 | `{ . . . }` |
| [`Conditional_Shielded`](./Passives_and_Statuses.md#object-conditional_shielded) | Object  | An object containing effects that are only applied if the target has a shield active. | 3 | `{ . . . }` |
| [`CookedChickenLeg`](./Engine_StatusAndPassiveKeys.md#object-cookedchickenleg) | Object  | An undefined object; no examples or paths found in the provided context. | 3 | `{ . . . }` |
| `CopyPassiveSlot` | Integer | An index (0-based) specifying which equipment slot's passive to copy onto this unit. | 3 | `0`<br>`1` |
| `CorpseVaporizer` | Integer | The number of corpses vaporized on hit. | 3 | `1` |
| [`count`](./Arrays.md#array-count) | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 3 | `0`<br>`1`<br>`10` |
| [`CreateGlobalModifiers`](./Passives_and_Statuses.md#object-createglobalmodifiers) | Object  | Defines global gameplay modifiers to activate. | 3 | `{ . . . }` |
| `DestroyWeapon` | Integer | The number of weapons destroyed. | 3 | `1` |
| `DestroyWeaponThrow` | Integer | The number of weapons destroyed after being thrown. | 3 | `1` |
| [`DigestDeadBodies`](./Enums.md#enum-digestdeadbodies) | Enum | Specifies the ability or animation used when digesting a dead body. | 3 | `Digest`<br>`LennyCatDies`<br>`MoonHead_Digest` |
| [`DoubleStatus`](./Enums.md#enum-doublestatus) | Enum | The name of a status effect whose stacks are doubled when applied. | 3 | `Bleed`<br>`Burn`<br>`Poison` |
| [`DropAsFamiliarOnArmorBreak`](./Enums.md#enum-dropasfamiliaronarmorbreak) | Enum | Specifies the familiar type to drop onto the tile when this status holder's armor breaks. | 3 | `FaceGrubFamiliar`<br>`HeadGrubFamiliar`<br>`NeckGrubFamiliar` |
| [`DustOnHit`](./Miscellaneous.md#object-dustonhit) | Object  | Configuration for a dust object spawned on hit. | 3 | `{ . . . }` |
| [`EquipPermanentItem`](./Enums.md#enum-equippermanentitem) | Enum | The name of the item to permanently equip to the source. | 3 | `BoneClub`<br>`Kidney` |
| `ExtraBasicMoves_Status` | Integer | The number of extra basic moves per turn granted. | 3 | `1` |
| `ForceDisplace` | Integer | The distance the target is forced to displace. | 3 | `1` |
| [`ForceMoveTowardsEnemies`](./Enums.md#enum-forcemovetowardsenemies) | Enum / Integer  | Specifies the ability or distance to force the target to move towards enemies. | 3 | `1`<br>`DumbMove_Impl`<br>`MoveOne` |
| [`FormChangeHealthThreshold`](./Passives_and_Statuses.md#object-formchangehealththreshold) | Object  | Specifies health thresholds that trigger form changes, with form_below for health at or below and form_above for health above. | 3 | `{ . . . }` |
| [`Holy`](./Passives_and_Statuses.md#object-holy) | Enum / Object  | Specifies the 'Holy' form within FormChanger, with its own animation suffix and passives. | 3 | `{ . . . }`<br>`MegaGuppy_TransformHoly` |
| `IllusionTint` | Integer | If non-zero, applies an illusionary tint to the unit's sprite. | 3 | `1` |
| [`IncAuxCounterClamped`](./Miscellaneous.md#object-incauxcounterclamped) | Object  | An object with `change` and `max` properties modifying the auxiliary counter by `change`, clamped to `max`. | 3 | `{ . . . }` |
| `include_spells` | Boolean | If true, the AI-controlled bonus turn includes spells as available actions. | 3 | `true` |
| `InstantMaxHealthUp` | Integer | The amount of permanent maximum health increase. | 3 | `20`<br>`4` |
| [`KnockOutCoin`](./Miscellaneous.md#object-knockoutcoin) | Integer / Object  | The number of coins knocked out, with an optional probability or an object with stacks and chance. | 3 | `{ . . . }`<br>`1`<br>`[1 .5]` |
| [`Lava_Distortion`](#object-lava_distortion) | Variable | A configuration object for a visual distortion effect, typically defining a movieclip and render settings. | 3 ||
| `Lifesteal` | Integer | The amount of lifesteal stacks applied. | 3 | `1`<br>`3` |
| [`ManaPickup`](./Passives_and_Statuses.md#object-manapickup) | Object  | The amount of mana stacks and the frame range for the pickup animation. | 3 | `{ . . . }` |
| `Meteornado` | Integer | The number of Meteornado status stacks applied, or an object defining its visual effects. | 3 | `1` |
| `MimicSpawnerAttacks` | Integer | If positive, the number of attacks mimicked; if -1, mimics all attacks from spawner. | 3 | `-1`<br>`1` |
| `MinimumKnockbackFromPhysicalAttacks` | Integer | The minimum knockback distance applied when hit by a physical attack. | 3 | `1` |
| `MoonHeadFinisherEnabler` | Integer | Determines the finisher state for MoonHead abilities; negative values may disable. | 3 | `-1`<br>`0`<br>`1` |
| [`MoveAndUseAbilityEachTurnBeginIfPossible`](./Enums.md#enum-moveanduseabilityeachturnbeginifpossible) | Enum | Specifies the name of the ability the unit will move and attempt to use at the start of each of its turns. | 3 | `Cannibalize`<br>`EatShit`<br>`face_EatNeverstone` |
| `must_do_damage` | Boolean | If true, the status or effect will only be applied if the attack or ability actually deals damage. | 3 | `true` |
| [`MutateViaAbility`](./Enums.md#enum-mutateviaability) | Enum | Specifies the ability that triggers a mutation form change. | 3 | `BBTransformMutant` |
| `NeckArmorPassiveMultiplierBonus` | Integer | A multiplier bonus applied to the passives of the unit's neck armor slot. | 3 | `1`<br>`2` |
| `NextAttackBonusRange` | Integer | The added range for the unit's next basic attack. | 3 | `1`<br>`3`<br>`5` |
| `PermanentDexterity` | Integer | The permanent amount of dexterity added or removed. | 3 | `1`<br>`2` |
| `PermanentSpeed` | Integer | The permanent amount of speed added or removed. | 3 | `-1`<br>`1`<br>`2` |
| `Piercing` | Integer | The amount of armor or damage reduction ignored by the attack or ability. | 3 | `1` |
| `PlayBackground` | Integer | Specifies the background index to play. | 3 | `0`<br>`1` |
| `PrioritizeHitDifferentTargets` | Integer | If set to 1, the unit's AI prioritizes hitting different targets rather than focusing one. | 3 | `1` |
| `RangeUp` | Integer | The number of stacks of bonus attack range applied. | 3 | `1` |
| `RepairOnKill` | Integer | The number of charges restored to the ability upon killing a target. | 3 | `1`<br>`2` |
| `RockyArmorPassive` | Integer | The number of stacks of the Rocky Armor status effect granted. | 3 | `1` |
| `RunInXTurns` | Integer | The number of turns after which this unit will flee the battle. | 3 | `1`<br>`2`<br>`3` |
| [`SetCrazyEyeBackgroundWeights`](./Miscellaneous.md#object-setcrazyeyebackgroundweights) | Object  | An object containing a `weights` array that sets the weighting for which Crazy Eye background variant is displayed. | 3 | `{ . . . }` |
| [`SetDefaultFacePassive`](./Enums.md#enum-setdefaultfacepassive) | Enum | Specifies the name of the default face passive to be assigned to this unit. | 3 | `euphoric`<br>`insane` |
| `SharePickupsWithSpawner` | Integer | If set to 1, pickups collected by this unit are also given to its spawner. | 3 | `0`<br>`1` |
| `SpawnCreepOnHit` | Integer | If set to 1, spawns creep on the tile when this unit takes damage. | 3 | `1` |
| [`SpawnCustomTrap`](./Enums.md#enum-spawncustomtrap) | Enum | Specifies the name of a custom trap blueprint to spawn at the target location. | 3 | `CharmTrap`<br>`EggSackTrap`<br>`SpikeTrap` |
| `SpawnNeutralWebTrapOnMiss` | Integer | The number of neutral web traps spawned on the tile if the attack misses. | 3 | `1` |
| [`SpawnVolcanoOnBattleStart`](./Miscellaneous.md#object-spawnvolcanoonbattlestart) | Object  | An object containing parameters (object type, tile, radius) for spawning a volcano effect at the start of battle. | 3 | `{ . . . }` |
| [`StackingFlowerTrail`](./Passives_and_Statuses.md#object-stackingflowertrail) | Object  | An object defining how a flower trail status stacks (stacks count, stack key) when the unit moves. | 3 | `{ . . . }` |
| [`StatusAllCharactersOnSpawn`](./Passives_and_Statuses.md#object-statusallcharactersonspawn) | Object  | Defines status effects applied to all characters when they spawn into the battlefield. | 3 | `{ . . . }` |
| [`StatusCharactersOnRoundEnd`](./Miscellaneous.md#object-statuscharactersonroundend) | Object  | An object whose nested keys define statuses or effects applied to characters at the end of each round. | 3 | `{ . . . }` |
| [`SupportFormChangeInsteadOfRun`](./Passives_and_Statuses.md#object-supportformchangeinsteadofrun) | Enum / Object  | Specifies a form change to trigger instead of fleeing, either as a passive object with ability details or a direct form name. | 3 | `{ . . . }`<br>`Attacker` |
| [`tag_filter`](./Enums.md#enum-tag_filter) | Enum | Specifies a tag (e.g., 'crow', 'rock', 'grub_familiar') used to filter which units a status or effect applies to. | 3 | `crow`<br>`grub_familiar`<br>`rock` |
| [`TakeBonusTurnWithAIControl`](./Miscellaneous.md#object-takebonusturnwithaicontrol) | Object  | An object configuring whether the bonus turn happens at the end of the round and whether spells are included. | 3 | `{ . . . }` |
| `TempInitiativeChange` | Integer | The flat change to the unit's initiative value. | 3 | `-100`<br>`-999`<br>`100` |
| [`ThornUpX`](./Engine_StatusAndPassiveKeys.md#object-thornupx) | Object  | An object defining a self-buff status effect, typically with its own animation (e.g., 'spikes'). | 3 | `{ . . . }` |
| [`TileTrail_Ahead`](./Enums.md#enum-tiletrail_ahead) | Enum | Specifies the type of tile to place one tile ahead of the unit's movement. | 3 | `FireTile`<br>`FlowerTile`<br>`OilTile` |
| `TriggerGameEnding` | Integer | If set to 1, triggers the game's ending sequence; 0 disables it. | 3 | `0`<br>`1` |
| `TrueShot` | Integer | The number of stacks of a buff that makes the unit's attacks unmissable. | 3 | `1` |
| [`TVOff`](./Engine_StatusAndPassiveKeys.md#object-tvoff) | Object  | An object defining a self-buff status effect that plays a 'turnOff' animation. | 3 | `{ . . . }` |
| [`UseAbility_NonStack`](./Enums.md#enum-useability_nonstack) | Enum | Specifies an ability to use on kill that does not stack with itself. | 3 | `BBTransformZealot`<br>`GenericRage` |
| `VaporizeTarget` | Integer | If non-zero, instantly destroys the target, leaving no corpse. | 3 | `1` |
| [`XIsMultipliedPercentHealth`](./Arrays.md#array-xismultipliedpercenthealth) | Array | The [stacks, probability] for multiplying health by a percentage. | 3 | `[1 12]`<br>`[14 1]`<br>`[6 2]` |
| [`AbilityChargeRefundChance`](./Passives_and_Statuses.md#object-abilitychargerefundchance) | Object  | An object containing a percentage chance to refund an ability charge, with an advantage softcap. | 2 | `{ . . . }` |
| [`AbilityEnabledIfHasStatus`](./Enums.md#enum-abilityenabledifhasstatus) | Enum | Specifies the status effect that must be present on the unit for the ability to be enabled. | 2 | `DemonicGlyph_Bite`<br>`DemonicGlyph_Summon` |
| [`AbilityHealthThreshold`](./Passives_and_Statuses.md#object-abilityhealththreshold) | Object  | Defines an ability and conditions for its activation when the unit's health reaches a threshold. | 2 | `{ . . . }` |
| [`AbilityOnRoundEnd`](./Passives_and_Statuses.md#object-abilityonroundend) | Object  | Specifies an ability that is automatically executed at the end of each round. | 2 | `{ . . . }` |
| [`AbsorbBuff`](#object-absorbbuff) | Variable | A visual effect object (e.g., ManaParticle) that plays when mana or a buff is absorbed. | 2 ||
| `AbsorbManaAura` | Integer | The amount of mana absorbed from nearby enemies each turn. | 2 | `1` |
| `AddAllyNeighborsToAbilityRange` | Integer | The number of additional tiles an ability's range is extended to include adjacent allies. | 2 | `1` |
| `AddChaScalingSpellDamage` | Integer | The amount of spell damage added that scales with the unit's Charisma stat. | 2 | `3` |
| [`AddHiddenTag`](./Enums.md#enum-addhiddentag) | Enum | A hidden tag applied to the unit for internal logic and triggers. | 2 | `bowling_ball`<br>`grown_hitler_clone`<br>`hitler_clone_fetus` |
| `AddInitiative` | Integer | The amount of bonus or penalty to the unit's turn order initiative value. | 2 | `-10`<br>`-100`<br>`-20` |
| `AddKnockbackToEverything` | Integer | The number of tiles of knockback added to all damage instances. | 2 | `1` |
| `AddLootMultiplier` | Integer | The multiplier added to loot drops from this unit. | 2 | `1` |
| [`AddPassivesToSummonAbilityMinions`](./Passives_and_Statuses.md#object-addpassivestosummonabilityminions) | Object  | An object whose nested keys define passives applied to minions summoned by abilities. | 2 | `{ . . . }` |
| [`AddPassiveToSpawnedRocks`](./Passives_and_Statuses.md#object-addpassivetospawnedrocks) | Object  | An object whose nested keys define passives applied to rocks spawned by the unit. | 2 | `{ . . . }` |
| `AddRangedCritChance` | Integer | The percentage chance added to critically hit with ranged attacks. | 2 | `25%` |
| [`AddSelfStatusToWeapons`](./Passives_and_Statuses.md#object-addselfstatustoweapons) | Object  | An object whose nested keys define status effects applied to the unit's own weapons. | 2 | `{ . . . }` |
| `AddSpellDamage` | Integer | The flat amount of spell damage added to all spell attacks. | 2 | `1`<br>`2` |
| `AddSpiritBombCharges` | Integer | The number of charges added to the Spirit Bomb ability. | 2 | `1`<br>`2` |
| `AddStartingMana` | Number | The amount of bonus mana the unit starts each battle with. | 2 | `20`<br>`5` |
| [`AddStatusToBasicAttackWithCooldown`](./Passives_and_Statuses.md#object-addstatustobasicattackwithcooldown) | Object  | An object whose nested keys define statuses applied to basic attacks, subject to a cooldown. | 2 | `{ . . . }` |
| [`AddStatusToExplosions`](./Passives_and_Statuses.md#object-addstatustoexplosions) | Object  | An object whose nested keys define statuses applied to explosion damage. | 2 | `{ . . . }` |
| [`AddStatusToFirstBasicAttack`](./Passives_and_Statuses.md#object-addstatustofirstbasicattack) | Object  | An object whose nested keys define statuses applied only to the unit's first basic attack. | 2 | `{ . . . }` |
| [`AddStatusToKnockbackDamage`](./Passives_and_Statuses.md#object-addstatustoknockbackdamage) | Object  | An object whose nested keys define statuses applied to damage caused by knockback. | 2 | `{ . . . }` |
| [`AddStatusToMeleeDamage`](./Passives_and_Statuses.md#object-addstatustomeleedamage) | Object  | An object whose nested keys define statuses applied to melee damage. | 2 | `{ . . . }` |
| [`AddStatusToSpells`](./Passives_and_Statuses.md#object-addstatustospells) | Object  | Specifies status effects added to all spell attacks used by this unit. | 2 | `{ . . . }` |
| [`AddStatusToTrampleDamage`](./Passives_and_Statuses.md#object-addstatustotrampledamage) | Object  | An object whose nested keys define statuses applied to trample damage. | 2 | `{ . . . }` |
| [`AddTag`](./Enums.md#enum-addtag) | Enum | Specifies a gameplay tag (e.g., 'rock', 'plant') to add to the unit, used for interaction checks. | 2 | `bug`<br>`cat`<br>`fetus` |
| [`AddTemporaryEffectsToEquipment`](./Passives_and_Statuses.md#object-addtemporaryeffectstoequipment) | Object  | An object whose nested keys define temporary status effects added to equipment. | 2 | `{ . . . }` |
| `AddUnfilledMaxHealth` | Integer | The amount of maximum health added, but not healed (the health bar remains at its current level). | 2 | `10`<br>`20`<br>`50` |
| `AddWeaponScaling` | Integer | The amount of scaling added to damage based on the weapon's stats. | 2 | `1` |
| [`AfterImage`](./Passives_and_Statuses.md#object-afterimage) | Object  | Specifies the object or skill used to create an afterimage of the unit. | 2 | `{ . . . }` |
| `AggroTargetIsBuddy` | Integer | If set to 1, the unit's aggro target is its buddy (linked partner). | 2 | `1` |
| `all_items` | Variable | A variable field for specifying all items; no standard examples provided. | 2 ||
| `AllDamageCrits` | Integer | If set to 1, all damage dealt by the unit becomes critical hits. | 2 | `1` |
| `AllDamageImmune_IncludingSpeculative` | Integer | If set to 1, this unit is immune to all damage, including speculative damage. | 2 | `1` |
| `AlliesAvoidTraps` | Integer | If set to 1, allied units will not trigger traps. | 2 | `1` |
| `AllowPassTurn` | Integer | If set to 1, the unit can skip its turn. If 0, it cannot. | 2 | `0`<br>`1` |
| [`AllyBonusAbilityAura`](./Enums.md#enum-allybonusabilityaura) | Enum | Specifies an ability name granted to adjacent allies in an aura, optionally with a square radius. | 2 | `NubbyToss` |
| `AllyChainKnockback` | Integer | The number of additional tiles of knockback applied to enemies hit by chain knockback effects. | 2 | `1` |
| [`AllyDamageReaction`](./Enums.md#enum-allydamagereaction) | Enum | Specifies the ability to use when an ally takes damage, such as 'attack'. | 2 | `attack` |
| [`AllyHealthRegenAura`](./Passives_and_Statuses.md#object-allyhealthregenaura) | Object  | An object defining an aura that grants health regeneration to allies, typically with 'stacks' and 'range' fields. | 2 | `{ . . . }` |
| [`AllyMoveAbilityAura`](./Enums.md#enum-allymoveabilityaura) | Enum | Determines the movement ability granted to allies within an aura. | 2 | `CatapultJump`<br>`CatapultJump2` |
| `AllyMultiplyKnockbackDamage` | Integer | A multiplier for knockback damage dealt to allies. | 2 | `2` |
| `AllyMultiplyKnockbackDistance` | Integer | A multiplier for knockback distance applied to allies. | 2 | `2` |
| `AllyUncappedHPAura` | Integer | The number of stacks granting uncapped maximum health to allies via an aura. | 2 | `1` |
| [`AlternateCraftingPools`](./Passives_and_Statuses.md#object-alternatecraftingpools) | Object  | An object mapping crafting pool categories to alternate pools for the unit. | 2 | `{ . . . }` |
| `AlwaysHitDifferentTargets` | Integer | If set to 1, attacks always target different units, never the same target twice. | 2 | `1` |
| `AmplifyNegativeStatus` | Integer | The number of stacks that amplify the intensity of negative statuses on enemies. | 2 | `1` |
| `AmplifyPositiveStatus` | Integer | The number of stacks that amplify the intensity of positive statuses on allies. | 2 | `1`<br>`2` |
| `Antidote` | Float | The multiplier for the number of antidote pickups spawned. | 2 | `.5`<br>`1` |
| [`ApplyStatusesToRandomEnemiesEachTurn`](./Passives_and_Statuses.md#object-applystatusestorandomenemieseachturn) | Object  | An object specifying statuses to apply to random enemies each turn, with an optional 'count' field. | 2 | `{ . . . }` |
| [`ApplyStatusIfCrit`](./Passives_and_Statuses.md#object-applystatusifcrit) | Object  | Defines effects that are applied only when the attack scores a critical hit. | 2 | `{ . . . }` |
| [`ApplyToTile`](./Miscellaneous.md#object-applytotile) | Object  | Defines effects to apply to the target tile. | 2 | `{ . . . }` |
| [`ArmorBreakOnHit`](./Passives_and_Statuses.md#object-armorbreakonhit) | Object  | An object defining durability loss and chance for armor to break when hit. | 2 | `{ . . . }` |
| `ArmorDodgeChance` | Integer | The percentage chance to dodge incoming attacks when wearing this armor. | 2 | `10%`<br>`15%`<br>`20%` |
| [`AutocastEachTurn`](./Enums.md#enum-autocasteachturn) | Enum | Specifies the ability automatically cast at the end of each turn. | 2 | `DarkOneStrike`<br>`ViolentOutburst` |
| [`AutocastEachTurnBegin`](./Enums.md#enum-autocasteachturnbegin) | Enum | Specifies the ability automatically cast at the start of each turn, optionally with chance and polarity. | 2 | `MindCrack_EldritchVisage`<br>`MindCrack_EldritchVisage2` |
| `AutoCritLowDamage` | Integer | The amount of damage below which attacks automatically critically strike. | 2 | `2`<br>`3` |
| `AutoEquipConsumables` | Integer | The number of consumables automatically equipped per turn. | 2 | `1` |
| [`BackstabCritChance`](./Enums.md#enum-backstabcritchance) | Float | A multiplier for critical hit chance on backstab attacks. | 2 | `.25`<br>`1` |
| `BackstabFront` | Integer | If set to 1, allows backstab bonuses to apply when attacking from the front. | 2 | `1` |
| `BasicAttackCantMiss` | Integer | If nonzero, the unit's basic attack cannot miss. | 2 | `1` |
| `BasicAttackStatusCarefulness` | Integer | The number of stacks of Carefulness applied by basic attacks. | 2 | `1` |
| [`BasicMonkMelee`](./Engine_StatusAndPassiveKeys.md#object-basicmonkmelee) | Object  | An object defining the basic melee attack for a monk class. | 2 | `{ . . . }` |
| [`BasicRanged`](./Engine_StatusAndPassiveKeys.md#object-basicranged) | Object  | An object defining the basic ranged attack for a unit. | 2 | `{ . . . }` |
| [`BasicSuplex`](./Engine_StatusAndPassiveKeys.md#object-basicsuplex) | Object  | An object defining the basic suplex ability for a unit. | 2 | `{ . . . }` |
| [`BodyGuard`](./Miscellaneous.md#object-bodyguard) | Object  | An object that applies a bodyguard status, optionally linking to a swap ability. | 2 | `{ . . . }` |
| [`BodyGuard`](./Miscellaneous.md#object-bodyguard) | Object  | An object that applies a bodyguard status, optionally linking to a swap ability. | 2 | `{ . . . }` |
| `BonusFoodEachBattle` | Integer | The amount of bonus food earned at the end of each battle. | 2 | `2`<br>`20` |
| `BonusHealthRegenBasedOnDex` | Integer | The amount of bonus health regeneration per point of dexterity. | 2 | `5` |
| `BonusRangeBasedOnDex` | Integer | The amount of bonus range per point of dexterity. | 2 | `5` |
| [`BonusToss`](./Engine_StatusAndPassiveKeys.md#object-bonustoss) | Object  | An object defining a bonus toss ability for the unit. | 2 | `{ . . . }` |
| [`BonusToss2`](./Engine_StatusAndPassiveKeys.md#object-bonustoss2) | Object  | An object defining a second bonus toss ability for the unit. | 2 | `{ . . . }` |
| [`BoobyTrapItems`](./Passives_and_Statuses.md#object-boobytrapitems) | Object  | An object defining effects to apply when items are thrown or broken. | 2 | `{ . . . }` |
| [`BoomerCatExplode`](./Engine_StatusAndPassiveKeys.md#object-boomercatexplode) | Object  | An object defining the explosion ability for a boomerang cat, including its spell template and graphics. | 2 | `{ . . . }` |
| `BoostAllyStatsOnDeath` | Integer | The number of stacks that boost ally stats when this unit dies. | 2 | `1`<br>`2` |
| `BoostDamageGlobalAura` | Integer | The amount of damage boost applied by a global aura to all allies. | 2 | `1` |
| `BoostHeals` | Integer | The number of stacks that increase healing received or dealt. | 2 | `-2`<br>`1`<br>`2` |
| `BoostRangeGlobalAura` | Integer | The amount of range boost applied by a global aura to all allies. | 2 | `1` |
| [`BouncyProjectiles`](./Passives_and_Statuses.md#object-bouncyprojectiles) | Object  | An object with 'max_bounces' and 'max_range' defining projectile bounciness behavior. | 2 | `{ . . . }` |
| `Bound` | Integer | The number of stacks of the Bound status effect applied to the target. | 2 | `3` |
| `BraceForEachNeighboringEnemy` | Integer | The number of Brace stacks gained for each adjacent enemy. | 2 | `1`<br>`2` |
| `BreakWhenNoShield` | Integer | If 1, the armor breaks when the unit has no shield remaining. | 2 | `1` |
| [`BungaEntrance`](./Passives_and_Statuses.md#object-bungaentrance) | Object  | Specifies the entrance animation, ability, and conditions for this unit's dramatic battle entrance. | 2 | `{ . . . }` |
| [`BungaSwipe`](./Engine_StatusAndPassiveKeys.md#object-bungaswipe) | Object  | An object defining a melee swipe ability with AI and graphics. | 2 | `{ . . . }` |
| `CancelPrimedAbilities` | Integer | If non-zero, cancels any primed abilities on the target. | 2 | `1` |
| `CanLevelUpWhenDead` | Integer | If 1, allows the unit to gain experience and level up while dead. | 2 | `1` |
| `CanRemoveCursedItems` | Integer | If nonzero, allows the unit to remove cursed items from equipment slots. | 2 | `1` |
| `CanShield` | Integer | If set to 1, this unit can generate shields. | 2 | `1` |
| `CapDamageFromAllies` | Integer | The maximum amount of damage the unit can take from allies per hit. | 2 | `1` |
| `CapMovementAbilityRange` | Integer | The maximum range allowed for movement abilities. | 2 | `1` |
| `CapTechSpent` | Integer | The maximum amount of tech that can be spent on this ability per turn. | 2 | `0`<br>`1` |
| [`CatAPultAnimation`](./Passives_and_Statuses.md#object-catapultanimation) | Object  | An object specifying the ability and animation used for the CatAPult passive. | 2 | `{ . . . }` |
| [`CatapultJump`](./Engine_StatusAndPassiveKeys.md#object-catapultjump) | Object  | An object defining the Catapult Jump ability, a variant of BasicJump. | 2 | `{ . . . }` |
| [`CatapultJump2`](./Engine_StatusAndPassiveKeys.md#object-catapultjump2) | Object  | An object defining an upgraded Catapult Jump ability with a different description. | 2 | `{ . . . }` |
| [`CatchProjectiles`](./Passives_and_Statuses.md#object-catchprojectiles) | Object  | An object defining chance to catch projectiles and optionally apply statuses. | 2 | `{ . . . }` |
| `CCImmunity` | Integer | If set to 1, this unit is immune to crowd control effects. | 2 | `1` |
| `ChainKnockback` | Integer | If 1, enables knockback to chain to additional targets. | 2 | `1` |
| [`ChanceToBlockAndCounter`](./Passives_and_Statuses.md#object-chancetoblockandcounter) | Integer / Object  | The percentage chance or an object defining chance and conditions to block and counter an attack. | 2 | `{ . . . }`<br>`15%`<br>`25%`<br>`33%` |
| `ChanceToDisableActionsIfNotCharmed` | Integer | The percentage chance to disable actions of enemies that are not charmed. | 2 | `75%` |
| [`ChanceToRevive`](./Passives_and_Statuses.md#object-chancetorevive) | Integer / Object  | The percentage chance or an object defining chance, health, and statuses on revival. | 2 | `{ . . . }`<br>`100`<br>`25` |
| [`ChangeFaction`](./Enums.md#enum-changefaction) | Enum | Specifies the name of the faction to switch the target to. | 2 | `sabertooths` |
| `ChangeTauntPriority` | Integer | The amount to adjust the unit's taunt priority, affecting enemy targeting. | 2 | `-1` |
| [`ChangeTileOnDeath`](./Enums.md#enum-changetileondeath) | Enum | Specifies the tile type that replaces the current tile when this unit dies. | 2 | `WaterTile` |
| [`ChargeFists`](./Engine_StatusAndPassiveKeys.md#object-chargefists) | Integer / Object  | The number of charge stacks applied to unarmed attacks. | 2 | `{ . . . }`<br>`1` |
| [`ChargeFists`](./Engine_StatusAndPassiveKeys.md#object-chargefists) | Integer / Object  | The number of charge stacks applied to unarmed attacks. | 2 | `{ . . . }`<br>`1` |
| [`ChargeSpiritBombAura`](./Enums.md#enum-chargespiritbombaura) | Enum | Specifies the ability to charge for spirit bomb aura. | 2 | `DonateEnergy`<br>`DonateEnergy2` |
| `CharmAllFlies` | Integer | If 1, charms all fly-type enemies, causing them to become allies. | 2 | `1` |
| [`CharmedDemonKitten`](./Engine_StatusAndPassiveKeys.md#object-charmeddemonkitten) | Object  | An object defining the Charmed Demon Kitten familiar, a variant of Hyde. | 2 | `{ . . . }` |
| [`CharmedFlySwarm`](./Engine_StatusAndPassiveKeys.md#object-charmedflyswarm) | Object  | Specifies the definition for a charmed fly swarm that inherits properties from FlySwarm, with faction set to allies and inheriting faction. | 2 | `{ . . . }` |
| `CharmedForceAttack` | Integer | If non-zero, forces the charmed target to use its basic attack on a random nearby unit. | 2 | `1` |
| [`CherubimReaction`](./Passives_and_Statuses.md#object-cherubimreaction) | Object  | Specifies the abilities used when this unit leaves or returns to the battlefield. | 2 | `{ . . . }` |
| `ClearNegativeEffects` | Integer | The number of negative effects cleared from the target. | 2 | `1` |
| `CoinsAddDamage` | Integer | The amount of damage added based on the number of coins the unit has. | 2 | `1`<br>`2` |
| `CollectPickupsOnBattleEnd` | Integer | The number of pickups automatically collected from corpses on the battlefield when the battle ends. | 2 | `1` |
| `CollideWithThrowTarget` | Integer | Determines whether the thrown object collides with the primary target (0 disables collision). | 2 | `0` |
| [`Conductor`](./Passives_and_Statuses.md#object-conductor) | Object  | The number of times the Conduct effect is applied. | 2 | `{ . . . }` |
| `ConductorManaRegen` | Integer | The amount of mana regenerated per turn by the Conductor effect. | 2 | `2` |
| [`ConjureBonusAbility`](./Passives_and_Statuses.md#object-conjurebonusability) | Enum / Object  | Specifies the name of the bonus ability to conjure. | 2 | `{ . . . }`<br>`Class`<br>`Colorless`<br>`Mage` |
| [`ConjureBonusAbility`](./Passives_and_Statuses.md#object-conjurebonusability) | Enum / Object  | Specifies the name of the bonus ability to conjure. | 2 | `{ . . . }`<br>`Class`<br>`Colorless`<br>`Mage` |
| `ConjureCastSpellsForAllies` | Integer | The number of additional spells conjured for allies when casting. | 2 | `1`<br>`2` |
| `ConsumableEffectsMultiplierBonus` | Integer | A multiplier bonus applied to the effects of consumable items. | 2 | `1` |
| `CopyCatPassive_Initializer` | Integer | The number of copies of this passive to initialize. | 2 | `1`<br>`2` |
| [`CopySpells`](./Miscellaneous.md#object-copyspells) | Integer / Object  | The number of spells copied from the target, or an object specifying `stacks` and whether the copy is `upgraded`. | 2 | `{ . . . }`<br>`1` |
| [`Counterspell`](./Engine_StatusAndPassiveKeys.md#object-counterspell) | Integer / Object  | If non-zero, negates the next incoming enemy spell and triggers the configured counterspell effects. | 2 | `{ . . . }`<br>`1` |
| [`damage`](./Miscellaneous.md#object-damage) | Enum / Integer / Object  | Specifies the amount of damage dealt, can be a number or expression. | 2 | `{ . . . }`<br>`"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| `DamageBasedOnMissingHealth` | Integer | The percentage of the target's missing health dealt as additional damage. | 2 | `25`<br>`50` |
| `DamageDistanceAOEFalloff` | Integer | The falloff multiplier applied to AoE damage based on distance from the center of the effect. | 2 | `1`<br>`2` |
| `DamageEnemiesOnHeal` | Integer | The amount of damage dealt to enemies whenever the unit is healed. | 2 | `1`<br>`2` |
| `DamageEnemiesOnKill` | Integer | The amount of damage dealt to enemies whenever the unit kills an enemy. | 2 | `1`<br>`2` |
| [`DamageNeighborsAfterMove`](./Passives_and_Statuses.md#object-damageneighborsaftermove) | Object  | Defines the spell damage and effects applied to neighboring tiles after the unit moves. | 2 | `{ . . . }` |
| [`DamageNeighborTilesWhenCastSpell`](./Passives_and_Statuses.md#object-damageneighbortileswhencastspell) | Object  | Defines the spell damage and effects applied to neighbor tiles when a spell is cast. | 2 | `{ . . . }` |
| [`DamageReductionAura`](./Passives_and_Statuses.md#object-damagereductionaura) | Object  | Defines an aura that reduces incoming damage, with range, ally-only, and stack settings. | 2 | `{ . . . }` |
| `DamageTrinket` | Integer | The amount of durability damage dealt to the target's equipped trinket. | 2 | `1` |
| `DeathChill` | Integer | The number of Chill stacks applied to the killer upon death. | 2 | `1` |
| [`DeathRattle`](./Passives_and_Statuses.md#object-deathrattle) | Enum / Object  | Specifies an ability or effect triggered when the unit dies, optionally with a pop_corpse flag. | 2 | `{ . . . }`<br>`BBExplode`<br>`BloatyExplodey`<br>`BombFlyExplode` |
| `DebuffImmunity` | Integer | If 1, the unit is immune to debuffs. | 2 | `1` |
| `DejaVu` | Integer | The percentage chance or definition for the DejaVu disorder, causing repeated events. | 2 | `10%` |
| [`DelayCastAbility`](./Miscellaneous.md#object-delaycastability) | Enum / Object  | Specifies the name of an ability to cast after a delay. | 2 | `{ . . . }`<br>`HitlerNuke` |
| `DelayedFury` | Integer | The percentage of Fury damage that is stored and applied after a delay. | 2 | `0`<br>`75` |
| `DemonicGlyph_Bite` | Integer | The weight for the demonic glyph of bite, or its configuration. | 2 | `1` |
| `DemonicGlyph_Summon` | Integer | The weight for the demonic glyph of summon, or its configuration. | 2 | `1` |
| `DemonicGlyphFrames` | Integer | The number of animation frames for the demonic glyph effect. | 2 | `1` |
| [`DepressionAura`](#depressionaura) | Integer | The number of stacks of Depression status applied to nearby enemies each turn; can be an object with range and ally settings. | 2 | `1`<br>`2` |
| [`DiesToElement`](./Passives_and_Statuses.md#object-diestoelement) | Enum / Object  | Specifies the element that instantly kills this unit, optionally with an instant flag. | 2 | `{ . . . }`<br>`Wind` |
| `DieViaAbilityInternally` | Integer | If non-zero, causes the target to die via an internal ability trigger. | 2 | `1` |
| `DirtyClaws` | Integer | The number of additional damage instances from Dirty Claws on attack. | 2 | `1` |
| `DisablePassiveSlot` | Integer | If non-zero, disables the specified passive slot index (0 or 1). | 2 | `0`<br>`1` |
| `DisplaceToOriginalPosition` | Integer | If non-zero, returns the unit to its original position after the effect resolves. | 2 | `1` |
| `DissuadeInstakills` | Integer | If set to 1, this unit cannot be instantly killed. | 2 | `1` |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 2 | `1`<br>`10`<br>`100` |
| `DoubleCastSpell` | Integer | The number of times the next spell cast is doubled, or a template with name and tooltip. | 2 | `1`<br>`2` |
| `DoubleCastWeapons` | Integer | The number of additional weapon casts per attack. | 2 | `1`<br>`2` |
| [`DoubleLoot`](./Engine_StatusAndPassiveKeys.md#object-doubleloot) | Integer / Object  | The multiplier for loot drops, where 1 or 2 doubles the loot. | 2 | `{ . . . }`<br>`1`<br>`2` |
| [`DoubleLoot`](./Engine_StatusAndPassiveKeys.md#object-doubleloot) | Integer / Object  | The multiplier for loot drops, where 1 or 2 doubles the loot. | 2 | `{ . . . }`<br>`1`<br>`2` |
| `DrinkWater` | Integer | The number of water-drink actions performed. | 2 | `1` |
| [`DrMangler`](./Engine_StatusAndPassiveKeys.md#object-drmangler) | Object  | Defines the Dr Mangler passive, typically increasing damage based on missing health. | 2 | `{ . . . }` |
| `DukeOfFlies` | Integer | The number of flies spawned when the unit dies. | 2 | `1` |
| [`Dyslexia`](./Arrays.md#array-dyslexia) | Array | An array [minRange maxRange] defining the random range of spell range swap caused by Dyslexia. | 2 | `[3 5]`<br>`[6 9]` |
| `EachSpellFreeAtFullMana` | Integer | The number of spells that cost no mana when the unit has full mana. | 2 | `1` |
| [`Earth`](./Passives_and_Statuses.md#object-earth) | Object  | Defines the Earth element effects, including damage value. | 2 | `{ . . . }` |
| [`ElementalAttunement`](./Passives_and_Statuses.md#object-elementalattunement) | Object  | Defines the elemental effects (Fire, Ice, etc.) applied by the attunement. | 2 | `{ . . . }` |
| [`EMP`](./Passives_and_Statuses.md#object-emp) | Object  | Defines the EMP effect, including spell graphics override for pulsed area damage. | 2 | `{ . . . }` |
| `Empath` | Integer | The percentage of damage shared with nearby allies from the Empath disorder. | 2 | `100%`<br>`50%` |
| `EmptyMana` | Integer | If non-zero, sets the unit's mana to empty when applied. | 2 | `1` |
| [`EmptyMind`](./Engine_StatusAndPassiveKeys.md#object-emptymind) | Integer / Object  | The number of Empty Mind stacks, likely disabling special abilities. | 2 | `{ . . . }`<br>`1` |
| [`EmptyMind`](./Engine_StatusAndPassiveKeys.md#object-emptymind) | Integer / Object  | The number of Empty Mind stacks, likely disabling special abilities. | 2 | `{ . . . }`<br>`1` |
| `EnemiesGetPickupsKnockedOut` | Integer | The number of pickups knocked out of enemies when they are defeated. | 2 | `1`<br>`2` |
| `EnergyStorm` | Integer | The period or definition for the Energy Storm, dealing periodic damage in an area. | 2 | `3` |
| [`Enlarge`](./Engine_StatusAndPassiveKeys.md#object-enlarge) | Integer / Object  | The number of turns the unit is enlarged, increasing its size and stats. | 2 | `{ . . . }`<br>`3` |
| [`Enlarge`](./Engine_StatusAndPassiveKeys.md#object-enlarge) | Integer / Object  | The number of turns the unit is enlarged, increasing its size and stats. | 2 | `{ . . . }`<br>`3` |
| `EquipmentPassiveMultiplierBonus` | Integer | A multiplier bonus applied to passive effects from equipment. | 2 | `1` |
| `EquipmentSetBonusBonus` | Integer | The number of additional set bonuses granted from equipment. | 2 | `1`<br>`2` |
| [`EscapeSequence`](./Passives_and_Statuses.md#object-escapesequence) | Object  | Defines an escape sequence with safe explosion displacement and random distance displacement. | 2 | `{ . . . }` |
| [`Eternal`](./Passives_and_Statuses.md#object-eternal) | Object  | Defines the Eternal revival effect, setting stacks and the health percentage restored. | 2 | `{ . . . }` |
| `ExpireOnSpawnerTurnEnd` | Integer | If set to 1, this unit is removed from battle at the end of its spawner's turn. | 2 | `1` |
| `ExplodeOverkilledEnemies` | Integer | The number of explosions caused by overkilled enemies. | 2 | `1`<br>`2` |
| `ExplosionImmunity` | Integer | If non-zero, grants immunity to explosion damage. | 2 | `1` |
| [`ExtraStatusWhenDealingDamage`](./Passives_and_Statuses.md#object-extrastatuswhendealingdamage) | Object  | Defines additional statuses applied to the target or source when dealing damage, with conditionals. | 2 | `{ . . . }` |
| `ExtraTrinketUses` | Integer | The number of additional uses granted to trinkets. | 2 | `1`<br>`10` |
| [`FaceLastDamage`](./Passives_and_Statuses.md#object-facelastdamage) | Integer / Object  | If set to 1, the unit turns to face the direction of the last damage received; an object can specify animation settings. | 2 | `{ . . . }`<br>`1` |
| `FaceShield` | Integer | If 1, the unit has a face shield that protects it from certain attacks or effects. | 2 | `0`<br>`1` |
| [`FamiliarBonusAbility`](./Enums.md#enum-familiarbonusability) | Enum | Specifies the name of the bonus ability added to familiars. | 2 | `FamiliarSelfDestruct`<br>`FamiliarSelfDestruct2` |
| `FamiliarSecondaryDamageImmunity` | Integer | If non-zero, grants immunity to secondary damage sources for familiars. | 2 | `1` |
| [`FinalBossShield`](./Enums.md#enum-finalbossshield) | Enum | Specifies the shield ability used by a final boss, or None for no shield. | 2 | `DestroyerShieldBash`<br>`None` |
| [`FindExtraItemFromPoolOnBattleEnd`](./Enums.md#enum-findextraitemfrompoolonbattleend) | Enum | Specifies the item pool from which an extra item is granted at the end of combat. | 2 | `combat_reward_easy`<br>`pills` |
| [`FindItem`](./Enums.md#enum-finditem) | Enum | The name of the specific item to find and add to the source's inventory. | 2 | `BoneClub`<br>`Molars`<br>`Pearl` |
| `FireStorm` | Integer | The percentage chance or combo definition for the Fire Storm effect. | 2 | `0%`<br>`33%` |
| `FlatHealWhenDealDamage` | Integer | The flat amount of health healed each time damage is dealt. | 2 | `1` |
| `FlatLeechIfDamaged` | Integer | The flat amount of health leeched when the unit takes damage. | 2 | `3`<br>`5` |
| `FlippedFacingForceAttack` | Integer | If non-zero, forces the unit to attack after flipping its facing direction. | 2 | `1` |
| `FlowerPowerAuraBrace` | Integer | The amount of brace (defense) granted by the Flower Power aura. | 2 | `1` |
| `FlowerPowerAuraStrength` | Integer | The amount of strength (attack) granted by the Flower Power aura. | 2 | `1` |
| `FlowersOnEndTurn` | Integer | The number of flowers spawned on the unit's tile at the end of each turn. | 2 | `1`<br>`3`<br>`4` |
| `FlowersOnHit` | Integer | The number of flowers spawned on the tile upon hitting the target. | 2 | `1` |
| [`FlyDamageIncrease`](./Passives_and_Statuses.md#object-flydamageincrease) | Object  | The number of stacks or alias for damage increase against flying units. | 2 | `{ . . . }` |
| `Flying` | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 2 | `1` |
| [`FollowUp`](./Enums.md#enum-followup) | Enum | Specifies the name of the follow-up ability triggered after an attack. | 2 | `FollowUpDash`<br>`FollowUpDash2` |
| `ForceMoveNonAlliesInRangeTowardsTile` | Integer | The tile range within which non-allied units are forcibly moved towards a specified tile. | 2 | `3`<br>`4` |
| [`ForceMoveTowardsTaggedObject`](./Miscellaneous.md#object-forcemovetowardstaggedobject) | Object  | An object specifying the `ability` and optional `tag` used to forcibly move the unit towards a tagged object. | 2 | `{ . . . }` |
| [`FormChangeDuringWeatherElement`](./Passives_and_Statuses.md#object-formchangeduringweatherelement) | Object  | Specifies a form change that triggers when the weather matches a given element. | 2 | `{ . . . }` |
| `FrontstabCritChance` | Integer | The percentage chance to critically hit when attacking from the front. | 2 | `100%` |
| `FullHealthAllStatsUp` | Integer | The number of AllStatsUp stacks granted when at full health. | 2 | `1` |
| `FullHealthCritChance` | Integer | The additional critical hit chance percentage when at full health. | 2 | `100` |
| `FullHealthManaRegen` | Integer | The amount of mana regenerated per turn while at full health. | 2 | `5` |
| `FullPower` | Integer | The number of stacks applied per turn while at full health or full mana. | 2 | `3` |
| `GainExtraShield` | Integer | The amount of shield gained on turn start. | 2 | `2`<br>`4` |
| `GainManaWhenAnythingDies` | Integer | The amount of mana gained whenever any unit dies. | 2 | `1` |
| `GlobalManaBurnAura` | Integer | The amount of mana burned from all enemies per turn. | 2 | `-1` |
| [`GlobalSpawnOnRoundEnd`](./Miscellaneous.md#object-globalspawnonroundend) | Object  | Specifies the object to spawn globally at the end of each round. | 2 | `{ . . . }` |
| `GoopWalk` | Integer | If set to 1, this unit can move through goop tiles without being slowed or damaged. | 2 | `1` |
| [`Grass`](./Passives_and_Statuses.md#object-grass) | Object  | Specifies the status effects applied to allies standing on grass tiles. | 2 | `{ . . . }` |
| `GrassTileHealing` | Integer | The amount of healing received per turn while on a grass tile. | 2 | `1` |
| [`GravityWell`](./Passives_and_Statuses.md#object-gravitywell) | Object  | Specifies the damage and effect applied to units pulled into a gravity well. | 2 | `{ . . . }` |
| `greater` | Variable | Specifies a conditional check for a value being greater than another value. | 2 ||
| [`GrenadeExplode`](./Engine_StatusAndPassiveKeys.md#object-grenadeexplode) | Object  | Specifies the explosion effect and graphics used when a grenade detonates. | 2 | `{ . . . }` |
| [`Haunt`](./Engine_StatusAndPassiveKeys.md#object-haunt) | Object  | Specifies the status effect applied when haunting a target. | 2 | `{ . . . }` |
| `HealAndOverhealToShield` | Integer | The amount of healing that also converts overhealing into shield. | 2 | `12`<br>`20` |
| `HealAtStart` | Integer | The percentage or amount of health restored at the start of the turn. | 2 | `100%` |
| `HealDamagesEnemies` | Integer | If true, healing actions also damage enemies by this amount. | 2 | `1` |
| `HealingAura` | Integer | The amount of healing per turn granted to nearby allies. | 2 | `1` |
| `HealsAlsoRegenMana` | Integer | The percentage or amount of mana regenerated whenever healing is applied. | 2 | `2`<br>`50%` |
| `HealsCanRevive` | Integer | The number of times per battle healing can revive a fallen ally. | 2 | `1`<br>`3` |
| `HolyDamageMultiplierBonus` | Integer | The multiplier bonus applied to holy damage. | 2 | `1` |
| `HolyShieldTransferToSpawner` | Integer | If true, holy shield is transferred to the unit that spawned this one on death. | 2 | `1` |
| [`HolyShieldTransferToTaggedMinions`](./Enums.md#enum-holyshieldtransfertotaggedminions) | Enum | Specifies the tag of minions that receive holy shield on the owner's death. | 2 | `any`<br>`crow` |
| `HPGainBlock` | Integer | If true, the unit cannot gain health from any source. | 2 | `1` |
| [`IceArmor`](./Engine_StatusAndPassiveKeys.md#object-icearmor) | Integer / Object  | The number of Ice Armor stacks granting defensive properties. | 2 | `{ . . . }`<br>`1` |
| [`IceArmor`](./Engine_StatusAndPassiveKeys.md#object-icearmor) | Integer / Object  | The number of Ice Armor stacks granting defensive properties. | 2 | `{ . . . }`<br>`1` |
| [`ImmediateUseDirectionalAbility`](./Enums.md#enum-immediateusedirectionalability) | Enum | Specifies the name of a directional ability to be used immediately by the unit. | 2 | `BowlDash`<br>`BowlDash2` |
| `ImmobilePassive` | Integer | If set to 1, this unit cannot move from its starting position. | 2 | `1` |
| `ImmortalLeeches` | Integer | The number of leech stacks that persist beyond death. | 2 | `1` |
| `IncreaseExplosionSize` | Integer | The number of extra tiles added to the radius of explosions. | 2 | `1`<br>`2`<br>`7` |
| `IncreaseHealingSpellRange` | Integer | The number of extra tiles added to the range of healing spells. | 2 | `2` |
| `IncreaseItemUsesOnEquip` | Integer | The number of extra uses granted to items when equipped. | 2 | `1` |
| `IncreaseSpellRange` | Integer | The number of extra tiles added to the range of spells. | 2 | `10`<br>`2`<br>`20` |
| [`InfiniteRebirth`](./Passives_and_Statuses.md#object-infiniterebirth) | Object  | Specifies the health and effects for unlimited rebirth upon death. | 2 | `{ . . . }` |
| `InjuryImmunity` | Integer | The number of turns the unit is immune to injuries. | 2 | `1` |
| `JohnnyCriesForWashers` | Integer | The number of washers (currency) requested by the Johnny NPC. | 2 | `1`<br>`2` |
| [`KaijuWinCon`](./Enums.md#enum-kaijuwincon) | Enum | Determines which kaiju victory condition is active for this unit. | 2 | `pyrophina`<br>`zaratana` |
| `KillsHeal` | Integer | The amount or percentage of health restored on kill. | 2 | `5`<br>`50%` |
| [`KillsToMeat`](./Enums.md#enum-killstomeat) | Enum | Specifies the type of meat item spawned when killing certain enemies. | 2 | `Food` |
| [`LateBloomer`](./Passives_and_Statuses.md#object-latebloomer) | Object  | Specifies the stats gained after a set number of turns or stacks. | 2 | `{ . . . }` |
| [`LeaveBehindOnceEachMove`](./Enums.md#enum-leavebehindonceeachmove) | Enum | Specifies the object left behind on the tile once per move. | 2 | `Poop`<br>`Scrap` |
| `LeechPercent` | Integer | The percentage of damage dealt restored as health. | 2 | `50` |
| `LightningAspectCharge` | Integer | The number of charges gained that enhance the next lightning attack. | 2 | `0`<br>`1` |
| [`LightningRod`](./Passives_and_Statuses.md#object-lightningrod) | Object  | Specifies the unit tags and conditions that cause lightning strikes. | 2 | `{ . . . }` |
| `LimitDamage` | Integer | The maximum amount of damage the unit can take from a single hit. | 2 | `1` |
| `LimitHeal` | Integer | If 1, prevents the unit from being healed. | 2 | `0`<br>`1` |
| [`LineOfSightTrueSightAura`](./Enums.md#enum-lineofsighttruesightaura) | Float | The multiplier or chance for line of sight true sight aura to reveal hidden units. | 2 | `.5`<br>`0` |
| `LobbedHook` | Integer | The number of hooks that arc over obstacles to pull targets. | 2 | `1`<br>`2` |
| [`LowHealthAllyDodgeChanceAura`](./Passives_and_Statuses.md#object-lowhealthallydodgechanceaura) | Object  | Specifies the health threshold and dodge chance granted to nearby low-health allies. | 2 | `{ . . . }` |
| `MagicDamageImmune` | Integer | If set to 1, this unit is immune to magic damage. | 2 | `1` |
| `MakeBasicAttackPassThroughThings` | Integer | If true, basic attacks pass through obstacles and other units. | 2 | `1` |
| `MakeBasicAttackPull` | Integer | If nonzero, the unit's basic attack pulls the target closer. | 2 | `1` |
| `MakeSpellsRequireCharge` | Integer | If true, spells require a charge-up turn before casting. | 2 | `1` |
| `MamaCatAnimations` | Integer | If set to 1, enables special mama cat animations. | 2 | `1` |
| `ManaRegenMultiplierIfManaEmpty` | Integer | The multiplier applied to mana regen when mana is empty. | 2 | `2` |
| [`Math`](./Miscellaneous.md#object-math) | Object  | An object containing a `stacks` value that determines how many times the nested effects are applied. | 2 | `{ . . . }` |
| `MaxHPUp` | Integer | The amount of maximum health permanently increased. | 2 | `100` |
| `MegaMinions` | Integer | The number of extra minions spawned or maximum minion count. | 2 | `3` |
| `Metal` | Integer | The number of armor stacks or metal keyword effects. | 2 | `1` |
| `MetalDetector` | Integer | The number of extra metal drops or scrap found per turn. | 2 | `10`<br>`5` |
| `MinimumTech` | Integer | The minimum tech level guaranteed when crafting or upgrading. | 2 | `1` |
| [`MiniVolcanoReaction`](./Enums.md#enum-minivolcanoreaction) | Enum | Specifies the ability triggered when a mini volcano erupts near this unit. | 2 | `MiniVolcano_Spurt`<br>`ThrobShot_Reaction` |
| [`MockingbirdForm`](./Engine_StatusAndPassiveKeys.md#object-mockingbirdform) | Object  | Specifies the shape-shift ability that transforms the unit into a mockingbird. | 2 | `{ . . . }` |
| [`ModifyAbility`](./Miscellaneous.md#object-modifyability) | Object  | Specifies the modifications to an ability's properties, such as cost or type. | 2 | `{ . . . }` |
| [`MotherTumorSpawnInCapture`](./Passives_and_Statuses.md#object-mothertumorspawnincapture) | Object  | Specifies the form changes and statuses applied when the mother tumor spawns after capturing a cat or non-cat. | 2 | `{ . . . }` |
| [`MoveAwayFromDamageSource`](./Passives_and_Statuses.md#object-moveawayfromdamagesource) | Object  | Specifies the move ability used to flee from the source of damage, or an object with `move_ability`. | 2 | `{ . . . }` |
| [`MovementReaction`](./Passives_and_Statuses.md#object-movementreaction) | Object  | Specifies an ability to cast when a unit moves within range, with options for targeting and conditions. | 2 | `{ . . . }` |
| [`MoveOne`](./Engine_StatusAndPassiveKeys.md#object-moveone) | Object  | Specifies a forced movement of exactly one tile in a direction. | 2 | `{ . . . }` |
| `MoveRandomly` | Integer | If true, the unit moves randomly to an adjacent tile each turn. | 2 | `1` |
| [`MoveSpeedMultiplier`](./Enums.md#enum-movespeedmultiplier) | Float | A multiplier for the unit's movement speed. | 2 | `.5` |
| [`MoveTowardsDamageSource`](./Passives_and_Statuses.md#object-movetowardsdamagesource) | Enum / Object  | Determines the movement behavior when moving towards the unit that dealt damage to it. | 2 | `{ . . . }`<br>`MoveOne` |
| [`MoveWhenDamaged`](./Passives_and_Statuses.md#object-movewhendamaged) | Enum / Object  | Defines movement behavior when the unit takes damage, such as weights and move ability. | 2 | `{ . . . }`<br>`TKNG_Hop`<br>`move` |
| [`neck_NukeBonus`](./Engine_StatusAndPassiveKeys.md#object-neck_nukebonus) | Object  | A self-buff ability that grants the Nuke Explosion sub-ability, augmenting the unit's next weapon-based attack with a nuclear detonation. | 2 | `{ . . . }` |
| [`neck_NukeExplode`](./Engine_StatusAndPassiveKeys.md#object-neck_nukeexplode) | Object  | A spell template ability representing the nuclear explosion triggered by Nuke Bonus, playing the NukeBlastLarge center particle and no animation. | 2 | `{ . . . }` |
| [`Necro_SoulDagger_Uncharged`](./Engine_StatusAndPassiveKeys.md#object-necro_souldagger_uncharged) | Object  | The uncharged state of the Necromancer's Soul Dagger ability, dealing reduced damage or having a weaker effect compared to the charged version. | 2 | `{ . . . }` |
| [`NextAttackSpecialCrit`](./Miscellaneous.md#object-nextattackspecialcrit) | Integer / Object  | The number of charges for a special crit on the next attack, or an object defining its bonus properties. | 2 | `{ . . . }`<br>`1` |
| [`NextBattleStatus`](./Passives_and_Statuses.md#object-nextbattlestatus) | Object  | A set of status effects (e.g., stat buffs, full heal) automatically applied to the unit at the start of the next battle. | 2 | `{ . . . }` |
| `NoManaRegen` | Integer | The unit does not naturally regenerate mana per turn. Value indicates the stage or flag enabling this restriction. | 2 | `1` |
| `NoReflection` | Integer | The unit's reflected damage effects are disabled. Value acts as a binary flag. | 2 | `1` |
| [`NubbyToss`](./Engine_StatusAndPassiveKeys.md#object-nubbytoss) | Object  | An ability or action where the unit throws a stumpy or truncated projectile, typically dealing damage or applying a debuff. | 2 | `{ . . . }` |
| `NubbyTossPriority` | Integer | Determines the priority order for the Nubby Toss action relative to other available actions. | 2 | `1` |
| [`NukeQuestFinalBossModifications`](./Miscellaneous.md#object-nukequestfinalbossmodifications) | Object  | Contains modifications for the nuke quest final boss, such as damage_instance effects. | 2 | `{ . . . }` |
| `NumbingLeeches` | Integer | The number of leeches that apply a numbing effect, reducing the target's output or disabling certain actions. Also the name of a Necromancer passive. | 2 | `3` |
| `OneUseSpellDamageUp` | Integer | Increases spell damage by the specified amount, but the effect is consumed after a single use. Alias for SpellDamageUp. | 2 | `2` |
| `OverhealGainsBothShield` | Integer | Any healing beyond maximum health also grants shield points equal to the overheal amount. Value controls the conversion rate. | 2 | `1`<br>`2` |
| [`OverHealToStatuses`](./Miscellaneous.md#object-overhealtostatuses) | Object  | Specifies a set of statuses applied to the target based on the amount of over-healing dealt. | 2 | `{ . . . }` |
| `ParasitesArentCursed` | Integer | Parasites attached to the unit are not considered cursed items, preventing negative curse effects. Value is a binary flag. | 2 | `1` |
| [`passive0`](./Enums.md#enum-passive0) | Enum | Specifies the first passive ability assigned to the unit from a predefined list (e.g., SelfAssured, HotBlooded). | 2 | `HotBlooded`<br>`SelfAssured` |
| [`PassiveAfterXKills`](./Passives_and_Statuses.md#object-passiveafterxkills) | Object  | Activates a set of passive effects (e.g., extra attacks, stat boosts) after the unit achieves a certain number of kills defined by the 'stacks' sub-key. | 2 | `{ . . . }` |
| [`PassiveAtFullHealth`](./Passives_and_Statuses.md#object-passiveatfullhealth) | Object  | Applies a set of passive effects (e.g., mana cost reduction, extra damage taken) only while the unit is at maximum health. | 2 | `{ . . . }` |
| [`PassiveAtInjuryThreshold`](./Passives_and_Statuses.md#object-passiveatinjurythreshold) | Object  | Applies a set of passive effects when the unit's injury level ('injury' sub-key) meets or exceeds the specified 'threshold' using the comparison 'mode'. | 2 | `{ . . . }` |
| [`PassiveEnergized`](#object-passiveenergized) | Variable | Enables an electrified visual effect (using Particle_Electric particle) on the unit, indicating a charged or energized state. | 2 ||
| [`PassiveIfWeaponIsUsable`](./Passives_and_Statuses.md#object-passiveifweaponisusable) | Object  | Activates a set of passive effects (e.g., Brace) only if the unit's current weapon is in a usable condition (not broken or disabled). | 2 | `{ . . . }` |
| [`PassiveTar`](#object-passivetar) | Variable | Enables a dripping tar particle effect (using Particle_TarDrip) on the unit, indicating a tar-related passive. | 2 ||
| [`PassiveUntilCastSpell`](./Passives_and_Statuses.md#object-passiveuntilcastspell) | Object  | Applies a set of passive effects (e.g., healing allies each turn) that remain active until the unit casts a spell. | 2 | `{ . . . }` |
| [`PassiveUntilGetKill`](./Passives_and_Statuses.md#object-passiveuntilgetkill) | Object  | Applies a set of passive effects (e.g., Holy Damage Blessing with burn) that remain active until the unit scores a kill. | 2 | `{ . . . }` |
| [`PassiveWhenTheAlpha`](./Passives_and_Statuses.md#object-passivewhenthealpha) | Object  | Activates a set of passive effects (e.g., TogglableRoundEndExtraTurn) only while the unit holds the Alpha status on the team. | 2 | `{ . . . }` |
| [`PassiveWhileHasStatus`](./Miscellaneous.md#object-passivewhilehasstatus) | Object  | An object containing `status` and `passives` that grants the listed passives while the unit has the specified status. | 2 | `{ . . . }` |
| [`PassiveWhileInMonkMeleeStance`](./Passives_and_Statuses.md#object-passivewhileinmonkmeleestance) | Object  | Applies specific passive effects (e.g., Brace, HealthRegenUp) while the unit is in the Monk's melee combat stance. | 2 | `{ . . . }` |
| [`PassiveWhileInMonkRangedStance`](./Passives_and_Statuses.md#object-passivewhileinmonkrangedstance) | Object  | Applies specific passive effects (e.g., AddBonusRange, AddSpellDamage) while the unit is in the Monk's ranged combat stance. | 2 | `{ . . . }` |
| [`PassiveWhileNotHasStatus`](./Passives_and_Statuses.md#object-passivewhilenothasstatus) | Object  | Specifies a set of passives that are active only when this unit does not have the given status. | 2 | `{ . . . }` |
| [`PassiveWhilePreviewingMonkRangedStance`](./Passives_and_Statuses.md#object-passivewhilepreviewingmonkrangedstance) | Object  | Applies specific passive effects (e.g., AddBonusRange) while the unit is previewing the Monk's ranged stance before committing to it. | 2 | `{ . . . }` |
| [`PassiveWhileWearingMetal`](./Passives_and_Statuses.md#object-passivewhilewearingmetal) | Object  | Applies a set of passive effects (e.g., AddElementsToWeapon with Electric) while the unit is equipped with metal armor or accessories. | 2 | `{ . . . }` |
| `PermanentItems` | Integer | The number of equipment slots that are immune to being unequipped or removed, permanently binding items to those slots. | 2 | `1`<br>`2` |
| `PermanentUpgradeRandomActive` | Integer | The number of random active abilities permanently upgraded. | 2 | `1`<br>`4` |
| `Phasing` | Integer | If set to 1, allows the character to phase through solid objects or obstacles. | 2 | `1` |
| [`PlayerCat_ThiefShade2`](./Engine_StatusAndPassiveKeys.md#object-playercat_thiefshade2) | Object  | A customization or modifier for the Thief Shade ability variant 2, altering its behavior or appearance for the player cat. | 2 | `{ . . . }` |
| `PoisonMultiplier` | Integer | A multiplier on all poison damage or poison stack application, increasing the potency of poison effects. | 2 | `2` |
| [`Poop`](Events_and_Encounters.md#object-poop) | Object | A deployable object that acts as a hazard or obstacle, spawning a Poop movieclip with its own name and sound effects. | 2 | `{ . . . }` |
| `PrioritizeAggroTarget` | Integer | A priority weight for targeting the current aggro target. | 2 | `1` |
| `PrioritizePlayerCats` | Integer | A priority weight for targeting player-controlled cats. | 2 | `1` |
| `PrioritizeWeakestEnemy` | Integer | A priority weight for targeting the weakest enemy unit. | 2 | `1` |
| [`ProtectTargetedAllies`](./Passives_and_Statuses.md#object-protecttargetedallies) | Object  | Specifies the ability used to protect targeted allies, including an optional target filter. | 2 | `{ . . . }` |
| [`QuakeAreaChance`](./Miscellaneous.md#object-quakeareachance) | Object  | An object containing a radius and a chance to trigger a quake area effect. | 2 | `{ . . . }` |
| `Quiver` | Integer | Grants additional ammunition capacity or reload charges for ranged weapon abilities, increasing how many times they can be fired. | 2 | `1`<br>`2` |
| [`RandomDistanceDisplace`](./Miscellaneous.md#object-randomdistancedisplace) | Integer / Object  | The number of stacks of a random distance displacement effect, or an object with stacks, min_dist, and chance. | 2 | `{ . . . }`<br>`20` |
| [`RandomKnockback`](./Miscellaneous.md#object-randomknockback) | Object  | An object defining the minimum and maximum distance in tiles for a random knockback. | 2 | `{ . . . }` |
| `RandomLightning` | Integer | Chance per turn or action for a random lightning strike to occur, expressed as a percentage (e.g., 50%). | 2 | `50%` |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`RandomTaggedMutation`](./Enums.md#enum-randomtaggedmutation) | Enum | Specifies the tag to filter random mutations by. | 2 | `bird`<br>`melted` |
| `RangedTrueShot` | Integer | Ranged attacks cannot miss or be dodged, guaranteeing a hit. Value acts as a binary flag. | 2 | `1` |
| [`RatKing`](./Engine_StatusAndPassiveKeys.md#object-ratking) | Object  | An ability or entity that spawns or controls a group of rats, applying swarm mechanics or empowered rat effects. | 2 | `{ . . . }` |
| [`ReaperRevenge`](./Engine_StatusAndPassiveKeys.md#object-reaperrevenge) | Object  | A teleport-based ability that damages the user while applying buffs (e.g., AllStatsUp) upon arrival at the target location. | 2 | `{ . . . }` |
| `RebukeDamage` | Integer | The amount of damage dealt by a rebuke backlash effect. | 2 | `1`<br>`2` |
| [`red`](./Miscellaneous.md#object-red) | Object  | Configuration for one of the dialog options (label 'EVENT_RED_ANSW'), with a fixed chance and associated animation, in a choice event. | 2 | `{ . . . }` |
| [`Reflect`](./Engine_StatusAndPassiveKeys.md#object-reflect) | Integer / Object  | The amount of reflect stacks applied. | 2 | `{ . . . }`<br>`1`<br>`5` |
| [`RefreshEquipmentAbilityOnElement`](./Passives_and_Statuses.md#object-refreshequipmentabilityonelement) | Object  | Refreshes the cooldown of the unit's equipment ability when the unit's attack matches the specified element (e.g., Electric), displaying a recharge popup. | 2 | `{ . . . }` |
| `RefreshMoveOnWeaponConnect` | Integer | Grants an extra move action when the unit successfully lands a weapon hit. Value indicates the number of extra moves. | 2 | `1` |
| [`Regurge`](./Engine_StatusAndPassiveKeys.md#object-regurge) | Integer / Object  | The number of regurgitation triggers. | 2 | `{ . . . }`<br>`1` |
| [`Regurge`](./Engine_StatusAndPassiveKeys.md#object-regurge) | Integer / Object  | The number of regurgitation triggers. | 2 | `{ . . . }`<br>`1` |
| `ReloadOnKill` | Integer | If set, this ability's reload charge is restored on kill (any kill). | 2 | `1` |
| `ReloadOnKillEnemy` | Integer | If set, this ability's reload charge is restored only when killing an enemy. | 2 | `1` |
| `ReloadOnTotalDamageReceived` | Integer | The threshold of total damage received to restore a reload charge. | 2 | `15`<br>`25` |
| `RemoteLeech` | Integer | The amount of remote leech applied to the target on basic attack. | 2 | `1` |
| `RemoveLineOfSightRestrictions` | Integer | Line of sight requirements for targeting are ignored, allowing the unit to target any visible cell regardless of obstacles. | 2 | `1` |
| `RemoveOncePerFightRestriction` | Integer | Abilities or effects with a 'once per fight' limitation can be used multiple times per fight. Value acts as a binary flag. | 2 | `1` |
| `RepairArmorCondition` | Integer | The amount of armor condition restored. | 2 | `1` |
| [`ReplaceBasicAttack_Mutation`](./Enums.md#enum-replacebasicattack_mutation) | Enum | Specifies the mutation-based ability (e.g., FetusSpit) that replaces the unit's standard basic attack. | 2 | `FetusSpit` |
| [`ReplaceBasicAttackWhenDead`](./Enums.md#enum-replacebasicattackwhendead) | Enum | Specifies the ability (e.g., Haunt) that replaces the unit's basic attack when it is in a dead state. | 2 | `Haunt` |
| [`ReplaceBrain`](./Passives_and_Statuses.md#object-replacebrain) | Object  | Defines a replacement AI brain and behavior pattern for the mutant. | 2 | `{ . . . }` |
| [`ReplaceSpellsWhenDead`](./Enums.md#enum-replacespellswhendead) | Enum | Specifies the spell set (e.g., Spook) that replaces the unit's normal spell list when it is in a dead state. | 2 | `Spook` |
| `ResetArmorShield` | Integer | The amount of armor shield restored. | 2 | `1` |
| `ReturnBoundItemOnBattleEnd` | Integer | If set to 1, items bound to this character are returned to their owner at the end of battle. | 2 | `1` |
| `ReviveOnWin` | Integer | Chance (as a percentage) for the unit to automatically revive after the battle ends, if it was dead at the time of victory. | 2 | `100%` |
| [`Robot`](./Passives_and_Statuses.md#object-robot) | Integer / Object  | If an integer 1, the unit is robotic and affected by electric/energized effects. If an object, contains further robot-specific properties. | 2 | `{ . . . }`<br>`1` |
| [`robot`](Characters_and_Bosses.md#object-robot) | Variable | Indicates the unit is considered a robotic entity, potentially sharing interactions or restrictions with mechanical/robot-related systems. | 2 ||
| `RobotsInheritArmor` | Integer | Robots summoned or controlled by the unit inherit a percentage of the unit's armor value. Value controls the inheritance amount. | 2 | `1`<br>`2` |
| `RockDetector` | Integer | Grants the ability to detect or sense rock-type objects or terrain within the specified range (e.g., 10 tiles). | 2 | `10` |
| `SafeExplosions` | Integer | Explosions caused by the unit do not damage friendly units. Value acts as a binary flag. | 2 | `1` |
| [`Sandstorm`](./Engine_StatusAndPassiveKeys.md#object-sandstorm) | Object  | A self-buff ability that creates a sandstorm, applying a status effect (may be 'Sandstorm 1' or an object definition with a specific template). | 2 | `{ . . . }` |
| [`Sandstorm`](./Engine_StatusAndPassiveKeys.md#object-sandstorm) | Object  | A self-buff ability that creates a sandstorm, applying a status effect (may be 'Sandstorm 1' or an object definition with a specific template). | 2 | `{ . . . }` |
| [`ScaledStatusOnLoseShield`](./Passives_and_Statuses.md#object-scaledstatusonloseshield) | Object  | Applies a scaled status effect (e.g., Thorns proportional to shield lost) when the unit loses shield points. Value includes a 'shield' sub-key for threshold. | 2 | `{ . . . }` |
| [`ScaledStatusOnOverHealed`](./Passives_and_Statuses.md#object-scaledstatusonoverhealed) | Object  | An object containing status effect definitions to apply when the unit receives healing that exceeds its maximum health, with the number of stacks scaled by the amount of over-healing. | 2 | `{ . . . }` |
| [`ScaledStatusOnOverMana`](./Passives_and_Statuses.md#object-scaledstatusonovermana) | Object  | An object containing status effect definitions to apply when the unit gains mana that exceeds its maximum mana, with the number of stacks scaled by the amount of over-mana. | 2 | `{ . . . }` |
| [`ScaledStatusOnSpendMana`](./Passives_and_Statuses.md#object-scaledstatusonspendmana) | Object  | An object containing status effect definitions to apply when the unit spends mana, with the number of stacks scaled by the amount of mana spent. | 2 | `{ . . . }` |
| `ScrambleEverything` | Integer | The percentage chance to scramble all abilities and passives on the target. | 2 | `0`<br>`10%` |
| [`SecurityBotProtect`](./Passives_and_Statuses.md#object-securitybotprotect) | Object  | Specifies the ability and movement used by a security bot to protect allies. | 2 | `{ . . . }` |
| `SelfStatusCarefulness` | Integer | The carefulness level when applying statuses to self, used to control stacking. | 2 | `1` |
| [`SelfStun`](./Arrays.md#array-selfstun) | Array / Integer | The number of stacks of self-stun applied, with an optional probability as a second element. | 2 | `1`<br>`[1 .5]` |
| [`SetDefaultFace`](./Enums.md#enum-setdefaultface) | Enum | Specifies the default facial expression, such as 'happy', 'sad', or 'insane'. | 2 | `happy`<br>`insane`<br>`sad` |
| [`SetItemAux`](./Miscellaneous.md#object-setitemaux) | Object  | Configures an item's auxiliary value by specifying a target slot and a formula for the new value. | 2 | `{ . . . }` |
| `SetSpellCosts` | Integer | Overrides the cost of all spells to this value. | 2 | `0`<br>`1`<br>`3` |
| [`Shadowstep`](./Engine_StatusAndPassiveKeys.md#object-shadowstep) | Object  | An object defining the Shadowstep ability, which allows the unit to teleport behind a target before an attack. | 2 | `{ . . . }` |
| `ShareHealthRegen` | Integer | The amount of health regeneration shared with nearby allies. | 2 | `1` |
| [`SharePickups`](./Passives_and_Statuses.md#object-sharepickups) | Object  | If 1 or an object with include_coins, makes the unit share pickups with nearby allies. | 2 | `{ . . . }` |
| [`Shatter`](./Engine_StatusAndPassiveKeys.md#object-shatter) | Integer / Object  | The amount of damage dealt when a frozen or petrified status is shattered, or a template definition for a Shatter ability. | 2 | `{ . . . }`<br>`15` |
| [`ShortCircuit`](./Engine_StatusAndPassiveKeys.md#object-shortcircuit) | Integer / Object  | The number of stacks of the ShortCircuit status effect. | 2 | `{ . . . }`<br>`1` |
| [`ShortCircuit`](./Engine_StatusAndPassiveKeys.md#object-shortcircuit) | Integer / Object  | The number of stacks of the ShortCircuit status effect. | 2 | `{ . . . }`<br>`1` |
| `ShoulderCheck` | Integer | The chance (as a percentage) to perform a Shoulder Check, pushing a target back after a melee attack. | 2 | `100%`<br>`33%` |
| [`ShovingMatch`](./Enums.md#enum-shovingmatch) | Enum | Determines which stat (e.g., 'attack') is used for the Shoving Match shoving contest. | 2 | `attack` |
| `SignalFinalBossShieldBroke` | Integer | If set to a non-zero number, signals that the final boss's shield has been broken. | 2 | `1` |
| [`SleepDart2`](./Engine_StatusAndPassiveKeys.md#object-sleepdart2) | Object  | An object defining the Sleep Dart 2 status, which puts a target to sleep on hit. | 2 | `{ . . . }` |
| [`SlotMachineRollPool`](./Passives_and_Statuses.md#object-slotmachinerollpool) | Object  | Defines the weighted pool of possible slot machine roll results. | 2 | `{ . . . }` |
| `SmallEnemiesIgnoreYou` | Integer | If non-zero, enemies considered 'small' will ignore this unit and not target it. | 2 | `1` |
| [`SmellBlood`](./Engine_StatusAndPassiveKeys.md#object-smellblood) | Integer / Object  | If non-zero, activates the Smell Blood ability which reveals nearby injured units. | 2 | `{ . . . }`<br>`1` |
| [`SmellBlood`](./Engine_StatusAndPassiveKeys.md#object-smellblood) | Integer / Object  | If non-zero, activates the Smell Blood ability which reveals nearby injured units. | 2 | `{ . . . }`<br>`1` |
| [`SmiteEnemiesWhoKill`](./Passives_and_Statuses.md#object-smiteenemieswhokill) | Object  | An object defining a smite effect applied to enemies who kill another unit, typically dealing damage and applying a stun. | 2 | `{ . . . }` |
| [`SparkleBuff`](#object-sparklebuff) | Variable | A variable defining a sparkle particle effect buffer for visual feedback. | 2 ||
| `SpawnBearTrapOnMiss` | Integer | The number of bear traps to spawn on the tile adjacent to the target when the unit misses an attack. | 2 | `1` |
| [`SpawnCatCopyWhenDowned`](./Passives_and_Statuses.md#object-spawncatcopywhendowned) | Object  | An object defining a cat copy to spawn when the unit is downed, typically a shade or specter. | 2 | `{ . . . }` |
| [`SpawnExtraThingsOnBattleStart`](./Passives_and_Statuses.md#object-spawnextrathingsonbattlestart) | Object  | An object with `object` and `number` (or range) defining what and how many objects to spawn at battle start. | 2 | `{ . . . }` |
| [`SpawnItemLinkedFamiliar`](./Passives_and_Statuses.md#object-spawnitemlinkedfamiliar) | Object  | An object defining a familiar to spawn that is linked to a specific item, which breaks when the familiar is defeated. | 2 | `{ . . . }` |
| [`SpawnMeatOnMove`](./Enums.md#enum-spawnmeatonmove) | Enum | Specifies the type of meat object (e.g., 'Food') to spawn on the tile the unit moves from. | 2 | `Food` |
| `SpawnNearEnemies` | Integer | The number of units to spawn near each enemy at the start of battle. | 2 | `1` |
| [`SpawnObjectOnPopCorpse`](./Passives_and_Statuses.md#object-spawnobjectonpopcorpse) | Enum / Object  | Specifies an object (as a string or an object with 'object', 'count', 'except_tiny' keys) to spawn on a corpse when it is popped. | 2 | `{ . . . }`<br>`Catnip`<br>`Coin`<br>`Food` |
| [`SpecialFriends`](./Passives_and_Statuses.md#object-specialfriends) | Object  | An object containing a set of status effects applied to allied units that are considered 'special friends' (e.g., granted by a passive). | 2 | `{ . . . }` |
| [`SpecialGodRays`](./Miscellaneous.md#object-specialgodrays) | Object  | An object defining visual god rays that follow a specific character tag, used for cinematic or boss effects. | 2 | `{ . . . }` |
| [`SpikeBuff`](#object-spikebuff) | Variable | A variable defining a spike/bramble particle effect buffer for visual feedback. | 2 ||
| `SplittableMove` | Integer | The number of times a move action can be split into smaller segments. | 2 | `1`<br>`3` |
| [`Spook`](./Engine_StatusAndPassiveKeys.md#object-spook) | Object  | An object defining the Spook status, which causes the affected unit to flee or become frightened. | 2 | `{ . . . }` |
| `SpreadExtraDebuffs` | Integer | The number of additional debuffs to spread to nearby enemies when applying a debuff. | 2 | `1`<br>`2` |
| `SpreadPainBonus` | Integer | The amount of bonus damage dealt to enemies who are also affected by the Spread Pain effect. | 2 | `2` |
| `SpreadPainBonusCrit` | Integer | The additional critical hit chance against enemies affected by Spread Pain. | 2 | `1` |
| [`StackingDodgeChanceOnTookDamage`](./Passives_and_Statuses.md#object-stackingdodgechanceontookdamage) | Object  | An object with 'amount' (percent) and 'cap' (percent) defining a stacking dodge chance buff that increases each time the unit takes damage, up to a maximum. | 2 | `{ . . . }` |
| `StatMinimum` | Integer | The minimum value that a particular stat cannot fall below. | 2 | `5`<br>`7` |
| [`StatsAtLowHealth`](./Passives_and_Statuses.md#object-statsatlowhealth) | Object  | An object containing a 'threshold' (health value) and stat bonuses (e.g., 'strength', 'speed') that are applied when the unit's health is below the threshold. | 2 | `{ . . . }` |
| [`StatusAfterCastSpell`](./Passives_and_Statuses.md#object-statusaftercastspell) | Object  | An object containing status effects to apply to the unit immediately after it casts any spell. | 2 | `{ . . . }` |
| [`StatusAfterXTurns`](./Passives_and_Statuses.md#object-statusafterxturns) | Object  | Applies a status effect or forces an ability usage after a set number of turns. | 2 | `{ . . . }` |
| [`StatusAlliesOnBattleStart`](./Passives_and_Statuses.md#object-statusalliesonbattlestart) | Object  | An object containing status effects to apply to all allies at the start of battle. | 2 | `{ . . . }` |
| [`StatusAlliesOnGainCoins`](./Passives_and_Statuses.md#object-statusalliesongaincoins) | Object  | An object containing status effects to apply to allies when the unit gains coins, with an optional 'scaled' boolean to scale stacks. | 2 | `{ . . . }` |
| [`StatusAlliesOnKill`](./Passives_and_Statuses.md#object-statusalliesonkill) | Object  | An object containing status effects to apply to all allies when any ally kills an enemy. | 2 | `{ . . . }` |
| [`StatusAlliesOnSpendMana`](./Passives_and_Statuses.md#object-statusalliesonspendmana) | Object  | An object containing status effects to apply to allies when the unit spends mana. | 2 | `{ . . . }` |
| [`StatusAlliesScaledByCursedOnDeath`](./Passives_and_Statuses.md#object-statusalliesscaledbycursedondeath) | Object  | An object containing status effects to apply to allies when the unit dies, with stacks scaled by the number of Cursed stacks the unit had. | 2 | `{ . . . }` |
| [`StatusAllyWhenAllySpendsMana`](./Passives_and_Statuses.md#object-statusallywhenallyspendsmana) | Object  | An object with a 'threshold' (mana amount) and status effects to apply to an ally whenever any ally spends at least that much mana. | 2 | `{ . . . }` |
| [`StatusAnyCatAllyWhoKills`](./Passives_and_Statuses.md#object-statusanycatallywhokills) | Object  | An object containing status effects to apply to any cat ally who kills an enemy. | 2 | `{ . . . }` |
| `StatusCarefulness` | Integer | The carefulness level when applying statuses, used to control stacking behavior. | 2 | `1` |
| [`StatusCharactersOnRoundStart`](./Miscellaneous.md#object-statuscharactersonroundstart) | Object  | An object containing status effects to apply to all characters on the battlefield at the start of each round. | 2 | `{ . . . }` |
| [`StatusDamagers`](./Passives_and_Statuses.md#object-statusdamagers) | Object  | An object defining status effects that damage the unit, with parameters for each status. | 2 | `{ . . . }` |
| [`StatusEachRoundEnd`](./Passives_and_Statuses.md#object-statuseachroundend) | Object  | An object listing status effects applied to the unit at the end of each round. | 2 | `{ . . . }` |
| [`StatusEachTurnEndForEachTurn`](./Passives_and_Statuses.md#object-statuseachturnendforeachturn) | Object  | Statuses applied at the end of each turn, with the number of turns as nested values. | 2 | `{ . . . }` |
| [`StatusEachTurnEndPerEnemyKill`](./Passives_and_Statuses.md#object-statuseachturnendperenemykill) | Object  | An object containing status effects to apply at the end of each turn for each enemy killed during that turn. | 2 | `{ . . . }` |
| [`StatusEnemiesOnDeath`](./Passives_and_Statuses.md#object-statusenemiesondeath) | Object  | An object containing status effects to apply to all enemies when the unit dies. | 2 | `{ . . . }` |
| [`StatusEveryXSpellCastsEachTurn`](./Passives_and_Statuses.md#object-statuseveryxspellcastseachturn) | Object  | An object with a 'stacks' value defining status effects applied every X spell casts within a single turn. | 2 | `{ . . . }` |
| [`StatusEveryXTurnBegins`](./Passives_and_Statuses.md#object-statuseveryxturnbegins) | Object  | An object with a 'turns' value defining status effects applied every X turns at the start of the turn. | 2 | `{ . . . }` |
| [`StatusIfDidntMove`](./Passives_and_Statuses.md#object-statusifdidntmove) | Object  | An object containing status effects to apply to the unit if it did not move during its turn. | 2 | `{ . . . }` |
| [`StatusIfUnusedActPoints`](./Passives_and_Statuses.md#object-statusifunusedactpoints) | Object  | An object containing status effects to apply to the unit if it has unused action points at the end of its turn. | 2 | `{ . . . }` |
| [`StatusKillers`](./Passives_and_Statuses.md#object-statuskillers) | Object  | An object containing nested conditionals that apply status effects when the unit kills an enemy. | 2 | `{ . . . }` |
| [`StatusOnAnyDeath`](./Passives_and_Statuses.md#object-statusonanydeath) | Object  | An object containing status effects to apply whenever any unit (ally or enemy) dies. | 2 | `{ . . . }` |
| [`StatusOnBackstab`](./Passives_and_Statuses.md#object-statusonbackstab) | Object  | An object containing status effects to apply when the unit performs a backstab attack. | 2 | `{ . . . }` |
| [`StatusOnBattleEndIfKillThresholdMet`](./Passives_and_Statuses.md#object-statusonbattleendifkillthresholdmet) | Object  | An object containing a 'kills' threshold and status effects to apply at the end of battle if the unit's kill count meets or exceeds the threshold. | 2 | `{ . . . }` |
| [`StatusOnBattleStart`](./Passives_and_Statuses.md#object-statusonbattlestart) | Object  | An object containing status effects to apply to the unit at the start of every battle. | 2 | `{ . . . }` |
| [`StatusOnBreakItem`](./Passives_and_Statuses.md#object-statusonbreakitem) | Object  | An object containing status effects to apply when the unit breaks a weapon or armor item. | 2 | `{ . . . }` |
| [`StatusOnCollectPickup`](./Passives_and_Statuses.md#object-statusoncollectpickup) | Object  | An object containing status effects to apply when the unit collects a pickup item. | 2 | `{ . . . }` |
| [`StatusOnDealtDamage`](./Passives_and_Statuses.md#object-statusondealtdamage) | Object  | An object containing status effects to apply to the unit whenever it deals damage to an enemy. | 2 | `{ . . . }` |
| [`StatusOnDealtDamageThreshold`](./Passives_and_Statuses.md#object-statusondealtdamagethreshold) | Object  | Specifies the effects applied when the unit deals damage equal to or exceeding the defined threshold. | 2 | `{ . . . }` |
| [`StatusOnDie`](./Passives_and_Statuses.md#object-statusondie) | Object  | Specifies status effects or actions triggered when the unit dies. | 2 | `{ . . . }` |
| [`StatusOnEatPill`](./Passives_and_Statuses.md#object-statusoneatpill) | Object  | Specifies the effects applied when the unit consumes a pill item. | 2 | `{ . . . }` |
| [`StatusOnGainShield`](./Passives_and_Statuses.md#object-statusongainshield) | Object  | Specifies the effects applied when the unit gains a shield. | 2 | `{ . . . }` |
| [`StatusOnHeal`](./Passives_and_Statuses.md#object-statusonheal) | Object  | Specifies the effects applied when the unit receives healing. | 2 | `{ . . . }` |
| [`StatusOnKillEnemy`](./Passives_and_Statuses.md#object-statusonkillenemy) | Object  | Specifies the effects applied when the unit kills an enemy. | 2 | `{ . . . }` |
| [`StatusOnOverMana`](./Passives_and_Statuses.md#object-statusonovermana) | Object  | Specifies the effects applied when the unit's mana exceeds its maximum. | 2 | `{ . . . }` |
| [`StatusOnPickupCoins`](./Passives_and_Statuses.md#object-statusonpickupcoins) | Object  | Specifies the effects applied when the unit picks up coins. | 2 | `{ . . . }` |
| [`StatusOnPopCorpse`](./Passives_and_Statuses.md#object-statusonpopcorpse) | Object  | Specifies the effects applied when the unit pops a corpse. | 2 | `{ . . . }` |
| [`StatusOnSetPieceBreak`](./Passives_and_Statuses.md#object-statusonsetpiecebreak) | Object  | Specifies the effects applied when the unit breaks a set piece. | 2 | `{ . . . }` |
| [`StatusOnSpawnIn`](./Passives_and_Statuses.md#object-statusonspawnin) | Object  | Applies statuses or actions upon the unit spawning into the battlefield. | 2 | `{ . . . }` |
| [`StatusOnTookDamageFromEnemyAbility`](./Passives_and_Statuses.md#object-statusontookdamagefromenemyability) | Object  | Specifies the effects applied when the unit takes damage from an enemy ability. | 2 | `{ . . . }` |
| [`StatusOnTriggerTrap`](./Passives_and_Statuses.md#object-statusontriggertrap) | Object  | Specifies the effects applied when the unit triggers a trap. | 2 | `{ . . . }` |
| [`StatusOnUseBasicAttack`](./Passives_and_Statuses.md#object-statusonusebasicattack) | Object  | Specifies the effects applied when the unit performs a basic attack. | 2 | `{ . . . }` |
| [`StatusOnUseElementAbility`](./Passives_and_Statuses.md#object-statusonuseelementability) | Object  | Specifies the effects applied when the unit uses an ability matching the specified element. | 2 | `{ . . . }` |
| [`StatusPerInjury`](./Passives_and_Statuses.md#object-statusperinjury) | Object  | Specifies the effects granted per injury the unit has, up to an optional cap. | 2 | `{ . . . }` |
| [`StatusReplacement`](./Arrays.md#array-statusreplacement) | Array | Specifies status replacements, where the first status is replaced by the second when applied. | 2 | `[Petrify PetrifyCharmed]` |
| [`StatusThingsKnockedBack`](./Passives_and_Statuses.md#object-statusthingsknockedback) | Object  | Specifies the effects applied when the unit knocks back another unit. | 2 | `{ . . . }` |
| [`StatusWhenAllySpendsMana`](./Passives_and_Statuses.md#object-statuswhenallyspendsmana) | Object  | Specifies the effects applied when an ally spends mana. | 2 | `{ . . . }` |
| `StrengthForEachNeighboringEnemy` | Integer | The amount of strength gained for each adjacent enemy. | 2 | `2`<br>`3` |
| `StrengthInNumbersAura` | Integer | The amount of strength gained per nearby ally within the aura. | 2 | `1` |
| `Study` | Integer | The number of stacks of the Study status applied. | 2 | `1` |
| `SurviveAt1HP` | Integer | If 1, the unit survives a fatal hit with 1 HP instead of dying. | 2 | `1` |
| `SwallowSmallCharacter` | Integer | The percentage chance to swallow a smaller character on hit. | 2 | `100%`<br>`50%` |
| `SwapHighestAndLowestStat` | Integer | If non-zero, swaps the unit's highest base stat value with its lowest. | 2 | `1` |
| [`Switcheroo`](./Engine_StatusAndPassiveKeys.md#object-switcheroo) | Integer / Object  | The number of stacks of the Switcheroo status effect. | 2 | `{ . . . }`<br>`1` |
| [`Switcheroo`](./Engine_StatusAndPassiveKeys.md#object-switcheroo) | Integer / Object  | The number of stacks of the Switcheroo status effect. | 2 | `{ . . . }`<br>`1` |
| [`TaggedPickupEffectReplacement`](./Passives_and_Statuses.md#object-taggedpickupeffectreplacement) | Object  | Specifies a replacement effect for picking up items with a given tag. | 2 | `{ . . . }` |
| `TempCounterAttack` | Integer | The number of turns TempCounterAttack lasts, ticking down at the start of the unit's turn. | 2 | `1` |
| `TempCritChanceUp` | Integer | The amount of temporary critical hit chance (in percentage points) added. | 2 | `100`<br>`30` |
| `TempNoManaRegen` | Integer | The number of turns the unit cannot regenerate mana. | 2 | `1` |
| `ThornsDamageImmuneUntilSettled` | Integer | The number of turns the target is immune to thorns damage until it settles. | 2 | `1` |
| `TileDamageImmuneUntilSettled` | Integer | The number of turns the target is immune to tile damage until it settles. | 2 | `1` |
| `TileDamageMultiplier` | Integer | Multiplier for damage dealt to environmental tiles. | 2 | `2` |
| [`TinkererBasicAttackSwitching`](./Passives_and_Statuses.md#object-tinkererbasicattackswitching) | Object  | Defines the abilities used for the Tinkerer's basic attack switching mechanic. | 2 | `{ . . . }` |
| [`TowerDefense`](./Passives_and_Statuses.md#object-towerdefense) | Object  | Specifies the range and damage of the Tower Defense counterattack. | 2 | `{ . . . }` |
| [`TowerDefenseReflex`](./Enums.md#enum-towerdefensereflex) | Enum | Specifies the ability or attack used when the unit counterattacks in tower defense reflex mode. | 2 | `BasicRanged_1DMG`<br>`attack` |
| [`TradeLife`](./Engine_StatusAndPassiveKeys.md#object-tradelife) | Integer / Object  | The amount of health life traded, or a template for a TradeLife ability. | 2 | `{ . . . }`<br>`1` |
| [`TradeLife`](./Engine_StatusAndPassiveKeys.md#object-tradelife) | Integer / Object  | The amount of health life traded, or a template for a TradeLife ability. | 2 | `{ . . . }`<br>`1` |
| [`TrailBlazer`](./Engine_StatusAndPassiveKeys.md#object-trailblazer) | Enum / Integer / Object  | The number of trail blazer stacks applied, or a string alias like 'mov'. | 2 | `{ . . . }`<br>`1`<br>`mov` |
| [`TrailBlazer`](./Engine_StatusAndPassiveKeys.md#object-trailblazer) | Enum / Integer / Object  | The number of trail blazer stacks applied, or a string alias like 'mov'. | 2 | `{ . . . }`<br>`1`<br>`mov` |
| [`TransformOnElementInfluencex`](./Passives_and_Statuses.md#object-transformonelementinfluencex) | Object  | Transforms into a specified object when influenced by a given element. | 2 | `{ . . . }` |
| [`TransformWhenBuddyDies`](./Enums.md#enum-transformwhenbuddydies) | Enum | Specifies the form the unit transforms into when its buddy dies. | 2 | `UltraOrnstein`<br>`UltraSmough` |
| `TrapEffectsMultiplier` | Integer | Multiplier for the potency of trap effects triggered by the unit. | 2 | `2` |
| `TriggerDOTStatuses` | Integer | If set to 1, triggers damage over time statuses on the target immediately. | 2 | `0`<br>`1` |
| `triggers_limit` | Integer | The maximum number of times this passive effect can trigger per battle. | 2 | `1` |
| `TrinketActiveEffectsMultiplierBonus` | Integer | Bonus multiplier to the active effects of equipped trinkets. | 2 | `1`<br>`2` |
| `TrinketPassiveMultiplierBonus` | Integer | Bonus multiplier to the passive effects of equipped trinkets. | 2 | `1`<br>`2` |
| `UncappedHP` | Integer | If 1, the unit's maximum HP is not capped by standard limits. | 2 | `1` |
| `UncappedHPBonusStr` | Integer | The amount of strength gained per point of HP exceeding the maximum cap. | 2 | `5` |
| `Uncontrollable` | Integer | If non-zero, the unit becomes uncontrollable by the player. | 2 | `1` |
| `UnlockOrientation` | Integer | If 1, allows the unit to freely rotate or face any direction regardless of movement. | 2 | `1` |
| [`UpgradeLevelUpClassActives`](./Enums.md#enum-upgradelevelupclassactives) | Enum | Specifies the upgrade path for class active abilities on level up. | 2 | `Colorless` |
| [`UpgradeLevelUpClassPassives`](./Enums.md#enum-upgradelevelupclasspassives) | Enum | Specifies the upgrade path for class passive abilities on level up. | 2 | `Colorless` |
| `UpgradeSpawnedPickups` | Integer | The number of times spawned pickups are upgraded in quality. | 2 | `1`<br>`2` |
| [`UpgradeTaggedSpawnsToChampions`](./Enums.md#enum-upgradetaggedspawnstochampions) | Enum | Specifies which tag of spawns are upgraded to champion versions. | 2 | `bug`<br>`worm` |
| `Vengeful` | Integer | The number of Vengeful stacks, causing retaliation damage when hit. | 2 | `1` |
| `VisualFlySwarm` | Integer | If non-zero, enables the visual fly swarm effect on the unit. | 2 | `1` |
| `WeaponActiveEffectsMultiplierBonus` | Integer | Bonus multiplier to the active effects of the equipped weapon. | 2 | `2` |
| `WeaponCountsAsBasicAttack` | Integer | If non-zero, the weapon's ability counts as a basic attack. | 2 | `1` |
| `WeaponDamageMultiplierBonus` | Integer | Bonus multiplier to weapon damage. | 2 | `1`<br>`2` |
| `WeaponPassiveMultiplierBonus` | Integer | Bonus multiplier to the passive effects of the equipped weapon. | 2 | `2` |
| `WeaponsDontLoseDurability` | Integer | If set to 1, weapons equipped by this unit do not lose durability. | 2 | `0`<br>`1` |
| [`XIsLivingCharactersWithTag`](./Enums.md#enum-xislivingcharacterswithtag) | Enum | Specifies the tag that living characters must have for this passive to affect them. | 2 | `husk`<br>`rock` |
| `XIsOtherHealsThisTurn` | Integer | If set, tracks other heals this turn for some effect. | 2 | `1` |
| [`XIsSpellStormRampAndReset`](./Miscellaneous.md#object-xisspellstormrampandreset) | Integer / Object  | If integer 0, resets stacks; if object, contains 'stacks' and 'reset_percent' for spell storm ramp. | 2 | `{ . . . }`<br>`0` |
| [`XIsTargetHealth`](./Miscellaneous.md#object-xistargethealth) | Object  | Evaluates a bonus damage formula where X is the target's current health. | 2 | `{ . . . }` |
| `XIsTimesDamageTaken` | Integer | If set, multiplier for damage taken to apply some effect. | 2 | `1` |
| `Zombie` | Number | The number of stacks or value for the Zombie status. | 2 | `1` |
| `AbilityDamageMultiplier` | Float | Multiplier for all ability damage dealt by the unit. | 1 | `1.5` |
| `AbilityDisableIfLivingCrow` | Integer | If set, disables the ability if there is a living crow on the field. | 1 | `1` |
| `AbilityEnabledAtHealthThreshold` | Integer | The health percentage threshold at which the ability becomes enabled. | 1 | `50%` |
| `AbilityEnabledIfBasicAttackUsedThisTurn` | Integer | If set, ability is enabled only if the unit used a basic attack this turn. | 1 | `1` |
| `AbilityEnabledIfMovementTrapped` | Integer | If set, ability is enabled only when the unit's movement is trapped. | 1 | `1` |
| `AbilityEnabledIfNoAggroTarget` | Integer | If set, ability is enabled only when the unit has no aggro target. | 1 | `1` |
| [`AbilityEnabledIfNotHasStatus`](./Enums.md#enum-abilityenabledifnothasstatus) | Enum | Specifies the status that must be absent for ability to be enabled. | 1 | `BackflipWhenTargeted` |
| [`AbilityEnabledIfSpecificItemEquipped`](./Enums.md#enum-abilityenabledifspecificitemequipped) | Enum | Specifies the item that must be equipped for ability to be enabled. | 1 | `Neverstone` |
| [`AbilityOnBattleStart_UseAI`](./Enums.md#enum-abilityonbattlestart_useai) | Enum | Specifies the ability the unit will use at the start of battle via AI resolution. | 1 | `TheCreator_SpawnCloneTeam` |
| [`AbilityOnRoundEndOnce`](./Passives_and_Statuses.md#object-abilityonroundendonce) | Object  | Specifies an ability to be used once at the end of the round. | 1 | `{ . . . }` |
| `AbsorbManaFromOtherSpells` | Integer | If set, this ability absorbs mana from other spells when cast. | 1 | `1` |
| `AcidRain` | Integer | If non-zero, enables the Acid Rain weather effect dealing damage each turn. | 1 | `2` |
| [`AddAdvantageToEvent`](./Passives_and_Statuses.md#object-addadvantagetoevent) | Object  | Specifies additional advantage options to add to a specific event type. | 1 | `{ . . . }` |
| `AddAllyNeighborsToAttackRange` | Integer | The number of ally-occupied tiles added to the unit's attack range. | 1 | `1` |
| `AddConstitution` | Integer | The amount of constitution added to the unit. | 1 | `2` |
| [`AddElementsToSpells`](./Enums.md#enum-addelementstospells) | Enum | Specifies which element to add to spells. | 1 | `Earth` |
| `AddExtraTurnsBeforeRun` | Integer | The number of additional turns added before the run ends. | 1 | `2` |
| `AddLevelUpStatMultiplier` | Integer | Multiplier applied to stat gains on level up. | 1 | `1` |
| [`AddPostProcessEffect`](./Miscellaneous.md#object-addpostprocesseffect) | Object  | Specifies a post-process shader effect to apply to the scene. | 1 | `{ . . . }` |
| `AddRandomEliteBuff` | Integer | The number of random elite buffs to apply to the unit. | 1 | `1` |
| [`AddStatusesIfPersistentWeatherElement`](./Passives_and_Statuses.md#object-addstatusesifpersistentweatherelement) | Object  | Specifies statuses applied if the persistent weather matches the given elements. | 1 | `{ . . . }` |
| [`AddStatusesToReceivedElementalDamage`](./Passives_and_Statuses.md#object-addstatusestoreceivedelementaldamage) | Object  | An object defining statuses applied to the unit when it takes elemental damage of the specified types. | 1 | `{ . . . }` |
| [`AddStatusToBackstabs`](./Passives_and_Statuses.md#object-addstatustobackstabs) | Object  | An object defining statuses applied to the target when the unit performs a backstab attack. | 1 | `{ . . . }` |
| [`AddStatusToFirstSpellEachTurn`](./Passives_and_Statuses.md#object-addstatustofirstspelleachturn) | Object  | An object defining statuses applied to the target after the first spell cast by the unit each turn. | 1 | `{ . . . }` |
| [`AddStatusToReceivedDamage`](./Passives_and_Statuses.md#object-addstatustoreceiveddamage) | Object  | Applies a status effect to the attacker when the unit takes damage. | 1 | `{ . . . }` |
| [`AddStatusToReceivedDamage_ExcludeStatuses`](./Passives_and_Statuses.md#object-addstatustoreceiveddamage_excludestatuses) | Object  | An object defining statuses applied to the attacking unit when the owner receives damage, excluding damage from sources carrying the specified statuses. | 1 | `{ . . . }` |
| [`AddTilesetObjects`](./Miscellaneous.md#object-addtilesetobjects) | Object  | An object configuring the spawning of decorative debris or objects on the tileset for an effect. | 1 | `{ . . . }` |
| `Adrenaline` | Integer | The flat amount of Adrenaline (a resource or stat) granted to the unit. | 1 | `10` |
| [`AdvancedTint`](./Arrays.md#array-advancedtint) | Array | An RGBA color array for advanced sprite tinting. | 1 | `[` |
| [`AdventureTokenPassivePool`](./Miscellaneous.md#object-adventuretokenpassivepool) | Object  | A pool of passive definitions granted to the unit when picked up as an adventure token. | 1 | `{ . . . }` |
| [`AggroTargetIsGovernedByHitEffect`](./Passives_and_Statuses.md#object-aggrotargetisgovernedbyhiteffect) | Object  | If set, the aggro target is determined by the unit's hit effect, with a sub-key for enemies_only. | 1 | `{ . . . }` |
| `AggroTargetIsLastEnemyThatDealtDamage` | Integer | If 1, the unit's aggro target is the last enemy that damaged it. | 1 | `1` |
| `AggroTargetIsLowestHealthEnemyTillItDies` | Integer | If 1, the unit focuses the lowest health enemy until that enemy dies. | 1 | `1` |
| `AggroTargetIsLowestMaxHealthCat` | Integer | If 1, the unit targets the cat ally with the lowest maximum health. | 1 | `1` |
| [`AIControlNextTurn`](./Passives_and_Statuses.md#object-aicontrolnextturn) | Object  | An object that causes the unit to be controlled by the AI on its next turn, with configurable stacks and spell usage. | 1 | `{ . . . }` |
| `AIFavorLowHealth` | Integer | The AI's favorability weight for targeting low-health units. | 1 | `100` |
| [`AlienBeastDangerZones`](./Arrays.md#array-alienbeastdangerzones) | Array | An array of ability names that mark dangerous zones for the Alien Beast fight. | 1 ||
| `AlienBeastEyeStalks` | Integer | The number of eye stalk segments on the Alien Beast. | 1 | `3` |
| `all_spells` | Variable | A variable representing a collection of every spell definition available in the game. | 1 ||
| `AlliesScrambleSpellAfterCast` | Integer | The number of times an ally's next spell cast will be scrambled (randomly redirected or modified) after the owner casts a spell. | 1 | `1` |
| `AlliesTakeExtraTurn` | Integer | The number of extra turns granted to allies. | 1 | `1` |
| `AllSpellsCostActPoints` | Integer | If 1, all spells require action points instead of mana or other resources. | 1 | `1` |
| `AllSpellsCostCharge` | Integer | The number of charges required to cast any spell, adding a universal charge cost. | 1 | `1` |
| [`AllStatsAura`](./Passives_and_Statuses.md#object-allstatsaura) | Object  | An aura that grants bonus stacks of all stats to allies within range. | 1 | `{ . . . }` |
| `AllUnitsExplodeOnDeath` | Integer | The radius of the explosion that triggers when any unit dies. | 1 | `5` |
| [`AlluringDoodieEater`](./Passives_and_Statuses.md#object-alluringdoodieeater) | Object  | An object defining the chance and damage instance for a unit that consumes an alluring doodie. | 1 | `{ . . . }` |
| [`AllyDodgeChanceAura`](./Passives_and_Statuses.md#object-allydodgechanceaura) | Object  | An object granting allies within a specified range a percentage chance to dodge incoming attacks. | 1 | `{ . . . }` |
| `AlphaAllStatsUp` | Integer | The amount by which all of the unit's stats are increased if it is the alpha (highest stat total or designated leader). | 1 | `1` |
| `AlphaDodgeChance` | Integer | The dodge chance granted to the alpha (leader) unit. | 1 | `50%` |
| [`AlphaStatusOnTurnBegin`](./Miscellaneous.md#object-alphastatusonturnbegin) | Object  | Specifies status effects applied to the alpha at the start of each turn. | 1 | `{ . . . }` |
| [`AlternateIdleAnimation`](./Enums.md#enum-alternateidleanimation) | Enum | Specifies the name of an alternative idle animation to play. | 1 | `berserkIdle` |
| `AlwaysChosenForLevelUp` | Integer | If set to 1, this unit is always presented as a level-up option when gaining a level. | 1 | `1` |
| `AOEBonus` | Integer | The bonus number of additional targets or tiles affected by an area-of-effect ability. | 1 | `1` |
| [`ApplyPassivesToSpawnerWhileAlive`](./Miscellaneous.md#object-applypassivestospawnerwhilealive) | Object  | An object defining passives that are applied to the spawner while this unit is alive. | 1 | `{ . . . }` |
| `ApplyShieldToApplierBasedOnMaxHealth` | Integer | The amount of shield applied to the applier based on a fraction of their max health. | 1 | `1` |
| [`ApplyStatusesNextTurnBegin`](./Miscellaneous.md#object-applystatusesnextturnbegin) | Object  | Specifies a set of statuses to apply to the target at the beginning of their next turn. | 1 | `{ . . . }` |
| [`ApplyToOthersWithSharedTagAndFaction`](./Miscellaneous.md#object-applytootherswithsharedtagandfaction) | Object  | Specifies statuses to apply to other units that share a tag and faction with the target. | 1 | `{ . . . }` |
| [`ApplyToRandomClosestAlly`](./Miscellaneous.md#object-applytorandomclosestally) | Object  | Specifies statuses to apply to a random ally closest to the target. | 1 | `{ . . . }` |
| [`Autism`](./Passives_and_Statuses.md#object-autism) | Object  | An object defining the Autism disorder, including its name, description, class, and stat modifications for innate and learned levels. | 1 | `{ . . . }` |
| `AvoidDamagingCharmedEnemies` | Integer | If 1, the unit avoids dealing damage to charmed enemies. | 1 | `1` |
| `AwardCoinsOnDeath` | Integer | The amount of coins awarded to the killer when this unit dies. | 1 | `10` |
| `BackstabWeakness` | Float | A multiplier for damage taken from backstab attacks. | 1 | `0.75` |
| `BalanceStats` | Integer | If set to 1, the unit's stats are balanced (redistributed) towards an average value. | 1 | `1` |
| `BasicAIDangerZone` | Integer | The radius of the danger zone used by the basic AI for area denial. | 1 | `2` |
| [`BasicAttackStatusSwap`](./Arrays.md#array-basicattackstatusswap) | Array | An array of two status IDs; when the unit performs a basic attack, the first status is removed and the second is applied in its place. | 1 | `[TempDamageUp DamageUp]` |
| [`BasicButcherMelee`](./Engine_StatusAndPassiveKeys.md#object-basicbutchermelee) | Object  | An object defining a basic melee attack for the Butcher class. | 1 | `{ . . . }` |
| [`BasicDruidAbility`](./Engine_StatusAndPassiveKeys.md#object-basicdruidability) | Object  | An object defining a basic ability for the Druid class. | 1 | `{ . . . }` |
| [`BasicMagicShortRanged`](./Engine_StatusAndPassiveKeys.md#object-basicmagicshortranged) | Object  | An object defining a basic short-ranged magical attack. | 1 | `{ . . . }` |
| [`BasicMedicMelee`](./Engine_StatusAndPassiveKeys.md#object-basicmedicmelee) | Object  | An object defining a basic melee attack for the Medic class. | 1 | `{ . . . }` |
| [`BasicMelee_4Hits`](./Engine_StatusAndPassiveKeys.md#object-basicmelee_4hits) | Object  | An object defining a variant of the basic melee attack that hits the target 4 times. | 1 | `{ . . . }` |
| [`BasicNecroRanged`](./Engine_StatusAndPassiveKeys.md#object-basicnecroranged) | Object  | An object defining a basic ranged attack for the Necromancer class. | 1 | `{ . . . }` |
| [`BasicPsychicPull`](./Engine_StatusAndPassiveKeys.md#object-basicpsychicpull) | Object  | An object defining a basic psychic ability that pulls a target towards the caster. | 1 | `{ . . . }` |
| [`BattlefieldUniqueRandomPassive`](./Passives_and_Statuses.md#object-battlefielduniquerandompassive) | Object  | A pool of unique random passives that can be applied to each battlefield instance. | 1 | `{ . . . }` |
| [`BBTransformMutant`](./Engine_StatusAndPassiveKeys.md#object-bbtransformmutant) | Object  | An object defining a transformation spell that turns the unit into a mutant. | 1 | `{ . . . }` |
| [`BBTransformZealot`](./Engine_StatusAndPassiveKeys.md#object-bbtransformzealot) | Object  | An object defining a transformation spell that turns the unit into a zealot. | 1 | `{ . . . }` |
| [`BiggestFood`](./Engine_LogicKeys.md#object-biggestfood) | Integer / Object  | The number of biggest food pickups spawned. | 1 | `{ . . . }`<br>`1`<br>`15`<br>`4` |
| `BigSplashDamage` | Integer | The additional tile radius of the splash damage effect applied by an attack. | 1 | `2` |
| `BlackHolePassive` | Integer | If 1, the unit has black hole passive mechanics. | 1 | `1` |
| `BlackHoleSuck` | Integer | The strength of the black hole's pull effect. | 1 | `1` |
| `BlessingOfPeace` | Integer | The number of stacks of the Blessing of Peace status applied to the unit each turn. | 1 | `1` |
| [`BloatEyeMovement2`](./Engine_StatusAndPassiveKeys.md#object-bloateyemovement2) | Object  | An object defining a movement ability for the Bloat Eye enemy. | 1 | `{ . . . }` |
| [`BloatEyePassive2`](./Enums.md#enum-bloateyepassive2) | Enum | Specifies the movement ability for the Bloat Eye enemy. | 1 | `BloatEyeMovement2` |
| [`BloatyExplodey`](./Engine_StatusAndPassiveKeys.md#object-bloatyexplodey) | Object  | An object defining a spell that causes the target to become bloated and explode. | 1 | `{ . . . }` |
| `BlockAllDamage` | Integer | If 1, the unit blocks all incoming damage. | 1 | `1` |
| `BlockDamageUnderThreshold` | Integer | The maximum amount of damage from a single hit that will be completely blocked. | 1 | `1` |
| `BlockNegativeStatus` | Integer | The percentage chance to completely block the application of a negative status effect. | 1 | `30%` |
| `Bloodzerked` | Integer | The number of Bloodzerk stacks applied. | 1 | `1` |
| `BombBehavior` | Integer | If 1, the unit explodes after a set duration or on death. | 1 | `1` |
| [`BombRatTurtle`](./Engine_StatusAndPassiveKeys.md#object-bombratturtle) | Integer / Object  | The number of bomb rat turtle spawns triggered. | 1 | `{ . . . }`<br>`1` |
| [`BoneWormShotMed`](./Engine_StatusAndPassiveKeys.md#object-bonewormshotmed) | Object  | An object defining a medium-range lobbed attack that fires a bone worm projectile. | 1 | `{ . . . }` |
| [`BonusAbility_DelayedApplication`](./Enums.md#enum-bonusability_delayedapplication) | Enum | Specifies the name of a bonus ability to apply with a delay. | 1 | `Slap` |
| `BonusDamageBasedOnMana` | Integer | The amount of bonus damage dealt, scaled by the target's current mana. | 1 | `1` |
| `BonusHealthRegenPerDisorder` | Integer | The amount of additional health regenerated per turn for each disorder the unit has. | 1 | `1` |
| `BoostDamageAura` | Integer | The amount of bonus damage granted to allies within the aura's range. | 1 | `1` |
| `BoostRangeAura` | Integer | The amount of bonus range (in tiles) granted to allies within the aura's range. | 1 | `1` |
| `BoostReceivedHealing` | Integer | The amount of bonus healing received from all sources. | 1 | `2` |
| [`BoyDino`](./Engine_StatusAndPassiveKeys.md#object-boydino) | Object  | An object defining the Boy Dino passive or character definition. | 1 | `{ . . . }` |
| [`BoyDinoCry`](./Engine_StatusAndPassiveKeys.md#object-boydinocry) | Object  | An object defining an ability or effect that causes the unit to cry, typically applying a debuff to nearby enemies. | 1 | `{ . . . }` |
| `BrittleCharismaUp` | Integer | The number of stacks of temporary Charisma gained on kill. | 1 | `2` |
| `BrittleConstitutionUp` | Integer | The number of stacks of temporary Constitution gained on kill. | 1 | `2` |
| `BrittleDexterityUp` | Integer | The number of stacks of temporary Dexterity gained on kill. | 1 | `2` |
| `BrittleIntelligenceUp` | Integer | The number of stacks of temporary Intelligence gained on kill. | 1 | `2` |
| `BrittleLuckUp` | Integer | The number of stacks of temporary Luck gained on kill. | 1 | `2` |
| `BrittleSpeedUp` | Integer | The number of stacks of temporary Speed gained on kill. | 1 | `2` |
| `BrittleStrengthUp` | Integer | The number of stacks of temporary Strength gained on kill. | 1 | `2` |
| [`BungaCheers`](./Passives_and_Statuses.md#object-bungacheers) | Object  | Defines cheer particle effects and sounds triggered by ally or enemy actions. | 1 | `{ . . . }` |
| `ButterflySwarm` | Integer | The number of butterflies spawned for the Butterfly Swarm effect. | 1 | `2` |
| `BypassRockKnockback` | Integer | If set to a non-zero number, bypasses normal rock knockback behavior. | 1 | `1` |
| `CanceledQueuedInput` | Integer | If set to a non-zero number, cancels any queued input from the target. | 1 | `1` |
| `CantDodge` | Integer | If set to 1, the unit cannot dodge any incoming attacks. | 1 | `1` |
| `CapBasicAttackDamage` | Integer | The maximum amount of damage that can be dealt by a basic attack. | 1 | `1` |
| `CapReceivedDamage` | Integer | If 1, the unit caps incoming damage to a maximum per hit. | 1 | `1` |
| [`CatGoop`](./Engine_StatusAndPassiveKeys.md#object-catgoop) | Object  | Defines a specific attack or ability template, including its graphics and targeting parameters. | 1 | `{ . . . }` |
| [`CatPartsSizeScale`](./Passives_and_Statuses.md#object-catpartssizescale) | Object  | A multiplier for the size of specific cat parts (e.g., head, body). | 1 | `{ . . . }` |
| [`CaveCatDad`](./Engine_StatusAndPassiveKeys.md#object-cavecatdad) | Object  | Configures a specific enemy cat type, including its graphics, name, and custom data. | 1 | `{ . . . }` |
| `CaveWomanBirthControl` | Integer | If true, restricts or controls the spawning of additional units via birth mechanics. | 1 | `1` |
| [`CerberubsAggroTargetBehavior`](./Passives_and_Statuses.md#object-cerberubsaggrotargetbehavior) | Object  | Defines the default and alert forms used by Cerberubs when changing aggro behavior. | 1 | `{ . . . }` |
| [`CerberubsStraightReaction`](./Engine_StatusAndPassiveKeys.md#object-cerberubsstraightreaction) | Object  | Defines a specific attack ability with a straight-line projectile and configurable area of effect. | 1 | `{ . . . }` |
| `ChampionUpgradeNextMinion` | Integer | The number of champion upgrades applied to the next spawned minion. | 1 | `1` |
| [`chance`](./Enums.md#enum-chance) | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| `ChanceToAmbush` | Integer | The percentage chance for the unit to ambush an enemy. | 1 | `25%` |
| [`ChanceToForceEvent`](./Passives_and_Statuses.md#object-chancetoforceevent) | Object  | Defines the chance and the specific event to force to occur. | 1 | `{ . . . }` |
| [`ChanceToFormChangeOnAbilityDamage`](./Passives_and_Statuses.md#object-chancetoformchangeonabilitydamage) | Object  | A chance to transform into a different form when damaged by an ability. | 1 | `{ . . . }` |
| [`ChangeTileUnderCharacterAtStart`](./Enums.md#enum-changetileundercharacteratstart) | Enum | Specifies the tile type to change the tile under the character to at the start of battle. | 1 | `GlassTile` |
| `ChaosBossFlipMidTeleport` | Integer | If set to a non-zero number, causes the chaos boss to flip direction mid-teleport. | 1 | `1` |
| `ChaosBossFormChange` | Integer | If set to a non-zero number, triggers a chaos boss form change. | 1 | `1` |
| [`ChaosBossFormChangeGuide`](./Passives_and_Statuses.md#object-chaosbossformchangeguide) | Object  | Defines active and passive piece sets and a health threshold for the Chaos boss's form change pattern. | 1 | `{ . . . }` |
| [`ChaosBossPieces`](./Passives_and_Statuses.md#object-chaosbosspieces) | Object  | Defines the list of active and passive piece tags for the Chaos boss fight. | 1 | `{ . . . }` |
| [`ChaosHeadDropIn`](./Passives_and_Statuses.md#object-chaosheaddropin) | Object  | Defines the tag, spawn ability, and music for the Chaos head's drop-in sequence. | 1 | `{ . . . }` |
| [`CharacterTypeGainsStatusAtBattleStart`](./Miscellaneous.md#object-charactertypegainsstatusatbattlestart) | Object  | Defines status effects applied to characters with a specific tag at the start of a battle. | 1 | `{ . . . }` |
| `CharismaIsMaxStat` | Integer | Treats the Charisma stat as the character's maximum stat for calculations. | 1 | `1` |
| `CharmedFacingForceAttack` | Integer | If set to a non-zero number, the charmed target is forced to attack the direction they are facing. | 1 | `1` |
| [`CharmedLeech`](./Engine_StatusAndPassiveKeys.md#object-charmedleech) | Object  | Defines a charmed version of the Leech familiar, including its variant and graphics. | 1 | `{ . . . }` |
| [`CharmedPooter`](./Engine_StatusAndPassiveKeys.md#object-charmedpooter) | Object  | Defines a charmed version of the Pooter familiar, including its variant, faction, and properties. | 1 | `{ . . . }` |
| [`CharmedReaper`](./Engine_StatusAndPassiveKeys.md#object-charmedreaper) | Object  | Defines a charmed version of the Reaper familiar, including its variant, faction, and properties. | 1 | `{ . . . }` |
| `CharmImmunity` | Integer | If true, the unit is immune to the Charmed status effect. | 1 | `1` |
| `choose_favorite_cat` | Variable | A variable referencing the selection of the player's favorite cat. | 1 ||
| [`Chubs`](./Engine_StatusAndPassiveKeys.md#object-chubs) | Object  | Defines the Chubs enemy or summon type, including its properties and abilities. | 1 | `{ . . . }` |
| [`ChubsGoop`](./Engine_StatusAndPassiveKeys.md#object-chubsgoop) | Object  | Defines the specific attack ability for Chubs, using a straight-shot template with no mana cost. | 1 | `{ . . . }` |
| [`ChubsRage`](./Engine_StatusAndPassiveKeys.md#object-chubsrage) | Object  | Defines the self-buff ability for Chubs, typically applying a rage animation and stat increases. | 1 | `{ . . . }` |
| `ClearDefaultDebris` | Integer | If true, removes all default debris from the battlefield. | 1 | `1` |
| `ClearFinalBossBattlefield` | Integer | If set to a non-zero number, clears the battlefield during the final boss fight. | 1 | `1` |
| `CloneWeaponTemp` | Integer | The number of turns the cloned weapon persists before being removed. | 1 | `1` |
| `CockroachSwarm` | Integer | If true, the unit spawns as a Cockroach Swarm, with its specific mechanics and effects. | 1 | `1` |
| [`CoinTossBounce`](./Enums.md#enum-cointossbounce) | Enum | Specifies the ability triggered when the coin lands on its edge after a bounce. | 1 | `X` |
| [`Conditional_Flying`](Engine_Uncategorized_Resources.md#conditional_flying) | Object | Defines a conditional block that applies effects or actions only to flying units. | 1 | `{ . . . }` |
| [`Conditional_ManaThreshold`](./Miscellaneous.md#object-conditional_manathreshold) | Object  | Defines a conditional block that applies effects only if a unit's mana meets a specified threshold. | 1 | `{ . . . }` |
| [`Conditional_SourceHasTag`](./Passives_and_Statuses.md#object-conditional_sourcehastag) | Object  | Defines a conditional block that applies effects only if the source of the effect has a specified tag. | 1 | `{ . . . }` |
| [`Conditional_Tiny`](Engine_Uncategorized_Resources.md#conditional_tiny) | Object | Defines a conditional block that applies effects only to tiny-sized units. | 1 | `{ . . . }` |
| [`ConfusionEffectOnTaggedAbilities`](./Enums.md#enum-confusioneffectontaggedabilities) | Enum | Specifies the type of ability tag (e.g., consumable) that triggers a confusion effect when used. | 1 | `consumable` |
| [`ConjureSingleUseBonusAbility`](./Enums.md#enum-conjuresingleusebonusability) | Enum | Specifies the bonus ability to conjure for single use (e.g., 'random' for a random one). | 1 | `random` |
| `ConsumablesMeleeRange` | Integer | Causes consumable items to have a melee range instead of their default range. | 1 | `1` |
| [`ConvertDamageToScaledStatus`](./Passives_and_Statuses.md#object-convertdamagetoscaledstatus) | Object  | Converts a portion of incoming damage into a specified status effect with a given number of stacks. | 1 | `{ . . . }` |
| [`CounterAttackAfterEnemyCastSpell`](./Enums.md#enum-counterattackafterenemycastspell) | Enum | Specifies the ability the unit uses to counterattack after an enemy casts a spell. | 1 | `Telekinesis` |
| `CounterNextAttacks` | Integer | The number of incoming attacks the unit will counterattack. | 1 | `2` |
| [`CraterCreeperOut`](./Engine_StatusAndPassiveKeys.md#object-cratercreeperout) | Object  | Defines the specific enemy type Crater Creeper Out, including its graphics and spawn offset. | 1 | `{ . . . }` |
| `CrowAttackLink` | Integer | If 1, allows this unit's attacks to chain or link to nearby enemies like a crow. | 1 | `1` |
| `CurrentWeaponAddElectricElement` | Integer | The number of turns the current weapon gains the electric element. | 1 | `1` |
| [`CyborgTurns`](./Passives_and_Statuses.md#object-cyborgturns) | Object  | Defines the number of extra turns controlled by AI and their timing for a Cyborg unit. | 1 | `{ . . . }` |
| `DamageFromBehindOnly` | Integer | If 1, the unit can only be damaged when attacked from behind. | 1 | `1` |
| [`DamageIfDidntUseSpecificAbility`](./Passives_and_Statuses.md#object-damageifdidntusespecificability) | Object  | Deals a specified amount of damage if the unit did not use a designated ability on its previous turn. | 1 | `{ . . . }` |
| `DamageWeapon` | Integer | The amount of durability damage dealt to the equipped weapon. | 1 | `1` |
| [`DarkOneStrike`](./Engine_StatusAndPassiveKeys.md#object-darkonestrike) | Object  | Defines a specific powerful attack ability for the Dark One enemy. | 1 | `{ . . . }` |
| [`DeathwormUnderground`](./Enums.md#enum-deathwormunderground) | Enum | Specifies the ability triggered when the Deathworm emerges from underground. | 1 | `DeathWormEat` |
| [`DecoyExplode`](./Engine_StatusAndPassiveKeys.md#object-decoyexplode) | Object  | Defines the explosion effect for a decoy unit. | 1 | `{ . . . }` |
| `DecoySwapper` | Integer | If true, the decoy swaps places with the source when spawned. | 1 | `1` |
| `DelayedPain` | Integer | The number of stacks of DelayedPain applied, dealing damage after a delay. | 1 | `1` |
| [`DelayedWindCone`](./Passives_and_Statuses.md#object-delayedwindcone) | Object  | An object containing parameters for a delayed wind cone, such as damage and distance. | 1 | `{ . . . }` |
| `DeleteInanimateObjectsChance` | Integer | The percentage chance per tick to delete all inanimate objects on the battlefield. | 1 | `25%` |
| `DeleteTraps` | Integer | If true, removes all traps from the map. | 1 | `1` |
| `DemonicGlyph_Bounce` | Integer | The weight for the demonic glyph of bounce, or its configuration. | 1 | `1` |
| `DemonicGlyph_Fire` | Integer | The weight for the demonic glyph of fire, or its configuration. | 1 | `1` |
| `DemonicGlyph_Movement` | Integer | The weight for the demonic glyph of movement, or its configuration. | 1 | `1` |
| `DemonicGlyphStealer` | Integer | If 1, the unit can steal demonic glyphs from other units. | 1 | `1` |
| [`DestroyerShieldBash`](./Engine_StatusAndPassiveKeys.md#object-destroyershieldbash) | Object  | Defines the shield bash ability for the Destroyer enemy type. | 1 | `{ . . . }` |
| `DestroyNeckArmor` | Integer | If true, destroys the target's neck armor slot. | 1 | `1` |
| [`Diabetes`](./Passives_and_Statuses.md#object-diabetes) | Object  | Defines the Diabetes disorder, including its name, description, and associated passive effects. | 1 | `{ . . . }` |
| [`DiceBehavior`](./Passives_and_Statuses.md#object-dicebehavior) | Object  | Defines the dice size and knockback damage for the Dice enemy. | 1 | `{ . . . }` |
| [`DicerArt`](./Arrays.md#array-dicerart) | Array | An array of art offset values for the Dicer enemy. | 1 | `[59 52 65 50 54 63 64]` |
| [`DiesToPiercingAndSpikes`](./Passives_and_Statuses.md#object-diestopiercingandspikes) | Object  | Makes the unit take lethal damage from piercing attacks and spike terrain. | 1 | `{ . . . }` |
| `DieWhenOnlyGolemsLeft` | Integer | If 1, the unit dies when only golem-type allies remain on the field. | 1 | `1` |
| `DieWhenSpawnerDies` | Integer | If 1, the unit dies when its spawner unit dies. | 1 | `1` |
| [`Digest`](./Engine_StatusAndPassiveKeys.md#object-digest) | Object  | Defines the digestion mechanic, typically applied to units that swallow others. | 1 | `{ . . . }` |
| [`DinoLegAnimation`](./Enums.md#enum-dinoleganimation) | Enum | Specifies the animation trigger for the dinosaur leg (e.g., 'poop' for the poop animation). | 1 | `poop` |
| `DisableSpells` | Integer | If 1, the unit cannot cast spells. | 1 | `1` |
| `Disguised` | Integer | If true, the unit is disguised, appearing as a different faction or model. | 1 | `1` |
| [`DisguisedTrapper`](./Enums.md#enum-disguisedtrapper) | Enum | Specifies the passive used when disguised as a trapper, e.g. FearMelee. | 1 | `FearMelee` |
| `DisplayBuddyCatOnSpawn` | Integer | The number of buddy cat objects to display when the unit spawns. | 1 | `3` |
| `DissolveRandomArmorPiece` | Integer | If true, destroys a random armor piece (head, body, neck) on the target. | 1 | `1` |
| `DivineShieldPickup` | Integer | The number of divine shield charges granted on pickup. | 1 | `1` |
| `DodgeChanceWithBlindSpot` | Integer | The percentage chance to dodge attacks while a blind spot condition is active. | 1 | `25%` |
| [`DodgeWhenTargeted`](./Passives_and_Statuses.md#object-dodgewhentargeted) | Object  | An object defining the ability and effects triggered when the unit is targeted for an attack. | 1 | `{ . . . }` |
| `DoubleCast` | Integer | The number of double-cast stacks, allowing a spell to be cast twice. | 1 | `1` |
| `DoubleCastSpellIfManaCostUnderThreshold` | Integer | If a spell's mana cost is under this threshold, it will be cast twice. | 1 | `3` |
| `DoubleCastSpellsEachTurn_Status` | Integer | The number of turns the unit gains Double Cast for spells each turn. | 1 | `1` |
| `DoubleCastSpellThisTurn` | Integer | If non-zero, grants the unit a double cast effect for spells this turn. | 1 | `1` |
| [`DoubleCastTaggedSpells`](./Enums.md#enum-doublecasttaggedspells) | Enum | Specifies the spell tag (e.g., musical) that causes spells to be cast twice. | 1 | `musical` |
| `DoubleReceivedNegativeStatus` | Integer | If true, the unit receives double the stacks of negative status effects applied to it. | 1 | `1` |
| `DoubleReceivedPositiveStatus` | Integer | If true, the unit receives double the stacks of positive status effects applied to it. | 1 | `1` |
| `DrainAllyCatsForFleshGolem` | Integer | The amount of health drained from ally cats to heal the Flesh Golem. | 1 | `7` |
| [`DropAsFamiliarOnTookDamage`](./Enums.md#enum-dropasfamiliarontookdamage) | Enum | Specifies the familiar type to be dropped when the unit takes damage. | 1 | `PhantomMaskRock` |
| [`DropSoulJarOnDeath`](./Enums.md#enum-dropsouljarondeath) | Enum | Specifies the type of soul jar to be dropped when the unit dies. | 1 | `SoulJar_Full` |
| `DuplicateRandomEquippedItem` | Integer | If true, creates a copy of a random equipped item. | 1 | `1` |
| `DustCloudBehavior` | Integer | An integer flag that controls the behavior mode of a dust cloud entity. | 1 | `1` |
| `Dybbuk1HPTracker` | Integer | A flag indicating the unit tracks that it has 1 HP remaining for Dybbuk possession mechanics. | 1 | `1` |
| `DybbukManualExitTag` | Variable | A variable referencing the tag that allows a Dybbuk unit to manually exit its host. | 1 ||
| [`DybbukPossessionFallback`](./Passives_and_Statuses.md#object-dybbukpossessionfallback) | Object  | An object specifying the fallback form and exit ability used when possession fails. | 1 | `{ . . . }` |
| [`EatShit`](./Engine_StatusAndPassiveKeys.md#object-eatshit) | Object  | Defines a specific ability or effect related to consuming or eating feces. | 1 | `{ . . . }` |
| `ElectricArcs` | Integer | The number of electric arcs emitted by this unit. | 1 | `1` |
| [`element`](./Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 1 | `Electric`<br>`Fire`<br>`Gravity` |
| [`ElementWeakness`](./Enums.md#enum-elementweakness) | Enum | Determines which element the unit is weak to, e.g. Fire. | 1 | `Fire` |
| `EliteUpgradeNextMinion` | Integer | The number of elite upgrades applied to the next spawned minion. | 1 | `1` |
| `end_of_round` | Boolean | If true, the effect triggers at the end of the round instead of at the start of the turn. | 1 | `true` |
| `enemies` | Variable | A variable representing the group of enemy units. | 1 ||
| `EnrageOnDamage` | Integer | If set to 1, the unit gains enrage stacks when taking damage. | 1 | `1` |
| [`EnterMount`](./Enums.md#enum-entermount) | Enum | Specifies the name of the mount status to apply to the unit. | 1 | `enter` |
| `EraseSpawnCoins` | Integer | If set to 1, the unit erases spawn coins from the map on spawn. | 1 | `1` |
| [`euphoric`](./Miscellaneous.md#object-euphoric) | Object  | Defines the facial expression configuration for the euphoric emotional state of a unit. | 1 | `{ . . . }` |
| `EventBounterHunterPassive` | Integer | A flag enabling the event bounty hunter passive behavior. | 1 | `1` |
| `exclude_self` | Boolean | If true, the effect does not apply to the source unit itself. | 1 | `false` |
| [`ExcludeFromEvents`](./Enums.md#enum-excludefromevents) | Enum | Specifies the event type (e.g., Tragedy) that this unit is excluded from participating in. | 1 | `Tragedy` |
| `ExhaustionRoundChange` | Integer | The number of rounds added to the exhaustion counter. | 1 | `3` |
| `ExistUntilIdleUpkeep` | Integer | If true, the entity persists until the source unit enters idle upkeep. | 1 | `1` |
| `ExplodeCharacter_DeathBloom` | Integer | The amount of damage dealt by the DeathBloom explosion. | 1 | `5` |
| `ExplodeCharacter_DeathBloom2` | Integer | The amount of damage dealt by the DeathBloom2 explosion. | 1 | `5` |
| `ExtraInjuryOnDeath` | Integer | The number of additional injuries inflicted upon death. | 1 | `1` |
| [`ExtraTurnsPerTaggedUnit`](./Enums.md#enum-extraturnspertaggedunit) | Enum | Specifies the tag of units that grant extra turns when present. | 1 | `sprout` |
| [`face_EatNeverstone`](./Engine_StatusAndPassiveKeys.md#object-face_eatneverstone) | Object  | Defines the ability used when the unit eats a Neverstone, typically a self-buff. | 1 | `{ . . . }` |
| [`face_LeechBrood`](./Engine_StatusAndPassiveKeys.md#object-face_leechbrood) | Object  | Defines the ability used when the unit activates Leech Brood, typically a self-buff or attack. | 1 | `{ . . . }` |
| [`FaceAwayLastDamage`](./Passives_and_Statuses.md#object-faceawaylastdamage) | Object  | An object defining animation overrides for the last damage event when the unit faces away. | 1 | `{ . . . }` |
| `FactionDisguiseSource` | Integer | If true, the unit adopts the faction of the source unit for disguise. | 1 | `1` |
| `FastKnockback` | Integer | The number of tiles the target is knocked back with fast animation. | 1 | `4` |
| [`FinalBossBeamQueue`](./Passives_and_Statuses.md#object-finalbossbeamqueue) | Object  | An object defining the queue of beam ability actions for the final boss form. | 1 | `{ . . . }` |
| [`FinalBossBecomeTheChild`](./Passives_and_Statuses.md#object-finalbossbecomethechild) | Object  | An object defining the transformation and environment changes when the boss becomes TheChild. | 1 | `{ . . . }` |
| [`FinalBossHitCountdownBoris`](./Passives_and_Statuses.md#object-finalbosshitcountdownboris) | Object  | An object defining the countdown status effect properties for the Boris phase, including stacks, icons, and forced abilities. | 1 | `{ . . . }` |
| [`FinalBossHitCountdownExplosive`](./Passives_and_Statuses.md#object-finalbosshitcountdownexplosive) | Object  | An object defining the countdown status effect properties for the Explosive phase, including stacks, icons, and forced abilities. | 1 | `{ . . . }` |
| [`FinalBossHitCountdownHoly`](./Passives_and_Statuses.md#object-finalbosshitcountdownholy) | Object  | An object defining the countdown status effect properties for the Holy phase, including stacks and icons. | 1 | `{ . . . }` |
| [`FinalBossPupils`](./Passives_and_Statuses.md#object-finalbosspupils) | Object  | An object configuring the visual tracking of the final boss's pupils, including radius, head position, and teleport tracking. | 1 | `{ . . . }` |
| `FinalBossQueueBeam` | Integer | If true, queues the final boss beam attack. | 1 | `1` |
| [`FinalBossShieldHealth`](./Passives_and_Statuses.md#object-finalbossshieldhealth) | Object  | An object defining the shield health thresholds per visual state for the final boss. | 1 | `{ . . . }` |
| [`FinalBossSyncAnimations`](./Passives_and_Statuses.md#object-finalbosssyncanimations) | Object  | An object defining animation synchronization with another character, including form change abilities. | 1 | `{ . . . }` |
| [`FireArmor`](./Engine_StatusAndPassiveKeys.md#object-firearmor) | Integer / Object  | The number of Fire Armor stacks providing damage reflection. | 1 | `{ . . . }`<br>`1` |
| [`FireArmor2`](./Engine_StatusAndPassiveKeys.md#object-firearmor2) | Integer / Object  | The number of Fire Armor2 stacks (likely a variant). | 1 | `{ . . . }`<br>`1` |
| [`FireExtinguish_Steam`](#object-fireextinguish_steam) | Variable | Defines the particle effect for steam created when fire is extinguished. | 1 ||
| `FireflySwarm` | Integer | The number of fireflies in the swarm effect. | 1 | `2` |
| `FistOfFateUniqueEnemyTracker` | Integer | Increases the damage tracking counter for unique enemies hit by Fist of Fate. | 1 | `1` |
| `FlingObjectsOnTop` | Integer | The number of objects to fling on top of this unit. | 1 | `8` |
| [`FlushmasterCelebration`](./Enums.md#enum-flushmastercelebration) | Enum | Specifies the celebration animation or effect name used by the Flushmaster. | 1 | `celebrate` |
| [`FlyBuff`](#object-flybuff) | Variable | Defines the visual effect or buff for the Fly familiar. | 1 ||
| `Fog` | Integer | When an integer, the intensity of fog; when an object, defines the fog particle effect. | 1 | `1` |
| `ForceCollectsPickups` | Integer | If true, the unit automatically collects nearby pickups. | 1 | `1` |
| `ForceDodgeEverything` | Integer | If set to 1, the unit will always dodge all incoming attacks. | 1 | `1` |
| [`ForceImmediateMoveAndAttack`](./Miscellaneous.md#object-forceimmediatemoveandattack) | Object  | An object that forces the unit to instantly move toward the target and perform a specified ability attack. | 1 | `{ . . . }` |
| `ForceMoveAndAttack` | Integer | If true, forces the target to move and attack its nearest enemy. | 1 | `1` |
| `ForceTransferWeapon` | Integer | If true, forces the weapon to be transferred to the target. | 1 | `1` |
| [`ForceUseAbilityOnTarget`](./Miscellaneous.md#object-forceuseabilityontarget) | Object  | Defines a chance to force the unit to use a specified ability on the target. | 1 | `{ . . . }` |
| [`FormChangeWhenBuddyDies`](./Enums.md#enum-formchangewhenbuddydies) | Enum | Specifies the form name the unit changes into when its buddy dies. | 1 | `Rage` |
| [`FrankBolts`](./Passives_and_Statuses.md#object-frankbolts) | Integer / Object  | The number of Frank Bolts applied or available. | 1 | `{ . . . }`<br>`1` |
| `FreeFirstCastAndAfterSpendMana` | Integer | If set to 1, the first cast of the ability and each cast after spending mana costs no resources. | 1 | `1` |
| `FreeFirstCastEachMatch` | Integer | If set to 1, the first cast of the ability each match costs no resources. | 1 | `1` |
| `FreeSpellsAtFullMana` | Integer | The number of spells that cost no mana when mana is full. | 1 | `1` |
| `FrontstabBasicAttackCritChance` | Integer | The percentage chance for basic attacks to critically hit when attacking from the front. | 1 | `100%` |
| `FullBlockEverything` | Integer | If set to 1, the unit fully blocks all incoming damage. | 1 | `1` |
| `FullBlockEverythingTo0Damage` | Integer | If set to 1, the unit reduces all incoming damage to 0. | 1 | `1` |
| [`FurnitureStats`](./Passives_and_Statuses.md#object-furniturestats) | Object  | Defines the Comfort, Stimulation, and Appeal stats of furniture. | 1 | `{ . . . }` |
| `GasCanBehavior` | Integer | An integer flag that controls the behavior mode of a gas can entity. | 1 | `1` |
| `GasCloudBehavior2` | Integer | An integer flag that controls a secondary behavior mode of a gas cloud entity. | 1 | `2` |
| `GeminiTwin` | Integer | If set to 1, this unit is the twin in a Gemini pair. | 1 | `1` |
| [`GirlDino`](./Engine_StatusAndPassiveKeys.md#object-girldino) | Object  | Defines the Girl Dino creature or its ability. | 1 | `{ . . . }` |
| [`GirlDinoCry`](./Engine_StatusAndPassiveKeys.md#object-girldinocry) | Object  | Defines the cry ability of Girl Dino, typically a self-buff with a cry animation. | 1 | `{ . . . }` |
| `GiveBoundItemToTarget` | Integer | If true, gives the source's bound item to the target. | 1 | `1` |
| `GlobalFamiliarDamageBoost` | Integer | The amount of damage boost applied to all familiars globally. | 1 | `1` |
| `GlobalFamiliarMoveBoost` | Integer | The amount of movement boost applied to all familiars globally. | 1 | `1` |
| [`GlobalFlowerTrapperAura`](./Passives_and_Statuses.md#object-globalflowertrapperaura) | Object  | Defines an aura that applies Tangled to enemies with specified stacks and probability. | 1 | `{ . . . }` |
| `GlobalHealthRegenAura` | Integer | The amount of health regenerated per turn to all units in range. | 1 | `3` |
| `GlobalManaDrainAura` | Integer | The amount of mana drained per turn from all units in range. | 1 | `-1` |
| [`GlobalMeleeRevengeDamage`](./Passives_and_Statuses.md#object-globalmeleerevengedamage) | Object  | Defines revenge damage properties (e.g., knockback) when hit by a melee attack. | 1 | `{ . . . }` |
| [`GlobalSpawnCharacter`](./Enums.md#enum-globalspawncharacter) | Enum | Specifies the name of a character to spawn globally. | 1 | `MegaGuppy` |
| `GoopImmunity` | Integer | If set to 1, the unit is immune to goop status effects. | 1 | `1` |
| `grub_familiar` | Variable | Defines the Grub familiar's properties. | 1 ||
| [`Guillotina2Body`](./Engine_StatusAndPassiveKeys.md#object-guillotina2body) | Object  | Defines the Guillotina's second body ability or body part. | 1 | `{ . . . }` |
| [`Guillotina2Head`](./Engine_StatusAndPassiveKeys.md#object-guillotina2head) | Object  | Defines the Guillotina's second head ability or head part. | 1 | `{ . . . }` |
| [`Guillotina3Body`](./Engine_StatusAndPassiveKeys.md#object-guillotina3body) | Object  | Defines the Guillotina's third body ability or body part. | 1 | `{ . . . }` |
| [`Guillotina3Head`](./Engine_StatusAndPassiveKeys.md#object-guillotina3head) | Object  | Defines the Guillotina's third head ability or head part. | 1 | `{ . . . }` |
| `GuillotinaDeathHead` | Integer | If set to 1, the unit spawns a head object upon death via guillotine. | 1 | `1` |
| [`HarpoonTrapPassive`](./Enums.md#enum-harpoontrappassive) | Enum | Specifies the ability name used when the harpoon trap is triggered. | 1 | `HarpoonTrapPull` |
| [`HCHumanDie`](./Engine_StatusAndPassiveKeys.md#object-hchumandie) | Object  | Defines the human die animation and buff when a human dies. | 1 | `{ . . . }` |
| [`HealNeighborsEachTurn`](./Passives_and_Statuses.md#object-healneighborseachturn) | Object  | An object defining the amount and target filtering for healing adjacent units each turn. | 1 | `{ . . . }` |
| `HealPercentMaxHP` | Integer | The percentage of max HP healed (e.g., 100 for full heal). | 1 | `100` |
| `HealTo` | Integer | The target HP percentage to heal the unit to (e.g., '50%' for half max HP). | 1 | `50%` |
| `HeatWave` | Integer | When an integer, the intensity of the heat wave; when an object, defines the visual effects or status properties. | 1 | `1` |
| `HeavyHits` | Integer | The number of Heavy Hits stacks increasing attack impact. | 1 | `1` |
| [`HemBounce`](./Engine_StatusAndPassiveKeys.md#object-hembounce) | Object  | Defines the Hem's bounce melee attack ability. | 1 | `{ . . . }` |
| `HiddenDoomed` | Integer | The number of stacks of a hidden doomed status effect applied to the unit. | 1 | `2` |
| [`HideEquipment`](./Enums.md#enum-hideequipment) | Enum | Specifies which equipment slot is visually hidden. | 1 | `neck` |
| `HideSomeHudStuff` | Integer | If set to 1, hides certain HUD elements. | 1 | `1` |
| [`HitlerExecute`](./Passives_and_Statuses.md#object-hitlerexecute) | Object  | An object defining the tag, ability, and health threshold for executing a clone. | 1 | `{ . . . }` |
| [`HPAltStates`](./Passives_and_Statuses.md#object-hpaltstates) | Object  | An object defining alternate visual frames based on current HP thresholds. | 1 | `{ . . . }` |
| `Hypomania` | Integer | When an integer, the stacks of Hypomania; when an object, defines the Hypomania disorder status. | 1 | `3` |
| `IceBlockBehavior` | Integer | An integer flag that controls the behavior mode of an ice block entity. | 1 | `1` |
| [`IDSprout`](./Engine_StatusAndPassiveKeys.md#object-idsprout) | Object  | Defines the ID Sprout spawn ability. | 1 | `{ . . . }` |
| `IgnoreDebuffs` | Integer | If true, the effect ignores debuffs on the target. | 1 | `1` |
| [`IncAuxCounterCycle`](./Miscellaneous.md#object-incauxcountercycle) | Object  | An object containing parameters for incrementing an auxiliary counter with a change and maximum value. | 1 | `{ . . . }` |
| `IncreaseCumulativeBlastDamage` | Integer | If true, increases the cumulative blast damage counter. | 1 | `1` |
| `IncreaseItemAuxOnKill` | Integer | If true, increases the item's aux counter on kill. | 1 | `1` |
| `InheritSpawnerStats` | Integer | If set to 1, the unit inherits the stats of its spawner. | 1 | `1` |
| [`insane`](./Miscellaneous.md#object-insane) | Object  | Defines the 'insane' facial expression with eyebrow and mouth positions. | 1 | `{ . . . }` |
| `InsertIntoBackgroundPlaceholder` | Integer | If set to 1, the unit is inserted into a background placeholder slot. | 1 | `1` |
| `InterchangeDisabler` | Integer | If set to 1, prevents the unit from being interchanged with another unit. | 1 | `1` |
| `InterchangeMoveActPoints` | Integer | If true, swaps the unit's remaining move points and action points. | 1 | `1` |
| `InvertBrainFaction` | Integer | If set to 1, inverts the unit's faction (e.g., allies become enemies). | 1 | `1` |
| `Invulnerable` | Integer | The number of Invulnerable stacks, making the unit immune to damage. | 1 | `1` |
| `JesterLevelUpRerolls` | Integer | The number of additional rerolls granted when leveling up. | 1 | `1` |
| [`JohnnyNeedsWashing`](./Passives_and_Statuses.md#object-johnnyneedswashing) | Object  | An object specifying the form names for washed and unwashed states. | 1 | `{ . . . }` |
| [`JohnnyWasher`](./Enums.md#enum-johnnywasher) | Enum | Specifies the ability name used by the washer form to clean Johnny. | 1 | `BBTransformZealot` |
| `JudgementDay` | Integer | When an integer, the turn count or damage for Judgement Day; when an object, defines the weather status. | 1 | `25` |
| [`KnockbackIfCrit`](./Miscellaneous.md#object-knockbackifcrit) | Object  | Defines knockback properties applied when a critical hit occurs. | 1 | `{ . . . }` |
| [`LegacySpawnSavedCatIfExists`](./Enums.md#enum-legacyspawnsavedcatifexists) | Enum | Specifies the legacy saved cat ID to spawn if it exists in the save data. | 1 | `Legacy_Marshmallow_StolenCatID` |
| [`LennyCatDies`](./Engine_StatusAndPassiveKeys.md#object-lennycatdies) | Object  | Defines the ability triggered when Lenny the cat dies. | 1 | `{ . . . }` |
| [`LimitedTileTrail`](./Enums.md#enum-limitedtiletrail) | Enum | Specifies the type of tile left behind as a trail when the unit moves. | 1 | `FlowerTile` |
| `LimitSelfKnockbackDamage` | Integer | The maximum amount of damage taken from self-inflicted knockback. | 1 | `1` |
| [`LockOrientationFaceTile`](./Arrays.md#array-lockorientationfacetile) | Array | A tile coordinate [x y] that the unit's orientation is locked to face. | 1 | `[0 0]` |
| `LowGravityKnockbackBoost` | Integer | The multiplier or bonus to knockback force under low gravity. | 1 | `1` |
| `LowGravityRangeBoost` | Integer | The increase in attack range under low gravity. | 1 | `2` |
| `MadnessChanceOnTurnBegin` | Integer | The chance (as a multiplier) to inflict Madness status at the start of each turn in the next battle. | 1 | `2` |
| `MakeWeaponUnbreakable` | Integer | If true, makes the equipped weapon unbreakable. | 1 | `1` |
| [`ManaGainRange`](./Miscellaneous.md#object-managainrange) | Object  | Defines the minimum and maximum mana gained per turn. | 1 | `{ . . . }` |
| `ManaStealToHealth` | Integer | The amount of mana stolen and converted to health (negative values may drain health). | 1 | `-1` |
| `ManglerAttack` | Integer | If true, the attack triggers the Mangler's attack pattern. | 1 | `1` |
| [`ManglerEnrage`](./Engine_StatusAndPassiveKeys.md#object-manglerenrage) | Object  | Defines the enrage ability of the Mangler monster. | 1 | `{ . . . }` |
| [`ManglerMonsterDashAttack`](./Engine_StatusAndPassiveKeys.md#object-manglermonsterdashattack) | Object  | Defines the dash attack ability of the Mangler monster. | 1 | `{ . . . }` |
| [`ManglerMonsterPassive`](./Enums.md#enum-manglermonsterpassive) | Enum | Specifies the ability name used for the Mangler monster's dash attack. | 1 | `ManglerMonsterDashAttack` |
| `ManglerShuffle` | Boolean | If true, the order of effects in this damage instance is randomized before application. | 1 | `false` |
| [`ManglersMonster`](./Engine_StatusAndPassiveKeys.md#object-manglersmonster) | Object  | Defines the Mangler monster's properties. | 1 | `{ . . . }` |
| `MassAttackThis` | Integer | The number of additional targets this attack hits via the Mass Attack mechanic. | 1 | `1` |
| `MaxAccuracy` | Integer | The maximum allowed accuracy percentage for the unit. | 1 | `1` |
| `MaxStartingMana` | Integer | The maximum amount of mana the unit starts with. | 1 | `1` |
| `Meaty` | Integer | The number of Meaty stacks increasing health or size. | 1 | `1` |
| [`MechExplode`](./Engine_StatusAndPassiveKeys.md#object-mechexplode) | Object  | Defines the explosion ability of a mech unit. | 1 | `{ . . . }` |
| [`MegaDinoDropController`](./Passives_and_Statuses.md#object-megadinodropcontroller) | Object  | An object defining the abilities and stable leg count for the Mega Dino's leg drop sequence. | 1 | `{ . . . }` |
| [`MegaFart`](./Engine_StatusAndPassiveKeys.md#object-megafart) | Object  | Defines the Mega Fart ability. | 1 | `{ . . . }` |
| [`MegaGuppy_SummonTheChild`](./Engine_StatusAndPassiveKeys.md#object-megaguppy_summonthechild) | Object  | Defines the ability to summon the child from Mega Guppy. | 1 | `{ . . . }` |
| [`MergeDamageInstance`](./Miscellaneous.md#object-mergedamageinstance) | Object  | Specifies parameters to merge multiple damage instances into one, controlling hit animation and instant pop behavior. | 1 | `{ . . . }` |
| `MeteorShower` | Integer | The chance (as a percentage) for a meteor shower to occur on a given turn. | 1 | `25%` |
| `MimicMetronome` | Integer | The number of random abilities the Metronome effect selects from this unit's ability pool. | 1 | `1` |
| `ModelingClayPassive` | Integer | If set to 1, enables the passive that duplicates the equipped item on the unit. | 1 | `1` |
| [`ModularPickup`](./Passives_and_Statuses.md#object-modularpickup) | Object  | An object defining the effects and sounds triggered when the unit is picked up. | 1 | `{ . . . }` |
| [`MonkCatReactionAbilities`](./Passives_and_Statuses.md#object-monkcatreactionabilities) | Object  | A set of mappings from action types (move, attack, spell, trinket) to the corresponding ability IDs the MonkCat will use for reactions. | 1 | `{ . . . }` |
| [`MoonHead_KillHands`](./Engine_StatusAndPassiveKeys.md#object-moonhead_killhands) | Object  | An object defining a targeted status effect applied when MoonHead kills an enemy with its hands. | 1 | `{ . . . }` |
| [`MoonHeadCrackedVisual`](./Enums.md#enum-moonheadcrackedvisual) | Enum | Specifies the visual state for the character's cracked head appearance. | 1 | `Cracked` |
| [`MotherGrowController`](./Passives_and_Statuses.md#object-mothergrowcontroller) | Object  | Controls the growth of tumors on The Mother, including the tumor object, damage type, damage amount, and whether it pierces defense when eating damage. | 1 | `{ . . . }` |
| `MotherTumorDebugForcePass` | Integer | If non-zero, forces the Mother Tumor boss to pass its turn, skipping its normal action. | 1 | `1` |
| [`MotherTumorPassive`](./Passives_and_Statuses.md#object-mothertumorpassive) | Object  | Defines the passive behavior for a MotherTumor, including the forms considered for pass/receive, the pass and receive animations, and the grow ability. | 1 | `{ . . . }` |
| [`Mount`](./Passives_and_Statuses.md#object-mount) | Object  | Defines the entering and ejecting abilities for a mountable unit, along with its death rattle ability. | 1 | `{ . . . }` |
| [`MoveAfterAnyAttemptedAttack`](./Passives_and_Statuses.md#object-moveafteranyattemptedattack) | Object  | Defines the movement behavior (weights and abilities) used after any attempted attack. | 1 | `{ . . . }` |
| [`MoveAwayWhenEnemyAdjacent`](./Passives_and_Statuses.md#object-moveawaywhenenemyadjacent) | Object  | Defines the movement behavior (move_ability, weights, and whether it triggers once per turn) when an enemy is adjacent. | 1 | `{ . . . }` |
| `MulticatHeads` | Integer | The number of additional heads the Multicat has. | 1 | `0` |
| `MultiplyCoinsOnBattleStart` | Integer | The multiplier applied to the unit's coin count at the start of battle. | 1 | `2` |
| `MultiplyReceivedHealing` | Integer | The multiplier applied to all healing the unit receives. | 1 | `2` |
| [`MultiSpawnOnDeath`](./Passives_and_Statuses.md#object-multispawnondeath) | Object  | Specifies the object to spawn and the range of number of objects to spawn on death. | 1 | `{ . . . }` |
| `MutateAfterXTurns` | Integer | The number of turns after which the character automatically mutates (or transforms). | 1 | `3` |
| `Muted` | Integer | The number of Muted stacks, disabling certain abilities. | 1 | `1` |
| `MuteDemonicGlyphDisplay` | Integer | If set to 1, suppresses the display of demonic glyphs on the character. | 1 | `1` |
| `NextAbilityHeals` | Integer | The number of stacks causing the next ability to heal instead of damage. | 1 | `1` |
| `NextActionLuckUp` | Integer | The number of stacks increasing luck for the next action. | 1 | `99` |
| [`NextBasicAttackCritsThisTurn`](./Miscellaneous.md#object-nextbasicattackcritsthisturn) | Object  | An object or number configuring the next basic attack to be a critical hit this turn. An object may contain stack, cant_miss, or piercing sub-keys. | 1 | `{ . . . }` |
| [`NextBattleStatusStacks`](./Miscellaneous.md#object-nextbattlestatusstacks) | Object  | An object specifying status effects and their stacks to be applied at the start of the next battle. Contains a "fights" counter and nested status keys. | 1 | `{ . . . }` |
| `NextDamageReduceAndHealAllies` | Integer | The number of stacks reducing next damage and healing nearby allies. | 1 | `1` |
| `NextTurnDoubleRangedDamage` | Integer | The number of stacks doubling ranged damage on the next turn. | 1 | `1` |
| [`NoHead`](./Engine_StatusAndPassiveKeys.md#object-nohead) | Object  | An object that replaces the unit's head graphics with a headless cat model and sets the enemy name. | 1 | `{ . . . }` |
| [`NonChampionFlySwarm`](./Engine_StatusAndPassiveKeys.md#object-nonchampionflyswarm) | Object  | An object defining a fly swarm that only spawns on non-champion units. | 1 | `{ . . . }` |
| `NonLethal` | Integer | If set to 1, damage dealt by the unit cannot kill enemies; it leaves them at 1 HP. | 1 | `1` |
| [`Nubs`](./Engine_StatusAndPassiveKeys.md#object-nubs) | Object  | An object defining a visual or mechanical replacement of the unit's limbs with stubs. | 1 | `{ . . . }` |
| [`NubsGoop`](./Engine_StatusAndPassiveKeys.md#object-nubsgoop) | Object  | An object defining a lobbed attack that costs 0 mana and fires goop. | 1 | `{ . . . }` |
| [`ObjectDetector`](./Passives_and_Statuses.md#object-objectdetector) | Object  | An object that grants a chance to detect a specific item (e.g., CharmedDip) when loot is evaluated. | 1 | `{ . . . }` |
| [`ObjectOnHitFullyEmpty`](./Enums.md#enum-objectonhitfullyempty) | Enum | Specifies the object (e.g., RandomArmorPickup) to spawn on the target when the attacker's inventory is completely empty. | 1 | `RandomArmorPickup` |
| [`Ornstein`](./Engine_StatusAndPassiveKeys.md#object-ornstein) | Object  | An object defining a passive or status effect mimicking Ornstein's behavior (e.g., charge attack). | 1 | `{ . . . }` |
| `OrthogonalAIDangerZone` | Integer | The range (in tiles) for the AI's orthogonal danger zone detection. | 1 | `10` |
| `OverHealToShield` | Integer | The amount of excess healing converted into temporary shield points. | 1 | `1` |
| `OverManaReducesManaCosts` | Integer | If set to 1, any mana the unit has above their maximum reduces the cost of abilities. | 1 | `1` |
| `OverrideMaxMana` | Integer | Sets the unit's maximum mana to this integer value, overriding the default. | 1 | `1` |
| `OverridePalette` | Integer | Forces the unit to use a specific color palette index. | 1 | `87` |
| `PackHunting` | Integer | If set to 1, enables pack hunting behavior for the character. | 1 | `1` |
| [`Paranoia`](./Enums.md#enum-paranoia) | Enum | Specifies the type of paranoid melee attack the unit will use instead of their normal attack. | 1 | `ParanoiaBasicMelee` |
| [`PassiveLevelScaledStatus`](./Passives_and_Statuses.md#object-passivelevelscaledstatus) | Object  | An object containing status effects whose values scale with the unit's level, using X as the level variable. | 1 | `{ . . . }` |
| [`PassiveWhileHasDurability`](./Passives_and_Statuses.md#object-passivewhilehasdurability) | Object  | An object containing passives that are active only while the item has remaining durability. | 1 | `{ . . . }` |
| [`PassiveWhileNotTakingTurn`](./Miscellaneous.md#object-passivewhilenottakingturn) | Object  | A nested passive object that is active only while the unit is not currently taking its turn. | 1 | `{ . . . }` |
| [`PassiveWhileShielded`](./Passives_and_Statuses.md#object-passivewhileshielded) | Object  | An object containing passives that are active only while the unit has a shield. | 1 | `{ . . . }` |
| `PercentHeal` | Integer | The percentage of max HP healed when this effect triggers. | 1 | `50` |
| `PermanentConfusion` | Number | If set to 1, the unit is permanently confused and cannot be cured. | 1 | `1` |
| `PermanentImmobile` | Integer | The permanent amount of immobility stacks applied. | 1 | `1` |
| `PermanentKitten` | Integer | If set to 1, the unit retains its kitten form permanently instead of aging. | 1 | `1` |
| `PermanentUpgradeRandomActiveOrPassive` | Integer | The number of random active or passive abilities permanently upgraded. | 1 | `1` |
| [`PersistentElement`](./Enums.md#enum-persistentelement) | Enum | Specifies the element type that this status effect permanently imbues (e.g., Holy). | 1 | `Holy` |
| `PhysicalAttacksMiss` | Integer | If set to 1, all physical attacks against the unit automatically miss. | 1 | `1` |
| `pickup` | Variable | A variable that marks an object as a pickup item that can be collected on the battlefield. | 1 ||
| `plant` | Variable | A variable that marks an object as a plantable item on the battlefield. | 1 ||
| [`PoolMetronome`](./Miscellaneous.md#object-poolmetronome) | Object  | An object containing a "pool" array of ability names that the Metronome effect can randomly select from. | 1 | `{ . . . }` |
| `PreEmptiveCounterNextAttacks` | Integer | The number of next incoming attacks that the unit will counter preemptively before they land. | 1 | `1` |
| [`PreventSpecificInjury`](./Enums.md#enum-preventspecificinjury) | Enum | Specifies a body part tag (e.g., 'int' for head) that cannot receive injuries. | 1 | `int` |
| [`QueueUseAbility`](./Enums.md#enum-queueuseability) | Enum | Specifies the ability ID to be used immediately after the current action resolves. | 1 | `Spider_GoInsane` |
| `RandomKnockbackDirection` | Integer | The number of random directions the target can be knocked back (e.g., 4 selects from 4 cardinal directions). | 1 | `4` |
| [`RandomPermanentStatsDistinct`](./Miscellaneous.md#object-randompermanentstatsdistinct) | Object  | An object defining a set of stat changes (positive and negative) that are randomly applied as permanent modifications. | 1 | `{ . . . }` |
| [`RandomWeatherEachFight`](./Arrays.md#array-randomweathereachfight) | Array | An array of weather types from which one is randomly selected at the start of each battle. | 1 ||
| `RealTimePressure_OneUnit` | Integer | The amount of real-time pressure (countdown) applied to the unit each turn. | 1 | `5` |
| [`ReceivedStatusReplacement`](./Arrays.md#array-receivedstatusreplacement) | Array | An array specifying a status that replaces another status when it would be applied (e.g., Sleep becomes SleepParalysis). | 1 | `[Sleep SleepParalysis]` |
| `ReclaimItemOnBreak` | Integer | If set to 1, the item returns to the inventory when it breaks instead of being lost. | 1 | `1` |
| `ReduceManaCostExcludeBrainstorm` | Integer | The number of stacks reducing mana cost, excluding Brainstorm. | 1 | `1` |
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
| [`ReloadOnElementalDamageReceived`](./Enums.md#enum-reloadonelementaldamagereceived) | Enum | Specifies the elemental type of damage that, when received, restores a charge. | 1 | `Holy` |
| `ReloadOnGainCoins` | Integer | If set to 1, restores a charge when coins are gained. | 1 | `1` |
| `ReloadOnGainDivineShield` | Integer | If set to 1, restores a charge when a Divine Shield is gained. | 1 | `1` |
| [`ReloadOnKillTagged`](./Enums.md#enum-reloadonkilltagged) | Enum | Specifies the tag of enemies that, when killed, restore a charge. | 1 | `rock` |
| `ReloadOnSpendMana` | Integer | If set to 1, restores a charge when mana is spent. | 1 | `1` |
| `ReloadOnUseAbilityWithManaCost` | Integer | Specifies the amount of mana cost that, when used, restores a charge. | 1 | `6` |
| `RemoteFlatLeech` | Integer | The flat amount of remote leech applied to the target on basic attack. | 1 | `1` |
| [`RemoveAmbientLightEffects`](./Enums.md#enum-removeambientlighteffects) | Float | The fade-out duration in seconds for ambient light effects. | 1 | `.5`<br>`4` |
| `RemoveExtraDispersedTurn` | Integer | If set to 1, the unit's turn order is not delayed by the 'Dispersed' status effect. | 1 | `1` |
| [`RemoveGlobalModifiers`](./Arrays.md#array-removeglobalmodifiers) | Array | List of global modifier names to remove upon death. | 1 | `[BloodRain]` |
| `RepairAllCondition` | Integer | If non-zero, fully repairs the condition of all equipped items. | 1 | `1` |
| [`ReplaceBlankTilesOnBattleStart`](./Enums.md#enum-replaceblanktilesonbattlestart) | Enum | Specifies a tile type (e.g., GlassTile) that replaces all blank tiles on the battle grid at the start of combat. | 1 | `GlassTile` |
| `RerollEnemy` | Integer | The number of times the target enemy is re-rolled (transformed into a new random enemy). | 1 | `1` |
| `RerollItemsOnBattleEnd` | Integer | If set to 1, all items in the unit's inventory are rerolled to new random items at the end of battle. | 1 | `1` |
| `ReturnDinoLegs` | Integer | If non-zero, returns the Dino Legs ability to the unit after it is consumed. | 1 | `1` |
| `RNGCannonRandomDamage` | Integer | The maximum random damage value for the RNG Cannon attack. | 1 | `100` |
| [`RockyArmorSalvage`](./Enums.md#enum-rockyarmorsalvage) | Float | A multiplier for the percentage of armor value salvaged when the unit takes damage. | 1 | `.75` |
| `RunWhenKittensDead` | Integer | If set to 1, causes the character to attempt to flee when all associated kittens are dead. | 1 | `1` |
| [`RunWhenLastPlayerCatIsCharmed`](./Passives_and_Statuses.md#object-runwhenlastplayercatischarmed) | Object  | Defines the behavior (including mid-turn decision allowance and legacy save key) for fleeing when the last player cat is charmed. | 1 | `{ . . . }` |
| [`SandStormBuff`](#object-sandstormbuff) | Variable | A variable containing graphical settings (movieclip, render mode) for a sandstorm visual effect on the unit. | 1 ||
| [`ScaldingOrbMoonBossOneShot`](./Passives_and_Statuses.md#object-scaldingorbmoonbossoneshot) | Object  | An object that completes the ScaldingOrb quest and removes the item from the unit's inventory. | 1 | `{ . . . }` |
| [`ScaledStatusAlliesOnSpendMana`](./Passives_and_Statuses.md#object-scaledstatusalliesonspendmana) | Object  | An object that applies a scaled status (e.g., ManaGain) to adjacent allies whenever the unit spends mana. | 1 | `{ . . . }` |
| [`ScaledStatusOnBleedDamage`](./Passives_and_Statuses.md#object-scaledstatusonbleeddamage) | Object  | An object that applies a scaled status (e.g., Charge) on the unit when they take bleed damage. | 1 | `{ . . . }` |
| [`ScaledStatusOnHolyShieldBlock`](./Passives_and_Statuses.md#object-scaledstatusonholyshieldblock) | Object  | An object that applies a scaled status (e.g., RandomMagicMissile) when the unit blocks an attack with a holy shield. | 1 | `{ . . . }` |
| [`ScalingAttackAnimation`](./Passives_and_Statuses.md#object-scalingattackanimation) | Object  | Maps attack animations to damage thresholds; when the unit's attack stat reaches a threshold, the corresponding animation overrides the default. | 1 | `{ . . . }` |
| `SchizoIllusionAIModifier` | Integer | If non-zero, modifies the AI behavior for schizo illusions. | 1 | `1` |
| `SchrodingerDisorder` | Integer | A percentage chance for the unit to be simultaneously alive and dead (Schrödinger's cat) at the start of battle. | 1 | `50%` |
| `Scleroderma` | Integer | If set to 1, the unit's skin becomes hard, reducing damage but also movement. | 1 | `1` |
| [`ScrambleLastUsedSpell`](./Miscellaneous.md#object-scramblelastusedspell) | Object  | An object containing a "permanent" boolean. If true, permanently scrambles (randomizes) the last used spell. | 1 | `{ . . . }` |
| [`self_status_next_fight`](./Miscellaneous.md#object-self_status_next_fight) | Object  | An object defining status effects applied to the unit at the start of the next fight. | 1 | `{ . . . }` |
| [`SelfDamageWhenDealDamage`](./Passives_and_Statuses.md#object-selfdamagewhendealdamage) | Object  | An object defining the damage the unit takes to itself whenever it deals damage to an enemy. | 1 | `{ . . . }` |
| [`set_WitchJump`](./Engine_StatusAndPassiveKeys.md#object-set_witchjump) | Object  | An object that configures the unit's witch jump ability (teleport-like movement). | 1 | `{ . . . }` |
| [`SetAnimationAlts`](./Miscellaneous.md#object-setanimationalts) | Object  | Specifies alternative animation names for the target's dying and dead states. | 1 | `{ . . . }` |
| [`SetFaction`](./Enums.md#enum-setfaction) | Enum | Specifies the faction the unit belongs to (e.g., 'enemies'). | 1 | `enemies` |
| `ShadowCrit` | Integer | If non-zero, enables the Shadow Crit mechanic, granting bonus critical hit chance or damage from stealth. | 1 | `1` |
| [`ShineBuff`](#object-shinebuff) | Variable | A variable containing graphical settings (movieclip, render mode) for a sparkling visual effect on the unit. | 1 ||
| `ShootHereCommand` | Integer | If non-zero, commands an allied unit to shoot at this unit's target. | 1 | `1` |
| `ShootHereReceiver` | Integer | If non-zero, marks this unit as the receiver of a Shoot Here command. | 1 | `1` |
| [`Shove`](./Engine_StatusAndPassiveKeys.md#object-shove) | Object  | Configures a knockback ability that pushes the target a set distance. | 1 | `{ . . . }` |
| [`SkipFirstRounds`](./Passives_and_Statuses.md#object-skipfirstrounds) | Object  | Determines the number of initial rounds to skip and the chance per round of 'popping' (becoming active). | 1 | `{ . . . }` |
| [`SleepDart`](./Engine_StatusAndPassiveKeys.md#object-sleepdart) | Object  | Defines a projectile or targeted ability that applies the Sleep status effect on hit. | 1 | `{ . . . }` |
| `SleepParalysis` | Variable | The amount of stacks of Sleep Paralysis applied, which prevents the unit from acting while asleep. | 1 ||
| `SmallHitExplosion` | Integer | The number of small explosion VFX to spawn on hit. | 1 | `1` |
| [`SmokeBuff`](#object-smokebuff) | Variable | Defines a visual particle effect (SmokeBuff) for rendering smoke or fog around the unit. | 1 ||
| [`Smough`](./Engine_StatusAndPassiveKeys.md#object-smough) | Object  | An object defining the Smough ability or template, likely a melee attack or passive with special properties. | 1 | `{ . . . }` |
| `Snow` | Integer | The number of snow particle instances or the integer value controlling snow intensity for weather effects. | 1 | `1` |
| [`Snow`](./Miscellaneous.md#object-snow) | Number / Object  | The number of snow particle instances or the integer value controlling snow intensity for weather effects. | 1 | `{ . . . }`<br>`1` |
| [`SolarFlare`](./Miscellaneous.md#object-solarflare) | Object  | Defines the Solar Flare weather effect, which applies damage and status effects (burn, blind) to units each turn. | 1 | `{ . . . }` |
| [`SoundEventOnHit`](./Enums.md#enum-soundeventonhit) | Enum | Specifies the sound event ID to play on hit (e.g., "Batterup_Connect"). | 1 | `Batterup_Connect` |
| [`SourceSwapsBackEndOfTurn`](./Enums.md#enum-sourceswapsbackendofturn) | Enum | Specifies the ability ID to use to swap the source unit back at the end of the turn. | 1 | `ThiefSwapBack` |
| `SpawnCatCloneOnCorpsePopped` | Integer | The number of cat clones spawned when a corpse is popped (destroyed) by the unit. | 1 | `1` |
| `SpawnCreepOnHitKnockback` | Integer | If set to 1, spawns creep on the tile where a hit knocks back an enemy. | 1 | `1` |
| `spawner` | Variable | A variable identifying the unit or object responsible for spawning other entities or effects. | 1 ||
| `SpawnerCatDataReference` | Integer | A reference ID pointing to the spawner cat's data, used by minions to link back to their spawner. | 1 | `1` |
| [`SpawnRandomPickupsOnTaggedUnitKilled`](./Passives_and_Statuses.md#object-spawnrandompickupsontaggedunitkilled) | Object  | Defines a pool of random pickups (items) spawned when a unit with a specific tag is killed, with a count range. | 1 | `{ . . . }` |
| [`SpawnTilePuddleOnBattleStart`](./Miscellaneous.md#object-spawntilepuddleonbattlestart) | Object  | Defines a puddle of a specific tile type (e.g., OilTile) that is spawned on the battlefield at the start, with a radius range. | 1 | `{ . . . }` |
| `SpawnWebTrap` | Integer | The number of web traps to spawn on the target tile. | 1 | `1` |
| [`SpecialBossMultipartInstakill`](./Enums.md#enum-specialbossmultipartinstakill) | Enum | Specifies the boss ID (e.g., "moonboss") whose multipart instakill mechanic is triggered. | 1 | `moonboss` |
| `SpeedUp_WithoutInitiative` | Integer | The number of stacks of Speed Up that do not affect the unit's initiative (turn order) stat. | 1 | `1` |
| `SpellShield` | Integer | The number of stacks of SpellShield, which blocks incoming spells. | 1 | `1` |
| [`SpewerAltGraphics`](./Passives_and_Statuses.md#object-speweraltgraphics) | Object  | Maps different Spewer liquid types (Normal, Fire, Tar) to their corresponding alternate graphic indices. | 1 | `{ . . . }` |
| [`SpiderReturn`](./Engine_StatusAndPassiveKeys.md#object-spiderreturn) | Object  | Defines the Spider Return ability, which teleports the unit back to a previously marked location after attacking. | 1 | `{ . . . }` |
| `SpitConsumed` | Integer | If non-zero, marks the object consumed by the Spit ability as having been used. | 1 | `1` |
| `SpreadWater` | Integer | If set to 1, causes the character to spread water onto adjacent tiles. | 1 | `1` |
| `sprout` | Variable | A variable associated with plant-based growth or spawning mechanics, likely a seed or sprout identifier. | 1 ||
| `SproutsGrantMovement` | Integer | If set to 1, sprouts on the character grant additional movement (aliases to MovementUp). | 1 | `1` |
| [`StacyMutant_Brace`](./Miscellaneous.md#object-stacymutant_brace) | Object  | A passive group granting the Brace ability and cosmetic changes. | 1 | `{ . . . }` |
| [`StacyMutant_Counter`](./Miscellaneous.md#object-stacymutant_counter) | Object  | A passive group granting a counter attack and a bleed effect on basic attacks. | 1 | `{ . . . }` |
| [`StacyMutant_Damage`](./Miscellaneous.md#object-stacymutant_damage) | Object  | A passive group increasing damage and decreasing max health with cosmetic changes. | 1 | `{ . . . }` |
| [`StacyMutant_DoubleHead`](./Miscellaneous.md#object-stacymutant_doublehead) | Object  | A passive group granting an extra dispersed turn and cosmetic changes. | 1 | `{ . . . }` |
| [`StacyMutant_Fire`](./Miscellaneous.md#object-stacymutant_fire) | Object  | A passive group granting fire immunity and a lava shot basic attack. | 1 | `{ . . . }` |
| [`StacyMutant_Health`](./Miscellaneous.md#object-stacymutant_health) | Object  | A passive group increasing max health, reducing speed, and scaling size. | 1 | `{ . . . }` |
| [`StacyMutant_Holy`](./Miscellaneous.md#object-stacymutant_holy) | Object  | A passive group granting a divine shield and cosmetic changes. | 1 | `{ . . . }` |
| [`StacyMutant_Ice`](./Miscellaneous.md#object-stacymutant_ice) | Object  | A passive group granting ice immunity and an ice breath basic attack. | 1 | `{ . . . }` |
| [`StacyMutant_Lightning`](./Miscellaneous.md#object-stacymutant_lightning) | Object  | A passive group granting electric immunity and a lightning dash basic attack. | 1 | `{ . . . }` |
| [`StacyMutant_Mirror`](./Miscellaneous.md#object-stacymutant_mirror) | Object  | A passive group granting projectile reflection and random magic missile each turn. | 1 | `{ . . . }` |
| [`StacyMutant_Speed`](./Miscellaneous.md#object-stacymutant_speed) | Object  | A passive group increasing speed, reducing damage, and scaling size. | 1 | `{ . . . }` |
| [`StacyMutant_Thorns`](./Miscellaneous.md#object-stacymutant_thorns) | Object  | A passive group granting thorns damage and cosmetic changes. | 1 | `{ . . . }` |
| `StartDead` | Integer | The percentage chance that the character starts the battle already dead. | 1 | `100%` |
| `StatBounty` | Integer | The number of stacks of the StatBounty status effect. | 1 | `1` |
| [`StatDependentPassive`](./Passives_and_Statuses.md#object-statdependentpassive) | Object  | An object containing formulas that dynamically modify passive effects based on the unit's stats (e.g., str, dex, int). | 1 | `{ . . . }` |
| [`StatusAdjacentOnTheirTurnBegin`](./Passives_and_Statuses.md#object-statusadjacentontheirturnbegin) | Object  | Defines a status effect applied to adjacent units when their turn begins, such as forcing them to move away. | 1 | `{ . . . }` |
| [`StatusAdjacentOnTheirTurnEnd`](./Passives_and_Statuses.md#object-statusadjacentontheirturnend) | Object  | Defines a status effect applied to adjacent units when their turn ends, such as forcing them to move away. | 1 | `{ . . . }` |
| [`StatusAfterXStacks`](./Miscellaneous.md#object-statusafterxstacks) | Object  | Defines a condition that triggers a status effect when a specified stack key reaches a threshold, optionally expiring at turn end. | 1 | `{ . . . }` |
| [`StatusAlliesEachTurn`](./Passives_and_Statuses.md#object-statusallieseachturn) | Object  | Defines a status effect applied to all allies each turn, with an optional exclusion of the owner and conditional checks. | 1 | `{ . . . }` |
| [`StatusEachTurnBeginIfHasStatus`](./Passives_and_Statuses.md#object-statuseachturnbeginifhasstatus) | Object  | Defines a status effect to apply (and optionally consume) at the start of each turn if the character already has a specific status, with a specified animation. | 1 | `{ . . . }` |
| [`StatusEachTurnEndIfEnabledAtStartOfTurn`](./Passives_and_Statuses.md#object-statuseachturnendifenabledatstartofturn) | Object  | Defines an ability to force-use at the end of each turn if the character was in the specified form at the start of the turn. | 1 | `{ . . . }` |
| [`StatusIfBattleAlreadyBegan`](./Passives_and_Statuses.md#object-statusifbattlealreadybegan) | Object  | Defines a status effect that is applied only if the battle has already started (not on the first turn). | 1 | `{ . . . }` |
| [`StatusOnDodge`](./Passives_and_Statuses.md#object-statusondodge) | Object  | Defines a status effect applied to the unit each time it successfully dodges an attack. | 1 | `{ . . . }` |
| [`StatusOnEnemyCastSpell`](./Passives_and_Statuses.md#object-statusonenemycastspell) | Object  | Defines a status effect applied to the unit each time an enemy casts a spell. | 1 | `{ . . . }` |
| [`StatusOnEnemyConfused`](./Passives_and_Statuses.md#object-statusonenemyconfused) | Object  | Defines an ability to immediately use when an enemy becomes confused. | 1 | `{ . . . }` |
| [`StatusOnEnemyDeath`](./Passives_and_Statuses.md#object-statusonenemydeath) | Object  | Defines a status effect applied to the unit each time an enemy dies. | 1 | `{ . . . }` |
| [`StatusOnFallAsleep`](./Passives_and_Statuses.md#object-statusonfallasleep) | Object  | Defines one or more beneficial status effects applied to the unit when it falls asleep. | 1 | `{ . . . }` |
| [`StatusOnFullMana`](./Passives_and_Statuses.md#object-statusonfullmana) | Object  | Defines a status effect applied to the unit when its mana is full, with an optional once-per-battle conditional. | 1 | `{ . . . }` |
| [`StatusOnLoseShield`](./Passives_and_Statuses.md#object-statusonloseshield) | Object  | Defines a status effect applied to the unit each time it loses a shield point. | 1 | `{ . . . }` |
| [`StatusOnTakeHealthDamage`](./Passives_and_Statuses.md#object-statusontakehealthdamage) | Object  | Defines a status effect applied to the unit each time it takes health damage, such as a permanent stat reduction. | 1 | `{ . . . }` |
| [`StatusOverlappingCharactersAndDie`](./Passives_and_Statuses.md#object-statusoverlappingcharactersanddie) | Object  | Defines a status effect applied to overlapping characters, after which the character dies. | 1 | `{ . . . }` |
| [`StatusWhenStatusCompletelyRemoved`](./Passives_and_Statuses.md#object-statuswhenstatuscompletelyremoved) | Object  | Defines a status to apply and an ability to use when a specific status is completely removed from the character. | 1 | `{ . . . }` |
| `StealDemonicGlyph` | Integer | The number of Demonic Glyphs stolen from the target. | 1 | `1` |
| [`StealEquipment`](./Enums.md#enum-stealequipment) | Enum | Specifies the type of equipment to steal (e.g., "any") from the target. | 1 | `any` |
| `StealthCritChance` | Integer | The percentage chance to critically hit while stealthed. | 1 | `100` |
| `StealthUntilBasicAttack` | Integer | The number of stacks of Stealth that are removed when the unit performs a basic attack. | 1 | `1` |
| `StealTurn` | Integer | The number of turns stolen from the target to grant to the attacker. | 1 | `1` |
| `StevenBolts` | Integer | The number of Steven Bolts (a special resource or charge) the unit has for a unique ability. | 1 | `1` |
| `StrictLimitDamage` | Integer | The amount of damage strict limit applies, capping incoming damage to a fixed value per hit. | 1 | `1` |
| `StripKnockback` | Integer | If non-zero, removes all knockback effects from the unit's attacks or abilities. | 1 | `1` |
| [`SupportDieInsteadOfRun`](./Passives_and_Statuses.md#object-supportdieinsteadofrun) | Object  | Configures alternative dying and dead animations for support units that die instead of fleeing. | 1 | `{ . . . }` |
| [`SwapWeapon`](./Miscellaneous.md#object-swapweapon) | Object  | An object containing a "pool" array of weapon names to randomly swap to. | 1 | `{ . . . }` |
| [`SwimmingFormChange`](./Passives_and_Statuses.md#object-swimmingformchange) | Object  | Defines the form names to switch to when in water and when exiting water. | 1 | `{ . . . }` |
| [`SyncFormsWithBuddy`](./Passives_and_Statuses.md#object-syncformswithbuddy) | Object  | Specifies the form to revert to if the character has no buddy, ensuring form synchronization. | 1 | `{ . . . }` |
| `T2CopyCatInternal` | Variable | An internal variable used by the T2 Copy Cat passive to track clone spawning state. | 1 ||
| [`T3HitlerSpawningPhase`](./Passives_and_Statuses.md#object-t3hitlerspawningphase) | Object  | Defines weighted groups of spawn abilities used during the T3Hitler boss's spawning phase. | 1 | `{ . . . }` |
| `T3HitlerTriggerInitialSpawns` | Integer | If non-zero, triggers the initial spawn sequence for the T3 Hitler boss. | 1 | `1` |
| [`TagMetronome`](./Enums.md#enum-tagmetronome) | Enum | Specifies a tag (e.g., "musical") used to filter which abilities the Metronome effect can pick. | 1 | `musical` |
| [`TakeBonusTurnWithStatus`](./Passives_and_Statuses.md#object-takebonusturnwithstatus) | Object  | Container for status effects applied when taking a bonus turn. | 1 | `{ . . . }` |
| `TakeExtraTurnEndOfRound` | Integer | The number of extra turns taken at the end of the round. | 1 | `1` |
| `TakeWeaponFromSpawner` | Integer | If set to 1, the minion inherits the weapon from its spawner. | 1 | `1` |
| `Tall` | Integer | If set to 1, the character occupies a taller hitbox or sprite space. | 1 | `1` |
| [`TallTumorManaBurn`](./Enums.md#enum-talltumormanaburn) | Enum | Specifies the mana burn ability used by the TallTumor. | 1 | `TT_ManaBurn` |
| `TargetedMetronome` | Integer | The number of random targets hit by the Targeted Metronome effect. | 1 | `20` |
| [`TattersFear`](./Engine_StatusAndPassiveKeys.md#object-tattersfear) | Object  | Defines a targeted fear ability that causes the target to flee in a random direction. | 1 | `{ . . . }` |
| `TauntAtFullHealth` | Integer | The number of stacks of Taunt applied to the unit when it is at full health. | 1 | `1` |
| `Taunting` | Integer | The number of stacks of Taunting, which forces enemies to target the unit. | 1 | `1` |
| [`TC_DashReaction`](./Engine_StatusAndPassiveKeys.md#object-tc_dashreaction) | Object  | Defines a trample dash reaction ability that triggers when a unit dashes, dealing damage to enemies in the path. | 1 | `{ . . . }` |
| [`TeamBonusAbility`](./Enums.md#enum-teambonusability) | Enum | Specifies the ability ID granted to allies as a team bonus. | 1 | `ShootHere` |
| [`TeleportBackAtTurnEnd`](./Enums.md#enum-teleportbackatturnend) | Enum | Specifies the ability ID used to teleport the unit back to its starting position at turn end. | 1 | `FlashBack` |
| `TempBackstab` | Integer | The amount of temporary backstab bonus, typically as a percentage. | 1 | `75` |
| `TempBackstabBleed` | Integer | The number of temporary Bleed status stacks applied on a backstab attack. | 1 | `1` |
| `TempBackstabPiercing` | Integer | The amount of temporary piercing added to backstab attacks. | 1 | `1` |
| `TempBackstabPoison` | Integer | The amount of temporary poison stacks applied with backstab attacks. | 1 | `1` |
| `TempBasicAttackBonusAOE` | Integer | The amount of temporary area-of-effect bonus on basic attacks. | 1 | `1` |
| `TempBonusKnockback` | Integer | The number of stacks of temporary bonus knockback distance. | 1 | `1` |
| `TempBonusKnockbackDamage` | Integer | The number of stacks of temporary bonus knockback damage. | 1 | `1` |
| `TempInjuryImmunity` | Integer | The number of stacks of temporary immunity to Injuries. | 1 | `1` |
| `TempManaCostReduction` | Integer | The number of stacks of temporary mana cost reduction. | 1 | `1` |
| `TempMeleeRangeUp` | Integer | The number of tiles added to the unit's melee attack range as a temporary buff. | 1 | `1` |
| `TempPenetrate` | Integer | The amount of temporary penetration applied to attacks. | 1 | `1` |
| `TempPreEmptiveCounterAttack` | Integer | The number of turns of temporary pre-emptive counterattack status. | 1 | `1` |
| [`Terminator2Chase`](./Enums.md#enum-terminator2chase) | Enum | Specifies the movement ability used by Terminator2 when chasing the target. | 1 | `move` |
| [`Terminator2Run`](./Passives_and_Statuses.md#object-terminator2run) | Object  | Defines the movement ability and movement weights used by Terminator2 when running away. | 1 | `{ . . . }` |
| [`TerminatorChase`](./Passives_and_Statuses.md#object-terminatorchase) | Object  | Defines the movement ability and reaction ability used by Terminator1 when chasing a target, plus whether it prioritizes player cats. | 1 | `{ . . . }` |
| [`TerminatorSkin`](./Passives_and_Statuses.md#object-terminatorskin) | Object  | Defines the status effect and groups of stacks applied by the Terminator's skin passive. | 1 | `{ . . . }` |
| [`TheCreator_SpawnCloneTeam`](./Engine_StatusAndPassiveKeys.md#object-thecreator_spawncloneteam) | Object  | Defines an ability that spawns a team of clones of the original cat, controlled by The Creator. | 1 | `{ . . . }` |
| [`TheHunger`](./Passives_and_Statuses.md#object-thehunger) | Object  | Defines the Hunger passive, which applies Madness or other effects each turn, representing a disorder. | 1 | `{ . . . }` |
| [`ThornUp`](./Engine_StatusAndPassiveKeys.md#object-thornup) | Object  | Defines a self-buff ability that increases the unit's Thorns damage, reflecting damage back to attackers. | 1 | `{ . . . }` |
| [`ThrobbingKing2`](./Engine_StatusAndPassiveKeys.md#object-throbbingking2) | Object  | An object defining the Throbbing King 2 ability, likely a boss attack or passive with pulsing damage or effects. | 1 | `{ . . . }` |
| [`TickDownStatus`](./Enums.md#enum-tickdownstatus) | Enum | Specifies the name of the status effect whose duration is reduced by one tick. | 1 | `ShortCircuit` |
| [`TileElementDamageImmunity`](./Enums.md#enum-tileelementdamageimmunity) | Enum | Determines which tile element type the character is immune to damage from. | 1 | `Ice` |
| `TilesMovedToCritChance` | Integer | The number of stacks of a status that grants critical hit chance based on tiles moved. | 1 | `1` |
| `TilesMovedToMana` | Integer | The number of stacks of a status that grants mana based on tiles moved. | 1 | `1` |
| [`TilesMovedToNeighborHeal`](./Enums.md#enum-tilesmovedtoneighborheal) | Enum | Specifies the scaling type for healing neighbors based on tiles moved (e.g., 'level'). | 1 | `level` |
| `TilesMovedToStrength` | Integer | The number of stacks of a status that grants strength based on tiles moved. | 1 | `1` |
| [`TintItem`](./Passives_and_Statuses.md#object-tintitem) | Object  | Defines additive and multiplicative color tint adjustments applied to an item's appearance, with an optional ignore condition. | 1 | `{ . . . }` |
| `TireBehavior` | Integer | If set to 1, activates special tire-related behavior for the character. | 1 | `1` |
| `TormentorHeal` | Integer | If set to 1, the Tormentor can heal itself. | 1 | `1` |
| [`TormentorRuneAbsorb`](./Engine_StatusAndPassiveKeys.md#object-tormentorruneabsorb) | Object  | Defines a spell ability that absorbs runes or energy from a target, typically used by the Tormentor enemy. | 1 | `{ . . . }` |
| `TossTargetIsAggroTarget` | Integer | If set to 1, the toss target is the unit's current aggro target. | 1 | `1` |
| `TossTargetIsBuddy` | Integer | If set to 1, the toss target is the unit's buddy. | 1 | `1` |
| `TossTargetIsNotInWater` | Integer | If set to 1, the toss target must not be in water terrain. | 1 | `1` |
| [`TourettesMeows`](./Passives_and_Statuses.md#object-tourettesmeows) | Object  | Defines a passive that triggers random vocalizations (hiss, hit, normal) at random cooldown intervals. | 1 | `{ . . . }` |
| `TowerDefenseStatus` | Integer | The number of stacks of the sentry/tower defense status, granting stationary attack capabilities. | 1 | `1` |
| `TowerDefenseStatus2` | Integer | The number of stacks of the enhanced sentry/tower defense status. | 1 | `1` |
| [`ToxicBubbles`](#object-toxicbubbles) | Variable | A variable defining the visual particle effect for toxic bubbles, used for environmental hazards or attacks. | 1 ||
| [`ToxPuff`](./Engine_StatusAndPassiveKeys.md#object-toxpuff) | Object  | Defines a self-buff ability that creates a toxic puff visual effect around the unit. | 1 | `{ . . . }` |
| [`TrackAmountKilledByPlayer`](./Enums.md#enum-trackamountkilledbyplayer) | Enum | Specifies the name of the counter used to track how many of this type the player has killed. | 1 | `BonusBirdsKilled` |
| [`TransformBasicMove`](./Enums.md#enum-transformbasicmove) | Enum | Specifies the name of the basic move to transform into. | 1 | `BasicDashAttackMove_NoKnockback` |
| [`TransformEquipment`](./Miscellaneous.md#object-transformequipment) | Object  | Defines an equipment transformation from one item to another, with 'from' and 'to' sub-keys. | 1 | `{ . . . }` |
| [`TransformNow`](./Enums.md#enum-transformnow) | Enum | Specifies the name of the form to immediately transform into. | 1 | `Hitler` |
| [`TransformOnStatusThreshold`](./Passives_and_Statuses.md#object-transformonstatusthreshold) | Object  | Defines the status effect, the stack threshold at which to transform, and the object to transform into. | 1 | `{ . . . }` |
| `Trapper_Status` | Integer | The number of trap-related status stacks applied. | 1 | `1` |
| [`TrexSwitchTarget`](./Engine_StatusAndPassiveKeys.md#object-trexswitchtarget) | Object  | Defines a targeted status ability that forces an enemy to switch its target to the caster. | 1 | `{ . . . }` |
| `TriggerBleedOnBleed` | Integer | If non-zero, causes the unit to trigger additional bleed effects whenever it applies bleed to an enemy. | 1 | `1` |
| `TriggerMotherConsume` | Integer | The number of times the Mother consume effect is triggered. | 1 | `1` |
| `TriggerMotherGrow` | Integer | The number of times the Mother grow effect is triggered. | 1 | `4` |
| `Triskaidekaphobia` | Integer | The threshold number (typically 13) at which a negative effect triggers due to the disorder Triskaidekaphobia. | 1 | `13` |
| [`TT_Thrash`](./Engine_StatusAndPassiveKeys.md#object-tt_thrash) | Object  | Defines a melee attack ability that uses the thrash animation and deals damage to the target. | 1 | `{ . . . }` |
| `tumor` | Variable | A variable identifying a tumor growth passive or effect, likely related to status application or visual changes. | 1 ||
| [`TunnelVision`](./Passives_and_Statuses.md#object-tunnelvision) | Object  | If present, grants the TunnelVision status, which modifies crit_chance as defined in its sub-properties. | 1 | `{ . . . }` |
| `TurnAround` | Integer | The number of times the unit turns around. | 1 | `1` |
| [`TurnControlDelay`](./Enums.md#enum-turncontroldelay) | Float | Specifies the delay in seconds before the unit regains turn control. | 1 | `.25` |
| `TurnRight` | Integer | The number of times the unit turns to the right. | 1 | `1` |
| `TutorialBossRiggedFight` | Integer | The turn count at which the tutorial boss fight becomes rigged. | 1 | `16` |
| `TVBotDisableAttack` | Integer | If set to 1, disables the TVBot's ability to attack. | 1 | `1` |
| `TVBotDisableMove` | Integer | If set to 1, disables the TVBot's ability to move. | 1 | `1` |
| `TVBotDisableSpells` | Integer | If set to 1, disables the TVBot's ability to use spells. | 1 | `1` |
| [`TVBotScreen`](./Passives_and_Statuses.md#object-tvbotscreen) | Object  | Maps TVBot screen channel names to their corresponding form indices. | 1 | `{ . . . }` |
| `Twister_loop` | Enum | Specifies which loop animation to use for the Twister effect. | 1 ||
| [`TwisterFling`](./Passives_and_Statuses.md#object-twisterfling) | Object  | Defines the minimum distance, maximum distance, and damage for the TwisterFling ability. | 1 | `{ . . . }` |
| [`UFO_BigExplode`](./Engine_StatusAndPassiveKeys.md#object-ufo_bigexplode) | Object  | Defines the visual and template properties for the UFO's large explosion effect. | 1 | `{ . . . }` |
| [`UltraSmough`](./Engine_StatusAndPassiveKeys.md#object-ultrasmough) | Object  | Defines the properties for the UltraSmough entity or status. | 1 | `{ . . . }` |
| `UndoDamage` | Integer | The amount of damage reversed. | 1 | `1` |
| [`UnlimitedDeathRattleRevive`](./Passives_and_Statuses.md#object-unlimiteddeathrattlerevive) | Object  | Configures an unlimited revive effect, including the ability to use and whether it works even when stunned. | 1 | `{ . . . }` |
| `UpTireBehavior` | Integer | The behavior type integer for the Tire's upward form. | 1 | `5` |
| [`UseAbility_Madness`](./Enums.md#enum-useability_madness) | Enum | Determines which ability type (e.g., weapon) is forcibly used when Madness triggers. | 1 | `weapon` |
| [`UseAbilityWhenOutOfStatus`](./Passives_and_Statuses.md#object-useabilitywhenoutofstatus) | Object  | Defines an ability to execute when the unit no longer has a specified status. | 1 | `{ . . . }` |
| [`UseAbilityWhenShieldDepleted`](./Enums.md#enum-useabilitywhenshielddepleted) | Enum | The ability to use when the unit's shield is fully depleted. | 1 | `T3Pebbles_PrimeBoulderDrop` |
| [`UseMoveAbilityWithAI`](./Miscellaneous.md#object-usemoveabilitywithai) | Object  | Defines a move ability to execute with AI-controlled movement weights. | 1 | `{ . . . }` |
| `UseRandomSpell_Madness` | Integer | The number of random spells cast when Madness triggers. | 1 | `1` |
| `VaporizeDice` | Integer | The number of dice vaporized. | 1 | `1` |
| [`VisualCountDownThenApplyStatus`](./Miscellaneous.md#object-visualcountdownthenapplystatus) | Object  | Contains a visual countdown sequence that culminates in applying a status effect, optionally forcing an ability use. | 1 | `{ . . . }` |
| [`WaggleClone`](./Miscellaneous.md#object-waggleclone) | Object  | Defines a waggle clone ability with health thresholds and object sizes. | 1 | `{ . . . }` |
| `Wall` | Integer | If 1, the unit is treated as an impassable wall. | 1 | `1` |
| `Wet` | Integer | The number of stacks of the Wet status effect applied. | 1 | `1` |
| [`WhitelistPickupType`](./Enums.md#enum-whitelistpickuptype) | Enum | Specifies the type of pickup that this unit is allowed to collect. | 1 | `food` |
| `WideBackstab` | Integer | The additional width for backstab attacks, in tiles. | 1 | `1` |
| [`Wind`](./Passives_and_Statuses.md#object-wind) | Object  | Defines the properties for the Wind element, such as knockback amount. | 1 | `{ . . . }` |
| `Windy` | Integer | The number representing the Windy weather intensity or whether it is active. | 1 | `1`<br>`10` |
| [`Windy`](./Miscellaneous.md#object-windy) | Number / Object  | The number representing the Windy weather intensity or whether it is active. | 1 | `{ . . . }`<br>`1`<br>`10` |
| `WispDodge` | Integer | If 1, the unit gains the Wisp's dodge ability. | 1 | `1` |
| `WobblyCat` | Integer | The chance (as a percentage) or stack count for the WobblyCat disorder. | 1 | `25%` |
| `XIsConsumedCharacterMaxHP` | Integer | Specifies the multiplier used to set X to the maximum HP of the consumed character. | 1 | `3` |
| `XIsCountDeaths` | Integer | If set to 1, X is equal to the number of deaths in the match. | 1 | `1` |
| [`XIsCountStatusStacks`](./Enums.md#enum-xiscountstatusstacks) | Enum | Specifies the status field whose stacks are counted to set X. | 1 | `DodgeChance_Status` |
| [`XIsFormulaLockedUntilComplete`](./Enums.md#enum-xisformulalockeduntilcomplete) | Enum | Specifies a stat (e.g., dex) whose value is locked in and used for X until the ability completes. | 1 | `dex` |
| `XIsIncreaseEachTurn` | Integer | Specifies the amount by which X increases each turn. | 1 | `1` |
| `XIsRampAndReset` | Integer | If set to 1, X ramps up over time and resets after use; 0 disables this behavior. | 1 | `0` |
| `XIsRecycleCostReduction` | Integer | Specifies the amount of recycle cost reduction applied to X. | 1 | `5` |
| `ZeroKnockbackDamage` | Integer | If 1, the unit takes no damage from knockback effects. | 1 | `1` |
| [`AcidRain`](./Engine_StatusAndPassiveKeys.md#object-acidrain) | Number / Object  | If non-zero, enables the Acid Rain weather effect dealing damage each turn. || `{ . . . }`<br>`2` |
| `Adrenaline` | Integer | The flat amount of Adrenaline (a resource or stat) granted to the unit. || `10` |
| `Ammo` | Integer | The amount of ammo to add or remove (negative values subtract). || `-1`<br>`-99999`<br>`1` |
| `Bloodzerked` | Integer | The number of Bloodzerk stacks applied. || `1` |
| [`BombRatTurtle`](./Engine_StatusAndPassiveKeys.md#object-bombratturtle) | Integer / Object  | The number of bomb rat turtle spawns triggered. || `{ . . . }`<br>`1` |
| [`BounceRock`](./Arrays.md#array-bouncerock) | Array / Enum  | Specifies the rock object to bounce. || `LavaBoulder`<br>`SmallLavaRock`<br>`SmallRock` |
| [`ButterflySwarm`](./Engine_StatusAndPassiveKeys.md#object-butterflyswarm) | Number / Object  | The number of butterflies spawned for the Butterfly Swarm effect. || `{ . . . }`<br>`2` |
| `ChampionUpgradeNextMinion` | Integer | The number of champion upgrades applied to the next spawned minion. || `1` |
| [`CockroachSwarm`](./Engine_StatusAndPassiveKeys.md#object-cockroachswarm) | Number / Object  | If true, the unit spawns as a Cockroach Swarm, with its specific mechanics and effects. || `{ . . . }`<br>`1` |
| `CollideWithConsumed` | String | Damage formula for collision with consumed objects, e.g., '4+bonus_melee_damage'. || `1+bonus_melee_damage`<br>`4+bonus_melee_damage`<br>`5+bonus_melee_damage` |
| [`CopySpells`](./Miscellaneous.md#object-copyspells) | Integer / Object  | The number of spells copied from the target, or an object specifying `stacks` and whether the copy is `upgraded`. || `{ . . . }`<br>`1` |
| [`Counterspell`](./Engine_StatusAndPassiveKeys.md#object-counterspell) | Integer / Object  | If non-zero, negates the next incoming enemy spell and triggers the configured counterspell effects. || `{ . . . }`<br>`1` |
| [`DelayCastAbility`](./Miscellaneous.md#object-delaycastability) | Enum / Object  | Specifies the name of an ability to cast after a delay. || `{ . . . }`<br>`HitlerNuke` |
| [`DelayCastAbility`](./Miscellaneous.md#object-delaycastability) | Enum / Object  | Specifies the name of an ability to cast after a delay. || `{ . . . }`<br>`HitlerNuke` |
| `DoubleCast` | Integer | The number of double-cast stacks, allowing a spell to be cast twice. || `1` |
| `DoubleCastSpell` | Integer | The number of times the next spell cast is doubled, or a template with name and tooltip. || `1`<br>`2` |
| `EliteUpgradeNextMinion` | Integer | The number of elite upgrades applied to the next spawned minion. || `1` |
| [`FactionUprising`](./Miscellaneous.md#object-factionuprising) | Enum / Object  | Specifies which faction triggers a global uprising event, adding allied units of that faction. || `{ . . . }`<br>`alien`<br>`ghost`<br>`robot` |
| [`FireArmor`](./Engine_StatusAndPassiveKeys.md#object-firearmor) | Integer / Object  | The number of Fire Armor stacks providing damage reflection. || `{ . . . }`<br>`1` |
| [`FireArmor2`](./Engine_StatusAndPassiveKeys.md#object-firearmor2) | Integer / Object  | The number of Fire Armor2 stacks (likely a variant). || `{ . . . }`<br>`1` |
| [`FireflySwarm`](./Engine_StatusAndPassiveKeys.md#object-fireflyswarm) | Number / Object  | The number of fireflies in the swarm effect. || `{ . . . }`<br>`2` |
| [`FireStorm`](./Engine_StatusAndPassiveKeys.md#object-firestorm) | Number / Object  | The percentage chance or combo definition for the Fire Storm effect. || `{ . . . }`<br>`0%`<br>`33%` |
| [`Fog`](./Engine_StatusAndPassiveKeys.md#object-fog) | Number / Object  | When an integer, the intensity of fog; when an object, defines the fog particle effect. || `{ . . . }`<br>`1` |
| [`ForceMoveTowardsEnemies`](./Enums.md#enum-forcemovetowardsenemies) | Enum / Integer  | Specifies the ability or distance to force the target to move towards enemies. || `1`<br>`DumbMove_Impl`<br>`MoveOne` |
| [`Grappled`](./Arrays.md#array-grappled) | Array / Integer  | The number of stacks and probability of applying the Grappled status, in format [stacks, probability] or just stacks. || `1`<br>`[1, .50]`<br>`[1, .75]` |
| [`HeatWave`](./Engine_StatusAndPassiveKeys.md#object-heatwave) | Array / Number / Object  | When an integer, the intensity of the heat wave; when an object, defines the visual effects or status properties. || `{ . . . }`<br>`1` |
| `HeavyHits` | Integer | The number of Heavy Hits stacks increasing attack impact. || `1` |
| `IgnoreSelf` | Boolean / Integer | If set to 1 or true, the damage instance ignores the source unit (does not affect itself). || `1`<br>`true` |
| `Invulnerable` | Integer | The number of Invulnerable stacks, making the unit immune to damage. || `1` |
| [`JudgementDay`](./Engine_StatusAndPassiveKeys.md#object-judgementday) | Number / Object  | When an integer, the turn count or damage for Judgement Day; when an object, defines the weather status. || `{ . . . }`<br>`25` |
| [`KnockbackDirectionIsFacingDirection`](./Enums.md#enum-knockbackdirectionisfacingdirection) | Enum / Integer  | Specifies how to alter knockback direction relative to the unit's facing: 1 (same), flip (opposite), rotate_right. || `1`<br>`flip`<br>`rotate_right` |
| `Meaty` | Integer | The number of Meaty stacks increasing health or size. || `1` |
| [`Meteornado`](./Engine_StatusAndPassiveKeys.md#object-meteornado) | Number / Object  | The number of Meteornado status stacks applied, or an object defining its visual effects. || `{ . . . }`<br>`1` |
| [`MeteorShower`](./Engine_StatusAndPassiveKeys.md#object-meteorshower) | Number / Object  | The chance (as a percentage) for a meteor shower to occur on a given turn. || `{ . . . }`<br>`25%` |
| `Muted` | Integer | The number of Muted stacks, disabling certain abilities. || `1` |
| `NextAbilityHeals` | Integer | The number of stacks causing the next ability to heal instead of damage. || `1` |
| `NextActionLuckUp` | Integer | The number of stacks increasing luck for the next action. || `99` |
| `NextAttackBonusRange` | Integer | The added range for the unit's next basic attack. || `1`<br>`3`<br>`5` |
| [`NextAttackSpecialCrit`](./Miscellaneous.md#object-nextattackspecialcrit) | Integer / Object  | The number of charges for a special crit on the next attack, or an object defining its bonus properties. || `{ . . . }`<br>`1` |
| [`NextBasicAttackCritsThisTurn`](./Miscellaneous.md#object-nextbasicattackcritsthisturn) | Object  | An object or number configuring the next basic attack to be a critical hit this turn. An object may contain stack, cant_miss, or piercing sub-keys. || `{ . . . }` |
| `NextDamageReduceAndHealAllies` | Integer | The number of stacks reducing next damage and healing nearby allies. || `1` |
| `NextTurnDoubleRangedDamage` | Integer | The number of stacks doubling ranged damage on the next turn. || `1` |
| `OverrideKnockbackDamage` | Enum / Integer | A formula or flat value that sets the damage dealt when knockback occurs, overriding default calculations. || `"max(5+bonus_melee_ability_damage, 1)"`<br>`0`<br>`2` |
| `OverrideKnockbackDamage` | Enum / Integer | A formula or flat value that sets the damage dealt when knockback occurs, overriding default calculations. || `"max(5+bonus_melee_ability_damage, 1)"`<br>`0`<br>`2` |
| `PermanentImmobile` | Integer | The permanent amount of immobility stacks applied. || `1` |
| [`RandomDistanceDisplace`](./Miscellaneous.md#object-randomdistancedisplace) | Integer / Object  | The number of stacks of a random distance displacement effect, or an object with stacks, min_dist, and chance. || `{ . . . }`<br>`20` |
| `ReduceManaCostExcludeBrainstorm` | Integer | The number of stacks reducing mana cost, excluding Brainstorm. || `1` |
| [`ScatterHeldCoin`](./Arrays.md#array-scatterheldcoin) | Array / Integer  | The number of coins scattered, with an optional probability as a second element. || `1`<br>`[1 .3]`<br>`[1 .5]` |
| [`SelfStun`](./Arrays.md#array-selfstun) | Array / Integer  | The number of stacks of self-stun applied, with an optional probability as a second element. || `1`<br>`[1 .5]` |
| [`Shatter`](./Engine_StatusAndPassiveKeys.md#object-shatter) | Integer / Object  | The amount of damage dealt when a frozen or petrified status is shattered, or a template definition for a Shatter ability. || `{ . . . }`<br>`15` |
| [`SpawnRock`](./Arrays.md#array-spawnrock) | Array / Integer  | The number of rocks to spawn, or an array with stacks and probability. || `1`<br>`[1, .20]` |
| `SpellShield` | Integer | The number of stacks of SpellShield, which blocks incoming spells. || `1` |
| `StatBounty` | Integer | The number of stacks of the StatBounty status effect. || `1` |
| `Taunting` | Integer | The number of stacks of Taunting, which forces enemies to target the unit. || `1` |
| [`TeamCastAbility`](./Miscellaneous.md#object-teamcastability) | Enum / Object  | Specifies the ability name for the team to cast, with optional tag restriction and same orientation. || `{ . . . }`<br>`Huddle_Impl`<br>`Spin`<br>`TeamFlex_Impl` |
| `TempBackstab` | Integer | The amount of temporary backstab bonus, typically as a percentage. || `75` |
| `TempBonusKnockback` | Integer | The number of stacks of temporary bonus knockback distance. || `1` |
| `TempBonusKnockbackDamage` | Integer | The number of stacks of temporary bonus knockback damage. || `1` |
| `TempCritChanceUp` | Integer | The amount of temporary critical hit chance (in percentage points) added. || `100`<br>`30` |
| `TempInitiativeChange` | Integer | The flat change to the unit's initiative value. || `-100`<br>`-999`<br>`100` |
| `TempInitiativeChange` | Integer | The flat change to the unit's initiative value. || `-100`<br>`-999`<br>`100` |
| `TempInjuryImmunity` | Integer | The number of stacks of temporary immunity to Injuries. || `1` |
| `TempManaCostReduction` | Integer | The number of stacks of temporary mana cost reduction. || `1` |
| `TempPreEmptiveCounterAttack` | Integer | The number of turns of temporary pre-emptive counterattack status. || `1` |
| `TilesMovedToCritChance` | Integer | The number of stacks of a status that grants critical hit chance based on tiles moved. || `1` |
| `TilesMovedToMana` | Integer | The number of stacks of a status that grants mana based on tiles moved. || `1` |
| [`TilesMovedToNeighborHeal`](./Enums.md#enum-tilesmovedtoneighborheal) | Enum  | Specifies the scaling type for healing neighbors based on tiles moved (e.g., 'level'). || `level` |
| `TilesMovedToStrength` | Integer | The number of stacks of a status that grants strength based on tiles moved. || `1` |
| `TowerDefenseStatus` | Integer | The number of stacks of the sentry/tower defense status, granting stationary attack capabilities. || `1` |
| `TowerDefenseStatus2` | Integer | The number of stacks of the enhanced sentry/tower defense status. || `1` |
| [`TriggerWerewolfTransform`](./Arrays.md#array-triggerwerewolftransform) | Array / Number  | The number of stacks and probability of triggering the werewolf transformation. || `.5`<br>`[1 .15]`<br>`[1 .20]` |
| `TurnControlDelay` | Number | Specifies the delay in seconds before the unit regains turn control. || `.25` |
| [`VisualFlySwarm`](./Engine_StatusAndPassiveKeys.md#object-visualflyswarm) | Number / Object  | If non-zero, enables the visual fly swarm effect on the unit. || `{ . . . }`<br>`1` |

| [`AddDamageToElementDamage`](./Passives_and_Statuses.md#object-adddamagetoelementdamage) | Object  | Defines additional damage of a specific element added to the unit's attacks. | 6 | `{ . . . }` | `AddLeechesStatus` | Integer | The number of stacks of Leech status applied to the source, healing when dealing damage. | 0 | `1` | [`AddStatusesIfPersistentWeatherElement`](Miscellaneous.md#object-addstatusesifpersistentweatherelement) | Object | Specifies statuses applied if the persistent weather matches the given elements. | 0 | `{ . . . }` | [`AddStatusesToReceivedElementalDamage`](Miscellaneous.md#object-addstatusestoreceivedelementaldamage) | Object | An object defining statuses applied to the unit when it takes elemental damage of the specified types. | 0 | `{ . . . }` | [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | Contains status effects to add to the basic attack. | 178 | `{ . . . }` | [`AddStatusToElementDamage`](Items_and_Equipment.md#object-addstatustoelementdamage) | Object | An object that applies a specific status effect when dealing damage of a specified element. Contains sub-keys for the element and the status to apply. | 4 | `{ . . . }` | [`AddStatusToTrampleDamage`](Characters_and_Bosses.md#object-addstatustotrampledamage) | Object | An object whose nested keys define statuses applied to trample damage. | 2 | `{ . . . }` | `AddWeaponAux` | Integer / String | The amount or expression to add to the source's weapon auxiliary stat. | 0 | `"-max(min(X+1, item_aux), 0)"`<br>`-item_aux`<br>`1` | `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 0 | `-1`<br>`-2`<br>`1` | `AlphaCat` | Integer | The number of AlphaCat stacks applied to the source on kill. | 2 | `1` | [`ApplyPassives`](Abilities_and_Spells.md#object-applypassives) | Object | Specifies the passives or status effects to apply to the unit. | 0 | `{ . . . }` | `BigSplashDamage` | Integer | The additional tile radius of the splash damage effect applied by an attack. | 0 | `2` | `Bleed` | Array / Integer | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `1`<br>`10`<br>`2` | `Blind` | Array / Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 6 | `-1`<br>`1`<br>`2` | [`BloodRain`](Engine_GlobalModifierKeys.md#object-bloodrain) | Integer / Object | If non-zero, enables the blood rain visual effect. | 2 | `{ . . . }`<br>`1` | `BonusCritChance` | Integer | The flat percentage increase to critical hit chance. | 0 | `100`<br>`25`<br>`50` | `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 0 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` | `BonusDamageBasedOnDistance` | Integer | The flat bonus damage added per tile of distance between the source and target. | 0 | `1` | `BonusKnockbackDamage` | Integer | The extra damage dealt per tile of knockback. | 0 | `2`<br>`3`<br>`5` | `BrittleCharismaUp` | Integer | The number of stacks of temporary Charisma gained on kill. | 0 | `2` | `BrittleConstitutionUp` | Integer | The number of stacks of temporary Constitution gained on kill. | 0 | `2` | `BrittleDexterityUp` | Integer | The number of stacks of temporary Dexterity gained on kill. | 0 | `2` | `BrittleIntelligenceUp` | Integer | The number of stacks of temporary Intelligence gained on kill. | 0 | `2` | `BrittleLuckUp` | Integer | The number of stacks of temporary Luck gained on kill. | 0 | `2` | `BrittleSpeedUp` | Integer | The number of stacks of temporary Speed gained on kill. | 0 | `2` | `BrittleStrengthUp` | Integer | The number of stacks of temporary Strength gained on kill. | 0 | `2` | [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `{ . . . }`<br>`1`<br>`2`<br>`3` | `Burn` | Array / Enum / Integer | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` | `CapDamage` | Integer | The maximum amount of damage dealt, capping the total after all modifiers are applied. | 0 | `1` | `CaptureFamiliar` | Integer | The number of times to attempt to capture the target as a familiar. | 0 | `1` | `ChanceToBreak` | Integer | Specifies the percentage chance that the item breaks on use. | 0 | `100`<br>`15`<br>`20` | [`CharacterTypeGainsStatusAtBattleStart`](Engine_LogicKeys.md#object-charactertypegainsstatusatbattlestart) | Object | Defines status effects applied to characters with a specific tag at the start of a battle. | 1 | `{ . . . }` | `Charge` | Integer | The number of charge stacks applied. | 0 | `1`<br>`2`<br>`3` | `Charmed` | Array / Enum / Integer | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 0 | `1`<br>`2`<br>`3` | [`Cleanse`](#object-cleanse) | Integer / Object | The number of stacks of negative status effects removed from the target. | 2 | `{ . . . }`<br>`0`<br>`1` | `CompleteItemQuest` | Enum | Specifies the item quest ID to mark as complete on kill. | 0 | `BlackShard`<br>`Nuke`<br>`ScaldingOrb` | [`Conditional_HasStatus`](Abilities_and_Spells.md#object-conditional_hasstatus) | Object | Contains an inner effect block that only executes if the target has the specified status effect. | 0 | `{ . . . }` | [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `{ . . . }`<br>`1`<br>`10`<br>`2` | `ConjureRandomAbilityFromCat` | Integer | The number of random abilities created or given to the cat unit from a pool of cat-themed abilities. | 0 | `1` | `CrackMoonHead` | Integer | If set, cracks the MoonHead's head, triggering its death sequence. | 0 | `1` | `CurrentWeaponDamageUp` | Integer | The amount of temporary damage increase to the current weapon. | 0 | `1`<br>`3`<br>`5` | `DeleteObject` | Integer | If set, deletes the target object from the map. | 0 | `1` | `DestroyTrinket` | Integer | The number of trinkets destroyed. | 0 | `1` | [`Die`](Characters_and_Bosses.md#object-die) | Integer / Object | If set, kills the target immediately. | 0 | `{ . . . }`<br>`1`<br>`6` | `DieViolently` | Integer | If true, causes the target to die with a violent, explosive visual effect. | 0 | `1` | `DisableWeapon` | Integer | If set, disables the source's weapon, preventing its use. | 0 | `1` | `disallow_modifications` | Boolean | If true, the damage instance cannot be modified by external effects (e.g., passives, statuses). | 0 | `true` | `DisplaceToAbilityTarget` | Integer | If set, displaces the source to the ability's target location. | 0 | `1` | `DisplaceTowardsSource` | Integer | If set, displaces the target towards the source of the effect. | 0 | `1` | [`DistanceBonusDamage`](#object-distancebonusdamage) | Object | An object that adds bonus damage based on the distance from the target, with sub-keys for stacks and minimum range. | 0 | `{ . . . }` | `DivineShield` | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 0 | `1`<br>`2`<br>`4` | `DontHealEnemies` | Integer | If true, the healing effect does not affect enemy units. | 0 | `1` | `Doomed` | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. | 0 | `1`<br>`2`<br>`3` | `EmptyMana` | Integer | If non-zero, sets the unit's mana to empty when applied. | 0 | `1` | `EventBounty` | Integer | The number of stacks of Event Bounty applied, increasing event rewards. | 0 | `5` | `ExplodeCharacter` | Integer | The radius (in tiles) of an explosion centered on the character. | 0 | `5` | `ExplodeCharacter_NoDie` | Integer | The damage dealt when a character explodes without dying. | 0 | `1`<br>`5` | `ExplodeCharacter_Party` | Integer | The radius (in tiles) of an explosion centered on the character that also damages party members. | 0 | `5` | `ExplodeCharacter_PartyBoss` | Integer | The damage dealt to the party boss when it explodes. | 0 | `5` | `ExplodeCharacter_RockCrusher` | Integer | The number of RockCrusher explosion triggers applied to non-boss characters. | 0 | `5`<br>`9` | `ExplodeCharacter_RockCrusher_PetrifyBreak` | Integer | The damage dealt when a petrified RockCrusher explodes. | 0 | `5`<br>`9` | `FaceAway` | Integer | If set, forces the target to face away from the source. | 0 | `1` | `FaceCamera` | Integer | If non-zero, forces the character to rotate and face the camera. | 0 | `1` | `FactionConversion` | Integer | Converts the target to the caster's faction. | 0 | `1` | `Fear` | Array / Integer | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 0 | `1`<br>`10`<br>`2` | `Fights` | Number | The number of fights this status or effect persists for. | 4 | `1`<br>`3`<br>`99` | `FillMana` | Integer | The amount of mana restored, or an [amount, probability] array. | 0 | `1`<br>`[1 .10]`<br>`[1 .25]` | `FlatAIBonus` | Integer | A flat adjustment to the AI's evaluation score for this action; positive values encourage the AI to use it, negative values discourage it. | 0 | `-999999`<br>`100`<br>`999999` | `FlatLeech` | Integer | The flat amount of health restored to the source when dealing damage, applied after the hit. | 0 | `1`<br>`10`<br>`2` | `FloatingRockTrap` | Integer | The number of stacks of Floating Rock Trap applied to the target, dealing damage when stepped on. | 0 | `1` | `ForceImmediateMove` | Integer | If non-zero, forces the character to move instantly without waiting for normal action order. | 0 | `1` | `ForceMoveAway` | Integer | The distance to force the target away from the source. | 0 | `1` | `ForceMoveTowards` | Integer | The number of tiles to force the target to move toward the caster. | 0 | `1` | `ForceUseAbility_NonStack` | Enum | Forces the unit to use a specific non-stackable ability when the conditional roll is successful. | 0 | `Endeavor_Auto`<br>`Indigestion_Fart`<br>`Indigestion_Fart2` | [`ForceUseAbilityOnTarget`](#object-forceuseabilityontarget) | Object | Defines a chance to force the unit to use a specified ability on the target. | 0 | `{ . . . }` | `FullHeal` | Integer | If non-zero, fully restores the target's health. | 0 | `0`<br>`1` | `GainDisorder` | Enum | Specifies the name of the disorder gained. | 0 | `Chungus`<br>`Psychosis` | `GainDisorderFromPool_PostCast` | Enum | Specifies the pool of disorders the unit can gain after the spell is cast. | 0 | `forbidden_spell_consequences`<br>`forbidden_spell_consequences_crippling` | `GenericDebuff` | Integer | The number of stacks of a generic, untooltipped debuff applied to the target. | 0 | `1`<br>`10`<br>`100` | `HealRandomInjury` | Integer | The number of random injuries healed on the target. | 0 | `1` | `HealthGain` | Integer | The amount of health restored to the source. | 0 | `1`<br>`10`<br>`2` | `IgnoreDamage` | Integer | If set, the target ignores all damage for the duration. | 0 | `1` | [`ImmediateUseAbility`](#object-immediateuseability) | Enum / Object | Specifies the name of an ability to be triggered instantly from this effect. | 0 | `{ . . . }`<br>`FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` | `ImmediateUseAbility_Instant` | Enum | Specifies the name of an ability to use instantly as a passive effect. | 0 | `head_CrownOfHorns` | `Immobile` | Array / Integer | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 | `0`<br>`1`<br>`10%` | `Imprison` | Enum | Specifies the type of unit or object to summon as a prison. | 0 | `BeefyCharmedLeech`<br>`CharmedLeech`<br>`Fly` | `InnateElement` | Enum | Specifies the innate elemental type of the unit (e.g., Fire, Ice, Electric). | 8 | `Earth`<br>`Electric`<br>`Fire` | `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 0 | `25`<br>`50`<br>`999` | [`KnockbackIfCrit`](#object-knockbackifcrit) | Object | Defines knockback properties applied when a critical hit occurs. | 0 | `{ . . . }` | `KnockOutClone` | Enum | Specifies the ability ID used to knock out or remove the player's clone unit from battle. | 0 | `PlayerCat_MiniMiniMe` | `LaunchOffScreen` | Equation | A formula string that determines the knockback force to launch the unit off-screen. | 0 | `10+bonus_melee_ability_damage` | `LaunchOffScreenInstakill` | Integer | If non-zero, the unit is instantly killed and launched off-screen. | 0 | `1` | `LeaveBehindRockOnKnockback` | Integer | If non-zero, leaves behind a rock on each tile the target is knocked through. | 0 | `1` | `Leech` | Integer | The amount of health leeched from the target (heals the attacker). | 6 | `1`<br>`2` | `LeechPercent` | Integer | The percentage of damage dealt restored as health. | 0 | `50` | [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 0 | `{ . . . }`<br>`1`<br>`2`<br>`3` | `ManaGain` | Enum / Integer | The amount of mana restored to the source, which can be an expression. | 0 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` | [`Marked`](#object-marked) | Array / Integer / Object | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 0 | `{ . . . }`<br>`1`<br>`3`<br>`5` | `NonLethal` | Integer | If set to 1, damage dealt by the unit cannot kill enemies; it leaves them at 1 HP. | 0 | `1` | `OverrideDamage` | Integer | Overrides the damage of the current action to this flat value (can be negative to heal). | 0 | `-10`<br>`0`<br>`1` | [`passives`](Cat_Mutations.md#object-passives) | Object | A container object listing passive effects granted to the unit. | 5118 | `{ . . . }` | `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. | 0 | `1` | `PermanentDexterity` | Integer | The permanent amount of dexterity added or removed. | 0 | `1`<br>`2` | `PreEmptiveCounterNextAttacks` | Integer | The number of next incoming attacks that the unit will counter preemptively before they land. | 0 | `1` | `PurgeAll` | Integer | If non-zero, removes all temporary status effects (buffs, debuffs) from the target. | 0 | `1` | `RandomBonusDamage` | Integer | The maximum random bonus damage added to the base damage; the actual bonus is a random value between 0 and this number. | 0 | `25` | `RandomStatDown` | Array / Integer / String | The amount of random stat reduction applied, either as a fixed number, a formula string, or an array of [stacks, probability]. | 0 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`1` | `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` | [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | A collection of status effects; one is randomly chosen and applied to the target. | 0 | `{ . . . }` | `RefreshActPoints` | Integer | The amount of action points restored to the source. | 0 | `1` | `RefreshMovePoints` | Integer | The amount of movement points restored to the source. | 0 | `1` | `RefreshWeaponAbility` | Integer | The number of times the weapon's ability is refreshed. | 0 | `1` | `RemoteFlatLeech` | Integer | The flat amount of remote leech applied to the target on basic attack. | 0 | `1` | `RemoteLeech` | Integer | The amount of remote leech applied to the target on basic attack. | 0 | `1` | `RemoveAmbientLightEffects` | Float | The fade-out duration in seconds for ambient light effects. | 0 | `.5`<br>`4` | `RemoveGlobalModifiers` | Array | List of global modifier names to remove upon death. | 0 | `[BloodRain]` | `RemoveItem` | Enum | Specifies the item ID to remove from the source on kill. | 0 | `BlackShard`<br>`BlackShard_Glowing`<br>`ScaldingOrb` | `RemoveKnockback` | Integer | The number of knockback stacks removed from the received damage. | 0 | `1` | `RemoveMovePoints` | Integer | The number of move points to remove from the target, preventing them from moving. | 0 | `1` | `RemoveStatus` | Enum | The name of the status effect to remove from the source. | 0 | `AlphaCat`<br>`Brace`<br>`DodgeChance_Status` | [`RemoveStatusStacks`](Abilities_and_Spells.md#object-removestatusstacks) | Object | An object specifying a status name and the number of stacks to remove from the target. | 0 | `{ . . . }` | `RemoveTurnsThisRound` | Integer | The number of turns to remove from the target's turn order this round. | 0 | `1` | `RepairWeapon` | Array / Integer | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 0 | `1`<br>`6`<br>`99` | [`Revive`](#object-revive) | Integer / Object | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 2 | `{ . . . }`<br>`1`<br>`100%`<br>`50%` | `Rot` | Array / Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 0 | `-999999`<br>`1`<br>`2` | `ScatterRandomPickups` | Integer | The number of random pickups scattered around the target's location. | 0 | `2`<br>`5` | `SetHealth` | Integer | Sets the target's health to a specific flat value or percentage. | 0 | `1`<br>`100%`<br>`50%` | [`SetItemAux`](#object-setitemaux) | Object | Configures an item's auxiliary value by specifying a target slot and a formula for the new value. | 0 | `{ . . . }` | `SetKnockback` | Integer | The knockback distance to set for the damage instance, overriding default. | 0 | `0` | `SetShield` | Integer | Sets the target's shield value to a specific flat amount. | 0 | `0`<br>`88` | `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` | [`ShowFakeDamage`](Abilities_and_Spells.md#object-showfakedamage) | Object | Displays a fake damage number (with optional style) for visual effect without actually changing health. | 0 | `{ . . . }` | `ShowText` | String | Specifies the localization key for a popup text displayed on the target. | 0 | `"COMBAT_POPUP_BRAINSTORM"`<br>`"COMBAT_POPUP_RELOAD"`<br>`"COMBAT_POPUP_REPAIRED"` | [`Slow`](Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 | `{ . . . }`<br>`-1`<br>`1`<br>`2` | `SpawnBearTrap` | Integer | If non-zero, spawns a bear trap on the tile. | 0 | `1` | `SpawnBearTrapIfHitKills` | Integer | If non-zero, spawns a bear trap at the target's location upon a killing blow. | 0 | `1` | `SpawnBearTrapOnMiss` | Integer | The number of bear traps to spawn on the tile adjacent to the target when the unit misses an attack. | 0 | `1` | `SpawnFlames` | `Array` | An array containing the number of flame tiles to spawn and the chance per tile. | 0 | `[1, .20+.1*level]`<br>`[1, .20]` | `SpawnThingIfHitKills` | Enum | The name of the thing (e.g., a food type) to spawn at the target's location upon a killing blow. | 0 | `Bait`<br>`BigFood`<br>`BiggestFood` | `SpecificInjury` | Enum | The stat (str, spd, int) to which a specific injury is applied, reducing that stat. | 0 | `int`<br>`spd`<br>`str` | `SpeculativeMoveSelfCorpseOffMap` | Integer | If true, attempts to remove the character's corpse from the map, used for speculative AI targeting. | 0 | `1` | `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 0 | `-1`<br>`-2`<br>`-4` | `SpeedUp_WithoutInitiative` | Integer | The number of stacks of Speed Up that do not affect the unit's initiative (turn order) stat. | 0 | `1` | `StackingSandstorm` | Integer | If non-zero, enables the stacking sandstorm mechanic which increases damage per stack. | 0 | `1` | `StanceSwitchToMelee` | Integer | If set, switches the source to melee stance. | 0 | `1` | `StanceSwitchToRanged` | Integer | If set, switches the source to ranged stance. | 0 | `1` | `status` | Enum | Specifies the status effect to apply in a Temporary object. | 0 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` | [`StatusEachRoundEnd`](Cat_Mutations.md#object-statuseachroundend) | Object | An object listing status effects applied to the unit at the end of each round. | 2 | `{ . . . }` | `StatusImmunity` | Array / Enum | A list of status effect names the unit is immune to. | 0 | `Burn`<br>`Poison`<br>`Tarred` | [`StatusRandomEnemiesOnBattleStart`](Events_and_Encounters.md#object-statusrandomenemiesonbattlestart) | Object | An object that applies a status effect to a random number of enemies at the start of battle, with sub-keys for count and the status. | 0 | `{ . . . }` | `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 0 | `"max(int, 0)"`<br>`-1`<br>`-2` | `Stun` | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 0 | `1`<br>`2`<br>`3` | `T2CopyCat` | Integer | The number of T2 Clone copies created or applied to the target cat. | 0 | `1` | `TakeExtraTurn` | Integer | The number of extra turns granted to the source. | 0 | `1` | `TempDexterityUp` | Enum | The number of temporary dexterity stacks applied, or a string alias like 'X'. | 0 | `2`<br>`X` | `TempLuckUp` | Integer | The amount of temporary luck increase. | 0 | `2`<br>`99` | [`Temporary`](Abilities_and_Spells.md#object-temporary) | Object | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 0 | `{ . . . }` | [`TempPassiveUntilSettled`](Characters_and_Bosses.md#object-temppassiveuntilsettled) | Object | An object containing a temporary passive that is applied until the character's position is settled. | 0 | `{ . . . }` | [`TempPassiveWhileHasStatus`](Abilities_and_Spells.md#object-temppassivewhilehasstatus) | Object | An object defining passives temporarily granted to the unit while it has a specific status effect. | 0 | `{ . . . }` | `TempStrengthUp` | Equation | The number of stacks of temporary Strength Up applied to the unit. | 0 | `1`<br>`2`<br>`X` | `TempTrampleUntilSettled` | Integer | The number of stacks of temporary Trample applied to the source, allowing movement through enemies until the source ends its turn. | 0 | `3` | `Trample` | Integer | The amount of bonus damage dealt when moving through an enemy. | 14 | `1`<br>`3`<br>`4` | `UseAbility_Madness` | Enum | Determines which ability type (e.g., weapon) is forcibly used when Madness triggers. | 0 | `weapon` | `UseAbility_NonStack` | Enum | Specifies an ability to use on kill that does not stack with itself. | 0 | `BBTransformZealot`<br>`GenericRage` | `Vaporize` | Integer | Removes the target from play, preventing its corpse from being interacted with. | 0 | `1`<br>`20` | `VaporizeCorpse` | Integer | If set, vaporizes the target's corpse, preventing revival. | 0 | `1` | `VaporizeCorpseFlipAdvantage` | `Array` | The number of stacks and probability of vaporizing a corpse to gain loot flip advantage. | 0 | `[1 .33]` | `VaporizeInanimate` | Integer | If non-zero, instantly destroys inanimate objects (corpses, rocks) as if they were vaporized. | 0 | `1` | `VisualFX` | Enum | Specifies the name of the visual effect to play. | 0 | `BigMagicMissileBlast`<br>`Bolt`<br>`Cleanse` | [`Weakness`](Passives_and_Statuses.md#object-weakness) | Array / Integer / Object | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 4 | `{ . . . }`<br>`1`<br>`2`<br>`3` | `WeaponAuxMultiplier` | Number | A multiplier string (e.g., '.5') for the weapon's auxiliary counter on kill. | 0 | `.5`

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
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `-1`<br>`-2`<br>`1` |

</details>


---


#### `AddPassivesToMinions`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 36

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 | `1`<br>`2`<br>`3` |
| [`Quivered`](./Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 10 | `1`<br>`2`<br>`5` |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `PoisonThorns` | Integer | The number of stacks of Poison applied to melee attackers when they hit this unit. | 6 | `1`<br>`2`<br>`3` |
| [`tag_filter`](./Enums.md#enum-tag_filter) | Enum | Specifies a tag (e.g., 'crow', 'rock', 'grub_familiar') used to filter which units a status or effect applies to. | 3 | `crow`<br>`grub_familiar`<br>`rock` |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `-1`<br>`-2`<br>`1` |
| [`Buddy`](./Passives_and_Statuses.md#object-buddy) | Enum / Object  | Specifies a buddy unit that accompanies or is spawned alongside the unit, with optional reclaim and targeting properties. || `{ . . . }`<br>`BoyDino`<br>`CaveCatDad`<br>`Chubs` |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `1`<br>`2`<br>`4` |
| [`ForceAttack`](./Miscellaneous.md#object-forceattack) | Integer / Object  | If set to 1, forces the target to perform an attack against a random or specified target. || `{ . . . }`<br>`1` |
| `HealthGain` | Integer | The amount of health restored to the source. || `1`<br>`10`<br>`2` |

</details>


---


#### `AddSelfStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`Quivered`](./Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 10 | `1`<br>`2`<br>`5` |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `1`<br>`10`<br>`2` |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. || `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`RandomMagicMissile`](./Miscellaneous.md#object-randommagicmissile) | Integer / Object  | The number of random magic missiles fired, or an object defining its properties. || `{ . . . }`<br>`1`<br>`10`<br>`2` |

</details>


---


#### `AddSelfStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RepairWeapon`](./Arrays.md#array-repairweapon) | Array / Integer  | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. || `1`<br>`6`<br>`99` |
| `ChanceToBreak` | Integer | Specifies the percentage chance that the item breaks on use. | 0 | `100`<br>`15`<br>`20` |
| [`RepairWeapon`](./Arrays.md#array-repairweapon) | Array / Integer | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. | 0 | `1`<br>`6`<br>`99` |

</details>


---


#### `AddStatusToAllDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Blind`](./Arrays.md#array-blind) | Array / Integer  | The amount of blind stacks applied, or an [stacks, probability] array. | 6 | `-1`<br>`1`<br>`2` |
| [`Blind`](./Arrays.md#array-blind) | Array / Integer | The amount of blind stacks applied, or an [stacks, probability] array. | 6 | `-1`<br>`1`<br>`2` |
| [`Conditional_HasStatus`](./Passives_and_Statuses.md#object-conditional_hasstatus) | Object  | Contains an inner effect block that only executes if the target has the specified status effect. | 3 | `{ . . . }` |
| [`Conditional_HasTag`](./Passives_and_Statuses.md#object-conditional_hastag) | Object  | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 3 | `{ . . . }` |
| `must_do_damage` | Boolean | If true, the status or effect will only be applied if the attack or ability actually deals damage. | 3 | `true` |
| [`Rot`](./Arrays.md#array-rot) | Array / Integer  | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. || `-999999`<br>`1`<br>`2` |
| [`KnockbackIfCrit`](./Miscellaneous.md#object-knockbackifcrit) | Object  | Defines knockback properties applied when a critical hit occurs. | 0 | `{ . . . }` |
| `LeaveBehindRockOnKnockback` | Integer | If non-zero, leaves behind a rock on each tile the target is knocked through. | 0 | `1` |
| `NonLethal` | Integer | If set to 1, damage dealt by the unit cannot kill enemies; it leaves them at 1 HP. | 0 | `1` |
| [`Rot`](./Arrays.md#array-rot) | Array / Integer | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. | 0 | `-999999`<br>`1`<br>`2` |
| `BonusKnockbackDamage` | Integer | The extra damage dealt per tile of knockback. | 0 | `2`<br>`3`<br>`5` |

</details>


---


#### `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 248

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `1`<br>`10`<br>`2` |
| [`Bruise`](./Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Poison`](./Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 | `1`<br>`10`<br>`2` |
| [`Blind`](./Arrays.md#array-blind) | Array / Integer  | The amount of blind stacks applied, or an [stacks, probability] array. | 6 | `-1`<br>`1`<br>`2` |
| [`Confusion`](./Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `Leech` | Integer | The amount of health leeched from the target (heals the attacker). | 6 | `1`<br>`2` |
| [`Conditional_Ally`](./Passives_and_Statuses.md#object-conditional_ally) | Object  | Defines effects that apply only if the target is an ally, with an optional else block for non-allies. | 5 | `{ . . . }` |
| [`Immobile`](./Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 | `0`<br>`1`<br>`10%` |
| [`Slow`](./Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 | `{ . . . }`<br>`-1`<br>`1`<br>`2` |
| [`Weakness`](./Passives_and_Statuses.md#object-weakness) | Array / Integer / Object  | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 4 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Conditional_Enemy`](./Passives_and_Statuses.md#object-conditional_enemy) | Object  | An object containing status effects or actions applied only if the target is an enemy. | 3 | `{ . . . }` |
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 3 | `{ . . . }` |
| [`Conditional_Adjacent`](./Passives_and_Statuses.md#object-conditional_adjacent) | Object  | An object whose nested keys define statuses or effects applied to or by units that are adjacent to the unit. | 2 | `{ . . . }` |
| [`Conditional_Shielded`](./Passives_and_Statuses.md#object-conditional_shielded) | Object  | An object containing effects that are only applied if the target has a shield active. | 2 | `{ . . . }` |
| [`Leeches`](./Engine_StatusAndPassiveKeys.md#object-leeches) | Integer / Object  | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`MagicWeakness`](./Arrays.md#array-magicweakness) | Array / Integer  | The amount of magic weakness stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`2`<br>`3` |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`SoulLink`](./Engine_StatusAndPassiveKeys.md#object-soullink) | Integer / Object  | The number of soul link stacks applied. | 2 | `{ . . . }`<br>`1` |
| [`Conditional_HasTag`](./Passives_and_Statuses.md#object-conditional_hastag) | Object  | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 1 | `{ . . . }` |
| [`Conditional_SourceHasTag`](./Passives_and_Statuses.md#object-conditional_sourcehastag) | Object  | Defines a conditional block that applies effects only if the source of the effect has a specified tag. | 1 | `{ . . . }` |
| [`Burn`](./Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` |
| [`Else`](./Passives_and_Statuses.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ . . . }` |
| [`ApplyToSource`](./Passives_and_Statuses.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). || `{ . . . }` |
| [`BounceObject`](./Miscellaneous.md#object-bounceobject) | Enum / Object  | Specifies the object or projectile to spawn and bounce from the target. || `{ . . . }`<br>`AllyRotFly`<br>`Amoeba`<br>`BeefyCharmedLeech` |
| [`BurgleCoin`](./Arrays.md#array-burglecoin) | Array / Integer  | The number of coins stolen from the target, or an array of `[number, probability]`. || `1`<br>`3`<br>`[1 .5]` |
| [`ChangeTile`](./Passives_and_Statuses.md#object-changetile) | Enum / Object  | Specifies the tile type to change to, or an object defining tile change parameters (tile type and area of effect). || `{ . . . }`<br>`BlankTile`<br>`BrambleTile`<br>`CreepTile` |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. || `1`<br>`2`<br>`3` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`10`<br>`2` |
| `FlatLeech` | Integer | The flat amount of health restored to the source when dealing damage, applied after the hit. || `1`<br>`10`<br>`2` |
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. || `1`<br>`2`<br>`[1 .01]` |
| [`GainDisorderFromPool`](./Miscellaneous.md#object-gaindisorderfrompool) | Enum / Object  | Specifies a pool of disorders from which one is randomly gained on basic attack, with an optional chance. || `{ . . . }`<br>`all_disorders` |
| `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). || `25`<br>`50`<br>`999` |
| `Knockback` | Integer | The number of tiles the target is pushed away from the source on hit. || `1`<br>`10`<br>`2` |
| [`KnockOutCoin`](./Miscellaneous.md#object-knockoutcoin) | Integer / Object  | The number of coins knocked out, with an optional probability or an object with stacks and chance. || `{ . . . }`<br>`1`<br>`[1 .5]` |
| [`KnockUpAndAway`](./Miscellaneous.md#object-knockupandaway) | Object  | Contains parameters for launching the target upward and away from the source, including stacks and distance. || `{ . . . }` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. || `-1`<br>`-2`<br>`-4` |
| [`Madness`](./Passives_and_Statuses.md#object-madness) | Array / Enum / Integer / Object  | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. || `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `ManaLeeches` | Integer | The number of mana leech stacks applied. || `1`<br>`2` |
| [`Marked`](./Engine_StatusAndPassiveKeys.md#object-marked) | Array / Integer / Object  | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. || `{ . . . }`<br>`1`<br>`3`<br>`5` |
| `OverrideChainKnockback` | Integer | The custom number of tiles for chain knockback, overriding the default. || `0`<br>`1`<br>`10` |
| `OverrideChainKnockbackDamage` | String | A formula string that overrides the damage dealt by chain knockback (e.g., "3+bonus_melee_ability_damage"). || `0`<br>`3+bonus_melee_ability_damage` |
| [`Petrify`](./Arrays.md#array-petrify) | Array / Integer  | The amount of petrify stacks applied, or an [stacks, probability] array. || `1`<br>`[1 .15]`<br>`[1 .1]` |
| `Possessed` | Integer | The number of possession stacks applied, or a template with name and tooltips. || `1` |
| `PullSourceToTarget` | Integer | The amount of tiles the source is pulled towards the target after the attack. || `1` |
| [`Rot`](./Arrays.md#array-rot) | Array / Integer  | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. || `-999999`<br>`1`<br>`2` |
| `SpiderInfested` | Integer | The number of spider infestation stacks applied. || `1`<br>`2`<br>`4` |
| `SplashDamage` | Integer | The radius (in tiles) for splash damage applied to adjacent targets. || `1`<br>`2` |
| [`SpreadDisease`](./Passives_and_Statuses.md#object-spreaddisease) | Object  | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. || `{ . . . }` |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`2`<br>`3` |
| [`Tangled`](./Miscellaneous.md#object-tangled) | Array / Integer / Object  | The number of stacks of the Tangled status effect applied, or an object defining its properties such as `stacks` and `alt_art`. || `{ . . . }`<br>`1`<br>`2`<br>`[1, .05]` |
| [`VisualFXTile`](./Enums.md#enum-visualfxtile) | Enum  | Specifies the name of the visual effect to play on the target tile. || `Bolt`<br>`BurnTrigger`<br>`Explosion` |
| `Webbed` | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. || `1`<br>`2`<br>`[1 .1]` |

</details>


---


#### `AddStatusToBasicMeleeAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `1`<br>`10`<br>`2` |
| [`Bruise`](./Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Confusion`](./Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Immobile`](./Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 | `0`<br>`1`<br>`10%` |
| `Knockback` | Integer | The number of tiles the target is pushed away from the source on hit. || `1`<br>`10`<br>`2` |
| [`KnockUpAndAway`](./Miscellaneous.md#object-knockupandaway) | Object  | Contains parameters for launching the target upward and away from the source, including stacks and distance. || `{ . . . }` |
| [`SpreadDisease`](./Passives_and_Statuses.md#object-spreaddisease) | Object  | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. || `{ . . . }` |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`2`<br>`3` |

</details>


---


#### `AddStatusToElementDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AddDamageToElementDamage`](./Passives_and_Statuses.md#object-adddamagetoelementdamage) | Object  | Defines additional damage of a specific element added to the unit's attacks. | 6 | `{ . . . }` |
| [`Conditional_Corpse`](./Passives_and_Statuses.md#object-conditional_corpse) | Object  | Contains an inner effect block that only executes if the target is a corpse. | 2 | `{ . . . }` |
| [`element`](./Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 1 | `Electric`<br>`Fire`<br>`Gravity` |
| [`Burn`](./Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`2`<br>`3` |

</details>


---


#### `AddStatusToKnockbackDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bruise`](./Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Bruise`](./Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`2`<br>`3` |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 0 | `1`<br>`2`<br>`3` |

</details>


---


#### `AddStatusToSpells`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Leech` | Integer | The amount of health leeched from the target (heals the attacker). | 6 | `1`<br>`2` |
| `Leech` | Integer | The amount of health leeched from the target (heals the attacker). | 6 | `1`<br>`2` |
| [`Conditional_Enemy`](./Passives_and_Statuses.md#object-conditional_enemy) | Object  | An object containing status effects or actions applied only if the target is an enemy. | 1 | `{ . . . }` |
| `LeechPercent` | Integer | The percentage of damage dealt restored as health. | 0 | `50` |

</details>


---


#### `AddStatusToTrampleDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bruise`](./Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Bruise`](./Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Cleave`](./Miscellaneous.md#object-cleave) | Integer / Object  | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. || `{ . . . }`<br>`1` |
| [`Cleave`](./Miscellaneous.md#object-cleave) | Integer / Object  | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. | 0 | `{ . . . }`<br>`1` |

</details>


---


#### `AddStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `1`<br>`10`<br>`2` |
| `Leech` | Integer | The amount of health leeched from the target (heals the attacker). | 6 | `1`<br>`2` |
| [`Cleave`](./Miscellaneous.md#object-cleave) | Integer / Object  | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. || `{ . . . }`<br>`1` |
| `PullSourceToKnockbackImmuneTarget` | Integer | The amount of pull force applied to the source toward a knockback-immune target. || `1` |

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
| `YOffset` | Number | The vertical offset applied to the unit's visual position, used for floating or hovering effects. | 6 | `-.18`<br>`.25`<br>`.35` |
| `Flying` | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 2 | `1` |

</details>


---


#### `ApplyStatusIfCrit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `1`<br>`10`<br>`2` |
| [`Purge`](./Engine_StatusAndPassiveKeys.md#object-purge) | Integer / Object  | The number of status effects to purge from the target. | 2 | `{ . . . }`<br>`0`<br>`3` |
| [`ApplyToSource`](./Passives_and_Statuses.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). || `{ . . . }` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. || `-1`<br>`-2`<br>`-4` |

</details>


---


#### `ApplyStatusesToRandomEnemiesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 3 | `0`<br>`1`<br>`10` |
| `Bounty` | Integer | The number of bounty stacks applied to enemies, increasing rewards on defeat. || `1`<br>`3` |
| [`Marked`](./Engine_StatusAndPassiveKeys.md#object-marked) | Array / Integer / Object  | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. || `{ . . . }`<br>`1`<br>`3`<br>`5` |

</details>


---


#### `CatchProjectiles`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. | 5441 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. | 5027 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`Quivered`](./Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 10 | `1`<br>`2`<br>`5` |
| `ally_chance` | Integer | The percentage chance for an ally to catch incoming projectiles. | 5 | `100%`<br>`15%` |
| [`chance`](./Enums.md#enum-chance) | Float | A probability (decimal or percentage) for a form change or other effect to occur. | 1 | `.02`<br>`.1`<br>`.15` |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `-1`<br>`-2`<br>`1` |

</details>


---


#### `CharacterTypeGainsStatusAtBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 981 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |
| [`Stealth`](./Arrays.md#array-stealth) | Array / Integer  | The number of stealth stacks applied. | 2 | `1`<br>`2`<br>`[1 .1]` |
| [`Conditional_Flying`](Engine_Uncategorized_Resources.md#conditional_flying) | Object | Defines a conditional block that applies effects or actions only to flying units. | 1 | `{ . . . }` |
| [`Else`](./Passives_and_Statuses.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ . . . }` |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `-1`<br>`-2`<br>`1` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`10`<br>`2` |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`2`<br>`3` |

</details>


---


#### `CritsApplyStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `1`<br>`10`<br>`2` |
| [`Bruise`](./Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Confusion`](./Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Immobile`](./Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 | `0`<br>`1`<br>`10%` |
| [`Weakness`](./Passives_and_Statuses.md#object-weakness) | Array / Integer / Object  | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 4 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Conditional_HasStatus`](./Passives_and_Statuses.md#object-conditional_hasstatus) | Object  | Contains an inner effect block that only executes if the target has the specified status effect. | 2 | `{ . . . }` |
| [`Else`](./Passives_and_Statuses.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ . . . }` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`10`<br>`2` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. || `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`2`<br>`3` |

</details>


---


#### `ExtraStatusWhenDealingDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_PartyMember`](./Passives_and_Statuses.md#object-conditional_partymember) | Object  | A conditional block that executes its child actions only if the target is a party member. | 3 | `{ . . . }` |
| [`Conditional_Ally`](./Passives_and_Statuses.md#object-conditional_ally) | Object  | Defines effects that apply only if the target is an ally, with an optional else block for non-allies. | 2 | `{ . . . }` |

</details>


---


#### `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 73

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 62 | `{ . . . }` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 54 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`knockback`](./Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 24 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| [`Poison`](./Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 | `1`<br>`10`<br>`2` |
| [`InnateElement`](./Enums.md#enum-innateelement) | Enum | Specifies the innate elemental type of the unit (e.g., Fire, Ice, Electric). | 8 | `Earth`<br>`Electric`<br>`Fire` |
| [`AddDamageToElementDamage`](./Passives_and_Statuses.md#object-adddamagetoelementdamage) | Object  | Defines additional damage of a specific element added to the unit's attacks. | 6 | `{ . . . }` |
| [`Immobile`](./Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 | `0`<br>`1`<br>`10%` |
| [`Weakness`](./Passives_and_Statuses.md#object-weakness) | Array / Integer / Object  | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 4 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`AddStatusToElementDamage`](./Passives_and_Statuses.md#object-addstatustoelementdamage) | Object  | An object that applies a specific status effect when dealing damage of a specified element. Contains sub-keys for the element and the status to apply. | 4 | `{ . . . }` |
| [`damage`](./Arrays.md#array-damage) | Equation | Specifies the amount of damage dealt, can be a number or expression. | 2 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| `cant_miss` | Boolean | If true, the damage instance always hits its target regardless of accuracy or evasion. | 1 | `true` |
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. || `1`<br>`2`<br>`[1 .01]` |
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 0 | `[`<br>`[Heat Fire]` |
| [`SpreadDisease`](./Passives_and_Statuses.md#object-spreaddisease) | Object  | Defines the parameters for spreading a disease, including chance, disease type, and whether it can apply to any target. || `{ . . . }` |
| [`StatusImmunity`](./Arrays.md#array-statusimmunity) | Array / Enum  | A list of status effect names the unit is immune to. | 0 | `Burn`<br>`Poison`<br>`Tarred` |

</details>


---


#### `PassiveAfterXKills`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 5118 | `{ . . . }` |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

</details>


---


#### `PassiveAtHealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 5118 | `{ . . . }` |
| [`mode`](./Enums.md#enum-mode) | Enum | Specifies the comparison mode (equal, greater, less_or_equal, etc.) used for a conditional check. | 9 | `equal`<br>`greater`<br>`greater_or_equal` |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Enum / Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 9 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |

</details>


---


#### `PassiveAtStatThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 5118 | `{ . . . }` |
| [`mode`](./Enums.md#enum-mode) | Enum | Specifies the comparison mode (equal, greater, less_or_equal, etc.) used for a conditional check. | 13 | `equal`<br>`greater`<br>`greater_or_equal` |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Enum / Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 13 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |

</details>


---


#### `PassiveGroup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `-1`<br>`-2`<br>`1` |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. || `{ . . . }` |
| `CharismaUp` | Enum / Integer | The amount of charisma change, or a keyword like 'item_aux'. || `-1`<br>`-2`<br>`1` |
| [`FormChange`](./Miscellaneous.md#object-formchange) | Enum / Object  | Specifies the form the target transforms into, either as a string or an object with a `form` field. || `{ . . . }`<br>`Big`<br>`BigHolding`<br>`BigHoldingCat` |
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. || `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `-1`<br>`-2`<br>`-4` |

</details>


---


#### `PassiveWhenAffectedByElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 5118 | `{ . . . }` |
| [`element`](./Arrays.md#array-element) | Array / Enum  | Specifies which element(s) the conditional checks against. | 1 | `Electric`<br>`Fire`<br>`Gravity` |

</details>


---


#### `PassiveWhenAtFullMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Brace`](./Passives_and_Statuses.md#object-brace) | Enum / Integer / Object  | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 20 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `Flying` | Integer | If set to 1, grants the unit the Flying passive, allowing movement over obstacles and ignoring terrain penalties. | 2 | `1` |

</details>


---


#### `PassiveWhenDead`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`StatusEachTurnBegin`](./Passives_and_Statuses.md#object-statuseachturnbegin) | Object  | Specifies status effects applied to the unit at the start of each of its turns. | 16 | `{ . . . }` |
| [`AutocastEachRound`](./Passives_and_Statuses.md#object-autocasteachround) | Enum / Object  | Contains an ability name and optional 'even_if_stunned' flag to autocast each round. | 4 | `{ . . . }`<br>`SpiderReturn` |
| [`AutocastEachRound`](./Passives_and_Statuses.md#object-autocasteachround) | Enum / Object  | Contains an ability name and optional 'even_if_stunned' flag to autocast each round. | 4 | `{ . . . }`<br>`SpiderReturn` |
| [`StatusEachRoundEnd`](./Passives_and_Statuses.md#object-statuseachroundend) | Object  | An object listing status effects applied to the unit at the end of each round. | 2 | `{ . . . }` |
| [`AddStatusToTrampleDamage`](./Passives_and_Statuses.md#object-addstatustotrampledamage) | Object  | An object whose nested keys define statuses applied to trample damage. | 2 | `{ . . . }` |

</details>


---


#### `PassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 5118 | `{ . . . }` |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 6 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |

</details>


---


#### `PassiveWhileInMonkMeleeStance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 | `1`<br>`2`<br>`3` |
| [`Brace`](./Passives_and_Statuses.md#object-brace) | Enum / Integer / Object  | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 20 | `{ . . . }`<br>`1`<br>`10`<br>`2` |

</details>


---


#### `RandomPassivePool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TransformInXTurns`](./Passives_and_Statuses.md#object-transforminxturns) | Object  | Defines a delayed transformation after a set number of turns, with optional target object and initiative handling. || `{ . . . }` |

</details>


---


#### `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 35

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 36 | `1`<br>`10`<br>`100` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 36 | `1`<br>`2`<br>`3` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 | `1`<br>`2`<br>`3` |
| [`Brace`](./Passives_and_Statuses.md#object-brace) | Enum / Integer / Object  | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 20 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Quivered`](./Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 10 | `1`<br>`2`<br>`5` |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `1`<br>`10`<br>`2` |
| `BleedThorns` | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 8 | `1`<br>`2`<br>`3` |
| [`Bruise`](./Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Poison`](./Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 | `1`<br>`10`<br>`2` |
| [`Blind`](./Arrays.md#array-blind) | Array / Integer  | The amount of blind stacks applied, or an [stacks, probability] array. | 6 | `-1`<br>`1`<br>`2` |
| [`Confusion`](./Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 6 | `1`<br>`2`<br>`3` |
| `MoveQuivered` | Integer | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 6 | `1`<br>`2`<br>`[1, 0.1]` |
| [`Immobile`](./Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 | `0`<br>`1`<br>`10%` |
| [`Slow`](./Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 | `{ . . . }`<br>`-1`<br>`1`<br>`2` |
| [`Weakness`](./Passives_and_Statuses.md#object-weakness) | Array / Integer / Object  | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 4 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`BackflipWhenTargeted`](./Passives_and_Statuses.md#object-backflipwhentargeted) | Enum / Integer / Object  | The number of backflip charges, or an object defining its ability. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`X` |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 2 | `1`<br>`10`<br>`100` |
| [`MagicWeakness`](./Arrays.md#array-magicweakness) | Array / Integer  | The amount of magic weakness stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`2`<br>`3` |
| [`PoisonLace`](./Engine_StatusAndPassiveKeys.md#object-poisonlace) | Integer / Object / String  | Integer or fractional string (e.g., 'X/3') specifying the duration or intensity of the PoisonLace effect. | 2 | `{ . . . }`<br>`"X/3"`<br>`"X/5"`<br>`1` |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`Reflect`](./Engine_StatusAndPassiveKeys.md#object-reflect) | Integer / Object  | The amount of reflect stacks applied. | 2 | `{ . . . }`<br>`1`<br>`5` |
| [`Burn`](./Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` |
| [`Infested`](./Engine_StatusAndPassiveKeys.md#object-infested) | Integer / Object  | The number of stacks of Infested applied. | 1 | `{ . . . }`<br>`1` |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `-1`<br>`-2`<br>`1` |
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). || `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| `Charge` | Integer | The number of charge stacks applied. || `1`<br>`2`<br>`3` |
| `CharismaUp` | Enum / Integer | The amount of charisma change, or a keyword like 'item_aux'. || `-1`<br>`-2`<br>`1` |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. || `1`<br>`2`<br>`3` |
| [`ConstitutionUp`](./Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. || `-1`<br>`-2`<br>`1` |
| `DelayedPain` | Integer | The number of stacks of DelayedPain applied, dealing damage after a delay. || `1` |
| `DexterityUp` | Enum / Integer | The amount of dexterity change, or a keyword like 'item_aux'. || `-1`<br>`1`<br>`2` |
| `DiminishingHealthRegen` | Integer | The number of diminishing health regen stacks applied. || `1`<br>`2`<br>`3` |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `1`<br>`2`<br>`4` |
| `Drowsy` | Integer | The amount of drowsy stacks applied, or an [stacks, probability] array. || `1`<br>`8` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`10`<br>`2` |
| [`FormChange`](./Miscellaneous.md#object-formchange) | Enum / Object  | Specifies the form the target transforms into, either as a string or an object with a `form` field. || `{ . . . }`<br>`Big`<br>`BigHolding`<br>`BigHoldingCat` |
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. || `1`<br>`2`<br>`[1 .01]` |
| [`GainCoins`](./Arrays.md#array-gaincoins) | Array / Integer  | The amount of coins gained, or a [min, max] range. || `-5`<br>`1`<br>`2` |
| `Hex` | Integer | The number of stacks of Hex applied, causing the target to take increased damage from spells. || `1` |
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. || `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `Lifesteal` | Integer | The amount of lifesteal stacks applied. || `1`<br>`3` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. || `-1`<br>`-2`<br>`-4` |
| [`Madness`](./Passives_and_Statuses.md#object-madness) | Array / Enum / Integer / Object  | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. || `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `ManaGain` | Enum / Integer | The amount of mana restored to the source, which can be an expression. || `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`Marked`](./Engine_StatusAndPassiveKeys.md#object-marked) | Array / Integer / Object  | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. || `{ . . . }`<br>`1`<br>`3`<br>`5` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. || `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| `Ostracized` | Integer | The number of stacks of Ostracized applied. || `1`<br>`2`<br>`4` |
| `PermanentCharisma` | Integer | The amount of permanent Charisma added to the unit's base stats. || `1`<br>`2` |
| `PermanentLuck` | Integer | The amount of permanent Luck added to the unit's base stats. || `1`<br>`2` |
| `PermanentStrength` | Integer | The amount of permanent bonus strength (physical damage modifier) granted. || `1`<br>`2` |
| [`Petrify`](./Arrays.md#array-petrify) | Array / Integer  | The amount of petrify stacks applied, or an [stacks, probability] array. || `1`<br>`[1 .15]`<br>`[1 .1]` |
| [`RandomStatDown`](./Arrays.md#array-randomstatdown) | Array / Integer / String  | The amount of random stat reduction applied, either as a fixed number, a formula string, or an array of [stacks, probability]. || `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`1` |
| [`Rot`](./Arrays.md#array-rot) | Array / Integer  | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. || `-999999`<br>`1`<br>`2` |
| `Scrambled` | Integer | The number of stacks of Scrambled applied. || `1`<br>`2` |
| [`Sleep`](./Arrays.md#array-sleep) | Array / Integer  | The amount of sleep stacks applied, or an [stacks, probability] array. || `1`<br>`2`<br>`3` |
| [`SpawnCoinAnywhere`](./Arrays.md#array-spawncoinanywhere) | Array / Integer  | The number of coins to spawn. If an array, the second value is the probability of spawning them anywhere. || `1`<br>`[1 .5]` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `-1`<br>`-2`<br>`-4` |
| `SpellDamageUp` | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. || `1`<br>`3` |
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. || `"max(int, 0)"`<br>`-1`<br>`-2` |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`2`<br>`3` |
| [`Tarred`](./Arrays.md#array-tarred) | Array / Integer  | The amount of tarred stacks applied, or an [stacks, probability] array. || `1`<br>`2`<br>`[1 .1]` |
| `TempCounterAttack` | Integer | The number of turns TempCounterAttack lasts, ticking down at the start of the unit's turn. || `1` |

</details>


---


#### `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 31

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 62 | `{ . . . }` |
| [`type`](./Enums.md#enum-type) | Enum | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 54 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`knockback`](./Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 3 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| [`damage`](./Arrays.md#array-damage) | Equation | Specifies the amount of damage dealt, can be a number or expression. | 2 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`elements`](./Arrays.md#array-elements) | Array | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. | 0 | `[`<br>`[Heat Fire]` |

</details>


---


#### `StatusAfterCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TempDamageUp` | Integer | The amount of temporary damage increase applied. || `-1`<br>`1`<br>`2` |
| `TempRangeUp` | Integer | The amount of temporary range increase applied. || `1`<br>`2`<br>`20` |
| `TempSpellDamageUp` | Integer | The amount of temporary spell damage increase applied. || `1` |
| [`UseAbility`](./Passives_and_Statuses.md#object-useability) | Enum / Object  | The name of the ability the target is forced to use. || `{ . . . }`<br>`GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |

</details>


---


#### `StatusAfterXTurns`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. || `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |

</details>


---


#### `StatusAllCharactersOnSpawn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Poison`](./Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 | `1`<br>`10`<br>`2` |
| [`Conditional_Boss`](./Passives_and_Statuses.md#object-conditional_boss) | Object  | Contains effects that apply only if the target is a boss enemy. | 2 | `{ . . . }` |
| [`Conditional_PartyMember`](./Passives_and_Statuses.md#object-conditional_partymember) | Object  | A conditional block that executes its child actions only if the target is a party member. | 1 | `{ . . . }` |
| [`Conditional_Tiny`](Engine_Uncategorized_Resources.md#conditional_tiny) | Object | Defines a conditional block that applies effects only to tiny-sized units. | 1 | `{ . . . }` |
| [`Else`](./Passives_and_Statuses.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ . . . }` |

</details>


---


#### `StatusAlliesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`Conditional_Adjacent`](./Passives_and_Statuses.md#object-conditional_adjacent) | Object  | An object whose nested keys define statuses or effects applied to or by units that are adjacent to the unit. | 1 | `{ . . . }` |
| `exclude_self` | Boolean | If true, the effect does not apply to the source unit itself. | 1 | `false` |

</details>


---


#### `StatusAlliesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`Brace`](./Passives_and_Statuses.md#object-brace) | Enum / Integer / Object  | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 20 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`ConstitutionUp`](./Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. || `-1`<br>`-2`<br>`1` |
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. || `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. || `-1`<br>`-2`<br>`-4` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `-1`<br>`-2`<br>`-4` |
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. || `"max(int, 0)"`<br>`-1`<br>`-2` |

</details>


---


#### `StatusAlliesOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Reanimate`](./Engine_StatusAndPassiveKeys.md#object-reanimate) | Integer / Object  | The percentage chance to reanimate the target. | 4 | `{ . . . }`<br>`100%`<br>`33%`<br>`50%` |
| `triggers_limit` | Integer | The maximum number of times this passive effect can trigger per battle. | 2 | `1` |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `-1`<br>`-2`<br>`1` |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `1`<br>`2`<br>`4` |
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. || `1`<br>`2`<br>`[1 .01]` |

</details>


---


#### `StatusEachRoundEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DoDamage`](./Miscellaneous.md#object-dodamage) | Object  | Contains damage parameters (amount, type, tile targets) to deal damage to the target. || `{ . . . }` |
| [`UseAbility`](./Passives_and_Statuses.md#object-useability) | Enum / Object  | The name of the ability the target is forced to use. || `{ . . . }`<br>`GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |

</details>


---


#### `StatusEachTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 27

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MissChance` | Integer | The flat percentage chance that the unit's attacks will miss. | 24 | `10`<br>`15`<br>`20` |
| [`Quivered`](./Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 10 | `1`<br>`2`<br>`5` |
| `MoveQuivered` | Integer | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 6 | `1`<br>`2`<br>`[1, 0.1]` |
| [`Conditional_BadRoll`](./Passives_and_Statuses.md#object-conditional_badroll) | Object  | An object containing an `odds` value and effects that are applied when a random roll succeeds. | 5 | `{ . . . }` |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`Revive`](./Engine_StatusAndPassiveKeys.md#object-revive) | Integer / Object  | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 2 | `{ . . . }`<br>`1`<br>`100%`<br>`50%` |
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 1 | `{ . . . }` |
| [`Burn`](./Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` |
| `BlessingOfPeace` | Integer | The number of stacks of the Blessing of Peace status applied to the unit each turn. || `1` |
| `DoubleCastSpellThisTurn` | Integer | If non-zero, grants the unit a double cast effect for spells this turn. || `1` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`10`<br>`2` |
| `FillMana` | Integer | The amount of mana restored, or an [amount, probability] array. || `1`<br>`[1 .10]`<br>`[1 .25]` |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. || `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. || `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `-1`<br>`-2`<br>`-4` |
| [`UseAbility`](./Passives_and_Statuses.md#object-useability) | Enum / Object  | The name of the ability the target is forced to use. || `{ . . . }`<br>`GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |
| `Wet` | Integer | The number of stacks of the Wet status effect applied. || `1` |

</details>


---


#### `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 57

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 6 | `1`<br>`2`<br>`3` |
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 2 | `{ . . . }` |
| [`Cleanse`](./Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object  | The number of stacks of negative status effects removed from the target. | 2 | `{ . . . }`<br>`0`<br>`1` |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`Stealth`](./Arrays.md#array-stealth) | Array / Integer  | The number of stealth stacks applied. | 2 | `1`<br>`2`<br>`[1 .1]` |
| [`Conditional_BadRoll`](./Passives_and_Statuses.md#object-conditional_badroll) | Object  | An object containing an `odds` value and effects that are applied when a random roll succeeds. | 1 | `{ . . . }` |
| [`Conditional_HasCleansableDebuffs`](./Miscellaneous.md#object-conditional_hascleansabledebuffs) | Object  | An object containing effects that execute only if the unit has cleansable debuffs. | 1 | `{ . . . }` |
| [`Conditional_ManaThreshold`](./Miscellaneous.md#object-conditional_manathreshold) | Object  | Defines a conditional block that applies effects only if a unit's mana meets a specified threshold. | 1 | `{ . . . }` |
| [`Burn`](./Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` |
| `AddWeaponAux` | Integer / String | The amount or expression to add to the source's weapon auxiliary stat. || `"-max(min(X+1, item_aux), 0)"`<br>`-item_aux`<br>`1` |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `-1`<br>`-2`<br>`1` |
| `Charge` | Integer | The number of charge stacks applied. || `1`<br>`2`<br>`3` |
| [`ConstitutionUp`](./Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. || `-1`<br>`-2`<br>`1` |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `1`<br>`2`<br>`4` |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. || `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| `HealthGain` | Integer | The amount of health restored to the source. || `1`<br>`10`<br>`2` |
| [`ImmediateUseAbility`](./Miscellaneous.md#object-immediateuseability) | Enum / Object  | Specifies the name of an ability to be triggered instantly from this effect. || `{ . . . }`<br>`FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. || `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `NonStackingDivineShield` | Integer | The number of Divine Shield stacks that do not stack with duplicates. || `1` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. || `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| `PermanentMadness` | Integer | The number of permanent madness stacks applied. || `1` |
| `PreEmptiveCounterNextAttacks` | Integer | The number of next incoming attacks that the unit will counter preemptively before they land. || `1` |
| [`RandomStatDown`](./Arrays.md#array-randomstatdown) | Array / Integer / String  | The amount of random stat reduction applied, either as a fixed number, a formula string, or an array of [stacks, probability]. || `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`1` |
| `RangeUp` | Integer | The number of stacks of bonus attack range applied. || `1` |
| [`SpawnCoinAnywhere`](./Arrays.md#array-spawncoinanywhere) | Array / Integer  | The number of coins to spawn. If an array, the second value is the probability of spawning them anywhere. || `1`<br>`[1 .5]` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `-1`<br>`-2`<br>`-4` |
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. || `"max(int, 0)"`<br>`-1`<br>`-2` |

</details>


---


#### `StatusEachTurnEndForEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. || `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`RandomMagicMissile`](./Miscellaneous.md#object-randommagicmissile) | Integer / Object  | The number of random magic missiles fired, or an object defining its properties. || `{ . . . }`<br>`1`<br>`10`<br>`2` |

</details>


---


#### `StatusEveryXSpellCasts`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 8 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `-1`<br>`-2`<br>`1` |
| `Charge` | Integer | The number of charge stacks applied. || `1`<br>`2`<br>`3` |
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. || `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. || `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| [`RandomMagicMissile`](./Miscellaneous.md#object-randommagicmissile) | Integer / Object  | The number of random magic missiles fired, or an object defining its properties. || `{ . . . }`<br>`1`<br>`10`<br>`2` |
| `ReduceManaCost` | Integer | The number of stacks reducing mana cost of abilities. || `1`<br>`2` |
| [`RepairWeapon`](./Arrays.md#array-repairweapon) | Array / Integer  | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. || `1`<br>`6`<br>`99` |
| `RepairWeaponCondition` | Integer | The amount of weapon condition restored. || `1` |
| `SpellDamageUp` | Integer | The number of stacks of SpellDamageUp applied, increasing spell damage. || `1`<br>`3` |

</details>


---


#### `StatusGroup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DexterityUp` | Enum / Integer | The amount of dexterity change, or a keyword like 'item_aux'. || `-1`<br>`1`<br>`2` |
| [`FindItemFromPool`](./Passives_and_Statuses.md#object-finditemfrompool) | Enum / Object  | Specifies the loot pool from which to find an item, with an optional chance. || `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. || `1`<br>`2`<br>`[1 .01]` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. || `-1`<br>`-2`<br>`-4` |
| [`SpawnCoinAnywhere`](./Arrays.md#array-spawncoinanywhere) | Array / Integer  | The number of coins to spawn. If an array, the second value is the probability of spawning them anywhere. || `1`<br>`[1 .5]` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `-1`<br>`-2`<br>`-4` |

</details>


---


#### `StatusIfUnusedMovePoints`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`Brace`](./Passives_and_Statuses.md#object-brace) | Enum / Integer / Object  | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 20 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| `MoveQuivered` | Integer | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 6 | `1`<br>`2`<br>`[1, 0.1]` |
| `Charge` | Integer | The number of charge stacks applied. || `1`<br>`2`<br>`3` |
| [`ConstitutionUp`](./Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. || `-1`<br>`-2`<br>`1` |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `1`<br>`2`<br>`4` |
| `HealthGain` | Integer | The amount of health restored to the source. || `1`<br>`10`<br>`2` |
| `ManaGain` | Enum / Integer | The amount of mana restored to the source, which can be an expression. || `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |

</details>


---


#### `StatusKilledCharacters`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_RandomChance`](./Miscellaneous.md#object-conditional_randomchance) | Object  | An object containing effects that execute only if a random roll succeeds, with an odds value defined inside. | 2 | `{ . . . }` |
| [`Conditional_Ally`](./Passives_and_Statuses.md#object-conditional_ally) | Object  | Defines effects that apply only if the target is an ally, with an optional else block for non-allies. | 1 | `{ . . . }` |
| `AutoReanimate` | Number | The percentage chance for the unit to automatically reanimate upon death. || `100%`<br>`50%` |
| `AutoReanimate` | Number | The percentage chance for the unit to automatically reanimate upon death. | 0 | `100%`<br>`50%` |

</details>


---


#### `StatusKillers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Confusion`](./Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Confusion`](./Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Conditional_Boss`](./Passives_and_Statuses.md#object-conditional_boss) | Object  | Contains effects that apply only if the target is a boss enemy. | 2 | `{ . . . }` |
| [`Conditional_NotBoss`](./Passives_and_Statuses.md#object-conditional_notboss) | Object  | Contains effects that apply only if the target is not a boss enemy. | 2 | `{ . . . }` |

</details>


---


#### `StatusOnAllyCatDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `-1`<br>`-2`<br>`1` |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `1`<br>`2`<br>`4` |
| `FillMana` | Integer | The amount of mana restored, or an [amount, probability] array. || `1`<br>`[1 .10]`<br>`[1 .25]` |
| `HealthGain` | Integer | The amount of health restored to the source. || `1`<br>`10`<br>`2` |

</details>


---


#### `StatusOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 53

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `even_if_dead` | Boolean | If true, the effect triggers even if the unit is dead. | 25 | `true` |
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 6 | `{ . . . }` |
| [`Conditional_Corpse`](./Passives_and_Statuses.md#object-conditional_corpse) | Object  | Contains an inner effect block that only executes if the target is a corpse. | 1 | `{ . . . }` |
| [`Conditional_Shielded`](./Passives_and_Statuses.md#object-conditional_shielded) | Object  | An object containing effects that are only applied if the target has a shield active. | 1 | `{ . . . }` |
| [`FindItemFromPool`](./Passives_and_Statuses.md#object-finditemfrompool) | Enum / Object  | Specifies the loot pool from which to find an item, with an optional chance. || `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`GainCoins`](./Arrays.md#array-gaincoins) | Array / Integer  | The amount of coins gained, or a [min, max] range. || `-5`<br>`1`<br>`2` |
| `PermanentStrength` | Integer | The amount of permanent bonus strength (physical damage modifier) granted. || `1`<br>`2` |
| `RepairAll` | Integer | The amount of durability restored to all equipped items. || `1`<br>`10` |
| [`RepairWeapon`](./Arrays.md#array-repairweapon) | Array / Integer  | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. || `1`<br>`6`<br>`99` |
| [`TransformWeapon`](./Miscellaneous.md#object-transformweapon) | Object  | An object with `from` and `to` fields specifying the weapon transformation. || `{ . . . }` |

</details>


---


#### `StatusOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Brace`](./Passives_and_Statuses.md#object-brace) | Enum / Integer / Object  | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 20 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Craft`](./Passives_and_Statuses.md#object-craft) | Object  | Specifies the loot pool and slot to craft an item for the source. | 2 | `{ . . . }` |
| [`DestroyEquipmentAndAttachParasite`](./Miscellaneous.md#object-destroyequipmentandattachparasite) | Object  | Attempts to destroy a random piece of the target's equipment and attach a parasite from the specified pool. || `{ . . . }` |
| [`FindItemFromPool`](./Passives_and_Statuses.md#object-finditemfrompool) | Enum / Object  | Specifies the loot pool from which to find an item, with an optional chance. || `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. || `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. || `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| [`RandomMagicMissile`](./Miscellaneous.md#object-randommagicmissile) | Integer / Object  | The number of random magic missiles fired, or an object defining its properties. || `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`ReviveNextRound`](./Miscellaneous.md#object-revivenextround) | Integer / Object  | The number of revives granted, or an object defining revive properties. || `{ . . . }`<br>`2` |
| `SafeDie` | Integer | The number of times the unit can survive a fatal hit. || `1` |
| [`Sleep`](./Arrays.md#array-sleep) | Array / Integer  | The amount of sleep stacks applied, or an [stacks, probability] array. || `1`<br>`2`<br>`3` |
| `StealthUntilBasicAttack` | Integer | The number of stacks of Stealth that are removed when the unit performs a basic attack. || `1` |

</details>


---


#### `StatusOnBreak`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 22

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 | `1`<br>`2`<br>`3` |
| [`Bruise`](./Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`ApplyToRandomPartyMemberIfPossible`](./Miscellaneous.md#object-applytorandompartymemberifpossible) | Object  | Contains an inner effect block that is applied to a random living party member if one exists. || `{ . . . }` |
| [`ConstitutionUp`](./Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. || `-1`<br>`-2`<br>`1` |
| `DexterityUp` | Enum / Integer | The amount of dexterity change, or a keyword like 'item_aux'. || `-1`<br>`1`<br>`2` |
| [`FindItemFromPool`](./Passives_and_Statuses.md#object-finditemfrompool) | Enum / Object  | Specifies the loot pool from which to find an item, with an optional chance. || `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| `HealthGain` | Integer | The amount of health restored to the source. || `1`<br>`10`<br>`2` |
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. || `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. || `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. || `"max(int, 0)"`<br>`-1`<br>`-2` |

</details>


---


#### `StatusOnBreakItem`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 36 | `1`<br>`2`<br>`3` |
| [`DoDamage`](./Miscellaneous.md#object-dodamage) | Object  | Contains damage parameters (amount, type, tile targets) to deal damage to the target. || `{ . . . }` |

</details>


---


#### `StatusOnCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `Charge` | Integer | The number of charge stacks applied. || `1`<br>`2`<br>`3` |
| `HealthGain` | Integer | The amount of health restored to the source. || `1`<br>`10`<br>`2` |

</details>


---


#### `StatusOnCollectPickup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Tech` | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 2 | `1`<br>`3` |

</details>


---


#### `StatusOnDie`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_RandomChance`](./Miscellaneous.md#object-conditional_randomchance) | Object  | An object containing effects that execute only if a random roll succeeds, with an odds value defined inside. | 1 | `{ . . . }` |
| [`FindItemFromPool`](./Passives_and_Statuses.md#object-finditemfrompool) | Enum / Object  | Specifies the loot pool from which to find an item, with an optional chance. || `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`RandomMagicMissile`](./Miscellaneous.md#object-randommagicmissile) | Integer / Object  | The number of random magic missiles fired, or an object defining its properties. || `{ . . . }`<br>`1`<br>`10`<br>`2` |
| `RemoveAmbientLightEffects` | Number | The fade-out duration in seconds for ambient light effects. || `.5`<br>`4` |
| [`ScatterCoins`](./Miscellaneous.md#object-scattercoins) | Object  | The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula. || `{ . . . }` |

</details>


---


#### `StatusOnEatFood`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 | `1`<br>`2`<br>`3` |
| [`Cleanse`](./Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object  | The number of stacks of negative status effects removed from the target. | 2 | `{ . . . }`<br>`0`<br>`1` |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. || `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. || `"max(int, 0)"`<br>`-1`<br>`-2` |

</details>


---


#### `StatusOnEatPill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `-1`<br>`-2`<br>`1` |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 0 | `-1`<br>`-2`<br>`1` |
| [`RandomPermanentStatsDistinct`](./Miscellaneous.md#object-randompermanentstatsdistinct) | Object  | An object defining a set of stat changes (positive and negative) that are randomly applied as permanent modifications. | 0 | `{ . . . }` |

</details>


---


#### `StatusOnEndMove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_FirstApplicationThisTurn`](./Passives_and_Statuses.md#object-conditional_firstapplicationthisturn) | Object  | Container for effects applied only on the first application of this ability during the turn. | 1 | `{ . . . }` |
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 1 | `{ . . . }` |
| `Charge` | Integer | The number of charge stacks applied. || `1`<br>`2`<br>`3` |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `1`<br>`2`<br>`4` |
| [`ForceAttack`](./Miscellaneous.md#object-forceattack) | Integer / Object  | If set to 1, forces the target to perform an attack against a random or specified target. || `{ . . . }`<br>`1` |
| [`ImmediateUseAbility`](./Miscellaneous.md#object-immediateuseability) | Enum / Object  | Specifies the name of an ability to be triggered instantly from this effect. || `{ . . . }`<br>`FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `-1`<br>`-2`<br>`-4` |
| `SpeedUp_WithoutInitiative` | Integer | The number of stacks of Speed Up that do not affect the unit's initiative (turn order) stat. || `1` |
| [`RemoveStatusStacks`](./Miscellaneous.md#object-removestatusstacks) | Object  | An object specifying a status name and the number of stacks to remove from the target. | 0 | `{ . . . }` |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 0 | `1`<br>`2`<br>`4` |
| [`ImmediateUseAbility`](./Miscellaneous.md#object-immediateuseability) | Enum / Object  | Specifies the name of an ability to be triggered instantly from this effect. | 0 | `{ . . . }`<br>`FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |
| `Charge` | Integer | The number of charge stacks applied. | 0 | `1`<br>`2`<br>`3` |
| `SpeedUp_WithoutInitiative` | Integer | The number of stacks of Speed Up that do not affect the unit's initiative (turn order) stat. | 0 | `1` |
| [`ForceAttack`](./Miscellaneous.md#object-forceattack) | Integer / Object  | If set to 1, forces the target to perform an attack against a random or specified target. | 0 | `{ . . . }`<br>`1` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 0 | `-1`<br>`-2`<br>`-4` |

</details>


---


#### `StatusOnGainCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`BackflipWhenTargeted`](./Passives_and_Statuses.md#object-backflipwhentargeted) | Enum / Integer / Object  | The number of backflip charges, or an object defining its ability. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`X` |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `1`<br>`2`<br>`4` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. || `-1`<br>`-2`<br>`-4` |

</details>


---


#### `StatusOnHealed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 36 | `1`<br>`2`<br>`3` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. || `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |

</details>


---


#### `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 40

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 | `1`<br>`2`<br>`3` |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 4 | `{ . . . }` |
| [`Conditional_FirstApplicationThisTurn`](./Passives_and_Statuses.md#object-conditional_firstapplicationthisturn) | Object  | Container for effects applied only on the first application of this ability during the turn. | 2 | `{ . . . }` |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`Stealth`](./Arrays.md#array-stealth) | Array / Integer  | The number of stealth stacks applied. | 2 | `1`<br>`2`<br>`[1 .1]` |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `-1`<br>`-2`<br>`1` |
| `CharismaUp` | Enum / Integer | The amount of charisma change, or a keyword like 'item_aux'. || `-1`<br>`-2`<br>`1` |
| [`ConstitutionUp`](./Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. || `-1`<br>`-2`<br>`1` |
| `DexterityUp` | Enum / Integer | The amount of dexterity change, or a keyword like 'item_aux'. || `-1`<br>`1`<br>`2` |
| `HealthGain` | Integer | The amount of health restored to the source. || `1`<br>`10`<br>`2` |
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. || `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. || `-1`<br>`-2`<br>`-4` |
| `RangeUp` | Integer | The number of stacks of bonus attack range applied. || `1` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `-1`<br>`-2`<br>`-4` |
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. || `"max(int, 0)"`<br>`-1`<br>`-2` |
| `BrittleCharismaUp` | Integer | The number of stacks of temporary Charisma gained on kill. | 0 | `2` |
| `BrittleConstitutionUp` | Integer | The number of stacks of temporary Constitution gained on kill. | 0 | `2` |
| `BrittleDexterityUp` | Integer | The number of stacks of temporary Dexterity gained on kill. | 0 | `2` |
| `BrittleIntelligenceUp` | Integer | The number of stacks of temporary Intelligence gained on kill. | 0 | `2` |
| `BrittleLuckUp` | Integer | The number of stacks of temporary Luck gained on kill. | 0 | `2` |
| `BrittleSpeedUp` | Integer | The number of stacks of temporary Speed gained on kill. | 0 | `2` |
| `BrittleStrengthUp` | Integer | The number of stacks of temporary Strength gained on kill. | 0 | `2` |
| [`UseAbility_NonStack`](./Enums.md#enum-useability_nonstack) | Enum | Specifies an ability to use on kill that does not stack with itself. | 0 | `BBTransformZealot`<br>`GenericRage` |

</details>


---


#### `StatusOnKillEnemy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Brace`](./Passives_and_Statuses.md#object-brace) | Enum / Integer / Object  | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 20 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `1`<br>`2`<br>`4` |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. || `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| `HealthGain` | Integer | The amount of health restored to the source. || `1`<br>`10`<br>`2` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. || `-1`<br>`-2`<br>`-4` |
| `ManaGain` | Enum / Integer | The amount of mana restored to the source, which can be an expression. || `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |

</details>


---


#### `StatusOnPickupCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DexterityUp` | Enum / Integer | The amount of dexterity change, or a keyword like 'item_aux'. || `-1`<br>`1`<br>`2` |
| [`GainCoins`](./Arrays.md#array-gaincoins) | Array / Integer  | The amount of coins gained, or a [min, max] range. || `-5`<br>`1`<br>`2` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `-1`<br>`-2`<br>`-4` |

</details>


---


#### `StatusOnPopCorpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthGain` | Integer | The amount of health restored to the source. || `1`<br>`10`<br>`2` |
| [`RepairWeapon`](./Arrays.md#array-repairweapon) | Array / Integer  | The number of weapon durability points restored; an array [stacks, probability] applies a chance-based repair. || `1`<br>`6`<br>`99` |

</details>


---


#### `StatusOnTookDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 46

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 36 | `1`<br>`2`<br>`3` |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `1`<br>`10`<br>`2` |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`Conditional_HasStatus`](./Passives_and_Statuses.md#object-conditional_hasstatus) | Object  | Contains an inner effect block that only executes if the target has the specified status effect. | 2 | `{ . . . }` |
| [`Craft`](./Passives_and_Statuses.md#object-craft) | Object  | Specifies the loot pool and slot to craft an item for the source. | 2 | `{ . . . }` |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 2 | `1`<br>`10`<br>`100` |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`Conditional_HealthThreshold`](./Miscellaneous.md#object-conditional_healththreshold) | Object  | Contains an inner effect block that only executes if the target's health is below a threshold, defined by `threshold_flat`, `threshold_percent`, or `threshold_expr`. | 1 | `{ . . . }` |
| [`Else`](./Passives_and_Statuses.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ . . . }` |
| `Charge` | Integer | The number of charge stacks applied. || `1`<br>`2`<br>`3` |
| [`ConstitutionUp`](./Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. || `-1`<br>`-2`<br>`1` |
| `DiminishingHealthRegen` | Integer | The number of diminishing health regen stacks applied. || `1`<br>`2`<br>`3` |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `1`<br>`2`<br>`4` |
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. || `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. || `-1`<br>`-2`<br>`-4` |
| `MovementUp` | Integer | The amount of movement increase or decrease applied. || `-2`<br>`1`<br>`2` |
| `RandomInjury` | Integer | The number of random injuries applied. || `1` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `-1`<br>`-2`<br>`-4` |
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. || `"max(int, 0)"`<br>`-1`<br>`-2` |
| `TempDamageUp` | Integer | The amount of temporary damage increase applied. || `-1`<br>`1`<br>`2` |
| `TempMovement` | Enum / Integer | The amount of temporary movement range added, or a string alias like 'mov'. || `1`<br>`20`<br>`mov` |

</details>


---


#### `StatusOnTookDamageFromAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 422 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 | `1`<br>`2`<br>`3` |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `1`<br>`10`<br>`2` |
| `DiminishingHealthRegen` | Integer | The number of diminishing health regen stacks applied. || `1`<br>`2`<br>`3` |
| `ExtraBasicAttacks_Status` | Integer | The number of additional basic attacks the unit can perform each turn. || `1` |

</details>


---


#### `StatusOnUseBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `HealthGain` | Integer | The amount of health restored to the source. || `1`<br>`10`<br>`2` |

</details>


---


#### `StatusRandomEnemiesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `1`<br>`10`<br>`2` |
| [`Confusion`](./Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`count`](./Arrays.md#array-count) | Array / Integer | The number of units to spawn or enrage, as a fixed number or a range [min max]. | 3 | `0`<br>`1`<br>`10` |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. || `1`<br>`2`<br>`3` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`10`<br>`2` |
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. || `1`<br>`2`<br>`[1 .01]` |

</details>


---


#### `StatusWhenAllySpendsMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Charge` | Integer | The number of charge stacks applied. || `1`<br>`2`<br>`3` |
| `ManaGain` | Enum / Integer | The amount of mana restored to the source, which can be an expression. || `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`OneUseSpellDamageUp`](./Engine_StatusAndPassiveKeys.md#object-oneusespelldamageup) | Array / Number / Object  | Increases spell damage by the specified amount, but the effect is consumed after a single use. Alias for SpellDamageUp. || `{ . . . }`<br>`2` |

</details>


---


#### `TakeBonusTurnWithAIControl`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `include_spells` | Boolean | If true, the AI-controlled bonus turn includes spells as available actions. | 3 | `true` |
| `end_of_round` | Boolean | If true, the effect triggers at the end of the round instead of at the start of the turn. | 1 | `true` |

</details>


---


#### `TakeBonusTurnWithStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Confusion`](./Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Madness`](./Passives_and_Statuses.md#object-madness) | Array / Enum / Integer / Object  | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. || `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`2`<br>`3` |

</details>


---


#### `TempPassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 | `1`<br>`2`<br>`3` |
| [`status`](./Enums.md#enum-status) | Enum | Specifies the status effect to apply in a Temporary object. | 3 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |

</details>


---


#### `additional_passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 6 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `-1`<br>`-2`<br>`1` |
| `FillMana` | Integer | The amount of mana restored, or an [amount, probability] array. || `1`<br>`[1 .10]`<br>`[1 .25]` |
| `HealthGain` | Integer | The amount of health restored to the source. || `1`<br>`10`<br>`2` |
| `PermanentMadness` | Integer | The number of permanent madness stacks applied. || `1` |
| [`ReviveNextRound`](./Miscellaneous.md#object-revivenextround) | Integer / Object  | The number of revives granted, or an object defining revive properties. || `{ . . . }`<br>`2` |
| [`SafeDoomed`](./Enums.md#enum-safedoomed) | Enum / Integer  | The number of SafeDoomed stacks applied, or 'level' to scale with character level. || `1`<br>`2`<br>`level` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `-1`<br>`-2`<br>`-4` |

</details>


---


#### `bonus_passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 138

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 36 | `1`<br>`10`<br>`100` |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 | `1`<br>`2`<br>`3` |
| `Trample` | Integer | The amount of bonus damage dealt when moving through an enemy. | 14 | `1`<br>`3`<br>`4` |
| [`AutocastEachRound`](./Passives_and_Statuses.md#object-autocasteachround) | Enum / Object  | Contains an ability name and optional 'even_if_stunned' flag to autocast each round. | 4 | `{ . . . }`<br>`SpiderReturn` |
| `AlphaDodgeChance` | Integer | The dodge chance granted to the alpha (leader) unit. || `50%` |
| `DownRankAIIfWeaponUsable` | Number | A multiplier that reduces the AI's priority to use this ability if the unit has a usable weapon. || `.001` |
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. || `"min(-int, 0)"`<br>`-1`<br>`-2` |
| [`XIsSpellStormRampAndReset`](./Miscellaneous.md#object-xisspellstormrampandreset) | Integer / Object  | If integer 0, resets stacks; if object, contains 'stacks' and 'reset_percent' for spell storm ramp. || `{ . . . }`<br>`0` |

</details>


---


#### `extra_statuses`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Poison`](./Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 | `1`<br>`10`<br>`2` |
| [`Conditional_HasTag`](./Passives_and_Statuses.md#object-conditional_hastag) | Object  | Evaluates whether the target has a specific tag; if true, applies the effects within; otherwise, runs the Else block. | 1 | `{ . . . }` |
| [`Burn`](./Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `-1`<br>`-2`<br>`1` |
| `HealthGain` | Integer | The amount of health restored to the source. || `1`<br>`10`<br>`2` |
| [`Tarred`](./Arrays.md#array-tarred) | Array / Integer  | The amount of tarred stacks applied, or an [stacks, probability] array. || `1`<br>`2`<br>`[1 .1]` |

</details>


---


#### `party_status_next_fight`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 24

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 | `1`<br>`2`<br>`3` |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `1`<br>`10`<br>`2` |
| [`Poison`](./Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 | `1`<br>`10`<br>`2` |
| [`Immobile`](./Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 4 | `0`<br>`1`<br>`10%` |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `1`<br>`2`<br>`4` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`10`<br>`2` |
| [`NoHealthRegen`](./Engine_StatusAndPassiveKeys.md#object-nohealthregen) | Array / Number / Object  | Prevents the unit from regenerating health normally. || `{ . . . }`<br>`1` |
| [`Tangled`](./Miscellaneous.md#object-tangled) | Array / Integer / Object  | The number of stacks of the Tangled status effect applied, or an object defining its properties such as `stacks` and `alt_art`. || `{ . . . }`<br>`1`<br>`2`<br>`[1, .05]` |
| [`Tarred`](./Arrays.md#array-tarred) | Array / Integer  | The amount of tarred stacks applied, or an [stacks, probability] array. || `1`<br>`2`<br>`[1 .1]` |
| `Webbed` | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. || `1`<br>`2`<br>`[1 .1]` |

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
| `HealthRegenUp` | Integer | The amount of bonus health regeneration granted to a unit per turn, additive with existing regeneration. | 26 | `1`<br>`2`<br>`3` |
| `MissChance` | Integer | The flat percentage chance that the unit's attacks will miss. | 24 | `10`<br>`15`<br>`20` |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 9 | `1`<br>`10`<br>`2` |
| [`Bruise`](./Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 8 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Poison`](./Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 8 | `1`<br>`10`<br>`2` |
| [`Blind`](./Arrays.md#array-blind) | Array / Integer  | The amount of blind stacks applied, or an [stacks, probability] array. | 6 | `-1`<br>`1`<br>`2` |
| [`Confusion`](./Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 6 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Slow`](./Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 | `{ . . . }`<br>`-1`<br>`1`<br>`2` |
| [`Burn`](./Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 1 | `1`<br>`10`<br>`2` |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `-1`<br>`-2`<br>`1` |
| `CharismaUp` | Enum / Integer | The amount of charisma change, or a keyword like 'item_aux'. || `-1`<br>`-2`<br>`1` |
| [`ConstitutionUp`](./Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. || `-1`<br>`-2`<br>`1` |
| `DexterityUp` | Enum / Integer | The amount of dexterity change, or a keyword like 'item_aux'. || `-1`<br>`1`<br>`2` |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. || `1`<br>`2`<br>`4` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`10`<br>`2` |
| `IntelligenceUp` | Enum / Integer | The amount of Intelligence added as a flat bonus. || `"min(-int, 0)"`<br>`-1`<br>`-2` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. || `-1`<br>`-2`<br>`-4` |
| [`Madness`](./Passives_and_Statuses.md#object-madness) | Array / Enum / Integer / Object  | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. || `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`NoHealthRegen`](./Engine_StatusAndPassiveKeys.md#object-nohealthregen) | Array / Number / Object  | Prevents the unit from regenerating health normally. || `{ . . . }`<br>`1` |
| [`NoManaRegen`](./Passives_and_Statuses.md#object-nomanaregen) | Array / Number / Object  | The unit does not naturally regenerate mana per turn. Value indicates the stage or flag enabling this restriction. || `{ . . . }`<br>`1` |
| [`PermanentConfusion`](./Engine_StatusAndPassiveKeys.md#object-permanentconfusion) | Array / Number / Object  | If set to 1, the unit is permanently confused and cannot be cured. || `{ . . . }`<br>`1` |
| `ProbeCharmed` | Integer | The number of charm stacks applied by a probe. || `1` |
| [`Rot`](./Arrays.md#array-rot) | Array / Integer  | Integer, or an array [stacks, probability] specifying the amount of Rot stacks applied with the given probability. || `-999999`<br>`1`<br>`2` |
| [`Sleep`](./Arrays.md#array-sleep) | Array / Integer  | The amount of sleep stacks applied, or an [stacks, probability] array. || `1`<br>`2`<br>`3` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. || `-1`<br>`-2`<br>`-4` |
| `SpiderInfested` | Integer | The number of spider infestation stacks applied. || `1`<br>`2`<br>`4` |
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. || `"max(int, 0)"`<br>`-1`<br>`-2` |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`2`<br>`3` |
| [`Tarred`](./Arrays.md#array-tarred) | Array / Integer  | The amount of tarred stacks applied, or an [stacks, probability] array. || `1`<br>`2`<br>`[1 .1]` |
| `TempStrengthUp` | Enum | The number of stacks of temporary Strength Up applied to the unit. || `1`<br>`2`<br>`X` |
| `Webbed` | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. || `1`<br>`2`<br>`[1 .1]` |

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
| [`alias`](./Enums.md#enum-alias) | Enum  | Specifies the reference name of another status effect to alias or copy properties from. || `AllStatsUp`<br>`Brace`<br>`Brittle` |


### Object: `AlphaStatusOnTurnBegin`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DoubleCastSpellThisTurn` | Integer | If non-zero, grants the unit a double cast effect for spells this turn. | 2 | `1` |


### Object: `ApplyPassivesToSpawnerWhileAlive`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`HideEquipment`](./Enums.md#enum-hideequipment) | Enum  | Specifies which equipment slot is visually hidden. | 2 | `neck` |


### Object: `ApplyToRandomPartyMemberIfPossible`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`GainDisorderFromPool`](./Miscellaneous.md#object-gaindisorderfrompool) | Enum / Object  | Specifies a pool of disorders from which one is randomly gained on basic attack, with an optional chance. | 4 | `{ . . . }`<br>`all_disorders` |


### Object: `ApplyToSource`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 12 | `-1`<br>`-2`<br>`1` |
| `HealthGain` | Integer | The amount of health restored to the source. | 12 | `1`<br>`10`<br>`2` |
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. | 12 | `"max(int, 0)"`<br>`-1`<br>`-2` |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 10 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`EvolveAbilityFromPool`](./Miscellaneous.md#object-evolveabilityfrompool) | Enum / Object  | Specifies the ability pool from which to evolve an ability for the source, optionally upgrading it. | 8 | `{ . . . }`<br>`Butcher`<br>`Druid`<br>`Fighter` |
| [`FormChange`](./Miscellaneous.md#object-formchange) | Enum / Object  | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 8 | `{ . . . }`<br>`Big`<br>`BigHolding`<br>`BigHoldingCat` |
| `AddWeaponAux` | Integer / String | The amount or expression to add to the source's weapon auxiliary stat. | 6 | `"-max(min(X+1, item_aux), 0)"`<br>`-item_aux`<br>`1` |
| [`ConstitutionUp`](./Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 6 | `-1`<br>`-2`<br>`1` |
| `Charge` | Integer | The number of charge stacks applied. | 4 | `1`<br>`2`<br>`3` |
| [`Cleanse`](./Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object  | The number of stacks of negative status effects removed from the target. | 4 | `{ . . . }`<br>`0`<br>`1` |
| [`EquipPermanentItem`](./Enums.md#enum-equippermanentitem) | Enum  | The name of the item to permanently equip to the source. | 4 | `BoneClub`<br>`Kidney` |
| [`FindItemFromPool`](./Passives_and_Statuses.md#object-finditemfrompool) | Enum / Object  | Specifies the loot pool from which to find an item, with an optional chance. | 4 | `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| `FreeSpell` | Integer | The number of stacks of Free Spell applied to the source, allowing the next spells to be cast without mana cost. | 4 | `1`<br>`2` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 4 | `-1`<br>`-2`<br>`-4` |
| [`Brace`](./Passives_and_Statuses.md#object-brace) | Enum / Integer / Object  | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 2 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Bruise`](./Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 2 | `1`<br>`2`<br>`4` |
| [`FindItem`](./Enums.md#enum-finditem) | Enum  | The name of the specific item to find and add to the source's inventory. | 2 | `BoneClub`<br>`Molars`<br>`Pearl` |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 2 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| [`GainCoinsRange`](./Miscellaneous.md#object-gaincoinsrange) | Object  | An object with `min` and `max` fields specifying a range for the amount of coins gained. | 2 | `{ . . . }` |
| `KineticSpikes` | Integer | The number of stacks of Kinetic Spikes applied, dealing damage back to attackers. | 2 | `1`<br>`2`<br>`3` |
| `ManaGain` | Enum / Integer | The amount of mana restored to the source, which can be an expression. | 2 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `MoveQuivered` | Integer | The number of stacks of bonus movement points applied to the source. Can be an array [stacks, probability]. | 2 | `1`<br>`2`<br>`[1, 0.1]` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | `-1`<br>`-2`<br>`-4` |
| `Tech` | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 2 | `1`<br>`3` |


### Object: `BlessingOfPeace`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |


### Object: `BounceObject`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`obj`](./Arrays.md#array-obj) | Array / Enum  | Specifies one or more object names to bounce towards the target. | 6 | `BeefyCharmedLeech`<br>`Dice`<br>`Maggot` |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 4 | `.02`<br>`.1`<br>`.15` |
| `slide` | Integer | The number of tiles the bounced object slides toward the target. | 2 | `10` |


### Object: `Bounty`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `ChangeTile`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tile`](./Arrays.md#array-tile) | Array / Enum  | Specifies the tile type(s) to change to, either a single tile string or an array of tiles. | 22 | `BrambleTile`<br>`CreepTile`<br>`DirtTile` |
| `aoe` | Integer | The radius (in tiles) of the area affected by the tile change. | 4 | `1` |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 4 | `.02`<br>`.1`<br>`.15` |


### Object: `CharismaUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `name_stacks_neg` | String | Localization key for the name of the negative variant (e.g., stat down) of this status effect. || `"KEYWORD_ALLSTATSDOWN_NAME"`<br>`"KEYWORD_CHADOWN_NAME"`<br>`"KEYWORD_CONDOWN_NAME"` |
| [`tooltip_stackless`](./Enums.md#enum-tooltip_stackless) | Enum   | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks_neg` | String | Localization key for the tooltip description of the negative variant (e.g., stat down) of this status effect. || `"KEYWORD_ALLSTATSDOWN_DESC"`<br>`"KEYWORD_CHADOWN_DESC"`<br>`"KEYWORD_CONDOWN_DESC"` |
| `tooltip_stacks_pos` | String | Localization key for the tooltip description of the positive variant (e.g., stat up) of this status effect. || `"KEYWORD_ALLSTATSUP_DESC"`<br>`"KEYWORD_CHAUP_DESC"`<br>`"KEYWORD_CONUP_DESC"` |


### Object: `Charmed`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |


### Object: `Cleanse`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |


### Object: `Cleave`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | `.02`<br>`.1`<br>`.15` |
| `icon_frame` | Number | The sprite frame index for the buff icon. || `141`<br>`148`<br>`149` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `Conditional_Adjacent`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer  | The amount of bleed stacks applied, or an [stacks, probability] array. | 4 | `1`<br>`10`<br>`2` |
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 4 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | | `{ . . . }` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | `Default`<br>`FormChange`<br>`Druid` |


### Object: `Conditional_Ally`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 10 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 6 | `-1`<br>`-2`<br>`1` |
| [`Cleanse`](./Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object  | The number of stacks of negative status effects removed from the target. | 6 | `{ . . . }`<br>`0`<br>`1` |
| `HealthGain` | Integer | The amount of health restored to the source. | 4 | `1`<br>`10`<br>`2` |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 4 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 4 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `TempSpeedUp` | Enum / Integer | The number of stacks of temporary Speed Up applied to the unit. | 4 | `10`<br>`4`<br>`X` |
| `BleedThorns` | Integer | The amount of bleed thorns damage dealt to attackers on hit. | 2 | `1`<br>`2`<br>`3` |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 2 | `1`<br>`2`<br>`3` |
| `ManaGain` | Enum / Integer | The amount of mana restored to the source, which can be an expression. | 2 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | `-1`<br>`-2`<br>`-4` |
| `TempDamageUp` | Integer | The amount of temporary damage increase applied. | 2 | `-1`<br>`1`<br>`2` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 2 | `1`<br>`2`<br>`3` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | | `{ . . . }` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | `Default`<br>`FormChange`<br>`Druid` |


### Object: `Conditional_BadRoll`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Number | The probability of the effect occurring, expressed as a decimal or percentage. | 16 | `.1`<br>`.16666666`<br>`.3` |
| `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 2 | `25`<br>`50`<br>`999` |
| [`Madness`](./Passives_and_Statuses.md#object-madness) | Array / Enum / Integer / Object  | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | | `{ . . . }` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | `Default`<br>`FormChange`<br>`Druid` |


### Object: `Conditional_Boss`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 6 | `1`<br>`2`<br>`3` |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 4 | `-1`<br>`-2`<br>`1` |
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 4 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 4 | `1`<br>`2`<br>`3` |
| `Drowsy` | Integer | The amount of drowsy stacks applied, or an [stacks, probability] array. | 4 | `1`<br>`8` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`10`<br>`2` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | | `{ . . . }` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | `Default`<br>`FormChange`<br>`Druid` |


### Object: `Conditional_Corpse`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Revive`](./Engine_StatusAndPassiveKeys.md#object-revive) | Integer / Object  | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 13 | `{ . . . }`<br>`1`<br>`100%`<br>`50%` |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 4 | `-1`<br>`-2`<br>`1` |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 4 | `1`<br>`2`<br>`3` |
| [`SafeDoomed`](./Enums.md#enum-safedoomed) | Enum / Integer  | The number of SafeDoomed stacks applied, or 'level' to scale with character level. | 4 | `1`<br>`2`<br>`level` |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `HealRandomInjury` | Integer | The number of random injuries healed on the target. | 2 | `1` |
| `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. | 2 | `1` |
| `RandomMutation` | Integer | The number of random mutations to apply. | 2 | `1`<br>`3` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | `-1`<br>`-2`<br>`-4` |
| [`Madness`](./Passives_and_Statuses.md#object-madness) | Array / Enum / Integer / Object  | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 1 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | | `{ . . . }` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | `Default`<br>`FormChange`<br>`Druid` |


### Object: `Conditional_Enemy`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Confusion`](./Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 16 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 4 | `-1`<br>`-2`<br>`1` |
| `Attraction` | Integer | The number of stacks of Attraction applied, drawing enemy units toward the target. | 4 | `1` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 4 | `1`<br>`10`<br>`2` |
| [`Madness`](./Passives_and_Statuses.md#object-madness) | Array / Enum / Integer / Object  | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. | 4 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Weakness`](./Passives_and_Statuses.md#object-weakness) | Array / Integer / Object  | The amount of Weakness applied, either as a fixed number or an array of [stacks, probability]. | 4 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 2 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [`Burn`](./Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 2 | `1`<br>`10`<br>`2` |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 2 | `1`<br>`2`<br>`3` |
| `Doomed` | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. | 2 | `1`<br>`2`<br>`3` |
| `Hex` | Integer | The number of stacks of Hex applied, causing the target to take increased damage from spells. | 2 | `1` |
| [`Leeches`](./Engine_StatusAndPassiveKeys.md#object-leeches) | Integer / Object  | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Marked`](./Engine_StatusAndPassiveKeys.md#object-marked) | Array / Integer / Object  | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 2 | `{ . . . }`<br>`1`<br>`3`<br>`5` |
| `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. | 2 | `1` |
| [`Poison`](./Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`10`<br>`2` |
| `TempDamageUp` | Integer | The amount of temporary damage increase applied. | 2 | `-1`<br>`1`<br>`2` |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`2`<br>`3` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | | `{ . . . }` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | `Default`<br>`FormChange`<br>`Druid` |


### Object: `Conditional_FirstApplicationThisTurn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |
| `Charge` | Integer | The number of charge stacks applied. | 2 | `1`<br>`2`<br>`3` |
| `FillMana` | Integer | The amount of mana restored, or an [amount, probability] array. | 2 | `1`<br>`[1 .10]`<br>`[1 .25]` |
| `ManaGain` | Enum / Integer | The amount of mana restored to the source, which can be an expression. | 2 | `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | | `{ . . . }` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | `Default`<br>`FormChange`<br>`Druid` |


### Object: `Conditional_GoodRoll`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Number | The probability of the effect occurring, expressed as a decimal or percentage. | 72 | `.1`<br>`.16666666`<br>`.3` |
| [`Freeze`](./Arrays.md#array-freeze) | Array / Integer  | The amount of freeze stacks applied, or an [stacks, probability] array. | 12 | `1`<br>`2`<br>`[1 .01]` |
| [`FindItemFromPool`](./Passives_and_Statuses.md#object-finditemfrompool) | Enum / Object  | Specifies the loot pool from which to find an item, with an optional chance. | 10 | `{ . . . }`<br>`blackbird_pool`<br>`chapter`<br>`chapter_common` |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 6 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |
| `RandomMutation` | Integer | The number of random mutations to apply. | 6 | `1`<br>`3` |
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum  | The tile type to change the ground tiles under the target to. | 2 | `DirtTile`<br>`GlassTile`<br>`LavaTile` |
| [`ImmediateUseAbility`](./Miscellaneous.md#object-immediateuseability) | Enum / Object  | Specifies the name of an ability to be triggered instantly from this effect. | 2 | `{ . . . }`<br>`FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | | `{ . . . }` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | `Default`<br>`FormChange`<br>`Druid` |


### Object: `Conditional_HasCleansableDebuffs`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GenericBuff` | Integer | A generic buff value applied to the unit. | 2 | `100`<br>`5` |
| `PartialCleanse` | Integer | The number of stacks of temporary status effects to remove from the target. | 2 | `1`<br>`9999` |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 2 | `{ . . . }` |
| [`VisualFX`](./Enums.md#enum-visualfx) | Enum  | Specifies the name of the visual effect to play. | 2 | `BigMagicMissileBlast`<br>`Bolt`<br>`Cleanse` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | | `{ . . . }` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | `Default`<br>`FormChange`<br>`Druid` |


### Object: `Conditional_HasStatus`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 12 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [`Burn`](./Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 4 | `1`<br>`10`<br>`2` |
| [`Confusion`](./Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 4 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`Slow`](./Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 4 | `{ . . . }`<br>`-1`<br>`1`<br>`2` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`10`<br>`2` |
| [`FormChange`](./Miscellaneous.md#object-formchange) | Enum / Object  | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 2 | `{ . . . }`<br>`Big`<br>`BigHolding`<br>`BigHoldingCat` |
| [`Quivered`](./Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`2`<br>`5` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | | `{ . . . }` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | `Default`<br>`FormChange`<br>`Druid` |


### Object: `Conditional_HasTag`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ImmediateUseAbility`](./Miscellaneous.md#object-immediateuseability) | Enum / Object  | Specifies the name of an ability to be triggered instantly from this effect. | 6 | `{ . . . }`<br>`FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum  | The tile type to change the ground tiles under the target to. | 4 | `DirtTile`<br>`GlassTile`<br>`LavaTile` |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 4 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| [`Die`](./Miscellaneous.md#object-die) | Integer / Object  | If set, kills the target immediately. | 4 | `{ . . . }`<br>`1`<br>`6` |
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 2 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 2 | `1`<br>`2`<br>`3` |
| `EventBounty` | Integer | The number of stacks of Event Bounty applied, increasing event rewards. | 2 | `5` |
| `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 2 | `25`<br>`50`<br>`999` |
| [`PopAndSpawn`](./Miscellaneous.md#object-popandspawn) | Enum / Object  | The object (enemy or entity) to spawn on the target's tile, optionally with visual effects. | 2 | `{ . . . }`<br>`Sprout`<br>`StemCat_HalfHealth`<br>`TheDestroyer` |
| [`UseAbility`](./Passives_and_Statuses.md#object-useability) | Enum / Object  | The name of the ability the target is forced to use. | 2 | `{ . . . }`<br>`GirlDinoPoop`<br>`KirbySpit`<br>`MD_PoopChain` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | | `{ . . . }` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | `Default`<br>`FormChange`<br>`Druid` |


### Object: `Conditional_HealthThreshold`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 2 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [`Die`](./Miscellaneous.md#object-die) | Integer / Object  | If set, kills the target immediately. | 2 | `{ . . . }`<br>`1`<br>`6` |
| `FlatLeech` | Integer | The flat amount of health restored to the source when dealing damage, applied after the hit. | 2 | `1`<br>`10`<br>`2` |
| `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 2 | `25`<br>`50`<br>`999` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | | `{ . . . }` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | `Default`<br>`FormChange`<br>`Druid` |


### Object: `Conditional_ManaThreshold`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RepairTrinket` | Integer | The number of stacks of the Repair Trinket status effect to apply. | 2 | `1`<br>`99` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | | `{ . . . }` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | `Default`<br>`FormChange`<br>`Druid` |


### Object: `Conditional_NotBoss`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Doomed` | Integer | The number of stacks of Doomed applied, causing the target to die after a set number of turns. | 4 | `1`<br>`2`<br>`3` |
| `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. | 2 | `1` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`10`<br>`2` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | | `{ . . . }` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | `Default`<br>`FormChange`<br>`Druid` |


### Object: `Conditional_PartyMember`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 4 | `1`<br>`2`<br>`3` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | | `{ . . . }` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | `Default`<br>`FormChange`<br>`Druid` |


### Object: `Conditional_Shielded`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cleave`](./Miscellaneous.md#object-cleave) | Integer / Object  | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. | 4 | `{ . . . }`<br>`1` |
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 2 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [`SetItemAux`](./Miscellaneous.md#object-setitemaux) | Object  | Configures an item's auxiliary value by specifying a target slot and a formula for the new value. | 2 | `{ . . . }` |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`2`<br>`3` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | | `{ . . . }` |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Inherits core engine logic parameters. You can utilize any key from the Engine Logic Keys list here to handle special conditions, state tracking, or math formulas. | | `Default`<br>`FormChange`<br>`Druid` |


### Object: `ConstitutionUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `name_stacks_neg` | String | Localization key for the name of the negative variant (e.g., stat down) of this status effect. || `"KEYWORD_ALLSTATSDOWN_NAME"`<br>`"KEYWORD_CHADOWN_NAME"`<br>`"KEYWORD_CONDOWN_NAME"` |
| [`tooltip_stackless`](./Enums.md#enum-tooltip_stackless) | Enum   | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks_neg` | String | Localization key for the tooltip description of the negative variant (e.g., stat down) of this status effect. || `"KEYWORD_ALLSTATSDOWN_DESC"`<br>`"KEYWORD_CHADOWN_DESC"`<br>`"KEYWORD_CONDOWN_DESC"` |
| `tooltip_stacks_pos` | String | Localization key for the tooltip description of the positive variant (e.g., stat up) of this status effect. || `"KEYWORD_ALLSTATSUP_DESC"`<br>`"KEYWORD_CHAUP_DESC"`<br>`"KEYWORD_CONUP_DESC"` |


### Object: `Craft`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 30 | `2`<br>`3`<br>`4` |
| [`slot`](./Enums.md#enum-slot) | Enum / Integer  | Specifies the equipment slot (e.g., 'head', 'trinket', 'random_empty') where the crafted item is placed. | 28 | `0`<br>`1`<br>`2` |
| `temporary` | Boolean | If true, the crafted item is temporary and will be removed after the battle or a set duration. | 8 | `false` |
| `works_with_tech` | Boolean | If true, the craft effect is compatible with tech-based interactions or abilities. | 8 | `true` |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |


### Object: `CureDisease`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 12 | `.02`<br>`.1`<br>`.15` |
| [`disease`](./Enums.md#enum-disease) | Enum  | Determines which disease is applied when spreading disease. | 12 | `BirdFlu`<br>`Cancer`<br>`CommonCold` |
| `can_apply_to_anything` | Boolean | If true, this disease can be spread to any unit, regardless of type. | 2 | `true` |


### Object: `DelayedPain`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `DestroyEquipmentAndAttachParasite`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 8 | `.02`<br>`.1`<br>`.15` |
| [`pool`](./Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 4 | `2`<br>`3`<br>`4` |


### Object: `DexterityUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `name_stacks_neg` | String | Localization key for the name of the negative variant (e.g., stat down) of this status effect. || `"KEYWORD_ALLSTATSDOWN_NAME"`<br>`"KEYWORD_CHADOWN_NAME"`<br>`"KEYWORD_CONDOWN_NAME"` |
| [`tooltip_stackless`](./Enums.md#enum-tooltip_stackless) | Enum   | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks_neg` | String | Localization key for the tooltip description of the negative variant (e.g., stat down) of this status effect. || `"KEYWORD_ALLSTATSDOWN_DESC"`<br>`"KEYWORD_CHADOWN_DESC"`<br>`"KEYWORD_CONDOWN_DESC"` |
| `tooltip_stacks_pos` | String | Localization key for the tooltip description of the positive variant (e.g., stat up) of this status effect. || `"KEYWORD_ALLSTATSUP_DESC"`<br>`"KEYWORD_CHAUP_DESC"`<br>`"KEYWORD_CONUP_DESC"` |


### Object: `DiminishingHealthRegen`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `DistanceBonusDamage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `min_range` | Integer | The minimum range of the ability. | 8 | `0`<br>`1`<br>`2` |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 8 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |


### Object: `DoDamage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Equation | Specifies the amount of damage dealt, can be a number or expression. | 14 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`type`](./Enums.md#enum-type) | Enum  | Specifies the damage type classification (e.g., melee, spell_cost, enter) used for interactions with mods, statuses, and passives. | 14 | `[attack move spell]`<br>`attack`<br>`battle` |
| [`damage_tiles`](./Enums.md#enum-damage_tiles) | Enum   | Specifies whether the damage effect applies to tiles; 'all' damages every tile in the area. | 8 | `all` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 8 | `{ . . . }` |
| [`elements`](./Arrays.md#array-elements) | Array  | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. || `[`<br>`[Heat Fire]` |


### Object: `DoubleCastSpellThisTurn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `Drowsy`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `Else`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 12 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |
| [`Cleanse`](./Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object  | The number of stacks of negative status effects removed from the target. | 4 | `{ . . . }`<br>`0`<br>`1` |
| [`Confusion`](./Passives_and_Statuses.md#object-confusion) | Array / Integer / Object  | The amount of confusion applied, either as a fixed number or an array of [stacks, probability]. | 4 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`FormChange`](./Miscellaneous.md#object-formchange) | Enum / Object  | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 4 | `{ . . . }`<br>`Big`<br>`BigHolding`<br>`BigHoldingCat` |
| [`GainCoinsRange`](./Miscellaneous.md#object-gaincoinsrange) | Object  | An object with `min` and `max` fields specifying a range for the amount of coins gained. | 4 | `{ . . . }` |
| [`Marked`](./Engine_StatusAndPassiveKeys.md#object-marked) | Array / Integer / Object  | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 4 | `{ . . . }`<br>`1`<br>`3`<br>`5` |
| `PermanentCharm` | Integer | If non-zero, permanently charms the target, converting it to the caster's faction permanently. | 4 | `1` |
| [`RandomStatDown`](./Arrays.md#array-randomstatdown) | Array / Integer / String  | The amount of random stat reduction applied, either as a fixed number, a formula string, or an array of [stacks, probability]. | 4 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`1` |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 4 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| [`Revive`](./Engine_StatusAndPassiveKeys.md#object-revive) | Integer / Object  | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 4 | `{ . . . }`<br>`1`<br>`100%`<br>`50%` |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 2 | `-1`<br>`-2`<br>`1` |
| [`Bruise`](./Passives_and_Statuses.md#object-bruise) | Array / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Bruise debuff applied, which increases damage taken. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`Charmed`](./Arrays.md#array-charmed) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of the Charmed status effect applied, making the target act as an ally. | 2 | `1`<br>`2`<br>`3` |
| [`Cleave`](./Miscellaneous.md#object-cleave) | Integer / Object  | The number of additional targets hit; if an object, contains a chance parameter for each cleave attempt. | 2 | `{ . . . }`<br>`1` |
| [`ConstitutionUp`](./Arrays.md#array-constitutionup) | Array / Enum / Integer  | The number of stacks (or [stacks, probability] array) of a Constitution buff applied, increasing maximum health. | 2 | `-1`<br>`-2`<br>`1` |
| `CritChanceUp` | Integer | The amount of critical hit chance added as a flat percentage. | 2 | `1`<br>`10`<br>`100` |
| `DamageUp` | Integer / String | The number of stacks (or a formula string) of a damage buff applied, increasing outgoing damage. | 2 | `"(-ceil(abs(X/2)))"`<br>`"(-ceil(abs(X/3)))"`<br>`-1` |
| `DodgeChance_Status` | Integer | The flat percentage increase to dodge chance applied as a status effect. | 2 | `1`<br>`10`<br>`100` |
| [`DybbukPossessed`](./Miscellaneous.md#object-dybbukpossessed) | Object  | Contains parameters for the Dybbuk possession status, specifying exit ability and self-punch ability. | 2 | `{ . . . }` |
| [`Fear`](./Arrays.md#array-fear) | Array / Integer  | The amount of Fear applied, either as a fixed number or an array of [stacks, probability]. | 2 | `1`<br>`10`<br>`2` |
| [`ImmediateUseAbility`](./Miscellaneous.md#object-immediateuseability) | Enum / Object  | Specifies the name of an ability to be triggered instantly from this effect. | 2 | `{ . . . }`<br>`FuzzerReact`<br>`HitlerCloneHeil`<br>`HitlerCloneTransform` |
| [`Immobile`](./Arrays.md#array-immobile) | Array / Integer  | The number of stacks (or [stacks, probability] array) of the Immobile debuff applied, preventing movement. | 2 | `0`<br>`1`<br>`10%` |
| `Instakill` | Integer | The amount of damage dealt to instantly kill the target; can be a flat value or a probability array (e.g., [damage, chance]). | 2 | `25`<br>`50`<br>`999` |
| [`Leeches`](./Engine_StatusAndPassiveKeys.md#object-leeches) | Integer / Object  | The number of stacks of the Leeches debuff applied, which deals damage over time and heals the applier. | 2 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 2 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| `PartialCleanse` | Integer | The number of stacks of temporary status effects to remove from the target. | 2 | `1`<br>`9999` |
| [`ScatterCoins`](./Miscellaneous.md#object-scattercoins) | Object  | The number of coins (or [stacks, probability] array) to scatter on the ground; can also include stacking behavior and formula. | 2 | `{ . . . }` |
| [`Slow`](./Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object  | The number of stacks (or [stacks, probability] array) of the Slow debuff applied, reducing speed. | 2 | `{ . . . }`<br>`-1`<br>`1`<br>`2` |
| `SpeedUp` | Enum / Integer | The number of stacks of a Speed buff applied, increasing the target's turn order priority. | 2 | `-1`<br>`-2`<br>`-4` |
| `TempSpeedUp` | Enum / Integer | The number of stacks of temporary Speed Up applied to the unit. | 2 | `10`<br>`4`<br>`X` |
| `Webbed` | Integer | The amount of webbed stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`2`<br>`[1 .1]` |
| [`AllyInfested`](./Miscellaneous.md#object-allyinfested) | Array / Number / Object  | Defines the AllyInfested object, which spawns an infested ally under the player's control. | 1 | `{ . . . }` |
| [`Poison`](./Arrays.md#array-poison) | Array / Integer  | The amount of Poison applied, either as a fixed number or an array of [stacks, probability]. || `1`<br>`10`<br>`2` |


### Object: `Fear`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `ForceAttack`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `immediate` | Boolean | If true, the action (e.g., attack) occurs instantly without waiting for the unit's turn in the initiative order. | 4 | `false`<br>`true` |


### Object: `ForceUseAbilityOnTarget`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | `.02`<br>`.1`<br>`.15` |


### Object: `FormChange`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`form`](./Enums.md#enum-form) | Enum / Integer  | Specifies the name of the form the unit changes into. | 150 | `"Angry"`<br>`"Big"`<br>`"Bishop"` |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | `.02`<br>`.1`<br>`.15` |


### Object: `Freeze`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `GainCoinsRange`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer | The maximum amount of coins that can be gained. | 22 | `10`<br>`2`<br>`25` |
| `min` | Integer | The minimum amount of coins that will be gained. | 22 | `0`<br>`1`<br>`10` |


### Object: `GainDisorderFromPool`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | `.02`<br>`.1`<br>`.15` |
| [`pool`](./Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 2 | `2`<br>`3`<br>`4` |


### Object: `Hex`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `ImmediateUseAbility`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_if_stunned` | Boolean | If true, the autocast triggers even if the unit is stunned. | 2 | `true` |


### Object: `IncAuxCounterClamped`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `change` | Integer | The amount to adjust the auxiliary counter by. | 6 | `-1`<br>`-2`<br>`-3` |
| `max` | Integer | The maximum amount of coins that can be gained. | 6 | `10`<br>`2`<br>`25` |


### Object: `Infested`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. || `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. || `{ . . . }` |
| [`class`](./Enums.md#enum-class) | Enum  | Specifies the class that this ability belongs to, used for categorization and restrictions. || `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| `default_frame` | Number | The default sprite frame used for the character's portrait or body. || `1`<br>`1000`<br>`1001` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| `icon_frame` | Number | The sprite frame index for the buff icon. || `141`<br>`148`<br>`149` |
| `lefteye` | Number | The sprite frame index for the character's left eye. || `1`<br>`100`<br>`1001` |
| `lefteyebrow` | Number | The sprite frame index for the character's left eyebrow. || `1`<br>`1000`<br>`1001` |
| `mouth` | Number | The catalog ID for the cat's mouth part. || `-1`<br>`-2`<br>`1` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`palette`](./Enums.md#enum-palette) | Enum / Integer  | Specifies the color palette index for the ability's visuals. || `-1`<br>`0`<br>`1` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| `pitch` | String | The sound pitch multiplier for the character's voice or sounds. || `.3`<br>`.5`<br>`.6` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |
| `righteye` | Number | The sprite frame index for the character's right eye. || `1`<br>`100`<br>`1001` |
| `righteyebrow` | Number | The sprite frame index for the character's right eyebrow. || `1`<br>`1000`<br>`1001` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). || `{ . . . }` |
| `texture` | Integer | The catalog ID for the cat's texture. || `-1`<br>`1`<br>`1000` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| `value` | Enum | The numeric value or formula associated with the buff. || `.5`<br>`0`<br>`1` |
| [`voice`](./Enums.md#enum-voice) | Enum  | Determines which voice set or type is used for the character. || `ankylosaurus`<br>`female1`<br>`female10` |


### Object: `IntelligenceUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `name_stacks_neg` | String | Localization key for the name of the negative variant (e.g., stat down) of this status effect. || `"KEYWORD_ALLSTATSDOWN_NAME"`<br>`"KEYWORD_CHADOWN_NAME"`<br>`"KEYWORD_CONDOWN_NAME"` |
| [`tooltip_stackless`](./Enums.md#enum-tooltip_stackless) | Enum   | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks_neg` | String | Localization key for the tooltip description of the negative variant (e.g., stat down) of this status effect. || `"KEYWORD_ALLSTATSDOWN_DESC"`<br>`"KEYWORD_CHADOWN_DESC"`<br>`"KEYWORD_CONDOWN_DESC"` |
| `tooltip_stacks_pos` | String | Localization key for the tooltip description of the positive variant (e.g., stat up) of this status effect. || `"KEYWORD_ALLSTATSUP_DESC"`<br>`"KEYWORD_CHAUP_DESC"`<br>`"KEYWORD_CONUP_DESC"` |


### Object: `KnockOutCoin`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | `.02`<br>`.1`<br>`.15` |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |


### Object: `KnockUpAndAway`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 48 | `-3`<br>`10`<br>`2` |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 44 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `displace` | Boolean | If true, the knockback also displaces the target to a different tile. | 4 | `true` |
| `height` | Integer | The height in tiles the target is launched into the air. | 4 | `0`<br>`1`<br>`2` |
| [`self_damage`](./Miscellaneous.md#object-self_damage) | Boolean / Integer / Object  | Defines damage or effects applied to the caster when using the ability. | 4 | `{ . . . }`<br>`1`<br>`10`<br>`100%` |
| `circular_variance` | Integer | The random variance in the knockback direction, in tiles. | 2 | `2` |


### Object: `Knockback`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `KnockbackIfCrit`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`knockback`](./Enums.md#enum-knockback) | Enum / Integer  | The amount of knockback applied by the damage instance; positive values push away, negative values pull toward the source. | 2 | `"ceil(X*.25/5)"`<br>`-10`<br>`-2` |
| `override_chain_knockback` | Integer | The distance in tiles the unit is knocked back if a critical hit triggers chain knockback. | 2 | `10` |


### Object: `Leech`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `icon_frame` | Number | The sprite frame index for the buff icon. || `141`<br>`148`<br>`149` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. || `3` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `Leeches`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `name_reference_applier` | String | A localization key for the name displayed to the applier of this status effect. || `"KEYWORD_ATTRACTION_REF"`<br>`"KEYWORD_LEECHES_NAME_APPLIER"`<br>`"KEYWORD_MANALEECHES_NAME_APPLIER"` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |
| `tooltip_reference_applier` | String | A localization key for the tooltip description displayed to the applier of this status effect. || `"KEYWORD_ATTRACTION_DESC_REF"`<br>`"KEYWORD_LEECHES_DESC_APPLIER"`<br>`"KEYWORD_MANALEECHES_DESC_APPLIER"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `MagicWeakness`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `ManaGainRange`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer | The maximum amount of coins that can be gained. | 2 | `10`<br>`2`<br>`25` |
| `min` | Integer | The minimum amount of coins that will be gained. | 2 | `0`<br>`1`<br>`10` |


### Object: `ManaLeeches`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `name_reference_applier` | String | A localization key for the name displayed to the applier of this status effect. || `"KEYWORD_ATTRACTION_REF"`<br>`"KEYWORD_LEECHES_NAME_APPLIER"`<br>`"KEYWORD_MANALEECHES_NAME_APPLIER"` |
| `tooltip_reference_applier` | String | A localization key for the tooltip description displayed to the applier of this status effect. || `"KEYWORD_ATTRACTION_DESC_REF"`<br>`"KEYWORD_LEECHES_DESC_APPLIER"`<br>`"KEYWORD_MANALEECHES_DESC_APPLIER"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `Marked`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `ModifyAbility`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 4 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 4 | `{ . . . }` |


### Object: `MovementUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `name_stacks_neg` | String | Localization key for the name of the negative variant (e.g., stat down) of this status effect. || `"KEYWORD_ALLSTATSDOWN_NAME"`<br>`"KEYWORD_CHADOWN_NAME"`<br>`"KEYWORD_CONDOWN_NAME"` |
| `tooltip_stackless_neg` | String | Localization key for the tooltip of the negative variant when not showing stack count. || `"KEYWORD_DAMAGEDOWN_DESC_STACKLESS"`<br>`"KEYWORD_MOVEMENTDOWN_DESC_STACKLESS"`<br>`"KEYWORD_TEMPINITDOWN_DESC"` |
| `tooltip_stackless_pos` | String | Localization key for the tooltip of the positive variant when not showing stack count. || `"KEYWORD_DAMAGEUP_DESC_STACKLESS"`<br>`"KEYWORD_MOVEMENTUP_DESC_STACKLESS"` |
| `tooltip_stacks_neg` | String | Localization key for the tooltip description of the negative variant (e.g., stat down) of this status effect. || `"KEYWORD_ALLSTATSDOWN_DESC"`<br>`"KEYWORD_CHADOWN_DESC"`<br>`"KEYWORD_CONDOWN_DESC"` |
| `tooltip_stacks_pos` | String | Localization key for the tooltip description of the positive variant (e.g., stat up) of this status effect. || `"KEYWORD_ALLSTATSUP_DESC"`<br>`"KEYWORD_CHAUP_DESC"`<br>`"KEYWORD_CONUP_DESC"` |


### Object: `NextBattleStatus`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 4 | `-1`<br>`-2`<br>`1` |
| `FullHeal` | Integer | If non-zero, fully restores the target's health. | 4 | `0`<br>`1` |


### Object: `NoHealthRegen`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `NukeQuestFinalBossModifications`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`self_damage`](./Miscellaneous.md#object-self_damage) | Boolean / Integer / Object  | Defines damage or effects applied to the caster when using the ability. | 4 | `{ . . . }`<br>`1`<br>`10`<br>`100%` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 2 | `{ . . . }` |
| [`splash_damage`](./Miscellaneous.md#object-splash_damage) | Object  | Defines additional damage or effects applied to nearby targets around the primary target. | 2 | `{ . . . }` |


### Object: `ObjectOnHitCharacter`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 14 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 10 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 4 | `.02`<br>`.1`<br>`.15` |


### Object: `OneUseSpellDamageUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alias`](./Enums.md#enum-alias) | Enum  | Specifies the reference name of another status effect to alias or copy properties from. || `AllStatsUp`<br>`Brace`<br>`Brittle` |


### Object: `Ostracized`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `PassiveWhileNotTakingTurn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack) | Object  | Contains status effects to add to the basic attack. | 2 | `{ . . . }` |


### Object: `PermanentConfusion`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `Petrify`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |
| `tooltip_stacks_singular` | String ||| `"KEYWORD_AUTOREVIVE_DESC_SINGULAR"`<br>`"KEYWORD_BLIND_DESC_STACKLESS"`<br>`"KEYWORD_BONUSMOVE_DESC"` |


### Object: `PoisonLace`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `Possessed`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |
| `tooltip_stacks_singular` | String ||| `"KEYWORD_AUTOREVIVE_DESC_SINGULAR"`<br>`"KEYWORD_BLIND_DESC_STACKLESS"`<br>`"KEYWORD_BONUSMOVE_DESC"` |


### Object: `PreEmptiveCounterNextAttacks`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |
| `tooltip_stacks_singular` | String ||| `"KEYWORD_AUTOREVIVE_DESC_SINGULAR"`<br>`"KEYWORD_BLIND_DESC_STACKLESS"`<br>`"KEYWORD_BONUSMOVE_DESC"` |


### Object: `ProbeCharmed`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |


### Object: `Purge`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |


### Object: `RandomInjury`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number | The sprite frame index for the buff icon. || `141`<br>`148`<br>`149` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `RandomMagicMissile`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `full_size` | Boolean || 4 | `true` |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `icon_frame` | Number | The sprite frame index for the buff icon. || `141`<br>`148`<br>`149` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `RandomPermanentStatsDistinct`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). || `{ . . . }` |


### Object: `RangeUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `Reanimate`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |


### Object: `Reflect`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |
| `tooltip_stacks_singular` | String ||| `"KEYWORD_AUTOREVIVE_DESC_SINGULAR"`<br>`"KEYWORD_BLIND_DESC_STACKLESS"`<br>`"KEYWORD_BONUSMOVE_DESC"` |


### Object: `RemoveStatusStacks`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 8 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`status`](./Enums.md#enum-status) | Enum  || 8 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |


### Object: `ReplaceSpell`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 8 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`slot`](./Enums.md#enum-slot) | Enum / Integer  | Specifies the equipment slot (e.g., 'head', 'trinket', 'random_empty') where the crafted item is placed. | 8 | `0`<br>`1`<br>`2` |


### Object: `Revive`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |


### Object: `ReviveNextRound`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `revive_health` | Integer || 8 | `1`<br>`100%`<br>`50%` |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 6 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). | 4 | `-1`<br>`-2`<br>`1` |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 2 | `1`<br>`2`<br>`4` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |
| `tooltip_stacks_singular` | String ||| `"KEYWORD_AUTOREVIVE_DESC_SINGULAR"`<br>`"KEYWORD_BLIND_DESC_STACKLESS"`<br>`"KEYWORD_BONUSMOVE_DESC"` |


### Object: `Rot`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `ScatterCoins`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stackable` | Boolean || 4 | `true` |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |


### Object: `Scrambled`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `SetItemAux`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`slot`](./Enums.md#enum-slot) | Enum / Integer  | Specifies the equipment slot (e.g., 'head', 'trinket', 'random_empty') where the crafted item is placed. | 6 | `0`<br>`1`<br>`2` |
| `value` | Enum | The numeric value or formula associated with the buff. | 6 | `.5`<br>`0`<br>`1` |


### Object: `Shield`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |


### Object: `Sleep`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `SoulLink`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `SpeedUp_WithoutInitiative`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alias`](./Enums.md#enum-alias) | Enum  | Specifies the reference name of another status effect to alias or copy properties from. || `AllStatsUp`<br>`Brace`<br>`Brittle` |


### Object: `SpiderInfested`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `SpreadDisease`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`disease`](./Enums.md#enum-disease) | Enum  | Determines which disease is applied when spreading disease. | 26 | `BirdFlu`<br>`Cancer`<br>`CommonCold` |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 24 | `.02`<br>`.1`<br>`.15` |
| `can_apply_to_anything` | Boolean | If true, this disease can be spread to any unit, regardless of type. | 12 | `true` |


### Object: `StacyMutant_Brace`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Brace`](./Passives_and_Statuses.md#object-brace) | Enum / Integer / Object  | The number of stacks of Brace applied to the source, reducing knockback and damage taken. | 2 | `{ . . . }`<br>`1`<br>`10`<br>`2` |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 2 | `{ . . . }` |


### Object: `StacyMutant_Counter`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AddStatusToBasicAttack`](./Passives_and_Statuses.md#object-addstatustobasicattack) | Object  | Contains status effects to add to the basic attack. | 2 | `{ . . . }` |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 2 | `{ . . . }` |
| [`CounterAttack`](./Passives_and_Statuses.md#object-counterattack) | Array / Enum / Object  | Specifies the ability used when the unit counterattacks after being hit. | 2 | `{ . . . }`<br>`BungaSwipe`<br>`CloakerHex`<br>`CollectiveCounter` |


### Object: `StacyMutant_Damage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddDamage` | Integer | The amount of damage added to all attacks. Negative values reduce damage. | 2 | `-1`<br>`1`<br>`2` |
| `AddMaxHealth` | Integer | The amount added to the unit's maximum health. Negative values reduce max health. | 2 | `-25`<br>`10`<br>`2` |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 2 | `{ . . . }` |


### Object: `StacyMutant_DoubleHead`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 2 | `{ . . . }` |
| `ExtraDispersedTurns` | Integer | The number of additional or fewer turns in the dispersed turn order. | 2 | `-1`<br>`1` |


### Object: `StacyMutant_Fire`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 2 | `{ . . . }` |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum  | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 2 | `Creep`<br>`Electric`<br>`Fire` |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum  | Specifies the ability ID that replaces the unit's basic attack. | 2 | `BasicButcherMeleeWideDoubleSpin`<br>`BasicButcherMeleeWideSpin`<br>`BasicDruidAbilityVersatile` |
| [`ReplaceBrain`](./Passives_and_Statuses.md#object-replacebrain) | Object  | Defines a replacement AI brain and behavior pattern for the mutant. | 2 | `{ . . . }` |


### Object: `StacyMutant_Health`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddMaxHealth` | Integer | The amount added to the unit's maximum health. Negative values reduce max health. | 2 | `-25`<br>`10`<br>`2` |
| `AddSpeed` | Integer | The amount of speed added (or subtracted) to the unit. | 2 | `-3`<br>`4`<br>`6` |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 2 | `{ . . . }` |
| `SizeScale` | Number | The multiplier applied to the unit's visual and hitbox size. | 2 | `.4`<br>`.6`<br>`.7` |


### Object: `StacyMutant_Holy`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 2 | `{ . . . }` |
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer  | The number of stacks of Divine Shield applied, granting immunity to damage. Can be an array [stacks, probability]. | 2 | `1`<br>`2`<br>`4` |


### Object: `StacyMutant_Ice`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddMovement` | Integer | The amount of bonus movement points added to the unit's base movement. | 2 | `-1`<br>`-2`<br>`1` |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 2 | `{ . . . }` |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum  | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 2 | `Creep`<br>`Electric`<br>`Fire` |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum  | Specifies the ability ID that replaces the unit's basic attack. | 2 | `BasicButcherMeleeWideDoubleSpin`<br>`BasicButcherMeleeWideSpin`<br>`BasicDruidAbilityVersatile` |
| [`ReplaceBrain`](./Passives_and_Statuses.md#object-replacebrain) | Object  | Defines a replacement AI brain and behavior pattern for the mutant. | 2 | `{ . . . }` |


### Object: `StacyMutant_Lightning`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 2 | `{ . . . }` |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum  | Specifies an element type (e.g., Fire, Ice) that the unit is immune to damage from. | 2 | `Creep`<br>`Electric`<br>`Fire` |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum  | Specifies the ability ID that replaces the unit's basic attack. | 2 | `BasicButcherMeleeWideDoubleSpin`<br>`BasicButcherMeleeWideSpin`<br>`BasicDruidAbilityVersatile` |
| [`ReplaceBrain`](./Passives_and_Statuses.md#object-replacebrain) | Object  | Defines a replacement AI brain and behavior pattern for the mutant. | 2 | `{ . . . }` |


### Object: `StacyMutant_Mirror`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 2 | `{ . . . }` |
| [`ReflectProjectiles`](./Passives_and_Statuses.md#object-reflectprojectiles) | Integer / Object  | The percentage chance to reflect projectiles back at the attacker; optionally includes self-damage. | 2 | `{ . . . }`<br>`1`<br>`10%`<br>`100%` |
| [`StatusEachTurnEndForEachTurn`](./Passives_and_Statuses.md#object-statuseachturnendforeachturn) | Object  | Statuses applied at the end of each turn, with the number of turns as nested values. | 2 | `{ . . . }` |


### Object: `StacyMutant_Speed`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddDamage` | Integer | The amount of damage added to all attacks. Negative values reduce damage. | 2 | `-1`<br>`1`<br>`2` |
| `AddSpeed` | Integer | The amount of speed added (or subtracted) to the unit. | 2 | `-3`<br>`4`<br>`6` |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 2 | `{ . . . }` |
| `SizeScale` | Number | The multiplier applied to the unit's visual and hitbox size. | 2 | `.4`<br>`.6`<br>`.7` |


### Object: `StacyMutant_Thorns`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](./Passives_and_Statuses.md#object-catpartstransform) | Object  | Transforms the target's visual cat parts (e.g., head, body, tail) using specified part IDs. | 2 | `{ . . . }` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 2 | `1`<br>`2`<br>`3` |


### Object: `StatusAfterXStacks`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`stack_key`](./Enums.md#enum-stack_key) | Enum   || 4 | `CATHIDE`<br>`EMPTY_GENERATOR`<br>`FANNY_PACK` |
| [`threshold`](./Passives_and_Statuses.md#object-threshold) | Enum / Integer / Object  | The health threshold value, either as a formula using X (max health) or a fixed integer. | 4 | `{ . . . }`<br>`"X*.4"`<br>`"X*.8"`<br>`"max(X*.33, 5)"` |
| `ExtraBasicMoves_Status` | Integer | The number of extra basic moves per turn granted. | 2 | `1` |
| `RefreshActPoints` | Integer | The amount of action points restored to the source. | 2 | `1` |
| `expires_on_end_turn` | Boolean | If true, the temporary effect expires at the end of the target's turn. | 2 | `true` |


### Object: `StealthUntilBasicAttack`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `Stun`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `Tangled`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alt_art`](./Enums.md#enum-alt_art) | Enum   || 2 | `TangledMeat` |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `Tarred`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `TempCounterAttack`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `TempDamageUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alias`](./Enums.md#enum-alias) | Enum  | Specifies the reference name of another status effect to alias or copy properties from. || `AllStatsUp`<br>`Brace`<br>`Brittle` |


### Object: `TempMovement`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alias`](./Enums.md#enum-alias) | Enum  | Specifies the reference name of another status effect to alias or copy properties from. || `AllStatsUp`<br>`Brace`<br>`Brittle` |


### Object: `TempPassiveUntilSettled`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`MeleeRevengeDamage`](./Passives_and_Statuses.md#object-meleerevengedamage) | Object  | Defines the damage and effects applied back to a melee attacker upon being hit. | 4 | `{ . . . }` |
| `LimitHeal` | Integer | If 1, prevents the unit from being healed. | 2 | `0`<br>`1` |


### Object: `TempRangeUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `TempSpellDamageUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alias`](./Enums.md#enum-alias) | Enum  | Specifies the reference name of another status effect to alias or copy properties from. || `AllStatsUp`<br>`Brace`<br>`Brittle` |


### Object: `TempStrengthUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alias`](./Enums.md#enum-alias) | Enum  | Specifies the reference name of another status effect to alias or copy properties from. || `AllStatsUp`<br>`Brace`<br>`Brittle` |


### Object: `Temporary`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 114 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`status`](./Enums.md#enum-status) | Enum  || 112 | `AddKnockbackToEverything`<br>`AllDamageCrits`<br>`AllDamageImmune` |
| [`turns`](./Miscellaneous.md#object-turns) | Array / Integer / Object  | Specifies the duration of a temporary effect, either as a number of turns or an object with fields like `takes_turns` and `dispersed_bonus_turns`. | 104 | `{ . . . }`<br>`1`<br>`2`<br>`3` |
| `expires_on_begin_turn` | Boolean || 50 | `true` |
| `expires_on_end_turn` | Boolean | If true, the temporary effect expires at the end of the target's turn. | 42 | `true` |
| `data` | Integer | An integer value used for custom data associated with the temporary effect. | 4 | `2` |
| `expires_on_appliers_turn` | Boolean | If true, the temporary effect expires at the start of the applier's next turn. | 4 | `true` |
| `expires_on_move` | Boolean | If true, the temporary effect expires when the target moves. | 2 | `true` |


### Object: `TransformWeapon`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum  || 4 | `JarOfChaos`<br>`Necro_SoulDagger_Charged`<br>`Necro_SoulDagger_Uncharged` |
| [`to`](./Enums.md#enum-to) | Enum  || 4 | `JarOfNothing`<br>`Necro_SoulDagger_Charged`<br>`Necro_SoulDagger_Uncharged` |


### Object: `Webbed`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `Wet`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `XIsSpellStormRampAndReset`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `reset_percent` | Integer || 2 | `50%` |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |

#### `ApplyToSourceOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 15

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AlphaCat` | Integer | The number of AlphaCat stacks applied to the source on kill. | 2 | `1` |
| [`Revive`](./Engine_StatusAndPassiveKeys.md#object-revive) | Integer / Object  | Revives a dead target with the specified percentage of health (e.g., "50%", "100%") or a fixed number. | 2 | `{ . . . }`<br>`1`<br>`100%`<br>`50%` |
| `AllStatsUp` | Enum / Integer | The number of stacks of a global stat increase applied to all stats (DamageUp, SpeedUp, ConstitutionUp, DodgeChance). || `-1`<br>`-2`<br>`1` |
| [`EvolveAbilityFromPool`](./Miscellaneous.md#object-evolveabilityfrompool) | Enum / Object  | Specifies the ability pool from which to evolve an ability for the source, optionally upgrading it. || `{ . . . }`<br>`Butcher`<br>`Druid`<br>`Fighter` |
| `HealthGain` | Integer | The amount of health restored to the source. || `1`<br>`10`<br>`2` |
| `ManaGain` | Enum / Integer | The amount of mana restored to the source, which can be an expression. || `"-ceil(X/2)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |
| `StrengthUp` | Enum / Integer | The number of stacks of Strength Up applied to the source, increasing its Strength stat. || `"max(int, 0)"`<br>`-1`<br>`-2` |
| `WeaponAuxMultiplier` | Number ||| `.5` |

</details>


---


#### `Consumed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 23

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`struggle_ability`](./Enums.md#enum-struggle_ability) | Enum | Specifies the name of the ability the consumed unit uses to attempt escape. | 17 | `CHuskStruggle`<br>`CaveWomanEscape`<br>`LennyStruggle` |
| `force_contact` | Boolean | If true, the consumed unit is forced into contact with the consumer. | 15 | `true` |
| `instant` | Boolean | If true, the consumption happens immediately without a timer. | 12 | `true` |
| [`mount_mode`](./Enums.md#enum-mount_mode) | Boolean / Enum | Specifies the mounting mode; values include 'auto' or 'true'. | 12 | `auto`<br>`true` |
| `do_not_pop_corpse` | Boolean | If true, the consumed unit's corpse is not popped upon consumption. | 11 | `true` |
| [`drop_on_death`](./Enums.md#enum-drop_on_death) | Boolean / Enum | Determines if and how the consumed unit is dropped on death; values include 'true', 'false', or 'deferred'. | 11 | `deferred`<br>`false`<br>`true` |
| `wet` | Boolean | If true, the consumed unit is considered wet (e.g., for elemental interactions). | 8 | `false`<br>`true` |
| `drop_on_self_death` | Boolean | If true, the consumed unit is dropped when the consumer dies. | 3 | `true` |
| [`extra_statuses`](./Miscellaneous.md#object-extra_statuses) | Object  | An object containing additional status effects (with stack counts) applied to the consumed unit. | 3 | `{ . . . }` |
| `use_placeholder` | Boolean | If true, renders the ability using a temporary placeholder animation instead of the final art. | 3 | `true` |
| [`drop_body_ability`](./Enums.md#enum-drop_body_ability) | Enum | Specifies the ability used to drop the consumed body. | 1 | `MoonHandDrop` |
| `kill_on_consume` | Boolean | If true, the consumed unit is killed immediately upon consumption. | 1 | `true` |

</details>


---


### Object: `AcidRain`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha` | String | The alpha transparency value for the particle system (e.g., '0.03'). || `.005`<br>`.01`<br>`.03` |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. || `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |
| `chain` | Boolean | Specifies the ability to chain into and execute. || `AcidSplash`<br>`CaveSplash`<br>`FireFullSmall` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. || `{ . . . }` |
| `emit_amount` | Number | The number of particles emitted per burst. || `1`<br>`10`<br>`100` |
| [`emit_box`](./Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. || `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| [`emit_direction`](./Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. || `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_rate` | Number | The rate of particle emission per second. || `.5`<br>`1`<br>`10` |
| `emit_spread` | Number | The angle spread for particle emission direction. || `0`<br>`1`<br>`10` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. || `false`<br>`true` |
| [`force`](./Arrays.md#array-force) | Array  | The force vector applied to particles. || `0`<br>`1`<br>`1.5` |
| [`live_bounds`](./Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. || `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| [`movieclip`](./Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. || `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `particle_lifetime` | Number | The duration in seconds particles remain alive. || `.`<br>`.025`<br>`.35` |
| [`projection_matrix`](./Enums.md#enum-projection_matrix) | Enum   | The projection matrix mode for particle rendering (e.g., 'default'). || `default` |
| [`render_mode`](./Enums.md#enum-render_mode) | Enum   | The rendering mode for particles (e.g., 'default', 'separate'). || `default`<br>`separate` |
| [`scripts`](./Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. || `{ . . . }` |
| [`simulation_space`](./Enums.md#enum-simulation_space) | Enum   | The coordinate space for particle simulation ('local' or 'global'). || `global`<br>`local` |
| `size_start` | String | The starting size of particles. || `.1`<br>`.2`<br>`.3` |
| `speed_scale` | String | A multiplier for particle speed. || `.05`<br>`.1`<br>`.2` |
| `speed_start` | Number | The initial speed of particles. || `-2`<br>`.001`<br>`.1` |


### Object: `AddPostProcessEffect`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `requires_framebuffer` | Boolean || 1 | `false` |
| [`shader`](./Enums.md#enum-shader) | Enum  || 1 | `shimmervignette` |


### Object: `AddTilesetObjects`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`FloatingDebris`](./Miscellaneous.md#object-floatingdebris) | Object  || 1 | `{ . . . }` |


### Object: `Adrenaline`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `ApplyMultipleTimes`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RandomStatusFromPool`](./Passives_and_Statuses.md#object-randomstatusfrompool) | Object  | A collection of status effects; one is randomly chosen and applied to the target. | 6 | `{ . . . }` |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 6 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |


### Object: `ApplyStatusesNextTurnBegin`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Quivered`](./Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`2`<br>`5` |


### Object: `ApplyToConsumed`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DeleteObject` | Integer || 6 | `1` |
| [`Die`](./Miscellaneous.md#object-die) | Integer / Object  | If set, kills the target immediately. | 2 | `{ . . . }`<br>`1`<br>`6` |


### Object: `ApplyToOthersWithSharedTagAndFaction`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Marked`](./Engine_StatusAndPassiveKeys.md#object-marked) | Array / Integer / Object  | The amount of Marked applied, either as a fixed number or an array of [stacks, probability]. | 2 | `{ . . . }`<br>`1`<br>`3`<br>`5` |


### Object: `ApplyToRandomClosestAlly`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ForceMoveTowards` | Integer || 2 | `1` |


### Object: `ApplyToTile`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ObjectOnHit`](./Miscellaneous.md#object-objectonhit) | Enum / Object  || 4 | `{ . . . }`<br>`Bait`<br>`BiggestFood`<br>`Carcus` |
| `SpawnBearTrap` | Integer || 4 | `1` |


### Object: `ArcLightning`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `enemies_only` | Boolean | If true, the arc lightning effect only chains to enemy units, ignoring allies. | 8 | `false`<br>`true` |
| `max_distance` | Integer || 8 | `1`<br>`2`<br>`3` |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 8 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 2 | `.02`<br>`.1`<br>`.15` |
| `ignore_self` | Boolean || 2 | `true` |


### Object: `Bloodzerked`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `BodyGuard`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `BombRatTurtle`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |


### Object: `ButterflySwarm`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. || `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |


### Object: `CanApplyToInanimate`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ObjectOnHitCharacter`](./Passives_and_Statuses.md#object-objectonhitcharacter) | Enum / Object  | Specifies the name (or object with name and stacks) of an object/entity to spawn on the target's location when hit. | 20 | `{ . . . }`<br>`AllyRotFly`<br>`BeefyCharmedLeech`<br>`BestBud` |
| [`BreakIntoRocks`](./Enums.md#enum-breakintorocks) | Enum  || 8 | `Coin`<br>`SmallRock` |
| [`ApplyToSource`](./Passives_and_Statuses.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 6 | `{ . . . }` |
| `Vaporize` | Integer | Removes the target from play, preventing its corpse from being interacted with. | 6 | `1`<br>`20` |
| `GetAggroTarget` | Integer || 4 | `1` |
| `PreventDeathTransforms` | Integer || 2 | `1` |
| [`Temporary`](./Passives_and_Statuses.md#object-temporary) | Object  | Contains parameters for applying a temporary status effect with specific stacks, turns, and expiration conditions. | 2 | `{ . . . }` |


### Object: `CastAgainWithStatus`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `OverrideDamage` | Integer || 2 | `-10`<br>`0`<br>`1` |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |


### Object: `CatPartsSizeScaleStatus`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `arm1` | Number | The catalog ID for the cat's first arm part. | 2 | `-1`<br>`-2`<br>`1` |
| `arm2` | Number | The catalog ID for the cat's second arm part. | 2 | `-1`<br>`-2`<br>`1` |
| `body` | Number | The catalog ID for the cat's body part. | 2 | `-1`<br>`1`<br>`1.1` |
| `mouth` | Number | The catalog ID for the cat's mouth part. | 2 | `-1`<br>`-2`<br>`1` |


### Object: `ChampionUpgradeNextMinion`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `ChanceToBreakFree`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 22 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`fail_ability`](./Enums.md#enum-fail_ability) | Enum   || 6 | `CHuskDropFail`<br>`LennyStruggleFail`<br>`XXX` |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 6 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |


### Object: `ChargeFists`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`keyword_tooltips`](./Passives_and_Statuses.md#object-keyword_tooltips) | Object  | Associates keyword tooltips with the ability, often used for status effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |
| `tooltip_stacks_singular` | String ||| `"KEYWORD_AUTOREVIVE_DESC_SINGULAR"`<br>`"KEYWORD_BLIND_DESC_STACKLESS"`<br>`"KEYWORD_BONUSMOVE_DESC"` |


### Object: `CockroachSwarm`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |


### Object: `CollectsPickupsWithAltEffects`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Tech` | Integer | The number of stacks of Tech applied, increasing the source's Tech stat. | 4 | `1`<br>`3` |
| `CurrentWeaponAddPoison` | Integer || 2 | `1` |
| `LuckUp` | Enum / Integer | The amount of Luck stat changed on the source, affecting random chance outcomes. | 2 | `-1`<br>`-2`<br>`-4` |
| [`Quivered`](./Arrays.md#array-quivered) | Array / Integer  | The amount of quivered stacks applied, or an [stacks, probability] array. | 2 | `1`<br>`2`<br>`5` |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| `Shield` | Enum / Integer | The amount of shield granted to the source, absorbing incoming damage. | 2 | `"2*(X-1)"`<br>`"max((X-1)*2, 0)"`<br>`"max(X*3, 0)"` |


### Object: `CopySpells`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `upgraded` | Boolean | If true, the evolved ability is the upgraded version. | 2 | `true` |


### Object: `Counterspell`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |


### Object: `CurrentWeaponAddPoison`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `DelayCastAbility`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `lingering` | Boolean | If true, the ability effect lingers after the initial cast. | 2 | `true` |
| `relative` | Boolean | If true, the delay is calculated relative to the current turn count rather than as an absolute time. | 2 | `false` |


### Object: `DelayedWind`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 2 | `-3`<br>`10`<br>`2` |


### Object: `DelayedWindCone`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer | The number of tiles the target is knocked back or pulled. | 4 | `-3`<br>`10`<br>`2` |
| `damage` | Equation | Specifies the amount of damage dealt, can be a number or expression. | 2 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |


### Object: `DoDistortionRing`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `intensity` | Integer | The strength of the screen shake effect; positive values shake more, negative values may invert direction. | 12 | `-1`<br>`-2`<br>`1` |
| [`radius`](./Arrays.md#array-radius) | Array / Integer  || 12 | `0`<br>`1`<br>`13` |
| [`speed`](./Arrays.md#array-speed) | Array / Number  | The speed of the projectile or move, can be a value or a range. | 12 | `-30`<br>`-4`<br>`.5` |


### Object: `DoScreenShake`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `intensity` | Integer | The strength of the screen shake effect; positive values shake more, negative values may invert direction. | 20 | `-1`<br>`-2`<br>`1` |
| `time` | Number | The duration in seconds of the screen shake effect. | 20 | `.5`<br>`.75`<br>`1` |


### Object: `DoubleCast`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `DoubleCastSpell`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `DoubleLoot`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |


### Object: `Drag`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`class`](./Enums.md#enum-class) | Enum  | Specifies the class that this ability belongs to, used for categorization and restrictions. || `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |


### Object: `DustOnHit`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 6 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |


### Object: `EliteUpgradeNextMinion`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `EmptyMind`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `Enlarge`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`self_damage`](./Miscellaneous.md#object-self_damage) | Boolean / Integer / Object  | Defines damage or effects applied to the caster when using the ability. || `{ . . . }`<br>`1`<br>`10`<br>`100%` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |


### Object: `FactionUprising`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`extra_statuses`](./Miscellaneous.md#object-extra_statuses) | Object  || 1 | `{ . . . }` |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 1 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |


### Object: `FireArmor`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`class`](./Enums.md#enum-class) | Enum  | Specifies the class that this ability belongs to, used for categorization and restrictions. || `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `FireArmor2`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `FireStorm`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`combo`](./Arrays.md#array-combo) | Array  | A list of particle effect names that are spawned together in sequence. || `[BloodPoof BloodBounce]`<br>`[BloodPoofCrit BloodBounceCrit BloodPopCrit]`<br>`[BloodPoof_Absorb BloodBounce_Absorb]` |


### Object: `FireflySwarm`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |


### Object: `FlySwarm`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. || `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. || `{ . . . }` |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. || `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. || `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. || `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). || `{ . . . }` |


### Object: `Fog`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_end` | Number ||| `.2`<br>`.5`<br>`0` |
| `alpha_start` | Number ||| `-1`<br>`.5`<br>`.8` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. || `{ . . . }` |
| `emit_amount` | Number | The number of particles emitted per burst. || `1`<br>`10`<br>`100` |
| [`emit_box`](./Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. || `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| [`emit_direction`](./Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. || `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_rate` | Number | The rate of particle emission per second. || `.5`<br>`1`<br>`10` |
| `emit_spread` | Number | The angle spread for particle emission direction. || `0`<br>`1`<br>`10` |
| [`friction`](./Arrays.md#array-friction) | Array  | A scalar or 3D vector multiplier for velocity reduction applied over time. || `.1`<br>`.2`<br>`.5` |
| [`live_bounds`](./Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. || `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| [`movieclip`](./Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. || `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`particle_lifetime`](./Arrays.md#array-particle_lifetime) | Array   | The duration in seconds particles remain alive. || `.`<br>`.025`<br>`.35` |
| [`projection_matrix`](./Enums.md#enum-projection_matrix) | Enum   | The projection matrix mode for particle rendering (e.g., 'default'). || `default` |
| [`render_mode`](./Enums.md#enum-render_mode) | Enum   | The rendering mode for particles (e.g., 'default', 'separate'). || `default`<br>`separate` |
| [`scripts`](./Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. || `{ . . . }` |
| [`simulation_space`](./Enums.md#enum-simulation_space) | Enum   | The coordinate space for particle simulation ('local' or 'global'). || `global`<br>`local` |
| [`size_start`](./Arrays.md#array-size_start) | Array   | The starting size of particles. || `.1`<br>`.2`<br>`.3` |
| `speed_start` | String | The initial speed of particles. || `-2`<br>`.001`<br>`.1` |


### Object: `ForceImmediateMoveAndAttack`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `even_if_cant_reach` | Boolean || 2 | `true` |


### Object: `ForceMoveTowardsTaggedObject`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`tag`](./Arrays.md#array-tag) | Array / Enum  | Specifies the tag(s) to check on the target, used in conditional effects. | 2 | `[alien robot]`<br>`[alien rock]`<br>`[alien]` |


### Object: `GlobalSpawnOnRoundEnd`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 2 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| [`number`](./Arrays.md#array-number) | Array / Integer  ||| `1`<br>`10`<br>`2` |


### Object: `Grappled`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `Grappling`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit_animations`](./Miscellaneous.md#object-exit_animations) | Object  || 2 | `{ . . . }` |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer   | Specifies an animation suffix for partial form changes. | 2 | `""`<br>`"Angry"`<br>`"Belly"` |


### Object: `HealAlliesEachTurn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exclude_self` | Boolean || 4 | `false` |
| `mana` | Enum / Integer || 4 | `"4-clamp(floor(X/7), 0, 1)"`<br>`"max(4-X, 0)"`<br>`"max(7-2*X,0)"` |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |


### Object: `HeatWave`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`combo`](./Arrays.md#array-combo) | Array  | A list of particle effect names that are spawned together in sequence. || `[BloodPoof BloodBounce]`<br>`[BloodPoofCrit BloodBounceCrit BloodPopCrit]`<br>`[BloodPoof_Absorb BloodBounce_Absorb]` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. || `{ . . . }` |
| [`hint_persistent_elements`](./Arrays.md#array-hint_persistent_elements) | Array   | A list of element types that remain persistent on the ground during this weather. || `[Fire]`<br>`[Heat]`<br>`[Holy]` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `HeavyHits`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](./Enums.md#enum-tooltip_stackless) | Enum   | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `HolyDamageBlessing`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Burn`](./Arrays.md#array-burn) | Array / Enum / Integer  | The amount of Burn applied, either as a fixed number or a formula string. | 4 | `1`<br>`10`<br>`2` |
| `damage_multiplier` | Number || 4 | `2`<br>`3` |


### Object: `IceArmor`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`class`](./Enums.md#enum-class) | Enum  | Specifies the class that this ability belongs to, used for categorization and restrictions. || `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `IncAuxCounterCycle`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `change` | Integer | The amount to adjust the auxiliary counter by. | 2 | `-1`<br>`-2`<br>`-3` |
| `max` | Integer | The maximum amount of coins that can be gained. | 2 | `10`<br>`2`<br>`25` |


### Object: `Invulnerable`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `JudgementDay`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |


### Object: `KillEnemyOfTypeAtBattleStart`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`enemy_type`](./Enums.md#enum-enemy_type) | Enum   || 2 | `any`<br>`cat` |
| [`fallback_spawn`](./Arrays.md#array-fallback_spawn) | Array   ||| `[TomTom Kitten CatCaller Mangy]` |


### Object: `LateStatusApplication`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CurrentWeaponDamageUp` | Integer || 6 | `1`<br>`3`<br>`5` |
| `AddWeaponAux` | Integer / String | The amount or expression to add to the source's weapon auxiliary stat. | 2 | `"-max(min(X+1, item_aux), 0)"`<br>`-item_aux`<br>`1` |


### Object: `LeaveBehind`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 8 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |


### Object: `Math`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer  | The amount of Stun applied, either as a fixed number or an array of [stacks, probability]. | 4 | `1`<br>`2`<br>`3` |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`ApplyToSource`](./Passives_and_Statuses.md#object-applytosource) | Object  | An object of effects that are applied to the source of the ability (the caster). | 2 | `{ . . . }` |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |


### Object: `Meaty`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `MergeDamageInstance`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `can_instapop` | Boolean || 2 | `false` |
| `force_no_hit_animation` | Boolean || 2 | `true` |


### Object: `MeteorShower`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |


### Object: `Meteornado`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_in` | String ||| `.01`<br>`.05`<br>`.1` |
| `alpha_out` | String ||| `.2`<br>`.3`<br>`.5` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. || `{ . . . }` |
| `emit_amount` | Number | The number of particles emitted per burst. || `1`<br>`10`<br>`100` |
| [`emit_box`](./Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. || `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| [`emit_direction`](./Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. || `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_rate` | Number | The rate of particle emission per second. || `.5`<br>`1`<br>`10` |
| `emit_spread` | Number | The angle spread for particle emission direction. || `0`<br>`1`<br>`10` |
| [`live_bounds`](./Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. || `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| [`movieclip`](./Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. || `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`particle_lifetime`](./Arrays.md#array-particle_lifetime) | Array   | The duration in seconds particles remain alive. || `.`<br>`.025`<br>`.35` |
| [`projection_matrix`](./Enums.md#enum-projection_matrix) | Enum   | The projection matrix mode for particle rendering (e.g., 'default'). || `default` |
| [`render_mode`](./Enums.md#enum-render_mode) | Enum   | The rendering mode for particles (e.g., 'default', 'separate'). || `default`<br>`separate` |
| [`rotation`](./Arrays.md#array-rotation) | Array  ||| `-90`<br>`90`<br>`[-10 10]` |
| [`rotation_speed`](./Arrays.md#array-rotation_speed) | Array   ||| `[-10, 10]`<br>`[-100 100]`<br>`[-100, 100]` |
| [`scripts`](./Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. || `{ . . . }` |
| [`simulation_space`](./Enums.md#enum-simulation_space) | Enum   | The coordinate space for particle simulation ('local' or 'global'). || `global`<br>`local` |
| [`size_start`](./Arrays.md#array-size_start) | Array   | The starting size of particles. || `.1`<br>`.2`<br>`.3` |
| `speed_start` | Number | The initial speed of particles. || `-2`<br>`.001`<br>`.1` |


### Object: `Metronome`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. || `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`banned_abilities`](./Arrays.md#array-banned_abilities) | Array   | A list of ability IDs that are excluded from random selection or usage in the Metronome effect. || `[BatteryNuke WeAreOne Metronome SmartMetronome BecomeEntropy ForbiddenFamine]` (Array) |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Integer | The sprite frame index to display. || `1`<br>`10`<br>`100` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`kind`](./Enums.md#enum-kind) | Enum  | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). || `face`<br>`head`<br>`modifier` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`rarity`](./Enums.md#enum-rarity) | Enum  | Determines the rarity tier of the item, affecting drop rates and item quality. || `common`<br>`consumable_common`<br>`consumable_rare` |
| [`set`](./Arrays.md#array-set) | Array / Enum  | Specifies the set name(s) the item belongs to for set bonuses. || `80s`<br>`90s`<br>`AdvancedAlloy` |
| [`tags`](./Arrays.md#array-tags) | Array / Enum  | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). || `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |


### Object: `Muted`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |
| `tooltip_stacks_singular` | String ||| `"KEYWORD_AUTOREVIVE_DESC_SINGULAR"`<br>`"KEYWORD_BLIND_DESC_STACKLESS"`<br>`"KEYWORD_BONUSMOVE_DESC"` |


### Object: `NextAbilityHeals`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `NextActionLuckUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alias`](./Enums.md#enum-alias) | Enum  | Specifies the reference name of another status effect to alias or copy properties from. || `AllStatsUp`<br>`Brace`<br>`Brittle` |


### Object: `NextAttackBonusRange`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `NextAttackSpecialCrit`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crit_multiplier_bonus` | Integer || 2 | `2` |
| `extra_coins_per_stack` | Integer || 2 | `2` |
| `luck_increase` | Integer || 2 | `1` |


### Object: `NextBasicAttackCritsThisTurn`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cant_miss` | Boolean | If true, the damage instance always hits its target regardless of accuracy or evasion. | 2 | `true` |
| `piercing` | Boolean | If true, the damage instance ignores armor or damage reduction effects on the target. | 2 | `true` |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |


### Object: `NextBattleStatusStacks`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MadnessChanceOnTurnBegin` | Integer || 2 | `2` |
| `fights` | Integer | The number of future battles the status effect will be applied at the start of. | 2 | `1`<br>`9999` |


### Object: `NextDamageReduceAndHealAllies`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `NextTurnDoubleRangedDamage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `ObjectOnHit`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 4 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |


### Object: `OverHealToStatuses`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RandomStatUp` | Integer / String | The amount of random stat increase applied, either as a fixed number or a formula string. | 2 | `"ceil(X/2)"`<br>`"ceil(X/3)"`<br>`-1` |
| `TakeExtraTurn` | Integer | The number of extra turns granted to the source. | 2 | `1` |
| `stack_scale` | Integer | The scaling factor for how many stacks of the over-heal status are applied. | 2 | `0` |


### Object: `PoolMetronome`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. || `2`<br>`3`<br>`4` |


### Object: `QuakeAreaChance`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number | A probability (decimal or percentage) for a form change or other effect to occur. | 4 | `.02`<br>`.1`<br>`.15` |
| [`radius`](./Arrays.md#array-radius) | Array / Integer  || 4 | `0`<br>`1`<br>`13` |


### Object: `RandomDistanceDisplace`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `min_dist` | Integer | The minimum distance in tiles the target must be displaced by the knockback effect. | 2 | `2`<br>`3`<br>`4` |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |


### Object: `RandomKnockback`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer | The maximum amount of coins that can be gained. | 4 | `10`<br>`2`<br>`25` |
| `min` | Integer | The minimum amount of coins that will be gained. | 4 | `0`<br>`1`<br>`10` |


### Object: `ReduceManaCostExcludeBrainstorm`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `Regurge`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`self_damage`](./Miscellaneous.md#object-self_damage) | Boolean / Integer / Object  | Defines damage or effects applied to the caster when using the ability. || `{ . . . }`<br>`1`<br>`10`<br>`100%` |
| [`spawn`](./Miscellaneous.md#object-spawn) | Object  | Defines what object or unit is spawned when the ability is used. || `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |


### Object: `RepressedMemoriesMetronome`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. | 4 | `2`<br>`3`<br>`4` |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 4 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |


### Object: `Sandstorm`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. || `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |


### Object: `ScrambleLastUsedSpell`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `permanent` | Boolean || 2 | `true` |


### Object: `SerratedClaws`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `SetAnimationAlts`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`dead`](./Enums.md#enum-dead) | Enum  | Determines the animation set used when the unit is dead. | 2 | `deadShot` |
| [`dying`](./Enums.md#enum-dying) | Enum  | Determines the animation set used when the unit is in a dying state. | 2 | `shot` |


### Object: `SetCrazyEyeBackgroundWeights`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`weights`](./Arrays.md#array-weights) | Array / Enum  | Specifies the weight array or named preset for the crazy eye background AI. || `[0 0 1]`<br>`[0 1 0]`<br>`[1 0 0]` |


### Object: `Shatter`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |


### Object: `ShortCircuit`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `SmartMetronome`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| `upgraded` | Boolean | If true, the evolved ability is the upgraded version. | 2 | `true` |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`tags`](./Arrays.md#array-tags) | Array / Enum  | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). || `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |


### Object: `SmellBlood`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |


### Object: `Snow`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum   | Specifies the weather type on the adventure map, determining visual and gameplay effects. | 1 | `Rain`<br>`Snow`<br>`Thunderstorm` |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. | 1 | `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |
| `prewarm` | Number | The number of seconds the particle system simulates forward before becoming visible. | 1 | `20`<br>`5` |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum   | Determines which skybox background frame is displayed for this weather. | 1 | `day_rain`<br>`day_snow`<br>`day_thunderstorm` |
| `alpha` | String | The alpha transparency value for the particle system (e.g., '0.03'). || `.005`<br>`.01`<br>`.03` |
| [`combo`](./Arrays.md#array-combo) | Array  | A list of particle effect names that are spawned together in sequence. || `[BloodPoof BloodBounce]`<br>`[BloodPoofCrit BloodBounceCrit BloodPopCrit]`<br>`[BloodPoof_Absorb BloodBounce_Absorb]` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. || `{ . . . }` |
| `emit_amount` | Number | The number of particles emitted per burst. || `1`<br>`10`<br>`100` |
| [`emit_box`](./Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. || `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| [`emit_direction`](./Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. || `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_rate` | Number | The rate of particle emission per second. || `.5`<br>`1`<br>`10` |
| `emit_spread` | Number | The angle spread for particle emission direction. || `0`<br>`1`<br>`10` |
| [`hint_persistent_elements`](./Arrays.md#array-hint_persistent_elements) | Array   | A list of element types that remain persistent on the ground during this weather. || `[Fire]`<br>`[Heat]`<br>`[Holy]` |
| [`live_bounds`](./Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. || `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| [`movieclip`](./Arrays.md#array-movieclip) | Array / Enum  | Specifies the visual movie clip or sprite asset used for the object. || `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `particle_lifetime` | Number | The duration in seconds particles remain alive. || `.`<br>`.025`<br>`.35` |
| [`particles`](./Arrays.md#array-particles) | Array  | A list of particle system identifiers used to render the weather effects. || `[Rain]`<br>`[Snow]`<br>`[Thunderstorm]` |
| [`projection_matrix`](./Enums.md#enum-projection_matrix) | Enum   | The projection matrix mode for particle rendering (e.g., 'default'). || `default` |
| [`render_mode`](./Enums.md#enum-render_mode) | Enum   | The rendering mode for particles (e.g., 'default', 'separate'). || `default`<br>`separate` |
| [`rotation`](./Arrays.md#array-rotation) | Array  ||| `-90`<br>`90`<br>`[-10 10]` |
| [`rotation_speed`](./Arrays.md#array-rotation_speed) | Array   ||| `[-10, 10]`<br>`[-100 100]`<br>`[-100, 100]` |
| `rotation_speed_end` | Number ||| `0` |
| [`scripts`](./Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. || `{ . . . }` |
| [`simulation_space`](./Enums.md#enum-simulation_space) | Enum   | The coordinate space for particle simulation ('local' or 'global'). || `global`<br>`local` |
| `size_end` | Number ||| `.1`<br>`.2`<br>`.3` |
| [`size_start`](./Arrays.md#array-size_start) | Array   | The starting size of particles. || `.1`<br>`.2`<br>`.3` |
| [`speed_start`](./Arrays.md#array-speed_start) | Array   | The initial speed of particles. || `-2`<br>`.001`<br>`.1` |


### Object: `SolarFlare`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Equation | Specifies the amount of damage dealt, can be a number or expression. | 1 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. | 1 | `{ . . . }` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`elements`](./Arrays.md#array-elements) | Array  | An array of element tags (e.g., [Heat Fire]) that define the elemental types of the damage instance for resistances and interactions. || `[`<br>`[Heat Fire]` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |


### Object: `SpawnTilePuddleOnBattleStart`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max_radius` | Number || 1 | `2.2`<br>`3.5` |
| `min_radius` | Number || 1 | `.2`<br>`1`<br>`1.5` |
| [`tile`](./Arrays.md#array-tile) | Array / Enum  | Specifies the tile type(s) to change to, either a single tile string or an array of tiles. | 1 | `BrambleTile`<br>`CreepTile`<br>`DirtTile` |


### Object: `SpawnVolcanoOnBattleStart`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`object`](./Arrays.md#array-object) | Array / Enum  | Specifies the object or unit to be spawned. | 3 | `AlbinoTomTom`<br>`AlbinoTomTom_Elite`<br>`AlienBeast` |
| `max_radius` | Number || 2 | `2.2`<br>`3.5` |
| `min_radius` | Number / String || 2 | `.2`<br>`1`<br>`1.5` |
| [`puddle_tile`](./Arrays.md#array-puddle_tile) | Array / Enum   || 1 | `LavaTile`<br>`[BrambleTile TallBrambleTile]` |
| [`number`](./Arrays.md#array-number) | Array / Integer  ||| `1`<br>`10`<br>`2` |


### Object: `SpecialGodRays`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Big`](./Miscellaneous.md#object-big) | Object  || 2 | `{ . . . }` |


### Object: `SpellShield`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `StatBounty`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `StatusCharactersOnRoundEnd`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 1 | `{ . . . }` |
| `FloatingRockTrap` | Integer || 1 | `1` |
| `Thorns` | Integer | The amount of thorns damage dealt to attackers on hit. | 1 | `1`<br>`2`<br>`3` |
| [`tag_filter`](./Enums.md#enum-tag_filter) | Enum   || 1 | `crow`<br>`grub_familiar`<br>`rock` |


### Object: `StatusCharactersOnRoundStart`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_GoodRoll`](./Passives_and_Statuses.md#object-conditional_goodroll) | Object  | Contains an inner effect block that only executes on a successful luck roll, with an `odds` field specifying the probability. | 1 | `{ . . . }` |
| [`Else`](./Passives_and_Statuses.md#object-else) | Object  | Contains the fallback effects to apply when a preceding conditional check fails. | 1 | `{ . . . }` |
| [`Madness`](./Passives_and_Statuses.md#object-madness) | Array / Enum / Integer / Object  | The amount of Madness applied, either as a fixed number, a string like "level", or an array of [stacks, probability]. || `{ . . . }`<br>`1`<br>`2`<br>`3` |


### Object: `SwapWeapon`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`pool`](./Arrays.md#array-pool) | Array / Enum  | Specifies the name of the pool from which an ability is learned or an item is crafted. || `2`<br>`3`<br>`4` |


### Object: `SwitchMusic`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`new_layer`](./Enums.md#enum-new_layer) | Enum   || 14 | `battle`<br>`event`<br>`map` |
| [`new_song`](./Enums.md#enum-new_song) | Enum   || 12 | `same` |
| `crossfade_speed` | Integer | The duration in seconds for the crossfade transition between music tracks. | 2 | `1` |


### Object: `Switcheroo`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `Taunting`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `TeamCastAbility`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 4 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`tag_restriction`](./Enums.md#enum-tag_restriction) | Enum   | Specifies a tag that the target unit must have for the team cast to trigger. | 4 | `collective`<br>`dc_cat`<br>`dinofamily` |
| `same_orientation` | Boolean | If true, the team cast ability only triggers if the caster and target face the same direction. | 2 | `true` |


### Object: `TempBackstab`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `TempBonusKnockback`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](./Enums.md#enum-tooltip_stackless) | Enum   | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `TempBonusKnockbackDamage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](./Enums.md#enum-tooltip_stackless) | Enum   | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `TempCritChanceUp`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`alias`](./Enums.md#enum-alias) | Enum  | Specifies the reference name of another status effect to alias or copy properties from. || `AllStatsUp`<br>`Brace`<br>`Brittle` |


### Object: `TempInjuryImmunity`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip_stackless`](./Enums.md#enum-tooltip_stackless) | Enum   | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |
| `tooltip_stacks_singular` | String ||| `"KEYWORD_AUTOREVIVE_DESC_SINGULAR"`<br>`"KEYWORD_BLIND_DESC_STACKLESS"`<br>`"KEYWORD_BONUSMOVE_DESC"` |


### Object: `TempManaCostReduction`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `TempPreEmptiveCounterAttack`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `TemporaryItem`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number | The sprite frame index for the buff icon. || `141`<br>`148`<br>`149` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `TilesMovedToCritChance`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `TilesMovedToMana`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `TilesMovedToNeighborHeal`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `TilesMovedToStrength`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `TimeDelayStatusApplication`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `delay` | Number || 8 | `.05`<br>`.1`<br>`.25` |
| [`SwitchMusic`](./Miscellaneous.md#object-switchmusic) | Object  || 4 | `{ . . . }` |
| [`Cleanse`](./Engine_StatusAndPassiveKeys.md#object-cleanse) | Integer / Object  | The number of stacks of negative status effects removed from the target. | 2 | `{ . . . }`<br>`0`<br>`1` |
| [`CreateGlobalModifiers`](./Passives_and_Statuses.md#object-createglobalmodifiers) | Object  | Defines global gameplay modifiers to activate. | 2 | `{ . . . }` |
| [`DoScreenShake`](./Miscellaneous.md#object-doscreenshake) | Integer / Object  || 2 | `{ . . . }`<br>`1` |
| [`FormChange`](./Miscellaneous.md#object-formchange) | Enum / Object  | Specifies the form the target transforms into, either as a string or an object with a `form` field. | 2 | `{ . . . }`<br>`Big`<br>`BigHolding`<br>`BigHoldingCat` |
| `FullHeal` | Integer | If non-zero, fully restores the target's health. | 2 | `0`<br>`1` |
| [`GlobalSpawnCharacter`](./Enums.md#enum-globalspawncharacter) | Enum  || 2 | `MegaGuppy` |
| `PlayBackground` | Integer || 2 | `0`<br>`1` |
| `RemoveAmbientLightEffects` | Number | The fade-out duration in seconds for ambient light effects. | 2 | `.5`<br>`4` |
| `Vaporize` | Integer | Removes the target from play, preventing its corpse from being interacted with. | 2 | `1`<br>`20` |


### Object: `TowerDefenseStatus`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `TowerDefenseStatus2`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `tooltip_stackless` | String | A localization key for the tooltip description of this status effect when it has no stack count. || `"KEYWORD_ALPHA_DESC_STACKLESS"`<br>`"KEYWORD_ATTRACTION_DESC_STACKLESS"`<br>`"KEYWORD_BLASTRESISTANCE_DESC_STACKLESS"` |
| `tooltip_stacks` | String | A localization key for the tooltip description of this status effect when displayed with its stack count. || `"KEYWORD_AMMO_DESC"`<br>`"KEYWORD_ATTRACTION_DESC"`<br>`"KEYWORD_AUTOREVIVE_DESC"` |


### Object: `TradeLife`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bonus_passives`](./Miscellaneous.md#object-bonus_passives) | Object  ||| `{ . . . }` |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |


### Object: `TrailBlazer`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. || `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`tooltip`](./Enums.md#enum-tooltip) | Enum  | The localization string key used for the tooltip displayed on hover. || `""`<br>`"Bad miniboss. this needs to be redesigned."`<br>`"Beaver!"` |


### Object: `TransformEquipment`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`from`](./Enums.md#enum-from) | Enum  || 2 | `JarOfChaos`<br>`Necro_SoulDagger_Charged`<br>`Necro_SoulDagger_Uncharged` |
| [`to`](./Enums.md#enum-to) | Enum  || 2 | `JarOfNothing`<br>`Necro_SoulDagger_Charged`<br>`Necro_SoulDagger_Uncharged` |


### Object: `TwisterDisplaceWithDamage`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Equation | Specifies the amount of damage dealt, can be a number or expression. | 12 | `"(15+bonus_melee_damage)*.5"`<br>`"(4+bonus_ranged_damage+1)/2"`<br>`"(5+bonus_melee_ability_damage)*.5"` |
| `max_dist` | Integer | The maximum distance in tiles the target can be displaced by the knockback effect. | 12 | `2`<br>`20`<br>`3` |
| `min_dist` | Integer | The minimum distance in tiles the target must be displaced by the knockback effect. | 4 | `2`<br>`3`<br>`4` |
| [`exclude_prefix`](./Enums.md#enum-exclude_prefix) | Enum   | Specifies a prefix string; units with a matching prefix in their ID are excluded from the displacement effect. | 2 | `Twister` |


### Object: `UseMoveAbilityWithAI`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ability`](./Enums.md#enum-ability) | Enum  | Specifies the ability to be used or triggered when the parent condition is met. | 2 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| [`move_weights`](./Enums.md#enum-move_weights) | Enum   | Determines the movement strategy used by the AI when executing this move ability. | 2 | `bird`<br>`blind_move_far`<br>`chaos_always_move` |


### Object: `VisualCountDownThenApplyStatus`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](./Passives_and_Statuses.md#object-forceuseability) | Enum / Object  | The name of the ability the source is forced to use, optionally with a chance. | 2 | `{ . . . }`<br>`CancerExplode`<br>`DustDash`<br>`Hallucinate_Disorder` |


### Object: `VisualFlySwarm`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. || `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. || `{ . . . }` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |


### Object: `WaggleClone`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cWaggle`](./Miscellaneous.md#object-cwaggle) | Boolean (Flag) / Object  | Defines a clone variant of the Waggle unit with its own graphics and properties. | 2 | `{ . . . }` |
| [`cWaggle2x2`](./Miscellaneous.md#object-cwaggle2x2) | Boolean (Flag) / Object  | Defines a larger 2x2 tile clone variant of the Waggle unit. | 2 | `{ . . . }` |
| `stacks` | Enum / Integer | Specifies the number of stacks for a temporary status effect, either as a fixed number, a formula string, or by referencing an item's auxiliary value. | 2 | `"floor(lck/4)"`<br>`"max(min(X+1, item_aux), 0)"`<br>`-2` |
| [`cWaggle3x3`](./Miscellaneous.md#object-cwaggle3x3) | Boolean (Flag) / Object  | Defines an even larger 3x3 tile clone variant of the Waggle unit. || `{ . . . }` |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. || `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. || `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. || `{ . . . }` |
| [`template`](./Enums.md#enum-template) | Enum  | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). || `dash_attack`<br>`jump_attack`<br>`jump_move` |


### Object: `Windy`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`adventure_weather`](./Enums.md#enum-adventure_weather) | Enum   | Specifies the weather type on the adventure map, determining visual and gameplay effects. | 1 | `Rain`<br>`Snow`<br>`Thunderstorm` |
| `ambient_sound` | String | The filename of the ambient sound loop played during this weather type. | 1 | `amb_acidrain.ogg`<br>`amb_blizzard.ogg`<br>`amb_butterflyswarm.ogg` |
| `prewarm` | Number | The number of seconds the particle system simulates forward before becoming visible. | 1 | `20`<br>`5` |
| [`skybox_frame`](./Enums.md#enum-skybox_frame) | Enum   | Determines which skybox background frame is displayed for this weather. | 1 | `day_rain`<br>`day_snow`<br>`day_thunderstorm` |
| [`desc`](./Enums.md#enum-desc) | Enum  | Specifies the localized description string for the item or ability. || `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| [`effects`](./Passives_and_Statuses.md#object-effects) | Object  | Applies a list of status effects or visual effects to targets. || `{ . . . }` |
| [`hint_persistent_elements`](./Arrays.md#array-hint_persistent_elements) | Array   | A list of element types that remain persistent on the ground during this weather. || `[Fire]`<br>`[Heat]`<br>`[Holy]` |
| [`name`](./Enums.md#enum-name) | Enum  | Specifies the localized name string for the entity, item, or ability. || `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`particles`](./Arrays.md#array-particles) | Array  | A list of particle system identifiers used to render the weather effects. || `[Rain]`<br>`[Snow]`<br>`[Thunderstorm]` |


### Object: `XIsTargetHealth`


| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BonusDamage` | Enum / Integer | The amount of flat bonus damage added (negative values reduce damage). | 4 | `"ceil(X/2)"`<br>`"max(0, floor(X/2)-1)"`<br>`"max(0, floor(X/6)-1)"` |


---


## Auto-Discovered Objects


### Object: `AbsorbBuff`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_end` | Number | The alpha (opacity) value at the end of the effect's duration or animation. | 1 | `.2`<br>`.5`<br>`0` |
| `alpha_start` | Number | The alpha (opacity) value at the start of the effect's duration or animation. | 1 | `-1`<br>`.5`<br>`.8` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| [`emit_box`](./Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| [`emit_direction`](./Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_rate` | Number | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0`<br>`1`<br>`10` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `false`<br>`true` |
| [`live_bounds`](./Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `ownership` | String | The ownership scope for the effect, such as local to the caster. | 1 | `local`<br>`local*/` |
| [`particle_lifetime`](./Arrays.md#array-particle_lifetime) | Array   | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| [`scripts`](./Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. | 1 | `{ . . . }` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| `size_end` | Number | The size (scalar or 2D vector) of the effect at the end of its animation. | 1 | `.1`<br>`.2`<br>`.3` |
| [`size_start`](./Arrays.md#array-size_start) | Array   | The starting size of particles. | 1 | `.1`<br>`.2`<br>`.3` |
| `speed_scale` | Number | A multiplier for particle speed. | 1 | `.05`<br>`.1`<br>`.2` |
| `speed_start` | Number | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |

</details>


### Object: `BBTransformMutant`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BBTransformZealot`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BasicButcherMelee`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BasicDruidAbility`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`tags`](./Arrays.md#array-tags) | Array  | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BasicMagicMissile`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BasicMagicShortRanged`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BasicMedicMelee`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BasicMelee`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BasicMelee_4Hits`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `BasicMonkMelee`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BasicNecroRanged`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BasicPsychicPull`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BasicRanged`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BasicStraightShot`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BasicSuplex`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`tags`](./Arrays.md#array-tags) | Array  | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BasicTankMelee`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BeefyCharmedLeech`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Bionic`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. | 1 | `3` |

</details>


### Object: `BloatEyeMovement2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BloatyExplodey`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BoneWormShotMed`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BonusToss`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BonusToss2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `BoomerCatExplode`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BoyDino`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `BoyDinoCry`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BrambleRandomTileEvent`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `BungaSwipe`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai_ability` | String | Specifies the ability to use as the AI's behavior for this ability. | 1 | `AZ_Jump_AI`<br>`BasicBigMelee`<br>`BasicMelee` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `CatGoop`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `CatapultJump`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `CatapultJump2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `CaveCatDad`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`equipment`](./Miscellaneous.md#object-equipment) | Object  | A container object defining the character's equipped items (head, face, neck, weapon, etc.). | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `CerberubsStraightReaction`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `CharmedDemonKitten`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `CharmedFly`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `CharmedFlySwarm`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `CharmedLeech`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `CharmedPooter`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `CharmedReaper`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `CharmedTinySpider`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 2 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 2 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |

</details>


### Object: `CharmedTinyTumor`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Chubs`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `ChubsGoop`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `ChubsRage`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `CookedChickenLeg`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `CraterCreeperOut`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `DarkOneStrike`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `DecoyExplode`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `DefaultMove`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `DestroyerShieldBash`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `Digest`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`self_damage`](./Miscellaneous.md#object-self_damage) | Object  | Defines damage or effects applied to the caster when using the ability. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `DrMangler`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `EatShit`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `FireExtinguish_Steam`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha` | Number | The alpha transparency value for the particle system (e.g., '0.03'). | 1 | `.005`<br>`.01`<br>`.03` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| [`emit_box`](./Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| [`emit_direction`](./Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_radius` | Number | The radius from which particles or effects are emitted. | 1 | `.05`<br>`.1`<br>`.2` |
| `emit_rate` | Number | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| `emit_timespread` | Number | The time spread over which emissions occur, controlling the duration of the emission burst. | 1 | `.1`<br>`.25`<br>`.75` |
| `emit_timespread_curve` | String | The curve type (e.g., ease_out) that defines how emission rate changes over time. | 1 | `ease_out` |
| [`live_bounds`](./Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `particle_lifetime` | Number | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| [`scripts`](./Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. | 1 | `{ . . . }` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| [`size`](./Arrays.md#array-size) | Array  | The scale factor (size multiplier) of the spawned unit. | 1 | `.2`<br>`.5`<br>`1` |
| [`speed`](./Arrays.md#array-speed) | Array  | The speed of the projectile or move, can be a value or a range. | 1 | `-30`<br>`-4`<br>`.5` |

</details>


### Object: `FlyBuff`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_end` | Number | The alpha (opacity) value at the end of the effect's duration or animation. | 1 | `.2`<br>`.5`<br>`0` |
| `alpha_start` | Number | The alpha (opacity) value at the start of the effect's duration or animation. | 1 | `-1`<br>`.5`<br>`.8` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| [`emit_box`](./Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| [`emit_direction`](./Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_rate` | Number | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0`<br>`1`<br>`10` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `false`<br>`true` |
| [`live_bounds`](./Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `ownership` | String | The ownership scope for the effect, such as local to the caster. | 1 | `local`<br>`local*/` |
| [`particle_lifetime`](./Arrays.md#array-particle_lifetime) | Array   | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| [`scripts`](./Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. | 1 | `{ . . . }` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| `size_end` | Number | The size (scalar or 2D vector) of the effect at the end of its animation. | 1 | `.1`<br>`.2`<br>`.3` |
| [`size_start`](./Arrays.md#array-size_start) | Array   | The starting size of particles. | 1 | `.1`<br>`.2`<br>`.3` |
| `speed_scale` | Number | A multiplier for particle speed. | 1 | `.05`<br>`.1`<br>`.2` |
| `speed_start` | Number | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |

</details>


### Object: `GirlDino`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `GirlDinoCry`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `GrenadeExplode`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`self_damage`](./Miscellaneous.md#object-self_damage) | Object  | Defines damage or effects applied to the caster when using the ability. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `Guillotina2Body`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `Guillotina2Head`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `Guillotina3Body`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `Guillotina3Head`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `HCHumanDie`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `Haunt`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `HemBounce`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `Hyde`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| `arm1` | Number | The catalog ID for the cat's first arm part. | 1 | `-1`<br>`-2`<br>`1` |
| `arm2` | Number | The catalog ID for the cat's second arm part. | 1 | `-1`<br>`-2`<br>`1` |
| `body` | Number | The catalog ID for the cat's body part. | 1 | `-1`<br>`1`<br>`1.1` |
| `claws` | Number | The sprite frame index for the character's claws. | 1 | `1`<br>`1032`<br>`2` |
| `default_face` | String | Specifies the default facial expression for the unit's portrait. | 1 | `angry`<br>`happy`<br>`mad` |
| `default_frame` | Number | The default sprite frame used for the character's portrait or body. | 1 | `1`<br>`1000`<br>`1001` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `head` | Number | The catalog ID for the cat's head part. | 1 | `-1`<br>`1`<br>`1.3` |
| `leftear` | Number | The sprite frame index for the character's left ear. | 1 | `1`<br>`1000`<br>`1001` |
| `lefteye` | Number | The sprite frame index for the character's left eye. | 1 | `1`<br>`100`<br>`1001` |
| `lefteyebrow` | Number | The sprite frame index for the character's left eyebrow. | 1 | `1`<br>`1000`<br>`1001` |
| `leg1` | Number | The catalog ID for the cat's first leg part. | 1 | `-1`<br>`-2`<br>`1` |
| `leg2` | Number | The catalog ID for the cat's second leg part. | 1 | `-1`<br>`1`<br>`10` |
| `mouth` | Number | The catalog ID for the cat's mouth part. | 1 | `-1`<br>`-2`<br>`1` |
| `palette` | Number | Specifies the color palette index for the ability's visuals. | 1 | `-1`<br>`0`<br>`1` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `pitch` | Number | The sound pitch multiplier for the character's voice or sounds. | 1 | `.3`<br>`.5`<br>`.6` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| `rightear` | Number | The sprite frame index for the character's right ear. | 1 | `1000`<br>`1001`<br>`1004` |
| `righteye` | Number | The sprite frame index for the character's right eye. | 1 | `1`<br>`100`<br>`1001` |
| `righteyebrow` | Number | The sprite frame index for the character's right eyebrow. | 1 | `1`<br>`1000`<br>`1001` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| `tail` | Number | The catalog ID for the cat's tail part. | 1 | `-1`<br>`1000`<br>`1001` |
| `texture` | Number | The catalog ID for the cat's texture. | 1 | `-1`<br>`1`<br>`1000` |
| `voice` | String | Determines which voice set or type is used for the character. | 1 | `ankylosaurus`<br>`female1`<br>`female10` |

</details>


### Object: `IDSprout`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`spawn`](./Miscellaneous.md#object-spawn) | Object  | Defines what object or unit is spawned when the ability is used. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `Lava_Distortion`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha` | Number | The alpha transparency value for the particle system (e.g., '0.03'). | 1 | `.005`<br>`.01`<br>`.03` |
| `alpha_end` | Number | The alpha (opacity) value at the end of the effect's duration or animation. | 1 | `.2`<br>`.5`<br>`0` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| [`emit_box`](./Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| [`emit_direction`](./Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_rate` | Number | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0`<br>`1`<br>`10` |
| [`live_bounds`](./Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| `material` | String | The material shader name used for rendering the visual effect. | 1 | `distorter`<br>`mist` |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`particle_lifetime`](./Arrays.md#array-particle_lifetime) | Array   | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| `render_layer` | String | The render layer on which the effect is drawn (e.g., background, top). | 1 | `background`<br>`sorted_distortions`<br>`splatters` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| [`rotation`](./Arrays.md#array-rotation) | Array  | The rotation of the effect, specified as a single value or a random range [min, max] in degrees. | 1 | `-90`<br>`90`<br>`[-10 10]` |
| `rotation_speed_end` | Number | The rotation speed (in degrees per second) of the effect at the end of its animation. | 1 | `0` |
| [`scripts`](./Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. | 1 | `{ . . . }` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| `size_end` | Number | The size (scalar or 2D vector) of the effect at the end of its animation. | 1 | `.1`<br>`.2`<br>`.3` |
| `size_start` | Number | The starting size of particles. | 1 | `.1`<br>`.2`<br>`.3` |
| [`speed_start`](./Arrays.md#array-speed_start) | Array   | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |

</details>


### Object: `LennyCatDies`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Specifies the class that this ability belongs to, used for categorization and restrictions. | 1 | `AOESpellAbility`<br>`BounceDashAbility`<br>`Butcher` |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`self_damage`](./Miscellaneous.md#object-self_damage) | Object  | Defines damage or effects applied to the caster when using the ability. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `Maggot`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `ManglerEnrage`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `ManglerMonsterDashAttack`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `ManglersMonster`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `MechExplode`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`self_damage`](./Miscellaneous.md#object-self_damage) | Object  | Defines damage or effects applied to the caster when using the ability. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `MegaFart`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `MegaGuppy_SummonTheChild`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`spawn`](./Miscellaneous.md#object-spawn) | Object  | Defines what object or unit is spawned when the ability is used. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `MockingbirdForm`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`tags`](./Arrays.md#array-tags) | Array  | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `MoonHead_KillHands`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `MoveOne`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `Necro_SoulDagger_Uncharged`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |

</details>


### Object: `NoHead`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| `claws` | Number | The sprite frame index for the character's claws. | 1 | `1`<br>`1032`<br>`2` |
| `default_frame` | Number | The default sprite frame used for the character's portrait or body. | 1 | `1`<br>`1000`<br>`1001` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `head` | Number | The catalog ID for the cat's head part. | 1 | `-1`<br>`1`<br>`1.3` |
| `leftear` | Number | The sprite frame index for the character's left ear. | 1 | `1`<br>`1000`<br>`1001` |
| `lefteye` | Number | The sprite frame index for the character's left eye. | 1 | `1`<br>`100`<br>`1001` |
| `lefteyebrow` | Number | The sprite frame index for the character's left eyebrow. | 1 | `1`<br>`1000`<br>`1001` |
| `mouth` | Number | The catalog ID for the cat's mouth part. | 1 | `-1`<br>`-2`<br>`1` |
| `palette` | Number | Specifies the color palette index for the ability's visuals. | 1 | `-1`<br>`0`<br>`1` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `pitch` | Number | The sound pitch multiplier for the character's voice or sounds. | 1 | `.3`<br>`.5`<br>`.6` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| `rightear` | Number | The sprite frame index for the character's right ear. | 1 | `1000`<br>`1001`<br>`1004` |
| `righteye` | Number | The sprite frame index for the character's right eye. | 1 | `1`<br>`100`<br>`1001` |
| `righteyebrow` | Number | The sprite frame index for the character's right eyebrow. | 1 | `1`<br>`1000`<br>`1001` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| `texture` | Number | The catalog ID for the cat's texture. | 1 | `-1`<br>`1`<br>`1000` |
| `voice` | String | Determines which voice set or type is used for the character. | 1 | `ankylosaurus`<br>`female1`<br>`female10` |

</details>


### Object: `NonChampionFlySwarm`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `NubbyToss`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `Nubs`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `NubsGoop`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `Ornstein`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `Paper`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. | 1 | `3` |

</details>


### Object: `PassiveEnergized`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| [`emit_box`](./Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| [`emit_direction`](./Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_radius` | Number | The radius from which particles or effects are emitted. | 1 | `.05`<br>`.1`<br>`.2` |
| `emit_rate` | Number | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0`<br>`1`<br>`10` |
| [`friction`](./Arrays.md#array-friction) | Array  | A scalar or 3D vector multiplier for velocity reduction applied over time. | 1 | `.1`<br>`.2`<br>`.5` |
| [`live_bounds`](./Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `particle_lifetime` | Number | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| [`rotation`](./Arrays.md#array-rotation) | Array  | The rotation of the effect, specified as a single value or a random range [min, max] in degrees. | 1 | `-90`<br>`90`<br>`[-10 10]` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| [`size`](./Arrays.md#array-size) | Array  | The scale factor (size multiplier) of the spawned unit. | 1 | `.2`<br>`.5`<br>`1` |
| `size_in` | Number | The size of the effect at the beginning of its intro animation. | 1 | `.1`<br>`.3`<br>`.5` |
| [`speed_start`](./Arrays.md#array-speed_start) | Array   | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |
| `unlit` | Boolean | If true, the effect is not affected by scene lighting. | 1 | `true` |

</details>


### Object: `PassiveTar`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_in` | Number | The alpha (opacity) value at the start of the effect's intro animation. | 1 | `.01`<br>`.05`<br>`.1` |
| `alpha_out` | Number | The alpha (opacity) value at the end of the effect's outro animation. | 1 | `.2`<br>`.3`<br>`.5` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| [`emit_box`](./Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| [`emit_direction`](./Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_radius` | Number | The radius from which particles or effects are emitted. | 1 | `.05`<br>`.1`<br>`.2` |
| `emit_rate` | Number | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| [`force_end`](./Arrays.md#array-force_end) | Array   | The final force applied to particles over time, as a scalar or 3D vector. | 1 | `200`<br>`500`<br>`[0 -1 0]` |
| [`force_start`](./Arrays.md#array-force_start) | Array   | The initial force applied to particles, as a scalar or 3D vector. | 1 | `0`<br>`[0 -10 0]`<br>`[0 -20 0]` |
| [`live_bounds`](./Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| [`particle_lifetime`](./Arrays.md#array-particle_lifetime) | Array   | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| `rotation` | Number | The rotation of the effect, specified as a single value or a random range [min, max] in degrees. | 1 | `-90`<br>`90`<br>`[-10 10]` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| `size` | Number | The scale factor (size multiplier) of the spawned unit. | 1 | `.2`<br>`.5`<br>`1` |
| `size_in` | Number | The size of the effect at the beginning of its intro animation. | 1 | `.1`<br>`.3`<br>`.5` |
| `speed_start` | Number | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |
| `spurt` | String | The name of the spurt particle effect to play. | 1 | `GibsBloodSpurt`<br>`GibsBloodSpurtHuge`<br>`PassiveTarSplat` |

</details>


### Object: `PlayerCat_ThiefShade2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `RatKing`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `ReaperRevenge`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`self_damage`](./Miscellaneous.md#object-self_damage) | Object  | Defines damage or effects applied to the caster when using the ability. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `SandStormBuff`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_end` | Number | The alpha (opacity) value at the end of the effect's duration or animation. | 1 | `.2`<br>`.5`<br>`0` |
| `alpha_start` | Number | The alpha (opacity) value at the start of the effect's duration or animation. | 1 | `-1`<br>`.5`<br>`.8` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| [`emit_box`](./Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| [`emit_direction`](./Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_rate` | Number | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0`<br>`1`<br>`10` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `false`<br>`true` |
| [`live_bounds`](./Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `ownership` | String | The ownership scope for the effect, such as local to the caster. | 1 | `local`<br>`local*/` |
| [`particle_lifetime`](./Arrays.md#array-particle_lifetime) | Array   | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| [`scripts`](./Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. | 1 | `{ . . . }` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| `size_end` | Number | The size (scalar or 2D vector) of the effect at the end of its animation. | 1 | `.1`<br>`.2`<br>`.3` |
| [`size_start`](./Arrays.md#array-size_start) | Array   | The starting size of particles. | 1 | `.1`<br>`.2`<br>`.3` |
| `speed_scale` | Number | A multiplier for particle speed. | 1 | `.05`<br>`.1`<br>`.2` |
| `speed_start` | Number | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |

</details>


### Object: `Shadowstep`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `ShineBuff`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_end` | Number | The alpha (opacity) value at the end of the effect's duration or animation. | 1 | `.2`<br>`.5`<br>`0` |
| `alpha_start` | Number | The alpha (opacity) value at the start of the effect's duration or animation. | 1 | `-1`<br>`.5`<br>`.8` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| [`emit_box`](./Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| [`emit_direction`](./Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_rate` | Number | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0`<br>`1`<br>`10` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `false`<br>`true` |
| [`live_bounds`](./Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `ownership` | String | The ownership scope for the effect, such as local to the caster. | 1 | `local`<br>`local*/` |
| `particle_lifetime` | Number | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| [`scripts`](./Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. | 1 | `{ . . . }` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| `size_end` | Number | The size (scalar or 2D vector) of the effect at the end of its animation. | 1 | `.1`<br>`.2`<br>`.3` |
| `size_start` | Number | The starting size of particles. | 1 | `.1`<br>`.2`<br>`.3` |
| `speed_scale` | Number | A multiplier for particle speed. | 1 | `.05`<br>`.1`<br>`.2` |
| `speed_start` | Number | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |

</details>


### Object: `Shove`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `SleepDart`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `durability` | Number | The amount of durability consumed by this ability or required for its use. | 1 | `0`<br>`1`<br>`10` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |

</details>


### Object: `SleepDart2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Specifies the ability to be used or triggered when the parent condition is met. | 1 | `AZ_LoseHead`<br>`AlienBeam`<br>`AlienBeastGoop` |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `durability` | Number | The amount of durability consumed by this ability or required for its use. | 1 | `0`<br>`1`<br>`10` |
| `frame` | Number | The sprite frame index to display. | 1 | `1`<br>`10`<br>`100` |
| `kind` | String | Specifies the item category (e.g., face, weapon, neck, trinket, modifier). | 1 | `face`<br>`head`<br>`modifier` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |

</details>


### Object: `SmokeBuff`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_end` | Number | The alpha (opacity) value at the end of the effect's duration or animation. | 1 | `.2`<br>`.5`<br>`0` |
| `alpha_start` | Number | The alpha (opacity) value at the start of the effect's duration or animation. | 1 | `-1`<br>`.5`<br>`.8` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| [`emit_box`](./Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| [`emit_direction`](./Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_rate` | Number | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0`<br>`1`<br>`10` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `false`<br>`true` |
| [`live_bounds`](./Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `ownership` | String | The ownership scope for the effect, such as local to the caster. | 1 | `local`<br>`local*/` |
| [`particle_lifetime`](./Arrays.md#array-particle_lifetime) | Array   | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| [`scripts`](./Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. | 1 | `{ . . . }` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| `size_end` | Number | The size (scalar or 2D vector) of the effect at the end of its animation. | 1 | `.1`<br>`.2`<br>`.3` |
| [`size_start`](./Arrays.md#array-size_start) | Array   | The starting size of particles. | 1 | `.1`<br>`.2`<br>`.3` |
| `speed_scale` | Number | A multiplier for particle speed. | 1 | `.05`<br>`.1`<br>`.2` |
| `speed_start` | Number | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |

</details>


### Object: `Smough`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `SparkleBuff`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_end` | Number | The alpha (opacity) value at the end of the effect's duration or animation. | 1 | `.2`<br>`.5`<br>`0` |
| `alpha_start` | Number | The alpha (opacity) value at the start of the effect's duration or animation. | 1 | `-1`<br>`.5`<br>`.8` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| [`emit_box`](./Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| [`emit_direction`](./Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_rate` | Number | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0`<br>`1`<br>`10` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `false`<br>`true` |
| [`live_bounds`](./Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `ownership` | String | The ownership scope for the effect, such as local to the caster. | 1 | `local`<br>`local*/` |
| [`particle_lifetime`](./Arrays.md#array-particle_lifetime) | Array   | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| [`scripts`](./Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. | 1 | `{ . . . }` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| `size_end` | Number | The size (scalar or 2D vector) of the effect at the end of its animation. | 1 | `.1`<br>`.2`<br>`.3` |
| [`size_start`](./Arrays.md#array-size_start) | Array   | The starting size of particles. | 1 | `.1`<br>`.2`<br>`.3` |
| `speed_scale` | Number | A multiplier for particle speed. | 1 | `.05`<br>`.1`<br>`.2` |
| `speed_start` | Number | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |

</details>


### Object: `SpiderReturn`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `SpikeBuff`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_end` | Number | The alpha (opacity) value at the end of the effect's duration or animation. | 1 | `.2`<br>`.5`<br>`0` |
| `alpha_start` | Number | The alpha (opacity) value at the start of the effect's duration or animation. | 1 | `-1`<br>`.5`<br>`.8` |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| [`emit_box`](./Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| [`emit_direction`](./Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| `emit_rate` | Number | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0`<br>`1`<br>`10` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `false`<br>`true` |
| [`live_bounds`](./Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `ownership` | String | The ownership scope for the effect, such as local to the caster. | 1 | `local`<br>`local*/` |
| `particle_lifetime` | Number | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| [`scripts`](./Miscellaneous.md#object-scripts) | Object  | An object containing particle system scripts like forces or collisions. | 1 | `{ . . . }` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| `size_end` | Number | The size (scalar or 2D vector) of the effect at the end of its animation. | 1 | `.1`<br>`.2`<br>`.3` |
| `size_start` | Number | The starting size of particles. | 1 | `.1`<br>`.2`<br>`.3` |
| `speed_scale` | Number | A multiplier for particle speed. | 1 | `.05`<br>`.1`<br>`.2` |
| `speed_start` | Number | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |

</details>


### Object: `Spook`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `TC_DashReaction`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai_ability` | String | Specifies the ability to use as the AI's behavior for this ability. | 1 | `AZ_Jump_AI`<br>`BasicBigMelee`<br>`BasicMelee` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |
| [`temporary_effects`](./Miscellaneous.md#object-temporary_effects) | Object  | Applies temporary status effects on the caster upon using the ability. | 1 | `{ . . . }` |

</details>


### Object: `TT_Thrash`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `TVOff`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `TattersFear`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `TheCreator_SpawnCloneTeam`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`spawn`](./Miscellaneous.md#object-spawn) | Object  | Defines what object or unit is spawned when the ability is used. | 1 | `{ . . . }` |
| [`tags`](./Arrays.md#array-tags) | Array  | A list of tags that categorize the ability (e.g., weapon_throw, musical, consumable). | 1 | `[cant_be_simulcast]`<br>`[cat robot]`<br>`[consumable shapeshift]` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `ThornUp`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `ThornUpX`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `ThrobbingKing2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `ToadJump_BasicMove`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `TormentorRuneAbsorb`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `ToxPuff`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `ToxicBubbles`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `emit_amount` | Number | The number of particles emitted per burst. | 1 | `1`<br>`10`<br>`100` |
| [`emit_box`](./Arrays.md#array-emit_box) | Array   | The spatial bounds (min x, max x, min y, max y, min z, max z) for particle emission. | 1 | `[-.02 .02 .1 0 -.02 .02]`<br>`[-.03 .03 .1 0 -.03 .03]`<br>`[-.1 .1 .2 .2 -.1 .1]` |
| [`emit_direction`](./Arrays.md#array-emit_direction) | Array   | The initial direction vector for emitted particles. | 1 | `[-.4, -.4, 0]`<br>`[-.5, -1, 0]`<br>`[.1, -1, .1]` |
| [`emit_rate`](./Arrays.md#array-emit_rate) | Array   | The rate of particle emission per second. | 1 | `.5`<br>`1`<br>`10` |
| `emit_spread` | Number | The angle spread for particle emission direction. | 1 | `0`<br>`1`<br>`10` |
| `face_moving_direction` | Boolean | If true, particles rotate to face their movement direction. | 1 | `false`<br>`true` |
| [`live_bounds`](./Arrays.md#array-live_bounds) | Array   | The bounds within which particles can exist. | 1 | `[-.2 10 0 10 -.2 10]`<br>`[-0.5 999  -999 999 -0.5 999]`<br>`[-999 999  -999 999 -999 999]` |
| `movieclip` | String | Specifies the visual movie clip or sprite asset used for the object. | 1 | `AcidOoze`<br>`AcidRainParticle`<br>`AcidRainSplashParticle` |
| `particle_lifetime` | Number | The duration in seconds particles remain alive. | 1 | `.`<br>`.025`<br>`.35` |
| `projection_matrix` | String | The projection matrix mode for particle rendering (e.g., 'default'). | 1 | `default` |
| `render_mode` | String | The rendering mode for particles (e.g., 'default', 'separate'). | 1 | `default`<br>`separate` |
| `simulation_space` | String | The coordinate space for particle simulation ('local' or 'global'). | 1 | `global`<br>`local` |
| [`size_start`](./Arrays.md#array-size_start) | Array   | The starting size of particles. | 1 | `.1`<br>`.2`<br>`.3` |
| `speed_start` | Number | The initial speed of particles. | 1 | `-2`<br>`.001`<br>`.1` |

</details>


### Object: `TrexSwitchTarget`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `UFO_BigExplode`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `UltraSmough`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`ai`](./Miscellaneous.md#object-ai) | Object  | A container object defining the character's artificial intelligence brain and decision weights. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |

</details>


### Object: `Wood`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Specifies the localized description string for the item or ability. | 1 | `""`<br>`"ABIITY_FRIENDORFOE2_DESC"`<br>`"ABIITY_FRIENDORFOE_DESC"` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| `pieces_required` | Number | The number of scrap pieces required to craft this item. | 1 | `3` |

</details>


### Object: `cWaggle`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `cWaggle2x2`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](./Miscellaneous.md#object-abilities) | Object  | A container object defining a character's move, attack, and spell abilities. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`passives`](./Passives_and_Statuses.md#object-passives) | Object  | A container object listing passive effects granted to the unit. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `cWaggle3x3`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`properties`](./Miscellaneous.md#object-properties) | Object  | A container object defining a character's base attributes, tags, faction, health, movement, and other core properties. | 1 | `{ . . . }` |
| [`stats`](./Passives_and_Statuses.md#object-stats) | Object  | A container object defining a character's primary statistics (strength, dexterity, constitution, intelligence, speed, etc.). | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `face_EatNeverstone`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bonus_passives`](./Miscellaneous.md#object-bonus_passives) | Object  | Grants temporary passive abilities to the caster for the duration of the ability. | 1 | `{ . . . }` |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `face_LeechBrood`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `neck_NukeBonus`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bonus_passives`](./Miscellaneous.md#object-bonus_passives) | Object  | Grants temporary passive abilities to the caster for the duration of the ability. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`meta`](./Shops.md#object-meta) | Object  | Contains metadata for the ability including name, description, class, and type icon. | 1 | `{ . . . }` |
| `sub_ability` | String | Specifies a sub-ability that is part of this ability, often used for multi-part abilities. | 1 | `CollectiveCounterImpl`<br>`CollectiveSpinImpl`<br>`HomingBlasts2_sub` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `neck_NukeExplode`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bonus_passives`](./Miscellaneous.md#object-bonus_passives) | Object  | Grants temporary passive abilities to the caster for the duration of the ability. | 1 | `{ . . . }` |
| [`cost`](./Miscellaneous.md#object-cost) | Object  | Defines the resource cost (e.g., mana) and other casting requirements. | 1 | `{ . . . }` |
| [`damage_instance`](./Miscellaneous.md#object-damage_instance) | Object  | Defines damage properties, effects, and healing for the ability's direct damage. | 1 | `{ . . . }` |
| [`graphics`](./Miscellaneous.md#object-graphics) | Object  | An object defining visual aspects of the ability, such as animation, particle, projectile, and other graphical effects. | 1 | `{ . . . }` |
| [`self_damage`](./Miscellaneous.md#object-self_damage) | Object  | Defines damage or effects applied to the caster when using the ability. | 1 | `{ . . . }` |
| [`splash_damage`](./Miscellaneous.md#object-splash_damage) | Object  | Defines additional damage or effects applied to nearby targets around the primary target. | 1 | `{ . . . }` |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `template` | String | Specifies the gameplay template of the ability (e.g., lobbed_attack, swap, ranged_attack). | 1 | `dash_attack`<br>`jump_attack`<br>`jump_move` |

</details>


### Object: `pyrophina`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BOSS_PYROPHINA_QUOTE_1` | String | Localization key for the first boss quote for Pyrophina. | 1 ||
| `BOSS_PYROPHINA_QUOTE_2` | String | Localization key for the second boss quote for Pyrophina. | 1 ||
| `act` | Number | The act number (game progression stage) in which this encounter or script takes place. | 1 | `1`<br>`2`<br>`3` |
| `arrival_unlock` | String | The name of the cutscene or event that is unlocked upon arrival. | 1 | `npc_houseboss_intro_guillotina_1`<br>`npc_houseboss_intro_guillotina_2`<br>`npc_houseboss_intro_guillotina_3` |
| `frame_label` | String | Specifies the frame or cutscene animation label for the boss encounter. | 1 | `AlienBeast`<br>`ColorlessCat_Tutorial`<br>`DrMangler` |
| `index` | Number | The index used to order or identify this encounter within its list. | 1 | `1`<br>`2`<br>`3` |
| [`initial_cooldown`](./Arrays.md#array-initial_cooldown) | Array   | A list of possible initial cooldown values (in turns) before the encounter can trigger. | 1 | `[0]`<br>`[3 7]` |
| `initial_cutscene_day` | String | The name of the cutscene that plays on the first day the encounter appears. | 1 | `kaiju_fight`<br>`moonboss_intro`<br>`pyro_intro` |
| `lead_time` | Number | The number of turns before the event activates. | 1 | `7` |
| `level` | String | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| `music` | String | Specifies the name of the music track to play during the encounter. | 1 | `alley`<br>`guillotina`<br>`hitler3` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `quotes` | Array | An array of dialogue quotes for the boss cutscene. | 1 | `[` |
| [`rematch_cooldown`](./Arrays.md#array-rematch_cooldown) | Array   | The minimum and maximum number of days before a rematch becomes available. | 1 | `[3 7]` |
| `rematch_cutscene_day` | String | Specifies the cutscene to play on the day of the rematch. | 1 | `house_boss_returns_kaijufight`<br>`house_boss_returns_pyro`<br>`house_boss_returns_zara` |
| `savefile_string` | String | A unique string identifier used to track the save file associated with this encounter. | 1 | `"SAVE_FILE_FIGHT_HOUSEBOSS_GUILLOTINA_1"`<br>`"SAVE_FILE_FIGHT_HOUSEBOSS_GUILLOTINA_2"`<br>`"SAVE_FILE_FIGHT_HOUSEBOSS_GUILLOTINA_3"` |

</details>


### Object: `set_WitchJump`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`target`](./Miscellaneous.md#object-target) | Object  | Defines targeting parameters like range, AoE, restrictions, and multihit behavior. | 1 | `{ . . . }` |
| `variant_of` | String | Indicates this ability is a variant of another named ability, inheriting its properties. | 1 | `Absorb`<br>`AbsorbSoul`<br>`Adoubement` |

</details>


### Object: `zaratana`


<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BOSS_ZARATANA_QUOTE_1` | String | A string for the first quote spoken by the boss Zara Tana. | 1 ||
| `BOSS_ZARATANA_QUOTE_2` | String | A string for the second quote spoken by the boss Zara Tana. | 1 ||
| `act` | Number | The act number (game progression stage) in which this encounter or script takes place. | 1 | `1`<br>`2`<br>`3` |
| `arrival_unlock` | String | The name of the cutscene or event that is unlocked upon arrival. | 1 | `npc_houseboss_intro_guillotina_1`<br>`npc_houseboss_intro_guillotina_2`<br>`npc_houseboss_intro_guillotina_3` |
| `frame_label` | String | Specifies the frame or cutscene animation label for the boss encounter. | 1 | `AlienBeast`<br>`ColorlessCat_Tutorial`<br>`DrMangler` |
| `index` | Number | The index used to order or identify this encounter within its list. | 1 | `1`<br>`2`<br>`3` |
| [`initial_cooldown`](./Arrays.md#array-initial_cooldown) | Array   | A list of possible initial cooldown values (in turns) before the encounter can trigger. | 1 | `[0]`<br>`[3 7]` |
| `initial_cutscene_day` | String | The name of the cutscene that plays on the first day the encounter appears. | 1 | `kaiju_fight`<br>`moonboss_intro`<br>`pyro_intro` |
| `lead_time` | Number | The number of turns before the event activates. | 1 | `7` |
| `level` | String | The level or quest identifier to load. | 1 | `"house_bosses/guillotina1.lvl"`<br>`"house_bosses/guillotina2.lvl"`<br>`"house_bosses/guillotina3.lvl"` |
| `music` | String | Specifies the name of the music track to play during the encounter. | 1 | `alley`<br>`guillotina`<br>`hitler3` |
| `name` | String | Specifies the localized name string for the entity, item, or ability. | 1 | `""`<br>`"2x2 Static Cactus"`<br>`"ABIITY_FRIENDORFOE_NAME"` |
| `quotes` | Array | An array of dialogue quotes for the boss cutscene. | 1 | `[` |
| [`rematch_cooldown`](./Arrays.md#array-rematch_cooldown) | Array   | The minimum and maximum number of days before a rematch becomes available. | 1 | `[3 7]` |
| `rematch_cutscene_day` | String | Specifies the cutscene to play on the day of the rematch. | 1 | `house_boss_returns_kaijufight`<br>`house_boss_returns_pyro`<br>`house_boss_returns_zara` |
| `savefile_string` | String | A unique string identifier used to track the save file associated with this encounter. | 1 | `"SAVE_FILE_FIGHT_HOUSEBOSS_GUILLOTINA_1"`<br>`"SAVE_FILE_FIGHT_HOUSEBOSS_GUILLOTINA_2"`<br>`"SAVE_FILE_FIGHT_HOUSEBOSS_GUILLOTINA_3"` |

</details>