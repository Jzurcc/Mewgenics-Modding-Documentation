# Mewgenics Mod Developer Documentation: Engine: Statuses and Passives

## Engine: Statuses and Passives

This document lists every confirmed Status and Passive ID found across all game data files. These IDs are used as **dynamic keys** in any Status or Passive Container block (e.g. `statuses`, `passives`, `AddStatusToBasicAttack`, `bonus_passives`). The value paired with each key depends on the context: typically a stack count or duration for statuses, or a boolean/nested block for passives.

> **Note:** With over 1,200 unique IDs, this is the largest system in the game. Granting a character an ID (like `AddStatusToBasicAttack`) gives the character that reactive behaviour permanently.

> **Referenced by:** [`damage_instance` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-damage_instance), [`effects` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-effects), [`bonus_passives` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-bonus_passives), [`temporary_effects` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-temporary_effects), [`Else` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-else), [`ApplyToSource` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytosource), [`Conditional_HasTag` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_hastag), [`Conditional_Enemy` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_enemy), [`Conditional_Ally` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_ally), [`keyword_tooltips` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-keyword_tooltips), [`additional_passives` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-additional_passives), [`RandomStatusFromPool` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-randomstatusfrompool), [`Conditional_Boss` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_boss), [`ApplyToSourceOnKill` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytosourceonkill), [`CanApplyToInanimate` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-canapplytoinanimate), [`Conditional_NotBoss` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_notboss), [`Conditional_HasStatus` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_hasstatus), [`Conditional_GoodRoll` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_goodroll), [`Conditional_Speculative` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_speculative), [`ApplyPassives` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applypassives), [`Conditional_FormulaIsPositive` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_formulaispositive), [`ApplyStatusIfCrit` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applystatusifcrit), [`Conditional_Corpse` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_corpse), [`Conditional_InForm` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_inform), [`Conditional_HealthThreshold` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_healththreshold), [`Conditional_Object` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_object), [`Conditional_PlayerCat` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_playercat), [`CollectsPickupsWithAltEffects` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-collectspickupswithalteffects), [`Conditional_Familiar` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_familiar), [`LateStatusApplication` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-latestatusapplication), [`TakeBonusTurnWithStatus` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-takebonusturnwithstatus), [`TempPassiveWhileHasStatus` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-temppassivewhilehasstatus), [`TimeDelayStatusApplication` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-timedelaystatusapplication), [`post_spawn_statuses` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-post_spawn_statuses), [`ApplyMultipleTimes` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applymultipletimes), [`Conditional_AffectedByElement` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_affectedbyelement), [`Conditional_FirstApplicationThisTurn` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_firstapplicationthisturn), [`Conditional_LastHit` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_lasthit), [`StatusOnBattleEnd` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-statusonbattleend), [`extra_statuses` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-extra_statuses), [`AddStatusToBasicAttack` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-addstatustobasicattack), [`ApplyToRandomPartyMemberIfPossible` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytorandompartymemberifpossible), [`Conditional_BadRoll` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_badroll), [`Conditional_BossOrBig` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_bossorbig), [`Conditional_Buddy` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_buddy), [`Conditional_Displaceable` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_displaceable), [`Conditional_NotAlly` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_notally), [`Conditional_NotBossOrBig` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_notbossorbig), [`Conditional_NotShielded` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_notshielded), [`Conditional_OncePerBattle` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_onceperbattle), [`Conditional_Shielded` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_shielded), [`Math` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-math), [`MeleeRevengeDamage` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-meleerevengedamage), [`OverHealToStatuses` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-overhealtostatuses), [`XIsTargetHealth` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-xistargethealth), [`AlphaStatusOnTurnBegin` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-alphastatusonturnbegin), [`ApplyPassivesToSpawnerWhileAlive` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applypassivestospawnerwhilealive), [`ApplyStatusesNextTurnBegin` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applystatusesnextturnbegin), [`ApplyToOthersWithSharedTagAndFaction` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytootherswithsharedtagandfaction), [`Conditional_ActiveWeather_Any` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_activeweather_any), [`Conditional_Backstab` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_backstab), [`Conditional_CanBeHealed` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_canbehealed), [`Conditional_DebuffRoll` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_debuffroll), [`Conditional_HasCleansableDebuffs` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_hascleansabledebuffs), [`Conditional_LivingPlayerCat` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_livingplayercat), [`Conditional_RandomChance` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_randomchance), [`Conditional_SourceAbilityHasTag` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_sourceabilityhastag), [`Conditional_SourceHasStatus` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_sourcehasstatus), [`PassiveWhileNotTakingTurn` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-passivewhilenottakingturn), [`ReviveNextRound` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-revivenextround), [`StatusGroup` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-statusgroup), [`StatusKillers` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-statuskillers), [`VisualCountDownThenApplyStatus` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-visualcountdownthenapplystatus), [`innate_passives` (Cat_Classes)](./Cat_Classes.md#context-innate_passives), [`passives` (Cat_Mutations)](./Cat_Mutations.md#context-passives), [`AddStatusToBasicAttack` (Cat_Mutations)](./Cat_Mutations.md#context-addstatustobasicattack), [`effects` (Cat_Mutations)](./Cat_Mutations.md#context-effects), [`MeleeRevengeDamage` (Cat_Mutations)](./Cat_Mutations.md#context-meleerevengedamage), [`AddStatusToBasicMeleeAttack` (Cat_Mutations)](./Cat_Mutations.md#context-addstatustobasicmeleeattack), [`StatusOnTookDamage` (Cat_Mutations)](./Cat_Mutations.md#context-statusontookdamage), [`StatusEachTurnBegin` (Cat_Mutations)](./Cat_Mutations.md#context-statuseachturnbegin), [`RandomStatusFromPool` (Cat_Mutations)](./Cat_Mutations.md#context-randomstatusfrompool), [`StatusEachTurnEnd` (Cat_Mutations)](./Cat_Mutations.md#context-statuseachturnend), [`Conditional_RandomChance` (Cat_Mutations)](./Cat_Mutations.md#context-conditional_randomchance), [`StatusEveryXSpellCasts` (Cat_Mutations)](./Cat_Mutations.md#context-statuseveryxspellcasts), [`StatusKilledCharacters` (Cat_Mutations)](./Cat_Mutations.md#context-statuskilledcharacters), [`StatusOnBattleEnd` (Cat_Mutations)](./Cat_Mutations.md#context-statusonbattleend), [`StatusOnEndMove` (Cat_Mutations)](./Cat_Mutations.md#context-statusonendmove), [`StatusOnTookDamageFromAbility` (Cat_Mutations)](./Cat_Mutations.md#context-statusontookdamagefromability), [`Conditional_FirstApplicationThisTurn` (Cat_Mutations)](./Cat_Mutations.md#context-conditional_firstapplicationthisturn), [`Conditional_GoodRoll` (Cat_Mutations)](./Cat_Mutations.md#context-conditional_goodroll), [`PassiveWhenAtFullMana` (Cat_Mutations)](./Cat_Mutations.md#context-passivewhenatfullmana), [`StatusEachRoundEnd` (Cat_Mutations)](./Cat_Mutations.md#context-statuseachroundend), [`StatusEveryXSpellCastsEachTurn` (Cat_Mutations)](./Cat_Mutations.md#context-statuseveryxspellcastseachturn), [`StatusIfDidntMove` (Cat_Mutations)](./Cat_Mutations.md#context-statusifdidntmove), [`StatusIfUnusedMovePoints` (Cat_Mutations)](./Cat_Mutations.md#context-statusifunusedmovepoints), [`StatusOnAllyCatDeath` (Cat_Mutations)](./Cat_Mutations.md#context-statusonallycatdeath), [`StatusOnCastSpell` (Cat_Mutations)](./Cat_Mutations.md#context-statusoncastspell), [`StatusOnDie` (Cat_Mutations)](./Cat_Mutations.md#context-statusondie), [`StatusOnEatFood` (Cat_Mutations)](./Cat_Mutations.md#context-statusoneatfood), [`StatusOnKill` (Cat_Mutations)](./Cat_Mutations.md#context-statusonkill), [`passives` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-passives), [`AddStatusToBasicAttack` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-addstatustobasicattack), [`MeleeRevengeDamage` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-meleerevengedamage), [`ally_rewards` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-ally_rewards), [`effects` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-effects), [`PassiveGroup` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-passivegroup), [`StatusCollector` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statuscollector), [`statuses` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statuses), [`StatusEachTurnEnd` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statuseachturnend), [`StatusOnKill` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusonkill), [`StatusOnTookDamageFromAbility` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusontookdamagefromability), [`keyword_tooltips` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-keyword_tooltips), [`RandomPassivePool` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-randompassivepool), [`Conditional_GoodRoll` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_goodroll), [`Holy` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-holy), [`StatusGroup` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusgroup), [`StatusOnSpawnIn` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusonspawnin), [`StatusOnTookDamage` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusontookdamage), [`TempPassiveUntilSettled` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-temppassiveuntilsettled), [`alternate_energized_effect` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-alternate_energized_effect), [`passive` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-passive), [`statuses_on_enter_form` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statuses_on_enter_form), [`AddStatusToReceivedDamage` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-addstatustoreceiveddamage), [`AddStatusToSpells` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-addstatustospells), [`AddStatusToTrampleDamage` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-addstatustotrampledamage), [`AddStatusToWeapons` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-addstatustoweapons), [`AdventureTokenPassivePool` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-adventuretokenpassivepool), [`Conditional_BadRoll` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_badroll), [`Conditional_HasKnockback` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_hasknockback), [`Conditional_IsPhysicalAttack` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_isphysicalattack), [`Else` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-else), [`FinalBossHitCountdownBoris` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-finalbosshitcountdownboris), [`FinalBossHitCountdownExplosive` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-finalbosshitcountdownexplosive), [`Fire` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-fire), [`ModularPickup` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-modularpickup), [`PassiveWhenDead` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-passivewhendead), [`RandomStatusFromPool` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-randomstatusfrompool), [`StacyMutant_Brace` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_brace), [`StacyMutant_Counter` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_counter), [`StacyMutant_Damage` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_damage), [`StacyMutant_DoubleHead` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_doublehead), [`StacyMutant_Fire` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_fire), [`StacyMutant_Health` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_health), [`StacyMutant_Holy` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_holy), [`StacyMutant_Ice` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_ice), [`StacyMutant_Lightning` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_lightning), [`StacyMutant_Mirror` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_mirror), [`StacyMutant_Speed` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_speed), [`StacyMutant_Thorns` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_thorns), [`StatusAfterXTurns` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusafterxturns), [`StatusEachTurnBeginIfHasStatus` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statuseachturnbeginifhasstatus), [`StatusEachTurnEndForEachTurn` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statuseachturnendforeachturn), [`StatusEachTurnEndIfEnabledAtStartOfTurn` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statuseachturnendifenabledatstartofturn), [`StatusOnDie` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusondie), [`StatusOnEndMove` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusonendmove), [`StatusOnEnemyConfused` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusonenemyconfused), [`StatusOnGainCoins` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusongaincoins), [`StatusOverlappingCharactersAndDie` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusoverlappingcharactersanddie), [`StatusWhenStatusCompletelyRemoved` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statuswhenstatuscompletelyremoved), [`additional_statuses` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-additional_statuses), [`damage_instance` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-damage_instance), [`passives` (Elite_Buffs)](./Elite_Buffs.md#context-passives), [`StatusEachRoundBegin` (Elite_Buffs)](./Elite_Buffs.md#context-statuseachroundbegin), [`effects` (Elite_Buffs)](./Elite_Buffs.md#context-effects), [`MeleeRevengeDamage` (Elite_Buffs)](./Elite_Buffs.md#context-meleerevengedamage), [`StatusEachTurnEnd` (Elite_Buffs)](./Elite_Buffs.md#context-statuseachturnend), [`statuses` (Elite_Buffs)](./Elite_Buffs.md#context-statuses), [`AddStatusToBasicAttack` (Elite_Buffs)](./Elite_Buffs.md#context-addstatustobasicattack), [`StatusEachRoundEnd` (Elite_Buffs)](./Elite_Buffs.md#context-statuseachroundend), [`StatusOnDie` (Elite_Buffs)](./Elite_Buffs.md#context-statusondie), [`StatusOnEnemyCastSpell` (Elite_Buffs)](./Elite_Buffs.md#context-statusonenemycastspell), [`StatusOnKill` (Elite_Buffs)](./Elite_Buffs.md#context-statusonkill), [`self_status_next_fight` (Events_and_Encounters)](./Events_and_Encounters.md#context-self_status_next_fight), [`party_status_next_fight` (Events_and_Encounters)](./Events_and_Encounters.md#context-party_status_next_fight), [`global_effect_next_fight` (Events_and_Encounters)](./Events_and_Encounters.md#context-global_effect_next_fight), [`CharacterTypeGainsStatusAtBattleStart` (Events_and_Encounters)](./Events_and_Encounters.md#context-charactertypegainsstatusatbattlestart), [`StatusRandomEnemiesOnBattleStart` (Events_and_Encounters)](./Events_and_Encounters.md#context-statusrandomenemiesonbattlestart), [`effects` (House_and_Environment)](./House_and_Environment.md#context-effects), [`Else` (House_and_Environment)](./House_and_Environment.md#context-else), [`StatusCharactersOnRoundEnd` (House_and_Environment)](./House_and_Environment.md#context-statuscharactersonroundend), [`ApplyPassives` (House_and_Environment)](./House_and_Environment.md#context-applypassives), [`CharacterTypeGainsStatusAtBattleStart` (House_and_Environment)](./House_and_Environment.md#context-charactertypegainsstatusatbattlestart), [`Conditional_GoodRoll` (House_and_Environment)](./House_and_Environment.md#context-conditional_goodroll), [`RandomStatusFromPool` (House_and_Environment)](./House_and_Environment.md#context-randomstatusfrompool), [`StatusAllCharactersOnSpawn` (House_and_Environment)](./House_and_Environment.md#context-statusallcharactersonspawn), [`StatusCharactersOnRoundStart` (House_and_Environment)](./House_and_Environment.md#context-statuscharactersonroundstart), [`Conditional_Corpse` (House_and_Environment)](./House_and_Environment.md#context-conditional_corpse), [`Conditional_HasTag` (House_and_Environment)](./House_and_Environment.md#context-conditional_hastag), [`Conditional_PartyMember` (House_and_Environment)](./House_and_Environment.md#context-conditional_partymember), [`StatusOnBattleEnd` (House_and_Environment)](./House_and_Environment.md#context-statusonbattleend), [`extra_statuses` (House_and_Environment)](./House_and_Environment.md#context-extra_statuses), [`passives` (Items_and_Equipment)](./Items_and_Equipment.md#context-passives), [`AddStatusToBasicAttack` (Items_and_Equipment)](./Items_and_Equipment.md#context-addstatustobasicattack), [`effects` (Items_and_Equipment)](./Items_and_Equipment.md#context-effects), [`MeleeRevengeDamage` (Items_and_Equipment)](./Items_and_Equipment.md#context-meleerevengedamage), [`StatusOnBattleEnd` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonbattleend), [`StatusEachTurnEnd` (Items_and_Equipment)](./Items_and_Equipment.md#context-statuseachturnend), [`StatusOnBreak` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonbreak), [`Conditional_GoodRoll` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_goodroll), [`StatusOnKill` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonkill), [`StatusOnTookDamage` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusontookdamage), [`StatusOnBattleStart` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonbattlestart), [`StatusEachTurnBegin` (Items_and_Equipment)](./Items_and_Equipment.md#context-statuseachturnbegin), [`AddSelfStatusToBasicAttack` (Items_and_Equipment)](./Items_and_Equipment.md#context-addselfstatustobasicattack), [`AddStatusToAllDamage` (Items_and_Equipment)](./Items_and_Equipment.md#context-addstatustoalldamage), [`StatusAlliesOnBattleStart` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusalliesonbattlestart), [`StatusOnKillEnemy` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonkillenemy), [`AddPassivesToMinions` (Items_and_Equipment)](./Items_and_Equipment.md#context-addpassivestominions), [`ApplyToSource` (Items_and_Equipment)](./Items_and_Equipment.md#context-applytosource), [`StatusOnDie` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusondie), [`StatusOnEndMove` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonendmove), [`Conditional_HasStatus` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_hasstatus), [`Else` (Items_and_Equipment)](./Items_and_Equipment.md#context-else), [`StatusOnTakeHealthOrShieldDamage` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusontakehealthorshielddamage), [`StatusOnTurnEndIfDidntCastAbilityTypes` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonturnendifdidntcastabilitytypes), [`StatusRandomEnemiesOnBattleStart` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusrandomenemiesonbattlestart), [`CatchProjectiles` (Items_and_Equipment)](./Items_and_Equipment.md#context-catchprojectiles), [`Conditional_PartyMember` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_partymember), [`PassiveWhenDead` (Items_and_Equipment)](./Items_and_Equipment.md#context-passivewhendead), [`StatusAllCharactersOnSpawn` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusallcharactersonspawn), [`StatusEveryXSpellCasts` (Items_and_Equipment)](./Items_and_Equipment.md#context-statuseveryxspellcasts), [`StatusIfUnusedMovePoints` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusifunusedmovepoints), [`StatusOnPopCorpse` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonpopcorpse), [`AddStatusToElementDamage` (Items_and_Equipment)](./Items_and_Equipment.md#context-addstatustoelementdamage), [`AddStatusToKnockbackDamage` (Items_and_Equipment)](./Items_and_Equipment.md#context-addstatustoknockbackdamage), [`AddStatusToSpells` (Items_and_Equipment)](./Items_and_Equipment.md#context-addstatustospells), [`ApplyStatusesToRandomEnemiesEachTurn` (Items_and_Equipment)](./Items_and_Equipment.md#context-applystatusestorandomenemieseachturn), [`Conditional_Adjacent` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_adjacent), [`Conditional_BadRoll` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_badroll), [`Conditional_Boss` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_boss), [`Conditional_HasTag` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_hastag), [`Conditional_OncePerBattle` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_onceperbattle), [`PassiveIfWeaponIsUsable` (Items_and_Equipment)](./Items_and_Equipment.md#context-passiveifweaponisusable), [`StatusAfterCastSpell` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusaftercastspell), [`StatusAfterXStacks` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusafterxstacks), [`StatusIfUnusedActPoints` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusifunusedactpoints), [`StatusOnAllyCatDeath` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonallycatdeath), [`StatusOnBackstab` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonbackstab), [`StatusOnBreakItem` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonbreakitem), [`StatusOnCastSpell` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusoncastspell), [`StatusOnGainCoins` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusongaincoins), [`StatusOnSetPieceBreak` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonsetpiecebreak), [`bonus_passives` (Items_and_Equipment)](./Items_and_Equipment.md#context-bonus_passives), [`keyword_tooltips` (Items_and_Equipment)](./Items_and_Equipment.md#context-keyword_tooltips), [`passive` (Items_and_Equipment)](./Items_and_Equipment.md#context-passive), [`AddPassivesToCharmed` (Items_and_Equipment)](./Items_and_Equipment.md#context-addpassivestocharmed), [`AddSelfStatusToWeapons` (Items_and_Equipment)](./Items_and_Equipment.md#context-addselfstatustoweapons), [`AddStatusToBackstabs` (Items_and_Equipment)](./Items_and_Equipment.md#context-addstatustobackstabs), [`AddStatusToFirstSpellEachTurn` (Items_and_Equipment)](./Items_and_Equipment.md#context-addstatustofirstspelleachturn), [`AddStatusToWeapons` (Items_and_Equipment)](./Items_and_Equipment.md#context-addstatustoweapons), [`ApplyPassives` (Items_and_Equipment)](./Items_and_Equipment.md#context-applypassives), [`ApplyToRandomPartyMemberIfPossible` (Items_and_Equipment)](./Items_and_Equipment.md#context-applytorandompartymemberifpossible), [`Conditional_Ally` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_ally), [`Conditional_Corpse` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_corpse), [`Conditional_Enemy` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_enemy), [`Conditional_HasCleansableDebuffs` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_hascleansabledebuffs), [`Conditional_HealthThreshold` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_healththreshold), [`Conditional_ManaThreshold` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_manathreshold), [`Conditional_PlayerCat` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_playercat), [`Conditional_RandomChance` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_randomchance), [`Conditional_Shielded` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_shielded), [`ConvertDamageToScaledStatus` (Items_and_Equipment)](./Items_and_Equipment.md#context-convertdamagetoscaledstatus), [`CritsApplyStatus` (Items_and_Equipment)](./Items_and_Equipment.md#context-critsapplystatus), [`Eternal` (Items_and_Equipment)](./Items_and_Equipment.md#context-eternal), [`GlobalFlowerTrapperAura` (Items_and_Equipment)](./Items_and_Equipment.md#context-globalflowertrapperaura), [`PassiveWhileHasDurability` (Items_and_Equipment)](./Items_and_Equipment.md#context-passivewhilehasdurability), [`PassiveWhileInMonkMeleeStance` (Items_and_Equipment)](./Items_and_Equipment.md#context-passivewhileinmonkmeleestance), [`PassiveWhileShielded` (Items_and_Equipment)](./Items_and_Equipment.md#context-passivewhileshielded), [`RandomStatusFromPool` (Items_and_Equipment)](./Items_and_Equipment.md#context-randomstatusfrompool), [`ReviveNextRound` (Items_and_Equipment)](./Items_and_Equipment.md#context-revivenextround), [`ScaledStatusOnHolyShieldBlock` (Items_and_Equipment)](./Items_and_Equipment.md#context-scaledstatusonholyshieldblock), [`ScaledStatusOnSpendMana` (Items_and_Equipment)](./Items_and_Equipment.md#context-scaledstatusonspendmana), [`StatDependentPassive` (Items_and_Equipment)](./Items_and_Equipment.md#context-statdependentpassive), [`StatusAfterXTurns` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusafterxturns), [`StatusAlliesEachTurn` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusallieseachturn), [`StatusAlliesOnDeath` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusalliesondeath), [`StatusEachRoundEnd` (Items_and_Equipment)](./Items_and_Equipment.md#context-statuseachroundend), [`StatusEachTurnEndForEachTurn` (Items_and_Equipment)](./Items_and_Equipment.md#context-statuseachturnendforeachturn), [`StatusOnCollectPickup` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusoncollectpickup), [`StatusOnDodge` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusondodge), [`StatusOnEatFood` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusoneatfood), [`StatusOnEatPill` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusoneatpill), [`StatusOnEnemyDeath` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonenemydeath), [`StatusOnFallAsleep` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonfallasleep), [`StatusOnHealed` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonhealed), [`StatusOnPickupCoins` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonpickupcoins), [`StatusOnTurnEndIfCastNSpells` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonturnendifcastnspells), [`StatusOnUseBasicAttack` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonusebasicattack), [`StatusWhenAllySpendsMana` (Items_and_Equipment)](./Items_and_Equipment.md#context-statuswhenallyspendsmana), [`TempPassiveUntilSettled` (Items_and_Equipment)](./Items_and_Equipment.md#context-temppassiveuntilsettled), [`damage_instance` (Items_and_Equipment)](./Items_and_Equipment.md#context-damage_instance), [`CharacterTypeGainsStatusAtBattleStart` (Miscellaneous)](./Miscellaneous.md#context-charactertypegainsstatusatbattlestart), [`passives` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passives), [`AddStatusToBasicAttack` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustobasicattack), [`effects` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-effects), [`AddPassivesToMinions` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addpassivestominions), [`StatusOnTookDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusontookdamage), [`StatusEachTurnEnd` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuseachturnend), [`StatusOnBattleEnd` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonbattleend), [`StatusOnKill` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonkill), [`StatusOnStanceSwitch` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonstanceswitch), [`StatusEachTurnBegin` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuseachturnbegin), [`Conditional_Ally` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_ally), [`CritsApplyStatus` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-critsapplystatus), [`MeleeRevengeDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-meleerevengedamage), [`PassiveIfAllArmorEmpty` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passiveifallarmorempty), [`RandomStatusFromPool` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-randomstatusfrompool), [`StatusOnCrit` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusoncrit), [`Conditional_Enemy` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_enemy), [`PassiveIfEmptyFace` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passiveifemptyface), [`PassiveIfEmptyHead` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passiveifemptyhead), [`PassiveIfEmptyNeck` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passiveifemptyneck), [`StatusAlliesOnDeath` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusalliesondeath), [`StatusOnUseAbilityWithTag` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonuseabilitywithtag), [`AddStatusToElementAbilities` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustoelementabilities), [`AddStatusToWeapons` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustoweapons), [`Else` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-else), [`keyword_tooltips` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-keyword_tooltips), [`AddStatusToAllDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustoalldamage), [`AddStatusToBasicMeleeAttack` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustobasicmeleeattack), [`StatusOnCastSpell` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusoncastspell), [`StatusOnOverHealed` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonoverhealed), [`AddPassivesToCharmed` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addpassivestocharmed), [`AddStatusToElementDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustoelementdamage), [`AddStatusToExplosions` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustoexplosions), [`Conditional_FirstApplicationThisTurn` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_firstapplicationthisturn), [`PassiveWhenAtFullMana` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passivewhenatfullmana), [`StatusAlliesOnKill` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusalliesonkill), [`StatusIfUnusedMovePoints` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusifunusedmovepoints), [`StatusOnTurnEndIfCastNSpells` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonturnendifcastnspells), [`StatusOnTurnEndIfManaExact` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonturnendifmanaexact), [`StatusOnTurnEndIfManaOrHealthExact` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonturnendifmanaorhealthexact), [`AddSelfStatusToBasicAttack` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addselfstatustobasicattack), [`Conditional_BadRoll` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_badroll), [`Conditional_HasStatus` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_hasstatus), [`StatusEveryXSpellCasts` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuseveryxspellcasts), [`StatusGroup` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusgroup), [`StatusKilledCharacters` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuskilledcharacters), [`StatusOnAllyCatDeath` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonallycatdeath), [`StatusOnBattleStart` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonbattlestart), [`StatusOnEatFood` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusoneatfood), [`StatusOnGainCoins` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusongaincoins), [`StatusOnHealed` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonhealed), [`StatusOnKillEnemy` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonkillenemy), [`StatusOnTookDamageFromAbility` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusontookdamagefromability), [`statuses` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuses), [`AddPassivesToSummonAbilityMinions` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addpassivestosummonabilityminions), [`AddSelfStatusToWeapons` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addselfstatustoweapons), [`AddStatusToAllDamageAbilities` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustoalldamageabilities), [`AddStatusToFirstBasicAttack` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustofirstbasicattack), [`AddStatusToTrampleDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustotrampledamage), [`ApplyStatusIfCrit` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-applystatusifcrit), [`ApplyStatusesToRandomEnemiesEachTurn` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-applystatusestorandomenemieseachturn), [`ApplyToSource` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-applytosource), [`CatchProjectiles` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-catchprojectiles), [`Conditional_Adjacent` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_adjacent), [`Conditional_Boss` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_boss), [`Conditional_Corpse` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_corpse), [`Conditional_HasTag` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_hastag), [`Conditional_NotBoss` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_notboss), [`Conditional_PartyMember` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_partymember), [`Conditional_Shielded` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_shielded), [`Electric` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-electric), [`Eternal` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-eternal), [`Fire` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-fire), [`Grass` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-grass), [`Gravity` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-gravity), [`Holy` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-holy), [`HolyDamageBlessing` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-holydamageblessing), [`Ice` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-ice), [`LateBloomer` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-latebloomer), [`LightningRod` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-lightningrod), [`NextBattleStatus` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-nextbattlestatus), [`PassiveAtFullHealth` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passiveatfullhealth), [`PassiveGroup` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passivegroup), [`PassiveUntilCastSpell` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passiveuntilcastspell), [`PassiveWhileInMonkMeleeStance` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passivewhileinmonkmeleestance), [`PassiveWhileInMonkRangedStance` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passivewhileinmonkrangedstance), [`PassiveWhilePreviewingMonkRangedStance` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passivewhilepreviewingmonkrangedstance), [`ScaledStatusOnOverMana` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-scaledstatusonovermana), [`ScaledStatusOnSpendMana` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-scaledstatusonspendmana), [`SpecialFriends` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-specialfriends), [`StatusAfterCastSpell` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusaftercastspell), [`StatusAlliesOnBattleStart` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusalliesonbattlestart), [`StatusAlliesOnGainCoins` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusalliesongaincoins), [`StatusAllyWhenAllySpendsMana` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusallywhenallyspendsmana), [`StatusAnyCatAllyWhoKills` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusanycatallywhokills), [`StatusDamagers` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusdamagers), [`StatusEachTurnEndForEachTurn` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuseachturnendforeachturn), [`StatusEachTurnEndPerEnemyKill` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuseachturnendperenemykill), [`StatusEnemiesOnDeath` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusenemiesondeath), [`StatusEveryXTurnBegins` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuseveryxturnbegins), [`StatusKillers` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuskillers), [`StatusOnAnyDeath` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonanydeath), [`StatusOnBreakItem` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonbreakitem), [`StatusOnCollectPickup` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusoncollectpickup), [`StatusOnDealtDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusondealtdamage), [`StatusOnDealtDamageThreshold` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusondealtdamagethreshold), [`StatusOnEndMove` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonendmove), [`StatusOnGainShield` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusongainshield), [`StatusOnHeal` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonheal), [`StatusOnOverMana` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonovermana), [`StatusOnPickupCoins` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonpickupcoins), [`StatusOnPopCorpse` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonpopcorpse), [`StatusOnTookDamageFromEnemyAbility` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusontookdamagefromenemyability), [`StatusOnTriggerTrap` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusontriggertrap), [`StatusOnUseBasicAttack` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonusebasicattack), [`StatusOnUseElementAbility` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonuseelementability), [`StatusPerInjury` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusperinjury), [`StatusWhenAllySpendsMana` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuswhenallyspendsmana), [`TaggedPickupEffectReplacement` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-taggedpickupeffectreplacement), [`AddStatusToKnockbackDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustoknockbackdamage), [`AddStatusToSpells` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustospells), [`AddStatusesIfPersistentWeatherElement` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatusesifpersistentweatherelement), [`AddStatusesToReceivedElementalDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatusestoreceivedelementaldamage), [`Conditional_DoesDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_doesdamage), [`Conditional_GoodRoll` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_goodroll), [`Diabetes` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-diabetes), [`PassiveLevelScaledStatus` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passivelevelscaledstatus), [`RandomPassivePool` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-randompassivepool), [`ScaledStatusOnBleedDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-scaledstatusonbleeddamage), [`ScaledStatusOnLoseShield` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-scaledstatusonloseshield), [`StatusAlliesEachTurn` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusallieseachturn), [`StatusAlliesOnSpendMana` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusalliesonspendmana), [`StatusAlliesScaledByCursedOnDeath` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusalliesscaledbycursedondeath), [`StatusIfBattleAlreadyBegan` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusifbattlealreadybegan), [`StatusOnEatPill` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusoneatpill), [`StatusOnLoseShield` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonloseshield), [`StatusOnTakeHealthDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusontakehealthdamage), [`StatusOnTurnEndIfDidntCastAbilityTypes` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonturnendifdidntcastabilitytypes), [`TakeBonusTurnWithStatus` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-takebonusturnwithstatus), [`TheHunger` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-thehunger)

### Valid Property Keys

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`AIControlNextTurn`](#aicontrolnextturn) | Block | Applies or references the 'AIControlNextTurn' effect/state. |
| `AOEBonus` | Integer | Applies or references the 'AOEBonus' effect/state. |
| [`AbilityAfterEnemyCastSpell_Stackable`](./Enums.md#enum-abilityafterenemycastspell_stackable) | Enum | Applies or references the 'AbilityAfterEnemyCastSpell_Stackable' effect/state. |
| [`AbilityChargeRefundChance`](#abilitychargerefundchance) | Block | Applies the 'AbilityChargeRefundChance' effect. |
| `AbilityDamageMultiplier` | Integer |  |
| `AbilityDisableIfLivingCrow` | Integer | Applies or references the 'AbilityDisableIfLivingCrow' effect/state. |
| [`AbilityEnableIfConsumedCharacterHasTag`](./Enums.md#enum-abilityenableifconsumedcharacterhastag) | Enum | Applies or references the 'AbilityEnableIfConsumedCharacterHasTag' effect/state. |
| `AbilityEnabledAtHealthThreshold` | Integer | Applies or references the 'AbilityEnabledAtHealthThreshold' effect/state. |
| `AbilityEnabledIfBasicAttackUsedThisTurn` | Integer | Applies or references the 'AbilityEnabledIfBasicAttackUsedThisTurn' effect/state. |
| [`AbilityEnabledIfHasStatus`](./Enums.md#enum-abilityenabledifhasstatus) | Enum | Applies or references the 'AbilityEnabledIfHasStatus' effect/state. |
| `AbilityEnabledIfMovementTrapped` | Integer | Applies or references the 'AbilityEnabledIfMovementTrapped' effect/state. |
| `AbilityEnabledIfNoAggroTarget` | Integer | Applies or references the 'AbilityEnabledIfNoAggroTarget' effect/state. |
| [`AbilityEnabledIfNotHasStatus`](./Enums.md#enum-abilityenabledifnothasstatus) | Enum | Applies or references the 'AbilityEnabledIfNotHasStatus' effect/state. |
| [`AbilityEnabledIfSpecificItemEquipped`](./Enums.md#enum-abilityenabledifspecificitemequipped) | Enum | Applies or references the 'AbilityEnabledIfSpecificItemEquipped' effect/state. |
| `AbilityEnabledOncePerFightAtHealthThreshold` | Integer | Applies or references the 'AbilityEnabledOncePerFightAtHealthThreshold' effect/state. |
| `AbilityEnabledOncePerRound` | Integer | Applies or references the 'AbilityEnabledOncePerRound' effect/state. |
| `AbilityEnabledPercentEachTurn` | Integer | Applies or references the 'AbilityEnabledPercentEachTurn' effect/state. |
| [`AbilityHealthThreshold`](#abilityhealththreshold) | Block | AI Trigger: Executes an ability when health drops below a specific threshold. |
| `AbilityInheritsWeaponEffects` | Integer | Applies or references the 'AbilityInheritsWeaponEffects' effect/state. |
| [`AbilityOnBattleStart`](./Enums.md#enum-abilityonbattlestart) | Enum | Applies or references the 'AbilityOnBattleStart' effect/state. |
| `AbilityOnBattleStart_Immediate` | Enum/String | Applies or references the 'AbilityOnBattleStart_Immediate' effect/state. |
| [`AbilityOnBattleStart_UseAI`](./Enums.md#enum-abilityonbattlestart_useai) | Enum | Applies or references the 'AbilityOnBattleStart_UseAI' effect/state. |
| [`AbilityOnRoundEnd`](#abilityonroundend) | Block | AI Trigger: Executes an ability at the end of the combat round. |
| [`AbilityOnRoundEndOnce`](#abilityonroundendonce) | Block | Applies or references the 'AbilityOnRoundEndOnce' effect/state. |
| [`AbilityReaction`](./Enums.md#enum-abilityreaction) | Enum | AI Trigger: Executes an ability in reaction to a specific event (e.g., taking damage). |
| [`AbilityWhenBuddyDies`](./Enums.md#enum-abilitywhenbuddydies) | Enum | Applies or references the 'AbilityWhenBuddyDies' effect/state. |
| [`AbilityWhenTaggedCharacterMovesNear`](#abilitywhentaggedcharactermovesnear) | Block | AI Trigger: Executes an ability when a character with a specific tag moves adjacent. |
| `AbsorbManaAura` | Integer | Applies the 'AbsorbManaAura' effect. |
| `AbsorbManaFromOtherSpells` | Integer | Applies or references the 'AbsorbManaFromOtherSpells' effect/state. |
| [`AddAdvantageToEvent`](#addadvantagetoevent) | Block | Applies or references the 'AddAdvantageToEvent' effect/state. |
| `AddAllyNeighborsToAbilityRange` | Integer | Applies the 'AddAllyNeighborsToAbilityRange' effect. |
| `AddAllyNeighborsToAttackRange` | Integer | Applies the 'AddAllyNeighborsToAttackRange' effect. |
| `AddBonusMeleeRange` | Integer | Applies the 'AddBonusMeleeRange' effect. |
| `AddBonusRange` | Integer | Applies or references the 'AddBonusRange' effect/state. |
| `AddChaScalingSpellDamage` | Integer | Applies the 'AddChaScalingSpellDamage' effect. |
| `AddConstitution` | Integer |  |
| `AddCorpseHealth` | Integer | Applies the 'AddCorpseHealth' effect. |
| `AddCritMultiplier` | Integer | Applies the 'AddCritMultiplier' effect. |
| `AddDamage` | Integer | Applies or references the 'AddDamage' effect/state. |
| `AddDamageToBasicAttack` | Integer | Applies the 'AddDamageToBasicAttack' effect. |
| [`AddDamageToElementDamage`](#adddamagetoelementdamage) | Block | Applies or references the 'AddDamageToElementDamage' effect/state. |
| [`AddElementsToBasicAttack`](./Enums.md#enum-addelementstobasicattack) | Enum |  |
| [`AddElementsToSpells`](./Enums.md#enum-addelementstospells) | Enum | Applies or references the 'AddElementsToSpells' effect/state. |
| `AddEndOfCombatRegen` | Integer | Applies or references the 'AddEndOfCombatRegen' effect/state. |
| [`AddHiddenTag`](./Enums.md#enum-addhiddentag) | Enum | Applies or references the 'AddHiddenTag' effect/state. |
| `AddInitiative` | Integer | Applies or references the 'AddInitiative' effect/state. |
| `AddKnockbackDamage` | Integer | Applies or references the 'AddKnockbackDamage' effect/state. |
| `AddKnockbackToEverything` | Integer | Applies the 'AddKnockbackToEverything' effect. |
| `AddLevelUpRerolls` | Integer | Applies or references the 'AddLevelUpRerolls' effect/state. |
| `AddLevelUpStatMultiplier` | Integer | Applies the 'AddLevelUpStatMultiplier' effect. |
| `AddLootMultiplier` | Integer |  |
| `AddManaRegen` | Integer | Applies or references the 'AddManaRegen' effect/state. |
| `AddMaxHealth` | Integer | Applies or references the 'AddMaxHealth' effect/state. |
| `AddMeleeKnockback` | Integer | Applies or references the 'AddMeleeKnockback' effect/state. |
| `AddMovement` | Integer | Applies or references the 'AddMovement' effect/state. |
| [`AddPassiveToSpawnedRocks`](#addpassivetospawnedrocks) | Block | Applies the 'AddPassiveToSpawnedRocks' effect. |
| [`AddPassivesToCharmed`](#addpassivestocharmed) | Block | Applies the 'AddPassivesToCharmed' effect. |
| [`AddPassivesToMinions`](#addpassivestominions) | Block | Applies the 'AddPassivesToMinions' effect. |
| [`AddPassivesToSummonAbilityMinions`](#addpassivestosummonabilityminions) | Block | Applies the 'AddPassivesToSummonAbilityMinions' effect. |
| `AddRandomEliteBuff` | Integer |  |
| `AddRangedCritChance` | Integer | Applies the 'AddRangedCritChance' effect. |
| [`AddSelfStatusToBasicAttack`](#addselfstatustobasicattack) | Block | Applies or references the 'AddSelfStatusToBasicAttack' effect/state. |
| [`AddSelfStatusToWeapons`](#addselfstatustoweapons) | Block | Applies the 'AddSelfStatusToWeapons' effect. |
| `AddSpeed` | Integer | Applies the 'AddSpeed' effect. |
| `AddSpellDamage` | Integer | Applies the 'AddSpellDamage' effect. |
| `AddStartingMana` | Integer | Applies or references the 'AddStartingMana' effect/state. |
| [`AddStatusToAllDamage`](#addstatustoalldamage) | Block | Modifier: Injects a status effect into a specific action. |
| [`AddStatusToAllDamageAbilities`](#addstatustoalldamageabilities) | Block | Applies the 'AddStatusToAllDamageAbilities' effect. |
| [`AddStatusToBackstabs`](#addstatustobackstabs) | Block | Modifier: Injects a status effect into a specific action. |
| [`AddStatusToBasicAttack`](#addstatustobasicattack) | Block | Injects a status effect payload that applies whenever the character performs a basic attack. |
| [`AddStatusToBasicAttackWithCooldown`](#addstatustobasicattackwithcooldown) | Block | Applies the 'AddStatusToBasicAttackWithCooldown' effect. |
| [`AddStatusToBasicMeleeAttack`](#addstatustobasicmeleeattack) | Block |  |
| [`AddStatusToElementAbilities`](#addstatustoelementabilities) | Block | Applies the 'AddStatusToElementAbilities' effect. |
| [`AddStatusToElementDamage`](#addstatustoelementdamage) | Block | Applies the 'AddStatusToElementDamage' effect. |
| [`AddStatusToExplosions`](#addstatustoexplosions) | Block | Applies the 'AddStatusToExplosions' effect. |
| [`AddStatusToFirstBasicAttack`](#addstatustofirstbasicattack) | Block | Applies the 'AddStatusToFirstBasicAttack' effect. |
| [`AddStatusToFirstSpellEachTurn`](#addstatustofirstspelleachturn) | Block |  |
| [`AddStatusToKnockbackDamage`](#addstatustoknockbackdamage) | Block | Modifier: Injects a status effect into a specific action. |
| [`AddStatusToMeleeDamage`](#addstatustomeleedamage) | Block | Applies the 'AddStatusToMeleeDamage' effect. |
| [`AddStatusToReceivedDamage`](#addstatustoreceiveddamage) | Block | Modifier: Applies a status effect whenever the character takes damage. |
| [`AddStatusToReceivedDamage_ExcludeStatuses`](#addstatustoreceiveddamage_excludestatuses) | Block | Applies the 'AddStatusToReceivedDamage_ExcludeStatuses' effect. |
| [`AddStatusToSpells`](#addstatustospells) | Block | Modifier: Injects a status effect into a specific action. |
| [`AddStatusToTrampleDamage`](#addstatustotrampledamage) | Block | Applies the 'AddStatusToTrampleDamage' effect. |
| [`AddStatusToWeapons`](#addstatustoweapons) | Block | Applies the 'AddStatusToWeapons' effect. |
| [`AddStatusesIfPersistentWeatherElement`](#addstatusesifpersistentweatherelement) | Block | Applies the 'AddStatusesIfPersistentWeatherElement' effect. |
| [`AddStatusesToReceivedElementalDamage`](#addstatusestoreceivedelementaldamage) | Block | Applies the 'AddStatusesToReceivedElementalDamage' effect. |
| [`AddTag`](./Enums.md#enum-addtag) | Enum | Applies or references the 'AddTag' effect/state. |
| [`AddTemporaryEffectsToBasicAttack`](#addtemporaryeffectstobasicattack) | Block | Applies the 'AddTemporaryEffectsToBasicAttack' effect. |
| [`AddTemporaryEffectsToEquipment`](#addtemporaryeffectstoequipment) | Block | Applies the 'AddTemporaryEffectsToEquipment' effect. |
| `AddUnfilledMaxHealth` | Integer | Applies the 'AddUnfilledMaxHealth' effect. |
| `AddWeaponAux` | Integer | Applies or references the 'AddWeaponAux' effect/state. |
| `AddWeaponScaling` | Integer | Applies the 'AddWeaponScaling' effect. |
| [`AdvancedTint`](./Arrays.md#array-advancedtint) | Array | Applies or references the 'AdvancedTint' effect/state. |
| [`AdventureTokenPassivePool`](#adventuretokenpassivepool) | Block | Map/Metaprogression: Pool of passive modifiers applied by adventure tokens. |
| [`AfterImage`](./Enums.md#enum-afterimage) | Enum | Spawns a visual decoy or shade at the caster's previous location. |
| `AggroTargetIsBuddy` | Integer | Applies or references the 'AggroTargetIsBuddy' effect/state. |
| `AggroTargetIsCurrentTurn` | Integer | Applies or references the 'AggroTargetIsCurrentTurn' effect/state. |
| [`AggroTargetIsGovernedByHitEffect`](#aggrotargetisgovernedbyhiteffect) | Block | AI Logic: Forces the character's aggro to follow specific hit effects rather than default proximity. |
| `AggroTargetIsLastEnemyThatDealtDamage` | Integer | Applies or references the 'AggroTargetIsLastEnemyThatDealtDamage' effect/state. |
| `AggroTargetIsLowestHealthEnemyTillItDies` | Integer | Applies or references the 'AggroTargetIsLowestHealthEnemyTillItDies' effect/state. |
| `AggroTargetIsLowestMaxHealthCat` | Integer | Applies or references the 'AggroTargetIsLowestMaxHealthCat' effect/state. |
| [`AlienBeastDangerZones`](./Arrays.md#array-alienbeastdangerzones) | Array | Applies or references the 'AlienBeastDangerZones' effect/state. |
| `AlienBeastEyeStalks` | Integer | Applies or references the 'AlienBeastEyeStalks' effect/state. |
| `AllDamageCrits` | Integer | Applies the 'AllDamageCrits' effect. |
| `AllDamageImmune_IncludingSpeculative` | Integer | Applies or references the 'AllDamageImmune_IncludingSpeculative' effect/state. |
| `AllSpellsCostActPoints` | Integer | Applies or references the 'AllSpellsCostActPoints' effect/state. |
| `AllSpellsCostCharge` | Integer | Applies or references the 'AllSpellsCostCharge' effect/state. |
| [`AllStatsAura`](#allstatsaura) | Block | Passive: Projects an aura that modifies all primary stats of nearby characters. |
| `AllStatsUp` | Integer | Applies or references the 'AllStatsUp' effect/state. |
| `AllStatsUpPerDisorder` | Integer | Applies or references the 'AllStatsUpPerDisorder' effect/state. |
| `AllUnitsExplodeOnDeath` | Integer | Applies or references the 'AllUnitsExplodeOnDeath' effect/state. |
| `AlliesAvoidTraps` | Integer | Applies the 'AlliesAvoidTraps' effect. |
| `AlliesScrambleSpellAfterCast` | Integer | Applies or references the 'AlliesScrambleSpellAfterCast' effect/state. |
| `AllowPassTurn` | Integer | Applies the 'AllowPassTurn' effect. |
| [`AlluringDoodieEater`](#alluringdoodieeater) | Block | Applies or references the 'AlluringDoodieEater' effect/state. |
| [`AllyBonusAbilityAura`](./Enums.md#enum-allybonusabilityaura) | Enum | Applies the 'AllyBonusAbilityAura' effect. |
| `AllyChainKnockback` | Integer | Applies the 'AllyChainKnockback' effect. |
| [`AllyDamageReaction`](./Enums.md#enum-allydamagereaction) | Enum | Applies the 'AllyDamageReaction' effect. |
| `AllyDamageReduction` | Integer | Applies the 'AllyDamageReduction' effect. |
| [`AllyDodgeChanceAura`](#allydodgechanceaura) | Block | Applies or references the 'AllyDodgeChanceAura' effect/state. |
| [`AllyHealthRegenAura`](#allyhealthregenaura) | Block | Applies the 'AllyHealthRegenAura' effect. |
| [`AllyManaRegenAura`](#allymanaregenaura) | Block | Applies the 'AllyManaRegenAura' effect. |
| [`AllyMoveAbilityAura`](./Enums.md#enum-allymoveabilityaura) | Enum | Applies the 'AllyMoveAbilityAura' effect. |
| `AllyMultiplyKnockbackDamage` | Integer | Applies the 'AllyMultiplyKnockbackDamage' effect. |
| `AllyMultiplyKnockbackDistance` | Integer | Applies the 'AllyMultiplyKnockbackDistance' effect. |
| `AllyUncappedHPAura` | Integer | Applies the 'AllyUncappedHPAura' effect. |
| `AlphaAllStatsUp` | Integer | Applies or references the 'AlphaAllStatsUp' effect/state. |
| `AlphaCat` | Integer | Applies or references the 'AlphaCat' effect/state. |
| `AlphaDodgeChance` | Integer | Applies or references the 'AlphaDodgeChance' effect/state. |
| [`AlphaStatusOnTurnBegin`](#alphastatusonturnbegin) | Block | Grants a specific status effect to the 'Alpha' (the party leader) at the start of their turn. |
| `AlphaTurns` | Integer | Applies the 'AlphaTurns' effect. |
| [`AlternateCraftingPools`](#alternatecraftingpools) | Block | Applies the 'AlternateCraftingPools' effect. |
| `AlwaysChosenForLevelUp` | Integer | Applies or references the 'AlwaysChosenForLevelUp' effect/state. |
| `AlwaysHitDifferentTargets` | Integer | Applies or references the 'AlwaysHitDifferentTargets' effect/state. |
| `Ammo` | Integer | Applies or references the 'Ammo' effect/state. |
| `AmplifyKnockback` | Integer | Applies the 'AmplifyKnockback' effect. |
| `AmplifyNegativeStatus` | Integer | Applies the 'AmplifyNegativeStatus' effect. |
| `AmplifyPositiveStatus` | Integer | Applies the 'AmplifyPositiveStatus' effect. |
| [`AmplifyStatus`](./Enums.md#enum-amplifystatus) | Enum | Applies the 'AmplifyStatus' effect. |
| `Angel` | Integer | Applies or references the 'Angel' effect/state. |
| [`ApplyPassivesToSpawnerWhileAlive`](#applypassivestospawnerwhilealive) | Block | Grants nested passives to the entity that spawned this object, lasting only as long as this object remains alive. |
| [`ApplyStatusIfCrit`](#applystatusifcrit) | Block | Conditional trigger: Executes the nested logic only if the triggering action was a critical hit. |
| [`ApplyStatusesToRandomEnemiesEachTurn`](#applystatusestorandomenemieseachturn) | Block | Applies or references the 'ApplyStatusesToRandomEnemiesEachTurn' effect/state. |
| [`ApplyToRandomPartyMemberIfPossible`](#applytorandompartymemberifpossible) | Block | Redirects the nested effects to apply to a random living member of the player's party. |
| [`ApplyToSource`](#applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| [`ArmorBreakOnHit`](#armorbreakonhit) | Block | Applies or references the 'ArmorBreakOnHit' effect/state. |
| `ArmorDodgeChance` | Integer | Applies or references the 'ArmorDodgeChance' effect/state. |
| [`ArmorPickup`](#armorpickup) | Block | Pickup Logic: Defines what happens when an armor item is collected. |
| [`Autism`](#autism) | Block | Applies the 'Autism' effect. |
| `AutoCritLowDamage` | Integer | Applies the 'AutoCritLowDamage' effect. |
| `AutoEquipConsumables` | Integer | Applies or references the 'AutoEquipConsumables' effect/state. |
| `AutoReanimate` | Integer | Applies the 'AutoReanimate' effect. |
| [`AutocastEachRound`](#autocasteachround) | Block | Forces the character to automatically cast a specific ability at the start of each combat round. |
| [`AutocastEachTurn`](./Enums.md#enum-autocasteachturn) | Enum | Applies the 'AutocastEachTurn' effect. |
| [`AutocastEachTurnBegin`](./Enums.md#enum-autocasteachturnbegin) | Enum | Applies the 'AutocastEachTurnBegin' effect. |
| `AvoidDamagingCharmedEnemies` | Integer | Applies or references the 'AvoidDamagingCharmedEnemies' effect/state. |
| `AwardCoinsOnDeath` | Integer | Applies or references the 'AwardCoinsOnDeath' effect/state. |
| `BackflipWhenTargeted` | Integer | Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack. |
| `BackstabAllDirections` | Integer | Applies or references the 'BackstabAllDirections' effect/state. |
| `BackstabCritChance` | Integer | Applies the 'BackstabCritChance' effect. |
| `BackstabFront` | Integer |  |
| `BackstabImmunity` | Integer | Applies or references the 'BackstabImmunity' effect/state. |
| `BackstabWeakness` | Integer | Applies the 'BackstabWeakness' effect. |
| [`BaitAura`](#baitaura) | Block | Passive: Projects an aura that attracts specific enemy types (e.g., flies/maggots). |
| `BalanceStats` | Integer | Applies or references the 'BalanceStats' effect/state. |
| `BaseStatMultiply` | Float | Applies or references the 'BaseStatMultiply' effect/state. |
| `BasicAIDangerZone` | Integer | Applies or references the 'BasicAIDangerZone' effect/state. |
| `BasicAttackAOEBonus` | Integer | Applies the 'BasicAttackAOEBonus' effect. |
| `BasicAttackCantMiss` | Integer |  |
| `BasicAttackCritChance` | Integer | Applies the 'BasicAttackCritChance' effect. |
| `BasicAttackDamageMultiplier` | Integer | Applies the 'BasicAttackDamageMultiplier' effect. |
| `BasicAttackStatusCarefulness` | Integer | Applies the 'BasicAttackStatusCarefulness' effect. |
| [`BasicAttackStatusSwap`](./Arrays.md#array-basicattackstatusswap) | Array | Applies the 'BasicAttackStatusSwap' effect. |
| [`BattlefieldUniqueRandomPassive`](#battlefielduniquerandompassive) | Block | Map Rule: Grants a unique random passive modifier to the battlefield. |
| `BigSplashDamage` | Integer | Applies the 'BigSplashDamage' effect. |
| [`Bird`](./Enums.md#enum-bird) | Enum | Applies or references the 'Bird' effect/state. |
| [`BirdRewards`](#birdrewards) | Block | Loot logic: Rewards dropped by bird-type enemies. |
| `BlackHolePassive` | Integer | Applies or references the 'BlackHolePassive' effect/state. |
| [`BlacklistPickupType`](./Enums.md#enum-blacklistpickuptype) | Enum |  |
| `BlastResistance` | Integer | Applies the 'BlastResistance' effect. |
| `Bleed` | Integer | Applies or references the 'Bleed' effect/state. |
| `BleedThorns` | Integer | Applies or references the 'BleedThorns' effect/state. |
| `BlessingOfPeace` | Integer | Applies or references the 'BlessingOfPeace' effect/state. |
| `Blind` | Integer |  |
| [`BloatEyePassive2`](./Enums.md#enum-bloateyepassive2) | Enum | Applies or references the 'BloatEyePassive2' effect/state. |
| `BlockAllDamage` | Integer | Applies or references the 'BlockAllDamage' effect/state. |
| `BlockDamageUnderThreshold` | Integer | Applies or references the 'BlockDamageUnderThreshold' effect/state. |
| `BlockNegativeStatus` | Integer | Applies or references the 'BlockNegativeStatus' effect/state. |
| `BombBehavior` | Integer | Applies or references the 'BombBehavior' effect/state. |
| `BoneArmorPassive` | Integer | Applies or references the 'BoneArmorPassive' effect/state. |
| [`BonusAbility`](./Enums.md#enum-bonusability) | Enum | Applies the 'BonusAbility' effect. |
| [`BonusAbility_DelayedApplication`](./Enums.md#enum-bonusability_delayedapplication) | Enum | Applies or references the 'BonusAbility_DelayedApplication' effect/state. |
| `BonusDamage` | Integer | Applies or references the 'BonusDamage' effect/state. |
| `BonusFoodEachBattle` | Integer | Applies the 'BonusFoodEachBattle' effect. |
| `BonusHealthRegenBasedOnDex` | Integer | Applies the 'BonusHealthRegenBasedOnDex' effect. |
| `BonusHealthRegenPerDisorder` | Integer |  |
| `BonusKnockbackDamage` | Integer | Applies or references the 'BonusKnockbackDamage' effect/state. |
| `BonusRangeBasedOnDex` | Integer | Applies the 'BonusRangeBasedOnDex' effect. |
| [`BonusTurnPattern`](./Arrays.md#array-bonusturnpattern) | Array | Applies or references the 'BonusTurnPattern' effect/state. |
| [`BoobyTrapItems`](#boobytrapitems) | Block | Applies the 'BoobyTrapItems' effect. |
| `BoostAllyStatsOnDeath` | Integer | Applies the 'BoostAllyStatsOnDeath' effect. |
| `BoostDamageAura` | Integer | Applies the 'BoostDamageAura' effect. |
| `BoostDamageGlobalAura` | Integer | Applies the 'BoostDamageGlobalAura' effect. |
| `BoostHeals` | Integer | Applies or references the 'BoostHeals' effect/state. |
| `BoostRangeAura` | Integer | Applies the 'BoostRangeAura' effect. |
| `BoostRangeGlobalAura` | Integer | Applies the 'BoostRangeGlobalAura' effect. |
| `BoostReceivedHealing` | Integer | Applies or references the 'BoostReceivedHealing' effect/state. |
| `BoostWeaponDamage` | Integer | Applies the 'BoostWeaponDamage' effect. |
| [`BossRewards`](#bossrewards) | Block | Loot logic: Rewards dropped upon defeating a boss. |
| [`BounceObject`](./Enums.md#enum-bounceobject) | Enum | Spawns a physics object that visually bounces off the target. |
| [`BouncyProjectiles`](#bouncyprojectiles) | Block | Applies the 'BouncyProjectiles' effect. |
| `Bounty` | Integer | Applies the 'Bounty' effect. |
| `Brace` | Integer | Applies or references the 'Brace' effect/state. |
| `BraceForEachNeighboringEnemy` | Integer | Applies the 'BraceForEachNeighboringEnemy' effect. |
| `BreakAtAux` | Integer | Applies or references the 'BreakAtAux' effect/state. |
| [`BreakOnElement`](./Enums.md#enum-breakonelement) | Enum | Applies or references the 'BreakOnElement' effect/state. |
| `BreakWhenNoShield` | Integer | Applies or references the 'BreakWhenNoShield' effect/state. |
| `Brittle` | Integer | Applies or references the 'Brittle' effect/state. |
| `BrittleCharismaUp` | Integer | Applies or references the 'BrittleCharismaUp' effect/state. |
| `BrittleConstitutionUp` | Integer | Applies or references the 'BrittleConstitutionUp' effect/state. |
| `BrittleDexterityUp` | Integer | Applies or references the 'BrittleDexterityUp' effect/state. |
| [`BrittleDuringElement`](./Enums.md#enum-brittleduringelement) | Enum | Applies or references the 'BrittleDuringElement' effect/state. |
| `BrittleIntelligenceUp` | Integer | Applies or references the 'BrittleIntelligenceUp' effect/state. |
| `BrittleLuckUp` | Integer | Applies or references the 'BrittleLuckUp' effect/state. |
| `BrittleSpeedUp` | Integer | Applies or references the 'BrittleSpeedUp' effect/state. |
| `BrittleStrengthUp` | Integer | Applies or references the 'BrittleStrengthUp' effect/state. |
| `Bruise` | Integer | Applies or references the 'Bruise' effect/state. |
| [`Buddy`](./Enums.md#enum-buddy) | Enum | Character Form / AI State: Behavior and stats for the 'Buddy' familiar state. |
| `BuffImmunity` | Integer | Applies or references the 'BuffImmunity' effect/state. |
| [`BungaCheers`](#bungacheers) | Block | Animation/AI State: Bunga cheering animation logic. |
| [`BungaEntrance`](#bungaentrance) | Block | Animation/AI State: Bunga entering the arena. |
| `BurgleCoin` | Integer | Applies the 'BurgleCoin' effect. |
| `Burn` | Integer | Applies or references the 'Burn' effect/state. |
| `CCImmunity` | Integer | Applies the 'CCImmunity' effect. |
| `CanLevelUpWhenDead` | Integer | Applies or references the 'CanLevelUpWhenDead' effect/state. |
| [`CanMutateTo`](./Enums.md#enum-canmutateto) | Enum | Applies or references the 'CanMutateTo' effect/state. |
| `CanRemoveCursedItems` | Integer |  |
| `CanShield` | Integer | Applies or references the 'CanShield' effect/state. |
| `CantCatchDiseases` | Integer | Applies or references the 'CantCatchDiseases' effect/state. |
| `CantDodge` | Integer | Applies the 'CantDodge' effect. |
| `CantSpreadDiseases` | Integer | Applies or references the 'CantSpreadDiseases' effect/state. |
| `CapBasicAttackDamage` | Integer | Applies or references the 'CapBasicAttackDamage' effect/state. |
| `CapDamageFromAllies` | Integer | Applies the 'CapDamageFromAllies' effect. |
| `CapMovementAbilityRange` | Integer | Applies or references the 'CapMovementAbilityRange' effect/state. |
| `CapReceivedDamage` | Integer | Applies or references the 'CapReceivedDamage' effect/state. |
| `CapTechSpent` | Integer | Applies the 'CapTechSpent' effect. |
| `CaptureFamiliar` | Integer | Applies or references the 'CaptureFamiliar' effect/state. |
| [`CatAPultAnimation`](#catapultanimation) | Block | Applies the 'CatAPultAnimation' effect. |
| [`CatPartsSizeScale`](#catpartssizescale) | Block | Applies or references the 'CatPartsSizeScale' effect/state. |
| [`CatPartsTransform`](#catpartstransform) | Block | Visual: Transforms specific body parts of the character. |
| `CatchBoomerang` | Integer | Applies or references the 'CatchBoomerang' effect/state. |
| [`CatchProjectiles`](#catchprojectiles) | Block | Applies or references the 'CatchProjectiles' effect/state. |
| [`CaveFamilyEnrage`](#cavefamilyenrage) | Block | AI Trigger: Enrage logic triggered when a cave family member is killed. |
| `CaveWomanBirthControl` | Integer | Applies or references the 'CaveWomanBirthControl' effect/state. |
| [`CerberubsAggroTargetBehavior`](#cerberubsaggrotargetbehavior) | Block | AI Logic: Custom aggro targeting rules for Cerberubs. |
| `ChainKnockback` | Integer | Applies the 'ChainKnockback' effect. |
| `ChanceToAmbush` | Integer | Applies or references the 'ChanceToAmbush' effect/state. |
| [`ChanceToBackflip`](#chancetobackflip) | Block | Applies or references the 'ChanceToBackflip' effect/state. |
| `ChanceToBlock` | Integer | Applies or references the 'ChanceToBlock' effect/state. |
| `ChanceToBlockAndCounter` | Integer | Applies or references the 'ChanceToBlockAndCounter' effect/state. |
| `ChanceToBreak` | Integer | Applies the 'ChanceToBreak' effect. |
| `ChanceToDisableActionsIfNotCharmed` | Integer | Applies or references the 'ChanceToDisableActionsIfNotCharmed' effect/state. |
| [`ChanceToForceEvent`](#chancetoforceevent) | Block | Applies or references the 'ChanceToForceEvent' effect/state. |
| [`ChanceToFormChangeOnAbilityDamage`](#chancetoformchangeonabilitydamage) | Block | Reaction: Probability to change forms when taking ability damage. |
| `ChanceToRevive` | Integer | Applies or references the 'ChanceToRevive' effect/state. |
| [`ChanceToSpitOnDamage`](#chancetospitondamage) | Block | Reaction: Probability to use a spit counter-attack when damaged. |
| `ChangeTauntPriority` | Integer | Applies the 'ChangeTauntPriority' effect. |
| [`ChangeTile`](./Enums.md#enum-changetile) | Enum |  |
| [`ChangeTileOnDeath`](./Enums.md#enum-changetileondeath) | Enum | Applies or references the 'ChangeTileOnDeath' effect/state. |
| [`ChangeTileOnPop`](./Enums.md#enum-changetileonpop) | Enum | Applies or references the 'ChangeTileOnPop' effect/state. |
| `ChangeTileUnderCharacterAtStart` | Enum/String | Applies or references the 'ChangeTileUnderCharacterAtStart' effect/state. |
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum | Applies or references the 'ChangeTilesUnder' effect/state. |
| [`ChaosBossFormChangeGuide`](#chaosbossformchangeguide) | Block | Boss Logic: Maps the form transition phases for the Chaos Boss. |
| [`ChaosBossPieces`](#chaosbosspieces) | Block | Boss Logic: Defines the separate destructible pieces of the Chaos Boss. |
| [`ChaosHeadDropIn`](#chaosheaddropin) | Block | Boss Logic: Drop-in attack/animation for the Chaos Head. |
| [`CharacterLightSource`](#characterlightsource) | Block | Visual: Attaches a dynamic lighting source to the character. |
| `Charge` | Integer | Applies or references the 'Charge' effect/state. |
| [`ChargeSpiritBombAura`](./Enums.md#enum-chargespiritbombaura) | Enum | Applies or references the 'ChargeSpiritBombAura' effect/state. |
| `CharismaIsMaxStat` | Integer | Applies or references the 'CharismaIsMaxStat' effect/state. |
| `CharismaUp` | Integer | Applies or references the 'CharismaUp' effect/state. |
| `CharmAllFlies` | Integer | Applies the 'CharmAllFlies' effect. |
| `CharmImmunity` | Integer | Applies or references the 'CharmImmunity' effect/state. |
| `Charmed` | Integer | Applies the 'Charmed' effect. |
| [`CherubimReaction`](#cherubimreaction) | Block | Reaction: Custom reaction triggers for Cherubim enemies. |
| [`ClassManaCostReduction`](#classmanacostreduction) | Block | Applies or references the 'ClassManaCostReduction' effect/state. |
| `Cleanse` | Integer |  |
| `Cleave` | Integer | Causes the attack to hit adjacent enemies alongside the primary target. |
| [`CobraReflex`](./Enums.md#enum-cobrareflex) | Enum | Applies the 'CobraReflex' effect. |
| `CoinPickup` | Integer | Applies or references the 'CoinPickup' effect/state. |
| `CoinsAddDamage` | Integer | Applies the 'CoinsAddDamage' effect. |
| `CollectPickupsOnBattleEnd` | Integer | Applies the 'CollectPickupsOnBattleEnd' effect. |
| [`Conditional_Adjacent`](#conditional_adjacent) | Block | Conditional block: Executes nested logic only if the target is/has Adjacent. |
| [`Conditional_Ally`](#conditional_ally) | Block | Conditional trigger: Executes nested logic if the target is friendly to the caster. |
| [`Conditional_BadRoll`](#conditional_badroll) | Block | Conditional trigger: Executes nested logic based on a randomized bad outcome probability. |
| [`Conditional_Boss`](#conditional_boss) | Block | Conditional trigger: Executes nested logic if the target is a Boss. |
| [`Conditional_Corpse`](#conditional_corpse) | Block | Conditional trigger: Executes nested logic if the target is a dead body/corpse. |
| [`Conditional_Enemy`](#conditional_enemy) | Block | Conditional trigger: Executes nested logic if the target is hostile to the caster. |
| [`Conditional_FirstApplicationThisTurn`](#conditional_firstapplicationthisturn) | Block | Conditional trigger: Executes nested logic only if this is the first time this specific effect has been applied this turn. |
| [`Conditional_Flying`](#conditional_flying) | Block |  |
| [`Conditional_GoodRoll`](#conditional_goodroll) | Block | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. |
| [`Conditional_HasCleansableDebuffs`](#conditional_hascleansabledebuffs) | Block |  |
| [`Conditional_HasStatus`](#conditional_hasstatus) | Block | Conditional trigger: Executes nested logic if the target currently has the specified status effect. |
| [`Conditional_HasTag`](#conditional_hastag) | Block | Conditional trigger: Executes nested logic if the target possesses the specified entity tag. |
| [`Conditional_HealthThreshold`](#conditional_healththreshold) | Block | Conditional trigger: Executes nested logic if the target's health falls below the specified threshold. |
| [`Conditional_ManaThreshold`](#conditional_manathreshold) | Block | Conditional constraint. Nested properties only trigger if this is true. |
| [`Conditional_NotBoss`](#conditional_notboss) | Block | Conditional trigger: Executes nested logic if the target is NOT a Boss. |
| [`Conditional_PartyMember`](#conditional_partymember) | Block | Conditional constraint. Nested properties only trigger if this is true. |
| [`Conditional_RandomChance`](#conditional_randomchance) | Block |  |
| [`Conditional_Shielded`](#conditional_shielded) | Block | Conditional trigger: Executes nested logic if the target currently has a Shield status. |
| [`Conditional_SourceHasTag`](#conditional_sourcehastag) | Block | Conditional block: Executes nested logic only if the target is/has SourceHasTag. |
| [`Conditional_Tiny`](#conditional_tiny) | Block |  |
| `Conductor` | Integer | Applies the 'Conductor' effect. |
| `ConductorManaRegen` | Integer | Applies the 'ConductorManaRegen' effect. |
| `Confusion` | Integer | Applies the 'Confusion' effect. |
| [`ConfusionEffectOnTaggedAbilities`](./Enums.md#enum-confusioneffectontaggedabilities) | Enum | Applies the 'ConfusionEffectOnTaggedAbilities' effect. |
| [`ConjureBonusAbility`](./Enums.md#enum-conjurebonusability) | Enum |  |
| `ConjureCastSpellsForAllies` | Integer | Applies the 'ConjureCastSpellsForAllies' effect. |
| `ConstitutionUp` | Integer | Applies or references the 'ConstitutionUp' effect/state. |
| `ConsumableEffectsMultiplierBonus` | Integer | Applies the 'ConsumableEffectsMultiplierBonus' effect. |
| `ConsumablesInfiniteRange` | Integer | Applies the 'ConsumablesInfiniteRange' effect. |
| `ConsumablesMeleeRange` | Integer | Applies the 'ConsumablesMeleeRange' effect. |
| [`Consumed`](#consumed) | Block | State triggered when the entity is eaten/consumed. |
| [`ConvertDamageToScaledStatus`](#convertdamagetoscaledstatus) | Block | Applies or references the 'ConvertDamageToScaledStatus' effect/state. |
| `CopyBasicAttackEffects` | Integer | Applies or references the 'CopyBasicAttackEffects' effect/state. |
| `CopyCatPassive_Initializer` | Integer | Applies or references the 'CopyCatPassive_Initializer' effect/state. |
| `CopyPassiveSlot` | Integer | Applies or references the 'CopyPassiveSlot' effect/state. |
| `CountAsCorpse` | Integer | Applies or references the 'CountAsCorpse' effect/state. |
| [`CounterAttack`](./Enums.md#enum-counterattack) | Enum | Reaction: Executes a counter-attack ability when hit. |
| [`CounterAttackAfterEnemyCastSpell`](./Enums.md#enum-counterattackafterenemycastspell) | Enum | Applies or references the 'CounterAttackAfterEnemyCastSpell' effect/state. |
| `CounterNextAttacks` | Integer | Applies or references the 'CounterNextAttacks' effect/state. |
| [`Craft`](#craft) | Block | Synthesizes or spawns a new item from a specific pool. |
| [`CreateGlobalModifiers`](#createglobalmodifiers) | Block | Encounter Rule: Generates map-wide modifiers. |
| `CritChanceUp` | Integer | Applies the 'CritChanceUp' effect. |
| [`CritsApplyStatus`](#critsapplystatus) | Block | Applies the 'CritsApplyStatus' effect. |
| `CrowAttackLink` | Integer | Applies or references the 'CrowAttackLink' effect/state. |
| [`CureDisease`](#curedisease) | Block | Applies the 'CureDisease' effect. |
| `CurrentWeaponDamageUp` | Integer | Applies the 'CurrentWeaponDamageUp' effect. |
| [`CyborgTurns`](#cyborgturns) | Block |  |
| `DamageEnemiesOnHeal` | Integer | Combat Trigger: Deals damage to enemies on heal. |
| `DamageEnemiesOnKill` | Integer | Combat Trigger: Deals damage to enemies on kill. |
| `DamageFromBehindOnly` | Integer | Applies or references the 'DamageFromBehindOnly' effect/state. |
| [`DamageIfDidntUseSpecificAbility`](#damageifdidntusespecificability) | Block | Combat Trigger: Deals damage to if didnt use specific ability. |
| [`DamageNeighborTilesWhenCastSpell`](#damageneighbortileswhencastspell) | Block | Combat Trigger: Deals damage to neighbor tiles when cast spell. |
| [`DamageNeighborsAfterMove`](#damageneighborsaftermove) | Block |  |
| [`DamageNeighborsOnEndMove`](#damageneighborsonendmove) | Block | Combat Trigger: Deals damage to neighbors on end move. |
| `DamageOrHealConditionally` | Integer | Applies or references the 'DamageOrHealConditionally' effect/state. |
| [`DamageReductionAura`](#damagereductionaura) | Block | Combat Trigger: Deals damage to reduction aura. |
| `DamageUp` | Integer | Applies or references the 'DamageUp' effect/state. |
| [`DeadAltAbility`](./Enums.md#enum-deadaltability) | Enum | Applies or references the 'DeadAltAbility' effect/state. |
| `DeathChill` | Integer | Applies the 'DeathChill' effect. |
| [`DeathRattle`](./Enums.md#enum-deathrattle) | Enum | Event Trigger: Executes logic or abilities exactly when the character dies. |
| [`DeathRattleRevive`](#deathrattlerevive) | Block | Event Trigger: Revives the character immediately upon death. |
| `DebuffImmunity` | Integer | Applies or references the 'DebuffImmunity' effect/state. |
| `DejaVu` | Integer | Applies the 'DejaVu' effect. |
| [`DelayedAutoRevive`](#delayedautorevive) | Block | Applies or references the 'DelayedAutoRevive' effect/state. |
| `DelayedPain` | Integer | Applies or references the 'DelayedPain' effect/state. |
| `DemonicGlyphFrames` | Integer | Applies or references the 'DemonicGlyphFrames' effect/state. |
| `DemonicGlyphStealer` | Integer | Applies or references the 'DemonicGlyphStealer' effect/state. |
| [`DepressionAura`](#depressionaura) | Block |  |
| [`DestroyEquipmentAndAttachParasite`](#destroyequipmentandattachparasite) | Block | Removes an equipped item and replaces it with a parasite from a specified pool. |
| `DestroyTrinket` | Integer | Applies or references the 'DestroyTrinket' effect/state. |
| `DexterityUp` | Integer | Applies or references the 'DexterityUp' effect/state. |
| [`Diabetes`](#diabetes) | Block | Applies the 'Diabetes' effect. |
| [`DiceBehavior`](#dicebehavior) | Block | AI Logic: Custom behavior for Dice enemies. |
| [`DicerArt`](./Arrays.md#array-dicerart) | Array | Applies or references the 'DicerArt' effect/state. |
| `DieWhenOnlyGolemsLeft` | Integer | Applies or references the 'DieWhenOnlyGolemsLeft' effect/state. |
| `DieWhenSpawnerDies` | Integer | Applies or references the 'DieWhenSpawnerDies' effect/state. |
| [`DiesToElement`](./Enums.md#enum-diestoelement) | Enum | Vulnerability: Character dies instantly if hit by this element. |
| [`DiesToPiercingAndSpikes`](#diestopiercingandspikes) | Block | Vulnerability: Character dies instantly if hit by piercing attacks or spikes. |
| [`DigestDeadBodies`](./Enums.md#enum-digestdeadbodies) | Enum | Applies or references the 'DigestDeadBodies' effect/state. |
| `DiminishingHealthRegen` | Integer | Applies or references the 'DiminishingHealthRegen' effect/state. |
| `DirtyClaws` | Integer | Applies the 'DirtyClaws' effect. |
| [`DisableAbilities`](./Enums.md#enum-disableabilities) | Enum | Applies or references the 'DisableAbilities' effect/state. |
| [`DisableAbilitiesWithTag`](./Enums.md#enum-disableabilitieswithtag) | Enum |  |
| `DisablePassiveSlot` | Integer | Applies or references the 'DisablePassiveSlot' effect/state. |
| `DisableSpells` | Integer | Applies or references the 'DisableSpells' effect/state. |
| `Disguised` | Integer | Applies or references the 'Disguised' effect/state. |
| [`DisguisedTrapper`](./Enums.md#enum-disguisedtrapper) | Enum | Applies or references the 'DisguisedTrapper' effect/state. |
| `DisplayBuddyCatOnSpawn` | Integer | Applies or references the 'DisplayBuddyCatOnSpawn' effect/state. |
| [`DisplayDangerAOE`](./Enums.md#enum-displaydangeraoe) | Enum | Applies or references the 'DisplayDangerAOE' effect/state. |
| `DissuadeInstakills` | Integer | Applies or references the 'DissuadeInstakills' effect/state. |
| [`DistanceBonusDamage`](#distancebonusdamage) | Block | Applies the 'DistanceBonusDamage' effect. |
| [`Divide4OnDeath`](./Enums.md#enum-divide4ondeath) | Enum | Applies or references the 'Divide4OnDeath' effect/state. |
| `DivineShield` | Integer | Applies or references the 'DivineShield' effect/state. |
| `DivineShieldPickup` | Integer | Applies or references the 'DivineShieldPickup' effect/state. |
| [`DoDamage`](#dodamage) | Block | Explicitly triggers a secondary damage instance independent of the main attack. |
| `DodgeChance` | Integer |  |
| `DodgeChanceWithBlindSpot` | Integer | Applies or references the 'DodgeChanceWithBlindSpot' effect/state. |
| `DodgeChance_Status` | Integer | Applies or references the 'DodgeChance_Status' effect/state. |
| [`DodgeWhenTargeted`](#dodgewhentargeted) | Block | Reaction: Executes a dodge maneuver when targeted. |
| `Doomed` | Integer | Applies the 'Doomed' effect. |
| `DoubleCastSpellIfManaCostUnderThreshold` | Integer | Applies or references the 'DoubleCastSpellIfManaCostUnderThreshold' effect/state. |
| `DoubleCastSpellThisTurn` | Integer | Applies or references the 'DoubleCastSpellThisTurn' effect/state. |
| `DoubleCastSpellsEachTurn_Status` | Integer |  |
| [`DoubleCastTaggedSpells`](./Enums.md#enum-doublecasttaggedspells) | Enum | Applies or references the 'DoubleCastTaggedSpells' effect/state. |
| `DoubleCastWeapons` | Integer | Applies the 'DoubleCastWeapons' effect. |
| `DoubleReceivedNegativeStatus` | Integer | Applies or references the 'DoubleReceivedNegativeStatus' effect/state. |
| `DoubleReceivedPositiveStatus` | Integer | Applies or references the 'DoubleReceivedPositiveStatus' effect/state. |
| `DownRankAIIfWeaponUsable` | Float | Applies or references the 'DownRankAIIfWeaponUsable' effect/state. |
| `DrinkWater` | Integer | Applies or references the 'DrinkWater' effect/state. |
| [`DropAsFamiliarOnArmorBreak`](./Enums.md#enum-dropasfamiliaronarmorbreak) | Enum | Applies or references the 'DropAsFamiliarOnArmorBreak' effect/state. |
| [`DropAsFamiliarOnTookDamage`](./Enums.md#enum-dropasfamiliarontookdamage) | Enum | Applies or references the 'DropAsFamiliarOnTookDamage' effect/state. |
| [`DropSoulJarOnDeath`](./Enums.md#enum-dropsouljarondeath) | Enum | Applies or references the 'DropSoulJarOnDeath' effect/state. |
| `Drowsy` | Integer |  |
| `DukeOfFlies` | Integer | Applies the 'DukeOfFlies' effect. |
| [`DurabilityTransform`](#durabilitytransform) | Block | Applies or references the 'DurabilityTransform' effect/state. |
| `DustCloudBehavior` | Integer | Applies or references the 'DustCloudBehavior' effect/state. |
| `Dybbuk1HPTracker` | Integer | Applies or references the 'Dybbuk1HPTracker' effect/state. |
| [`DybbukPossessionFallback`](#dybbukpossessionfallback) | Block | Logic: Fallback state when a Dybbuk possession fails. |
| [`Dyslexia`](./Arrays.md#array-dyslexia) | Array | Applies the 'Dyslexia' effect. |
| [`EMP`](#emp) | Block | Applies the 'EMP' effect. |
| `EachSpellFreeAtFullMana` | Integer | Applies the 'EachSpellFreeAtFullMana' effect. |
| `ElectricArcs` | Integer | Applies or references the 'ElectricArcs' effect/state. |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum | Applies or references the 'ElementImmune' effect/state. |
| [`ElementWeakness`](./Enums.md#enum-elementweakness) | Enum | Applies or references the 'ElementWeakness' effect/state. |
| [`ElementalAttunement`](#elementalattunement) | Block | Applies the 'ElementalAttunement' effect. |
| [`ElementalManaCostReduction`](#elementalmanacostreduction) | Block | Applies the 'ElementalManaCostReduction' effect. |
| [`EliteFlatTint`](./Arrays.md#array-eliteflattint) | Array |  |
| [`EliteParticle`](./Enums.md#enum-eliteparticle) | Enum |  |
| [`EliteTint`](./Arrays.md#array-elitetint) | Array |  |
| [`Else`](#else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |
| `Empath` | Integer | Applies the 'Empath' effect. |
| `EmptyMana` | Integer | Applies the 'EmptyMana' effect. |
| `EnemiesGetPickupsKnockedOut` | Integer | Applies the 'EnemiesGetPickupsKnockedOut' effect. |
| `EnergyStorm` | Integer | Applies the 'EnergyStorm' effect. |
| `EnrageOnDamage` | Integer | Applies or references the 'EnrageOnDamage' effect/state. |
| [`EquipPermanentItem`](./Enums.md#enum-equippermanentitem) | Enum | Applies the 'EquipPermanentItem' effect. |
| [`EquipRandomTemporaryItemFromPool`](./Enums.md#enum-equiprandomtemporaryitemfrompool) | Enum |  |
| [`EquipTemporaryItem`](./Enums.md#enum-equiptemporaryitem) | Enum | Applies the 'EquipTemporaryItem' effect. |
| `EquipmentPassiveMultiplierBonus` | Integer | Applies the 'EquipmentPassiveMultiplierBonus' effect. |
| `EquipmentSetBonusBonus` | Integer | Applies the 'EquipmentSetBonusBonus' effect. |
| `EraseSpawnCoins` | Integer | Applies or references the 'EraseSpawnCoins' effect/state. |
| [`EscapeSequence`](#escapesequence) | Block | Applies the 'EscapeSequence' effect. |
| [`Eternal`](#eternal) | Block | Applies the 'Eternal' effect. |
| `EventBounterHunterPassive` | Integer | Applies or references the 'EventBounterHunterPassive' effect/state. |
| [`ExcludeFromEvents`](./Enums.md#enum-excludefromevents) | Enum | Applies or references the 'ExcludeFromEvents' effect/state. |
| `ExhaustionRoundChange` | Integer | Applies the 'ExhaustionRoundChange' effect. |
| `ExpireOnSpawnerTurnEnd` | Integer | Applies or references the 'ExpireOnSpawnerTurnEnd' effect/state. |
| `ExplodeOverkilledEnemies` | Integer | Applies the 'ExplodeOverkilledEnemies' effect. |
| `ExplosionImmunity` | Integer | Applies or references the 'ExplosionImmunity' effect/state. |
| `ExtraBasicAttacks` | Integer | Applies the 'ExtraBasicAttacks' effect. |
| `ExtraBasicAttacks_Status` | Integer | Applies or references the 'ExtraBasicAttacks_Status' effect/state. |
| `ExtraBasicMoves_Status` | Integer | Applies or references the 'ExtraBasicMoves_Status' effect/state. |
| `ExtraDispersedTurns` | Integer | Applies or references the 'ExtraDispersedTurns' effect/state. |
| `ExtraInjuryOnDeath` | Integer | Applies the 'ExtraInjuryOnDeath' effect. |
| `ExtraMovePoints` | Integer | Applies the 'ExtraMovePoints' effect. |
| [`ExtraStatusWhenDealingDamage`](#extrastatuswhendealingdamage) | Block | Applies or references the 'ExtraStatusWhenDealingDamage' effect/state. |
| `ExtraTrinketUses` | Integer | Applies or references the 'ExtraTrinketUses' effect/state. |
| [`ExtraTurnsPerTaggedUnit`](./Enums.md#enum-extraturnspertaggedunit) | Enum | Applies or references the 'ExtraTurnsPerTaggedUnit' effect/state. |
| `ExtraWeaponAttacks` | Integer | Applies the 'ExtraWeaponAttacks' effect. |
| `FaceArmorPassiveMultiplierBonus` | Integer | Applies or references the 'FaceArmorPassiveMultiplierBonus' effect/state. |
| `FaceAway` | Integer | Applies the 'FaceAway' effect. |
| [`FaceAwayLastDamage`](#faceawaylastdamage) | Block | Reaction: Forces the character to face away from the last damage source. |
| `FaceLastDamage` | Integer | Reaction: Forces the character to face towards the last damage source. |
| `FaceShield` | Integer | Applies or references the 'FaceShield' effect/state. |
| `FadeInsteadOfDie` | Integer | Applies or references the 'FadeInsteadOfDie' effect/state. |
| [`FamiliarBonusAbility`](./Enums.md#enum-familiarbonusability) | Enum | Applies the 'FamiliarBonusAbility' effect. |
| `FamiliarSecondaryDamageImmunity` | Integer | Applies the 'FamiliarSecondaryDamageImmunity' effect. |
| `Fear` | Integer | Applies or references the 'Fear' effect/state. |
| `Fights` | Integer | Applies or references the 'Fights' effect/state. |
| [`FillMana`](./Arrays.md#array-fillmana) | Array | Applies the 'FillMana' effect. |
| [`FinalBossBeamQueue`](#finalbossbeamqueue) | Block | Boss Logic: Attack queue for the final boss beam. |
| [`FinalBossBecomeTheChild`](#finalbossbecomethechild) | Block | Boss Logic: Phase transition for the final boss. |
| [`FinalBossHitCountdownBoris`](#finalbosshitcountdownboris) | Block | Boss Logic: Countdown trigger for Boris. |
| [`FinalBossHitCountdownExplosive`](#finalbosshitcountdownexplosive) | Block | Boss Logic: Countdown trigger for explosives. |
| [`FinalBossHitCountdownHoly`](#finalbosshitcountdownholy) | Block | Boss Logic: Countdown trigger for holy attacks. |
| [`FinalBossPupils`](#finalbosspupils) | Block | Boss Logic: Pupil state management. |
| [`FinalBossShield`](./Enums.md#enum-finalbossshield) | Enum | Applies or references the 'FinalBossShield' effect/state. |
| [`FinalBossShieldHealth`](#finalbossshieldhealth) | Block | Boss Logic: Shield health management. |
| [`FinalBossSyncAnimations`](#finalbosssyncanimations) | Block | Boss Logic: Synchronizes multi-part boss animations. |
| [`FindExtraItemFromPoolOnBattleEnd`](./Enums.md#enum-findextraitemfrompoolonbattleend) | Enum | Applies or references the 'FindExtraItemFromPoolOnBattleEnd' effect/state. |
| [`FindItem`](./Enums.md#enum-finditem) | Enum | Applies or references the 'FindItem' effect/state. |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Enum | Generates an item drop from the specified loot pool. |
| `FistOfFateUniqueEnemyTracker` | Integer | Applies or references the 'FistOfFateUniqueEnemyTracker' effect/state. |
| `Flammable` | Integer | Applies or references the 'Flammable' effect/state. |
| `FlatHealWhenDealDamage` | Integer |  |
| `FlatLeech` | Integer |  |
| `FlingObjectsOnTop` | Integer | Applies or references the 'FlingObjectsOnTop' effect/state. |
| `FlippedFacingForceAttack` | Integer | Applies the 'FlippedFacingForceAttack' effect. |
| `FlowerPowerAuraBrace` | Integer | Applies the 'FlowerPowerAuraBrace' effect. |
| `FlowerPowerAuraStrength` | Integer | Applies the 'FlowerPowerAuraStrength' effect. |
| `FlowersOnEndTurn` | Integer | Applies or references the 'FlowersOnEndTurn' effect/state. |
| [`FlushmasterCelebration`](./Enums.md#enum-flushmastercelebration) | Enum | Applies or references the 'FlushmasterCelebration' effect/state. |
| `FlyDamageIncrease` | Integer | Applies the 'FlyDamageIncrease' effect. |
| `Flying` | Integer | Applies or references the 'Flying' effect/state. |
| [`FollowUp`](./Enums.md#enum-followup) | Enum | Applies the 'FollowUp' effect. |
| `ForceAttack` | Integer | Forces the character to execute an immediate attack. |
| `ForceDodgeEverything` | Integer | Applies or references the 'ForceDodgeEverything' effect/state. |
| [`ForceSpecificInjury`](./Enums.md#enum-forcespecificinjury) | Enum | Applies the 'ForceSpecificInjury' effect. |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | Applies or references the 'ForceUseAbility' effect/state. |
| [`ForceUseAbilityOnTarget`](#forceuseabilityontarget) | Block | Applies or references the 'ForceUseAbilityOnTarget' effect/state. |
| [`FormChange`](#formchange) | Block | Transforms the character into a different state or form (e.g., Rage, HasCat). |
| [`FormChangeDuringWeatherElement`](#formchangeduringweatherelement) | Block | Logic: Changes form automatically during specific weather conditions. |
| [`FormChangeHealthThreshold`](#formchangehealththreshold) | Block | Logic: Changes form when health crosses a threshold. |
| [`FormChangeOffMap`](#formchangeoffmap) | Block | Logic: Changes form when pushed off the map. |
| [`FormChangeOnElementInfluence`](#formchangeonelementinfluence) | Block | Logic: Changes form when affected by an element. |
| [`FormChangeWhenBuddyDies`](./Enums.md#enum-formchangewhenbuddydies) | Enum | Applies or references the 'FormChangeWhenBuddyDies' effect/state. |
| [`FormChangeWhileHasStatus`](#formchangewhilehasstatus) | Block | Logic: Changes form automatically while possessing a specific status. |
| [`FormChangeWhilePrimingAbility`](#formchangewhileprimingability) | Block | Logic: Changes form while preparing/priming a specific ability. |
| [`FormChanger`](#formchanger) | Block | AI Role: Designates the character as one that frequently shifts forms. |
| `Fragile` | Integer | Applies or references the 'Fragile' effect/state. |
| [`FragileDuringElement`](./Enums.md#enum-fragileduringelement) | Enum | Applies or references the 'FragileDuringElement' effect/state. |
| `FrankBolts` | Integer | Applies or references the 'FrankBolts' effect/state. |
| `FreeFirstCast` | Integer | Applies or references the 'FreeFirstCast' effect/state. |
| `FreeFirstCastAndAfterSpendMana` | Integer | Applies or references the 'FreeFirstCastAndAfterSpendMana' effect/state. |
| `FreeFirstCastEachMatch` | Integer | Applies or references the 'FreeFirstCastEachMatch' effect/state. |
| [`FreePathfindElement`](./Enums.md#enum-freepathfindelement) | Enum | Applies the 'FreePathfindElement' effect. |
| `FreeSpellsAtFullMana` | Integer | Applies the 'FreeSpellsAtFullMana' effect. |
| `Freeze` | Integer | Applies the 'Freeze' effect. |
| `FreezePiercing` | Integer | Applies the 'FreezePiercing' effect. |
| `FrontstabBasicAttackCritChance` | Integer | Applies the 'FrontstabBasicAttackCritChance' effect. |
| `FrontstabCritChance` | Integer | Applies the 'FrontstabCritChance' effect. |
| `FullBlockEverything` | Integer | Applies or references the 'FullBlockEverything' effect/state. |
| `FullBlockEverythingTo0Damage` | Integer | Applies or references the 'FullBlockEverythingTo0Damage' effect/state. |
| `FullHeal` | Integer | Applies the 'FullHeal' effect. |
| `FullHealthAllStatsUp` | Integer | Applies the 'FullHealthAllStatsUp' effect. |
| `FullHealthCritChance` | Integer | Applies the 'FullHealthCritChance' effect. |
| `FullHealthManaRegen` | Integer | Applies the 'FullHealthManaRegen' effect. |
| `FullPower` | Integer | Applies the 'FullPower' effect. |
| [`FurnitureStats`](#furniturestats) | Block | Applies the 'FurnitureStats' effect. |
| `GainCoins` | Integer | Applies or references the 'GainCoins' effect/state. |
| [`GainCoinsRange`](#gaincoinsrange) | Block | Grants the player a randomized amount of coins within a min/max range. |
| [`GainDisorder`](./Enums.md#enum-gaindisorder) | Enum | Applies or references the 'GainDisorder' effect/state. |
| [`GainDisorderFromPool`](#gaindisorderfrompool) | Block | Logic: Applies a negative mutation/disorder from a specific pool. |
| `GainExtraShield` | Integer | Applies the 'GainExtraShield' effect. |
| `GainManaWhenAnythingDies` | Integer |  |
| `GasCanBehavior` | Integer | Applies or references the 'GasCanBehavior' effect/state. |
| `GasCloudBehavior2` | Integer | Applies or references the 'GasCloudBehavior2' effect/state. |
| `GeminiTwin` | Integer | Applies or references the 'GeminiTwin' effect/state. |
| `GlobalFamiliarDamageBoost` | Integer |  |
| `GlobalFamiliarMoveBoost` | Integer |  |
| [`GlobalFlowerTrapperAura`](#globalflowertrapperaura) | Block |  |
| `GlobalManaBurnAura` | Integer |  |
| `GlobalManaDrainAura` | Integer | Applies or references the 'GlobalManaDrainAura' effect/state. |
| [`GlobalMeleeRevengeDamage`](#globalmeleerevengedamage) | Block | Applies or references the 'GlobalMeleeRevengeDamage' effect/state. |
| `GoopImmunity` | Integer | Applies or references the 'GoopImmunity' effect/state. |
| `GoopWalk` | Integer | Applies or references the 'GoopWalk' effect/state. |
| `GrassTileHealing` | Integer | Applies the 'GrassTileHealing' effect. |
| [`GravityWell`](#gravitywell) | Block | Applies the 'GravityWell' effect. |
| [`GroundFlopper`](./Enums.md#enum-groundflopper) | Enum | Applies or references the 'GroundFlopper' effect/state. |
| `GuillotinaDeathHead` | Integer | Applies or references the 'GuillotinaDeathHead' effect/state. |
| [`HPAltStates`](#hpaltstates) | Block | Visual: Alternative sprite states based on current health. |
| `HPGainBlock` | Integer | Applies or references the 'HPGainBlock' effect/state. |
| [`HarpoonTrapPassive`](./Enums.md#enum-harpoontrappassive) | Enum | Applies or references the 'HarpoonTrapPassive' effect/state. |
| `HeadArmorPassiveMultiplierBonus` | Integer | Applies or references the 'HeadArmorPassiveMultiplierBonus' effect/state. |
| `HealAndOverhealToShield` | Integer | Applies the 'HealAndOverhealToShield' effect. |
| `HealAtStart` | Integer | Applies the 'HealAtStart' effect. |
| `HealDamagesEnemies` | Integer | Applies the 'HealDamagesEnemies' effect. |
| [`HealNeighborsEachTurn`](#healneighborseachturn) | Block | Passive: Restores health to adjacent allies at the start of the turn. |
| `HealingAura` | Integer | Applies the 'HealingAura' effect. |
| `HealsAlsoRegenMana` | Integer | Applies the 'HealsAlsoRegenMana' effect. |
| `HealsCanRevive` | Integer | Applies the 'HealsCanRevive' effect. |
| `HealthGain` | Integer | Applies or references the 'HealthGain' effect/state. |
| `HealthMultiplier` | Float |  |
| [`HealthPickup`](#healthpickup) | Block | Pickup Logic: Defines what happens when a health item is collected. |
| `HealthRegenUp` | Integer | Applies or references the 'HealthRegenUp' effect/state. |
| `Hex` | Integer | Applies or references the 'Hex' effect/state. |
| `HiddenDoomed` | Integer | Applies or references the 'HiddenDoomed' effect/state. |
| [`HideEquipment`](./Enums.md#enum-hideequipment) | Enum | Applies or references the 'HideEquipment' effect/state. |
| `HideSomeHudStuff` | Integer | Applies or references the 'HideSomeHudStuff' effect/state. |
| [`HitlerExecute`](#hitlerexecute) | Block | Boss Logic: Specific execution or ultimate attack state. |
| `HolyDamageMultiplierBonus` | Integer | Applies the 'HolyDamageMultiplierBonus' effect. |
| `HolyShieldTransferToSpawner` | Integer | Applies the 'HolyShieldTransferToSpawner' effect. |
| [`HolyShieldTransferToTaggedMinions`](./Enums.md#enum-holyshieldtransfertotaggedminions) | Enum | Applies the 'HolyShieldTransferToTaggedMinions' effect. |
| `HouseFoodRequirementMultiplier` | Integer |  |
| `Hypomania` | Integer | Applies the 'Hypomania' effect. |
| `IceBlockBehavior` | Integer | Applies or references the 'IceBlockBehavior' effect/state. |
| `IgnoreTiles` | Integer |  |
| `IllusionTint` | Integer | Applies or references the 'IllusionTint' effect/state. |
| [`ImmediateAbilityReaction`](./Enums.md#enum-immediateabilityreaction) | Enum | Reaction: Executes an ability instantly, interrupting the current sequence. |
| [`ImmediateUseAbility`](./Enums.md#enum-immediateuseability) | Enum | Applies or references the 'ImmediateUseAbility' effect/state. |
| `Immobile` | Integer | Applies the 'Immobile' effect. |
| `ImmobilePassive` | Integer | Applies or references the 'ImmobilePassive' effect/state. |
| `ImmortalLeeches` | Integer | Applies the 'ImmortalLeeches' effect. |
| [`IncAuxCounterClamped`](#incauxcounterclamped) | Block | Increments a generic auxiliary counter on the character, capped by a maximum value. |
| `IncreaseExplosionDamage` | Integer | Applies the 'IncreaseExplosionDamage' effect. |
| `IncreaseExplosionSize` | Integer | Applies or references the 'IncreaseExplosionSize' effect/state. |
| `IncreaseHealingSpellRange` | Integer | Applies the 'IncreaseHealingSpellRange' effect. |
| `IncreaseItemUsesOnEquip` | Integer | Applies the 'IncreaseItemUsesOnEquip' effect. |
| `IncreaseSpellRange` | Integer | Applies or references the 'IncreaseSpellRange' effect/state. |
| `Infested` | Integer | Applies or references the 'Infested' effect/state. |
| [`InfiniteRebirth`](#infiniterebirth) | Block | Applies the 'InfiniteRebirth' effect. |
| `InheritSpawnerStats` | Integer | Applies or references the 'InheritSpawnerStats' effect/state. |
| `InjuryImmunity` | Integer | Applies or references the 'InjuryImmunity' effect/state. |
| [`InnateElement`](./Enums.md#enum-innateelement) | Enum | Applies the 'InnateElement' effect. |
| `InsertIntoBackgroundPlaceholder` | Integer | Applies or references the 'InsertIntoBackgroundPlaceholder' effect/state. |
| [`Instakill`](./Arrays.md#array-instakill) | Array |  |
| `IntelligenceUp` | Integer | Applies or references the 'IntelligenceUp' effect/state. |
| `InterchangeDisabler` | Integer | Applies or references the 'InterchangeDisabler' effect/state. |
| `InvertBrainFaction` | Integer | Applies the 'InvertBrainFaction' effect. |
| [`ItemAuxTransform`](#itemauxtransform) | Block | Applies or references the 'ItemAuxTransform' effect/state. |
| `JesterLevelUpRerolls` | Integer | Applies or references the 'JesterLevelUpRerolls' effect/state. |
| [`JohnnyNeedsWashing`](#johnnyneedswashing) | Block | Character Form: Behavior and stats for the 'JohnnyNeedsWashing' state. |
| [`JohnnyWasher`](./Enums.md#enum-johnnywasher) | Enum | Applies or references the 'JohnnyWasher' effect/state. |
| `KaijuKnockbackImmune` | Integer | Applies or references the 'KaijuKnockbackImmune' effect/state. |
| [`KaijuWinCon`](./Enums.md#enum-kaijuwincon) | Enum | Applies or references the 'KaijuWinCon' effect/state. |
| `KillsHeal` | Integer | Applies the 'KillsHeal' effect. |
| [`KillsToMeat`](./Enums.md#enum-killstomeat) | Enum | Applies or references the 'KillsToMeat' effect/state. |
| `KineticSpikes` | Integer | Applies or references the 'KineticSpikes' effect/state. |
| `KnockOutCoin` | Integer | Forces the target to drop coins. |
| [`KnockUpAndAway`](#knockupandaway) | Block |  |
| `Knockback` | Integer | Applies or references the 'Knockback' effect/state. |
| [`KnockbackIfCrit`](#knockbackifcrit) | Block | Applies or references the 'KnockbackIfCrit' effect/state. |
| `KnockbackImmunity` | Integer | Applies the 'KnockbackImmunity' effect. |
| [`LateBloomer`](#latebloomer) | Block | Applies the 'LateBloomer' effect. |
| [`LeaveBehindOnceEachMove`](./Enums.md#enum-leavebehindonceeachmove) | Enum | Applies or references the 'LeaveBehindOnceEachMove' effect/state. |
| `LeaveBehindRockOnKnockback` | Integer | Applies the 'LeaveBehindRockOnKnockback' effect. |
| `Leech` | Integer | Applies the 'Leech' effect. |
| `LeechPercent` | Integer | Applies the 'LeechPercent' effect. |
| `Leeches` | Integer |  |
| [`LegacySpawnSavedCatIfExists`](./Enums.md#enum-legacyspawnsavedcatifexists) | Enum | Applies or references the 'LegacySpawnSavedCatIfExists' effect/state. |
| [`LevelUpClassOverride`](./Enums.md#enum-levelupclassoverride) | Enum | Applies the 'LevelUpClassOverride' effect. |
| `Lifesteal` | Integer | Applies or references the 'Lifesteal' effect/state. |
| `LightningAspectCharge` | Integer | Applies the 'LightningAspectCharge' effect. |
| [`LightningRod`](#lightningrod) | Block | Applies the 'LightningRod' effect. |
| `LimitDamage` | Integer | Applies or references the 'LimitDamage' effect/state. |
| `LimitHeal` | Integer | Applies or references the 'LimitHeal' effect/state. |
| `LimitSelfKnockbackDamage` | Integer | Applies the 'LimitSelfKnockbackDamage' effect. |
| [`LimitedTileTrail`](./Enums.md#enum-limitedtiletrail) | Enum | Applies the 'LimitedTileTrail' effect. |
| `LineOfSightTrueSightAura` | Float | Applies the 'LineOfSightTrueSightAura' effect. |
| `LobbedHook` | Integer | Applies the 'LobbedHook' effect. |
| [`LockOrientationFaceTile`](./Arrays.md#array-lockorientationfacetile) | Array | Applies or references the 'LockOrientationFaceTile' effect/state. |
| [`LoopingSoundWhileAlive`](./Enums.md#enum-loopingsoundwhilealive) | Enum | Applies or references the 'LoopingSoundWhileAlive' effect/state. |
| [`LowHealthAllyDodgeChanceAura`](#lowhealthallydodgechanceaura) | Block | Applies the 'LowHealthAllyDodgeChanceAura' effect. |
| `LuckUp` | Integer | Applies or references the 'LuckUp' effect/state. |
| `Madness` | Integer | Applies the Madness debuff/status effect. |
| `MagicDamageImmune` | Integer | Applies or references the 'MagicDamageImmune' effect/state. |
| `MagicWeakness` | Integer | Applies or references the 'MagicWeakness' effect/state. |
| `MakeBasicAttackPassThroughThings` | Integer | Applies the 'MakeBasicAttackPassThroughThings' effect. |
| `MakeBasicAttackPull` | Integer |  |
| `MakeSpellsRequireCharge` | Integer | Applies the 'MakeSpellsRequireCharge' effect. |
| `MamaCatAnimations` | Integer | Applies or references the 'MamaCatAnimations' effect/state. |
| `ManaCostReduction` | Integer | Applies or references the 'ManaCostReduction' effect/state. |
| [`ManaCostReductionTagged`](#manacostreductiontagged) | Block | Applies the 'ManaCostReductionTagged' effect. |
| [`ManaGain`](./Math_Equations.md) | Equation | Applies or references the 'ManaGain' effect/state. |
| [`ManaGainRange`](#managainrange) | Block | Applies or references the 'ManaGainRange' effect/state. |
| `ManaLeeches` | Integer | Applies or references the 'ManaLeeches' effect/state. |
| [`ManaPickup`](#manapickup) | Block | Pickup Logic: Defines what happens when a mana item is collected. |
| `ManaRegenMultiplierIfManaEmpty` | Integer | Applies the 'ManaRegenMultiplierIfManaEmpty' effect. |
| [`ManglerMonsterPassive`](./Enums.md#enum-manglermonsterpassive) | Enum | Applies or references the 'ManglerMonsterPassive' effect/state. |
| `Marked` | Integer | Applies or references the 'Marked' effect/state. |
| `MaxAccuracy` | Integer | Applies the 'MaxAccuracy' effect. |
| `MaxStartingMana` | Integer | Applies the 'MaxStartingMana' effect. |
| [`MegaDinoDropController`](#megadinodropcontroller) | Block | Boss Logic: Manages loot drops for the Mega Dino. |
| `MegaMinions` | Integer | Applies the 'MegaMinions' effect. |
| [`MeleeRevengeDamage`](#meleerevengedamage) | Block | Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack. |
| `Metal` | Integer | Applies or references the 'Metal' effect/state. |
| `MetalDetector` | Integer | Applies the 'MetalDetector' effect. |
| `MimicSpawnerAttacks` | Integer | Applies or references the 'MimicSpawnerAttacks' effect/state. |
| [`MiniVolcanoReaction`](./Enums.md#enum-minivolcanoreaction) | Enum | Applies or references the 'MiniVolcanoReaction' effect/state. |
| `MinimumKnockbackFromAllDamage` | Integer | Applies or references the 'MinimumKnockbackFromAllDamage' effect/state. |
| `MinimumKnockbackFromPhysicalAttacks` | Integer | Applies or references the 'MinimumKnockbackFromPhysicalAttacks' effect/state. |
| `MinimumTech` | Integer | Applies the 'MinimumTech' effect. |
| `MissChance` | Integer | Applies the 'MissChance' effect. |
| `ModelingClayPassive` | Integer | Applies or references the 'ModelingClayPassive' effect/state. |
| [`ModifyAbility`](#modifyability) | Block | Applies or references the 'ModifyAbility' effect/state. |
| [`ModularPickup`](#modularpickup) | Block | Pickup Logic: Defines what happens when a modular item is collected. |
| [`MonkCatReactionAbilities`](#monkcatreactionabilities) | Block | Reaction: Specific counter-attack or dodge abilities used by the Monk class. |
| [`MoonHeadCrackedVisual`](./Enums.md#enum-moonheadcrackedvisual) | Enum | Applies or references the 'MoonHeadCrackedVisual' effect/state. |
| `MoonHeadFinisherEnabler` | Integer | Applies or references the 'MoonHeadFinisherEnabler' effect/state. |
| [`MotherGrowController`](#mothergrowcontroller) | Block | Boss Logic: Manages the growth phases of the Mother boss. |
| [`MotherTumorPassive`](#mothertumorpassive) | Block | Boss Logic: Passive effects applied to the Mother's tumors. |
| [`MotherTumorSpawnInCapture`](#mothertumorspawnincapture) | Block | Boss Logic: Logic for capturing entities inside the Mother's tumors upon spawning. |
| [`Mount`](#mount) | Block | Character Form: Behavior and stats for the 'Mount' state. |
| [`MoveAfterAnyAttemptedAttack`](#moveafteranyattemptedattack) | Block | AI Movement: Forces a move action immediately after attacking, even if it missed. |
| [`MoveAndUseAbilityEachTurnBeginIfPossible`](./Enums.md#enum-moveanduseabilityeachturnbeginifpossible) | Enum | Applies the 'MoveAndUseAbilityEachTurnBeginIfPossible' effect. |
| [`MoveAwayFromDamageSource`](./Enums.md#enum-moveawayfromdamagesource) | Enum |  |
| [`MoveAwayWhenEnemyAdjacent`](#moveawaywhenenemyadjacent) | Block | AI Movement: Moves away if an enemy enters an adjacent tile. |
| `MoveQuivered` | Integer | Applies the 'MoveQuivered' effect. |
| `MoveRandomly` | Integer | Applies the 'MoveRandomly' effect. |
| `MoveSpeedMultiplier` | Float | Applies or references the 'MoveSpeedMultiplier' effect/state. |
| [`MoveTowardsDamageSource`](./Enums.md#enum-movetowardsdamagesource) | Enum | AI Movement: Closes distance on the last source of damage. |
| [`MoveTowardsKillers`](./Enums.md#enum-movetowardskillers) | Enum | AI Movement: Seeks out entities that have recently killed an ally. |
| [`MoveWhenDamaged`](./Enums.md#enum-movewhendamaged) | Enum | AI Movement: Forces a reposition when taking damage. |
| [`MovementReaction`](#movementreaction) | Block | Reaction: Triggers an effect or ability when forced to move. |
| `MovementUp` | Integer | Applies the 'MovementUp' effect. |
| [`MultiSpawnOnDeath`](#multispawnondeath) | Block | Event Trigger: Spawns multiple entities upon death. |
| `MulticatHeads` | Integer | Applies or references the 'MulticatHeads' effect/state. |
| [`MulticlassLevelUp`](./Enums.md#enum-multiclasslevelup) | Enum | Applies the 'MulticlassLevelUp' effect. |
| `MultiplyCoinsOnBattleStart` | Integer | Applies or references the 'MultiplyCoinsOnBattleStart' effect/state. |
| `MultiplyReceivedHealing` | Integer | Applies or references the 'MultiplyReceivedHealing' effect/state. |
| `MutateAfterXTurns` | Integer | Applies or references the 'MutateAfterXTurns' effect/state. |
| [`MutateViaAbility`](./Enums.md#enum-mutateviaability) | Enum | Applies or references the 'MutateViaAbility' effect/state. |
| `MuteDemonicGlyphDisplay` | Integer | Applies or references the 'MuteDemonicGlyphDisplay' effect/state. |
| `NeckArmorPassiveMultiplierBonus` | Integer | Applies or references the 'NeckArmorPassiveMultiplierBonus' effect/state. |
| [`NextBattleStatus`](#nextbattlestatus) | Block | Applies the 'NextBattleStatus' effect. |
| `NoHealthOnlyShield` | Integer | Applies or references the 'NoHealthOnlyShield' effect/state. |
| `NoHealthRegen` | Integer | Applies or references the 'NoHealthRegen' effect/state. |
| `NoManaRegen` | Integer | Applies the 'NoManaRegen' effect. |
| `NoReflection` | Integer | Applies the 'NoReflection' effect. |
| `NonLethal` | Integer | Applies the 'NonLethal' effect. |
| `NonStackingDivineShield` | Integer | Applies the 'NonStackingDivineShield' effect. |
| `NonStackingShield` | Integer |  |
| `NubbyTossPriority` | Integer | Applies the 'NubbyTossPriority' effect. |
| [`NukeQuestFinalBossModifications`](#nukequestfinalbossmodifications) | Block | Special encounter trigger for the Nuke Quest ending. |
| `NumbingLeeches` | Integer | Applies the 'NumbingLeeches' effect. |
| [`ObjectDetector`](#objectdetector) | Block | Applies or references the 'ObjectDetector' effect/state. |
| [`ObjectOnHitCharacter`](./Enums.md#enum-objectonhitcharacter) | Enum | Spawns a specific character or entity upon impact. |
| `OneUseSpellDamageUp` | Integer | Applies the 'OneUseSpellDamageUp' effect. |
| `OrthogonalAIDangerZone` | Integer | Applies or references the 'OrthogonalAIDangerZone' effect/state. |
| `Ostracized` | Integer | Applies or references the 'Ostracized' effect/state. |
| `OverManaReducesManaCosts` | Integer |  |
| `OverhealGainsBothShield` | Integer | Applies the 'OverhealGainsBothShield' effect. |
| [`OverrideBasicAttack`](./Enums.md#enum-overridebasicattack) | Enum | Applies or references the 'OverrideBasicAttack' effect/state. |
| `OverrideChainKnockback` | Integer | Applies or references the 'OverrideChainKnockback' effect/state. |
| `OverrideChainKnockbackDamage` | Integer | Applies the 'OverrideChainKnockbackDamage' effect. |
| `OverrideMaxHealth` | Integer | Applies or references the 'OverrideMaxHealth' effect/state. |
| `OverrideMaxMana` | Integer | Applies the 'OverrideMaxMana' effect. |
| `OverridePalette` | Integer | Applies the 'OverridePalette' effect. |
| `PackHunting` | Integer | Applies or references the 'PackHunting' effect/state. |
| [`Paranoia`](./Enums.md#enum-paranoia) | Enum | Applies the 'Paranoia' effect. |
| `ParasitesArentCursed` | Integer | Applies the 'ParasitesArentCursed' effect. |
| `PartialCleanse` | Integer | Applies or references the 'PartialCleanse' effect/state. |
| [`PassiveAfterXKills`](#passiveafterxkills) | Block | Applies or references the 'PassiveAfterXKills' effect/state. |
| [`PassiveAtFullHealth`](#passiveatfullhealth) | Block | Applies the 'PassiveAtFullHealth' effect. |
| [`PassiveAtHealthThreshold`](#passiveathealththreshold) | Block | Applies or references the 'PassiveAtHealthThreshold' effect/state. |
| [`PassiveAtInjuryThreshold`](#passiveatinjurythreshold) | Block | Applies the 'PassiveAtInjuryThreshold' effect. |
| [`PassiveAtStatThreshold`](#passiveatstatthreshold) | Block | Applies the 'PassiveAtStatThreshold' effect. |
| [`PassiveGroup`](#passivegroup) | Block | Passive: A collection of passives grouped together for easier management. |
| [`PassiveIfAllArmorEmpty`](#passiveifallarmorempty) | Block | Applies the 'PassiveIfAllArmorEmpty' effect. |
| [`PassiveIfEmptyFace`](#passiveifemptyface) | Block | Applies the 'PassiveIfEmptyFace' effect. |
| [`PassiveIfEmptyHead`](#passiveifemptyhead) | Block | Applies the 'PassiveIfEmptyHead' effect. |
| [`PassiveIfEmptyNeck`](#passiveifemptyneck) | Block | Applies the 'PassiveIfEmptyNeck' effect. |
| [`PassiveIfStrAuxEquals`](#passiveifstrauxequals) | Block | Applies or references the 'PassiveIfStrAuxEquals' effect/state. |
| [`PassiveIfWeaponIsUsable`](#passiveifweaponisusable) | Block | Applies or references the 'PassiveIfWeaponIsUsable' effect/state. |
| [`PassiveLevelScaledStatus`](#passivelevelscaledstatus) | Block | Applies the 'PassiveLevelScaledStatus' effect. |
| `PassiveLevelUpAtCombatEnd` | Integer | Applies the 'PassiveLevelUpAtCombatEnd' effect. |
| [`PassiveUntilCastSpell`](#passiveuntilcastspell) | Block | Applies the 'PassiveUntilCastSpell' effect. |
| [`PassiveUntilGetKill`](#passiveuntilgetkill) | Block | Applies the 'PassiveUntilGetKill' effect. |
| [`PassiveWhenAffectedByElement`](#passivewhenaffectedbyelement) | Block |  |
| [`PassiveWhenAtFullMana`](#passivewhenatfullmana) | Block | State Trigger: Grants nested passives when at full mana. |
| [`PassiveWhenDead`](#passivewhendead) | Block | State Trigger: Grants passives when this condition is met. |
| [`PassiveWhenOnTile`](#passivewhenontile) | Block | State Trigger: Grants passives when this condition is met. |
| [`PassiveWhenTheAlpha`](#passivewhenthealpha) | Block | State Trigger: Grants nested passives when the alpha. |
| [`PassiveWhileHasDurability`](#passivewhilehasdurability) | Block | Applies or references the 'PassiveWhileHasDurability' effect/state. |
| [`PassiveWhileHasStatus`](#passivewhilehasstatus) | Block | Passive: Activates only while the character has the specified status. |
| [`PassiveWhileInMonkMeleeStance`](#passivewhileinmonkmeleestance) | Block | Applies the 'PassiveWhileInMonkMeleeStance' effect. |
| [`PassiveWhileInMonkRangedStance`](#passivewhileinmonkrangedstance) | Block | Applies the 'PassiveWhileInMonkRangedStance' effect. |
| [`PassiveWhileNotHasStatus`](#passivewhilenothasstatus) | Block | Passive: Activates only while the character does NOT have the specified status. |
| [`PassiveWhileNotTakingTurn`](#passivewhilenottakingturn) | Block | Grants nested passives that are only active while it is NOT the character's turn. |
| [`PassiveWhilePreviewingMonkRangedStance`](#passivewhilepreviewingmonkrangedstance) | Block | Applies the 'PassiveWhilePreviewingMonkRangedStance' effect. |
| [`PassiveWhileShielded`](#passivewhileshielded) | Block | Applies or references the 'PassiveWhileShielded' effect/state. |
| [`PassiveWhileWearingMetal`](#passivewhilewearingmetal) | Block | Applies the 'PassiveWhileWearingMetal' effect. |
| `PercentHeal` | Integer | Applies the 'PercentHeal' effect. |
| `PermanentCharisma` | Integer | Applies or references the 'PermanentCharisma' effect/state. |
| `PermanentConfusion` | Integer | Applies or references the 'PermanentConfusion' effect/state. |
| `PermanentConstitution` | Integer | Applies or references the 'PermanentConstitution' effect/state. |
| `PermanentDexterity` | Integer | Applies the 'PermanentDexterity' effect. |
| `PermanentImmobile` | Integer | Applies the 'PermanentImmobile' effect. |
| `PermanentIntelligence` | Integer | Applies or references the 'PermanentIntelligence' effect/state. |
| `PermanentItems` | Integer | Applies the 'PermanentItems' effect. |
| `PermanentKitten` | Integer | Applies the 'PermanentKitten' effect. |
| `PermanentLuck` | Integer | Applies or references the 'PermanentLuck' effect/state. |
| `PermanentMadness` | Integer | Applies or references the 'PermanentMadness' effect/state. |
| `PermanentSpeed` | Integer | Applies the 'PermanentSpeed' effect. |
| `PermanentStrength` | Integer | Applies or references the 'PermanentStrength' effect/state. |
| `Petrify` | Integer | Applies the 'Petrify' effect. |
| `Phasing` | Integer | Applies or references the 'Phasing' effect/state. |
| `PhysicalAttacksMiss` | Integer | Applies or references the 'PhysicalAttacksMiss' effect/state. |
| `Piercing` | Integer | Applies the 'Piercing' effect. |
| `Plant` | Integer | Applies or references the 'Plant' effect/state. |
| `Poison` | Integer | Applies or references the 'Poison' effect/state. |
| `PoisonLace` | Integer | Applies or references the 'PoisonLace' effect/state. |
| `PoisonMultiplier` | Integer | Applies the 'PoisonMultiplier' effect. |
| `PoisonThorns` | Integer | Applies or references the 'PoisonThorns' effect/state. |
| [`PoopWhenHit`](./Enums.md#enum-poopwhenhit) | Enum |  |
| `Possessed` | Integer | Applies or references the 'Possessed' effect/state. |
| `PreEmptiveCounterNextAttacks` | Integer | Applies or references the 'PreEmptiveCounterNextAttacks' effect/state. |
| [`PreventSpecificInjury`](./Enums.md#enum-preventspecificinjury) | Enum | Applies or references the 'PreventSpecificInjury' effect/state. |
| `PrioritizeAggroTarget` | Integer | Applies or references the 'PrioritizeAggroTarget' effect/state. |
| `PrioritizeFarAwayTargets` | Integer | Applies or references the 'PrioritizeFarAwayTargets' effect/state. |
| `PrioritizeHitDifferentTargets` | Integer | Applies or references the 'PrioritizeHitDifferentTargets' effect/state. |
| `PrioritizePlayerCats` | Integer | Applies or references the 'PrioritizePlayerCats' effect/state. |
| `PrioritizeWeakestEnemy` | Integer | Applies or references the 'PrioritizeWeakestEnemy' effect/state. |
| `ProbeCharmed` | Integer | Applies or references the 'ProbeCharmed' effect/state. |
| [`ProtectTargetedAllies`](#protecttargetedallies) | Block | AI Logic: Navigates to intercept attacks directed at allies. |
| `PullSourceToKnockbackImmuneTarget` | Integer | Applies the 'PullSourceToKnockbackImmuneTarget' effect. |
| `PullSourceToTarget` | Integer | Applies or references the 'PullSourceToTarget' effect/state. |
| `Purge` | Integer | Applies the 'Purge' effect. |
| `Quiver` | Integer | Applies the 'Quiver' effect. |
| `Quivered` | Integer | Applies or references the 'Quivered' effect/state. |
| `RandomInjury` | Integer | Applies the 'RandomInjury' effect. |
| `RandomMagicMissile` | Integer | Fires a randomized number of magic missiles. |
| `RandomMutation` | Integer | Applies or references the 'RandomMutation' effect/state. |
| [`RandomPassivePool`](#randompassivepool) | Block | Logic: Grants a random passive from the specified pool upon spawning. |
| `RandomPermanentStat` | Integer | Applies or references the 'RandomPermanentStat' effect/state. |
| [`RandomPermanentStatsDistinct`](#randompermanentstatsdistinct) | Block |  |
| [`RandomSeededStatModifier`](./Arrays.md#array-randomseededstatmodifier) | Array | Applies or references the 'RandomSeededStatModifier' effect/state. |
| `RandomStatDown` | Integer |  |
| `RandomStatUp` | Integer | Applies or references the 'RandomStatUp' effect/state. |
| [`RandomStatusFromPool`](#randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. |
| [`RandomTaggedMutation`](./Enums.md#enum-randomtaggedmutation) | Enum | Applies or references the 'RandomTaggedMutation' effect/state. |
| [`RandomizeAIWeightsEachTurn`](./Arrays.md#array-randomizeaiweightseachturn) | Array | Applies or references the 'RandomizeAIWeightsEachTurn' effect/state. |
| `RangeUp` | Integer | Applies the 'RangeUp' effect. |
| `RangedTrueShot` | Integer | Applies or references the 'RangedTrueShot' effect/state. |
| `RealTimePressure_OneUnit` | Integer | Applies the 'RealTimePressure_OneUnit' effect. |
| `Reanimate` | Integer | Applies the 'Reanimate' effect. |
| [`ReceivedStatusReplacement`](./Arrays.md#array-receivedstatusreplacement) | Array | Applies the 'ReceivedStatusReplacement' effect. |
| `ReclaimItemOnBreak` | Integer | Applies or references the 'ReclaimItemOnBreak' effect/state. |
| `ReduceManaCost` | Integer | Applies the 'ReduceManaCost' effect. |
| `ReduceSpellCostsPerDisorder` | Integer | Applies or references the 'ReduceSpellCostsPerDisorder' effect/state. |
| `ReduceSpellCostsPerParasite` | Integer | Applies or references the 'ReduceSpellCostsPerParasite' effect/state. |
| `Reflect` | Integer | Applies or references the 'Reflect' effect/state. |
| `ReflectProjectiles` | Integer | Passive: Reflects incoming projectiles back at the attacker. |
| `RefreshActPoints` | Integer | Applies the 'RefreshActPoints' effect. |
| [`RefreshEquipmentAbilityOnElement`](#refreshequipmentabilityonelement) | Block | Applies or references the 'RefreshEquipmentAbilityOnElement' effect/state. |
| `RefreshMoveOnWeaponConnect` | Integer | Applies the 'RefreshMoveOnWeaponConnect' effect. |
| `RefreshMovePoints` | Integer | Applies the 'RefreshMovePoints' effect. |
| `ReloadOnAllyCatDies` | Integer | Applies or references the 'ReloadOnAllyCatDies' effect/state. |
| `ReloadOnAllyDies` | Integer | Applies or references the 'ReloadOnAllyDies' effect/state. |
| `ReloadOnAnyDamage` | Integer | Applies or references the 'ReloadOnAnyDamage' effect/state. |
| `ReloadOnBackstab` | Integer | Applies or references the 'ReloadOnBackstab' effect/state. |
| [`ReloadOnElementalDamageReceived`](./Enums.md#enum-reloadonelementaldamagereceived) | Enum | Applies or references the 'ReloadOnElementalDamageReceived' effect/state. |
| `ReloadOnGainCoins` | Integer | Applies or references the 'ReloadOnGainCoins' effect/state. |
| `ReloadOnGainDivineShield` | Integer | Applies or references the 'ReloadOnGainDivineShield' effect/state. |
| `ReloadOnKill` | Integer | Applies or references the 'ReloadOnKill' effect/state. |
| `ReloadOnKillEnemy` | Integer | Applies or references the 'ReloadOnKillEnemy' effect/state. |
| [`ReloadOnKillTagged`](./Enums.md#enum-reloadonkilltagged) | Enum | Applies or references the 'ReloadOnKillTagged' effect/state. |
| `ReloadOnSpendMana` | Integer | Applies or references the 'ReloadOnSpendMana' effect/state. |
| `ReloadOnTotalDamageReceived` | Integer | Applies or references the 'ReloadOnTotalDamageReceived' effect/state. |
| `ReloadOnUseAbilityWithManaCost` | Integer | Applies or references the 'ReloadOnUseAbilityWithManaCost' effect/state. |
| `RemoteFlatLeech` | Integer | Applies or references the 'RemoteFlatLeech' effect/state. |
| `RemoteLeech` | Integer | Applies or references the 'RemoteLeech' effect/state. |
| `RemoveAmbientLightEffects` | Float | Applies or references the 'RemoveAmbientLightEffects' effect/state. |
| `RemoveExtraDispersedTurn` | Integer |  |
| [`RemoveGlobalModifiers`](./Arrays.md#array-removeglobalmodifiers) | Array | Applies or references the 'RemoveGlobalModifiers' effect/state. |
| `RemoveLineOfSightRestrictions` | Integer | Applies the 'RemoveLineOfSightRestrictions' effect. |
| `RemoveOncePerFightRestriction` | Integer | Applies the 'RemoveOncePerFightRestriction' effect. |
| [`RemoveStatus`](./Enums.md#enum-removestatus) | Enum | Applies or references the 'RemoveStatus' effect/state. |
| [`RemoveStatusStacks`](#removestatusstacks) | Block | Logic: Removes stacks of a specific status effect. |
| `RepairAll` | Integer | Applies or references the 'RepairAll' effect/state. |
| `RepairTrinket` | Integer | Applies or references the 'RepairTrinket' effect/state. |
| `RepairWeapon` | Integer | Applies the 'RepairWeapon' effect. |
| `RepairWeaponCondition` | Integer | Applies the 'RepairWeaponCondition' effect. |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum | Applies or references the 'ReplaceBasicAttack' effect/state. |
| [`ReplaceBasicAttackWhenCastable`](./Enums.md#enum-replacebasicattackwhencastable) | Enum | Applies the 'ReplaceBasicAttackWhenCastable' effect. |
| [`ReplaceBasicAttackWhenDead`](./Enums.md#enum-replacebasicattackwhendead) | Enum | Applies the 'ReplaceBasicAttackWhenDead' effect. |
| [`ReplaceBasicAttack_Mutation`](./Enums.md#enum-replacebasicattack_mutation) | Enum |  |
| [`ReplaceBasicMove`](./Enums.md#enum-replacebasicmove) | Enum | Applies or references the 'ReplaceBasicMove' effect/state. |
| [`ReplaceBasicMove_Mutation`](./Enums.md#enum-replacebasicmove_mutation) | Enum |  |
| [`ReplaceBlankTilesOnBattleStart`](./Enums.md#enum-replaceblanktilesonbattlestart) | Enum | Applies or references the 'ReplaceBlankTilesOnBattleStart' effect/state. |
| [`ReplaceBrain`](#replacebrain) | Block | Applies the 'ReplaceBrain' effect. |
| [`ReplaceSpawnedObjects`](./Arrays.md#array-replacespawnedobjects) | Array | Applies the 'ReplaceSpawnedObjects' effect. |
| [`ReplaceSpell`](#replacespell) | Block | Replaces a spell in the character's hand/deck with a different one. |
| [`ReplaceSpellsWhenDead`](./Enums.md#enum-replacespellswhendead) | Enum | Applies the 'ReplaceSpellsWhenDead' effect. |
| `RerollItemsOnBattleEnd` | Integer | Applies or references the 'RerollItemsOnBattleEnd' effect/state. |
| `ReturnBoundItemOnBattleEnd` | Integer |  |
| [`RevengeDamage`](#revengedamage) | Block |  |
| `Revive` | Integer | Applies or references the 'Revive' effect/state. |
| [`ReviveNextRound`](#revivenextround) | Block | Queues the character to be resurrected at the start of the next combat round. |
| `ReviveOnWin` | Integer | Applies the 'ReviveOnWin' effect. |
| `Robot` | Integer | Character Form: Behavior and stats for the 'Robot' state. |
| `RobotsInheritArmor` | Integer | Applies the 'RobotsInheritArmor' effect. |
| `RockDetector` | Integer | Applies the 'RockDetector' effect. |
| `RockyArmorPassive` | Integer | Applies or references the 'RockyArmorPassive' effect/state. |
| `RockyArmorSalvage` | Float |  |
| `Rot` | Integer | Applies or references the 'Rot' effect/state. |
| `RunInXTurns` | Integer | Applies or references the 'RunInXTurns' effect/state. |
| `RunWhenKittensDead` | Integer | Applies or references the 'RunWhenKittensDead' effect/state. |
| [`RunWhenLastPlayerCatIsCharmed`](#runwhenlastplayercatischarmed) | Block | AI Logic: Flee logic when the player team is entirely crowd-controlled. |
| `SafeDie` | Integer | Applies or references the 'SafeDie' effect/state. |
| `SafeDoomed` | Integer | Applies or references the 'SafeDoomed' effect/state. |
| `SafeExplosions` | Integer | Applies the 'SafeExplosions' effect. |
| [`ScaldingOrbMoonBossOneShot`](#scaldingorbmoonbossoneshot) | Block | Applies or references the 'ScaldingOrbMoonBossOneShot' effect/state. |
| [`ScaledStatusAlliesOnSpendMana`](#scaledstatusalliesonspendmana) | Block | Applies or references the 'ScaledStatusAlliesOnSpendMana' effect/state. |
| [`ScaledStatusOnBleedDamage`](#scaledstatusonbleeddamage) | Block | Applies the 'ScaledStatusOnBleedDamage' effect. |
| [`ScaledStatusOnHolyShieldBlock`](#scaledstatusonholyshieldblock) | Block | Applies or references the 'ScaledStatusOnHolyShieldBlock' effect/state. |
| [`ScaledStatusOnLoseShield`](#scaledstatusonloseshield) | Block | Applies the 'ScaledStatusOnLoseShield' effect. |
| [`ScaledStatusOnOverHealed`](#scaledstatusonoverhealed) | Block | Applies the 'ScaledStatusOnOverHealed' effect. |
| [`ScaledStatusOnOverMana`](#scaledstatusonovermana) | Block | Applies the 'ScaledStatusOnOverMana' effect. |
| [`ScaledStatusOnSpendMana`](#scaledstatusonspendmana) | Block | Applies the 'ScaledStatusOnSpendMana' effect. |
| [`ScalingAttackAnimation`](#scalingattackanimation) | Block | Visual: Animation scales based on damage output. |
| `ScatterCoins` | Integer |  |
| `SchizoIllusionAIModifier` | Integer | Applies or references the 'SchizoIllusionAIModifier' effect/state. |
| `SchrodingerDisorder` | Integer | Applies the 'SchrodingerDisorder' effect. |
| `Scleroderma` | Integer | Applies the 'Scleroderma' effect. |
| `Scrambled` | Integer | Applies or references the 'Scrambled' effect/state. |
| [`SecurityBotProtect`](#securitybotprotect) | Block | AI Logic: Guarding behavior for Security Bot units. |
| [`SelfDamageWhenDealDamage`](#selfdamagewhendealdamage) | Block | Applies the 'SelfDamageWhenDealDamage' effect. |
| `SelfStatusCarefulness` | Integer | Applies or references the 'SelfStatusCarefulness' effect/state. |
| [`SetBrittleImmune`](./Enums.md#enum-setbrittleimmune) | Enum | Applies or references the 'SetBrittleImmune' effect/state. |
| [`SetDefaultFace`](./Enums.md#enum-setdefaultface) | Enum | Applies the 'SetDefaultFace' effect. |
| [`SetDefaultFacePassive`](./Enums.md#enum-setdefaultfacepassive) | Enum | Applies or references the 'SetDefaultFacePassive' effect/state. |
| [`SetFaction`](./Enums.md#enum-setfaction) | Enum | Applies or references the 'SetFaction' effect/state. |
| [`SetFragileImmune`](./Enums.md#enum-setfragileimmune) | Enum | Applies or references the 'SetFragileImmune' effect/state. |
| `SetHealth` | Integer | Applies or references the 'SetHealth' effect/state. |
| [`SetItemAux`](#setitemaux) | Block | Applies or references the 'SetItemAux' effect/state. |
| `SetSpellCosts` | Integer | Applies the 'SetSpellCosts' effect. |
| `ShareHealthRegen` | Integer | Applies the 'ShareHealthRegen' effect. |
| `SharePickups` | Integer | Applies the 'SharePickups' effect. |
| `SharePickupsWithSpawner` | Integer | Applies or references the 'SharePickupsWithSpawner' effect/state. |
| `SharkySmellsBlood` | Integer | Applies or references the 'SharkySmellsBlood' effect/state. |
| `Shield` | Integer | Applies or references the 'Shield' effect/state. |
| `ShoulderCheck` | Integer | Applies the 'ShoulderCheck' effect. |
| [`ShovingMatch`](./Enums.md#enum-shovingmatch) | Enum | Applies the 'ShovingMatch' effect. |
| `ShowHiddenThings` | Integer |  |
| `SizeScale` | Float |  |
| [`SkipFirstRounds`](#skipfirstrounds) | Block | AI Logic: Passes turn for the first X rounds of combat. |
| `Sleep` | Integer | Applies the 'Sleep' effect. |
| [`SlotMachineRollPool`](#slotmachinerollpool) | Block | Logic: Defines the possible outcomes for slot machine enemies. |
| `Slow` | Integer | Applies or references the 'Slow' effect/state. |
| `SmallEnemiesIgnoreYou` | Integer | Applies the 'SmallEnemiesIgnoreYou' effect. |
| `SmallRockBehavior` | Integer | AI Logic: Movement/interaction profile for small rocks. |
| [`SmiteEnemiesWhoKill`](#smiteenemieswhokill) | Block | Applies the 'SmiteEnemiesWhoKill' effect. |
| `SoulLink` | Integer | Applies the 'SoulLink' effect. |
| `SpawnBearTrapOnMiss` | Integer | Applies the 'SpawnBearTrapOnMiss' effect. |
| `SpawnCatCloneOnCorpsePopped` | Integer | Applies or references the 'SpawnCatCloneOnCorpsePopped' effect/state. |
| [`SpawnCatCopyOnBattleStart`](#spawncatcopyonbattlestart) | Block | Applies the 'SpawnCatCopyOnBattleStart' effect. |
| [`SpawnCatCopyWhenDowned`](#spawncatcopywhendowned) | Block |  |
| `SpawnCoinAnywhere` | Integer | Applies or references the 'SpawnCoinAnywhere' effect/state. |
| `SpawnCreepOnHit` | Integer | Applies or references the 'SpawnCreepOnHit' effect/state. |
| `SpawnCreepOnHitKnockback` | Integer | Applies or references the 'SpawnCreepOnHitKnockback' effect/state. |
| [`SpawnEachTurn`](#spawneachturn) | Block | Applies or references the 'SpawnEachTurn' effect/state. |
| [`SpawnExtraThingsOnBattleStart`](#spawnextrathingsonbattlestart) | Block | Applies or references the 'SpawnExtraThingsOnBattleStart' effect/state. |
| [`SpawnItemLinkedFamiliar`](#spawnitemlinkedfamiliar) | Block | Applies or references the 'SpawnItemLinkedFamiliar' effect/state. |
| [`SpawnMeatOnMove`](./Enums.md#enum-spawnmeatonmove) | Enum | Applies the 'SpawnMeatOnMove' effect. |
| `SpawnNearEnemies` | Integer | Applies or references the 'SpawnNearEnemies' effect/state. |
| [`SpawnObjectOnPopCorpse`](./Enums.md#enum-spawnobjectonpopcorpse) | Enum | Applies or references the 'SpawnObjectOnPopCorpse' effect/state. |
| [`SpawnOnBattleStart`](./Enums.md#enum-spawnonbattlestart) | Enum | Applies or references the 'SpawnOnBattleStart' effect/state. |
| [`SpawnOnBattleStartRandomEmptyTile`](#spawnonbattlestartrandomemptytile) | Block | Applies or references the 'SpawnOnBattleStartRandomEmptyTile' effect/state. |
| [`SpawnOnDeath`](#spawnondeath) | Block | Event Trigger: Spawns a specific entity when killed. |
| [`SpawnOnDowned`](./Enums.md#enum-spawnondowned) | Enum |  |
| [`SpawnRandomPickupsOnTaggedUnitKilled`](#spawnrandompickupsontaggedunitkilled) | Block | Applies or references the 'SpawnRandomPickupsOnTaggedUnitKilled' effect/state. |
| [`SpawnThingOnDamage`](#spawnthingondamage) | Block | Applies or references the 'SpawnThingOnDamage' effect/state. |
| [`SpawnThingOnDeath`](./Enums.md#enum-spawnthingondeath) | Enum | Applies or references the 'SpawnThingOnDeath' effect/state. |
| `SpawnerCatDataReference` | Integer | Applies or references the 'SpawnerCatDataReference' effect/state. |
| [`SpecialFriends`](#specialfriends) | Block | Applies the 'SpecialFriends' effect. |
| `SpeedUp` | Integer | Applies or references the 'SpeedUp' effect/state. |
| `SpeedUp_WithoutInitiative` | Integer | Applies or references the 'SpeedUp_WithoutInitiative' effect/state. |
| `SpellDamageUp` | Integer | Applies or references the 'SpellDamageUp' effect/state. |
| [`SpewerAltGraphics`](#speweraltgraphics) | Block | Visual: Alternative graphics for Spewer enemies. |
| `SpiderInfested` | Integer | Applies or references the 'SpiderInfested' effect/state. |
| `SplashDamage` | Integer | Applies the 'SplashDamage' effect. |
| `SplittableMove` | Integer | Applies the 'SplittableMove' effect. |
| [`SpreadDisease`](#spreaddisease) | Block | Provides a chance to transmit a disease status to adjacent targets. |
| `SpreadExtraDebuffs` | Integer | Applies the 'SpreadExtraDebuffs' effect. |
| `SpreadPainBonus` | Integer | Applies the 'SpreadPainBonus' effect. |
| `SpreadPainBonusCrit` | Integer | Applies the 'SpreadPainBonusCrit' effect. |
| `SpreadWater` | Integer | Applies or references the 'SpreadWater' effect/state. |
| `SproutsGrantMovement` | Integer | Applies or references the 'SproutsGrantMovement' effect/state. |
| [`StackingDodgeChanceOnTookDamage`](#stackingdodgechanceontookdamage) | Block | Applies the 'StackingDodgeChanceOnTookDamage' effect. |
| [`StackingFlowerTrail`](#stackingflowertrail) | Block | Applies or references the 'StackingFlowerTrail' effect/state. |
| `StackingSandstorm` | Integer |  |
| [`StacyMutant_Brace`](#stacymutant_brace) | Block | Character Form: Behavior and stats for the 'StacyMutant_Brace' state. |
| [`StacyMutant_Counter`](#stacymutant_counter) | Block | Character Form: Behavior and stats for the 'StacyMutant_Counter' state. |
| [`StacyMutant_Damage`](#stacymutant_damage) | Block | Character Form: Behavior and stats for the 'StacyMutant_Damage' state. |
| [`StacyMutant_DoubleHead`](#stacymutant_doublehead) | Block | Character Form: Behavior and stats for the 'StacyMutant_DoubleHead' state. |
| [`StacyMutant_Fire`](#stacymutant_fire) | Block | Character Form: Behavior and stats for the 'StacyMutant_Fire' state. |
| [`StacyMutant_Health`](#stacymutant_health) | Block | Character Form: Behavior and stats for the 'StacyMutant_Health' state. |
| [`StacyMutant_Holy`](#stacymutant_holy) | Block | Character Form: Behavior and stats for the 'StacyMutant_Holy' state. |
| [`StacyMutant_Ice`](#stacymutant_ice) | Block | Character Form: Behavior and stats for the 'StacyMutant_Ice' state. |
| [`StacyMutant_Lightning`](#stacymutant_lightning) | Block | Character Form: Behavior and stats for the 'StacyMutant_Lightning' state. |
| [`StacyMutant_Mirror`](#stacymutant_mirror) | Block | Character Form: Behavior and stats for the 'StacyMutant_Mirror' state. |
| [`StacyMutant_Speed`](#stacymutant_speed) | Block | Character Form: Behavior and stats for the 'StacyMutant_Speed' state. |
| [`StacyMutant_Thorns`](#stacymutant_thorns) | Block | Character Form: Behavior and stats for the 'StacyMutant_Thorns' state. |
| `StartDead` | Integer | Applies or references the 'StartDead' effect/state. |
| `StartOffMap` | Integer | Applies or references the 'StartOffMap' effect/state. |
| [`StatDependentPassive`](#statdependentpassive) | Block | Applies or references the 'StatDependentPassive' effect/state. |
| `StatMinimum` | Integer | Applies the 'StatMinimum' effect. |
| [`StatsAtLowHealth`](#statsatlowhealth) | Block | Applies the 'StatsAtLowHealth' effect. |
| [`StatusAdjacentOnTheirTurnBegin`](#statusadjacentontheirturnbegin) | Block | Event Trigger: Applies nested statuses to adjacent on their turn begin. |
| [`StatusAdjacentOnTheirTurnEnd`](#statusadjacentontheirturnend) | Block | Applies or references the 'StatusAdjacentOnTheirTurnEnd' effect/state. |
| [`StatusAfterCastSpell`](#statusaftercastspell) | Block | Applies or references the 'StatusAfterCastSpell' effect/state. |
| [`StatusAfterXStacks`](#statusafterxstacks) | Block | Applies or references the 'StatusAfterXStacks' effect/state. |
| [`StatusAfterXTurns`](#statusafterxturns) | Block | Event Trigger: Applies a status effect after X turns have passed. |
| [`StatusAllCharactersOnSpawn`](#statusallcharactersonspawn) | Block | Applies or references the 'StatusAllCharactersOnSpawn' effect/state. |
| [`StatusAlliesEachTurn`](#statusallieseachturn) | Block | Applies or references the 'StatusAlliesEachTurn' effect/state. |
| [`StatusAlliesOnBattleStart`](#statusalliesonbattlestart) | Block | Applies or references the 'StatusAlliesOnBattleStart' effect/state. |
| [`StatusAlliesOnDeath`](#statusalliesondeath) | Block | Event Trigger: Applies nested statuses to allies on death. |
| [`StatusAlliesOnGainCoins`](#statusalliesongaincoins) | Block | Event Trigger: Applies nested statuses to allies on gain coins. |
| [`StatusAlliesOnKill`](#statusalliesonkill) | Block | Event Trigger: Applies nested statuses to allies on kill. |
| [`StatusAlliesOnSpendMana`](#statusalliesonspendmana) | Block | Event Trigger: Applies nested statuses to allies on spend mana. |
| [`StatusAlliesScaledByCursedOnDeath`](#statusalliesscaledbycursedondeath) | Block | Event Trigger: Applies nested statuses to allies scaled by cursed on death. |
| [`StatusAllyWhenAllySpendsMana`](#statusallywhenallyspendsmana) | Block | Event Trigger: Applies nested statuses to ally when ally spends mana. |
| [`StatusAnyCatAllyWhoKills`](#statusanycatallywhokills) | Block | Event Trigger: Applies nested statuses to any cat ally who kills. |
| `StatusCarefulness` | Integer | Applies or references the 'StatusCarefulness' effect/state. |
| [`StatusCollector`](#statuscollector) | Block | Passive: Gains benefits based on the number of statuses applied to them. |
| [`StatusDamagers`](#statusdamagers) | Block | Event Trigger: Applies nested statuses to damagers. |
| [`StatusEachRoundBegin`](#statuseachroundbegin) | Block |  |
| [`StatusEachRoundEnd`](#statuseachroundend) | Block |  |
| [`StatusEachTurnBegin`](#statuseachturnbegin) | Block | Event Trigger: Applies nested statuses to each turn begin. |
| [`StatusEachTurnBeginIfHasStatus`](#statuseachturnbeginifhasstatus) | Block | Event Trigger: Applies a status at the start of the turn if a prerequisite status is met. |
| [`StatusEachTurnEnd`](#statuseachturnend) | Block | Applies or references the 'StatusEachTurnEnd' effect/state. |
| [`StatusEachTurnEndForEachTurn`](#statuseachturnendforeachturn) | Block | Event Trigger: Applies nested statuses to each turn end for each turn. |
| [`StatusEachTurnEndIfEnabledAtStartOfTurn`](#statuseachturnendifenabledatstartofturn) | Block | Event Trigger: Applies a status at the end of the turn if an enabling condition was met at the start. |
| [`StatusEachTurnEndPerEnemyKill`](#statuseachturnendperenemykill) | Block | Event Trigger: Applies nested statuses to each turn end per enemy kill. |
| [`StatusEnemiesOnDeath`](#statusenemiesondeath) | Block | Event Trigger: Applies nested statuses to enemies on death. |
| [`StatusEveryXSpellCasts`](#statuseveryxspellcasts) | Block | Applies or references the 'StatusEveryXSpellCasts' effect/state. |
| [`StatusEveryXSpellCastsEachTurn`](#statuseveryxspellcastseachturn) | Block |  |
| [`StatusEveryXTurnBegins`](#statuseveryxturnbegins) | Block | Event Trigger: Applies nested statuses to every x turn begins. |
| [`StatusGroup`](#statusgroup) | Block | Groups multiple status effects together for batch application. |
| [`StatusIfBattleAlreadyBegan`](#statusifbattlealreadybegan) | Block | Event Trigger: Applies nested statuses to if battle already began. |
| [`StatusIfDidntMove`](#statusifdidntmove) | Block |  |
| [`StatusIfUnusedActPoints`](#statusifunusedactpoints) | Block | Applies or references the 'StatusIfUnusedActPoints' effect/state. |
| [`StatusIfUnusedMovePoints`](#statusifunusedmovepoints) | Block | Event Trigger: Applies nested statuses to if unused move points. |
| [`StatusImmunity`](./Enums.md#enum-statusimmunity) | Enum | Applies or references the 'StatusImmunity' effect/state. |
| [`StatusKilledCharacters`](#statuskilledcharacters) | Block | Event Trigger: Applies nested statuses to killed characters. |
| [`StatusKillers`](#statuskillers) | Block | Instantly kills the target if they possess the specified status effects. |
| [`StatusOnAllyCatDeath`](#statusonallycatdeath) | Block | Event Trigger: Applies nested statuses when ally cat death. |
| [`StatusOnAnyDeath`](#statusonanydeath) | Block | Event Trigger: Applies nested statuses when any death. |
| [`StatusOnBackstab`](#statusonbackstab) | Block | Event Trigger: Applies statuses when this action occurs. |
| [`StatusOnBattleEnd`](#statusonbattleend) | Block | Applies the nested status effects when the encounter finishes. |
| [`StatusOnBattleEndIfKillThresholdMet`](#statusonbattleendifkillthresholdmet) | Block | Event Trigger: Applies nested statuses when battle end if kill threshold met. |
| [`StatusOnBattleStart`](#statusonbattlestart) | Block | Event Trigger: Applies statuses when this action occurs. |
| [`StatusOnBreak`](#statusonbreak) | Block | Event Trigger: Applies statuses when this action occurs. |
| [`StatusOnBreakItem`](#statusonbreakitem) | Block | Event Trigger: Applies statuses when this action occurs. |
| [`StatusOnCastSpell`](#statusoncastspell) | Block | Event Trigger: Applies nested statuses when cast spell. |
| [`StatusOnCollectPickup`](#statusoncollectpickup) | Block | Event Trigger: Applies nested statuses when collect pickup. |
| [`StatusOnCrit`](#statusoncrit) | Block | Event Trigger: Applies nested statuses when crit. |
| [`StatusOnDealtDamage`](#statusondealtdamage) | Block | Event Trigger: Applies nested statuses when dealt damage. |
| [`StatusOnDealtDamageThreshold`](#statusondealtdamagethreshold) | Block | Event Trigger: Applies nested statuses when dealt damage threshold. |
| [`StatusOnDie`](#statusondie) | Block | Event Trigger: Applies statuses when this action occurs. |
| [`StatusOnDodge`](#statusondodge) | Block | Event Trigger: Applies statuses when this action occurs. |
| [`StatusOnEatFood`](#statusoneatfood) | Block | Event Trigger: Applies nested statuses when eat food. |
| [`StatusOnEatPill`](#statusoneatpill) | Block |  |
| [`StatusOnEndMove`](#statusonendmove) | Block | Event Trigger: Applies statuses when this action occurs. |
| [`StatusOnEnemyCastSpell`](#statusonenemycastspell) | Block |  |
| [`StatusOnEnemyConfused`](#statusonenemyconfused) | Block | Event Trigger: Applies statuses when an enemy becomes confused. |
| [`StatusOnEnemyDeath`](#statusonenemydeath) | Block | Event Trigger: Applies statuses when this action occurs. |
| [`StatusOnFallAsleep`](#statusonfallasleep) | Block | Event Trigger: Applies statuses when this action occurs. |
| [`StatusOnFullMana`](#statusonfullmana) | Block | Event Trigger: Applies statuses when this action occurs. |
| [`StatusOnGainCoins`](#statusongaincoins) | Block | Event Trigger: Applies nested statuses when gain coins. |
| [`StatusOnGainShield`](#statusongainshield) | Block | Event Trigger: Applies nested statuses when gain shield. |
| [`StatusOnHeal`](#statusonheal) | Block | Event Trigger: Applies nested statuses when heal. |
| [`StatusOnHealed`](#statusonhealed) | Block | Event Trigger: Applies nested statuses when healed. |
| [`StatusOnKill`](#statusonkill) | Block | Event Trigger: Applies statuses when this action occurs. |
| [`StatusOnKillEnemy`](#statusonkillenemy) | Block | Event Trigger: Applies statuses when this action occurs. |
| [`StatusOnLoseShield`](#statusonloseshield) | Block | Event Trigger: Applies nested statuses when lose shield. |
| [`StatusOnOverHealed`](#statusonoverhealed) | Block | Event Trigger: Applies nested statuses when over healed. |
| [`StatusOnOverMana`](#statusonovermana) | Block | Event Trigger: Applies nested statuses when over mana. |
| [`StatusOnPickupCoins`](#statusonpickupcoins) | Block | Event Trigger: Applies nested statuses when pickup coins. |
| [`StatusOnPopCorpse`](#statusonpopcorpse) | Block | Event Trigger: Applies statuses when this action occurs. |
| [`StatusOnSetPieceBreak`](#statusonsetpiecebreak) | Block |  |
| [`StatusOnSpawnIn`](#statusonspawnin) | Block | Event Trigger: Applies statuses immediately when spawned. |
| [`StatusOnStanceSwitch`](#statusonstanceswitch) | Block | Event Trigger: Applies nested statuses when stance switch. |
| [`StatusOnTakeHealthDamage`](#statusontakehealthdamage) | Block | Event Trigger: Applies nested statuses when take health damage. |
| [`StatusOnTakeHealthOrShieldDamage`](#statusontakehealthorshielddamage) | Block | Event Trigger: Applies statuses when this action occurs. |
| [`StatusOnTookDamage`](#statusontookdamage) | Block | Event Trigger: Applies nested statuses when took damage. |
| [`StatusOnTookDamageFromAbility`](#statusontookdamagefromability) | Block | Event Trigger: Applies statuses when taking damage from an ability. |
| [`StatusOnTookDamageFromEnemyAbility`](#statusontookdamagefromenemyability) | Block | Event Trigger: Applies nested statuses when took damage from enemy ability. |
| [`StatusOnTriggerTrap`](#statusontriggertrap) | Block | Event Trigger: Applies nested statuses when trigger trap. |
| [`StatusOnTurnEndIfCastNSpells`](#statusonturnendifcastnspells) | Block | Event Trigger: Applies nested statuses when turn end if cast n spells. |
| [`StatusOnTurnEndIfDidntCastAbilityTypes`](#statusonturnendifdidntcastabilitytypes) | Block | Event Trigger: Applies statuses when this action occurs. |
| [`StatusOnTurnEndIfManaExact`](#statusonturnendifmanaexact) | Block | Event Trigger: Applies nested statuses when turn end if mana exact. |
| [`StatusOnTurnEndIfManaOrHealthExact`](#statusonturnendifmanaorhealthexact) | Block | Event Trigger: Applies nested statuses when turn end if mana or health exact. |
| [`StatusOnUseAbilityWithTag`](#statusonuseabilitywithtag) | Block | Event Trigger: Applies nested statuses when use ability with tag. |
| [`StatusOnUseBasicAttack`](#statusonusebasicattack) | Block | Event Trigger: Applies nested statuses when use basic attack. |
| [`StatusOnUseElementAbility`](#statusonuseelementability) | Block | Event Trigger: Applies nested statuses when use element ability. |
| [`StatusOverlappingCharactersAndDie`](#statusoverlappingcharactersanddie) | Block | Event Trigger: Applies statuses to overlapping entities, then destroys self. |
| [`StatusPerInjury`](#statusperinjury) | Block | Event Trigger: Applies nested statuses to per injury. |
| [`StatusRandomEnemiesOnBattleStart`](#statusrandomenemiesonbattlestart) | Block | Applies or references the 'StatusRandomEnemiesOnBattleStart' effect/state. |
| [`StatusReplacement`](./Arrays.md#array-statusreplacement) | Array | Event Trigger: Applies nested statuses to replacement. |
| [`StatusThingsKnockedBack`](#statusthingsknockedback) | Block | Event Trigger: Applies nested statuses to things knocked back. |
| [`StatusWhenAllySpendsMana`](#statuswhenallyspendsmana) | Block | Event Trigger: Applies nested statuses to when ally spends mana. |
| [`StatusWhenStatusCompletelyRemoved`](#statuswhenstatuscompletelyremoved) | Block | Event Trigger: Applies statuses when a tracked status effect is fully cleansed. |
| `Stealth` | Integer | Applies the 'Stealth' effect. |
| `StealthUntilBasicAttack` | Integer | Applies or references the 'StealthUntilBasicAttack' effect/state. |
| `StevenBolts` | Integer | Applies or references the 'StevenBolts' effect/state. |
| `StrengthForEachNeighboringEnemy` | Integer | Applies the 'StrengthForEachNeighboringEnemy' effect. |
| `StrengthInNumbersAura` | Integer | Applies the 'StrengthInNumbersAura' effect. |
| `StrengthUp` | Integer | Applies or references the 'StrengthUp' effect/state. |
| `StrictLimitDamage` | Integer | Applies the 'StrictLimitDamage' effect. |
| `StripKnockback` | Integer | Applies or references the 'StripKnockback' effect/state. |
| `StripStatuses` | Integer | Applies or references the 'StripStatuses' effect/state. |
| `Study` | Integer | Applies the 'Study' effect. |
| `Stun` | Integer | Applies the 'Stun' effect. |
| `StunImmunity` | Integer | Passive: Prevents Stun from being applied. |
| [`SupportDieInsteadOfRun`](#supportdieinsteadofrun) | Block | AI Logic: Forces a support unit to die rather than flee. |
| [`SupportFormChangeInsteadOfRun`](./Enums.md#enum-supportformchangeinsteadofrun) | Enum | AI Logic: Forces a support unit to transform rather than flee. |
| `SurviveAt1HP` | Integer | Applies or references the 'SurviveAt1HP' effect/state. |
| `SwapHighestAndLowestStat` | Integer |  |
| [`SwimmingFormChange`](#swimmingformchange) | Block | Logic: Automates form change when entering/exiting water. |
| [`SyncFormsWithBuddy`](#syncformswithbuddy) | Block | Logic: Forces this character's form to match their familiar/buddy. |
| [`T3HitlerSpawningPhase`](#t3hitlerspawningphase) | Block | Boss Logic: Minion spawn phase for the T3 Hitler boss. |
| `TVBotDisableAttack` | Integer | Applies or references the 'TVBotDisableAttack' effect/state. |
| `TVBotDisableMove` | Integer | Applies or references the 'TVBotDisableMove' effect/state. |
| `TVBotDisableSpells` | Integer | Applies or references the 'TVBotDisableSpells' effect/state. |
| [`TVBotScreen`](#tvbotscreen) | Block | Visual: TV Bot screen state. |
| [`TagGreed`](./Enums.md#enum-taggreed) | Enum | Applies or references the 'TagGreed' effect/state. |
| [`TaggedPickupEffectReplacement`](#taggedpickupeffectreplacement) | Block | Applies the 'TaggedPickupEffectReplacement' effect. |
| [`TakeBonusTurnWithStatus`](#takebonusturnwithstatus) | Block | Grants the character an immediate extra turn while afflicted with specific statuses. |
| `TakeExtraTurn` | Integer | Applies the 'TakeExtraTurn' effect. |
| `TakeWeaponFromSpawner` | Integer | Applies or references the 'TakeWeaponFromSpawner' effect/state. |
| `Tall` | Integer | Applies or references the 'Tall' effect/state. |
| [`TallTumorManaBurn`](./Enums.md#enum-talltumormanaburn) | Enum | Applies or references the 'TallTumorManaBurn' effect/state. |
| [`Tangled`](./Arrays.md#array-tangled) | Array | Applies a tangled/ensnared status effect, often modifying visual sprites. |
| `Tarred` | Integer | Applies or references the 'Tarred' effect/state. |
| `TauntAlways` | Integer | Applies the 'TauntAlways' effect. |
| `TauntAtFullHealth` | Integer | Applies the 'TauntAtFullHealth' effect. |
| `Tech` | Integer | Applies the 'Tech' effect. |
| `TempCounterAttack` | Integer | Applies or references the 'TempCounterAttack' effect/state. |
| `TempDamageUp` | Integer | Applies the 'TempDamageUp' effect. |
| `TempInitiativeChange` | Integer | Applies the 'TempInitiativeChange' effect. |
| `TempMeleeRangeUp` | Integer | Applies or references the 'TempMeleeRangeUp' effect/state. |
| `TempMovement` | Integer | Applies the 'TempMovement' effect. |
| `TempNoManaRegen` | Integer | Applies or references the 'TempNoManaRegen' effect/state. |
| [`TempPassiveUntilSettled`](#temppassiveuntilsettled) | Block | Applies or references the 'TempPassiveUntilSettled' effect/state. |
| `TempRangeUp` | Integer | Applies or references the 'TempRangeUp' effect/state. |
| `TempSpellDamageUp` | Integer | Applies the 'TempSpellDamageUp' effect. |
| `TempStrengthUp` | Integer | Applies or references the 'TempStrengthUp' effect/state. |
| [`Temporary`](#temporary) | Block | A wrapper block for applying status effects that automatically expire. |
| [`Terminator2Chase`](./Enums.md#enum-terminator2chase) | Enum | Applies or references the 'Terminator2Chase' effect/state. |
| [`Terminator2Run`](#terminator2run) | Block | AI Movement: Specific run logic for Terminator2. |
| [`TerminatorChase`](#terminatorchase) | Block | AI Movement: Specific chase logic for Terminator. |
| [`TerminatorSkin`](#terminatorskin) | Block | Visual: Skin definition for Terminator. |
| [`TheHunger`](#thehunger) | Block | Applies the 'TheHunger' effect. |
| `Thorns` | Integer | Applies or references the 'Thorns' effect/state. |
| `TileDamageMultiplier` | Integer | Applies the 'TileDamageMultiplier' effect. |
| [`TileElementDamageImmunity`](./Enums.md#enum-tileelementdamageimmunity) | Enum | Applies or references the 'TileElementDamageImmunity' effect/state. |
| [`TileTrail`](./Enums.md#enum-tiletrail) | Enum |  |
| [`TileTrail_Ahead`](./Enums.md#enum-tiletrail_ahead) | Enum | Applies or references the 'TileTrail_Ahead' effect/state. |
| [`TinkererBasicAttackSwitching`](#tinkererbasicattackswitching) | Block | Logic: Allows Tinkerer to swap basic attacks. |
| [`TintItem`](#tintitem) | Block | Applies or references the 'TintItem' effect/state. |
| `TireBehavior` | Integer | Applies or references the 'TireBehavior' effect/state. |
| `TormentorHeal` | Integer | Applies or references the 'TormentorHeal' effect/state. |
| `TossTargetIsAggroTarget` | Integer | Applies or references the 'TossTargetIsAggroTarget' effect/state. |
| `TossTargetIsBuddy` | Integer | Applies or references the 'TossTargetIsBuddy' effect/state. |
| `TossTargetIsNotInWater` | Integer | Applies or references the 'TossTargetIsNotInWater' effect/state. |
| [`TourettesMeows`](#tourettesmeows) | Block | Applies the 'TourettesMeows' effect. |
| [`TowerDefense`](#towerdefense) | Block | Applies the 'TowerDefense' effect. |
| [`TowerDefenseReflex`](./Enums.md#enum-towerdefensereflex) | Enum | Applies the 'TowerDefenseReflex' effect. |
| [`TrackAmountKilledByPlayer`](./Enums.md#enum-trackamountkilledbyplayer) | Enum | Applies or references the 'TrackAmountKilledByPlayer' effect/state. |
| `Trample` | Integer | Applies or references the 'Trample' effect/state. |
| [`TransformInXTurns`](#transforminxturns) | Block | Logic: Forces a form change after X turns. |
| [`TransformItemOnElementInfluence`](#transformitemonelementinfluence) | Block | Applies or references the 'TransformItemOnElementInfluence' effect/state. |
| [`TransformOnDeath`](./Enums.md#enum-transformondeath) | Enum | Applies or references the 'TransformOnDeath' effect/state. |
| [`TransformOnDeathImmediately`](./Enums.md#enum-transformondeathimmediately) | Enum | Logic: Bypasses death sequence to instantly assume a new form. |
| [`TransformOnElementInfluence`](#transformonelementinfluence) | Block | Logic: Changes form when affected by elements. |
| [`TransformOnElementInfluencex`](#transformonelementinfluencex) | Block | Logic: Variant element influence transformation. |
| [`TransformOnStatusThreshold`](#transformonstatusthreshold) | Block | Logic: Changes form when a status effect reaches a certain stack count. |
| [`TransformWeapon`](#transformweapon) | Block | Transforms the equipped weapon into another specific weapon state. |
| [`TransformWhenBuddyDies`](./Enums.md#enum-transformwhenbuddydies) | Enum | Applies or references the 'TransformWhenBuddyDies' effect/state. |
| `TrapEffectsMultiplier` | Integer | Applies the 'TrapEffectsMultiplier' effect. |
| [`Trapper`](#trapper) | Block | Character Form: Behavior and stats for the 'Trapper' state. |
| `TriggerBleedOnBleed` | Integer |  |
| `TrinketActiveEffectsMultiplierBonus` | Integer | Applies or references the 'TrinketActiveEffectsMultiplierBonus' effect/state. |
| `TrinketPassiveMultiplierBonus` | Integer | Applies or references the 'TrinketPassiveMultiplierBonus' effect/state. |
| `Triskaidekaphobia` | Integer | Applies the 'Triskaidekaphobia' effect. |
| `TrueShot` | Integer | Applies or references the 'TrueShot' effect/state. |
| [`TunnelVision`](#tunnelvision) | Block | Applies or references the 'TunnelVision' effect/state. |
| `TutorialBossRiggedFight` | Integer | Applies or references the 'TutorialBossRiggedFight' effect/state. |
| [`TwisterFling`](#twisterfling) | Block | Logic: Fling behavior for tornado attacks. |
| `UncappedHP` | Integer | Applies the 'UncappedHP' effect. |
| `UncappedHPBonusStr` | Integer | Applies the 'UncappedHPBonusStr' effect. |
| `UncappedMana` | Integer | Applies the 'UncappedMana' effect. |
| `Uncontrollable` | Integer | Applies or references the 'Uncontrollable' effect/state. |
| `Undead` | Integer | Applies or references the 'Undead' effect/state. |
| [`UnlimitedDeathRattleRevive`](#unlimiteddeathrattlerevive) | Block | Logic: Endless resurrection on death. |
| `UnlockOrientation` | Integer | Applies or references the 'UnlockOrientation' effect/state. |
| `UpTireBehavior` | Integer | Applies or references the 'UpTireBehavior' effect/state. |
| [`UpgradeLevelUpClassActives`](./Enums.md#enum-upgradelevelupclassactives) | Enum | Applies the 'UpgradeLevelUpClassActives' effect. |
| [`UpgradeLevelUpClassPassives`](./Enums.md#enum-upgradelevelupclasspassives) | Enum | Applies the 'UpgradeLevelUpClassPassives' effect. |
| `UpgradeSpawnedPickups` | Integer | Applies the 'UpgradeSpawnedPickups' effect. |
| [`UpgradeTaggedSpawnsToChampions`](./Enums.md#enum-upgradetaggedspawnstochampions) | Enum |  |
| [`UseAbility`](./Enums.md#enum-useability) | Enum | Logic: Forces execution of an ability. |
| [`UseAbilityWhenOutOfStatus`](#useabilitywhenoutofstatus) | Block | Logic: Casts a specific ability the moment a status effect expires. |
| [`UseAbilityWhenShieldDepleted`](./Enums.md#enum-useabilitywhenshielddepleted) | Enum | Applies or references the 'UseAbilityWhenShieldDepleted' effect/state. |
| [`UseAbility_Madness`](./Enums.md#enum-useability_madness) | Enum | Applies the 'UseAbility_Madness' effect. |
| [`UseAbility_NonStack`](./Enums.md#enum-useability_nonstack) | Enum | Applies or references the 'UseAbility_NonStack' effect/state. |
| `VaporizeInanimate` | Integer |  |
| `Vegan` | Integer |  |
| `Vengeful` | Integer | Applies the 'Vengeful' effect. |
| [`VisualFXTile`](./Enums.md#enum-visualfxtile) | Enum |  |
| `Wall` | Integer | Applies or references the 'Wall' effect/state. |
| `WaterWalk` | Integer | Applies or references the 'WaterWalk' effect/state. |
| `Weakness` | Integer | Applies the 'Weakness' effect. |
| `WeaponActiveEffectsMultiplierBonus` | Integer |  |
| `WeaponCountsAsBasicAttack` | Integer | Applies the 'WeaponCountsAsBasicAttack' effect. |
| `WeaponDamageMultiplierBonus` | Integer | Applies the 'WeaponDamageMultiplierBonus' effect. |
| `WeaponPassiveMultiplierBonus` | Integer |  |
| `WeaponsDontLoseDurability` | Integer | Applies or references the 'WeaponsDontLoseDurability' effect/state. |
| `Webbed` | Integer | Applies or references the 'Webbed' effect/state. |
| [`WeremanTransformationReceiver`](./Enums.md#enum-weremantransformationreceiver) | Enum | Applies or references the 'WeremanTransformationReceiver' effect/state. |
| `Wet` | Integer | Applies or references the 'Wet' effect/state. |
| [`WhitelistPickupType`](./Enums.md#enum-whitelistpickuptype) | Enum | Applies or references the 'WhitelistPickupType' effect/state. |
| `WideBackstab` | Integer | Applies or references the 'WideBackstab' effect/state. |
| `WispDodge` | Integer | Applies or references the 'WispDodge' effect/state. |
| `WobblyCat` | Integer | Applies the 'WobblyCat' effect. |
| `XIsConsumedCharacterMaxHP` | Integer | Applies or references the 'XIsConsumedCharacterMaxHP' effect/state. |
| `XIsCountDeaths` | Integer | Applies or references the 'XIsCountDeaths' effect/state. |
| [`XIsCountStatusStacks`](./Enums.md#enum-xiscountstatusstacks) | Enum | Applies or references the 'XIsCountStatusStacks' effect/state. |
| [`XIsFormulaLockedUntilComplete`](./Enums.md#enum-xisformulalockeduntilcomplete) | Enum | Applies or references the 'XIsFormulaLockedUntilComplete' effect/state. |
| `XIsFreeArmorSlots` | Integer | Applies or references the 'XIsFreeArmorSlots' effect/state. |
| `XIsIncreaseEachTurn` | Integer | Applies or references the 'XIsIncreaseEachTurn' effect/state. |
| [`XIsLivingAlliesWithTag`](./Enums.md#enum-xislivingallieswithtag) | Enum | Applies or references the 'XIsLivingAlliesWithTag' effect/state. |
| [`XIsLivingCharactersWithTag`](./Enums.md#enum-xislivingcharacterswithtag) | Enum | Applies or references the 'XIsLivingCharactersWithTag' effect/state. |
| [`XIsMultipliedPercentHealth`](./Arrays.md#array-xismultipliedpercenthealth) | Array | Applies or references the 'XIsMultipliedPercentHealth' effect/state. |
| `XIsOtherHealsThisTurn` | Integer | Applies or references the 'XIsOtherHealsThisTurn' effect/state. |
| `XIsRampAndReset` | Integer | Applies or references the 'XIsRampAndReset' effect/state. |
| `XIsRecycleCostReduction` | Integer | Applies or references the 'XIsRecycleCostReduction' effect/state. |
| `XIsSpellStormRampAndReset` | Integer | Math variable assignment: Evaluates X based on Spell Storm stacks, then resets them. |
| `XIsTimesDamageTaken` | Integer | Applies or references the 'XIsTimesDamageTaken' effect/state. |
| `YOffset` | Float | Applies or references the 'YOffset' effect/state. |
| `ZeroKnockbackDamage` | Integer | Applies or references the 'ZeroKnockbackDamage' effect/state. |
| `Zombie` | Integer |  |
| `ally_chance` | Integer |  |
| `cant_miss` | Boolean |  |
| `chance` | Integer | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `count` | Integer | Quantity. |
| `damage` | Integer | The base damage properties of an attack. |
| [`effects`](#effects) | Block | Non-damaging status applications and logic triggers executed on impact. |
| [`element`](./Enums.md#enum-element) | Enum |  |
| [`elements`](./Arrays.md#array-elements) | Array |  |
| `end_of_round` | Boolean |  |
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. |
| `exclude_self` | Boolean |  |
| `include_spells` | Boolean | If true, allows the AI to cast spells during this bonus turn. |
| `knockback` | Integer |  |
| [`mode`](./Enums.md#enum-mode) | Enum |  |
| `must_do_damage` | Boolean |  |
| [`passives`](#passives) | Block |  |
| `stacks` | Integer | Number of stacks or intensity to apply. |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. |
| [`tag_filter`](./Enums.md#enum-tag_filter) | Enum |  |
| [`threshold`](#threshold) | Block |  |
| `triggers_limit` | Integer |  |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. |
| [`{Damage Blocks}`](#{damage blocks}) | Block | **(Supports Multiple)** A damage hit definition. See Engine_Damage.md for the full schema. |
| `{Statuses / Passives}` | Variable | Any valid Status or Passive ID. Value varies (typically a stack count, `true`, or a nested Block). See Engine_Statuses_and_Passives.md for all confirmed IDs. |

</details>

### Valid Nested Blocks

The following blocks all behave as `[status_passive_id]` containers. Each has its own unique parameters listed below its entry.

---

#### `AddPassivesToCharmed`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `AddPassivesToMinions`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`tag_filter`](./Enums.md#enum-tag_filter) | Enum |  |

</details>

---

#### `AddSelfStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `AddSelfStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `AddStatusToAllDamage`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| `must_do_damage` | Boolean |  |
| [`Conditional_HasStatus`](#conditional_hasstatus) | Block | Nested conditional. |
| [`Conditional_HasTag`](#conditional_hastag) | Block | Nested conditional. |

</details>

---

#### `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`Conditional_Adjacent`](#conditional_adjacent) | Block | Nested conditional. |
| [`Conditional_Ally`](#conditional_ally) | Block | Nested conditional. |
| [`Conditional_Enemy`](#conditional_enemy) | Block | Nested conditional. |
| [`Conditional_GoodRoll`](#conditional_goodroll) | Block | Nested conditional. |
| [`Conditional_HasTag`](#conditional_hastag) | Block | Nested conditional. |
| [`Conditional_Shielded`](#conditional_shielded) | Block | Nested conditional. |
| [`Conditional_SourceHasTag`](#conditional_sourcehastag) | Block | Nested conditional. |

</details>

---

#### `AddStatusToBasicMeleeAttack`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `AddStatusToElementDamage`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type required or applied. |
| [`Conditional_Corpse`](#conditional_corpse) | Block | Nested conditional. |

</details>

---

#### `AddStatusToKnockbackDamage`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `AddStatusToSpells`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`Conditional_Enemy`](#conditional_enemy) | Block | Nested conditional. |

</details>

---

#### `AddStatusToTrampleDamage`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `AddStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `AdventureTokenPassivePool`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `ApplyPassives`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `ApplyStatusIfCrit`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `ApplyStatusesToRandomEnemiesEachTurn`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| `count` | Integer | Quantity. |

</details>

---

#### `CatchProjectiles`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| `ally_chance` | Integer |  |
| `chance` | Integer | Probability (0.0 to 1.0 or percentage) of this occurring. |

</details>

---

#### `CharacterTypeGainsStatusAtBattleStart`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. |
| [`Conditional_Flying`](#conditional_flying) | Block | Nested conditional. |

</details>

---

#### `CritsApplyStatus`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`Conditional_HasStatus`](#conditional_hasstatus) | Block | Nested conditional. |

</details>

---

#### `ExtraStatusWhenDealingDamage`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`Conditional_Ally`](#conditional_ally) | Block | Nested conditional. |
| [`Conditional_PartyMember`](#conditional_partymember) | Block | Nested conditional. |

</details>

---

#### `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| `cant_miss` | Boolean |  |
| `damage` | Integer | The base damage properties of an attack. |
| [`effects`](#effects) | Block | Non-damaging status applications and logic triggers executed on impact. |
| [`elements`](./Arrays.md#array-elements) | Array |  |
| `knockback` | Integer |  |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. |

</details>

---

#### `PassiveAfterXKills`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`passives`](#passives) | Block | Passives granted by equipping this. |
| `stacks` | Integer | Number of stacks or intensity to apply. |

</details>

---

#### `PassiveAtHealthThreshold`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`mode`](./Enums.md#enum-mode) | Enum |  |
| [`passives`](#passives) | Block | Passives granted by equipping this. |
| `threshold` | Integer |  |

</details>

---

#### `PassiveAtStatThreshold`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`mode`](./Enums.md#enum-mode) | Enum |  |
| [`passives`](#passives) | Block |  |
| [`threshold`](#threshold) | Block |  |

</details>

---

#### `PassiveGroup`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `PassiveWhenAffectedByElement`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`element`](./Enums.md#enum-element) | Enum |  |
| [`passives`](#passives) | Block |  |

</details>

---

#### `PassiveWhenAtFullMana`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `PassiveWhenDead`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `PassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`passives`](#passives) | Block | Block listing intrinsic passive modifiers. |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. |

</details>

---

#### `PassiveWhileInMonkMeleeStance`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `RandomPassivePool`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| `damage` | Integer |  |
| [`effects`](#effects) | Block |  |
| [`elements`](./Arrays.md#array-elements) | Array |  |
| `knockback` | Integer |  |
| [`type`](./Enums.md#enum-type) | Enum |  |

</details>

---

#### `StatusAfterCastSpell`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `StatusAfterXTurns`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| `stacks` | Integer | Number of stacks or intensity to apply. |

</details>

---

#### `StatusAllCharactersOnSpawn`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`Conditional_Boss`](#conditional_boss) | Block | Nested conditional. |
| [`Conditional_PartyMember`](#conditional_partymember) | Block | Nested conditional. |
| [`Conditional_Tiny`](#conditional_tiny) | Block | Nested conditional. |

</details>

---

#### `StatusAlliesEachTurn`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| `exclude_self` | Boolean |  |
| [`Conditional_Adjacent`](#conditional_adjacent) | Block | Nested conditional. |

</details>

---

#### `StatusAlliesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `StatusAlliesOnDeath`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| `triggers_limit` | Integer |  |

</details>

---

#### `StatusEachRoundEnd`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `StatusEachTurnBegin`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`Conditional_BadRoll`](#conditional_badroll) | Block | Nested conditional. |
| [`Conditional_GoodRoll`](#conditional_goodroll) | Block | Nested conditional. |

</details>

---

#### `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`Conditional_BadRoll`](#conditional_badroll) | Block | Nested conditional. |
| [`Conditional_GoodRoll`](#conditional_goodroll) | Block | Nested conditional. |
| [`Conditional_HasCleansableDebuffs`](#conditional_hascleansabledebuffs) | Block | Nested conditional. |
| [`Conditional_ManaThreshold`](#conditional_manathreshold) | Block | Nested conditional. |

</details>

---

#### `StatusEachTurnEndForEachTurn`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `StatusEveryXSpellCasts`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| `stacks` | Integer | Number of stacks or intensity to apply. |

</details>

---

#### `StatusGroup`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `StatusIfUnusedMovePoints`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `StatusKilledCharacters`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`Conditional_Ally`](#conditional_ally) | Block | Nested conditional. |
| [`Conditional_RandomChance`](#conditional_randomchance) | Block | Nested conditional. |

</details>

---

#### `StatusKillers`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`Conditional_Boss`](#conditional_boss) | Block | Nested conditional. |
| [`Conditional_NotBoss`](#conditional_notboss) | Block | Nested conditional. |

</details>

---

#### `StatusOnAllyCatDeath`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `StatusOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. |
| [`Conditional_Corpse`](#conditional_corpse) | Block | Nested conditional. |
| [`Conditional_GoodRoll`](#conditional_goodroll) | Block | Nested conditional. |
| [`Conditional_Shielded`](#conditional_shielded) | Block | Nested conditional. |

</details>

---

#### `StatusOnBattleStart`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `StatusOnBreak`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `StatusOnBreakItem`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `StatusOnCastSpell`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `StatusOnCollectPickup`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `StatusOnDie`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`Conditional_RandomChance`](#conditional_randomchance) | Block | Nested conditional. |

</details>

---

#### `StatusOnEatFood`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `StatusOnEatPill`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `StatusOnEndMove`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`Conditional_FirstApplicationThisTurn`](#conditional_firstapplicationthisturn) | Block | Nested conditional. |
| [`Conditional_GoodRoll`](#conditional_goodroll) | Block | Nested conditional. |

</details>

---

#### `StatusOnGainCoins`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `StatusOnHealed`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`Conditional_FirstApplicationThisTurn`](#conditional_firstapplicationthisturn) | Block | Nested conditional. |
| [`Conditional_GoodRoll`](#conditional_goodroll) | Block | Nested conditional. |

</details>

---

#### `StatusOnKillEnemy`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `StatusOnPickupCoins`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `StatusOnPopCorpse`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `StatusOnTookDamage`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`Conditional_HasStatus`](#conditional_hasstatus) | Block | Nested conditional. |
| [`Conditional_HealthThreshold`](#conditional_healththreshold) | Block | Nested conditional. |

</details>

---

#### `StatusOnTookDamageFromAbility`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `StatusOnUseBasicAttack`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `StatusRandomEnemiesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| `count` | Integer | Quantity. |

</details>

---

#### `StatusWhenAllySpendsMana`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `TakeBonusTurnWithAIControl`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| `end_of_round` | Boolean |  |
| `include_spells` | Boolean | If true, allows the AI to cast spells during this bonus turn. |

</details>

---

#### `TakeBonusTurnWithStatus`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `TempPassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`status`](./Enums.md#enum-status) | Enum | The required status effect. |

</details>

---

#### `additional_passives`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `bonus_passives`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `extra_statuses`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| [`Conditional_HasTag`](#conditional_hastag) | Block | Nested conditional. |

</details>

---

#### `party_status_next_fight`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `passives`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `self_status_next_fight`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

---

#### `statuses`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |

</details>

