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
| [`passives`](Cat_Mutations.md#object-passives) | Object | Examples: `{ ... }` | 5118 ||
| [`class`](./Enums.md#enum-class) | Enum | Categorizes the ability for specific UI filters. | 1200 ||
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specific entity tag required. | 981 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Core block defining the AI behavior logic and weights. | 928 ||
| `int` | Enum / Integer | `aux` | 401 ||
| [`neck`](./Enums.md#enum-neck) | Enum | `AngelicAura`, `AngelicAura_Terminator`, `DruidNeck`, `DruidNeck_Terminator`, `MageCollar` | 378 ||
| `lck` | Enum / Integer | `aux` | 351 ||
| [`bonus_passives`](Abilities_and_Spells.md#object-bonus_passives) | Object | Passives granted to the character while this ability is equipped. | 272 ||
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | Injects a status effect payload that applies whenever the character performs a basic attack. | 178 ||
| [`Colorless`](Engine_LogicKeys.md#object-colorless) | Object | Applies or references the 'Colorless' effect/state. | 140 ||
| `consumable` | Boolean | `true` | 140 ||
| [`move`](./Arrays.md#array-move) | Enum | `BasicJump`, `BungaJumpMove`, `DefaultMove`, `DoNothing`, `DustMove` | 122 ||
| [`FormChanger`](Characters_and_Bosses.md#object-formchanger) | Object | AI Role: Designates the character as one that frequently shifts forms. | 106 ||
| [`SpawnOnDeath`](Characters_and_Bosses.md#object-spawnondeath) | Enum / Object | Event Trigger: Spawns a specific entity when killed. | 81 ||
| `IgnoreSelf` | Boolean / Integer | Applies or references the 'IgnoreSelf' effect/state. | 75 ||
| [`Tinkerer`](Engine_LogicKeys.md#object-tinkerer) | Object | Applies or references the 'Tinkerer' effect/state. | 70 ||
| [`Hunter`](Engine_LogicKeys.md#object-hunter) | Object | Applies or references the 'Hunter' effect/state. | 68 ||
| [`Fear`](./Arrays.md#array-fear) | Array / Integer | Applies or references the 'Fear' effect/state. | 59 ||
| [`Medic`](Engine_LogicKeys.md#object-medic) | Object | Applies or references the 'Medic' effect/state. | 58 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 54 ||
| [`RandomArmorPickup`](Engine_LogicKeys.md#object-randomarmorpickup) | Number / Object | Applies or references the 'RandomArmorPickup' effect/state. | 43 ||
| [`BasicMelee`](#object-basicmelee) | Object || 42 ||
| [`StatusImmunity`](./Enums.md#enum-statusimmunity) | Array / Enum | Applies or references the 'StatusImmunity' effect/state. | 38 ||
| [`Wood`](#object-wood) | Variable || 38 ||
| `CritChanceUp` | Integer | Applies or references the 'CritChanceUp' effect/state. | 36 ||
| `HealthGain` | Integer | Applies or references the 'HealthGain' effect/state. | 36 ||
| `Thorns` | Integer | Applies or references the 'Thorns' effect/state. | 36 ||
| [`FormChangeWhileHasStatus`](Characters_and_Bosses.md#object-formchangewhilehasstatus) | Object | Logic: Changes form automatically while possessing a specific status. | 35 ||
| [`StatusOnTookDamage`](Cat_Mutations.md#object-statusontookdamage) | Object | Event Trigger: Applies nested statuses when took damage. | 34 ||
| [`AddElementsToBasicAttack`](./Enums.md#enum-addelementstobasicattack) | Enum | Examples: `Ice, Electric, Water` | 32 ||
| [`Jester`](./Arrays.md#array-jester) | Array | Examples: `[ CAT_VS_BOSS_QUOTES_JESTER_1 CAT_VS_BOSS_QUOTES_JESTER_2..., [ CAT_RETURN_EA...` | 32 ||
| [`MulticlassLevelUp`](./Enums.md#enum-multiclasslevelup) | Enum | Applies the 'MulticlassLevelUp' effect. | 32 ||
| [`AddPassivesToMinions`](Items_and_Equipment.md#object-addpassivestominions) | Object | Applies the 'AddPassivesToMinions' effect. | 30 ||
| `Charge` | Integer | Applies or references the 'Charge' effect/state. | 30 ||
| `DodgeChance` | Integer | Examples: `2, 5, 10` | 30 ||
| [`EliteTint`](./Arrays.md#array-elitetint) | Array | Examples: `[ .4 .4 .4 ], [ .6 .6 .6 .50 ], red` | 30 ||
| [`RevengeDamage`](Abilities_and_Spells.md#object-revengedamage) | Object | Reaction trigger: Deals damage to the attacker when hit. | 30 ||
| `AddCritMultiplier` | Integer | Applies the 'AddCritMultiplier' effect. | 28 ||
| [`TransformAbility`](./Enums.md#enum-transformability) | Enum | Applies or references the 'TransformAbility' effect/state. | 28 ||
| `knockback` | Enum / Integer | The base physics pushing power (in tiles). | 27 ||
| `AddBonusRange` | Integer | Applies or references the 'AddBonusRange' effect/state. | 26 ||
| `HealthRegenUp` | Integer | Applies or references the 'HealthRegenUp' effect/state. | 26 ||
| [`ImmediateAbilityReaction`](Characters_and_Bosses.md#object-immediateabilityreaction) | Array / Enum / Object | Reaction: Executes an ability instantly, interrupting the current sequence. | 26 ||
| `Knockback` | Integer | Applies or references the 'Knockback' effect/state. | 26 ||
| [`Paper`](#object-paper) | Variable || 26 ||
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. | 25 ||
| `Undead` | Integer | Applies or references the 'Undead' effect/state. | 25 ||
| `Brittle` | Integer | Applies or references the 'Brittle' effect/state. | 24 ||
| `MissChance` | Integer | Applies the 'MissChance' effect. | 24 ||
| [`party_status_next_fight`](Events_and_Encounters.md#object-party_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. | 24 ||
| [`PassiveWhenAffectedByElement`](Cat_Mutations.md#object-passivewhenaffectedbyelement) | Object | Examples: `{ ... }` | 24 ||
| [`SpawnOnBattleStart`](Elite_Buffs.md#object-spawnonbattlestart) | Enum / Object | Applies or references the 'SpawnOnBattleStart' effect/state. | 24 ||
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 23 ||
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer | Applies or references the 'DivineShield' effect/state. | 22 ||
| [`mode`](./Enums.md#enum-mode) | Enum | `equal`, `greater`, `greater_or_equal`, `less_or_equal`, `yeet` | 22 ||
| [`StatusOnBreak`](Items_and_Equipment.md#object-statusonbreak) | Object | Event Trigger: Applies statuses when this action occurs. | 22 ||
| [`threshold`](Items_and_Equipment.md#object-threshold) | Enum / Integer / Object | Examples: `4*champion_multiplier, 3*champion_multiplier, 1` | 22 ||
| [`additional_passives`](Abilities_and_Spells.md#object-additional_passives) | Object | Passives granted intrinsically to a spawned entity. | 20 ||
| [`BossRewards`](Characters_and_Bosses.md#object-bossrewards) | Object | Loot logic: Rewards dropped upon defeating a boss. | 20 ||
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object | Applies or references the 'Brace' effect/state. | 20 ||
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object | Applies or references the 'ForceUseAbility' effect/state. | 20 ||
| [`MeleeRevengeDamage`](Abilities_and_Spells.md#object-meleerevengedamage) | Object | Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack. | 20 ||
| [`EliteParticle`](./Enums.md#enum-eliteparticle) | Enum | Examples: `SpikeBuff, Lava_Distortion, SparkleBuff` | 19 ||
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object | Generates an item drop from the specified loot pool. | 19 ||
| [`BirdRewards`](Characters_and_Bosses.md#object-birdrewards) | Object | Loot logic: Rewards dropped by bird-type enemies. | 18 ||
| [`Buddy`](Characters_and_Bosses.md#object-buddy) | Enum / Object | Character Form / AI State: Behavior and stats for the 'Buddy' familiar state. | 18 ||
| [`Coin`](Engine_LogicKeys.md#object-coin) | Integer / Object | Applies or references the 'Coin' effect/state. | 18 ||
| [`Consumed`](Abilities_and_Spells.md#object-consumed) | Object | State object triggered when this object or entity is eaten/consumed by another character. | 18 ||
| [`SpawnThingOnDamage`](Cat_Mutations.md#object-spawnthingondamage) | Object | Applies or references the 'SpawnThingOnDamage' effect/state. | 18 ||
| [`StatusOnKill`](Cat_Mutations.md#object-statusonkill) | Object | Event Trigger: Applies statuses when this action occurs. | 18 ||
| [`AbilityOnBattleStart_Immediate`](./Enums.md#enum-abilityonbattlestart_immediate) | Enum | Applies or references the 'AbilityOnBattleStart_Immediate' effect/state. | 17 ||
| `CollectsPickups` | Integer | Applies or references the 'CollectsPickups' effect/state. | 17 ||
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 17 ||
| `LuckUp` | Enum / Integer | Applies or references the 'LuckUp' effect/state. | 17 ||
| [`OverrideKnockbackDamage`](./Enums.md#enum-overrideknockbackdamage) | Enum / Integer | Applies or references the 'OverrideKnockbackDamage' effect/state. | 17 ||
| [`RandomMagicMissile`](Abilities_and_Spells.md#object-randommagicmissile) | Integer / Object | Fires a randomized number of magic missiles. | 17 ||
| `rat` | Variable || 17 ||
| [`AddStatusToBasicMeleeAttack`](Cat_Mutations.md#object-addstatustobasicmeleeattack) | Object | Examples: `{ ... }` | 16 ||
| [`CharacterLightSource`](Characters_and_Bosses.md#object-characterlightsource) | Object | Visual: Attaches a dynamic lighting source to the character. | 16 ||
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum | Applies or references the 'ElementImmune' effect/state. | 16 ||
| [`HealthPickup`](Characters_and_Bosses.md#object-healthpickup) | Object | Pickup Logic: Defines what happens when a health item is collected. | 16 ||
| `less_or_equal` | Variable || 16 ||
| `PassiveLevelUpAtCombatEnd` | Integer | Applies the 'PassiveLevelUpAtCombatEnd' effect. | 16 ||
| [`pyrophina`](#object-pyrophina) | Variable || 16 ||
| [`StatusEachTurnBegin`](Cat_Mutations.md#object-statuseachturnbegin) | Object | Event Trigger: Applies nested statuses to each turn begin. | 16 ||
| [`StatusEachTurnEnd`](Cat_Mutations.md#object-statuseachturnend) | Object | Applies or references the 'StatusEachTurnEnd' effect/state. | 16 ||
| [`zaratana`](#object-zaratana) | Variable || 16 ||
| [`ApplyToSourceOnKill`](Abilities_and_Spells.md#object-applytosourceonkill) | Object | Conditional redirect: Applies the nested effects to the caster, but only if the target was killed by the action. | 15 ||
| [`CanApplyToInanimate`](Abilities_and_Spells.md#object-canapplytoinanimate) | Object | Modifier object that allows its nested effects to target inanimate objects (like rocks or furniture) instead of just characters. | 15 ||
| `HealthMultiplier` | Float | Examples: `1.5, .5, .8` | 15 ||
| [`Maggot`](#object-maggot) | Object || 15 ||
| [`ReplaceSpawnedObjects`](./Arrays.md#array-replacespawnedobjects) | Array | Applies or references the 'ReplaceSpawnedObjects' effect/state. | 15 ||
| [`ChangeCatClass`](./Enums.md#enum-changecatclass) | Enum | Applies or references the 'ChangeCatClass' effect/state. | 14 ||
| `EndTurn` | Integer | Applies or references the 'EndTurn' effect/state. | 14 ||
| `meat` | Variable || 14 ||
| [`PassiveGroup`](Characters_and_Bosses.md#object-passivegroup) | Object | Passive: A collection of passives grouped together for easier management. | 14 ||
| [`SpawnOnDowned`](./Enums.md#enum-spawnondowned) | Enum | Examples: `CharmedKitten, CharmedFly` | 14 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 14 ||
| [`statuses`](Characters_and_Bosses.md#object-statuses) | Object | Status effects possessed by the character. | 14 ||
| [`Trample`](./Arrays.md#array-trample) | Integer | Applies or references the 'Trample' effect/state. | 14 ||
| [`TransformBasicAttack`](./Enums.md#enum-transformbasicattack) | Enum | Applies or references the 'TransformBasicAttack' effect/state. | 14 ||
| [`ApplyPassives`](Abilities_and_Spells.md#object-applypassives) | Object | Grants the nested passive abilities dynamically. | 13 ||
| [`DeathRattleRevive`](Characters_and_Bosses.md#object-deathrattlerevive) | Enum / Object | Event Trigger: Revives the character immediately upon death. | 13 ||
| `Flammable` | Integer | Applies or references the 'Flammable' effect/state. | 13 ||
| `SafeDoomed` | Enum / Integer | Applies or references the 'SafeDoomed' effect/state. | 13 ||
| [`TransformOnDeath`](./Enums.md#enum-transformondeath) | Array / Enum | Applies or references the 'TransformOnDeath' effect/state. | 13 ||
| `AddBonusMeleeRange` | Integer | Applies the 'AddBonusMeleeRange' effect. | 12 ||
| `AddCorpseHealth` | Integer | Applies the 'AddCorpseHealth' effect. | 12 ||
| `AddMaxHealth` | Integer | Applies or references the 'AddMaxHealth' effect/state. | 12 ||
| [`Bionic`](#object-bionic) | Variable || 12 ||
| [`BonusAbility`](./Enums.md#enum-bonusability) | Enum | Applies the 'BonusAbility' effect. | 12 ||
| [`CritsApplyStatus`](Items_and_Equipment.md#object-critsapplystatus) | Object | Applies the 'CritsApplyStatus' effect. | 12 ||
| [`DeadAltAbility`](./Enums.md#enum-deadaltability) | Enum | Applies or references the 'DeadAltAbility' effect/state. | 12 ||
| `Displace` | Integer | Applies or references the 'Displace' effect/state. | 12 ||
| [`elements`](./Arrays.md#array-elements) | Array | Array of elemental tags to apply (e.g., `[Fire Holy]`). | 12 ||
| [`EquipTemporaryItem`](./Enums.md#enum-equiptemporaryitem) | Enum | Applies the 'EquipTemporaryItem' effect. | 12 ||
| `IgnoreTiles` | Integer | Applies or references the 'IgnoreTiles' effect/state. | 12 ||
| `NoHealthOnlyShield` | Integer | Applies or references the 'NoHealthOnlyShield' effect/state. | 12 ||
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object | Spawns a specific character or entity upon impact. | 12 ||
| [`SpawnEachTurn`](Cat_Mutations.md#object-spawneachturn) | Object | Applies or references the 'SpawnEachTurn' effect/state. | 12 ||
| [`ChanceToBreakFree`](Abilities_and_Spells.md#object-chancetobreakfree) | Object | Provides a probability to escape a grapple or restraining effect. | 11 ||
| [`DoScreenShake`](Abilities_and_Spells.md#object-doscreenshake) | Integer / Object | Triggers a camera screen shake effect. | 11 ||
| [`EliteFlatTint`](./Arrays.md#array-eliteflattint) | Array | Examples: `[ 1.1 1.1 1.1 ], [ 1.1 1.1 1.3 ], [ 1.1 1.1 1 ]` | 11 ||
| [`Food`](Engine_LogicKeys.md#object-food) | Integer / Object | Applies or references the 'Food' effect/state. | 11 ||
| `PermanentMadness` | Integer | Applies or references the 'PermanentMadness' effect/state. | 11 ||
| [`BoostWeaponDamage`](Items_and_Equipment.md#object-boostweapondamage) | Object | Applies the 'BoostWeaponDamage' effect. | 10 ||
| [`BrambleRandomTileEvent`](#object-bramblerandomtileevent) | Object || 10 ||
| `CoinPickup` | Integer | Applies or references the 'CoinPickup' effect/state. | 10 ||
| `ExtraMovePoints` | Integer | Applies the 'ExtraMovePoints' effect. | 10 ||
| `FadeInsteadOfDie` | Integer | Applies or references the 'FadeInsteadOfDie' effect/state. | 10 ||
| [`GainCoins`](./Arrays.md#array-gaincoins) | Array / Integer | Applies or references the 'GainCoins' effect/state. | 10 ||
| `KnockbackDamageImmuneUntilSettled` | Integer | Applies or references the 'KnockbackDamageImmuneUntilSettled' effect/state. | 10 ||
| `PartialPurge` | Integer | Applies or references the 'PartialPurge' effect/state. | 10 ||
| [`PassiveAtStatThreshold`](Items_and_Equipment.md#object-passiveatstatthreshold) | Object | Applies the 'PassiveAtStatThreshold' effect. | 10 ||
| [`Quivered`](./Arrays.md#array-quivered) | Array / Integer | Applies or references the 'Quivered' effect/state. | 10 ||
| `RandomPermanentStat` | Integer | Applies or references the 'RandomPermanentStat' effect/state. | 10 ||
| [`ReplaceBasicMove`](./Enums.md#enum-replacebasicmove) | Enum | Applies or references the 'ReplaceBasicMove' effect/state. | 10 ||
| [`SpawnOnBattleStartRandomEmptyTile`](Cat_Mutations.md#object-spawnonbattlestartrandomemptytile) | Object | Applies or references the 'SpawnOnBattleStartRandomEmptyTile' effect/state. | 10 ||
| [`StatusOnCrit`](Miscellaneous.md#object-statusoncrit) | Object | Event Trigger: Applies nested statuses when crit. | 10 ||
| `StripStatuses` | Integer | Applies or references the 'StripStatuses' effect/state. | 10 ||
| `WaterWalk` | Integer | Applies or references the 'WaterWalk' effect/state. | 10 ||
| `Ammo` | Integer | Applies or references the 'Ammo' effect/state. | 9 ||
| [`Bleed`](./Arrays.md#array-bleed) | Array / Integer | Applies or references the 'Bleed' effect/state. | 9 ||
| `Creep` | Variable || 9 ||
| `DeferVaporize` | Integer | Applies or references the 'DeferVaporize' effect/state. | 9 ||
| `DiminishingHealthRegen` | Integer | Applies or references the 'DiminishingHealthRegen' effect/state. | 9 ||
| [`FormChangeOnElementInfluence`](Characters_and_Bosses.md#object-formchangeonelementinfluence) | Object | Logic: Changes form when affected by an element. | 9 ||
| `Plant` | Integer | Applies or references the 'Plant' effect/state. | 9 ||
| `RandomMutation` | Integer | Applies or references the 'RandomMutation' effect/state. | 9 ||
| [`Rot`](./Arrays.md#array-rot) | Array / Integer | Applies or references the 'Rot' effect/state. | 9 ||
| [`SmallRockBehavior`](Characters_and_Bosses.md#object-smallrockbehavior) | Integer / Object | AI Logic: Movement/interaction profile for small rocks. | 9 ||
| `SpawnCreep` | Integer | Applies or references the 'SpawnCreep' effect/state. | 9 ||
| `SpellDamageUp` | Integer | Applies or references the 'SpellDamageUp' effect/state. | 9 ||
| [`StatusCollector`](Characters_and_Bosses.md#object-statuscollector) | Object | Passive: Gains benefits based on the number of statuses applied to them. | 9 ||
| [`TransformInXTurns`](Characters_and_Bosses.md#object-transforminxturns) | Object | Logic: Forces a form change after X turns. | 9 ||
| [`TransformOnElementInfluence`](Characters_and_Bosses.md#object-transformonelementinfluence) | Object | Logic: Changes form when affected by elements. | 9 ||
| `AddKnockbackDamage` | Integer | Applies or references the 'AddKnockbackDamage' effect/state. | 8 ||
| `AddLevelUpRerolls` | Integer | Applies or references the 'AddLevelUpRerolls' effect/state. | 8 ||
| [`AddStatusToWeapons`](Characters_and_Bosses.md#object-addstatustoweapons) | Object | Applies the 'AddStatusToWeapons' effect. | 8 ||
| `AlphaTurns` | Integer | Applies the 'AlphaTurns' effect. | 8 ||
| [`AmplifyStatus`](./Enums.md#enum-amplifystatus) | Enum | Applies the 'AmplifyStatus' effect. | 8 ||
| [`BasicMagicMissile`](#object-basicmagicmissile) | Object || 8 ||
| [`BlacklistPickupType`](./Enums.md#enum-blacklistpickuptype) | Enum | Examples: `food, catnip` | 8 ||
| `BleedThorns` | Integer | Applies or references the 'BleedThorns' effect/state. | 8 ||
| [`CharmedFly`](#object-charmedfly) | Object || 8 ||
| [`DisableAbilitiesWithTag`](./Enums.md#enum-disableabilitieswithtag) | Enum | Examples: `musical, consumable` | 8 ||
| `ExtraWeaponAttacks` | Integer | Applies the 'ExtraWeaponAttacks' effect. | 8 ||
| [`ForceSpecificInjury`](./Enums.md#enum-forcespecificinjury) | Enum | Applies the 'ForceSpecificInjury' effect. | 8 ||
| [`FormChangeOffMap`](Characters_and_Bosses.md#object-formchangeoffmap) | Object | Logic: Changes form when pushed off the map. | 8 ||
| [`Grappled`](./Arrays.md#array-grappled) | Array / Integer | Applies or references the 'Grappled' effect/state. | 8 ||
| [`InnateElement`](./Enums.md#enum-innateelement) | Enum | Applies the 'InnateElement' effect. | 8 ||
| `Lucky` | Enum | data/boss_elite_buffs.gon, data/elite_buffs.gon | 8 ||
| [`ManaCostReductionTagged`](Miscellaneous.md#object-manacostreductiontagged) | Object | Applies the 'ManaCostReductionTagged' effect. | 8 ||
| `NonStackingDivineShield` | Integer | Applies or references the 'NonStackingDivineShield' effect/state. | 8 ||
| `NonStackingShield` | Integer | Examples: `12, 4, 8` | 8 ||
| [`PassiveIfAllArmorEmpty`](Miscellaneous.md#object-passiveifallarmorempty) | Object | Applies the 'PassiveIfAllArmorEmpty' effect. | 8 ||
| [`PassiveIfEmptyFace`](Miscellaneous.md#object-passiveifemptyface) | Object | Applies the 'PassiveIfEmptyFace' effect. | 8 ||
| [`PassiveIfEmptyHead`](Miscellaneous.md#object-passiveifemptyhead) | Object | Applies the 'PassiveIfEmptyHead' effect. | 8 ||
| [`PassiveIfEmptyNeck`](Miscellaneous.md#object-passiveifemptyneck) | Object | Applies the 'PassiveIfEmptyNeck' effect. | 8 ||
| [`Poison`](./Arrays.md#array-poison) | Array / Integer | Applies or references the 'Poison' effect/state. | 8 ||
| [`RandomizeAIWeightsEachTurn`](./Arrays.md#array-randomizeaiweightseachturn) | Array | Applies or references the 'RandomizeAIWeightsEachTurn' effect/state. | 8 ||
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | Selects and applies a random status effect from the provided nested object. | 8 ||
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum | Applies or references the 'ReplaceBasicAttack' effect/state. | 8 ||
| [`StatusAlliesOnDeath`](Items_and_Equipment.md#object-statusalliesondeath) | Object | Event Trigger: Applies nested statuses to allies on death. | 8 ||
| [`StatusEachRoundBegin`](Elite_Buffs.md#object-statuseachroundbegin) | Object | Examples: `{ ... }` | 8 ||
| [`StatusEveryXSpellCasts`](Cat_Mutations.md#object-statuseveryxspellcasts) | Object | Applies or references the 'StatusEveryXSpellCasts' effect/state. | 8 ||
| [`StatusOnCastSpell`](Cat_Mutations.md#object-statusoncastspell) | Object | Event Trigger: Applies nested statuses when cast spell. | 8 ||
| [`StatusOnUseAbilityWithTag`](Miscellaneous.md#object-statusonuseabilitywithtag) | Object | Event Trigger: Applies nested statuses when use ability with tag. | 8 ||
| `AbilityEnabledOncePerFightAtHealthThreshold` | Integer | Applies or references the 'AbilityEnabledOncePerFightAtHealthThreshold' effect/state. | 7 ||
| [`AbilityWhenBuddyDies`](./Enums.md#enum-abilitywhenbuddydies) | Enum | Applies or references the 'AbilityWhenBuddyDies' effect/state. | 7 ||
| `BramblesOnHit` | Integer | Applies or references the 'BramblesOnHit' effect/state. | 7 ||
| [`BrittleDuringElement`](./Enums.md#enum-brittleduringelement) | Enum | Applies or references the 'BrittleDuringElement' effect/state. | 7 ||
| [`ChanceToSpitOnDamage`](Characters_and_Bosses.md#object-chancetospitondamage) | Object | Reaction: Probability to use a spit counter-attack when damaged. | 7 ||
| `CharismaUp` | Enum / Integer | Applies or references the 'CharismaUp' effect/state. | 7 ||
| `ContextualHeal` | Integer | Applies or references the 'ContextualHeal' effect/state. | 7 ||
| [`DamageNeighborsOnEndMove`](Miscellaneous.md#object-damageneighborsonendmove) | Object | Combat Trigger: Deals damage to neighbors on end move. | 7 ||
| [`DurabilityTransform`](Items_and_Equipment.md#object-durabilitytransform) | Object | Applies or references the 'DurabilityTransform' effect/state. | 7 ||
| [`GainCoinsRange`](Abilities_and_Spells.md#object-gaincoinsrange) | Object | Grants the player a randomized amount of coins within a min/max range. | 7 ||
| [`Ice`](Engine_LogicKeys.md#object-ice) | Object | Examples: `{ ... }` | 7 ||
| `ManaSteal` | Integer | Applies or references the 'ManaSteal' effect/state. | 7 ||
| `MinimumKnockbackFromAllDamage` | Integer | Applies or references the 'MinimumKnockbackFromAllDamage' effect/state. | 7 ||
| [`OverrideBasicAttack`](./Enums.md#enum-overridebasicattack) | Enum | Applies or references the 'OverrideBasicAttack' effect/state. | 7 ||
| `OverrideMaxHealth` | Integer | Applies or references the 'OverrideMaxHealth' effect/state. | 7 ||
| [`PassiveIfStrAuxEquals`](Items_and_Equipment.md#object-passiveifstrauxequals) | Object | Applies or references the 'PassiveIfStrAuxEquals' effect/state. | 7 ||
| [`PassiveWhenOnTile`](Items_and_Equipment.md#object-passivewhenontile) | Object | State Trigger: Grants passives when this condition is met. | 7 ||
| [`SetFragileImmune`](./Enums.md#enum-setfragileimmune) | String | Applies or references the 'SetFragileImmune' effect/state. | 7 ||
| [`TriggerWerewolfTransform`](./Arrays.md#array-triggerwerewolftransform) | Array / Number | Applies or references the 'TriggerWerewolfTransform' effect/state. | 7 ||
| [`Webbed`](./Arrays.md#array-webbed) | Integer | Applies or references the 'Webbed' effect/state. | 7 ||
| `XIsFreeArmorSlots` | Integer | Applies or references the 'XIsFreeArmorSlots' effect/state. | 7 ||
| `AbilityEnabledPercentEachTurn` | Integer | Applies or references the 'AbilityEnabledPercentEachTurn' effect/state. | 6 ||
| [`AbilityOnBattleStart`](./Enums.md#enum-abilityonbattlestart) | Enum | Applies or references the 'AbilityOnBattleStart' effect/state. | 6 ||
| `AddDamage` | Integer | Applies or references the 'AddDamage' effect/state. | 6 ||
| [`AddDamageToElementDamage`](Cat_Mutations.md#object-adddamagetoelementdamage) | Object | Applies or references the 'AddDamageToElementDamage' effect/state. | 6 ||
| `AddMovement` | Integer | Applies or references the 'AddMovement' effect/state. | 6 ||
| [`AddStatusToElementAbilities`](Miscellaneous.md#object-addstatustoelementabilities) | Object | Applies the 'AddStatusToElementAbilities' effect. | 6 ||
| [`AddTemporaryEffectsToBasicAttack`](Cat_Mutations.md#object-addtemporaryeffectstobasicattack) | Object | Applies the 'AddTemporaryEffectsToBasicAttack' effect. | 6 ||
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | Enum / Integer | ``, `Big`, `BigHolding`, `BigHoldingCat`, `Bishop` | 6 ||
| `BackstabImmunity` | Integer | Applies or references the 'BackstabImmunity' effect/state. | 6 ||
| `BasicAttackAOEBonus` | Integer | Applies the 'BasicAttackAOEBonus' effect. | 6 ||
| `BasicAttackDamageMultiplier` | Integer | Applies the 'BasicAttackDamageMultiplier' effect. | 6 ||
| [`Bird`](Passives_and_Statuses.md#object-bird) | Enum / Object | Applies or references the 'Bird' effect/state. | 6 ||
| `BlastResistance` | Integer | Applies the 'BlastResistance' effect. | 6 ||
| [`BounceRock`](./Enums.md#enum-bouncerock) | Array / Enum | Applies or references the 'BounceRock' effect/state. | 6 ||
| [`CaveFamilyEnrage`](Characters_and_Bosses.md#object-cavefamilyenrage) | Object | AI Trigger: Enrage logic triggered when a cave family member is killed. | 6 ||
| `ClearStarving` | Integer | Applies or references the 'ClearStarving' effect/state. | 6 ||
| [`Conditional_BadRoll`](Abilities_and_Spells.md#object-conditional_badroll) | Object | Conditional trigger: Executes nested logic based on a randomized bad outcome probability. | 6 ||
| [`CureDisease`](#object-curedisease) | Object | Applies the 'CureDisease' effect. | 6 ||
| `DamageUp` | Integer / String | Applies or references the 'DamageUp' effect/state. | 6 ||
| [`DefaultMove`](#object-defaultmove) | Object || 6 ||
| [`DelayedAutoRevive`](Characters_and_Bosses.md#object-delayedautorevive) | Object | Applies or references the 'DelayedAutoRevive' effect/state. | 6 ||
| [`Divide4OnDeath`](./Enums.md#enum-divide4ondeath) | Enum | Applies or references the 'Divide4OnDeath' effect/state. | 6 ||
| [`DoDistortionRing`](Abilities_and_Spells.md#object-dodistortionring) | Object | Creates a visual distortion ring effect on the screen. | 6 ||
| [`Electric`](Engine_LogicKeys.md#object-electric) | Object | Examples: `{ ... }` | 6 ||
| `ExtraBasicAttacks` | Integer | Applies the 'ExtraBasicAttacks' effect. | 6 ||
| [`Fire`](Characters_and_Bosses.md#object-fire) | Integer / Object | Character Form: Behavior and stats for the 'Fire' state. | 6 ||
| [`FormChangeWhilePrimingAbility`](Characters_and_Bosses.md#object-formchangewhileprimingability) | Object | Logic: Changes form while preparing/priming a specific ability. | 6 ||
| `Fragile` | Integer | Applies or references the 'Fragile' effect/state. | 6 ||
| `FreeFirstCast` | Integer | Applies or references the 'FreeFirstCast' effect/state. | 6 ||
| [`FreePathfindElement`](./Enums.md#enum-freepathfindelement) | Enum | Applies the 'FreePathfindElement' effect. | 6 ||
| [`Hyde`](#object-hyde) | Object || 6 ||
| [`ItemAuxTransform`](Items_and_Equipment.md#object-itemauxtransform) | Object | Applies or references the 'ItemAuxTransform' effect/state. | 6 ||
| `KaijuKnockbackImmune` | Integer | Applies or references the 'KaijuKnockbackImmune' effect/state. | 6 ||
| `KineticSpikes` | Integer | Applies or references the 'KineticSpikes' effect/state. | 6 ||
| `KnockbackImmunity` | Integer | Applies the 'KnockbackImmunity' effect. | 6 ||
| [`MoveQuivered`](./Arrays.md#array-movequivered) | Integer | Applies or references the 'MoveQuivered' effect/state. | 6 ||
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | Enum / Integer | ``, `Alert`, `Angry`, `Belly`, `Button` | 6 ||
| [`PassiveWhenAtFullMana`](Cat_Mutations.md#object-passivewhenatfullmana) | Object | State Trigger: Grants nested passives when at full mana. | 6 ||
| `PermanentConstitution` | Integer | Applies or references the 'PermanentConstitution' effect/state. | 6 ||
| `PoisonThorns` | Integer | Applies or references the 'PoisonThorns' effect/state. | 6 ||
| [`ReplaceBasicAttackWhenCastable`](./Enums.md#enum-replacebasicattackwhencastable) | Enum | Applies the 'ReplaceBasicAttackWhenCastable' effect. | 6 ||
| [`ReplaceBasicMove_Mutation`](./Enums.md#enum-replacebasicmove_mutation) | Enum | Examples: `BasicJump, BasicDig` | 6 ||
| [`ScatterCoins`](Abilities_and_Spells.md#object-scattercoins) | Object | Throws coins out into the level randomly. | 6 ||
| [`ScatterHeldCoin`](./Arrays.md#array-scatterheldcoin) | Array / Integer | Applies or references the 'ScatterHeldCoin' effect/state. | 6 ||
| [`SetBrittleImmune`](./Enums.md#enum-setbrittleimmune) | String | Applies or references the 'SetBrittleImmune' effect/state. | 6 ||
| `SetDistanceDisplace` | Integer | Applies or references the 'SetDistanceDisplace' effect/state. | 6 ||
| `ShowHiddenThings` | Integer | Examples: `1` | 6 ||
| [`StatusIfUnusedMovePoints`](Cat_Mutations.md#object-statusifunusedmovepoints) | Object | Event Trigger: Applies nested statuses to if unused move points. | 6 ||
| [`StatusKilledCharacters`](Cat_Mutations.md#object-statuskilledcharacters) | Object | Event Trigger: Applies nested statuses to killed characters. | 6 ||
| [`StatusOnBattleEnd`](Abilities_and_Spells.md#object-statusonbattleend) | Object | Applies the nested status effects when the encounter finishes. | 6 ||
| [`StatusOnEndMove`](Cat_Mutations.md#object-statusonendmove) | Object | Event Trigger: Applies statuses when this action occurs. | 6 ||
| [`StatusOnStanceSwitch`](Miscellaneous.md#object-statusonstanceswitch) | Object | Event Trigger: Applies nested statuses when stance switch. | 6 ||
| [`StatusOnTookDamageFromAbility`](Cat_Mutations.md#object-statusontookdamagefromability) | Object | Event Trigger: Applies statuses when taking damage from an ability. | 6 ||
| [`StunImmunity`](Characters_and_Bosses.md#object-stunimmunity) | Integer / Object | Passive: Prevents Stun from being applied. | 6 ||
| [`TagGreed`](./Enums.md#enum-taggreed) | Enum | Applies or references the 'TagGreed' effect/state. | 6 ||
| [`TeamCastAbility`](Abilities_and_Spells.md#object-teamcastability) | Enum / Object | Requires or involves multiple characters to execute the ability. | 6 ||
| [`TwisterDisplaceWithDamage`](Abilities_and_Spells.md#object-twisterdisplacewithdamage) | Object | A whirlwind effect that randomly displaces targets and deals damage. | 6 ||
| [`YOffset`](./Enums.md#enum-yoffset) | Float | Applies or references the 'YOffset' effect/state. | 6 ||
| `ally_chance` | Integer | Examples: `15, 100` | 5 ||
| `Angel` | Integer | Applies or references the 'Angel' effect/state. | 5 ||
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum | Applies or references the 'ChangeTilesUnder' effect/state. | 5 ||
| [`CollectsPickupsWithAltEffects`](Abilities_and_Spells.md#object-collectspickupswithalteffects) | Object | Triggers alternative nested effects when collecting items or pickups. | 5 ||
| `DamageOrHealConditionally` | Integer | Applies or references the 'DamageOrHealConditionally' effect/state. | 5 ||
| `fetus` | Variable || 5 ||
| [`FlySwarm`](#object-flyswarm) | Object | Examples: `50` | 5 ||
| [`FlySwarm`](#object-flyswarm) | Object || 5 | `50` (Number), `{ ... }` (Object) |
| `HeadArmorPassiveMultiplierBonus` | Integer | Applies or references the 'HeadArmorPassiveMultiplierBonus' effect/state. | 5 ||
| `HitExplosion` | Integer | Applies or references the 'HitExplosion' effect/state. | 5 ||
| `KnockbackDirectionIsFacingDirection` | Enum / Integer | Applies or references the 'KnockbackDirectionIsFacingDirection' effect/state. | 5 ||
| `MonkStanceSwitch` | Integer | Applies or references the 'MonkStanceSwitch' effect/state. | 5 ||
| [`MoveTowardsKillers`](Characters_and_Bosses.md#object-movetowardskillers) | Enum / Object | AI Movement: Seeks out entities that have recently killed an ally. | 5 ||
| `NoHealthRegen` | Number | Applies or references the 'NoHealthRegen' effect/state. | 5 ||
| [`ObjectOnHit`](Abilities_and_Spells.md#object-objectonhit) | Enum / Object | Spawns a specific physics/item object upon impact. | 5 ||
| [`ObjectOnHitEmpty`](./Enums.md#enum-objectonhitempty) | Enum | Applies or references the 'ObjectOnHitEmpty' effect/state. | 5 ||
| `RefreshMovePointsIfHit` | Integer | Applies or references the 'RefreshMovePointsIfHit' effect/state. | 5 ||
| `RepairTrinket` | Integer | Applies or references the 'RepairTrinket' effect/state. | 5 ||
| `SharkySmellsBlood` | Integer | Applies or references the 'SharkySmellsBlood' effect/state. | 5 ||
| [`SpawnCoinAnywhere`](./Arrays.md#array-spawncoinanywhere) | Array / Integer | Applies or references the 'SpawnCoinAnywhere' effect/state. | 5 ||
| [`SpawnRock`](./Arrays.md#array-spawnrock) | Array / Integer | Applies or references the 'SpawnRock' effect/state. | 5 ||
| `StartOffMap` | Integer | Applies or references the 'StartOffMap' effect/state. | 5 ||
| [`StatusGroup`](Abilities_and_Spells.md#object-statusgroup) | Object | Groups multiple status effects together for batch application. | 5 ||
| [`StatusOnTurnEndIfDidntCastAbilityTypes`](Items_and_Equipment.md#object-statusonturnendifdidntcastabilitytypes) | Object | Event Trigger: Applies statuses when this action occurs. | 5 ||
| [`Tangled`](Abilities_and_Spells.md#object-tangled) | Array / Integer / Object | Applies a tangled/ensnared status effect, often modifying visual sprites. | 5 ||
| [`TransformItemOnElementInfluence`](Items_and_Equipment.md#object-transformitemonelementinfluence) | Object | Applies or references the 'TransformItemOnElementInfluence' effect/state. | 5 ||
| [`TransformOnDeathImmediately`](Characters_and_Bosses.md#object-transformondeathimmediately) | Enum / Object | Logic: Bypasses death sequence to instantly assume a new form. | 5 ||
| `UpgradeRandomAbility` | Integer | Applies or references the 'UpgradeRandomAbility' effect/state. | 5 ||
| [`water`](Characters_and_Bosses.md#object-water) | Variable || 5 ||
| [`Water`](Characters_and_Bosses.md#object-water) | Object | Character Form: Behavior and stats for the \'Water\' state. | 5 ||
| [`XIsLivingAlliesWithTag`](./Enums.md#enum-xislivingallieswithtag) | Enum | Applies or references the 'XIsLivingAlliesWithTag' effect/state. | 5 ||
| [`AbilityAfterEnemyCastSpell_Stackable`](./Enums.md#enum-abilityafterenemycastspell_stackable) | Enum | Applies or references the 'AbilityAfterEnemyCastSpell_Stackable' effect/state. | 4 |  |
| [`AbilityReaction`](Characters_and_Bosses.md#object-abilityreaction) | Enum / Object | AI Trigger: Executes an ability in reaction to a specific event (e.g., taking damage). | 4 ||
| [`AbilityWhenTaggedCharacterMovesNear`](Cat_Mutations.md#object-abilitywhentaggedcharactermovesnear) | Object | AI Trigger: Executes an ability when a character with a specific tag moves adjacent. | 4 ||
| `AddDamageToBasicAttack` | String | Applies the 'AddDamageToBasicAttack' effect. | 4 ||
| `AddManaRegen` | Integer | Applies or references the 'AddManaRegen' effect/state. | 4 ||
| `AddMeleeKnockback` | Integer | Applies or references the 'AddMeleeKnockback' effect/state. | 4 ||
| [`AddPassivesToCharmed`](Items_and_Equipment.md#object-addpassivestocharmed) | Object | Applies the 'AddPassivesToCharmed' effect. | 4 ||
| [`AddSelfStatusToBasicAttack`](Items_and_Equipment.md#object-addselfstatustobasicattack) | Object | Applies or references the 'AddSelfStatusToBasicAttack' effect/state. | 4 ||
| `AddSpeed` | Integer | Applies the 'AddSpeed' effect. | 4 ||
| [`AddStatusToAllDamage`](Items_and_Equipment.md#object-addstatustoalldamage) | Object | Modifier: Injects a status effect into a specific action. | 4 ||
| [`AddStatusToAllDamageAbilities`](Miscellaneous.md#object-addstatustoalldamageabilities) | Object | Applies the 'AddStatusToAllDamageAbilities' effect. | 4 ||
| [`AddStatusToElementDamage`](Items_and_Equipment.md#object-addstatustoelementdamage) | Object | Applies the 'AddStatusToElementDamage' effect. | 4 ||
| `AllyDamageReduction` | Integer | Applies the 'AllyDamageReduction' effect. | 4 ||
| [`AllyManaRegenAura`](Miscellaneous.md#object-allymanaregenaura) | Object | Applies the 'AllyManaRegenAura' effect. | 4 ||
| `AmplifyKnockback` | Integer | Applies the 'AmplifyKnockback' effect. | 4 ||
| `any` | Variable || 4 ||
| `AOEPuddle` | Enum || 4 | `X-1` (Enum) |
| [`ApplyToConsumed`](Abilities_and_Spells.md#object-applytoconsumed) | Object | Redirects the nested effects to apply to the entity that just consumed this object. | 4 ||
| [`ArcLightning`](Abilities_and_Spells.md#object-arclightning) | Object | Executes a chain-lightning logic block that bounces between targets. | 4 ||
| [`AutocastEachRound`](Abilities_and_Spells.md#object-autocasteachround) | Enum / Object | Forces the character to automatically cast a specific ability at the start of each combat round. | 4 ||
| `BackstabAllDirections` | Integer | Applies or references the 'BackstabAllDirections' effect/state. | 4 ||
| [`BaitAura`](Characters_and_Bosses.md#object-baitaura) | Object | Passive: Projects an aura that attracts specific enemy types (e.g., flies/maggots). | 4 ||
| [`BasicStraightShot`](#object-basicstraightshot) | Object || 4 ||
| [`BasicTankMelee`](#object-basictankmelee) | Object || 4 ||
| [`BeefyCharmedLeech`](#object-beefycharmedleech) | Object || 4 ||
| `BreakAtAux` | Integer | Applies or references the 'BreakAtAux' effect/state. | 4 ||
| [`BuffImmunity`](Items_and_Equipment.md#object-buffimmunity) | Integer / Object | Applies or references the 'BuffImmunity' effect/state. | 4 ||
| `bug` | Variable || 4 ||
| `CatchBoomerang` | Integer | Applies or references the 'CatchBoomerang' effect/state. | 4 ||
| [`ChanceToBackflip`](Cat_Mutations.md#object-chancetobackflip) | Object | Applies or references the 'ChanceToBackflip' effect/state. | 4 ||
| [`ChangeTileOnPop`](./Enums.md#enum-changetileonpop) | Enum | Applies or references the 'ChangeTileOnPop' effect/state. | 4 ||
| [`CharmedTinySpider`](#object-charmedtinyspider) | Object || 4 ||
| [`ClassManaCostReduction`](Cat_Mutations.md#object-classmanacostreduction) | Object | Applies or references the 'ClassManaCostReduction' effect/state. | 4 ||
| [`CobraReflex`](./Enums.md#enum-cobrareflex) | Enum | Applies the 'CobraReflex' effect. | 4 ||
| [`Conditional_PartyMember`](Engine_LogicKeys.md#conditional_partymember) | Object | Conditional constraint. Nested properties only trigger if this is true. | 4 ||
| `ConsumablesInfiniteRange` | Integer | Applies the 'ConsumablesInfiniteRange' effect. | 4 ||
| `CopyBasicAttackEffects` | Integer | Applies or references the 'CopyBasicAttackEffects' effect/state. | 4 ||
| `CountAsCorpse` | Integer | Applies or references the 'CountAsCorpse' effect/state. | 4 ||
| [`CounterAttack`](Cat_Mutations.md#object-counterattack) | Array / Enum / Object | Reaction: Executes a counter-attack ability when hit. | 4 ||
| `CreepTile` | Variable || 4 ||
| `crow` | Variable || 4 ||
| [`DisableAbilities`](./Enums.md#enum-disableabilities) | Enum | Applies or references the 'DisableAbilities' effect/state. | 4 ||
| [`DisplayDangerAOE`](./Enums.md#enum-displaydangeraoe) | Enum | Applies or references the 'DisplayDangerAOE' effect/state. | 4 ||
| [`DistanceBonusDamage`](#object-distancebonusdamage) | Object | Applies the 'DistanceBonusDamage' effect. | 4 ||
| [`DownRankAIIfWeaponUsable`](./Enums.md#enum-downrankaiifweaponusable) | Float | Applies or references the 'DownRankAIIfWeaponUsable' effect/state. | 4 ||
| [`ElementalManaCostReduction`](Items_and_Equipment.md#object-elementalmanacostreduction) | Object | Applies the 'ElementalManaCostReduction' effect. | 4 ||
| [`EnableWeather`](./Enums.md#enum-enableweather) | Enum | Applies or references the 'EnableWeather' effect/state. | 4 ||
| `equal` | Variable || 4 ||
| [`EquipRandomTemporaryItemFromPool`](./Enums.md#enum-equiprandomtemporaryitemfrompool) | Enum | Examples: `pills` | 4 ||
| `ExplosionIfHitSomething` | Integer | Applies or references the 'ExplosionIfHitSomething' effect/state. | 4 ||
| [`extra_statuses`](Abilities_and_Spells.md#object-extra_statuses) | Object | Additional generic status applications. | 4 ||
| `ExtraDispersedTurns` | Integer | Applies or references the 'ExtraDispersedTurns' effect/state. | 4 ||
| `FaceArmorPassiveMultiplierBonus` | Integer | Applies or references the 'FaceArmorPassiveMultiplierBonus' effect/state. | 4 ||
| [`FactionUprising`](./Enums.md#enum-factionuprising) | Enum | Examples: `alien, robot, ghost` | 4 ||
| `Fights` | Number | Applies or references the 'Fights' effect/state. | 4 ||
| [`FragileDuringElement`](./Enums.md#enum-fragileduringelement) | Enum | Applies or references the 'FragileDuringElement' effect/state. | 4 ||
| `FreezePiercing` | Integer | Applies the 'FreezePiercing' effect. | 4 ||
| `GrassTile` | Number | Examples: `80, 15` | 4 ||
| [`GroundFlopper`](./Enums.md#enum-groundflopper) | Enum | Applies or references the 'GroundFlopper' effect/state. | 4 ||
| `HouseFoodRequirementMultiplier` | Integer | Examples: `0` | 4 ||
| `IncreaseExplosionDamage` | Integer | Applies the 'IncreaseExplosionDamage' effect. | 4 ||
| [`LateStatusApplication`](Abilities_and_Spells.md#object-latestatusapplication) | Object | Applies a status effect after all primary damage and effects have fully resolved. | 4 ||
| [`LevelUpClassOverride`](./Enums.md#enum-levelupclassoverride) | Enum | Applies the 'LevelUpClassOverride' effect. | 4 ||
| [`LoopingSoundWhileAlive`](./Enums.md#enum-loopingsoundwhilealive) | Enum | Applies or references the 'LoopingSoundWhileAlive' effect/state. | 4 ||
| [`LowerAmbientLight`](Abilities_and_Spells.md#object-lowerambientlight) | Object | A visual effect that dims the map's lighting. | 4 ||
| [`LowerAmbientLight`](Abilities_and_Spells.md#object-lowerambientlight) | Object | A visual effect that dims the map's lighting. | 4 ||
| `ManaCostReduction` | Integer | Applies or references the 'ManaCostReduction' effect/state. | 4 ||
| [`Metronome`](Abilities_and_Spells.md#object-metronome) | Integer / Object | Executes a random musical or metronome ability. | 4 ||
| [`Metronome`](Abilities_and_Spells.md#object-metronome) | Boolean (Flag) / Number / Object || 4 | `(Flag)` (Boolean (Flag)), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `musical` | Variable || 4 ||
| `PartialCleanse` | Integer | Applies or references the 'PartialCleanse' effect/state. | 4 ||
| [`PassiveAtHealthThreshold`](Items_and_Equipment.md#object-passiveathealththreshold) | Object | Applies or references the 'PassiveAtHealthThreshold' effect/state. | 4 ||
| [`PassiveWhenDead`](Characters_and_Bosses.md#object-passivewhendead) | Object | State Trigger: Grants passives when this condition is met. | 4 ||
| `PermanentIntelligence` | Integer | Applies or references the 'PermanentIntelligence' effect/state. | 4 ||
| [`PoopWhenHit`](Items_and_Equipment.md#object-poopwhenhit) | Object | Examples: `Poop` | 4 ||
| `PrioritizeFarAwayTargets` | Integer | Applies or references the 'PrioritizeFarAwayTargets' effect/state. | 4 ||
| [`RandomPassivePool`](Characters_and_Bosses.md#object-randompassivepool) | Object | Logic: Grants a random passive from the specified pool upon spawning. | 4 ||
| [`RandomSeededStatModifier`](./Arrays.md#array-randomseededstatmodifier) | Array | Applies or references the 'RandomSeededStatModifier' effect/state. | 4 ||
| [`ReflectProjectiles`](Characters_and_Bosses.md#object-reflectprojectiles) | Integer / Object | Passive: Reflects incoming projectiles back at the attacker. | 4 ||
| `RemoveActPoints` | Integer | Applies or references the 'RemoveActPoints' effect/state. | 4 ||
| [`RepairWeapon`](./Arrays.md#array-repairweapon) | Array / Integer | Applies or references the 'RepairWeapon' effect/state. | 4 ||
| [`ReplaceSpell`](Abilities_and_Spells.md#object-replacespell) | Object | Replaces a spell in the character's hand/deck with a different one. | 4 ||
| `SendRock` | Integer | Applies or references the 'SendRock' effect/state. | 4 ||
| [`SizeScale`](./Enums.md#enum-sizescale) | Number | Applies or references the 'SizeScale' effect/state. | 4 ||
| [`SmartMetronome`](Abilities_and_Spells.md#object-smartmetronome) | Integer / Object | Executes a 'smart' random ability that aims to be beneficial based on context. | 4 ||
| [`SmartMetronome`](Abilities_and_Spells.md#object-smartmetronome) | Integer / Object || 4 | `20` (Number), `{ ... }` (Object) |
| [`SpawnCatCopyOnBattleStart`](Miscellaneous.md#object-spawncatcopyonbattlestart) | Object | Applies the 'SpawnCatCopyOnBattleStart' effect. | 4 ||
| [`SpawnThingOnDeath`](./Enums.md#enum-spawnthingondeath) | Enum | Applies or references the 'SpawnThingOnDeath' effect/state. | 4 ||
| [`StatusOnAllyCatDeath`](Cat_Mutations.md#object-statusonallycatdeath) | Object | Event Trigger: Applies nested statuses when ally cat death. | 4 ||
| [`StatusOnEatFood`](Cat_Mutations.md#object-statusoneatfood) | Object | Event Trigger: Applies nested statuses when eat food. | 4 ||
| [`StatusOnGainCoins`](Characters_and_Bosses.md#object-statusongaincoins) | Object | Event Trigger: Applies nested statuses when gain coins. | 4 ||
| [`StatusOnHealed`](Items_and_Equipment.md#object-statusonhealed) | Object | Event Trigger: Applies nested statuses when healed. | 4 ||
| [`StatusOnOverHealed`](Miscellaneous.md#object-statusonoverhealed) | Object | Event Trigger: Applies nested statuses when over healed. | 4 ||
| [`StatusOnTakeHealthOrShieldDamage`](Items_and_Equipment.md#object-statusontakehealthorshielddamage) | Object | Event Trigger: Applies statuses when this action occurs. | 4 ||
| [`StatusOnTurnEndIfCastNSpells`](Miscellaneous.md#object-statusonturnendifcastnspells) | Object | Event Trigger: Applies nested statuses when turn end if cast n spells. | 4 ||
| [`StatusOnTurnEndIfManaExact`](Miscellaneous.md#object-statusonturnendifmanaexact) | Object | Event Trigger: Applies nested statuses when turn end if mana exact. | 4 ||
| [`StatusOnTurnEndIfManaOrHealthExact`](Miscellaneous.md#object-statusonturnendifmanaorhealthexact) | Object | Event Trigger: Applies nested statuses when turn end if mana or health exact. | 4 ||
| [`StatusRandomEnemiesOnBattleStart`](Events_and_Encounters.md#object-statusrandomenemiesonbattlestart) | Object | Applies or references the 'StatusRandomEnemiesOnBattleStart' effect/state. | 4 ||
| [`SwitchMusic`](Abilities_and_Spells.md#object-switchmusic) | Object | Changes the background music track or layer during combat. | 4 ||
| `TauntAlways` | Integer | Applies the 'TauntAlways' effect. | 4 ||
| [`TempPassiveWhileHasStatus`](Abilities_and_Spells.md#object-temppassivewhilehasstatus) | Object | Grants nested passives only while the character possesses the specified status. | 4 ||
| [`TileTrail`](./Enums.md#enum-tiletrail) | Enum | Applies or references the 'TileTrail' effect/state. | 4 ||
| [`TimeDelayStatusApplication`](Abilities_and_Spells.md#object-timedelaystatusapplication) | Object | Delays the nested effects by a specified amount of real-time seconds. | 4 ||
| [`ToadJump_BasicMove`](#object-toadjump_basicmove) | Object || 4 ||
| [`Trapper`](Characters_and_Bosses.md#object-trapper) | Object | Character Form: Behavior and stats for the 'Trapper' state. | 4 ||
| `UncappedMana` | Integer | Applies the 'UncappedMana' effect. | 4 ||
| `Vegan` | Integer | Examples: `1` | 4 ||
| [`WeremanTransformationReceiver`](./Enums.md#enum-weremantransformationreceiver) | Enum | Applies or references the 'WeremanTransformationReceiver' effect/state. | 4 ||
| `AbilityEnabledOncePerRound` | Integer | Applies or references the 'AbilityEnabledOncePerRound' effect/state. | 3 ||
| [`AbilityEnableIfConsumedCharacterHasTag`](./Enums.md#enum-abilityenableifconsumedcharacterhastag) | Enum | Applies or references the 'AbilityEnableIfConsumedCharacterHasTag' effect/state. | 3 ||
| `AbilityInheritsWeaponEffects` | Integer | Applies or references the 'AbilityInheritsWeaponEffects' effect/state. | 3 ||
| `AddEndOfCombatRegen` | Integer | Applies or references the 'AddEndOfCombatRegen' effect/state. | 3 ||
| `AggroTargetIsCurrentTurn` | Integer | Applies or references the 'AggroTargetIsCurrentTurn' effect/state. | 3 ||
| `AllStatsUpPerDisorder` | Integer | Applies or references the 'AllStatsUpPerDisorder' effect/state. | 3 ||
| [`ApplyMultipleTimes`](Abilities_and_Spells.md#object-applymultipletimes) | Object | A loop object that executes its nested logic multiple times. | 3 ||
| [`BaseStatMultiply`](./Enums.md#enum-basestatmultiply) | Float | Applies or references the 'BaseStatMultiply' effect/state. | 3 ||
| [`BasicAttackCritChance`](./Enums.md#enum-basicattackcritchance) | Float | Applies the 'BasicAttackCritChance' effect. | 3 ||
| `bishop_hat` | Variable || 3 ||
| `BoneArmorPassive` | Integer | Applies or references the 'BoneArmorPassive' effect/state. | 3 ||
| [`BonusTurnPattern`](./Arrays.md#array-bonusturnpattern) | Array | Applies or references the 'BonusTurnPattern' effect/state. | 3 ||
| `Bounty` | Integer | Applies the 'Bounty' effect. | 3 ||
| [`BreakOnElement`](./Enums.md#enum-breakonelement) | Enum | Applies or references the 'BreakOnElement' effect/state. | 3 ||
| [`CanMutateTo`](./Enums.md#enum-canmutateto) | Array / Enum | Applies or references the 'CanMutateTo' effect/state. | 3 ||
| `CantCatchDiseases` | Integer | Applies or references the 'CantCatchDiseases' effect/state. | 3 ||
| `CantSpreadDiseases` | Integer | Applies or references the 'CantSpreadDiseases' effect/state. | 3 ||
| [`CatPartsSizeScaleStatus`](Abilities_and_Spells.md#object-catpartssizescalestatus) | Object | Visually scales specific body parts of a character. | 3 ||
| `ChanceToBlock` | Integer | Applies or references the 'ChanceToBlock' effect/state. | 3 ||
| [`CharmedTinyTumor`](#object-charmedtinytumor) | Object || 3 ||
| [`CollideWithConsumed`](./Math_Equations.md) | Equation | Applies or references the 'CollideWithConsumed' effect/state. | 3 ||
| [`Conditional_Adjacent`](Engine_LogicKeys.md#conditional_adjacent) | Object | Conditional object: Executes nested logic only if the target is/has Adjacent. | 3 ||
| [`Conditional_RandomChance`](Abilities_and_Spells.md#object-conditional_randomchance) | Object | Conditional trigger: Executes nested logic based on a flat percentage random roll. | 3 ||
| [`Conditional_Shielded`](Abilities_and_Spells.md#object-conditional_shielded) | Object | Conditional trigger: Executes nested logic if the target currently has a Shield status. | 3 ||
| [`CookedChickenLeg`](#object-cookedchickenleg) | Object || 3 ||
| `CopyPassiveSlot` | Integer | Applies or references the 'CopyPassiveSlot' effect/state. | 3 ||
| `CorpseVaporizer` | Integer | Applies or references the 'CorpseVaporizer' effect/state. | 3 ||
| [`count`](./Arrays.md#array-count) | Array / Integer | Quantity. | 3 ||
| [`CreateGlobalModifiers`](Abilities_and_Spells.md#object-createglobalmodifiers) | Object | Generates global map or encounter rules/modifiers. | 3 ||
| `DestroyWeapon` | Integer | Applies or references the 'DestroyWeapon' effect/state. | 3 ||
| `DestroyWeaponThrow` | Integer | Applies or references the 'DestroyWeaponThrow' effect/state. | 3 ||
| [`DigestDeadBodies`](./Enums.md#enum-digestdeadbodies) | Enum | Applies or references the 'DigestDeadBodies' effect/state. | 3 ||
| [`DoubleStatus`](./Enums.md#enum-doublestatus) | Enum | Applies or references the 'DoubleStatus' effect/state. | 3 ||
| [`DropAsFamiliarOnArmorBreak`](./Enums.md#enum-dropasfamiliaronarmorbreak) | Enum | Applies or references the 'DropAsFamiliarOnArmorBreak' effect/state. | 3 ||
| [`DustOnHit`](Abilities_and_Spells.md#object-dustonhit) | Object | Spawns a specific particle or cloud object upon impact. | 3 ||
| [`EquipPermanentItem`](./Enums.md#enum-equippermanentitem) | Enum | Applies or references the 'EquipPermanentItem' effect/state. | 3 ||
| `ExtraBasicMoves_Status` | Integer | Applies or references the 'ExtraBasicMoves_Status' effect/state. | 3 ||
| `ForceDisplace` | Integer | Applies or references the 'ForceDisplace' effect/state. | 3 ||
| `ForceMoveTowardsEnemies` | Enum / Integer | Applies or references the 'ForceMoveTowardsEnemies' effect/state. | 3 ||
| [`FormChangeHealthThreshold`](Characters_and_Bosses.md#object-formchangehealththreshold) | Object | Logic: Changes form when health crosses a threshold. | 3 ||
| [`Holy`](Characters_and_Bosses.md#object-holy) | Enum / Object | `MegaGuppy_TransformHoly` | 3 ||
| `IllusionTint` | Integer | Applies or references the 'IllusionTint' effect/state. | 3 ||
| [`IncAuxCounterClamped`](Abilities_and_Spells.md#object-incauxcounterclamped) | Object | Increments a generic auxiliary counter on the character, capped by a maximum value. | 3 ||
| `include_spells` | Boolean | If true, allows the AI to cast spells during this bonus turn. | 3 ||
| `InstantMaxHealthUp` | Integer | Applies or references the 'InstantMaxHealthUp' effect/state. | 3 ||
| [`KnockOutCoin`](Abilities_and_Spells.md#object-knockoutcoin) | Integer / Object | Forces the target to drop coins. | 3 ||
| [`Lava_Distortion`](#object-lava_distortion) | Variable || 3 ||
| `Lifesteal` | Integer | Applies or references the 'Lifesteal' effect/state. | 3 ||
| [`ManaPickup`](Characters_and_Bosses.md#object-manapickup) | Object | Pickup Logic: Defines what happens when a mana item is collected. | 3 ||
| `Meteornado` | Integer | Examples: `1` | 3 ||
| `MimicSpawnerAttacks` | Integer | Applies or references the 'MimicSpawnerAttacks' effect/state. | 3 ||
| `MinimumKnockbackFromPhysicalAttacks` | Integer | Applies or references the 'MinimumKnockbackFromPhysicalAttacks' effect/state. | 3 ||
| `MoonHeadFinisherEnabler` | Integer | Applies or references the 'MoonHeadFinisherEnabler' effect/state. | 3 ||
| [`MoveAndUseAbilityEachTurnBeginIfPossible`](./Enums.md#enum-moveanduseabilityeachturnbeginifpossible) | Enum | Applies the 'MoveAndUseAbilityEachTurnBeginIfPossible' effect. | 3 ||
| `must_do_damage` | Boolean | `true` | 3 ||
| [`MutateViaAbility`](./Enums.md#enum-mutateviaability) | Enum | Applies or references the 'MutateViaAbility' effect/state. | 3 ||
| `NeckArmorPassiveMultiplierBonus` | Integer | Applies or references the 'NeckArmorPassiveMultiplierBonus' effect/state. | 3 ||
| `NextAttackBonusRange` | Integer | Applies or references the 'NextAttackBonusRange' effect/state. | 3 ||
| `PermanentDexterity` | Integer | Applies or references the 'PermanentDexterity' effect/state. | 3 ||
| `PermanentSpeed` | Integer | Applies or references the 'PermanentSpeed' effect/state. | 3 ||
| `Piercing` | Integer | Applies the 'Piercing' effect. | 3 ||
| `PlayBackground` | Integer | Applies or references the 'PlayBackground' effect/state. | 3 ||
| `PrioritizeHitDifferentTargets` | Integer | Applies or references the 'PrioritizeHitDifferentTargets' effect/state. | 3 ||
| `RangeUp` | Integer | Applies or references the 'RangeUp' effect/state. | 3 ||
| `RepairOnKill` | Integer | Applies or references the 'RepairOnKill' effect/state. | 3 ||
| `RockyArmorPassive` | Integer | Applies or references the 'RockyArmorPassive' effect/state. | 3 ||
| `RunInXTurns` | Integer | Applies or references the 'RunInXTurns' effect/state. | 3 ||
| [`SetCrazyEyeBackgroundWeights`](Abilities_and_Spells.md#object-setcrazyeyebackgroundweights) | Object | Adjusts visual rendering weights for the 'Crazy Eye' background effect. | 3 ||
| [`SetDefaultFacePassive`](./Enums.md#enum-setdefaultfacepassive) | Enum | Applies or references the 'SetDefaultFacePassive' effect/state. | 3 ||
| `SharePickupsWithSpawner` | Integer | Applies or references the 'SharePickupsWithSpawner' effect/state. | 3 ||
| `SpawnCreepOnHit` | Integer | Applies or references the 'SpawnCreepOnHit' effect/state. | 3 ||
| [`SpawnCustomTrap`](./Enums.md#enum-spawncustomtrap) | Enum | Applies or references the 'SpawnCustomTrap' effect/state. | 3 ||
| `SpawnNeutralWebTrapOnMiss` | Integer | Applies or references the 'SpawnNeutralWebTrapOnMiss' effect/state. | 3 ||
| [`SpawnVolcanoOnBattleStart`](#object-spawnvolcanoonbattlestart) | Object | Examples: `{ ... }` | 3 ||
| [`StackingFlowerTrail`](Items_and_Equipment.md#object-stackingflowertrail) | Object | Applies or references the 'StackingFlowerTrail' effect/state. | 3 ||
| [`StatusAllCharactersOnSpawn`](House_and_Environment.md#object-statusallcharactersonspawn) | Object | Applies or references the 'StatusAllCharactersOnSpawn' effect/state. | 3 ||
| [`StatusCharactersOnRoundEnd`](#object-statuscharactersonroundend) | Object | Examples: `{ ... }` | 3 ||
| [`SupportFormChangeInsteadOfRun`](Characters_and_Bosses.md#object-supportformchangeinsteadofrun) | Enum / Object | AI Logic: Forces a support unit to transform rather than flee. | 3 ||
| [`tag_filter`](./Enums.md#enum-tag_filter) | Enum | Examples: `crow, grub_familiar` | 3 ||
| [`TakeBonusTurnWithAIControl`](Abilities_and_Spells.md#object-takebonusturnwithaicontrol) | Object | Grants the character an immediate extra turn, but forces the AI to control them during it. | 3 ||
| `TempInitiativeChange` | Integer | Applies or references the 'TempInitiativeChange' effect/state. | 3 ||
| [`ThornUpX`](#object-thornupx) | Object || 3 ||
| [`TileTrail_Ahead`](./Enums.md#enum-tiletrail_ahead) | Enum | Applies or references the 'TileTrail_Ahead' effect/state. | 3 ||
| `TriggerGameEnding` | Integer | Applies or references the 'TriggerGameEnding' effect/state. | 3 ||
| `TrueShot` | Integer | Applies or references the 'TrueShot' effect/state. | 3 ||
| [`TVOff`](#object-tvoff) | Object || 3 ||
| [`UseAbility_NonStack`](./Enums.md#enum-useability_nonstack) | Enum | Applies or references the 'UseAbility_NonStack' effect/state. | 3 ||
| `VaporizeTarget` | Integer | Applies or references the 'VaporizeTarget' effect/state. | 3 ||
| [`XIsMultipliedPercentHealth`](./Arrays.md#array-xismultipliedpercenthealth) | Array | Applies or references the 'XIsMultipliedPercentHealth' effect/state. | 3 ||
| [`AbilityChargeRefundChance`](Miscellaneous.md#object-abilitychargerefundchance) | Object | Applies the 'AbilityChargeRefundChance' effect. | 2 ||
| [`AbilityEnabledIfHasStatus`](./Enums.md#enum-abilityenabledifhasstatus) | Enum | Applies or references the 'AbilityEnabledIfHasStatus' effect/state. | 2 ||
| [`AbilityHealthThreshold`](Characters_and_Bosses.md#object-abilityhealththreshold) | Object | AI Trigger: Executes an ability when health drops below a specific threshold. | 2 ||
| [`AbilityOnRoundEnd`](Characters_and_Bosses.md#object-abilityonroundend) | Object | AI Trigger: Executes an ability at the end of the combat round. | 2 ||
| [`AbsorbBuff`](#object-absorbbuff) | Variable || 2 ||
| `AbsorbManaAura` | Integer | Applies the 'AbsorbManaAura' effect. | 2 ||
| `AddAllyNeighborsToAbilityRange` | Integer | Applies the 'AddAllyNeighborsToAbilityRange' effect. | 2 ||
| `AddChaScalingSpellDamage` | Integer | Applies the 'AddChaScalingSpellDamage' effect. | 2 ||
| [`AddHiddenTag`](./Enums.md#enum-addhiddentag) | Enum | Applies or references the 'AddHiddenTag' effect/state. | 2 ||
| `AddInitiative` | Integer | Applies or references the 'AddInitiative' effect/state. | 2 ||
| `AddKnockbackToEverything` | Integer | Applies the 'AddKnockbackToEverything' effect. | 2 ||
| `AddLootMultiplier` | Integer | Examples: `1` | 2 ||
| [`AddPassivesToSummonAbilityMinions`](Miscellaneous.md#object-addpassivestosummonabilityminions) | Object | Applies the 'AddPassivesToSummonAbilityMinions' effect. | 2 ||
| [`AddPassiveToSpawnedRocks`](Miscellaneous.md#object-addpassivetospawnedrocks) | Object | Applies the 'AddPassiveToSpawnedRocks' effect. | 2 ||
| `AddRangedCritChance` | Integer | Applies the 'AddRangedCritChance' effect. | 2 ||
| [`AddSelfStatusToWeapons`](Items_and_Equipment.md#object-addselfstatustoweapons) | Object | Applies the 'AddSelfStatusToWeapons' effect. | 2 ||
| `AddSpellDamage` | Integer | Applies the 'AddSpellDamage' effect. | 2 ||
| `AddSpiritBombCharges` | Integer | Applies or references the 'AddSpiritBombCharges' effect/state. | 2 ||
| `AddStartingMana` | Number | Applies or references the 'AddStartingMana' effect/state. | 2 ||
| [`AddStatusToBasicAttackWithCooldown`](Miscellaneous.md#object-addstatustobasicattackwithcooldown) | Object | Applies the 'AddStatusToBasicAttackWithCooldown' effect. | 2 ||
| [`AddStatusToExplosions`](Miscellaneous.md#object-addstatustoexplosions) | Object | Applies the 'AddStatusToExplosions' effect. | 2 ||
| [`AddStatusToFirstBasicAttack`](Miscellaneous.md#object-addstatustofirstbasicattack) | Object | Applies the 'AddStatusToFirstBasicAttack' effect. | 2 ||
| [`AddStatusToKnockbackDamage`](Items_and_Equipment.md#object-addstatustoknockbackdamage) | Object | Modifier: Injects a status effect into a specific action. | 2 ||
| [`AddStatusToMeleeDamage`](Miscellaneous.md#object-addstatustomeleedamage) | Object | Applies the 'AddStatusToMeleeDamage' effect. | 2 ||
| [`AddStatusToSpells`](Characters_and_Bosses.md#object-addstatustospells) | Object | Modifier: Injects a status effect into a specific action. | 2 ||
| [`AddStatusToTrampleDamage`](Characters_and_Bosses.md#object-addstatustotrampledamage) | Object | Applies the 'AddStatusToTrampleDamage' effect. | 2 ||
| [`AddTag`](./Enums.md#enum-addtag) | Enum | Applies or references the 'AddTag' effect/state. | 2 ||
| [`AddTemporaryEffectsToEquipment`](Miscellaneous.md#object-addtemporaryeffectstoequipment) | Object | Applies the 'AddTemporaryEffectsToEquipment' effect. | 2 ||
| `AddUnfilledMaxHealth` | Integer | Applies the 'AddUnfilledMaxHealth' effect. | 2 ||
| `AddWeaponScaling` | Integer | Applies the 'AddWeaponScaling' effect. | 2 ||
| [`AfterImage`](Abilities_and_Spells.md#object-afterimage) | Object | Spawns a visual decoy or shade at the caster's previous location. | 2 ||
| `AggroTargetIsBuddy` | Integer | Applies or references the 'AggroTargetIsBuddy' effect/state. | 2 ||
| `all_items` | Variable || 2 ||
| `AllDamageCrits` | Integer | Applies the 'AllDamageCrits' effect. | 2 ||
| `AllDamageImmune_IncludingSpeculative` | Integer | Applies or references the 'AllDamageImmune_IncludingSpeculative' effect/state. | 2 ||
| `AlliesAvoidTraps` | Integer | Applies the 'AlliesAvoidTraps' effect. | 2 ||
| `AllowPassTurn` | Integer | Applies the 'AllowPassTurn' effect. | 2 ||
| [`AllyBonusAbilityAura`](./Enums.md#enum-allybonusabilityaura) | Enum | Applies the 'AllyBonusAbilityAura' effect. | 2 ||
| `AllyChainKnockback` | Integer | Applies the 'AllyChainKnockback' effect. | 2 ||
| [`AllyDamageReaction`](./Enums.md#enum-allydamagereaction) | Enum | Applies the 'AllyDamageReaction' effect. | 2 ||
| [`AllyHealthRegenAura`](Miscellaneous.md#object-allyhealthregenaura) | Object | Applies the 'AllyHealthRegenAura' effect. | 2 ||
| [`AllyMoveAbilityAura`](./Enums.md#enum-allymoveabilityaura) | Enum | Applies the 'AllyMoveAbilityAura' effect. | 2 ||
| `AllyMultiplyKnockbackDamage` | Integer | Applies the 'AllyMultiplyKnockbackDamage' effect. | 2 ||
| `AllyMultiplyKnockbackDistance` | Integer | Applies the 'AllyMultiplyKnockbackDistance' effect. | 2 ||
| `AllyUncappedHPAura` | Integer | Applies the 'AllyUncappedHPAura' effect. | 2 ||
| [`AlternateCraftingPools`](Miscellaneous.md#object-alternatecraftingpools) | Object | Applies the 'AlternateCraftingPools' effect. | 2 ||
| `AlwaysHitDifferentTargets` | Integer | Applies or references the 'AlwaysHitDifferentTargets' effect/state. | 2 ||
| `AmplifyNegativeStatus` | Integer | Applies the 'AmplifyNegativeStatus' effect. | 2 ||
| `AmplifyPositiveStatus` | Integer | Applies the 'AmplifyPositiveStatus' effect. | 2 ||
| `Antidote` | Float | Applies or references the 'Antidote' effect/state. | 2 ||
| [`ApplyStatusesToRandomEnemiesEachTurn`](Items_and_Equipment.md#object-applystatusestorandomenemieseachturn) | Object | Applies or references the 'ApplyStatusesToRandomEnemiesEachTurn' effect/state. | 2 ||
| [`ApplyStatusIfCrit`](Abilities_and_Spells.md#object-applystatusifcrit) | Object | Conditional trigger: Executes the nested logic only if the triggering action was a critical hit. | 2 ||
| [`ApplyToTile`](Abilities_and_Spells.md#object-applytotile) | Object | Redirects the nested effects to apply to the terrain/tile underneath the target rather than the target itself. | 2 ||
| [`ArmorBreakOnHit`](Items_and_Equipment.md#object-armorbreakonhit) | Object | Applies or references the 'ArmorBreakOnHit' effect/state. | 2 ||
| `ArmorDodgeChance` | Integer | Applies or references the 'ArmorDodgeChance' effect/state. | 2 ||
| [`AutocastEachTurn`](./Enums.md#enum-autocasteachturn) | Enum | Applies the 'AutocastEachTurn' effect. | 2 ||
| [`AutocastEachTurnBegin`](./Enums.md#enum-autocasteachturnbegin) | Enum | Applies the 'AutocastEachTurnBegin' effect. | 2 ||
| `AutoCritLowDamage` | Integer | Applies the 'AutoCritLowDamage' effect. | 2 ||
| `AutoEquipConsumables` | Integer | Applies or references the 'AutoEquipConsumables' effect/state. | 2 ||
| [`BackstabCritChance`](./Enums.md#enum-backstabcritchance) | Float | Applies the 'BackstabCritChance' effect. | 2 ||
| `BackstabFront` | Integer | Examples: `1` | 2 ||
| `BasicAttackCantMiss` | Integer | Examples: `1` | 2 ||
| `BasicAttackStatusCarefulness` | Integer | Applies the 'BasicAttackStatusCarefulness' effect. | 2 ||
| [`BasicMonkMelee`](#object-basicmonkmelee) | Object || 2 ||
| [`BasicRanged`](#object-basicranged) | Object || 2 ||
| [`BasicSuplex`](#object-basicsuplex) | Object || 2 ||
| [`BodyGuard`](Abilities_and_Spells.md#object-bodyguard) | Object | Protects an ally by intercepting attacks directed at them. | 2 ||
| [`BodyGuard`](Abilities_and_Spells.md#object-bodyguard) | Object || 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `BonusFoodEachBattle` | Integer | Applies the 'BonusFoodEachBattle' effect. | 2 ||
| `BonusHealthRegenBasedOnDex` | Integer | Applies the 'BonusHealthRegenBasedOnDex' effect. | 2 ||
| `BonusRangeBasedOnDex` | Integer | Applies the 'BonusRangeBasedOnDex' effect. | 2 ||
| [`BonusToss`](#object-bonustoss) | Object || 2 ||
| [`BonusToss2`](#object-bonustoss2) | Object || 2 ||
| [`BoobyTrapItems`](Miscellaneous.md#object-boobytrapitems) | Object | Applies the 'BoobyTrapItems' effect. | 2 ||
| [`BoomerCatExplode`](#object-boomercatexplode) | Object || 2 ||
| `BoostAllyStatsOnDeath` | Integer | Applies the 'BoostAllyStatsOnDeath' effect. | 2 ||
| `BoostDamageGlobalAura` | Integer | Applies the 'BoostDamageGlobalAura' effect. | 2 ||
| `BoostHeals` | Integer | Applies or references the 'BoostHeals' effect/state. | 2 ||
| `BoostRangeGlobalAura` | Integer | Applies the 'BoostRangeGlobalAura' effect. | 2 ||
| [`BouncyProjectiles`](Items_and_Equipment.md#object-bouncyprojectiles) | Object | Applies the 'BouncyProjectiles' effect. | 2 ||
| `Bound` | Integer | Applies or references the 'Bound' effect/state. | 2 ||
| `BraceForEachNeighboringEnemy` | Integer | Applies the 'BraceForEachNeighboringEnemy' effect. | 2 ||
| `BreakWhenNoShield` | Integer | Applies or references the 'BreakWhenNoShield' effect/state. | 2 ||
| [`BungaEntrance`](Characters_and_Bosses.md#object-bungaentrance) | Object | Animation/AI State: Bunga entering the arena. | 2 ||
| [`BungaSwipe`](#object-bungaswipe) | Object || 2 ||
| `CancelPrimedAbilities` | Integer | Applies or references the 'CancelPrimedAbilities' effect/state. | 2 ||
| `CanLevelUpWhenDead` | Integer | Applies or references the 'CanLevelUpWhenDead' effect/state. | 2 ||
| `CanRemoveCursedItems` | Integer | Examples: `1` | 2 ||
| `CanShield` | Integer | Applies or references the 'CanShield' effect/state. | 2 ||
| `CapDamageFromAllies` | Integer | Applies the 'CapDamageFromAllies' effect. | 2 ||
| `CapMovementAbilityRange` | Integer | Applies or references the 'CapMovementAbilityRange' effect/state. | 2 ||
| `CapTechSpent` | Integer | Applies the 'CapTechSpent' effect. | 2 ||
| [`CatAPultAnimation`](Miscellaneous.md#object-catapultanimation) | Object | Applies the 'CatAPultAnimation' effect. | 2 ||
| [`CatapultJump`](#object-catapultjump) | Object || 2 ||
| [`CatapultJump2`](#object-catapultjump2) | Object || 2 ||
| [`CatchProjectiles`](Items_and_Equipment.md#object-catchprojectiles) | Object | Applies or references the 'CatchProjectiles' effect/state. | 2 ||
| `CCImmunity` | Integer | Applies the 'CCImmunity' effect. | 2 ||
| `ChainKnockback` | Integer | Applies the 'ChainKnockback' effect. | 2 ||
| [`ChanceToBlockAndCounter`](Items_and_Equipment.md#object-chancetoblockandcounter) | Integer / Object | Applies or references the 'ChanceToBlockAndCounter' effect/state. | 2 ||
| `ChanceToDisableActionsIfNotCharmed` | Integer | Applies or references the 'ChanceToDisableActionsIfNotCharmed' effect/state. | 2 ||
| [`ChanceToRevive`](Elite_Buffs.md#object-chancetorevive) | Integer / Object | Applies or references the 'ChanceToRevive' effect/state. | 2 ||
| [`ChangeFaction`](./Enums.md#enum-changefaction) | Enum | Applies or references the 'ChangeFaction' effect/state. | 2 ||
| `ChangeTauntPriority` | Integer | Applies the 'ChangeTauntPriority' effect. | 2 ||
| [`ChangeTileOnDeath`](./Enums.md#enum-changetileondeath) | Enum | Applies or references the 'ChangeTileOnDeath' effect/state. | 2 ||
| [`ChargeFists`](#object-chargefists) | Integer / Object | Applies or references the 'ChargeFists' effect/state. | 2 ||
| [`ChargeFists`](#object-chargefists) | Integer / Object || 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`ChargeSpiritBombAura`](./Enums.md#enum-chargespiritbombaura) | Enum | Applies or references the 'ChargeSpiritBombAura' effect/state. | 2 ||
| `CharmAllFlies` | Integer | Applies the 'CharmAllFlies' effect. | 2 ||
| [`CharmedDemonKitten`](#object-charmeddemonkitten) | Object || 2 ||
| [`CharmedFlySwarm`](#object-charmedflyswarm) | Object || 2 ||
| `CharmedForceAttack` | Integer | Applies or references the 'CharmedForceAttack' effect/state. | 2 ||
| [`CherubimReaction`](Characters_and_Bosses.md#object-cherubimreaction) | Object | Reaction: Custom reaction triggers for Cherubim enemies. | 2 ||
| `ClearNegativeEffects` | Integer | Applies the 'ClearNegativeEffects' effect. | 2 ||
| `CoinsAddDamage` | Integer | Applies the 'CoinsAddDamage' effect. | 2 ||
| `CollectPickupsOnBattleEnd` | Integer | Applies the 'CollectPickupsOnBattleEnd' effect. | 2 ||
| `CollideWithThrowTarget` | Integer | Applies or references the 'CollideWithThrowTarget' effect/state. | 2 ||
| [`Conductor`](Passives_and_Statuses.md#object-conductor) | Object | Applies the 'Conductor' effect. | 2 ||
| `ConductorManaRegen` | Integer | Applies the 'ConductorManaRegen' effect. | 2 ||
| [`ConjureBonusAbility`](Abilities_and_Spells.md#object-conjurebonusability) | Enum / Object | Adds a temporary bonus ability to the character's hand/deck. | 2 ||
| [`ConjureBonusAbility`](Abilities_and_Spells.md#object-conjurebonusability) | Enum / Object || 2 | `random` (Enum), `Mage` (Enum), `{ ... }` (Object) |
| `ConjureCastSpellsForAllies` | Integer | Applies the 'ConjureCastSpellsForAllies' effect. | 2 ||
| `ConsumableEffectsMultiplierBonus` | Integer | Applies the 'ConsumableEffectsMultiplierBonus' effect. | 2 ||
| `CopyCatPassive_Initializer` | Integer | Applies or references the 'CopyCatPassive_Initializer' effect/state. | 2 ||
| [`CopySpells`](Abilities_and_Spells.md#object-copyspells) | Integer / Object | Duplicates existing spells currently in the character's hand. | 2 ||
| [`Counterspell`](#object-counterspell) | Integer / Object | Applies or references the 'Counterspell' effect/state. | 2 ||
| [`damage`](Abilities_and_Spells.md#object-damage) | Enum / Integer / Object | The base damage properties of an attack. | 2 ||
| `DamageBasedOnMissingHealth` | Integer | Applies or references the 'DamageBasedOnMissingHealth' effect/state. | 2 ||
| `DamageDistanceAOEFalloff` | Integer | Applies or references the 'DamageDistanceAOEFalloff' effect/state. | 2 ||
| `DamageEnemiesOnHeal` | Integer | Combat Trigger: Deals damage to enemies on heal. | 2 ||
| `DamageEnemiesOnKill` | Integer | Combat Trigger: Deals damage to enemies on kill. | 2 ||
| [`DamageNeighborsAfterMove`](Elite_Buffs.md#object-damageneighborsaftermove) | Object | Examples: `{ ... }` | 2 ||
| [`DamageNeighborTilesWhenCastSpell`](Miscellaneous.md#object-damageneighbortileswhencastspell) | Object | Combat Trigger: Deals damage to neighbor tiles when cast spell. | 2 ||
| [`DamageReductionAura`](Miscellaneous.md#object-damagereductionaura) | Object | Combat Trigger: Deals damage to reduction aura. | 2 ||
| `DamageTrinket` | Integer | Applies or references the 'DamageTrinket' effect/state. | 2 ||
| `DeathChill` | Integer | Applies the 'DeathChill' effect. | 2 ||
| [`DeathRattle`](Characters_and_Bosses.md#object-deathrattle) | Enum / Object | Event Trigger: Executes logic or abilities exactly when the character dies. | 2 ||
| `DebuffImmunity` | Integer | Applies or references the 'DebuffImmunity' effect/state. | 2 ||
| `DejaVu` | Integer | Applies the 'DejaVu' effect. | 2 ||
| [`DelayCastAbility`](Abilities_and_Spells.md#object-delaycastability) | Enum / Object | Queues an ability to be cast automatically after a certain delay or trigger. | 2 ||
| `DelayedFury` | Integer | Applies or references the 'DelayedFury' effect/state. | 2 ||
| `DemonicGlyph_Bite` | Integer | Applies or references the 'DemonicGlyph_Bite' effect/state. | 2 ||
| `DemonicGlyph_Summon` | Integer | Applies or references the 'DemonicGlyph_Summon' effect/state. | 2 ||
| `DemonicGlyphFrames` | Integer | Applies or references the 'DemonicGlyphFrames' effect/state. | 2 ||
| [`DepressionAura`](#depressionaura) | Integer | Examples: `1` | 2 ||
| [`DiesToElement`](Characters_and_Bosses.md#object-diestoelement) | Enum / Object | Vulnerability: Character dies instantly if hit by this element. | 2 ||
| `DieViaAbilityInternally` | Integer | Applies or references the 'DieViaAbilityInternally' effect/state. | 2 ||
| `DirtyClaws` | Integer | Applies the 'DirtyClaws' effect. | 2 ||
| `DisablePassiveSlot` | Integer | Applies or references the 'DisablePassiveSlot' effect/state. | 2 ||
| `DisplaceToOriginalPosition` | Integer | Applies or references the 'DisplaceToOriginalPosition' effect/state. | 2 ||
| `DissuadeInstakills` | Integer | Applies or references the 'DissuadeInstakills' effect/state. | 2 ||
| `DodgeChance_Status` | Integer | Applies or references the 'DodgeChance_Status' effect/state. | 2 ||
| `DoubleCastSpell` | Integer | Applies or references the 'DoubleCastSpell' effect/state. | 2 ||
| `DoubleCastWeapons` | Integer | Applies the 'DoubleCastWeapons' effect. | 2 ||
| [`DoubleLoot`](#object-doubleloot) | Integer / Object | Applies or references the 'DoubleLoot' effect/state. | 2 ||
| [`DoubleLoot`](#object-doubleloot) | Integer / Object || 2 | `2` (Number), `1` (Number), `{ ... }` (Object) |
| `DrinkWater` | Integer | Applies or references the 'DrinkWater' effect/state. | 2 ||
| [`DrMangler`](#object-drmangler) | Object || 2 ||
| `DukeOfFlies` | Integer | Applies the 'DukeOfFlies' effect. | 2 ||
| [`Dyslexia`](./Arrays.md#array-dyslexia) | Array | Examples: `[ 6 9 ], [ 3 5 ]` | 2 ||
| `EachSpellFreeAtFullMana` | Integer | Applies the 'EachSpellFreeAtFullMana' effect. | 2 ||
| [`Earth`](Engine_LogicKeys.md#object-earth) | Object | Examples: `{ ... }` | 2 ||
| [`ElementalAttunement`](Miscellaneous.md#object-elementalattunement) | Object | Applies the 'ElementalAttunement' effect. | 2 ||
| [`EMP`](Miscellaneous.md#object-emp) | Object | Applies the 'EMP' effect. | 2 ||
| `Empath` | Integer | Applies the 'Empath' effect. | 2 ||
| `EmptyMana` | Integer | Applies the 'EmptyMana' effect. | 2 ||
| [`EmptyMind`](#object-emptymind) | Integer / Object | Applies or references the 'EmptyMind' effect/state. | 2 ||
| [`EmptyMind`](#object-emptymind) | Integer / Object || 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `EnemiesGetPickupsKnockedOut` | Integer | Applies the 'EnemiesGetPickupsKnockedOut' effect. | 2 ||
| `EnergyStorm` | Integer | Applies the 'EnergyStorm' effect. | 2 ||
| [`Enlarge`](#object-enlarge) | Integer / Object | Applies or references the 'Enlarge' effect/state. | 2 ||
| [`Enlarge`](#object-enlarge) | Integer / Object || 2 | `3` (Number), `{ ... }` (Object) |
| `EquipmentPassiveMultiplierBonus` | Integer | Applies the 'EquipmentPassiveMultiplierBonus' effect. | 2 ||
| `EquipmentSetBonusBonus` | Integer | Applies the 'EquipmentSetBonusBonus' effect. | 2 ||
| [`EscapeSequence`](Miscellaneous.md#object-escapesequence) | Object | Applies the 'EscapeSequence' effect. | 2 ||
| [`Eternal`](Items_and_Equipment.md#object-eternal) | Object | Applies the 'Eternal' effect. | 2 ||
| `ExpireOnSpawnerTurnEnd` | Integer | Applies or references the 'ExpireOnSpawnerTurnEnd' effect/state. | 2 ||
| `ExplodeOverkilledEnemies` | Integer | Applies the 'ExplodeOverkilledEnemies' effect. | 2 ||
| `ExplosionImmunity` | Integer | Applies or references the 'ExplosionImmunity' effect/state. | 2 ||
| [`ExtraStatusWhenDealingDamage`](Items_and_Equipment.md#object-extrastatuswhendealingdamage) | Object | Applies or references the 'ExtraStatusWhenDealingDamage' effect/state. | 2 ||
| `ExtraTrinketUses` | Integer | Applies or references the 'ExtraTrinketUses' effect/state. | 2 ||
| [`FaceLastDamage`](Characters_and_Bosses.md#object-facelastdamage) | Integer / Object | Reaction: Forces the character to face towards the last damage source. | 2 ||
| `FaceShield` | Integer | Applies or references the 'FaceShield' effect/state. | 2 ||
| [`FamiliarBonusAbility`](./Enums.md#enum-familiarbonusability) | Enum | Applies the 'FamiliarBonusAbility' effect. | 2 ||
| `FamiliarSecondaryDamageImmunity` | Integer | Applies the 'FamiliarSecondaryDamageImmunity' effect. | 2 ||
| [`FinalBossShield`](./Enums.md#enum-finalbossshield) | Enum | Applies or references the 'FinalBossShield' effect/state. | 2 ||
| [`FindExtraItemFromPoolOnBattleEnd`](./Enums.md#enum-findextraitemfrompoolonbattleend) | Enum | Applies or references the 'FindExtraItemFromPoolOnBattleEnd' effect/state. | 2 ||
| [`FindItem`](./Enums.md#enum-finditem) | Enum | Applies or references the 'FindItem' effect/state. | 2 ||
| `FireStorm` | Integer | Examples: `33, 0` | 2 ||
| `FlatHealWhenDealDamage` | Integer | Examples: `1` | 2 ||
| `FlatLeechIfDamaged` | Integer | Applies or references the 'FlatLeechIfDamaged' effect/state. | 2 ||
| `FlippedFacingForceAttack` | Integer | Applies the 'FlippedFacingForceAttack' effect. | 2 ||
| `FlowerPowerAuraBrace` | Integer | Applies the 'FlowerPowerAuraBrace' effect. | 2 ||
| `FlowerPowerAuraStrength` | Integer | Applies the 'FlowerPowerAuraStrength' effect. | 2 ||
| `FlowersOnEndTurn` | Integer | Applies or references the 'FlowersOnEndTurn' effect/state. | 2 ||
| `FlowersOnHit` | Integer | Applies or references the 'FlowersOnHit' effect/state. | 2 ||
| [`FlyDamageIncrease`](Items_and_Equipment.md#object-flydamageincrease) | Object | Applies the 'FlyDamageIncrease' effect. | 2 ||
| `Flying` | Integer | Applies or references the 'Flying' effect/state. | 2 ||
| [`FollowUp`](./Enums.md#enum-followup) | Enum | Applies the 'FollowUp' effect. | 2 ||
| `ForceMoveNonAlliesInRangeTowardsTile` | Integer | Applies or references the 'ForceMoveNonAlliesInRangeTowardsTile' effect/state. | 2 ||
| [`ForceMoveTowardsTaggedObject`](Abilities_and_Spells.md#object-forcemovetowardstaggedobject) | Object | Forces the character to move towards the nearest object with a specific tag. | 2 ||
| [`FormChangeDuringWeatherElement`](Characters_and_Bosses.md#object-formchangeduringweatherelement) | Object | Logic: Changes form automatically during specific weather conditions. | 2 ||
| `FrontstabCritChance` | Integer | Applies the 'FrontstabCritChance' effect. | 2 ||
| `FullHealthAllStatsUp` | Integer | Applies the 'FullHealthAllStatsUp' effect. | 2 ||
| `FullHealthCritChance` | Integer | Applies the 'FullHealthCritChance' effect. | 2 ||
| `FullHealthManaRegen` | Integer | Applies the 'FullHealthManaRegen' effect. | 2 ||
| `FullPower` | Integer | Applies the 'FullPower' effect. | 2 ||
| `GainExtraShield` | Integer | Applies the 'GainExtraShield' effect. | 2 ||
| `GainManaWhenAnythingDies` | Integer | Examples: `1` | 2 ||
| `GlobalManaBurnAura` | Integer | Examples: `-1` | 2 ||
| [`GlobalSpawnOnRoundEnd`](#object-globalspawnonroundend) | Object | Examples: `{ ... }` | 2 ||
| `GoopWalk` | Integer | Applies or references the 'GoopWalk' effect/state. | 2 ||
| [`Grass`](Engine_LogicKeys.md#object-grass) | Object | Examples: `{ ... }` | 2 ||
| `GrassTileHealing` | Integer | Applies the 'GrassTileHealing' effect. | 2 ||
| [`GravityWell`](Miscellaneous.md#object-gravitywell) | Object | Applies the 'GravityWell' effect. | 2 ||
| `greater` | Variable || 2 ||
| [`GrenadeExplode`](#object-grenadeexplode) | Object || 2 ||
| [`Haunt`](#object-haunt) | Object || 2 ||
| `HealAndOverhealToShield` | Integer | Applies the 'HealAndOverhealToShield' effect. | 2 ||
| `HealAtStart` | Integer | Applies the 'HealAtStart' effect. | 2 ||
| `HealDamagesEnemies` | Integer | Applies the 'HealDamagesEnemies' effect. | 2 ||
| `HealingAura` | Integer | Applies the 'HealingAura' effect. | 2 ||
| `HealsAlsoRegenMana` | Integer | Applies the 'HealsAlsoRegenMana' effect. | 2 ||
| `HealsCanRevive` | Integer | Applies the 'HealsCanRevive' effect. | 2 ||
| `HolyDamageMultiplierBonus` | Integer | Applies the 'HolyDamageMultiplierBonus' effect. | 2 ||
| `HolyShieldTransferToSpawner` | Integer | Applies the 'HolyShieldTransferToSpawner' effect. | 2 ||
| [`HolyShieldTransferToTaggedMinions`](./Enums.md#enum-holyshieldtransfertotaggedminions) | Enum | Applies the 'HolyShieldTransferToTaggedMinions' effect. | 2 ||
| `HPGainBlock` | Integer | Applies or references the 'HPGainBlock' effect/state. | 2 ||
| [`IceArmor`](#object-icearmor) | Integer / Object | Applies or references the 'IceArmor' effect/state. | 2 ||
| [`IceArmor`](#object-icearmor) | Integer / Object || 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`ImmediateUseDirectionalAbility`](./Enums.md#enum-immediateusedirectionalability) | Enum | Applies or references the 'ImmediateUseDirectionalAbility' effect/state. | 2 ||
| `ImmobilePassive` | Integer | Applies or references the 'ImmobilePassive' effect/state. | 2 ||
| `ImmortalLeeches` | Integer | Applies the 'ImmortalLeeches' effect. | 2 ||
| `IncreaseExplosionSize` | Integer | Applies or references the 'IncreaseExplosionSize' effect/state. | 2 ||
| `IncreaseHealingSpellRange` | Integer | Applies the 'IncreaseHealingSpellRange' effect. | 2 ||
| `IncreaseItemUsesOnEquip` | Integer | Applies the 'IncreaseItemUsesOnEquip' effect. | 2 ||
| `IncreaseSpellRange` | Integer | Applies or references the 'IncreaseSpellRange' effect/state. | 2 ||
| [`InfiniteRebirth`](Characters_and_Bosses.md#object-infiniterebirth) | Object | Applies the 'InfiniteRebirth' effect. | 2 ||
| `InjuryImmunity` | Integer | Applies or references the 'InjuryImmunity' effect/state. | 2 ||
| `JohnnyCriesForWashers` | Integer | Applies or references the 'JohnnyCriesForWashers' effect/state. | 2 ||
| [`KaijuWinCon`](./Enums.md#enum-kaijuwincon) | Enum | Applies or references the 'KaijuWinCon' effect/state. | 2 ||
| `KillsHeal` | Integer | Applies the 'KillsHeal' effect. | 2 ||
| [`KillsToMeat`](./Enums.md#enum-killstomeat) | Enum | Applies or references the 'KillsToMeat' effect/state. | 2 ||
| [`LateBloomer`](Miscellaneous.md#object-latebloomer) | Object | Applies the 'LateBloomer' effect. | 2 ||
| [`LeaveBehindOnceEachMove`](./Enums.md#enum-leavebehindonceeachmove) | Enum | Applies or references the 'LeaveBehindOnceEachMove' effect/state. | 2 ||
| `LeechPercent` | Integer | Applies the 'LeechPercent' effect. | 2 ||
| `LightningAspectCharge` | Integer | Applies the 'LightningAspectCharge' effect. | 2 ||
| [`LightningRod`](Miscellaneous.md#object-lightningrod) | Object | Applies the 'LightningRod' effect. | 2 ||
| `LimitDamage` | Integer | Applies or references the 'LimitDamage' effect/state. | 2 ||
| `LimitHeal` | Integer | Applies or references the 'LimitHeal' effect/state. | 2 ||
| [`LineOfSightTrueSightAura`](./Enums.md#enum-lineofsighttruesightaura) | Float | Applies the 'LineOfSightTrueSightAura' effect. | 2 ||
| `LobbedHook` | Integer | Applies the 'LobbedHook' effect. | 2 ||
| [`LowHealthAllyDodgeChanceAura`](Miscellaneous.md#object-lowhealthallydodgechanceaura) | Object | Applies the 'LowHealthAllyDodgeChanceAura' effect. | 2 ||
| `MagicDamageImmune` | Integer | Applies or references the 'MagicDamageImmune' effect/state. | 2 ||
| `MakeBasicAttackPassThroughThings` | Integer | Applies the 'MakeBasicAttackPassThroughThings' effect. | 2 ||
| `MakeBasicAttackPull` | Integer | Examples: `1` | 2 ||
| `MakeSpellsRequireCharge` | Integer | Applies the 'MakeSpellsRequireCharge' effect. | 2 ||
| `MamaCatAnimations` | Integer | Applies or references the 'MamaCatAnimations' effect/state. | 2 ||
| `ManaRegenMultiplierIfManaEmpty` | Integer | Applies the 'ManaRegenMultiplierIfManaEmpty' effect. | 2 ||
| [`Math`](Abilities_and_Spells.md#object-math) | Object | Triggers the Tinkerer's Math ability sequence. | 2 ||
| `MaxHPUp` | Integer | Applies or references the 'MaxHPUp' effect/state. | 2 ||
| `MegaMinions` | Integer | Applies the 'MegaMinions' effect. | 2 ||
| `Metal` | Integer | Applies or references the 'Metal' effect/state. | 2 ||
| `MetalDetector` | Integer | Applies the 'MetalDetector' effect. | 2 ||
| `MinimumTech` | Integer | Applies the 'MinimumTech' effect. | 2 ||
| [`MiniVolcanoReaction`](./Enums.md#enum-minivolcanoreaction) | Enum | Applies or references the 'MiniVolcanoReaction' effect/state. | 2 ||
| [`MockingbirdForm`](#object-mockingbirdform) | Object || 2 ||
| [`ModifyAbility`](#object-modifyability) | Object | Applies or references the 'ModifyAbility' effect/state. | 2 ||
| [`MotherTumorSpawnInCapture`](Characters_and_Bosses.md#object-mothertumorspawnincapture) | Object | Boss Logic: Logic for capturing entities inside the Mother's tumors upon spawning. | 2 ||
| [`MoveAwayFromDamageSource`](Characters_and_Bosses.md#object-moveawayfromdamagesource) | Object | Examples: `BasicJump` | 2 ||
| [`MovementReaction`](Characters_and_Bosses.md#object-movementreaction) | Object | Reaction: Triggers an effect or ability when forced to move. | 2 ||
| [`MoveOne`](#object-moveone) | Object || 2 ||
| `MoveRandomly` | Integer | Applies the 'MoveRandomly' effect. | 2 ||
| [`MoveSpeedMultiplier`](./Enums.md#enum-movespeedmultiplier) | Float | Applies or references the 'MoveSpeedMultiplier' effect/state. | 2 ||
| [`MoveTowardsDamageSource`](Characters_and_Bosses.md#object-movetowardsdamagesource) | Enum / Object | AI Movement: Closes distance on the last source of damage. | 2 ||
| [`MoveWhenDamaged`](Cat_Mutations.md#object-movewhendamaged) | Enum / Object | AI Movement: Forces a reposition when taking damage. | 2 ||
| [`neck_NukeBonus`](#object-neck_nukebonus) | Object || 2 ||
| [`neck_NukeExplode`](#object-neck_nukeexplode) | Object || 2 ||
| [`Necro_SoulDagger_Uncharged`](#object-necro_souldagger_uncharged) | Object || 2 ||
| [`NextAttackSpecialCrit`](Abilities_and_Spells.md#object-nextattackspecialcrit) | Integer / Object | Modifies the character's next attack to have special critical properties. | 2 ||
| [`NextBattleStatus`](#object-nextbattlestatus) | Object | Applies the 'NextBattleStatus' effect. | 2 ||
| `NoManaRegen` | Integer | Applies the 'NoManaRegen' effect. | 2 ||
| `NoReflection` | Integer | Applies the 'NoReflection' effect. | 2 ||
| [`NubbyToss`](#object-nubbytoss) | Object || 2 ||
| `NubbyTossPriority` | Integer | Applies the 'NubbyTossPriority' effect. | 2 ||
| [`NukeQuestFinalBossModifications`](Abilities_and_Spells.md#object-nukequestfinalbossmodifications) | Object | Special encounter trigger for the Nuke Quest ending. | 2 ||
| `NumbingLeeches` | Integer | Applies the 'NumbingLeeches' effect. | 2 ||
| `OneUseSpellDamageUp` | Integer | Applies the 'OneUseSpellDamageUp' effect. | 2 ||
| `OverhealGainsBothShield` | Integer | Applies the 'OverhealGainsBothShield' effect. | 2 ||
| [`OverHealToStatuses`](Abilities_and_Spells.md#object-overhealtostatuses) | Object | Converts excessive healing beyond maximum health into specific status effects. | 2 ||
| `ParasitesArentCursed` | Integer | Applies the 'ParasitesArentCursed' effect. | 2 ||
| [`passive0`](./Enums.md#enum-passive0) | Enum | `HotBlooded`, `SelfAssured` | 2 ||
| [`PassiveAfterXKills`](Items_and_Equipment.md#object-passiveafterxkills) | Object | Applies or references the 'PassiveAfterXKills' effect/state. | 2 ||
| [`PassiveAtFullHealth`](Miscellaneous.md#object-passiveatfullhealth) | Object | Applies the 'PassiveAtFullHealth' effect. | 2 ||
| [`PassiveAtInjuryThreshold`](Miscellaneous.md#object-passiveatinjurythreshold) | Object | Applies the 'PassiveAtInjuryThreshold' effect. | 2 ||
| [`PassiveEnergized`](#object-passiveenergized) | Variable || 2 ||
| [`PassiveIfWeaponIsUsable`](Items_and_Equipment.md#object-passiveifweaponisusable) | Object | Applies or references the 'PassiveIfWeaponIsUsable' effect/state. | 2 ||
| [`PassiveTar`](#object-passivetar) | Variable || 2 ||
| [`PassiveUntilCastSpell`](Miscellaneous.md#object-passiveuntilcastspell) | Object | Applies the 'PassiveUntilCastSpell' effect. | 2 ||
| [`PassiveUntilGetKill`](Miscellaneous.md#object-passiveuntilgetkill) | Object | Applies the 'PassiveUntilGetKill' effect. | 2 ||
| [`PassiveWhenTheAlpha`](Miscellaneous.md#object-passivewhenthealpha) | Object | State Trigger: Grants nested passives when the alpha. | 2 ||
| [`PassiveWhileHasStatus`](Cat_Mutations.md#object-passivewhilehasstatus) | Object | Passive: Activates only while the character has the specified status. | 2 ||
| [`PassiveWhileInMonkMeleeStance`](Items_and_Equipment.md#object-passivewhileinmonkmeleestance) | Object | Applies the 'PassiveWhileInMonkMeleeStance' effect. | 2 ||
| [`PassiveWhileInMonkRangedStance`](Miscellaneous.md#object-passivewhileinmonkrangedstance) | Object | Applies the 'PassiveWhileInMonkRangedStance' effect. | 2 ||
| [`PassiveWhileNotHasStatus`](Characters_and_Bosses.md#object-passivewhilenothasstatus) | Object | Passive: Activates only while the character does NOT have the specified status. | 2 ||
| [`PassiveWhilePreviewingMonkRangedStance`](Miscellaneous.md#object-passivewhilepreviewingmonkrangedstance) | Object | Applies the 'PassiveWhilePreviewingMonkRangedStance' effect. | 2 ||
| [`PassiveWhileWearingMetal`](Miscellaneous.md#object-passivewhilewearingmetal) | Object | Applies the 'PassiveWhileWearingMetal' effect. | 2 ||
| `PermanentItems` | Integer | Applies the 'PermanentItems' effect. | 2 ||
| `PermanentUpgradeRandomActive` | Integer | Applies or references the 'PermanentUpgradeRandomActive' effect/state. | 2 ||
| `Phasing` | Integer | Applies or references the 'Phasing' effect/state. | 2 ||
| [`PlayerCat_ThiefShade2`](#object-playercat_thiefshade2) | Object || 2 ||
| `PoisonMultiplier` | Integer | Applies the 'PoisonMultiplier' effect. | 2 ||
| [`Poop`](Events_and_Encounters.md#object-poop) | Object || 2 ||
| `PrioritizeAggroTarget` | Integer | Applies or references the 'PrioritizeAggroTarget' effect/state. | 2 ||
| `PrioritizePlayerCats` | Integer | Applies or references the 'PrioritizePlayerCats' effect/state. | 2 ||
| `PrioritizeWeakestEnemy` | Integer | Applies or references the 'PrioritizeWeakestEnemy' effect/state. | 2 ||
| [`ProtectTargetedAllies`](Characters_and_Bosses.md#object-protecttargetedallies) | Object | AI Logic: Navigates to intercept attacks directed at allies. | 2 ||
| [`QuakeAreaChance`](Abilities_and_Spells.md#object-quakeareachance) | Object | Provides a probability to trigger an earthquake Area of Effect. | 2 ||
| `Quiver` | Integer | Applies the 'Quiver' effect. | 2 ||
| [`RandomDistanceDisplace`](Abilities_and_Spells.md#object-randomdistancedisplace) | Integer / Object | Displaces the target by a randomized distance. | 2 ||
| [`RandomKnockback`](Abilities_and_Spells.md#object-randomknockback) | Object | Applies a randomized amount of knockback force. | 2 ||
| `RandomLightning` | Integer | Examples: `50` | 2 ||
| `RandomStatUp` | Integer / String | Applies or references the 'RandomStatUp' effect/state. | 2 ||
| [`RandomTaggedMutation`](./Enums.md#enum-randomtaggedmutation) | Enum | Applies or references the 'RandomTaggedMutation' effect/state. | 2 ||
| `RangedTrueShot` | Integer | Applies or references the 'RangedTrueShot' effect/state. | 2 ||
| [`RatKing`](#object-ratking) | Object || 2 ||
| [`ReaperRevenge`](#object-reaperrevenge) | Object || 2 ||
| `RebukeDamage` | Integer | Applies or references the 'RebukeDamage' effect/state. | 2 ||
| [`red`](Events_and_Encounters.md#object-red) | Object | Event Object: Story branch or dialog option representing the \'Red\' action. | 2 ||
| [`Reflect`](#object-reflect) | Integer / Object | Applies or references the 'Reflect' effect/state. | 2 ||
| [`RefreshEquipmentAbilityOnElement`](Items_and_Equipment.md#object-refreshequipmentabilityonelement) | Object | Applies or references the 'RefreshEquipmentAbilityOnElement' effect/state. | 2 ||
| `RefreshMoveOnWeaponConnect` | Integer | Applies the 'RefreshMoveOnWeaponConnect' effect. | 2 ||
| [`Regurge`](#object-regurge) | Integer / Object | Applies or references the 'Regurge' effect/state. | 2 ||
| [`Regurge`](#object-regurge) | Integer / Object || 2 | `1` (Number), `{ ... }` (Object) |
| `ReloadOnKill` | Integer | Applies or references the 'ReloadOnKill' effect/state. | 2 ||
| `ReloadOnKillEnemy` | Integer | Applies or references the 'ReloadOnKillEnemy' effect/state. | 2 ||
| `ReloadOnTotalDamageReceived` | Integer | Applies or references the 'ReloadOnTotalDamageReceived' effect/state. | 2 ||
| `RemoteLeech` | Integer | Applies or references the 'RemoteLeech' effect/state. | 2 ||
| `RemoveLineOfSightRestrictions` | Integer | Applies the 'RemoveLineOfSightRestrictions' effect. | 2 ||
| `RemoveOncePerFightRestriction` | Integer | Applies the 'RemoveOncePerFightRestriction' effect. | 2 ||
| `RepairArmorCondition` | Integer | Applies or references the 'RepairArmorCondition' effect/state. | 2 ||
| [`ReplaceBasicAttack_Mutation`](./Enums.md#enum-replacebasicattack_mutation) | Enum | Examples: `FetusSpit` | 2 ||
| [`ReplaceBasicAttackWhenDead`](./Enums.md#enum-replacebasicattackwhendead) | Enum | Applies the 'ReplaceBasicAttackWhenDead' effect. | 2 ||
| [`ReplaceBrain`](Characters_and_Bosses.md#object-replacebrain) | Object | Applies the 'ReplaceBrain' effect. | 2 ||
| [`ReplaceSpellsWhenDead`](./Enums.md#enum-replacespellswhendead) | Enum | Applies the 'ReplaceSpellsWhenDead' effect. | 2 ||
| `ResetArmorShield` | Integer | Applies or references the 'ResetArmorShield' effect/state. | 2 ||
| `ReturnBoundItemOnBattleEnd` | Integer | Applies or references the 'ReturnBoundItemOnBattleEnd' effect/state. | 2 ||
| `ReviveOnWin` | Integer | Applies the 'ReviveOnWin' effect. | 2 ||
| [`Robot`](Characters_and_Bosses.md#object-robot) | Integer / Object | Character Form: Behavior and stats for the 'Robot' state. | 2 ||
| [`robot`](Characters_and_Bosses.md#object-robot) | Variable || 2 ||
| `RobotsInheritArmor` | Integer | Applies the 'RobotsInheritArmor' effect. | 2 ||
| `RockDetector` | Integer | Applies the 'RockDetector' effect. | 2 ||
| `SafeExplosions` | Integer | Applies the 'SafeExplosions' effect. | 2 ||
| [`Sandstorm`](#object-sandstorm) | Object | Examples: `1` | 2 ||
| [`Sandstorm`](#object-sandstorm) | Object || 2 | `1` (Number), `{ ... }` (Object) |
| [`ScaledStatusOnLoseShield`](Miscellaneous.md#object-scaledstatusonloseshield) | Object | Applies the 'ScaledStatusOnLoseShield' effect. | 2 ||
| [`ScaledStatusOnOverHealed`](Miscellaneous.md#object-scaledstatusonoverhealed) | Object | Applies the 'ScaledStatusOnOverHealed' effect. | 2 ||
| [`ScaledStatusOnOverMana`](Miscellaneous.md#object-scaledstatusonovermana) | Object | Applies the 'ScaledStatusOnOverMana' effect. | 2 ||
| [`ScaledStatusOnSpendMana`](Items_and_Equipment.md#object-scaledstatusonspendmana) | Object | Applies the 'ScaledStatusOnSpendMana' effect. | 2 ||
| `ScrambleEverything` | Integer | Applies or references the 'ScrambleEverything' effect/state. | 2 ||
| [`SecurityBotProtect`](Characters_and_Bosses.md#object-securitybotprotect) | Object | AI Logic: Guarding behavior for Security Bot units. | 2 ||
| `SelfStatusCarefulness` | Integer | Applies or references the 'SelfStatusCarefulness' effect/state. | 2 ||
| [`SelfStun`](./Arrays.md#array-selfstun) | Array / Integer | Applies or references the 'SelfStun' effect/state. | 2 ||
| [`SetDefaultFace`](./Enums.md#enum-setdefaultface) | Enum | Applies or references the 'SetDefaultFace' effect/state. | 2 ||
| [`SetItemAux`](#object-setitemaux) | Object | Applies or references the 'SetItemAux' effect/state. | 2 ||
| `SetSpellCosts` | Integer | Applies the 'SetSpellCosts' effect. | 2 ||
| [`Shadowstep`](#object-shadowstep) | Object || 2 ||
| `ShareHealthRegen` | Integer | Applies the 'ShareHealthRegen' effect. | 2 ||
| [`SharePickups`](Characters_and_Bosses.md#object-sharepickups) | Object | Applies the 'SharePickups' effect. | 2 ||
| [`Shatter`](#object-shatter) | Integer / Object | Applies or references the 'Shatter' effect/state. | 2 ||
| [`ShortCircuit`](#object-shortcircuit) | Integer / Object | Applies or references the 'ShortCircuit' effect/state. | 2 ||
| [`ShortCircuit`](#object-shortcircuit) | Integer / Object || 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `ShoulderCheck` | Integer | Applies the 'ShoulderCheck' effect. | 2 ||
| [`ShovingMatch`](./Enums.md#enum-shovingmatch) | Enum | Applies the 'ShovingMatch' effect. | 2 ||
| `SignalFinalBossShieldBroke` | Integer | Applies or references the 'SignalFinalBossShieldBroke' effect/state. | 2 ||
| [`SleepDart2`](#object-sleepdart2) | Object || 2 ||
| [`SlotMachineRollPool`](Characters_and_Bosses.md#object-slotmachinerollpool) | Object | Logic: Defines the possible outcomes for slot machine enemies. | 2 ||
| `SmallEnemiesIgnoreYou` | Integer | Applies the 'SmallEnemiesIgnoreYou' effect. | 2 ||
| [`SmellBlood`](#object-smellblood) | Integer / Object | Applies or references the 'SmellBlood' effect/state. | 2 ||
| [`SmellBlood`](#object-smellblood) | Integer / Object || 2 | `1` (Number), `{ ... }` (Object) |
| [`SmiteEnemiesWhoKill`](Miscellaneous.md#object-smiteenemieswhokill) | Object | Applies the 'SmiteEnemiesWhoKill' effect. | 2 ||
| [`SparkleBuff`](#object-sparklebuff) | Variable || 2 ||
| `SpawnBearTrapOnMiss` | Integer | Applies the 'SpawnBearTrapOnMiss' effect. | 2 ||
| [`SpawnCatCopyWhenDowned`](Miscellaneous.md#object-spawncatcopywhendowned) | Object | Examples: `{ ... }` | 2 ||
| [`SpawnExtraThingsOnBattleStart`](Cat_Mutations.md#object-spawnextrathingsonbattlestart) | Object | Examples: `{ ... }` | 2 ||
| [`SpawnItemLinkedFamiliar`](Items_and_Equipment.md#object-spawnitemlinkedfamiliar) | Object | Applies or references the 'SpawnItemLinkedFamiliar' effect/state. | 2 ||
| [`SpawnMeatOnMove`](./Enums.md#enum-spawnmeatonmove) | Enum | Applies the 'SpawnMeatOnMove' effect. | 2 ||
| `SpawnNearEnemies` | Integer | Applies or references the 'SpawnNearEnemies' effect/state. | 2 ||
| [`SpawnObjectOnPopCorpse`](Items_and_Equipment.md#object-spawnobjectonpopcorpse) | Enum / Object | Applies or references the 'SpawnObjectOnPopCorpse' effect/state. | 2 ||
| [`SpecialFriends`](Miscellaneous.md#object-specialfriends) | Object | Applies the 'SpecialFriends' effect. | 2 ||
| [`SpecialGodRays`](#object-specialgodrays) | Object | Examples: `{ ... }` | 2 ||
| [`SpikeBuff`](#object-spikebuff) | Variable || 2 ||
| `SplittableMove` | Integer | Applies the 'SplittableMove' effect. | 2 ||
| [`Spook`](#object-spook) | Object || 2 ||
| `SpreadExtraDebuffs` | Integer | Applies the 'SpreadExtraDebuffs' effect. | 2 ||
| `SpreadPainBonus` | Integer | Applies the 'SpreadPainBonus' effect. | 2 ||
| `SpreadPainBonusCrit` | Integer | Applies the 'SpreadPainBonusCrit' effect. | 2 ||
| [`StackingDodgeChanceOnTookDamage`](Miscellaneous.md#object-stackingdodgechanceontookdamage) | Object | Applies the 'StackingDodgeChanceOnTookDamage' effect. | 2 ||
| `StatMinimum` | Integer | Applies the 'StatMinimum' effect. | 2 ||
| [`StatsAtLowHealth`](Miscellaneous.md#object-statsatlowhealth) | Object | Applies the 'StatsAtLowHealth' effect. | 2 ||
| [`StatusAfterCastSpell`](Items_and_Equipment.md#object-statusaftercastspell) | Object | Applies or references the 'StatusAfterCastSpell' effect/state. | 2 ||
| [`StatusAfterXTurns`](Characters_and_Bosses.md#object-statusafterxturns) | Object | Event Trigger: Applies a status effect after X turns have passed. | 2 ||
| [`StatusAlliesOnBattleStart`](Items_and_Equipment.md#object-statusalliesonbattlestart) | Object | Applies or references the 'StatusAlliesOnBattleStart' effect/state. | 2 ||
| [`StatusAlliesOnGainCoins`](Miscellaneous.md#object-statusalliesongaincoins) | Object | Event Trigger: Applies nested statuses to allies on gain coins. | 2 ||
| [`StatusAlliesOnKill`](Miscellaneous.md#object-statusalliesonkill) | Object | Event Trigger: Applies nested statuses to allies on kill. | 2 ||
| [`StatusAlliesOnSpendMana`](Miscellaneous.md#object-statusalliesonspendmana) | Object | Event Trigger: Applies nested statuses to allies on spend mana. | 2 ||
| [`StatusAlliesScaledByCursedOnDeath`](Miscellaneous.md#object-statusalliesscaledbycursedondeath) | Object | Event Trigger: Applies nested statuses to allies scaled by cursed on death. | 2 ||
| [`StatusAllyWhenAllySpendsMana`](Miscellaneous.md#object-statusallywhenallyspendsmana) | Object | Event Trigger: Applies nested statuses to ally when ally spends mana. | 2 ||
| [`StatusAnyCatAllyWhoKills`](Miscellaneous.md#object-statusanycatallywhokills) | Object | Event Trigger: Applies nested statuses to any cat ally who kills. | 2 ||
| `StatusCarefulness` | Integer | Applies or references the 'StatusCarefulness' effect/state. | 2 ||
| [`StatusCharactersOnRoundStart`](#object-statuscharactersonroundstart) | Object | Examples: `{ ... }` | 2 ||
| [`StatusDamagers`](Miscellaneous.md#object-statusdamagers) | Object | Event Trigger: Applies nested statuses to damagers. | 2 ||
| [`StatusEachRoundEnd`](Cat_Mutations.md#object-statuseachroundend) | Object | Applies or references the 'StatusEachRoundEnd' effect/state. | 2 ||
| [`StatusEachTurnEndForEachTurn`](Characters_and_Bosses.md#object-statuseachturnendforeachturn) | Object | Event Trigger: Applies nested statuses to each turn end for each turn. | 2 ||
| [`StatusEachTurnEndPerEnemyKill`](Miscellaneous.md#object-statuseachturnendperenemykill) | Object | Event Trigger: Applies nested statuses to each turn end per enemy kill. | 2 ||
| [`StatusEnemiesOnDeath`](Miscellaneous.md#object-statusenemiesondeath) | Object | Event Trigger: Applies nested statuses to enemies on death. | 2 ||
| [`StatusEveryXSpellCastsEachTurn`](Cat_Mutations.md#object-statuseveryxspellcastseachturn) | Object | Examples: `{ ... }` | 2 ||
| [`StatusEveryXTurnBegins`](Miscellaneous.md#object-statuseveryxturnbegins) | Object | Event Trigger: Applies nested statuses to every x turn begins. | 2 ||
| [`StatusIfDidntMove`](Cat_Mutations.md#object-statusifdidntmove) | Object | Examples: `{ ... }` | 2 ||
| [`StatusIfUnusedActPoints`](Items_and_Equipment.md#object-statusifunusedactpoints) | Object | Applies or references the 'StatusIfUnusedActPoints' effect/state. | 2 ||
| [`StatusKillers`](Abilities_and_Spells.md#object-statuskillers) | Object | Instantly kills the target if they possess the specified status effects. | 2 ||
| [`StatusOnAnyDeath`](Miscellaneous.md#object-statusonanydeath) | Object | Event Trigger: Applies nested statuses when any death. | 2 ||
| [`StatusOnBackstab`](Items_and_Equipment.md#object-statusonbackstab) | Object | Event Trigger: Applies statuses when this action occurs. | 2 ||
| [`StatusOnBattleEndIfKillThresholdMet`](Miscellaneous.md#object-statusonbattleendifkillthresholdmet) | Object | Event Trigger: Applies nested statuses when battle end if kill threshold met. | 2 ||
| [`StatusOnBattleStart`](Items_and_Equipment.md#object-statusonbattlestart) | Object | Event Trigger: Applies statuses when this action occurs. | 2 ||
| [`StatusOnBreakItem`](Items_and_Equipment.md#object-statusonbreakitem) | Object | Event Trigger: Applies statuses when this action occurs. | 2 ||
| [`StatusOnCollectPickup`](Items_and_Equipment.md#object-statusoncollectpickup) | Object | Event Trigger: Applies nested statuses when collect pickup. | 2 ||
| [`StatusOnDealtDamage`](Miscellaneous.md#object-statusondealtdamage) | Object | Event Trigger: Applies nested statuses when dealt damage. | 2 ||
| [`StatusOnDealtDamageThreshold`](Miscellaneous.md#object-statusondealtdamagethreshold) | Object | Event Trigger: Applies nested statuses when dealt damage threshold. | 2 ||
| [`StatusOnDie`](Cat_Mutations.md#object-statusondie) | Object | Event Trigger: Applies statuses when this action occurs. | 2 ||
| [`StatusOnEatPill`](Miscellaneous.md#object-statusoneatpill) | Object | Examples: `{ ... }` | 2 ||
| [`StatusOnGainShield`](Miscellaneous.md#object-statusongainshield) | Object | Event Trigger: Applies nested statuses when gain shield. | 2 ||
| [`StatusOnHeal`](Miscellaneous.md#object-statusonheal) | Object | Event Trigger: Applies nested statuses when heal. | 2 ||
| [`StatusOnKillEnemy`](Items_and_Equipment.md#object-statusonkillenemy) | Object | Event Trigger: Applies statuses when this action occurs. | 2 ||
| [`StatusOnOverMana`](Miscellaneous.md#object-statusonovermana) | Object | Event Trigger: Applies nested statuses when over mana. | 2 ||
| [`StatusOnPickupCoins`](Items_and_Equipment.md#object-statusonpickupcoins) | Object | Event Trigger: Applies nested statuses when pickup coins. | 2 ||
| [`StatusOnPopCorpse`](Items_and_Equipment.md#object-statusonpopcorpse) | Object | Event Trigger: Applies statuses when this action occurs. | 2 ||
| [`StatusOnSetPieceBreak`](Miscellaneous.md#object-statusonsetpiecebreak) | Object | Examples: `{ ... }` | 2 ||
| [`StatusOnSpawnIn`](Characters_and_Bosses.md#object-statusonspawnin) | Object | Event Trigger: Applies statuses immediately when spawned. | 2 ||
| [`StatusOnTookDamageFromEnemyAbility`](Miscellaneous.md#object-statusontookdamagefromenemyability) | Object | Event Trigger: Applies nested statuses when took damage from enemy ability. | 2 ||
| [`StatusOnTriggerTrap`](Miscellaneous.md#object-statusontriggertrap) | Object | Event Trigger: Applies nested statuses when trigger trap. | 2 ||
| [`StatusOnUseBasicAttack`](Items_and_Equipment.md#object-statusonusebasicattack) | Object | Event Trigger: Applies nested statuses when use basic attack. | 2 ||
| [`StatusOnUseElementAbility`](Miscellaneous.md#object-statusonuseelementability) | Object | Event Trigger: Applies nested statuses when use element ability. | 2 ||
| [`StatusPerInjury`](Miscellaneous.md#object-statusperinjury) | Object | Event Trigger: Applies nested statuses to per injury. | 2 ||
| [`StatusReplacement`](./Arrays.md#array-statusreplacement) | Array | Examples: `[ Petrify PetrifyCharmed ]` | 2 ||
| [`StatusThingsKnockedBack`](Miscellaneous.md#object-statusthingsknockedback) | Object | Event Trigger: Applies nested statuses to things knocked back. | 2 ||
| [`StatusWhenAllySpendsMana`](Items_and_Equipment.md#object-statuswhenallyspendsmana) | Object | Event Trigger: Applies nested statuses to when ally spends mana. | 2 ||
| `StrengthForEachNeighboringEnemy` | Integer | Applies the 'StrengthForEachNeighboringEnemy' effect. | 2 ||
| `StrengthInNumbersAura` | Integer | Applies the 'StrengthInNumbersAura' effect. | 2 ||
| `Study` | Integer | Applies the 'Study' effect. | 2 ||
| `SurviveAt1HP` | Integer | Applies or references the 'SurviveAt1HP' effect/state. | 2 ||
| `SwallowSmallCharacter` | Integer | Applies or references the 'SwallowSmallCharacter' effect/state. | 2 ||
| `SwapHighestAndLowestStat` | Integer | Applies or references the 'SwapHighestAndLowestStat' effect/state. | 2 ||
| [`Switcheroo`](#object-switcheroo) | Integer / Object | Applies or references the 'Switcheroo' effect/state. | 2 ||
| [`Switcheroo`](#object-switcheroo) | Integer / Object || 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`TaggedPickupEffectReplacement`](Miscellaneous.md#object-taggedpickupeffectreplacement) | Object | Applies the 'TaggedPickupEffectReplacement' effect. | 2 ||
| `TempCounterAttack` | Integer | Applies or references the 'TempCounterAttack' effect/state. | 2 ||
| `TempCritChanceUp` | Integer | Applies or references the 'TempCritChanceUp' effect/state. | 2 ||
| `TempNoManaRegen` | Integer | Applies or references the 'TempNoManaRegen' effect/state. | 2 ||
| `ThornsDamageImmuneUntilSettled` | Integer | Applies or references the 'ThornsDamageImmuneUntilSettled' effect/state. | 2 ||
| `TileDamageImmuneUntilSettled` | Integer | Applies or references the 'TileDamageImmuneUntilSettled' effect/state. | 2 ||
| `TileDamageMultiplier` | Integer | Applies the 'TileDamageMultiplier' effect. | 2 ||
| [`TinkererBasicAttackSwitching`](Cat_Classes.md#object-tinkererbasicattackswitching) | Object | Logic: Allows Tinkerer to swap basic attacks. | 2 ||
| [`TowerDefense`](Miscellaneous.md#object-towerdefense) | Object | Applies the 'TowerDefense' effect. | 2 ||
| [`TowerDefenseReflex`](./Enums.md#enum-towerdefensereflex) | Enum | Applies the 'TowerDefenseReflex' effect. | 2 ||
| [`TradeLife`](#object-tradelife) | Integer / Object | Applies or references the 'TradeLife' effect/state. | 2 ||
| [`TradeLife`](#object-tradelife) | Integer / Object || 2 | `1` (Number), `{ ... }` (Object) |
| [`TrailBlazer`](#object-trailblazer) | Enum / Integer / Object | Applies or references the 'TrailBlazer' effect/state. | 2 ||
| [`TrailBlazer`](#object-trailblazer) | Enum / Integer / Object || 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`TransformOnElementInfluencex`](Characters_and_Bosses.md#object-transformonelementinfluencex) | Object | Logic: Variant element influence transformation. | 2 ||
| [`TransformWhenBuddyDies`](./Enums.md#enum-transformwhenbuddydies) | Enum | Applies or references the 'TransformWhenBuddyDies' effect/state. | 2 ||
| `TrapEffectsMultiplier` | Integer | Applies the 'TrapEffectsMultiplier' effect. | 2 ||
| `TriggerDOTStatuses` | Integer | Applies or references the 'TriggerDOTStatuses' effect/state. | 2 ||
| `triggers_limit` | Integer | Examples: `1` | 2 ||
| `TrinketActiveEffectsMultiplierBonus` | Integer | Applies or references the 'TrinketActiveEffectsMultiplierBonus' effect/state. | 2 ||
| `TrinketPassiveMultiplierBonus` | Integer | Applies or references the 'TrinketPassiveMultiplierBonus' effect/state. | 2 ||
| `UncappedHP` | Integer | Applies the 'UncappedHP' effect. | 2 ||
| `UncappedHPBonusStr` | Integer | Applies the 'UncappedHPBonusStr' effect. | 2 ||
| `Uncontrollable` | Integer | Applies or references the 'Uncontrollable' effect/state. | 2 ||
| `UnlockOrientation` | Integer | Applies or references the 'UnlockOrientation' effect/state. | 2 ||
| [`UpgradeLevelUpClassActives`](./Enums.md#enum-upgradelevelupclassactives) | Enum | Applies the 'UpgradeLevelUpClassActives' effect. | 2 ||
| [`UpgradeLevelUpClassPassives`](./Enums.md#enum-upgradelevelupclasspassives) | Enum | Applies the 'UpgradeLevelUpClassPassives' effect. | 2 ||
| `UpgradeSpawnedPickups` | Integer | Applies the 'UpgradeSpawnedPickups' effect. | 2 ||
| [`UpgradeTaggedSpawnsToChampions`](./Enums.md#enum-upgradetaggedspawnstochampions) | Enum | Examples: `worm, bug` | 2 ||
| `Vengeful` | Integer | Applies the 'Vengeful' effect. | 2 ||
| `VisualFlySwarm` | Integer | Examples: `1` | 2 ||
| `WeaponActiveEffectsMultiplierBonus` | Integer | Examples: `2` | 2 ||
| `WeaponCountsAsBasicAttack` | Integer | Applies the 'WeaponCountsAsBasicAttack' effect. | 2 ||
| `WeaponDamageMultiplierBonus` | Integer | Applies the 'WeaponDamageMultiplierBonus' effect. | 2 ||
| `WeaponPassiveMultiplierBonus` | Integer | Examples: `2` | 2 ||
| `WeaponsDontLoseDurability` | Integer | Applies or references the 'WeaponsDontLoseDurability' effect/state. | 2 ||
| [`XIsLivingCharactersWithTag`](./Enums.md#enum-xislivingcharacterswithtag) | Enum | Applies or references the 'XIsLivingCharactersWithTag' effect/state. | 2 ||
| `XIsOtherHealsThisTurn` | Integer | Applies or references the 'XIsOtherHealsThisTurn' effect/state. | 2 ||
| [`XIsSpellStormRampAndReset`](Abilities_and_Spells.md#object-xisspellstormrampandreset) | Integer / Object | Math variable assignment: Evaluates X based on Spell Storm stacks, then resets them. | 2 ||
| [`XIsTargetHealth`](Abilities_and_Spells.md#object-xistargethealth) | Object | Math variable assignment: Evaluates X as the target's current health. | 2 ||
| `XIsTimesDamageTaken` | Integer | Applies or references the 'XIsTimesDamageTaken' effect/state. | 2 ||
| `Zombie` | Number | Examples: `1` | 2 ||
| `AbilityDamageMultiplier` | Float | Examples: `1.5` | 1 ||
| `AbilityDisableIfLivingCrow` | Integer | Applies or references the 'AbilityDisableIfLivingCrow' effect/state. | 1 ||
| `AbilityEnabledAtHealthThreshold` | Integer | Applies or references the 'AbilityEnabledAtHealthThreshold' effect/state. | 1 ||
| `AbilityEnabledIfBasicAttackUsedThisTurn` | Integer | Applies or references the 'AbilityEnabledIfBasicAttackUsedThisTurn' effect/state. | 1 ||
| `AbilityEnabledIfMovementTrapped` | Integer | Applies or references the 'AbilityEnabledIfMovementTrapped' effect/state. | 1 ||
| `AbilityEnabledIfNoAggroTarget` | Integer | Applies or references the 'AbilityEnabledIfNoAggroTarget' effect/state. | 1 ||
| [`AbilityEnabledIfNotHasStatus`](./Enums.md#enum-abilityenabledifnothasstatus) | Enum | Applies or references the 'AbilityEnabledIfNotHasStatus' effect/state. | 1 ||
| [`AbilityEnabledIfSpecificItemEquipped`](./Enums.md#enum-abilityenabledifspecificitemequipped) | Enum | Applies or references the 'AbilityEnabledIfSpecificItemEquipped' effect/state. | 1 ||
| [`AbilityOnBattleStart_UseAI`](./Enums.md#enum-abilityonbattlestart_useai) | Enum | Applies or references the 'AbilityOnBattleStart_UseAI' effect/state. | 1 ||
| [`AbilityOnRoundEndOnce`](Items_and_Equipment.md#object-abilityonroundendonce) | Object | Applies or references the 'AbilityOnRoundEndOnce' effect/state. | 1 ||
| `AbsorbManaFromOtherSpells` | Integer | Applies or references the 'AbsorbManaFromOtherSpells' effect/state. | 1 ||
| `AcidRain` | Integer | Examples: `2` | 1 ||
| [`AddAdvantageToEvent`](Items_and_Equipment.md#object-addadvantagetoevent) | Object | Applies or references the 'AddAdvantageToEvent' effect/state. | 1 ||
| `AddAllyNeighborsToAttackRange` | Integer | Applies the 'AddAllyNeighborsToAttackRange' effect. | 1 ||
| `AddConstitution` | Integer | Examples: `2` | 1 ||
| [`AddElementsToSpells`](./Enums.md#enum-addelementstospells) | Enum | Applies or references the 'AddElementsToSpells' effect/state. | 1 ||
| `AddExtraTurnsBeforeRun` | Integer | Examples: `2` | 1 ||
| `AddLevelUpStatMultiplier` | Integer | Applies the 'AddLevelUpStatMultiplier' effect. | 1 ||
| [`AddPostProcessEffect`](#object-addpostprocesseffect) | Object | Examples: `{ ... }` | 1 ||
| `AddRandomEliteBuff` | Integer | Examples: `1` | 1 ||
| [`AddStatusesIfPersistentWeatherElement`](Miscellaneous.md#object-addstatusesifpersistentweatherelement) | Object | Applies the 'AddStatusesIfPersistentWeatherElement' effect. | 1 ||
| [`AddStatusesToReceivedElementalDamage`](Miscellaneous.md#object-addstatusestoreceivedelementaldamage) | Object | Applies the 'AddStatusesToReceivedElementalDamage' effect. | 1 ||
| [`AddStatusToBackstabs`](Items_and_Equipment.md#object-addstatustobackstabs) | Object | Modifier: Injects a status effect into a specific action. | 1 ||
| [`AddStatusToFirstSpellEachTurn`](Miscellaneous.md#object-addstatustofirstspelleachturn) | Object | Examples: `{ ... }` | 1 ||
| [`AddStatusToReceivedDamage`](Characters_and_Bosses.md#object-addstatustoreceiveddamage) | Object | Modifier: Applies a status effect whenever the character takes damage. | 1 ||
| [`AddStatusToReceivedDamage_ExcludeStatuses`](Miscellaneous.md#object-addstatustoreceiveddamage_excludestatuses) | Object | Applies the 'AddStatusToReceivedDamage_ExcludeStatuses' effect. | 1 ||
| [`AddTilesetObjects`](#object-addtilesetobjects) | Object | Examples: `{ ... }` | 1 ||
| `Adrenaline` | Integer | Applies or references the 'Adrenaline' effect/state. | 1 ||
| [`AdvancedTint`](./Arrays.md#array-advancedtint) | Array | Applies or references the 'AdvancedTint' effect/state. | 1 ||
| [`AdventureTokenPassivePool`](Characters_and_Bosses.md#object-adventuretokenpassivepool) | Object | Map/Metaprogression: Pool of passive modifiers applied by adventure tokens. | 1 ||
| [`AggroTargetIsGovernedByHitEffect`](Characters_and_Bosses.md#object-aggrotargetisgovernedbyhiteffect) | Object | AI Logic: Forces the character's aggro to follow specific hit effects rather than default proximity. | 1 ||
| `AggroTargetIsLastEnemyThatDealtDamage` | Integer | Applies or references the 'AggroTargetIsLastEnemyThatDealtDamage' effect/state. | 1 ||
| `AggroTargetIsLowestHealthEnemyTillItDies` | Integer | Applies or references the 'AggroTargetIsLowestHealthEnemyTillItDies' effect/state. | 1 ||
| `AggroTargetIsLowestMaxHealthCat` | Integer | Applies or references the 'AggroTargetIsLowestMaxHealthCat' effect/state. | 1 ||
| [`AIControlNextTurn`](Items_and_Equipment.md#object-aicontrolnextturn) | Object | Applies or references the 'AIControlNextTurn' effect/state. | 1 ||
| `AIFavorLowHealth` | Integer | Applies or references the 'AIFavorLowHealth' effect/state. | 1 ||
| [`AlienBeastDangerZones`](./Arrays.md#array-alienbeastdangerzones) | Array | Applies or references the 'AlienBeastDangerZones' effect/state. | 1 ||
| `AlienBeastEyeStalks` | Integer | Applies or references the 'AlienBeastEyeStalks' effect/state. | 1 ||
| `all_spells` | Variable || 1 ||
| `AlliesScrambleSpellAfterCast` | Integer | Applies or references the 'AlliesScrambleSpellAfterCast' effect/state. | 1 ||
| `AlliesTakeExtraTurn` | Integer | Applies or references the 'AlliesTakeExtraTurn' effect/state. | 1 ||
| `AllSpellsCostActPoints` | Integer | Applies or references the 'AllSpellsCostActPoints' effect/state. | 1 ||
| `AllSpellsCostCharge` | Integer | Applies or references the 'AllSpellsCostCharge' effect/state. | 1 ||
| [`AllStatsAura`](Characters_and_Bosses.md#object-allstatsaura) | Object | Passive: Projects an aura that modifies all primary stats of nearby characters. | 1 ||
| `AllUnitsExplodeOnDeath` | Integer | Applies or references the 'AllUnitsExplodeOnDeath' effect/state. | 1 ||
| [`AlluringDoodieEater`](Items_and_Equipment.md#object-alluringdoodieeater) | Object | Applies or references the 'AlluringDoodieEater' effect/state. | 1 ||
| [`AllyDodgeChanceAura`](Items_and_Equipment.md#object-allydodgechanceaura) | Object | Applies or references the 'AllyDodgeChanceAura' effect/state. | 1 ||
| `AlphaAllStatsUp` | Integer | Applies or references the 'AlphaAllStatsUp' effect/state. | 1 ||
| `AlphaDodgeChance` | Integer | Applies or references the 'AlphaDodgeChance' effect/state. | 1 ||
| [`AlphaStatusOnTurnBegin`](Abilities_and_Spells.md#object-alphastatusonturnbegin) | Object | Grants a specific status effect to the 'Alpha' (the party leader) at the start of their turn. | 1 ||
| [`AlternateIdleAnimation`](./Enums.md#enum-alternateidleanimation) | Enum | Applies or references the 'AlternateIdleAnimation' effect/state. | 1 ||
| `AlwaysChosenForLevelUp` | Integer | Applies or references the 'AlwaysChosenForLevelUp' effect/state. | 1 ||
| `AOEBonus` | Integer | Applies or references the 'AOEBonus' effect/state. | 1 ||
| [`ApplyPassivesToSpawnerWhileAlive`](Abilities_and_Spells.md#object-applypassivestospawnerwhilealive) | Object | Grants nested passives to the entity that spawned this object, lasting only as long as this object remains alive. | 1 ||
| `ApplyShieldToApplierBasedOnMaxHealth` | Integer | Applies or references the 'ApplyShieldToApplierBasedOnMaxHealth' effect/state. | 1 ||
| [`ApplyStatusesNextTurnBegin`](Abilities_and_Spells.md#object-applystatusesnextturnbegin) | Object | Delays the application of the nested status effects until the start of the target's next turn. | 1 ||
| [`ApplyToOthersWithSharedTagAndFaction`](Abilities_and_Spells.md#object-applytootherswithsharedtagandfaction) | Object | Redirects the nested effects to apply to all other entities on the map that share the target's faction and specified tags. | 1 ||
| [`ApplyToRandomClosestAlly`](Abilities_and_Spells.md#object-applytorandomclosestally) | Object | Redirects the nested effects to apply to the nearest friendly unit. If tied, chooses randomly among them. | 1 ||
| [`Autism`](Miscellaneous.md#object-autism) | Object | Applies the 'Autism' effect. | 1 ||
| `AvoidDamagingCharmedEnemies` | Integer | Applies or references the 'AvoidDamagingCharmedEnemies' effect/state. | 1 ||
| `AwardCoinsOnDeath` | Integer | Applies or references the 'AwardCoinsOnDeath' effect/state. | 1 ||
| `BackstabWeakness` | Float | Applies the 'BackstabWeakness' effect. | 1 ||
| `BalanceStats` | Integer | Applies or references the 'BalanceStats' effect/state. | 1 ||
| `BasicAIDangerZone` | Integer | Applies or references the 'BasicAIDangerZone' effect/state. | 1 ||
| [`BasicAttackStatusSwap`](./Arrays.md#array-basicattackstatusswap) | Array | Examples: `[ TempDamageUp DamageUp ]` | 1 ||
| [`BasicButcherMelee`](#object-basicbutchermelee) | Object || 1 ||
| [`BasicDruidAbility`](#object-basicdruidability) | Object || 1 ||
| [`BasicMagicShortRanged`](#object-basicmagicshortranged) | Object || 1 ||
| [`BasicMedicMelee`](#object-basicmedicmelee) | Object || 1 ||
| [`BasicMelee_4Hits`](#object-basicmelee_4hits) | Object || 1 ||
| [`BasicNecroRanged`](#object-basicnecroranged) | Object || 1 ||
| [`BasicPsychicPull`](#object-basicpsychicpull) | Object || 1 ||
| [`BattlefieldUniqueRandomPassive`](Characters_and_Bosses.md#object-battlefielduniquerandompassive) | Object | Map Rule: Grants a unique random passive modifier to the battlefield. | 1 ||
| [`BBTransformMutant`](#object-bbtransformmutant) | Object || 1 ||
| [`BBTransformZealot`](#object-bbtransformzealot) | Object || 1 ||
| [`BiggestFood`](Engine_LogicKeys.md#object-biggestfood) | Integer / Object | Applies or references the 'BiggestFood' effect/state. | 1 ||
| `BigSplashDamage` | Integer | Applies the 'BigSplashDamage' effect. | 1 ||
| `BlackHolePassive` | Integer | Applies or references the 'BlackHolePassive' effect/state. | 1 ||
| `BlackHoleSuck` | Integer | Applies or references the 'BlackHoleSuck' effect/state. | 1 ||
| `BlessingOfPeace` | Integer | Applies or references the 'BlessingOfPeace' effect/state. | 1 ||
| [`BloatEyeMovement2`](#object-bloateyemovement2) | Object || 1 ||
| [`BloatEyePassive2`](./Enums.md#enum-bloateyepassive2) | Enum | Applies or references the 'BloatEyePassive2' effect/state. | 1 ||
| [`BloatyExplodey`](#object-bloatyexplodey) | Object || 1 ||
| `BlockAllDamage` | Integer | Applies or references the 'BlockAllDamage' effect/state. | 1 ||
| `BlockDamageUnderThreshold` | Integer | Applies or references the 'BlockDamageUnderThreshold' effect/state. | 1 ||
| `BlockNegativeStatus` | Integer | Applies or references the 'BlockNegativeStatus' effect/state. | 1 ||
| `Bloodzerked` | Integer | Applies or references the 'Bloodzerked' effect/state. | 1 ||
| `BombBehavior` | Integer | Applies or references the 'BombBehavior' effect/state. | 1 ||
| [`BombRatTurtle`](#object-bombratturtle) | Integer / Object | Applies or references the 'BombRatTurtle' effect/state. | 1 ||
| [`BoneWormShotMed`](#object-bonewormshotmed) | Object || 1 ||
| [`BonusAbility_DelayedApplication`](./Enums.md#enum-bonusability_delayedapplication) | Enum | Applies or references the 'BonusAbility_DelayedApplication' effect/state. | 1 ||
| `BonusDamageBasedOnMana` | Integer | Applies or references the 'BonusDamageBasedOnMana' effect/state. | 1 ||
| `BonusHealthRegenPerDisorder` | Integer | Examples: `1` | 1 ||
| `BoostDamageAura` | Integer | Applies the 'BoostDamageAura' effect. | 1 ||
| `BoostRangeAura` | Integer | Applies the 'BoostRangeAura' effect. | 1 ||
| `BoostReceivedHealing` | Integer | Applies or references the 'BoostReceivedHealing' effect/state. | 1 ||
| [`BoyDino`](#object-boydino) | Object || 1 ||
| [`BoyDinoCry`](#object-boydinocry) | Object || 1 ||
| `BrittleCharismaUp` | Integer | Applies or references the 'BrittleCharismaUp' effect/state. | 1 ||
| `BrittleConstitutionUp` | Integer | Applies or references the 'BrittleConstitutionUp' effect/state. | 1 ||
| `BrittleDexterityUp` | Integer | Applies or references the 'BrittleDexterityUp' effect/state. | 1 ||
| `BrittleIntelligenceUp` | Integer | Applies or references the 'BrittleIntelligenceUp' effect/state. | 1 ||
| `BrittleLuckUp` | Integer | Applies or references the 'BrittleLuckUp' effect/state. | 1 ||
| `BrittleSpeedUp` | Integer | Applies or references the 'BrittleSpeedUp' effect/state. | 1 ||
| `BrittleStrengthUp` | Integer | Applies or references the 'BrittleStrengthUp' effect/state. | 1 ||
| [`BungaCheers`](Characters_and_Bosses.md#object-bungacheers) | Object | Animation/AI State: Bunga cheering animation logic. | 1 ||
| `ButterflySwarm` | Integer | Examples: `2` | 1 ||
| `BypassRockKnockback` | Integer | Applies or references the 'BypassRockKnockback' effect/state. | 1 ||
| `CanceledQueuedInput` | Integer | Applies or references the 'CanceledQueuedInput' effect/state. | 1 ||
| `CantDodge` | Integer | Applies the 'CantDodge' effect. | 1 ||
| `CapBasicAttackDamage` | Integer | Applies or references the 'CapBasicAttackDamage' effect/state. | 1 ||
| `CapReceivedDamage` | Integer | Applies or references the 'CapReceivedDamage' effect/state. | 1 ||
| [`CatGoop`](#object-catgoop) | Object || 1 ||
| [`CatPartsSizeScale`](Items_and_Equipment.md#object-catpartssizescale) | Object | Applies or references the 'CatPartsSizeScale' effect/state. | 1 ||
| [`CaveCatDad`](#object-cavecatdad) | Object || 1 ||
| `CaveWomanBirthControl` | Integer | Applies or references the 'CaveWomanBirthControl' effect/state. | 1 ||
| [`CerberubsAggroTargetBehavior`](Characters_and_Bosses.md#object-cerberubsaggrotargetbehavior) | Object | AI Logic: Custom aggro targeting rules for Cerberubs. | 1 ||
| [`CerberubsStraightReaction`](#object-cerberubsstraightreaction) | Object || 1 ||
| `ChampionUpgradeNextMinion` | Integer | Applies or references the 'ChampionUpgradeNextMinion' effect/state. | 1 ||
| [`chance`](./Enums.md#enum-chance) | Float | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 ||
| `ChanceToAmbush` | Integer | Applies or references the 'ChanceToAmbush' effect/state. | 1 ||
| [`ChanceToForceEvent`](Items_and_Equipment.md#object-chancetoforceevent) | Object | Applies or references the 'ChanceToForceEvent' effect/state. | 1 ||
| [`ChanceToFormChangeOnAbilityDamage`](Characters_and_Bosses.md#object-chancetoformchangeonabilitydamage) | Object | Reaction: Probability to change forms when taking ability damage. | 1 ||
| [`ChangeTileUnderCharacterAtStart`](./Enums.md#enum-changetileundercharacteratstart) | Enum | Applies or references the 'ChangeTileUnderCharacterAtStart' effect/state. | 1 ||
| `ChaosBossFlipMidTeleport` | Integer | Applies or references the 'ChaosBossFlipMidTeleport' effect/state. | 1 ||
| `ChaosBossFormChange` | Integer | Applies or references the 'ChaosBossFormChange' effect/state. | 1 ||
| [`ChaosBossFormChangeGuide`](Characters_and_Bosses.md#object-chaosbossformchangeguide) | Object | Boss Logic: Maps the form transition phases for the Chaos Boss. | 1 ||
| [`ChaosBossPieces`](Characters_and_Bosses.md#object-chaosbosspieces) | Object | Boss Logic: Defines the separate destructible pieces of the Chaos Boss. | 1 ||
| [`ChaosHeadDropIn`](Characters_and_Bosses.md#object-chaosheaddropin) | Object | Boss Logic: Drop-in attack/animation for the Chaos Head. | 1 ||
| [`CharacterTypeGainsStatusAtBattleStart`](Engine_LogicKeys.md#object-charactertypegainsstatusatbattlestart) | Object | Encounter Modifier: Applies a status effect to all characters of a specific type (e.g., Cats, Bosses) at the start of battle. | 1 ||
| `CharismaIsMaxStat` | Integer | Applies or references the 'CharismaIsMaxStat' effect/state. | 1 ||
| `CharmedFacingForceAttack` | Integer | Applies or references the 'CharmedFacingForceAttack' effect/state. | 1 ||
| [`CharmedLeech`](#object-charmedleech) | Object || 1 ||
| [`CharmedPooter`](#object-charmedpooter) | Object || 1 ||
| [`CharmedReaper`](#object-charmedreaper) | Object || 1 ||
| `CharmImmunity` | Integer | Applies or references the 'CharmImmunity' effect/state. | 1 ||
| `choose_favorite_cat` | Variable || 1 ||
| [`Chubs`](#object-chubs) | Object || 1 ||
| [`ChubsGoop`](#object-chubsgoop) | Object || 1 ||
| [`ChubsRage`](#object-chubsrage) | Object || 1 ||
| `ClearDefaultDebris` | Integer | Examples: `1` | 1 ||
| `ClearFinalBossBattlefield` | Integer | Applies or references the 'ClearFinalBossBattlefield' effect/state. | 1 ||
| `CloneWeaponTemp` | Integer | Applies or references the 'CloneWeaponTemp' effect/state. | 1 ||
| `CockroachSwarm` | Integer | Examples: `1` | 1 ||
| [`CoinTossBounce`](./Enums.md#enum-cointossbounce) | Enum | Applies or references the 'CoinTossBounce' effect/state. | 1 ||
| [`Conditional_Flying`](Engine_Uncategorized_Resources.md#conditional_flying) | Object | Examples: `{ ... }` | 1 ||
| [`Conditional_ManaThreshold`](Engine_LogicKeys.md#conditional_manathreshold) | Object | Conditional constraint. Nested properties only trigger if this is true. | 1 ||
| [`Conditional_SourceHasTag`](Engine_LogicKeys.md#conditional_sourcehastag) | Object | Conditional object: Executes nested logic only if the target is/has SourceHasTag. | 1 ||
| [`Conditional_Tiny`](Engine_Uncategorized_Resources.md#conditional_tiny) | Object | Examples: `{ ... }` | 1 ||
| [`ConfusionEffectOnTaggedAbilities`](./Enums.md#enum-confusioneffectontaggedabilities) | Enum | Applies the 'ConfusionEffectOnTaggedAbilities' effect. | 1 ||
| [`ConjureSingleUseBonusAbility`](./Enums.md#enum-conjuresingleusebonusability) | Enum | Applies or references the 'ConjureSingleUseBonusAbility' effect/state. | 1 ||
| `ConsumablesMeleeRange` | Integer | Applies the 'ConsumablesMeleeRange' effect. | 1 ||
| [`ConvertDamageToScaledStatus`](Items_and_Equipment.md#object-convertdamagetoscaledstatus) | Object | Applies or references the 'ConvertDamageToScaledStatus' effect/state. | 1 ||
| [`CounterAttackAfterEnemyCastSpell`](./Enums.md#enum-counterattackafterenemycastspell) | Enum | Applies or references the 'CounterAttackAfterEnemyCastSpell' effect/state. | 1 ||
| `CounterNextAttacks` | Integer | Applies or references the 'CounterNextAttacks' effect/state. | 1 ||
| [`CraterCreeperOut`](#object-cratercreeperout) | Object || 1 ||
| `CrowAttackLink` | Integer | Applies or references the 'CrowAttackLink' effect/state. | 1 ||
| `CurrentWeaponAddElectricElement` | Integer | Applies or references the 'CurrentWeaponAddElectricElement' effect/state. | 1 ||
| [`CyborgTurns`](Miscellaneous.md#object-cyborgturns) | Object | Examples: `{ ... }` | 1 ||
| `DamageFromBehindOnly` | Integer | Applies or references the 'DamageFromBehindOnly' effect/state. | 1 ||
| [`DamageIfDidntUseSpecificAbility`](Miscellaneous.md#object-damageifdidntusespecificability) | Object | Combat Trigger: Deals damage to if didnt use specific ability. | 1 ||
| `DamageWeapon` | Integer | Applies or references the 'DamageWeapon' effect/state. | 1 ||
| [`DarkOneStrike`](#object-darkonestrike) | Object || 1 ||
| [`DeathwormUnderground`](./Enums.md#enum-deathwormunderground) | Enum | Applies or references the 'DeathwormUnderground' effect/state. | 1 ||
| [`DecoyExplode`](#object-decoyexplode) | Object || 1 ||
| `DecoySwapper` | Integer | Applies or references the 'DecoySwapper' effect/state. | 1 ||
| `DelayedPain` | Integer | Applies or references the 'DelayedPain' effect/state. | 1 ||
| [`DelayedWindCone`](Abilities_and_Spells.md#object-delayedwindcone) | Object | Creates a delayed Area of Effect cone. | 1 ||
| `DeleteInanimateObjectsChance` | Integer | Examples: `25` | 1 ||
| `DeleteTraps` | Integer | Applies or references the 'DeleteTraps' effect/state. | 1 ||
| `DemonicGlyph_Bounce` | Integer | Applies or references the 'DemonicGlyph_Bounce' effect/state. | 1 ||
| `DemonicGlyph_Fire` | Integer | Applies or references the 'DemonicGlyph_Fire' effect/state. | 1 ||
| `DemonicGlyph_Movement` | Integer | Applies or references the 'DemonicGlyph_Movement' effect/state. | 1 ||
| `DemonicGlyphStealer` | Integer | Applies or references the 'DemonicGlyphStealer' effect/state. | 1 ||
| [`DestroyerShieldBash`](#object-destroyershieldbash) | Object || 1 ||
| `DestroyNeckArmor` | Integer | Applies or references the 'DestroyNeckArmor' effect/state. | 1 ||
| [`Diabetes`](Miscellaneous.md#object-diabetes) | Object | Applies the 'Diabetes' effect. | 1 ||
| [`DiceBehavior`](Characters_and_Bosses.md#object-dicebehavior) | Object | AI Logic: Custom behavior for Dice enemies. | 1 ||
| [`DicerArt`](./Arrays.md#array-dicerart) | Array | Applies or references the 'DicerArt' effect/state. | 1 ||
| [`DiesToPiercingAndSpikes`](Characters_and_Bosses.md#object-diestopiercingandspikes) | Object | Vulnerability: Character dies instantly if hit by piercing attacks or spikes. | 1 ||
| `DieWhenOnlyGolemsLeft` | Integer | Applies or references the 'DieWhenOnlyGolemsLeft' effect/state. | 1 ||
| `DieWhenSpawnerDies` | Integer | Applies or references the 'DieWhenSpawnerDies' effect/state. | 1 ||
| [`Digest`](#object-digest) | Object || 1 ||
| [`DinoLegAnimation`](./Enums.md#enum-dinoleganimation) | Enum | Applies or references the 'DinoLegAnimation' effect/state. | 1 ||
| `DisableSpells` | Integer | Applies or references the 'DisableSpells' effect/state. | 1 ||
| `Disguised` | Integer | Applies or references the 'Disguised' effect/state. | 1 ||
| [`DisguisedTrapper`](./Enums.md#enum-disguisedtrapper) | Enum | Applies or references the 'DisguisedTrapper' effect/state. | 1 ||
| `DisplayBuddyCatOnSpawn` | Integer | Applies or references the 'DisplayBuddyCatOnSpawn' effect/state. | 1 ||
| `DissolveRandomArmorPiece` | Integer | Applies or references the 'DissolveRandomArmorPiece' effect/state. | 1 ||
| `DivineShieldPickup` | Integer | Applies or references the 'DivineShieldPickup' effect/state. | 1 ||
| `DodgeChanceWithBlindSpot` | Integer | Applies or references the 'DodgeChanceWithBlindSpot' effect/state. | 1 ||
| [`DodgeWhenTargeted`](Characters_and_Bosses.md#object-dodgewhentargeted) | Object | Reaction: Executes a dodge maneuver when targeted. | 1 ||
| `DoubleCast` | Integer | Applies or references the 'DoubleCast' effect/state. | 1 ||
| `DoubleCastSpellIfManaCostUnderThreshold` | Integer | Applies or references the 'DoubleCastSpellIfManaCostUnderThreshold' effect/state. | 1 ||
| `DoubleCastSpellsEachTurn_Status` | Integer | Applies or references the 'DoubleCastSpellsEachTurn_Status' effect/state. | 1 ||
| `DoubleCastSpellThisTurn` | Integer | Applies or references the 'DoubleCastSpellThisTurn' effect/state. | 1 ||
| [`DoubleCastTaggedSpells`](./Enums.md#enum-doublecasttaggedspells) | Enum | Applies or references the 'DoubleCastTaggedSpells' effect/state. | 1 ||
| `DoubleReceivedNegativeStatus` | Integer | Applies or references the 'DoubleReceivedNegativeStatus' effect/state. | 1 ||
| `DoubleReceivedPositiveStatus` | Integer | Applies or references the 'DoubleReceivedPositiveStatus' effect/state. | 1 ||
| `DrainAllyCatsForFleshGolem` | Integer | Applies or references the 'DrainAllyCatsForFleshGolem' effect/state. | 1 ||
| [`DropAsFamiliarOnTookDamage`](./Enums.md#enum-dropasfamiliarontookdamage) | Enum | Applies or references the 'DropAsFamiliarOnTookDamage' effect/state. | 1 ||
| [`DropSoulJarOnDeath`](./Enums.md#enum-dropsouljarondeath) | Enum | Applies or references the 'DropSoulJarOnDeath' effect/state. | 1 ||
| `DuplicateRandomEquippedItem` | Integer | Applies or references the 'DuplicateRandomEquippedItem' effect/state. | 1 ||
| `DustCloudBehavior` | Integer | Applies or references the 'DustCloudBehavior' effect/state. | 1 ||
| `Dybbuk1HPTracker` | Integer | Applies or references the 'Dybbuk1HPTracker' effect/state. | 1 ||
| `DybbukManualExitTag` | Variable || 1 ||
| [`DybbukPossessionFallback`](Characters_and_Bosses.md#object-dybbukpossessionfallback) | Object | Logic: Fallback state when a Dybbuk possession fails. | 1 ||
| [`EatShit`](#object-eatshit) | Object || 1 ||
| `ElectricArcs` | Integer | Applies or references the 'ElectricArcs' effect/state. | 1 ||
| [`element`](./Enums.md#enum-element) | Array / Enum | The specific element type to check for. | 1 ||
| [`ElementWeakness`](./Enums.md#enum-elementweakness) | Enum | Applies or references the 'ElementWeakness' effect/state. | 1 ||
| `EliteUpgradeNextMinion` | Integer | Applies or references the 'EliteUpgradeNextMinion' effect/state. | 1 ||
| `end_of_round` | Boolean | `true` | 1 ||
| `enemies` | Variable || 1 ||
| `EnrageOnDamage` | Integer | Applies or references the 'EnrageOnDamage' effect/state. | 1 ||
| [`EnterMount`](./Enums.md#enum-entermount) | Enum | Applies or references the 'EnterMount' effect/state. | 1 ||
| `EraseSpawnCoins` | Integer | Applies or references the 'EraseSpawnCoins' effect/state. | 1 ||
| [`euphoric`](Miscellaneous.md#object-euphoric) | Object | Examples: `{ ... }` | 1 ||
| `EventBounterHunterPassive` | Integer | Applies or references the 'EventBounterHunterPassive' effect/state. | 1 ||
| `exclude_self` | Boolean | `false` | 1 ||
| [`ExcludeFromEvents`](./Enums.md#enum-excludefromevents) | Enum | Applies or references the 'ExcludeFromEvents' effect/state. | 1 ||
| `ExhaustionRoundChange` | Integer | Applies the 'ExhaustionRoundChange' effect. | 1 ||
| `ExistUntilIdleUpkeep` | Integer | Applies or references the 'ExistUntilIdleUpkeep' effect/state. | 1 ||
| `ExplodeCharacter_DeathBloom` | Integer | Applies or references the 'ExplodeCharacter_DeathBloom' effect/state. | 1 ||
| `ExplodeCharacter_DeathBloom2` | Integer | Applies or references the 'ExplodeCharacter_DeathBloom2' effect/state. | 1 ||
| `ExtraInjuryOnDeath` | Integer | Applies the 'ExtraInjuryOnDeath' effect. | 1 ||
| [`ExtraTurnsPerTaggedUnit`](./Enums.md#enum-extraturnspertaggedunit) | Enum | Applies or references the 'ExtraTurnsPerTaggedUnit' effect/state. | 1 ||
| [`face_EatNeverstone`](#object-face_eatneverstone) | Object || 1 ||
| [`face_LeechBrood`](#object-face_leechbrood) | Object || 1 ||
| [`FaceAwayLastDamage`](Characters_and_Bosses.md#object-faceawaylastdamage) | Object | Reaction: Forces the character to face away from the last damage source. | 1 ||
| `FactionDisguiseSource` | Integer | Applies or references the 'FactionDisguiseSource' effect/state. | 1 ||
| `FastKnockback` | Integer | Applies or references the 'FastKnockback' effect/state. | 1 ||
| [`FinalBossBeamQueue`](Characters_and_Bosses.md#object-finalbossbeamqueue) | Object | Boss Logic: Attack queue for the final boss beam. | 1 ||
| [`FinalBossBecomeTheChild`](Characters_and_Bosses.md#object-finalbossbecomethechild) | Object | Boss Logic: Phase transition for the final boss. | 1 ||
| [`FinalBossHitCountdownBoris`](Characters_and_Bosses.md#object-finalbosshitcountdownboris) | Object | Boss Logic: Countdown trigger for Boris. | 1 ||
| [`FinalBossHitCountdownExplosive`](Characters_and_Bosses.md#object-finalbosshitcountdownexplosive) | Object | Boss Logic: Countdown trigger for explosives. | 1 ||
| [`FinalBossHitCountdownHoly`](Characters_and_Bosses.md#object-finalbosshitcountdownholy) | Object | Boss Logic: Countdown trigger for holy attacks. | 1 ||
| [`FinalBossPupils`](Characters_and_Bosses.md#object-finalbosspupils) | Object | Boss Logic: Pupil state management. | 1 ||
| `FinalBossQueueBeam` | Integer | Applies or references the 'FinalBossQueueBeam' effect/state. | 1 ||
| [`FinalBossShieldHealth`](Characters_and_Bosses.md#object-finalbossshieldhealth) | Object | Boss Logic: Shield health management. | 1 ||
| [`FinalBossSyncAnimations`](Characters_and_Bosses.md#object-finalbosssyncanimations) | Object | Boss Logic: Synchronizes multi-part boss animations. | 1 ||
| [`FireArmor`](#object-firearmor) | Integer / Object | Applies or references the 'FireArmor' effect/state. | 1 ||
| [`FireArmor2`](#object-firearmor2) | Integer / Object | Applies or references the 'FireArmor2' effect/state. | 1 ||
| [`FireExtinguish_Steam`](#object-fireextinguish_steam) | Variable || 1 ||
| `FireflySwarm` | Integer | Examples: `2` | 1 ||
| `FistOfFateUniqueEnemyTracker` | Integer | Applies or references the 'FistOfFateUniqueEnemyTracker' effect/state. | 1 ||
| `FlingObjectsOnTop` | Integer | Applies or references the 'FlingObjectsOnTop' effect/state. | 1 ||
| [`FlushmasterCelebration`](./Enums.md#enum-flushmastercelebration) | Enum | Applies or references the 'FlushmasterCelebration' effect/state. | 1 ||
| [`FlyBuff`](#object-flybuff) | Variable || 1 ||
| `Fog` | Integer | Examples: `1` | 1 ||
| `ForceCollectsPickups` | Integer | Applies or references the 'ForceCollectsPickups' effect/state. | 1 ||
| `ForceDodgeEverything` | Integer | Applies or references the 'ForceDodgeEverything' effect/state. | 1 ||
| [`ForceImmediateMoveAndAttack`](Abilities_and_Spells.md#object-forceimmediatemoveandattack) | Object | Forces the character to immediately move to a target and use a specified ability. | 1 ||
| `ForceMoveAndAttack` | Integer | Applies or references the 'ForceMoveAndAttack' effect/state. | 1 ||
| `ForceTransferWeapon` | Integer | Applies or references the 'ForceTransferWeapon' effect/state. | 1 ||
| [`ForceUseAbilityOnTarget`](#object-forceuseabilityontarget) | Object | Applies or references the 'ForceUseAbilityOnTarget' effect/state. | 1 ||
| [`FormChangeWhenBuddyDies`](./Enums.md#enum-formchangewhenbuddydies) | Enum | Applies or references the 'FormChangeWhenBuddyDies' effect/state. | 1 ||
| [`FrankBolts`](Passives_and_Statuses.md#object-frankbolts) | Integer / Object | Applies or references the 'FrankBolts' effect/state. | 1 ||
| `FreeFirstCastAndAfterSpendMana` | Integer | Applies or references the 'FreeFirstCastAndAfterSpendMana' effect/state. | 1 ||
| `FreeFirstCastEachMatch` | Integer | Applies or references the 'FreeFirstCastEachMatch' effect/state. | 1 ||
| `FreeSpellsAtFullMana` | Integer | Applies the 'FreeSpellsAtFullMana' effect. | 1 ||
| `FrontstabBasicAttackCritChance` | Integer | Applies the 'FrontstabBasicAttackCritChance' effect. | 1 ||
| `FullBlockEverything` | Integer | Applies or references the 'FullBlockEverything' effect/state. | 1 ||
| `FullBlockEverythingTo0Damage` | Integer | Applies or references the 'FullBlockEverythingTo0Damage' effect/state. | 1 ||
| [`FurnitureStats`](Miscellaneous.md#object-furniturestats) | Object | Applies the 'FurnitureStats' effect. | 1 ||
| `GasCanBehavior` | Integer | Applies or references the 'GasCanBehavior' effect/state. | 1 ||
| `GasCloudBehavior2` | Integer | Applies or references the 'GasCloudBehavior2' effect/state. | 1 ||
| `GeminiTwin` | Integer | Applies or references the 'GeminiTwin' effect/state. | 1 ||
| [`GirlDino`](#object-girldino) | Object || 1 ||
| [`GirlDinoCry`](#object-girldinocry) | Object || 1 ||
| `GiveBoundItemToTarget` | Integer | Applies or references the 'GiveBoundItemToTarget' effect/state. | 1 ||
| `GlobalFamiliarDamageBoost` | Integer | Examples: `1` | 1 ||
| `GlobalFamiliarMoveBoost` | Integer | Examples: `1` | 1 ||
| [`GlobalFlowerTrapperAura`](Miscellaneous.md#object-globalflowertrapperaura) | Object | Examples: `{ ... }` | 1 ||
| `GlobalHealthRegenAura` | Integer | Examples: `3` | 1 ||
| `GlobalManaDrainAura` | Integer | Applies or references the 'GlobalManaDrainAura' effect/state. | 1 ||
| [`GlobalMeleeRevengeDamage`](Items_and_Equipment.md#object-globalmeleerevengedamage) | Object | Applies or references the 'GlobalMeleeRevengeDamage' effect/state. | 1 ||
| [`GlobalSpawnCharacter`](./Enums.md#enum-globalspawncharacter) | Enum | Applies or references the 'GlobalSpawnCharacter' effect/state. | 1 ||
| `GoopImmunity` | Integer | Applies or references the 'GoopImmunity' effect/state. | 1 ||
| `grub_familiar` | Variable || 1 ||
| [`Guillotina2Body`](#object-guillotina2body) | Object || 1 ||
| [`Guillotina2Head`](#object-guillotina2head) | Object || 1 ||
| [`Guillotina3Body`](#object-guillotina3body) | Object || 1 ||
| [`Guillotina3Head`](#object-guillotina3head) | Object || 1 ||
| `GuillotinaDeathHead` | Integer | Applies or references the 'GuillotinaDeathHead' effect/state. | 1 ||
| [`HarpoonTrapPassive`](./Enums.md#enum-harpoontrappassive) | Enum | Applies or references the 'HarpoonTrapPassive' effect/state. | 1 ||
| [`HCHumanDie`](#object-hchumandie) | Object || 1 ||
| [`HealNeighborsEachTurn`](Characters_and_Bosses.md#object-healneighborseachturn) | Object | Passive: Restores health to adjacent allies at the start of the turn. | 1 ||
| `HealPercentMaxHP` | Integer | Applies or references the 'HealPercentMaxHP' effect/state. | 1 ||
| `HealTo` | Integer | Applies or references the 'HealTo' effect/state. | 1 ||
| `HeatWave` | Integer | Examples: `1` | 1 ||
| `HeavyHits` | Integer | Applies or references the 'HeavyHits' effect/state. | 1 ||
| [`HemBounce`](#object-hembounce) | Object || 1 ||
| `HiddenDoomed` | Integer | Applies or references the 'HiddenDoomed' effect/state. | 1 ||
| [`HideEquipment`](./Enums.md#enum-hideequipment) | Enum | Applies or references the 'HideEquipment' effect/state. | 1 ||
| `HideSomeHudStuff` | Integer | Applies or references the 'HideSomeHudStuff' effect/state. | 1 ||
| [`HitlerExecute`](Characters_and_Bosses.md#object-hitlerexecute) | Object | Boss Logic: Specific execution or ultimate attack state. | 1 ||
| [`HPAltStates`](Characters_and_Bosses.md#object-hpaltstates) | Object | Visual: Alternative sprite states based on current health. | 1 ||
| `Hypomania` | Integer | Applies the 'Hypomania' effect. | 1 ||
| `IceBlockBehavior` | Integer | Applies or references the 'IceBlockBehavior' effect/state. | 1 ||
| [`IDSprout`](#object-idsprout) | Object || 1 ||
| `IgnoreDebuffs` | Integer | Applies or references the 'IgnoreDebuffs' effect/state. | 1 ||
| [`IncAuxCounterCycle`](Abilities_and_Spells.md#object-incauxcountercycle) | Object | Increments a generic auxiliary counter, looping back to 0 when it exceeds the maximum. | 1 ||
| `IncreaseCumulativeBlastDamage` | Integer | Applies or references the 'IncreaseCumulativeBlastDamage' effect/state. | 1 ||
| `IncreaseItemAuxOnKill` | Integer | Applies or references the 'IncreaseItemAuxOnKill' effect/state. | 1 ||
| `InheritSpawnerStats` | Integer | Applies or references the 'InheritSpawnerStats' effect/state. | 1 ||
| [`insane`](Miscellaneous.md#object-insane) | Object | Examples: `{ ... }` | 1 ||
| `InsertIntoBackgroundPlaceholder` | Integer | Applies or references the 'InsertIntoBackgroundPlaceholder' effect/state. | 1 ||
| `InterchangeDisabler` | Integer | Applies or references the 'InterchangeDisabler' effect/state. | 1 ||
| `InterchangeMoveActPoints` | Integer | Applies or references the 'InterchangeMoveActPoints' effect/state. | 1 ||
| `InvertBrainFaction` | Integer | Applies the 'InvertBrainFaction' effect. | 1 ||
| `Invulnerable` | Integer | Applies or references the 'Invulnerable' effect/state. | 1 ||
| `JesterLevelUpRerolls` | Integer | Applies or references the 'JesterLevelUpRerolls' effect/state. | 1 ||
| [`JohnnyNeedsWashing`](Characters_and_Bosses.md#object-johnnyneedswashing) | Object | Character Form: Behavior and stats for the 'JohnnyNeedsWashing' state. | 1 ||
| [`JohnnyWasher`](./Enums.md#enum-johnnywasher) | Enum | Applies or references the 'JohnnyWasher' effect/state. | 1 ||
| `JudgementDay` | Integer | Examples: `25` | 1 ||
| [`KnockbackIfCrit`](#object-knockbackifcrit) | Object | Applies or references the 'KnockbackIfCrit' effect/state. | 1 ||
| [`LegacySpawnSavedCatIfExists`](./Enums.md#enum-legacyspawnsavedcatifexists) | Enum | Applies or references the 'LegacySpawnSavedCatIfExists' effect/state. | 1 ||
| [`LennyCatDies`](#object-lennycatdies) | Object || 1 ||
| [`LimitedTileTrail`](./Enums.md#enum-limitedtiletrail) | Enum | Applies the 'LimitedTileTrail' effect. | 1 ||
| `LimitSelfKnockbackDamage` | Integer | Applies the 'LimitSelfKnockbackDamage' effect. | 1 ||
| [`LockOrientationFaceTile`](./Arrays.md#array-lockorientationfacetile) | Array | Applies or references the 'LockOrientationFaceTile' effect/state. | 1 ||
| `LowGravityKnockbackBoost` | Integer | Examples: `1` | 1 ||
| `LowGravityRangeBoost` | Integer | Examples: `2` | 1 ||
| `MadnessChanceOnTurnBegin` | Integer | Applies or references the 'MadnessChanceOnTurnBegin' effect/state. | 1 ||
| `MakeWeaponUnbreakable` | Integer | Applies or references the 'MakeWeaponUnbreakable' effect/state. | 1 ||
| [`ManaGainRange`](#object-managainrange) | Object | Applies or references the 'ManaGainRange' effect/state. | 1 ||
| `ManaStealToHealth` | Integer | Applies or references the 'ManaStealToHealth' effect/state. | 1 ||
| `ManglerAttack` | Integer | Applies or references the 'ManglerAttack' effect/state. | 1 ||
| [`ManglerEnrage`](#object-manglerenrage) | Object || 1 ||
| [`ManglerMonsterDashAttack`](#object-manglermonsterdashattack) | Object || 1 ||
| [`ManglerMonsterPassive`](./Enums.md#enum-manglermonsterpassive) | Enum | Applies or references the 'ManglerMonsterPassive' effect/state. | 1 ||
| `ManglerShuffle` | Boolean | Applies or references the 'ManglerShuffle' effect/state. | 1 ||
| [`ManglersMonster`](#object-manglersmonster) | Object || 1 ||
| `MassAttackThis` | Integer | Applies or references the 'MassAttackThis' effect/state. | 1 ||
| `MaxAccuracy` | Integer | Applies the 'MaxAccuracy' effect. | 1 ||
| `MaxStartingMana` | Integer | Applies the 'MaxStartingMana' effect. | 1 ||
| `Meaty` | Integer | Applies or references the 'Meaty' effect/state. | 1 ||
| [`MechExplode`](#object-mechexplode) | Object || 1 ||
| [`MegaDinoDropController`](Characters_and_Bosses.md#object-megadinodropcontroller) | Object | Boss Logic: Manages loot drops for the Mega Dino. | 1 ||
| [`MegaFart`](#object-megafart) | Object || 1 ||
| [`MegaGuppy_SummonTheChild`](#object-megaguppy_summonthechild) | Object || 1 ||
| [`MergeDamageInstance`](Abilities_and_Spells.md#object-mergedamageinstance) | Object | Combines damage numbers or visual hit effects. | 1 ||
| `MeteorShower` | Integer | Examples: `25` | 1 ||
| `MimicMetronome` | Integer | Applies or references the 'MimicMetronome' effect/state. | 1 ||
| `ModelingClayPassive` | Integer | Applies or references the 'ModelingClayPassive' effect/state. | 1 ||
| [`ModularPickup`](Characters_and_Bosses.md#object-modularpickup) | Object | Pickup Logic: Defines what happens when a modular item is collected. | 1 ||
| [`MonkCatReactionAbilities`](Characters_and_Bosses.md#object-monkcatreactionabilities) | Object | Reaction: Specific counter-attack or dodge abilities used by the Monk class. | 1 ||
| [`MoonHead_KillHands`](#object-moonhead_killhands) | Object || 1 ||
| [`MoonHeadCrackedVisual`](./Enums.md#enum-moonheadcrackedvisual) | Enum | Applies or references the 'MoonHeadCrackedVisual' effect/state. | 1 ||
| [`MotherGrowController`](Characters_and_Bosses.md#object-mothergrowcontroller) | Object | Boss Logic: Manages the growth phases of the Mother boss. | 1 ||
| `MotherTumorDebugForcePass` | Integer | Applies or references the 'MotherTumorDebugForcePass' effect/state. | 1 ||
| [`MotherTumorPassive`](Characters_and_Bosses.md#object-mothertumorpassive) | Object | Boss Logic: Passive effects applied to the Mother's tumors. | 1 ||
| [`Mount`](Characters_and_Bosses.md#object-mount) | Object | Character Form: Behavior and stats for the 'Mount' state. | 1 ||
| [`MoveAfterAnyAttemptedAttack`](Characters_and_Bosses.md#object-moveafteranyattemptedattack) | Object | AI Movement: Forces a move action immediately after attacking, even if it missed. | 1 ||
| [`MoveAwayWhenEnemyAdjacent`](Characters_and_Bosses.md#object-moveawaywhenenemyadjacent) | Object | AI Movement: Moves away if an enemy enters an adjacent tile. | 1 ||
| `MulticatHeads` | Integer | Applies or references the 'MulticatHeads' effect/state. | 1 ||
| `MultiplyCoinsOnBattleStart` | Integer | Applies or references the 'MultiplyCoinsOnBattleStart' effect/state. | 1 ||
| `MultiplyReceivedHealing` | Integer | Applies or references the 'MultiplyReceivedHealing' effect/state. | 1 ||
| [`MultiSpawnOnDeath`](Characters_and_Bosses.md#object-multispawnondeath) | Object | Event Trigger: Spawns multiple entities upon death. | 1 ||
| `MutateAfterXTurns` | Integer | Applies or references the 'MutateAfterXTurns' effect/state. | 1 ||
| `Muted` | Integer | Applies or references the 'Muted' effect/state. | 1 ||
| `MuteDemonicGlyphDisplay` | Integer | Applies or references the 'MuteDemonicGlyphDisplay' effect/state. | 1 ||
| `NextAbilityHeals` | Integer | Applies or references the 'NextAbilityHeals' effect/state. | 1 ||
| `NextActionLuckUp` | Integer | Applies or references the 'NextActionLuckUp' effect/state. | 1 ||
| [`NextBasicAttackCritsThisTurn`](Abilities_and_Spells.md#object-nextbasicattackcritsthisturn) | Object | Guarantees the next basic attack executed this turn will be a critical hit. | 1 ||
| [`NextBattleStatusStacks`](Abilities_and_Spells.md#object-nextbattlestatusstacks) | Object | Carries over the specified status effects into the next encounter/battle. | 1 ||
| `NextDamageReduceAndHealAllies` | Integer | Applies or references the 'NextDamageReduceAndHealAllies' effect/state. | 1 ||
| `NextTurnDoubleRangedDamage` | Integer | Applies or references the 'NextTurnDoubleRangedDamage' effect/state. | 1 ||
| [`NoHead`](#object-nohead) | Object || 1 ||
| [`NonChampionFlySwarm`](#object-nonchampionflyswarm) | Object || 1 ||
| `NonLethal` | Integer | Applies the 'NonLethal' effect. | 1 ||
| [`Nubs`](#object-nubs) | Object || 1 ||
| [`NubsGoop`](#object-nubsgoop) | Object || 1 ||
| [`ObjectDetector`](Items_and_Equipment.md#object-objectdetector) | Object | Applies or references the 'ObjectDetector' effect/state. | 1 ||
| [`ObjectOnHitFullyEmpty`](./Enums.md#enum-objectonhitfullyempty) | Enum | Applies or references the 'ObjectOnHitFullyEmpty' effect/state. | 1 ||
| [`Ornstein`](#object-ornstein) | Object || 1 ||
| `OrthogonalAIDangerZone` | Integer | Applies or references the 'OrthogonalAIDangerZone' effect/state. | 1 ||
| `OverHealToShield` | Integer | Applies or references the 'OverHealToShield' effect/state. | 1 ||
| `OverManaReducesManaCosts` | Integer | Examples: `1` | 1 ||
| `OverrideMaxMana` | Integer | Applies the 'OverrideMaxMana' effect. | 1 ||
| `OverridePalette` | Integer | Applies the 'OverridePalette' effect. | 1 ||
| `PackHunting` | Integer | Applies or references the 'PackHunting' effect/state. | 1 ||
| [`Paranoia`](./Enums.md#enum-paranoia) | Enum | Applies the 'Paranoia' effect. | 1 ||
| [`PassiveLevelScaledStatus`](Miscellaneous.md#object-passivelevelscaledstatus) | Object | Applies the 'PassiveLevelScaledStatus' effect. | 1 ||
| [`PassiveWhileHasDurability`](Items_and_Equipment.md#object-passivewhilehasdurability) | Object | Applies or references the 'PassiveWhileHasDurability' effect/state. | 1 ||
| [`PassiveWhileNotTakingTurn`](Abilities_and_Spells.md#object-passivewhilenottakingturn) | Object | Grants nested passives that are only active while it is NOT the character's turn. | 1 ||
| [`PassiveWhileShielded`](Items_and_Equipment.md#object-passivewhileshielded) | Object | Applies or references the 'PassiveWhileShielded' effect/state. | 1 ||
| `PercentHeal` | Integer | Applies the 'PercentHeal' effect. | 1 ||
| `PermanentConfusion` | Number | Applies or references the 'PermanentConfusion' effect/state. | 1 ||
| `PermanentImmobile` | Integer | Applies or references the 'PermanentImmobile' effect/state. | 1 ||
| `PermanentKitten` | Integer | Applies the 'PermanentKitten' effect. | 1 ||
| `PermanentUpgradeRandomActiveOrPassive` | Integer | Applies or references the 'PermanentUpgradeRandomActiveOrPassive' effect/state. | 1 ||
| [`PersistentElement`](./Enums.md#enum-persistentelement) | Enum | Examples: `Holy` | 1 ||
| `PhysicalAttacksMiss` | Integer | Applies or references the 'PhysicalAttacksMiss' effect/state. | 1 ||
| `pickup` | Variable || 1 ||
| `plant` | Variable || 1 ||
| [`PoolMetronome`](Abilities_and_Spells.md#object-poolmetronome) | Object | Executes a random ability drawn from a specific pool. | 1 ||
| `PreEmptiveCounterNextAttacks` | Integer | Applies or references the 'PreEmptiveCounterNextAttacks' effect/state. | 1 ||
| [`PreventSpecificInjury`](./Enums.md#enum-preventspecificinjury) | Enum | Applies or references the 'PreventSpecificInjury' effect/state. | 1 ||
| [`QueueUseAbility`](./Enums.md#enum-queueuseability) | Enum | Applies or references the 'QueueUseAbility' effect/state. | 1 ||
| `RandomKnockbackDirection` | Integer | Applies or references the 'RandomKnockbackDirection' effect/state. | 1 ||
| [`RandomPermanentStatsDistinct`](#object-randompermanentstatsdistinct) | Object | Examples: `{ ... }` | 1 ||
| [`RandomWeatherEachFight`](./Arrays.md#array-randomweathereachfight) | Array | Examples: `[ Fog Rain Windy Sandstorm HeatWave Snow Thunderstorm Bli...` | 1 ||
| `RealTimePressure_OneUnit` | Integer | Applies the 'RealTimePressure_OneUnit' effect. | 1 ||
| [`ReceivedStatusReplacement`](./Arrays.md#array-receivedstatusreplacement) | Array | Examples: `[ Sleep SleepParalysis ]` | 1 ||
| `ReclaimItemOnBreak` | Integer | Applies or references the 'ReclaimItemOnBreak' effect/state. | 1 ||
| `ReduceManaCostExcludeBrainstorm` | Integer | Applies or references the 'ReduceManaCostExcludeBrainstorm' effect/state. | 1 ||
| `ReduceSpellCostsPerDisorder` | Integer | Applies or references the 'ReduceSpellCostsPerDisorder' effect/state. | 1 ||
| `ReduceSpellCostsPerParasite` | Integer | Applies or references the 'ReduceSpellCostsPerParasite' effect/state. | 1 ||
| `ReformMoonHead` | Integer | Applies or references the 'ReformMoonHead' effect/state. | 1 ||
| `RefreshItemAbilities` | Integer | Applies or references the 'RefreshItemAbilities' effect/state. | 1 ||
| `RefreshNonManaItemAbilities` | Integer | Applies or references the 'RefreshNonManaItemAbilities' effect/state. | 1 ||
| `RefreshOncePerFightAbilities` | Integer | Applies or references the 'RefreshOncePerFightAbilities' effect/state. | 1 ||
| `ReloadOnAllyCatDies` | Integer | Applies or references the 'ReloadOnAllyCatDies' effect/state. | 1 ||
| `ReloadOnAllyDies` | Integer | Applies or references the 'ReloadOnAllyDies' effect/state. | 1 ||
| `ReloadOnAnyDamage` | Integer | Applies or references the 'ReloadOnAnyDamage' effect/state. | 1 ||
| `ReloadOnBackstab` | Integer | Applies or references the 'ReloadOnBackstab' effect/state. | 1 ||
| [`ReloadOnElementalDamageReceived`](./Enums.md#enum-reloadonelementaldamagereceived) | Enum | Applies or references the 'ReloadOnElementalDamageReceived' effect/state. | 1 ||
| `ReloadOnGainCoins` | Integer | Applies or references the 'ReloadOnGainCoins' effect/state. | 1 ||
| `ReloadOnGainDivineShield` | Integer | Applies or references the 'ReloadOnGainDivineShield' effect/state. | 1 ||
| [`ReloadOnKillTagged`](./Enums.md#enum-reloadonkilltagged) | Enum | Applies or references the 'ReloadOnKillTagged' effect/state. | 1 ||
| `ReloadOnSpendMana` | Integer | Applies or references the 'ReloadOnSpendMana' effect/state. | 1 ||
| `ReloadOnUseAbilityWithManaCost` | Integer | Applies or references the 'ReloadOnUseAbilityWithManaCost' effect/state. | 1 ||
| `RemoteFlatLeech` | Integer | Applies or references the 'RemoteFlatLeech' effect/state. | 1 ||
| [`RemoveAmbientLightEffects`](./Enums.md#enum-removeambientlighteffects) | Float | Applies or references the 'RemoveAmbientLightEffects' effect/state. | 1 ||
| `RemoveExtraDispersedTurn` | Integer | Examples: `1` | 1 ||
| [`RemoveGlobalModifiers`](./Arrays.md#array-removeglobalmodifiers) | Array | Applies or references the 'RemoveGlobalModifiers' effect/state. | 1 ||
| `RepairAllCondition` | Integer | Applies or references the 'RepairAllCondition' effect/state. | 1 ||
| [`ReplaceBlankTilesOnBattleStart`](./Enums.md#enum-replaceblanktilesonbattlestart) | Enum | Applies or references the 'ReplaceBlankTilesOnBattleStart' effect/state. | 1 ||
| `RerollEnemy` | Integer | Applies or references the 'RerollEnemy' effect/state. | 1 ||
| `RerollItemsOnBattleEnd` | Integer | Applies or references the 'RerollItemsOnBattleEnd' effect/state. | 1 ||
| `ReturnDinoLegs` | Integer | Applies or references the 'ReturnDinoLegs' effect/state. | 1 ||
| `RNGCannonRandomDamage` | Integer | Applies or references the 'RNGCannonRandomDamage' effect/state. | 1 ||
| [`RockyArmorSalvage`](./Enums.md#enum-rockyarmorsalvage) | Float | Examples: `.75` | 1 ||
| `RunWhenKittensDead` | Integer | Applies or references the 'RunWhenKittensDead' effect/state. | 1 ||
| [`RunWhenLastPlayerCatIsCharmed`](Characters_and_Bosses.md#object-runwhenlastplayercatischarmed) | Object | AI Logic: Flee logic when the player team is entirely crowd-controlled. | 1 ||
| [`SandStormBuff`](#object-sandstormbuff) | Variable || 1 ||
| [`ScaldingOrbMoonBossOneShot`](Items_and_Equipment.md#object-scaldingorbmoonbossoneshot) | Object | Applies or references the 'ScaldingOrbMoonBossOneShot' effect/state. | 1 ||
| [`ScaledStatusAlliesOnSpendMana`](Items_and_Equipment.md#object-scaledstatusalliesonspendmana) | Object | Applies or references the 'ScaledStatusAlliesOnSpendMana' effect/state. | 1 ||
| [`ScaledStatusOnBleedDamage`](Miscellaneous.md#object-scaledstatusonbleeddamage) | Object | Applies the 'ScaledStatusOnBleedDamage' effect. | 1 ||
| [`ScaledStatusOnHolyShieldBlock`](Items_and_Equipment.md#object-scaledstatusonholyshieldblock) | Object | Applies or references the 'ScaledStatusOnHolyShieldBlock' effect/state. | 1 ||
| [`ScalingAttackAnimation`](Characters_and_Bosses.md#object-scalingattackanimation) | Object | Visual: Animation scales based on damage output. | 1 ||
| `SchizoIllusionAIModifier` | Integer | Applies or references the 'SchizoIllusionAIModifier' effect/state. | 1 ||
| `SchrodingerDisorder` | Integer | Applies the 'SchrodingerDisorder' effect. | 1 ||
| `Scleroderma` | Integer | Applies the 'Scleroderma' effect. | 1 ||
| [`ScrambleLastUsedSpell`](Abilities_and_Spells.md#object-scramblelastusedspell) | Object | Randomizes or scrambles the properties of the last spell cast. | 1 ||
| [`self_status_next_fight`](Events_and_Encounters.md#object-self_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 1 ||
| [`SelfDamageWhenDealDamage`](Miscellaneous.md#object-selfdamagewhendealdamage) | Object | Applies the 'SelfDamageWhenDealDamage' effect. | 1 ||
| [`set_WitchJump`](#object-set_witchjump) | Object || 1 ||
| [`SetAnimationAlts`](Abilities_and_Spells.md#object-setanimationalts) | Object | Overrides specific animation states with alternative animations. | 1 ||
| [`SetFaction`](./Enums.md#enum-setfaction) | Enum | Applies or references the 'SetFaction' effect/state. | 1 ||
| `ShadowCrit` | Integer | Applies or references the 'ShadowCrit' effect/state. | 1 ||
| [`ShineBuff`](#object-shinebuff) | Variable || 1 ||
| `ShootHereCommand` | Integer | Applies or references the 'ShootHereCommand' effect/state. | 1 ||
| `ShootHereReceiver` | Integer | Applies or references the 'ShootHereReceiver' effect/state. | 1 ||
| [`Shove`](#object-shove) | Object || 1 ||
| [`SkipFirstRounds`](Characters_and_Bosses.md#object-skipfirstrounds) | Object | AI Logic: Passes turn for the first X rounds of combat. | 1 ||
| [`SleepDart`](#object-sleepdart) | Object || 1 ||
| `SleepParalysis` | Variable || 1 ||
| `SmallHitExplosion` | Integer | Applies or references the 'SmallHitExplosion' effect/state. | 1 ||
| [`SmokeBuff`](#object-smokebuff) | Variable || 1 ||
| [`Smough`](#object-smough) | Object || 1 ||
| `Snow` | Integer | Examples: `{ ... }` | 1 ||
| [`Snow`](#object-snow) | Number / Object || 1 | `1` (Number), `{ ... }` (Object) |
| [`SolarFlare`](#object-solarflare) | Object | Examples: `{ ... }` | 1 ||
| [`SoundEventOnHit`](./Enums.md#enum-soundeventonhit) | Enum | Applies or references the 'SoundEventOnHit' effect/state. | 1 ||
| [`SourceSwapsBackEndOfTurn`](./Enums.md#enum-sourceswapsbackendofturn) | Enum | Applies or references the 'SourceSwapsBackEndOfTurn' effect/state. | 1 ||
| `SpawnCatCloneOnCorpsePopped` | Integer | Applies or references the 'SpawnCatCloneOnCorpsePopped' effect/state. | 1 ||
| `SpawnCreepOnHitKnockback` | Integer | Applies or references the 'SpawnCreepOnHitKnockback' effect/state. | 1 ||
| `spawner` | Variable || 1 ||
| `SpawnerCatDataReference` | Integer | Applies or references the 'SpawnerCatDataReference' effect/state. | 1 ||
| [`SpawnRandomPickupsOnTaggedUnitKilled`](Items_and_Equipment.md#object-spawnrandompickupsontaggedunitkilled) | Object | Applies or references the 'SpawnRandomPickupsOnTaggedUnitKilled' effect/state. | 1 ||
| [`SpawnTilePuddleOnBattleStart`](#object-spawntilepuddleonbattlestart) | Object | Examples: `{ ... }` | 1 ||
| `SpawnWebTrap` | Integer | Applies or references the 'SpawnWebTrap' effect/state. | 1 ||
| [`SpecialBossMultipartInstakill`](./Enums.md#enum-specialbossmultipartinstakill) | Enum | Applies or references the 'SpecialBossMultipartInstakill' effect/state. | 1 ||
| `SpeedUp_WithoutInitiative` | Integer | Applies or references the 'SpeedUp_WithoutInitiative' effect/state. | 1 ||
| `SpellShield` | Integer | Applies or references the 'SpellShield' effect/state. | 1 ||
| [`SpewerAltGraphics`](Characters_and_Bosses.md#object-speweraltgraphics) | Object | Visual: Alternative graphics for Spewer enemies. | 1 ||
| [`SpiderReturn`](#object-spiderreturn) | Object || 1 ||
| `SpitConsumed` | Integer | Applies or references the 'SpitConsumed' effect/state. | 1 ||
| `SpreadWater` | Integer | Applies or references the 'SpreadWater' effect/state. | 1 ||
| `sprout` | Variable || 1 ||
| `SproutsGrantMovement` | Integer | Applies or references the 'SproutsGrantMovement' effect/state. | 1 ||
| [`StacyMutant_Brace`](Characters_and_Bosses.md#object-stacymutant_brace) | Object | Character Form: Behavior and stats for the 'StacyMutant_Brace' state. | 1 ||
| [`StacyMutant_Counter`](Characters_and_Bosses.md#object-stacymutant_counter) | Object | Character Form: Behavior and stats for the 'StacyMutant_Counter' state. | 1 ||
| [`StacyMutant_Damage`](Characters_and_Bosses.md#object-stacymutant_damage) | Object | Character Form: Behavior and stats for the 'StacyMutant_Damage' state. | 1 ||
| [`StacyMutant_DoubleHead`](Characters_and_Bosses.md#object-stacymutant_doublehead) | Object | Character Form: Behavior and stats for the 'StacyMutant_DoubleHead' state. | 1 ||
| [`StacyMutant_Fire`](Characters_and_Bosses.md#object-stacymutant_fire) | Object | Character Form: Behavior and stats for the 'StacyMutant_Fire' state. | 1 ||
| [`StacyMutant_Health`](Characters_and_Bosses.md#object-stacymutant_health) | Object | Character Form: Behavior and stats for the 'StacyMutant_Health' state. | 1 ||
| [`StacyMutant_Holy`](Characters_and_Bosses.md#object-stacymutant_holy) | Object | Character Form: Behavior and stats for the 'StacyMutant_Holy' state. | 1 ||
| [`StacyMutant_Ice`](Characters_and_Bosses.md#object-stacymutant_ice) | Object | Character Form: Behavior and stats for the 'StacyMutant_Ice' state. | 1 ||
| [`StacyMutant_Lightning`](Characters_and_Bosses.md#object-stacymutant_lightning) | Object | Character Form: Behavior and stats for the 'StacyMutant_Lightning' state. | 1 ||
| [`StacyMutant_Mirror`](Characters_and_Bosses.md#object-stacymutant_mirror) | Object | Character Form: Behavior and stats for the 'StacyMutant_Mirror' state. | 1 ||
| [`StacyMutant_Speed`](Characters_and_Bosses.md#object-stacymutant_speed) | Object | Character Form: Behavior and stats for the 'StacyMutant_Speed' state. | 1 ||
| [`StacyMutant_Thorns`](Characters_and_Bosses.md#object-stacymutant_thorns) | Object | Character Form: Behavior and stats for the 'StacyMutant_Thorns' state. | 1 ||
| `StartDead` | Integer | Applies or references the 'StartDead' effect/state. | 1 ||
| `StatBounty` | Integer | Applies or references the 'StatBounty' effect/state. | 1 ||
| [`StatDependentPassive`](Items_and_Equipment.md#object-statdependentpassive) | Object | Applies or references the 'StatDependentPassive' effect/state. | 1 ||
| [`StatusAdjacentOnTheirTurnBegin`](Miscellaneous.md#object-statusadjacentontheirturnbegin) | Object | Event Trigger: Applies nested statuses to adjacent on their turn begin. | 1 ||
| [`StatusAdjacentOnTheirTurnEnd`](Items_and_Equipment.md#object-statusadjacentontheirturnend) | Object | Applies or references the 'StatusAdjacentOnTheirTurnEnd' effect/state. | 1 ||
| [`StatusAfterXStacks`](#object-statusafterxstacks) | Object | Applies or references the 'StatusAfterXStacks' effect/state. | 1 ||
| [`StatusAlliesEachTurn`](Items_and_Equipment.md#object-statusallieseachturn) | Object | Applies or references the 'StatusAlliesEachTurn' effect/state. | 1 ||
| [`StatusEachTurnBeginIfHasStatus`](Characters_and_Bosses.md#object-statuseachturnbeginifhasstatus) | Object | Event Trigger: Applies a status at the start of the turn if a prerequisite status is met. | 1 ||
| [`StatusEachTurnEndIfEnabledAtStartOfTurn`](Characters_and_Bosses.md#object-statuseachturnendifenabledatstartofturn) | Object | Event Trigger: Applies a status at the end of the turn if an enabling condition was met at the start. | 1 ||
| [`StatusIfBattleAlreadyBegan`](Miscellaneous.md#object-statusifbattlealreadybegan) | Object | Event Trigger: Applies nested statuses to if battle already began. | 1 ||
| [`StatusOnDodge`](Items_and_Equipment.md#object-statusondodge) | Object | Event Trigger: Applies statuses when this action occurs. | 1 ||
| [`StatusOnEnemyCastSpell`](Elite_Buffs.md#object-statusonenemycastspell) | Object | Examples: `{ ... }` | 1 ||
| [`StatusOnEnemyConfused`](Characters_and_Bosses.md#object-statusonenemyconfused) | Object | Event Trigger: Applies statuses when an enemy becomes confused. | 1 ||
| [`StatusOnEnemyDeath`](Items_and_Equipment.md#object-statusonenemydeath) | Object | Event Trigger: Applies statuses when this action occurs. | 1 ||
| [`StatusOnFallAsleep`](Items_and_Equipment.md#object-statusonfallasleep) | Object | Event Trigger: Applies statuses when this action occurs. | 1 ||
| [`StatusOnFullMana`](Items_and_Equipment.md#object-statusonfullmana) | Object | Event Trigger: Applies statuses when this action occurs. | 1 ||
| [`StatusOnLoseShield`](Miscellaneous.md#object-statusonloseshield) | Object | Event Trigger: Applies nested statuses when lose shield. | 1 ||
| [`StatusOnTakeHealthDamage`](Miscellaneous.md#object-statusontakehealthdamage) | Object | Event Trigger: Applies nested statuses when take health damage. | 1 ||
| [`StatusOverlappingCharactersAndDie`](Characters_and_Bosses.md#object-statusoverlappingcharactersanddie) | Object | Event Trigger: Applies statuses to overlapping entities, then destroys self. | 1 ||
| [`StatusWhenStatusCompletelyRemoved`](Characters_and_Bosses.md#object-statuswhenstatuscompletelyremoved) | Object | Event Trigger: Applies statuses when a tracked status effect is fully cleansed. | 1 ||
| `StealDemonicGlyph` | Integer | Applies or references the 'StealDemonicGlyph' effect/state. | 1 ||
| [`StealEquipment`](./Enums.md#enum-stealequipment) | Enum | Applies or references the 'StealEquipment' effect/state. | 1 ||
| `StealthCritChance` | Integer | Applies or references the 'StealthCritChance' effect/state. | 1 ||
| `StealthUntilBasicAttack` | Integer | Applies or references the 'StealthUntilBasicAttack' effect/state. | 1 ||
| `StealTurn` | Integer | Applies or references the 'StealTurn' effect/state. | 1 ||
| `StevenBolts` | Integer | Applies or references the 'StevenBolts' effect/state. | 1 ||
| `StrictLimitDamage` | Integer | Applies the 'StrictLimitDamage' effect. | 1 ||
| `StripKnockback` | Integer | Applies or references the 'StripKnockback' effect/state. | 1 ||
| [`SupportDieInsteadOfRun`](Characters_and_Bosses.md#object-supportdieinsteadofrun) | Object | AI Logic: Forces a support unit to die rather than flee. | 1 ||
| [`SwapWeapon`](Abilities_and_Spells.md#object-swapweapon) | Object | Replaces the character's currently equipped weapon with one from a specified pool. | 1 ||
| [`SwimmingFormChange`](Characters_and_Bosses.md#object-swimmingformchange) | Object | Logic: Automates form change when entering/exiting water. | 1 ||
| [`SyncFormsWithBuddy`](Characters_and_Bosses.md#object-syncformswithbuddy) | Object | Logic: Forces this character's form to match their familiar/buddy. | 1 ||
| `T2CopyCatInternal` | Variable || 1 ||
| [`T3HitlerSpawningPhase`](Characters_and_Bosses.md#object-t3hitlerspawningphase) | Object | Boss Logic: Minion spawn phase for the T3 Hitler boss. | 1 ||
| `T3HitlerTriggerInitialSpawns` | Integer | Applies or references the 'T3HitlerTriggerInitialSpawns' effect/state. | 1 ||
| [`TagMetronome`](./Enums.md#enum-tagmetronome) | Enum | Applies or references the 'TagMetronome' effect/state. | 1 ||
| [`TakeBonusTurnWithStatus`](Abilities_and_Spells.md#object-takebonusturnwithstatus) | Object | Grants the character an immediate extra turn while afflicted with specific statuses. | 1 ||
| `TakeExtraTurnEndOfRound` | Integer | Applies or references the 'TakeExtraTurnEndOfRound' effect/state. | 1 ||
| `TakeWeaponFromSpawner` | Integer | Applies or references the 'TakeWeaponFromSpawner' effect/state. | 1 ||
| `Tall` | Integer | Applies or references the 'Tall' effect/state. | 1 ||
| [`TallTumorManaBurn`](./Enums.md#enum-talltumormanaburn) | Enum | Applies or references the 'TallTumorManaBurn' effect/state. | 1 ||
| `TargetedMetronome` | Integer | Applies or references the 'TargetedMetronome' effect/state. | 1 ||
| [`TattersFear`](#object-tattersfear) | Object || 1 ||
| `TauntAtFullHealth` | Integer | Applies the 'TauntAtFullHealth' effect. | 1 ||
| `Taunting` | Integer | Applies or references the 'Taunting' effect/state. | 1 ||
| [`TC_DashReaction`](#object-tc_dashreaction) | Object || 1 ||
| [`TeamBonusAbility`](./Enums.md#enum-teambonusability) | Enum | Applies or references the 'TeamBonusAbility' effect/state. | 1 ||
| [`TeleportBackAtTurnEnd`](./Enums.md#enum-teleportbackatturnend) | Enum | Applies or references the 'TeleportBackAtTurnEnd' effect/state. | 1 ||
| `TempBackstab` | Integer | Applies or references the 'TempBackstab' effect/state. | 1 ||
| `TempBackstabBleed` | Integer | Applies or references the 'TempBackstabBleed' effect/state. | 1 ||
| `TempBackstabPiercing` | Integer | Applies or references the 'TempBackstabPiercing' effect/state. | 1 ||
| `TempBackstabPoison` | Integer | Applies or references the 'TempBackstabPoison' effect/state. | 1 ||
| `TempBasicAttackBonusAOE` | Integer | Applies or references the 'TempBasicAttackBonusAOE' effect/state. | 1 ||
| `TempBonusKnockback` | Integer | Applies or references the 'TempBonusKnockback' effect/state. | 1 ||
| `TempBonusKnockbackDamage` | Integer | Applies or references the 'TempBonusKnockbackDamage' effect/state. | 1 ||
| `TempInjuryImmunity` | Integer | Applies or references the 'TempInjuryImmunity' effect/state. | 1 ||
| `TempManaCostReduction` | Integer | Applies or references the 'TempManaCostReduction' effect/state. | 1 ||
| `TempMeleeRangeUp` | Integer | Applies or references the 'TempMeleeRangeUp' effect/state. | 1 ||
| `TempPenetrate` | Integer | Applies or references the 'TempPenetrate' effect/state. | 1 ||
| `TempPreEmptiveCounterAttack` | Integer | Applies or references the 'TempPreEmptiveCounterAttack' effect/state. | 1 ||
| [`Terminator2Chase`](./Enums.md#enum-terminator2chase) | Enum | Applies or references the 'Terminator2Chase' effect/state. | 1 ||
| [`Terminator2Run`](Characters_and_Bosses.md#object-terminator2run) | Object | AI Movement: Specific run logic for Terminator2. | 1 ||
| [`TerminatorChase`](Characters_and_Bosses.md#object-terminatorchase) | Object | AI Movement: Specific chase logic for Terminator. | 1 ||
| [`TerminatorSkin`](Characters_and_Bosses.md#object-terminatorskin) | Object | Visual: Skin definition for Terminator. | 1 ||
| [`TheCreator_SpawnCloneTeam`](#object-thecreator_spawncloneteam) | Object || 1 ||
| [`TheHunger`](Miscellaneous.md#object-thehunger) | Object | Applies the 'TheHunger' effect. | 1 ||
| [`ThornUp`](#object-thornup) | Object || 1 ||
| [`ThrobbingKing2`](#object-throbbingking2) | Object || 1 ||
| [`TickDownStatus`](./Enums.md#enum-tickdownstatus) | Enum | Applies or references the 'TickDownStatus' effect/state. | 1 ||
| [`TileElementDamageImmunity`](./Enums.md#enum-tileelementdamageimmunity) | Enum | Applies or references the 'TileElementDamageImmunity' effect/state. | 1 ||
| `TilesMovedToCritChance` | Integer | Applies or references the 'TilesMovedToCritChance' effect/state. | 1 ||
| `TilesMovedToMana` | Integer | Applies or references the 'TilesMovedToMana' effect/state. | 1 ||
| [`TilesMovedToNeighborHeal`](./Enums.md#enum-tilesmovedtoneighborheal) | Enum | Applies or references the 'TilesMovedToNeighborHeal' effect/state. | 1 ||
| `TilesMovedToStrength` | Integer | Applies or references the 'TilesMovedToStrength' effect/state. | 1 ||
| [`TintItem`](Items_and_Equipment.md#object-tintitem) | Object | Applies or references the 'TintItem' effect/state. | 1 ||
| `TireBehavior` | Integer | Applies or references the 'TireBehavior' effect/state. | 1 ||
| `TormentorHeal` | Integer | Applies or references the 'TormentorHeal' effect/state. | 1 ||
| [`TormentorRuneAbsorb`](#object-tormentorruneabsorb) | Object || 1 ||
| `TossTargetIsAggroTarget` | Integer | Applies or references the 'TossTargetIsAggroTarget' effect/state. | 1 ||
| `TossTargetIsBuddy` | Integer | Applies or references the 'TossTargetIsBuddy' effect/state. | 1 ||
| `TossTargetIsNotInWater` | Integer | Applies or references the 'TossTargetIsNotInWater' effect/state. | 1 ||
| [`TourettesMeows`](Miscellaneous.md#object-tourettesmeows) | Object | Applies the 'TourettesMeows' effect. | 1 ||
| `TowerDefenseStatus` | Integer | Applies or references the 'TowerDefenseStatus' effect/state. | 1 ||
| `TowerDefenseStatus2` | Integer | Applies or references the 'TowerDefenseStatus2' effect/state. | 1 ||
| [`ToxicBubbles`](#object-toxicbubbles) | Variable || 1 ||
| [`ToxPuff`](#object-toxpuff) | Object || 1 ||
| [`TrackAmountKilledByPlayer`](./Enums.md#enum-trackamountkilledbyplayer) | Enum | Applies or references the 'TrackAmountKilledByPlayer' effect/state. | 1 ||
| [`TransformBasicMove`](./Enums.md#enum-transformbasicmove) | Enum | Applies or references the 'TransformBasicMove' effect/state. | 1 ||
| [`TransformEquipment`](Abilities_and_Spells.md#object-transformequipment) | Object | Upgrades or transforms a specific equipped item into another. | 1 ||
| [`TransformNow`](./Enums.md#enum-transformnow) | Enum | Applies or references the 'TransformNow' effect/state. | 1 ||
| [`TransformOnStatusThreshold`](Characters_and_Bosses.md#object-transformonstatusthreshold) | Object | Logic: Changes form when a status effect reaches a certain stack count. | 1 ||
| `Trapper_Status` | Integer | Applies or references the 'Trapper_Status' effect/state. | 1 ||
| [`TrexSwitchTarget`](#object-trexswitchtarget) | Object || 1 ||
| `TriggerBleedOnBleed` | Integer | Examples: `1` | 1 ||
| `TriggerMotherConsume` | Integer | Applies or references the 'TriggerMotherConsume' effect/state. | 1 ||
| `TriggerMotherGrow` | Integer | Applies or references the 'TriggerMotherGrow' effect/state. | 1 ||
| `Triskaidekaphobia` | Integer | Applies the 'Triskaidekaphobia' effect. | 1 ||
| [`TT_Thrash`](#object-tt_thrash) | Object || 1 ||
| `tumor` | Variable || 1 ||
| [`TunnelVision`](Items_and_Equipment.md#object-tunnelvision) | Object | Applies or references the 'TunnelVision' effect/state. | 1 ||
| `TurnAround` | Integer | Applies or references the 'TurnAround' effect/state. | 1 ||
| [`TurnControlDelay`](./Enums.md#enum-turncontroldelay) | Float | Applies or references the 'TurnControlDelay' effect/state. | 1 ||
| `TurnRight` | Integer | Applies or references the 'TurnRight' effect/state. | 1 ||
| `TutorialBossRiggedFight` | Integer | Applies or references the 'TutorialBossRiggedFight' effect/state. | 1 ||
| `TVBotDisableAttack` | Integer | Applies or references the 'TVBotDisableAttack' effect/state. | 1 ||
| `TVBotDisableMove` | Integer | Applies or references the 'TVBotDisableMove' effect/state. | 1 ||
| `TVBotDisableSpells` | Integer | Applies or references the 'TVBotDisableSpells' effect/state. | 1 ||
| [`TVBotScreen`](Characters_and_Bosses.md#object-tvbotscreen) | Object | Visual: TV Bot screen state. | 1 ||
| `Twister_loop` | Enum || 1 ||
| [`TwisterFling`](Characters_and_Bosses.md#object-twisterfling) | Object | Logic: Fling behavior for tornado attacks. | 1 ||
| [`UFO_BigExplode`](#object-ufo_bigexplode) | Object || 1 ||
| [`UltraSmough`](#object-ultrasmough) | Object || 1 ||
| `UndoDamage` | Integer | Applies or references the 'UndoDamage' effect/state. | 1 ||
| [`UnlimitedDeathRattleRevive`](Characters_and_Bosses.md#object-unlimiteddeathrattlerevive) | Object | Logic: Endless resurrection on death. | 1 ||
| `UpTireBehavior` | Integer | Applies or references the 'UpTireBehavior' effect/state. | 1 ||
| [`UseAbility_Madness`](./Enums.md#enum-useability_madness) | Enum | Applies the 'UseAbility_Madness' effect. | 1 ||
| [`UseAbilityWhenOutOfStatus`](Characters_and_Bosses.md#object-useabilitywhenoutofstatus) | Object | Logic: Casts a specific ability the moment a status effect expires. | 1 ||
| [`UseAbilityWhenShieldDepleted`](./Enums.md#enum-useabilitywhenshielddepleted) | Enum | Applies or references the 'UseAbilityWhenShieldDepleted' effect/state. | 1 ||
| [`UseMoveAbilityWithAI`](Abilities_and_Spells.md#object-usemoveabilitywithai) | Object | Forces the character to execute a movement ability using specific AI weights. | 1 ||
| `UseRandomSpell_Madness` | Integer | Applies the 'UseRandomSpell_Madness' effect. | 1 ||
| `VaporizeDice` | Integer | Applies or references the 'VaporizeDice' effect/state. | 1 ||
| [`VisualCountDownThenApplyStatus`](Abilities_and_Spells.md#object-visualcountdownthenapplystatus) | Object | Displays a visual countdown above the target before applying the nested effects. | 1 ||
| [`WaggleClone`](Abilities_and_Spells.md#object-waggleclone) | Object | Spawns visual clones or alternative hitbox variants of the projectile. | 1 ||
| `Wall` | Integer | Applies or references the 'Wall' effect/state. | 1 ||
| `Wet` | Integer | Applies or references the 'Wet' effect/state. | 1 ||
| [`WhitelistPickupType`](./Enums.md#enum-whitelistpickuptype) | Enum | Applies or references the 'WhitelistPickupType' effect/state. | 1 ||
| `WideBackstab` | Integer | Applies or references the 'WideBackstab' effect/state. | 1 ||
| [`Wind`](Engine_LogicKeys.md#object-wind) | Object | Examples: `{ ... }` | 1 ||
| `Windy` | Integer | Examples: `{ ... }` | 1 ||
| [`Windy`](#object-windy) | Number / Object || 1 | `10` (Number), `1` (Number), `{ ... }` (Object) |
| `WispDodge` | Integer | Applies or references the 'WispDodge' effect/state. | 1 ||
| `WobblyCat` | Integer | Applies the 'WobblyCat' effect. | 1 ||
| `XIsConsumedCharacterMaxHP` | Integer | Applies or references the 'XIsConsumedCharacterMaxHP' effect/state. | 1 ||
| `XIsCountDeaths` | Integer | Applies or references the 'XIsCountDeaths' effect/state. | 1 ||
| [`XIsCountStatusStacks`](./Enums.md#enum-xiscountstatusstacks) | Enum | Applies or references the 'XIsCountStatusStacks' effect/state. | 1 ||
| [`XIsFormulaLockedUntilComplete`](./Enums.md#enum-xisformulalockeduntilcomplete) | Enum | Applies or references the 'XIsFormulaLockedUntilComplete' effect/state. | 1 ||
| `XIsIncreaseEachTurn` | Integer | Applies or references the 'XIsIncreaseEachTurn' effect/state. | 1 ||
| `XIsRampAndReset` | Integer | Applies or references the 'XIsRampAndReset' effect/state. | 1 ||
| `XIsRecycleCostReduction` | Integer | Applies or references the 'XIsRecycleCostReduction' effect/state. | 1 ||
| `ZeroKnockbackDamage` | Integer | Applies or references the 'ZeroKnockbackDamage' effect/state. | 1 ||
| [`AcidRain`](#object-acidrain) | Number / Object ||| `2` (Number), `{ ... }` (Object) |
| `Adrenaline` | Integer ||| `[1 .5]` (Array), `10` (Number), `1` (Number), `{ ... }` (Object) |
| `Ammo` | Integer ||| `[1 .5]` (Array), `1` (Number), `6` (Number), `{ ... }` (Object) |
| `Bloodzerked` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`BombRatTurtle`](#object-bombratturtle) | Integer / Object ||| `1` (Number), `{ ... }` (Object) |
| `BounceRock` | Array / Enum ||| `[1 .2]` (Array), `LavaBoulder` (Enum), `SmallRock` (Enum) |
| [`ButterflySwarm`](#object-butterflyswarm) | Number / Object ||| `2` (Number), `{ ... }` (Object) |
| `ChampionUpgradeNextMinion` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`CockroachSwarm`](#object-cockroachswarm) | Number / Object ||| `1` (Number), `{ ... }` (Object) |
| `CollideWithConsumed` | String ||| `5+bonus_melee_damage` (Enum), `4+bonus_melee_damage` (Enum) |
| [`CopySpells`](Abilities_and_Spells.md#object-copyspells) | Integer / Object ||| `1` (Number), `{ ... }` (Object) |
| [`Counterspell`](#object-counterspell) | Integer / Object ||| `1` (Number), `{ ... }` (Object) |
| [`DelayCastAbility`](Abilities_and_Spells.md#object-delaycastability) | Enum / Object ||| `HitlerNuke` (Enum), `{ ... }` (Object) |
| [`DelayCastAbility`](Abilities_and_Spells.md#object-delaycastability) | Enum / Object ||| `HitlerNuke` (Enum), `{ ... }` (Object) |
| `DoubleCast` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `DoubleCastSpell` | Integer ||| `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `EliteUpgradeNextMinion` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`FactionUprising`](#object-factionuprising) | Enum / Object ||| `robot` (Enum), `ghost` (Enum), `{ ... }` (Object) |
| [`FireArmor`](#object-firearmor) | Integer / Object ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`FireArmor2`](#object-firearmor2) | Integer / Object ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`FireflySwarm`](#object-fireflyswarm) | Number / Object ||| `2` (Number), `{ ... }` (Object) |
| [`FireStorm`](#object-firestorm) | Number / Object ||| `33` (Number), `0` (Number), `{ ... }` (Object) |
| [`Fog`](#object-fog) | Number / Object ||| `1` (Number), `{ ... }` (Object) |
| `ForceMoveTowardsEnemies` | Enum / Integer ||| `MoveOne` (Enum), `DumbMove_Impl` (Enum), `1` (Number) |
| `Grappled` | Array / Integer ||| `[1 .5]` (Array), `[1 .75]` (Array), `1` (Number), `{ ... }` (Object) |
| [`HeatWave`](#object-heatwave) | Array / Number / Object ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `HeavyHits` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `IgnoreSelf` | Boolean / Integer ||| `true` (Boolean), `1` (Number) |
| `Invulnerable` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`JudgementDay`](#object-judgementday) | Number / Object ||| `25` (Number), `{ ... }` (Object) |
| `KnockbackDirectionIsFacingDirection` | Enum / Integer ||| `flip` (Enum), `rotate_right` (Enum), `1` (Number) |
| `Meaty` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`Meteornado`](#object-meteornado) | Number / Object ||| `1` (Number), `{ ... }` (Object) |
| [`MeteorShower`](#object-meteorshower) | Number / Object ||| `25` (Number), `{ ... }` (Object) |
| `Muted` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `NextAbilityHeals` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `NextActionLuckUp` | Integer ||| `[1 .5]` (Array), `1` (Number), `99` (Number), `{ ... }` (Object) |
| `NextAttackBonusRange` | Integer ||| `[1 .5]` (Array), `5` (Number), `1` (Number), `{ ... }` (Object) |
| [`NextAttackSpecialCrit`](Abilities_and_Spells.md#object-nextattackspecialcrit) | Integer / Object ||| `1` (Number), `{ ... }` (Object) |
| [`NextBasicAttackCritsThisTurn`](Abilities_and_Spells.md#object-nextbasicattackcritsthisturn) | Object ||| `1` (Number), `{ ... }` (Object) |
| `NextDamageReduceAndHealAllies` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `NextTurnDoubleRangedDamage` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `OverrideKnockbackDamage` | Enum / Integer ||| `str` (Enum), `X*10` (Enum), `5` (Number), `2` (Number), `"max(5+bonus_melee_ability_damage, 1)"` (String) |
| `OverrideKnockbackDamage` | Enum / Integer ||| `str` (Enum), `3+bonus_melee_ability_damage` (Enum), `2` (Number), `3` (Number), `"max(5+bonus_melee_ability_damage, 1)"` (String) |
| `PermanentImmobile` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`RandomDistanceDisplace`](Abilities_and_Spells.md#object-randomdistancedisplace) | Integer / Object ||| `20` (Number), `{ ... }` (Object) |
| `ReduceManaCostExcludeBrainstorm` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `ScatterHeldCoin` | Array / Integer ||| `[1 .3]` (Array), `[1 .5]` (Array), `1` (Number) |
| `SelfStun` | Array / Integer ||| `[1 .5]` (Array), `1` (Number) |
| [`Shatter`](#object-shatter) | Integer / Object ||| `15` (Number), `{ ... }` (Object) |
| `SpawnRock` | Array / Integer ||| `[1 .20]` (Array), `1` (Number) |
| `SpellShield` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `StatBounty` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Taunting` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`TeamCastAbility`](Abilities_and_Spells.md#object-teamcastability) | Enum / Object ||| `TeamFlex_Impl2` (Enum), `TeamFlex_Impl` (Enum), `{ ... }` (Object) |
| `TempBackstab` | Integer ||| `[1 .5]` (Array), `75` (Number), `1` (Number), `{ ... }` (Object) |
| `TempBonusKnockback` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TempBonusKnockbackDamage` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TempCritChanceUp` | Integer ||| `[1 .5]` (Array), `30` (Number), `1` (Number), `{ ... }` (Object) |
| `TempInitiativeChange` | Integer ||| `[1 .5]` (Array), `9999` (Number), `1` (Number), `{ ... }` (Object) |
| `TempInitiativeChange` | Integer ||| `[1 .5]` (Array), `9999` (Number), `1` (Number), `{ ... }` (Object) |
| `TempInjuryImmunity` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TempManaCostReduction` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TempPreEmptiveCounterAttack` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TilesMovedToCritChance` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TilesMovedToMana` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TilesMovedToNeighborHeal` | Enum ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TilesMovedToStrength` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TowerDefenseStatus` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TowerDefenseStatus2` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `TriggerWerewolfTransform` | Array / Number ||| `[1 .5]` (Array), `[1 .20]` (Array), `.5` (String) |
| `TurnControlDelay` | Number ||| `.25` (String) |
| [`VisualFlySwarm`](#object-visualflyswarm) | Number / Object ||| `1` (Number), `{ ... }` (Object) |

| [`AddDamageToElementDamage`](Cat_Mutations.md#object-adddamagetoelementdamage) | Object | Applies or references the 'AddDamageToElementDamage' effect/state. | 6 |
| `AddLeechesStatus` | Integer | Applies or references the 'AddLeechesStatus' effect/state. | 0 |
| [`AddStatusesIfPersistentWeatherElement`](Miscellaneous.md#object-addstatusesifpersistentweatherelement) | Object | Applies the 'AddStatusesIfPersistentWeatherElement' effect. | 0 |
| [`AddStatusesToReceivedElementalDamage`](Miscellaneous.md#object-addstatusestoreceivedelementaldamage) | Object | Applies the 'AddStatusesToReceivedElementalDamage' effect. | 0 |
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object | Injects a status effect payload that applies whenever the character performs a basic attack. | 178 |
| [`AddStatusToElementDamage`](Items_and_Equipment.md#object-addstatustoelementdamage) | Object | Applies the 'AddStatusToElementDamage' effect. | 4 |
| [`AddStatusToTrampleDamage`](Characters_and_Bosses.md#object-addstatustotrampledamage) | Object | Applies the 'AddStatusToTrampleDamage' effect. | 2 |
| `AddWeaponAux` | Integer / String | Applies or references the 'AddWeaponAux' effect/state. | 0 |
| `AllStatsUp` | Enum / Integer | Applies or references the 'AllStatsUp' effect/state. | 0 |
| `AlphaCat` | Integer | Applies or references the 'AlphaCat' effect/state. | 2 |
| [`ApplyPassives`](Abilities_and_Spells.md#object-applypassives) | Object | Grants the nested passive abilities dynamically. | 0 |
| `BigSplashDamage` | Integer | Applies the 'BigSplashDamage' effect. | 0 |
| `Bleed` | Array / Integer | Applies or references the 'Bleed' effect/state. | 9 |
| `Blind` | Array / Integer | Applies or references the 'Blind' effect/state. | 6 |
| [`BloodRain`](Engine_GlobalModifierKeys.md#object-bloodrain) | Integer / Object | Applies or references the 'BloodRain' effect/state. | 2 |
| `BonusCritChance` | Integer | Applies the 'BonusCritChance' effect. | 0 |
| `BonusDamage` | Enum / Integer | Applies or references the 'BonusDamage' effect/state. | 0 |
| `BonusDamageBasedOnDistance` | Integer | Applies or references the 'BonusDamageBasedOnDistance' effect/state. | 0 |
| `BonusKnockbackDamage` | Integer | Applies or references the 'BonusKnockbackDamage' effect/state. | 0 |
| `BrittleCharismaUp` | Integer | Applies or references the 'BrittleCharismaUp' effect/state. | 0 |
| `BrittleConstitutionUp` | Integer | Applies or references the 'BrittleConstitutionUp' effect/state. | 0 |
| `BrittleDexterityUp` | Integer | Applies or references the 'BrittleDexterityUp' effect/state. | 0 |
| `BrittleIntelligenceUp` | Integer | Applies or references the 'BrittleIntelligenceUp' effect/state. | 0 |
| `BrittleLuckUp` | Integer | Applies or references the 'BrittleLuckUp' effect/state. | 0 |
| `BrittleSpeedUp` | Integer | Applies or references the 'BrittleSpeedUp' effect/state. | 0 |
| `BrittleStrengthUp` | Integer | Applies or references the 'BrittleStrengthUp' effect/state. | 0 |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | Applies or references the 'Bruise' effect/state. | 8 |
| `Burn` | Array / Enum / Integer | Applies or references the 'Burn' effect/state. | 1 |
| `CapDamage` | Integer | Applies or references the 'CapDamage' effect/state. | 0 |
| `CaptureFamiliar` | Integer | Applies or references the 'CaptureFamiliar' effect/state. | 0 |
| `ChanceToBreak` | Integer | Applies or references the 'ChanceToBreak' effect/state. | 0 |
| [`CharacterTypeGainsStatusAtBattleStart`](Engine_LogicKeys.md#object-charactertypegainsstatusatbattlestart) | Object | Encounter Modifier: Applies a status effect to all characters of a specific type (e.g., Cats, Bosses) at the start of battle. | 1 |
| `Charge` | Integer | Applies or references the 'Charge' effect/state. | 0 |
| `Charmed` | Array / Enum / Integer | Applies or references the 'Charmed' effect/state. | 0 |
| [`Cleanse`](#object-cleanse) | Integer / Object | Applies or references the 'Cleanse' effect/state. | 2 |
| `CompleteItemQuest` | Enum | Applies or references the 'CompleteItemQuest' effect/state. | 0 |
| [`Conditional_HasStatus`](Abilities_and_Spells.md#object-conditional_hasstatus) | Object | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 0 |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | Applies or references the 'Confusion' effect/state. | 6 |
| `ConjureRandomAbilityFromCat` | Integer | Applies or references the 'ConjureRandomAbilityFromCat' effect/state. | 0 |
| `CrackMoonHead` | Integer | Applies or references the 'CrackMoonHead' effect/state. | 0 |
| `CurrentWeaponDamageUp` | Integer | Applies or references the 'CurrentWeaponDamageUp' effect/state. | 0 |
| `DeleteObject` | Integer | Applies or references the 'DeleteObject' effect/state. | 0 |
| `DestroyTrinket` | Integer | Applies or references the 'DestroyTrinket' effect/state. | 0 |
| [`Die`](Characters_and_Bosses.md#object-die) | Integer / Object | Applies or references the 'Die' effect/state. | 0 |
| `DieViolently` | Integer | Applies or references the 'DieViolently' effect/state. | 0 |
| `DisableWeapon` | Integer | Applies or references the 'DisableWeapon' effect/state. | 0 |
| `disallow_modifications` | Boolean | Prevents passives from altering this damage instance. | 0 |
| `DisplaceToAbilityTarget` | Integer | Applies or references the 'DisplaceToAbilityTarget' effect/state. | 0 |
| `DisplaceTowardsSource` | Integer | Applies or references the 'DisplaceTowardsSource' effect/state. | 0 |
| [`DistanceBonusDamage`](#object-distancebonusdamage) | Object | Applies the 'DistanceBonusDamage' effect. | 0 |
| `DivineShield` | Array / Integer | Applies or references the 'DivineShield' effect/state. | 0 |
| `DontHealEnemies` | Integer | Applies or references the 'DontHealEnemies' effect/state. | 0 |
| `Doomed` | Integer | Applies or references the 'Doomed' effect/state. | 0 |
| `EmptyMana` | Integer | Applies the 'EmptyMana' effect. | 0 |
| `EventBounty` | Integer | Applies or references the 'EventBounty' effect/state. | 0 |
| `ExplodeCharacter` | Integer | Applies or references the 'ExplodeCharacter' effect/state. | 0 |
| `ExplodeCharacter_NoDie` | Integer | Applies or references the 'ExplodeCharacter_NoDie' effect/state. | 0 |
| `ExplodeCharacter_Party` | Integer | Applies or references the 'ExplodeCharacter_Party' effect/state. | 0 |
| `ExplodeCharacter_PartyBoss` | Integer | Applies or references the 'ExplodeCharacter_PartyBoss' effect/state. | 0 |
| `ExplodeCharacter_RockCrusher` | Integer | Applies or references the 'ExplodeCharacter_RockCrusher' effect/state. | 0 |
| `ExplodeCharacter_RockCrusher_PetrifyBreak` | Integer | Applies or references the 'ExplodeCharacter_RockCrusher_PetrifyBreak' effect/state. | 0 |
| `FaceAway` | Integer | Applies or references the 'FaceAway' effect/state. | 0 |
| `FaceCamera` | Integer | Applies or references the 'FaceCamera' effect/state. | 0 |
| `FactionConversion` | Integer | Applies or references the 'FactionConversion' effect/state. | 0 |
| `Fear` | Array / Integer | Applies or references the 'Fear' effect/state. | 0 |
| `Fights` | Number | Applies or references the 'Fights' effect/state. | 4 |
| `FillMana` | Integer | Applies or references the 'FillMana' effect/state. | 0 |
| `FlatAIBonus` | Integer | Applies or references the 'FlatAIBonus' effect/state. | 0 |
| `FlatLeech` | Integer | Applies or references the 'FlatLeech' effect/state. | 0 |
| `FloatingRockTrap` | Integer | Applies or references the 'FloatingRockTrap' effect/state. | 0 |
| `ForceImmediateMove` | Integer | Applies or references the 'ForceImmediateMove' effect/state. | 0 |
| `ForceMoveAway` | Integer | Applies or references the 'ForceMoveAway' effect/state. | 0 |
| `ForceMoveTowards` | Integer | Applies or references the 'ForceMoveTowards' effect/state. | 0 |
| `ForceUseAbility_NonStack` | Enum | Applies or references the 'ForceUseAbility_NonStack' effect/state. | 0 |
| [`ForceUseAbilityOnTarget`](#object-forceuseabilityontarget) | Object | Applies or references the 'ForceUseAbilityOnTarget' effect/state. | 0 |
| `FullHeal` | Integer | Applies or references the 'FullHeal' effect/state. | 0 |
| `GainDisorder` | Enum | Applies or references the 'GainDisorder' effect/state. | 0 |
| `GainDisorderFromPool_PostCast` | Enum | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. | 0 |
| `GenericDebuff` | Integer | Applies or references the 'GenericDebuff' effect/state. | 0 |
| `HealRandomInjury` | Integer | Applies or references the 'HealRandomInjury' effect/state. | 0 |
| `HealthGain` | Integer | Applies or references the 'HealthGain' effect/state. | 0 |
| `IgnoreDamage` | Integer | Applies or references the 'IgnoreDamage' effect/state. | 0 |
| [`ImmediateUseAbility`](#object-immediateuseability) | Enum / Object | Applies or references the 'ImmediateUseAbility' effect/state. | 0 |
| `ImmediateUseAbility_Instant` | Enum | Applies or references the 'ImmediateUseAbility_Instant' effect/state. | 0 |
| `Immobile` | Array / Integer | Applies or references the 'Immobile' effect/state. | 4 |
| `Imprison` | Enum | Applies or references the 'Imprison' effect/state. | 0 |
| `InnateElement` | Enum | Applies the 'InnateElement' effect. | 8 |
| `Instakill` | Integer | Applies or references the 'Instakill' effect/state. | 0 |
| [`KnockbackIfCrit`](#object-knockbackifcrit) | Object | Applies or references the 'KnockbackIfCrit' effect/state. | 0 |
| `KnockOutClone` | Enum | Applies or references the 'KnockOutClone' effect/state. | 0 |
| `LaunchOffScreen` | Equation | Applies or references the 'LaunchOffScreen' effect/state. | 0 |
| `LaunchOffScreenInstakill` | Integer | Applies or references the 'LaunchOffScreenInstakill' effect/state. | 0 |
| `LeaveBehindRockOnKnockback` | Integer | Applies or references the 'LeaveBehindRockOnKnockback' effect/state. | 0 |
| `Leech` | Integer | Applies or references the 'Leech' effect/state. | 6 |
| `LeechPercent` | Integer | Applies the 'LeechPercent' effect. | 0 |
| [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object | Applies the Madness debuff/status effect. | 0 |
| `ManaGain` | Enum / Integer | Applies or references the 'ManaGain' effect/state. | 0 |
| [`Marked`](#object-marked) | Array / Integer / Object | Applies or references the 'Marked' effect/state. | 0 |
| `NonLethal` | Integer | Applies the 'NonLethal' effect. | 0 |
| `OverrideDamage` | Integer | Applies or references the 'OverrideDamage' effect/state. | 0 |
| [`passives`](Cat_Mutations.md#object-passives) | Object | List of {Status and Passive Keys}. | 5118 |
| `PermanentCharm` | Integer | Applies the 'PermanentCharm' effect. | 0 |
| `PermanentDexterity` | Integer | Applies or references the 'PermanentDexterity' effect/state. | 0 |
| `PreEmptiveCounterNextAttacks` | Integer | Applies or references the 'PreEmptiveCounterNextAttacks' effect/state. | 0 |
| `PurgeAll` | Integer | Applies or references the 'PurgeAll' effect/state. | 0 |
| `RandomBonusDamage` | Integer | Applies or references the 'RandomBonusDamage' effect/state. | 0 |
| `RandomStatDown` | Array / Integer / String | Applies or references the 'RandomStatDown' effect/state. | 0 |
| `RandomStatUp` | Integer / String | Applies or references the 'RandomStatUp' effect/state. | 2 |
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object | Selects and applies a random status effect from the provided nested block. | 0 |
| `RefreshActPoints` | Integer | Applies or references the 'RefreshActPoints' effect/state. | 0 |
| `RefreshMovePoints` | Integer | Applies or references the 'RefreshMovePoints' effect/state. | 0 |
| `RefreshWeaponAbility` | Integer | Applies or references the 'RefreshWeaponAbility' effect/state. | 0 |
| `RemoteFlatLeech` | Integer | Applies or references the 'RemoteFlatLeech' effect/state. | 0 |
| `RemoteLeech` | Integer | Applies or references the 'RemoteLeech' effect/state. | 0 |
| `RemoveAmbientLightEffects` | Float | Applies or references the 'RemoveAmbientLightEffects' effect/state. | 0 |
| `RemoveGlobalModifiers` | Array | Applies or references the 'RemoveGlobalModifiers' effect/state. | 0 |
| `RemoveItem` | Enum | Applies or references the 'RemoveItem' effect/state. | 0 |
| `RemoveKnockback` | Integer | Applies or references the 'RemoveKnockback' effect/state. | 0 |
| `RemoveMovePoints` | Integer | Applies or references the 'RemoveMovePoints' effect/state. | 0 |
| `RemoveStatus` | Enum | Applies or references the 'RemoveStatus' effect/state. | 0 |
| [`RemoveStatusStacks`](Abilities_and_Spells.md#object-removestatusstacks) | Object | Removes a specific number of stacks of a status effect. | 0 |
| `RemoveTurnsThisRound` | Integer | Applies or references the 'RemoveTurnsThisRound' effect/state. | 0 |
| `RepairWeapon` | Array / Integer | Applies or references the 'RepairWeapon' effect/state. | 0 |
| [`Revive`](#object-revive) | Integer / Object | Applies or references the 'Revive' effect/state. | 2 |
| `Rot` | Array / Integer | Applies or references the 'Rot' effect/state. | 0 |
| `ScatterRandomPickups` | Integer | Applies or references the 'ScatterRandomPickups' effect/state. | 0 |
| `SetHealth` | Integer | Applies or references the 'SetHealth' effect/state. | 0 |
| [`SetItemAux`](#object-setitemaux) | Object | Applies or references the 'SetItemAux' effect/state. | 0 |
| `SetKnockback` | Integer | Applies or references the 'SetKnockback' effect/state. | 0 |
| `SetShield` | Integer | Applies or references the 'SetShield' effect/state. | 0 |
| `Shield` | Enum / Integer | Applies or references the 'Shield' effect/state. | 422 |
| [`ShowFakeDamage`](Abilities_and_Spells.md#object-showfakedamage) | Object | Displays a visual damage number without actually modifying health. | 0 |
| `ShowText` | String | Applies or references the 'ShowText' effect/state. | 0 |
| [`Slow`](Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object | Applies or references the 'Slow' effect/state. | 4 |
| `SpawnBearTrap` | Integer | Applies or references the 'SpawnBearTrap' effect/state. | 0 |
| `SpawnBearTrapIfHitKills` | Integer | Applies or references the 'SpawnBearTrapIfHitKills' effect/state. | 0 |
| `SpawnBearTrapOnMiss` | Integer | Applies the 'SpawnBearTrapOnMiss' effect. | 0 |
| `SpawnFlames` | `Array` | Applies or references the 'SpawnFlames' effect/state. | 0 |
| `SpawnThingIfHitKills` | Enum | Applies or references the 'SpawnThingIfHitKills' effect/state. | 0 |
| `SpecificInjury` | Enum | Applies or references the 'SpecificInjury' effect/state. | 0 |
| `SpeculativeMoveSelfCorpseOffMap` | Integer | Applies or references the 'SpeculativeMoveSelfCorpseOffMap' effect/state. | 0 |
| `SpeedUp` | Enum / Integer | Applies or references the 'SpeedUp' effect/state. | 0 |
| `SpeedUp_WithoutInitiative` | Integer | Applies or references the 'SpeedUp_WithoutInitiative' effect/state. | 0 |
| `StackingSandstorm` | Integer | Applies or references the 'StackingSandstorm' effect/state. | 0 |
| `StanceSwitchToMelee` | Integer | Applies or references the 'StanceSwitchToMelee' effect/state. | 0 |
| `StanceSwitchToRanged` | Integer | Applies or references the 'StanceSwitchToRanged' effect/state. | 0 |
| `status` | Enum | The status effect to apply. | 0 |
| [`StatusEachRoundEnd`](Cat_Mutations.md#object-statuseachroundend) | Object | Applies or references the 'StatusEachRoundEnd' effect/state. | 2 |
| `StatusImmunity` | Array / Enum | Applies or references the 'StatusImmunity' effect/state. | 0 |
| [`StatusRandomEnemiesOnBattleStart`](Events_and_Encounters.md#object-statusrandomenemiesonbattlestart) | Object | Applies or references the 'StatusRandomEnemiesOnBattleStart' effect/state. | 0 |
| `StrengthUp` | Enum / Integer | Applies or references the 'StrengthUp' effect/state. | 0 |
| `Stun` | Array / Integer | Applies or references the 'Stun' effect/state. | 0 |
| `T2CopyCat` | Integer | Applies or references the 'T2CopyCat' effect/state. | 0 |
| `TakeExtraTurn` | Integer | Applies or references the 'TakeExtraTurn' effect/state. | 0 |
| `TempDexterityUp` | Enum | Applies or references the 'TempDexterityUp' effect/state. | 0 |
| `TempLuckUp` | Integer | Applies or references the 'TempLuckUp' effect/state. | 0 |
| [`Temporary`](Abilities_and_Spells.md#object-temporary) | Object | A wrapper object for applying status effects that automatically expire. | 0 |
| [`TempPassiveUntilSettled`](Characters_and_Bosses.md#object-temppassiveuntilsettled) | Object | Passive: Active only until the physics engine stops moving the character. | 0 |
| [`TempPassiveWhileHasStatus`](Abilities_and_Spells.md#object-temppassivewhilehasstatus) | Object | Grants nested passives only while the character possesses the specified status. | 0 |
| `TempStrengthUp` | Equation | Applies or references the 'TempStrengthUp' effect/state. | 0 |
| `TempTrampleUntilSettled` | Integer | Applies or references the 'TempTrampleUntilSettled' effect/state. | 0 |
| `Trample` | Integer | Applies or references the 'Trample' effect/state. | 14 |
| `UseAbility_Madness` | Enum | Applies the 'UseAbility_Madness' effect. | 0 |
| `UseAbility_NonStack` | Enum | Applies or references the 'UseAbility_NonStack' effect/state. | 0 |
| `Vaporize` | Integer | Applies or references the 'Vaporize' effect/state. | 0 |
| `VaporizeCorpse` | Integer | Applies or references the 'VaporizeCorpse' effect/state. | 0 |
| `VaporizeCorpseFlipAdvantage` | `Array` | Applies or references the 'VaporizeCorpseFlipAdvantage' effect/state. | 0 |
| `VaporizeInanimate` | Integer | Applies or references the 'VaporizeInanimate' effect/state. | 0 |
| `VisualFX` | Enum | Applies or references the 'VisualFX' effect/state. | 0 |
| [`Weakness`](Passives_and_Statuses.md#object-weakness) | Array / Integer / Object | Applies or references the 'Weakness' effect/state. | 4 |
| `WeaponAuxMultiplier` | Number | Applies or references the 'WeaponAuxMultiplier' effect/state. | 0 |
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
| `DamageUp` | Integer / String || 6 | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `AddPassivesToMinions`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 36

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer || 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `HealthRegenUp` | Integer || 26 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Quivered` | Array / Integer || 10 | `[1 0.1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String || 6 | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `PoisonThorns` | Integer || 6 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`tag_filter`](./Enums.md#enum-tag_filter) | Enum | Examples: `crow, grub_familiar` | 3 ||
| `AllStatsUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| [`Buddy`](Characters_and_Bosses.md#object-buddy) | Enum / Object ||| `spawner` (Enum), `Ornstein` (Enum), `{ ... }` (Object) |
| `DivineShield` | Array / Integer ||| `[1 .5]` (Array), `[1 .33]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`ForceAttack`](Abilities_and_Spells.md#object-forceattack) | Integer / Object ||| `1` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer ||| `3*X` (Enum), `2*X` (Enum), `2` (Number), `1` (Number) |

</details>

---

#### `AddSelfStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer || 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Quivered` | Array / Integer || 10 | `[1 0.1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Bleed` | Array / Integer || 9 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object ||| `head_HitlersToupe` (Enum), `tk_JarOfRadiation` (Enum), `{ ... }` (Object) |
| [`RandomMagicMissile`](Abilities_and_Spells.md#object-randommagicmissile) | Integer / Object ||| `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `AddSelfStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RepairWeapon` | Array / Integer ||| `[1 .25]` (Array), `6` (Number), `1` (Number) |
| `ChanceToBreak` | Integer | Applies or references the 'ChanceToBreak' effect/state. | 0 ||
| [`RepairWeapon`](./Arrays.md#array-repairweapon) | Array / Integer | Applies or references the 'RepairWeapon' effect/state. | 0 ||

</details>

---

#### `AddStatusToAllDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Blind` | Array / Integer || 6 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Blind`](./Arrays.md#array-blind) | Array / Integer | Applies or references the 'Blind' effect/state. | 6 ||
| [`Conditional_HasStatus`](Abilities_and_Spells.md#object-conditional_hasstatus) | Object | Nested conditional. | 3 ||
| [`Conditional_HasTag`](Abilities_and_Spells.md#object-conditional_hastag) | Object | Nested conditional. | 3 ||
| `must_do_damage` | Boolean | `true` | 3 ||
| `Rot` | Array / Integer ||| `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `-999999` (Number), `{ ... }` (Object) |
| [`KnockbackIfCrit`](#object-knockbackifcrit) | Object | Applies or references the 'KnockbackIfCrit' effect/state. | 0 ||
| `LeaveBehindRockOnKnockback` | Integer | Applies or references the 'LeaveBehindRockOnKnockback' effect/state. | 0 ||
| `NonLethal` | Integer | Applies the 'NonLethal' effect. | 0 ||
| [`Rot`](./Arrays.md#array-rot) | Array / Integer | Applies or references the 'Rot' effect/state. | 0 ||
| `BonusKnockbackDamage` | Integer | Applies or references the 'BonusKnockbackDamage' effect/state. | 0 ||

</details>

---

#### `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 248

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Array / Integer || 9 | `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object || 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Poison` | Array / Integer || 8 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Blind` | Array / Integer || 6 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object || 6 | `[1 .15]` (Array), `[1 .2]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String || 6 | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Leech` | Integer || 6 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Conditional_Ally`](Abilities_and_Spells.md#object-conditional_ally) | Object | Nested conditional. | 5 ||
| `Immobile` | Array / Integer || 4 | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| [`Slow`](Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object || 4 | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Weakness`](Passives_and_Statuses.md#object-weakness) | Array / Integer / Object || 4 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_Enemy`](Abilities_and_Spells.md#object-conditional_enemy) | Object | Nested conditional. | 3 ||
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Nested conditional. | 3 ||
| [`Conditional_Adjacent`](Engine_LogicKeys.md#conditional_adjacent) | Object | Nested conditional. | 2 ||
| [`Conditional_Shielded`](Abilities_and_Spells.md#object-conditional_shielded) | Object | Nested conditional. | 2 ||
| [`Leeches`](#object-leeches) | Integer / Object || 2 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `MagicWeakness` | Array / Integer || 2 | `[1 .1]` (Array), `[1 .5]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| `RandomStatUp` | Integer / String || 2 | `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `2` (Number), `-5` (Number) |
| [`SoulLink`](#object-soullink) | Integer / Object || 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`Conditional_HasTag`](Abilities_and_Spells.md#object-conditional_hastag) | Object | Nested conditional. | 1 ||
| [`Conditional_SourceHasTag`](Engine_LogicKeys.md#conditional_sourcehastag) | Object | Nested conditional. | 1 ||
| `Burn` | Array / Enum / Integer || 1 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Else`](Abilities_and_Spells.md#object-else) | Object || 1 | `{ ... }` (Object) |
| [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object ||| `{ ... }` (Object) |
| [`BounceObject`](Abilities_and_Spells.md#object-bounceobject) | Enum / Object ||| `AllyRotFly` (Enum), `CharmedFlea_Champion` (Enum), `{ ... }` (Object) |
| `BurgleCoin` | Array / Integer ||| `[1 .5]` (Array), `3` (Number), `1` (Number) |
| [`ChangeTile`](Abilities_and_Spells.md#object-changetile) | Enum / Object ||| `LavaTile` (Enum), `TallGrassTile` (Enum), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer ||| `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer ||| `[1 .25]` (Array), `[1 .15]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `FlatLeech` | Integer ||| `X` (Enum), `5` (Number), `2` (Number) |
| `Freeze` | Array / Integer ||| `[1 .01]` (Array), `[1 .20]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`GainDisorderFromPool`](Characters_and_Bosses.md#object-gaindisorderfrompool) | Enum / Object ||| `all_disorders` (Enum), `{ ... }` (Object) |
| `Instakill` | Integer ||| `[25 .01]` (Array), `50` (Number), `999` (Number) |
| `Knockback` | Integer ||| `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`KnockOutCoin`](Abilities_and_Spells.md#object-knockoutcoin) | Integer / Object ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`KnockUpAndAway`](Abilities_and_Spells.md#object-knockupandaway) | Object ||| `{ ... }` (Object) |
| `LuckUp` | Enum / Integer ||| `[1 .5]` (Array), `222` (Number), `2` (Number), `{ ... }` (Object) |
| [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object ||| `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `ManaLeeches` | Integer ||| `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`Marked`](#object-marked) | Array / Integer / Object ||| `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `3` (Number), `{ ... }` (Object) |
| `OverrideChainKnockback` | Integer ||| `10` (Number), `3` (Number) |
| `OverrideChainKnockbackDamage` | String ||| `3+bonus_melee_ability_damage` (Enum), `0` (Number) |
| `Petrify` | Array / Integer ||| `[1 .1]` (Array), `[1 .20]` (Array), `1` (Number), `{ ... }` (Object) |
| `Possessed` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `PullSourceToTarget` | Integer ||| `1` (Number) |
| `Rot` | Array / Integer ||| `[1 .1]` (Array), `[1 .5]` (Array), `-999999` (Number), `2` (Number), `{ ... }` (Object) |
| `SpiderInfested` | Integer ||| `[1 .5]` (Array), `4` (Number), `1` (Number), `{ ... }` (Object) |
| `SplashDamage` | Integer ||| `1` (Number), `2` (Number) |
| [`SpreadDisease`](Abilities_and_Spells.md#object-spreaddisease) | Object ||| `{ ... }` (Object) |
| `Stun` | Array / Integer ||| `[1 .25]` (Array), `[1 .15]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| [`Tangled`](Abilities_and_Spells.md#object-tangled) | Array / Integer / Object ||| `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `VisualFXTile` | Enum ||| `PoisonPoof` (Enum), `FireBlastSmall` (Enum) |
| `Webbed` | Integer ||| `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `AddStatusToBasicMeleeAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Array / Integer || 9 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object || 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object || 6 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Immobile` | Array / Integer || 4 | `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| `Knockback` | Integer ||| `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`KnockUpAndAway`](Abilities_and_Spells.md#object-knockupandaway) | Object ||| `{ ... }` (Object) |
| [`SpreadDisease`](Abilities_and_Spells.md#object-spreaddisease) | Object ||| `{ ... }` (Object) |
| `Stun` | Array / Integer ||| `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `AddStatusToElementDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AddDamageToElementDamage`](Cat_Mutations.md#object-adddamagetoelementdamage) | Object | Applies or references the 'AddDamageToElementDamage' effect/state. | 6 ||
| [`Conditional_Corpse`](Abilities_and_Spells.md#object-conditional_corpse) | Object | Nested conditional. | 2 ||
| [`element`](./Enums.md#enum-element) | Array / Enum | The specific element type required or applied. | 1 ||
| `Burn` | Array / Enum / Integer || 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Stun` | Array / Integer ||| `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `AddStatusToKnockbackDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object || 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | Applies or references the 'Bruise' effect/state. | 8 ||
| `Stun` | Array / Integer ||| `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| [`Stun`](./Arrays.md#array-stun) | Array / Integer | Applies or references the 'Stun' effect/state. | 0 ||

</details>

---

#### `AddStatusToSpells`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Leech` | Integer || 6 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Leech` | Integer | Applies or references the 'Leech' effect/state. | 6 ||
| [`Conditional_Enemy`](Abilities_and_Spells.md#object-conditional_enemy) | Object | Nested conditional. | 1 ||
| `LeechPercent` | Integer | Applies the 'LeechPercent' effect. | 0 ||

</details>

---

#### `AddStatusToTrampleDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object || 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object | Applies or references the 'Bruise' effect/state. | 8 ||
| [`Cleave`](Abilities_and_Spells.md#object-cleave) | Integer / Object ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`Cleave`](Abilities_and_Spells.md#object-cleave) | Integer / Object | Causes the attack to hit adjacent enemies alongside the primary target. | 0 ||

</details>

---

#### `AddStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Array / Integer || 9 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Leech` | Integer || 6 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Cleave`](Abilities_and_Spells.md#object-cleave) | Integer / Object ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `PullSourceToKnockbackImmuneTarget` | Integer ||| `1` (Number) |

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
| `YOffset` | Number || 6 | `-.18` (String), `.25` (String) |
| `Flying` | Integer || 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `ApplyStatusIfCrit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Array / Integer || 9 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Purge`](#object-purge) | Integer / Object || 2 | `3` (Number), `0` (Number), `{ ... }` (Object) |
| [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object ||| `{ ... }` (Object) |
| `LuckUp` | Enum / Integer ||| `[1 .5]` (Array), `222` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `ApplyStatusesToRandomEnemiesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`count`](./Arrays.md#array-count) | Array / Integer | Quantity. | 3 ||
| `Bounty` | Integer ||| `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| [`Marked`](#object-marked) | Array / Integer / Object ||| `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `CatchProjectiles`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum || 5441 | `"PASSIVE_CATCHPROJECTILES_DESC"` (String) |
| `name` | Enum || 5027 | `"PASSIVE_CATCHPROJECTILES_NAME"` (String) |
| `Quivered` | Array / Integer || 10 | `[1 0.1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `ally_chance` | Integer | Examples: `15, 100` | 5 ||
| [`chance`](./Enums.md#enum-chance) | Float | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 ||
| `AllStatsUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `CharacterTypeGainsStatusAtBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Array / Enum | Specific entity tag required. | 981 ||
| `Stealth` | Array / Integer || 2 | `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_Flying`](Engine_Uncategorized_Resources.md#conditional_flying) | Object | Nested conditional. | 1 ||
| [`Else`](Abilities_and_Spells.md#object-else) | Object || 1 | `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer ||| `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Stun` | Array / Integer ||| `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `CritsApplyStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Array / Integer || 9 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object || 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object || 6 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Immobile` | Array / Integer || 4 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| [`Weakness`](Passives_and_Statuses.md#object-weakness) | Array / Integer / Object || 4 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_HasStatus`](Abilities_and_Spells.md#object-conditional_hasstatus) | Object | Nested conditional. | 2 ||
| [`Else`](Abilities_and_Spells.md#object-else) | Object || 1 | `{ ... }` (Object) |
| `Fear` | Array / Integer ||| `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object ||| `Coin` (Enum), `SmallRock` (Enum), `{ ... }` (Object) |
| `Stun` | Array / Integer ||| `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `ExtraStatusWhenDealingDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_PartyMember`](Engine_LogicKeys.md#conditional_partymember) | Object | Nested conditional. | 3 ||
| [`Conditional_Ally`](Abilities_and_Spells.md#object-conditional_ally) | Object | Nested conditional. | 2 ||

</details>

---

#### `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 73

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 62 ||
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 54 ||
| `knockback` | Enum / Integer | The base physics pushing power (in tiles). | 24 ||
| `Poison` | Array / Integer || 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`InnateElement`](./Enums.md#enum-innateelement) | Enum | Applies the 'InnateElement' effect. | 8 ||
| [`AddDamageToElementDamage`](Cat_Mutations.md#object-adddamagetoelementdamage) | Object | Applies or references the 'AddDamageToElementDamage' effect/state. | 6 ||
| `Immobile` | Array / Integer || 4 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| [`Weakness`](Passives_and_Statuses.md#object-weakness) | Array / Integer / Object || 4 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`AddStatusToElementDamage`](Items_and_Equipment.md#object-addstatustoelementdamage) | Object | Applies the 'AddStatusToElementDamage' effect. | 4 ||
| [`damage`](./Arrays.md#array-damage) | Equation | The base damage properties of an attack. | 2 ||
| `cant_miss` | Boolean | Guarantees the hit, bypassing dodge mechanics. | 1 ||
| `Freeze` | Array / Integer ||| `[1 .1]` (Array), `[1 0.15]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`elements`](./Arrays.md#array-elements) | Array | Array of elemental tags to apply (e.g., `[Fire Holy]`). | 0 ||
| [`SpreadDisease`](Abilities_and_Spells.md#object-spreaddisease) | Object ||| `{ ... }` (Object) |
| [`StatusImmunity`](./Enums.md#enum-statusimmunity) | Array / Enum | Applies or references the 'StatusImmunity' effect/state. | 0 ||

</details>

---

#### `PassiveAfterXKills`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Passives granted by equipping this. | 5118 ||
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 4 ||

</details>

---

#### `PassiveAtHealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Passives granted by equipping this. | 5118 ||
| [`mode`](./Enums.md#enum-mode) | Enum | `equal`, `greater`, `greater_or_equal`, `less_or_equal`, `yeet` | 9 ||
| [`threshold`](Items_and_Equipment.md#object-threshold) | Enum / Integer / Object | Examples: `4*champion_multiplier, 3*champion_multiplier, 1` | 9 ||

</details>

---

#### `PassiveAtStatThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Examples: `{ ... }` | 5118 ||
| [`mode`](./Enums.md#enum-mode) | Enum | `equal`, `greater`, `greater_or_equal`, `less_or_equal`, `yeet` | 13 ||
| [`threshold`](Items_and_Equipment.md#object-threshold) | Enum / Integer / Object | Examples: `4*champion_multiplier, 3*champion_multiplier, 1` | 13 ||

</details>

---

#### `PassiveGroup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object ||| `{ ... }` (Object) |
| `CharismaUp` | Enum / Integer ||| `[1 .5]` (Array), `5` (Number), `-2` (Number), `{ ... }` (Object) |
| [`FormChange`](Abilities_and_Spells.md#object-formchange) | Enum / Object ||| `Fighter` (Enum), `Medic` (Enum), `{ ... }` (Object) |
| `IntelligenceUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer ||| `[1 .5]` (Array), `5` (Number), `-2` (Number), `{ ... }` (Object) |

</details>

---

#### `PassiveWhenAffectedByElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Examples: `{ ... }` | 5118 ||
| [`element`](./Enums.md#enum-element) | Array / Enum | The specific element type to check for. | 1 ||

</details>

---

#### `PassiveWhenAtFullMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object || 20 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String || 6 | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Flying` | Integer || 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `PassiveWhenDead`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`StatusEachTurnBegin`](Cat_Mutations.md#object-statuseachturnbegin) | Object | Event Trigger: Applies nested statuses to each turn begin. | 16 ||
| [`AutocastEachRound`](Abilities_and_Spells.md#object-autocasteachround) | Enum / Object || 4 | `SpiderReturn` (Enum), `{ ... }` (Object) |
| [`AutocastEachRound`](Abilities_and_Spells.md#object-autocasteachround) | Enum / Object | Forces the character to automatically cast a specific ability at the start of each combat round. | 4 ||
| [`StatusEachRoundEnd`](Cat_Mutations.md#object-statuseachroundend) | Object | Applies or references the 'StatusEachRoundEnd' effect/state. | 2 ||
| [`AddStatusToTrampleDamage`](Characters_and_Bosses.md#object-addstatustotrampledamage) | Object | Applies the 'AddStatusToTrampleDamage' effect. | 2 ||

</details>

---

#### `PassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Object listing intrinsic passive modifiers. | 5118 ||
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 6 ||

</details>

---

#### `PassiveWhileInMonkMeleeStance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer || 26 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object || 20 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `RandomPassivePool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`TransformInXTurns`](Characters_and_Bosses.md#object-transforminxturns) | Object ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 35

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer || 422 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `CritChanceUp` | Integer || 36 | `[1 .5]` (Array), `5` (Number), `1` (Number), `{ ... }` (Object) |
| `Thorns` | Integer || 36 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `HealthRegenUp` | Integer || 26 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object || 20 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Quivered` | Array / Integer || 10 | `[1 0.1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Bleed` | Array / Integer || 9 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `BleedThorns` | Integer || 8 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object || 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Poison` | Array / Integer || 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Blind` | Array / Integer || 6 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object || 6 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String || 6 | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `KineticSpikes` | Integer || 6 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `MoveQuivered` | Integer || 6 | `[1 0.1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Immobile` | Array / Integer || 4 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| [`Slow`](Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object || 4 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Weakness`](Passives_and_Statuses.md#object-weakness) | Array / Integer / Object || 4 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`BackflipWhenTargeted`](Abilities_and_Spells.md#object-backflipwhentargeted) | Enum / Integer / Object || 2 | `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `DodgeChance_Status` | Integer || 2 | `[1 .5]` (Array), `40` (Number), `10` (Number), `{ ... }` (Object) |
| `MagicWeakness` | Array / Integer || 2 | `[1 .1]` (Array), `[1 .5]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| [`PoisonLace`](#object-poisonlace) | Integer / Object / String || 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `RandomStatUp` | Integer / String || 2 | `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `2` (Number), `-5` (Number) |
| [`Reflect`](#object-reflect) | Integer / Object || 2 | `[1 .5]` (Array), `5` (Number), `1` (Number), `{ ... }` (Object) |
| `Burn` | Array / Enum / Integer || 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Infested`](#object-infested) | Integer / Object || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `BonusDamage` | Enum / Integer ||| `str` (Enum), `20+bonus_melee_damage` (Enum), `-5` (Number), `-4` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Charge` | Integer ||| `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `CharismaUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer ||| `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer ||| `[1 .5]` (Array), `-1` (Number), `-2` (Number), `{ ... }` (Object) |
| `DelayedPain` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `DexterityUp` | Enum / Integer ||| `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `DiminishingHealthRegen` | Integer ||| `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer ||| `[1 .5]` (Array), `[1 .33]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Drowsy` | Integer ||| `[1 .5]` (Array), `8` (Number), `1` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer ||| `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`FormChange`](Abilities_and_Spells.md#object-formchange) | Enum / Object ||| `passive` (Enum), `Boris` (Enum), `{ ... }` (Object) |
| `Freeze` | Array / Integer ||| `[1 .1]` (Array), `[1 0.15]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `GainCoins` | Array / Integer ||| `[3 5]` (Array), `2` (Number), `-5` (Number) |
| `Hex` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `IntelligenceUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `Lifesteal` | Integer ||| `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `LuckUp` | Enum / Integer ||| `[1 .5]` (Array), `222` (Number), `2` (Number), `{ ... }` (Object) |
| [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object ||| `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `ManaGain` | Enum / Integer ||| `item_aux` (Enum), `X` (Enum), `5` (Number), `2` (Number), `"max(X*3, 0)"` (String), `"max((X-1)*2, 0)"` (String) |
| [`Marked`](#object-marked) | Array / Integer / Object ||| `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `3` (Number), `{ ... }` (Object) |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object ||| `SmallRock` (Enum), `BeefyCharmedLeech` (Enum), `{ ... }` (Object) |
| `Ostracized` | Integer ||| `[1 .5]` (Array), `4` (Number), `1` (Number), `{ ... }` (Object) |
| `PermanentCharisma` | Integer ||| `1` (Number), `2` (Number) |
| `PermanentLuck` | Integer ||| `1` (Number), `2` (Number) |
| `PermanentStrength` | Integer ||| `1` (Number), `2` (Number) |
| `Petrify` | Array / Integer ||| `[1 .1]` (Array), `[1 .20]` (Array), `1` (Number), `{ ... }` (Object) |
| `RandomStatDown` | Array / Integer / String ||| `[1 .25]` (Array), `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `1` (Number) |
| `Rot` | Array / Integer ||| `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `-999999` (Number), `{ ... }` (Object) |
| `Scrambled` | Integer ||| `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `Sleep` | Array / Integer ||| `[1 .1]` (Array), `[1 .5]` (Array), `8` (Number), `3` (Number), `{ ... }` (Object) |
| `SpawnCoinAnywhere` | Array / Integer ||| `[1 .5]` (Array), `1` (Number) |
| `SpeedUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `SpellDamageUp` | Integer ||| `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Stun` | Array / Integer ||| `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| `Tarred` | Array / Integer ||| `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `TempCounterAttack` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 31

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 62 ||
| [`type`](./Enums.md#enum-type) | Enum | The classification of damage (`melee`, `ranged`, `spell`, `trample`, `knockblock`, `spawn`). | 54 ||
| `knockback` | Enum / Integer | The base physics pushing power (in tiles). | 3 ||
| [`damage`](./Arrays.md#array-damage) | Equation | The base damage properties of an attack. | 2 ||
| [`elements`](./Arrays.md#array-elements) | Array | Array of elemental tags to apply (e.g., `[Fire Holy]`). | 0 ||

</details>

---

#### `StatusAfterCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `TempDamageUp` | Integer ||| `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `TempRangeUp` | Integer ||| `[1 .5]` (Array), `20` (Number), `3` (Number), `{ ... }` (Object) |
| `TempSpellDamageUp` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object ||| `GirlDinoPoop` (Enum), `TormentorRuneAbsorb` (Enum), `{ ... }` (Object) |

</details>

---

#### `StatusAfterXTurns`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 2 ||
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object ||| `head_HitlersToupe` (Enum), `tk_JarOfRadiation` (Enum), `{ ... }` (Object) |

</details>

---

#### `StatusAllCharactersOnSpawn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Poison` | Array / Integer || 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_Boss`](Abilities_and_Spells.md#object-conditional_boss) | Object | Nested conditional. | 2 ||
| [`Conditional_PartyMember`](Engine_LogicKeys.md#conditional_partymember) | Object | Nested conditional. | 1 ||
| [`Conditional_Tiny`](Engine_Uncategorized_Resources.md#conditional_tiny) | Object | Nested conditional. | 1 ||
| [`Else`](Abilities_and_Spells.md#object-else) | Object || 1 | `{ ... }` (Object) |

</details>

---

#### `StatusAlliesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RandomStatUp` | Integer / String || 2 | `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `2` (Number), `-5` (Number) |
| `RandomStatUp` | Integer / String | Applies or references the 'RandomStatUp' effect/state. | 2 ||
| [`Conditional_Adjacent`](Engine_LogicKeys.md#conditional_adjacent) | Object | Nested conditional. | 1 ||
| `exclude_self` | Boolean | `false` | 1 ||

</details>

---

#### `StatusAlliesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer || 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object || 20 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String || 6 | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer ||| `[1 .5]` (Array), `-1` (Number), `-2` (Number), `{ ... }` (Object) |
| `IntelligenceUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `LuckUp` | Enum / Integer ||| `[1 .5]` (Array), `222` (Number), `2` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusAlliesOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Reanimate`](#object-reanimate) | Integer / Object || 4 | `50` (Number), `100` (Number), `{ ... }` (Object) |
| `triggers_limit` | Integer | Examples: `1` | 2 ||
| `AllStatsUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer ||| `[1 .5]` (Array), `[1 .33]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Freeze` | Array / Integer ||| `[1 .1]` (Array), `[1 0.15]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusEachRoundEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`DoDamage`](Abilities_and_Spells.md#object-dodamage) | Object ||| `{ ... }` (Object) |
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object ||| `GirlDinoPoop` (Enum), `Spit` (Enum), `{ ... }` (Object) |

</details>

---

#### `StatusEachTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 27

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MissChance` | Integer || 24 | `[1 .5]` (Array), `5` (Number), `10` (Number), `{ ... }` (Object) |
| `Quivered` | Array / Integer || 10 | `[1 0.1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `MoveQuivered` | Integer || 6 | `[1 0.1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Conditional_BadRoll`](Abilities_and_Spells.md#object-conditional_badroll) | Object | Nested conditional. | 5 ||
| `RandomStatUp` | Integer / String || 2 | `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `2` (Number), `-5` (Number) |
| [`Revive`](#object-revive) | Integer / Object || 2 | `50` (Number), `100` (Number), `{ ... }` (Object) |
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Nested conditional. | 1 ||
| `Burn` | Array / Enum / Integer || 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `BlessingOfPeace` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `DoubleCastSpellThisTurn` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer ||| `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `FillMana` | Integer ||| `[1 .10]` (Array), `[1 .25]` (Array), `1` (Number) |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object ||| `head_HitlersToupe` (Enum), `tk_JarOfRadiation` (Enum), `{ ... }` (Object) |
| `IntelligenceUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object ||| `GirlDinoPoop` (Enum), `TormentorRuneAbsorb` (Enum), `{ ... }` (Object) |
| `Wet` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 57

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer || 422 | `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `KineticSpikes` | Integer || 6 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Nested conditional. | 2 ||
| [`Cleanse`](#object-cleanse) | Integer / Object || 2 | `0` (Number), `1` (Number), `{ ... }` (Object) |
| `RandomStatUp` | Integer / String || 2 | `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `2` (Number), `-5` (Number) |
| `Stealth` | Array / Integer || 2 | `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_BadRoll`](Abilities_and_Spells.md#object-conditional_badroll) | Object | Nested conditional. | 1 ||
| [`Conditional_HasCleansableDebuffs`](Abilities_and_Spells.md#object-conditional_hascleansabledebuffs) | Object | Nested conditional. | 1 ||
| [`Conditional_ManaThreshold`](Engine_LogicKeys.md#conditional_manathreshold) | Object | Nested conditional. | 1 ||
| `Burn` | Array / Enum / Integer || 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `AddWeaponAux` | Integer / String ||| `-item_aux` (Enum), `2` (Number), `1` (Number), `"-max(min(X+1, item_aux), 0)"` (String) |
| `AllStatsUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Charge` | Integer ||| `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer ||| `[1 .5]` (Array), `-1` (Number), `-2` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer ||| `[1 .5]` (Array), `[1 .33]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object ||| `head_HitlersToupe` (Enum), `tk_RoboSucc` (Enum), `{ ... }` (Object) |
| `HealthGain` | Integer ||| `3*X` (Enum), `2*X` (Enum), `5` (Number), `10` (Number) |
| [`ImmediateUseAbility`](#object-immediateuseability) | Enum / Object ||| `MoonHandMegaSqueeze` (Enum), `head_ThrobbingCrown` (Enum), `{ ... }` (Object) |
| `IntelligenceUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `NonStackingDivineShield` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object ||| `SmallRock` (Enum), `SkeletonCatFamiliar` (Enum), `{ ... }` (Object) |
| `PermanentMadness` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `PreEmptiveCounterNextAttacks` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `RandomStatDown` | Array / Integer / String ||| `[1 .25]` (Array), `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `1` (Number) |
| `RangeUp` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `SpawnCoinAnywhere` | Array / Integer ||| `[1 .5]` (Array), `1` (Number) |
| `SpeedUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusEachTurnEndForEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object ||| `head_HitlersToupe` (Enum), `tk_JarOfRadiation` (Enum), `{ ... }` (Object) |
| [`RandomMagicMissile`](Abilities_and_Spells.md#object-randommagicmissile) | Integer / Object ||| `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusEveryXSpellCasts`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer | Number of stacks or intensity to apply. | 8 ||
| `AllStatsUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Charge` | Integer ||| `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `IntelligenceUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object ||| `SmallRock` (Enum), `SkeletonCatFamiliar` (Enum), `{ ... }` (Object) |
| [`RandomMagicMissile`](Abilities_and_Spells.md#object-randommagicmissile) | Integer / Object ||| `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `ReduceManaCost` | Integer ||| `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `RepairWeapon` | Array / Integer ||| `[1 .25]` (Array), `99` (Number), `1` (Number) |
| `RepairWeaponCondition` | Integer ||| `1` (Number) |
| `SpellDamageUp` | Integer ||| `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusGroup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DexterityUp` | Enum / Integer ||| `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object ||| `mutant_pool` (Enum), `parasites` (Enum), `{ ... }` (Object) |
| `Freeze` | Array / Integer ||| `[1 .1]` (Array), `[1 0.15]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `LuckUp` | Enum / Integer ||| `[1 .5]` (Array), `222` (Number), `2` (Number), `{ ... }` (Object) |
| `SpawnCoinAnywhere` | Array / Integer ||| `[1 .5]` (Array), `1` (Number) |
| `SpeedUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusIfUnusedMovePoints`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer || 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object || 20 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `MoveQuivered` | Integer || 6 | `[1 0.1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Charge` | Integer ||| `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer ||| `[1 .5]` (Array), `-1` (Number), `-2` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer ||| `[1 .5]` (Array), `[1 .33]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer ||| `3*X` (Enum), `2*X` (Enum), `5` (Number), `10` (Number) |
| `ManaGain` | Enum / Integer ||| `X` (Enum), `item_aux` (Enum), `5` (Number), `2` (Number), `"max(X*3, 0)"` (String), `"max((X-1)*2, 0)"` (String) |

</details>

---

#### `StatusKilledCharacters`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_RandomChance`](Abilities_and_Spells.md#object-conditional_randomchance) | Object | Nested conditional. | 2 ||
| [`Conditional_Ally`](Abilities_and_Spells.md#object-conditional_ally) | Object | Nested conditional. | 1 ||
| `AutoReanimate` | Number ||| `100` (Number), `50` (Number) |
| `AutoReanimate` | Number | Examples: `50` | 0 ||

</details>

---

#### `StatusKillers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object || 6 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object | Applies or references the 'Confusion' effect/state. | 6 ||
| [`Conditional_Boss`](Abilities_and_Spells.md#object-conditional_boss) | Object | Nested conditional. | 2 ||
| [`Conditional_NotBoss`](Abilities_and_Spells.md#object-conditional_notboss) | Object | Nested conditional. | 2 ||

</details>

---

#### `StatusOnAllyCatDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageUp` | Integer / String || 6 | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer ||| `[1 .5]` (Array), `[1 .33]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `FillMana` | Integer ||| `[1 .10]` (Array), `[1 .25]` (Array), `1` (Number) |
| `HealthGain` | Integer ||| `3*X` (Enum), `2*X` (Enum), `5` (Number), `10` (Number) |

</details>

---

#### `StatusOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 53

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. | 25 ||
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Nested conditional. | 6 ||
| [`Conditional_Corpse`](Abilities_and_Spells.md#object-conditional_corpse) | Object | Nested conditional. | 1 ||
| [`Conditional_Shielded`](Abilities_and_Spells.md#object-conditional_shielded) | Object | Nested conditional. | 1 ||
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object ||| `pills` (Enum), `chapter_specific_item` (Enum), `{ ... }` (Object) |
| `GainCoins` | Array / Integer ||| `[3 5]` (Array), `5` (Number), `2` (Number) |
| `PermanentStrength` | Integer ||| `1` (Number), `2` (Number) |
| `RepairAll` | Integer ||| `10` (Number), `1` (Number) |
| `RepairWeapon` | Array / Integer ||| `[1 .25]` (Array), `99` (Number), `1` (Number) |
| [`TransformWeapon`](Abilities_and_Spells.md#object-transformweapon) | Object ||| `{ ... }` (Object) |

</details>

---

#### `StatusOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object || 20 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Craft`](Abilities_and_Spells.md#object-craft) | Object || 2 | `{ ... }` (Object) |
| [`DestroyEquipmentAndAttachParasite`](Abilities_and_Spells.md#object-destroyequipmentandattachparasite) | Object ||| `{ ... }` (Object) |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object ||| `chapter` (Enum), `pills` (Enum), `{ ... }` (Object) |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object ||| `head_HitlersToupe` (Enum), `tk_JarOfRadiation` (Enum), `{ ... }` (Object) |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object ||| `SmallRock` (Enum), `SkeletonCatFamiliar` (Enum), `{ ... }` (Object) |
| [`RandomMagicMissile`](Abilities_and_Spells.md#object-randommagicmissile) | Integer / Object ||| `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`ReviveNextRound`](Abilities_and_Spells.md#object-revivenextround) | Integer / Object ||| `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `SafeDie` | Integer ||| `1` (Number) |
| `Sleep` | Array / Integer ||| `[1 .1]` (Array), `[1 .5]` (Array), `8` (Number), `3` (Number), `{ ... }` (Object) |
| `StealthUntilBasicAttack` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusOnBreak`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 22

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer || 26 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object || 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`ApplyToRandomPartyMemberIfPossible`](Abilities_and_Spells.md#object-applytorandompartymemberifpossible) | Object ||| `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer ||| `[1 .5]` (Array), `-1` (Number), `-2` (Number), `{ ... }` (Object) |
| `DexterityUp` | Enum / Integer ||| `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object ||| `chapter` (Enum), `pills` (Enum), `{ ... }` (Object) |
| `HealthGain` | Integer ||| `3*X` (Enum), `2*X` (Enum), `5` (Number), `10` (Number) |
| `IntelligenceUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object ||| `BestBud` (Enum), `SmallRock` (Enum), `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusOnBreakItem`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer || 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Thorns` | Integer || 36 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`DoDamage`](Abilities_and_Spells.md#object-dodamage) | Object ||| `{ ... }` (Object) |

</details>

---

#### `StatusOnCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer || 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Charge` | Integer ||| `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer ||| `3*X` (Enum), `2*X` (Enum), `5` (Number), `10` (Number) |

</details>

---

#### `StatusOnCollectPickup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Tech` | Integer || 2 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusOnDie`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_RandomChance`](Abilities_and_Spells.md#object-conditional_randomchance) | Object | Nested conditional. | 1 ||
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object ||| `pills` (Enum), `chapter_common` (Enum), `{ ... }` (Object) |
| [`RandomMagicMissile`](Abilities_and_Spells.md#object-randommagicmissile) | Integer / Object ||| `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `RemoveAmbientLightEffects` | Number ||| `4` (Number), `.5` (String) |
| [`ScatterCoins`](Abilities_and_Spells.md#object-scattercoins) | Object ||| `[1 .5]` (Array), `5` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusOnEatFood`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer || 26 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Cleanse`](#object-cleanse) | Integer / Object || 2 | `0` (Number), `1` (Number), `{ ... }` (Object) |
| `RandomStatUp` | Integer / String || 2 | `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `2` (Number), `-5` (Number) |
| `IntelligenceUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusOnEatPill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| [`AllStatsUp`](./Arrays.md#array-allstatsup) | Enum / Integer | Applies or references the 'AllStatsUp' effect/state. | 0 ||
| [`RandomPermanentStatsDistinct`](#object-randompermanentstatsdistinct) | Object | Examples: `{ ... }` | 0 ||

</details>

---

#### `StatusOnEndMove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_FirstApplicationThisTurn`](Abilities_and_Spells.md#object-conditional_firstapplicationthisturn) | Object | Nested conditional. | 1 ||
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Nested conditional. | 1 ||
| `Charge` | Integer ||| `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer ||| `[1 .5]` (Array), `[1 .33]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`ForceAttack`](Abilities_and_Spells.md#object-forceattack) | Integer / Object ||| `1` (Number), `{ ... }` (Object) |
| [`ImmediateUseAbility`](#object-immediateuseability) | Enum / Object ||| `MoonHandMegaSqueeze` (Enum), `head_MagnetoAttract` (Enum), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `SpeedUp_WithoutInitiative` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`RemoveStatusStacks`](Abilities_and_Spells.md#object-removestatusstacks) | Object | Removes a specific number of stacks of a status effect. | 0 ||
| [`DivineShield`](./Arrays.md#array-divineshield) | Array / Integer | Applies or references the 'DivineShield' effect/state. | 0 ||
| [`ImmediateUseAbility`](#object-immediateuseability) | Enum / Object | Applies or references the 'ImmediateUseAbility' effect/state. | 0 ||
| `Charge` | Integer | Applies or references the 'Charge' effect/state. | 0 ||
| `SpeedUp_WithoutInitiative` | Integer | Applies or references the 'SpeedUp_WithoutInitiative' effect/state. | 0 ||
| [`ForceAttack`](Abilities_and_Spells.md#object-forceattack) | Integer / Object | Forces the character to execute an immediate attack. | 0 ||
| `SpeedUp` | Enum / Integer | Applies or references the 'SpeedUp' effect/state. | 0 ||

</details>

---

#### `StatusOnGainCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer || 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`BackflipWhenTargeted`](Abilities_and_Spells.md#object-backflipwhentargeted) | Enum / Integer / Object || 2 | `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer ||| `[1 .5]` (Array), `[1 .33]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `LuckUp` | Enum / Integer ||| `[1 .5]` (Array), `222` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusOnHealed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer || 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Thorns` | Integer || 36 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object ||| `SmallRock` (Enum), `SkeletonCatFamiliar` (Enum), `{ ... }` (Object) |

</details>

---

#### `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 40

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer || 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `HealthRegenUp` | Integer || 26 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String || 6 | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object | Nested conditional. | 4 ||
| [`Conditional_FirstApplicationThisTurn`](Abilities_and_Spells.md#object-conditional_firstapplicationthisturn) | Object | Nested conditional. | 2 ||
| `RandomStatUp` | Integer / String || 2 | `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `2` (Number), `-5` (Number) |
| `Stealth` | Array / Integer || 2 | `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `CharismaUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer ||| `[1 .5]` (Array), `-1` (Number), `-2` (Number), `{ ... }` (Object) |
| `DexterityUp` | Enum / Integer ||| `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer ||| `3*X` (Enum), `2*X` (Enum), `5` (Number), `10` (Number) |
| `IntelligenceUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `LuckUp` | Enum / Integer ||| `[1 .5]` (Array), `222` (Number), `2` (Number), `{ ... }` (Object) |
| `RangeUp` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `BrittleCharismaUp` | Integer | Applies or references the 'BrittleCharismaUp' effect/state. | 0 ||
| `BrittleConstitutionUp` | Integer | Applies or references the 'BrittleConstitutionUp' effect/state. | 0 ||
| `BrittleDexterityUp` | Integer | Applies or references the 'BrittleDexterityUp' effect/state. | 0 ||
| `BrittleIntelligenceUp` | Integer | Applies or references the 'BrittleIntelligenceUp' effect/state. | 0 ||
| `BrittleLuckUp` | Integer | Applies or references the 'BrittleLuckUp' effect/state. | 0 ||
| `BrittleSpeedUp` | Integer | Applies or references the 'BrittleSpeedUp' effect/state. | 0 ||
| `BrittleStrengthUp` | Integer | Applies or references the 'BrittleStrengthUp' effect/state. | 0 ||
| [`UseAbility_NonStack`](./Enums.md#enum-useability_nonstack) | Enum | Applies or references the 'UseAbility_NonStack' effect/state. | 0 ||

</details>

---

#### `StatusOnKillEnemy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object || 20 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String || 6 | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer ||| `[1 .5]` (Array), `[1 .33]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object ||| `head_HitlersToupe` (Enum), `tk_JarOfRadiation` (Enum), `{ ... }` (Object) |
| `HealthGain` | Integer ||| `3*X` (Enum), `2*X` (Enum), `5` (Number), `2` (Number) |
| `LuckUp` | Enum / Integer ||| `[1 .5]` (Array), `222` (Number), `2` (Number), `{ ... }` (Object) |
| `ManaGain` | Enum / Integer ||| `X` (Enum), `item_aux` (Enum), `5` (Number), `2` (Number), `"max(X*3, 0)"` (String), `"max((X-1)*2, 0)"` (String) |

</details>

---

#### `StatusOnPickupCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DexterityUp` | Enum / Integer ||| `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `GainCoins` | Array / Integer ||| `[3 5]` (Array), `5` (Number), `2` (Number) |
| `SpeedUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusOnPopCorpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthGain` | Integer ||| `3*X` (Enum), `2*X` (Enum), `2` (Number), `1` (Number) |
| `RepairWeapon` | Array / Integer ||| `[1 .25]` (Array), `99` (Number), `1` (Number) |

</details>

---

#### `StatusOnTookDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 46

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer || 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Thorns` | Integer || 36 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Bleed` | Array / Integer || 9 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String || 6 | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_HasStatus`](Abilities_and_Spells.md#object-conditional_hasstatus) | Object | Nested conditional. | 2 ||
| [`Craft`](Abilities_and_Spells.md#object-craft) | Object || 2 | `{ ... }` (Object) |
| `DodgeChance_Status` | Integer || 2 | `[1 .5]` (Array), `5` (Number), `40` (Number), `{ ... }` (Object) |
| `RandomStatUp` | Integer / String || 2 | `"ceil(X/3)"` (Enum), `"ceil(X/2)"` (Enum), `2` (Number), `-5` (Number) |
| [`Conditional_HealthThreshold`](Abilities_and_Spells.md#object-conditional_healththreshold) | Object | Nested conditional. | 1 ||
| [`Else`](Abilities_and_Spells.md#object-else) | Object || 1 | `{ ... }` (Object) |
| `Charge` | Integer ||| `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer ||| `[1 .5]` (Array), `-1` (Number), `-2` (Number), `{ ... }` (Object) |
| `DiminishingHealthRegen` | Integer ||| `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer ||| `[1 .5]` (Array), `[1 .33]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `IntelligenceUp` | Enum / Integer ||| `[1 .5]` (Array), `-1` (Number), `3` (Number), `{ ... }` (Object) |
| `LuckUp` | Enum / Integer ||| `[1 .5]` (Array), `222` (Number), `2` (Number), `{ ... }` (Object) |
| `MovementUp` | Integer ||| `[1 .5]` (Array), `-2` (Number), `1` (Number), `{ ... }` (Object) |
| `RandomInjury` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `TempDamageUp` | Integer ||| `[1 .5]` (Array), `-1` (Number), `1` (Number), `{ ... }` (Object) |
| `TempMovement` | Enum / Integer ||| `[1 .5]` (Array), `1` (Number), `20` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusOnTookDamageFromAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Shield` | Enum / Integer || 422 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `HealthRegenUp` | Integer || 26 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Bleed` | Array / Integer || 9 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `DiminishingHealthRegen` | Integer ||| `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `ExtraBasicAttacks_Status` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusOnUseBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageUp` | Integer / String || 6 | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer ||| `3*X` (Enum), `2*X` (Enum), `5` (Number), `10` (Number) |

</details>

---

#### `StatusRandomEnemiesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Array / Integer || 9 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object || 6 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`count`](./Arrays.md#array-count) | Array / Integer | Quantity. | 3 ||
| `Charmed` | Array / Enum / Integer ||| `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer ||| `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Freeze` | Array / Integer ||| `[1 .1]` (Array), `[1 0.15]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `StatusWhenAllySpendsMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Charge` | Integer ||| `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `ManaGain` | Enum / Integer ||| `X` (Enum), `item_aux` (Enum), `5` (Number), `2` (Number), `"max(X*3, 0)"` (String), `"max((X-1)*2, 0)"` (String) |
| [`OneUseSpellDamageUp`](#object-oneusespelldamageup) | Array / Number / Object ||| `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |

</details>

---

#### `TakeBonusTurnWithAIControl`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `include_spells` | Boolean | If true, allows the AI to cast spells during this bonus turn. | 3 ||
| `end_of_round` | Boolean | `true` | 1 ||

</details>

---

#### `TakeBonusTurnWithStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object || 6 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object ||| `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Stun` | Array / Integer ||| `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |

</details>

---

#### `TempPassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer || 26 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`status`](./Enums.md#enum-status) | Enum | The required status effect. | 3 ||

</details>

---

#### `additional_passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageUp` | Integer / String || 6 | `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `FillMana` | Integer ||| `[1 .10]` (Array), `[1 .25]` (Array), `1` (Number) |
| `HealthGain` | Integer ||| `3*X` (Enum), `2*X` (Enum), `5` (Number), `10` (Number) |
| `PermanentMadness` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`ReviveNextRound`](Abilities_and_Spells.md#object-revivenextround) | Integer / Object ||| `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `SafeDoomed` | Enum / Integer ||| `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `bonus_passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 138

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CritChanceUp` | Integer || 36 | `[1 .5]` (Array), `5` (Number), `1` (Number), `{ ... }` (Object) |
| `HealthRegenUp` | Integer || 26 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Trample` | Integer || 14 | `[1 .5]` (Array), `[3 X-8]` (Array), `5` (Number), `9` (Number), `{ ... }` (Object) |
| [`AutocastEachRound`](Abilities_and_Spells.md#object-autocasteachround) | Enum / Object || 4 | `SpiderReturn` (Enum), `{ ... }` (Object) |
| `AlphaDodgeChance` | Integer ||| `[1 .5]` (Array), `50` (Number), `1` (Number), `{ ... }` (Object) |
| `DownRankAIIfWeaponUsable` | Number ||| `.001` (String) |
| `IntelligenceUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| [`XIsSpellStormRampAndReset`](Abilities_and_Spells.md#object-xisspellstormrampandreset) | Integer / Object ||| `0` (Number), `{ ... }` (Object) |

</details>

---

#### `extra_statuses`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Poison` | Array / Integer || 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Conditional_HasTag`](Abilities_and_Spells.md#object-conditional_hastag) | Object | Nested conditional. | 1 ||
| `Burn` | Array / Enum / Integer || 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer ||| `3*X` (Enum), `2*X` (Enum), `5` (Number), `10` (Number) |
| `Tarred` | Array / Integer ||| `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |

</details>

---

#### `party_status_next_fight`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 24

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HealthRegenUp` | Integer || 26 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Bleed` | Array / Integer || 9 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Poison` | Array / Integer || 8 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Immobile` | Array / Integer || 4 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `10` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer ||| `[1 .5]` (Array), `[1 .33]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer ||| `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`NoHealthRegen`](#object-nohealthregen) | Array / Number / Object ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`Tangled`](Abilities_and_Spells.md#object-tangled) | Array / Integer / Object ||| `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Tarred` | Array / Integer ||| `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `Webbed` | Integer ||| `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |

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
| `HealthRegenUp` | Integer || 26 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `MissChance` | Integer || 24 | `[1 .5]` (Array), `5` (Number), `10` (Number), `{ ... }` (Object) |
| `Bleed` | Array / Integer || 9 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object || 8 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Poison` | Array / Integer || 8 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Blind` | Array / Integer || 6 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object || 6 | `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| [`Slow`](Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object || 4 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `Burn` | Array / Enum / Integer || 1 | `[1 .5]` (Array), `[1 .1]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `CharismaUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer ||| `[1 .5]` (Array), `-1` (Number), `-2` (Number), `{ ... }` (Object) |
| `DexterityUp` | Enum / Integer ||| `[1 .5]` (Array), `-1` (Number), `1` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer ||| `[1 .5]` (Array), `[1 .33]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer ||| `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `IntelligenceUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `LuckUp` | Enum / Integer ||| `[1 .5]` (Array), `222` (Number), `2` (Number), `{ ... }` (Object) |
| [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object ||| `[1 .1]` (Array), `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`NoHealthRegen`](#object-nohealthregen) | Array / Number / Object ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`NoManaRegen`](Passives_and_Statuses.md#object-nomanaregen) | Array / Number / Object ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`PermanentConfusion`](#object-permanentconfusion) | Array / Number / Object ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `ProbeCharmed` | Integer ||| `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Rot` | Array / Integer ||| `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `-999999` (Number), `{ ... }` (Object) |
| `Sleep` | Array / Integer ||| `[1 .1]` (Array), `[1 .5]` (Array), `8` (Number), `3` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `SpiderInfested` | Integer ||| `[1 .5]` (Array), `4` (Number), `1` (Number), `{ ... }` (Object) |
| `StrengthUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `Stun` | Array / Integer ||| `[1 .5]` (Array), `[1 .1]` (Array), `2` (Number), `3` (Number), `{ ... }` (Object) |
| `Tarred` | Array / Integer ||| `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `TempStrengthUp` | Enum ||| `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |
| `Webbed` | Integer ||| `[1 .1]` (Array), `[1 .5]` (Array), `2` (Number), `1` (Number), `{ ... }` (Object) |

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
| `alias` | Enum ||| `DodgeChance_Status` (Enum) |

### Object: `AlphaStatusOnTurnBegin`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DoubleCastSpellThisTurn` | Integer || 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |

### Object: `ApplyPassivesToSpawnerWhileAlive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `HideEquipment` | Enum || 2 | `neck` (Enum) |

### Object: `ApplyToRandomPartyMemberIfPossible`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`GainDisorderFromPool`](Characters_and_Bosses.md#object-gaindisorderfrompool) | Enum / Object || 4 | `all_disorders` (Enum), `{ ... }` (Object) |

### Object: `ApplyToSource`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer || 12 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer || 12 | `2*X` (Enum), `3*X` (Enum), `3` (Number), `8` (Number) |
| `StrengthUp` | Enum / Integer || 12 | `[1 .5]` (Array), `4` (Number), `-2` (Number), `{ ... }` (Object) |
| `Shield` | Enum / Integer || 10 | `[1 .5]` (Array), `5` (Number), `2` (Number), `{ ... }` (Object) |
| [`EvolveAbilityFromPool`](Abilities_and_Spells.md#object-evolveabilityfrompool) | Enum / Object || 8 | `Medic` (Enum), `Psychic` (Enum), `{ ... }` (Object) |
| [`FormChange`](Abilities_and_Spells.md#object-formchange) | Enum / Object || 8 | `Default` (Enum), `passive` (Enum), `{ ... }` (Object) |
| `AddWeaponAux` | Integer / String || 6 | `-item_aux` (Enum), `1` (Number), `2` (Number), `"-max(min(X+1, item_aux), 0)"` (String) |
| `ConstitutionUp` | Array / Enum / Integer || 6 | `[1 .5]` (Array), `-1` (Number), `-2` (Number), `{ ... }` (Object) |
| `Charge` | Integer || 4 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| [`Cleanse`](#object-cleanse) | Integer / Object || 4 | `1` (Number), `0` (Number), `{ ... }` (Object) |
| `EquipPermanentItem` | Enum || 4 | `BoneClub` (Enum), `Kidney` (Enum) |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object || 4 | `chapter_specific_item` (Enum), `chapter_common` (Enum), `{ ... }` (Object) |
| `FreeSpell` | Integer || 4 | `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `LuckUp` | Enum / Integer || 4 | `[1 .5]` (Array), `-4` (Number), `3` (Number), `{ ... }` (Object) |
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object || 2 | `[1 .5]` (Array), `10` (Number), `4` (Number), `{ ... }` (Object) |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object || 2 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| `DivineShield` | Array / Integer || 2 | `[1 .5]` (Array), `[1 .33]` (Array), `4` (Number), `1` (Number), `{ ... }` (Object) |
| `FindItem` | Enum || 2 | `BoneClub` (Enum), `Pearl` (Enum) |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object || 2 | `neck_ChefsApron` (Enum), `head_HitlersToupe` (Enum), `{ ... }` (Object) |
| [`GainCoinsRange`](Abilities_and_Spells.md#object-gaincoinsrange) | Object || 2 | `{ ... }` (Object) |
| `KineticSpikes` | Integer || 2 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `ManaGain` | Enum / Integer || 2 | `X-1` (Enum), `X+2` (Enum), `15` (Number), `10` (Number), `"max((X-1)*2, 0)"` (String), `"max(X*3, 0)"` (String) |
| `MoveQuivered` | Integer || 2 | `[1 0.1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer || 2 | `[1 .5]` (Array), `-2` (Number), `6` (Number), `{ ... }` (Object) |
| `Tech` | Integer || 2 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |

### Object: `BlessingOfPeace`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_BLESSINGOFPEACE_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_BLESSINGOFPEACE_DESC"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_BLESSINGOFPEACE_DESC_STACKLESS"` (String) |

### Object: `BounceObject`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `obj` | Array / Enum || 6 | `SmallLavaRock` (Enum), `chapter_corpse_medium` (Enum) |
| `chance` | Number || 4 | `.5` (String), `.25` (String) |
| `slide` | Integer || 2 | `10` (Number) |

### Object: `Bounty`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_BOUNTY_NAME"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_BOUNTY_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_BOUNTY_DESC"` (String) |

### Object: `ChangeTile`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `tile` | Array / Enum || 22 | `[TallGrassTile TallFlowerTile BrambleTile]` (Array), `LavaTile` (Enum), `ToxicTile` (Enum) |
| `aoe` | Integer || 4 | `1` (Number) |
| `chance` | Number || 4 | `25` (Number), `.25` (String) |

### Object: `CharismaUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_CHAUP_NAME"` (String) |
| `name_stacks_neg` | String ||| `"KEYWORD_CHADOWN_NAME"` (String) |
| `tooltip_stackless` | Enum ||| `none` (Enum) |
| `tooltip_stacks_neg` | String ||| `"KEYWORD_CHADOWN_DESC"` (String) |
| `tooltip_stacks_pos` | String ||| `"KEYWORD_CHAUP_DESC"` (String) |

### Object: `Charmed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_CHARMED_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_CHARMED_DESC"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_CHARMED_DESC_STACKLESS"` (String) |

### Object: `Cleanse`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object ||| `{ ... }` (Object) |
| `template` | Enum ||| `spell` (Enum) |

### Object: `Cleave`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number || 2 | `.25` (String) |
| `icon_frame` | Number ||| `152` (Number) |
| `name` | Enum ||| `"KEYWORD_CLEAVE_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_CLEAVE_DESC"` (String) |

### Object: `Conditional_Adjacent`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Bleed` | Array / Integer || 4 | `[1 .1]` (Array), `[3 .1]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |
| `BonusDamage` | Enum / Integer || 4 | `"ceil(X/2)"` (Enum), `str` (Enum), `-4` (Number), `3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `effects` | Object | Effects to execute. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | | |

### Object: `Conditional_Ally`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DamageUp` | Integer / String || 10 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer || 6 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| [`Cleanse`](#object-cleanse) | Integer / Object || 6 | `1` (Number), `0` (Number), `{ ... }` (Object) |
| `HealthGain` | Integer || 4 | `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `RandomStatUp` | Integer / String || 4 | `"ceil(X/2)"` (Enum), `"ceil(X/3)"` (Enum), `10` (Number), `3` (Number) |
| `Shield` | Enum / Integer || 4 | `[1 .5]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `TempSpeedUp` | Enum / Integer || 4 | `[1 .5]` (Array), `10` (Number), `4` (Number), `{ ... }` (Object) |
| `BleedThorns` | Integer || 2 | `[1 .5]` (Array), `6` (Number), `3` (Number), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer || 2 | `[1 .1+.02*cha]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `ManaGain` | Enum / Integer || 2 | `X-1` (Enum), `X+2` (Enum), `15` (Number), `10` (Number), `"max((X-1)*2, 0)"` (String), `"max(X*3, 0)"` (String) |
| `SpeedUp` | Enum / Integer || 2 | `[1 .5]` (Array), `-2` (Number), `6` (Number), `{ ... }` (Object) |
| `TempDamageUp` | Integer || 2 | `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `Thorns` | Integer || 2 | `[1 .5]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |
| `effects` | Object | Effects to execute. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | | |

### Object: `Conditional_BadRoll`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Number || 16 | `0.5` (Number), `.16666666` (String), `.1` (String) |
| `Instakill` | Integer || 2 | `[25 .01]` (Array), `25` (Number), `50` (Number) |
| [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object || 2 | `[1 .1]` (Array), `[1 .5]` (Array), `999` (Number), `3` (Number), `{ ... }` (Object) |
| `effects` | Object | Effects to execute. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | | |

### Object: `Conditional_Boss`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Stun` | Array / Integer || 6 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer || 4 | `[1 .5]` (Array), `-1` (Number), `3` (Number), `{ ... }` (Object) |
| `BonusDamage` | Enum / Integer || 4 | `"ceil(X/2)"` (Enum), `str` (Enum), `25` (Number), `-4` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Charmed` | Array / Enum / Integer || 4 | `[1 .1+.02*cha]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `Drowsy` | Integer || 4 | `[1 .5]` (Array), `8` (Number), `1` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer || 2 | `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `effects` | Object | Effects to execute. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | | |

### Object: `Conditional_Corpse`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Revive`](#object-revive) | Integer / Object || 13 | `50` (Number), `100` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer || 4 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer || 4 | `[1 .1+.02*cha]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `SafeDoomed` | Enum / Integer || 4 | `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String || 2 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| `HealRandomInjury` | Integer || 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `PermanentCharm` | Integer || 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `RandomMutation` | Integer || 2 | `3` (Number), `1` (Number) |
| `SpeedUp` | Enum / Integer || 2 | `[1 .5]` (Array), `-2` (Number), `6` (Number), `{ ... }` (Object) |
| [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object || 1 | `[1 .1]` (Array), `[1 .5]` (Array), `999` (Number), `3` (Number), `{ ... }` (Object) |
| `effects` | Object | Effects to execute. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | | |

### Object: `Conditional_Enemy`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object || 16 | `[2 .15]` (Array), `[1 .1]` (Array), `4` (Number), `2` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer || 4 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `Attraction` | Integer || 4 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer || 4 | `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object || 4 | `[1 .1]` (Array), `[1 .5]` (Array), `999` (Number), `3` (Number), `{ ... }` (Object) |
| [`Weakness`](Passives_and_Statuses.md#object-weakness) | Array / Integer / Object || 4 | `[1 .1]` (Array), `[1 .25]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |
| `BonusDamage` | Enum / Integer || 2 | `"ceil(X/2)"` (Enum), `str` (Enum), `-4` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Burn` | Array / Enum / Integer || 2 | `[1 .1]` (Array), `[1 .25]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer || 2 | `[1 .1+.02*cha]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `Doomed` | Integer || 2 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `Hex` | Integer || 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`Leeches`](#object-leeches) | Integer / Object || 2 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| [`Marked`](#object-marked) | Array / Integer / Object || 2 | `[1 .1]` (Array), `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `PermanentCharm` | Integer || 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Poison` | Array / Integer || 2 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |
| `TempDamageUp` | Integer || 2 | `[1 .5]` (Array), `1` (Number), `-1` (Number), `{ ... }` (Object) |
| `Stun` | Array / Integer ||| `[1 .1]` (Array), `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `effects` | Object | Effects to execute. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | | |

### Object: `Conditional_FirstApplicationThisTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer || 2 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `Charge` | Integer || 2 | `[1 .5]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| `FillMana` | Integer || 2 | `[1 .25]` (Array), `[1 .10]` (Array), `1` (Number) |
| `ManaGain` | Enum / Integer || 2 | `X-1` (Enum), `X+2` (Enum), `15` (Number), `10` (Number), `"max((X-1)*2, 0)"` (String), `"max(X*3, 0)"` (String) |
| `effects` | Object | Effects to execute. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | | |

### Object: `Conditional_GoodRoll`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `odds` | Number || 72 | `15` (Number), `50` (Number), `.5` (String) |
| `Freeze` | Array / Integer || 12 | `[1 .1]` (Array), `[1 0.15]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`FindItemFromPool`](Abilities_and_Spells.md#object-finditemfrompool) | Enum / Object || 10 | `parasites` (Enum), `chapter_specific_item` (Enum), `{ ... }` (Object) |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object || 6 | `cm_RaptorEggSpawn` (Enum), `tk_WeirdEgg_Spawn` (Enum), `{ ... }` (Object) |
| `RandomMutation` | Integer || 6 | `3` (Number), `1` (Number) |
| `ChangeTilesUnder` | Enum || 2 | `LavaTile` (Enum), `DirtTile` (Enum) |
| [`ImmediateUseAbility`](#object-immediateuseability) | Enum / Object || 2 | `cm_Lard_Impl` (Enum), `tk_ButterBean_Mega` (Enum), `{ ... }` (Object) |
| `effects` | Object | Effects to execute. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | | |

### Object: `Conditional_HasCleansableDebuffs`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `GenericBuff` | Integer || 2 | `100` (Number), `5` (Number) |
| `PartialCleanse` | Integer || 2 | `1` (Number), `9999` (Number) |
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object || 2 | `{ ... }` (Object) |
| `VisualFX` | Enum || 2 | `MagicMissleBlast` (Enum), `BigMagicMissileBlast` (Enum) |
| `effects` | Object | Effects to execute. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | | |

### Object: `Conditional_HasStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BonusDamage` | Enum / Integer || 12 | `"ceil(X/2)"` (Enum), `str` (Enum), `20` (Number), `10` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Burn` | Array / Enum / Integer || 4 | `[1 .1]` (Array), `[1 .25]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object || 4 | `[2 .15]` (Array), `[1 .1]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| [`Slow`](Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object || 4 | `[1 .1]` (Array), `[1 .25]` (Array), `-1` (Number), `3` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer || 2 | `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| [`FormChange`](Abilities_and_Spells.md#object-formchange) | Enum / Object || 2 | `passive` (Enum), `Bully` (Enum), `{ ... }` (Object) |
| `Quivered` | Array / Integer || 2 | `[1 0.1]` (Array), `[1 .5]` (Array), `1` (Number), `5` (Number), `{ ... }` (Object) |
| `effects` | Object | Effects to execute. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | | |

### Object: `Conditional_HasTag`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ImmediateUseAbility`](#object-immediateuseability) | Enum / Object || 6 | `HitlerCloneTransform` (Enum), `head_ThrobbingCrown` (Enum), `{ ... }` (Object) |
| `ChangeTilesUnder` | Enum || 4 | `LavaTile` (Enum), `DirtTile` (Enum) |
| `DamageUp` | Integer / String || 4 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| [`Die`](Characters_and_Bosses.md#object-die) | Integer / Object || 4 | `6` (Number), `1` (Number), `{ ... }` (Object) |
| `BonusDamage` | Enum / Integer || 2 | `"ceil(X/2)"` (Enum), `str` (Enum), `10` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| `Charmed` | Array / Enum / Integer || 2 | `[1 .1+.02*cha]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `EventBounty` | Integer || 2 | `[1 .5]` (Array), `1` (Number), `5` (Number), `{ ... }` (Object) |
| `Instakill` | Integer || 2 | `[25 .01]` (Array), `25` (Number), `50` (Number) |
| [`PopAndSpawn`](Abilities_and_Spells.md#object-popandspawn) | Enum / Object || 2 | `TheDestroyer` (Enum), `StemCat_HalfHealth` (Enum), `{ ... }` (Object) |
| [`UseAbility`](Abilities_and_Spells.md#object-useability) | Enum / Object || 2 | `GirlDinoPoop` (Enum), `TormentorRuneAbsorb` (Enum), `{ ... }` (Object) |
| `effects` | Object | Effects to execute. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | | |

### Object: `Conditional_HealthThreshold`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BonusDamage` | Enum / Integer || 2 | `"ceil(X/2)"` (Enum), `str` (Enum), `-4` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| [`Die`](Characters_and_Bosses.md#object-die) | Integer / Object || 2 | `6` (Number), `1` (Number), `{ ... }` (Object) |
| `FlatLeech` | Integer || 2 | `X` (Enum), `10` (Number), `1` (Number) |
| `Instakill` | Integer || 2 | `[25 .01]` (Array), `25` (Number), `50` (Number) |
| `effects` | Object | Effects to execute. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | | |

### Object: `Conditional_ManaThreshold`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RepairTrinket` | Integer || 2 | `1` (Number), `99` (Number) |
| `effects` | Object | Effects to execute. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | | |

### Object: `Conditional_NotBoss`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Doomed` | Integer || 4 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `PermanentCharm` | Integer || 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer ||| `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `effects` | Object | Effects to execute. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | | |

### Object: `Conditional_PartyMember`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Charmed` | Array / Enum / Integer || 4 | `[1 .1+.02*cha]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `effects` | Object | Effects to execute. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | | |

### Object: `Conditional_Shielded`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Cleave`](Abilities_and_Spells.md#object-cleave) | Integer / Object || 4 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `BonusDamage` | Enum / Integer || 2 | `"ceil(X/2)"` (Enum), `str` (Enum), `-4` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| [`SetItemAux`](#object-setitemaux) | Object || 2 | `{ ... }` (Object) |
| `Stun` | Array / Integer || 2 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `effects` | Object | Effects to execute. | | |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Variable | Properties for conditional execution. | | |

### Object: `ConstitutionUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_CONUP_NAME"` (String) |
| `name_stacks_neg` | String ||| `"KEYWORD_CONDOWN_NAME"` (String) |
| `tooltip_stackless` | Enum ||| `none` (Enum) |
| `tooltip_stacks_neg` | String ||| `"KEYWORD_CONDOWN_DESC"` (String) |
| `tooltip_stacks_pos` | String ||| `"KEYWORD_CONUP_DESC"` (String) |

### Object: `Craft`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pool` | Array / Enum || 30 | `pelts` (Enum), `eyes_nonrare` (Enum) |
| `slot` | Enum / Integer || 28 | `weapon` (Enum), `trinket` (Enum) |
| `temporary` | Boolean || 8 | `false` (Boolean) |
| `works_with_tech` | Boolean || 8 | `true` (Boolean) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object ||| `{ ... }` (Object) |
| `template` | Enum ||| `self_buff` (Enum) |

### Object: `CureDisease`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number || 12 | `30` (Number), `15` (Number) |
| `disease` | Enum || 12 | `Pox` (Enum), `Covid` (Enum) |
| `can_apply_to_anything` | Boolean || 2 | `true` (Boolean) |

### Object: `DelayedPain`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_DELAYEDPAIN_NAME"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_DELAYEDPAIN_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_DELAYEDPAIN_DESC"` (String) |

### Object: `DestroyEquipmentAndAttachParasite`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number || 8 | `1` (Number), `.75` (String), `.15` (String) |
| `pool` | Array / Enum || 4 | `[AmoebaHat AmoebaNeck AmoebaFace]` (Array), `[FlyHat FlyMask FlyNeck]` (Array), `parasites` (Enum) |

### Object: `DexterityUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_DEXUP_NAME"` (String) |
| `name_stacks_neg` | String ||| `"KEYWORD_DEXDOWN_NAME"` (String) |
| `tooltip_stackless` | Enum ||| `none` (Enum) |
| `tooltip_stacks_neg` | String ||| `"KEYWORD_DEXDOWN_DESC"` (String) |
| `tooltip_stacks_pos` | String ||| `"KEYWORD_DEXUP_DESC"` (String) |

### Object: `DiminishingHealthRegen`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_DIMINISHREGEN_NAME"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_DIMINISHREGEN_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_DIMINISHREGEN_DESC"` (String) |

### Object: `DistanceBonusDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `min_range` | Integer || 8 | `3` (Number), `1` (Number) |
| `stacks` | Enum / Integer || 8 | `1` (Number) |

### Object: `DoDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Equation || 14 | `8` (Equation), `5` (Equation) |
| `type` | Enum || 14 | `melee` (Enum), `generic_physical` (Enum) |
| `damage_tiles` | Enum || 8 | `all` (Enum) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object || 8 | `{ ... }` (Object) |
| `elements` | Array ||| `[Fire]` (Array), `[Water]` (Array) |

### Object: `DoubleCastSpellThisTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_DOUBLECASTTHISTURN_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_DOUBLECASTTHISTURN_DESC"` (String) |

### Object: `Drowsy`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_DROWSY_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_DROWSY_DESC"` (String) |

### Object: `Else`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BonusDamage` | Enum / Integer || 12 | `"ceil(X/2)"` (Enum), `str` (Enum), `-4` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |
| [`Cleanse`](#object-cleanse) | Integer / Object || 4 | `1` (Number), `0` (Number), `{ ... }` (Object) |
| [`Confusion`](Passives_and_Statuses.md#object-confusion) | Array / Integer / Object || 4 | `[2 .15]` (Array), `[1 .1]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| [`FormChange`](Abilities_and_Spells.md#object-formchange) | Enum / Object || 4 | `passive` (Enum), `Nuke` (Enum), `{ ... }` (Object) |
| [`GainCoinsRange`](Abilities_and_Spells.md#object-gaincoinsrange) | Object || 4 | `{ ... }` (Object) |
| [`Marked`](#object-marked) | Array / Integer / Object || 4 | `[1 .1]` (Array), `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `PermanentCharm` | Integer || 4 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `RandomStatDown` | Array / Integer / String || 4 | `[1 .25]` (Array), `"ceil(X/2)"` (Enum), `"ceil(X/3)"` (Enum), `1` (Number) |
| `RandomStatUp` | Integer / String || 4 | `"ceil(X/2)"` (Enum), `"ceil(X/3)"` (Enum), `10` (Number), `3` (Number) |
| [`Revive`](#object-revive) | Integer / Object || 4 | `50` (Number), `100` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer || 2 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| [`Bruise`](Passives_and_Statuses.md#object-bruise) | Array / Integer / Object || 2 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `4` (Number), `{ ... }` (Object) |
| `Charmed` | Array / Enum / Integer || 2 | `[1 .1+.02*cha]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| [`Cleave`](Abilities_and_Spells.md#object-cleave) | Integer / Object || 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `ConstitutionUp` | Array / Enum / Integer || 2 | `[1 .5]` (Array), `-1` (Number), `-2` (Number), `{ ... }` (Object) |
| `CritChanceUp` | Integer || 2 | `[1 .5]` (Array), `50` (Number), `20` (Number), `{ ... }` (Object) |
| `DamageUp` | Integer / String || 2 | `[1 .5]` (Array), `-2` (Number), `3` (Number), `{ ... }` (Object) |
| `DodgeChance_Status` | Integer || 2 | `[1 .5]` (Array), `15` (Number), `66` (Number), `{ ... }` (Object) |
| [`DybbukPossessed`](Abilities_and_Spells.md#object-dybbukpossessed) | Object || 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Fear` | Array / Integer || 2 | `[1 .1]` (Array), `[1 .05]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| [`ImmediateUseAbility`](#object-immediateuseability) | Enum / Object || 2 | `cm_Lard_Impl` (Enum), `tk_ButterBean_Mega` (Enum), `{ ... }` (Object) |
| `Immobile` | Array / Integer || 2 | `[1 .1]` (Array), `[1 .25]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |
| `Instakill` | Integer || 2 | `[25 .01]` (Array), `25` (Number), `50` (Number) |
| [`Leeches`](#object-leeches) | Integer / Object || 2 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object || 2 | `Maggot` (Enum), `BeefyCharmedLeech` (Enum), `{ ... }` (Object) |
| `PartialCleanse` | Integer || 2 | `1` (Number), `9999` (Number) |
| [`ScatterCoins`](Abilities_and_Spells.md#object-scattercoins) | Object || 2 | `[1 .5]` (Array), `5` (Number), `{ ... }` (Object) |
| [`Slow`](Passives_and_Statuses.md#object-slow) | Array / Enum / Integer / Object || 2 | `[1 .1]` (Array), `[1 .25]` (Array), `-1` (Number), `3` (Number), `{ ... }` (Object) |
| `SpeedUp` | Enum / Integer || 2 | `[1 .5]` (Array), `-2` (Number), `6` (Number), `{ ... }` (Object) |
| `TempSpeedUp` | Enum / Integer || 2 | `[1 .5]` (Array), `10` (Number), `4` (Number), `{ ... }` (Object) |
| `Webbed` | Integer || 2 | `[1 .1]` (Array), `[1 .5]` (Array), `1` (Number), `2` (Number), `{ ... }` (Object) |
| [`AllyInfested`](Engine_LogicKeys.md#object-allyinfested) | Array / Number / Object || 1 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `Poison` | Array / Integer ||| `[1 .1]` (Array), `[1 .5]` (Array), `3` (Number), `6` (Number), `{ ... }` (Object) |

### Object: `Fear`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_FEAR_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_FEAR_DESC"` (String) |

### Object: `ForceAttack`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `immediate` | Boolean || 4 | `true` (Boolean) |

### Object: `ForceUseAbilityOnTarget`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 2 | `head_MiniMoonArmorAsteroid` (Enum) |
| `chance` | Number || 2 | `25` (Number) |

### Object: `FormChange`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `form` | Enum / Integer || 150 | `Rage` (Enum), `"Default"` (Enum), `4` (Number), `1` (Number) |
| `chance` | Number || 2 | `30` (Number) |

### Object: `Freeze`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_FREEZE_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_FREEZE_DESC"` (String) |

### Object: `GainCoinsRange`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer || 22 | `30` (Number), `3` (Number) |
| `min` | Integer || 22 | `30` (Number), `15` (Number) |

### Object: `GainDisorderFromPool`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number || 2 | `.1` (String) |
| `pool` | Array / Enum || 2 | `diseases` (Enum) |

### Object: `Hex`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_HEX_NAME"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_HEX_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_HEX_DESC"` (String) |

### Object: `ImmediateUseAbility`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 2 | `wp_NuclearKnifeExplode` (Enum) |
| `even_if_stunned` | Boolean || 2 | `true` (Boolean) |

### Object: `IncAuxCounterClamped`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `change` | Integer || 6 | `-2` (Number), `-3` (Number) |
| `max` | Integer || 6 | `3` (Number) |

### Object: `Infested`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object ||| `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object ||| `{ ... }` (Object) |
| `class` | Enum ||| `Colorless` (Enum) |
| `default_frame` | Number ||| `1002` (Number) |
| `desc` | Enum ||| `"PASSIVE_INFESTED_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| `icon_frame` | Number ||| `517` (Number) |
| `lefteye` | Number ||| `1040` (Number) |
| `lefteyebrow` | Number ||| `1022` (Number) |
| `mouth` | Number ||| `1041` (Number) |
| `name` | Enum ||| `"PASSIVE_INFESTED_NAME"` (String), `"KEYWORD_INFESTED_NAME"` (String) |
| `palette` | Enum / Integer ||| `50` (Number) |
| [`passives`](Cat_Mutations.md#object-passives) | Object ||| `{ ... }` (Object) |
| `pitch` | String ||| `.7` (String) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object ||| `{ ... }` (Object) |
| `righteye` | Number ||| `1041` (Number) |
| `righteyebrow` | Number ||| `1022` (Number) |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object ||| `{ ... }` (Object) |
| `texture` | Integer ||| `1000` (Number) |
| `tooltip` | Enum ||| `"KEYWORD_INFESTED_DESC"` (String) |
| `value` | Enum ||| `1` (Number) |
| `voice` | Enum ||| `female2` (Enum) |

### Object: `IntelligenceUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_INTUP_NAME"` (String) |
| `name_stacks_neg` | String ||| `"KEYWORD_INTDOWN_NAME"` (String) |
| `tooltip_stackless` | Enum ||| `none` (Enum) |
| `tooltip_stacks_neg` | String ||| `"KEYWORD_INTDOWN_DESC"` (String) |
| `tooltip_stacks_pos` | String ||| `"KEYWORD_INTUP_DESC"` (String) |

### Object: `KnockOutCoin`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number || 2 | `.5` (String) |
| `stacks` | Enum / Integer || 2 | `1` (Number) |

### Object: `KnockUpAndAway`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer || 48 | `3` (Number), `-3` (Number) |
| `stacks` | Enum / Integer || 44 | `5+bonus_melee_ability_damage` (Enum), `3` (Number), `1` (Number) |
| `displace` | Boolean || 4 | `true` (Boolean) |
| `height` | Integer || 4 | `0` (Number), `2` (Number) |
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Boolean / Integer / Object || 4 | `false` (Boolean) |
| `circular_variance` | Integer || 2 | `2` (Number) |

### Object: `Knockback`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"Knockback"` (Enum) |
| `tooltip` | Enum ||| `None` (Enum) |

### Object: `KnockbackIfCrit`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `knockback` | Enum / Integer || 2 | `10` (Number) |
| `override_chain_knockback` | Integer || 2 | `10` (Number) |

### Object: `Leech`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum ||| `"SETBONUS_LEECH_DESC"` (String) |
| `icon_frame` | Number ||| `17` (Number) |
| `name` | Enum ||| `"SETBONUS_LEECH_NAME"` (String), `"KEYWORD_LIFESTEAL_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object ||| `{ ... }` (Object) |
| `pieces_required` | Number ||| `3` (Number) |
| `tooltip` | Enum ||| `"KEYWORD_LIFESTEAL2_DESC"` (String) |

### Object: `Leeches`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| `name` | Enum ||| `"KEYWORD_LEECHES_NAME"` (String) |
| `name_reference_applier` | String ||| `"KEYWORD_LEECHES_NAME_APPLIER"` (String) |
| [`target`](Abilities_and_Spells.md#object-target) | Object ||| `{ ... }` (Object) |
| `template` | Enum ||| `lobbed_attack` (Enum) |
| `tooltip_reference_applier` | String ||| `"KEYWORD_LEECHES_DESC_APPLIER"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_LEECHES_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_LEECHES_DESC"` (String) |

### Object: `MagicWeakness`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_MAGICWEAKNESS_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_MAGICWEAKNESS_DESC"` (String) |

### Object: `ManaGainRange`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer || 2 | `4` (Number) |
| `min` | Integer || 2 | `0` (Number) |

### Object: `ManaLeeches`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_MANALEECHES_NAME"` (String) |
| `name_reference_applier` | String ||| `"KEYWORD_MANALEECHES_NAME_APPLIER"` (String) |
| `tooltip_reference_applier` | String ||| `"KEYWORD_MANALEECHES_DESC_APPLIER"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_MANALEECHES_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_MANALEECHES_DESC"` (String) |

### Object: `Marked`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| `name` | Enum ||| `"KEYWORD_MARKED_NAME"` (String) |
| [`target`](Abilities_and_Spells.md#object-target) | Object ||| `{ ... }` (Object) |
| `template` | Enum ||| `targeted_status` (Enum) |
| `tooltip` | Enum ||| `"KEYWORD_MARKED_DESC"` (String) |

### Object: `ModifyAbility`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object || 4 | `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object || 4 | `{ ... }` (Object) |

### Object: `MovementUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_MOVEMENTUP_NAME"` (String) |
| `name_stacks_neg` | String ||| `"KEYWORD_MOVEMENTDOWN_NAME"` (String) |
| `tooltip_stackless_neg` | String ||| `"KEYWORD_MOVEMENTDOWN_DESC_STACKLESS"` (String) |
| `tooltip_stackless_pos` | String ||| `"KEYWORD_MOVEMENTUP_DESC_STACKLESS"` (String) |
| `tooltip_stacks_neg` | String ||| `"KEYWORD_MOVEMENTDOWN_DESC"` (String) |
| `tooltip_stacks_pos` | String ||| `"KEYWORD_MOVEMENTUP_DESC"` (String) |

### Object: `NextBattleStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AllStatsUp` | Enum / Integer || 4 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `FullHeal` | Integer || 4 | `1` (Number), `0` (Number) |

### Object: `NoHealthRegen`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_NOHEALTHREGEN_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_NOHEALTHREGEN_DESC"` (String) |

### Object: `NukeQuestFinalBossModifications`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Boolean / Integer / Object || 4 | `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object || 2 | `{ ... }` (Object) |
| [`splash_damage`](Abilities_and_Spells.md#object-splash_damage) | Object || 2 | `{ ... }` (Object) |

### Object: `ObjectOnHitCharacter`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum || 14 | `CharmedLeech` (Enum), `CharmedTinySpider` (Enum) |
| `stacks` | Enum / Integer || 10 | `"floor(lck/4)"` (Enum), `1` (Number), `2` (Number) |
| `chance` | Number || 4 | `1` (Number), `.5` (String) |

### Object: `OneUseSpellDamageUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum ||| `SpellDamageUp` (Enum) |

### Object: `Ostracized`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_OSTRACIZED_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_OSTRACIZED_DESC"` (String) |

### Object: `PassiveWhileNotTakingTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object || 2 | `{ ... }` (Object) |

### Object: `PermanentConfusion`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_CONFUSION_NAME"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_CONFUSION_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_CONFUSION_DESC_STACKLESS"` (String) |

### Object: `Petrify`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_PETRIFY_NAME"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_PETRIFY_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_PETRIFY_DESC"` (String) |
| `tooltip_stacks_singular` | String ||| `KEYWORD_PETRIFY_DESC_SINGULAR` (String) |

### Object: `PoisonLace`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| `name` | Enum ||| `"KEYWORD_POISONLACE_NAME"` (String) |
| [`target`](Abilities_and_Spells.md#object-target) | Object ||| `{ ... }` (Object) |
| `template` | Enum ||| `targeted_status` (Enum) |
| `tooltip_stackless` | String ||| `"KEYWORD_POISONLACE_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_POISONLACE_DESC"` (String) |

### Object: `Possessed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_POSSESED_NAME"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_POSSESSED_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_POSSESSED_DESC"` (String) |
| `tooltip_stacks_singular` | String ||| `KEYWORD_POSSESSED_DESC_SIGNULAR` (String) |

### Object: `PreEmptiveCounterNextAttacks`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_PREEMTIVECOUNTER_NAME"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_PREEMTIVECOUNTER_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_PREEMTIVECOUNTER_DESC"` (String) |
| `tooltip_stacks_singular` | String ||| `"KEYWORD_PREEMTIVECOUNTER_DESC_STACKLESS"` (String) |

### Object: `ProbeCharmed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_PROBED_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_PROBED_DESC"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_PROBED_DESC_STACKLESS"` (String) |

### Object: `Purge`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object ||| `{ ... }` (Object) |
| `template` | Enum ||| `spell` (Enum) |

### Object: `RandomInjury`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number ||| `58` (Number) |
| `name` | Enum ||| `"KEYWORD_RANDOMINJURY_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_RANDOMINJURY_DESC"` (String) |

### Object: `RandomMagicMissile`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `full_size` | Boolean || 4 | `true` (Boolean) |
| `stacks` | Enum / Integer || 4 | `3` (Number), `4` (Number) |
| `icon_frame` | Number ||| `154` (Number) |
| `name` | Enum ||| `"KEYWORD_SPARKLE_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_SPARKLE_DESC"` (String) |

### Object: `RandomPermanentStatsDistinct`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object ||| `[1 -1]` (Array) |

### Object: `RangeUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_RANGEUP_NAME"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_RANGEUP_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_RANGEUP_DESC"` (String) |

### Object: `Reanimate`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object ||| `{ ... }` (Object) |
| `template` | Enum ||| `targeted_status` (Enum) |

### Object: `Reflect`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| `name` | Enum ||| `"KEYWORD_REFLECT_NAME"` (String) |
| `template` | Enum ||| `self_buff` (Enum) |
| `tooltip_stacks` | String ||| `"KEYWORD_REFLECT_DESC"` (String) |
| `tooltip_stacks_singular` | String ||| `"KEYWORD_REFLECT_DESC_STACKLESS"` (String) |

### Object: `RemoveStatusStacks`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer || 8 | `10` (Number), `1` (Number) |
| `status` | Enum || 8 | `Thorns` (Enum), `DodgeChance_Status` (Enum) |

### Object: `ReplaceSpell`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 8 | `MoonHeadCommandStopHittingYourself` (Enum), `None` (Enum) |
| `slot` | Enum / Integer || 8 | `3` (Number), `1` (Number) |

### Object: `Revive`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object ||| `{ ... }` (Object) |
| `template` | Enum ||| `melee_spell` (Enum) |

### Object: `ReviveNextRound`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `revive_health` | Integer || 8 | `100` (Number), `1` (Number) |
| `Shield` | Enum / Integer || 6 | `[1 .5]` (Array), `15` (Number), `5` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer || 4 | `[1 .5]` (Array), `-2` (Number), `-1` (Number), `{ ... }` (Object) |
| `stacks` | Enum / Integer || 4 | `2` (Number) |
| `DivineShield` | Array / Integer || 2 | `[1 .5]` (Array), `[1 .33]` (Array), `4` (Number), `1` (Number), `{ ... }` (Object) |
| `name` | Enum ||| `"KEYWORD_AUTOREVIVE_NAME"` (String) |
| `tooltip_stackless` | String ||| `KEYWORD_AUTOREVIVE_DESC` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_AUTOREVIVE_DESC"` (String) |
| `tooltip_stacks_singular` | String ||| `"KEYWORD_AUTOREVIVE_DESC_SINGULAR"` (String) |

### Object: `Rot`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_ROT_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_ROT_DESC"` (String) |

### Object: `ScatterCoins`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stackable` | Boolean || 4 | `true` (Boolean) |
| `stacks` | Enum / Integer || 4 | `item_aux` (Enum), `"max(min(X+1, item_aux), 0)"` (String) |

### Object: `Scrambled`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_SCRAMBLED_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_SCRAMBLED_DESC"` (String) |

### Object: `SetItemAux`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `slot` | Enum / Integer || 6 | `face` (Enum), `head` (Enum) |
| `value` | Enum || 6 | `item_aux+1` (Enum), `item_aux+2` (Enum) |

### Object: `Shield`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_SHIELD_NAME"` (String) |
| `tooltip` | Enum ||| `None` (Enum) |
| `tooltip_stackless` | String ||| `"KEYWORD_SHIELD_DESC_STACKLESS"` (String) |

### Object: `Sleep`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_SLEEP_NAME"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_SLEEP_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_SLEEP_DESC"` (String) |

### Object: `SoulLink`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| `name` | Enum ||| `"KEYWORD_SOULLINK_NAME"` (String) |
| [`target`](Abilities_and_Spells.md#object-target) | Object ||| `{ ... }` (Object) |
| `template` | Enum ||| `targeted_status` (Enum) |
| `tooltip` | Enum ||| `"KEYWORD_SOULLINK_DESC"` (String) |

### Object: `SpeedUp_WithoutInitiative`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum ||| `SpeedUp` (Enum) |

### Object: `SpiderInfested`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_SPIDERINFESTED_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_SPIDERINFESTED_DESC"` (String) |

### Object: `SpreadDisease`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `disease` | Enum || 26 | `Pox` (Enum), `Toxoplasmosis` (Enum) |
| `chance` | Number || 24 | `30` (Number), `50` (Number) |
| `can_apply_to_anything` | Boolean || 12 | `true` (Boolean) |

### Object: `StacyMutant_Brace`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Brace`](Events_and_Encounters.md#object-brace) | Enum / Integer / Object || 2 | `[1 .5]` (Array), `4` (Number), `10` (Number), `{ ... }` (Object) |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object || 2 | `{ ... }` (Object) |

### Object: `StacyMutant_Counter`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`AddStatusToBasicAttack`](Abilities_and_Spells.md#object-addstatustobasicattack) | Object || 2 | `{ ... }` (Object) |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object || 2 | `{ ... }` (Object) |
| [`CounterAttack`](Cat_Mutations.md#object-counterattack) | Array / Enum / Object || 2 | `[attack GSScream]` (Array), `CollectiveCounter` (Enum), `YeticatSnowball_Counter` (Enum), `{ ... }` (Object) |

### Object: `StacyMutant_Damage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddDamage` | Integer || 2 | `-1` (Number), `4` (Number) |
| `AddMaxHealth` | Integer || 2 | `25` (Number), `-25` (Number) |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object || 2 | `{ ... }` (Object) |

### Object: `StacyMutant_DoubleHead`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object || 2 | `{ ... }` (Object) |
| `ExtraDispersedTurns` | Integer || 2 | `1` (Number), `-1` (Number) |

### Object: `StacyMutant_Fire`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object || 2 | `{ ... }` (Object) |
| `ElementImmune` | Enum || 2 | `Fire` (Enum), `Creep` (Enum) |
| `ReplaceBasicAttack` | Enum || 2 | `BasicButcherMeleeWideSpin` (Enum), `BasicDruidAbilityVersatile` (Enum) |
| [`ReplaceBrain`](Characters_and_Bosses.md#object-replacebrain) | Object || 2 | `{ ... }` (Object) |

### Object: `StacyMutant_Health`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddMaxHealth` | Integer || 2 | `25` (Number), `10` (Number) |
| `AddSpeed` | Integer || 2 | `4` (Number), `-3` (Number) |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object || 2 | `{ ... }` (Object) |
| `SizeScale` | Number || 2 | `1.2` (Number), `1.65` (Number), `.6` (String), `.8` (String) |

### Object: `StacyMutant_Holy`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object || 2 | `{ ... }` (Object) |
| `DivineShield` | Array / Integer || 2 | `[1 .5]` (Array), `[1 .33]` (Array), `4` (Number), `1` (Number), `{ ... }` (Object) |

### Object: `StacyMutant_Ice`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddMovement` | Integer || 2 | `-1` (Number), `3` (Number) |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object || 2 | `{ ... }` (Object) |
| `ElementImmune` | Enum || 2 | `Fire` (Enum), `Creep` (Enum) |
| `ReplaceBasicAttack` | Enum || 2 | `BasicButcherMeleeWideSpin` (Enum), `BasicDruidAbilityVersatile` (Enum) |
| [`ReplaceBrain`](Characters_and_Bosses.md#object-replacebrain) | Object || 2 | `{ ... }` (Object) |

### Object: `StacyMutant_Lightning`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object || 2 | `{ ... }` (Object) |
| `ElementImmune` | Enum || 2 | `Fire` (Enum), `Creep` (Enum) |
| `ReplaceBasicAttack` | Enum || 2 | `SM_LightningDash` (Enum), `BasicButcherMeleeWideSpin` (Enum) |
| [`ReplaceBrain`](Characters_and_Bosses.md#object-replacebrain) | Object || 2 | `{ ... }` (Object) |

### Object: `StacyMutant_Mirror`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object || 2 | `{ ... }` (Object) |
| [`ReflectProjectiles`](Characters_and_Bosses.md#object-reflectprojectiles) | Integer / Object || 2 | `25` (Number), `20` (Number), `{ ... }` (Object) |
| [`StatusEachTurnEndForEachTurn`](Characters_and_Bosses.md#object-statuseachturnendforeachturn) | Object || 2 | `{ ... }` (Object) |

### Object: `StacyMutant_Speed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AddDamage` | Integer || 2 | `-1` (Number), `4` (Number) |
| `AddSpeed` | Integer || 2 | `6` (Number), `-3` (Number) |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object || 2 | `{ ... }` (Object) |
| `SizeScale` | Number || 2 | `1.1` (Number), `1.3` (Number), `.6` (String), `.8` (String) |

### Object: `StacyMutant_Thorns`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`CatPartsTransform`](Abilities_and_Spells.md#object-catpartstransform) | Object || 2 | `{ ... }` (Object) |
| `Thorns` | Integer || 2 | `[1 .5]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |

### Object: `StatusAfterXStacks`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stack_key` | Enum || 4 | `EMPTY_GENERATOR` (String), `FANNY_PACK` (String) |
| [`threshold`](Items_and_Equipment.md#object-threshold) | Enum / Integer / Object || 4 | `3` (Number), `12` (Number) |
| `ExtraBasicMoves_Status` | Integer || 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `RefreshActPoints` | Integer || 2 | `1` (Number) |
| `expires_on_end_turn` | Boolean || 2 | `true` (Boolean) |

### Object: `StealthUntilBasicAttack`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_STEALTHUNTIL_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_STEALTHUNTIL_DESC"` (String) |

### Object: `Stun`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_STUN_NAME"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_STUN_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_STUN_DESC"` (String) |

### Object: `Tangled`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alt_art` | Enum || 2 | `TangledMeat` (Enum) |
| `stacks` | Enum / Integer || 2 | `1` (Number) |
| `name` | Enum ||| `"KEYWORD_TANGLED_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_TANGLED_DESC"` (String) |

### Object: `Tarred`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_TARRED_NAME"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_TARRED_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_TARRED_DESC"` (String) |

### Object: `TempCounterAttack`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_TEMPCOUNTER_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_TEMPCOUNTER_DESC"` (String) |

### Object: `TempDamageUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum ||| `DamageUp` (Enum) |

### Object: `TempMovement`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum ||| `MovementUp` (Enum) |

### Object: `TempPassiveUntilSettled`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`MeleeRevengeDamage`](Abilities_and_Spells.md#object-meleerevengedamage) | Object || 4 | `{ ... }` (Object) |
| `LimitHeal` | Integer || 2 | `1` (Number), `0` (Number) |

### Object: `TempRangeUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_TEMPRANGE_NAME"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_TEMPRANGE_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_TEMPRANGE_DESC"` (String) |

### Object: `TempSpellDamageUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum ||| `SpellDamageUp` (Enum) |

### Object: `TempStrengthUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum ||| `StrengthUp` (Enum) |

### Object: `Temporary`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer || 114 | `5` (Number), `-2` (Number) |
| `status` | Enum || 112 | `Trample` (Enum), `Brace` (Enum) |
| [`turns`](Characters_and_Bosses.md#object-turns) | Array / Integer / Object || 104 | `3` (Number), `1` (Number) |
| `expires_on_begin_turn` | Boolean || 50 | `true` (Boolean) |
| `expires_on_end_turn` | Boolean || 42 | `true` (Boolean) |
| `data` | Integer || 4 | `2` (Number) |
| `expires_on_appliers_turn` | Boolean || 4 | `true` (Boolean) |
| `expires_on_move` | Boolean || 2 | `true` (Boolean) |

### Object: `TransformWeapon`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `from` | Enum || 4 | `Necro_SoulDagger_Charged` (Enum), `Necro_SoulDagger_Uncharged` (Enum) |
| `to` | Enum || 4 | `Necro_SoulDagger_Charged` (Enum), `Necro_SoulDagger_Uncharged` (Enum) |

### Object: `Webbed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_WEBBED_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_WEBBED_DESC"` (String) |

### Object: `Wet`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_WET_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_WET_DESC"` (String) |

### Object: `XIsSpellStormRampAndReset`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `reset_percent` | Integer || 2 | `50` (Number) |
| `stacks` | Enum / Integer || 2 | `0` (Number) |

#### `ApplyToSourceOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 15

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `AlphaCat` | Integer || 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| [`Revive`](#object-revive) | Integer / Object || 2 | `1` (Number), `50` (Number), `{ ... }` (Object) |
| `AllStatsUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| [`EvolveAbilityFromPool`](Abilities_and_Spells.md#object-evolveabilityfrompool) | Enum / Object ||| `Hunter` (Enum), `Fighter` (Enum), `{ ... }` (Object) |
| `HealthGain` | Integer ||| `2*X` (Enum), `3*X` (Enum), `10` (Number), `4` (Number) |
| `ManaGain` | Enum / Integer ||| `X` (Enum), `item_aux` (Enum), `5` (Number), `2` (Number), `"max(X*3, 0)"` (String), `"max((X-1)*2, 0)"` (String) |
| `StrengthUp` | Enum / Integer ||| `[1 .5]` (Array), `-2` (Number), `2` (Number), `{ ... }` (Object) |
| `WeaponAuxMultiplier` | Number ||| `.5` (String) |

</details>

---

#### `Consumed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 23

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`struggle_ability`](./Enums.md#enum-struggle_ability) | Enum | Ability triggered by the consumed entity while inside the consumer. | 17 ||
| `force_contact` | Boolean | If true, enforces physical overlap. | 15 ||
| `instant` | Boolean | Examples: `true` | 12 ||
| [`mount_mode`](./Enums.md#enum-mount_mode) | Boolean / Enum | If true, treats the consumption as riding/mounting instead of eating. | 12 ||
| `do_not_pop_corpse` | Boolean | Examples: `true` | 11 ||
| [`drop_on_death`](./Enums.md#enum-drop_on_death) | Boolean / Enum | Examples: `false, true, deferred` | 11 ||
| `wet` | Boolean | Examples: `false, true` | 8 ||
| `drop_on_self_death` | Boolean | Examples: `true` | 3 ||
| [`extra_statuses`](Abilities_and_Spells.md#object-extra_statuses) | Object | Additional generic status applications. | 3 ||
| `use_placeholder` | Boolean | Examples: `true` | 3 ||
| [`drop_body_ability`](./Enums.md#enum-drop_body_ability) | Enum | Examples: `MoonHandDrop` | 1 ||
| `kill_on_consume` | Boolean | Examples: `true` | 1 ||

</details>

---

### Object: `AcidRain`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha` | String ||| `.5` (String) |
| `ambient_sound` | String ||| `amb_acidrain.ogg` (String) |
| `chain` | Boolean ||| `AcidSplash` (Enum) |
| `desc` | Enum ||| `"WEATHER_ACIDRAIN_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object ||| `{ ... }` (Object) |
| `emit_amount` | Number ||| `1` (Number) |
| `emit_box` | Array ||| `[0 10 10 10 0 10]` (Array) |
| `emit_direction` | Array ||| `[0 -1 0]` (Array) |
| `emit_rate` | Number ||| `100` (Number) |
| `emit_spread` | Number ||| `0` (Number) |
| `face_moving_direction` | Boolean ||| `true` (Boolean) |
| `force` | Array ||| `[0 -10 0]` (Array) |
| `live_bounds` | Array ||| `[-999 999 0 999 -999 999]` (Array) |
| `movieclip` | Array / Enum ||| `AcidRainParticle` (Enum) |
| `name` | Enum ||| `"WEATHER_ACIDRAIN_NAME"` (String) |
| `particle_lifetime` | Number ||| `5` (Number) |
| `projection_matrix` | Enum ||| `default` (Enum) |
| `render_mode` | Enum ||| `separate` (Enum) |
| [`scripts`](Miscellaneous.md#object-scripts) | Object ||| `{ ... }` (Object) |
| `simulation_space` | Enum ||| `global` (Enum) |
| `size_start` | String ||| `.5` (String) |
| `speed_scale` | String ||| `.1` (String) |
| `speed_start` | Number ||| `10` (Number) |

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
| `name` | Enum ||| `"KEYWORD_ADRENALINE_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_ADRENALINE_DESC"` (String) |

### Object: `ApplyMultipleTimes`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`RandomStatusFromPool`](Abilities_and_Spells.md#object-randomstatusfrompool) | Object || 6 | `{ ... }` (Object) |
| `stacks` | Enum / Integer || 6 | `X` (Enum), `4` (Number), `8` (Number) |

### Object: `ApplyStatusesNextTurnBegin`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Quivered` | Array / Integer || 2 | `[1 0.1]` (Array), `[1 .5]` (Array), `1` (Number), `5` (Number), `{ ... }` (Object) |

### Object: `ApplyToConsumed`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `DeleteObject` | Integer || 6 | `1` (Number) |
| [`Die`](Characters_and_Bosses.md#object-die) | Integer / Object || 2 | `6` (Number), `1` (Number), `{ ... }` (Object) |

### Object: `ApplyToOthersWithSharedTagAndFaction`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Marked`](#object-marked) | Array / Integer / Object || 2 | `[1 .1]` (Array), `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |

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
| `enemies_only` | Boolean || 8 | `false` (Boolean), `true` (Boolean) |
| `max_distance` | Integer || 8 | `3` (Number), `1` (Number) |
| `stacks` | Enum / Integer || 8 | `100` (Number) |
| `chance` | Number || 2 | `.5` (String) |
| `ignore_self` | Boolean || 2 | `true` (Boolean) |

### Object: `Bloodzerked`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_BLOODZERK_NAME"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_BLOODZERK_DESC"` (String) |

### Object: `BodyGuard`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 4 | `BodyGuardSwap2` (Enum), `BodyGuardSwap` (Enum) |
| `stacks` | Enum / Integer || 4 | `1` (Number) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| `name` | Enum ||| `"KEYWORD_BODYGUARD_NAME"` (String) |
| `template` | Enum ||| `self_buff` (Enum) |
| `tooltip` | Enum ||| `"KEYWORD_BODYGUARD_DESC"` (String) |

### Object: `BombRatTurtle`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| `template` | Enum ||| `self_buff` (Enum) |

### Object: `ButterflySwarm`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ambient_sound` | String ||| `amb_butterflyswarm.ogg` (String) |
| `desc` | Enum ||| `"WEATHER_BUTTERFLY_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object ||| `{ ... }` (Object) |
| `name` | Enum ||| `"WEATHER_BUTTERFLY_NAME"` (String) |

### Object: `CanApplyToInanimate`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ObjectOnHitCharacter`](Abilities_and_Spells.md#object-objectonhitcharacter) | Enum / Object || 20 | `AllyRotFly` (Enum), `CharmedLeech` (Enum), `{ ... }` (Object) |
| `BreakIntoRocks` | Enum || 8 | `Coin` (Enum), `SmallRock` (Enum) |
| [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object || 6 | `{ ... }` (Object) |
| `Vaporize` | Integer || 6 | `1` (Number), `20` (Number) |
| `GetAggroTarget` | Integer || 4 | `1` (Number) |
| `PreventDeathTransforms` | Integer || 2 | `1` (Number) |
| [`Temporary`](Abilities_and_Spells.md#object-temporary) | Object || 2 | `{ ... }` (Object) |

### Object: `CastAgainWithStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `OverrideDamage` | Integer || 2 | `25` (Number), `10` (Number) |
| `stacks` | Enum / Integer || 2 | `1` (Number) |

### Object: `CatPartsSizeScaleStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `arm1` | Number || 2 | `1.1` (Number) |
| `arm2` | Number || 2 | `1.1` (Number) |
| `body` | Number || 2 | `1.1` (Number) |
| `mouth` | Number || 2 | `1.1` (Number) |

### Object: `ChampionUpgradeNextMinion`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_PROMOTE_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_PROMOTE_DESC"` (String) |

### Object: `ChanceToBreakFree`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 22 | `CHuskDrop` (Enum), `LennyDrop` (Enum) |
| `fail_ability` | Enum || 6 | `CHuskDropFail` (Enum), `XXX` (Enum) |
| `stacks` | Enum / Integer || 6 | `25` (Number) |

### Object: `ChargeFists`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`keyword_tooltips`](Abilities_and_Spells.md#object-keyword_tooltips) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| `name` | Enum ||| `"KEYWORD_CHARGEFISTS_NAME"` (String) |
| `template` | Enum ||| `self_buff` (Enum) |
| `tooltip_stackless` | String ||| `"KEYWORD_CHARGEFISTS_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_CHARGEFISTS_DESC"` (String) |
| `tooltip_stacks_singular` | String ||| `"KEYWORD_CHARGEFISTS_DESC_SINGULAR"` (String) |

### Object: `CockroachSwarm`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum ||| `"WEATHER_COCKROACHES_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object ||| `{ ... }` (Object) |
| `name` | Enum ||| `"WEATHER_COCKROACHES_NAME"` (String) |

### Object: `CollectsPickupsWithAltEffects`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Tech` | Integer || 4 | `[1 .5]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `CurrentWeaponAddPoison` | Integer || 2 | `[1 .5]` (Array), `1` (Number), `{ ... }` (Object) |
| `LuckUp` | Enum / Integer || 2 | `[1 .5]` (Array), `-4` (Number), `3` (Number), `{ ... }` (Object) |
| `Quivered` | Array / Integer || 2 | `[1 0.1]` (Array), `[1 .5]` (Array), `1` (Number), `5` (Number), `{ ... }` (Object) |
| `RandomStatUp` | Integer / String || 2 | `"ceil(X/2)"` (Enum), `"ceil(X/3)"` (Enum), `10` (Number), `3` (Number) |
| `Shield` | Enum / Integer || 2 | `[1 .5]` (Array), `10` (Number), `3` (Number), `{ ... }` (Object) |

### Object: `CopySpells`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer || 2 | `1` (Number) |
| `upgraded` | Boolean || 2 | `true` (Boolean) |

### Object: `Counterspell`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| `template` | Enum ||| `self_buff` (Enum) |

### Object: `CurrentWeaponAddPoison`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_WPOISONLACE_NAME"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_WPOISONLACE_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_WPOISONLACE_DESC"` (String) |

### Object: `DelayCastAbility`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 2 | `FetusAirstrike` (Enum) |
| `lingering` | Boolean || 2 | `true` (Boolean) |
| `relative` | Boolean || 2 | `false` (Boolean) |

### Object: `DelayedWind`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer || 2 | `2` (Number) |

### Object: `DelayedWindCone`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `distance` | Integer || 4 | `10` (Number) |
| `damage` | Equation || 2 | `5` (Equation) |

### Object: `DoDistortionRing`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `intensity` | Integer || 12 | `-2` (Number), `1` (Number) |
| `radius` | Array / Integer || 12 | `4` (Number), `5` (Number) |
| `speed` | Array / Number || 12 | `30` (Number), `-30` (Number) |

### Object: `DoScreenShake`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `intensity` | Integer || 20 | `10` (Number), `3` (Number) |
| `time` | Number || 20 | `1` (Number), `2` (Number), `.75` (String), `.5` (String) |

### Object: `DoubleCast`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_DOUBLECAST_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_DOUBLECAST_DESC"` (String) |

### Object: `DoubleCastSpell`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_DOUBLECASTSPELL_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_DOUBLECASTSPELL_DESC"` (String) |

### Object: `DoubleLoot`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| `template` | Enum ||| `self_buff` (Enum) |

### Object: `Drag`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum ||| `Psychic` (Enum) |
| `desc` | Enum ||| `"PASSIVE_DRAG_DESC"` (String) |
| `name` | Enum ||| `"PASSIVE_DRAG_NAME"` (String) |

### Object: `DustOnHit`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum || 6 | `GasCloud` (Enum) |

### Object: `EliteUpgradeNextMinion`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_PROMOTE2_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_PROMOTE2_DESC"` (String) |

### Object: `EmptyMind`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| `name` | Enum ||| `"KEYWORD_EMPTYMIND_NAME"` (String) |
| `template` | Enum ||| `self_buff` (Enum) |
| `tooltip` | Enum ||| `"KEYWORD_EMPTYMIND_DESC"` (String) |

### Object: `Enlarge`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Boolean / Integer / Object ||| `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object ||| `{ ... }` (Object) |
| `template` | Enum ||| `spell` (Enum) |

### Object: `FactionUprising`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`extra_statuses`](Abilities_and_Spells.md#object-extra_statuses) | Object || 1 | `{ ... }` (Object) |
| `tag` | Array / Enum || 1 | `bird` (Enum) |

### Object: `FireArmor`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum ||| `Mage` (Enum) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| `desc` | Enum ||| `"PASSIVE_FIREASPECT_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| `name` | Enum ||| `"FireArmor"` (Enum), `"PASSIVE_FIREASPECT_NAME"` (String) |
| `template` | Enum ||| `self_buff` (Enum) |
| `tooltip` | Enum ||| `None` (Enum) |

### Object: `FireArmor2`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| `name` | Enum ||| `"FireArmor2"` (Enum) |
| `template` | Enum ||| `self_buff` (Enum) |
| `tooltip` | Enum ||| `None` (Enum) |

### Object: `FireStorm`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `combo` | Array ||| `[Firestorm_Fire Firestorm_Embers Firestorm_Distortion]` (Array) |

### Object: `FireflySwarm`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum ||| `"WEATHER_FIREFLY_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object ||| `{ ... }` (Object) |
| `name` | Enum ||| `"WEATHER_FIREFLY_NAME"` (String) |

### Object: `FlySwarm`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object ||| `{ ... }` (Object) |
| [`ai`](Characters_and_Bosses.md#object-ai) | Object ||| `{ ... }` (Object) |
| `ambient_sound` | String ||| `amb_flyswarm.ogg` (String) |
| `desc` | Enum ||| `"WEATHER_FLYSWARM_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object ||| `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| `name` | Enum ||| `"WEATHER_FLYSWARM_NAME"` (String) |
| [`passives`](Cat_Mutations.md#object-passives) | Object ||| `{ ... }` (Object) |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object ||| `{ ... }` (Object) |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object ||| `{ ... }` (Object) |

### Object: `Fog`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_end` | Number ||| `0` (Number) |
| `alpha_start` | Number ||| `2` (Number) |
| `desc` | Enum ||| `"WEATHER_FOG_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object ||| `{ ... }` (Object) |
| `emit_amount` | Number ||| `1` (Number) |
| `emit_box` | Array ||| `[-5 10 0 2 -5 10]` (Array) |
| `emit_direction` | Array ||| `[0 1 0]` (Array) |
| `emit_rate` | Number ||| `100` (Number) |
| `emit_spread` | Number ||| `360` (Number) |
| `friction` | Array ||| `[0 1 0]` (Array) |
| `live_bounds` | Array ||| `[-999 999 -999 999 -999 999]` (Array) |
| `movieclip` | Array / Enum ||| `FogParticle` (Enum) |
| `name` | Enum ||| `"WEATHER_FOG_NAME"` (String) |
| `particle_lifetime` | Array ||| `[3 5]` (Array) |
| `projection_matrix` | Enum ||| `default` (Enum) |
| `render_mode` | Enum ||| `separate` (Enum) |
| [`scripts`](Miscellaneous.md#object-scripts) | Object ||| `{ ... }` (Object) |
| `simulation_space` | Enum ||| `global` (Enum) |
| `size_start` | Array ||| `[.2 1]` (Array) |
| `speed_start` | String ||| `.1` (String) |

### Object: `ForceImmediateMoveAndAttack`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 2 | `G3GrabHead` (Enum) |
| `even_if_cant_reach` | Boolean || 2 | `true` (Boolean) |

### Object: `ForceMoveTowardsTaggedObject`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 4 | `MoveOneTrample` (Enum), `MoveTwoTrample` (Enum) |
| `tag` | Array / Enum || 2 | `food` (Enum) |

### Object: `GlobalSpawnOnRoundEnd`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum || 2 | `NeutralZombieKitten` (Enum), `NeutralTwister` (Enum) |
| `number` | Array / Integer ||| `[1 2]` (Array) |

### Object: `Grappled`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_GRAPPLED_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_GRAPPLED_DESC"` (String) |

### Object: `Grappling`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`exit_animations`](Characters_and_Bosses.md#object-exit_animations) | Object || 2 | `{ ... }` (Object) |
| `partial_animation_suffix` | Enum / Integer || 2 | `Grapple` (Enum) |

### Object: `HealAlliesEachTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `exclude_self` | Boolean || 4 | `false` (Boolean) |
| `mana` | Enum / Integer || 4 | `3` (Number), `2` (Number) |
| `stacks` | Enum / Integer || 4 | `3` (Number), `2` (Number) |

### Object: `HeatWave`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `combo` | Array ||| `[HeatWave_Particles HeatWave_Distortion]` (Array) |
| `desc` | Enum ||| `"WEATHER_HEATWAVE_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object ||| `{ ... }` (Object) |
| `hint_persistent_elements` | Array ||| `[Heat]` (Array) |
| `name` | Enum ||| `"WEATHER_HEATWAVE_NAME"` (String), `"KEYWORD_DEHYDRATED_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_DEHYDRATED_DESC"` (String) |

### Object: `HeavyHits`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_HEAVYHITS_NAME"` (String) |
| `tooltip_stackless` | Enum ||| `none` (Enum) |
| `tooltip_stacks` | String ||| `"KEYWORD_HEAVYHITS_DESC_STACKS"` (String) |

### Object: `HolyDamageBlessing`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Burn` | Array / Enum / Integer || 4 | `[1 .1]` (Array), `[1 .25]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |
| `damage_multiplier` | Number || 4 | `3` (Number), `2` (Number) |

### Object: `IceArmor`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | Enum ||| `Mage` (Enum) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| `desc` | Enum ||| `"PASSIVE_ICEASPECT_DESC"` (String) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| `name` | Enum ||| `"IceArmor"` (Enum), `"PASSIVE_ICEASPECT_NAME"` (String) |
| `template` | Enum ||| `self_buff` (Enum) |
| `tooltip` | Enum ||| `None` (Enum) |

### Object: `IncAuxCounterCycle`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `change` | Integer || 2 | `1` (Number) |
| `max` | Integer || 2 | `3` (Number) |

### Object: `Invulnerable`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_INVULNERABLE_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_INVULNERABLE_DESC"` (String) |

### Object: `JudgementDay`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum ||| `"WEATHER_JUDGEMENT_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object ||| `{ ... }` (Object) |
| `name` | Enum ||| `"WEATHER_JUDGEMENT_NAME"` (String) |

### Object: `KillEnemyOfTypeAtBattleStart`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `enemy_type` | Enum || 2 | `cat` (Enum), `any` (Enum) |
| `fallback_spawn` | Array ||| `[TomTom Kitten CatCaller Mangy]` (Array) |

### Object: `LateStatusApplication`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `CurrentWeaponDamageUp` | Integer || 6 | `3` (Number), `1` (Number) |
| `AddWeaponAux` | Integer / String || 2 | `-item_aux` (Enum), `1` (Number), `2` (Number), `"-max(min(X+1, item_aux), 0)"` (String) |

### Object: `LeaveBehind`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum || 8 | `CharmedMaggot` (Enum), `Twister` (Enum) |

### Object: `Math`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `Stun` | Array / Integer || 4 | `[1 .1]` (Array), `[1 .25]` (Array), `3` (Number), `1` (Number), `{ ... }` (Object) |
| `stacks` | Enum / Integer || 4 | `1` (Number) |
| [`ApplyToSource`](Abilities_and_Spells.md#object-applytosource) | Object || 2 | `{ ... }` (Object) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object ||| `{ ... }` (Object) |
| `template` | Enum ||| `spell` (Enum) |

### Object: `Meaty`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_MEATY_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_MEATY_DESC"` (String) |

### Object: `MergeDamageInstance`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `can_instapop` | Boolean || 2 | `false` (Boolean) |
| `force_no_hit_animation` | Boolean || 2 | `true` (Boolean) |

### Object: `MeteorShower`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | Enum ||| `"WEATHER_METEORS_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object ||| `{ ... }` (Object) |
| `name` | Enum ||| `"WEATHER_METEORS_NAME"` (String) |

### Object: `Meteornado`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_in` | String ||| `.2` (String) |
| `alpha_out` | String ||| `.2` (String) |
| `desc` | Enum ||| `"WEATHER_METEORNADO_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object ||| `{ ... }` (Object) |
| `emit_amount` | Number ||| `1` (Number) |
| `emit_box` | Array ||| `[0 10 0 5 0 10]` (Array) |
| `emit_direction` | Array ||| `[0 1 0]` (Array) |
| `emit_rate` | Number ||| `200` (Number) |
| `emit_spread` | Number ||| `360` (Number) |
| `live_bounds` | Array ||| `[-999 999 -999 999 -999 999]` (Array) |
| `movieclip` | Array / Enum ||| `FX_MoonRock` (Enum) |
| `name` | Enum ||| `"WEATHER_METEORNADO_NAME"` (String) |
| `particle_lifetime` | Array ||| `[.1 3]` (Array) |
| `projection_matrix` | Enum ||| `default` (Enum) |
| `render_mode` | Enum ||| `separate` (Enum) |
| `rotation` | Array ||| `[0 360]` (Array) |
| `rotation_speed` | Array ||| `[-1000 1000]` (Array) |
| [`scripts`](Miscellaneous.md#object-scripts) | Object ||| `{ ... }` (Object) |
| `simulation_space` | Enum ||| `global` (Enum) |
| `size_start` | Array ||| `[.5 1.5]` (Array) |
| `speed_start` | Number ||| `5` (Number) |

### Object: `Metronome`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer || 2 | `1` (Number) |
| `ability` | Enum ||| `tk_Metronome` (Enum) |
| `banned_abilities` | Array ||| `[BatteryNuke WeAreOne Metronome SmartMetronome BecomeEntropy ForbiddenFamine]` (Array) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| `desc` | Enum ||| `"ITEM_METRONOME_DESC"` (String) |
| `frame` | Integer ||| `17` (Number) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| `kind` | Enum ||| `trinket` (Enum) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| `name` | Enum ||| `"ITEM_METRONOME_NAME"` (String) |
| `rarity` | Enum ||| `rare` (Enum) |
| `set` | Array / Enum ||| `Jester` (Enum) |
| `tags` | Array / Enum ||| `[musical]` (Array) |
| `template` | Enum ||| `self_buff` (Enum) |

### Object: `Muted`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_MUTED_NAME"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_MUTED_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_MUTED_DESC"` (String) |
| `tooltip_stacks_singular` | String ||| `"KEYWORD_MUTED_DESC_SINGULAR"` (String) |

### Object: `NextAbilityHeals`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"NextAbilityHeals"` (Enum) |
| `tooltip` | Enum ||| `None` (Enum) |

### Object: `NextActionLuckUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum ||| `LuckUp` (Enum) |

### Object: `NextAttackBonusRange`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_BONUSRANGE_NAME"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_BONUSRANGE_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_BONUSRANGE_DESC"` (String) |

### Object: `NextAttackSpecialCrit`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `crit_multiplier_bonus` | Integer || 2 | `2` (Number) |
| `extra_coins_per_stack` | Integer || 2 | `2` (Number) |
| `luck_increase` | Integer || 2 | `1` (Number) |

### Object: `NextBasicAttackCritsThisTurn`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `cant_miss` | Boolean || 2 | `true` (Boolean) |
| `piercing` | Boolean || 2 | `true` (Boolean) |
| `stacks` | Enum / Integer || 2 | `1` (Number) |

### Object: `NextBattleStatusStacks`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `MadnessChanceOnTurnBegin` | Integer || 2 | `2` (Number) |
| `fights` | Integer || 2 | `9999` (Number) |

### Object: `NextDamageReduceAndHealAllies`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"NextDamageReduceAndHealAllies"` (Enum) |
| `tooltip` | Enum ||| `None` (Enum) |

### Object: `NextTurnDoubleRangedDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_DOUBLERANGEDDMG_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_DOUBLERANGEDDMG_DESC"` (String) |

### Object: `ObjectOnHit`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum || 4 | `Poop` (Enum) |

### Object: `OverHealToStatuses`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `RandomStatUp` | Integer / String || 2 | `"ceil(X/2)"` (Enum), `"ceil(X/3)"` (Enum), `10` (Number), `3` (Number) |
| `TakeExtraTurn` | Integer || 2 | `1` (Number) |
| `stack_scale` | Integer || 2 | `0` (Number) |

### Object: `PoolMetronome`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pool` | Array / Enum ||| `[Shockwave Ping Telefrag Stasis Reduce Zealot]` (Array) |

### Object: `QuakeAreaChance`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `chance` | Number || 4 | `50` (Number) |
| `radius` | Array / Integer || 4 | `1` (Number), `0` (Number) |

### Object: `RandomDistanceDisplace`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `min_dist` | Integer || 2 | `4` (Number) |
| `stacks` | Enum / Integer || 2 | `20` (Number) |

### Object: `RandomKnockback`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max` | Integer || 4 | `10` (Number), `3` (Number) |
| `min` | Integer || 4 | `1` (Number) |

### Object: `ReduceManaCostExcludeBrainstorm`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_INSIGHT_NAME"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_INSIGHT_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_INSIGHT_DESC"` (String) |

### Object: `Regurge`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Boolean / Integer / Object ||| `{ ... }` (Object) |
| [`spawn`](Abilities_and_Spells.md#object-spawn) | Object ||| `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object ||| `{ ... }` (Object) |
| `template` | Enum ||| `spawn` (Enum) |

### Object: `RepressedMemoriesMetronome`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pool` | Array / Enum || 4 | `Psychic` (Enum), `Jester` (Enum) |
| `stacks` | Enum / Integer || 4 | `1` (Number) |

### Object: `Sandstorm`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ambient_sound` | String ||| `amb_sandstorm.ogg` (String) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| `desc` | Enum ||| `"WEATHER_SANDSTORM_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| `name` | Enum ||| `"WEATHER_SANDSTORM_NAME"` (String) |
| `template` | Enum ||| `self_buff` (Enum) |

### Object: `ScrambleLastUsedSpell`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `permanent` | Boolean || 2 | `true` (Boolean) |

### Object: `SerratedClaws`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_SERRATED_NAME"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_SERRATED_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_SERRATED_DESC"` (String) |

### Object: `SetAnimationAlts`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `dead` | Enum || 2 | `deadShot` (Enum) |
| `dying` | Enum || 2 | `shot` (Enum) |

### Object: `SetCrazyEyeBackgroundWeights`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `weights` | Array / Enum ||| `[0 0 1]` (Array), `[0 1 0]` (Array) |

### Object: `Shatter`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| `template` | Enum ||| `melee_attack` (Enum) |

### Object: `ShortCircuit`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| `name` | Enum ||| `"KEYWORD_SHORTCIRCUIT_NAME"` (String) |
| [`target`](Abilities_and_Spells.md#object-target) | Object ||| `{ ... }` (Object) |
| `template` | Enum ||| `spell` (Enum) |
| `tooltip` | Enum ||| `"KEYWORD_SHORTCIRCUIT_DESC"` (String) |

### Object: `SmartMetronome`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `stacks` | Enum / Integer || 2 | `20` (Number) |
| `upgraded` | Boolean || 2 | `true` (Boolean) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| `tags` | Array / Enum ||| `[musical]` (Array) |
| `template` | Enum ||| `self_buff` (Enum) |

### Object: `SmellBlood`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| `template` | Enum ||| `self_buff` (Enum) |

### Object: `Snow`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `adventure_weather` | Enum || 1 | `Snow` (Enum) |
| `ambient_sound` | String || 1 | `amb_snow.ogg` (String) |
| `prewarm` | Number || 1 | `20` (Number) |
| `skybox_frame` | Enum || 1 | `day_snow` (Enum) |
| `alpha` | String ||| `.5` (String) |
| `combo` | Array ||| `[SnowB SnowM SnowF]` (Array) |
| `desc` | Enum ||| `"WEATHER_SNOW_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object ||| `{ ... }` (Object) |
| `emit_amount` | Number ||| `1` (Number) |
| `emit_box` | Array ||| `[0 10 10 10 0 10]` (Array) |
| `emit_direction` | Array ||| `[0 -1 0]` (Array) |
| `emit_rate` | Number ||| `200` (Number) |
| `emit_spread` | Number ||| `10` (Number) |
| `hint_persistent_elements` | Array ||| `[Ice]` (Array) |
| `live_bounds` | Array ||| `[-0.5 999 -999 999 -0.5 999]` (Array) |
| `movieclip` | Array / Enum ||| `ParticleTestNoRandom` (Enum) |
| `name` | Enum ||| `"WEATHER_SNOW_NAME"` (String) |
| `particle_lifetime` | Number ||| `7` (Number) |
| `particles` | Array ||| `[Snow]` (Array) |
| `projection_matrix` | Enum ||| `default` (Enum) |
| `render_mode` | Enum ||| `separate` (Enum) |
| `rotation` | Array ||| `[0 360]` (Array) |
| `rotation_speed` | Array ||| `[-100 100]` (Array) |
| `rotation_speed_end` | Number ||| `0` (Number) |
| [`scripts`](Miscellaneous.md#object-scripts) | Object ||| `{ ... }` (Object) |
| `simulation_space` | Enum ||| `global` (Enum) |
| `size_end` | Number ||| `0` (Number) |
| `size_start` | Array ||| `[.3 .8]` (Array) |
| `speed_start` | Array ||| `[2 4]` (Array) |

### Object: `SolarFlare`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Equation || 1 | `5` (Equation) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object || 1 | `{ ... }` (Object) |
| `desc` | Enum ||| `"WEATHER_SOLARFLARE_DESC"` (String) |
| `elements` | Array ||| `[Fire]` (Array) |
| `name` | Enum ||| `"WEATHER_SOLARFLARE_NAME"` (String) |

### Object: `SpawnTilePuddleOnBattleStart`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `max_radius` | Number || 1 | `3.5` (Number) |
| `min_radius` | Number || 1 | `1.5` (Number) |
| `tile` | Array / Enum || 1 | `OilTile` (Enum) |

### Object: `SpawnVolcanoOnBattleStart`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `object` | Array / Enum || 3 | `Sprout` (Enum), `MiniVolcano` (Enum) |
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
| `name` | Enum ||| `"SpellShield"` (Enum) |
| `tooltip` | Enum ||| `None` (Enum) |

### Object: `StatBounty`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_STATBOUNTY_NAME"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_STATBOUNTY_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_STATBOUNTY_DESC"` (String) |

### Object: `StatusCharactersOnRoundEnd`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object || 1 | `{ ... }` (Object) |
| `FloatingRockTrap` | Integer || 1 | `1` (Number) |
| `Thorns` | Integer || 1 | `[1 .5]` (Array), `4` (Number), `3` (Number), `{ ... }` (Object) |
| `tag_filter` | Enum || 1 | `rock` (Enum) |

### Object: `StatusCharactersOnRoundStart`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`Conditional_GoodRoll`](Abilities_and_Spells.md#object-conditional_goodroll) | Object || 1 | `{ ... }` (Object) |
| [`Else`](Abilities_and_Spells.md#object-else) | Object || 1 | `{ ... }` (Object) |
| [`Madness`](Abilities_and_Spells.md#object-madness) | Array / Enum / Integer / Object ||| `[1 .1]` (Array), `[1 .25]` (Array), `999` (Number), `3` (Number), `{ ... }` (Object) |

### Object: `SwapWeapon`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `pool` | Array / Enum ||| `[TerminatorShotgun TerminatorSniper TerminatorUzi]` (Array) |

### Object: `SwitchMusic`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `new_layer` | Enum || 14 | `battle` (Enum), `map` (Enum) |
| `new_song` | Enum || 12 | `same` (Enum) |
| `crossfade_speed` | Integer || 2 | `1` (Number) |

### Object: `Switcheroo`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| `name` | Enum ||| `"Switcheroo"` (Enum) |
| `template` | Enum ||| `self_buff` (Enum) |
| `tooltip` | Enum ||| `None` (Enum) |

### Object: `Taunting`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"Taunting"` (Enum) |
| `tooltip` | Enum ||| `None` (Enum) |

### Object: `TeamCastAbility`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 4 | `CollectiveSpinImpl` (Enum), `CollectiveCounterImpl` (Enum) |
| `tag_restriction` | Enum || 4 | `collective` (Enum) |
| `same_orientation` | Boolean || 2 | `true` (Boolean) |

### Object: `TempBackstab`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_TEMPBACKSTAB_NAME"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_TEMPBACKSTAB_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_TEMPBACKSTAB_DESC"` (String) |

### Object: `TempBonusKnockback`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_BONUSKNOCKBACK_NAME"` (String) |
| `tooltip_stackless` | Enum ||| `None` (Enum) |
| `tooltip_stacks` | String ||| `"KEYWORD_BONUSKNOCKBACK_DESC"` (String) |

### Object: `TempBonusKnockbackDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_BONUSKNOCKBACKDAMAGE_NAME"` (String) |
| `tooltip_stackless` | Enum ||| `None` (Enum) |
| `tooltip_stacks` | String ||| `"KEYWORD_BONUSKNOCKBACKDAMAGE_DESC"` (String) |

### Object: `TempCritChanceUp`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alias` | Enum ||| `CritChanceUp` (Enum) |

### Object: `TempInjuryImmunity`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_TEMPIMMUNE_NAME"` (String) |
| `tooltip_stackless` | Enum ||| `none` (Enum) |
| `tooltip_stacks` | String ||| `"KEYWORD_TEMPIMMUNE_DESC"` (String) |
| `tooltip_stacks_singular` | String ||| `"KEYWORD_TEMPIMMUNE_DESC_SINGULAR"` (String) |

### Object: `TempManaCostReduction`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_TEMPMANAREDUCTION_NAME"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_TEMPMANAREDUCTION_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_TEMPMANAREDUCTION_DESC"` (String) |

### Object: `TempPreEmptiveCounterAttack`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_PRECOUNTER_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_PRECOUNTER_DESC"` (String) |

### Object: `TemporaryItem`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `icon_frame` | Number ||| `164` (Number) |
| `name` | Enum ||| `"KEYWORD_TEMPITEM_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_TEMPITEM_DESC"` (String) |

### Object: `TilesMovedToCritChance`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"TilesMovedToCritChance"` (Enum) |
| `tooltip` | Enum ||| `None` (Enum) |

### Object: `TilesMovedToMana`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"TilesMovedToMana"` (Enum) |
| `tooltip` | Enum ||| `None` (Enum) |

### Object: `TilesMovedToNeighborHeal`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"TilesMovedToNeighborHeal"` (Enum) |
| `tooltip` | Enum ||| `None` (Enum) |

### Object: `TilesMovedToStrength`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"TilesMovedToStrength"` (Enum) |
| `tooltip` | Enum ||| `None` (Enum) |

### Object: `TimeDelayStatusApplication`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `delay` | Number || 8 | `1.13333` (Number), `3` (Number), `.1` (String), `.25` (String) |
| [`SwitchMusic`](Abilities_and_Spells.md#object-switchmusic) | Object || 4 | `{ ... }` (Object) |
| [`Cleanse`](#object-cleanse) | Integer / Object || 2 | `1` (Number), `0` (Number), `{ ... }` (Object) |
| [`CreateGlobalModifiers`](Abilities_and_Spells.md#object-createglobalmodifiers) | Object || 2 | `{ ... }` (Object) |
| [`DoScreenShake`](Abilities_and_Spells.md#object-doscreenshake) | Integer / Object || 2 | `1` (Number), `{ ... }` (Object) |
| [`FormChange`](Abilities_and_Spells.md#object-formchange) | Enum / Object || 2 | `passive` (Enum), `Boris` (Enum), `{ ... }` (Object) |
| `FullHeal` | Integer || 2 | `1` (Number), `0` (Number) |
| `GlobalSpawnCharacter` | Enum || 2 | `MegaGuppy` (Enum) |
| `PlayBackground` | Integer || 2 | `1` (Number), `0` (Number) |
| `RemoveAmbientLightEffects` | Number || 2 | `4` (Number), `.5` (String) |
| `Vaporize` | Integer || 2 | `1` (Number), `20` (Number) |

### Object: `TowerDefenseStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_SENTRY_NAME"` (String) |
| `tooltip` | Enum ||| `"KEYWORD_SENTRY_DESC"` (String) |

### Object: `TowerDefenseStatus2`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `name` | Enum ||| `"KEYWORD_SENTRYPLUS_NAME"` (String) |
| `tooltip_stackless` | String ||| `"KEYWORD_SENTRYPLUS_DESC_STACKLESS"` (String) |
| `tooltip_stacks` | String ||| `"KEYWORD_SENTRYPLUS_DESC"` (String) |

### Object: `TradeLife`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bonus_passives`](Abilities_and_Spells.md#object-bonus_passives) | Object ||| `{ ... }` (Object) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object ||| `{ ... }` (Object) |
| `template` | Enum ||| `spell` (Enum) |

### Object: `TrailBlazer`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object ||| `{ ... }` (Object) |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object ||| `{ ... }` (Object) |
| `name` | Enum ||| `"Trail Blazer"` (String) |
| `template` | Enum ||| `self_buff` (Enum) |
| `tooltip` | Enum ||| `None` (Enum) |

### Object: `TransformEquipment`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `from` | Enum || 2 | `JarOfChaos` (Enum) |
| `to` | Enum || 2 | `JarOfNothing` (Enum) |

### Object: `TwisterDisplaceWithDamage`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `damage` | Equation || 12 | `inherit` (Equation), `1` (Equation) |
| `max_dist` | Integer || 12 | `3` (Number), `20` (Number) |
| `min_dist` | Integer || 4 | `3` (Number), `2` (Number) |
| `exclude_prefix` | Enum || 2 | `Twister` (Enum) |

### Object: `UseMoveAbilityWithAI`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | Enum || 2 | `LEPortFar` (Enum) |
| `move_weights` | Enum || 2 | `stay_far_move_far` (Enum) |

### Object: `VisualCountDownThenApplyStatus`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`ForceUseAbility`](Characters_and_Bosses.md#object-forceuseability) | Enum / Object || 2 | `neck_ChefsApron` (Enum), `head_HitlersToupe` (Enum), `{ ... }` (Object) |

### Object: `VisualFlySwarm`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ambient_sound` | String ||| `amb_flyswarm.ogg` (String) |
| `desc` | Enum ||| `"WEATHER_TORFLIES_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object ||| `{ ... }` (Object) |
| `name` | Enum ||| `"WEATHER_TORFLIES_NAME"` (String) |

### Object: `WaggleClone`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cWaggle`](Abilities_and_Spells.md#object-cwaggle) | Boolean (Flag) / Object || 2 | `(Flag)` (Boolean (Flag)), `{ ... }` (Object) |
| [`cWaggle2x2`](Abilities_and_Spells.md#object-cwaggle2x2) | Boolean (Flag) / Object || 2 | `(Flag)` (Boolean (Flag)), `{ ... }` (Object) |
| `stacks` | Enum / Integer || 2 | `5` (Number) |
| [`cWaggle3x3`](Abilities_and_Spells.md#object-cwaggle3x3) | Boolean (Flag) / Object ||| `(Flag)` (Boolean (Flag)), `{ ... }` (Object) |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object ||| `{ ... }` (Object) |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object ||| `{ ... }` (Object) |
| [`target`](Abilities_and_Spells.md#object-target) | Object ||| `{ ... }` (Object) |
| `template` | Enum ||| `lobbed_attack` (Enum) |

### Object: `Windy`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `adventure_weather` | Enum || 1 | `Windy` (Enum) |
| `ambient_sound` | String || 1 | `amb_windy.ogg` (String) |
| `prewarm` | Number || 1 | `5` (Number) |
| `skybox_frame` | Enum || 1 | `day_windy` (Enum) |
| `desc` | Enum ||| `"WEATHER_WINDY_DESC"` (String) |
| [`effects`](Abilities_and_Spells.md#object-effects) | Object ||| `{ ... }` (Object) |
| `hint_persistent_elements` | Array ||| `[Wind]` (Array) |
| `name` | Enum ||| `"WEATHER_WINDY_NAME"` (String) |
| `particles` | Array ||| `[WindFull]` (Array) |

### Object: `XIsTargetHealth`

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BonusDamage` | Enum / Integer || 4 | `"ceil(X/2)"` (Enum), `str` (Enum), `-4` (Number), `-3` (Number), `"max(0, floor(X/2)-1)"` (String), `"max(0, floor(X/6)-1)"` (String) |



---

## Auto-Discovered Objects


### Object: `AbsorbBuff`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_end` | Number | Undocumented. | 1 | `2` |
| `alpha_start` | Number | Undocumented. | 1 | `-1` |
| `emit_amount` | Number | Undocumented. | 1 | `1` |
| `emit_box` | Array | Undocumented. | 1 | `0 0 0 1 0 0` |
| `emit_direction` | Array | Undocumented. | 1 | `0 1 0` |
| `emit_rate` | Number | Undocumented. | 1 | `4` |
| `emit_spread` | Number | Undocumented. | 1 | `180` |
| `face_moving_direction` | Boolean | Undocumented. | 1 | `true` |
| `live_bounds` | Array | Undocumented. | 1 | `-999 999 -999 999 -999 999` |
| `movieclip` | String | Undocumented. | 1 | `ManaParticle` |
| `ownership` | String | Undocumented. | 1 | `local` |
| `particle_lifetime` | Array | Undocumented. | 1 | `.5 1.5` |
| `projection_matrix` | String | Undocumented. | 1 | `default` |
| `render_mode` | String | Undocumented. | 1 | `separate` |
| [`scripts`](Miscellaneous.md#object-scripts) | Object | Undocumented. | 1 ||
| `simulation_space` | String | Undocumented. | 1 | `global` |
| `size_end` | Number | Undocumented. | 1 | `.5` |
| `size_start` | Array | Undocumented. | 1 | `2 3` |
| `speed_scale` | Number | Undocumented. | 1 | `0` |
| `speed_start` | Number | Undocumented. | 1 | `1` |

</details>

### Object: `BBTransformMutant`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `self_buff` |

</details>

### Object: `BBTransformZealot`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `self_buff` |

</details>

### Object: `BasicButcherMelee`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `melee_attack` |

</details>

### Object: `BasicDruidAbility`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| `tags` | Array | Undocumented. | 1 | `musical` |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `spell` |

</details>

### Object: `BasicMagicMissile`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `spell` |

</details>

### Object: `BasicMagicShortRanged`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `ranged_attack` |

</details>

### Object: `BasicMedicMelee`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `melee_attack` |

</details>

### Object: `BasicMelee`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `melee_attack` |

</details>

### Object: `BasicMelee_4Hits`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `BasicMelee` |

</details>

### Object: `BasicMonkMelee`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `melee_attack` |

</details>

### Object: `BasicNecroRanged`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `lobbed_attack` |

</details>

### Object: `BasicPsychicPull`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `spell` |

</details>

### Object: `BasicRanged`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `lobbed_attack` |

</details>

### Object: `BasicStraightShot`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `straightshot_attack` |

</details>

### Object: `BasicSuplex`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Undocumented. | 1 | `SuplexAbility` |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| `tags` | Array | Undocumented. | 1 | `cant_be_simulcast` |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `melee_attack` |

</details>

### Object: `BasicTankMelee`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `dash_attack` |

</details>

### Object: `BeefyCharmedLeech`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `Maggot` |

</details>

### Object: `Bionic`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Undocumented. | 1 | `"SETBONUS_BIONIC_DESC"` |
| `name` | String | Undocumented. | 1 | `"SETBONUS_BIONIC_NAME"` |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| `pieces_required` | Number | Undocumented. | 1 | `3` |

</details>

### Object: `BloatEyeMovement2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `move` |

</details>

### Object: `BloatyExplodey`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `spell` |

</details>

### Object: `BoneWormShotMed`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `lobbed_attack` |

</details>

### Object: `BonusToss`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `throw_attack` |

</details>

### Object: `BonusToss2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `BonusToss` |

</details>

### Object: `BoomerCatExplode`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `spell` |

</details>

### Object: `BoyDino`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

</details>

### Object: `BoyDinoCry`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `self_buff` |

</details>

### Object: `BrambleRandomTileEvent`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `spell` |

</details>

### Object: `BungaSwipe`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai_ability` | String | Undocumented. | 1 | `BungaSwipe_ai` |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `melee_attack` |

</details>

### Object: `CatGoop`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `straightshot_attack` |

</details>

### Object: `CatapultJump`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `BasicJump` |

</details>

### Object: `CatapultJump2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `CatapultJump` |

</details>

### Object: `CaveCatDad`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Undocumented. | 1 ||
| [`equipment`](Characters_and_Bosses.md#object-equipment) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

</details>

### Object: `CerberubsStraightReaction`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `straightshot_attack` |

</details>

### Object: `CharmedDemonKitten`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `Hyde` |

</details>

### Object: `CharmedFly`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `Fly` |

</details>

### Object: `CharmedFlySwarm`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `FlySwarm` |

</details>

### Object: `CharmedLeech`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `Maggot` |

</details>

### Object: `CharmedPooter`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `Pooter` |

</details>

### Object: `CharmedReaper`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `Reaper` |

</details>

### Object: `CharmedTinySpider`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 2 ||
| `variant_of` | String | Undocumented. | 2 | `TinySpider` |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||

</details>

### Object: `CharmedTinyTumor`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `TinyTumor` |

</details>

### Object: `Chubs`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

</details>

### Object: `ChubsGoop`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `straightshot_attack` |

</details>

### Object: `ChubsRage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `self_buff` |

</details>

### Object: `CookedChickenLeg`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `CookedBigFood` |

</details>

### Object: `CraterCreeperOut`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

</details>

### Object: `DarkOneStrike`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `spell` |

</details>

### Object: `DecoyExplode`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `spell` |

</details>

### Object: `DefaultMove`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `move` |

</details>

### Object: `DestroyerShieldBash`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `BasicBigMelee` |

</details>

### Object: `Digest`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Undocumented. | 1 | `DamageConsumedCharactersAbilit` |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `self_buff` |

</details>

### Object: `DrMangler`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

</details>

### Object: `EatShit`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `tile_targeted_melee_attack` |

</details>

### Object: `FireExtinguish_Steam`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha` | Number | Undocumented. | 1 | `.1` |
| `emit_amount` | Number | Undocumented. | 1 | `200` |
| `emit_box` | Array | Undocumented. | 1 | `-.1 .1 .2 .2 -.1 .1` |
| `emit_direction` | Array | Undocumented. | 1 | `0 1 0` |
| `emit_radius` | Number | Undocumented. | 1 | `.4` |
| `emit_rate` | Number | Undocumented. | 1 | `1` |
| `emit_timespread` | Number | Undocumented. | 1 | `.75` |
| `emit_timespread_curve` | String | Undocumented. | 1 | `ease_out` |
| `live_bounds` | Array | Undocumented. | 1 | `-999 999 -999 999 -999 999` |
| `movieclip` | String | Undocumented. | 1 | `ParticleDustCloud` |
| `particle_lifetime` | Number | Undocumented. | 1 | `1` |
| `projection_matrix` | String | Undocumented. | 1 | `default` |
| `render_mode` | String | Undocumented. | 1 | `separate` |
| [`scripts`](Miscellaneous.md#object-scripts) | Object | Undocumented. | 1 ||
| `simulation_space` | String | Undocumented. | 1 | `global` |
| `size` | Array | Undocumented. | 1 | `.5 2` |
| `speed` | Array | Undocumented. | 1 | `1 3` |

</details>

### Object: `FlyBuff`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_end` | Number | Undocumented. | 1 | `2` |
| `alpha_start` | Number | Undocumented. | 1 | `-1` |
| `emit_amount` | Number | Undocumented. | 1 | `1` |
| `emit_box` | Array | Undocumented. | 1 | `0 0 0 1 0 0` |
| `emit_direction` | Array | Undocumented. | 1 | `0 1 0` |
| `emit_rate` | Number | Undocumented. | 1 | `50` |
| `emit_spread` | Number | Undocumented. | 1 | `180` |
| `face_moving_direction` | Boolean | Undocumented. | 1 | `true` |
| `live_bounds` | Array | Undocumented. | 1 | `-999 999 -999 999 -999 999` |
| `movieclip` | String | Undocumented. | 1 | `Critter_Fly` |
| `ownership` | String | Undocumented. | 1 | `local` |
| `particle_lifetime` | Array | Undocumented. | 1 | `.5 1.5` |
| `projection_matrix` | String | Undocumented. | 1 | `default` |
| `render_mode` | String | Undocumented. | 1 | `separate` |
| [`scripts`](Miscellaneous.md#object-scripts) | Object | Undocumented. | 1 ||
| `simulation_space` | String | Undocumented. | 1 | `global` |
| `size_end` | Number | Undocumented. | 1 | `0` |
| `size_start` | Array | Undocumented. | 1 | `3 4` |
| `speed_scale` | Number | Undocumented. | 1 | `.25` |
| `speed_start` | Number | Undocumented. | 1 | `1` |

</details>

### Object: `GirlDino`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

</details>

### Object: `GirlDinoCry`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `self_buff` |

</details>

### Object: `GrenadeExplode`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `spell` |

</details>

### Object: `Guillotina2Body`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

</details>

### Object: `Guillotina2Head`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

</details>

### Object: `Guillotina3Body`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

</details>

### Object: `Guillotina3Head`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

</details>

### Object: `HCHumanDie`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `self_buff` |

</details>

### Object: `Haunt`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `spell` |

</details>

### Object: `HemBounce`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `melee_attack` |

</details>

### Object: `Hyde`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Undocumented. | 1 ||
| `arm1` | Number | Undocumented. | 1 | `1013` |
| `arm2` | Number | Undocumented. | 1 | `1013` |
| `body` | Number | Undocumented. | 1 | `31` |
| `claws` | Number | Undocumented. | 1 | `1` |
| `default_face` | String | Undocumented. | 1 | `angry` |
| `default_frame` | Number | Undocumented. | 1 | `1` |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| `head` | Number | Undocumented. | 1 | `62` |
| `leftear` | Number | Undocumented. | 1 | `1013` |
| `lefteye` | Number | Undocumented. | 1 | `1013` |
| `lefteyebrow` | Number | Undocumented. | 1 | `63` |
| `leg1` | Number | Undocumented. | 1 | `37` |
| `leg2` | Number | Undocumented. | 1 | `37` |
| `mouth` | Number | Undocumented. | 1 | `1013` |
| `palette` | Number | Undocumented. | 1 | `59` |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| `pitch` | Number | Undocumented. | 1 | `.9` |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| `rightear` | Number | Undocumented. | 1 | `1013` |
| `righteye` | Number | Undocumented. | 1 | `1013` |
| `righteyebrow` | Number | Undocumented. | 1 | `63` |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||
| `tail` | Number | Undocumented. | 1 | `1004` |
| `texture` | Number | Undocumented. | 1 | `1000` |
| `voice` | String | Undocumented. | 1 | `male9` |

</details>

### Object: `IDSprout`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`spawn`](Abilities_and_Spells.md#object-spawn) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `spawn` |

</details>

### Object: `Lava_Distortion`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha` | Number | Undocumented. | 1 | `.01` |
| `alpha_end` | Number | Undocumented. | 1 | `0` |
| `emit_amount` | Number | Undocumented. | 1 | `1` |
| `emit_box` | Array | Undocumented. | 1 | `-.4 .4 0 0 -.4 .4` |
| `emit_direction` | Array | Undocumented. | 1 | `0 1 0` |
| `emit_rate` | Number | Undocumented. | 1 | `10` |
| `emit_spread` | Number | Undocumented. | 1 | `4` |
| `live_bounds` | Array | Undocumented. | 1 | `-999 999 0 999 -999 999` |
| `material` | String | Undocumented. | 1 | `distorter` |
| `movieclip` | String | Undocumented. | 1 | `Particle_HeatWaveDistortion` |
| `particle_lifetime` | Array | Undocumented. | 1 | `.5 1` |
| `projection_matrix` | String | Undocumented. | 1 | `default` |
| `render_layer` | String | Undocumented. | 1 | `sorted_distortions` |
| `render_mode` | String | Undocumented. | 1 | `separate` |
| `rotation` | Array | Undocumented. | 1 | `0 0` |
| `rotation_speed_end` | Number | Undocumented. | 1 | `0` |
| [`scripts`](Miscellaneous.md#object-scripts) | Object | Undocumented. | 1 ||
| `simulation_space` | String | Undocumented. | 1 | `global` |
| `size_end` | Number | Undocumented. | 1 | `3` |
| `size_start` | Number | Undocumented. | 1 | `1` |
| `speed_start` | Array | Undocumented. | 1 | `1 2` |

</details>

### Object: `LennyCatDies`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `class` | String | Undocumented. | 1 | `DamageConsumedCharactersAbilit` |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `self_buff` |

</details>

### Object: `Maggot`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

</details>

### Object: `ManglerEnrage`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `self_buff` |

</details>

### Object: `ManglerMonsterDashAttack`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `dash_attack` |

</details>

### Object: `ManglersMonster`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

</details>

### Object: `MechExplode`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `throw_attack` |

</details>

### Object: `MegaFart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `spell` |

</details>

### Object: `MegaGuppy_SummonTheChild`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`spawn`](Abilities_and_Spells.md#object-spawn) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `spawn` |

</details>

### Object: `MockingbirdForm`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| `tags` | Array | Undocumented. | 1 | `shapeshift` |
| `template` | String | Undocumented. | 1 | `self_buff` |

</details>

### Object: `MoonHead_KillHands`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `targeted_status` |

</details>

### Object: `MoveOne`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `move` |

</details>

### Object: `Necro_SoulDagger_Uncharged`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Undocumented. | 1 | `wp_NecroSoulDagger` |
| `desc` | String | Undocumented. | 1 | `"ITEM_SOULDAGGER_DESC"` |
| `frame` | Number | Undocumented. | 1 | `118` |
| `kind` | String | Undocumented. | 1 | `weapon` |
| `name` | String | Undocumented. | 1 | `"ITEM_SOULDAGGER_NAME"` |

</details>

### Object: `NoHead`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Undocumented. | 1 ||
| `claws` | Number | Undocumented. | 1 | `1` |
| `default_frame` | Number | Undocumented. | 1 | `1000` |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| `head` | Number | Undocumented. | 1 | `1036` |
| `leftear` | Number | Undocumented. | 1 | `1005` |
| `lefteye` | Number | Undocumented. | 1 | `1028` |
| `lefteyebrow` | Number | Undocumented. | 1 | `1022` |
| `mouth` | Number | Undocumented. | 1 | `1042` |
| `palette` | Number | Undocumented. | 1 | `9` |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| `pitch` | Number | Undocumented. | 1 | `.5` |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| `rightear` | Number | Undocumented. | 1 | `1005` |
| `righteye` | Number | Undocumented. | 1 | `1028` |
| `righteyebrow` | Number | Undocumented. | 1 | `1022` |
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||
| `texture` | Number | Undocumented. | 1 | `1000` |
| `voice` | String | Undocumented. | 1 | `male1` |

</details>

### Object: `NonChampionFlySwarm`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `FlySwarm` |

</details>

### Object: `NubbyToss`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `throw_attack` |

</details>

### Object: `Nubs`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

</details>

### Object: `NubsGoop`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `lobbed_attack` |

</details>

### Object: `Ornstein`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

</details>

### Object: `Paper`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Undocumented. | 1 | `"SETBONUS_PAPER_DESC"` |
| `name` | String | Undocumented. | 1 | `"SETBONUS_PAPER_NAME"` |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| `pieces_required` | Number | Undocumented. | 1 | `3` |

</details>

### Object: `PassiveEnergized`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `emit_amount` | Number | Undocumented. | 1 | `1` |
| `emit_box` | Array | Undocumented. | 1 | `0 0 .3 .3 0 0` |
| `emit_direction` | Array | Undocumented. | 1 | `0 1 0` |
| `emit_radius` | Number | Undocumented. | 1 | `.4` |
| `emit_rate` | Number | Undocumented. | 1 | `15` |
| `emit_spread` | Number | Undocumented. | 1 | `45` |
| `friction` | Array | Undocumented. | 1 | `-.05 -.1 -.05` |
| `live_bounds` | Array | Undocumented. | 1 | `-999 999 -999 999 -999 999` |
| `movieclip` | String | Undocumented. | 1 | `Particle_Electric` |
| `particle_lifetime` | Number | Undocumented. | 1 | `.5` |
| `projection_matrix` | String | Undocumented. | 1 | `default` |
| `render_mode` | String | Undocumented. | 1 | `separate` |
| `rotation` | Array | Undocumented. | 1 | `-90 90` |
| `simulation_space` | String | Undocumented. | 1 | `global` |
| `size` | Array | Undocumented. | 1 | `.5 1` |
| `size_in` | Number | Undocumented. | 1 | `.1` |
| `speed_start` | Array | Undocumented. | 1 | `0 2` |
| `unlit` | Boolean | Undocumented. | 1 | `true` |

</details>

### Object: `PassiveTar`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_in` | Number | Undocumented. | 1 | `.2` |
| `alpha_out` | Number | Undocumented. | 1 | `.5` |
| `emit_amount` | Number | Undocumented. | 1 | `1` |
| `emit_box` | Array | Undocumented. | 1 | `0 0 .7 .7 0 0` |
| `emit_direction` | Array | Undocumented. | 1 | `0 1 0` |
| `emit_radius` | Number | Undocumented. | 1 | `.4` |
| `emit_rate` | Number | Undocumented. | 1 | `4` |
| `force_end` | Array | Undocumented. | 1 | `0 -1 0` |
| `force_start` | Array | Undocumented. | 1 | `0 0 0` |
| `live_bounds` | Array | Undocumented. | 1 | `-999 999 -999 999 -999 999` |
| `movieclip` | String | Undocumented. | 1 | `Particle_TarDrip` |
| `particle_lifetime` | Array | Undocumented. | 1 | `1 1.5` |
| `projection_matrix` | String | Undocumented. | 1 | `default` |
| `render_mode` | String | Undocumented. | 1 | `separate` |
| `rotation` | Number | Undocumented. | 1 | `-90` |
| `simulation_space` | String | Undocumented. | 1 | `global` |
| `size` | Number | Undocumented. | 1 | `.5` |
| `size_in` | Number | Undocumented. | 1 | `.1` |
| `speed_start` | Number | Undocumented. | 1 | `0` |
| `spurt` | String | Undocumented. | 1 | `PassiveTarSplat` |

</details>

### Object: `PlayerCat_ThiefShade2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `PlayerCat` |

</details>

### Object: `RatKing`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

</details>

### Object: `ReaperRevenge`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `teleport` |

</details>

### Object: `SandStormBuff`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_end` | Number | Undocumented. | 1 | `2` |
| `alpha_start` | Number | Undocumented. | 1 | `-1` |
| `emit_amount` | Number | Undocumented. | 1 | `1` |
| `emit_box` | Array | Undocumented. | 1 | `0 0 0 1 0 0` |
| `emit_direction` | Array | Undocumented. | 1 | `0 1 0` |
| `emit_rate` | Number | Undocumented. | 1 | `100` |
| `emit_spread` | Number | Undocumented. | 1 | `180` |
| `face_moving_direction` | Boolean | Undocumented. | 1 | `true` |
| `live_bounds` | Array | Undocumented. | 1 | `-999 999 -999 999 -999 999` |
| `movieclip` | String | Undocumented. | 1 | `SandStormParticle` |
| `ownership` | String | Undocumented. | 1 | `local` |
| `particle_lifetime` | Array | Undocumented. | 1 | `.1 1` |
| `projection_matrix` | String | Undocumented. | 1 | `default` |
| `render_mode` | String | Undocumented. | 1 | `separate` |
| [`scripts`](Miscellaneous.md#object-scripts) | Object | Undocumented. | 1 ||
| `simulation_space` | String | Undocumented. | 1 | `global` |
| `size_end` | Number | Undocumented. | 1 | `0` |
| `size_start` | Array | Undocumented. | 1 | `.4 .6` |
| `speed_scale` | Number | Undocumented. | 1 | `.25` |
| `speed_start` | Number | Undocumented. | 1 | `1` |

</details>

### Object: `Shadowstep`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `teleport` |

</details>

### Object: `ShineBuff`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_end` | Number | Undocumented. | 1 | `2` |
| `alpha_start` | Number | Undocumented. | 1 | `.5` |
| `emit_amount` | Number | Undocumented. | 1 | `1` |
| `emit_box` | Array | Undocumented. | 1 | `0 0 0 1 0 0` |
| `emit_direction` | Array | Undocumented. | 1 | `0 1 0` |
| `emit_rate` | Number | Undocumented. | 1 | `15` |
| `emit_spread` | Number | Undocumented. | 1 | `180` |
| `face_moving_direction` | Boolean | Undocumented. | 1 | `true` |
| `live_bounds` | Array | Undocumented. | 1 | `-999 999 -999 999 -999 999` |
| `movieclip` | String | Undocumented. | 1 | `SparkleParticle` |
| `ownership` | String | Undocumented. | 1 | `local` |
| `particle_lifetime` | Number | Undocumented. | 1 | `.5` |
| `projection_matrix` | String | Undocumented. | 1 | `default` |
| `render_mode` | String | Undocumented. | 1 | `separate` |
| [`scripts`](Miscellaneous.md#object-scripts) | Object | Undocumented. | 1 ||
| `simulation_space` | String | Undocumented. | 1 | `global` |
| `size_end` | Number | Undocumented. | 1 | `.7` |
| `size_start` | Number | Undocumented. | 1 | `.5` |
| `speed_scale` | Number | Undocumented. | 1 | `.50` |
| `speed_start` | Number | Undocumented. | 1 | `1` |

</details>

### Object: `Shove`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `melee_attack` |

</details>

### Object: `SleepDart`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Undocumented. | 1 | `wp_SleepDart` |
| `desc` | String | Undocumented. | 1 | `"ITEM_SLEEPDART_DESC"` |
| `durability` | Number | Undocumented. | 1 | `1` |
| `frame` | Number | Undocumented. | 1 | `151` |
| `kind` | String | Undocumented. | 1 | `weapon` |
| `name` | String | Undocumented. | 1 | `"ITEM_SLEEPDART_NAME"` |

</details>

### Object: `SleepDart2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ability` | String | Undocumented. | 1 | `wp_SleepDart` |
| `desc` | String | Undocumented. | 1 | `"ITEM_SLEEPDART_DESC"` |
| `durability` | Number | Undocumented. | 1 | `2` |
| `frame` | Number | Undocumented. | 1 | `151` |
| `kind` | String | Undocumented. | 1 | `weapon` |
| `name` | String | Undocumented. | 1 | `"ITEM_SLEEPDART_NAME"` |

</details>

### Object: `SmokeBuff`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_end` | Number | Undocumented. | 1 | `2` |
| `alpha_start` | Number | Undocumented. | 1 | `-1` |
| `emit_amount` | Number | Undocumented. | 1 | `1` |
| `emit_box` | Array | Undocumented. | 1 | `0 0 0 1 0 0` |
| `emit_direction` | Array | Undocumented. | 1 | `0 1 0` |
| `emit_rate` | Number | Undocumented. | 1 | `25` |
| `emit_spread` | Number | Undocumented. | 1 | `100` |
| `face_moving_direction` | Boolean | Undocumented. | 1 | `true` |
| `live_bounds` | Array | Undocumented. | 1 | `-999 999 -999 999 -999 999` |
| `movieclip` | String | Undocumented. | 1 | `ParticleSmoke1` |
| `ownership` | String | Undocumented. | 1 | `local` |
| `particle_lifetime` | Array | Undocumented. | 1 | `.5 1` |
| `projection_matrix` | String | Undocumented. | 1 | `default` |
| `render_mode` | String | Undocumented. | 1 | `separate` |
| [`scripts`](Miscellaneous.md#object-scripts) | Object | Undocumented. | 1 ||
| `simulation_space` | String | Undocumented. | 1 | `global` |
| `size_end` | Number | Undocumented. | 1 | `0` |
| `size_start` | Array | Undocumented. | 1 | `1 1.4` |
| `speed_scale` | Number | Undocumented. | 1 | `.25` |
| `speed_start` | Number | Undocumented. | 1 | `.001` |

</details>

### Object: `Smough`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

</details>

### Object: `SparkleBuff`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_end` | Number | Undocumented. | 1 | `2` |
| `alpha_start` | Number | Undocumented. | 1 | `-1` |
| `emit_amount` | Number | Undocumented. | 1 | `1` |
| `emit_box` | Array | Undocumented. | 1 | `0 0 0 1 0 0` |
| `emit_direction` | Array | Undocumented. | 1 | `0 1 0` |
| `emit_rate` | Number | Undocumented. | 1 | `50` |
| `emit_spread` | Number | Undocumented. | 1 | `180` |
| `face_moving_direction` | Boolean | Undocumented. | 1 | `true` |
| `live_bounds` | Array | Undocumented. | 1 | `-999 999 -999 999 -999 999` |
| `movieclip` | String | Undocumented. | 1 | `SparkleParticle` |
| `ownership` | String | Undocumented. | 1 | `local` |
| `particle_lifetime` | Array | Undocumented. | 1 | `.1 1` |
| `projection_matrix` | String | Undocumented. | 1 | `default` |
| `render_mode` | String | Undocumented. | 1 | `separate` |
| [`scripts`](Miscellaneous.md#object-scripts) | Object | Undocumented. | 1 ||
| `simulation_space` | String | Undocumented. | 1 | `global` |
| `size_end` | Number | Undocumented. | 1 | `0` |
| `size_start` | Array | Undocumented. | 1 | `.4 .6` |
| `speed_scale` | Number | Undocumented. | 1 | `1` |
| `speed_start` | Number | Undocumented. | 1 | `.8` |

</details>

### Object: `SpiderReturn`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `return` |

</details>

### Object: `SpikeBuff`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `alpha_end` | Number | Undocumented. | 1 | `2` |
| `alpha_start` | Number | Undocumented. | 1 | `1` |
| `emit_amount` | Number | Undocumented. | 1 | `1` |
| `emit_box` | Array | Undocumented. | 1 | `0 0 0 1 0 0` |
| `emit_direction` | Array | Undocumented. | 1 | `0 1 0` |
| `emit_rate` | Number | Undocumented. | 1 | `4` |
| `emit_spread` | Number | Undocumented. | 1 | `180` |
| `face_moving_direction` | Boolean | Undocumented. | 1 | `true` |
| `live_bounds` | Array | Undocumented. | 1 | `-999 999 -999 999 -999 999` |
| `movieclip` | String | Undocumented. | 1 | `Particle_Thorns` |
| `ownership` | String | Undocumented. | 1 | `local` |
| `particle_lifetime` | Number | Undocumented. | 1 | `.5` |
| `projection_matrix` | String | Undocumented. | 1 | `default` |
| `render_mode` | String | Undocumented. | 1 | `separate` |
| [`scripts`](Miscellaneous.md#object-scripts) | Object | Undocumented. | 1 ||
| `simulation_space` | String | Undocumented. | 1 | `global` |
| `size_end` | Number | Undocumented. | 1 | `.5` |
| `size_start` | Number | Undocumented. | 1 | `.3` |
| `speed_scale` | Number | Undocumented. | 1 | `.25` |
| `speed_start` | Number | Undocumented. | 1 | `.5` |

</details>

### Object: `Spook`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `spell` |

</details>

### Object: `TC_DashReaction`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `ai_ability` | String | Undocumented. | 1 | `TC_DashReaction_AI` |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `trample_dash` |
| [`temporary_effects`](Abilities_and_Spells.md#object-temporary_effects) | Object | Undocumented. | 1 ||

</details>

### Object: `TT_Thrash`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `melee_attack` |

</details>

### Object: `TVOff`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `self_buff` |

</details>

### Object: `TattersFear`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `targeted_status` |

</details>

### Object: `TheCreator_SpawnCloneTeam`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`spawn`](Abilities_and_Spells.md#object-spawn) | Object | Undocumented. | 1 ||
| `tags` | Array | Undocumented. | 1 | `summon` |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `spawn` |

</details>

### Object: `ThornUp`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `self_buff` |

</details>

### Object: `ThornUpX`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `self_buff` |

</details>

### Object: `ThrobbingKing2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

</details>

### Object: `ToadJump_BasicMove`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `jump_attack` |

</details>

### Object: `TormentorRuneAbsorb`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `spell` |

</details>

### Object: `ToxPuff`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `self_buff` |

</details>

### Object: `ToxicBubbles`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `emit_amount` | Number | Undocumented. | 1 | `1` |
| `emit_box` | Array | Undocumented. | 1 | `-.4 .4 0 0 -.4 .4` |
| `emit_direction` | Array | Undocumented. | 1 | `0 0 0` |
| `emit_rate` | Array | Undocumented. | 1 | `.7 2` |
| `emit_spread` | Number | Undocumented. | 1 | `0` |
| `face_moving_direction` | Boolean | Undocumented. | 1 | `false` |
| `live_bounds` | Array | Undocumented. | 1 | `-999 999 0 999 -999 999` |
| `movieclip` | String | Undocumented. | 1 | `ToxicBubbleParticle` |
| `particle_lifetime` | Number | Undocumented. | 1 | `1.5` |
| `projection_matrix` | String | Undocumented. | 1 | `default` |
| `render_mode` | String | Undocumented. | 1 | `separate` |
| `simulation_space` | String | Undocumented. | 1 | `global` |
| `size_start` | Array | Undocumented. | 1 | `.5 1` |
| `speed_start` | Number | Undocumented. | 1 | `0` |

</details>

### Object: `TrexSwitchTarget`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `targeted_status` |

</details>

### Object: `UFO_BigExplode`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `spell` |

</details>

### Object: `UltraSmough`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`ai`](Characters_and_Bosses.md#object-ai) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||

</details>

### Object: `Wood`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `desc` | String | Undocumented. | 1 | `"SETBONUS_WOOD_DESC"` |
| `name` | String | Undocumented. | 1 | `"SETBONUS_WOOD_NAME"` |
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| `pieces_required` | Number | Undocumented. | 1 | `3` |

</details>

### Object: `cWaggle`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `Waggle` |

</details>

### Object: `cWaggle2x2`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`abilities`](Characters_and_Bosses.md#object-abilities) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`passives`](Cat_Mutations.md#object-passives) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `cWaggle` |

</details>

### Object: `cWaggle3x3`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`properties`](Characters_and_Bosses.md#object-properties) | Object | Undocumented. | 1 ||
| [`stats`](Characters_and_Bosses.md#object-stats) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `cWaggle2x2` |

</details>

### Object: `face_EatNeverstone`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bonus_passives`](Abilities_and_Spells.md#object-bonus_passives) | Object | Undocumented. | 1 ||
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `self_buff` |

</details>

### Object: `face_LeechBrood`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `lobbed_attack` |

</details>

### Object: `neck_NukeBonus`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bonus_passives`](Abilities_and_Spells.md#object-bonus_passives) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`meta`](Abilities_and_Spells.md#object-meta) | Object | Undocumented. | 1 ||
| `sub_ability` | String | Undocumented. | 1 | `neck_NukeExplode` |
| `template` | String | Undocumented. | 1 | `self_buff` |

</details>

### Object: `neck_NukeExplode`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`bonus_passives`](Abilities_and_Spells.md#object-bonus_passives) | Object | Undocumented. | 1 ||
| [`cost`](Abilities_and_Spells.md#object-cost) | Object | Undocumented. | 1 ||
| [`damage_instance`](Abilities_and_Spells.md#object-damage_instance) | Object | Undocumented. | 1 ||
| [`graphics`](Abilities_and_Spells.md#object-graphics) | Object | Undocumented. | 1 ||
| [`self_damage`](Abilities_and_Spells.md#object-self_damage) | Object | Undocumented. | 1 ||
| [`splash_damage`](Abilities_and_Spells.md#object-splash_damage) | Object | Undocumented. | 1 ||
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `template` | String | Undocumented. | 1 | `spell` |

</details>

### Object: `pyrophina`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BOSS_PYROPHINA_QUOTE_1` | String | Undocumented. | 1 ||
| `BOSS_PYROPHINA_QUOTE_2` | String | Undocumented. | 1 ||
| `act` | Number | Undocumented. | 1 | `2` |
| `arrival_unlock` | String | Undocumented. | 1 | `npc_houseboss_intro_pyrophina` |
| `frame_label` | String | Undocumented. | 1 | `pyrophina` |
| `index` | Number | Undocumented. | 1 | `1` |
| `initial_cooldown` | Array | Undocumented. | 1 | `0` |
| `initial_cutscene_day` | String | Undocumented. | 1 | `pyro_intro` |
| `lead_time` | Number | Undocumented. | 1 | `7` |
| `level` | String | Undocumented. | 1 | `"house_bosses/pyrophina.lvl"` |
| `music` | String | Undocumented. | 1 | `kaiju` |
| `name` | String | Undocumented. | 1 | `BOSS_PYROPHINA_NAME` |
| `quotes` | Array | Undocumented. | 1 ||
| `rematch_cooldown` | Array | Undocumented. | 1 | `3 7` |
| `rematch_cutscene_day` | String | Undocumented. | 1 | `house_boss_returns_pyro` |
| `savefile_string` | String | Undocumented. | 1 | `"SAVE_FILE_FIGHT_HOUSEBOSS_PYR` |

</details>

### Object: `set_WitchJump`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 1

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| [`target`](Abilities_and_Spells.md#object-target) | Object | Undocumented. | 1 ||
| `variant_of` | String | Undocumented. | 1 | `BasicJump` |

</details>

### Object: `zaratana`

<details>
<summary><b>Expand</b></summary>

**Total Count:** 2

| Key | Type | Definition | Count | Example Inputs |
| :--- | :--- | :--- | :--- | :--- |
| `BOSS_ZARATANA_QUOTE_1` | String | Undocumented. | 1 ||
| `BOSS_ZARATANA_QUOTE_2` | String | Undocumented. | 1 ||
| `act` | Number | Undocumented. | 1 | `2` |
| `arrival_unlock` | String | Undocumented. | 1 | `npc_houseboss_intro_zaratana` |
| `frame_label` | String | Undocumented. | 1 | `zaratana` |
| `index` | Number | Undocumented. | 1 | `2` |
| `initial_cooldown` | Array | Undocumented. | 1 | `0` |
| `initial_cutscene_day` | String | Undocumented. | 1 | `moonboss_intro` |
| `lead_time` | Number | Undocumented. | 1 | `7` |
| `level` | String | Undocumented. | 1 | `"house_bosses/zaratana.lvl"` |
| `music` | String | Undocumented. | 1 | `kaiju` |
| `name` | String | Undocumented. | 1 | `BOSS_ZARATANA_NAME` |
| `quotes` | Array | Undocumented. | 1 ||
| `rematch_cooldown` | Array | Undocumented. | 1 | `3 7` |
| `rematch_cutscene_day` | String | Undocumented. | 1 | `house_boss_returns_zara` |
| `savefile_string` | String | Undocumented. | 1 | `"SAVE_FILE_FIGHT_HOUSEBOSS_ZAR` |

</details>
