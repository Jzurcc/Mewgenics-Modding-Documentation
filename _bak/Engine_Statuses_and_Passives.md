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
| `AOEBonus` | Number | Applies or references the 'AOEBonus' effect/state. |
| [`AbilityAfterEnemyCastSpell_Stackable`](./Enums.md#enum-abilityafterenemycastspell_stackable) | Enum | Applies or references the 'AbilityAfterEnemyCastSpell_Stackable' effect/state. |
| [`AbilityChargeRefundChance`](#abilitychargerefundchance) | Block | Applies the 'AbilityChargeRefundChance' effect. |
| `AbilityDamageMultiplier` | Number |  |
| `AbilityDisableIfLivingCrow` | Number | Applies or references the 'AbilityDisableIfLivingCrow' effect/state. |
| [`AbilityEnableIfConsumedCharacterHasTag`](./Enums.md#enum-abilityenableifconsumedcharacterhastag) | Enum | Applies or references the 'AbilityEnableIfConsumedCharacterHasTag' effect/state. |
| `AbilityEnabledAtHealthThreshold` | Number | Applies or references the 'AbilityEnabledAtHealthThreshold' effect/state. |
| `AbilityEnabledIfBasicAttackUsedThisTurn` | Number | Applies or references the 'AbilityEnabledIfBasicAttackUsedThisTurn' effect/state. |
| [`AbilityEnabledIfHasStatus`](./Enums.md#enum-abilityenabledifhasstatus) | Enum | Applies or references the 'AbilityEnabledIfHasStatus' effect/state. |
| `AbilityEnabledIfMovementTrapped` | Number | Applies or references the 'AbilityEnabledIfMovementTrapped' effect/state. |
| `AbilityEnabledIfNoAggroTarget` | Number | Applies or references the 'AbilityEnabledIfNoAggroTarget' effect/state. |
| [`AbilityEnabledIfNotHasStatus`](./Enums.md#enum-abilityenabledifnothasstatus) | Enum | Applies or references the 'AbilityEnabledIfNotHasStatus' effect/state. |
| [`AbilityEnabledIfSpecificItemEquipped`](./Enums.md#enum-abilityenabledifspecificitemequipped) | Enum | Applies or references the 'AbilityEnabledIfSpecificItemEquipped' effect/state. |
| `AbilityEnabledOncePerFightAtHealthThreshold` | Number | Applies or references the 'AbilityEnabledOncePerFightAtHealthThreshold' effect/state. |
| `AbilityEnabledOncePerRound` | Number | Applies or references the 'AbilityEnabledOncePerRound' effect/state. |
| `AbilityEnabledPercentEachTurn` | Number | Applies or references the 'AbilityEnabledPercentEachTurn' effect/state. |
| [`AbilityHealthThreshold`](#abilityhealththreshold) | Block | AI Trigger: Executes an ability when health drops below a specific threshold. |
| `AbilityInheritsWeaponEffects` | Number | Applies or references the 'AbilityInheritsWeaponEffects' effect/state. |
| [`AbilityOnBattleStart`](./Enums.md#enum-abilityonbattlestart) | Enum | Applies or references the 'AbilityOnBattleStart' effect/state. |
| `AbilityOnBattleStart_Immediate` | Enum/String | Applies or references the 'AbilityOnBattleStart_Immediate' effect/state. |
| [`AbilityOnBattleStart_UseAI`](./Enums.md#enum-abilityonbattlestart_useai) | Enum | Applies or references the 'AbilityOnBattleStart_UseAI' effect/state. |
| [`AbilityOnRoundEnd`](#abilityonroundend) | Block | AI Trigger: Executes an ability at the end of the combat round. |
| [`AbilityOnRoundEndOnce`](#abilityonroundendonce) | Block | Applies or references the 'AbilityOnRoundEndOnce' effect/state. |
| [`AbilityReaction`](./Enums.md#enum-abilityreaction) | Enum | AI Trigger: Executes an ability in reaction to a specific event (e.g., taking damage). |
| [`AbilityWhenBuddyDies`](./Enums.md#enum-abilitywhenbuddydies) | Enum | Applies or references the 'AbilityWhenBuddyDies' effect/state. |
| [`AbilityWhenTaggedCharacterMovesNear`](#abilitywhentaggedcharactermovesnear) | Block | AI Trigger: Executes an ability when a character with a specific tag moves adjacent. |
| `AbsorbManaAura` | Number | Applies the 'AbsorbManaAura' effect. |
| `AbsorbManaFromOtherSpells` | Number | Applies or references the 'AbsorbManaFromOtherSpells' effect/state. |
| [`AddAdvantageToEvent`](#addadvantagetoevent) | Block | Applies or references the 'AddAdvantageToEvent' effect/state. |
| `AddAllyNeighborsToAbilityRange` | Number | Applies the 'AddAllyNeighborsToAbilityRange' effect. |
| `AddAllyNeighborsToAttackRange` | Number | Applies the 'AddAllyNeighborsToAttackRange' effect. |
| `AddBonusMeleeRange` | Number | Applies the 'AddBonusMeleeRange' effect. |
| `AddBonusRange` | Number | Applies or references the 'AddBonusRange' effect/state. |
| `AddChaScalingSpellDamage` | Number | Applies the 'AddChaScalingSpellDamage' effect. |
| `AddConstitution` | Number |  |
| `AddCorpseHealth` | Number | Applies the 'AddCorpseHealth' effect. |
| `AddCritMultiplier` | Number | Applies the 'AddCritMultiplier' effect. |
| `AddDamage` | Number | Applies or references the 'AddDamage' effect/state. |
| `AddDamageToBasicAttack` | Number | Applies the 'AddDamageToBasicAttack' effect. |
| [`AddDamageToElementDamage`](#adddamagetoelementdamage) | Block | Applies or references the 'AddDamageToElementDamage' effect/state. |
| [`AddElementsToBasicAttack`](./Enums.md#enum-addelementstobasicattack) | Enum |  |
| [`AddElementsToSpells`](./Enums.md#enum-addelementstospells) | Enum | Applies or references the 'AddElementsToSpells' effect/state. |
| `AddEndOfCombatRegen` | Number | Applies or references the 'AddEndOfCombatRegen' effect/state. |
| [`AddHiddenTag`](./Enums.md#enum-addhiddentag) | Enum | Applies or references the 'AddHiddenTag' effect/state. |
| `AddInitiative` | Number | Applies or references the 'AddInitiative' effect/state. |
| `AddKnockbackDamage` | Number | Applies or references the 'AddKnockbackDamage' effect/state. |
| `AddKnockbackToEverything` | Number | Applies the 'AddKnockbackToEverything' effect. |
| `AddLevelUpRerolls` | Number | Applies or references the 'AddLevelUpRerolls' effect/state. |
| `AddLevelUpStatMultiplier` | Number | Applies the 'AddLevelUpStatMultiplier' effect. |
| `AddLootMultiplier` | Number |  |
| `AddManaRegen` | Number | Applies or references the 'AddManaRegen' effect/state. |
| `AddMaxHealth` | Number | Applies or references the 'AddMaxHealth' effect/state. |
| `AddMeleeKnockback` | Number | Applies or references the 'AddMeleeKnockback' effect/state. |
| `AddMovement` | Number | Applies or references the 'AddMovement' effect/state. |
| [`AddPassiveToSpawnedRocks`](#addpassivetospawnedrocks) | Block | Applies the 'AddPassiveToSpawnedRocks' effect. |
| [`AddPassivesToCharmed`](#addpassivestocharmed) | Block | Applies the 'AddPassivesToCharmed' effect. |
| [`AddPassivesToMinions`](#addpassivestominions) | Block | Applies the 'AddPassivesToMinions' effect. |
| [`AddPassivesToSummonAbilityMinions`](#addpassivestosummonabilityminions) | Block | Applies the 'AddPassivesToSummonAbilityMinions' effect. |
| `AddRandomEliteBuff` | Number |  |
| `AddRangedCritChance` | Number | Applies the 'AddRangedCritChance' effect. |
| [`AddSelfStatusToBasicAttack`](#addselfstatustobasicattack) | Block | Applies or references the 'AddSelfStatusToBasicAttack' effect/state. |
| [`AddSelfStatusToWeapons`](#addselfstatustoweapons) | Block | Applies the 'AddSelfStatusToWeapons' effect. |
| `AddSpeed` | Number | Applies the 'AddSpeed' effect. |
| `AddSpellDamage` | Number | Applies the 'AddSpellDamage' effect. |
| `AddStartingMana` | Number | Applies or references the 'AddStartingMana' effect/state. |
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
| `AddUnfilledMaxHealth` | Number | Applies the 'AddUnfilledMaxHealth' effect. |
| `AddWeaponAux` | Number | Applies or references the 'AddWeaponAux' effect/state. |
| `AddWeaponScaling` | Number | Applies the 'AddWeaponScaling' effect. |
| [`AdvancedTint`](./Arrays.md#array-advancedtint) | Array | Applies or references the 'AdvancedTint' effect/state. |
| [`AdventureTokenPassivePool`](#adventuretokenpassivepool) | Block | Map/Metaprogression: Pool of passive modifiers applied by adventure tokens. |
| [`AfterImage`](./Enums.md#enum-afterimage) | Enum | Spawns a visual decoy or shade at the caster's previous location. |
| `AggroTargetIsBuddy` | Number | Applies or references the 'AggroTargetIsBuddy' effect/state. |
| `AggroTargetIsCurrentTurn` | Number | Applies or references the 'AggroTargetIsCurrentTurn' effect/state. |
| [`AggroTargetIsGovernedByHitEffect`](#aggrotargetisgovernedbyhiteffect) | Block | AI Logic: Forces the character's aggro to follow specific hit effects rather than default proximity. |
| `AggroTargetIsLastEnemyThatDealtDamage` | Number | Applies or references the 'AggroTargetIsLastEnemyThatDealtDamage' effect/state. |
| `AggroTargetIsLowestHealthEnemyTillItDies` | Number | Applies or references the 'AggroTargetIsLowestHealthEnemyTillItDies' effect/state. |
| `AggroTargetIsLowestMaxHealthCat` | Number | Applies or references the 'AggroTargetIsLowestMaxHealthCat' effect/state. |
| [`AlienBeastDangerZones`](./Arrays.md#array-alienbeastdangerzones) | Array | Applies or references the 'AlienBeastDangerZones' effect/state. |
| `AlienBeastEyeStalks` | Number | Applies or references the 'AlienBeastEyeStalks' effect/state. |
| `AllDamageCrits` | Number | Applies the 'AllDamageCrits' effect. |
| `AllDamageImmune_IncludingSpeculative` | Number | Applies or references the 'AllDamageImmune_IncludingSpeculative' effect/state. |
| `AllSpellsCostActPoints` | Number | Applies or references the 'AllSpellsCostActPoints' effect/state. |
| `AllSpellsCostCharge` | Number | Applies or references the 'AllSpellsCostCharge' effect/state. |
| [`AllStatsAura`](#allstatsaura) | Block | Passive: Projects an aura that modifies all primary stats of nearby characters. |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. |
| `AllStatsUpPerDisorder` | Number | Applies or references the 'AllStatsUpPerDisorder' effect/state. |
| `AllUnitsExplodeOnDeath` | Number | Applies or references the 'AllUnitsExplodeOnDeath' effect/state. |
| `AlliesAvoidTraps` | Number | Applies the 'AlliesAvoidTraps' effect. |
| `AlliesScrambleSpellAfterCast` | Number | Applies or references the 'AlliesScrambleSpellAfterCast' effect/state. |
| `AllowPassTurn` | Number | Applies the 'AllowPassTurn' effect. |
| [`AlluringDoodieEater`](#alluringdoodieeater) | Block | Applies or references the 'AlluringDoodieEater' effect/state. |
| [`AllyBonusAbilityAura`](./Enums.md#enum-allybonusabilityaura) | Enum | Applies the 'AllyBonusAbilityAura' effect. |
| `AllyChainKnockback` | Number | Applies the 'AllyChainKnockback' effect. |
| [`AllyDamageReaction`](./Enums.md#enum-allydamagereaction) | Enum | Applies the 'AllyDamageReaction' effect. |
| `AllyDamageReduction` | Number | Applies the 'AllyDamageReduction' effect. |
| [`AllyDodgeChanceAura`](#allydodgechanceaura) | Block | Applies or references the 'AllyDodgeChanceAura' effect/state. |
| [`AllyHealthRegenAura`](#allyhealthregenaura) | Block | Applies the 'AllyHealthRegenAura' effect. |
| [`AllyManaRegenAura`](#allymanaregenaura) | Block | Applies the 'AllyManaRegenAura' effect. |
| [`AllyMoveAbilityAura`](./Enums.md#enum-allymoveabilityaura) | Enum | Applies the 'AllyMoveAbilityAura' effect. |
| `AllyMultiplyKnockbackDamage` | Number | Applies the 'AllyMultiplyKnockbackDamage' effect. |
| `AllyMultiplyKnockbackDistance` | Number | Applies the 'AllyMultiplyKnockbackDistance' effect. |
| `AllyUncappedHPAura` | Number | Applies the 'AllyUncappedHPAura' effect. |
| `AlphaAllStatsUp` | Number | Applies or references the 'AlphaAllStatsUp' effect/state. |
| `AlphaCat` | Number | Applies or references the 'AlphaCat' effect/state. |
| `AlphaDodgeChance` | Number | Applies or references the 'AlphaDodgeChance' effect/state. |
| [`AlphaStatusOnTurnBegin`](#alphastatusonturnbegin) | Block | Grants a specific status effect to the 'Alpha' (the party leader) at the start of their turn. |
| `AlphaTurns` | Number | Applies the 'AlphaTurns' effect. |
| [`AlternateCraftingPools`](#alternatecraftingpools) | Block | Applies the 'AlternateCraftingPools' effect. |
| `AlwaysChosenForLevelUp` | Number | Applies or references the 'AlwaysChosenForLevelUp' effect/state. |
| `AlwaysHitDifferentTargets` | Number | Applies or references the 'AlwaysHitDifferentTargets' effect/state. |
| `Ammo` | Number | Applies or references the 'Ammo' effect/state. |
| `AmplifyKnockback` | Number | Applies the 'AmplifyKnockback' effect. |
| `AmplifyNegativeStatus` | Number | Applies the 'AmplifyNegativeStatus' effect. |
| `AmplifyPositiveStatus` | Number | Applies the 'AmplifyPositiveStatus' effect. |
| [`AmplifyStatus`](./Enums.md#enum-amplifystatus) | Enum | Applies the 'AmplifyStatus' effect. |
| `Angel` | Number | Applies or references the 'Angel' effect/state. |
| [`ApplyPassivesToSpawnerWhileAlive`](#applypassivestospawnerwhilealive) | Block | Grants nested passives to the entity that spawned this object, lasting only as long as this object remains alive. |
| [`ApplyStatusIfCrit`](#applystatusifcrit) | Block | Conditional trigger: Executes the nested logic only if the triggering action was a critical hit. |
| [`ApplyStatusesToRandomEnemiesEachTurn`](#applystatusestorandomenemieseachturn) | Block | Applies or references the 'ApplyStatusesToRandomEnemiesEachTurn' effect/state. |
| [`ApplyToRandomPartyMemberIfPossible`](#applytorandompartymemberifpossible) | Block | Redirects the nested effects to apply to a random living member of the player's party. |
| [`ApplyToSource`](#applytosource) | Block | Redirects the nested effects to apply to the caster/source of the ability instead of the target. |
| [`ArmorBreakOnHit`](#armorbreakonhit) | Block | Applies or references the 'ArmorBreakOnHit' effect/state. |
| `ArmorDodgeChance` | Number | Applies or references the 'ArmorDodgeChance' effect/state. |
| [`ArmorPickup`](#armorpickup) | Block | Pickup Logic: Defines what happens when an armor item is collected. |
| [`Autism`](#autism) | Block | Applies the 'Autism' effect. |
| `AutoCritLowDamage` | Number | Applies the 'AutoCritLowDamage' effect. |
| `AutoEquipConsumables` | Number | Applies or references the 'AutoEquipConsumables' effect/state. |
| `AutoReanimate` | Number | Applies the 'AutoReanimate' effect. |
| [`AutocastEachRound`](#autocasteachround) | Block | Forces the character to automatically cast a specific ability at the start of each combat round. |
| [`AutocastEachTurn`](./Enums.md#enum-autocasteachturn) | Enum | Applies the 'AutocastEachTurn' effect. |
| [`AutocastEachTurnBegin`](./Enums.md#enum-autocasteachturnbegin) | Enum | Applies the 'AutocastEachTurnBegin' effect. |
| `AvoidDamagingCharmedEnemies` | Number | Applies or references the 'AvoidDamagingCharmedEnemies' effect/state. |
| `AwardCoinsOnDeath` | Number | Applies or references the 'AwardCoinsOnDeath' effect/state. |
| `BackflipWhenTargeted` | Number | Reaction trigger: Executes a backflip dodge maneuver when targeted by an attack. |
| `BackstabAllDirections` | Number | Applies or references the 'BackstabAllDirections' effect/state. |
| `BackstabCritChance` | Number | Applies the 'BackstabCritChance' effect. |
| `BackstabFront` | Number |  |
| `BackstabImmunity` | Number | Applies or references the 'BackstabImmunity' effect/state. |
| `BackstabWeakness` | Number | Applies the 'BackstabWeakness' effect. |
| [`BaitAura`](#baitaura) | Block | Passive: Projects an aura that attracts specific enemy types (e.g., flies/maggots). |
| `BalanceStats` | Number | Applies or references the 'BalanceStats' effect/state. |
| [`BaseStatMultiply`](./Enums.md#enum-basestatmultiply) | Enum | Applies or references the 'BaseStatMultiply' effect/state. |
| `BasicAIDangerZone` | Number | Applies or references the 'BasicAIDangerZone' effect/state. |
| `BasicAttackAOEBonus` | Number | Applies the 'BasicAttackAOEBonus' effect. |
| `BasicAttackCantMiss` | Number |  |
| `BasicAttackCritChance` | Number | Applies the 'BasicAttackCritChance' effect. |
| `BasicAttackDamageMultiplier` | Number | Applies the 'BasicAttackDamageMultiplier' effect. |
| `BasicAttackStatusCarefulness` | Number | Applies the 'BasicAttackStatusCarefulness' effect. |
| [`BasicAttackStatusSwap`](./Arrays.md#array-basicattackstatusswap) | Array | Applies the 'BasicAttackStatusSwap' effect. |
| [`BattlefieldUniqueRandomPassive`](#battlefielduniquerandompassive) | Block | Map Rule: Grants a unique random passive modifier to the battlefield. |
| `BigSplashDamage` | Number | Applies the 'BigSplashDamage' effect. |
| [`Bird`](./Enums.md#enum-bird) | Enum | Applies or references the 'Bird' effect/state. |
| [`BirdRewards`](#birdrewards) | Block | Loot logic: Rewards dropped by bird-type enemies. |
| `BlackHolePassive` | Number | Applies or references the 'BlackHolePassive' effect/state. |
| [`BlacklistPickupType`](./Enums.md#enum-blacklistpickuptype) | Enum |  |
| `BlastResistance` | Number | Applies the 'BlastResistance' effect. |
| `Bleed` | Number | Applies or references the 'Bleed' effect/state. |
| `BleedThorns` | Number | Applies or references the 'BleedThorns' effect/state. |
| `BlessingOfPeace` | Number | Applies or references the 'BlessingOfPeace' effect/state. |
| `Blind` | Number |  |
| [`BloatEyePassive2`](./Enums.md#enum-bloateyepassive2) | Enum | Applies or references the 'BloatEyePassive2' effect/state. |
| `BlockAllDamage` | Number | Applies or references the 'BlockAllDamage' effect/state. |
| `BlockDamageUnderThreshold` | Number | Applies or references the 'BlockDamageUnderThreshold' effect/state. |
| `BlockNegativeStatus` | Number | Applies or references the 'BlockNegativeStatus' effect/state. |
| `BombBehavior` | Number | Applies or references the 'BombBehavior' effect/state. |
| `BoneArmorPassive` | Number | Applies or references the 'BoneArmorPassive' effect/state. |
| [`BonusAbility`](./Enums.md#enum-bonusability) | Enum | Applies the 'BonusAbility' effect. |
| [`BonusAbility_DelayedApplication`](./Enums.md#enum-bonusability_delayedapplication) | Enum | Applies or references the 'BonusAbility_DelayedApplication' effect/state. |
| `BonusDamage` | Number | Applies or references the 'BonusDamage' effect/state. |
| `BonusFoodEachBattle` | Number | Applies the 'BonusFoodEachBattle' effect. |
| `BonusHealthRegenBasedOnDex` | Number | Applies the 'BonusHealthRegenBasedOnDex' effect. |
| `BonusHealthRegenPerDisorder` | Number |  |
| `BonusKnockbackDamage` | Number | Applies or references the 'BonusKnockbackDamage' effect/state. |
| `BonusRangeBasedOnDex` | Number | Applies the 'BonusRangeBasedOnDex' effect. |
| [`BonusTurnPattern`](./Arrays.md#array-bonusturnpattern) | Array | Applies or references the 'BonusTurnPattern' effect/state. |
| [`BoobyTrapItems`](#boobytrapitems) | Block | Applies the 'BoobyTrapItems' effect. |
| `BoostAllyStatsOnDeath` | Number | Applies the 'BoostAllyStatsOnDeath' effect. |
| `BoostDamageAura` | Number | Applies the 'BoostDamageAura' effect. |
| `BoostDamageGlobalAura` | Number | Applies the 'BoostDamageGlobalAura' effect. |
| `BoostHeals` | Number | Applies or references the 'BoostHeals' effect/state. |
| `BoostRangeAura` | Number | Applies the 'BoostRangeAura' effect. |
| `BoostRangeGlobalAura` | Number | Applies the 'BoostRangeGlobalAura' effect. |
| `BoostReceivedHealing` | Number | Applies or references the 'BoostReceivedHealing' effect/state. |
| `BoostWeaponDamage` | Number | Applies the 'BoostWeaponDamage' effect. |
| [`BossRewards`](#bossrewards) | Block | Loot logic: Rewards dropped upon defeating a boss. |
| [`BounceObject`](./Enums.md#enum-bounceobject) | Enum | Spawns a physics object that visually bounces off the target. |
| [`BouncyProjectiles`](#bouncyprojectiles) | Block | Applies the 'BouncyProjectiles' effect. |
| `Bounty` | Number | Applies the 'Bounty' effect. |
| `Brace` | Number | Applies or references the 'Brace' effect/state. |
| `BraceForEachNeighboringEnemy` | Number | Applies the 'BraceForEachNeighboringEnemy' effect. |
| `BreakAtAux` | Number | Applies or references the 'BreakAtAux' effect/state. |
| [`BreakOnElement`](./Enums.md#enum-breakonelement) | Enum | Applies or references the 'BreakOnElement' effect/state. |
| `BreakWhenNoShield` | Number | Applies or references the 'BreakWhenNoShield' effect/state. |
| `Brittle` | Number | Applies or references the 'Brittle' effect/state. |
| `BrittleCharismaUp` | Number | Applies or references the 'BrittleCharismaUp' effect/state. |
| `BrittleConstitutionUp` | Number | Applies or references the 'BrittleConstitutionUp' effect/state. |
| `BrittleDexterityUp` | Number | Applies or references the 'BrittleDexterityUp' effect/state. |
| [`BrittleDuringElement`](./Enums.md#enum-brittleduringelement) | Enum | Applies or references the 'BrittleDuringElement' effect/state. |
| `BrittleIntelligenceUp` | Number | Applies or references the 'BrittleIntelligenceUp' effect/state. |
| `BrittleLuckUp` | Number | Applies or references the 'BrittleLuckUp' effect/state. |
| `BrittleSpeedUp` | Number | Applies or references the 'BrittleSpeedUp' effect/state. |
| `BrittleStrengthUp` | Number | Applies or references the 'BrittleStrengthUp' effect/state. |
| `Bruise` | Number | Applies or references the 'Bruise' effect/state. |
| [`Buddy`](./Enums.md#enum-buddy) | Enum | Character Form / AI State: Behavior and stats for the 'Buddy' familiar state. |
| `BuffImmunity` | Number | Applies or references the 'BuffImmunity' effect/state. |
| [`BungaCheers`](#bungacheers) | Block | Animation/AI State: Bunga cheering animation logic. |
| [`BungaEntrance`](#bungaentrance) | Block | Animation/AI State: Bunga entering the arena. |
| `BurgleCoin` | Number | Applies the 'BurgleCoin' effect. |
| `Burn` | Number | Applies or references the 'Burn' effect/state. |
| `CCImmunity` | Number | Applies the 'CCImmunity' effect. |
| `CanLevelUpWhenDead` | Number | Applies or references the 'CanLevelUpWhenDead' effect/state. |
| [`CanMutateTo`](./Enums.md#enum-canmutateto) | Enum | Applies or references the 'CanMutateTo' effect/state. |
| `CanRemoveCursedItems` | Number |  |
| `CanShield` | Number | Applies or references the 'CanShield' effect/state. |
| `CantCatchDiseases` | Number | Applies or references the 'CantCatchDiseases' effect/state. |
| `CantDodge` | Number | Applies the 'CantDodge' effect. |
| `CantSpreadDiseases` | Number | Applies or references the 'CantSpreadDiseases' effect/state. |
| `CapBasicAttackDamage` | Number | Applies or references the 'CapBasicAttackDamage' effect/state. |
| `CapDamageFromAllies` | Number | Applies the 'CapDamageFromAllies' effect. |
| `CapMovementAbilityRange` | Number | Applies or references the 'CapMovementAbilityRange' effect/state. |
| `CapReceivedDamage` | Number | Applies or references the 'CapReceivedDamage' effect/state. |
| `CapTechSpent` | Number | Applies the 'CapTechSpent' effect. |
| `CaptureFamiliar` | Number | Applies or references the 'CaptureFamiliar' effect/state. |
| [`CatAPultAnimation`](#catapultanimation) | Block | Applies the 'CatAPultAnimation' effect. |
| [`CatPartsSizeScale`](#catpartssizescale) | Block | Applies or references the 'CatPartsSizeScale' effect/state. |
| [`CatPartsTransform`](#catpartstransform) | Block | Visual: Transforms specific body parts of the character. |
| `CatchBoomerang` | Number | Applies or references the 'CatchBoomerang' effect/state. |
| [`CatchProjectiles`](#catchprojectiles) | Block | Applies or references the 'CatchProjectiles' effect/state. |
| [`CaveFamilyEnrage`](#cavefamilyenrage) | Block | AI Trigger: Enrage logic triggered when a cave family member is killed. |
| `CaveWomanBirthControl` | Number | Applies or references the 'CaveWomanBirthControl' effect/state. |
| [`CerberubsAggroTargetBehavior`](#cerberubsaggrotargetbehavior) | Block | AI Logic: Custom aggro targeting rules for Cerberubs. |
| `ChainKnockback` | Number | Applies the 'ChainKnockback' effect. |
| `ChanceToAmbush` | Number | Applies or references the 'ChanceToAmbush' effect/state. |
| [`ChanceToBackflip`](#chancetobackflip) | Block | Applies or references the 'ChanceToBackflip' effect/state. |
| `ChanceToBlock` | Number | Applies or references the 'ChanceToBlock' effect/state. |
| `ChanceToBlockAndCounter` | Number | Applies or references the 'ChanceToBlockAndCounter' effect/state. |
| `ChanceToBreak` | Number | Applies the 'ChanceToBreak' effect. |
| `ChanceToDisableActionsIfNotCharmed` | Number | Applies or references the 'ChanceToDisableActionsIfNotCharmed' effect/state. |
| [`ChanceToForceEvent`](#chancetoforceevent) | Block | Applies or references the 'ChanceToForceEvent' effect/state. |
| [`ChanceToFormChangeOnAbilityDamage`](#chancetoformchangeonabilitydamage) | Block | Reaction: Probability to change forms when taking ability damage. |
| `ChanceToRevive` | Number | Applies or references the 'ChanceToRevive' effect/state. |
| [`ChanceToSpitOnDamage`](#chancetospitondamage) | Block | Reaction: Probability to use a spit counter-attack when damaged. |
| `ChangeTauntPriority` | Number | Applies the 'ChangeTauntPriority' effect. |
| [`ChangeTile`](./Enums.md#enum-changetile) | Enum |  |
| [`ChangeTileOnDeath`](./Enums.md#enum-changetileondeath) | Enum | Applies or references the 'ChangeTileOnDeath' effect/state. |
| [`ChangeTileOnPop`](./Enums.md#enum-changetileonpop) | Enum | Applies or references the 'ChangeTileOnPop' effect/state. |
| `ChangeTileUnderCharacterAtStart` | Enum/String | Applies or references the 'ChangeTileUnderCharacterAtStart' effect/state. |
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum | Applies or references the 'ChangeTilesUnder' effect/state. |
| [`ChaosBossFormChangeGuide`](#chaosbossformchangeguide) | Block | Boss Logic: Maps the form transition phases for the Chaos Boss. |
| [`ChaosBossPieces`](#chaosbosspieces) | Block | Boss Logic: Defines the separate destructible pieces of the Chaos Boss. |
| [`ChaosHeadDropIn`](#chaosheaddropin) | Block | Boss Logic: Drop-in attack/animation for the Chaos Head. |
| [`CharacterLightSource`](#characterlightsource) | Block | Visual: Attaches a dynamic lighting source to the character. |
| `Charge` | Number | Applies or references the 'Charge' effect/state. |
| [`ChargeSpiritBombAura`](./Enums.md#enum-chargespiritbombaura) | Enum | Applies or references the 'ChargeSpiritBombAura' effect/state. |
| `CharismaIsMaxStat` | Number | Applies or references the 'CharismaIsMaxStat' effect/state. |
| `CharismaUp` | Number | Applies or references the 'CharismaUp' effect/state. |
| `CharmAllFlies` | Number | Applies the 'CharmAllFlies' effect. |
| `CharmImmunity` | Number | Applies or references the 'CharmImmunity' effect/state. |
| `Charmed` | Number | Applies the 'Charmed' effect. |
| [`CherubimReaction`](#cherubimreaction) | Block | Reaction: Custom reaction triggers for Cherubim enemies. |
| [`ClassManaCostReduction`](#classmanacostreduction) | Block | Applies or references the 'ClassManaCostReduction' effect/state. |
| `Cleanse` | Number |  |
| `Cleave` | Number | Causes the attack to hit adjacent enemies alongside the primary target. |
| [`CobraReflex`](./Enums.md#enum-cobrareflex) | Enum | Applies the 'CobraReflex' effect. |
| `CoinPickup` | Number | Applies or references the 'CoinPickup' effect/state. |
| `CoinsAddDamage` | Number | Applies the 'CoinsAddDamage' effect. |
| `CollectPickupsOnBattleEnd` | Number | Applies the 'CollectPickupsOnBattleEnd' effect. |
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
| `Conductor` | Number | Applies the 'Conductor' effect. |
| `ConductorManaRegen` | Number | Applies the 'ConductorManaRegen' effect. |
| `Confusion` | Number | Applies the 'Confusion' effect. |
| [`ConfusionEffectOnTaggedAbilities`](./Enums.md#enum-confusioneffectontaggedabilities) | Enum | Applies the 'ConfusionEffectOnTaggedAbilities' effect. |
| [`ConjureBonusAbility`](./Enums.md#enum-conjurebonusability) | Enum |  |
| `ConjureCastSpellsForAllies` | Number | Applies the 'ConjureCastSpellsForAllies' effect. |
| `ConstitutionUp` | Number | Applies or references the 'ConstitutionUp' effect/state. |
| `ConsumableEffectsMultiplierBonus` | Number | Applies the 'ConsumableEffectsMultiplierBonus' effect. |
| `ConsumablesInfiniteRange` | Number | Applies the 'ConsumablesInfiniteRange' effect. |
| `ConsumablesMeleeRange` | Number | Applies the 'ConsumablesMeleeRange' effect. |
| [`Consumed`](#consumed) | Block | State triggered when the entity is eaten/consumed. |
| [`ConvertDamageToScaledStatus`](#convertdamagetoscaledstatus) | Block | Applies or references the 'ConvertDamageToScaledStatus' effect/state. |
| `CopyBasicAttackEffects` | Number | Applies or references the 'CopyBasicAttackEffects' effect/state. |
| `CopyCatPassive_Initializer` | Number | Applies or references the 'CopyCatPassive_Initializer' effect/state. |
| `CopyPassiveSlot` | Number | Applies or references the 'CopyPassiveSlot' effect/state. |
| `CountAsCorpse` | Number | Applies or references the 'CountAsCorpse' effect/state. |
| [`CounterAttack`](./Enums.md#enum-counterattack) | Enum | Reaction: Executes a counter-attack ability when hit. |
| [`CounterAttackAfterEnemyCastSpell`](./Enums.md#enum-counterattackafterenemycastspell) | Enum | Applies or references the 'CounterAttackAfterEnemyCastSpell' effect/state. |
| `CounterNextAttacks` | Number | Applies or references the 'CounterNextAttacks' effect/state. |
| [`Craft`](#craft) | Block | Synthesizes or spawns a new item from a specific pool. |
| [`CreateGlobalModifiers`](#createglobalmodifiers) | Block | Encounter Rule: Generates map-wide modifiers. |
| `CritChanceUp` | Number | Applies the 'CritChanceUp' effect. |
| [`CritsApplyStatus`](#critsapplystatus) | Block | Applies the 'CritsApplyStatus' effect. |
| `CrowAttackLink` | Number | Applies or references the 'CrowAttackLink' effect/state. |
| [`CureDisease`](#curedisease) | Block | Applies the 'CureDisease' effect. |
| `CurrentWeaponDamageUp` | Number | Applies the 'CurrentWeaponDamageUp' effect. |
| [`CyborgTurns`](#cyborgturns) | Block |  |
| `DamageEnemiesOnHeal` | Number | Combat Trigger: Deals damage to enemies on heal. |
| `DamageEnemiesOnKill` | Number | Combat Trigger: Deals damage to enemies on kill. |
| `DamageFromBehindOnly` | Number | Applies or references the 'DamageFromBehindOnly' effect/state. |
| [`DamageIfDidntUseSpecificAbility`](#damageifdidntusespecificability) | Block | Combat Trigger: Deals damage to if didnt use specific ability. |
| [`DamageNeighborTilesWhenCastSpell`](#damageneighbortileswhencastspell) | Block | Combat Trigger: Deals damage to neighbor tiles when cast spell. |
| [`DamageNeighborsAfterMove`](#damageneighborsaftermove) | Block |  |
| [`DamageNeighborsOnEndMove`](#damageneighborsonendmove) | Block | Combat Trigger: Deals damage to neighbors on end move. |
| `DamageOrHealConditionally` | Number | Applies or references the 'DamageOrHealConditionally' effect/state. |
| [`DamageReductionAura`](#damagereductionaura) | Block | Combat Trigger: Deals damage to reduction aura. |
| `DamageUp` | Number | Applies or references the 'DamageUp' effect/state. |
| [`DeadAltAbility`](./Enums.md#enum-deadaltability) | Enum | Applies or references the 'DeadAltAbility' effect/state. |
| `DeathChill` | Number | Applies the 'DeathChill' effect. |
| [`DeathRattle`](./Enums.md#enum-deathrattle) | Enum | Event Trigger: Executes logic or abilities exactly when the character dies. |
| [`DeathRattleRevive`](#deathrattlerevive) | Block | Event Trigger: Revives the character immediately upon death. |
| `DebuffImmunity` | Number | Applies or references the 'DebuffImmunity' effect/state. |
| `DejaVu` | Number | Applies the 'DejaVu' effect. |
| [`DelayedAutoRevive`](#delayedautorevive) | Block | Applies or references the 'DelayedAutoRevive' effect/state. |
| `DelayedPain` | Number | Applies or references the 'DelayedPain' effect/state. |
| `DemonicGlyphFrames` | Number | Applies or references the 'DemonicGlyphFrames' effect/state. |
| `DemonicGlyphStealer` | Number | Applies or references the 'DemonicGlyphStealer' effect/state. |
| [`DepressionAura`](#depressionaura) | Block |  |
| [`DestroyEquipmentAndAttachParasite`](#destroyequipmentandattachparasite) | Block | Removes an equipped item and replaces it with a parasite from a specified pool. |
| `DestroyTrinket` | Number | Applies or references the 'DestroyTrinket' effect/state. |
| `DexterityUp` | Number | Applies or references the 'DexterityUp' effect/state. |
| [`Diabetes`](#diabetes) | Block | Applies the 'Diabetes' effect. |
| [`DiceBehavior`](#dicebehavior) | Block | AI Logic: Custom behavior for Dice enemies. |
| [`DicerArt`](./Arrays.md#array-dicerart) | Array | Applies or references the 'DicerArt' effect/state. |
| `DieWhenOnlyGolemsLeft` | Number | Applies or references the 'DieWhenOnlyGolemsLeft' effect/state. |
| `DieWhenSpawnerDies` | Number | Applies or references the 'DieWhenSpawnerDies' effect/state. |
| [`DiesToElement`](./Enums.md#enum-diestoelement) | Enum | Vulnerability: Character dies instantly if hit by this element. |
| [`DiesToPiercingAndSpikes`](#diestopiercingandspikes) | Block | Vulnerability: Character dies instantly if hit by piercing attacks or spikes. |
| [`DigestDeadBodies`](./Enums.md#enum-digestdeadbodies) | Enum | Applies or references the 'DigestDeadBodies' effect/state. |
| `DiminishingHealthRegen` | Number | Applies or references the 'DiminishingHealthRegen' effect/state. |
| `DirtyClaws` | Number | Applies the 'DirtyClaws' effect. |
| [`DisableAbilities`](./Enums.md#enum-disableabilities) | Enum | Applies or references the 'DisableAbilities' effect/state. |
| [`DisableAbilitiesWithTag`](./Enums.md#enum-disableabilitieswithtag) | Enum |  |
| `DisablePassiveSlot` | Number | Applies or references the 'DisablePassiveSlot' effect/state. |
| `DisableSpells` | Number | Applies or references the 'DisableSpells' effect/state. |
| `Disguised` | Number | Applies or references the 'Disguised' effect/state. |
| [`DisguisedTrapper`](./Enums.md#enum-disguisedtrapper) | Enum | Applies or references the 'DisguisedTrapper' effect/state. |
| `DisplayBuddyCatOnSpawn` | Number | Applies or references the 'DisplayBuddyCatOnSpawn' effect/state. |
| [`DisplayDangerAOE`](./Enums.md#enum-displaydangeraoe) | Enum | Applies or references the 'DisplayDangerAOE' effect/state. |
| `DissuadeInstakills` | Number | Applies or references the 'DissuadeInstakills' effect/state. |
| [`DistanceBonusDamage`](#distancebonusdamage) | Block | Applies the 'DistanceBonusDamage' effect. |
| [`Divide4OnDeath`](./Enums.md#enum-divide4ondeath) | Enum | Applies or references the 'Divide4OnDeath' effect/state. |
| `DivineShield` | Number | Applies or references the 'DivineShield' effect/state. |
| `DivineShieldPickup` | Number | Applies or references the 'DivineShieldPickup' effect/state. |
| [`DoDamage`](#dodamage) | Block | Explicitly triggers a secondary damage instance independent of the main attack. |
| `DodgeChance` | Number |  |
| `DodgeChanceWithBlindSpot` | Number | Applies or references the 'DodgeChanceWithBlindSpot' effect/state. |
| `DodgeChance_Status` | Number | Applies or references the 'DodgeChance_Status' effect/state. |
| [`DodgeWhenTargeted`](#dodgewhentargeted) | Block | Reaction: Executes a dodge maneuver when targeted. |
| `Doomed` | Number | Applies the 'Doomed' effect. |
| `DoubleCastSpellIfManaCostUnderThreshold` | Number | Applies or references the 'DoubleCastSpellIfManaCostUnderThreshold' effect/state. |
| `DoubleCastSpellThisTurn` | Number | Applies or references the 'DoubleCastSpellThisTurn' effect/state. |
| `DoubleCastSpellsEachTurn_Status` | Number |  |
| [`DoubleCastTaggedSpells`](./Enums.md#enum-doublecasttaggedspells) | Enum | Applies or references the 'DoubleCastTaggedSpells' effect/state. |
| `DoubleCastWeapons` | Number | Applies the 'DoubleCastWeapons' effect. |
| `DoubleReceivedNegativeStatus` | Number | Applies or references the 'DoubleReceivedNegativeStatus' effect/state. |
| `DoubleReceivedPositiveStatus` | Number | Applies or references the 'DoubleReceivedPositiveStatus' effect/state. |
| [`DownRankAIIfWeaponUsable`](./Enums.md#enum-downrankaiifweaponusable) | Enum | Applies or references the 'DownRankAIIfWeaponUsable' effect/state. |
| `DrinkWater` | Number | Applies or references the 'DrinkWater' effect/state. |
| [`DropAsFamiliarOnArmorBreak`](./Enums.md#enum-dropasfamiliaronarmorbreak) | Enum | Applies or references the 'DropAsFamiliarOnArmorBreak' effect/state. |
| [`DropAsFamiliarOnTookDamage`](./Enums.md#enum-dropasfamiliarontookdamage) | Enum | Applies or references the 'DropAsFamiliarOnTookDamage' effect/state. |
| [`DropSoulJarOnDeath`](./Enums.md#enum-dropsouljarondeath) | Enum | Applies or references the 'DropSoulJarOnDeath' effect/state. |
| `Drowsy` | Number |  |
| `DukeOfFlies` | Number | Applies the 'DukeOfFlies' effect. |
| [`DurabilityTransform`](#durabilitytransform) | Block | Applies or references the 'DurabilityTransform' effect/state. |
| `DustCloudBehavior` | Number | Applies or references the 'DustCloudBehavior' effect/state. |
| `Dybbuk1HPTracker` | Number | Applies or references the 'Dybbuk1HPTracker' effect/state. |
| [`DybbukPossessionFallback`](#dybbukpossessionfallback) | Block | Logic: Fallback state when a Dybbuk possession fails. |
| [`Dyslexia`](./Arrays.md#array-dyslexia) | Array | Applies the 'Dyslexia' effect. |
| [`EMP`](#emp) | Block | Applies the 'EMP' effect. |
| `EachSpellFreeAtFullMana` | Number | Applies the 'EachSpellFreeAtFullMana' effect. |
| `ElectricArcs` | Number | Applies or references the 'ElectricArcs' effect/state. |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum | Applies or references the 'ElementImmune' effect/state. |
| [`ElementWeakness`](./Enums.md#enum-elementweakness) | Enum | Applies or references the 'ElementWeakness' effect/state. |
| [`ElementalAttunement`](#elementalattunement) | Block | Applies the 'ElementalAttunement' effect. |
| [`ElementalManaCostReduction`](#elementalmanacostreduction) | Block | Applies the 'ElementalManaCostReduction' effect. |
| [`EliteFlatTint`](./Arrays.md#array-eliteflattint) | Array |  |
| [`EliteParticle`](./Enums.md#enum-eliteparticle) | Enum |  |
| [`EliteTint`](./Arrays.md#array-elitetint) | Array |  |
| [`Else`](#else) | Block | Fallback block that executes if the preceding `Conditional_` block evaluated to false. |
| `Empath` | Number | Applies the 'Empath' effect. |
| `EmptyMana` | Number | Applies the 'EmptyMana' effect. |
| `EnemiesGetPickupsKnockedOut` | Number | Applies the 'EnemiesGetPickupsKnockedOut' effect. |
| `EnergyStorm` | Number | Applies the 'EnergyStorm' effect. |
| `EnrageOnDamage` | Number | Applies or references the 'EnrageOnDamage' effect/state. |
| [`EquipPermanentItem`](./Enums.md#enum-equippermanentitem) | Enum | Applies the 'EquipPermanentItem' effect. |
| [`EquipRandomTemporaryItemFromPool`](./Enums.md#enum-equiprandomtemporaryitemfrompool) | Enum |  |
| [`EquipTemporaryItem`](./Enums.md#enum-equiptemporaryitem) | Enum | Applies the 'EquipTemporaryItem' effect. |
| `EquipmentPassiveMultiplierBonus` | Number | Applies the 'EquipmentPassiveMultiplierBonus' effect. |
| `EquipmentSetBonusBonus` | Number | Applies the 'EquipmentSetBonusBonus' effect. |
| `EraseSpawnCoins` | Number | Applies or references the 'EraseSpawnCoins' effect/state. |
| [`EscapeSequence`](#escapesequence) | Block | Applies the 'EscapeSequence' effect. |
| [`Eternal`](#eternal) | Block | Applies the 'Eternal' effect. |
| `EventBounterHunterPassive` | Number | Applies or references the 'EventBounterHunterPassive' effect/state. |
| [`ExcludeFromEvents`](./Enums.md#enum-excludefromevents) | Enum | Applies or references the 'ExcludeFromEvents' effect/state. |
| `ExhaustionRoundChange` | Number | Applies the 'ExhaustionRoundChange' effect. |
| `ExpireOnSpawnerTurnEnd` | Number | Applies or references the 'ExpireOnSpawnerTurnEnd' effect/state. |
| `ExplodeOverkilledEnemies` | Number | Applies the 'ExplodeOverkilledEnemies' effect. |
| `ExplosionImmunity` | Number | Applies or references the 'ExplosionImmunity' effect/state. |
| `ExtraBasicAttacks` | Number | Applies the 'ExtraBasicAttacks' effect. |
| `ExtraBasicAttacks_Status` | Number | Applies or references the 'ExtraBasicAttacks_Status' effect/state. |
| `ExtraBasicMoves_Status` | Number | Applies or references the 'ExtraBasicMoves_Status' effect/state. |
| `ExtraDispersedTurns` | Number | Applies or references the 'ExtraDispersedTurns' effect/state. |
| `ExtraInjuryOnDeath` | Number | Applies the 'ExtraInjuryOnDeath' effect. |
| `ExtraMovePoints` | Number | Applies the 'ExtraMovePoints' effect. |
| [`ExtraStatusWhenDealingDamage`](#extrastatuswhendealingdamage) | Block | Applies or references the 'ExtraStatusWhenDealingDamage' effect/state. |
| `ExtraTrinketUses` | Number | Applies or references the 'ExtraTrinketUses' effect/state. |
| [`ExtraTurnsPerTaggedUnit`](./Enums.md#enum-extraturnspertaggedunit) | Enum | Applies or references the 'ExtraTurnsPerTaggedUnit' effect/state. |
| `ExtraWeaponAttacks` | Number | Applies the 'ExtraWeaponAttacks' effect. |
| `FaceArmorPassiveMultiplierBonus` | Number | Applies or references the 'FaceArmorPassiveMultiplierBonus' effect/state. |
| `FaceAway` | Number | Applies the 'FaceAway' effect. |
| [`FaceAwayLastDamage`](#faceawaylastdamage) | Block | Reaction: Forces the character to face away from the last damage source. |
| `FaceLastDamage` | Number | Reaction: Forces the character to face towards the last damage source. |
| `FaceShield` | Number | Applies or references the 'FaceShield' effect/state. |
| `FadeInsteadOfDie` | Number | Applies or references the 'FadeInsteadOfDie' effect/state. |
| [`FamiliarBonusAbility`](./Enums.md#enum-familiarbonusability) | Enum | Applies the 'FamiliarBonusAbility' effect. |
| `FamiliarSecondaryDamageImmunity` | Number | Applies the 'FamiliarSecondaryDamageImmunity' effect. |
| `Fear` | Number | Applies or references the 'Fear' effect/state. |
| `Fights` | Number | Applies or references the 'Fights' effect/state. |
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
| `FistOfFateUniqueEnemyTracker` | Number | Applies or references the 'FistOfFateUniqueEnemyTracker' effect/state. |
| `Flammable` | Number | Applies or references the 'Flammable' effect/state. |
| `FlatHealWhenDealDamage` | Number |  |
| `FlatLeech` | Number |  |
| `FlingObjectsOnTop` | Number | Applies or references the 'FlingObjectsOnTop' effect/state. |
| `FlippedFacingForceAttack` | Number | Applies the 'FlippedFacingForceAttack' effect. |
| `FlowerPowerAuraBrace` | Number | Applies the 'FlowerPowerAuraBrace' effect. |
| `FlowerPowerAuraStrength` | Number | Applies the 'FlowerPowerAuraStrength' effect. |
| `FlowersOnEndTurn` | Number | Applies or references the 'FlowersOnEndTurn' effect/state. |
| [`FlushmasterCelebration`](./Enums.md#enum-flushmastercelebration) | Enum | Applies or references the 'FlushmasterCelebration' effect/state. |
| `FlyDamageIncrease` | Number | Applies the 'FlyDamageIncrease' effect. |
| `Flying` | Number | Applies or references the 'Flying' effect/state. |
| [`FollowUp`](./Enums.md#enum-followup) | Enum | Applies the 'FollowUp' effect. |
| `ForceAttack` | Number | Forces the character to execute an immediate attack. |
| `ForceDodgeEverything` | Number | Applies or references the 'ForceDodgeEverything' effect/state. |
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
| `Fragile` | Number | Applies or references the 'Fragile' effect/state. |
| [`FragileDuringElement`](./Enums.md#enum-fragileduringelement) | Enum | Applies or references the 'FragileDuringElement' effect/state. |
| `FrankBolts` | Number | Applies or references the 'FrankBolts' effect/state. |
| `FreeFirstCast` | Number | Applies or references the 'FreeFirstCast' effect/state. |
| `FreeFirstCastAndAfterSpendMana` | Number | Applies or references the 'FreeFirstCastAndAfterSpendMana' effect/state. |
| `FreeFirstCastEachMatch` | Number | Applies or references the 'FreeFirstCastEachMatch' effect/state. |
| [`FreePathfindElement`](./Enums.md#enum-freepathfindelement) | Enum | Applies the 'FreePathfindElement' effect. |
| `FreeSpellsAtFullMana` | Number | Applies the 'FreeSpellsAtFullMana' effect. |
| `Freeze` | Number | Applies the 'Freeze' effect. |
| `FreezePiercing` | Number | Applies the 'FreezePiercing' effect. |
| `FrontstabBasicAttackCritChance` | Number | Applies the 'FrontstabBasicAttackCritChance' effect. |
| `FrontstabCritChance` | Number | Applies the 'FrontstabCritChance' effect. |
| `FullBlockEverything` | Number | Applies or references the 'FullBlockEverything' effect/state. |
| `FullBlockEverythingTo0Damage` | Number | Applies or references the 'FullBlockEverythingTo0Damage' effect/state. |
| `FullHeal` | Number | Applies the 'FullHeal' effect. |
| `FullHealthAllStatsUp` | Number | Applies the 'FullHealthAllStatsUp' effect. |
| `FullHealthCritChance` | Number | Applies the 'FullHealthCritChance' effect. |
| `FullHealthManaRegen` | Number | Applies the 'FullHealthManaRegen' effect. |
| `FullPower` | Number | Applies the 'FullPower' effect. |
| [`FurnitureStats`](#furniturestats) | Block | Applies the 'FurnitureStats' effect. |
| `GainCoins` | Number | Applies or references the 'GainCoins' effect/state. |
| [`GainCoinsRange`](#gaincoinsrange) | Block | Grants the player a randomized amount of coins within a min/max range. |
| [`GainDisorder`](./Enums.md#enum-gaindisorder) | Enum | Applies or references the 'GainDisorder' effect/state. |
| [`GainDisorderFromPool`](#gaindisorderfrompool) | Block | Logic: Applies a negative mutation/disorder from a specific pool. |
| `GainExtraShield` | Number | Applies the 'GainExtraShield' effect. |
| `GainManaWhenAnythingDies` | Number |  |
| `GasCanBehavior` | Number | Applies or references the 'GasCanBehavior' effect/state. |
| `GasCloudBehavior2` | Number | Applies or references the 'GasCloudBehavior2' effect/state. |
| `GeminiTwin` | Number | Applies or references the 'GeminiTwin' effect/state. |
| `GlobalFamiliarDamageBoost` | Number |  |
| `GlobalFamiliarMoveBoost` | Number |  |
| [`GlobalFlowerTrapperAura`](#globalflowertrapperaura) | Block |  |
| `GlobalManaBurnAura` | Number |  |
| `GlobalManaDrainAura` | Number | Applies or references the 'GlobalManaDrainAura' effect/state. |
| [`GlobalMeleeRevengeDamage`](#globalmeleerevengedamage) | Block | Applies or references the 'GlobalMeleeRevengeDamage' effect/state. |
| `GoopImmunity` | Number | Applies or references the 'GoopImmunity' effect/state. |
| `GoopWalk` | Number | Applies or references the 'GoopWalk' effect/state. |
| `GrassTileHealing` | Number | Applies the 'GrassTileHealing' effect. |
| [`GravityWell`](#gravitywell) | Block | Applies the 'GravityWell' effect. |
| [`GroundFlopper`](./Enums.md#enum-groundflopper) | Enum | Applies or references the 'GroundFlopper' effect/state. |
| `GuillotinaDeathHead` | Number | Applies or references the 'GuillotinaDeathHead' effect/state. |
| [`HPAltStates`](#hpaltstates) | Block | Visual: Alternative sprite states based on current health. |
| `HPGainBlock` | Number | Applies or references the 'HPGainBlock' effect/state. |
| [`HarpoonTrapPassive`](./Enums.md#enum-harpoontrappassive) | Enum | Applies or references the 'HarpoonTrapPassive' effect/state. |
| `HeadArmorPassiveMultiplierBonus` | Number | Applies or references the 'HeadArmorPassiveMultiplierBonus' effect/state. |
| `HealAndOverhealToShield` | Number | Applies the 'HealAndOverhealToShield' effect. |
| `HealAtStart` | Number | Applies the 'HealAtStart' effect. |
| `HealDamagesEnemies` | Number | Applies the 'HealDamagesEnemies' effect. |
| [`HealNeighborsEachTurn`](#healneighborseachturn) | Block | Passive: Restores health to adjacent allies at the start of the turn. |
| `HealingAura` | Number | Applies the 'HealingAura' effect. |
| `HealsAlsoRegenMana` | Number | Applies the 'HealsAlsoRegenMana' effect. |
| `HealsCanRevive` | Number | Applies the 'HealsCanRevive' effect. |
| `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. |
| [`HealthMultiplier`](./Enums.md#enum-healthmultiplier) | Enum |  |
| [`HealthPickup`](#healthpickup) | Block | Pickup Logic: Defines what happens when a health item is collected. |
| `HealthRegenUp` | Number | Applies or references the 'HealthRegenUp' effect/state. |
| `Hex` | Number | Applies or references the 'Hex' effect/state. |
| `HiddenDoomed` | Number | Applies or references the 'HiddenDoomed' effect/state. |
| [`HideEquipment`](./Enums.md#enum-hideequipment) | Enum | Applies or references the 'HideEquipment' effect/state. |
| `HideSomeHudStuff` | Number | Applies or references the 'HideSomeHudStuff' effect/state. |
| [`HitlerExecute`](#hitlerexecute) | Block | Boss Logic: Specific execution or ultimate attack state. |
| `HolyDamageMultiplierBonus` | Number | Applies the 'HolyDamageMultiplierBonus' effect. |
| `HolyShieldTransferToSpawner` | Number | Applies the 'HolyShieldTransferToSpawner' effect. |
| [`HolyShieldTransferToTaggedMinions`](./Enums.md#enum-holyshieldtransfertotaggedminions) | Enum | Applies the 'HolyShieldTransferToTaggedMinions' effect. |
| `HouseFoodRequirementMultiplier` | Number |  |
| `Hypomania` | Number | Applies the 'Hypomania' effect. |
| `IceBlockBehavior` | Number | Applies or references the 'IceBlockBehavior' effect/state. |
| `IgnoreTiles` | Number |  |
| `IllusionTint` | Number | Applies or references the 'IllusionTint' effect/state. |
| [`ImmediateAbilityReaction`](./Enums.md#enum-immediateabilityreaction) | Enum | Reaction: Executes an ability instantly, interrupting the current sequence. |
| [`ImmediateUseAbility`](./Enums.md#enum-immediateuseability) | Enum | Applies or references the 'ImmediateUseAbility' effect/state. |
| `Immobile` | Number | Applies the 'Immobile' effect. |
| `ImmobilePassive` | Number | Applies or references the 'ImmobilePassive' effect/state. |
| `ImmortalLeeches` | Number | Applies the 'ImmortalLeeches' effect. |
| [`IncAuxCounterClamped`](#incauxcounterclamped) | Block | Increments a generic auxiliary counter on the character, capped by a maximum value. |
| `IncreaseExplosionDamage` | Number | Applies the 'IncreaseExplosionDamage' effect. |
| `IncreaseExplosionSize` | Number | Applies or references the 'IncreaseExplosionSize' effect/state. |
| `IncreaseHealingSpellRange` | Number | Applies the 'IncreaseHealingSpellRange' effect. |
| `IncreaseItemUsesOnEquip` | Number | Applies the 'IncreaseItemUsesOnEquip' effect. |
| `IncreaseSpellRange` | Number | Applies or references the 'IncreaseSpellRange' effect/state. |
| `Infested` | Number | Applies or references the 'Infested' effect/state. |
| [`InfiniteRebirth`](#infiniterebirth) | Block | Applies the 'InfiniteRebirth' effect. |
| `InheritSpawnerStats` | Number | Applies or references the 'InheritSpawnerStats' effect/state. |
| `InjuryImmunity` | Number | Applies or references the 'InjuryImmunity' effect/state. |
| [`InnateElement`](./Enums.md#enum-innateelement) | Enum | Applies the 'InnateElement' effect. |
| `InsertIntoBackgroundPlaceholder` | Number | Applies or references the 'InsertIntoBackgroundPlaceholder' effect/state. |
| [`Instakill`](./Arrays.md#array-instakill) | Array |  |
| `IntelligenceUp` | Number | Applies or references the 'IntelligenceUp' effect/state. |
| `InterchangeDisabler` | Number | Applies or references the 'InterchangeDisabler' effect/state. |
| `InvertBrainFaction` | Number | Applies the 'InvertBrainFaction' effect. |
| [`ItemAuxTransform`](#itemauxtransform) | Block | Applies or references the 'ItemAuxTransform' effect/state. |
| `JesterLevelUpRerolls` | Number | Applies or references the 'JesterLevelUpRerolls' effect/state. |
| [`JohnnyNeedsWashing`](#johnnyneedswashing) | Block | Character Form: Behavior and stats for the 'JohnnyNeedsWashing' state. |
| [`JohnnyWasher`](./Enums.md#enum-johnnywasher) | Enum | Applies or references the 'JohnnyWasher' effect/state. |
| `KaijuKnockbackImmune` | Number | Applies or references the 'KaijuKnockbackImmune' effect/state. |
| [`KaijuWinCon`](./Enums.md#enum-kaijuwincon) | Enum | Applies or references the 'KaijuWinCon' effect/state. |
| `KillsHeal` | Number | Applies the 'KillsHeal' effect. |
| [`KillsToMeat`](./Enums.md#enum-killstomeat) | Enum | Applies or references the 'KillsToMeat' effect/state. |
| `KineticSpikes` | Number | Applies or references the 'KineticSpikes' effect/state. |
| `KnockOutCoin` | Number | Forces the target to drop coins. |
| [`KnockUpAndAway`](#knockupandaway) | Block |  |
| `Knockback` | Number | Applies or references the 'Knockback' effect/state. |
| [`KnockbackIfCrit`](#knockbackifcrit) | Block | Applies or references the 'KnockbackIfCrit' effect/state. |
| `KnockbackImmunity` | Number | Applies the 'KnockbackImmunity' effect. |
| [`LateBloomer`](#latebloomer) | Block | Applies the 'LateBloomer' effect. |
| [`LeaveBehindOnceEachMove`](./Enums.md#enum-leavebehindonceeachmove) | Enum | Applies or references the 'LeaveBehindOnceEachMove' effect/state. |
| `LeaveBehindRockOnKnockback` | Number | Applies the 'LeaveBehindRockOnKnockback' effect. |
| `Leech` | Number | Applies the 'Leech' effect. |
| `LeechPercent` | Number | Applies the 'LeechPercent' effect. |
| `Leeches` | Number |  |
| [`LegacySpawnSavedCatIfExists`](./Enums.md#enum-legacyspawnsavedcatifexists) | Enum | Applies or references the 'LegacySpawnSavedCatIfExists' effect/state. |
| [`LevelUpClassOverride`](./Enums.md#enum-levelupclassoverride) | Enum | Applies the 'LevelUpClassOverride' effect. |
| `Lifesteal` | Number | Applies or references the 'Lifesteal' effect/state. |
| `LightningAspectCharge` | Number | Applies the 'LightningAspectCharge' effect. |
| [`LightningRod`](#lightningrod) | Block | Applies the 'LightningRod' effect. |
| `LimitDamage` | Number | Applies or references the 'LimitDamage' effect/state. |
| `LimitHeal` | Number | Applies or references the 'LimitHeal' effect/state. |
| `LimitSelfKnockbackDamage` | Number | Applies the 'LimitSelfKnockbackDamage' effect. |
| [`LimitedTileTrail`](./Enums.md#enum-limitedtiletrail) | Enum | Applies the 'LimitedTileTrail' effect. |
| [`LineOfSightTrueSightAura`](./Enums.md#enum-lineofsighttruesightaura) | Enum | Applies the 'LineOfSightTrueSightAura' effect. |
| `LobbedHook` | Number | Applies the 'LobbedHook' effect. |
| [`LockOrientationFaceTile`](./Arrays.md#array-lockorientationfacetile) | Array | Applies or references the 'LockOrientationFaceTile' effect/state. |
| [`LoopingSoundWhileAlive`](./Enums.md#enum-loopingsoundwhilealive) | Enum | Applies or references the 'LoopingSoundWhileAlive' effect/state. |
| [`LowHealthAllyDodgeChanceAura`](#lowhealthallydodgechanceaura) | Block | Applies the 'LowHealthAllyDodgeChanceAura' effect. |
| `LuckUp` | Number | Applies or references the 'LuckUp' effect/state. |
| `Madness` | Number | Applies the Madness debuff/status effect. |
| `MagicDamageImmune` | Number | Applies or references the 'MagicDamageImmune' effect/state. |
| `MagicWeakness` | Number | Applies or references the 'MagicWeakness' effect/state. |
| `MakeBasicAttackPassThroughThings` | Number | Applies the 'MakeBasicAttackPassThroughThings' effect. |
| `MakeBasicAttackPull` | Number |  |
| `MakeSpellsRequireCharge` | Number | Applies the 'MakeSpellsRequireCharge' effect. |
| `MamaCatAnimations` | Number | Applies or references the 'MamaCatAnimations' effect/state. |
| `ManaCostReduction` | Number | Applies or references the 'ManaCostReduction' effect/state. |
| [`ManaCostReductionTagged`](#manacostreductiontagged) | Block | Applies the 'ManaCostReductionTagged' effect. |
| [`ManaGain`](./Math_Equations.md) | Equation | Applies or references the 'ManaGain' effect/state. |
| [`ManaGainRange`](#managainrange) | Block | Applies or references the 'ManaGainRange' effect/state. |
| `ManaLeeches` | Number | Applies or references the 'ManaLeeches' effect/state. |
| [`ManaPickup`](#manapickup) | Block | Pickup Logic: Defines what happens when a mana item is collected. |
| `ManaRegenMultiplierIfManaEmpty` | Number | Applies the 'ManaRegenMultiplierIfManaEmpty' effect. |
| [`ManglerMonsterPassive`](./Enums.md#enum-manglermonsterpassive) | Enum | Applies or references the 'ManglerMonsterPassive' effect/state. |
| `Marked` | Number | Applies or references the 'Marked' effect/state. |
| `MaxAccuracy` | Number | Applies the 'MaxAccuracy' effect. |
| `MaxStartingMana` | Number | Applies the 'MaxStartingMana' effect. |
| [`MegaDinoDropController`](#megadinodropcontroller) | Block | Boss Logic: Manages loot drops for the Mega Dino. |
| `MegaMinions` | Number | Applies the 'MegaMinions' effect. |
| [`MeleeRevengeDamage`](#meleerevengedamage) | Block | Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack. |
| `Metal` | Number | Applies or references the 'Metal' effect/state. |
| `MetalDetector` | Number | Applies the 'MetalDetector' effect. |
| `MimicSpawnerAttacks` | Number | Applies or references the 'MimicSpawnerAttacks' effect/state. |
| [`MiniVolcanoReaction`](./Enums.md#enum-minivolcanoreaction) | Enum | Applies or references the 'MiniVolcanoReaction' effect/state. |
| `MinimumKnockbackFromAllDamage` | Number | Applies or references the 'MinimumKnockbackFromAllDamage' effect/state. |
| `MinimumKnockbackFromPhysicalAttacks` | Number | Applies or references the 'MinimumKnockbackFromPhysicalAttacks' effect/state. |
| `MinimumTech` | Number | Applies the 'MinimumTech' effect. |
| `MissChance` | Number | Applies the 'MissChance' effect. |
| `ModelingClayPassive` | Number | Applies or references the 'ModelingClayPassive' effect/state. |
| [`ModifyAbility`](#modifyability) | Block | Applies or references the 'ModifyAbility' effect/state. |
| [`ModularPickup`](#modularpickup) | Block | Pickup Logic: Defines what happens when a modular item is collected. |
| [`MonkCatReactionAbilities`](#monkcatreactionabilities) | Block | Reaction: Specific counter-attack or dodge abilities used by the Monk class. |
| [`MoonHeadCrackedVisual`](./Enums.md#enum-moonheadcrackedvisual) | Enum | Applies or references the 'MoonHeadCrackedVisual' effect/state. |
| `MoonHeadFinisherEnabler` | Number | Applies or references the 'MoonHeadFinisherEnabler' effect/state. |
| [`MotherGrowController`](#mothergrowcontroller) | Block | Boss Logic: Manages the growth phases of the Mother boss. |
| [`MotherTumorPassive`](#mothertumorpassive) | Block | Boss Logic: Passive effects applied to the Mother's tumors. |
| [`MotherTumorSpawnInCapture`](#mothertumorspawnincapture) | Block | Boss Logic: Logic for capturing entities inside the Mother's tumors upon spawning. |
| [`Mount`](#mount) | Block | Character Form: Behavior and stats for the 'Mount' state. |
| [`MoveAfterAnyAttemptedAttack`](#moveafteranyattemptedattack) | Block | AI Movement: Forces a move action immediately after attacking, even if it missed. |
| [`MoveAndUseAbilityEachTurnBeginIfPossible`](./Enums.md#enum-moveanduseabilityeachturnbeginifpossible) | Enum | Applies the 'MoveAndUseAbilityEachTurnBeginIfPossible' effect. |
| [`MoveAwayFromDamageSource`](./Enums.md#enum-moveawayfromdamagesource) | Enum |  |
| [`MoveAwayWhenEnemyAdjacent`](#moveawaywhenenemyadjacent) | Block | AI Movement: Moves away if an enemy enters an adjacent tile. |
| `MoveQuivered` | Number | Applies the 'MoveQuivered' effect. |
| `MoveRandomly` | Number | Applies the 'MoveRandomly' effect. |
| [`MoveSpeedMultiplier`](./Enums.md#enum-movespeedmultiplier) | Enum | Applies or references the 'MoveSpeedMultiplier' effect/state. |
| [`MoveTowardsDamageSource`](./Enums.md#enum-movetowardsdamagesource) | Enum | AI Movement: Closes distance on the last source of damage. |
| [`MoveTowardsKillers`](./Enums.md#enum-movetowardskillers) | Enum | AI Movement: Seeks out entities that have recently killed an ally. |
| [`MoveWhenDamaged`](./Enums.md#enum-movewhendamaged) | Enum | AI Movement: Forces a reposition when taking damage. |
| [`MovementReaction`](#movementreaction) | Block | Reaction: Triggers an effect or ability when forced to move. |
| `MovementUp` | Number | Applies the 'MovementUp' effect. |
| [`MultiSpawnOnDeath`](#multispawnondeath) | Block | Event Trigger: Spawns multiple entities upon death. |
| `MulticatHeads` | Number | Applies or references the 'MulticatHeads' effect/state. |
| [`MulticlassLevelUp`](./Enums.md#enum-multiclasslevelup) | Enum | Applies the 'MulticlassLevelUp' effect. |
| `MultiplyCoinsOnBattleStart` | Number | Applies or references the 'MultiplyCoinsOnBattleStart' effect/state. |
| `MultiplyReceivedHealing` | Number | Applies or references the 'MultiplyReceivedHealing' effect/state. |
| `MutateAfterXTurns` | Number | Applies or references the 'MutateAfterXTurns' effect/state. |
| [`MutateViaAbility`](./Enums.md#enum-mutateviaability) | Enum | Applies or references the 'MutateViaAbility' effect/state. |
| `MuteDemonicGlyphDisplay` | Number | Applies or references the 'MuteDemonicGlyphDisplay' effect/state. |
| `NeckArmorPassiveMultiplierBonus` | Number | Applies or references the 'NeckArmorPassiveMultiplierBonus' effect/state. |
| [`NextBattleStatus`](#nextbattlestatus) | Block | Applies the 'NextBattleStatus' effect. |
| `NoHealthOnlyShield` | Number | Applies or references the 'NoHealthOnlyShield' effect/state. |
| `NoHealthRegen` | Number | Applies or references the 'NoHealthRegen' effect/state. |
| `NoManaRegen` | Number | Applies the 'NoManaRegen' effect. |
| `NoReflection` | Number | Applies the 'NoReflection' effect. |
| `NonLethal` | Number | Applies the 'NonLethal' effect. |
| `NonStackingDivineShield` | Number | Applies the 'NonStackingDivineShield' effect. |
| `NonStackingShield` | Number |  |
| `NubbyTossPriority` | Number | Applies the 'NubbyTossPriority' effect. |
| [`NukeQuestFinalBossModifications`](#nukequestfinalbossmodifications) | Block | Special encounter trigger for the Nuke Quest ending. |
| `NumbingLeeches` | Number | Applies the 'NumbingLeeches' effect. |
| [`ObjectDetector`](#objectdetector) | Block | Applies or references the 'ObjectDetector' effect/state. |
| [`ObjectOnHitCharacter`](./Enums.md#enum-objectonhitcharacter) | Enum | Spawns a specific character or entity upon impact. |
| `OneUseSpellDamageUp` | Number | Applies the 'OneUseSpellDamageUp' effect. |
| `OrthogonalAIDangerZone` | Number | Applies or references the 'OrthogonalAIDangerZone' effect/state. |
| `Ostracized` | Number | Applies or references the 'Ostracized' effect/state. |
| `OverManaReducesManaCosts` | Number |  |
| `OverhealGainsBothShield` | Number | Applies the 'OverhealGainsBothShield' effect. |
| [`OverrideBasicAttack`](./Enums.md#enum-overridebasicattack) | Enum | Applies or references the 'OverrideBasicAttack' effect/state. |
| `OverrideChainKnockback` | Number | Applies or references the 'OverrideChainKnockback' effect/state. |
| `OverrideChainKnockbackDamage` | Number | Applies the 'OverrideChainKnockbackDamage' effect. |
| `OverrideMaxHealth` | Number | Applies or references the 'OverrideMaxHealth' effect/state. |
| `OverrideMaxMana` | Number | Applies the 'OverrideMaxMana' effect. |
| `OverridePalette` | Number | Applies the 'OverridePalette' effect. |
| `PackHunting` | Number | Applies or references the 'PackHunting' effect/state. |
| [`Paranoia`](./Enums.md#enum-paranoia) | Enum | Applies the 'Paranoia' effect. |
| `ParasitesArentCursed` | Number | Applies the 'ParasitesArentCursed' effect. |
| `PartialCleanse` | Number | Applies or references the 'PartialCleanse' effect/state. |
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
| `PassiveLevelUpAtCombatEnd` | Number | Applies the 'PassiveLevelUpAtCombatEnd' effect. |
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
| `PercentHeal` | Number | Applies the 'PercentHeal' effect. |
| `PermanentCharisma` | Number | Applies or references the 'PermanentCharisma' effect/state. |
| `PermanentConfusion` | Number | Applies or references the 'PermanentConfusion' effect/state. |
| `PermanentConstitution` | Number | Applies or references the 'PermanentConstitution' effect/state. |
| `PermanentDexterity` | Number | Applies the 'PermanentDexterity' effect. |
| `PermanentImmobile` | Number | Applies the 'PermanentImmobile' effect. |
| `PermanentIntelligence` | Number | Applies or references the 'PermanentIntelligence' effect/state. |
| `PermanentItems` | Number | Applies the 'PermanentItems' effect. |
| `PermanentKitten` | Number | Applies the 'PermanentKitten' effect. |
| `PermanentLuck` | Number | Applies or references the 'PermanentLuck' effect/state. |
| `PermanentMadness` | Number | Applies or references the 'PermanentMadness' effect/state. |
| `PermanentSpeed` | Number | Applies the 'PermanentSpeed' effect. |
| `PermanentStrength` | Number | Applies or references the 'PermanentStrength' effect/state. |
| `Petrify` | Number | Applies the 'Petrify' effect. |
| `Phasing` | Number | Applies or references the 'Phasing' effect/state. |
| `PhysicalAttacksMiss` | Number | Applies or references the 'PhysicalAttacksMiss' effect/state. |
| `Piercing` | Number | Applies the 'Piercing' effect. |
| `Plant` | Number | Applies or references the 'Plant' effect/state. |
| `Poison` | Number | Applies or references the 'Poison' effect/state. |
| `PoisonLace` | Number | Applies or references the 'PoisonLace' effect/state. |
| `PoisonMultiplier` | Number | Applies the 'PoisonMultiplier' effect. |
| `PoisonThorns` | Number | Applies or references the 'PoisonThorns' effect/state. |
| [`PoopWhenHit`](./Enums.md#enum-poopwhenhit) | Enum |  |
| `Possessed` | Number | Applies or references the 'Possessed' effect/state. |
| `PreEmptiveCounterNextAttacks` | Number | Applies or references the 'PreEmptiveCounterNextAttacks' effect/state. |
| [`PreventSpecificInjury`](./Enums.md#enum-preventspecificinjury) | Enum | Applies or references the 'PreventSpecificInjury' effect/state. |
| `PrioritizeAggroTarget` | Number | Applies or references the 'PrioritizeAggroTarget' effect/state. |
| `PrioritizeFarAwayTargets` | Number | Applies or references the 'PrioritizeFarAwayTargets' effect/state. |
| `PrioritizeHitDifferentTargets` | Number | Applies or references the 'PrioritizeHitDifferentTargets' effect/state. |
| `PrioritizePlayerCats` | Number | Applies or references the 'PrioritizePlayerCats' effect/state. |
| `PrioritizeWeakestEnemy` | Number | Applies or references the 'PrioritizeWeakestEnemy' effect/state. |
| `ProbeCharmed` | Number | Applies or references the 'ProbeCharmed' effect/state. |
| [`ProtectTargetedAllies`](#protecttargetedallies) | Block | AI Logic: Navigates to intercept attacks directed at allies. |
| `PullSourceToKnockbackImmuneTarget` | Number | Applies the 'PullSourceToKnockbackImmuneTarget' effect. |
| `PullSourceToTarget` | Number | Applies or references the 'PullSourceToTarget' effect/state. |
| `Purge` | Number | Applies the 'Purge' effect. |
| `Quiver` | Number | Applies the 'Quiver' effect. |
| `Quivered` | Number | Applies or references the 'Quivered' effect/state. |
| `RandomInjury` | Number | Applies the 'RandomInjury' effect. |
| `RandomMagicMissile` | Number | Fires a randomized number of magic missiles. |
| `RandomMutation` | Number | Applies or references the 'RandomMutation' effect/state. |
| [`RandomPassivePool`](#randompassivepool) | Block | Logic: Grants a random passive from the specified pool upon spawning. |
| `RandomPermanentStat` | Number | Applies or references the 'RandomPermanentStat' effect/state. |
| [`RandomPermanentStatsDistinct`](#randompermanentstatsdistinct) | Block |  |
| [`RandomSeededStatModifier`](./Arrays.md#array-randomseededstatmodifier) | Array | Applies or references the 'RandomSeededStatModifier' effect/state. |
| `RandomStatDown` | Number |  |
| `RandomStatUp` | Number | Applies or references the 'RandomStatUp' effect/state. |
| [`RandomStatusFromPool`](#randomstatusfrompool) | Block | Selects and applies a random status effect from the provided nested block. |
| [`RandomTaggedMutation`](./Enums.md#enum-randomtaggedmutation) | Enum | Applies or references the 'RandomTaggedMutation' effect/state. |
| [`RandomizeAIWeightsEachTurn`](./Arrays.md#array-randomizeaiweightseachturn) | Array | Applies or references the 'RandomizeAIWeightsEachTurn' effect/state. |
| `RangeUp` | Number | Applies the 'RangeUp' effect. |
| `RangedTrueShot` | Number | Applies or references the 'RangedTrueShot' effect/state. |
| `RealTimePressure_OneUnit` | Number | Applies the 'RealTimePressure_OneUnit' effect. |
| `Reanimate` | Number | Applies the 'Reanimate' effect. |
| [`ReceivedStatusReplacement`](./Arrays.md#array-receivedstatusreplacement) | Array | Applies the 'ReceivedStatusReplacement' effect. |
| `ReclaimItemOnBreak` | Number | Applies or references the 'ReclaimItemOnBreak' effect/state. |
| `ReduceManaCost` | Number | Applies the 'ReduceManaCost' effect. |
| `ReduceSpellCostsPerDisorder` | Number | Applies or references the 'ReduceSpellCostsPerDisorder' effect/state. |
| `ReduceSpellCostsPerParasite` | Number | Applies or references the 'ReduceSpellCostsPerParasite' effect/state. |
| `Reflect` | Number | Applies or references the 'Reflect' effect/state. |
| `ReflectProjectiles` | Number | Passive: Reflects incoming projectiles back at the attacker. |
| `RefreshActPoints` | Number | Applies the 'RefreshActPoints' effect. |
| [`RefreshEquipmentAbilityOnElement`](#refreshequipmentabilityonelement) | Block | Applies or references the 'RefreshEquipmentAbilityOnElement' effect/state. |
| `RefreshMoveOnWeaponConnect` | Number | Applies the 'RefreshMoveOnWeaponConnect' effect. |
| `RefreshMovePoints` | Number | Applies the 'RefreshMovePoints' effect. |
| `ReloadOnAllyCatDies` | Number | Applies or references the 'ReloadOnAllyCatDies' effect/state. |
| `ReloadOnAllyDies` | Number | Applies or references the 'ReloadOnAllyDies' effect/state. |
| `ReloadOnAnyDamage` | Number | Applies or references the 'ReloadOnAnyDamage' effect/state. |
| `ReloadOnBackstab` | Number | Applies or references the 'ReloadOnBackstab' effect/state. |
| [`ReloadOnElementalDamageReceived`](./Enums.md#enum-reloadonelementaldamagereceived) | Enum | Applies or references the 'ReloadOnElementalDamageReceived' effect/state. |
| `ReloadOnGainCoins` | Number | Applies or references the 'ReloadOnGainCoins' effect/state. |
| `ReloadOnGainDivineShield` | Number | Applies or references the 'ReloadOnGainDivineShield' effect/state. |
| `ReloadOnKill` | Number | Applies or references the 'ReloadOnKill' effect/state. |
| `ReloadOnKillEnemy` | Number | Applies or references the 'ReloadOnKillEnemy' effect/state. |
| [`ReloadOnKillTagged`](./Enums.md#enum-reloadonkilltagged) | Enum | Applies or references the 'ReloadOnKillTagged' effect/state. |
| `ReloadOnSpendMana` | Number | Applies or references the 'ReloadOnSpendMana' effect/state. |
| `ReloadOnTotalDamageReceived` | Number | Applies or references the 'ReloadOnTotalDamageReceived' effect/state. |
| `ReloadOnUseAbilityWithManaCost` | Number | Applies or references the 'ReloadOnUseAbilityWithManaCost' effect/state. |
| `RemoteFlatLeech` | Number | Applies or references the 'RemoteFlatLeech' effect/state. |
| `RemoteLeech` | Number | Applies or references the 'RemoteLeech' effect/state. |
| `RemoveAmbientLightEffects` | Number | Applies or references the 'RemoveAmbientLightEffects' effect/state. |
| `RemoveExtraDispersedTurn` | Number |  |
| [`RemoveGlobalModifiers`](./Arrays.md#array-removeglobalmodifiers) | Array | Applies or references the 'RemoveGlobalModifiers' effect/state. |
| `RemoveLineOfSightRestrictions` | Number | Applies the 'RemoveLineOfSightRestrictions' effect. |
| `RemoveOncePerFightRestriction` | Number | Applies the 'RemoveOncePerFightRestriction' effect. |
| [`RemoveStatus`](./Enums.md#enum-removestatus) | Enum | Applies or references the 'RemoveStatus' effect/state. |
| [`RemoveStatusStacks`](#removestatusstacks) | Block | Logic: Removes stacks of a specific status effect. |
| `RepairAll` | Number | Applies or references the 'RepairAll' effect/state. |
| `RepairTrinket` | Number | Applies or references the 'RepairTrinket' effect/state. |
| `RepairWeapon` | Number | Applies the 'RepairWeapon' effect. |
| `RepairWeaponCondition` | Number | Applies the 'RepairWeaponCondition' effect. |
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
| `RerollItemsOnBattleEnd` | Number | Applies or references the 'RerollItemsOnBattleEnd' effect/state. |
| `ReturnBoundItemOnBattleEnd` | Number |  |
| [`RevengeDamage`](#revengedamage) | Block |  |
| `Revive` | Number | Applies or references the 'Revive' effect/state. |
| [`ReviveNextRound`](#revivenextround) | Block | Queues the character to be resurrected at the start of the next combat round. |
| `ReviveOnWin` | Number | Applies the 'ReviveOnWin' effect. |
| `Robot` | Number | Character Form: Behavior and stats for the 'Robot' state. |
| `RobotsInheritArmor` | Number | Applies the 'RobotsInheritArmor' effect. |
| `RockDetector` | Number | Applies the 'RockDetector' effect. |
| `RockyArmorPassive` | Number | Applies or references the 'RockyArmorPassive' effect/state. |
| [`RockyArmorSalvage`](./Enums.md#enum-rockyarmorsalvage) | Enum |  |
| `Rot` | Number | Applies or references the 'Rot' effect/state. |
| `RunInXTurns` | Number | Applies or references the 'RunInXTurns' effect/state. |
| `RunWhenKittensDead` | Number | Applies or references the 'RunWhenKittensDead' effect/state. |
| [`RunWhenLastPlayerCatIsCharmed`](#runwhenlastplayercatischarmed) | Block | AI Logic: Flee logic when the player team is entirely crowd-controlled. |
| `SafeDie` | Number | Applies or references the 'SafeDie' effect/state. |
| `SafeDoomed` | Number | Applies or references the 'SafeDoomed' effect/state. |
| `SafeExplosions` | Number | Applies the 'SafeExplosions' effect. |
| [`ScaldingOrbMoonBossOneShot`](#scaldingorbmoonbossoneshot) | Block | Applies or references the 'ScaldingOrbMoonBossOneShot' effect/state. |
| [`ScaledStatusAlliesOnSpendMana`](#scaledstatusalliesonspendmana) | Block | Applies or references the 'ScaledStatusAlliesOnSpendMana' effect/state. |
| [`ScaledStatusOnBleedDamage`](#scaledstatusonbleeddamage) | Block | Applies the 'ScaledStatusOnBleedDamage' effect. |
| [`ScaledStatusOnHolyShieldBlock`](#scaledstatusonholyshieldblock) | Block | Applies or references the 'ScaledStatusOnHolyShieldBlock' effect/state. |
| [`ScaledStatusOnLoseShield`](#scaledstatusonloseshield) | Block | Applies the 'ScaledStatusOnLoseShield' effect. |
| [`ScaledStatusOnOverHealed`](#scaledstatusonoverhealed) | Block | Applies the 'ScaledStatusOnOverHealed' effect. |
| [`ScaledStatusOnOverMana`](#scaledstatusonovermana) | Block | Applies the 'ScaledStatusOnOverMana' effect. |
| [`ScaledStatusOnSpendMana`](#scaledstatusonspendmana) | Block | Applies the 'ScaledStatusOnSpendMana' effect. |
| [`ScalingAttackAnimation`](#scalingattackanimation) | Block | Visual: Animation scales based on damage output. |
| `ScatterCoins` | Number |  |
| `SchizoIllusionAIModifier` | Number | Applies or references the 'SchizoIllusionAIModifier' effect/state. |
| `SchrodingerDisorder` | Number | Applies the 'SchrodingerDisorder' effect. |
| `Scleroderma` | Number | Applies the 'Scleroderma' effect. |
| `Scrambled` | Number | Applies or references the 'Scrambled' effect/state. |
| [`SecurityBotProtect`](#securitybotprotect) | Block | AI Logic: Guarding behavior for Security Bot units. |
| [`SelfDamageWhenDealDamage`](#selfdamagewhendealdamage) | Block | Applies the 'SelfDamageWhenDealDamage' effect. |
| `SelfStatusCarefulness` | Number | Applies or references the 'SelfStatusCarefulness' effect/state. |
| [`SetBrittleImmune`](./Enums.md#enum-setbrittleimmune) | Enum | Applies or references the 'SetBrittleImmune' effect/state. |
| [`SetDefaultFace`](./Enums.md#enum-setdefaultface) | Enum | Applies the 'SetDefaultFace' effect. |
| [`SetDefaultFacePassive`](./Enums.md#enum-setdefaultfacepassive) | Enum | Applies or references the 'SetDefaultFacePassive' effect/state. |
| [`SetFaction`](./Enums.md#enum-setfaction) | Enum | Applies or references the 'SetFaction' effect/state. |
| [`SetFragileImmune`](./Enums.md#enum-setfragileimmune) | Enum | Applies or references the 'SetFragileImmune' effect/state. |
| `SetHealth` | Number | Applies or references the 'SetHealth' effect/state. |
| [`SetItemAux`](#setitemaux) | Block | Applies or references the 'SetItemAux' effect/state. |
| `SetSpellCosts` | Number | Applies the 'SetSpellCosts' effect. |
| `ShareHealthRegen` | Number | Applies the 'ShareHealthRegen' effect. |
| `SharePickups` | Number | Applies the 'SharePickups' effect. |
| `SharePickupsWithSpawner` | Number | Applies or references the 'SharePickupsWithSpawner' effect/state. |
| `SharkySmellsBlood` | Number | Applies or references the 'SharkySmellsBlood' effect/state. |
| `Shield` | Number | Applies or references the 'Shield' effect/state. |
| `ShoulderCheck` | Number | Applies the 'ShoulderCheck' effect. |
| [`ShovingMatch`](./Enums.md#enum-shovingmatch) | Enum | Applies the 'ShovingMatch' effect. |
| `ShowHiddenThings` | Number |  |
| [`SizeScale`](./Enums.md#enum-sizescale) | Enum |  |
| [`SkipFirstRounds`](#skipfirstrounds) | Block | AI Logic: Passes turn for the first X rounds of combat. |
| `Sleep` | Number | Applies the 'Sleep' effect. |
| [`SlotMachineRollPool`](#slotmachinerollpool) | Block | Logic: Defines the possible outcomes for slot machine enemies. |
| `Slow` | Number | Applies or references the 'Slow' effect/state. |
| `SmallEnemiesIgnoreYou` | Number | Applies the 'SmallEnemiesIgnoreYou' effect. |
| `SmallRockBehavior` | Number | AI Logic: Movement/interaction profile for small rocks. |
| [`SmiteEnemiesWhoKill`](#smiteenemieswhokill) | Block | Applies the 'SmiteEnemiesWhoKill' effect. |
| `SoulLink` | Number | Applies the 'SoulLink' effect. |
| `SpawnBearTrapOnMiss` | Number | Applies the 'SpawnBearTrapOnMiss' effect. |
| `SpawnCatCloneOnCorpsePopped` | Number | Applies or references the 'SpawnCatCloneOnCorpsePopped' effect/state. |
| [`SpawnCatCopyOnBattleStart`](#spawncatcopyonbattlestart) | Block | Applies the 'SpawnCatCopyOnBattleStart' effect. |
| [`SpawnCatCopyWhenDowned`](#spawncatcopywhendowned) | Block |  |
| `SpawnCoinAnywhere` | Number | Applies or references the 'SpawnCoinAnywhere' effect/state. |
| `SpawnCreepOnHit` | Number | Applies or references the 'SpawnCreepOnHit' effect/state. |
| `SpawnCreepOnHitKnockback` | Number | Applies or references the 'SpawnCreepOnHitKnockback' effect/state. |
| [`SpawnEachTurn`](#spawneachturn) | Block | Applies or references the 'SpawnEachTurn' effect/state. |
| [`SpawnExtraThingsOnBattleStart`](#spawnextrathingsonbattlestart) | Block | Applies or references the 'SpawnExtraThingsOnBattleStart' effect/state. |
| [`SpawnItemLinkedFamiliar`](#spawnitemlinkedfamiliar) | Block | Applies or references the 'SpawnItemLinkedFamiliar' effect/state. |
| [`SpawnMeatOnMove`](./Enums.md#enum-spawnmeatonmove) | Enum | Applies the 'SpawnMeatOnMove' effect. |
| `SpawnNearEnemies` | Number | Applies or references the 'SpawnNearEnemies' effect/state. |
| [`SpawnObjectOnPopCorpse`](./Enums.md#enum-spawnobjectonpopcorpse) | Enum | Applies or references the 'SpawnObjectOnPopCorpse' effect/state. |
| [`SpawnOnBattleStart`](./Enums.md#enum-spawnonbattlestart) | Enum | Applies or references the 'SpawnOnBattleStart' effect/state. |
| [`SpawnOnBattleStartRandomEmptyTile`](#spawnonbattlestartrandomemptytile) | Block | Applies or references the 'SpawnOnBattleStartRandomEmptyTile' effect/state. |
| [`SpawnOnDeath`](#spawnondeath) | Block | Event Trigger: Spawns a specific entity when killed. |
| [`SpawnOnDowned`](./Enums.md#enum-spawnondowned) | Enum |  |
| [`SpawnRandomPickupsOnTaggedUnitKilled`](#spawnrandompickupsontaggedunitkilled) | Block | Applies or references the 'SpawnRandomPickupsOnTaggedUnitKilled' effect/state. |
| [`SpawnThingOnDamage`](#spawnthingondamage) | Block | Applies or references the 'SpawnThingOnDamage' effect/state. |
| [`SpawnThingOnDeath`](./Enums.md#enum-spawnthingondeath) | Enum | Applies or references the 'SpawnThingOnDeath' effect/state. |
| `SpawnerCatDataReference` | Number | Applies or references the 'SpawnerCatDataReference' effect/state. |
| [`SpecialFriends`](#specialfriends) | Block | Applies the 'SpecialFriends' effect. |
| `SpeedUp` | Number | Applies or references the 'SpeedUp' effect/state. |
| `SpeedUp_WithoutInitiative` | Number | Applies or references the 'SpeedUp_WithoutInitiative' effect/state. |
| `SpellDamageUp` | Number | Applies or references the 'SpellDamageUp' effect/state. |
| [`SpewerAltGraphics`](#speweraltgraphics) | Block | Visual: Alternative graphics for Spewer enemies. |
| `SpiderInfested` | Number | Applies or references the 'SpiderInfested' effect/state. |
| `SplashDamage` | Number | Applies the 'SplashDamage' effect. |
| `SplittableMove` | Number | Applies the 'SplittableMove' effect. |
| [`SpreadDisease`](#spreaddisease) | Block | Provides a chance to transmit a disease status to adjacent targets. |
| `SpreadExtraDebuffs` | Number | Applies the 'SpreadExtraDebuffs' effect. |
| `SpreadPainBonus` | Number | Applies the 'SpreadPainBonus' effect. |
| `SpreadPainBonusCrit` | Number | Applies the 'SpreadPainBonusCrit' effect. |
| `SpreadWater` | Number | Applies or references the 'SpreadWater' effect/state. |
| `SproutsGrantMovement` | Number | Applies or references the 'SproutsGrantMovement' effect/state. |
| [`StackingDodgeChanceOnTookDamage`](#stackingdodgechanceontookdamage) | Block | Applies the 'StackingDodgeChanceOnTookDamage' effect. |
| [`StackingFlowerTrail`](#stackingflowertrail) | Block | Applies or references the 'StackingFlowerTrail' effect/state. |
| `StackingSandstorm` | Number |  |
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
| `StartDead` | Number | Applies or references the 'StartDead' effect/state. |
| `StartOffMap` | Number | Applies or references the 'StartOffMap' effect/state. |
| [`StatDependentPassive`](#statdependentpassive) | Block | Applies or references the 'StatDependentPassive' effect/state. |
| `StatMinimum` | Number | Applies the 'StatMinimum' effect. |
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
| `StatusCarefulness` | Number | Applies or references the 'StatusCarefulness' effect/state. |
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
| `Stealth` | Number | Applies the 'Stealth' effect. |
| `StealthUntilBasicAttack` | Number | Applies or references the 'StealthUntilBasicAttack' effect/state. |
| `StevenBolts` | Number | Applies or references the 'StevenBolts' effect/state. |
| `StrengthForEachNeighboringEnemy` | Number | Applies the 'StrengthForEachNeighboringEnemy' effect. |
| `StrengthInNumbersAura` | Number | Applies the 'StrengthInNumbersAura' effect. |
| `StrengthUp` | Number | Applies or references the 'StrengthUp' effect/state. |
| `StrictLimitDamage` | Number | Applies the 'StrictLimitDamage' effect. |
| `StripKnockback` | Number | Applies or references the 'StripKnockback' effect/state. |
| `StripStatuses` | Number | Applies or references the 'StripStatuses' effect/state. |
| `Study` | Number | Applies the 'Study' effect. |
| `Stun` | Number | Applies the 'Stun' effect. |
| `StunImmunity` | Number | Passive: Prevents Stun from being applied. |
| [`SupportDieInsteadOfRun`](#supportdieinsteadofrun) | Block | AI Logic: Forces a support unit to die rather than flee. |
| [`SupportFormChangeInsteadOfRun`](./Enums.md#enum-supportformchangeinsteadofrun) | Enum | AI Logic: Forces a support unit to transform rather than flee. |
| `SurviveAt1HP` | Number | Applies or references the 'SurviveAt1HP' effect/state. |
| `SwapHighestAndLowestStat` | Number |  |
| [`SwimmingFormChange`](#swimmingformchange) | Block | Logic: Automates form change when entering/exiting water. |
| [`SyncFormsWithBuddy`](#syncformswithbuddy) | Block | Logic: Forces this character's form to match their familiar/buddy. |
| [`T3HitlerSpawningPhase`](#t3hitlerspawningphase) | Block | Boss Logic: Minion spawn phase for the T3 Hitler boss. |
| `TVBotDisableAttack` | Number | Applies or references the 'TVBotDisableAttack' effect/state. |
| `TVBotDisableMove` | Number | Applies or references the 'TVBotDisableMove' effect/state. |
| `TVBotDisableSpells` | Number | Applies or references the 'TVBotDisableSpells' effect/state. |
| [`TVBotScreen`](#tvbotscreen) | Block | Visual: TV Bot screen state. |
| [`TagGreed`](./Enums.md#enum-taggreed) | Enum | Applies or references the 'TagGreed' effect/state. |
| [`TaggedPickupEffectReplacement`](#taggedpickupeffectreplacement) | Block | Applies the 'TaggedPickupEffectReplacement' effect. |
| [`TakeBonusTurnWithStatus`](#takebonusturnwithstatus) | Block | Grants the character an immediate extra turn while afflicted with specific statuses. |
| `TakeExtraTurn` | Number | Applies the 'TakeExtraTurn' effect. |
| `TakeWeaponFromSpawner` | Number | Applies or references the 'TakeWeaponFromSpawner' effect/state. |
| `Tall` | Number | Applies or references the 'Tall' effect/state. |
| [`TallTumorManaBurn`](./Enums.md#enum-talltumormanaburn) | Enum | Applies or references the 'TallTumorManaBurn' effect/state. |
| [`Tangled`](./Arrays.md#array-tangled) | Array | Applies a tangled/ensnared status effect, often modifying visual sprites. |
| `Tarred` | Number | Applies or references the 'Tarred' effect/state. |
| `TauntAlways` | Number | Applies the 'TauntAlways' effect. |
| `TauntAtFullHealth` | Number | Applies the 'TauntAtFullHealth' effect. |
| `Tech` | Number | Applies the 'Tech' effect. |
| `TempCounterAttack` | Number | Applies or references the 'TempCounterAttack' effect/state. |
| `TempDamageUp` | Number | Applies the 'TempDamageUp' effect. |
| `TempInitiativeChange` | Number | Applies the 'TempInitiativeChange' effect. |
| `TempMeleeRangeUp` | Number | Applies or references the 'TempMeleeRangeUp' effect/state. |
| `TempMovement` | Number | Applies the 'TempMovement' effect. |
| `TempNoManaRegen` | Number | Applies or references the 'TempNoManaRegen' effect/state. |
| [`TempPassiveUntilSettled`](#temppassiveuntilsettled) | Block | Applies or references the 'TempPassiveUntilSettled' effect/state. |
| `TempRangeUp` | Number | Applies or references the 'TempRangeUp' effect/state. |
| `TempSpellDamageUp` | Number | Applies the 'TempSpellDamageUp' effect. |
| `TempStrengthUp` | Number | Applies or references the 'TempStrengthUp' effect/state. |
| [`Temporary`](#temporary) | Block | A wrapper block for applying status effects that automatically expire. |
| [`Terminator2Chase`](./Enums.md#enum-terminator2chase) | Enum | Applies or references the 'Terminator2Chase' effect/state. |
| [`Terminator2Run`](#terminator2run) | Block | AI Movement: Specific run logic for Terminator2. |
| [`TerminatorChase`](#terminatorchase) | Block | AI Movement: Specific chase logic for Terminator. |
| [`TerminatorSkin`](#terminatorskin) | Block | Visual: Skin definition for Terminator. |
| [`TheHunger`](#thehunger) | Block | Applies the 'TheHunger' effect. |
| `Thorns` | Number | Applies or references the 'Thorns' effect/state. |
| `TileDamageMultiplier` | Number | Applies the 'TileDamageMultiplier' effect. |
| [`TileElementDamageImmunity`](./Enums.md#enum-tileelementdamageimmunity) | Enum | Applies or references the 'TileElementDamageImmunity' effect/state. |
| [`TileTrail`](./Enums.md#enum-tiletrail) | Enum |  |
| [`TileTrail_Ahead`](./Enums.md#enum-tiletrail_ahead) | Enum | Applies or references the 'TileTrail_Ahead' effect/state. |
| [`TinkererBasicAttackSwitching`](#tinkererbasicattackswitching) | Block | Logic: Allows Tinkerer to swap basic attacks. |
| [`TintItem`](#tintitem) | Block | Applies or references the 'TintItem' effect/state. |
| `TireBehavior` | Number | Applies or references the 'TireBehavior' effect/state. |
| `TormentorHeal` | Number | Applies or references the 'TormentorHeal' effect/state. |
| `TossTargetIsAggroTarget` | Number | Applies or references the 'TossTargetIsAggroTarget' effect/state. |
| `TossTargetIsBuddy` | Number | Applies or references the 'TossTargetIsBuddy' effect/state. |
| `TossTargetIsNotInWater` | Number | Applies or references the 'TossTargetIsNotInWater' effect/state. |
| [`TourettesMeows`](#tourettesmeows) | Block | Applies the 'TourettesMeows' effect. |
| [`TowerDefense`](#towerdefense) | Block | Applies the 'TowerDefense' effect. |
| [`TowerDefenseReflex`](./Enums.md#enum-towerdefensereflex) | Enum | Applies the 'TowerDefenseReflex' effect. |
| [`TrackAmountKilledByPlayer`](./Enums.md#enum-trackamountkilledbyplayer) | Enum | Applies or references the 'TrackAmountKilledByPlayer' effect/state. |
| `Trample` | Number | Applies or references the 'Trample' effect/state. |
| [`TransformInXTurns`](#transforminxturns) | Block | Logic: Forces a form change after X turns. |
| [`TransformItemOnElementInfluence`](#transformitemonelementinfluence) | Block | Applies or references the 'TransformItemOnElementInfluence' effect/state. |
| [`TransformOnDeath`](./Enums.md#enum-transformondeath) | Enum | Applies or references the 'TransformOnDeath' effect/state. |
| [`TransformOnDeathImmediately`](./Enums.md#enum-transformondeathimmediately) | Enum | Logic: Bypasses death sequence to instantly assume a new form. |
| [`TransformOnElementInfluence`](#transformonelementinfluence) | Block | Logic: Changes form when affected by elements. |
| [`TransformOnElementInfluencex`](#transformonelementinfluencex) | Block | Logic: Variant element influence transformation. |
| [`TransformOnStatusThreshold`](#transformonstatusthreshold) | Block | Logic: Changes form when a status effect reaches a certain stack count. |
| [`TransformWeapon`](#transformweapon) | Block | Transforms the equipped weapon into another specific weapon state. |
| [`TransformWhenBuddyDies`](./Enums.md#enum-transformwhenbuddydies) | Enum | Applies or references the 'TransformWhenBuddyDies' effect/state. |
| `TrapEffectsMultiplier` | Number | Applies the 'TrapEffectsMultiplier' effect. |
| [`Trapper`](#trapper) | Block | Character Form: Behavior and stats for the 'Trapper' state. |
| `TriggerBleedOnBleed` | Number |  |
| `TrinketActiveEffectsMultiplierBonus` | Number | Applies or references the 'TrinketActiveEffectsMultiplierBonus' effect/state. |
| `TrinketPassiveMultiplierBonus` | Number | Applies or references the 'TrinketPassiveMultiplierBonus' effect/state. |
| `Triskaidekaphobia` | Number | Applies the 'Triskaidekaphobia' effect. |
| `TrueShot` | Number | Applies or references the 'TrueShot' effect/state. |
| [`TunnelVision`](#tunnelvision) | Block | Applies or references the 'TunnelVision' effect/state. |
| `TutorialBossRiggedFight` | Number | Applies or references the 'TutorialBossRiggedFight' effect/state. |
| [`TwisterFling`](#twisterfling) | Block | Logic: Fling behavior for tornado attacks. |
| `UncappedHP` | Number | Applies the 'UncappedHP' effect. |
| `UncappedHPBonusStr` | Number | Applies the 'UncappedHPBonusStr' effect. |
| `UncappedMana` | Number | Applies the 'UncappedMana' effect. |
| `Uncontrollable` | Number | Applies or references the 'Uncontrollable' effect/state. |
| `Undead` | Number | Applies or references the 'Undead' effect/state. |
| [`UnlimitedDeathRattleRevive`](#unlimiteddeathrattlerevive) | Block | Logic: Endless resurrection on death. |
| `UnlockOrientation` | Number | Applies or references the 'UnlockOrientation' effect/state. |
| `UpTireBehavior` | Number | Applies or references the 'UpTireBehavior' effect/state. |
| [`UpgradeLevelUpClassActives`](./Enums.md#enum-upgradelevelupclassactives) | Enum | Applies the 'UpgradeLevelUpClassActives' effect. |
| [`UpgradeLevelUpClassPassives`](./Enums.md#enum-upgradelevelupclasspassives) | Enum | Applies the 'UpgradeLevelUpClassPassives' effect. |
| `UpgradeSpawnedPickups` | Number | Applies the 'UpgradeSpawnedPickups' effect. |
| [`UpgradeTaggedSpawnsToChampions`](./Enums.md#enum-upgradetaggedspawnstochampions) | Enum |  |
| [`UseAbility`](./Enums.md#enum-useability) | Enum | Logic: Forces execution of an ability. |
| [`UseAbilityWhenOutOfStatus`](#useabilitywhenoutofstatus) | Block | Logic: Casts a specific ability the moment a status effect expires. |
| [`UseAbilityWhenShieldDepleted`](./Enums.md#enum-useabilitywhenshielddepleted) | Enum | Applies or references the 'UseAbilityWhenShieldDepleted' effect/state. |
| [`UseAbility_Madness`](./Enums.md#enum-useability_madness) | Enum | Applies the 'UseAbility_Madness' effect. |
| [`UseAbility_NonStack`](./Enums.md#enum-useability_nonstack) | Enum | Applies or references the 'UseAbility_NonStack' effect/state. |
| `VaporizeInanimate` | Number |  |
| `Vegan` | Number |  |
| `Vengeful` | Number | Applies the 'Vengeful' effect. |
| [`VisualFXTile`](./Enums.md#enum-visualfxtile) | Enum |  |
| `Wall` | Number | Applies or references the 'Wall' effect/state. |
| `WaterWalk` | Number | Applies or references the 'WaterWalk' effect/state. |
| `Weakness` | Number | Applies the 'Weakness' effect. |
| `WeaponActiveEffectsMultiplierBonus` | Number |  |
| `WeaponCountsAsBasicAttack` | Number | Applies the 'WeaponCountsAsBasicAttack' effect. |
| `WeaponDamageMultiplierBonus` | Number | Applies the 'WeaponDamageMultiplierBonus' effect. |
| `WeaponPassiveMultiplierBonus` | Number |  |
| `WeaponsDontLoseDurability` | Number | Applies or references the 'WeaponsDontLoseDurability' effect/state. |
| `Webbed` | Number | Applies or references the 'Webbed' effect/state. |
| [`WeremanTransformationReceiver`](./Enums.md#enum-weremantransformationreceiver) | Enum | Applies or references the 'WeremanTransformationReceiver' effect/state. |
| `Wet` | Number | Applies or references the 'Wet' effect/state. |
| [`WhitelistPickupType`](./Enums.md#enum-whitelistpickuptype) | Enum | Applies or references the 'WhitelistPickupType' effect/state. |
| `WideBackstab` | Number | Applies or references the 'WideBackstab' effect/state. |
| `WispDodge` | Number | Applies or references the 'WispDodge' effect/state. |
| `WobblyCat` | Number | Applies the 'WobblyCat' effect. |
| `XIsConsumedCharacterMaxHP` | Number | Applies or references the 'XIsConsumedCharacterMaxHP' effect/state. |
| `XIsCountDeaths` | Number | Applies or references the 'XIsCountDeaths' effect/state. |
| [`XIsCountStatusStacks`](./Enums.md#enum-xiscountstatusstacks) | Enum | Applies or references the 'XIsCountStatusStacks' effect/state. |
| [`XIsFormulaLockedUntilComplete`](./Enums.md#enum-xisformulalockeduntilcomplete) | Enum | Applies or references the 'XIsFormulaLockedUntilComplete' effect/state. |
| `XIsFreeArmorSlots` | Number | Applies or references the 'XIsFreeArmorSlots' effect/state. |
| `XIsIncreaseEachTurn` | Number | Applies or references the 'XIsIncreaseEachTurn' effect/state. |
| [`XIsLivingAlliesWithTag`](./Enums.md#enum-xislivingallieswithtag) | Enum | Applies or references the 'XIsLivingAlliesWithTag' effect/state. |
| [`XIsLivingCharactersWithTag`](./Enums.md#enum-xislivingcharacterswithtag) | Enum | Applies or references the 'XIsLivingCharactersWithTag' effect/state. |
| [`XIsMultipliedPercentHealth`](./Arrays.md#array-xismultipliedpercenthealth) | Array | Applies or references the 'XIsMultipliedPercentHealth' effect/state. |
| `XIsOtherHealsThisTurn` | Number | Applies or references the 'XIsOtherHealsThisTurn' effect/state. |
| `XIsRampAndReset` | Number | Applies or references the 'XIsRampAndReset' effect/state. |
| `XIsRecycleCostReduction` | Number | Applies or references the 'XIsRecycleCostReduction' effect/state. |
| `XIsSpellStormRampAndReset` | Number | Math variable assignment: Evaluates X based on Spell Storm stacks, then resets them. |
| `XIsTimesDamageTaken` | Number | Applies or references the 'XIsTimesDamageTaken' effect/state. |
| [`YOffset`](./Enums.md#enum-yoffset) | Enum | Applies or references the 'YOffset' effect/state. |
| `ZeroKnockbackDamage` | Number | Applies or references the 'ZeroKnockbackDamage' effect/state. |
| `Zombie` | Number |  |
| `ally_chance` | Number |  |
| `cant_miss` | Boolean |  |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. |
| `count` | Number | Quantity. |
| `damage` | Number | The base damage properties of an attack. |
| [`effects`](#effects) | Block | Non-damaging status applications and logic triggers executed on impact. |
| [`element`](./Enums.md#enum-element) | Enum |  |
| [`elements`](./Arrays.md#array-elements) | Array |  |
| `end_of_round` | Boolean |  |
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. |
| `exclude_self` | Boolean |  |
| `include_spells` | Boolean | If true, allows the AI to cast spells during this bonus turn. |
| `knockback` | Number |  |
| [`mode`](./Enums.md#enum-mode) | Enum |  |
| `must_do_damage` | Boolean |  |
| [`passives`](#passives) | Block |  |
| `stacks` | Number | Number of stacks or intensity to apply. |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. |
| [`tag_filter`](./Enums.md#enum-tag_filter) | Enum |  |
| [`threshold`](#threshold) | Block |  |
| `triggers_limit` | Number |  |
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
| `count` | Number | Quantity. |

</details>

---

#### `CatchProjectiles`

<details>
<summary><b>Expand</b></summary>

| Property Key | Type | Definition |
| :--- | :--- | :--- |
| [`[status_passive_id]`](./Engine_Statuses_and_Passives.md#valid-property-keys) | Block | Any valid logic block from the global schema. |
| `ally_chance` | Number |  |
| `chance` | Number | Probability (0.0 to 1.0 or percentage) of this occurring. |

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
| `damage` | Number | The base damage properties of an attack. |
| [`effects`](#effects) | Block | Non-damaging status applications and logic triggers executed on impact. |
| [`elements`](./Arrays.md#array-elements) | Array |  |
| `knockback` | Number |  |
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
| `stacks` | Number | Number of stacks or intensity to apply. |

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
| `threshold` | Number |  |

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
| `damage` | Number |  |
| [`effects`](#effects) | Block |  |
| [`elements`](./Arrays.md#array-elements) | Array |  |
| `knockback` | Number |  |
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
| `stacks` | Number | Number of stacks or intensity to apply. |

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
| `triggers_limit` | Number |  |

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
| `stacks` | Number | Number of stacks or intensity to apply. |

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
| `count` | Number | Quantity. |

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

