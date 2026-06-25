# Mewgenics Mod Developer Documentation: Engine: Status and Passive Keys

## Engine: Status and Passive Keys

This document lists every confirmed Status and Passive ID found across all game data files. These IDs are used as **dynamic keys** in any Status or Passive Container block (e.g. `statuses`, `passives`, `AddStatusToBasicAttack`, `bonus_passives`). The value paired with each key depends on the context: typically a stack count or duration for statuses, or a boolean/nested object for passives.

> **Note:** With over 1,200 unique IDs, this is the largest system in the game. Granting a character an ID (like `AddStatusToBasicAttack`) gives the character that reactive behaviour permanently.

> **Referenced by:** [`damage_instance` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-damage_instance), [`effects` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-effects), [`bonus_passives` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-bonus_passives), [`temporary_effects` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-temporary_effects), [`Else` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-else), [`ApplyToSource` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytosource), [`Conditional_HasTag` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_hastag), [`Conditional_Enemy` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_enemy), [`Conditional_Ally` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_ally), [`keyword_tooltips` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-keyword_tooltips), [`additional_passives` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-additional_passives), [`RandomStatusFromPool` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-randomstatusfrompool), [`Conditional_Boss` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_boss), [`ApplyToSourceOnKill` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytosourceonkill), [`CanApplyToInanimate` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-canapplytoinanimate), [`Conditional_NotBoss` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_notboss), [`Conditional_HasStatus` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_hasstatus), [`Conditional_GoodRoll` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_goodroll), [`Conditional_Speculative` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_speculative), [`ApplyPassives` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applypassives), [`Conditional_FormulaIsPositive` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_formulaispositive), [`ApplyStatusIfCrit` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applystatusifcrit), [`Conditional_Corpse` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_corpse), [`Conditional_InForm` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_inform), [`Conditional_HealthThreshold` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_healththreshold), [`Conditional_Object` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_object), [`Conditional_PlayerCat` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_playercat), [`CollectsPickupsWithAltEffects` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-collectspickupswithalteffects), [`Conditional_Familiar` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_familiar), [`LateStatusApplication` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-latestatusapplication), [`TakeBonusTurnWithStatus` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-takebonusturnwithstatus), [`TempPassiveWhileHasStatus` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-temppassivewhilehasstatus), [`TimeDelayStatusApplication` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-timedelaystatusapplication), [`post_spawn_statuses` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-post_spawn_statuses), [`ApplyMultipleTimes` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applymultipletimes), [`Conditional_AffectedByElement` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_affectedbyelement), [`Conditional_FirstApplicationThisTurn` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_firstapplicationthisturn), [`Conditional_LastHit` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_lasthit), [`StatusOnBattleEnd` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-statusonbattleend), [`extra_statuses` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-extra_statuses), [`AddStatusToBasicAttack` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-addstatustobasicattack), [`ApplyToRandomPartyMemberIfPossible` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytorandompartymemberifpossible), [`Conditional_BadRoll` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_badroll), [`Conditional_BossOrBig` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_bossorbig), [`Conditional_Buddy` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_buddy), [`Conditional_Displaceable` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_displaceable), [`Conditional_NotAlly` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_notally), [`Conditional_NotBossOrBig` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_notbossorbig), [`Conditional_NotShielded` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_notshielded), [`Conditional_OncePerBattle` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_onceperbattle), [`Conditional_Shielded` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_shielded), [`Math` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-math), [`MeleeRevengeDamage` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-meleerevengedamage), [`OverHealToStatuses` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-overhealtostatuses), [`XIsTargetHealth` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-xistargethealth), [`AlphaStatusOnTurnBegin` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-alphastatusonturnbegin), [`ApplyPassivesToSpawnerWhileAlive` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applypassivestospawnerwhilealive), [`ApplyStatusesNextTurnBegin` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applystatusesnextturnbegin), [`ApplyToOthersWithSharedTagAndFaction` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-applytootherswithsharedtagandfaction), [`Conditional_ActiveWeather_Any` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_activeweather_any), [`Conditional_Backstab` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_backstab), [`Conditional_CanBeHealed` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_canbehealed), [`Conditional_DebuffRoll` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_debuffroll), [`Conditional_HasCleansableDebuffs` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_hascleansabledebuffs), [`Conditional_LivingPlayerCat` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_livingplayercat), [`Conditional_RandomChance` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_randomchance), [`Conditional_SourceAbilityHasTag` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_sourceabilityhastag), [`Conditional_SourceHasStatus` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-conditional_sourcehasstatus), [`PassiveWhileNotTakingTurn` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-passivewhilenottakingturn), [`ReviveNextRound` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-revivenextround), [`StatusGroup` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-statusgroup), [`StatusKillers` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-statuskillers), [`VisualCountDownThenApplyStatus` (Abilities_and_Spells)](./Abilities_and_Spells.md#context-visualcountdownthenapplystatus), [`innate_passives` (Cat_Classes)](./Cat_Classes.md#context-innate_passives), [`passives` (Cat_Mutations)](./Cat_Mutations.md#context-passives), [`AddStatusToBasicAttack` (Cat_Mutations)](./Cat_Mutations.md#context-addstatustobasicattack), [`effects` (Cat_Mutations)](./Cat_Mutations.md#context-effects), [`MeleeRevengeDamage` (Cat_Mutations)](./Cat_Mutations.md#context-meleerevengedamage), [`AddStatusToBasicMeleeAttack` (Cat_Mutations)](./Cat_Mutations.md#context-addstatustobasicmeleeattack), [`StatusOnTookDamage` (Cat_Mutations)](./Cat_Mutations.md#context-statusontookdamage), [`StatusEachTurnBegin` (Cat_Mutations)](./Cat_Mutations.md#context-statuseachturnbegin), [`RandomStatusFromPool` (Cat_Mutations)](./Cat_Mutations.md#context-randomstatusfrompool), [`StatusEachTurnEnd` (Cat_Mutations)](./Cat_Mutations.md#context-statuseachturnend), [`Conditional_RandomChance` (Cat_Mutations)](./Cat_Mutations.md#context-conditional_randomchance), [`StatusEveryXSpellCasts` (Cat_Mutations)](./Cat_Mutations.md#context-statuseveryxspellcasts), [`StatusKilledCharacters` (Cat_Mutations)](./Cat_Mutations.md#context-statuskilledcharacters), [`StatusOnBattleEnd` (Cat_Mutations)](./Cat_Mutations.md#context-statusonbattleend), [`StatusOnEndMove` (Cat_Mutations)](./Cat_Mutations.md#context-statusonendmove), [`StatusOnTookDamageFromAbility` (Cat_Mutations)](./Cat_Mutations.md#context-statusontookdamagefromability), [`Conditional_FirstApplicationThisTurn` (Cat_Mutations)](./Cat_Mutations.md#context-conditional_firstapplicationthisturn), [`Conditional_GoodRoll` (Cat_Mutations)](./Cat_Mutations.md#context-conditional_goodroll), [`PassiveWhenAtFullMana` (Cat_Mutations)](./Cat_Mutations.md#context-passivewhenatfullmana), [`StatusEachRoundEnd` (Cat_Mutations)](./Cat_Mutations.md#context-statuseachroundend), [`StatusEveryXSpellCastsEachTurn` (Cat_Mutations)](./Cat_Mutations.md#context-statuseveryxspellcastseachturn), [`StatusIfDidntMove` (Cat_Mutations)](./Cat_Mutations.md#context-statusifdidntmove), [`StatusIfUnusedMovePoints` (Cat_Mutations)](./Cat_Mutations.md#context-statusifunusedmovepoints), [`StatusOnAllyCatDeath` (Cat_Mutations)](./Cat_Mutations.md#context-statusonallycatdeath), [`StatusOnCastSpell` (Cat_Mutations)](./Cat_Mutations.md#context-statusoncastspell), [`StatusOnDie` (Cat_Mutations)](./Cat_Mutations.md#context-statusondie), [`StatusOnEatFood` (Cat_Mutations)](./Cat_Mutations.md#context-statusoneatfood), [`StatusOnKill` (Cat_Mutations)](./Cat_Mutations.md#context-statusonkill), [`passives` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-passives), [`AddStatusToBasicAttack` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-addstatustobasicattack), [`MeleeRevengeDamage` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-meleerevengedamage), [`ally_rewards` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-ally_rewards), [`effects` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-effects), [`PassiveGroup` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-passivegroup), [`StatusCollector` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statuscollector), [`statuses` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statuses), [`StatusEachTurnEnd` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statuseachturnend), [`StatusOnKill` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusonkill), [`StatusOnTookDamageFromAbility` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusontookdamagefromability), [`keyword_tooltips` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-keyword_tooltips), [`RandomPassivePool` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-randompassivepool), [`Conditional_GoodRoll` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_goodroll), [`Holy` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-holy), [`StatusGroup` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusgroup), [`StatusOnSpawnIn` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusonspawnin), [`StatusOnTookDamage` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusontookdamage), [`TempPassiveUntilSettled` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-temppassiveuntilsettled), [`alternate_energized_effect` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-alternate_energized_effect), [`passive` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-passive), [`statuses_on_enter_form` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statuses_on_enter_form), [`AddStatusToReceivedDamage` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-addstatustoreceiveddamage), [`AddStatusToSpells` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-addstatustospells), [`AddStatusToTrampleDamage` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-addstatustotrampledamage), [`AddStatusToWeapons` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-addstatustoweapons), [`AdventureTokenPassivePool` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-adventuretokenpassivepool), [`Conditional_BadRoll` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_badroll), [`Conditional_HasKnockback` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_hasknockback), [`Conditional_IsPhysicalAttack` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-conditional_isphysicalattack), [`Else` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-else), [`FinalBossHitCountdownBoris` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-finalbosshitcountdownboris), [`FinalBossHitCountdownExplosive` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-finalbosshitcountdownexplosive), [`Fire` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-fire), [`ModularPickup` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-modularpickup), [`PassiveWhenDead` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-passivewhendead), [`RandomStatusFromPool` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-randomstatusfrompool), [`StacyMutant_Brace` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_brace), [`StacyMutant_Counter` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_counter), [`StacyMutant_Damage` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_damage), [`StacyMutant_DoubleHead` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_doublehead), [`StacyMutant_Fire` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_fire), [`StacyMutant_Health` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_health), [`StacyMutant_Holy` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_holy), [`StacyMutant_Ice` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_ice), [`StacyMutant_Lightning` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_lightning), [`StacyMutant_Mirror` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_mirror), [`StacyMutant_Speed` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_speed), [`StacyMutant_Thorns` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-stacymutant_thorns), [`StatusAfterXTurns` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusafterxturns), [`StatusEachTurnBeginIfHasStatus` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statuseachturnbeginifhasstatus), [`StatusEachTurnEndForEachTurn` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statuseachturnendforeachturn), [`StatusEachTurnEndIfEnabledAtStartOfTurn` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statuseachturnendifenabledatstartofturn), [`StatusOnDie` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusondie), [`StatusOnEndMove` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusonendmove), [`StatusOnEnemyConfused` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusonenemyconfused), [`StatusOnGainCoins` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusongaincoins), [`StatusOverlappingCharactersAndDie` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statusoverlappingcharactersanddie), [`StatusWhenStatusCompletelyRemoved` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-statuswhenstatuscompletelyremoved), [`additional_statuses` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-additional_statuses), [`damage_instance` (Characters_and_Bosses)](./Characters_and_Bosses.md#context-damage_instance), [`passives` (Elite_Buffs)](./Elite_Buffs.md#context-passives), [`StatusEachRoundBegin` (Elite_Buffs)](./Elite_Buffs.md#context-statuseachroundbegin), [`effects` (Elite_Buffs)](./Elite_Buffs.md#context-effects), [`MeleeRevengeDamage` (Elite_Buffs)](./Elite_Buffs.md#context-meleerevengedamage), [`StatusEachTurnEnd` (Elite_Buffs)](./Elite_Buffs.md#context-statuseachturnend), [`statuses` (Elite_Buffs)](./Elite_Buffs.md#context-statuses), [`AddStatusToBasicAttack` (Elite_Buffs)](./Elite_Buffs.md#context-addstatustobasicattack), [`StatusEachRoundEnd` (Elite_Buffs)](./Elite_Buffs.md#context-statuseachroundend), [`StatusOnDie` (Elite_Buffs)](./Elite_Buffs.md#context-statusondie), [`StatusOnEnemyCastSpell` (Elite_Buffs)](./Elite_Buffs.md#context-statusonenemycastspell), [`StatusOnKill` (Elite_Buffs)](./Elite_Buffs.md#context-statusonkill), [`self_status_next_fight` (Events_and_Encounters)](./Events_and_Encounters.md#context-self_status_next_fight), [`party_status_next_fight` (Events_and_Encounters)](./Events_and_Encounters.md#context-party_status_next_fight), [`global_effect_next_fight` (Events_and_Encounters)](./Events_and_Encounters.md#context-global_effect_next_fight), [`CharacterTypeGainsStatusAtBattleStart` (Events_and_Encounters)](./Events_and_Encounters.md#context-charactertypegainsstatusatbattlestart), [`StatusRandomEnemiesOnBattleStart` (Events_and_Encounters)](./Events_and_Encounters.md#context-statusrandomenemiesonbattlestart), [`effects` (House_and_Environment)](./House_and_Environment.md#context-effects), [`Else` (House_and_Environment)](./House_and_Environment.md#context-else), [`StatusCharactersOnRoundEnd` (House_and_Environment)](./House_and_Environment.md#context-statuscharactersonroundend), [`ApplyPassives` (House_and_Environment)](./House_and_Environment.md#context-applypassives), [`CharacterTypeGainsStatusAtBattleStart` (House_and_Environment)](./House_and_Environment.md#context-charactertypegainsstatusatbattlestart), [`Conditional_GoodRoll` (House_and_Environment)](./House_and_Environment.md#context-conditional_goodroll), [`RandomStatusFromPool` (House_and_Environment)](./House_and_Environment.md#context-randomstatusfrompool), [`StatusAllCharactersOnSpawn` (House_and_Environment)](./House_and_Environment.md#context-statusallcharactersonspawn), [`StatusCharactersOnRoundStart` (House_and_Environment)](./House_and_Environment.md#context-statuscharactersonroundstart), [`Conditional_Corpse` (House_and_Environment)](./House_and_Environment.md#context-conditional_corpse), [`Conditional_HasTag` (House_and_Environment)](./House_and_Environment.md#context-conditional_hastag), [`Conditional_PartyMember` (House_and_Environment)](./House_and_Environment.md#context-conditional_partymember), [`StatusOnBattleEnd` (House_and_Environment)](./House_and_Environment.md#context-statusonbattleend), [`extra_statuses` (House_and_Environment)](./House_and_Environment.md#context-extra_statuses), [`passives` (Items_and_Equipment)](./Items_and_Equipment.md#context-passives), [`AddStatusToBasicAttack` (Items_and_Equipment)](./Items_and_Equipment.md#context-addstatustobasicattack), [`effects` (Items_and_Equipment)](./Items_and_Equipment.md#context-effects), [`MeleeRevengeDamage` (Items_and_Equipment)](./Items_and_Equipment.md#context-meleerevengedamage), [`StatusOnBattleEnd` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonbattleend), [`StatusEachTurnEnd` (Items_and_Equipment)](./Items_and_Equipment.md#context-statuseachturnend), [`StatusOnBreak` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonbreak), [`Conditional_GoodRoll` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_goodroll), [`StatusOnKill` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonkill), [`StatusOnTookDamage` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusontookdamage), [`StatusOnBattleStart` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonbattlestart), [`StatusEachTurnBegin` (Items_and_Equipment)](./Items_and_Equipment.md#context-statuseachturnbegin), [`AddSelfStatusToBasicAttack` (Items_and_Equipment)](./Items_and_Equipment.md#context-addselfstatustobasicattack), [`AddStatusToAllDamage` (Items_and_Equipment)](./Items_and_Equipment.md#context-addstatustoalldamage), [`StatusAlliesOnBattleStart` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusalliesonbattlestart), [`StatusOnKillEnemy` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonkillenemy), [`AddPassivesToMinions` (Items_and_Equipment)](./Items_and_Equipment.md#context-addpassivestominions), [`ApplyToSource` (Items_and_Equipment)](./Items_and_Equipment.md#context-applytosource), [`StatusOnDie` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusondie), [`StatusOnEndMove` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonendmove), [`Conditional_HasStatus` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_hasstatus), [`Else` (Items_and_Equipment)](./Items_and_Equipment.md#context-else), [`StatusOnTakeHealthOrShieldDamage` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusontakehealthorshielddamage), [`StatusOnTurnEndIfDidntCastAbilityTypes` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonturnendifdidntcastabilitytypes), [`StatusRandomEnemiesOnBattleStart` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusrandomenemiesonbattlestart), [`CatchProjectiles` (Items_and_Equipment)](./Items_and_Equipment.md#context-catchprojectiles), [`Conditional_PartyMember` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_partymember), [`PassiveWhenDead` (Items_and_Equipment)](./Items_and_Equipment.md#context-passivewhendead), [`StatusAllCharactersOnSpawn` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusallcharactersonspawn), [`StatusEveryXSpellCasts` (Items_and_Equipment)](./Items_and_Equipment.md#context-statuseveryxspellcasts), [`StatusIfUnusedMovePoints` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusifunusedmovepoints), [`StatusOnPopCorpse` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonpopcorpse), [`AddStatusToElementDamage` (Items_and_Equipment)](./Items_and_Equipment.md#context-addstatustoelementdamage), [`AddStatusToKnockbackDamage` (Items_and_Equipment)](./Items_and_Equipment.md#context-addstatustoknockbackdamage), [`AddStatusToSpells` (Items_and_Equipment)](./Items_and_Equipment.md#context-addstatustospells), [`ApplyStatusesToRandomEnemiesEachTurn` (Items_and_Equipment)](./Items_and_Equipment.md#context-applystatusestorandomenemieseachturn), [`Conditional_Adjacent` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_adjacent), [`Conditional_BadRoll` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_badroll), [`Conditional_Boss` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_boss), [`Conditional_HasTag` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_hastag), [`Conditional_OncePerBattle` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_onceperbattle), [`PassiveIfWeaponIsUsable` (Items_and_Equipment)](./Items_and_Equipment.md#context-passiveifweaponisusable), [`StatusAfterCastSpell` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusaftercastspell), [`StatusAfterXStacks` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusafterxstacks), [`StatusIfUnusedActPoints` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusifunusedactpoints), [`StatusOnAllyCatDeath` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonallycatdeath), [`StatusOnBackstab` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonbackstab), [`StatusOnBreakItem` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonbreakitem), [`StatusOnCastSpell` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusoncastspell), [`StatusOnGainCoins` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusongaincoins), [`StatusOnSetPieceBreak` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonsetpiecebreak), [`bonus_passives` (Items_and_Equipment)](./Items_and_Equipment.md#context-bonus_passives), [`keyword_tooltips` (Items_and_Equipment)](./Items_and_Equipment.md#context-keyword_tooltips), [`passive` (Items_and_Equipment)](./Items_and_Equipment.md#context-passive), [`AddPassivesToCharmed` (Items_and_Equipment)](./Items_and_Equipment.md#context-addpassivestocharmed), [`AddSelfStatusToWeapons` (Items_and_Equipment)](./Items_and_Equipment.md#context-addselfstatustoweapons), [`AddStatusToBackstabs` (Items_and_Equipment)](./Items_and_Equipment.md#context-addstatustobackstabs), [`AddStatusToFirstSpellEachTurn` (Items_and_Equipment)](./Items_and_Equipment.md#context-addstatustofirstspelleachturn), [`AddStatusToWeapons` (Items_and_Equipment)](./Items_and_Equipment.md#context-addstatustoweapons), [`ApplyPassives` (Items_and_Equipment)](./Items_and_Equipment.md#context-applypassives), [`ApplyToRandomPartyMemberIfPossible` (Items_and_Equipment)](./Items_and_Equipment.md#context-applytorandompartymemberifpossible), [`Conditional_Ally` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_ally), [`Conditional_Corpse` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_corpse), [`Conditional_Enemy` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_enemy), [`Conditional_HasCleansableDebuffs` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_hascleansabledebuffs), [`Conditional_HealthThreshold` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_healththreshold), [`Conditional_ManaThreshold` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_manathreshold), [`Conditional_PlayerCat` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_playercat), [`Conditional_RandomChance` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_randomchance), [`Conditional_Shielded` (Items_and_Equipment)](./Items_and_Equipment.md#context-conditional_shielded), [`ConvertDamageToScaledStatus` (Items_and_Equipment)](./Items_and_Equipment.md#context-convertdamagetoscaledstatus), [`CritsApplyStatus` (Items_and_Equipment)](./Items_and_Equipment.md#context-critsapplystatus), [`Eternal` (Items_and_Equipment)](./Items_and_Equipment.md#context-eternal), [`GlobalFlowerTrapperAura` (Items_and_Equipment)](./Items_and_Equipment.md#context-globalflowertrapperaura), [`PassiveWhileHasDurability` (Items_and_Equipment)](./Items_and_Equipment.md#context-passivewhilehasdurability), [`PassiveWhileInMonkMeleeStance` (Items_and_Equipment)](./Items_and_Equipment.md#context-passivewhileinmonkmeleestance), [`PassiveWhileShielded` (Items_and_Equipment)](./Items_and_Equipment.md#context-passivewhileshielded), [`RandomStatusFromPool` (Items_and_Equipment)](./Items_and_Equipment.md#context-randomstatusfrompool), [`ReviveNextRound` (Items_and_Equipment)](./Items_and_Equipment.md#context-revivenextround), [`ScaledStatusOnHolyShieldBlock` (Items_and_Equipment)](./Items_and_Equipment.md#context-scaledstatusonholyshieldblock), [`ScaledStatusOnSpendMana` (Items_and_Equipment)](./Items_and_Equipment.md#context-scaledstatusonspendmana), [`StatDependentPassive` (Items_and_Equipment)](./Items_and_Equipment.md#context-statdependentpassive), [`StatusAfterXTurns` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusafterxturns), [`StatusAlliesEachTurn` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusallieseachturn), [`StatusAlliesOnDeath` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusalliesondeath), [`StatusEachRoundEnd` (Items_and_Equipment)](./Items_and_Equipment.md#context-statuseachroundend), [`StatusEachTurnEndForEachTurn` (Items_and_Equipment)](./Items_and_Equipment.md#context-statuseachturnendforeachturn), [`StatusOnCollectPickup` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusoncollectpickup), [`StatusOnDodge` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusondodge), [`StatusOnEatFood` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusoneatfood), [`StatusOnEatPill` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusoneatpill), [`StatusOnEnemyDeath` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonenemydeath), [`StatusOnFallAsleep` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonfallasleep), [`StatusOnHealed` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonhealed), [`StatusOnPickupCoins` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonpickupcoins), [`StatusOnTurnEndIfCastNSpells` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonturnendifcastnspells), [`StatusOnUseBasicAttack` (Items_and_Equipment)](./Items_and_Equipment.md#context-statusonusebasicattack), [`StatusWhenAllySpendsMana` (Items_and_Equipment)](./Items_and_Equipment.md#context-statuswhenallyspendsmana), [`TempPassiveUntilSettled` (Items_and_Equipment)](./Items_and_Equipment.md#context-temppassiveuntilsettled), [`damage_instance` (Items_and_Equipment)](./Items_and_Equipment.md#context-damage_instance), [`CharacterTypeGainsStatusAtBattleStart` (Miscellaneous)](./Miscellaneous.md#context-charactertypegainsstatusatbattlestart), [`passives` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passives), [`AddStatusToBasicAttack` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustobasicattack), [`effects` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-effects), [`AddPassivesToMinions` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addpassivestominions), [`StatusOnTookDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusontookdamage), [`StatusEachTurnEnd` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuseachturnend), [`StatusOnBattleEnd` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonbattleend), [`StatusOnKill` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonkill), [`StatusOnStanceSwitch` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonstanceswitch), [`StatusEachTurnBegin` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuseachturnbegin), [`Conditional_Ally` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_ally), [`CritsApplyStatus` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-critsapplystatus), [`MeleeRevengeDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-meleerevengedamage), [`PassiveIfAllArmorEmpty` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passiveifallarmorempty), [`RandomStatusFromPool` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-randomstatusfrompool), [`StatusOnCrit` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusoncrit), [`Conditional_Enemy` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_enemy), [`PassiveIfEmptyFace` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passiveifemptyface), [`PassiveIfEmptyHead` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passiveifemptyhead), [`PassiveIfEmptyNeck` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passiveifemptyneck), [`StatusAlliesOnDeath` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusalliesondeath), [`StatusOnUseAbilityWithTag` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonuseabilitywithtag), [`AddStatusToElementAbilities` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustoelementabilities), [`AddStatusToWeapons` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustoweapons), [`Else` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-else), [`keyword_tooltips` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-keyword_tooltips), [`AddStatusToAllDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustoalldamage), [`AddStatusToBasicMeleeAttack` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustobasicmeleeattack), [`StatusOnCastSpell` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusoncastspell), [`StatusOnOverHealed` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonoverhealed), [`AddPassivesToCharmed` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addpassivestocharmed), [`AddStatusToElementDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustoelementdamage), [`AddStatusToExplosions` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustoexplosions), [`Conditional_FirstApplicationThisTurn` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_firstapplicationthisturn), [`PassiveWhenAtFullMana` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passivewhenatfullmana), [`StatusAlliesOnKill` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusalliesonkill), [`StatusIfUnusedMovePoints` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusifunusedmovepoints), [`StatusOnTurnEndIfCastNSpells` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonturnendifcastnspells), [`StatusOnTurnEndIfManaExact` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonturnendifmanaexact), [`StatusOnTurnEndIfManaOrHealthExact` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonturnendifmanaorhealthexact), [`AddSelfStatusToBasicAttack` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addselfstatustobasicattack), [`Conditional_BadRoll` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_badroll), [`Conditional_HasStatus` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_hasstatus), [`StatusEveryXSpellCasts` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuseveryxspellcasts), [`StatusGroup` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusgroup), [`StatusKilledCharacters` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuskilledcharacters), [`StatusOnAllyCatDeath` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonallycatdeath), [`StatusOnBattleStart` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonbattlestart), [`StatusOnEatFood` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusoneatfood), [`StatusOnGainCoins` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusongaincoins), [`StatusOnHealed` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonhealed), [`StatusOnKillEnemy` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonkillenemy), [`StatusOnTookDamageFromAbility` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusontookdamagefromability), [`statuses` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuses), [`AddPassivesToSummonAbilityMinions` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addpassivestosummonabilityminions), [`AddSelfStatusToWeapons` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addselfstatustoweapons), [`AddStatusToAllDamageAbilities` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustoalldamageabilities), [`AddStatusToFirstBasicAttack` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustofirstbasicattack), [`AddStatusToTrampleDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustotrampledamage), [`ApplyStatusIfCrit` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-applystatusifcrit), [`ApplyStatusesToRandomEnemiesEachTurn` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-applystatusestorandomenemieseachturn), [`ApplyToSource` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-applytosource), [`CatchProjectiles` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-catchprojectiles), [`Conditional_Adjacent` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_adjacent), [`Conditional_Boss` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_boss), [`Conditional_Corpse` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_corpse), [`Conditional_HasTag` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_hastag), [`Conditional_NotBoss` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_notboss), [`Conditional_PartyMember` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_partymember), [`Conditional_Shielded` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_shielded), [`Electric` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-electric), [`Eternal` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-eternal), [`Fire` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-fire), [`Grass` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-grass), [`Gravity` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-gravity), [`Holy` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-holy), [`HolyDamageBlessing` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-holydamageblessing), [`Ice` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-ice), [`LateBloomer` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-latebloomer), [`LightningRod` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-lightningrod), [`NextBattleStatus` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-nextbattlestatus), [`PassiveAtFullHealth` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passiveatfullhealth), [`PassiveGroup` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passivegroup), [`PassiveUntilCastSpell` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passiveuntilcastspell), [`PassiveWhileInMonkMeleeStance` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passivewhileinmonkmeleestance), [`PassiveWhileInMonkRangedStance` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passivewhileinmonkrangedstance), [`PassiveWhilePreviewingMonkRangedStance` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passivewhilepreviewingmonkrangedstance), [`ScaledStatusOnOverMana` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-scaledstatusonovermana), [`ScaledStatusOnSpendMana` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-scaledstatusonspendmana), [`SpecialFriends` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-specialfriends), [`StatusAfterCastSpell` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusaftercastspell), [`StatusAlliesOnBattleStart` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusalliesonbattlestart), [`StatusAlliesOnGainCoins` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusalliesongaincoins), [`StatusAllyWhenAllySpendsMana` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusallywhenallyspendsmana), [`StatusAnyCatAllyWhoKills` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusanycatallywhokills), [`StatusDamagers` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusdamagers), [`StatusEachTurnEndForEachTurn` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuseachturnendforeachturn), [`StatusEachTurnEndPerEnemyKill` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuseachturnendperenemykill), [`StatusEnemiesOnDeath` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusenemiesondeath), [`StatusEveryXTurnBegins` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuseveryxturnbegins), [`StatusKillers` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuskillers), [`StatusOnAnyDeath` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonanydeath), [`StatusOnBreakItem` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonbreakitem), [`StatusOnCollectPickup` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusoncollectpickup), [`StatusOnDealtDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusondealtdamage), [`StatusOnDealtDamageThreshold` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusondealtdamagethreshold), [`StatusOnEndMove` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonendmove), [`StatusOnGainShield` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusongainshield), [`StatusOnHeal` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonheal), [`StatusOnOverMana` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonovermana), [`StatusOnPickupCoins` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonpickupcoins), [`StatusOnPopCorpse` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonpopcorpse), [`StatusOnTookDamageFromEnemyAbility` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusontookdamagefromenemyability), [`StatusOnTriggerTrap` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusontriggertrap), [`StatusOnUseBasicAttack` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonusebasicattack), [`StatusOnUseElementAbility` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonuseelementability), [`StatusPerInjury` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusperinjury), [`StatusWhenAllySpendsMana` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statuswhenallyspendsmana), [`TaggedPickupEffectReplacement` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-taggedpickupeffectreplacement), [`AddStatusToKnockbackDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustoknockbackdamage), [`AddStatusToSpells` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatustospells), [`AddStatusesIfPersistentWeatherElement` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatusesifpersistentweatherelement), [`AddStatusesToReceivedElementalDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-addstatusestoreceivedelementaldamage), [`Conditional_DoesDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_doesdamage), [`Conditional_GoodRoll` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-conditional_goodroll), [`Diabetes` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-diabetes), [`PassiveLevelScaledStatus` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-passivelevelscaledstatus), [`RandomPassivePool` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-randompassivepool), [`ScaledStatusOnBleedDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-scaledstatusonbleeddamage), [`ScaledStatusOnLoseShield` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-scaledstatusonloseshield), [`StatusAlliesEachTurn` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusallieseachturn), [`StatusAlliesOnSpendMana` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusalliesonspendmana), [`StatusAlliesScaledByCursedOnDeath` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusalliesscaledbycursedondeath), [`StatusIfBattleAlreadyBegan` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusifbattlealreadybegan), [`StatusOnEatPill` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusoneatpill), [`StatusOnLoseShield` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonloseshield), [`StatusOnTakeHealthDamage` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusontakehealthdamage), [`StatusOnTurnEndIfDidntCastAbilityTypes` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-statusonturnendifdidntcastabilitytypes), [`TakeBonusTurnWithStatus` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-takebonusturnwithstatus), [`TheHunger` (Passives_and_Statuses)](./Passives_and_Statuses.md#context-thehunger)

### Valid Property Keys

<details>
<summary><b>Expand</b></summary>

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`AddStatusToBasicAttack`](#addstatustobasicattack) | Object | Injects a status effect payload that applies whenever the character performs a basic attack. | 246 |
| [`self_status_next_fight`](#self_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect specifically to the character that triggered the event during the next combat encounter. | 143 |
| [`bonus_passives`](#bonus_passives) | Object | Passives granted to the character while this ability is equipped. | 138 |
| `Brace` | Number | Applies or references the 'Brace' effect/state. | 119 |
| [`FormChanger`](#formchanger) | Object | AI Role: Designates the character as one that frequently shifts forms. | 106 |
| `Thorns` | Number | Applies or references the 'Thorns' effect/state. | 99 |
| [`Trample`](./Arrays.md#array-trample) | Number | Applies or references the 'Trample' effect/state. | 96 |
| [`Poison`](./Arrays.md#array-poison) | Number | Applies or references the 'Poison' effect/state. | 92 |
| `Metal` | Integer | Applies or references the 'Metal' effect/state. | 91 |
| [`Bleed`](./Arrays.md#array-bleed) | Number | Applies or references the 'Bleed' effect/state. | 87 |
| `HealthRegenUp` | Number | Applies or references the 'HealthRegenUp' effect/state. | 82 |
| [`SpawnOnDeath`](./Enums.md#enum-spawnondeath) | Object | Event Trigger: Spawns a specific entity when killed. | 81 |
| [`MeleeRevengeDamage`](#meleerevengedamage) | Object | Reaction trigger: Applies nested status effects to the attacker when hit by a melee attack. | 71 |
| [`Fear`](./Arrays.md#array-fear) | Array | Applies or references the 'Fear' effect/state. | 59 |
| [`StatusEachTurnEnd`](#statuseachturnend) | Object | Applies or references the 'StatusEachTurnEnd' effect/state. | 57 |
| [`passives`](#passives) | Object | Examples: `{ ... }` | 53 |
| [`SpawnOnBattleStart`](./Enums.md#enum-spawnonbattlestart) | Enum | Applies or references the 'SpawnOnBattleStart' effect/state. | 53 |
| [`StatusOnBattleEnd`](#statusonbattleend) | Object | Applies the nested status effects when the encounter finishes. | 53 |
| `DamageUp` | Number | Applies or references the 'DamageUp' effect/state. | 52 |
| [`ElementImmune`](./Enums.md#enum-elementimmune) | Enum | Applies or references the 'ElementImmune' effect/state. | 48 |
| `Robot` | Integer | Character Form: Behavior and stats for the 'Robot' state. | 48 |
| [`StatusOnTookDamage`](#statusontookdamage) | Object | Event Trigger: Applies nested statuses when took damage. | 46 |
| `RandomArmorPickup` | Number | Applies or references the 'RandomArmorPickup' effect/state. | 43 |
| [`StatusOnKill`](#statusonkill) | Object | Event Trigger: Applies statuses when this action occurs. | 40 |
| [`SpawnThingOnDamage`](#spawnthingondamage) | Object | Applies or references the 'SpawnThingOnDamage' effect/state. | 38 |
| [`StatusImmunity`](./Enums.md#enum-statusimmunity) | Enum | Applies or references the 'StatusImmunity' effect/state. | 38 |
| `CritChanceUp` | Number | Applies or references the 'CritChanceUp' effect/state. | 37 |
| [`AddPassivesToMinions`](#addpassivestominions) | Object | Applies the 'AddPassivesToMinions' effect. | 36 |
| [`CounterAttack`](./Enums.md#enum-counterattack) | Enum | Reaction: Executes a counter-attack ability when hit. | 36 |
| [`DeathRattle`](./Enums.md#enum-deathrattle) | Enum | Event Trigger: Executes logic or abilities exactly when the character dies. | 36 |
| `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. | 36 |
| [`FormChangeWhileHasStatus`](#formchangewhilehasstatus) | Object | Logic: Changes form automatically while possessing a specific status. | 35 |
| [`RevengeDamage`](#revengedamage) | Object | Reaction trigger: Deals damage to the attacker when hit. | 31 |
| `Charge` | Number | Applies or references the 'Charge' effect/state. | 30 |
| [`damage`](./Arrays.md#array-damage) | Integer | The base damage properties of an attack. | 30 |
| [`EliteTint`](./Arrays.md#array-elitetint) | Array | Examples: `[ .4 .4 .4 ], [ .6 .6 .6 .50 ], red` | 30 |
| `DodgeChance` | Integer | Examples: `2, 5, 10` | 29 |
| `AddBonusRange` | Integer | Applies or references the 'AddBonusRange' effect/state. | 28 |
| `KineticSpikes` | Number | Applies or references the 'KineticSpikes' effect/state. | 28 |
| [`MulticlassLevelUp`](./Enums.md#enum-multiclasslevelup) | Enum | Applies the 'MulticlassLevelUp' effect. | 28 |
| `knockback` | Integer | The base physics pushing power (in tiles). | 27 |
| [`StatusEachTurnBegin`](#statuseachturnbegin) | Object | Event Trigger: Applies nested statuses to each turn begin. | 27 |
| `Fire` | Object | Character Form: Behavior and stats for the 'Fire' state. | 26 |
| [`ImmediateAbilityReaction`](./Enums.md#enum-immediateabilityreaction) | Enum | Reaction: Executes an ability instantly, interrupting the current sequence. | 26 |
| `Knockback` | Number | Applies or references the 'Knockback' effect/state. | 26 |
| [`AbilityReaction`](./Enums.md#enum-abilityreaction) | Enum | AI Trigger: Executes an ability in reaction to a specific event (e.g., taking damage). | 25 |
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. | 25 |
| [`Quivered`](./Arrays.md#array-quivered) | Number | Applies or references the 'Quivered' effect/state. | 25 |
| `Undead` | Integer | Applies or references the 'Undead' effect/state. | 25 |
| `AddMovement` | Integer | Applies or references the 'AddMovement' effect/state. | 24 |
| `Brittle` | Integer | Applies or references the 'Brittle' effect/state. | 24 |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type to check for. | 24 |
| [`party_status_next_fight`](#party_status_next_fight) | Object | Event Penalty/Reward: Applies a status effect to the entire party at the start of the next combat encounter. | 24 |
| `water` | Variable |  | 24 |
| [`AddElementsToBasicAttack`](./Enums.md#enum-addelementstobasicattack) | Enum | Examples: `Ice, Electric, Water` | 23 |
| `MissChance` | Integer | Applies the 'MissChance' effect. | 23 |
| `RandomStatUp` | Number | Applies or references the 'RandomStatUp' effect/state. | 23 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 23 |
| [`DivineShield`](./Arrays.md#array-divineshield) | Number | Applies or references the 'DivineShield' effect/state. | 22 |
| `Fragile` | Integer | Applies or references the 'Fragile' effect/state. | 22 |
| [`mode`](./Enums.md#enum-mode) | Enum | `equal`, `greater`, `greater_or_equal`, `less_or_equal`, `yeet` | 22 |
| [`ReplaceBasicAttack`](./Enums.md#enum-replacebasicattack) | Enum | Applies or references the 'ReplaceBasicAttack' effect/state. | 22 |
| [`SpawnEachTurn`](#spawneachturn) | Object | Applies or references the 'SpawnEachTurn' effect/state. | 22 |
| [`StatusOnBreak`](#statusonbreak) | Object | Event Trigger: Applies statuses when this action occurs. | 22 |
| [`threshold`](#threshold) | Object | Examples: `4*champion_multiplier, 3*champion_multiplier, 1` | 22 |
| `WaterWalk` | Integer | Applies or references the 'WaterWalk' effect/state. | 21 |
| `AddCorpseHealth` | Integer | Applies the 'AddCorpseHealth' effect. | 20 |
| [`additional_passives`](#additional_passives) | Object | Passives granted intrinsically to a spawned entity. | 20 |
| `ArmorDodgeChance` | Integer | Applies or references the 'ArmorDodgeChance' effect/state. | 20 |
| [`BossRewards`](#bossrewards) | Object | Loot logic: Rewards dropped upon defeating a boss. | 20 |
| [`ForceUseAbility`](./Enums.md#enum-forceuseability) | Enum | Applies or references the 'ForceUseAbility' effect/state. | 20 |
| `BleedThorns` | Number | Applies or references the 'BleedThorns' effect/state. | 19 |
| [`EliteParticle`](./Enums.md#enum-eliteparticle) | Enum | Examples: `SpikeBuff, Lava_Distortion, SparkleBuff` | 19 |
| [`FindItemFromPool`](./Enums.md#enum-finditemfrompool) | Object | Generates an item drop from the specified loot pool. | 19 |
| `AddCritMultiplier` | Integer | Applies the 'AddCritMultiplier' effect. | 18 |
| [`BirdRewards`](#birdrewards) | Object | Loot logic: Rewards dropped by bird-type enemies. | 18 |
| [`Buddy`](./Enums.md#enum-buddy) | Enum | Character Form / AI State: Behavior and stats for the 'Buddy' familiar state. | 18 |
| [`InnateElement`](./Enums.md#enum-innateelement) | Enum | Applies the 'InnateElement' effect. | 18 |
| [`PassiveWhenAffectedByElement`](#passivewhenaffectedbyelement) | Object | Examples: `{ ... }` | 18 |
| [`AbilityOnBattleStart_Immediate`](./Enums.md#enum-abilityonbattlestart_immediate) | Enum | Applies or references the 'AbilityOnBattleStart_Immediate' effect/state. | 17 |
| `Conditional_GoodRoll` | Object | Conditional trigger: Executes nested logic based on a randomized favorable outcome probability. | 17 |
| `LuckUp` | Number | Applies or references the 'LuckUp' effect/state. | 17 |
| `RandomMagicMissile` | Object | Fires a randomized number of magic missiles. | 17 |
| [`ReplaceBasicMove`](./Enums.md#enum-replacebasicmove) | Enum | Applies or references the 'ReplaceBasicMove' effect/state. | 17 |
| `AddManaRegen` | Integer | Applies or references the 'AddManaRegen' effect/state. | 16 |
| [`CharacterLightSource`](#characterlightsource) | Object | Visual: Attaches a dynamic lighting source to the character. | 16 |
| [`HealthPickup`](#healthpickup) | Object | Pickup Logic: Defines what happens when a health item is collected. | 16 |
| `less_or_equal` | Variable |  | 16 |
| [`SizeScale`](./Enums.md#enum-sizescale) | Enum | Applies or references the 'SizeScale' effect/state. | 16 |
| [`SpawnThingOnDeath`](./Enums.md#enum-spawnthingondeath) | Enum | Applies or references the 'SpawnThingOnDeath' effect/state. | 16 |
| [`StatusOnBattleStart`](#statusonbattlestart) | Object | Event Trigger: Applies statuses when this action occurs. | 16 |
| [`AbilityOnBattleStart`](./Enums.md#enum-abilityonbattlestart) | Enum | Applies or references the 'AbilityOnBattleStart' effect/state. | 15 |
| `ExtraBasicAttacks` | Integer | Applies the 'ExtraBasicAttacks' effect. | 15 |
| `HealthMultiplier` | Float | Examples: `1.5, .5, .8` | 15 |
| `IgnoreTiles` | Integer | Applies or references the 'IgnoreTiles' effect/state. | 15 |
| [`ReplaceSpawnedObjects`](./Arrays.md#array-replacespawnedobjects) | Array | Applies or references the 'ReplaceSpawnedObjects' effect/state. | 15 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 15 |
| `AddLevelUpRerolls` | Integer | Applies or references the 'AddLevelUpRerolls' effect/state. | 14 |
| `Antidote` | Mixed | Applies or references the 'Antidote' effect/state. | 14 |
| `Flying` | Integer | Applies or references the 'Flying' effect/state. | 14 |
| [`MoveQuivered`](./Arrays.md#array-movequivered) | Number | Applies or references the 'MoveQuivered' effect/state. | 14 |
| [`PassiveGroup`](#passivegroup) | Object | Passive: A collection of passives grouped together for easier management. | 14 |
| `PoisonThorns` | Integer | Applies or references the 'PoisonThorns' effect/state. | 14 |
| `ReflectProjectiles` | Integer | Passive: Reflects incoming projectiles back at the attacker. | 14 |
| `stacks` | Integer | Number of stacks or intensity to apply. | 14 |
| [`statuses`](#statuses) | Object | Status effects possessed by the character. | 14 |
| [`AbilityHealthThreshold`](#abilityhealththreshold) | Object | AI Trigger: Executes an ability when health drops below a specific threshold. | 13 |
| [`AddStatusToAllDamage`](#addstatustoalldamage) | Object | Modifier: Injects a status effect into a specific action. | 13 |
| `AlphaTurns` | Integer | Applies the 'AlphaTurns' effect. | 13 |
| [`ApplyPassives`](#applypassives) | Object | Grants the nested passive abilities dynamically. | 13 |
| [`BonusAbility`](./Enums.md#enum-bonusability) | Enum | Applies the 'BonusAbility' effect. | 13 |
| [`DeathRattleRevive`](./Enums.md#enum-deathrattlerevive) | Object | Event Trigger: Revives the character immediately upon death. | 13 |
| `Flammable` | Integer | Applies or references the 'Flammable' effect/state. | 13 |
| `InjuryImmunity` | Integer | Applies or references the 'InjuryImmunity' effect/state. | 13 |
| [`PassiveAtStatThreshold`](#passiveatstatthreshold) | Object | Applies the 'PassiveAtStatThreshold' effect. | 13 |
| `SafeDoomed` | Number | Applies or references the 'SafeDoomed' effect/state. | 13 |
| [`TransformOnDeath`](./Enums.md#enum-transformondeath) | Enum | Applies or references the 'TransformOnDeath' effect/state. | 13 |
| `AddMaxHealth` | Integer | Applies or references the 'AddMaxHealth' effect/state. | 12 |
| [`AddTag`](./Enums.md#enum-addtag) | Enum | Applies or references the 'AddTag' effect/state. | 12 |
| [`AmplifyStatus`](./Enums.md#enum-amplifystatus) | Enum | Applies the 'AmplifyStatus' effect. | 12 |
| `BackstabImmunity` | Integer | Applies or references the 'BackstabImmunity' effect/state. | 12 |
| [`DeadAltAbility`](./Enums.md#enum-deadaltability) | Enum | Applies or references the 'DeadAltAbility' effect/state. | 12 |
| [`elements`](./Arrays.md#array-elements) | Array | Array of elemental tags to apply (e.g., `[Fire Holy]`). | 12 |
| [`EquipTemporaryItem`](./Enums.md#enum-equiptemporaryitem) | Enum | Applies the 'EquipTemporaryItem' effect. | 12 |
| [`MoveWhenDamaged`](./Enums.md#enum-movewhendamaged) | Enum | AI Movement: Forces a reposition when taking damage. | 12 |
| `NoHealthOnlyShield` | Integer | Applies or references the 'NoHealthOnlyShield' effect/state. | 12 |
| [`ObjectOnHitCharacter`](./Enums.md#enum-objectonhitcharacter) | Object | Spawns a specific character or entity upon impact. | 12 |
| `AddBonusMeleeRange` | Integer | Applies the 'AddBonusMeleeRange' effect. | 11 |
| [`AddSelfStatusToBasicAttack`](#addselfstatustobasicattack) | Object | Applies or references the 'AddSelfStatusToBasicAttack' effect/state. | 11 |
| [`AddStatusToBasicMeleeAttack`](#addstatustobasicmeleeattack) | Object | Examples: `{ ... }` | 11 |
| [`CritsApplyStatus`](#critsapplystatus) | Object | Applies the 'CritsApplyStatus' effect. | 11 |
| [`EliteFlatTint`](./Arrays.md#array-eliteflattint) | Array | Examples: `[ 1.1 1.1 1.1 ], [ 1.1 1.1 1.3 ], [ 1.1 1.1 1 ]` | 11 |
| [`MoveTowardsDamageSource`](./Enums.md#enum-movetowardsdamagesource) | Enum | AI Movement: Closes distance on the last source of damage. | 11 |
| `PermanentMadness` | Integer | Applies or references the 'PermanentMadness' effect/state. | 11 |
| [`SpawnOnBattleStartRandomEmptyTile`](#spawnonbattlestartrandomemptytile) | Object | Applies or references the 'SpawnOnBattleStartRandomEmptyTile' effect/state. | 11 |
| [`StatusOnKillEnemy`](#statusonkillenemy) | Object | Event Trigger: Applies statuses when this action occurs. | 11 |
| [`YOffset`](./Enums.md#enum-yoffset) | Float | Applies or references the 'YOffset' effect/state. | 11 |
| `AddInitiative` | Integer | Applies or references the 'AddInitiative' effect/state. | 10 |
| [`AutocastEachRound`](#autocasteachround) | Object | Forces the character to automatically cast a specific ability at the start of each combat round. | 10 |
| `BrambleRandomTileEvent` | Variable |  | 10 |
| `CoinPickup` | Integer | Applies or references the 'CoinPickup' effect/state. | 10 |
| [`DepressionAura`](#depressionaura) | Object | Examples: `1` | 10 |
| `DodgeChance_Status` | Number | Applies or references the 'DodgeChance_Status' effect/state. | 10 |
| `Electric` | Object | Examples: `{ ... }` | 10 |
| `ExtraWeaponAttacks` | Integer | Applies the 'ExtraWeaponAttacks' effect. | 10 |
| `FadeInsteadOfDie` | Integer | Applies or references the 'FadeInsteadOfDie' effect/state. | 10 |
| [`GainCoins`](./Arrays.md#array-gaincoins) | Integer | Applies or references the 'GainCoins' effect/state. | 10 |
| `Ice` | Object | Examples: `{ ... }` | 10 |
| `IncreaseExplosionDamage` | Integer | Applies the 'IncreaseExplosionDamage' effect. | 10 |
| `KnockbackImmunity` | Integer | Applies the 'KnockbackImmunity' effect. | 10 |
| `LimitDamage` | Integer | Applies or references the 'LimitDamage' effect/state. | 10 |
| [`MovementReaction`](#movementreaction) | Object | Reaction: Triggers an effect or ability when forced to move. | 10 |
| `PassiveLevelUpAtCombatEnd` | Integer | Applies the 'PassiveLevelUpAtCombatEnd' effect. | 10 |
| `RandomPermanentStat` | Number | Applies or references the 'RandomPermanentStat' effect/state. | 10 |
| [`StatusAlliesOnBattleStart`](#statusalliesonbattlestart) | Object | Applies or references the 'StatusAlliesOnBattleStart' effect/state. | 10 |
| [`StatusOnEndMove`](#statusonendmove) | Object | Event Trigger: Applies statuses when this action occurs. | 10 |
| `StripStatuses` | Integer | Applies or references the 'StripStatuses' effect/state. | 10 |
| `TrinketPassiveMultiplierBonus` | Integer | Applies or references the 'TrinketPassiveMultiplierBonus' effect/state. | 10 |
| [`AddDamageToElementDamage`](#adddamagetoelementdamage) | Object | Applies or references the 'AddDamageToElementDamage' effect/state. | 9 |
| `BoostHeals` | Integer | Applies or references the 'BoostHeals' effect/state. | 9 |
| `BoostWeaponDamage` | Integer | Applies the 'BoostWeaponDamage' effect. | 9 |
| `ChanceToRevive` | Integer | Applies or references the 'ChanceToRevive' effect/state. | 9 |
| [`count`](./Arrays.md#array-count) | Integer | Quantity. | 9 |
| `Creep` | Variable |  | 9 |
| `DiminishingHealthRegen` | Number | Applies or references the 'DiminishingHealthRegen' effect/state. | 9 |
| [`FormChangeOnElementInfluence`](#formchangeonelementinfluence) | Object | Logic: Changes form when affected by an element. | 9 |
| `LimitHeal` | Integer | Applies or references the 'LimitHeal' effect/state. | 9 |
| `ManaCostReduction` | Integer | Applies or references the 'ManaCostReduction' effect/state. | 9 |
| [`PassiveAtHealthThreshold`](#passiveathealththreshold) | Object | Applies or references the 'PassiveAtHealthThreshold' effect/state. | 9 |
| `Plant` | Integer | Applies or references the 'Plant' effect/state. | 9 |
| `RandomMutation` | Number | Applies or references the 'RandomMutation' effect/state. | 9 |
| [`Rot`](./Arrays.md#array-rot) | Array | Applies or references the 'Rot' effect/state. | 9 |
| `SmallRockBehavior` | Integer | AI Logic: Movement/interaction profile for small rocks. | 9 |
| `SpellDamageUp` | Number | Applies or references the 'SpellDamageUp' effect/state. | 9 |
| [`StatusCollector`](#statuscollector) | Object | Passive: Gains benefits based on the number of statuses applied to them. | 9 |
| [`StatusOnDie`](#statusondie) | Object | Event Trigger: Applies statuses when this action occurs. | 9 |
| [`StatusOnTookDamageFromAbility`](#statusontookdamagefromability) | Object | Event Trigger: Applies statuses when taking damage from an ability. | 9 |
| [`TransformInXTurns`](#transforminxturns) | Object | Logic: Forces a form change after X turns. | 9 |
| [`TransformOnElementInfluence`](#transformonelementinfluence) | Object | Logic: Changes form when affected by elements. | 9 |
| `AddKnockbackDamage` | Integer | Applies or references the 'AddKnockbackDamage' effect/state. | 8 |
| [`AddStatusToWeapons`](#addstatustoweapons) | Object | Applies the 'AddStatusToWeapons' effect. | 8 |
| [`CharacterTypeGainsStatusAtBattleStart`](#charactertypegainsstatusatbattlestart) | Object | Encounter Modifier: Applies a status effect to all characters of a specific type (e.g., Cats, Bosses) at the start of battle. | 8 |
| `DebuffImmunity` | Integer | Applies or references the 'DebuffImmunity' effect/state. | 8 |
| `ExtraMovePoints` | Integer | Applies the 'ExtraMovePoints' effect. | 8 |
| [`ForceSpecificInjury`](./Enums.md#enum-forcespecificinjury) | Enum | Applies the 'ForceSpecificInjury' effect. | 8 |
| [`FormChangeOffMap`](#formchangeoffmap) | Object | Logic: Changes form when pushed off the map. | 8 |
| [`FreePathfindElement`](./Enums.md#enum-freepathfindelement) | Enum | Applies the 'FreePathfindElement' effect. | 8 |
| `NonStackingDivineShield` | Number | Applies or references the 'NonStackingDivineShield' effect/state. | 8 |
| `NonStackingShield` | Integer | Examples: `12, 4, 8` | 8 |
| [`PassiveIfAllArmorEmpty`](#passiveifallarmorempty) | Object | Applies the 'PassiveIfAllArmorEmpty' effect. | 8 |
| [`RandomizeAIWeightsEachTurn`](./Arrays.md#array-randomizeaiweightseachturn) | Array | Applies or references the 'RandomizeAIWeightsEachTurn' effect/state. | 8 |
| [`RandomStatusFromPool`](#randomstatusfrompool) | Object | Selects and applies a random status effect from the provided nested object. | 8 |
| [`SecurityBotProtect`](#securitybotprotect) | Object | AI Logic: Guarding behavior for Security Bot units. | 8 |
| `SetSpellCosts` | Integer | Applies the 'SetSpellCosts' effect. | 8 |
| [`SpawnOnDowned`](./Enums.md#enum-spawnondowned) | Enum | Examples: `CharmedKitten, CharmedFly` | 8 |
| [`StatusAlliesOnDeath`](#statusalliesondeath) | Object | Event Trigger: Applies nested statuses to allies on death. | 8 |
| [`StatusEachRoundBegin`](#statuseachroundbegin) | Object | Examples: `{ ... }` | 8 |
| [`StatusEveryXSpellCasts`](#statuseveryxspellcasts) | Object | Applies or references the 'StatusEveryXSpellCasts' effect/state. | 8 |
| [`StatusIfUnusedMovePoints`](#statusifunusedmovepoints) | Object | Event Trigger: Applies nested statuses to if unused move points. | 8 |
| [`StatusOnCastSpell`](#statusoncastspell) | Object | Event Trigger: Applies nested statuses when cast spell. | 8 |
| [`StatusOnCrit`](#statusoncrit) | Object | Event Trigger: Applies nested statuses when crit. | 8 |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 8 |
| [`TileTrail`](./Enums.md#enum-tiletrail) | Enum | Applies or references the 'TileTrail' effect/state. | 8 |
| `AbilityEnabledOncePerFightAtHealthThreshold` | Integer | Applies or references the 'AbilityEnabledOncePerFightAtHealthThreshold' effect/state. | 7 |
| [`AbilityWhenBuddyDies`](./Enums.md#enum-abilitywhenbuddydies) | Enum | Applies or references the 'AbilityWhenBuddyDies' effect/state. | 7 |
| [`AddTemporaryEffectsToBasicAttack`](#addtemporaryeffectstobasicattack) | Object | Applies the 'AddTemporaryEffectsToBasicAttack' effect. | 7 |
| `BlastResistance` | Integer | Applies the 'BlastResistance' effect. | 7 |
| [`BrittleDuringElement`](./Enums.md#enum-brittleduringelement) | Enum | Applies or references the 'BrittleDuringElement' effect/state. | 7 |
| [`ChanceToSpitOnDamage`](#chancetospitondamage) | Object | Reaction: Probability to use a spit counter-attack when damaged. | 7 |
| `CharismaUp` | Number | Applies or references the 'CharismaUp' effect/state. | 7 |
| [`ClassManaCostReduction`](#classmanacostreduction) | Object | Applies or references the 'ClassManaCostReduction' effect/state. | 7 |
| [`DamageNeighborsOnEndMove`](#damageneighborsonendmove) | Object | Combat Trigger: Deals damage to neighbors on end move. | 7 |
| [`DurabilityTransform`](#durabilitytransform) | Object | Applies or references the 'DurabilityTransform' effect/state. | 7 |
| `GainCoinsRange` | Object | Grants the player a randomized amount of coins within a min/max range. | 7 |
| `IncreaseExplosionSize` | Integer | Applies or references the 'IncreaseExplosionSize' effect/state. | 7 |
| `MinimumKnockbackFromAllDamage` | Integer | Applies or references the 'MinimumKnockbackFromAllDamage' effect/state. | 7 |
| [`OverrideBasicAttack`](./Enums.md#enum-overridebasicattack) | Enum | Applies or references the 'OverrideBasicAttack' effect/state. | 7 |
| `OverrideMaxHealth` | Integer | Applies or references the 'OverrideMaxHealth' effect/state. | 7 |
| [`PassiveIfEmptyFace`](#passiveifemptyface) | Object | Applies the 'PassiveIfEmptyFace' effect. | 7 |
| [`PassiveIfEmptyHead`](#passiveifemptyhead) | Object | Applies the 'PassiveIfEmptyHead' effect. | 7 |
| [`PassiveIfEmptyNeck`](#passiveifemptyneck) | Object | Applies the 'PassiveIfEmptyNeck' effect. | 7 |
| [`PassiveIfStrAuxEquals`](#passiveifstrauxequals) | Object | Applies or references the 'PassiveIfStrAuxEquals' effect/state. | 7 |
| [`PassiveWhenOnTile`](#passivewhenontile) | Object | State Trigger: Grants passives when this condition is met. | 7 |
| [`SetFragileImmune`](./Enums.md#enum-setfragileimmune) | Enum | Applies or references the 'SetFragileImmune' effect/state. | 7 |
| [`StatusOnUseAbilityWithTag`](#statusonuseabilitywithtag) | Object | Event Trigger: Applies nested statuses when use ability with tag. | 7 |
| [`Webbed`](./Arrays.md#array-webbed) | Number | Applies or references the 'Webbed' effect/state. | 7 |
| `XIsFreeArmorSlots` | Integer | Applies or references the 'XIsFreeArmorSlots' effect/state. | 7 |
| `AbilityEnabledPercentEachTurn` | Integer | Applies or references the 'AbilityEnabledPercentEachTurn' effect/state. | 6 |
| `AddDamage` | Integer | Applies or references the 'AddDamage' effect/state. | 6 |
| [`AddHiddenTag`](./Enums.md#enum-addhiddentag) | Enum | Applies or references the 'AddHiddenTag' effect/state. | 6 |
| `AddStartingMana` | Number | Applies or references the 'AddStartingMana' effect/state. | 6 |
| [`AddStatusToElementAbilities`](#addstatustoelementabilities) | Object | Applies the 'AddStatusToElementAbilities' effect. | 6 |
| [`AddStatusToElementDamage`](#addstatustoelementdamage) | Object | Applies the 'AddStatusToElementDamage' effect. | 6 |
| [`BackstabCritChance`](./Enums.md#enum-backstabcritchance) | Float | Applies the 'BackstabCritChance' effect. | 6 |
| `BasicAttackDamageMultiplier` | Integer | Applies the 'BasicAttackDamageMultiplier' effect. | 6 |
| [`CaveFamilyEnrage`](#cavefamilyenrage) | Object | AI Trigger: Enrage logic triggered when a cave family member is killed. | 6 |
| [`ChanceToBackflip`](#chancetobackflip) | Object | Applies or references the 'ChanceToBackflip' effect/state. | 6 |
| `Conditional_BadRoll` | Object | Conditional trigger: Executes nested logic based on a randomized bad outcome probability. | 6 |
| [`CureDisease`](#curedisease) | Object | Applies the 'CureDisease' effect. | 6 |
| [`DelayedAutoRevive`](#delayedautorevive) | Object | Applies or references the 'DelayedAutoRevive' effect/state. | 6 |
| [`Divide4OnDeath`](./Enums.md#enum-divide4ondeath) | Enum | Applies or references the 'Divide4OnDeath' effect/state. | 6 |
| `FaceShield` | Integer | Applies or references the 'FaceShield' effect/state. | 6 |
| [`FormChangeWhilePrimingAbility`](#formchangewhileprimingability) | Object | Logic: Changes form while preparing/priming a specific ability. | 6 |
| `FreeFirstCast` | Integer | Applies or references the 'FreeFirstCast' effect/state. | 6 |
| `FreezePiercing` | Integer | Applies the 'FreezePiercing' effect. | 6 |
| [`ItemAuxTransform`](#itemauxtransform) | Object | Applies or references the 'ItemAuxTransform' effect/state. | 6 |
| `KaijuKnockbackImmune` | Integer | Applies or references the 'KaijuKnockbackImmune' effect/state. | 6 |
| [`LevelUpClassOverride`](./Enums.md#enum-levelupclassoverride) | Enum | Applies the 'LevelUpClassOverride' effect. | 6 |
| [`ManaCostReductionTagged`](#manacostreductiontagged) | Object | Applies the 'ManaCostReductionTagged' effect. | 6 |
| [`PassiveWhileHasStatus`](#passivewhilehasstatus) | Object | Passive: Activates only while the character has the specified status. | 6 |
| `PermanentConstitution` | Number | Applies or references the 'PermanentConstitution' effect/state. | 6 |
| [`ReplaceBasicAttackWhenCastable`](./Enums.md#enum-replacebasicattackwhencastable) | Enum | Applies the 'ReplaceBasicAttackWhenCastable' effect. | 6 |
| [`ScatterCoins`](./Arrays.md#array-scattercoins) | Object | Throws coins out into the level randomly. | 6 |
| [`SetBrittleImmune`](./Enums.md#enum-setbrittleimmune) | Enum | Applies or references the 'SetBrittleImmune' effect/state. | 6 |
| [`SpawnObjectOnPopCorpse`](./Enums.md#enum-spawnobjectonpopcorpse) | Enum | Applies or references the 'SpawnObjectOnPopCorpse' effect/state. | 6 |
| [`StatusOnAllyCatDeath`](#statusonallycatdeath) | Object | Event Trigger: Applies nested statuses when ally cat death. | 6 |
| [`StatusOnGainCoins`](#statusongaincoins) | Object | Event Trigger: Applies nested statuses when gain coins. | 6 |
| [`StatusOnStanceSwitch`](#statusonstanceswitch) | Object | Event Trigger: Applies nested statuses when stance switch. | 6 |
| `StunImmunity` | Integer | Passive: Prevents Stun from being applied. | 6 |
| [`TagGreed`](./Enums.md#enum-taggreed) | Enum | Applies or references the 'TagGreed' effect/state. | 6 |
| `TrinketActiveEffectsMultiplierBonus` | Integer | Applies or references the 'TrinketActiveEffectsMultiplierBonus' effect/state. | 6 |
| [`AbilityWhenTaggedCharacterMovesNear`](#abilitywhentaggedcharactermovesnear) | Object | AI Trigger: Executes an ability when a character with a specific tag moves adjacent. | 5 |
| [`AddPassivesToCharmed`](#addpassivestocharmed) | Object | Applies the 'AddPassivesToCharmed' effect. | 5 |
| `ally_chance` | Integer | Examples: `15, 100` | 5 |
| `AmplifyKnockback` | Integer | Applies the 'AmplifyKnockback' effect. | 5 |
| `Angel` | Integer | Applies or references the 'Angel' effect/state. | 5 |
| `BasicAttackAOEBonus` | Integer | Applies the 'BasicAttackAOEBonus' effect. | 5 |
| [`BlacklistPickupType`](./Enums.md#enum-blacklistpickuptype) | Enum | Examples: `food, catnip` | 5 |
| [`CatchProjectiles`](#catchprojectiles) | Object | Applies or references the 'CatchProjectiles' effect/state. | 5 |
| [`chance`](./Enums.md#enum-chance) | Float | Probability (0.0 to 1.0 or percentage) of this occurring. | 5 |
| [`ChangeTilesUnder`](./Enums.md#enum-changetilesunder) | Enum | Applies or references the 'ChangeTilesUnder' effect/state. | 5 |
| [`Colorless`](./Arrays.md#array-colorless) | Object | Applies or references the 'Colorless' effect/state. | 5 |
| `DamageOrHealConditionally` | Number | Applies or references the 'DamageOrHealConditionally' effect/state. | 5 |
| [`DisableAbilitiesWithTag`](./Enums.md#enum-disableabilitieswithtag) | Enum | Examples: `musical, consumable` | 5 |
| [`ElementalManaCostReduction`](#elementalmanacostreduction) | Object | Applies the 'ElementalManaCostReduction' effect. | 5 |
| [`ExtraStatusWhenDealingDamage`](#extrastatuswhendealingdamage) | Object | Applies or references the 'ExtraStatusWhenDealingDamage' effect/state. | 5 |
| `Food` | Object | Applies or references the 'Food' effect/state. | 5 |
| `HeadArmorPassiveMultiplierBonus` | Integer | Applies or references the 'HeadArmorPassiveMultiplierBonus' effect/state. | 5 |
| `MakeSpellsRequireCharge` | Integer | Applies the 'MakeSpellsRequireCharge' effect. | 5 |
| [`MoveTowardsKillers`](./Enums.md#enum-movetowardskillers) | Enum | AI Movement: Seeks out entities that have recently killed an ally. | 5 |
| `NoHealthRegen` | Number | Applies or references the 'NoHealthRegen' effect/state. | 5 |
| [`PassiveWhenAtFullMana`](#passivewhenatfullmana) | Object | State Trigger: Grants nested passives when at full mana. | 5 |
| `RepairTrinket` | Number | Applies or references the 'RepairTrinket' effect/state. | 5 |
| `SharkySmellsBlood` | Integer | Applies or references the 'SharkySmellsBlood' effect/state. | 5 |
| [`SpawnCoinAnywhere`](./Arrays.md#array-spawncoinanywhere) | Array | Applies or references the 'SpawnCoinAnywhere' effect/state. | 5 |
| `StartOffMap` | Integer | Applies or references the 'StartOffMap' effect/state. | 5 |
| [`StatusGroup`](#statusgroup) | Object | Groups multiple status effects together for batch application. | 5 |
| [`StatusKilledCharacters`](#statuskilledcharacters) | Object | Event Trigger: Applies nested statuses to killed characters. | 5 |
| [`StatusOnEatFood`](#statusoneatfood) | Object | Event Trigger: Applies nested statuses when eat food. | 5 |
| [`StatusOnOverHealed`](#statusonoverhealed) | Object | Event Trigger: Applies nested statuses when over healed. | 5 |
| [`StatusOnPopCorpse`](#statusonpopcorpse) | Object | Event Trigger: Applies statuses when this action occurs. | 5 |
| [`StatusOnTurnEndIfCastNSpells`](#statusonturnendifcastnspells) | Object | Event Trigger: Applies nested statuses when turn end if cast n spells. | 5 |
| [`StatusOnTurnEndIfDidntCastAbilityTypes`](#statusonturnendifdidntcastabilitytypes) | Object | Event Trigger: Applies statuses when this action occurs. | 5 |
| [`Tangled`](./Arrays.md#array-tangled) | Object | Applies a tangled/ensnared status effect, often modifying visual sprites. | 5 |
| [`TransformItemOnElementInfluence`](#transformitemonelementinfluence) | Object | Applies or references the 'TransformItemOnElementInfluence' effect/state. | 5 |
| [`TransformOnDeathImmediately`](./Enums.md#enum-transformondeathimmediately) | Enum | Logic: Bypasses death sequence to instantly assume a new form. | 5 |
| [`XIsLivingAlliesWithTag`](./Enums.md#enum-xislivingallieswithtag) | Enum | Applies or references the 'XIsLivingAlliesWithTag' effect/state. | 5 |
| [`AbilityAfterEnemyCastSpell_Stackable`](./Enums.md#enum-abilityafterenemycastspell_stackable) | Enum | Applies or references the 'AbilityAfterEnemyCastSpell_Stackable' effect/state. | 4 |
| `AddDamageToBasicAttack` | Integer | Applies the 'AddDamageToBasicAttack' effect. | 4 |
| `AddMeleeKnockback` | Integer | Applies or references the 'AddMeleeKnockback' effect/state. | 4 |
| `AddSpeed` | Integer | Applies the 'AddSpeed' effect. | 4 |
| [`AddStatusToExplosions`](#addstatustoexplosions) | Object | Applies the 'AddStatusToExplosions' effect. | 4 |
| [`AddStatusToSpells`](#addstatustospells) | Object | Modifier: Injects a status effect into a specific action. | 4 |
| `AddUnfilledMaxHealth` | Integer | Applies the 'AddUnfilledMaxHealth' effect. | 4 |
| [`AllyBonusAbilityAura`](./Enums.md#enum-allybonusabilityaura) | Enum | Applies the 'AllyBonusAbilityAura' effect. | 4 |
| `AllyDamageReduction` | Integer | Applies the 'AllyDamageReduction' effect. | 4 |
| [`AllyManaRegenAura`](#allymanaregenaura) | Object | Applies the 'AllyManaRegenAura' effect. | 4 |
| [`ApplyStatusesToRandomEnemiesEachTurn`](#applystatusestorandomenemieseachturn) | Object | Applies or references the 'ApplyStatusesToRandomEnemiesEachTurn' effect/state. | 4 |
| `AutoEquipConsumables` | Integer | Applies or references the 'AutoEquipConsumables' effect/state. | 4 |
| `BackstabAllDirections` | Integer | Applies or references the 'BackstabAllDirections' effect/state. | 4 |
| [`BaitAura`](#baitaura) | Object | Passive: Projects an aura that attracts specific enemy types (e.g., flies/maggots). | 4 |
| `BeefyCharmedLeech` | Variable |  | 4 |
| [`Bird`](./Enums.md#enum-bird) | Enum | Applies or references the 'Bird' effect/state. | 4 |
| `BreakAtAux` | Integer | Applies or references the 'BreakAtAux' effect/state. | 4 |
| `BuffImmunity` | Integer | Applies or references the 'BuffImmunity' effect/state. | 4 |
| `bug` | Variable |  | 4 |
| `CatchBoomerang` | Integer | Applies or references the 'CatchBoomerang' effect/state. | 4 |
| `ChanceToBlockAndCounter` | Integer | Applies or references the 'ChanceToBlockAndCounter' effect/state. | 4 |
| [`ChangeTileOnPop`](./Enums.md#enum-changetileonpop) | Enum | Applies or references the 'ChangeTileOnPop' effect/state. | 4 |
| `Conditional_PartyMember` | Object | Conditional constraint. Nested properties only trigger if this is true. | 4 |
| `CopyBasicAttackEffects` | Integer | Applies or references the 'CopyBasicAttackEffects' effect/state. | 4 |
| `CountAsCorpse` | Integer | Applies or references the 'CountAsCorpse' effect/state. | 4 |
| `CreepTile` | Variable |  | 4 |
| [`DamageNeighborsAfterMove`](#damageneighborsaftermove) | Object | Examples: `{ ... }` | 4 |
| [`DisableAbilities`](./Enums.md#enum-disableabilities) | Enum | Applies or references the 'DisableAbilities' effect/state. | 4 |
| [`DisplayDangerAOE`](./Enums.md#enum-displaydangeraoe) | Enum | Applies or references the 'DisplayDangerAOE' effect/state. | 4 |
| [`DistanceBonusDamage`](#distancebonusdamage) | Object | Applies the 'DistanceBonusDamage' effect. | 4 |
| [`DownRankAIIfWeaponUsable`](./Enums.md#enum-downrankaiifweaponusable) | Float | Applies or references the 'DownRankAIIfWeaponUsable' effect/state. | 4 |
| [`EMP`](#emp) | Object | Applies the 'EMP' effect. | 4 |
| `equal` | Variable |  | 4 |
| [`extra_statuses`](#extra_statuses) | Object | Additional generic status applications. | 4 |
| `ExtraDispersedTurns` | Integer | Applies or references the 'ExtraDispersedTurns' effect/state. | 4 |
| `FaceArmorPassiveMultiplierBonus` | Integer | Applies or references the 'FaceArmorPassiveMultiplierBonus' effect/state. | 4 |
| `FlowersOnEndTurn` | Integer | Applies or references the 'FlowersOnEndTurn' effect/state. | 4 |
| [`FragileDuringElement`](./Enums.md#enum-fragileduringelement) | Enum | Applies or references the 'FragileDuringElement' effect/state. | 4 |
| [`GroundFlopper`](./Enums.md#enum-groundflopper) | Enum | Applies or references the 'GroundFlopper' effect/state. | 4 |
| `IncreaseSpellRange` | Integer | Applies or references the 'IncreaseSpellRange' effect/state. | 4 |
| [`KillsToMeat`](./Enums.md#enum-killstomeat) | Enum | Applies or references the 'KillsToMeat' effect/state. | 4 |
| [`LoopingSoundWhileAlive`](./Enums.md#enum-loopingsoundwhilealive) | Enum | Applies or references the 'LoopingSoundWhileAlive' effect/state. | 4 |
| `Maggot` | Variable |  | 4 |
| `MoveOne` | Variable |  | 4 |
| `PartialCleanse` | Number | Applies or references the 'PartialCleanse' effect/state. | 4 |
| [`PassiveAfterXKills`](#passiveafterxkills) | Object | Applies or references the 'PassiveAfterXKills' effect/state. | 4 |
| [`PassiveWhenDead`](#passivewhendead) | Object | State Trigger: Grants passives when this condition is met. | 4 |
| `PermanentIntelligence` | Number | Applies or references the 'PermanentIntelligence' effect/state. | 4 |
| [`PoopWhenHit`](./Enums.md#enum-poopwhenhit) | Enum | Examples: `Poop` | 4 |
| `PrioritizeFarAwayTargets` | Integer | Applies or references the 'PrioritizeFarAwayTargets' effect/state. | 4 |
| [`ProtectTargetedAllies`](./Enums.md#enum-protecttargetedallies) | Object | AI Logic: Navigates to intercept attacks directed at allies. | 4 |
| [`RandomPassivePool`](#randompassivepool) | Object | Logic: Grants a random passive from the specified pool upon spawning. | 4 |
| [`RandomSeededStatModifier`](./Arrays.md#array-randomseededstatmodifier) | Array | Applies or references the 'RandomSeededStatModifier' effect/state. | 4 |
| `RangedTrueShot` | Integer | Applies or references the 'RangedTrueShot' effect/state. | 4 |
| `Reflect` | Number | Applies or references the 'Reflect' effect/state. | 4 |
| [`RepairWeapon`](./Arrays.md#array-repairweapon) | Number | Applies or references the 'RepairWeapon' effect/state. | 4 |
| [`ReplaceSpell`](#replacespell) | Object | Replaces a spell in the character's hand/deck with a different one. | 4 |
| `ShowHiddenThings` | Integer | Examples: `1` | 4 |
| [`SpawnCatCopyOnBattleStart`](#spawncatcopyonbattlestart) | Object | Applies the 'SpawnCatCopyOnBattleStart' effect. | 4 |
| [`StatusAfterCastSpell`](#statusaftercastspell) | Object | Applies or references the 'StatusAfterCastSpell' effect/state. | 4 |
| [`StatusAlliesOnKill`](#statusalliesonkill) | Object | Event Trigger: Applies nested statuses to allies on kill. | 4 |
| [`StatusOnBreakItem`](#statusonbreakitem) | Object | Event Trigger: Applies statuses when this action occurs. | 4 |
| [`StatusOnHealed`](#statusonhealed) | Object | Event Trigger: Applies nested statuses when healed. | 4 |
| [`StatusOnTakeHealthOrShieldDamage`](#statusontakehealthorshielddamage) | Object | Event Trigger: Applies statuses when this action occurs. | 4 |
| [`StatusOnTurnEndIfManaExact`](#statusonturnendifmanaexact) | Object | Event Trigger: Applies nested statuses when turn end if mana exact. | 4 |
| [`StatusOnTurnEndIfManaOrHealthExact`](#statusonturnendifmanaorhealthexact) | Object | Event Trigger: Applies nested statuses when turn end if mana or health exact. | 4 |
| [`StatusRandomEnemiesOnBattleStart`](#statusrandomenemiesonbattlestart) | Object | Applies or references the 'StatusRandomEnemiesOnBattleStart' effect/state. | 4 |
| `TauntAlways` | Integer | Applies the 'TauntAlways' effect. | 4 |
| [`TempPassiveWhileHasStatus`](#temppassivewhilehasstatus) | Object | Grants nested passives only while the character possesses the specified status. | 4 |
| [`Trapper`](#trapper) | Object | Character Form: Behavior and stats for the 'Trapper' state. | 4 |
| `UncappedHP` | Integer | Applies the 'UncappedHP' effect. | 4 |
| `WeaponsDontLoseDurability` | Integer | Applies or references the 'WeaponsDontLoseDurability' effect/state. | 4 |
| [`WeremanTransformationReceiver`](./Enums.md#enum-weremantransformationreceiver) | Enum | Applies or references the 'WeremanTransformationReceiver' effect/state. | 4 |
| `AbilityEnabledOncePerRound` | Integer | Applies or references the 'AbilityEnabledOncePerRound' effect/state. | 3 |
| [`AbilityEnableIfConsumedCharacterHasTag`](./Enums.md#enum-abilityenableifconsumedcharacterhastag) | Enum | Applies or references the 'AbilityEnableIfConsumedCharacterHasTag' effect/state. | 3 |
| `AbilityInheritsWeaponEffects` | Integer | Applies or references the 'AbilityInheritsWeaponEffects' effect/state. | 3 |
| `AddEndOfCombatRegen` | Integer | Applies or references the 'AddEndOfCombatRegen' effect/state. | 3 |
| [`AddSelfStatusToWeapons`](#addselfstatustoweapons) | Object | Applies the 'AddSelfStatusToWeapons' effect. | 3 |
| [`AddStatusToKnockbackDamage`](#addstatustoknockbackdamage) | Object | Modifier: Injects a status effect into a specific action. | 3 |
| [`AddStatusToTrampleDamage`](#addstatustotrampledamage) | Object | Applies the 'AddStatusToTrampleDamage' effect. | 3 |
| `AggroTargetIsCurrentTurn` | Integer | Applies or references the 'AggroTargetIsCurrentTurn' effect/state. | 3 |
| `AllStatsUpPerDisorder` | Integer | Applies or references the 'AllStatsUpPerDisorder' effect/state. | 3 |
| `any` | Variable |  | 3 |
| [`AutocastEachTurnBegin`](./Enums.md#enum-autocasteachturnbegin) | Enum | Applies the 'AutocastEachTurnBegin' effect. | 3 |
| [`BaseStatMultiply`](./Enums.md#enum-basestatmultiply) | Float | Applies or references the 'BaseStatMultiply' effect/state. | 3 |
| [`BasicAttackCritChance`](./Enums.md#enum-basicattackcritchance) | Float | Applies the 'BasicAttackCritChance' effect. | 3 |
| `bishop_hat` | Variable |  | 3 |
| `BoneArmorPassive` | Integer | Applies or references the 'BoneArmorPassive' effect/state. | 3 |
| [`BonusTurnPattern`](./Arrays.md#array-bonusturnpattern) | Array | Applies or references the 'BonusTurnPattern' effect/state. | 3 |
| [`BouncyProjectiles`](#bouncyprojectiles) | Object | Applies the 'BouncyProjectiles' effect. | 3 |
| `Bounty` | Integer | Applies the 'Bounty' effect. | 3 |
| [`BreakOnElement`](./Enums.md#enum-breakonelement) | Enum | Applies or references the 'BreakOnElement' effect/state. | 3 |
| [`CanMutateTo`](./Enums.md#enum-canmutateto) | Enum | Applies or references the 'CanMutateTo' effect/state. | 3 |
| `CanRemoveCursedItems` | Integer | Examples: `1` | 3 |
| `CantCatchDiseases` | Integer | Applies or references the 'CantCatchDiseases' effect/state. | 3 |
| `CantSpreadDiseases` | Integer | Applies or references the 'CantSpreadDiseases' effect/state. | 3 |
| `CCImmunity` | Integer | Applies the 'CCImmunity' effect. | 3 |
| `ChanceToBlock` | Integer | Applies or references the 'ChanceToBlock' effect/state. | 3 |
| `CharmedFly` | Variable |  | 3 |
| `CharmedTinySpider` | Variable |  | 3 |
| `CharmedTinyTumor` | Variable |  | 3 |
| [`CobraReflex`](./Enums.md#enum-cobrareflex) | Enum | Applies the 'CobraReflex' effect. | 3 |
| `Coin` | Number | Applies or references the 'Coin' effect/state. | 3 |
| [`Conditional_Adjacent`](#conditional_adjacent) | Object | Conditional object: Executes nested logic only if the target is/has Adjacent. | 3 |
| `Conditional_RandomChance` | Object | Conditional trigger: Executes nested logic based on a flat percentage random roll. | 3 |
| `Conditional_Shielded` | Object | Conditional trigger: Executes nested logic if the target currently has a Shield status. | 3 |
| `ConsumableEffectsMultiplierBonus` | Integer | Applies the 'ConsumableEffectsMultiplierBonus' effect. | 3 |
| `ConsumablesInfiniteRange` | Integer | Applies the 'ConsumablesInfiniteRange' effect. | 3 |
| `CookedChickenLeg` | Variable |  | 3 |
| `CopyPassiveSlot` | Integer | Applies or references the 'CopyPassiveSlot' effect/state. | 3 |
| `CreateGlobalModifiers` | Object | Generates global map or encounter rules/modifiers. | 3 |
| `crow` | Variable |  | 3 |
| [`DigestDeadBodies`](./Enums.md#enum-digestdeadbodies) | Enum | Applies or references the 'DigestDeadBodies' effect/state. | 3 |
| `DoubleCastWeapons` | Integer | Applies the 'DoubleCastWeapons' effect. | 3 |
| [`DropAsFamiliarOnArmorBreak`](./Enums.md#enum-dropasfamiliaronarmorbreak) | Enum | Applies or references the 'DropAsFamiliarOnArmorBreak' effect/state. | 3 |
| [`EquipPermanentItem`](./Enums.md#enum-equippermanentitem) | Enum | Applies or references the 'EquipPermanentItem' effect/state. | 3 |
| [`Eternal`](#eternal) | Object | Applies the 'Eternal' effect. | 3 |
| `ExtraBasicMoves_Status` | Number | Applies or references the 'ExtraBasicMoves_Status' effect/state. | 3 |
| `Fights` | Number | Applies or references the 'Fights' effect/state. | 3 |
| `FlyDamageIncrease` | Integer | Applies the 'FlyDamageIncrease' effect. | 3 |
| [`FormChangeHealthThreshold`](#formchangehealththreshold) | Object | Logic: Changes form when health crosses a threshold. | 3 |
| `GainExtraShield` | Integer | Applies the 'GainExtraShield' effect. | 3 |
| `Grass` | Object | Examples: `{ ... }` | 3 |
| [`Holy`](./Enums.md#enum-holy) | Object | `MegaGuppy_TransformHoly` | 3 |
| `HouseFoodRequirementMultiplier` | Integer | Examples: `0` | 3 |
| `IllusionTint` | Integer | Applies or references the 'IllusionTint' effect/state. | 3 |
| [`IncAuxCounterClamped`](#incauxcounterclamped) | Object | Increments a generic auxiliary counter on the character, capped by a maximum value. | 3 |
| `include_spells` | Boolean | If true, allows the AI to cast spells during this bonus turn. | 3 |
| [`InfiniteRebirth`](#infiniterebirth) | Object | Applies the 'InfiniteRebirth' effect. | 3 |
| [`Jester`](./Arrays.md#array-jester) | Array | Examples: `[ CAT_VS_BOSS_QUOTES_JESTER_1 CAT_VS_BOSS_QUOTES_JESTER_2..., [ CAT_RETURN_EA...` | 3 |
| [`KnockOutCoin`](./Arrays.md#array-knockoutcoin) | Object | Forces the target to drop coins. | 3 |
| `Lava_Distortion` | Variable |  | 3 |
| `Lifesteal` | Number | Applies or references the 'Lifesteal' effect/state. | 3 |
| [`ManaPickup`](#manapickup) | Object | Pickup Logic: Defines what happens when a mana item is collected. | 3 |
| `MimicSpawnerAttacks` | Integer | Applies or references the 'MimicSpawnerAttacks' effect/state. | 3 |
| `MinimumKnockbackFromPhysicalAttacks` | Integer | Applies or references the 'MinimumKnockbackFromPhysicalAttacks' effect/state. | 3 |
| `MoonHeadFinisherEnabler` | Integer | Applies or references the 'MoonHeadFinisherEnabler' effect/state. | 3 |
| [`MoveAndUseAbilityEachTurnBeginIfPossible`](./Enums.md#enum-moveanduseabilityeachturnbeginifpossible) | Enum | Applies the 'MoveAndUseAbilityEachTurnBeginIfPossible' effect. | 3 |
| [`MoveAwayFromDamageSource`](./Enums.md#enum-moveawayfromdamagesource) | Enum | Examples: `BasicJump` | 3 |
| `must_do_damage` | Boolean | `true` | 3 |
| [`MutateViaAbility`](./Enums.md#enum-mutateviaability) | Enum | Applies or references the 'MutateViaAbility' effect/state. | 3 |
| `NeckArmorPassiveMultiplierBonus` | Integer | Applies or references the 'NeckArmorPassiveMultiplierBonus' effect/state. | 3 |
| [`PassiveWhileInMonkMeleeStance`](#passivewhileinmonkmeleestance) | Object | Applies the 'PassiveWhileInMonkMeleeStance' effect. | 3 |
| `PermanentDexterity` | Number | Applies or references the 'PermanentDexterity' effect/state. | 3 |
| `PermanentSpeed` | Number | Applies or references the 'PermanentSpeed' effect/state. | 3 |
| `Piercing` | Integer | Applies the 'Piercing' effect. | 3 |
| `PrioritizeHitDifferentTargets` | Integer | Applies or references the 'PrioritizeHitDifferentTargets' effect/state. | 3 |
| `RangeUp` | Number | Applies or references the 'RangeUp' effect/state. | 3 |
| `rat` | Variable |  | 3 |
| `RemoveLineOfSightRestrictions` | Integer | Applies the 'RemoveLineOfSightRestrictions' effect. | 3 |
| [`ReplaceBasicMove_Mutation`](./Enums.md#enum-replacebasicmove_mutation) | Enum | Examples: `BasicJump, BasicDig` | 3 |
| `robot` | Variable |  | 3 |
| `RockyArmorPassive` | Integer | Applies or references the 'RockyArmorPassive' effect/state. | 3 |
| `RunInXTurns` | Integer | Applies or references the 'RunInXTurns' effect/state. | 3 |
| [`ScaledStatusOnSpendMana`](#scaledstatusonspendmana) | Object | Applies the 'ScaledStatusOnSpendMana' effect. | 3 |
| [`SetDefaultFacePassive`](./Enums.md#enum-setdefaultfacepassive) | Enum | Applies or references the 'SetDefaultFacePassive' effect/state. | 3 |
| `SharePickups` | Integer | Applies the 'SharePickups' effect. | 3 |
| `SharePickupsWithSpawner` | Integer | Applies or references the 'SharePickupsWithSpawner' effect/state. | 3 |
| `SpawnCreepOnHit` | Integer | Applies or references the 'SpawnCreepOnHit' effect/state. | 3 |
| [`StackingFlowerTrail`](#stackingflowertrail) | Object | Applies or references the 'StackingFlowerTrail' effect/state. | 3 |
| [`StatusAllCharactersOnSpawn`](#statusallcharactersonspawn) | Object | Applies or references the 'StatusAllCharactersOnSpawn' effect/state. | 3 |
| `StatusCarefulness` | Integer | Applies or references the 'StatusCarefulness' effect/state. | 3 |
| [`StatusEachRoundEnd`](#statuseachroundend) | Object | Applies or references the 'StatusEachRoundEnd' effect/state. | 3 |
| [`StatusEachTurnEndForEachTurn`](#statuseachturnendforeachturn) | Object | Event Trigger: Applies nested statuses to each turn end for each turn. | 3 |
| [`StatusKillers`](#statuskillers) | Object | Instantly kills the target if they possess the specified status effects. | 3 |
| [`StatusOnCollectPickup`](#statusoncollectpickup) | Object | Event Trigger: Applies nested statuses when collect pickup. | 3 |
| [`StatusOnPickupCoins`](#statusonpickupcoins) | Object | Event Trigger: Applies nested statuses when pickup coins. | 3 |
| [`StatusOnUseBasicAttack`](#statusonusebasicattack) | Object | Event Trigger: Applies nested statuses when use basic attack. | 3 |
| [`StatusWhenAllySpendsMana`](#statuswhenallyspendsmana) | Object | Event Trigger: Applies nested statuses to when ally spends mana. | 3 |
| [`SupportFormChangeInsteadOfRun`](./Enums.md#enum-supportformchangeinsteadofrun) | Enum | AI Logic: Forces a support unit to transform rather than flee. | 3 |
| [`tag_filter`](./Enums.md#enum-tag_filter) | Enum | Examples: `crow, grub_familiar` | 3 |
| [`TakeBonusTurnWithAIControl`](#takebonusturnwithaicontrol) | Object | Grants the character an immediate extra turn, but forces the AI to control them during it. | 3 |
| `ThornUpX` | Variable |  | 3 |
| [`TileTrail_Ahead`](./Enums.md#enum-tiletrail_ahead) | Enum | Applies or references the 'TileTrail_Ahead' effect/state. | 3 |
| [`TowerDefenseReflex`](./Enums.md#enum-towerdefensereflex) | Enum | Applies the 'TowerDefenseReflex' effect. | 3 |
| `TrueShot` | Integer | Applies or references the 'TrueShot' effect/state. | 3 |
| `TVOff` | Variable |  | 3 |
| `UncappedMana` | Integer | Applies the 'UncappedMana' effect. | 3 |
| `UpgradeSpawnedPickups` | Integer | Applies the 'UpgradeSpawnedPickups' effect. | 3 |
| [`UseAbility_NonStack`](./Enums.md#enum-useability_nonstack) | Enum | Applies or references the 'UseAbility_NonStack' effect/state. | 3 |
| `Vegan` | Integer | Examples: `1` | 3 |
| `Water` | Object | Character Form: Behavior and stats for the \'Water\' state. | 3 |
| `WeaponDamageMultiplierBonus` | Integer | Applies the 'WeaponDamageMultiplierBonus' effect. | 3 |
| [`XIsMultipliedPercentHealth`](./Arrays.md#array-xismultipliedpercenthealth) | Array | Applies or references the 'XIsMultipliedPercentHealth' effect/state. | 3 |
| [`AbilityEnabledIfHasStatus`](./Enums.md#enum-abilityenabledifhasstatus) | Enum | Applies or references the 'AbilityEnabledIfHasStatus' effect/state. | 2 |
| [`AbilityOnRoundEnd`](#abilityonroundend) | Object | AI Trigger: Executes an ability at the end of the combat round. | 2 |
| `AbsorbBuff` | Variable |  | 2 |
| `AbsorbManaAura` | Integer | Applies the 'AbsorbManaAura' effect. | 2 |
| [`AddPassivesToSummonAbilityMinions`](#addpassivestosummonabilityminions) | Object | Applies the 'AddPassivesToSummonAbilityMinions' effect. | 2 |
| [`AddPassiveToSpawnedRocks`](#addpassivetospawnedrocks) | Object | Applies the 'AddPassiveToSpawnedRocks' effect. | 2 |
| `AddSpellDamage` | Integer | Applies the 'AddSpellDamage' effect. | 2 |
| [`AddStatusToAllDamageAbilities`](#addstatustoalldamageabilities) | Object | Applies the 'AddStatusToAllDamageAbilities' effect. | 2 |
| [`AddStatusToBasicAttackWithCooldown`](#addstatustobasicattackwithcooldown) | Object | Applies the 'AddStatusToBasicAttackWithCooldown' effect. | 2 |
| [`AddStatusToFirstBasicAttack`](#addstatustofirstbasicattack) | Object | Applies the 'AddStatusToFirstBasicAttack' effect. | 2 |
| [`AddStatusToMeleeDamage`](#addstatustomeleedamage) | Object | Applies the 'AddStatusToMeleeDamage' effect. | 2 |
| `AddWeaponScaling` | Integer | Applies the 'AddWeaponScaling' effect. | 2 |
| [`AfterImage`](./Enums.md#enum-afterimage) | Enum | Spawns a visual decoy or shade at the caster's previous location. | 2 |
| `AggroTargetIsBuddy` | Integer | Applies or references the 'AggroTargetIsBuddy' effect/state. | 2 |
| `ai` | Object | Core block defining the AI behavior logic and weights. | 2 |
| `all_items` | Variable |  | 2 |
| `AllDamageImmune_IncludingSpeculative` | Integer | Applies or references the 'AllDamageImmune_IncludingSpeculative' effect/state. | 2 |
| `AllowPassTurn` | Integer | Applies the 'AllowPassTurn' effect. | 2 |
| [`AllyDamageReaction`](./Enums.md#enum-allydamagereaction) | Enum | Applies the 'AllyDamageReaction' effect. | 2 |
| [`AllyHealthRegenAura`](#allyhealthregenaura) | Object | Applies the 'AllyHealthRegenAura' effect. | 2 |
| [`AllyMoveAbilityAura`](./Enums.md#enum-allymoveabilityaura) | Enum | Applies the 'AllyMoveAbilityAura' effect. | 2 |
| `AllyMultiplyKnockbackDamage` | Integer | Applies the 'AllyMultiplyKnockbackDamage' effect. | 2 |
| [`AlternateCraftingPools`](#alternatecraftingpools) | Object | Applies the 'AlternateCraftingPools' effect. | 2 |
| `AlwaysHitDifferentTargets` | Integer | Applies or references the 'AlwaysHitDifferentTargets' effect/state. | 2 |
| `AmplifyPositiveStatus` | Integer | Applies the 'AmplifyPositiveStatus' effect. | 2 |
| [`ApplyStatusIfCrit`](#applystatusifcrit) | Object | Conditional trigger: Executes the nested logic only if the triggering action was a critical hit. | 2 |
| [`ArmorBreakOnHit`](#armorbreakonhit) | Object | Applies or references the 'ArmorBreakOnHit' effect/state. | 2 |
| [`AutocastEachTurn`](./Enums.md#enum-autocasteachturn) | Enum | Applies the 'AutocastEachTurn' effect. | 2 |
| `AutoCritLowDamage` | Integer | Applies the 'AutoCritLowDamage' effect. | 2 |
| `BasicAttackCantMiss` | Integer | Examples: `1` | 2 |
| `BasicAttackStatusCarefulness` | Integer | Applies the 'BasicAttackStatusCarefulness' effect. | 2 |
| `BasicMonkMelee` | Variable |  | 2 |
| `BonusFoodEachBattle` | Integer | Applies the 'BonusFoodEachBattle' effect. | 2 |
| [`BoobyTrapItems`](#boobytrapitems) | Object | Applies the 'BoobyTrapItems' effect. | 2 |
| `BoomerCatExplode` | Variable |  | 2 |
| `BoostAllyStatsOnDeath` | Integer | Applies the 'BoostAllyStatsOnDeath' effect. | 2 |
| `BraceForEachNeighboringEnemy` | Integer | Applies the 'BraceForEachNeighboringEnemy' effect. | 2 |
| `BreakWhenNoShield` | Integer | Applies or references the 'BreakWhenNoShield' effect/state. | 2 |
| [`BungaEntrance`](#bungaentrance) | Object | Animation/AI State: Bunga entering the arena. | 2 |
| `BungaSwipe` | Variable |  | 2 |
| `CanLevelUpWhenDead` | Integer | Applies or references the 'CanLevelUpWhenDead' effect/state. | 2 |
| `CanShield` | Integer | Applies or references the 'CanShield' effect/state. | 2 |
| `CapDamageFromAllies` | Integer | Applies the 'CapDamageFromAllies' effect. | 2 |
| `CapMovementAbilityRange` | Integer | Applies or references the 'CapMovementAbilityRange' effect/state. | 2 |
| `CapTechSpent` | Integer | Applies the 'CapTechSpent' effect. | 2 |
| [`CatAPultAnimation`](#catapultanimation) | Object | Applies the 'CatAPultAnimation' effect. | 2 |
| `ChainKnockback` | Integer | Applies the 'ChainKnockback' effect. | 2 |
| `ChanceToDisableActionsIfNotCharmed` | Integer | Applies or references the 'ChanceToDisableActionsIfNotCharmed' effect/state. | 2 |
| `ChangeTauntPriority` | Integer | Applies the 'ChangeTauntPriority' effect. | 2 |
| [`ChangeTileOnDeath`](./Enums.md#enum-changetileondeath) | Enum | Applies or references the 'ChangeTileOnDeath' effect/state. | 2 |
| [`ChargeSpiritBombAura`](./Enums.md#enum-chargespiritbombaura) | Enum | Applies or references the 'ChargeSpiritBombAura' effect/state. | 2 |
| `CharmAllFlies` | Integer | Applies the 'CharmAllFlies' effect. | 2 |
| `CharmedFlySwarm` | Variable |  | 2 |
| [`CherubimReaction`](#cherubimreaction) | Object | Reaction: Custom reaction triggers for Cherubim enemies. | 2 |
| `CoinsAddDamage` | Integer | Applies the 'CoinsAddDamage' effect. | 2 |
| `CollectPickupsOnBattleEnd` | Integer | Applies the 'CollectPickupsOnBattleEnd' effect. | 2 |
| `Conductor` | Integer | Applies the 'Conductor' effect. | 2 |
| `ConjureCastSpellsForAllies` | Integer | Applies the 'ConjureCastSpellsForAllies' effect. | 2 |
| `consumable` | Number | `true` | 2 |
| `CopyCatPassive_Initializer` | Integer | Applies or references the 'CopyCatPassive_Initializer' effect/state. | 2 |
| `DamageEnemiesOnHeal` | Integer | Combat Trigger: Deals damage to enemies on heal. | 2 |
| `DamageEnemiesOnKill` | Integer | Combat Trigger: Deals damage to enemies on kill. | 2 |
| [`DamageNeighborTilesWhenCastSpell`](#damageneighbortileswhencastspell) | Object | Combat Trigger: Deals damage to neighbor tiles when cast spell. | 2 |
| [`DamageReductionAura`](#damagereductionaura) | Object | Combat Trigger: Deals damage to reduction aura. | 2 |
| `DeathChill` | Integer | Applies the 'DeathChill' effect. | 2 |
| `DejaVu` | Integer | Applies the 'DejaVu' effect. | 2 |
| `DemonicGlyph_Bite` | Number | Applies or references the 'DemonicGlyph_Bite' effect/state. | 2 |
| `DemonicGlyph_Summon` | Number | Applies or references the 'DemonicGlyph_Summon' effect/state. | 2 |
| `DemonicGlyphFrames` | Integer | Applies or references the 'DemonicGlyphFrames' effect/state. | 2 |
| [`DiesToElement`](./Enums.md#enum-diestoelement) | Enum | Vulnerability: Character dies instantly if hit by this element. | 2 |
| `DirtyClaws` | Integer | Applies the 'DirtyClaws' effect. | 2 |
| `DisablePassiveSlot` | Integer | Applies or references the 'DisablePassiveSlot' effect/state. | 2 |
| `DissuadeInstakills` | Integer | Applies or references the 'DissuadeInstakills' effect/state. | 2 |
| `DrinkWater` | Number | Applies or references the 'DrinkWater' effect/state. | 2 |
| `DukeOfFlies` | Integer | Applies the 'DukeOfFlies' effect. | 2 |
| [`Dyslexia`](./Arrays.md#array-dyslexia) | Array | Examples: `[ 6 9 ], [ 3 5 ]` | 2 |
| `Earth` | Object | Examples: `{ ... }` | 2 |
| [`ElementalAttunement`](#elementalattunement) | Object | Applies the 'ElementalAttunement' effect. | 2 |
| `Empath` | Integer | Applies the 'Empath' effect. | 2 |
| `EmptyMana` | Integer | Applies the 'EmptyMana' effect. | 2 |
| `EnemiesGetPickupsKnockedOut` | Integer | Applies the 'EnemiesGetPickupsKnockedOut' effect. | 2 |
| `EnergyStorm` | Integer | Applies the 'EnergyStorm' effect. | 2 |
| `EquipmentPassiveMultiplierBonus` | Integer | Applies the 'EquipmentPassiveMultiplierBonus' effect. | 2 |
| `EquipmentSetBonusBonus` | Integer | Applies the 'EquipmentSetBonusBonus' effect. | 2 |
| [`EquipRandomTemporaryItemFromPool`](./Enums.md#enum-equiprandomtemporaryitemfrompool) | Enum | Examples: `pills` | 2 |
| [`EscapeSequence`](#escapesequence) | Object | Applies the 'EscapeSequence' effect. | 2 |
| `euphoric` | Object | Examples: `{ ... }` | 2 |
| `ExpireOnSpawnerTurnEnd` | Integer | Applies or references the 'ExpireOnSpawnerTurnEnd' effect/state. | 2 |
| `ExplodeOverkilledEnemies` | Integer | Applies the 'ExplodeOverkilledEnemies' effect. | 2 |
| `ExplosionImmunity` | Integer | Applies or references the 'ExplosionImmunity' effect/state. | 2 |
| `ExtraTrinketUses` | Integer | Applies or references the 'ExtraTrinketUses' effect/state. | 2 |
| `FaceLastDamage` | Integer | Reaction: Forces the character to face towards the last damage source. | 2 |
| [`FamiliarBonusAbility`](./Enums.md#enum-familiarbonusability) | Enum | Applies the 'FamiliarBonusAbility' effect. | 2 |
| `FamiliarSecondaryDamageImmunity` | Integer | Applies the 'FamiliarSecondaryDamageImmunity' effect. | 2 |
| [`FinalBossShield`](./Enums.md#enum-finalbossshield) | Enum | Applies or references the 'FinalBossShield' effect/state. | 2 |
| [`FindExtraItemFromPoolOnBattleEnd`](./Enums.md#enum-findextraitemfrompoolonbattleend) | Enum | Applies or references the 'FindExtraItemFromPoolOnBattleEnd' effect/state. | 2 |
| [`FindItem`](./Enums.md#enum-finditem) | Enum | Applies or references the 'FindItem' effect/state. | 2 |
| `FlippedFacingForceAttack` | Integer | Applies the 'FlippedFacingForceAttack' effect. | 2 |
| `FlowerPowerAuraBrace` | Integer | Applies the 'FlowerPowerAuraBrace' effect. | 2 |
| `FlowerPowerAuraStrength` | Integer | Applies the 'FlowerPowerAuraStrength' effect. | 2 |
| [`FollowUp`](./Enums.md#enum-followup) | Enum | Applies the 'FollowUp' effect. | 2 |
| [`FormChangeDuringWeatherElement`](#formchangeduringweatherelement) | Object | Logic: Changes form automatically during specific weather conditions. | 2 |
| `FullHealthCritChance` | Integer | Applies the 'FullHealthCritChance' effect. | 2 |
| `FullPower` | Integer | Applies the 'FullPower' effect. | 2 |
| `GlobalManaBurnAura` | Integer | Examples: `-1` | 2 |
| `GoopWalk` | Integer | Applies or references the 'GoopWalk' effect/state. | 2 |
| `GrassTile` | Number | Examples: `80, 15` | 2 |
| `GrassTileHealing` | Integer | Applies the 'GrassTileHealing' effect. | 2 |
| [`GravityWell`](#gravitywell) | Object | Applies the 'GravityWell' effect. | 2 |
| `greater` | Variable |  | 2 |
| `GrenadeExplode` | Variable |  | 2 |
| `Haunt` | Variable |  | 2 |
| `HealAndOverhealToShield` | Integer | Applies the 'HealAndOverhealToShield' effect. | 2 |
| `HealDamagesEnemies` | Integer | Applies the 'HealDamagesEnemies' effect. | 2 |
| `HealsAlsoRegenMana` | Integer | Applies the 'HealsAlsoRegenMana' effect. | 2 |
| `HealsCanRevive` | Integer | Applies the 'HealsCanRevive' effect. | 2 |
| `HolyShieldTransferToSpawner` | Integer | Applies the 'HolyShieldTransferToSpawner' effect. | 2 |
| [`HolyShieldTransferToTaggedMinions`](./Enums.md#enum-holyshieldtransfertotaggedminions) | Enum | Applies the 'HolyShieldTransferToTaggedMinions' effect. | 2 |
| `HPGainBlock` | Integer | Applies or references the 'HPGainBlock' effect/state. | 2 |
| `ImmobilePassive` | Integer | Applies or references the 'ImmobilePassive' effect/state. | 2 |
| `ImmortalLeeches` | Integer | Applies the 'ImmortalLeeches' effect. | 2 |
| `IncreaseHealingSpellRange` | Integer | Applies the 'IncreaseHealingSpellRange' effect. | 2 |
| `int` | Number | `aux` | 2 |
| [`KaijuWinCon`](./Enums.md#enum-kaijuwincon) | Enum | Applies or references the 'KaijuWinCon' effect/state. | 2 |
| `KillsHeal` | Integer | Applies the 'KillsHeal' effect. | 2 |
| [`LateBloomer`](#latebloomer) | Object | Applies the 'LateBloomer' effect. | 2 |
| `lck` | Number | `aux` | 2 |
| [`LeaveBehindOnceEachMove`](./Enums.md#enum-leavebehindonceeachmove) | Enum | Applies or references the 'LeaveBehindOnceEachMove' effect/state. | 2 |
| `LeechPercent` | Integer | Applies the 'LeechPercent' effect. | 2 |
| `LightningAspectCharge` | Integer | Applies the 'LightningAspectCharge' effect. | 2 |
| [`LightningRod`](#lightningrod) | Object | Applies the 'LightningRod' effect. | 2 |
| [`LineOfSightTrueSightAura`](./Enums.md#enum-lineofsighttruesightaura) | Float | Applies the 'LineOfSightTrueSightAura' effect. | 2 |
| `LobbedHook` | Integer | Applies the 'LobbedHook' effect. | 2 |
| [`LowHealthAllyDodgeChanceAura`](#lowhealthallydodgechanceaura) | Object | Applies the 'LowHealthAllyDodgeChanceAura' effect. | 2 |
| `MagicDamageImmune` | Integer | Applies or references the 'MagicDamageImmune' effect/state. | 2 |
| `MakeBasicAttackPassThroughThings` | Integer | Applies the 'MakeBasicAttackPassThroughThings' effect. | 2 |
| `MakeBasicAttackPull` | Integer | Examples: `1` | 2 |
| `MamaCatAnimations` | Integer | Applies or references the 'MamaCatAnimations' effect/state. | 2 |
| `ManaRegenMultiplierIfManaEmpty` | Integer | Applies the 'ManaRegenMultiplierIfManaEmpty' effect. | 2 |
| `MegaMinions` | Integer | Applies the 'MegaMinions' effect. | 2 |
| `MetalDetector` | Integer | Applies the 'MetalDetector' effect. | 2 |
| `MinimumTech` | Integer | Applies the 'MinimumTech' effect. | 2 |
| [`MiniVolcanoReaction`](./Enums.md#enum-minivolcanoreaction) | Enum | Applies or references the 'MiniVolcanoReaction' effect/state. | 2 |
| [`ModifyAbility`](#modifyability) | Object | Applies or references the 'ModifyAbility' effect/state. | 2 |
| [`MotherTumorSpawnInCapture`](#mothertumorspawnincapture) | Object | Boss Logic: Logic for capturing entities inside the Mother's tumors upon spawning. | 2 |
| [`MoveSpeedMultiplier`](./Enums.md#enum-movespeedmultiplier) | Float | Applies or references the 'MoveSpeedMultiplier' effect/state. | 2 |
| `musical` | Variable |  | 2 |
| [`NextBattleStatus`](#nextbattlestatus) | Object | Applies the 'NextBattleStatus' effect. | 2 |
| `NoManaRegen` | Integer | Applies the 'NoManaRegen' effect. | 2 |
| `NoReflection` | Integer | Applies the 'NoReflection' effect. | 2 |
| `NubbyToss` | Variable |  | 2 |
| `NubbyTossPriority` | Integer | Applies the 'NubbyTossPriority' effect. | 2 |
| [`NukeQuestFinalBossModifications`](#nukequestfinalbossmodifications) | Object | Special encounter trigger for the Nuke Quest ending. | 2 |
| `NumbingLeeches` | Integer | Applies the 'NumbingLeeches' effect. | 2 |
| `OneUseSpellDamageUp` | Integer | Applies the 'OneUseSpellDamageUp' effect. | 2 |
| `OverhealGainsBothShield` | Integer | Applies the 'OverhealGainsBothShield' effect. | 2 |
| `ParasitesArentCursed` | Integer | Applies the 'ParasitesArentCursed' effect. | 2 |
| [`partial_animation_suffix`](./Enums.md#enum-partial_animation_suffix) | String | ``, `Alert`, `Angry`, `Belly`, `Button` | 2 |
| [`passive0`](./Enums.md#enum-passive0) | Enum | `HotBlooded`, `SelfAssured` | 2 |
| [`PassiveAtFullHealth`](#passiveatfullhealth) | Object | Applies the 'PassiveAtFullHealth' effect. | 2 |
| [`PassiveAtInjuryThreshold`](#passiveatinjurythreshold) | Object | Applies the 'PassiveAtInjuryThreshold' effect. | 2 |
| `PassiveEnergized` | Variable |  | 2 |
| [`PassiveIfWeaponIsUsable`](#passiveifweaponisusable) | Object | Applies or references the 'PassiveIfWeaponIsUsable' effect/state. | 2 |
| `PassiveTar` | Variable |  | 2 |
| [`PassiveUntilCastSpell`](#passiveuntilcastspell) | Object | Applies the 'PassiveUntilCastSpell' effect. | 2 |
| [`PassiveUntilGetKill`](#passiveuntilgetkill) | Object | Applies the 'PassiveUntilGetKill' effect. | 2 |
| [`PassiveWhenTheAlpha`](#passivewhenthealpha) | Object | State Trigger: Grants nested passives when the alpha. | 2 |
| [`PassiveWhileInMonkRangedStance`](#passivewhileinmonkrangedstance) | Object | Applies the 'PassiveWhileInMonkRangedStance' effect. | 2 |
| [`PassiveWhileNotHasStatus`](#passivewhilenothasstatus) | Object | Passive: Activates only while the character does NOT have the specified status. | 2 |
| [`PassiveWhilePreviewingMonkRangedStance`](#passivewhilepreviewingmonkrangedstance) | Object | Applies the 'PassiveWhilePreviewingMonkRangedStance' effect. | 2 |
| [`PassiveWhileWearingMetal`](#passivewhilewearingmetal) | Object | Applies the 'PassiveWhileWearingMetal' effect. | 2 |
| `PermanentItems` | Integer | Applies the 'PermanentItems' effect. | 2 |
| `Phasing` | Integer | Applies or references the 'Phasing' effect/state. | 2 |
| `PrioritizeAggroTarget` | Integer | Applies or references the 'PrioritizeAggroTarget' effect/state. | 2 |
| `PrioritizePlayerCats` | Integer | Applies or references the 'PrioritizePlayerCats' effect/state. | 2 |
| `PrioritizeWeakestEnemy` | Integer | Applies or references the 'PrioritizeWeakestEnemy' effect/state. | 2 |
| `Quiver` | Integer | Applies the 'Quiver' effect. | 2 |
| [`RandomTaggedMutation`](./Enums.md#enum-randomtaggedmutation) | Enum | Applies or references the 'RandomTaggedMutation' effect/state. | 2 |
| `ReaperRevenge` | Variable |  | 2 |
| `red` | Object | Event Object: Story branch or dialog option representing the \'Red\' action. | 2 |
| [`RefreshEquipmentAbilityOnElement`](#refreshequipmentabilityonelement) | Object | Applies or references the 'RefreshEquipmentAbilityOnElement' effect/state. | 2 |
| `ReloadOnKill` | Integer | Applies or references the 'ReloadOnKill' effect/state. | 2 |
| `ReloadOnKillEnemy` | Integer | Applies or references the 'ReloadOnKillEnemy' effect/state. | 2 |
| `ReloadOnTotalDamageReceived` | Integer | Applies or references the 'ReloadOnTotalDamageReceived' effect/state. | 2 |
| `RemoteLeech` | Integer | Applies or references the 'RemoteLeech' effect/state. | 2 |
| `RemoveOncePerFightRestriction` | Integer | Applies the 'RemoveOncePerFightRestriction' effect. | 2 |
| [`ReplaceBasicAttackWhenDead`](./Enums.md#enum-replacebasicattackwhendead) | Enum | Applies the 'ReplaceBasicAttackWhenDead' effect. | 2 |
| `ReturnBoundItemOnBattleEnd` | Integer | Applies or references the 'ReturnBoundItemOnBattleEnd' effect/state. | 2 |
| `ReviveOnWin` | Integer | Applies the 'ReviveOnWin' effect. | 2 |
| `RobotsInheritArmor` | Integer | Applies the 'RobotsInheritArmor' effect. | 2 |
| `RockDetector` | Integer | Applies the 'RockDetector' effect. | 2 |
| `SafeExplosions` | Integer | Applies the 'SafeExplosions' effect. | 2 |
| [`ScaledStatusOnOverMana`](#scaledstatusonovermana) | Object | Applies the 'ScaledStatusOnOverMana' effect. | 2 |
| `SelfStatusCarefulness` | Integer | Applies or references the 'SelfStatusCarefulness' effect/state. | 2 |
| [`SetDefaultFace`](./Enums.md#enum-setdefaultface) | Enum | Applies or references the 'SetDefaultFace' effect/state. | 2 |
| `SetItemAux` | Object | Applies or references the 'SetItemAux' effect/state. | 2 |
| `ShareHealthRegen` | Integer | Applies the 'ShareHealthRegen' effect. | 2 |
| `ShoulderCheck` | Integer | Applies the 'ShoulderCheck' effect. | 2 |
| [`ShovingMatch`](./Enums.md#enum-shovingmatch) | Enum | Applies the 'ShovingMatch' effect. | 2 |
| [`SlotMachineRollPool`](#slotmachinerollpool) | Object | Logic: Defines the possible outcomes for slot machine enemies. | 2 |
| `SmallEnemiesIgnoreYou` | Integer | Applies the 'SmallEnemiesIgnoreYou' effect. | 2 |
| [`SmiteEnemiesWhoKill`](#smiteenemieswhokill) | Object | Applies the 'SmiteEnemiesWhoKill' effect. | 2 |
| `SparkleBuff` | Variable |  | 2 |
| `SpawnBearTrapOnMiss` | Integer | Applies the 'SpawnBearTrapOnMiss' effect. | 2 |
| [`SpawnCatCopyWhenDowned`](#spawncatcopywhendowned) | Object | Examples: `{ ... }` | 2 |
| [`SpawnItemLinkedFamiliar`](#spawnitemlinkedfamiliar) | Object | Applies or references the 'SpawnItemLinkedFamiliar' effect/state. | 2 |
| `SpawnNearEnemies` | Integer | Applies or references the 'SpawnNearEnemies' effect/state. | 2 |
| [`SpecialFriends`](#specialfriends) | Object | Applies the 'SpecialFriends' effect. | 2 |
| `SpikeBuff` | Variable |  | 2 |
| `SplittableMove` | Integer | Applies the 'SplittableMove' effect. | 2 |
| `SpreadExtraDebuffs` | Integer | Applies the 'SpreadExtraDebuffs' effect. | 2 |
| `SpreadPainBonus` | Integer | Applies the 'SpreadPainBonus' effect. | 2 |
| `StatMinimum` | Integer | Applies the 'StatMinimum' effect. | 2 |
| [`StatsAtLowHealth`](#statsatlowhealth) | Object | Applies the 'StatsAtLowHealth' effect. | 2 |
| [`StatusAfterXTurns`](#statusafterxturns) | Object | Event Trigger: Applies a status effect after X turns have passed. | 2 |
| [`StatusAlliesOnGainCoins`](#statusalliesongaincoins) | Object | Event Trigger: Applies nested statuses to allies on gain coins. | 2 |
| [`StatusAllyWhenAllySpendsMana`](#statusallywhenallyspendsmana) | Object | Event Trigger: Applies nested statuses to ally when ally spends mana. | 2 |
| [`StatusAnyCatAllyWhoKills`](#statusanycatallywhokills) | Object | Event Trigger: Applies nested statuses to any cat ally who kills. | 2 |
| [`StatusDamagers`](#statusdamagers) | Object | Event Trigger: Applies nested statuses to damagers. | 2 |
| [`StatusEachTurnEndPerEnemyKill`](#statuseachturnendperenemykill) | Object | Event Trigger: Applies nested statuses to each turn end per enemy kill. | 2 |
| [`StatusEnemiesOnDeath`](#statusenemiesondeath) | Object | Event Trigger: Applies nested statuses to enemies on death. | 2 |
| [`StatusEveryXTurnBegins`](#statuseveryxturnbegins) | Object | Event Trigger: Applies nested statuses to every x turn begins. | 2 |
| [`StatusIfUnusedActPoints`](#statusifunusedactpoints) | Object | Applies or references the 'StatusIfUnusedActPoints' effect/state. | 2 |
| [`StatusOnAnyDeath`](#statusonanydeath) | Object | Event Trigger: Applies nested statuses when any death. | 2 |
| [`StatusOnBackstab`](#statusonbackstab) | Object | Event Trigger: Applies statuses when this action occurs. | 2 |
| [`StatusOnBattleEndIfKillThresholdMet`](#statusonbattleendifkillthresholdmet) | Object | Event Trigger: Applies nested statuses when battle end if kill threshold met. | 2 |
| [`StatusOnDealtDamage`](#statusondealtdamage) | Object | Event Trigger: Applies nested statuses when dealt damage. | 2 |
| [`StatusOnDealtDamageThreshold`](#statusondealtdamagethreshold) | Object | Event Trigger: Applies nested statuses when dealt damage threshold. | 2 |
| [`StatusOnEatPill`](#statusoneatpill) | Object | Examples: `{ ... }` | 2 |
| [`StatusOnGainShield`](#statusongainshield) | Object | Event Trigger: Applies nested statuses when gain shield. | 2 |
| [`StatusOnHeal`](#statusonheal) | Object | Event Trigger: Applies nested statuses when heal. | 2 |
| [`StatusOnOverMana`](#statusonovermana) | Object | Event Trigger: Applies nested statuses when over mana. | 2 |
| [`StatusOnSetPieceBreak`](#statusonsetpiecebreak) | Object | Examples: `{ ... }` | 2 |
| [`StatusOnSpawnIn`](#statusonspawnin) | Object | Event Trigger: Applies statuses immediately when spawned. | 2 |
| [`StatusOnTookDamageFromEnemyAbility`](#statusontookdamagefromenemyability) | Object | Event Trigger: Applies nested statuses when took damage from enemy ability. | 2 |
| [`StatusOnTriggerTrap`](#statusontriggertrap) | Object | Event Trigger: Applies nested statuses when trigger trap. | 2 |
| [`StatusOnUseElementAbility`](#statusonuseelementability) | Object | Event Trigger: Applies nested statuses when use element ability. | 2 |
| [`StatusPerInjury`](#statusperinjury) | Object | Event Trigger: Applies nested statuses to per injury. | 2 |
| [`StatusReplacement`](./Arrays.md#array-statusreplacement) | Array | Examples: `[ Petrify PetrifyCharmed ]` | 2 |
| [`StatusThingsKnockedBack`](#statusthingsknockedback) | Object | Event Trigger: Applies nested statuses to things knocked back. | 2 |
| `StrengthForEachNeighboringEnemy` | Integer | Applies the 'StrengthForEachNeighboringEnemy' effect. | 2 |
| `StrengthInNumbersAura` | Integer | Applies the 'StrengthInNumbersAura' effect. | 2 |
| `Study` | Integer | Applies the 'Study' effect. | 2 |
| `SurviveAt1HP` | Integer | Applies or references the 'SurviveAt1HP' effect/state. | 2 |
| [`TaggedPickupEffectReplacement`](#taggedpickupeffectreplacement) | Object | Applies the 'TaggedPickupEffectReplacement' effect. | 2 |
| `TempCounterAttack` | Number | Applies or references the 'TempCounterAttack' effect/state. | 2 |
| `TempNoManaRegen` | Integer | Applies or references the 'TempNoManaRegen' effect/state. | 2 |
| `TileDamageMultiplier` | Integer | Applies the 'TileDamageMultiplier' effect. | 2 |
| [`TinkererBasicAttackSwitching`](#tinkererbasicattackswitching) | Object | Logic: Allows Tinkerer to swap basic attacks. | 2 |
| `ToadJump_BasicMove` | Variable |  | 2 |
| [`TowerDefense`](#towerdefense) | Object | Applies the 'TowerDefense' effect. | 2 |
| [`TransformOnElementInfluencex`](#transformonelementinfluencex) | Object | Logic: Variant element influence transformation. | 2 |
| [`TransformWhenBuddyDies`](./Enums.md#enum-transformwhenbuddydies) | Enum | Applies or references the 'TransformWhenBuddyDies' effect/state. | 2 |
| `TrapEffectsMultiplier` | Integer | Applies the 'TrapEffectsMultiplier' effect. | 2 |
| `triggers_limit` | Integer | Examples: `1` | 2 |
| `Uncontrollable` | Integer | Applies or references the 'Uncontrollable' effect/state. | 2 |
| `UnlockOrientation` | Integer | Applies or references the 'UnlockOrientation' effect/state. | 2 |
| [`UpgradeLevelUpClassActives`](./Enums.md#enum-upgradelevelupclassactives) | Enum | Applies the 'UpgradeLevelUpClassActives' effect. | 2 |
| [`UpgradeLevelUpClassPassives`](./Enums.md#enum-upgradelevelupclasspassives) | Enum | Applies the 'UpgradeLevelUpClassPassives' effect. | 2 |
| [`UpgradeTaggedSpawnsToChampions`](./Enums.md#enum-upgradetaggedspawnstochampions) | Enum | Examples: `worm, bug` | 2 |
| `Vengeful` | Integer | Applies the 'Vengeful' effect. | 2 |
| `WeaponActiveEffectsMultiplierBonus` | Integer | Examples: `2` | 2 |
| `WeaponCountsAsBasicAttack` | Integer | Applies the 'WeaponCountsAsBasicAttack' effect. | 2 |
| `WeaponPassiveMultiplierBonus` | Integer | Examples: `2` | 2 |
| [`XIsLivingCharactersWithTag`](./Enums.md#enum-xislivingcharacterswithtag) | Enum | Applies or references the 'XIsLivingCharactersWithTag' effect/state. | 2 |
| `XIsOtherHealsThisTurn` | Integer | Applies or references the 'XIsOtherHealsThisTurn' effect/state. | 2 |
| `XIsSpellStormRampAndReset` | Integer | Math variable assignment: Evaluates X based on Spell Storm stacks, then resets them. | 2 |
| `XIsTimesDamageTaken` | Integer | Applies or references the 'XIsTimesDamageTaken' effect/state. | 2 |
| `Zombie` | Number | Examples: `1` | 2 |
| [`AbilityChargeRefundChance`](#abilitychargerefundchance) | Object | Applies the 'AbilityChargeRefundChance' effect. | 1 |
| `AbilityDamageMultiplier` | Float | Examples: `1.5` | 1 |
| `AbilityDisableIfLivingCrow` | Integer | Applies or references the 'AbilityDisableIfLivingCrow' effect/state. | 1 |
| `AbilityEnabledAtHealthThreshold` | Integer | Applies or references the 'AbilityEnabledAtHealthThreshold' effect/state. | 1 |
| `AbilityEnabledIfBasicAttackUsedThisTurn` | Integer | Applies or references the 'AbilityEnabledIfBasicAttackUsedThisTurn' effect/state. | 1 |
| `AbilityEnabledIfMovementTrapped` | Integer | Applies or references the 'AbilityEnabledIfMovementTrapped' effect/state. | 1 |
| `AbilityEnabledIfNoAggroTarget` | Integer | Applies or references the 'AbilityEnabledIfNoAggroTarget' effect/state. | 1 |
| [`AbilityEnabledIfNotHasStatus`](./Enums.md#enum-abilityenabledifnothasstatus) | Enum | Applies or references the 'AbilityEnabledIfNotHasStatus' effect/state. | 1 |
| [`AbilityEnabledIfSpecificItemEquipped`](./Enums.md#enum-abilityenabledifspecificitemequipped) | Enum | Applies or references the 'AbilityEnabledIfSpecificItemEquipped' effect/state. | 1 |
| [`AbilityOnBattleStart_UseAI`](./Enums.md#enum-abilityonbattlestart_useai) | Enum | Applies or references the 'AbilityOnBattleStart_UseAI' effect/state. | 1 |
| [`AbilityOnRoundEndOnce`](#abilityonroundendonce) | Object | Applies or references the 'AbilityOnRoundEndOnce' effect/state. | 1 |
| `AbsorbManaFromOtherSpells` | Integer | Applies or references the 'AbsorbManaFromOtherSpells' effect/state. | 1 |
| [`AddAdvantageToEvent`](#addadvantagetoevent) | Object | Applies or references the 'AddAdvantageToEvent' effect/state. | 1 |
| `AddAllyNeighborsToAbilityRange` | Integer | Applies the 'AddAllyNeighborsToAbilityRange' effect. | 1 |
| `AddAllyNeighborsToAttackRange` | Integer | Applies the 'AddAllyNeighborsToAttackRange' effect. | 1 |
| `AddChaScalingSpellDamage` | Integer | Applies the 'AddChaScalingSpellDamage' effect. | 1 |
| `AddConstitution` | Integer | Examples: `2` | 1 |
| [`AddElementsToSpells`](./Enums.md#enum-addelementstospells) | Enum | Applies or references the 'AddElementsToSpells' effect/state. | 1 |
| `AddKnockbackToEverything` | Integer | Applies the 'AddKnockbackToEverything' effect. | 1 |
| `AddLevelUpStatMultiplier` | Integer | Applies the 'AddLevelUpStatMultiplier' effect. | 1 |
| `AddLootMultiplier` | Integer | Examples: `1` | 1 |
| `AddRandomEliteBuff` | Integer | Examples: `1` | 1 |
| `AddRangedCritChance` | Integer | Applies the 'AddRangedCritChance' effect. | 1 |
| [`AddStatusesIfPersistentWeatherElement`](#addstatusesifpersistentweatherelement) | Object | Applies the 'AddStatusesIfPersistentWeatherElement' effect. | 1 |
| [`AddStatusesToReceivedElementalDamage`](#addstatusestoreceivedelementaldamage) | Object | Applies the 'AddStatusesToReceivedElementalDamage' effect. | 1 |
| [`AddStatusToBackstabs`](#addstatustobackstabs) | Object | Modifier: Injects a status effect into a specific action. | 1 |
| [`AddStatusToFirstSpellEachTurn`](#addstatustofirstspelleachturn) | Object | Examples: `{ ... }` | 1 |
| [`AddStatusToReceivedDamage`](#addstatustoreceiveddamage) | Object | Modifier: Applies a status effect whenever the character takes damage. | 1 |
| [`AddStatusToReceivedDamage_ExcludeStatuses`](#addstatustoreceiveddamage_excludestatuses) | Object | Applies the 'AddStatusToReceivedDamage_ExcludeStatuses' effect. | 1 |
| [`AddTemporaryEffectsToEquipment`](#addtemporaryeffectstoequipment) | Object | Applies the 'AddTemporaryEffectsToEquipment' effect. | 1 |
| [`AdvancedTint`](./Arrays.md#array-advancedtint) | Array | Applies or references the 'AdvancedTint' effect/state. | 1 |
| [`AdventureTokenPassivePool`](#adventuretokenpassivepool) | Object | Map/Metaprogression: Pool of passive modifiers applied by adventure tokens. | 1 |
| [`AggroTargetIsGovernedByHitEffect`](#aggrotargetisgovernedbyhiteffect) | Object | AI Logic: Forces the character's aggro to follow specific hit effects rather than default proximity. | 1 |
| `AggroTargetIsLastEnemyThatDealtDamage` | Integer | Applies or references the 'AggroTargetIsLastEnemyThatDealtDamage' effect/state. | 1 |
| `AggroTargetIsLowestHealthEnemyTillItDies` | Integer | Applies or references the 'AggroTargetIsLowestHealthEnemyTillItDies' effect/state. | 1 |
| `AggroTargetIsLowestMaxHealthCat` | Integer | Applies or references the 'AggroTargetIsLowestMaxHealthCat' effect/state. | 1 |
| [`AIControlNextTurn`](#aicontrolnextturn) | Object | Applies or references the 'AIControlNextTurn' effect/state. | 1 |
| [`AlienBeastDangerZones`](./Arrays.md#array-alienbeastdangerzones) | Array | Applies or references the 'AlienBeastDangerZones' effect/state. | 1 |
| `AlienBeastEyeStalks` | Integer | Applies or references the 'AlienBeastEyeStalks' effect/state. | 1 |
| `all_spells` | Variable |  | 1 |
| `AllDamageCrits` | Integer | Applies the 'AllDamageCrits' effect. | 1 |
| `AlliesAvoidTraps` | Integer | Applies the 'AlliesAvoidTraps' effect. | 1 |
| `AlliesScrambleSpellAfterCast` | Integer | Applies or references the 'AlliesScrambleSpellAfterCast' effect/state. | 1 |
| `AllSpellsCostActPoints` | Integer | Applies or references the 'AllSpellsCostActPoints' effect/state. | 1 |
| `AllSpellsCostCharge` | Integer | Applies or references the 'AllSpellsCostCharge' effect/state. | 1 |
| [`AllStatsAura`](#allstatsaura) | Object | Passive: Projects an aura that modifies all primary stats of nearby characters. | 1 |
| `AllUnitsExplodeOnDeath` | Integer | Applies or references the 'AllUnitsExplodeOnDeath' effect/state. | 1 |
| [`AlluringDoodieEater`](#alluringdoodieeater) | Object | Applies or references the 'AlluringDoodieEater' effect/state. | 1 |
| `AllyChainKnockback` | Integer | Applies the 'AllyChainKnockback' effect. | 1 |
| [`AllyDodgeChanceAura`](#allydodgechanceaura) | Object | Applies or references the 'AllyDodgeChanceAura' effect/state. | 1 |
| `AllyMultiplyKnockbackDistance` | Integer | Applies the 'AllyMultiplyKnockbackDistance' effect. | 1 |
| `AllyUncappedHPAura` | Integer | Applies the 'AllyUncappedHPAura' effect. | 1 |
| `AlphaAllStatsUp` | Integer | Applies or references the 'AlphaAllStatsUp' effect/state. | 1 |
| `AlphaDodgeChance` | Integer | Applies or references the 'AlphaDodgeChance' effect/state. | 1 |
| [`AlphaStatusOnTurnBegin`](#alphastatusonturnbegin) | Object | Grants a specific status effect to the 'Alpha' (the party leader) at the start of their turn. | 1 |
| `AlwaysChosenForLevelUp` | Integer | Applies or references the 'AlwaysChosenForLevelUp' effect/state. | 1 |
| `AmplifyNegativeStatus` | Integer | Applies the 'AmplifyNegativeStatus' effect. | 1 |
| [`animation_suffix`](./Enums.md#enum-animation_suffix) | String | ``, `Big`, `BigHolding`, `BigHoldingCat`, `Bishop` | 1 |
| `AOEBonus` | Integer | Applies or references the 'AOEBonus' effect/state. | 1 |
| [`ApplyPassivesToSpawnerWhileAlive`](#applypassivestospawnerwhilealive) | Object | Grants nested passives to the entity that spawned this object, lasting only as long as this object remains alive. | 1 |
| [`Autism`](#autism) | Object | Applies the 'Autism' effect. | 1 |
| `AvoidDamagingCharmedEnemies` | Integer | Applies or references the 'AvoidDamagingCharmedEnemies' effect/state. | 1 |
| `AwardCoinsOnDeath` | Integer | Applies or references the 'AwardCoinsOnDeath' effect/state. | 1 |
| `BackstabFront` | Integer | Examples: `1` | 1 |
| `BackstabWeakness` | Float | Applies the 'BackstabWeakness' effect. | 1 |
| `BalanceStats` | Integer | Applies or references the 'BalanceStats' effect/state. | 1 |
| `BasicAIDangerZone` | Integer | Applies or references the 'BasicAIDangerZone' effect/state. | 1 |
| [`BasicAttackStatusSwap`](./Arrays.md#array-basicattackstatusswap) | Array | Examples: `[ TempDamageUp DamageUp ]` | 1 |
| `BasicButcherMelee` | Variable |  | 1 |
| `BasicDruidAbility` | Variable |  | 1 |
| `BasicMagicMissile` | Variable |  | 1 |
| `BasicMagicShortRanged` | Variable |  | 1 |
| `BasicMedicMelee` | Variable |  | 1 |
| `BasicMelee` | Variable |  | 1 |
| `BasicMelee_4Hits` | Variable |  | 1 |
| `BasicNecroRanged` | Variable |  | 1 |
| `BasicPsychicPull` | Variable |  | 1 |
| `BasicRanged` | Variable |  | 1 |
| `BasicStraightShot` | Variable |  | 1 |
| `BasicSuplex` | Variable |  | 1 |
| `BasicTankMelee` | Variable |  | 1 |
| [`BattlefieldUniqueRandomPassive`](#battlefielduniquerandompassive) | Object | Map Rule: Grants a unique random passive modifier to the battlefield. | 1 |
| `BBTransformMutant` | Variable |  | 1 |
| `BBTransformZealot` | Variable |  | 1 |
| `BiggestFood` | Number | Applies or references the 'BiggestFood' effect/state. | 1 |
| `BigSplashDamage` | Integer | Applies the 'BigSplashDamage' effect. | 1 |
| `Bionic` | Variable |  | 1 |
| `BlackHolePassive` | Integer | Applies or references the 'BlackHolePassive' effect/state. | 1 |
| `BlessingOfPeace` | Integer | Applies or references the 'BlessingOfPeace' effect/state. | 1 |
| `BloatEyeMovement2` | Variable |  | 1 |
| [`BloatEyePassive2`](./Enums.md#enum-bloateyepassive2) | Enum | Applies or references the 'BloatEyePassive2' effect/state. | 1 |
| `BloatyExplodey` | Variable |  | 1 |
| `BlockAllDamage` | Integer | Applies or references the 'BlockAllDamage' effect/state. | 1 |
| `BlockDamageUnderThreshold` | Integer | Applies or references the 'BlockDamageUnderThreshold' effect/state. | 1 |
| `BlockNegativeStatus` | Integer | Applies or references the 'BlockNegativeStatus' effect/state. | 1 |
| `BombBehavior` | Integer | Applies or references the 'BombBehavior' effect/state. | 1 |
| `BoneWormShotMed` | Variable |  | 1 |
| [`BonusAbility_DelayedApplication`](./Enums.md#enum-bonusability_delayedapplication) | Enum | Applies or references the 'BonusAbility_DelayedApplication' effect/state. | 1 |
| `BonusHealthRegenBasedOnDex` | Integer | Applies the 'BonusHealthRegenBasedOnDex' effect. | 1 |
| `BonusHealthRegenPerDisorder` | Integer | Examples: `1` | 1 |
| `BonusRangeBasedOnDex` | Integer | Applies the 'BonusRangeBasedOnDex' effect. | 1 |
| `BonusToss` | Variable |  | 1 |
| `BonusToss2` | Variable |  | 1 |
| `BoostDamageAura` | Integer | Applies the 'BoostDamageAura' effect. | 1 |
| `BoostDamageGlobalAura` | Integer | Applies the 'BoostDamageGlobalAura' effect. | 1 |
| `BoostRangeAura` | Integer | Applies the 'BoostRangeAura' effect. | 1 |
| `BoostRangeGlobalAura` | Integer | Applies the 'BoostRangeGlobalAura' effect. | 1 |
| `BoostReceivedHealing` | Integer | Applies or references the 'BoostReceivedHealing' effect/state. | 1 |
| `BoyDino` | Variable |  | 1 |
| `BoyDinoCry` | Variable |  | 1 |
| `BrittleCharismaUp` | Integer | Applies or references the 'BrittleCharismaUp' effect/state. | 1 |
| `BrittleConstitutionUp` | Integer | Applies or references the 'BrittleConstitutionUp' effect/state. | 1 |
| `BrittleDexterityUp` | Integer | Applies or references the 'BrittleDexterityUp' effect/state. | 1 |
| `BrittleIntelligenceUp` | Integer | Applies or references the 'BrittleIntelligenceUp' effect/state. | 1 |
| `BrittleLuckUp` | Integer | Applies or references the 'BrittleLuckUp' effect/state. | 1 |
| `BrittleSpeedUp` | Integer | Applies or references the 'BrittleSpeedUp' effect/state. | 1 |
| `BrittleStrengthUp` | Integer | Applies or references the 'BrittleStrengthUp' effect/state. | 1 |
| [`BungaCheers`](#bungacheers) | Object | Animation/AI State: Bunga cheering animation logic. | 1 |
| `CantDodge` | Integer | Applies the 'CantDodge' effect. | 1 |
| `CapBasicAttackDamage` | Integer | Applies or references the 'CapBasicAttackDamage' effect/state. | 1 |
| `CapReceivedDamage` | Integer | Applies or references the 'CapReceivedDamage' effect/state. | 1 |
| `CatapultJump` | Variable |  | 1 |
| `CatapultJump2` | Variable |  | 1 |
| `CatGoop` | Variable |  | 1 |
| [`CatPartsSizeScale`](#catpartssizescale) | Object | Applies or references the 'CatPartsSizeScale' effect/state. | 1 |
| `CaveCatDad` | Variable |  | 1 |
| `CaveWomanBirthControl` | Integer | Applies or references the 'CaveWomanBirthControl' effect/state. | 1 |
| [`CerberubsAggroTargetBehavior`](#cerberubsaggrotargetbehavior) | Object | AI Logic: Custom aggro targeting rules for Cerberubs. | 1 |
| `CerberubsStraightReaction` | Variable |  | 1 |
| `ChanceToAmbush` | Integer | Applies or references the 'ChanceToAmbush' effect/state. | 1 |
| [`ChanceToForceEvent`](#chancetoforceevent) | Object | Applies or references the 'ChanceToForceEvent' effect/state. | 1 |
| [`ChanceToFormChangeOnAbilityDamage`](#chancetoformchangeonabilitydamage) | Object | Reaction: Probability to change forms when taking ability damage. | 1 |
| [`ChangeTileUnderCharacterAtStart`](./Enums.md#enum-changetileundercharacteratstart) | Enum | Applies or references the 'ChangeTileUnderCharacterAtStart' effect/state. | 1 |
| [`ChaosBossFormChangeGuide`](#chaosbossformchangeguide) | Object | Boss Logic: Maps the form transition phases for the Chaos Boss. | 1 |
| [`ChaosBossPieces`](#chaosbosspieces) | Object | Boss Logic: Defines the separate destructible pieces of the Chaos Boss. | 1 |
| [`ChaosHeadDropIn`](#chaosheaddropin) | Object | Boss Logic: Drop-in attack/animation for the Chaos Head. | 1 |
| `CharismaIsMaxStat` | Integer | Applies or references the 'CharismaIsMaxStat' effect/state. | 1 |
| `CharmedDemonKitten` | Variable |  | 1 |
| `CharmedLeech` | Variable |  | 1 |
| `CharmedPooter` | Variable |  | 1 |
| `CharmedReaper` | Variable |  | 1 |
| `CharmImmunity` | Integer | Applies or references the 'CharmImmunity' effect/state. | 1 |
| `choose_favorite_cat` | Variable |  | 1 |
| `Chubs` | Variable |  | 1 |
| `ChubsGoop` | Variable |  | 1 |
| `ChubsRage` | Variable |  | 1 |
| [`class`](./Enums.md#enum-class) | Enum | Categorizes the ability for specific UI filters. | 1 |
| [`Conditional_Flying`](#conditional_flying) | Object | Examples: `{ ... }` | 1 |
| [`Conditional_ManaThreshold`](#conditional_manathreshold) | Object | Conditional constraint. Nested properties only trigger if this is true. | 1 |
| [`Conditional_SourceHasTag`](#conditional_sourcehastag) | Object | Conditional object: Executes nested logic only if the target is/has SourceHasTag. | 1 |
| [`Conditional_Tiny`](#conditional_tiny) | Object | Examples: `{ ... }` | 1 |
| `ConductorManaRegen` | Integer | Applies the 'ConductorManaRegen' effect. | 1 |
| [`ConfusionEffectOnTaggedAbilities`](./Enums.md#enum-confusioneffectontaggedabilities) | Enum | Applies the 'ConfusionEffectOnTaggedAbilities' effect. | 1 |
| `ConsumablesMeleeRange` | Integer | Applies the 'ConsumablesMeleeRange' effect. | 1 |
| [`ConvertDamageToScaledStatus`](#convertdamagetoscaledstatus) | Object | Applies or references the 'ConvertDamageToScaledStatus' effect/state. | 1 |
| [`CounterAttackAfterEnemyCastSpell`](./Enums.md#enum-counterattackafterenemycastspell) | Enum | Applies or references the 'CounterAttackAfterEnemyCastSpell' effect/state. | 1 |
| `CounterNextAttacks` | Integer | Applies or references the 'CounterNextAttacks' effect/state. | 1 |
| `CraterCreeperOut` | Variable |  | 1 |
| `CrowAttackLink` | Integer | Applies or references the 'CrowAttackLink' effect/state. | 1 |
| [`CyborgTurns`](#cyborgturns) | Object | Examples: `{ ... }` | 1 |
| `DamageFromBehindOnly` | Integer | Applies or references the 'DamageFromBehindOnly' effect/state. | 1 |
| [`DamageIfDidntUseSpecificAbility`](#damageifdidntusespecificability) | Object | Combat Trigger: Deals damage to if didnt use specific ability. | 1 |
| `DarkOneStrike` | Variable |  | 1 |
| `DecoyExplode` | Variable |  | 1 |
| `DefaultMove` | Variable |  | 1 |
| `DelayedPain` | Integer | Applies or references the 'DelayedPain' effect/state. | 1 |
| `DemonicGlyph_Bounce` | Number | Applies or references the 'DemonicGlyph_Bounce' effect/state. | 1 |
| `DemonicGlyph_Fire` | Number | Applies or references the 'DemonicGlyph_Fire' effect/state. | 1 |
| `DemonicGlyph_Movement` | Number | Applies or references the 'DemonicGlyph_Movement' effect/state. | 1 |
| `DemonicGlyphStealer` | Integer | Applies or references the 'DemonicGlyphStealer' effect/state. | 1 |
| `DestroyerShieldBash` | Variable |  | 1 |
| [`Diabetes`](#diabetes) | Object | Applies the 'Diabetes' effect. | 1 |
| [`DiceBehavior`](#dicebehavior) | Object | AI Logic: Custom behavior for Dice enemies. | 1 |
| [`DicerArt`](./Arrays.md#array-dicerart) | Array | Applies or references the 'DicerArt' effect/state. | 1 |
| [`DiesToPiercingAndSpikes`](#diestopiercingandspikes) | Object | Vulnerability: Character dies instantly if hit by piercing attacks or spikes. | 1 |
| `DieWhenOnlyGolemsLeft` | Integer | Applies or references the 'DieWhenOnlyGolemsLeft' effect/state. | 1 |
| `DieWhenSpawnerDies` | Integer | Applies or references the 'DieWhenSpawnerDies' effect/state. | 1 |
| `Digest` | Variable |  | 1 |
| `DisableSpells` | Integer | Applies or references the 'DisableSpells' effect/state. | 1 |
| [`DisguisedTrapper`](./Enums.md#enum-disguisedtrapper) | Enum | Applies or references the 'DisguisedTrapper' effect/state. | 1 |
| `DisplayBuddyCatOnSpawn` | Integer | Applies or references the 'DisplayBuddyCatOnSpawn' effect/state. | 1 |
| `DivineShieldPickup` | Integer | Applies or references the 'DivineShieldPickup' effect/state. | 1 |
| `DodgeChanceWithBlindSpot` | Integer | Applies or references the 'DodgeChanceWithBlindSpot' effect/state. | 1 |
| [`DodgeWhenTargeted`](#dodgewhentargeted) | Object | Reaction: Executes a dodge maneuver when targeted. | 1 |
| `DoubleCastSpellIfManaCostUnderThreshold` | Integer | Applies or references the 'DoubleCastSpellIfManaCostUnderThreshold' effect/state. | 1 |
| `DoubleCastSpellThisTurn` | Integer | Applies or references the 'DoubleCastSpellThisTurn' effect/state. | 1 |
| [`DoubleCastTaggedSpells`](./Enums.md#enum-doublecasttaggedspells) | Enum | Applies or references the 'DoubleCastTaggedSpells' effect/state. | 1 |
| `DoubleReceivedNegativeStatus` | Integer | Applies or references the 'DoubleReceivedNegativeStatus' effect/state. | 1 |
| `DoubleReceivedPositiveStatus` | Integer | Applies or references the 'DoubleReceivedPositiveStatus' effect/state. | 1 |
| `DrMangler` | Variable |  | 1 |
| [`DropAsFamiliarOnTookDamage`](./Enums.md#enum-dropasfamiliarontookdamage) | Enum | Applies or references the 'DropAsFamiliarOnTookDamage' effect/state. | 1 |
| [`DropSoulJarOnDeath`](./Enums.md#enum-dropsouljarondeath) | Enum | Applies or references the 'DropSoulJarOnDeath' effect/state. | 1 |
| `DustCloudBehavior` | Integer | Applies or references the 'DustCloudBehavior' effect/state. | 1 |
| `Dybbuk1HPTracker` | Integer | Applies or references the 'Dybbuk1HPTracker' effect/state. | 1 |
| [`DybbukPossessionFallback`](#dybbukpossessionfallback) | Object | Logic: Fallback state when a Dybbuk possession fails. | 1 |
| `EachSpellFreeAtFullMana` | Integer | Applies the 'EachSpellFreeAtFullMana' effect. | 1 |
| `EatShit` | Variable |  | 1 |
| `ElectricArcs` | Integer | Applies or references the 'ElectricArcs' effect/state. | 1 |
| [`ElementWeakness`](./Enums.md#enum-elementweakness) | Enum | Applies or references the 'ElementWeakness' effect/state. | 1 |
| `end_of_round` | Boolean | `true` | 1 |
| `enemies` | Variable |  | 1 |
| `EnrageOnDamage` | Integer | Applies or references the 'EnrageOnDamage' effect/state. | 1 |
| `EraseSpawnCoins` | Integer | Applies or references the 'EraseSpawnCoins' effect/state. | 1 |
| `EventBounterHunterPassive` | Integer | Applies or references the 'EventBounterHunterPassive' effect/state. | 1 |
| `exclude_self` | Boolean | `false` | 1 |
| [`ExcludeFromEvents`](./Enums.md#enum-excludefromevents) | Enum | Applies or references the 'ExcludeFromEvents' effect/state. | 1 |
| `ExhaustionRoundChange` | Integer | Applies the 'ExhaustionRoundChange' effect. | 1 |
| `ExtraInjuryOnDeath` | Integer | Applies the 'ExtraInjuryOnDeath' effect. | 1 |
| [`ExtraTurnsPerTaggedUnit`](./Enums.md#enum-extraturnspertaggedunit) | Enum | Applies or references the 'ExtraTurnsPerTaggedUnit' effect/state. | 1 |
| `face_EatNeverstone` | Variable |  | 1 |
| `face_LeechBrood` | Variable |  | 1 |
| [`FaceAwayLastDamage`](#faceawaylastdamage) | Object | Reaction: Forces the character to face away from the last damage source. | 1 |
| `fetus` | Variable |  | 1 |
| [`FinalBossBeamQueue`](#finalbossbeamqueue) | Object | Boss Logic: Attack queue for the final boss beam. | 1 |
| [`FinalBossBecomeTheChild`](#finalbossbecomethechild) | Object | Boss Logic: Phase transition for the final boss. | 1 |
| [`FinalBossHitCountdownBoris`](#finalbosshitcountdownboris) | Object | Boss Logic: Countdown trigger for Boris. | 1 |
| [`FinalBossHitCountdownExplosive`](#finalbosshitcountdownexplosive) | Object | Boss Logic: Countdown trigger for explosives. | 1 |
| [`FinalBossHitCountdownHoly`](#finalbosshitcountdownholy) | Object | Boss Logic: Countdown trigger for holy attacks. | 1 |
| [`FinalBossPupils`](#finalbosspupils) | Object | Boss Logic: Pupil state management. | 1 |
| [`FinalBossShieldHealth`](#finalbossshieldhealth) | Object | Boss Logic: Shield health management. | 1 |
| [`FinalBossSyncAnimations`](#finalbosssyncanimations) | Object | Boss Logic: Synchronizes multi-part boss animations. | 1 |
| `FireExtinguish_Steam` | Variable |  | 1 |
| `FistOfFateUniqueEnemyTracker` | Integer | Applies or references the 'FistOfFateUniqueEnemyTracker' effect/state. | 1 |
| `FlatHealWhenDealDamage` | Integer | Examples: `1` | 1 |
| `FlingObjectsOnTop` | Integer | Applies or references the 'FlingObjectsOnTop' effect/state. | 1 |
| [`FlushmasterCelebration`](./Enums.md#enum-flushmastercelebration) | Enum | Applies or references the 'FlushmasterCelebration' effect/state. | 1 |
| `FlyBuff` | Variable |  | 1 |
| `ForceDodgeEverything` | Integer | Applies or references the 'ForceDodgeEverything' effect/state. | 1 |
| [`ForceUseAbilityOnTarget`](#forceuseabilityontarget) | Object | Applies or references the 'ForceUseAbilityOnTarget' effect/state. | 1 |
| [`FormChangeWhenBuddyDies`](./Enums.md#enum-formchangewhenbuddydies) | Enum | Applies or references the 'FormChangeWhenBuddyDies' effect/state. | 1 |
| `FrankBolts` | Integer | Applies or references the 'FrankBolts' effect/state. | 1 |
| `FreeFirstCastAndAfterSpendMana` | Integer | Applies or references the 'FreeFirstCastAndAfterSpendMana' effect/state. | 1 |
| `FreeFirstCastEachMatch` | Integer | Applies or references the 'FreeFirstCastEachMatch' effect/state. | 1 |
| `FreeSpellsAtFullMana` | Integer | Applies the 'FreeSpellsAtFullMana' effect. | 1 |
| `FrontstabBasicAttackCritChance` | Integer | Applies the 'FrontstabBasicAttackCritChance' effect. | 1 |
| `FrontstabCritChance` | Integer | Applies the 'FrontstabCritChance' effect. | 1 |
| `FullBlockEverything` | Integer | Applies or references the 'FullBlockEverything' effect/state. | 1 |
| `FullBlockEverythingTo0Damage` | Integer | Applies or references the 'FullBlockEverythingTo0Damage' effect/state. | 1 |
| `FullHealthAllStatsUp` | Integer | Applies the 'FullHealthAllStatsUp' effect. | 1 |
| `FullHealthManaRegen` | Integer | Applies the 'FullHealthManaRegen' effect. | 1 |
| [`FurnitureStats`](#furniturestats) | Object | Applies the 'FurnitureStats' effect. | 1 |
| `GainManaWhenAnythingDies` | Integer | Examples: `1` | 1 |
| `GasCanBehavior` | Integer | Applies or references the 'GasCanBehavior' effect/state. | 1 |
| `GasCloudBehavior2` | Integer | Applies or references the 'GasCloudBehavior2' effect/state. | 1 |
| `GeminiTwin` | Integer | Applies or references the 'GeminiTwin' effect/state. | 1 |
| `GirlDino` | Variable |  | 1 |
| `GirlDinoCry` | Variable |  | 1 |
| `GlobalFamiliarDamageBoost` | Integer | Examples: `1` | 1 |
| `GlobalFamiliarMoveBoost` | Integer | Examples: `1` | 1 |
| [`GlobalFlowerTrapperAura`](#globalflowertrapperaura) | Object | Examples: `{ ... }` | 1 |
| `GlobalManaDrainAura` | Integer | Applies or references the 'GlobalManaDrainAura' effect/state. | 1 |
| [`GlobalMeleeRevengeDamage`](#globalmeleerevengedamage) | Object | Applies or references the 'GlobalMeleeRevengeDamage' effect/state. | 1 |
| `GoopImmunity` | Integer | Applies or references the 'GoopImmunity' effect/state. | 1 |
| `grub_familiar` | Variable |  | 1 |
| `Guillotina2Body` | Variable |  | 1 |
| `Guillotina2Head` | Variable |  | 1 |
| `Guillotina3Body` | Variable |  | 1 |
| `Guillotina3Head` | Variable |  | 1 |
| `GuillotinaDeathHead` | Integer | Applies or references the 'GuillotinaDeathHead' effect/state. | 1 |
| [`HarpoonTrapPassive`](./Enums.md#enum-harpoontrappassive) | Enum | Applies or references the 'HarpoonTrapPassive' effect/state. | 1 |
| `HCHumanDie` | Variable |  | 1 |
| `HealAtStart` | Integer | Applies the 'HealAtStart' effect. | 1 |
| `HealingAura` | Integer | Applies the 'HealingAura' effect. | 1 |
| [`HealNeighborsEachTurn`](#healneighborseachturn) | Object | Passive: Restores health to adjacent allies at the start of the turn. | 1 |
| `HemBounce` | Variable |  | 1 |
| `HiddenDoomed` | Integer | Applies or references the 'HiddenDoomed' effect/state. | 1 |
| [`HideEquipment`](./Enums.md#enum-hideequipment) | Enum | Applies or references the 'HideEquipment' effect/state. | 1 |
| `HideSomeHudStuff` | Integer | Applies or references the 'HideSomeHudStuff' effect/state. | 1 |
| [`HitlerExecute`](#hitlerexecute) | Object | Boss Logic: Specific execution or ultimate attack state. | 1 |
| `HolyDamageMultiplierBonus` | Integer | Applies the 'HolyDamageMultiplierBonus' effect. | 1 |
| [`HPAltStates`](#hpaltstates) | Object | Visual: Alternative sprite states based on current health. | 1 |
| [`Hunter`](./Arrays.md#array-hunter) | Object | Applies or references the 'Hunter' effect/state. | 1 |
| `Hyde` | Variable |  | 1 |
| `Hypomania` | Integer | Applies the 'Hypomania' effect. | 1 |
| `IceBlockBehavior` | Integer | Applies or references the 'IceBlockBehavior' effect/state. | 1 |
| `IDSprout` | Variable |  | 1 |
| `IncreaseItemUsesOnEquip` | Integer | Applies the 'IncreaseItemUsesOnEquip' effect. | 1 |
| `InheritSpawnerStats` | Integer | Applies or references the 'InheritSpawnerStats' effect/state. | 1 |
| `insane` | Object | Examples: `{ ... }` | 1 |
| `InsertIntoBackgroundPlaceholder` | Integer | Applies or references the 'InsertIntoBackgroundPlaceholder' effect/state. | 1 |
| `InterchangeDisabler` | Integer | Applies or references the 'InterchangeDisabler' effect/state. | 1 |
| `InvertBrainFaction` | Integer | Applies the 'InvertBrainFaction' effect. | 1 |
| `JesterLevelUpRerolls` | Integer | Applies or references the 'JesterLevelUpRerolls' effect/state. | 1 |
| [`JohnnyNeedsWashing`](#johnnyneedswashing) | Object | Character Form: Behavior and stats for the 'JohnnyNeedsWashing' state. | 1 |
| [`JohnnyWasher`](./Enums.md#enum-johnnywasher) | Enum | Applies or references the 'JohnnyWasher' effect/state. | 1 |
| [`KnockbackIfCrit`](#knockbackifcrit) | Object | Applies or references the 'KnockbackIfCrit' effect/state. | 1 |
| [`LegacySpawnSavedCatIfExists`](./Enums.md#enum-legacyspawnsavedcatifexists) | Enum | Applies or references the 'LegacySpawnSavedCatIfExists' effect/state. | 1 |
| `LennyCatDies` | Variable |  | 1 |
| [`LimitedTileTrail`](./Enums.md#enum-limitedtiletrail) | Enum | Applies the 'LimitedTileTrail' effect. | 1 |
| `LimitSelfKnockbackDamage` | Integer | Applies the 'LimitSelfKnockbackDamage' effect. | 1 |
| [`LockOrientationFaceTile`](./Arrays.md#array-lockorientationfacetile) | Array | Applies or references the 'LockOrientationFaceTile' effect/state. | 1 |
| `Lucky` | Enum | data/boss_elite_buffs.gon, data/elite_buffs.gon | 1 |
| [`ManaGainRange`](#managainrange) | Object | Applies or references the 'ManaGainRange' effect/state. | 1 |
| `ManglerEnrage` | Variable |  | 1 |
| `ManglerMonsterDashAttack` | Variable |  | 1 |
| [`ManglerMonsterPassive`](./Enums.md#enum-manglermonsterpassive) | Enum | Applies or references the 'ManglerMonsterPassive' effect/state. | 1 |
| `ManglersMonster` | Variable |  | 1 |
| `MaxAccuracy` | Integer | Applies the 'MaxAccuracy' effect. | 1 |
| `MaxStartingMana` | Integer | Applies the 'MaxStartingMana' effect. | 1 |
| `meat` | Variable |  | 1 |
| `MechExplode` | Variable |  | 1 |
| [`Medic`](./Arrays.md#array-medic) | Object | Applies or references the 'Medic' effect/state. | 1 |
| [`MegaDinoDropController`](#megadinodropcontroller) | Object | Boss Logic: Manages loot drops for the Mega Dino. | 1 |
| `MegaFart` | Variable |  | 1 |
| `MegaGuppy_SummonTheChild` | Variable |  | 1 |
| `MockingbirdForm` | Variable |  | 1 |
| `ModelingClayPassive` | Integer | Applies or references the 'ModelingClayPassive' effect/state. | 1 |
| [`ModularPickup`](#modularpickup) | Object | Pickup Logic: Defines what happens when a modular item is collected. | 1 |
| [`MonkCatReactionAbilities`](#monkcatreactionabilities) | Object | Reaction: Specific counter-attack or dodge abilities used by the Monk class. | 1 |
| `MoonHead_KillHands` | Variable |  | 1 |
| [`MoonHeadCrackedVisual`](./Enums.md#enum-moonheadcrackedvisual) | Enum | Applies or references the 'MoonHeadCrackedVisual' effect/state. | 1 |
| [`MotherGrowController`](#mothergrowcontroller) | Object | Boss Logic: Manages the growth phases of the Mother boss. | 1 |
| [`MotherTumorPassive`](#mothertumorpassive) | Object | Boss Logic: Passive effects applied to the Mother's tumors. | 1 |
| [`Mount`](#mount) | Object | Character Form: Behavior and stats for the 'Mount' state. | 1 |
| [`move`](./Arrays.md#array-move) | Enum | `BasicJump`, `BungaJumpMove`, `DefaultMove`, `DoNothing`, `DustMove` | 1 |
| [`MoveAfterAnyAttemptedAttack`](#moveafteranyattemptedattack) | Object | AI Movement: Forces a move action immediately after attacking, even if it missed. | 1 |
| [`MoveAwayWhenEnemyAdjacent`](#moveawaywhenenemyadjacent) | Object | AI Movement: Moves away if an enemy enters an adjacent tile. | 1 |
| `MoveRandomly` | Integer | Applies the 'MoveRandomly' effect. | 1 |
| `MulticatHeads` | Integer | Applies or references the 'MulticatHeads' effect/state. | 1 |
| `MultiplyCoinsOnBattleStart` | Integer | Applies or references the 'MultiplyCoinsOnBattleStart' effect/state. | 1 |
| `MultiplyReceivedHealing` | Integer | Applies or references the 'MultiplyReceivedHealing' effect/state. | 1 |
| [`MultiSpawnOnDeath`](#multispawnondeath) | Object | Event Trigger: Spawns multiple entities upon death. | 1 |
| `MutateAfterXTurns` | Integer | Applies or references the 'MutateAfterXTurns' effect/state. | 1 |
| `MuteDemonicGlyphDisplay` | Integer | Applies or references the 'MuteDemonicGlyphDisplay' effect/state. | 1 |
| [`neck`](./Enums.md#enum-neck) | Enum | `AngelicAura`, `AngelicAura_Terminator`, `DruidNeck`, `DruidNeck_Terminator`, `MageCollar` | 1 |
| `neck_NukeBonus` | Variable |  | 1 |
| `neck_NukeExplode` | Variable |  | 1 |
| `Necro_SoulDagger_Uncharged` | Variable |  | 1 |
| `NoHead` | Variable |  | 1 |
| `NonChampionFlySwarm` | Variable |  | 1 |
| `NonLethal` | Integer | Applies the 'NonLethal' effect. | 1 |
| `Nubs` | Variable |  | 1 |
| `NubsGoop` | Variable |  | 1 |
| [`ObjectDetector`](#objectdetector) | Object | Applies or references the 'ObjectDetector' effect/state. | 1 |
| `Ornstein` | Variable |  | 1 |
| `OrthogonalAIDangerZone` | Integer | Applies or references the 'OrthogonalAIDangerZone' effect/state. | 1 |
| `OverManaReducesManaCosts` | Integer | Examples: `1` | 1 |
| `OverrideMaxMana` | Integer | Applies the 'OverrideMaxMana' effect. | 1 |
| `OverridePalette` | Integer | Applies the 'OverridePalette' effect. | 1 |
| `PackHunting` | Integer | Applies or references the 'PackHunting' effect/state. | 1 |
| `Paper` | Variable |  | 1 |
| [`Paranoia`](./Enums.md#enum-paranoia) | Enum | Applies the 'Paranoia' effect. | 1 |
| [`PassiveLevelScaledStatus`](#passivelevelscaledstatus) | Object | Applies the 'PassiveLevelScaledStatus' effect. | 1 |
| [`PassiveWhileHasDurability`](#passivewhilehasdurability) | Object | Applies or references the 'PassiveWhileHasDurability' effect/state. | 1 |
| [`PassiveWhileNotTakingTurn`](#passivewhilenottakingturn) | Object | Grants nested passives that are only active while it is NOT the character's turn. | 1 |
| [`PassiveWhileShielded`](#passivewhileshielded) | Object | Applies or references the 'PassiveWhileShielded' effect/state. | 1 |
| `PercentHeal` | Integer | Applies the 'PercentHeal' effect. | 1 |
| `PermanentConfusion` | Number | Applies or references the 'PermanentConfusion' effect/state. | 1 |
| `PermanentKitten` | Integer | Applies the 'PermanentKitten' effect. | 1 |
| `PhysicalAttacksMiss` | Integer | Applies or references the 'PhysicalAttacksMiss' effect/state. | 1 |
| `pickup` | Variable |  | 1 |
| `plant` | Variable |  | 1 |
| `PlayerCat_ThiefShade2` | Variable |  | 1 |
| `PoisonMultiplier` | Integer | Applies the 'PoisonMultiplier' effect. | 1 |
| `Poop` | Variable |  | 1 |
| `PreEmptiveCounterNextAttacks` | Integer | Applies or references the 'PreEmptiveCounterNextAttacks' effect/state. | 1 |
| [`PreventSpecificInjury`](./Enums.md#enum-preventspecificinjury) | Enum | Applies or references the 'PreventSpecificInjury' effect/state. | 1 |
| `pyrophina` | Variable |  | 1 |
| [`RandomPermanentStatsDistinct`](#randompermanentstatsdistinct) | Object | Examples: `{ ... }` | 1 |
| `RatKing` | Variable |  | 1 |
| `RealTimePressure_OneUnit` | Integer | Applies the 'RealTimePressure_OneUnit' effect. | 1 |
| [`ReceivedStatusReplacement`](./Arrays.md#array-receivedstatusreplacement) | Array | Examples: `[ Sleep SleepParalysis ]` | 1 |
| `ReclaimItemOnBreak` | Integer | Applies or references the 'ReclaimItemOnBreak' effect/state. | 1 |
| `ReduceSpellCostsPerDisorder` | Integer | Applies or references the 'ReduceSpellCostsPerDisorder' effect/state. | 1 |
| `ReduceSpellCostsPerParasite` | Integer | Applies or references the 'ReduceSpellCostsPerParasite' effect/state. | 1 |
| `RefreshMoveOnWeaponConnect` | Integer | Applies the 'RefreshMoveOnWeaponConnect' effect. | 1 |
| `ReloadOnAllyCatDies` | Integer | Applies or references the 'ReloadOnAllyCatDies' effect/state. | 1 |
| `ReloadOnAllyDies` | Integer | Applies or references the 'ReloadOnAllyDies' effect/state. | 1 |
| `ReloadOnAnyDamage` | Integer | Applies or references the 'ReloadOnAnyDamage' effect/state. | 1 |
| `ReloadOnBackstab` | Integer | Applies or references the 'ReloadOnBackstab' effect/state. | 1 |
| [`ReloadOnElementalDamageReceived`](./Enums.md#enum-reloadonelementaldamagereceived) | Enum | Applies or references the 'ReloadOnElementalDamageReceived' effect/state. | 1 |
| `ReloadOnGainCoins` | Integer | Applies or references the 'ReloadOnGainCoins' effect/state. | 1 |
| `ReloadOnGainDivineShield` | Integer | Applies or references the 'ReloadOnGainDivineShield' effect/state. | 1 |
| [`ReloadOnKillTagged`](./Enums.md#enum-reloadonkilltagged) | Enum | Applies or references the 'ReloadOnKillTagged' effect/state. | 1 |
| `ReloadOnSpendMana` | Integer | Applies or references the 'ReloadOnSpendMana' effect/state. | 1 |
| `ReloadOnUseAbilityWithManaCost` | Integer | Applies or references the 'ReloadOnUseAbilityWithManaCost' effect/state. | 1 |
| `RemoteFlatLeech` | Integer | Applies or references the 'RemoteFlatLeech' effect/state. | 1 |
| [`RemoveAmbientLightEffects`](./Enums.md#enum-removeambientlighteffects) | Float | Applies or references the 'RemoveAmbientLightEffects' effect/state. | 1 |
| `RemoveExtraDispersedTurn` | Integer | Examples: `1` | 1 |
| [`RemoveGlobalModifiers`](./Arrays.md#array-removeglobalmodifiers) | Array | Applies or references the 'RemoveGlobalModifiers' effect/state. | 1 |
| [`ReplaceBasicAttack_Mutation`](./Enums.md#enum-replacebasicattack_mutation) | Enum | Examples: `FetusSpit` | 1 |
| [`ReplaceBlankTilesOnBattleStart`](./Enums.md#enum-replaceblanktilesonbattlestart) | Enum | Applies or references the 'ReplaceBlankTilesOnBattleStart' effect/state. | 1 |
| [`ReplaceBrain`](#replacebrain) | Object | Applies the 'ReplaceBrain' effect. | 1 |
| [`ReplaceSpellsWhenDead`](./Enums.md#enum-replacespellswhendead) | Enum | Applies the 'ReplaceSpellsWhenDead' effect. | 1 |
| `RerollItemsOnBattleEnd` | Integer | Applies or references the 'RerollItemsOnBattleEnd' effect/state. | 1 |
| [`RockyArmorSalvage`](./Enums.md#enum-rockyarmorsalvage) | Float | Examples: `.75` | 1 |
| `RunWhenKittensDead` | Integer | Applies or references the 'RunWhenKittensDead' effect/state. | 1 |
| [`RunWhenLastPlayerCatIsCharmed`](#runwhenlastplayercatischarmed) | Object | AI Logic: Flee logic when the player team is entirely crowd-controlled. | 1 |
| `SandStormBuff` | Variable |  | 1 |
| [`ScaldingOrbMoonBossOneShot`](#scaldingorbmoonbossoneshot) | Object | Applies or references the 'ScaldingOrbMoonBossOneShot' effect/state. | 1 |
| [`ScaledStatusAlliesOnSpendMana`](#scaledstatusalliesonspendmana) | Object | Applies or references the 'ScaledStatusAlliesOnSpendMana' effect/state. | 1 |
| [`ScaledStatusOnBleedDamage`](#scaledstatusonbleeddamage) | Object | Applies the 'ScaledStatusOnBleedDamage' effect. | 1 |
| [`ScaledStatusOnHolyShieldBlock`](#scaledstatusonholyshieldblock) | Object | Applies or references the 'ScaledStatusOnHolyShieldBlock' effect/state. | 1 |
| [`ScaledStatusOnLoseShield`](#scaledstatusonloseshield) | Object | Applies the 'ScaledStatusOnLoseShield' effect. | 1 |
| [`ScaledStatusOnOverHealed`](#scaledstatusonoverhealed) | Object | Applies the 'ScaledStatusOnOverHealed' effect. | 1 |
| [`ScalingAttackAnimation`](#scalingattackanimation) | Object | Visual: Animation scales based on damage output. | 1 |
| `SchizoIllusionAIModifier` | Integer | Applies or references the 'SchizoIllusionAIModifier' effect/state. | 1 |
| `SchrodingerDisorder` | Integer | Applies the 'SchrodingerDisorder' effect. | 1 |
| `Scleroderma` | Integer | Applies the 'Scleroderma' effect. | 1 |
| [`SelfDamageWhenDealDamage`](#selfdamagewhendealdamage) | Object | Applies the 'SelfDamageWhenDealDamage' effect. | 1 |
| `set_WitchJump` | Variable |  | 1 |
| [`SetFaction`](./Enums.md#enum-setfaction) | Enum | Applies or references the 'SetFaction' effect/state. | 1 |
| `Shadowstep` | Variable |  | 1 |
| `ShineBuff` | Variable |  | 1 |
| `Shove` | Variable |  | 1 |
| [`SkipFirstRounds`](#skipfirstrounds) | Object | AI Logic: Passes turn for the first X rounds of combat. | 1 |
| `SleepDart` | Variable |  | 1 |
| `SleepDart2` | Variable |  | 1 |
| `SmokeBuff` | Variable |  | 1 |
| `Smough` | Variable |  | 1 |
| `SpawnCatCloneOnCorpsePopped` | Integer | Applies or references the 'SpawnCatCloneOnCorpsePopped' effect/state. | 1 |
| `SpawnCreepOnHitKnockback` | Integer | Applies or references the 'SpawnCreepOnHitKnockback' effect/state. | 1 |
| `spawner` | Variable |  | 1 |
| `SpawnerCatDataReference` | Integer | Applies or references the 'SpawnerCatDataReference' effect/state. | 1 |
| [`SpawnMeatOnMove`](./Enums.md#enum-spawnmeatonmove) | Enum | Applies the 'SpawnMeatOnMove' effect. | 1 |
| [`SpawnRandomPickupsOnTaggedUnitKilled`](#spawnrandompickupsontaggedunitkilled) | Object | Applies or references the 'SpawnRandomPickupsOnTaggedUnitKilled' effect/state. | 1 |
| `SpeedUp_WithoutInitiative` | Integer | Applies or references the 'SpeedUp_WithoutInitiative' effect/state. | 1 |
| [`SpewerAltGraphics`](#speweraltgraphics) | Object | Visual: Alternative graphics for Spewer enemies. | 1 |
| `SpiderReturn` | Variable |  | 1 |
| `Spook` | Variable |  | 1 |
| `SpreadPainBonusCrit` | Integer | Applies the 'SpreadPainBonusCrit' effect. | 1 |
| `SpreadWater` | Integer | Applies or references the 'SpreadWater' effect/state. | 1 |
| `sprout` | Variable |  | 1 |
| `SproutsGrantMovement` | Integer | Applies or references the 'SproutsGrantMovement' effect/state. | 1 |
| [`StackingDodgeChanceOnTookDamage`](#stackingdodgechanceontookdamage) | Object | Applies the 'StackingDodgeChanceOnTookDamage' effect. | 1 |
| [`StacyMutant_Brace`](#stacymutant_brace) | Object | Character Form: Behavior and stats for the 'StacyMutant_Brace' state. | 1 |
| [`StacyMutant_Counter`](#stacymutant_counter) | Object | Character Form: Behavior and stats for the 'StacyMutant_Counter' state. | 1 |
| [`StacyMutant_Damage`](#stacymutant_damage) | Object | Character Form: Behavior and stats for the 'StacyMutant_Damage' state. | 1 |
| [`StacyMutant_DoubleHead`](#stacymutant_doublehead) | Object | Character Form: Behavior and stats for the 'StacyMutant_DoubleHead' state. | 1 |
| [`StacyMutant_Fire`](#stacymutant_fire) | Object | Character Form: Behavior and stats for the 'StacyMutant_Fire' state. | 1 |
| [`StacyMutant_Health`](#stacymutant_health) | Object | Character Form: Behavior and stats for the 'StacyMutant_Health' state. | 1 |
| [`StacyMutant_Holy`](#stacymutant_holy) | Object | Character Form: Behavior and stats for the 'StacyMutant_Holy' state. | 1 |
| [`StacyMutant_Ice`](#stacymutant_ice) | Object | Character Form: Behavior and stats for the 'StacyMutant_Ice' state. | 1 |
| [`StacyMutant_Lightning`](#stacymutant_lightning) | Object | Character Form: Behavior and stats for the 'StacyMutant_Lightning' state. | 1 |
| [`StacyMutant_Mirror`](#stacymutant_mirror) | Object | Character Form: Behavior and stats for the 'StacyMutant_Mirror' state. | 1 |
| [`StacyMutant_Speed`](#stacymutant_speed) | Object | Character Form: Behavior and stats for the 'StacyMutant_Speed' state. | 1 |
| [`StacyMutant_Thorns`](#stacymutant_thorns) | Object | Character Form: Behavior and stats for the 'StacyMutant_Thorns' state. | 1 |
| `StartDead` | Integer | Applies or references the 'StartDead' effect/state. | 1 |
| [`StatDependentPassive`](#statdependentpassive) | Object | Applies or references the 'StatDependentPassive' effect/state. | 1 |
| [`StatusAdjacentOnTheirTurnBegin`](#statusadjacentontheirturnbegin) | Object | Event Trigger: Applies nested statuses to adjacent on their turn begin. | 1 |
| [`StatusAdjacentOnTheirTurnEnd`](#statusadjacentontheirturnend) | Object | Applies or references the 'StatusAdjacentOnTheirTurnEnd' effect/state. | 1 |
| [`StatusAfterXStacks`](#statusafterxstacks) | Object | Applies or references the 'StatusAfterXStacks' effect/state. | 1 |
| [`StatusAlliesEachTurn`](#statusallieseachturn) | Object | Applies or references the 'StatusAlliesEachTurn' effect/state. | 1 |
| [`StatusAlliesOnSpendMana`](#statusalliesonspendmana) | Object | Event Trigger: Applies nested statuses to allies on spend mana. | 1 |
| [`StatusAlliesScaledByCursedOnDeath`](#statusalliesscaledbycursedondeath) | Object | Event Trigger: Applies nested statuses to allies scaled by cursed on death. | 1 |
| [`StatusEachTurnBeginIfHasStatus`](#statuseachturnbeginifhasstatus) | Object | Event Trigger: Applies a status at the start of the turn if a prerequisite status is met. | 1 |
| [`StatusEachTurnEndIfEnabledAtStartOfTurn`](#statuseachturnendifenabledatstartofturn) | Object | Event Trigger: Applies a status at the end of the turn if an enabling condition was met at the start. | 1 |
| [`StatusEveryXSpellCastsEachTurn`](#statuseveryxspellcastseachturn) | Object | Examples: `{ ... }` | 1 |
| [`StatusIfBattleAlreadyBegan`](#statusifbattlealreadybegan) | Object | Event Trigger: Applies nested statuses to if battle already began. | 1 |
| [`StatusIfDidntMove`](#statusifdidntmove) | Object | Examples: `{ ... }` | 1 |
| [`StatusOnDodge`](#statusondodge) | Object | Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnEnemyCastSpell`](#statusonenemycastspell) | Object | Examples: `{ ... }` | 1 |
| [`StatusOnEnemyConfused`](#statusonenemyconfused) | Object | Event Trigger: Applies statuses when an enemy becomes confused. | 1 |
| [`StatusOnEnemyDeath`](#statusonenemydeath) | Object | Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnFallAsleep`](#statusonfallasleep) | Object | Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnFullMana`](#statusonfullmana) | Object | Event Trigger: Applies statuses when this action occurs. | 1 |
| [`StatusOnLoseShield`](#statusonloseshield) | Object | Event Trigger: Applies nested statuses when lose shield. | 1 |
| [`StatusOnTakeHealthDamage`](#statusontakehealthdamage) | Object | Event Trigger: Applies nested statuses when take health damage. | 1 |
| [`StatusOverlappingCharactersAndDie`](#statusoverlappingcharactersanddie) | Object | Event Trigger: Applies statuses to overlapping entities, then destroys self. | 1 |
| [`StatusWhenStatusCompletelyRemoved`](#statuswhenstatuscompletelyremoved) | Object | Event Trigger: Applies statuses when a tracked status effect is fully cleansed. | 1 |
| `StealthUntilBasicAttack` | Integer | Applies or references the 'StealthUntilBasicAttack' effect/state. | 1 |
| `StevenBolts` | Integer | Applies or references the 'StevenBolts' effect/state. | 1 |
| `StrictLimitDamage` | Integer | Applies the 'StrictLimitDamage' effect. | 1 |
| `StripKnockback` | Integer | Applies or references the 'StripKnockback' effect/state. | 1 |
| [`SupportDieInsteadOfRun`](#supportdieinsteadofrun) | Object | AI Logic: Forces a support unit to die rather than flee. | 1 |
| [`SwimmingFormChange`](#swimmingformchange) | Object | Logic: Automates form change when entering/exiting water. | 1 |
| [`SyncFormsWithBuddy`](#syncformswithbuddy) | Object | Logic: Forces this character's form to match their familiar/buddy. | 1 |
| [`T3HitlerSpawningPhase`](#t3hitlerspawningphase) | Object | Boss Logic: Minion spawn phase for the T3 Hitler boss. | 1 |
| [`TakeBonusTurnWithStatus`](#takebonusturnwithstatus) | Object | Grants the character an immediate extra turn while afflicted with specific statuses. | 1 |
| `TakeWeaponFromSpawner` | Integer | Applies or references the 'TakeWeaponFromSpawner' effect/state. | 1 |
| `Tall` | Integer | Applies or references the 'Tall' effect/state. | 1 |
| [`TallTumorManaBurn`](./Enums.md#enum-talltumormanaburn) | Enum | Applies or references the 'TallTumorManaBurn' effect/state. | 1 |
| `TattersFear` | Variable |  | 1 |
| `TauntAtFullHealth` | Integer | Applies the 'TauntAtFullHealth' effect. | 1 |
| `TC_DashReaction` | Variable |  | 1 |
| `TempMeleeRangeUp` | Integer | Applies or references the 'TempMeleeRangeUp' effect/state. | 1 |
| [`Terminator2Chase`](./Enums.md#enum-terminator2chase) | Enum | Applies or references the 'Terminator2Chase' effect/state. | 1 |
| [`Terminator2Run`](#terminator2run) | Object | AI Movement: Specific run logic for Terminator2. | 1 |
| [`TerminatorChase`](#terminatorchase) | Object | AI Movement: Specific chase logic for Terminator. | 1 |
| [`TerminatorSkin`](#terminatorskin) | Object | Visual: Skin definition for Terminator. | 1 |
| `TheCreator_SpawnCloneTeam` | Variable |  | 1 |
| [`TheHunger`](#thehunger) | Object | Applies the 'TheHunger' effect. | 1 |
| `ThornUp` | Variable |  | 1 |
| `ThrobbingKing2` | Variable |  | 1 |
| [`TileElementDamageImmunity`](./Enums.md#enum-tileelementdamageimmunity) | Enum | Applies or references the 'TileElementDamageImmunity' effect/state. | 1 |
| [`Tinkerer`](./Arrays.md#array-tinkerer) | Object | Applies or references the 'Tinkerer' effect/state. | 1 |
| [`TintItem`](#tintitem) | Object | Applies or references the 'TintItem' effect/state. | 1 |
| `TireBehavior` | Integer | Applies or references the 'TireBehavior' effect/state. | 1 |
| `TormentorHeal` | Integer | Applies or references the 'TormentorHeal' effect/state. | 1 |
| `TormentorRuneAbsorb` | Variable |  | 1 |
| `TossTargetIsAggroTarget` | Integer | Applies or references the 'TossTargetIsAggroTarget' effect/state. | 1 |
| `TossTargetIsBuddy` | Integer | Applies or references the 'TossTargetIsBuddy' effect/state. | 1 |
| `TossTargetIsNotInWater` | Integer | Applies or references the 'TossTargetIsNotInWater' effect/state. | 1 |
| [`TourettesMeows`](#tourettesmeows) | Object | Applies the 'TourettesMeows' effect. | 1 |
| `ToxicBubbles` | Variable |  | 1 |
| `ToxPuff` | Variable |  | 1 |
| [`TrackAmountKilledByPlayer`](./Enums.md#enum-trackamountkilledbyplayer) | Enum | Applies or references the 'TrackAmountKilledByPlayer' effect/state. | 1 |
| [`TransformOnStatusThreshold`](#transformonstatusthreshold) | Object | Logic: Changes form when a status effect reaches a certain stack count. | 1 |
| `TrexSwitchTarget` | Variable |  | 1 |
| `TriggerBleedOnBleed` | Integer | Examples: `1` | 1 |
| `Triskaidekaphobia` | Integer | Applies the 'Triskaidekaphobia' effect. | 1 |
| `TT_Thrash` | Variable |  | 1 |
| `tumor` | Variable |  | 1 |
| [`TunnelVision`](#tunnelvision) | Object | Applies or references the 'TunnelVision' effect/state. | 1 |
| `TutorialBossRiggedFight` | Integer | Applies or references the 'TutorialBossRiggedFight' effect/state. | 1 |
| `TVBotDisableAttack` | Integer | Applies or references the 'TVBotDisableAttack' effect/state. | 1 |
| `TVBotDisableMove` | Integer | Applies or references the 'TVBotDisableMove' effect/state. | 1 |
| `TVBotDisableSpells` | Integer | Applies or references the 'TVBotDisableSpells' effect/state. | 1 |
| [`TVBotScreen`](#tvbotscreen) | Object | Visual: TV Bot screen state. | 1 |
| `Twister_loop` | Enum |  | 1 |
| [`TwisterFling`](#twisterfling) | Object | Logic: Fling behavior for tornado attacks. | 1 |
| `UFO_BigExplode` | Variable |  | 1 |
| `UltraSmough` | Variable |  | 1 |
| `UncappedHPBonusStr` | Integer | Applies the 'UncappedHPBonusStr' effect. | 1 |
| [`UnlimitedDeathRattleRevive`](#unlimiteddeathrattlerevive) | Object | Logic: Endless resurrection on death. | 1 |
| `UpTireBehavior` | Integer | Applies or references the 'UpTireBehavior' effect/state. | 1 |
| [`UseAbility_Madness`](./Enums.md#enum-useability_madness) | Enum | Applies the 'UseAbility_Madness' effect. | 1 |
| [`UseAbilityWhenOutOfStatus`](#useabilitywhenoutofstatus) | Object | Logic: Casts a specific ability the moment a status effect expires. | 1 |
| [`UseAbilityWhenShieldDepleted`](./Enums.md#enum-useabilitywhenshielddepleted) | Enum | Applies or references the 'UseAbilityWhenShieldDepleted' effect/state. | 1 |
| `Wall` | Integer | Applies or references the 'Wall' effect/state. | 1 |
| `Wet` | Integer | Applies or references the 'Wet' effect/state. | 1 |
| [`WhitelistPickupType`](./Enums.md#enum-whitelistpickuptype) | Enum | Applies or references the 'WhitelistPickupType' effect/state. | 1 |
| `WideBackstab` | Integer | Applies or references the 'WideBackstab' effect/state. | 1 |
| `Wind` | Object | Examples: `{ ... }` | 1 |
| `WispDodge` | Integer | Applies or references the 'WispDodge' effect/state. | 1 |
| `WobblyCat` | Integer | Applies the 'WobblyCat' effect. | 1 |
| `Wood` | Variable |  | 1 |
| `XIsConsumedCharacterMaxHP` | Integer | Applies or references the 'XIsConsumedCharacterMaxHP' effect/state. | 1 |
| `XIsCountDeaths` | Integer | Applies or references the 'XIsCountDeaths' effect/state. | 1 |
| [`XIsCountStatusStacks`](./Enums.md#enum-xiscountstatusstacks) | Enum | Applies or references the 'XIsCountStatusStacks' effect/state. | 1 |
| [`XIsFormulaLockedUntilComplete`](./Enums.md#enum-xisformulalockeduntilcomplete) | Enum | Applies or references the 'XIsFormulaLockedUntilComplete' effect/state. | 1 |
| `XIsIncreaseEachTurn` | Integer | Applies or references the 'XIsIncreaseEachTurn' effect/state. | 1 |
| `XIsRampAndReset` | Integer | Applies or references the 'XIsRampAndReset' effect/state. | 1 |
| `XIsRecycleCostReduction` | Integer | Applies or references the 'XIsRecycleCostReduction' effect/state. | 1 |
| `zaratana` | Variable |  | 1 |
| `ZeroKnockbackDamage` | Integer | Applies or references the 'ZeroKnockbackDamage' effect/state. | 1 |
| [`{Damaging Keys}`](./Engine_DamagingKeys.md#valid-property-keys) | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |
| [`{Event Keys}`](./Engine_EventKeys.md#valid-property-keys) | Object | Properties for configuring event outcomes (rewards, penalties, dialog options, status applications). Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |
| [`{Logic Keys}`](./Engine_LogicKeys.md#valid-property-keys) | Object | Properties for conditional execution, status effect logic, and execution flow control. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 0 |

| `AddDamageToElementDamage` | Object | Applies or references the 'AddDamageToElementDamage' effect/state. | 0 |
| `AddLeechesStatus` | Number | Applies or references the 'AddLeechesStatus' effect/state. | 0 |
| `AddStatusesIfPersistentWeatherElement` | Object | Applies the 'AddStatusesIfPersistentWeatherElement' effect. | 0 |
| `AddStatusesToReceivedElementalDamage` | Object | Applies the 'AddStatusesToReceivedElementalDamage' effect. | 0 |
| `AddStatusToBasicAttack` | Object | Injects a status effect payload that applies whenever the character performs a basic attack. | 0 |
| `AddStatusToElementDamage` | Object | Applies the 'AddStatusToElementDamage' effect. | 0 |
| `AddStatusToTrampleDamage` | Object | Applies the 'AddStatusToTrampleDamage' effect. | 0 |
| `AddWeaponAux` | String | Applies or references the 'AddWeaponAux' effect/state. | 0 |
| `AllStatsUp` | Number | Applies or references the 'AllStatsUp' effect/state. | 0 |
| `AlphaCat` | Number | Applies or references the 'AlphaCat' effect/state. | 0 |
| `ApplyPassives` | Object | Grants the nested passive abilities dynamically. | 0 |
| `BigSplashDamage` | Integer | Applies the 'BigSplashDamage' effect. | 0 |
| `Bleed` | Number | Applies or references the 'Bleed' effect/state. | 0 |
| `Blind` | Array | Applies or references the 'Blind' effect/state. | 0 |
| `BloodRain` | Integer | Applies or references the 'BloodRain' effect/state. | 0 |
| `BonusCritChance` | Integer | Applies the 'BonusCritChance' effect. | 0 |
| `BonusDamage` | Number | Applies or references the 'BonusDamage' effect/state. | 0 |
| `BonusDamageBasedOnDistance` | Number | Applies or references the 'BonusDamageBasedOnDistance' effect/state. | 0 |
| `BonusKnockbackDamage` | Number | Applies or references the 'BonusKnockbackDamage' effect/state. | 0 |
| `BrittleCharismaUp` | Integer | Applies or references the 'BrittleCharismaUp' effect/state. | 0 |
| `BrittleConstitutionUp` | Integer | Applies or references the 'BrittleConstitutionUp' effect/state. | 0 |
| `BrittleDexterityUp` | Integer | Applies or references the 'BrittleDexterityUp' effect/state. | 0 |
| `BrittleIntelligenceUp` | Integer | Applies or references the 'BrittleIntelligenceUp' effect/state. | 0 |
| `BrittleLuckUp` | Integer | Applies or references the 'BrittleLuckUp' effect/state. | 0 |
| `BrittleSpeedUp` | Integer | Applies or references the 'BrittleSpeedUp' effect/state. | 0 |
| `BrittleStrengthUp` | Integer | Applies or references the 'BrittleStrengthUp' effect/state. | 0 |
| `Bruise` | Number | Applies or references the 'Bruise' effect/state. | 0 |
| `Burn` | Number | Applies or references the 'Burn' effect/state. | 0 |
| `CapDamage` | Number | Applies or references the 'CapDamage' effect/state. | 0 |
| `CaptureFamiliar` | Number | Applies or references the 'CaptureFamiliar' effect/state. | 0 |
| `ChanceToBreak` | Number | Applies or references the 'ChanceToBreak' effect/state. | 0 |
| `CharacterTypeGainsStatusAtBattleStart` | Object | Encounter Modifier: Applies a status effect to all characters of a specific type (e.g., Cats, Bosses) at the start of battle. | 0 |
| `Charge` | Number | Applies or references the 'Charge' effect/state. | 0 |
| `Charmed` | Array | Applies or references the 'Charmed' effect/state. | 0 |
| `Cleanse` | Number | Applies or references the 'Cleanse' effect/state. | 0 |
| `CompleteItemQuest` | Enum/String | Applies or references the 'CompleteItemQuest' effect/state. | 0 |
| `Conditional_HasStatus` | Object | Conditional trigger: Executes nested logic if the target currently has the specified status effect. | 0 |
| `Confusion` | Number | Applies or references the 'Confusion' effect/state. | 0 |
| `ConjureRandomAbilityFromCat` | Number | Applies or references the 'ConjureRandomAbilityFromCat' effect/state. | 0 |
| `CrackMoonHead` | Number | Applies or references the 'CrackMoonHead' effect/state. | 0 |
| `CurrentWeaponDamageUp` | Number | Applies or references the 'CurrentWeaponDamageUp' effect/state. | 0 |
| `DeleteObject` | Number | Applies or references the 'DeleteObject' effect/state. | 0 |
| `DestroyTrinket` | Number | Applies or references the 'DestroyTrinket' effect/state. | 0 |
| `Die` | Number | Applies or references the 'Die' effect/state. | 0 |
| `DieViolently` | Number | Applies or references the 'DieViolently' effect/state. | 0 |
| `DisableWeapon` | Number | Applies or references the 'DisableWeapon' effect/state. | 0 |
| `disallow_modifications` | Boolean | Prevents passives from altering this damage instance. | 0 |
| `DisplaceToAbilityTarget` | Number | Applies or references the 'DisplaceToAbilityTarget' effect/state. | 0 |
| `DisplaceTowardsSource` | Number | Applies or references the 'DisplaceTowardsSource' effect/state. | 0 |
| `DistanceBonusDamage` | Object | Applies the 'DistanceBonusDamage' effect. | 0 |
| `DivineShield` | Number | Applies or references the 'DivineShield' effect/state. | 0 |
| `DontHealEnemies` | Integer | Applies or references the 'DontHealEnemies' effect/state. | 0 |
| `Doomed` | Number | Applies or references the 'Doomed' effect/state. | 0 |
| `EmptyMana` | Integer | Applies the 'EmptyMana' effect. | 0 |
| `EventBounty` | Integer | Applies or references the 'EventBounty' effect/state. | 0 |
| `ExplodeCharacter` | Number | Applies or references the 'ExplodeCharacter' effect/state. | 0 |
| `ExplodeCharacter_NoDie` | Number | Applies or references the 'ExplodeCharacter_NoDie' effect/state. | 0 |
| `ExplodeCharacter_Party` | Number | Applies or references the 'ExplodeCharacter_Party' effect/state. | 0 |
| `ExplodeCharacter_PartyBoss` | Integer | Applies or references the 'ExplodeCharacter_PartyBoss' effect/state. | 0 |
| `ExplodeCharacter_RockCrusher` | Number | Applies or references the 'ExplodeCharacter_RockCrusher' effect/state. | 0 |
| `ExplodeCharacter_RockCrusher_PetrifyBreak` | Integer | Applies or references the 'ExplodeCharacter_RockCrusher_PetrifyBreak' effect/state. | 0 |
| `FaceAway` | Number | Applies or references the 'FaceAway' effect/state. | 0 |
| `FaceCamera` | Number | Applies or references the 'FaceCamera' effect/state. | 0 |
| `FactionConversion` | Number | Applies or references the 'FactionConversion' effect/state. | 0 |
| `Fear` | Array | Applies or references the 'Fear' effect/state. | 0 |
| `Fights` | Number | Applies or references the 'Fights' effect/state. | 0 |
| `FillMana` | Number | Applies or references the 'FillMana' effect/state. | 0 |
| `FlatAIBonus` | Number | Applies or references the 'FlatAIBonus' effect/state. | 0 |
| `FlatLeech` | Number | Applies or references the 'FlatLeech' effect/state. | 0 |
| `FloatingRockTrap` | Number | Applies or references the 'FloatingRockTrap' effect/state. | 0 |
| `ForceImmediateMove` | Number | Applies or references the 'ForceImmediateMove' effect/state. | 0 |
| `ForceMoveAway` | Integer | Applies or references the 'ForceMoveAway' effect/state. | 0 |
| `ForceMoveTowards` | Number | Applies or references the 'ForceMoveTowards' effect/state. | 0 |
| `ForceUseAbility_NonStack` | Enum/String | Applies or references the 'ForceUseAbility_NonStack' effect/state. | 0 |
| `ForceUseAbilityOnTarget` | Object | Applies or references the 'ForceUseAbilityOnTarget' effect/state. | 0 |
| `FullHeal` | Number | Applies or references the 'FullHeal' effect/state. | 0 |
| `GainDisorder` | Enum/String | Applies or references the 'GainDisorder' effect/state. | 0 |
| `GainDisorderFromPool_PostCast` | Enum/String | Applies or references the 'GainDisorderFromPool_PostCast' effect/state. | 0 |
| `GenericDebuff` | Number | Applies or references the 'GenericDebuff' effect/state. | 0 |
| `HealRandomInjury` | Integer | Applies or references the 'HealRandomInjury' effect/state. | 0 |
| `HealthGain` | Number | Applies or references the 'HealthGain' effect/state. | 0 |
| `IgnoreDamage` | Number | Applies or references the 'IgnoreDamage' effect/state. | 0 |
| `ImmediateUseAbility` | Enum/String | Applies or references the 'ImmediateUseAbility' effect/state. | 0 |
| `ImmediateUseAbility_Instant` | Enum | Applies or references the 'ImmediateUseAbility_Instant' effect/state. | 0 |
| `Immobile` | Number | Applies or references the 'Immobile' effect/state. | 0 |
| `Imprison` | Enum/String | Applies or references the 'Imprison' effect/state. | 0 |
| `InnateElement` | Enum | Applies the 'InnateElement' effect. | 0 |
| `Instakill` | Number | Applies or references the 'Instakill' effect/state. | 0 |
| `KnockbackIfCrit` | Object | Applies or references the 'KnockbackIfCrit' effect/state. | 0 |
| `KnockOutClone` | Enum/String | Applies or references the 'KnockOutClone' effect/state. | 0 |
| `LaunchOffScreen` | Equation | Applies or references the 'LaunchOffScreen' effect/state. | 0 |
| `LaunchOffScreenInstakill` | Integer | Applies or references the 'LaunchOffScreenInstakill' effect/state. | 0 |
| `LeaveBehindRockOnKnockback` | Number | Applies or references the 'LeaveBehindRockOnKnockback' effect/state. | 0 |
| `Leech` | Number | Applies or references the 'Leech' effect/state. | 0 |
| `LeechPercent` | Integer | Applies the 'LeechPercent' effect. | 0 |
| `Madness` | Number | Applies the Madness debuff/status effect. | 0 |
| `ManaGain` | Number | Applies or references the 'ManaGain' effect/state. | 0 |
| `Marked` | Array | Applies or references the 'Marked' effect/state. | 0 |
| `NonLethal` | Integer | Applies the 'NonLethal' effect. | 0 |
| `OverrideDamage` | Number | Applies or references the 'OverrideDamage' effect/state. | 0 |
| `passives` | Array | List of {Status and Passive Keys}. | 0 |
| `PermanentCharm` | Integer | Applies the 'PermanentCharm' effect. | 0 |
| `PermanentDexterity` | Number | Applies or references the 'PermanentDexterity' effect/state. | 0 |
| `PreEmptiveCounterNextAttacks` | Integer | Applies or references the 'PreEmptiveCounterNextAttacks' effect/state. | 0 |
| `PurgeAll` | Number | Applies or references the 'PurgeAll' effect/state. | 0 |
| `RandomBonusDamage` | Number | Applies or references the 'RandomBonusDamage' effect/state. | 0 |
| `RandomStatDown` | String | Applies or references the 'RandomStatDown' effect/state. | 0 |
| `RandomStatUp` | Number | Applies or references the 'RandomStatUp' effect/state. | 0 |
| `RandomStatusFromPool` | Object | Selects and applies a random status effect from the provided nested block. | 0 |
| `RefreshActPoints` | Number | Applies or references the 'RefreshActPoints' effect/state. | 0 |
| `RefreshMovePoints` | Number | Applies or references the 'RefreshMovePoints' effect/state. | 0 |
| `RefreshWeaponAbility` | Number | Applies or references the 'RefreshWeaponAbility' effect/state. | 0 |
| `RemoteFlatLeech` | Integer | Applies or references the 'RemoteFlatLeech' effect/state. | 0 |
| `RemoteLeech` | Integer | Applies or references the 'RemoteLeech' effect/state. | 0 |
| `RemoveAmbientLightEffects` | Float | Applies or references the 'RemoveAmbientLightEffects' effect/state. | 0 |
| `RemoveGlobalModifiers` | Array | Applies or references the 'RemoveGlobalModifiers' effect/state. | 0 |
| `RemoveItem` | Enum/String | Applies or references the 'RemoveItem' effect/state. | 0 |
| `RemoveKnockback` | Number | Applies or references the 'RemoveKnockback' effect/state. | 0 |
| `RemoveMovePoints` | Number | Applies or references the 'RemoveMovePoints' effect/state. | 0 |
| `RemoveStatus` | Enum/String | Applies or references the 'RemoveStatus' effect/state. | 0 |
| `RemoveStatusStacks` | Object | Removes a specific number of stacks of a status effect. | 0 |
| `RemoveTurnsThisRound` | Number | Applies or references the 'RemoveTurnsThisRound' effect/state. | 0 |
| `RepairWeapon` | Number | Applies or references the 'RepairWeapon' effect/state. | 0 |
| `Revive` | Number | Applies or references the 'Revive' effect/state. | 0 |
| `Rot` | Array | Applies or references the 'Rot' effect/state. | 0 |
| `ScatterRandomPickups` | Number | Applies or references the 'ScatterRandomPickups' effect/state. | 0 |
| `SetHealth` | Number | Applies or references the 'SetHealth' effect/state. | 0 |
| `SetItemAux` | Object | Applies or references the 'SetItemAux' effect/state. | 0 |
| `SetKnockback` | Number | Applies or references the 'SetKnockback' effect/state. | 0 |
| `SetShield` | Number | Applies or references the 'SetShield' effect/state. | 0 |
| `Shield` | Number | Applies or references the 'Shield' effect/state. | 0 |
| `ShowFakeDamage` | Object | Displays a visual damage number without actually modifying health. | 0 |
| `ShowText` | String | Applies or references the 'ShowText' effect/state. | 0 |
| `Slow` | Array | Applies or references the 'Slow' effect/state. | 0 |
| `SpawnBearTrap` | Number | Applies or references the 'SpawnBearTrap' effect/state. | 0 |
| `SpawnBearTrapIfHitKills` | Number | Applies or references the 'SpawnBearTrapIfHitKills' effect/state. | 0 |
| `SpawnBearTrapOnMiss` | Integer | Applies the 'SpawnBearTrapOnMiss' effect. | 0 |
| `SpawnFlames` | `Array` | Applies or references the 'SpawnFlames' effect/state. | 0 |
| `SpawnThingIfHitKills` | Enum/String | Applies or references the 'SpawnThingIfHitKills' effect/state. | 0 |
| `SpecificInjury` | Enum/String | Applies or references the 'SpecificInjury' effect/state. | 0 |
| `SpeculativeMoveSelfCorpseOffMap` | Number | Applies or references the 'SpeculativeMoveSelfCorpseOffMap' effect/state. | 0 |
| `SpeedUp` | Number | Applies or references the 'SpeedUp' effect/state. | 0 |
| `SpeedUp_WithoutInitiative` | Integer | Applies or references the 'SpeedUp_WithoutInitiative' effect/state. | 0 |
| `StackingSandstorm` | Number | Applies or references the 'StackingSandstorm' effect/state. | 0 |
| `StanceSwitchToMelee` | Number | Applies or references the 'StanceSwitchToMelee' effect/state. | 0 |
| `StanceSwitchToRanged` | Number | Applies or references the 'StanceSwitchToRanged' effect/state. | 0 |
| `status` | Enum/String | The status effect to apply. | 0 |
| `StatusEachRoundEnd` | Object | Applies or references the 'StatusEachRoundEnd' effect/state. | 0 |
| `StatusImmunity` | Enum | Applies or references the 'StatusImmunity' effect/state. | 0 |
| `StatusRandomEnemiesOnBattleStart` | Object | Applies or references the 'StatusRandomEnemiesOnBattleStart' effect/state. | 0 |
| `StrengthUp` | Number | Applies or references the 'StrengthUp' effect/state. | 0 |
| `Stun` | Array | Applies or references the 'Stun' effect/state. | 0 |
| `T2CopyCat` | Number | Applies or references the 'T2CopyCat' effect/state. | 0 |
| `TakeExtraTurn` | Number | Applies or references the 'TakeExtraTurn' effect/state. | 0 |
| `TempDexterityUp` | Enum | Applies or references the 'TempDexterityUp' effect/state. | 0 |
| `TempLuckUp` | Integer | Applies or references the 'TempLuckUp' effect/state. | 0 |
| `Temporary` | Object | A wrapper object for applying status effects that automatically expire. | 0 |
| `TempPassiveUntilSettled` | Object | Passive: Active only until the physics engine stops moving the character. | 0 |
| `TempPassiveWhileHasStatus` | Object | Grants nested passives only while the character possesses the specified status. | 0 |
| `TempStrengthUp` | Equation | Applies or references the 'TempStrengthUp' effect/state. | 0 |
| `TempTrampleUntilSettled` | Number | Applies or references the 'TempTrampleUntilSettled' effect/state. | 0 |
| `Trample` | Number | Applies or references the 'Trample' effect/state. | 0 |
| `UseAbility_Madness` | Enum | Applies the 'UseAbility_Madness' effect. | 0 |
| `UseAbility_NonStack` | Enum | Applies or references the 'UseAbility_NonStack' effect/state. | 0 |
| `Vaporize` | Number | Applies or references the 'Vaporize' effect/state. | 0 |
| `VaporizeCorpse` | Number | Applies or references the 'VaporizeCorpse' effect/state. | 0 |
| `VaporizeCorpseFlipAdvantage` | `Array` | Applies or references the 'VaporizeCorpseFlipAdvantage' effect/state. | 0 |
| `VaporizeInanimate` | Number | Applies or references the 'VaporizeInanimate' effect/state. | 0 |
| `VisualFX` | Enum/String | Applies or references the 'VisualFX' effect/state. | 0 |
| `Weakness` | Array | Applies or references the 'Weakness' effect/state. | 0 |
| `WeaponAuxMultiplier` | Enum/String | Applies or references the 'WeaponAuxMultiplier' effect/state. | 0 |
</details>

### Valid Nested Objects

The following objects all behave as `{Status and Passive Keys}` containers. Each has its own unique parameters listed below its entry.

---

#### `AddPassivesToCharmed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 10 |

</details>

---

#### `AddPassivesToMinions`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 36

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 44 |
| [`tag_filter`](./Enums.md#enum-tag_filter) | Enum | Examples: `crow, grub_familiar` | 3 |

</details>

---

#### `AddSelfStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 10 |

</details>

---

#### `AddSelfStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
  | `ChanceToBreak` | Number | Applies or references the 'ChanceToBreak' effect/state. | 0 |
  | [`RepairWeapon`](./Arrays.md#array-repairweapon) | Number | Applies or references the 'RepairWeapon' effect/state. | 0 |

</details>

---

#### `AddStatusToAllDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 16 |
| [`Conditional_HasStatus`](#conditional_hasstatus) | Object | Nested conditional. | 3 |
| [`Conditional_HasTag`](#conditional_hastag) | Object | Nested conditional. | 3 |
| `must_do_damage` | Boolean | `true` | 3 |
  | [`KnockbackIfCrit`](#knockbackifcrit) | Object | Applies or references the 'KnockbackIfCrit' effect/state. | 0 |
  | `LeaveBehindRockOnKnockback` | Number | Applies or references the 'LeaveBehindRockOnKnockback' effect/state. | 0 |
  | [`Blind`](./Arrays.md#array-blind) | Array | Applies or references the 'Blind' effect/state. | 0 |
  | `NonLethal` | Integer | Applies the 'NonLethal' effect. | 0 |
  | [`Rot`](./Arrays.md#array-rot) | Array | Applies or references the 'Rot' effect/state. | 0 |
  | `BonusKnockbackDamage` | Number | Applies or references the 'BonusKnockbackDamage' effect/state. | 0 |

</details>

---

#### `AddStatusToBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 248

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 187 |
| [`Conditional_Ally`](#conditional_ally) | Object | Nested conditional. | 5 |
| [`Conditional_Enemy`](#conditional_enemy) | Object | Nested conditional. | 3 |
| [`Conditional_GoodRoll`](#conditional_goodroll) | Object | Nested conditional. | 3 |
| [`Conditional_Adjacent`](#conditional_adjacent) | Object | Nested conditional. | 2 |
| [`Conditional_Shielded`](#conditional_shielded) | Object | Nested conditional. | 2 |
| [`Conditional_HasTag`](#conditional_hastag) | Object | Nested conditional. | 1 |
| [`Conditional_SourceHasTag`](#conditional_sourcehastag) | Object | Nested conditional. | 1 |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |

</details>

---

#### `AddStatusToBasicMeleeAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 10 |

</details>

---

#### `AddStatusToElementDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 8 |
| [`Conditional_Corpse`](#conditional_corpse) | Object | Nested conditional. | 2 |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type required or applied. | 1 |
  | [`AddDamageToElementDamage`](#adddamagetoelementdamage) | Object | Applies or references the 'AddDamageToElementDamage' effect/state. | 0 |

</details>

---

#### `AddStatusToKnockbackDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
  | [`Stun`](./Arrays.md#array-stun) | Array | Applies or references the 'Stun' effect/state. | 0 |
  | `Bruise` | Number | Applies or references the 'Bruise' effect/state. | 0 |

</details>

---

#### `AddStatusToSpells`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| [`Conditional_Enemy`](#conditional_enemy) | Object | Nested conditional. | 1 |
  | `Leech` | Number | Applies or references the 'Leech' effect/state. | 0 |
  | `LeechPercent` | Integer | Applies the 'LeechPercent' effect. | 0 |

</details>

---

#### `AddStatusToTrampleDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
  | `Cleave` | Object | Causes the attack to hit adjacent enemies alongside the primary target. | 0 |
  | `Bruise` | Number | Applies or references the 'Bruise' effect/state. | 0 |

</details>

---

#### `AddStatusToWeapons`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 5 |

</details>

---

#### `AdventureTokenPassivePool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 1

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 12 |

</details>

---

#### `ApplyPassives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 13 |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |

</details>

---

#### `ApplyStatusIfCrit`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 8 |

</details>

---

#### `ApplyStatusesToRandomEnemiesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 4 |
| [`count`](./Arrays.md#array-count) | Integer | Quantity. | 3 |

</details>

---

#### `CatchProjectiles`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 6 |
| `ally_chance` | Integer | Examples: `15, 100` | 5 |
| [`chance`](./Enums.md#enum-chance) | Float | Probability (0.0 to 1.0 or percentage) of this occurring. | 1 |

</details>

---

#### `CharacterTypeGainsStatusAtBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`tag`](./Enums.md#enum-tag) | Enum | Specific entity tag required. | 981 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 8 |
| [`Conditional_Flying`](#conditional_flying) | Object | Nested conditional. | 1 |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |

</details>

---

#### `CritsApplyStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 12

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 12 |
| [`Conditional_HasStatus`](#conditional_hasstatus) | Object | Nested conditional. | 2 |

</details>

---

#### `ExtraStatusWhenDealingDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_PartyMember`](#conditional_partymember) | Object | Nested conditional. | 3 |
| [`Conditional_Ally`](#conditional_ally) | Object | Nested conditional. | 2 |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |

</details>

---

#### `MeleeRevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 73

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 75 |
| [`effects`](#effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 62 |
| [`type`](./Enums.md#enum-type) | Enum | Classification/category type. | 54 |
| `knockback` | Integer | The base physics pushing power (in tiles). | 24 |
| [`damage`](./Arrays.md#array-damage) | Integer | The base damage properties of an attack. | 2 |
| `cant_miss` | Boolean | Guarantees the hit, bypassing dodge mechanics. | 1 |
| [`elements`](./Arrays.md#array-elements) | Array | Array of elemental tags to apply (e.g., `[Fire Holy]`). | 0 |
  | [`AddDamageToElementDamage`](#adddamagetoelementdamage) | Object | Applies or references the 'AddDamageToElementDamage' effect/state. | 0 |
  | [`AddStatusToElementDamage`](#addstatustoelementdamage) | Object | Applies the 'AddStatusToElementDamage' effect. | 0 |
  | [`InnateElement`](./Enums.md#enum-innateelement) | Enum | Applies the 'InnateElement' effect. | 0 |
  | [`StatusImmunity`](./Enums.md#enum-statusimmunity) | Enum | Applies or references the 'StatusImmunity' effect/state. | 0 |

</details>

---

#### `PassiveAfterXKills`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#passives) | Object | Passives granted by equipping this. | 5118 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 8 |
| `stacks` | Integer | Number of stacks or intensity to apply. | 4 |

</details>

---

#### `PassiveAtHealthThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#passives) | Object | Passives granted by equipping this. | 5118 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 16 |
| [`mode`](./Enums.md#enum-mode) | Enum | `equal`, `greater`, `greater_or_equal`, `less_or_equal`, `yeet` | 9 |
| `threshold` | Integer | Examples: `4*champion_multiplier, 3*champion_multiplier, 1` | 9 |

</details>

---

#### `PassiveAtStatThreshold`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 13

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#passives) | Object | Examples: `{ ... }` | 5118 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 33 |
| [`mode`](./Enums.md#enum-mode) | Enum | `equal`, `greater`, `greater_or_equal`, `less_or_equal`, `yeet` | 13 |
| [`threshold`](#threshold) | Object | Examples: `4*champion_multiplier, 3*champion_multiplier, 1` | 13 |

</details>

---

#### `PassiveGroup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 14 |

</details>

---

#### `PassiveWhenAffectedByElement`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 18

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#passives) | Object | Examples: `{ ... }` | 5118 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 33 |
| [`element`](./Enums.md#enum-element) | Enum | The specific element type to check for. | 1 |

</details>

---

#### `PassiveWhenAtFullMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 5 |

</details>

---

#### `PassiveWhenDead`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 2 |
  | [`StatusEachRoundEnd`](#statuseachroundend) | Object | Applies or references the 'StatusEachRoundEnd' effect/state. | 0 |
  | [`StatusEachTurnBegin`](#statuseachturnbegin) | Object | Event Trigger: Applies nested statuses to each turn begin. | 0 |
  | [`AddStatusToTrampleDamage`](#addstatustotrampledamage) | Object | Applies the 'AddStatusToTrampleDamage' effect. | 0 |
  | [`AutocastEachRound`](#autocasteachround) | Object | Forces the character to automatically cast a specific ability at the start of each combat round. | 0 |

</details>

---

#### `PassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`passives`](#passives) | Object | Object listing intrinsic passive modifiers. | 5118 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 11 |
| [`status`](./Enums.md#enum-status) | Enum | ID of the status effect to apply or check. | 6 |

</details>

---

#### `PassiveWhileInMonkMeleeStance`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 3 |

</details>

---

#### `RandomPassivePool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 26 |

</details>

---

#### `RandomStatusFromPool`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 35

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 35 |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |

</details>

---

#### `RevengeDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 31

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`effects`](#effects) | Object | Non-damaging status applications and logic triggers executed on impact. | 62 |
| [`type`](./Enums.md#enum-type) | Enum | The classification of damage (`melee`, `ranged`, `spell`, `trample`, `knockblock`, `spawn`). | 54 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 17 |
| `knockback` | Integer | The base physics pushing power (in tiles). | 3 |
| [`damage`](./Arrays.md#array-damage) | Integer | The base damage properties of an attack. | 2 |
| [`elements`](./Arrays.md#array-elements) | Array | Array of elemental tags to apply (e.g., `[Fire Holy]`). | 0 |

</details>

---

#### `StatusAfterCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 1 |

</details>

---

#### `StatusAfterXTurns`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `stacks` | Integer | Number of stacks or intensity to apply. | 2 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 2 |

</details>

---

#### `StatusAllCharactersOnSpawn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 3 |
| [`Conditional_Boss`](#conditional_boss) | Object | Nested conditional. | 2 |
| [`Conditional_PartyMember`](#conditional_partymember) | Object | Nested conditional. | 1 |
| [`Conditional_Tiny`](#conditional_tiny) | Object | Nested conditional. | 1 |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |

</details>

---

#### `StatusAlliesEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_Adjacent`](#conditional_adjacent) | Object | Nested conditional. | 1 |
| `exclude_self` | Boolean | `false` | 1 |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
  | `RandomStatUp` | Number | Applies or references the 'RandomStatUp' effect/state. | 0 |

</details>

---

#### `StatusAlliesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 9 |

</details>

---

#### `StatusAlliesOnDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 8 |
| `triggers_limit` | Integer | Examples: `1` | 2 |

</details>

---

#### `StatusEachRoundEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 2 |

</details>

---

#### `StatusEachTurnBegin`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 27

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 11 |
| [`Conditional_BadRoll`](#conditional_badroll) | Object | Nested conditional. | 5 |
| [`Conditional_GoodRoll`](#conditional_goodroll) | Object | Nested conditional. | 1 |

</details>

---

#### `StatusEachTurnEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 57

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 55 |
| [`Conditional_GoodRoll`](#conditional_goodroll) | Object | Nested conditional. | 2 |
| [`Conditional_BadRoll`](#conditional_badroll) | Object | Nested conditional. | 1 |
| [`Conditional_HasCleansableDebuffs`](#conditional_hascleansabledebuffs) | Object | Nested conditional. | 1 |
| [`Conditional_ManaThreshold`](#conditional_manathreshold) | Object | Nested conditional. | 1 |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |

</details>

---

#### `StatusEachTurnEndForEachTurn`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 4 |

</details>

---

#### `StatusEveryXSpellCasts`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 9 |
| `stacks` | Integer | Number of stacks or intensity to apply. | 8 |

</details>

---

#### `StatusGroup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 6 |

</details>

---

#### `StatusIfUnusedMovePoints`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 8 |

</details>

---

#### `StatusKilledCharacters`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`Conditional_RandomChance`](#conditional_randomchance) | Object | Nested conditional. | 2 |
| [`Conditional_Ally`](#conditional_ally) | Object | Nested conditional. | 1 |
| `{Status and Passive Keys}` | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |
  | `AutoReanimate` | Number | Examples: `50` | 0 |

</details>

---

#### `StatusKillers`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 3 |
| [`Conditional_Boss`](#conditional_boss) | Object | Nested conditional. | 2 |
| [`Conditional_NotBoss`](#conditional_notboss) | Object | Nested conditional. | 2 |
  | [`Confusion`](./Arrays.md#array-confusion) | Number | Applies or references the 'Confusion' effect/state. | 0 |

</details>

---

#### `StatusOnAllyCatDeath`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 6 |

</details>

---

#### `StatusOnBattleEnd`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 53

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 58 |
| `even_if_dead` | Boolean | If true, triggers the effect even if the character died during the battle. | 25 |
| [`Conditional_GoodRoll`](#conditional_goodroll) | Object | Nested conditional. | 6 |
| [`Conditional_Corpse`](#conditional_corpse) | Object | Nested conditional. | 1 |
| [`Conditional_Shielded`](#conditional_shielded) | Object | Nested conditional. | 1 |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |

</details>

---

#### `StatusOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 16

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 11 |

</details>

---

#### `StatusOnBreak`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 22

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 15 |

</details>

---

#### `StatusOnBreakItem`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 4 |

</details>

---

#### `StatusOnCastSpell`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 8

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 8 |

</details>

---

#### `StatusOnCollectPickup`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 1 |

</details>

---

#### `StatusOnDie`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 6 |
| [`Conditional_RandomChance`](#conditional_randomchance) | Object | Nested conditional. | 1 |

</details>

---

#### `StatusOnEatFood`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 6 |

</details>

---

#### `StatusOnEatPill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | In addition to the other properties in this table, other keys from the specified engine dictionary may or may not also be applicable in this object. | 1 |
  | [`AllStatsUp`](./Arrays.md#array-allstatsup) | Number | Applies or references the 'AllStatsUp' effect/state. | 0 |
  | [`RandomPermanentStatsDistinct`](#randompermanentstatsdistinct) | Object | Examples: `{ ... }` | 0 |

</details>

---

#### `StatusOnEndMove`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 10

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 9 |
| [`Conditional_FirstApplicationThisTurn`](#conditional_firstapplicationthisturn) | Object | Nested conditional. | 1 |
| [`Conditional_GoodRoll`](#conditional_goodroll) | Object | Nested conditional. | 1 |
  | `RemoveStatusStacks` | Object | Removes a specific number of stacks of a status effect. | 0 |
  | [`DivineShield`](./Arrays.md#array-divineshield) | Number | Applies or references the 'DivineShield' effect/state. | 0 |
  | [`ImmediateUseAbility`](./Enums.md#enum-immediateuseability) | Enum | Applies or references the 'ImmediateUseAbility' effect/state. | 0 |
  | `Charge` | Number | Applies or references the 'Charge' effect/state. | 0 |
  | `SpeedUp_WithoutInitiative` | Integer | Applies or references the 'SpeedUp_WithoutInitiative' effect/state. | 0 |
  | `ForceAttack` | Object | Forces the character to execute an immediate attack. | 0 |
  | `SpeedUp` | Number | Applies or references the 'SpeedUp' effect/state. | 0 |

</details>

---

#### `StatusOnGainCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 6

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 5 |

</details>

---

#### `StatusOnHealed`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 4 |

</details>

---

#### `StatusOnKill`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 40

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `{Status and Passive Keys}` | Variable | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 36 |
| [`Conditional_GoodRoll`](#conditional_goodroll) | Object | Nested conditional. | 4 |
| [`Conditional_FirstApplicationThisTurn`](#conditional_firstapplicationthisturn) | Object | Nested conditional. | 2 |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |
  | `BrittleCharismaUp` | Integer | Applies or references the 'BrittleCharismaUp' effect/state. | 0 |
  | `BrittleConstitutionUp` | Integer | Applies or references the 'BrittleConstitutionUp' effect/state. | 0 |
  | `BrittleDexterityUp` | Integer | Applies or references the 'BrittleDexterityUp' effect/state. | 0 |
  | `BrittleIntelligenceUp` | Integer | Applies or references the 'BrittleIntelligenceUp' effect/state. | 0 |
  | `BrittleLuckUp` | Integer | Applies or references the 'BrittleLuckUp' effect/state. | 0 |
  | `BrittleSpeedUp` | Integer | Applies or references the 'BrittleSpeedUp' effect/state. | 0 |
  | `BrittleStrengthUp` | Integer | Applies or references the 'BrittleStrengthUp' effect/state. | 0 |
  | [`UseAbility_NonStack`](./Enums.md#enum-useability_nonstack) | Enum | Applies or references the 'UseAbility_NonStack' effect/state. | 0 |

</details>

---

#### `StatusOnKillEnemy`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 11

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 11 |

</details>

---

#### `StatusOnPickupCoins`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 3 |

</details>

---

#### `StatusOnPopCorpse`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 5 |

</details>

---

#### `StatusOnTookDamage`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 46

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 40 |
| [`Conditional_HasStatus`](#conditional_hasstatus) | Object | Nested conditional. | 2 |
| [`Conditional_HealthThreshold`](#conditional_healththreshold) | Object | Nested conditional. | 1 |

</details>

---

#### `StatusOnTookDamageFromAbility`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 9

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 8 |

</details>

---

#### `StatusOnUseBasicAttack`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 3 |

</details>

---

#### `StatusRandomEnemiesOnBattleStart`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 7

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 7 |
| [`count`](./Arrays.md#array-count) | Integer | Quantity. | 3 |

</details>

---

#### `StatusWhenAllySpendsMana`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 3 |

</details>

---

#### `TakeBonusTurnWithAIControl`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 3

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| `include_spells` | Boolean | If true, allows the AI to cast spells during this bonus turn. | 3 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 3 |
| `end_of_round` | Boolean | `true` | 1 |

</details>

---

#### `TakeBonusTurnWithStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 5

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 5 |

</details>

---

#### `TempPassiveWhileHasStatus`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`status`](./Enums.md#enum-status) | Enum | The required status effect. | 3 |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 3 |

</details>

---

#### `additional_passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 20

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 20 |

</details>

---

#### `bonus_passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 138

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 126 |

</details>

---

#### `extra_statuses`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 4

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 4 |
| [`Conditional_HasTag`](#conditional_hastag) | Object | Nested conditional. | 1 |
| `{Damaging Keys}` | Object | Properties for configuring damage instances (base damage, knockback, elements, accuracy, on-hit effects). Keys from the specified Engine Dictionary may or may not also be applicable in this object. | 0 |

</details>

---

#### `party_status_next_fight`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 24

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 23 |

</details>

---

#### `passives`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 2805

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 2827 |

</details>

---

#### `self_status_next_fight`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 143

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 133 |

</details>

---

#### `statuses`

<details>
<summary><b>Expand</b></summary>

> **Total Count:** 14

| Key | Type | Definition | Count |
| :--- | :--- | :--- | :--- |
| [`{Status and Passive Keys}`](./Engine_StatusAndPassiveKeys.md#valid-property-keys) | Object | References to status effect IDs and passive modifier IDs for application or checking. Keys from the specified Engine Dictionary may or may not also be applicable in this object.| 8 |

</details>

