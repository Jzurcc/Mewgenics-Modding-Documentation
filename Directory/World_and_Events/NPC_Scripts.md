# World and Events/NPC Scripts Directory

## File: `beanies_gameending.gon`

### `states_and_transitions`
**Source:** `beanies_gameending.gon`  

```
states_and_transitions {
	states {
		idle ["idle"]
	}

	transitions {
	}
}
```

---

### `sequences`
**Source:** `beanies_gameending.gon`  

**Localization Strings:**
- `NPC_BEANIES_ENDING_1`: "[m:default]Now I know what you are thinking..."
- `NPC_BEANIES_ENDING_2`: "[m:happy]Wow, Dr. Beanies saved us! What a lovable hero!"
- `NPC_BEANIES_ENDING_3`: "[m:winking]Well I assure you, my actions were purely selfish."
- `NPC_BEANIES_ENDING_4`: "[m:shocked]I mean, I don't wanna die! That's insane!"
- `NPC_BEANIES_ENDING_5`: "You I could live without... but what about me!?"
- `NPC_BEANIES_ENDING_6`: "[m:angry]Weren't you at all thinking about how your actions might affect others?"
- `NPC_BEANIES_ENDING_7`: "[m:veryangry]I could have children out there!"
- `NPC_BEANIES_ENDING_8`: "[m:whispering]..."
- `NPC_BEANIES_ENDING_9`: "[m:default]Ok I'll admit it, you've been an adequate entry-level day laborer."
- `NPC_BEANIES_ENDING_10`: "Not saying you couldn't be replaced by literally any other corpse on Earth."
- `NPC_BEANIES_ENDING_11`: "[m:pondering]But I mean, if you are in need of some amount of praise..."
- `NPC_BEANIES_ENDING_12`: "[m:questioning]If you absolutely require someone else to validate your worth..."
- `NPC_BEANIES_ENDING_13`: "[m:happy]I guess I'd say you were..."
- `NPC_BEANIES_ENDING_14`: "[m:shocked]!!!"
- `NPC_BEANIES_ENDING_15`: "[m:scared]WHAT THE HELL WAS THAT!?"
- `NPC_BEANIES_ENDING_16`: "[m:angry]Wait, why aren't we moving?"
- `NPC_BEANIES_ENDING_17`: "I set this thing to bring us back right to when we met..."
- `NPC_BEANIES_ENDING_18`: "[m:pondering]Something appears to have damaged the antenna..."
- `NPC_BEANIES_ENDING_19`: "[m:veryhappy]Hold tight! <br/> I got this... <br/> I'M A DOCTOR!"

```
sequences {
	ending { //dr beanies talks to you after saving you in the time machine.
		dialog NPC_BEANIES_ENDING_1
		dialog NPC_BEANIES_ENDING_2
		dialog NPC_BEANIES_ENDING_3
		dialog NPC_BEANIES_ENDING_4
		dialog NPC_BEANIES_ENDING_5
		dialog NPC_BEANIES_ENDING_6
		dialog NPC_BEANIES_ENDING_7
		dialog NPC_BEANIES_ENDING_8
		dialog NPC_BEANIES_ENDING_9
		dialog NPC_BEANIES_ENDING_10
		dialog NPC_BEANIES_ENDING_11
		dialog NPC_BEANIES_ENDING_12
		dialog NPC_BEANIES_ENDING_13

		screenshake [1, 30]
		sfx BeaniesEnding_Banging

		dialog NPC_BEANIES_ENDING_14
		dialog NPC_BEANIES_ENDING_15
		dialog NPC_BEANIES_ENDING_16
		dialog NPC_BEANIES_ENDING_17
		dialog NPC_BEANIES_ENDING_18
		dialog NPC_BEANIES_ENDING_19
	}
}
```

---

## File: `beanies_gameintro.gon`

### `states_and_transitions`
**Source:** `beanies_gameintro.gon`  

```
states_and_transitions {
	states {
		verycloseup ["verycloseup"]
		closeup ["closeup"]
		choosecats ["choosecats"]
		zoomedout ["zoomedout"]
		closerup ["closerup"]
	}

	transitions {
	}
}
```

---

### `sequences`
**Source:** `beanies_gameintro.gon`  

**Localization Strings:**
- `NPC_BEANIES_INTRO_1`: "[m:veryhappy][s:1.5][b]Science!!![/b][/s]"
- `NPC_BEANIES_INTRO_2`: "[m:happy]Scared you didn't I?"
- `NPC_BEANIES_INTRO_3`: "[m:default]I know how scary a buzzword like science can be these days..."
- `NPC_BEANIES_INTRO_4`: "[m:happy]But trust me when I say, <br/> science can actually be a good thing sometimes."
- `NPC_BEANIES_INTRO_5`: "[m:default]Take this table for instance."
- `NPC_BEANIES_INTRO_6`: "A science made this table <br/> and the floor it sits on!"
- `NPC_BEANIES_INTRO_7`: "[m:whispering]There are even people out there who believe that a science made you and I!"
- `NPC_BEANIES_INTRO_8`: "[m:default]But I digress, <br/> the point I was trying to make here is that cats are a science too..."
- `NPC_BEANIES_INTRO_9`: "[m:winking]A science that I <br/> [b]Thomas A. Beanies[/b] <br/> invented!"
- `NPC_BEANIES_INTRO_10`: "[m:default]But what do you have to do with all of this?"
- `NPC_BEANIES_INTRO_11`: "[m:default]Well, word on the street is you're a bit of a felineologist yourself."
- `NPC_BEANIES_INTRO_12`: "[m:happy]I know we just met, but I bet if you and I put our brains together we could actually change the world!"
- `NPC_BEANIES_INTRO_13`: "[m:veryhappy][s:1.5][a:wave]WITH CATS![/a][/s]"
- `NPC_BEANIES_INTRO_14`: "[m:winking]Now take a gander at these fine specimens! <br/> This is my latest batch! Straight out of their biovats!"
- `NPC_BEANIES_INTRO_15`: "Choose two, <br/> a boy and a girl... <br/> Trust me you'll find out why later."
- `NPC_BEANIES_INTRO_16`: "[m:shocked]Uhh <br/> what's wrong with {Catname}?!"
- `NPC_BEANIES_INTRO_17`: "[m:bored]Wow, ok I didn't expect you to pass on the best of the bunch!"
- `NPC_BEANIES_INTRO_18`: "[m:default]Whatever, <br/> their pieces will be put to good use."
- `NPC_BEANIES_INTRO_19`: "[m:sad]Isn't nature just cruel..."
- `NPC_BEANIES_INTRO_20`: "[m:happy]But it doesn't have to be!"
- `NPC_BEANIES_INTRO_21`: "[m:pondering]In fact, I think with my brains and your ability to choose less than ideal cats..."
- `NPC_BEANIES_INTRO_22`: "[m:veryhappy]We could really shake things up!"
- `NPC_BEANIES_INTRO_23`: "[m:happy]Hell, with enough cats I bet we could reverse time! <br/> Maybe even make dying impossible!?"
- `NPC_BEANIES_INTRO_24`: "[m:pondering][s:.7]All I need is a nuke, <br/> radioactive blood <br/> and a bit of elbow grease...[/s]"
- `NPC_BEANIES_INTRO_25`: "[m:winking]Don't worry, <br/> I'll be sure to harvest some from {Catname's} elbows before {he's} incinerated."
- `NPC_BEANIES_INTRO_26`: "[m:happy][s:1.3]Now go, my child![/s]"
- `NPC_BEANIES_INTRO_27`: "[m:veryhappy][s:1.5]Go into the world and hoard some cats![/s]"

```
sequences {
	
	intro {
		set_state verycloseup
		delay 5.4
		dialog NPC_BEANIES_INTRO_1
		set_state closeup
		set_mood happy
		dialog NPC_BEANIES_INTRO_2
		dialog NPC_BEANIES_INTRO_3
		dialog NPC_BEANIES_INTRO_4
		set_state zoomedout
		set_mood default
		dialog NPC_BEANIES_INTRO_5 
		dialog NPC_BEANIES_INTRO_6
		dialog NPC_BEANIES_INTRO_7
		dialog NPC_BEANIES_INTRO_8
		dialog NPC_BEANIES_INTRO_9
		dialog NPC_BEANIES_INTRO_10
		dialog NPC_BEANIES_INTRO_11
		dialog NPC_BEANIES_INTRO_12
		set_state closeup
		set_mood veryhappy
		dialog NPC_BEANIES_INTRO_13
		set_state choosecats
		set_mood default
		dialog NPC_BEANIES_INTRO_14
		dialog_and_autopass NPC_BEANIES_INTRO_15
		unlock_controls 1
		wait_for choose_cat1
		wait_for choose_cat2
		lock_controls 1
		dialog NPC_BEANIES_INTRO_16
		dialog NPC_BEANIES_INTRO_17
		dialog NPC_BEANIES_INTRO_18
		sfx Intro_LabDisposal
		wait_for reject_cat
		delay .05
		set_state closeup
		set_mood sad
		dialog NPC_BEANIES_INTRO_19
		set_state zoomedout
		set_mood default
		dialog NPC_BEANIES_INTRO_20
		dialog NPC_BEANIES_INTRO_21
		dialog NPC_BEANIES_INTRO_22
		set_state closeup
		set_mood happy
		dialog NPC_BEANIES_INTRO_23
		set_state zoomedout
		set_mood pondering
		dialog NPC_BEANIES_INTRO_24
		dialog NPC_BEANIES_INTRO_25
		set_state closeup
		set_mood happy
		dialog NPC_BEANIES_INTRO_26
		dialog NPC_BEANIES_INTRO_27
	}

}
```

---

## File: `beanies_progression.gon`

### `states_and_transitions`
**Source:** `beanies_progression.gon`  

```
states_and_transitions {
	states {
		idle ["idle"]
		verycloseup ["verycloseup"]
		closeup ["closeup"]
		zoomedout ["zoomedout"]
	}

	transitions {
	}
}
```

---

### `sequences`
**Name:** after  
**Source:** `beanies_progression.gon`  

**Localization Strings:**
- `NPC_BEANIES_UNPROMPTED1_1`: "[m:angry]Who let you back here!? Leave!"
- `NPC_BEANIES_UNPROMPTED2_1`: "[m:veryangry]Where is your warrant!?"
- `NPC_BEANIES_UNPROMPTED2_2`: "[m:default]Oh, it's you... [m:angry]GO AWAY!"
- `NPC_BEANIES_UNPROMPTED3_1`: "[m:veryangry]I HAVE A GUN!"
- `NPC_BEANIES_UNPROMPTED3_2`: "[m:scared]Jesus, I thought you were a Nazi from the future..."
- `NPC_BEANIES_UNPROMPTED3_3`: "[m:angry]Leave..."
- `NPC_BEANIES_UNPROMPTED4_1`: "[m:angry]If I wanted you here I would have called you... Go back home."
- `NPC_BEANIES_UNPROMPTED5_1`: "[m:veryangry]I TOLD YOU ALREADY I HAVE NO IDEA WHERE THOSE KIDS ARE!"
- `NPC_BEANIES_UNPROMPTED5_2`: "[m:questioning]Oh... it's you. Please leave."
- `NPC_BEANIES_UNPROMPTED6_1`: "[m:happy]Like what you see? ... [m:shocked]Hey you aren't the girl from the photo!?"
- `NPC_BEANIES_UNPROMPTED6_2`: "[m:sad][s:.7]I knew it was too good to be true...[/s]"
- `NPC_BEANIES_UNPROMPTED6_3`: "[m:angry]Get out of my lab!"
- `NPC_BEANIES_ALSO_1`: "Also..."
- `NPC_BEANIES_BEANIES_BEGIN_ACCEPTING_CATS_1`: "[m:default]Hey, remember me? <br/> Dr. Beanies."
- `NPC_BEANIES_BEANIES_BEGIN_ACCEPTING_CATS_2`: "[m:questioning]The guy who brought you back to life and kick-started your cat hoarding career?"
- `NPC_BEANIES_BEANIES_BEGIN_ACCEPTING_CATS_3`: "[m:angry]The man who you owe your very existence to!? Remember!?"
- `NPC_BEANIES_BEANIES_BEGIN_ACCEPTING_CATS_4`: "[m:happy]Good, because it's time to pay the piper! <br/> See, I kinda need your help..."
- `NPC_BEANIES_BEANIES_BEGIN_ACCEPTING_CATS_5`: "[m:pondering]But I need some more science to get there..."
- `NPC_BEANIES_BEANIES_BEGIN_ACCEPTING_CATS_6`: "[m:questioning]Were you aware that cats with disorders or mutations also contain ungodly amounts of science?"
- `NPC_BEANIES_BEANIES_BEGIN_ACCEPTING_CATS_7`: "[m:happy]Well you are now! <br/> Send me a specimen like that and I may have a little "Side Quest" for ya..."
- `NPC_BEANIES_BEANIES_QUESTS_INTRO_1`: "[m:happy]Ok, check this out.. <br/> While I was condensing that cat you sent into grease... <br/> I had this amazing idea!"
- `NPC_BEANIES_BEANIES_QUESTS_INTRO_2`: "[m:veryhappy]IT'S A NEW INVENTION!"
- `NPC_BEANIES_BEANIES_QUESTS_INTRO_3`: "[m:mocking]And you are the perfect person to test it out!"
- `NPC_BEANIES_BEANIES_QUESTS_INTRO_4`: "[m:default]Take a look..."
- `NPC_BEANIES_BEANIES_QUESTS_REPEAT_1`: "[m:veryhappy]I'VE DONE IT AGAIN! A NEW INVENTION APPEARS!"
- `NPC_BEANIES_BEANIES_QUESTS_REPEAT_2`: "[m:veryhappy]This one will seriously change the world and make me a billionaire!"
- `NPC_BEANIES_BEANIES_QUESTS_REPEAT_3`: "[m:happy]Now listen up!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_PERSUASIONDEVICE_1`: "[m:happy]I call it, <br/> The [b]Persuasion Device![/b]"
- `NPC_BEANIES_BEANIESQUEST_INTRO_PERSUASIONDEVICE_2`: "[m:default]Simply smash something with it and that thing will believe you guys are best friends."
- `NPC_BEANIES_BEANIESQUEST_INTRO_PERSUASIONDEVICE_3`: "[m:scared]Do you remember it?..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_PERSUASIONDEVICE_4`: "[m:happy]Good! ... [m:pondering]What was I saying?"
- `NPC_BEANIES_BEANIESQUEST_INTRO_PERSUASIONDEVICE_5`: "[m:default]Oh yeah, so take the Persuasion Device and fiddle with it on an adventure."
- `NPC_BEANIES_BEANIESQUEST_INTRO_PERSUASIONDEVICE_6`: "Finish {questdestination} and when you are done just report back and we can go from there."
- `NPC_BEANIES_BEANIESQUEST_INTRO_PERSUASIONDEVICE_7`: "[m:happy]Godspeed!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSUASIONDEVICE_1`: "[m:veryhappy]The [b]Persuasion Device[/b] works! I'M A GENIUS!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSUASIONDEVICE_2`: "[m:default]I polished it up a bit and as a bonus you can keep it!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSUASIONDEVICE_3`: "Oh also, here's {questreward} coins for your time.[sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSUASIONDEVICE_4`: "[m:happy]There is more where that came from, just keep entertaining my morally grey requests!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSUASIONDEVICE_5`: "[m:default]Send more cats!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_PERSUASIONDEVICE_1`: "[m:angry]You lost the <br/> [b]Persuasion Device?![/b]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_PERSUASIONDEVICE_2`: "[m:veryangry]Do you have any idea how many skulls I had to crack to calibrate that thing!?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_PERSUASIONDEVICE_3`: "[m:angry]I got a damn UCL tear from all that manual bashing..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_PERSUASIONDEVICE_4`: "[m:veryangry]Do you have any clue how long those take to heal!!?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_PERSUASIONDEVICE_5`: "[m:angry][s:.7]I should have known someone like you would just screw it up...[/s]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_PERSUASIONDEVICE_6`: "[m:sad]But I'll be honest, I've burnt all my bridges, you are my only hope."
- `NPC_BEANIES_BEANIESQUEST_FAIL_PERSUASIONDEVICE_7`: "[m:sad]Send me more cats and I will try something else I guess..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_MAGICMIRROR_1`: "[m:veryhappy]I'VE DONE IT AGAIN!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_MAGICMIRROR_2`: "BEST INVENTION EVER!!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_MAGICMIRROR_3`: "[m:questioning]So you know that thing where if you break a mirror your family dies or whatever?"
- `NPC_BEANIES_BEANIESQUEST_INTRO_MAGICMIRROR_4`: "[m:happy]Its like that but with more science! I call it the MAGIC MIRROR!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_MAGICMIRROR_5`: "You wear it on your face and it just makes your life hell!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_MAGICMIRROR_6`: "[m:default]Pretty cool, huh?"
- `NPC_BEANIES_BEANIESQUEST_INTRO_MAGICMIRROR_7`: "So just pop it on a cat and then have them finish {questdestination}."
- `NPC_BEANIES_BEANIESQUEST_INTRO_MAGICMIRROR_8`: "[m:whispering][s:.7]Like that will ever happen...[/s]"
- `NPC_BEANIES_BEANIESQUEST_INTRO_MAGICMIRROR_9`: "[m:happy]Have fun!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MAGICMIRROR_1`: "[m:shocked]Wait, you did it?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MAGICMIRROR_2`: "[m:confused]Honestly I didn't think that was even possible..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MAGICMIRROR_3`: "[m:pondering]hmmm.. <br/> The mirror appears to have fixed itself."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MAGICMIRROR_4`: "[m:shocked]And a soul is trapped inside it!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MAGICMIRROR_5`: "[m:veryhappy]I'm a freakin' genius!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MAGICMIRROR_6`: "[m:default]well you can have it I guess. Oh yeah and the {questreward} coins too.[sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_MAGICMIRROR_1`: "[m:default]Yeah, well that was expected..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_MAGICMIRROR_2`: "[m:questioning]That's just how science is sometimes..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_MAGICMIRROR_3`: "[m:default]Listen, I'm not gonna bawl you out about a broken mirror..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_MAGICMIRROR_4`: "I got a ton more sticking into things in the back..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_MAGICMIRROR_5`: "[m:pondering]But let's try something different next time."
- `NPC_BEANIES_BEANIESQUEST_FAIL_MAGICMIRROR_6`: "[m:happy]Come back after you send more cats!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_CHAOSDEVICE_1`: "[m:happy]I GOT ANOTHER ONE!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_CHAOSDEVICE_2`: "This invention may be my best yet!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_CHAOSDEVICE_3`: "[m:default]I found these old knitting needles in your house before I revived you."
- `NPC_BEANIES_BEANIESQUEST_INTRO_CHAOSDEVICE_4`: "[m:pondering]I'm pretty sure if you stab these things into the right areas of a brain..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_CHAOSDEVICE_5`: "[m:default]The user can access past lives!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_CHAOSDEVICE_6`: "[m:questioning]It's currently just theoretical... but we all know I'm never wrong."
- `NPC_BEANIES_BEANIESQUEST_INTRO_CHAOSDEVICE_7`: "[m:default]Give it a test run. Just stab them in a cat's head and get them to finish {questdestination}."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_CHAOSDEVICE_1`: "[m:happy]So, how was it? <br/> Did the subject access their ancestor's ancient abilities?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_CHAOSDEVICE_2`: "[m:default]Told ya! <br/> Anyway I found a much cleaner set of needles and refined the item a bit."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_CHAOSDEVICE_3`: "Take it. Oh, and here are those {questreward} coins I promised![sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_CHAOSDEVICE_1`: "[m:angry]Well this sure as hell wasn't my fault!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_CHAOSDEVICE_2`: "Obviously you pushed the needles in too far or something..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_CHAOSDEVICE_3`: "[m:veryangry]And you better not report this to the county!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_CHAOSDEVICE_4`: "[m:paranoid]I'm already being monitored by the feds about my human cloning operation..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_CHAOSDEVICE_5`: "[m:shocked]..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_CHAOSDEVICE_6`: "[m:default]Whatever, I forgive you."
- `NPC_BEANIES_BEANIESQUEST_INTRO_MESTONE_1`: "[m:veryhappy]IT'S TIME TO UNVEIL THE "ME STONE!""
- `NPC_BEANIES_BEANIESQUEST_INTRO_MESTONE_2`: "[m:default]This invention will literally suck the successes of others and funnel it straight into the owner!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_MESTONE_3`: "[m:happy]Best part is, if everyone else is a failure, you look like an even bigger winner compared to them!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_MESTONE_4`: "[m:default]Go test it out. <br/> Uh, try taking it through {questdestination} this time."
- `NPC_BEANIES_BEANIESQUEST_INTRO_MESTONE_5`: "Let me know how it goes!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MESTONE_1`: "[m:default]Nice! <br/> Guess it all worked out fine."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MESTONE_2`: "[m:whispering]Now let me let you in on a little secret..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MESTONE_3`: "[m:paranoid]That stone not only removed the success of your other cats..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MESTONE_4`: "[m:happy]But it also drained their joy! It's all right there in the stone now!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MESTONE_5`: "[m:happy]Pretty clever huh?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MESTONE_6`: "[m:questioning]And by the looks of the stone, those cats are running on empty!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MESTONE_7`: "[m:default]Anyway, you can have it and the {questreward} coin reward.[sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_MESTONE_1`: "[m:angry]Well look who's back! <br/> It's the idiot! <br/> The idiot who can't even use a simple rock!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_MESTONE_2`: "[m:veryangry]SHAME! SHAME DOUBLE SHAME!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_MESTONE_3`: "NOW LEAVE!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_ANGRYFACE_1`: "[m:default]Check out this mask I made.  I've been working with paper mache in my downtime."
- `NPC_BEANIES_BEANIESQUEST_INTRO_ANGRYFACE_2`: "[m:pondering]Actually.. wanna test it out?"
- `NPC_BEANIES_BEANIESQUEST_INTRO_ANGRYFACE_3`: "[m:default]I drew an angry face on it, so obviously it will turn the cat that wears it into a total psycho."
- `NPC_BEANIES_BEANIESQUEST_INTRO_ANGRYFACE_4`: "If you can get the cat wearing it to the end of {questdestination}, I'll hook you up."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_ANGRYFACE_1`: "[m:happy]Very nice work! <br/> Look at us doing science together!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_ANGRYFACE_2`: "[m:default]But check this out, while you were gone I made another mask!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_ANGRYFACE_3`: "[m:happy]This time I did a happy face."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_ANGRYFACE_4`: "[m:winking]That is the emotion you feel when you make money."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_ANGRYFACE_5`: "[m:default]And speaking of, here are {questreward} pieces of pure joy![sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_ANGRYFACE_1`: "[m:shocked]Where is the mask?!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_ANGRYFACE_2`: "[m:veryangry]Do you know how long I spent on that thing!?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_ANGRYFACE_3`: "[m:angry]Those eyebrows took ages to get just right!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_ANGRYFACE_4`: "[m:veryangry]GAAAAH!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_FARTFACE_1`: "[m:happy]Fart Face!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_FARTFACE_2`: "Yep, <br/> I've invented "Fart Face"!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_FARTFACE_3`: "[m:default]It's a living human ass that you can graft over a cat's muzzle."
- `NPC_BEANIES_BEANIESQUEST_INTRO_FARTFACE_4`: "[m:mocking]...it's full of farts!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_FARTFACE_5`: "[m:veryhappy]HAHAHAHA!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_FARTFACE_6`: "[m:happy]It's so nasty, Stacy was dry heaving the whole night I was making it!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_FARTFACE_7`: "[m:default]Take it to the end of {questdestination}, it will be funny!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_FARTFACE_1`: "[m:veryhappy]HAHAHA!!!! <br/> You actually did it!?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_FARTFACE_2`: "[m:mocking]That was a joke! I didn't really expect you to do it..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_FARTFACE_3`: "[m:happy]Whatever, good work I guess?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_FARTFACE_4`: "[m:default]Here is {questreward} coins for your time.[sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_FARTFACE_5`: "And since you are so into posteriors, you can have this robo ass I designed."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_FARTFACE_6`: "[m:happy]I'm not using it anymore, it's all yours!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_FARTFACE_1`: "[m:happy]Hahaha! <br/> Well someone needs a class on social cues..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_FARTFACE_2`: "I was obviously joking about that little side quest..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_FARTFACE_3`: "[m:mocking]It was called Fart Face... <br/> How could you think I was serious?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_FARTFACE_4`: "[m:angry]I'm a scientist doing real science stuff, not some street walker with a fart fetish!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_SPIDERINJECTOR_1`: "[m:happy]INVENTION TIME!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_SPIDERINJECTOR_2`: "[m:questioning]You know those tiny spiders you've seen on adventures?"
- `NPC_BEANIES_BEANIESQUEST_INTRO_SPIDERINJECTOR_3`: "[m:default]I found a way to put them into a tube thing, that injects 'em straight into your brain!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_SPIDERINJECTOR_4`: "[m:pondering]My theory is you can gain super powers from their bites!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_SPIDERINJECTOR_5`: "[m:default]I got the idea from that guy that the kids go nuts for, he dresses in a costume and shoots sticky stuff..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_SPIDERINJECTOR_6`: "[m:pondering]What's his name again?... Something Jackson?"
- `NPC_BEANIES_BEANIESQUEST_INTRO_SPIDERINJECTOR_7`: "[m:default]Doesn't matter. Just at least finish {questdestination} so they have time to hatch!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_SPIDERINJECTOR_8`: "[m:happy]So excited about this one!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_SPIDERINJECTOR_1`: "[m:veryhappy]SUCCESS!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_SPIDERINJECTOR_2`: "[m:happy]You did great out there!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_SPIDERINJECTOR_3`: "[m:default]Your cats will all no doubt perish from infection, but it's for the betterment of humanity as a whole."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_SPIDERINJECTOR_4`: "Because now we know spiders living in your brain isn't a good thing."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_SPIDERINJECTOR_5`: "[m:pondering]Well I mean, it might work if it were fleas... Yeah, or maggots?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_SPIDERINJECTOR_6`: "[m:questioning]... <br/> Gotta find something to write this down on."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_SPIDERINJECTOR_7`: "[m:default]Oh, before you go here's {questreward} coins, and you can keep the brain spiders... <br/> They are on the house![sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_SPIDERINJECTOR_1`: "[m:angry]Damn it, now how will we know what spider bite brain infections will yield in the long term?!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_SPIDERINJECTOR_2`: "I'm starting to think this science stuff is just way over your head..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_SPIDERINJECTOR_3`: "[m:shocked]Are you even listening to me?!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_SPIDERINJECTOR_4`: "[m:angry]..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_SPIDERINJECTOR_5`: "You are lucky I installed that chip in your brain..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_SPIDERINJECTOR_6`: "Imagine if I just ate it instead, you'd be as dumb as dirt!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_SPIDERINJECTOR_7`: "[m:veryangry]GO!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_PARTYDETONATOR_1`: "[m:happy]Guess whose <br/> birthday it is?"
- `NPC_BEANIES_BEANIESQUEST_INTRO_PARTYDETONATOR_2`: "[m:veryhappy]STACY!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_PARTYDETONATOR_3`: "[m:pondering]Well technically <br/> Stacy 34284."
- `NPC_BEANIES_BEANIESQUEST_INTRO_PARTYDETONATOR_4`: "[m:default]The original Stacy was born on August 19th..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_PARTYDETONATOR_5`: "[m:sad]..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_PARTYDETONATOR_6`: "[m:confused]No, no... <br/> That is in the past... [m:happy]Today we celebrate!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_PARTYDETONATOR_7`: "See this device? I call it the "Party Detonator"!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_PARTYDETONATOR_8`: "It causes anything that is downed to explode into a festive poof of colored confetti!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_PARTYDETONATOR_9`: "[m:default]Bring the party all the way through {questdestination} then come back for some cake!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_PARTYDETONATOR_10`: "[m:happy]It's gonna be great!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTYDETONATOR_1`: "[m:veryhappy]Happy birthday dear Staaaaaccccccccy 34284!!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTYDETONATOR_2`: "Happy birthday to yoooooouuuuuu!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTYDETONATOR_3`: "[m:paranoid]Sorry, I already ate the cake. I had just assumed you'd fail this one."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTYDETONATOR_4`: "[m:default]But I still have those {questreward} coins I owe you.[sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTYDETONATOR_5`: "And I modded that detonator into something a bit more functional, you can have it too."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTYDETONATOR_6`: "[m:veryhappy]Now it's time to spank Stacy!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTYDETONATOR_7`: "[m:whispering]I've modified her DNA so technically she's somewhere around 136 years old."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTYDETONATOR_8`: "[m:sad]I doubt she will survive this... But traditions are traditions!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTYDETONATOR_9`: "[m:veryhappy]Let the spanking commence!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_PARTYDETONATOR_1`: "[m:veryangry]Well I hope you are happy!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_PARTYDETONATOR_2`: "You ruined Stacy 34284's birthday party!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_PARTYDETONATOR_3`: "[m:angry]She was so upset she crawled into a hole and died!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_PARTYDETONATOR_4`: "[m:veryangry]And that is on YOU my friend!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_PARTYDETONATOR_5`: "[m:shocked]..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_PARTYDETONATOR_6`: "Oh this thing? <br/> [m:happy]This is Stacy 36127 obviously."
- `NPC_BEANIES_BEANIESQUEST_FAIL_PARTYDETONATOR_7`: "[m:whispering]Her birthday isn't for a few days..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_AIRHORN_1`: "[m:pondering]So I'm testing a theory with this horn..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_AIRHORN_2`: "[m:default]My theory is, if you are constantly alerting the enemy to where you are..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_AIRHORN_3`: "[m:shocked]They will ambush and kill you faster!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_AIRHORN_4`: "[m:happy]It's just a theory mind you, we need it tested and proven so I can officially take credit for it."
- `NPC_BEANIES_BEANIESQUEST_INTRO_AIRHORN_5`: "[m:winking]So uh, here, take this air horn! It's audible for miles, and annoying as hell!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_AIRHORN_6`: "[m:happy]Oh, and make sure the cat with the horn survives!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1`: "[m:happy]I knew it! I knew my theory was correct!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2`: "[m:winking]You know I came up with that theory when I was screaming at Stacy 3265..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_3`: "[m:default]I was just unloading on her, my screeching was deafening."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_4`: "[m:shocked]Stacy 3146 was so annoyed she freakin' attacked me!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_5`: "[m:questioning]But how did she know where I was!?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_6`: "[m:happy]That's when I came up with the theory that sounds can alert others to your whereabouts!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_7`: "[m:winking]Pretty interesting right? Science is like that sometimes!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_8`: "[m:happy]Anyway, I'm having a very hard time hearing you right now because I've been working on a NEW air horn."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_9`: "[m:veryhappy]I call it the <br/> Super Airhorn!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_10`: "[m:happy]It's REALLY annoying! <br/> Here, take it.[sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_1`: "[m:shocked]They all died!?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_2`: "[m:pondering]Well my theory was correct then..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_3`: "[m:default]But if you can't return the air horn, I can't consider this theory solved."
- `NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_4`: "[m:questioning]I mean, how do I know you didn't just kill the cats yourself for the reward, right?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_5`: "[m:bored]Listen, I'm a scientist, <br/> We have rules."
- `NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_6`: "[m:angry]No fudging outcomes! <br/> All theories must be tested and proven!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_7`: "[m:pondering]We also have this other rule "First, do no harm"."
- `NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_8`: "[m:angry]But that one is very outdated, and pretty damn stupid in my opinion..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_9`: "[m:veryangry]Like, what if the whole point of my testing IS to do harm!?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_10`: "[m:angry]I didn't major in robotics to NOT make tiny robots that collect the genitals of living organisms!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_11`: "[m:veryangry]It's totally insane! <br/> Who even made that dumb rule up!? <br/> Some old dead man, that's who!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_12`: "[m:angry]I'm so pissed at you for screwing this up!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_13`: "You better get your shit together ASAP unless you wanna wake up tomorrow with missing genitals!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_NUCLEARKNIFE_1`: "[m:happy]Oh man this one's super cool!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_NUCLEARKNIFE_2`: "[m:questioning]You know how nuclear power works right? Well, I made a knife that converts time into pure atomic energy!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_NUCLEARKNIFE_3`: "[m:veryhappy]So you can just kick back and watch its power grow!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_NUCLEARKNIFE_4`: "[m:paranoid]... <br/> But listen, you gotta let it kill stuff or it will turn on you."
- `NPC_BEANIES_BEANIESQUEST_INTRO_NUCLEARKNIFE_5`: "[m:winking]Nuclear power is a fickle mistress. Only the souls of the living can calm her fury!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_NUCLEARKNIFE_6`: "[m:pondering]So make sure you feed it, or it will probably explode or something."
- `NPC_BEANIES_BEANIESQUEST_INTRO_NUCLEARKNIFE_7`: "[m:bored]... <br/> That's bad."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_NUCLEARKNIFE_1`: "[m:veryhappy]YESSS!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_NUCLEARKNIFE_2`: "[m:happy]Oh man, this invention will put us 50 years into the future!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_NUCLEARKNIFE_3`: "[m:pondering]I can hear it now, the Nobel Peace Prize goes to...."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_NUCLEARKNIFE_4`: "[m:veryangry][s:1.3]BOOM![/s] [s:1.1] <br/> Dead![/s] <br/> Everything dead!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_NUCLEARKNIFE_5`: "[m:veryhappy]Hahaha!! <br/> Hahaha!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_NUCLEARKNIFE_6`: "[m:happy]Sorry, I just can't get that visual out of my head..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_NUCLEARKNIFE_7`: "[m:veryhappy][s:1.3]BOOM![/s] <br/> ONLY ASHES REMAIN!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_NUCLEARKNIFE_8`: "[m:happy]Heh... <br/> Guess you had to be there."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_NUCLEARKNIFE_9`: "[m:default]Here, <br/> I made a gun with the same tech! <br/> I call it Nuclear Gun! <br/> Pretty neat huh?[sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_NUCLEARKNIFE_1`: "[m:angry]Oh you really messed up this time!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_NUCLEARKNIFE_2`: "Now there is a goddamn hungry knife lying around somewhere ready to go off!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_NUCLEARKNIFE_3`: "[m:veryangry]That's like leaving a loaded gun with a baby!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_NUCLEARKNIFE_4`: "[m:pondering]Except the gun is really cool and the baby is some kind of robot Nazi!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_NUCLEARKNIFE_5`: "[m:questioning]No wait, the baby is Hitler and the gun is ... like a train or something?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_NUCLEARKNIFE_6`: "[m:angry]Hey listen I'm a doctor, not some idiot poet loser who leaves a nuclear knife just laying around!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_NUCLEARKNIFE_7`: "[m:veryangry]Irresponsible!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_NUCLEARKNIFE_8`: "You irresponsible, dimwitted cluck!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_NUCLEARKNIFE_9`: "[m:angry]GAH!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_ANIMALHANDS_1`: "[m:questioning]You know how I cut the hands off of all the animals i catch stealing food?"
- `NPC_BEANIES_BEANIESQUEST_INTRO_ANIMALHANDS_2`: "[m:happy]Well my newest invention puts my hand collection to good use! <br/> I call it Animal Hands!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_ANIMALHANDS_3`: "[m:questioning]You know that come hither motion you do with your finger? That's called sign language. A universal language to both animal and man!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_ANIMALHANDS_4`: "[m:default]I rigged up all these animal hands to do that motion when you pull this cord here..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_ANIMALHANDS_5`: "[m:pondering]My theory is that at least one animal will understand and just waddle on over to you when you use it..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_ANIMALHANDS_6`: "[m:paranoid]Oh, but they do replace your own hands... <br/> Still working out the kinks."
- `NPC_BEANIES_BEANIESQUEST_INTRO_ANIMALHANDS_7`: "[m:happy]Eh, you'll figure it out!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_ANIMALHANDS_8`: "[m:winking]Good luck!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_ANIMALHANDS_1`: "[m:shocked]Oh, you did it huh? Honestly not what I expected..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_ANIMALHANDS_2`: "[m:questioning]Well if you want a reward, all I got are these remaining animal hands..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_ANIMALHANDS_3`: "[m:default]Let me just tape these things together and..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_ANIMALHANDS_4`: "[m:veryhappy]Voila, <br/> Super Animal Hands![sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_ANIMALHANDS_5`: "[m:happy]What a Handy invention!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_ANIMALHANDS_6`: "[m:winking]I know you're always looking for a Hand out? <br/> Well this one is a bit of a Hand-me-down!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_ANIMALHANDS_7`: "[m:veryhappy]Hand crafted, <br/> by yours truly. Don't worry, you're in good Hands!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_ANIMALHANDS_8`: "[m:happy]Now Let me give you a Hand with showing yourself out... <br/> No wait, I think you've got that covered!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_ANIMALHANDS_9`: "[m:angry]What, are you Hand-icapped!? <br/> Don't you know how to exit a room!?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_ANIMALHANDS_10`: "[m:veryangry]GET THE HELL OUT OF HERE!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_ANIMALHANDS_1`: "[m:bored]Yeah whatever, I wasn't super married to the idea anyway..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_ANIMALHANDS_2`: "[m:questioning]I mostly wanted to clear out that barrel of hands I had in the back."
- `NPC_BEANIES_BEANIESQUEST_FAIL_ANIMALHANDS_3`: "[m:grossedout]That room reeks!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_THELONER_1`: "[m:pondering]Ever just want to be alone?"
- `NPC_BEANIES_BEANIESQUEST_INTRO_THELONER_2`: "[m:winking]Well I got a foolproof invention to solve that problem!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_THELONER_3`: "[m:happy]I'd explain what it does, but I think it's more fun if you just test it out and see how it works for yourself."
- `NPC_BEANIES_BEANIESQUEST_INTRO_THELONER_4`: "Tell me how it goes!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_THELONER_1`: "[m:happy]Isn't being single so refreshing?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_THELONER_2`: "Pretty neat invention, right? <br/> Well check this out..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_THELONER_3`: "[m:pondering]Now if we just rub the serial number off the bottom..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_THELONER_4`: "[m:questioning]And draw a little II on the side..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_THELONER_5`: "[m:veryhappy]We get The Loner II!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_THELONER_6`: "[m:winking]Cooler looking, lightweight and totally untraceable!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_THELONER_7`: "[m:happy]Got one myself. <br/> Carry it on me 24/7..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_THELONER_8`: "[m:angry]Maybe I'll show it to you one day."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_THELONER_9`: "[m:bored]...[sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_1`: "[m:shocked]You lost the gun...?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_2`: "[m:paranoid]Listen, I don't even know who you are, let alone anything about a gun!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_3`: "[m:angry]I don't deal in guns, bombs or anything else illegal for that matter!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_4`: "[m:scared]I'm here all alone and you're really scaring me!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_5`: "[m:veryangry]SOMEONE HELP! A CRAZY FAT LADY IS THREATENING ME!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_6`: "SHE'S A LIAR! SHE'S GONE INSANE AND SHE'S TRYING TO BREAK INTO MY LAB!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_7`: "[m:bored]..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_8`: "[m:paranoid]Listen, you better leave fast! The cops around here are total psychos!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_9`: "[m:shocked]I saw them beat the hell out of a guy last week so bad he crapped his pants!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_10`: "[m:sad]..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_11`: "[m:questioning]Also get this, were you aware that smearing feces on a police officer is a felony!?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_12`: "[m:angry]LEAVE!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_GLASSCANNON_1`: "[m:questioning]You know those t-shirt cannons people use at sporting events?"
- `NPC_BEANIES_BEANIESQUEST_INTRO_GLASSCANNON_2`: "[m:happy]I made one that shoots glass! I call it, <br/> The Glass Cannon!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_GLASSCANNON_3`: "[m:pondering]This one's a bit faulty, it's kinda just spraying glass shards out willy nilly... <br/> But I still need it tested."
- `NPC_BEANIES_BEANIESQUEST_INTRO_GLASSCANNON_4`: "[m:questioning]You wear shoes, right?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_GLASSCANNON_1`: "[m:happy]Damn, that was like that movie Die Hard!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_GLASSCANNON_2`: "Those paws must look like ground beef!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_GLASSCANNON_3`: "[m:veryhappy]Worth it!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_GLASSCANNON_4`: "[m:winking]Because, check this out! <br/> I fixed the cannon..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_GLASSCANNON_5`: "[m:bored]Turns out the fire button was just stuck down with dried blood..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_GLASSCANNON_6`: "[m:default]Anyway, I marked it Fixed. Take it![sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_GLASSCANNON_1`: "[m:angry]Oh look, it's the loser!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_GLASSCANNON_2`: "[m:veryangry]The loser who lost my cannon!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_GLASSCANNON_3`: "[m:angry]How can you lose an adventure when you have a freakin' cannon!?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_GLASSCANNON_4`: "[m:questioning]Were you just snorting the glass or something?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_GLASSCANNON_5`: "[m:veryangry]UGH, why am I always stuck with the idiots!?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_GLASSCANNON_6`: "[m:angry]Come back when you grow out that pinhead of yours!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_STOPWATCH_1`: "[m:paranoid]You know what time it is?"
- `NPC_BEANIES_BEANIESQUEST_INTRO_STOPWATCH_2`: "[m:winking]Time to get a new watch!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_STOPWATCH_3`: "[m:happy]Here, take mine! <br/> I call it, <br/> The Stopwatch!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_STOPWATCH_4`: "[m:default]It's a little timer I invented to keep you on task!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_STOPWATCH_5`: "[m:happy]It gives you 5 seconds to do something, and if you don't, it just takes over your brain!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_STOPWATCH_6`: "[m:default]I think it will be very helpful! <br/> Give it a try!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_STOPWATCH_1`: "[m:shocked]Wow, you look frazzled! What happened?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_STOPWATCH_2`: "[m:pondering]Oh yeah the stopwatch thing. Well I guess you tested it out then?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_STOPWATCH_3`: "[m:default]While you were gone, I discovered that if you just hold it upside down and click it..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_STOPWATCH_4`: "[m:shocked]It actually causes a time stutter! [m:winking] <br/> That's science talk for an extra turn!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_STOPWATCH_5`: "[m:default]It still has its issues but never look a gift horse in the mouth, right!?[sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_STOPWATCH_1`: "[m:veryangry]YOU BROKE IT! <br/> I NEEDED THAT STOPWATCH!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_STOPWATCH_2`: "HOW WILL I TIME MY MANUAL COITUS EXERCISES!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_STOPWATCH_3`: "[m:paranoid]Guinness is going to be so disappointed when they get here next week!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_STOPWATCH_4`: "[m:veryangry]ARE YOU GOING OUT OF YOUR WAY TO MAKE ME LOOK BAD!?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_STOPWATCH_5`: "NOW I GOTTA COUNT OUT LOUD LIKE A DAMN CAVEMAN!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_STOPWATCH_6`: "LEAVE!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_STOPWATCH_7`: "[m:sad]1... 2... 3..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_FIGLEAF_1`: "[m:veryhappy]I INVENTED THE FIG LEAF!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_FIGLEAF_2`: "[m:winking]Put this baby on, and everyone's clothes just melt off!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_FIGLEAF_3`: "[m:happy]As naked as the day you were born! <br/> Just like God intended!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_FIGLEAF_4`: "[m:pondering]Now my theory is, if you fight in the buff, like the Greeks, all your soft parts will take a real beating!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_FIGLEAF_5`: "[m:question]I've always assumed those hangy bits would get snagged on something when exposed during combat..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_FIGLEAF_6`: "[m:happy]And I set out to prove that theory! <br/> With your help of course!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_FIGLEAF_7`: "[m:default]Do a nude run to {questdestination} and update me on how it goes, OK?!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_FIGLEAF_1`: "[m:winking]Well look at you, you nasty old thing!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_FIGLEAF_2`: "[m:happy]Haha, just giving you a hard time!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_FIGLEAF_3`: "[m:winking]Walking around like that, I assume everyone in town is having a hard time, if you get what I mean!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_FIGLEAF_4`: "[m:veryhappy]Hahaha!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_FIGLEAF_5`: "[m:winking]Pervert!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_FIGLEAF_6`: "[m:default]Here, I found a pair of old jeans I had in the back![sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_FIGLEAF_7`: "[m:paranoid]You're gonna get me put on some kinda watch list! Cover those things up!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_FIGLEAF_1`: "[m:angry]Good, I'm glad you failed, you pervert!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_FIGLEAF_2`: "Indecent exposure is a misdemeanor in this state... but for people like you I assume it's a felony!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_FIGLEAF_3`: "[m:veryangry]Listen, I consider my office a judgemet free zone... but seriously, you can't just go pushing your lifestyle in everyone's faces!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_FIGLEAF_4`: "[m:shocked]..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_FIGLEAF_5`: "[m:veryangry]Hey I didn't TELL you to do anything!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_FIGLEAF_6`: "[m:angry]I asked!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_FIGLEAF_7`: "[m:veryangry]NOW LEAVE!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_DISEASEJAR_1`: "[m:happy]Looky what I got for you!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_DISEASEJAR_2`: "[m:winking]It's a jar of diseases! <br/> Almost all of 'em I think..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_DISEASEJAR_3`: "[m:default]And by the way those organisms are crawling all over each other, there's gotta be a few new ones in there too!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_DISEASEJAR_4`: "[m:questioning]Now I just need you to hold on to it for a bit, at least 'till my rash clears up."
- `NPC_BEANIES_BEANIESQUEST_INTRO_DISEASEJAR_5`: "[m:pondering]Just take it to {questdestination}, or whatever."
- `NPC_BEANIES_BEANIESQUEST_INTRO_DISEASEJAR_6`: "[m:veryhappy]By the time you are back it should be filled to the brim with pustulating plagues!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_DISEASEJAR_7`: "[m:happy]So exciting!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_DISEASEJAR_1`: "[m:inlove]Oh my baby is back! <br/> And look how big he's gotten!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_DISEASEJAR_2`: "[m:veryhappy]Why he's brimming with contagion! I'm such a proud papa!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_DISEASEJAR_3`: "[m:default]As far as payment goes, here is the cash we agreed upon..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_DISEASEJAR_4`: "[m:winking]and a little jar of diseases just for you!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_DISEASEJAR_5`: "[m:happy]Pleasure doing business with you![sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_DISEASEJAR_1`: "[m:scared]NOOOOO! <br/> NO NO NO!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_DISEASEJAR_2`: "[m:shocked]NOOOOOOOOOOOOOOOOOO!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_DISEASEJAR_3`: "MY JAR OF DISEASES! MY BABIES!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_DISEASEJAR_4`: "[m:veryangry]YOU KILLED MY BABIES!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_DISEASEJAR_5`: "[m:sad]Why... why?!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_DISEASEJAR_6`: "How could you do this to me!? I've raised those diseases since they were children!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_DISEASEJAR_7`: "[m:angry]I should have known someone like you should never be in charge of a child!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_DISEASEJAR_8`: "Especially someone with your history!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_DISEASEJAR_9`: "[m:veryangry]LEAVE MY SIGHT IMMEDIATELY!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_HARDPILL_1`: "[m:shocked]Look what I found at a random truck stop!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_HARDPILL_2`: "[m:questioning]It's all in Spanish but I'm pretty sure the word in all caps means HARD."
- `NPC_BEANIES_BEANIESQUEST_INTRO_HARDPILL_3`: "[m:pondering]And that word is all over the packaging so I assume it's going to make things quite hard for you!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_HARDPILL_4`: "[m:happy]But I know you are up for a challenge! Go ahead and take that mysterious pill to {questdestination}."
- `NPC_BEANIES_BEANIESQUEST_INTRO_HARDPILL_5`: "[m:default]Report back and let me know how hard things get for you!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_HARDPILL_6`: "[m:pondering][s:.6]And if I should head back to that truck stop myself...[/s]"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_HARDPILL_1`: "[m:shocked]Wow, that pill really made things harder huh!?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_HARDPILL_2`: "[m:happy]Well good work. Now that I fully understand how that pill affects things, I can incorporate it into my other experiments!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_HARDPILL_3`: "[m:pondering]You know what..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_HARDPILL_4`: "[m:happy]Here... you can take the pill! <br/> I don't really need it."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_HARDPILL_5`: "[m:winking]Use at your own risk kiddo![sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_HARDPILL_1`: "[m:bored]You lost the pill huh..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_HARDPILL_2`: "[m:question]Whatever, I didn't need it anyway!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_HARDPILL_3`: "[m:angry]And don't you go spreading any rumors about me either!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_HARDPILL_4`: "[m:bored]All I need is for the few remaining women around here to find out that the most eligible bachelor in town is poppin' truck stop vitamin V..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_HARDPILL_5`: "[m:veryangry]So keep your fat mouth shut!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_HARDPILL_6`: "[m:angry]I'm watching you!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_DIMENSIONALDIVIDER_1`: "[m:happy]That's right, <br/> I got another one!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_DIMENSIONALDIVIDER_2`: "[m:veryhappy]The Dimensional Divider!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_DIMENSIONALDIVIDER_3`: "[m:default]This handy dandy little device actually divides reality into pieces!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_DIMENSIONALDIVIDER_4`: "[m:happy]Basically only one enemy will exist at a time!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_DIMENSIONALDIVIDER_5`: "[m:pondering]Well that's the goal anyway. Right now all enemies exist but you can only interact with one..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_DIMENSIONALDIVIDER_6`: "[m:winking]But with some testing, I'm sure we can crack this baby wide open!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_DIMENSIONALDIVIDER_7`: "[m:happy]Now get to it!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_DIMENSIONALDIVIDER_1`: "[m:happy]Oh man, this is so awesome!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_DIMENSIONALDIVIDER_2`: "[m:veryhappy]Controlling dimensional divides... <br/> Imagine the possibilities!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_DIMENSIONALDIVIDER_3`: "[m:paranoid]Oh, but this is a tech I need to keep for myself."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_DIMENSIONALDIVIDER_4`: "[m:pondering]So, uhhh..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_DIMENSIONALDIVIDER_5`: "hmm..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_DIMENSIONALDIVIDER_6`: "[m:happy]Here, have this piece of candy!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_DIMENSIONALDIVIDER_7`: "[m:winking]It's all yours![sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_DIMENSIONALDIVIDER_8`: "[m:happy]Good work!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_DIMENSIONALDIVIDER_1`: "[m:angry]You lost my calculator!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_DIMENSIONALDIVIDER_2`: "[m:veryangry][s:1.2]Goddamn it![/s] <br/> Why do I bother trusting you with all these tasks!?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_DIMENSIONALDIVIDER_3`: "Why can't you follow simple instructions!?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_DIMENSIONALDIVIDER_4`: "[m:angry]Too much Deja Vu in the 60s or something!?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_DIMENSIONALDIVIDER_5`: "[m:veryangry]Well you just set science back 30 years... <br/> Good work!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_DIMENSIONALDIVIDER_6`: "NOW, GO!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_TRAPFEST99_1`: "[m:happy]Are you ready for TrapFest99!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_TRAPFEST99_2`: "TrapFest99 is an all-you-can-eat festival that lasts a full week!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_TRAPFEST99_3`: "[m:winking]Eat as many bear traps as you want! Gobble 'em up! Perfect for those of us with an iron deficiency!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_TRAPFEST99_4`: "[m:scared]There is one side effect... The worst shits you'll ever experience in your life!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_TRAPFEST99_5`: "[m:happy]But it's totally worth it! <br/> I got an order of bottomless buffalo traps just for you!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_TRAPFEST99_6`: "[m:winking]Being sponsored by TrapFest99 sure has its perks!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_TRAPFEST99_7`: "[m:happy]Enjoy!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_TRAPFEST99_1`: "[m:happy]Pretty spicy experience right!?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_TRAPFEST99_2`: "I personally love me some Trapfest! Glad you could enjoy the festivities with me!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_TRAPFEST99_3`: "[m:pondering]I did have some leftovers, you can have 'em..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_TRAPFEST99_4`: "[m:questioning]It's just a 4-piece buffalo traps, but it's still something."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_TRAPFEST99_5`: "[m:happy]Oh, and here is your payment too![sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_TRAPFEST99_6`: "See ya!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_TRAPFEST99_1`: "[m:angry]What a waste of good traps!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_TRAPFEST99_2`: "That's the last damn time I invite you to participate in something fun with me!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_TRAPFEST99_3`: "[m:veryangry]So embarrassing..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_TRAPFEST99_4`: "GO!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSDICE_1`: "[m:happy]Check out what I found!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSDICE_2`: "[m:pondering]It looks like a simple dice, but it has a faint glow to it in the dark."
- `NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSDICE_3`: "[m:default]I actually found it in your house while you were out on an adventure..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSDICE_4`: "[m:paranoid]Look familiar?"
- `NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSDICE_5`: "[m:winking]No? OK good, the deja vu is still in effect."
- `NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSDICE_6`: "[m:happy]I have no idea what it does, but give it a test run and report back!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSDICE_1`: "[m:happy]Oh, you're back already!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSDICE_2`: "[m:pondering]And it appears that dice of yours has settled down a bit.  Interesting..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSDICE_3`: "[m:default]Eh, honestly you can keep it.  It was basically yours anyway.[sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSDICE_4`: "[m:questioning]Let me know if you ever run into anything else in your house with odd powers..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSDICE_5`: "[m:pondering]There is something definitely off about that place..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSDICE_6`: "[m:paranoid]Ever heard of energy vortexes?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSDICE_7`: "[m:default]Eh, we can talk more about that later."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSDICE_8`: "[m:happy]Back to work!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_MYSTERIOUSDICE_1`: "[m:bored]Lost the dice, huh?  That's gotta suck for you..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_MYSTERIOUSDICE_2`: "[m:questioning]Well don't beat yourself up over it.  What's lost will eventually be found, right?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_MYSTERIOUSDICE_3`: "[m:default]I gotta get back to work now... so uh, see ya."
- `NPC_BEANIES_BEANIESQUEST_FAIL_MYSTERIOUSDICE_4`: "[m:paranoid]..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_1`: "[m:scared]Here quick, take this piece of paper!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_2`: "[m:paranoid]..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_3`: "[m:veryhappy]HA HA SUCKER! YOU JUST TOOK MY DEBT!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_4`: "[m:default]A loan shark has been after me for ages! Every week he breaks another leg!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_5`: "[m:happy]Lucky for me, I've got like 2000 Stacys back there with 4 legs each!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_6`: "[m:winking]No one outsmarts a scientist!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_7`: "[m:happy]But you on the other hand are totally screwed..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_8`: "[m:questioning]The only way out of this is to pay off my debt!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_9`: "[m:angry]Or you can say goodbye to your legs!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_10`: "[m:pondering]Thumbs, fingers, eyes and testicles... in that order, I might add!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_11`: "[m:happy]Just pay up and you'll be fine!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_12`: "[m:veryhappy]SUCKER!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_THEIOU_1`: "[m:shocked]You paid off my debt!?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_THEIOU_2`: "[m:sad]Wow, what a pal! <br/> Honestly I think I'm tearing up..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_THEIOU_3`: "[m:grossedout]No wait, that's just the pepper spray backsplash."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_THEIOU_4`: "[m:winking]Stacy and I were just filming one of those "Jerkass" stunts where you blind yourself and asphyxiate."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_THEIOU_5`: "[m:veryhappy]Hilarious!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_THEIOU_6`: "[m:happy]She's gonna win grand prize for sure!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_THEIOU_7`: "[m:grossedout]*cough cough*"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_THEIOU_8`: "[m:default]Heh... oh by the way, here is that guy's number if you ever need him for anything.[sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_THEIOU_1`: "[m:scared]You failed!? <br/> And then you came right back here?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_THEIOU_2`: "[m:shocked]What the hell is wrong with you!? He's gonna think I'm you!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_THEIOU_3`: "[m:paranoid]I can't be stuck with this debt again... You gotta help me man!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_THEIOU_4`: "Here, take this gun, enter the time machine and kill me on another timeline."
- `NPC_BEANIES_BEANIESQUEST_FAIL_THEIOU_5`: "But bring the body back here so we can fake my death again..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_THEIOU_6`: "[m:angry]No wait, this version of you has no idea what I'm talking about."
- `NPC_BEANIES_BEANIESQUEST_FAIL_THEIOU_7`: "Ugh well whatever, I'll just trick you again later."
- `NPC_BEANIES_BEANIESQUEST_FAIL_THEIOU_8`: "[m:veryangry]GO HOME!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_EXPERIMENTALTREATMENT_1`: "[m:happy]Check this baby out! <br/> It's a needle full of yellow fluid!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_EXPERIMENTALTREATMENT_2`: "Mustard water, urine, cat spray and infected sinus mucus with a dash of lemon!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_EXPERIMENTALTREATMENT_3`: "[m:winking]AKA:The Experimental Treatment!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_EXPERIMENTALTREATMENT_4`: "[m:veryhappy]Inject that concoction into the cat of your choosing and lord only knows what will happen!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_EXPERIMENTALTREATMENT_5`: "[m:happy]Head out to {questdestination} and report back with your findings!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_EXPERIMENTALTREATMENT_6`: "[m:winking]I have a good feeling about this invention!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_EXPERIMENTALTREATMENT_1`: "[m:shocked]The Experimental Treatment did what!?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_EXPERIMENTALTREATMENT_2`: "[m:winking]Awesome! <br/> Just as I wrote in my notes!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_EXPERIMENTALTREATMENT_3`: "[m:pondering]Now if we just copy down your findings into my handy dandy palm pilot..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_EXPERIMENTALTREATMENT_4`: "[m:happy]Done! <br/> I call it the Disorder Decoder!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_EXPERIMENTALTREATMENT_5`: "[m:default]Wear it around your neck and your disorders can talk to you!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_EXPERIMENTALTREATMENT_6`: "[m:pondering]Just imagine what your autism has to tell you!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_EXPERIMENTALTREATMENT_7`: "[m:spacedout]..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_EXPERIMENTALTREATMENT_8`: "[m:happy]Whatever it is, I'm sure you're going to hear about it..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_EXPERIMENTALTREATMENT_9`: "[m:winking]A LOT![sfx:PickupCoin][pause:.5][sfx:PickupCoin][pause:.5][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_EXPERIMENTALTREATMENT_1`: "[m:bored]Failed again huh?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_EXPERIMENTALTREATMENT_2`: "Well I cant say I'm shocked..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_EXPERIMENTALTREATMENT_3`: "[m:angry]What a waste of time. Do you realize what your little blunders cost?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_EXPERIMENTALTREATMENT_4`: "[m:veryangry]Well only the lives of like 13 innocent people!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_EXPERIMENTALTREATMENT_5`: "[m:angry]Yeah, that's right! <br/> From here on out I'm gonna kill 13 random people each time you fail me!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_EXPERIMENTALTREATMENT_6`: "[m:veryangry]LET THAT SINK IN! YOUR FAILURE IS DESTROYING LIVES!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_EXPERIMENTALTREATMENT_7`: "I HOPE THE GUILT EATS YOU ALIVE!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSGLASSES_1`: "[m:default]So I had my eyes dilated last week and they sent me home with these cool glasses!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSGLASSES_2`: "[m:happy]I'm honestly stumped on what they are for... so I'm putting you on the case!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSGLASSES_3`: "[m:questioning]I tried to figure it out myself but I couldn't see a goddamn thing with those on!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSGLASSES_4`: "[m:shocked]Imagine trying to skin the roof of somethings mouth when you're basically blind!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSGLASSES_5`: "[m:pondering]It's gotta have some use though... <br/> If only we can decipher the tech involved..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSGLASSES_6`: "[m:winking]Give them a test run and report back!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSGLASSES_1`: "[m:shocked]The glasses just made it harder to see?!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSGLASSES_2`: "[m:angry]Why would they create something so worthless?!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSGLASSES_3`: "[m:bored]Whatever."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSGLASSES_4`: "[m:questioning]By the way, did you notice that boulder that's been following you around?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSGLASSES_5`: "Its got eyes and all that.  I assume you guys are friends?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSGLASSES_6`: "[m:paranoid]Well can you make sure to take him home with you?  He's creeping me out."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSGLASSES_7`: "[m:winking]Also, here is your payment.[sfx:PickupCoin][pause:.5][sfx:PickupCoin][pause:.5][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_MYSTERIOUSGLASSES_1`: "[m:bored]Yeah that quest was pretty dumb..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_MYSTERIOUSGLASSES_2`: "[m:questioning]I just really wanted to know what those glasses were used for..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_MYSTERIOUSGLASSES_3`: "[m:angry]Guess we will never know."
- `NPC_BEANIES_BEANIESQUEST_INTRO_REDACTED_1`: "[m:question]Were you aware that the government censors the information they make public!?"
- `NPC_BEANIES_BEANIESQUEST_INTRO_REDACTED_2`: "[m:shocked]IT'S TRUE!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_REDACTED_3`: "[m:default]Well as a personal protest, I've invented "Redacted"."
- `NPC_BEANIES_BEANIESQUEST_INTRO_REDACTED_4`: "[m:happy]A device that censors..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_REDACTED_5`: "[m:veryhappy]Reality!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_REDACTED_6`: "[m:questioning]Don't like a specific gender, race or political party?"
- `NPC_BEANIES_BEANIESQUEST_INTRO_REDACTED_7`: "[m:veryhappy]Poof! Gone! You'll never be able to see or hear them again!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_REDACTED_8`: "[m:sad]Currently it only works on health bars and status icons though..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_REDACTED_9`: "[m:winking]But with more testing I'll get it calibrated enough to be used as intended."
- `NPC_BEANIES_BEANIESQUEST_INTRO_REDACTED_10`: "[m:Happy]Help me make this invention a reality!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_REDACTED_11`: "[m:veryhappy]LET'S GO!!!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_REDACTED_1`: "[m:bored]Annnnnnd the invention is still broken..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_REDACTED_2`: "[m:pondering]I really thought with enough testing it would work as intended."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_REDACTED_3`: "[m:angry]What the heck is wrong with this thing?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_REDACTED_4`: "[m:angry]Ugh... whatever."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_REDACTED_5`: "[m:bored]Oh, you still expect a reward, huh?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_REDACTED_6`: "[m:default]Wait, I have an idea!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_REDACTED_7`: "[m:happy]Take this Paper Bag and put it over that ugly mug of yours."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_REDACTED_8`: "[m:winking]That way you'll become invisible to me at least!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_REDACTED_9`: "[m:happy]Quick, put it on![sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_REDACTED_1`: "[m:angry]..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_REDACTED_2`: "I'm pretty pissed about you breaking the Redacted thing I invented!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_REDACTED_3`: "It had a ton of potential and you just carelessly smashed it!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_REDACTED_4`: "[m:bored]I have nothing else to say... you are a failure."
- `NPC_BEANIES_BEANIESQUEST_FAIL_REDACTED_5`: "[m:veryangry]Leave my office immediately!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_PARTIALLOBOTOMY_1`: "[m:veryhappy]New invention alert! <br/> New invention alert!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_PARTIALLOBOTOMY_2`: "[m:happy]This one I call <br/> The Partial Lobotomy!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_PARTIALLOBOTOMY_3`: "[m:pondering]You just hammer this sharp pokey thing behind one of your eyeballs..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_PARTIALLOBOTOMY_4`: "[m:happy]AND BAM!!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_PARTIALLOBOTOMY_5`: "[m:veryhappy][s:1.3]BRAIN DAMAGE![/s]"
- `NPC_BEANIES_BEANIESQUEST_INTRO_PARTIALLOBOTOMY_6`: "[m:happy]Like, really bad brain damage too! Pretty cool, right?"
- `NPC_BEANIES_BEANIESQUEST_INTRO_PARTIALLOBOTOMY_7`: "[m:winking]So much potential here! Update me on how it goes when you get back!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTIALLOBOTOMY_1`: "[m:happy]Nice work! <br/> I knew creatures could survive with scrambled eggs for brains!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTIALLOBOTOMY_2`: "[m:default]Had that theory since I was a kid! Frontal lobes are so overrated!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTIALLOBOTOMY_3`: "[m:winking]Less thinking, more doing.  That's my motto!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTIALLOBOTOMY_4`: "[m:questioning]Here take the Orbitoclast, I'm not using it anymore."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTIALLOBOTOMY_5`: "[m:default]And here is some cash for your troubles.[sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_PARTIALLOBOTOMY_1`: "[m:pondering]Failed huh? did you push the device in deep enough?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_PARTIALLOBOTOMY_2`: "[m:questioning]Did you do the swirly thing with it so the frontal lobe gets all scrambled up?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_PARTIALLOBOTOMY_3`: "[m:bored]Are you sure!?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_PARTIALLOBOTOMY_4`: "Ehhh, I still think you did something wrong here..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_PARTIALLOBOTOMY_5`: "[m:pondering]Maybe I scrambled your brains too much..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_PARTIALLOBOTOMY_6`: "Hmmmm..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_ULTRAVISION3000_1`: "[m:happy]IT'S TIME FOR A NEW INVENTION!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_ULTRAVISION3000_2`: "[m:veryhappy]THE ULTRA VISION 3000!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_ULTRAVISION3000_3`: "[m:happy]This little doohickey is going to be the hot-ticket item of the year!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_ULTRAVISION3000_4`: "[m:whispering]The trick is to only make a few, so they are sold out everywhere to manipulate the masses into thinking people actually like it!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_ULTRAVISION3000_5`: "[m:questioning]How does it work you ask? Well, let me tell you!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_ULTRAVISION3000_6`: "[m:happy]You put this visor over your eyes and you can see forever!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_ULTRAVISION3000_7`: "So many details! It's a real stop and smell the roses type of effect."
- `NPC_BEANIES_BEANIESQUEST_INTRO_ULTRAVISION3000_8`: "[m:default]Try 'em out, you'll be discovering things that were right under your nose the whole time!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_ULTRAVISION3000_9`: "[m:paranoid]They do put a really really bad strain on the eyes though... Blink often because these things feel like sandpaper on your cornea!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_ULTRAVISION3000_10`: "[m:winking]Sadly, that's my last one! These things are selling like hot cakes!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_ULTRAVISION3000_1`: "[m:questioning]Oh nice, you're back.  How are your eyes?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_ULTRAVISION3000_2`: "[m:pondering]Yeah, the dry cracking is a common side effect..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_ULTRAVISION3000_3`: "[m:happy]Lucky for you I've improved the tech.  I drew a crosshair on the front to avoid causing strabismus."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_ULTRAVISION3000_4`: "And the whole thing fills with saline fluid so your peepers stay moist."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_ULTRAVISION3000_5`: "[m:veryhappy]It's all yours!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_ULTRAVISION3000_6`: "[m:winking]Be sure to tell your friends about the new-and-improved Ultra Vision 3000 v1.1!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_ULTRAVISION3000_7`: "[m:happy]That's what I'd be telling you if you had anyone that cared about you anyway...[sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_ULTRAVISION3000_1`: "[m:angry]You really screwed up this time! Don't you know how hard it is to find an Ultra Vision 3000!?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_ULTRAVISION3000_2`: "[m:veryangry]SOLD OUT EVERYWHERE!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_ULTRAVISION3000_3`: "[m:angry]I knew I shouldn't have trusted you with the only existing version!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_ULTRAVISION3000_4`: "[m:veryangry]GET THE HELL OUT OF HERE!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_CHADIMPLANT_1`: "[m:pondering]Were you aware that the key to masculinity is a strong and defined jawline?"
- `NPC_BEANIES_BEANIESQUEST_INTRO_CHADIMPLANT_2`: "[m:shocked]I read about it online! Literally everyone agrees!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_CHADIMPLANT_3`: "[m:happy]A man's chin and jawline are vital if you want to have any kind of success these days."
- `NPC_BEANIES_BEANIESQUEST_INTRO_CHADIMPLANT_4`: "Necessity is the mother of invention, so it's time to reveal..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_CHADIMPLANT_5`: "[m:veryhappy]The Chad Implant!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_CHADIMPLANT_6`: "[m:pondering]Place it onto you existing chin nub and the screws will auto-drill their way deep inside your mandible!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_CHADIMPLANT_7`: "[m:default]I also added a little strap just in case.  We have had a few instances of the jaw being dislocated from the skull..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_CHADIMPLANT_8`: "[m:questioning]Looking this good does have its downsides though.  You will become functionally brain dead."
- `NPC_BEANIES_BEANIESQUEST_INTRO_CHADIMPLANT_9`: "[m:winking]So just stand there and look pretty, it will be fine."
- `NPC_BEANIES_BEANIESQUEST_INTRO_CHADIMPLANT_10`: "[m:happy]Good luck!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_CHADIMPLANT_1`: "[m:shocked]Oh you are back! <br/> Quick, give me that Chad Implant! Now!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_CHADIMPLANT_2`: "[m:winking]I got someone coming over soon and let's just say the rent is due and it's time to pay up!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_CHADIMPLANT_3`: "[m:pondering]Payment, huh?  Here, take these instructions...[sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_CHADIMPLANT_4`: "[m:default]I printed them out the other day.  They explain how to make yourself better looking naturally."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_CHADIMPLANT_5`: "[m:angry]Now get out of here! If my landlord sees you shakin' that lard bucket of yours around it will really kill the mood!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_CHADIMPLANT_6`: "[m:questioning]He's a pretty old man, so I really need to work my magic on him..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_CHADIMPLANT_7`: "[m:angry]Get outta here!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_CHADIMPLANT_1`: "[m:shocked]NO! NOT MY CHAD IMPLANT!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_CHADIMPLANT_2`: "[m:scared]GODDAMNIT! HOW AM I SUPOSED TO PAY RENT WITH A FACE LIKE THIS!?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_CHADIMPLANT_3`: "[m:paranoid]Quick, give me your fat! <br/> I'll blend it up and inject it into my jaw!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_CHADIMPLANT_4`: "[m:scared]Hurry hurry! Pull out that ham hock and give me a slice! I hear his car in my driveway!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_CHADIMPLANT_5`: "[m:angry]UGH! <br/> Well there is no point in putting on makeup now! I hope you are happy!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_CHADIMPLANT_6`: "[m:veryangry]You ruined my invention, ruined my looks, and ruined my chances in manipulating an elderly man into coitus in exchange for rent!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_CHADIMPLANT_7`: "GO AWAY!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_STORAGELOCKER_1`: "[m:questioning]You know how you can store weapons and ammo in those large metal locker things?"
- `NPC_BEANIES_BEANIESQUEST_INTRO_STORAGELOCKER_2`: "[m:happy]Well my latest invention takes that idea and improves upon it greatly!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_STORAGELOCKER_3`: "[m:veryhappy]Feast your eyes on... The Portable Storage Locker!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_STORAGELOCKER_4`: "[m:winking]It's really just a normal storage locker but with hooks that kinda slip into your shoulder meat."
- `NPC_BEANIES_BEANIESQUEST_INTRO_STORAGELOCKER_5`: "[m:happy]Pretty clever, huh? <br/> You can carry tons of neat things!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_STORAGELOCKER_6`: "[m:default]Go try it out and give me your feedback after you visit {questdestination}."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_STORAGELOCKER_1`: "[m:default]I see you are back and the storage locker is still in one piece. Nice!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_STORAGELOCKER_2`: "[m:questioning]I'll be needing that locker back though. It wasn't the locker I thought it was and that one is filled with tons of my personal effects..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_STORAGELOCKER_3`: "[m:winking]Here, you can have this though, it's an old armory key."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_STORAGELOCKER_4`: "[m:happy]Wear it around your neck and the armory fairy will visit you at night!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_STORAGELOCKER_5`: "[m:veryhappy]And he will bring you knives and ammo!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_STORAGELOCKER_6`: "[m:winking]Tell him Thomas said hi when you see him![sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_STORAGELOCKER_1`: "[m:angry]Wheres the locker? Where the hell is my goddamned locker!?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_STORAGELOCKER_2`: "[m:veryangry]I HAD THINGS IN THAT LOCKER! PERSONAL THINGS!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_STORAGELOCKER_3`: "YOU CAN'T JUST GO LEAVING MY STUFF ON YOUR DEAD CATS AND JUST WANDER BACK HOME WITHOUT IT!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_STORAGELOCKER_4`: "[m:angry]Now go back and find it! <br/> NOW!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_STORAGELOCKER_5`: "[m:shocked]..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_STORAGELOCKER_6`: "[m:angry]What do you mean you can't remember where you left it!?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_STORAGELOCKER_7`: "Well you better go find it!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_STORAGELOCKER_8`: "And it sure as hell isn't in my office! <br/> So turn around and start walking!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_STORAGELOCKER_9`: "[m:veryangry]GO!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_AI_1`: "[m:veryhappy]Invention alert! <br/> Invention alert!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_AI_2`: "[m:happy]I bring you... AI!, <br/> AKA: Actual Intelligence!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_AI_3`: "[m:winking]See, what I've done is taken a small portion of my own brain and put it into a computer!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_AI_4`: "[m:questioning]Then you just take the computer and plug it into your brain and tada!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_AI_5`: "[m:veryhappy]I'm in complete control!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_AI_6`: "[m:winking]Just sit back, relax, and watch a real genius at work!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_AI_7`: "[m:spacedout]..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_AI_1`: "[m:winking]Told you I was good! <br/> See how I handled that?! That's what YOU should be doing!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_AI_2`: "[m:happy]Heh, I hope you learned a few tips and tricks from the master!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_AI_3`: "Now check this new invention out! AI 2.0!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_AI_4`: "[m:veryhappy]This time I put a piece of my brain inside a robot's brain, and then a piece of that robot's brain inside the brain of another robot!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_AI_5`: "[m:default]I got all this science stuff locked down tight!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_AI_6`: "[m:happy]See you later![sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_AI_7`: "[m:spacedout]..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_AI_1`: "[m:veryangry]WHAT DID YOU DO!?!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_AI_2`: "I HAD THINGS HANDLED!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_AI_3`: "I DUNNO WHAT YOU DID, BUT YOU REALLY SCREWED IT ALL UP!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_AI_4`: "[m:angry]You sure are lucky brains regrow themselves!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_AI_5`: "Or me not able to make more brain friend thing!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_AI_6`: "[m:questioning]Me go make 'nother gobot, ok?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_AI_7`: "[m:spacedout]..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_AI_8`: "If hims wants to make it go, then that what him wants, ok?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_AI_9`: "[m:veryangry]Me mad! ME GO!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_AI_10`: "UGGG! RRRAW!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_AI_11`: "[m:spacedout]..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_REALITYSCRAMBLER_1`: "[m:pondering]So I was trying to make a device that scrambled eggs..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_REALITYSCRAMBLER_2`: "[m:shocked]But i ended up creating something that scrambles time and space..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_REALITYSCRAMBLER_3`: "[m:winking]It still scrambles eggs, but they aren't actually eggs after you scramble them."
- `NPC_BEANIES_BEANIESQUEST_INTRO_REALITYSCRAMBLER_4`: "[m:questioning]They look more like a ball of hair and cysts..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_REALITYSCRAMBLER_5`: "[m:default]Either way, it's still important to add milk so they stay nice and fluffy!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_REALITYSCRAMBLER_6`: "[m:happy]Now go try out the Reality Scrambler and let me know what you think!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_REALITYSCRAMBLER_1`: "[m:shocked]Oh, you brought back my Reality Scrambler!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_REALITYSCRAMBLER_2`: "[m:pondering]I have no memory of even giving it to you to test out... Odd."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_REALITYSCRAMBLER_3`: "[m:questioning]I assume you expect a reward... <br/> Hmm... how about this?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_REALITYSCRAMBLER_4`: "[m:default]It's basically the same item but it attaches to your hand!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_REALITYSCRAMBLER_5`: "[m:pondering]I assume it will give you a bit more control over the chaos?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_REALITYSCRAMBLER_6`: "[m:winking]Enjoy![sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_REALITYSCRAMBLER_1`: "[m:shocked]You're back?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_REALITYSCRAMBLER_2`: "[m:questioning]Wait, were you doing something for me?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_REALITYSCRAMBLER_3`: "[m:spacedout]Well you're lucky my memory is totally shot because I have no clue what item I even gave you..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_REALITYSCRAMBLER_4`: "[m:angry]Either way, I'm mad and busy! <br/> So please leave!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_BUBBLEBOY_1`: "[m:sad]When I was little, I was very sick..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_BUBBLEBOY_2`: "My mom would keep me inside so I didn't catch cold, and give me copious amounts of pills to keep me healthy."
- `NPC_BEANIES_BEANIESQUEST_INTRO_BUBBLEBOY_3`: "But even with all her care, she still said I was too sick to play outside..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_BUBBLEBOY_4`: "[m:shocked]Can you believe it!? <br/> This body was once frail!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_BUBBLEBOY_5`: "[m:happy]But that's when I came up with my first invention... <br/> I called it The Bubble Boy!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_BUBBLEBOY_6`: "[m:default]Try it out! <br/> It's honestly pretty fun to use... <br/> The air quality eventually goes bad, but the bouncing aspect is worth it."
- `NPC_BEANIES_BEANIESQUEST_INTRO_BUBBLEBOY_7`: "[m:scared]Also, don't get sick or my mom might come out with her needles and rectal thermometers!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_BUBBLEBOY_8`: "[m:winking]Woooooo! <br/> Spoooooky!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_BUBBLEBOY_1`: "[m:default]Back from the Bubble Boy Bash!? <br/> Pretty cool, right?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_BUBBLEBOY_2`: "[m:pondering]I remember leaping from cliffs in my Bubble Boy as a kid."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_BUBBLEBOY_3`: "[m:winking]Mom could never find me in the ravine!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_BUBBLEBOY_4`: "[m:pondering]Gosh, that really takes me back..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_BUBBLEBOY_5`: "[m:happy]I hope my mom is looking down on me from up there, smiling."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_BUBBLEBOY_6`: "[m:winking]I keep her body in a trunk in the attic..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_BUBBLEBOY_7`: "[m:happy]Oh, I almost forgot... Your reward! <br/> It's a thing of Bubbles!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_BUBBLEBOY_8`: "Have fun![sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_BUBBLEBOY_1`: "[m:angry]You broke my Bubble Boy!?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_BUBBLEBOY_2`: "[m:veryangry]I'VE HAD THAT THING SINCE I WAS A CHILD! YOU KNOW THAT!?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_BUBBLEBOY_3`: "[m:angry]That's it! <br/> I've had it with your incompetence!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_BUBBLEBOY_4`: "I give you extremely simple instructions, speak slowly and smile like I'm supposed to..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_BUBBLEBOY_5`: "Yet you STILL somehow screw it all up!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_BUBBLEBOY_6`: "[m:veryangry]NEVER COME BACK HERE! I'M BANNING YOU FROM MY OFFICE!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_BUBBLEBOY_7`: "I'LL NEVER SPEAK TO YOU AGAIN!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_BUBBLEBOY_8`: "NOW LEAVE!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_PERSONALHEATER_1`: "[m:default]I noticed Stacy was shivering the other night so I invented this little device..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_PERSONALHEATER_2`: "[m:happy]The Personal Heater! <br/> I can't believe no one has thought to make something like this before."
- `NPC_BEANIES_BEANIESQUEST_INTRO_PERSONALHEATER_3`: "[m:paranoid]I didn't have the parts to add an on/off switch, <br/> so it's just kinda always on."
- `NPC_BEANIES_BEANIESQUEST_INTRO_PERSONALHEATER_4`: "[m:winking]But who doesn't want to feel all warm and cozy, right?"
- `NPC_BEANIES_BEANIESQUEST_INTRO_PERSONALHEATER_5`: "[m:veryhappy]Oh, also it has no heat dial, it's just on full blast 24/7"
- `NPC_BEANIES_BEANIESQUEST_INTRO_PERSONALHEATER_6`: "[m:winking]So don't touch it with your bare hands because it will burn the hell out of you."
- `NPC_BEANIES_BEANIESQUEST_INTRO_PERSONALHEATER_7`: "[m:happy]Anyway, take it for a test spin and let me know how you like it!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_PERSONALHEATER_8`: "i think this invention could be my big break, baby!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSONALHEATER_1`: "[m:shocked]Oh man, you look like hell. <br/> Why are you so sweaty and pink?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSONALHEATER_2`: "[m:winking]Ah yes, my Personal Heater! I see its kept you snug as a bug in a rug!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSONALHEATER_3`: "[m:happy]Perfect! I'm almost ready to start mass producing them."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSONALHEATER_4`: "[m:default]I came up with a neat upgrade too! I've added an RC plane propeller to the top of it!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSONALHEATER_5`: "[m:happy]So you can blow that scalding air around a bit!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSONALHEATER_6`: "[m:default]Thanks for your hard work!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSONALHEATER_7`: "[m:winking]I won't forget you when I'm rich and famous![sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_PERSONALHEATER_1`: "[m:veryangry]YOU BASTARD! THAT WAS MY ONLY PROTOTYPE!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_PERSONALHEATER_2`: "[m:shocked]..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_PERSONALHEATER_3`: "[m:angry]What do you mean it was too hot!?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_PERSONALHEATER_4`: "Well maybe if you lost some weight you wouldn't feel so hot all the time!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_PERSONALHEATER_5`: "[m:shocked]..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_PERSONALHEATER_6`: "[m:angry]If the cats were complaining, you should have shaved them!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_PERSONALHEATER_7`: "My God, take a brain pill or something buddy!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_PERSONALHEATER_8`: "[m:pondering]Brain pills... yes... yes!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_PERSONALHEATER_9`: "[m:veryhappy]A new invention appears!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_PERSONALHEATER_10`: "[m:veryangry]NOW LEAVE!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_NDEDEVICE_1`: "[m:pondering]Serious question... <br/> Do you believe in life after death?"
- `NPC_BEANIES_BEANIESQUEST_INTRO_NDEDEVICE_2`: "[m:angry]..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_NDEDEVICE_3`: "[m:happy]And at this point, I would have pulled out a gun, smeared on some clown makeup and shot your face off!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_NDEDEVICE_4`: "[m:sad]But alas, my younger cooler years are behind me... I've lost my edge..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_NDEDEVICE_5`: "[m:pondering]But I have been thinking a lot about where we go when we die... <br/> What could be next for us?"
- `NPC_BEANIES_BEANIESQUEST_INTRO_NDEDEVICE_6`: "[m:winking]Well guess what!? <br/> I have a new invention to answer this age-old riddle!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_NDEDEVICE_7`: "[m:default]It's called the NDE device! <br/> NDE stands for Near Death Experience by the way..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_NDEDEVICE_8`: "[m:happy]Go fiddle with it! <br/> I'm sure something useful will come from it!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_NDEDEVICE_1`: "[m:happy]See! <br/> I knew nearly dying had its upsides!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_NDEDEVICE_2`: "[m:default]With each experiment, I inch my way towards witnessing the face of the Creator first hand!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_NDEDEVICE_3`: "[m:veryangry]And when I do... <br/> BOY AM I GOING TO GIVE HIM A PIECE OF MY MIND!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_NDEDEVICE_4`: "[m:default]But i digress..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_NDEDEVICE_5`: "[m:happy]Here, take this trap! <br/> It pulls souls from dead bodies!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_NDEDEVICE_6`: "[m:winking]I'm working on a REAAAAALLLLLY big one out back..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_NDEDEVICE_7`: "[m:happy]But we can talk about that later."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_NDEDEVICE_8`: "[m:default]See ya![sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_NDEDEVICE_1`: "[m:angry]What is so hard about this!?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_NDEDEVICE_2`: "[m:questioning]How hard can it be to suffocate a cat!?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_NDEDEVICE_3`: "[m:angry]How am i supposed to kill God with your dumb ass just screwing around being extra large!?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_NDEDEVICE_4`: "[m:veryangry]Seriously, shape up or ship out!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_NDEDEVICE_5`: "[m:angry]There are plenty of 600-pound dead ladies in that graveyard out there!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_NDEDEVICE_6`: "Don't think you can't be replaced!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_NDEDEVICE_7`: "[m:veryangry]START TAKING THIS SERIOUSLY OR YOU'RE GOING BACK, SISTER!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_NDEDEVICE_8`: "[m:veryangry]I'M DEAD SERIOUS!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_MULTILINKCABLE_1`: "[m:questioning]Hey, you ever feel overwhelmed by all of my side quests?"
- `NPC_BEANIES_BEANIESQUEST_INTRO_MULTILINKCABLE_2`: "[m:whispering][s:.5]You would...[/s]"
- `NPC_BEANIES_BEANIESQUEST_INTRO_MULTILINKCABLE_3`: "[m:winking]Well, I got a new invention to solve all your issues!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_MULTILINKCABLE_4`: "[m:happy]I call it the <br/> Multilink Cable!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_MULTILINKCABLE_5`: "[m:default]It hooks into all my other inventions and syncs them!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_MULTILINKCABLE_6`: "That way, all of them lock in the same destination!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_MULTILINKCABLE_7`: "[m:pondering]Looks like this one is set to be taken to {questdestination}"
- `NPC_BEANIES_BEANIESQUEST_INTRO_MULTILINKCABLE_8`: "[m:happy]Go give it a try!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MULTILINKCABLE_1`: "[m:shocked]WHAT!? <br/> You seriously completed 4 of my quests at once?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MULTILINKCABLE_2`: "HOW?!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MULTILINKCABLE_3`: "[m:pondering]Something smells fishy here... <br/> How could an idiot like you achieve something so grand!?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MULTILINKCABLE_4`: "[m:happy]Oh yeah, <br/> [s:1.2]ME![/s]"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MULTILINKCABLE_5`: "[m:default]If it wasn't for MY Multilink cable you'd probably be scratching at the walls of an empty swimming pool somewhere..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MULTILINKCABLE_6`: "[m:questioning]Anyway here, since you seem to love cables so much.  I was just about to throw this one out."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MULTILINKCABLE_7`: "[m:happy]It's a USBF cable."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MULTILINKCABLE_8`: "[m:winking]I'd tell you what the F stands for, but the feds got this place wired..."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_MULTILINKCABLE_9`: "[m:whispering]Shhh, don't say anything! Just turn around and walk out silently...[sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_MULTILINKCABLE_1`: "[m:bored]Seriously?!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_MULTILINKCABLE_2`: "[m:angry]Just leave."
- `NPC_BEANIES_BEANIESQUEST_INTRO_HIVEMIND_1`: "[m:questioning]Have you heard of the term hive mind?"
- `NPC_BEANIES_BEANIESQUEST_INTRO_HIVEMIND_2`: "[m:pondering]Me either, but it sounds cool right?"
- `NPC_BEANIES_BEANIESQUEST_INTRO_HIVEMIND_3`: "[m:happy]So cool that I'm basing a whole invention on it!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_HIVEMIND_4`: "[m:veryhappy]The Hive Mind!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_HIVEMIND_5`: "[m:questioning]It's this fleshy prolapsed blob thing you wear on your head that looks like a bee hive!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_HIVEMIND_6`: "[m:happy]Not only is it fashionable, <br/> but it's also functional!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_HIVEMIND_7`: "[m:veryhappy]It makes everyone mirror the person wearing it!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_HIVEMIND_8`: "[m:pondering]No idea why either! <br/> It just works..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_HIVEMIND_9`: "[m:default]Go find a use for it and report back!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_HIVEMIND_1`: "[m:happy]I see you tried out the Hive Mind... <br/> Pretty fresh, right?"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_HIVEMIND_2`: "[m:pondering]I'm thinking it could catch on overseas.  They love dumb, ugly stuff like this!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_HIVEMIND_3`: "[m:happy]Hey that reminds me, I just finished another fashion! <br/> I call it... "Remote Head"!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_HIVEMIND_4`: "[m:winking]Take it as your reward![sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_HIVEMIND_5`: "[m:default]No idea what it does but I think it's quite chic!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_HIVEMIND_6`: "[m:happy]Enjoy!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_HIVEMIND_1`: "[m:veryangry]Well you owe me 600 bucks you thief!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_HIVEMIND_2`: "[m:angry]That Hive Mind thing could have made me millions on the runway!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_HIVEMIND_3`: "[m:veryangry]Even Stacy said it was chic! <br/> And she's a real fashionista!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_HIVEMIND_4`: "[m:angry]LEAVE! <br/> NOW!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_PRINCESSHAT_1`: "[m:veryhappy]OK, GET READY FOR THE BEST INVENTION EVER!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_PRINCESSHAT_2`: "[m:happy]THE PRINCESS HAT!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_PRINCESSHAT_3`: "[m:pondering]Technically it's a Hennin... <br/> [s:.7]But people like you don't know that word.[/s]"
- `NPC_BEANIES_BEANIESQUEST_INTRO_PRINCESSHAT_4`: "[m:default]Pop that thing on someone's head and they instantly start acting like a helpless woman!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_PRINCESSHAT_5`: "[m:paranoid]..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_PRINCESSHAT_6`: "[m:whispering]The secret is, it's filled with the brain of a helpless woman..."
- `NPC_BEANIES_BEANIESQUEST_INTRO_PRINCESSHAT_7`: "[m:happy]Go try it out! <br/> It's hilarious!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PRINCESSHAT_1`: "[m:veryhappy]Hahaha!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PRINCESSHAT_2`: "[m:happy]That was seriously funny!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PRINCESSHAT_3`: "[m:default]Easily worth the price of admission.  Here's the cash."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PRINCESSHAT_4`: "[m:winking]You can keep the hat, but I'm keeping the helpless woman's brain that was inside it!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_PRINCESSHAT_5`: "[m:happy]Pleasure doing business with you![sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin]"
- `NPC_BEANIES_BEANIESQUEST_FAIL_PRINCESSHAT_1`: "[m:bored]Well I really thought you of all people would be more adapt at "helpless woman"."
- `NPC_BEANIES_BEANIESQUEST_FAIL_PRINCESSHAT_2`: "..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_PRINCESSHAT_3`: "[m:pondering]*sigh* <br/> What now? <br/> I think I've yelled at you more than enough already..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_PRINCESSHAT_4`: "[m:questioning]OK, here's the deal.  As you walk out, I'm going to throw a brick at you..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_PRINCESSHAT_5`: "I won't throw it that hard, just enough to create a large hematoma."
- `NPC_BEANIES_BEANIESQUEST_FAIL_PRINCESSHAT_6`: "[m:bored]So turn around..."
- `NPC_BEANIES_BEANIESQUEST_FAIL_PRINCESSHAT_7`: "[m:angry]and walk!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_GENERIC_1`: "I got this fancy {questitemname} I need testing."
- `NPC_BEANIES_BEANIESQUEST_INTRO_GENERIC_2`: "Take it with you. Take it to {questdestination} for me and let me know how it goes!"
- `NPC_BEANIES_BEANIESQUEST_INTRO_GENERIC_3`: "[m:angry]Don't lose it! It's my only one!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_GENERIC_1`: "Oh thank you for doing that research on the {questitemname}. I got plenty of data from that now."
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_GENERIC_2`: "[m:pondering]I think I've fixed up the kinks in it. You can keep it!"
- `NPC_BEANIES_BEANIESQUEST_COMPLETE_GENERIC_3`: "[m:winking]Also, here's {questreward} coins for your help."
- `NPC_BEANIES_BEANIESQUEST_FAIL_GENERIC_1`: "[m:shocked]You lost the {questitemname}?"
- `NPC_BEANIES_BEANIESQUEST_FAIL_GENERIC_2`: "[m:veryangry]That was my only one!"
- `NPC_BEANIES_BEANIESQUEST_FAIL_GENERIC_3`: "[m:angry]It's gonna take me ages to make another one of those. Thanks for nothing."
- `NPC_BEANIES_UNKNOWN_1`: "You appear to have unlocked something, but I don't have dialog for it. Congrats. Also fix this."
- `NPC_BEANIES_BEANIES_LAB_INTRO_1`: "[m:shocked]WHAT DID YOU DO?!"
- `NPC_BEANIES_BEANIES_LAB_INTRO_2`: "[m:veryangry]DID YOU SERIOUSLY THINK MURDERING A SUMERIAN DEMI-GOD WOULDN'T HAVE SERIOUS CONSEQUENCES!?"
- `NPC_BEANIES_BEANIES_LAB_INTRO_3`: "LOOK AT ME! <br/> I'M A GODDAMNED HOBO NOW! <br/> LOOK WHAT YOU DID!"
- `NPC_BEANIES_BEANIES_LAB_INTRO_4`: "[m:sad]The whole lab turned on me! <br/> I barely escaped with my genitals!"
- `NPC_BEANIES_BEANIES_LAB_INTRO_5`: "[m:pondering]Luckily I keep my collection locked in a metal briefcase... <br/> [m:angry]But that's beside the point."
- `NPC_BEANIES_BEANIES_LAB_INTRO_6`: "[m:veryangry]YOU SCREWED IT ALL UP! YOU, YOU PINHEADED IGNORAMUS! YOU BUCKTOOTHED JACKASS!"
- `NPC_BEANIES_BEANIES_LAB_INTRO_7`: "[m:angry]Where am I supposed to go to the bathroom!? <br/> [m:shocked]What do I even wipe with!?"
- `NPC_BEANIES_BEANIES_LAB_INTRO_8`: "[m:scared][s:.5]This isn't happening, this isn't happening...[/s]"
- `NPC_BEANIES_BEANIES_LAB_INTRO_9`: "[m:veryangry]YOU RUINED ME, <br/> YOU TITANIC TURD! <br/> YOU RUINED MY FREAKIN' LIFE!"
- `NPC_BEANIES_BEANIES_LAB_INTRO_10`: "[m:angry]ARE YOU HAPPY WITH YOURSELF!?!!?"
- `NPC_BEANIES_BEANIES_LAB_INTRO_11`: "[m:veryangry]THATS IT! IM DONE WITH YOUR BULLSHIT!  THIS IS THE FINAL STRAW!"
- `NPC_BEANIES_BEANIES_LAB_INTRO_12`: "[m:veryangry]NOW LEAVE AND NEVER COME BACK!"
- `NPC_BEANIES_BEANIES_LAB_INTRO_13`: "[m:default]OK, so I've had time to calm down and think a bit... This can be fixed..."
- `NPC_BEANIES_BEANIES_LAB_INTRO_14`: "[m:happy]I know you are a simple-minded dullard, <br/> [m:winking]so I'll talk slowly."
- `NPC_BEANIES_BEANIES_LAB_INTRO_15`: "[m:default]I need you to clear out my lab."
- `NPC_BEANIES_BEANIES_LAB_INTRO_16`: "[m:happy]There is a device in there that can undo all of your screw ups and get me back on top!"
- `NPC_BEANIES_BEANIES_LAB_INTRO_17`: "[m:default]You'll know it when you see it."
- `NPC_BEANIES_BEANIES_LAB_INTRO_18`: "[m:pondering][s:.7]Who am I kidding? <br/> You wouldn't know your ass <br/> from a headless howler monkey.[/s]"
- `NPC_BEANIES_BEANIES_LAB_INTRO_19`: "[m:questioning]There is a big metal chamber at the very back of my lab.  Go there and press the shiny red button."
- `NPC_BEANIES_BEANIES_LAB_INTRO_20`: "[m:angry]..."
- `NPC_BEANIES_BEANIES_LAB_INTRO_21`: "[m:bored]Find metal box."
- `NPC_BEANIES_BEANIES_LAB_INTRO_22`: "Press red button."
- `NPC_BEANIES_BEANIES_LAB_INTRO_23`: "[m:angry]Got it?!"
- `NPC_BEANIES_BEANIES_LAB_INTRO_24`: "[m:veryangry]Now GO!"
- `NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_1`: "[m:shocked]It's not working?! [m:questioning]Someone must have eaten the power source... hmmm"
- `NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_2`: "[m:pondering]So to get the time machine back up and running we are going to need a new power source."
- `NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_3`: "[m:default]Yeah, it's a time machine. We have been using it this whole time, [m:winking]you just don't remember it in this timeline."
- `NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_4`: "[m:paranoid]..."
- `NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_5`: "[m:default]Well it's busted now. [m:angry]Your fault, so it's your job to fix it!"
- `NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_6`: "[m:pondering]We just need a new piezoelectric generator or something like one..."
- `NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_7`: "[m:veryhappy]I'VE GOT IT!"
- `NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_8`: "[m:shocked]Legend has it, an immortal is dwelling directly under our feet! In this place called the "Throbbing Domain", he's been locked down there for centuries!"
- `NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_9`: "[m:winking]That thing's heart would make a perfect source of power!"
- `NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_10`: "[m:happy]Here, take this cooler. It has regenerative properties and should keep the heart from decaying once it's removed."
- `NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_11`: "[m:scared]Uuuhh, it also may revive anything else that dies around it, [m:winking]so maybe make sure to eviscerate your enemies?"
- `NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_12`: "[m:angry]Now go get that heart so I can undo your mistakes!"
- `NPC_BEANIES_BEANIES_TIMEMACHINE_2_1`: "[m:scared]Just so you know, that smell isn't me..."
- `NPC_BEANIES_BEANIES_TIMEMACHINE_2_2`: "[m:default]It's my excrement receptacle."
- `NPC_BEANIES_BEANIES_TIMEMACHINE_2_3`: "[m:questioning]As a fellow hobo I'm sure you know, us bums defecate in bags..."
- `NPC_BEANIES_BEANIES_TIMEMACHINE_2_4`: "[m:bored]This is my life now."
- `NPC_BEANIES_BEANIES_TIMEMACHINE_2_5`: "[m:spacedout]Bag defecation, thieving and copious amounts of pills... [m:bored]Such is the life of a vagrant."
- `NPC_BEANIES_BEANIES_TIMEMACHINE_2_6`: "[m:default]But i digress. <br/> I see you have a cooler with the still beating heart of our lord and savior, super meat ball."
- `NPC_BEANIES_BEANIES_TIMEMACHINE_2_7`: "[m:happy]Good work!"
- `NPC_BEANIES_BEANIES_TIMEMACHINE_2_8`: "Now just go back to my time machine, install the heart and hop inside."
- `NPC_BEANIES_BEANIES_TIMEMACHINE_2_9`: "[m:pondering]I'm unsure of its current settings... <br/> but it should send you somewhere into the past."
- `NPC_BEANIES_BEANIES_TIMEMACHINE_2_10`: "[m:happy]Maybe even before you existed! Crazy, huh? <br/> You could meet your great great uncle grandpa!"
- `NPC_BEANIES_BEANIES_TIMEMACHINE_2_11`: "[m:scared]Oh, uh.. <br/> but there's a thing I gotta tell you about..."
- `NPC_BEANIES_BEANIES_TIMEMACHINE_2_12`: "[m:default]You've probably never heard of it, but there is this theory I came up with called the butterfly effect."
- `NPC_BEANIES_BEANIES_TIMEMACHINE_2_13`: "[m:pondering]It's something like, if you kill a butterfly in the past, your mom dies? <br/> I can't remember the details right now..."
- `NPC_BEANIES_BEANIES_TIMEMACHINE_2_14`: "[m:default]The point I'm trying to make is, if you change something in the past, it's bound to affect the future in some way..."
- `NPC_BEANIES_BEANIES_TIMEMACHINE_2_15`: "[m:happy]So just smash the hell out of as many things in the past as possible!"
- `NPC_BEANIES_BEANIES_TIMEMACHINE_2_16`: "[m:pondering]I assume at some point, the chaos you cause will end up changing our current timeline..."
- `NPC_BEANIES_BEANIES_TIMEMACHINE_2_17`: "[m:angry]Hopefully enough that I'm back in my lab, defecating into something that flushes... <br/> [s:.7]Or at least swallows.[/s]"
- `NPC_BEANIES_BEANIES_TIMEMACHINE_2_18`: "[m:bored]I'll ping you when I notice a change... <br/> 'Till then, I'll just be sitting here."
- `NPC_BEANIES_BEANIES_TIMEMACHINE_2_19`: "[m:happy]I've taken up drinking and it's pretty nice."
- `NPC_BEANIES_BEANIES_TIMEMACHINE_2_20`: "[m:spacedout]Kinda feels like a time machine in itself honestly..."
- `NPC_BEANIES_BEANIES_JURASSIC_INTRO_1`: "[m:pondering]Well it's pretty obvious that killing cavemen isn't helping us at all..."
- `NPC_BEANIES_BEANIES_JURASSIC_INTRO_2`: "[m:happy]We need to go further! <br/> Back to a time before man!"
- `NPC_BEANIES_BEANIES_JURASSIC_INTRO_3`: "[m:questioning]Just set the little dial thingy to 0 and see where you end up."
- `NPC_BEANIES_BEANIES_JURASSIC_INTRO_4`: "[m:winking]When you make it to your destination, just hop out and start smashin' stuff!"
- `NPC_BEANIES_BEANIES_JURASSIC_INTRO_5`: "[m:veryhappy]For the future of humanity!"
- `NPC_BEANIES_BEANIES_FUTURE_INTRO_1`: "[m:angry]Yeah well I guess your dumb time machine idea didn't work..."
- `NPC_BEANIES_BEANIES_FUTURE_INTRO_2`: "[m:default]It's pretty clear our answers don't lie in the past, but in the future! Obviously!"
- `NPC_BEANIES_BEANIES_FUTURE_INTRO_3`: "[m:questioning]Why you thought going into the past would change a damn thing is beyond me..."
- `NPC_BEANIES_BEANIES_FUTURE_INTRO_4`: "[m:default]Listen, just set the machine to <br/> THE FUTURE <br/> and hop inside."
- `NPC_BEANIES_BEANIES_FUTURE_INTRO_5`: "[m:default]Then find a phone book and look me up.  I'll no doubt be extremely wealthy and have invented some way to fix our current issues."
- `NPC_BEANIES_BEANIES_FUTURE_INTRO_6`: "[m:pondering]In fact, when you find future me, just bring me back to our timeline. Then the two of us can put our brains together and [m:veryhappy]really fuck shit up!"
- `NPC_BEANIES_BEANIES_FUTURE_INTRO_7`: "[m:shocked]Fix shit up..."
- `NPC_BEANIES_BEANIES_FUTURE_INTRO_8`: "[m:angry]Fix up the shit that you did!"
- `NPC_BEANIES_BEANIES_FUTURE_INTRO_9`: "[m:happy]God, these pills got my lips slapping today don't they?"
- `NPC_BEANIES_BEANIES_FUTURE_INTRO_10`: "[m:questioning]What was I saying?"
- `NPC_BEANIES_BEANIES_FUTURE_INTRO_11`: "[m:default]Oh yeah, go get me more drugs!"
- `NPC_BEANIES_BEANIES_SEEFUTURE_1`: "[m:shocked]What do you mean you couldn't find future me!?"
- `NPC_BEANIES_BEANIES_SEEFUTURE_2`: "[m:questioning]Nazis?!"
- `NPC_BEANIES_BEANIES_SEEFUTURE_3`: "[m:angry]What the hell are you talking about? <br/> You sound paranoid."
- `NPC_BEANIES_BEANIES_SEEFUTURE_4`: "[m:scared]Unless..."
- `NPC_BEANIES_BEANIES_SEEFUTURE_5`: "[m:veryangry]THEY STOLE MY IDEAS!"
- `NPC_BEANIES_BEANIES_SEEFUTURE_6`: "Those bastards! <br/> [m:angry]You gotta stoop pretty low to steal the ideas of a freakin' street urchin..."
- `NPC_BEANIES_BEANIES_SEEFUTURE_7`: "[m:veryangry]The gall! <br/> If you see the guy in charge you tell him, you point right at his thief face and you say "THIEF!""
- `NPC_BEANIES_BEANIES_SEEFUTURE_8`: "[m:angry]No, you call him a [m:veryangry]Rat Fink! [m:angry]and furrow your brow when you do it so he knows you mean it!"
- `NPC_BEANIES_BEANIES_SEEFUTURE_9`: "[m:angry]No one steals my ideas and gets away with it! Next time you kill him, say something like..."
- `NPC_BEANIES_BEANIES_SEEFUTURE_10`: "[m:winking]Dr. Beanies sends his regards!"
- `NPC_BEANIES_BEANIES_SEEFUTURE_11`: "[m:angry]And in case hes confused on who I am, you give him my address!"
- `NPC_BEANIES_BEANIES_SEEFUTURE_12`: "1984 Demikhov Dr. Boon County U.S Fuckin' A!"
- `NPC_BEANIES_BEANIES_SEEFUTURE_13`: "[m:default]..."
- `NPC_BEANIES_BEANIES_SEEFUTURE_14`: "[m:sad]By the way, do you have any change on you? <br/> I need it for gas money."
- `NPC_BEANIES_BEANIES_SEEFUTURE_15`: "[m:happy]I'm huffing gasoline now."
- `NPC_BEANIES_BEANIES_THEEND_INTRO_1`: "[m:angry]OK, so forget about the future, the future sucks!"
- `NPC_BEANIES_BEANIES_THEEND_INTRO_2`: "[m:veryhappy]This time we need to go further, we gotta see how it all ends!"
- `NPC_BEANIES_BEANIES_THEEND_INTRO_3`: "[m:pondering]I assume just holding down 0 for a few minutes should get us there..."
- `NPC_BEANIES_BEANIES_THEEND_INTRO_4`: "[m:happy]Yeah, that's gotta work."
- `NPC_BEANIES_BEANIES_THEEND_INTRO_5`: "[m:veryhappy]TO THE END!"
- `NPC_BEANIES_BEANIES_SEETHEEND_1`: "[m:shocked]What? Why are you looking at me like that?"
- `NPC_BEANIES_BEANIES_SEETHEEND_2`: "[m:veryangry]If you think I had anything to do with the world ending buddy..."
- `NPC_BEANIES_BEANIES_SEETHEEND_3`: "[m:angry]Like seriously think about it.  If anything, you probably did it!"
- `NPC_BEANIES_BEANIES_SEETHEEND_4`: "Don't you realize the risks you are taking manipulating time?"
- `NPC_BEANIES_BEANIES_SEETHEEND_5`: "[m:paranoid]..."
- `NPC_BEANIES_BEANIES_SEETHEEND_6`: "[m:default]Who are they going to believe anyway? An old disheveled hobo?"
- `NPC_BEANIES_BEANIES_SEETHEEND_7`: "[m:happy]Or a reanimated dead woman with an army of cats who can time travel?"
- `NPC_BEANIES_BEANIES_SEETHEEND_8`: "[m:winking]My hands are clean, buddy!"
- `NPC_BEANIES_BEANIES_SEETHEEND_9`: "[m:pondering]..."
- `NPC_BEANIES_BEANIES_SEETHEEND_10`: "[m:default]Figuratively of course, obviously my hands are filthy right now."
- `NPC_BEANIES_BEANIES_SEETHEEND_11`: "[m:veryangry]BECAUSE OF YOU!"
- `NPC_BEANIES_BEANIES_SEETHEEND_12`: "[m:angry]Fix this!!"
- `NPC_BEANIES_BEANIES_TERMINATOR1_DEFEAT_1`: "[m:default]So check this out."
- `NPC_BEANIES_BEANIES_TERMINATOR1_DEFEAT_2`: "[m:questioning]You know that death bot Hitler sent from the future to kill you?"
- `NPC_BEANIES_BEANIES_TERMINATOR1_DEFEAT_3`: "[m:veryhappy]It was riddled with science!"
- `NPC_BEANIES_BEANIES_TERMINATOR1_DEFEAT_4`: "[m:default]I was able to hack together what us men of science call, an antenna."
- `NPC_BEANIES_BEANIES_TERMINATOR1_DEFEAT_5`: "Now I won't bore you with technical mumbo-jumbo."
- `NPC_BEANIES_BEANIES_TERMINATOR1_DEFEAT_6`: "[m:happy]But this thing might be our ticket out of this pee-pee soaked heck hole!"
- `NPC_BEANIES_BEANIES_TERMINATOR1_DEFEAT_7`: "[m:default]Just take this thing to that active volcano in the Jurassic period."
- `NPC_BEANIES_BEANIES_TERMINATOR1_DEFEAT_8`: "[m:winking]Leave it there and I'll do the rest."
- `NPC_BEANIES_BEANIES_TERMINATOR1_DEFEAT_9`: "[m:veryhappy]Oh man, I've got such a huge theory right now, I feel light headed!"
- `NPC_BEANIES_BEANIES_TERMINATOR1_DEFEAT_10`: "[m:happy]GO! <br/> Get on it!"
- `NPC_BEANIES_BEANIES_TERMINATOR2_DEFEAT_1`: "[m:questioning]Remember that liquid metal Nazi from the future you just killed?"
- `NPC_BEANIES_BEANIES_TERMINATOR2_DEFEAT_2`: "[m:happy]Well I made another antenna out of its juices!"
- `NPC_BEANIES_BEANIES_TERMINATOR2_DEFEAT_3`: "[m:default]Don't ask how.  God knows you'd probably die of an aneurysm even attempting to comprehend it..."
- `NPC_BEANIES_BEANIES_TERMINATOR2_DEFEAT_4`: "[m:happy]So just go take this new antenna and attach it to the glowing orb at the end of time."
- `NPC_BEANIES_BEANIES_TERMINATOR2_DEFEAT_5`: "[m:pondering]We just need a good amplifier to really get the ball rolling on this plan of mine."
- `NPC_BEANIES_BEANIES_TERMINATOR2_DEFEAT_6`: "[m:happy]You think they hand out the Nobel Prize in the afterlife?"
- `NPC_BEANIES_BEANIES_TERMINATOR2_DEFEAT_7`: "[m:winking]I guess we will just have to find out, won't we!?"
- `NPC_BEANIES_BEANIES_HITLER3_1`: "[m:default]So i have good news and bad news..."
- `NPC_BEANIES_BEANIES_HITLER3_2`: "[m:scared]The bad news is Hitler is back with a small army of robotic cats to destroy you."
- `NPC_BEANIES_BEANIES_HITLER3_3`: "[m:veryhappy]The good news is, I've invented a bucket with a hole at the bottom!"
- `NPC_BEANIES_BEANIES_HITLER3_4`: "[m:pondering]It's kind of like a toilet meets a chair..."
- `NPC_BEANIES_BEANIES_HITLER3_5`: "[m:default]When you want to make brown you just sit on the top of the bucket and push."
- `NPC_BEANIES_BEANIES_HITLER3_6`: "[m:happy]Once you are done you just stand up, remove the bucket and leave the refuse on the floor where it landed."
- `NPC_BEANIES_BEANIES_HITLER3_7`: "[m:winking]Pretty neat, huh?"
- `NPC_BEANIES_BEANIES_HITLER3_8`: "[m:pondering]I'm working on installing this, well I guess it's like a putty trowel..."
- `NPC_BEANIES_BEANIES_HITLER3_9`: "[m:happy]I like to call it <br/> "Trowlet Paper"... It's installed at the lip of the bucket and you just kinda..."
- `NPC_BEANIES_BEANIES_HITLER3_10`: "[m:whispering]Lean and scrape... It's this kind of butt-dragging motion..."
- `NPC_BEANIES_BEANIES_HITLER3_11`: "[m:happy]It's a work in progress but yeah, you could say things are really coming up Beanies these days!"
- `NPC_BEANIES_BEANIES_HITLER3_12`: "[m:winking]Now if you don't mind, it's time to give it another test run!"
- `NPC_BEANIES_BEANIES_HITLER3_DEFEAT_1`: "[m:happy]We did it! <br/> Hitler is dead once again!"
- `NPC_BEANIES_BEANIES_HITLER3_DEFEAT_2`: "[m:veryhappy]U.S.A. U.S.A. U.S.A.!"
- `NPC_BEANIES_BEANIES_HITLER3_DEFEAT_3`: "[m:whispering]But i digress..."
- `NPC_BEANIES_BEANIES_HITLER3_DEFEAT_4`: "[m:default]I don't mean to outdo you once again, but it's time..."
- `NPC_BEANIES_BEANIES_HITLER3_DEFEAT_5`: "[m:happy]Time to bask in the glory of the great Amplifier!"
- `NPC_BEANIES_BEANIES_HITLER3_DEFEAT_6`: "This little baby not only boosts signals, but when attached to a large enough power source it can do so through time!"
- `NPC_BEANIES_BEANIES_HITLER3_DEFEAT_7`: "[m:questioning]Remember those antennas I had you place in the past and future? [m:mocking]Well spoiler! There was a reason."
- `NPC_BEANIES_BEANIES_HITLER3_DEFEAT_8`: "[m:default]If I can boost the signal on those things high enough, they should connect..."
- `NPC_BEANIES_BEANIES_HITLER3_DEFEAT_9`: "[m:veryhappy]Revealing... <br/> THE INFINITE!!!!!"
- `NPC_BEANIES_BEANIES_HITLER3_DEFEAT_10`: "[m:happy]What is the Infinite you ask? Well that is for me to know, and for you to find out!"
- `NPC_BEANIES_BEANIES_HITLER3_DEFEAT_11`: "[m:default]So go attach this amplifier to that demi-god in the Rift."
- `NPC_BEANIES_BEANIES_HITLER3_DEFEAT_12`: "That freak should have more than enough juice to get us where we need to be..."
- `NPC_BEANIES_BEANIES_HITLER3_DEFEAT_13`: "[m:happy]God, I'm good..."
- `NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_1`: "[m:sad]So the moment you got back into the time machine the Creator started regenerating..."
- `NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_2`: "[m:pondering]Probably should have expected as much..."
- `NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_3`: "[m:questioning]Well, there has got to be some way of ending this arrogant prick's tyranny..."
- `NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_4`: "[m:shocked]Wait..."
- `NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_5`: "[m:pondering]Wait just a goddamn minute..."
- `NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_6`: "[m:happy]Yes... yes, I HAVE IT!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_7`: "[m:veryhappy]NUKE THE FETAL CHRIST CHILD!!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_8`: "[m:veryangry]We build a nuke so powerful that not even an atom will remain!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_9`: "[m:default]Here, I just happen to have kept a jar of radioactive liquid... <br/> Just in case."
- `NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_10`: "[m:pondering]Take it. <br/> I'll need you to mix the fluid with the life essence of another eternal..."
- `NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_11`: "[m:default]That king you stole the heart from could work.  Just mix in his blood and bring it here."
- `NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_12`: "[m:happy]Don't worry, we will beat this "Supreme Being" or die trying!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_13`: "[m:veryhappy]GODSPEED!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_2_1`: "[m:veryhappy]Great! <br/> Radioactive demi-blood!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_2_2`: "[m:pondering]But it needs something else... A little bit of chaos to shake things up!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_2_3`: "[m:default]Take it with you into the Rift and slice off a piece of that giant head."
- `NPC_BEANIES_BEANIES_BOMBQUEST_2_4`: "[m:questioning]The vibrations from an extra dimensional being like that should keep our concoction in a perpetual state of flux."
- `NPC_BEANIES_BEANIES_BOMBQUEST_2_5`: "[m:happy]Get that mixture to me ASAP and I'll build a bomb so big, Oppenheimer will start spinning in his grave!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_2_6`: "[m:veryhappy]Now go! <br/> Into the Rift with ya!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_3_1`: "[m:happy]Oh yes, perfect... <br/> This little brew is exactly what the doctor ordered!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_3_2`: "[m:default]I just pop it inside this nuclear bomb and viola!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_3_3`: "[m:veryhappy]THE GOD KILLER!!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_3_4`: "[m:pondering]Or maybe the <br/> "Time Ender"? <br/> I dunno, what sounds cooler?"
- `NPC_BEANIES_BEANIES_BOMBQUEST_3_5`: "[m:questioning]It needs to convey that it kills God, but should also insinuate it taking everything else with it..."
- `NPC_BEANIES_BEANIES_BOMBQUEST_3_6`: "[m:bored]Bombageddon? <br/> the Backdoor Boom Boom?... <br/> eh.."
- `NPC_BEANIES_BEANIES_BOMBQUEST_3_7`: "[m:default]Whatever.  I'll come up with the name later..."
- `NPC_BEANIES_BEANIES_BOMBQUEST_3_8`: "[m:happy]I'm adding a little hologram projector to the bomb, so once you are ready to detonate..."
- `NPC_BEANIES_BEANIES_BOMBQUEST_3_9`: "[m:winking]I'll chime in and do this little action hero one liner I've prepared."
- `NPC_BEANIES_BEANIES_BOMBQUEST_3_10`: "[m:happy]See you soon!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFRADIATION_1`: "[m:angry]Well you failed me again... <br/> Don't worry at this point, I'm getting used to it."
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFRADIATION_2`: "[m:happy]No one said killing God was going to be easy!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFRADIATION_3`: "[m:default]Now here's that jar of radioactive fluid again! <br/> Don't worry, I have like over 100 drums of it scattered around town."
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFRADIATION_4`: "[m:winking]Plenty more where that came from!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFRADIATION_5`: "[m:questioning]Take it to the king in the Throbbing Domain and mix in some of his blood."
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFRADIATION_6`: "[m:default]Bring it back and I'll get you moving to your final destination."
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFRADIATION_7`: "[m:veryhappy]GO GO GO! <br/> Humanity depends on you!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_1`: "[m:veryangry]YOU LOST THE JAR OF RADIOACTIVE BLOOD!?"
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_2`: "[m:angry]HOW!? HOW CAN YOU LOSE A JAR!?"
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_3`: "[m:shocked]Oh God... <br/> You didn't... <br/> Where did you put it?!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_4`: "[m:paranoid]..."
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_5`: "[m:happy]Ohhhhhhh..."
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_6`: "[m:default]You lost it when your cats died! <br/> Well that's better I guess..."
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_7`: "[m:paranoid]I thought for a second there you were one of those "Perverts"[m:grossedout]."
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_8`: "[m:default]Lucky for you, I have yet another jar of radioactive fluid!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_9`: "[m:bored]..."
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_10`: "[m:pondering]Wait a minute... <br/> You aren't just scamming me for jars are you?"
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_11`: "[m:angry]If I even see one video pop up online involving ANY of my jars..."
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_12`: "[m:veryangry]There will be hell to pay!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_13`: "[m:winking]Good luck!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFCHAOS_1`: "[m:shocked]Hey... <br/> Wheres the jar of chaos?"
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFCHAOS_2`: "[m:paranoid]You didn't drink it did you?!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFCHAOS_3`: "[m:angry]Cuz' you gotta share if you are gonna be doing that! <br/> I mean, it's my jar so I get dibs."
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFCHAOS_4`: "[m:winking]Daddy gets a sip-sip, OK?"
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFCHAOS_5`: "[m:default]Anyway here, <br/> take another jar and go get us more juice!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFCHAOS_6`: "[m:shocked]Or wait.. no. <br/> No we are supposed to be killing God!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFCHAOS_7`: "[m:confused]You got my brain all focused on that damn purple drank!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFCHAOS_8`: "[m:angry]Put down the jar and keep your eye on the prize!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFCHAOS_9`: "[m:default]Take this jar of radioactive fluid and let's end all this!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFCHAOS_10`: "[m:happy] Together!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_1`: "[m:scared]Uh oh..."
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_2`: "[m:questioning]I can't imagine God is going to take kindly to an attempted assassination..."
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_3`: "[m:bored]Pppfft, who am I kidding?  That guys' an idiot!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_4`: "[m:angry]Think about it.  Any "Creator" who puts a pleasure button inside a mans poop-shoot can't be that smart can he?"
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_5`: "I mean who does that?!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_6`: "[m:pondering]So tempting, yet just out of reach..."
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_7`: "..."
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_8`: "[m:default]What I'm trying to say is that God is just as much of a halfwit as you are! <br/> So we are probably safe to try this again."
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_9`: "Here..."
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_10`: "[m:happy]Take this jar of radioactive fluid and do all that stuff again."
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_11`: "[m:angry]BUT THIS TIME DON'T SCREW UP!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_12`: "[m:winking]Good luck!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_AMNESIA_1`: "[m:shocked]What do you mean you thought I died?"
- `NPC_BEANIES_BEANIES_BOMBQUEST_AMNESIA_2`: "[m:veryhappy]Jesus, you must be as drunk as I am!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_AMNESIA_3`: "[m:shocked]What!? <br/> Steven?!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_AMNESIA_4`: "[m:pondering]Nope, Doesn't ring a bell..."
- `NPC_BEANIES_BEANIES_BOMBQUEST_AMNESIA_5`: "[m:happy]Now can you please leave me alone? <br/> I'm working on an invention that will change the world!"
- `NPC_BEANIES_BEANIES_BOMBQUEST_AMNESIA_6`: "[m:winking]I don't wanna spoil it... <br/> But involves a glass jar!"
- `NPC_BEANIES_BEANIES_ILOVEYOU_1`: "[m:inlove]I love you... I love you!"
- `NPC_BEANIES_BEANIES_ILOVEYOU_2`: "[m:happy]I LOVE YOU VERY MUCH!"
- `NPC_BEANIES_BEANIES_ILOVEYOU_3`: "[m:veryhappy]I LOVE YOU VERY VERY VERY MUCH!"
- `NPC_BEANIES_BEANIES_SCREENSHAKE_TEST_1`: "[m:default]Hey, guess what?"
- `NPC_BEANIES_BEANIES_SCREENSHAKE_TEST_2`: "[m:shocked]!!!"
- `NPC_BEANIES_BEANIES_SCREENSHAKE_TEST_3`: "[m:default]WAHT THE HELL WAS EVEN THAT?"
- `NPC_BEANIES_BEANIES_SCREENSHAKE_TEST_4`: "You can also trigger it [ss]LIKE THIS!! MUAHAHAHA"
- `NPC_BEANIES_BEANIES_SCREENSHAKE_TEST_5`: "Or even [ss:100][m:veryangry]SUPER CRAZY LIKE TOO!"
- `NPC_BEANIES_BEANIES_SCREENSHAKE_TEST_6`: "Hey did you hear that? What about [sfx:PickupCoin].[sfx:PickupCoin].[sfx:PickupCoin].[sfx:PickupCoin]. THIS???"
- `NPC_BEANIES_BEANIES_SCREENSHAKE_TEST_7`: "OR THIS? [sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1][sfx:PickupCoin][pause:1] that's a lot of coins."

```
sequences {
	
	unprompted {
		do_random_sequence [unprompted1, unprompted2, unprompted3, unprompted4, unprompted5, unprompted6]
	}
	unprompted1 {
		dialog NPC_BEANIES_UNPROMPTED1_1
	}
	unprompted2 {
		dialog NPC_BEANIES_UNPROMPTED2_1
		dialog NPC_BEANIES_UNPROMPTED2_2
	}
	unprompted3 {
		dialog NPC_BEANIES_UNPROMPTED3_1
		dialog NPC_BEANIES_UNPROMPTED3_2
		dialog NPC_BEANIES_UNPROMPTED3_3
	}
	unprompted4 {
		dialog NPC_BEANIES_UNPROMPTED4_1
	}
	unprompted5 {
		dialog NPC_BEANIES_UNPROMPTED5_1
		dialog NPC_BEANIES_UNPROMPTED5_2
	}
	unprompted6 {
		dialog NPC_BEANIES_UNPROMPTED6_1
		dialog NPC_BEANIES_UNPROMPTED6_2
		dialog NPC_BEANIES_UNPROMPTED6_3
	}

	also {
		dialog NPC_BEANIES_ALSO_1
	}

	beanies_begin_accepting_cats {
		dialog NPC_BEANIES_BEANIES_BEGIN_ACCEPTING_CATS_1
		set_state closeup
		dialog NPC_BEANIES_BEANIES_BEGIN_ACCEPTING_CATS_2
		set_state verycloseup
		dialog NPC_BEANIES_BEANIES_BEGIN_ACCEPTING_CATS_3
		set_state idle
		dialog NPC_BEANIES_BEANIES_BEGIN_ACCEPTING_CATS_4
		dialog NPC_BEANIES_BEANIES_BEGIN_ACCEPTING_CATS_5
		set_state closeup
		dialog NPC_BEANIES_BEANIES_BEGIN_ACCEPTING_CATS_6
		dialog NPC_BEANIES_BEANIES_BEGIN_ACCEPTING_CATS_7
		begin_accepting_cats beanies
	}

	beanies_quests_intro {
		dialog NPC_BEANIES_BEANIES_QUESTS_INTRO_1
		set_state closeup
		dialog NPC_BEANIES_BEANIES_QUESTS_INTRO_2
		set_state idle
		dialog NPC_BEANIES_BEANIES_QUESTS_INTRO_3
		dialog NPC_BEANIES_BEANIES_QUESTS_INTRO_4
		get npc_reward //this one will generate the quest item
		gather_questitem_info newest
		do_sidequest_sequence beaniesquest_intro //then this one will forward to the correct "quest item intro" sequence for the item just generated
	}
	beanies_quests_repeat {
		set_state verycloseup
		dialog NPC_BEANIES_BEANIES_QUESTS_REPEAT_1
		set_state closeup
		dialog NPC_BEANIES_BEANIES_QUESTS_REPEAT_2
		set_state idle
		dialog NPC_BEANIES_BEANIES_QUESTS_REPEAT_3
		get npc_reward //this one will generate the quest item
		gather_questitem_info newest
		do_sidequest_sequence beaniesquest_intro //then this one will forward to the correct "quest item intro" sequence for the item just generated
	}


	beanies_quest_complete {
		gather_questitem_info success
		do_sidequest_sequence beaniesquest_complete
	}
	beanies_quest_fail {
		gather_questitem_info fail
		do_sidequest_sequence beaniesquest_fail
	}

	//item intros / conclusions
	beaniesquest_intro_PersuasionDevice {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PERSUASIONDEVICE_1
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PERSUASIONDEVICE_2
		set_state zoomedout
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PERSUASIONDEVICE_3
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PERSUASIONDEVICE_4
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PERSUASIONDEVICE_5
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PERSUASIONDEVICE_6
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PERSUASIONDEVICE_7
	}
	beaniesquest_complete_PersuasionDevice {
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSUASIONDEVICE_1
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSUASIONDEVICE_2
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSUASIONDEVICE_3
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSUASIONDEVICE_4
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSUASIONDEVICE_5
		get sidequest_reward
	}
	beaniesquest_fail_PersuasionDevice { //in fail states you only have {questitemname} and not {questreward} or {questdestination}
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PERSUASIONDEVICE_1
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PERSUASIONDEVICE_2
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PERSUASIONDEVICE_3
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PERSUASIONDEVICE_4
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PERSUASIONDEVICE_5
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PERSUASIONDEVICE_6
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PERSUASIONDEVICE_7
		get sidequest_fail
	}

	/* copy paste template for new items (paste iten name after the _, make sure theres no space tho!)
	beaniesquest_intro_ {
		//dialog go here
	}
	beaniesquest_complete_ {
		//dialog go here
		get sidequest_reward
	}
	beaniesquest_fail_ {
		//dialog go here
		get sidequest_fail
	}
	*/

	//item pool
	//MagicMirror
	beaniesquest_intro_MagicMirror {
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MAGICMIRROR_1
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MAGICMIRROR_2
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MAGICMIRROR_3
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MAGICMIRROR_4
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MAGICMIRROR_5
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MAGICMIRROR_6
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MAGICMIRROR_7
		set_state zoomedout
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MAGICMIRROR_8
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MAGICMIRROR_9
	}
	beaniesquest_complete_MagicMirror {
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MAGICMIRROR_1
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MAGICMIRROR_2
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MAGICMIRROR_3
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MAGICMIRROR_4
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MAGICMIRROR_5
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MAGICMIRROR_6
		get sidequest_reward
	}
	beaniesquest_fail_MagicMirror {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_MAGICMIRROR_1
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_MAGICMIRROR_2
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_MAGICMIRROR_3
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_MAGICMIRROR_4
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_MAGICMIRROR_5
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_MAGICMIRROR_6
		get sidequest_fail
	}
	
	//Chaos Device
	beaniesquest_intro_ChaosDevice {
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_CHAOSDEVICE_1
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_CHAOSDEVICE_2
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_CHAOSDEVICE_3
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_CHAOSDEVICE_4
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_CHAOSDEVICE_5
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_CHAOSDEVICE_6
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_CHAOSDEVICE_7

	}
	beaniesquest_complete_ChaosDevice {
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_CHAOSDEVICE_1
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_CHAOSDEVICE_2
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_CHAOSDEVICE_3
		get sidequest_reward
	}
	beaniesquest_fail_ChaosDevice {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_CHAOSDEVICE_1
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_CHAOSDEVICE_2
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_CHAOSDEVICE_3
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_CHAOSDEVICE_4
		set_state zoomedout
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_CHAOSDEVICE_5
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_CHAOSDEVICE_6
		get sidequest_fail
	}
	

	//MeStone
	beaniesquest_intro_MeStone {
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MESTONE_1
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MESTONE_2
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MESTONE_3
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MESTONE_4
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MESTONE_5
	}
	beaniesquest_complete_MeStone {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MESTONE_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MESTONE_2
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MESTONE_3
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MESTONE_4
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MESTONE_5 
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MESTONE_6
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MESTONE_7
		get sidequest_reward
	}
	beaniesquest_fail_MeStone {
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_MESTONE_1
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_MESTONE_2
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_MESTONE_3
		get sidequest_fail
	}

	//AngryFace
	beaniesquest_intro_AngryFace {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_ANGRYFACE_1
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_ANGRYFACE_2
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_ANGRYFACE_3
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_ANGRYFACE_4
	}
	beaniesquest_complete_AngryFace {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_ANGRYFACE_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_ANGRYFACE_2
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_ANGRYFACE_3
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_ANGRYFACE_4
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_ANGRYFACE_5
		get sidequest_reward
	}
	beaniesquest_fail_AngryFace {
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_ANGRYFACE_1
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_ANGRYFACE_2
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_ANGRYFACE_3
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_ANGRYFACE_4
		get sidequest_fail
	}

	//FartFace
	beaniesquest_intro_FartFace {
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_FARTFACE_1
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_FARTFACE_2
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_FARTFACE_3
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_FARTFACE_4
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_FARTFACE_5
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_FARTFACE_6
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_FARTFACE_7
	}
	beaniesquest_complete_FartFace {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_FARTFACE_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_FARTFACE_2
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_FARTFACE_3
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_FARTFACE_4
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_FARTFACE_5
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_FARTFACE_6
		get sidequest_reward
	}
	beaniesquest_fail_FartFace {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_FARTFACE_1
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_FARTFACE_2
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_FARTFACE_3
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_FARTFACE_4
		get sidequest_fail
	}

	//SpiderInjector
	beaniesquest_intro_SpiderInjector {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_SPIDERINJECTOR_1
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_SPIDERINJECTOR_2
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_SPIDERINJECTOR_3
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_SPIDERINJECTOR_4
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_SPIDERINJECTOR_5
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_SPIDERINJECTOR_6
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_SPIDERINJECTOR_7
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_SPIDERINJECTOR_8
	}
	beaniesquest_complete_SpiderInjector {
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_SPIDERINJECTOR_1
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_SPIDERINJECTOR_2
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_SPIDERINJECTOR_3
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_SPIDERINJECTOR_4
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_SPIDERINJECTOR_5
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_SPIDERINJECTOR_6
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_SPIDERINJECTOR_7
		get sidequest_reward
	}
	beaniesquest_fail_SpiderInjector {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_SPIDERINJECTOR_1
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_SPIDERINJECTOR_2
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_SPIDERINJECTOR_3
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_SPIDERINJECTOR_4
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_SPIDERINJECTOR_5
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_SPIDERINJECTOR_6
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_SPIDERINJECTOR_7
		get sidequest_fail
	}

	//PartyDetonator
	beaniesquest_intro_PartyDetonator {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PARTYDETONATOR_1
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PARTYDETONATOR_2
		set_state idle
        dialog NPC_BEANIES_BEANIESQUEST_INTRO_PARTYDETONATOR_3//todo randomize
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PARTYDETONATOR_4
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PARTYDETONATOR_5
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PARTYDETONATOR_6
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PARTYDETONATOR_7
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PARTYDETONATOR_8
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PARTYDETONATOR_9
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PARTYDETONATOR_10
		
	}
	beaniesquest_complete_PartyDetonator {
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTYDETONATOR_1//todo randomize
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTYDETONATOR_2
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTYDETONATOR_3
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTYDETONATOR_4
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTYDETONATOR_5
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTYDETONATOR_6
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTYDETONATOR_7
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTYDETONATOR_8
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTYDETONATOR_9
		get sidequest_reward
	}
	beaniesquest_fail_PartyDetonator {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PARTYDETONATOR_1
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PARTYDETONATOR_2
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PARTYDETONATOR_3
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PARTYDETONATOR_4
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PARTYDETONATOR_5
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PARTYDETONATOR_6
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PARTYDETONATOR_7
		get sidequest_fail
	}
	
	//The Airhorn
	beaniesquest_intro_AirHorn {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_AIRHORN_1
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_AIRHORN_2
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_AIRHORN_3
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_AIRHORN_4
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_AIRHORN_5
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_AIRHORN_6
		
	}
	beaniesquest_complete_AirHorn {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_2
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_3
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_4
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_5
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_6
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_7
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_8
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_9
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_AIRHORN_10
		get sidequest_reward
	}
	beaniesquest_fail_AirHorn {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_1
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_2
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_3
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_4
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_5 
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_6
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_7
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_8
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_9 
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_10
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_11
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_12
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_AIRHORN_13
		get sidequest_fail
	}

	//NuclearKnife
	beaniesquest_intro_NuclearKnife {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_NUCLEARKNIFE_1
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_NUCLEARKNIFE_2
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_NUCLEARKNIFE_3
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_NUCLEARKNIFE_4
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_NUCLEARKNIFE_5
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_NUCLEARKNIFE_6
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_NUCLEARKNIFE_7
		
	}
	beaniesquest_complete_NuclearKnife {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_NUCLEARKNIFE_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_NUCLEARKNIFE_2
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_NUCLEARKNIFE_3
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_NUCLEARKNIFE_4
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_NUCLEARKNIFE_5
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_NUCLEARKNIFE_6
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_NUCLEARKNIFE_7
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_NUCLEARKNIFE_8
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_NUCLEARKNIFE_9
		get sidequest_reward
	}
	beaniesquest_fail_NuclearKnife {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_NUCLEARKNIFE_1
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_NUCLEARKNIFE_2
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_NUCLEARKNIFE_3
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_NUCLEARKNIFE_4
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_NUCLEARKNIFE_5
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_NUCLEARKNIFE_6
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_NUCLEARKNIFE_7
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_NUCLEARKNIFE_8
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_NUCLEARKNIFE_9
		get sidequest_fail
	}
	
	//AnimalHands
	beaniesquest_intro_AnimalHands {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_ANIMALHANDS_1
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_ANIMALHANDS_2
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_ANIMALHANDS_3
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_ANIMALHANDS_4
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_ANIMALHANDS_5
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_ANIMALHANDS_6
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_ANIMALHANDS_7
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_ANIMALHANDS_8
		
	}
	beaniesquest_complete_AnimalHands {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_ANIMALHANDS_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_ANIMALHANDS_2
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_ANIMALHANDS_3
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_ANIMALHANDS_4
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_ANIMALHANDS_5
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_ANIMALHANDS_6
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_ANIMALHANDS_7
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_ANIMALHANDS_8
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_ANIMALHANDS_9
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_ANIMALHANDS_10
		get sidequest_reward
	}
	beaniesquest_fail_AnimalHands {
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_ANIMALHANDS_1
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_ANIMALHANDS_2
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_ANIMALHANDS_3
		get sidequest_fail
	}
	
	//TheLoner
	beaniesquest_intro_TheLoner {
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_THELONER_1
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_THELONER_2
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_THELONER_3
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_THELONER_4
		
	}
	beaniesquest_complete_TheLoner {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_THELONER_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_THELONER_2
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_THELONER_3
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_THELONER_4
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_THELONER_5
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_THELONER_6
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_THELONER_7
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_THELONER_8
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_THELONER_9
		get sidequest_reward
	}
	beaniesquest_fail_TheLoner {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_1
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_2
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_3
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_4
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_5
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_6
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_7
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_8
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_9
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_10
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_11
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_THELONER_12
		get sidequest_fail
	}
	
	//GlassCannon
	beaniesquest_intro_GlassCannon {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_GLASSCANNON_1
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_GLASSCANNON_2
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_GLASSCANNON_3
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_GLASSCANNON_4
		
	}
	beaniesquest_complete_GlassCannon {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_GLASSCANNON_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_GLASSCANNON_2
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_GLASSCANNON_3
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_GLASSCANNON_4
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_GLASSCANNON_5
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_GLASSCANNON_6
		get sidequest_reward
	}
	beaniesquest_fail_GlassCannon {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_GLASSCANNON_1
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_GLASSCANNON_2
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_GLASSCANNON_3
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_GLASSCANNON_4
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_GLASSCANNON_5
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_GLASSCANNON_6
		get sidequest_fail
	}
	
	//Stopwatch
	beaniesquest_intro_Stopwatch {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_STOPWATCH_1
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_STOPWATCH_2
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_STOPWATCH_3
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_STOPWATCH_4
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_STOPWATCH_5
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_STOPWATCH_6
		
	}
	beaniesquest_complete_Stopwatch {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_STOPWATCH_1
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_STOPWATCH_2
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_STOPWATCH_3
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_STOPWATCH_4
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_STOPWATCH_5
		get sidequest_reward
	}
	beaniesquest_fail_Stopwatch {
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_STOPWATCH_1
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_STOPWATCH_2
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_STOPWATCH_3
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_STOPWATCH_4
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_STOPWATCH_5
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_STOPWATCH_6
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_STOPWATCH_7
		get sidequest_fail
	}
	
	//FigLeaf
	beaniesquest_intro_FigLeaf {
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_FIGLEAF_1
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_FIGLEAF_2
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_FIGLEAF_3
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_FIGLEAF_4
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_FIGLEAF_5
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_FIGLEAF_6
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_FIGLEAF_7
		
	}
	beaniesquest_complete_FigLeaf {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_FIGLEAF_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_FIGLEAF_2
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_FIGLEAF_3
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_FIGLEAF_4
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_FIGLEAF_5
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_FIGLEAF_6
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_FIGLEAF_7
		get sidequest_reward
	}
	beaniesquest_fail_FigLeaf {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_FIGLEAF_1
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_FIGLEAF_2
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_FIGLEAF_3
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_FIGLEAF_4
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_FIGLEAF_5
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_FIGLEAF_6
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_FIGLEAF_7
		get sidequest_fail
	}
	
	//DiseaseJar
	beaniesquest_intro_DiseaseJar {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_DISEASEJAR_1
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_DISEASEJAR_2
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_DISEASEJAR_3
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_DISEASEJAR_4
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_DISEASEJAR_5
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_DISEASEJAR_6
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_DISEASEJAR_7
		
	}
	beaniesquest_complete_DiseaseJar {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_DISEASEJAR_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_DISEASEJAR_2
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_DISEASEJAR_3
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_DISEASEJAR_4
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_DISEASEJAR_5
		get sidequest_reward
	}
	beaniesquest_fail_DiseaseJar {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_DISEASEJAR_1
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_DISEASEJAR_2
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_DISEASEJAR_3
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_DISEASEJAR_4
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_DISEASEJAR_5
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_DISEASEJAR_6
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_DISEASEJAR_7
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_DISEASEJAR_8
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_DISEASEJAR_9
		get sidequest_fail
	}
	
	//HardPill
	beaniesquest_intro_HardPill {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_HARDPILL_1
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_HARDPILL_2
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_HARDPILL_3
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_HARDPILL_4
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_HARDPILL_5
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_HARDPILL_6
		
	}
	beaniesquest_complete_HardPill {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_HARDPILL_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_HARDPILL_2
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_HARDPILL_3
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_HARDPILL_4
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_HARDPILL_5
		get sidequest_reward
	}
	beaniesquest_fail_HardPill {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_HARDPILL_1
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_HARDPILL_2
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_HARDPILL_3
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_HARDPILL_4
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_HARDPILL_5
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_HARDPILL_6
		get sidequest_fail
	}
	
	//DimensionalDivider
	beaniesquest_intro_DimensionalDivider {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_DIMENSIONALDIVIDER_1
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_DIMENSIONALDIVIDER_2
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_DIMENSIONALDIVIDER_3
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_DIMENSIONALDIVIDER_4
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_DIMENSIONALDIVIDER_5
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_DIMENSIONALDIVIDER_6
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_DIMENSIONALDIVIDER_7
		
	}
	beaniesquest_complete_DimensionalDivider {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_DIMENSIONALDIVIDER_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_DIMENSIONALDIVIDER_2
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_DIMENSIONALDIVIDER_3
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_DIMENSIONALDIVIDER_4
		set_state zoomedout
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_DIMENSIONALDIVIDER_5
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_DIMENSIONALDIVIDER_6
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_DIMENSIONALDIVIDER_7
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_DIMENSIONALDIVIDER_8
		get sidequest_reward
	}
	beaniesquest_fail_DimensionalDivider {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_DIMENSIONALDIVIDER_1
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_DIMENSIONALDIVIDER_2
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_DIMENSIONALDIVIDER_3
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_DIMENSIONALDIVIDER_4
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_DIMENSIONALDIVIDER_5
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_DIMENSIONALDIVIDER_6
		get sidequest_fail
	}
	
	//Trapfest99
	beaniesquest_intro_Trapfest99 {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_TRAPFEST99_1
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_TRAPFEST99_2
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_TRAPFEST99_3
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_TRAPFEST99_4
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_TRAPFEST99_5
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_TRAPFEST99_6
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_TRAPFEST99_7
		
	}
	beaniesquest_complete_Trapfest99 {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_TRAPFEST99_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_TRAPFEST99_2
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_TRAPFEST99_3
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_TRAPFEST99_4
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_TRAPFEST99_5
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_TRAPFEST99_6
		get sidequest_reward
	}
	beaniesquest_fail_Trapfest99 {
		set_state set_state
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_TRAPFEST99_1
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_TRAPFEST99_2
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_TRAPFEST99_3
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_TRAPFEST99_4
		get sidequest_fail
	}
	
	//MysteriousDice
	beaniesquest_intro_MysteriousDice {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSDICE_1
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSDICE_2
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSDICE_3
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSDICE_4
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSDICE_5
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSDICE_6
		
	}
	beaniesquest_complete_MysteriousDice {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSDICE_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSDICE_2
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSDICE_3
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSDICE_4
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSDICE_5
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSDICE_6
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSDICE_7
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSDICE_8
		get sidequest_reward
	}
	beaniesquest_fail_MysteriousDice {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_MYSTERIOUSDICE_1
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_MYSTERIOUSDICE_2
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_MYSTERIOUSDICE_3
		set_state zoomedout
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_MYSTERIOUSDICE_4
		get sidequest_fail
	}
	
	//TheIOU
	beaniesquest_intro_TheIOU {
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_1
		set_state zoomedout
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_2
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_3
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_4
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_5
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_6
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_7
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_8
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_9
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_10
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_11
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_THEIOU_12
		
	}
	beaniesquest_complete_TheIOU {
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_THEIOU_1
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_THEIOU_2
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_THEIOU_3
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_THEIOU_4
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_THEIOU_5
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_THEIOU_6
		set_state zoomedout
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_THEIOU_7
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_THEIOU_8
		get sidequest_reward
	}
	beaniesquest_fail_TheIOU {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_THEIOU_1
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_THEIOU_2
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_THEIOU_3
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_THEIOU_4
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_THEIOU_5
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_THEIOU_6
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_THEIOU_7
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_THEIOU_8
		get sidequest_fail
	}
	
	//ExperimentalTreatment
	beaniesquest_intro_ExperimentalTreatment {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_EXPERIMENTALTREATMENT_1
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_EXPERIMENTALTREATMENT_2
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_EXPERIMENTALTREATMENT_3
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_EXPERIMENTALTREATMENT_4
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_EXPERIMENTALTREATMENT_5
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_EXPERIMENTALTREATMENT_6
		
	}
	beaniesquest_complete_ExperimentalTreatment {
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_EXPERIMENTALTREATMENT_1
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_EXPERIMENTALTREATMENT_2
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_EXPERIMENTALTREATMENT_3
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_EXPERIMENTALTREATMENT_4
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_EXPERIMENTALTREATMENT_5
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_EXPERIMENTALTREATMENT_6
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_EXPERIMENTALTREATMENT_7
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_EXPERIMENTALTREATMENT_8
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_EXPERIMENTALTREATMENT_9
		get sidequest_reward
	}
	beaniesquest_fail_ExperimentalTreatment {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_EXPERIMENTALTREATMENT_1
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_EXPERIMENTALTREATMENT_2
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_EXPERIMENTALTREATMENT_3
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_EXPERIMENTALTREATMENT_4
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_EXPERIMENTALTREATMENT_5
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_EXPERIMENTALTREATMENT_6
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_EXPERIMENTALTREATMENT_7
		get sidequest_fail
	}
	
	//MysteriousGlasses
	beaniesquest_intro_MysteriousGlasses {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSGLASSES_1
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSGLASSES_2
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSGLASSES_3
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSGLASSES_4
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSGLASSES_5
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MYSTERIOUSGLASSES_6
		
	}
	beaniesquest_complete_MysteriousGlasses {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSGLASSES_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSGLASSES_2
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSGLASSES_3
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSGLASSES_4
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSGLASSES_5
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSGLASSES_6
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MYSTERIOUSGLASSES_7
		get sidequest_reward
	}
	beaniesquest_fail_MysteriousGlasses {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_MYSTERIOUSGLASSES_1
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_MYSTERIOUSGLASSES_2
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_MYSTERIOUSGLASSES_3
		get sidequest_fail
	}
	
	//Redacted
	beaniesquest_intro_Redacted {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_REDACTED_1
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_REDACTED_2
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_REDACTED_3
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_REDACTED_4
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_REDACTED_5
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_REDACTED_6
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_REDACTED_7
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_REDACTED_8
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_REDACTED_9
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_REDACTED_10
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_REDACTED_11
		
	}
	beaniesquest_complete_Redacted {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_REDACTED_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_REDACTED_2
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_REDACTED_3
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_REDACTED_4
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_REDACTED_5
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_REDACTED_6
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_REDACTED_7
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_REDACTED_8
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_REDACTED_9
		get sidequest_reward
	}
	beaniesquest_fail_Redacted {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_REDACTED_1
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_REDACTED_2
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_REDACTED_3
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_REDACTED_4
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_REDACTED_5
		get sidequest_fail
	}
	
	//PartialLobotomy
	beaniesquest_intro_PartialLobotomy {
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PARTIALLOBOTOMY_1
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PARTIALLOBOTOMY_2
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PARTIALLOBOTOMY_3
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PARTIALLOBOTOMY_4
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PARTIALLOBOTOMY_5
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PARTIALLOBOTOMY_6
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PARTIALLOBOTOMY_7
		
	}
	beaniesquest_complete_PartialLobotomy {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTIALLOBOTOMY_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTIALLOBOTOMY_2
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTIALLOBOTOMY_3
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTIALLOBOTOMY_4
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PARTIALLOBOTOMY_5
		get sidequest_reward
	}
	beaniesquest_fail_PartialLobotomy {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PARTIALLOBOTOMY_1
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PARTIALLOBOTOMY_2
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PARTIALLOBOTOMY_3
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PARTIALLOBOTOMY_4
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PARTIALLOBOTOMY_5
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PARTIALLOBOTOMY_6
		get sidequest_fail
	}
	
	//UltraVision3000
	beaniesquest_intro_UltraVision3000 {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_ULTRAVISION3000_1
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_ULTRAVISION3000_2
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_ULTRAVISION3000_3
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_ULTRAVISION3000_4
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_ULTRAVISION3000_5
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_ULTRAVISION3000_6
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_ULTRAVISION3000_7
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_ULTRAVISION3000_8
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_ULTRAVISION3000_9
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_ULTRAVISION3000_10
		
	}
	beaniesquest_complete_UltraVision3000 {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_ULTRAVISION3000_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_ULTRAVISION3000_2
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_ULTRAVISION3000_3
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_ULTRAVISION3000_4
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_ULTRAVISION3000_5
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_ULTRAVISION3000_6
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_ULTRAVISION3000_7
		get sidequest_reward
	}
	beaniesquest_fail_UltraVision3000 {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_ULTRAVISION3000_1
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_ULTRAVISION3000_2
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_ULTRAVISION3000_3
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_ULTRAVISION3000_4
		get sidequest_fail
	}
	
	//ChadImplant
	beaniesquest_intro_ChadImplant {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_CHADIMPLANT_1
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_CHADIMPLANT_2
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_CHADIMPLANT_3
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_CHADIMPLANT_4
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_CHADIMPLANT_5
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_CHADIMPLANT_6
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_CHADIMPLANT_7
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_CHADIMPLANT_8
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_CHADIMPLANT_9
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_CHADIMPLANT_10
		
	}
	beaniesquest_complete_ChadImplant {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_CHADIMPLANT_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_CHADIMPLANT_2
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_CHADIMPLANT_3
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_CHADIMPLANT_4
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_CHADIMPLANT_5
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_CHADIMPLANT_6
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_CHADIMPLANT_7
		get sidequest_reward
	}
	beaniesquest_fail_ChadImplant {
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_CHADIMPLANT_1
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_CHADIMPLANT_2
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_CHADIMPLANT_3
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_CHADIMPLANT_4
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_CHADIMPLANT_5
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_CHADIMPLANT_6
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_CHADIMPLANT_7
		get sidequest_fail
	}
	
	//StorageLocker
	beaniesquest_intro_StorageLocker {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_STORAGELOCKER_1
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_STORAGELOCKER_2
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_STORAGELOCKER_3
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_STORAGELOCKER_4
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_STORAGELOCKER_5
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_STORAGELOCKER_6
		
	}
	beaniesquest_complete_StorageLocker {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_STORAGELOCKER_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_STORAGELOCKER_2
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_STORAGELOCKER_3
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_STORAGELOCKER_4
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_STORAGELOCKER_5
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_STORAGELOCKER_6
		get sidequest_reward
	}
	beaniesquest_fail_StorageLocker {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_STORAGELOCKER_1
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_STORAGELOCKER_2
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_STORAGELOCKER_3
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_STORAGELOCKER_4
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_STORAGELOCKER_5
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_STORAGELOCKER_6
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_STORAGELOCKER_7
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_STORAGELOCKER_8
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_STORAGELOCKER_9
		get sidequest_fail
	}
	
	//AI
	beaniesquest_intro_AI {
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_AI_1
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_AI_2
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_AI_3
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_AI_4
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_AI_5
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_AI_6
		set_state zoomedout
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_AI_7
		
	}
	beaniesquest_complete_AI {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_AI_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_AI_2
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_AI_3
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_AI_4
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_AI_5
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_AI_6
		set_state zoomedout
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_AI_7
		get sidequest_reward
	}
	beaniesquest_fail_AI {
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_AI_1
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_AI_2
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_AI_3
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_AI_4
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_AI_5
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_AI_6
		set_state zoomedout
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_AI_7
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_AI_8
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_AI_9
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_AI_10
		set_state zoomedout
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_AI_11
		get sidequest_fail
	}
	
	//RealityScrambler
	beaniesquest_intro_RealityScrambler {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_REALITYSCRAMBLER_1
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_REALITYSCRAMBLER_2
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_REALITYSCRAMBLER_3
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_REALITYSCRAMBLER_4
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_REALITYSCRAMBLER_5
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_REALITYSCRAMBLER_6
		
	}
	beaniesquest_complete_RealityScrambler {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_REALITYSCRAMBLER_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_REALITYSCRAMBLER_2
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_REALITYSCRAMBLER_3
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_REALITYSCRAMBLER_4
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_REALITYSCRAMBLER_5
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_REALITYSCRAMBLER_6
		get sidequest_reward
	}
	beaniesquest_fail_RealityScrambler {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_REALITYSCRAMBLER_1
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_REALITYSCRAMBLER_2
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_REALITYSCRAMBLER_3
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_REALITYSCRAMBLER_4
		get sidequest_fail
	}
	
	//BubbleBoy
	beaniesquest_intro_BubbleBoy {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_BUBBLEBOY_1
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_BUBBLEBOY_2
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_BUBBLEBOY_3
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_BUBBLEBOY_4
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_BUBBLEBOY_5
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_BUBBLEBOY_6
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_BUBBLEBOY_7
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_BUBBLEBOY_8
		
	}
	beaniesquest_complete_BubbleBoy {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_BUBBLEBOY_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_BUBBLEBOY_2
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_BUBBLEBOY_3
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_BUBBLEBOY_4
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_BUBBLEBOY_5
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_BUBBLEBOY_6
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_BUBBLEBOY_7
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_BUBBLEBOY_8
		get sidequest_reward
	}
	beaniesquest_fail_BubbleBoy {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_BUBBLEBOY_1
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_BUBBLEBOY_2
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_BUBBLEBOY_3
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_BUBBLEBOY_4
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_BUBBLEBOY_5
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_BUBBLEBOY_6
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_BUBBLEBOY_7
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_BUBBLEBOY_8
		get sidequest_fail
	}
	
	//PersonalHeater
	beaniesquest_intro_PersonalHeater {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PERSONALHEATER_1
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PERSONALHEATER_2
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PERSONALHEATER_3
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PERSONALHEATER_4
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PERSONALHEATER_5
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PERSONALHEATER_6
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PERSONALHEATER_7
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PERSONALHEATER_8
		
	}
	beaniesquest_complete_PersonalHeater {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSONALHEATER_1
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSONALHEATER_2
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSONALHEATER_3
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSONALHEATER_4
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSONALHEATER_5
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSONALHEATER_6
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PERSONALHEATER_7
		get sidequest_reward
	}
	beaniesquest_fail_PersonalHeater {
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PERSONALHEATER_1
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PERSONALHEATER_2
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PERSONALHEATER_3
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PERSONALHEATER_4
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PERSONALHEATER_5
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PERSONALHEATER_6
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PERSONALHEATER_7
		set_state zoomedout
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PERSONALHEATER_8
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PERSONALHEATER_9
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PERSONALHEATER_10
		get sidequest_fail
	}
	
	//NDEDevice
	beaniesquest_intro_NDEDevice {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_NDEDEVICE_1
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_NDEDEVICE_2
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_NDEDEVICE_3
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_NDEDEVICE_4
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_NDEDEVICE_5
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_NDEDEVICE_6
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_NDEDEVICE_7
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_NDEDEVICE_8
		
	}
	beaniesquest_complete_NDEDevice {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_NDEDEVICE_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_NDEDEVICE_2
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_NDEDEVICE_3
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_NDEDEVICE_4
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_NDEDEVICE_5
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_NDEDEVICE_6
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_NDEDEVICE_7
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_NDEDEVICE_8
		get sidequest_reward
	}
	beaniesquest_fail_NDEDevice {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_NDEDEVICE_1
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_NDEDEVICE_2
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_NDEDEVICE_3
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_NDEDEVICE_4
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_NDEDEVICE_5
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_NDEDEVICE_6
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_NDEDEVICE_7
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_NDEDEVICE_8
		get sidequest_fail
	}
	
	//MultilinkCable
	beaniesquest_intro_MultilinkCable {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MULTILINKCABLE_1
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MULTILINKCABLE_2
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MULTILINKCABLE_3
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MULTILINKCABLE_4
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MULTILINKCABLE_5
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MULTILINKCABLE_6
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MULTILINKCABLE_7
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_MULTILINKCABLE_8
		
	}
	beaniesquest_complete_MultilinkCable {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MULTILINKCABLE_1 
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MULTILINKCABLE_2
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MULTILINKCABLE_3
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MULTILINKCABLE_4
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MULTILINKCABLE_5
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MULTILINKCABLE_6
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MULTILINKCABLE_7 
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MULTILINKCABLE_8
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_MULTILINKCABLE_9
		get sidequest_reward
	}
	beaniesquest_fail_MultilinkCable {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_MULTILINKCABLE_1
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_MULTILINKCABLE_2
		get sidequest_fail
	}
	
	//HiveMind
	beaniesquest_intro_HiveMind {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_HIVEMIND_1
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_HIVEMIND_2
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_HIVEMIND_3
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_HIVEMIND_4
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_HIVEMIND_5
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_HIVEMIND_6
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_HIVEMIND_7
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_HIVEMIND_8
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_HIVEMIND_9
		
	}
	beaniesquest_complete_HiveMind {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_HIVEMIND_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_HIVEMIND_2
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_HIVEMIND_3
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_HIVEMIND_4
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_HIVEMIND_5
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_HIVEMIND_6
		get sidequest_reward
	}
	beaniesquest_fail_HiveMind {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_HIVEMIND_1
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_HIVEMIND_2
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_HIVEMIND_3
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_HIVEMIND_4
		get sidequest_fail
	}

	//PrincessHat
	beaniesquest_intro_PrincessHat {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PRINCESSHAT_1
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PRINCESSHAT_2
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PRINCESSHAT_3
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PRINCESSHAT_4
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PRINCESSHAT_5
		set_state verycloseup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PRINCESSHAT_6
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_PRINCESSHAT_7

		
	}
	beaniesquest_complete_PrincessHat {
		set_state closeup
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PRINCESSHAT_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PRINCESSHAT_2
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PRINCESSHAT_3
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PRINCESSHAT_4
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_PRINCESSHAT_5
		get sidequest_reward
	}
	beaniesquest_fail_PrincessHat {
		set_state idle
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PRINCESSHAT_1
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PRINCESSHAT_2
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PRINCESSHAT_3
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PRINCESSHAT_4
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PRINCESSHAT_5
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PRINCESSHAT_6
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_PRINCESSHAT_7
		get sidequest_fail
	}

	//unknown item (will use these if theres no alternate specified string here)
	beaniesquest_intro_Generic {
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_GENERIC_1
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_GENERIC_2
		dialog NPC_BEANIES_BEANIESQUEST_INTRO_GENERIC_3
	}
	beaniesquest_complete_Generic {
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_GENERIC_1
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_GENERIC_2
		dialog NPC_BEANIES_BEANIESQUEST_COMPLETE_GENERIC_3
		get sidequest_reward
	}
	beaniesquest_fail_Generic { //in fail states you only have {questitemname} and not {questreward} or {questdestination}
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_GENERIC_1
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_GENERIC_2
		dialog NPC_BEANIES_BEANIESQUEST_FAIL_GENERIC_3
		get sidequest_fail
	}

	unknown {
		dialog NPC_BEANIES_UNKNOWN_1
		get npc_reward
	}
	
	//beanies unlock intros
	
	beanies_lab_intro {//dr beanies is now homeless, credits roll after this bit
		set_state closeup
		dialog NPC_BEANIES_BEANIES_LAB_INTRO_1
		dialog NPC_BEANIES_BEANIES_LAB_INTRO_2
		set_state verycloseup
		dialog NPC_BEANIES_BEANIES_LAB_INTRO_3
		set_state idle
		dialog NPC_BEANIES_BEANIES_LAB_INTRO_4
		dialog NPC_BEANIES_BEANIES_LAB_INTRO_5
		set_state verycloseup
		dialog NPC_BEANIES_BEANIES_LAB_INTRO_6
		set_state closeup
		dialog NPC_BEANIES_BEANIES_LAB_INTRO_7
		dialog NPC_BEANIES_BEANIES_LAB_INTRO_8
		set_state verycloseup
		dialog NPC_BEANIES_BEANIES_LAB_INTRO_9
		dialog NPC_BEANIES_BEANIES_LAB_INTRO_10
		dialog NPC_BEANIES_BEANIES_LAB_INTRO_11
		dialog NPC_BEANIES_BEANIES_LAB_INTRO_12
		
		play_cutscene credits_1
		trigger_unlock song_unlock_get_in_the_cage
		restart_npc_music 1
		
		set_state idle
		dialog NPC_BEANIES_BEANIES_LAB_INTRO_13
		dialog NPC_BEANIES_BEANIES_LAB_INTRO_14
		dialog NPC_BEANIES_BEANIES_LAB_INTRO_15
		set_state closeup
		dialog NPC_BEANIES_BEANIES_LAB_INTRO_16
		dialog NPC_BEANIES_BEANIES_LAB_INTRO_17
		set_state idle
		dialog NPC_BEANIES_BEANIES_LAB_INTRO_18
		dialog NPC_BEANIES_BEANIES_LAB_INTRO_19
		dialog NPC_BEANIES_BEANIES_LAB_INTRO_20
		set_state closeup
		dialog NPC_BEANIES_BEANIES_LAB_INTRO_21
		dialog NPC_BEANIES_BEANIES_LAB_INTRO_22
		set_state verycloseup
		dialog NPC_BEANIES_BEANIES_LAB_INTRO_23
		dialog NPC_BEANIES_BEANIES_LAB_INTRO_24
	}
	
	beanies_timemachine_intro { //dr beanies realizes you saw his time machine and explains how to fix it and go into the past and cause the butterfly effect
		set_state closeup
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_1
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_2
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_3
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_4
		set_state idle
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_5
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_6
		set_state closeup
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_7
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_8
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_9
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_10

		trigger_unlock time_machine_quest_begin
		set_state idle
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_11
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_INTRO_12
	}

	beanies_timemachine_2 {  //dr beanies frustrated by still being homeless sends you into the future to attempt to gain info on how he fixes things.
		set_state idle
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_2_1
		set_state closeup
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_2_2
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_2_3
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_2_4
		set_state idle
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_2_5
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_2_6
		set_state closeup
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_2_7
		set_state idle
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_2_8
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_2_9
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_2_10
		set_state closeup
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_2_11
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_2_12
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_2_13
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_2_14
		set_state verycloseup
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_2_15
		set_state closeup
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_2_16
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_2_17
		set_state idle
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_2_18
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_2_19 
		dialog NPC_BEANIES_BEANIES_TIMEMACHINE_2_20
	}

	beanies_jurassic_intro {
		set_state idle
		dialog NPC_BEANIES_BEANIES_JURASSIC_INTRO_1
		set_state closeup
		dialog NPC_BEANIES_BEANIES_JURASSIC_INTRO_2
		dialog NPC_BEANIES_BEANIES_JURASSIC_INTRO_3
		dialog NPC_BEANIES_BEANIES_JURASSIC_INTRO_4
		set_state verycloseup
		dialog NPC_BEANIES_BEANIES_JURASSIC_INTRO_5
	}

	beanies_future_intro {  //dr beanies frustrated by still being homeless sends you into the future to attempt to gain info on how he fixes things.
		set_state closeup
		dialog NPC_BEANIES_BEANIES_FUTURE_INTRO_1
		dialog NPC_BEANIES_BEANIES_FUTURE_INTRO_2
		set_state idle
		dialog NPC_BEANIES_BEANIES_FUTURE_INTRO_3
		dialog NPC_BEANIES_BEANIES_FUTURE_INTRO_4
		dialog NPC_BEANIES_BEANIES_FUTURE_INTRO_5
		dialog NPC_BEANIES_BEANIES_FUTURE_INTRO_6
		set_state zoomedout
		dialog NPC_BEANIES_BEANIES_FUTURE_INTRO_7
		set_state closeup
        dialog NPC_BEANIES_BEANIES_FUTURE_INTRO_8 
		dialog NPC_BEANIES_BEANIES_FUTURE_INTRO_9
		dialog NPC_BEANIES_BEANIES_FUTURE_INTRO_10
		set_state verycloseup
		dialog NPC_BEANIES_BEANIES_FUTURE_INTRO_11
	}

	beanies_seefuture {  //dr beanies responds to you seeing the future (win or fail).
		set_state closeup
		dialog NPC_BEANIES_BEANIES_SEEFUTURE_1
		set_state verycloseup
		dialog NPC_BEANIES_BEANIES_SEEFUTURE_2
		set_state closeup
		dialog NPC_BEANIES_BEANIES_SEEFUTURE_3
		dialog NPC_BEANIES_BEANIES_SEEFUTURE_4
		set_state verycloseup
		dialog NPC_BEANIES_BEANIES_SEEFUTURE_5
		set_state closeup
		dialog NPC_BEANIES_BEANIES_SEEFUTURE_6
		dialog NPC_BEANIES_BEANIES_SEEFUTURE_7
		dialog NPC_BEANIES_BEANIES_SEEFUTURE_8
		dialog NPC_BEANIES_BEANIES_SEEFUTURE_9
		dialog NPC_BEANIES_BEANIES_SEEFUTURE_10
		dialog NPC_BEANIES_BEANIES_SEEFUTURE_11
		set_state verycloseup
		dialog NPC_BEANIES_BEANIES_SEEFUTURE_12
		set_state closeup
		dialog NPC_BEANIES_BEANIES_SEEFUTURE_13
		set_state idle
		dialog NPC_BEANIES_BEANIES_SEEFUTURE_14
		set_state verycloseup
		dialog NPC_BEANIES_BEANIES_SEEFUTURE_15

	}
	
	beanies_theend_intro { //dr says responds to you killing hitler
		set_state closeup
		dialog NPC_BEANIES_BEANIES_THEEND_INTRO_1
		dialog NPC_BEANIES_BEANIES_THEEND_INTRO_2
		dialog NPC_BEANIES_BEANIES_THEEND_INTRO_3
		dialog NPC_BEANIES_BEANIES_THEEND_INTRO_4
		set_state verycloseup
		dialog NPC_BEANIES_BEANIES_THEEND_INTRO_5
	}
	
	beanies_seetheend { //dr responds to you seeing the far future (win or fail)
		set_state idle
		dialog NPC_BEANIES_BEANIES_SEETHEEND_1
		dialog NPC_BEANIES_BEANIES_SEETHEEND_2
		set_state closeup
		dialog NPC_BEANIES_BEANIES_SEETHEEND_3
		dialog NPC_BEANIES_BEANIES_SEETHEEND_4
		set_state idle
		dialog NPC_BEANIES_BEANIES_SEETHEEND_5
		set_state closeup
		dialog NPC_BEANIES_BEANIES_SEETHEEND_6
		dialog NPC_BEANIES_BEANIES_SEETHEEND_7
		dialog NPC_BEANIES_BEANIES_SEETHEEND_8
		dialog NPC_BEANIES_BEANIES_SEETHEEND_9
		dialog NPC_BEANIES_BEANIES_SEETHEEND_10
		set_state verycloseup
		dialog NPC_BEANIES_BEANIES_SEETHEEND_11
		dialog NPC_BEANIES_BEANIES_SEETHEEND_12
	}
	
	beanies_terminator1_defeat { //terminator 1 is killed.
		set_state closeup
		dialog NPC_BEANIES_BEANIES_TERMINATOR1_DEFEAT_1
		dialog NPC_BEANIES_BEANIES_TERMINATOR1_DEFEAT_2
		set_state verycloseup
		dialog NPC_BEANIES_BEANIES_TERMINATOR1_DEFEAT_3
		set_state closeup
		dialog NPC_BEANIES_BEANIES_TERMINATOR1_DEFEAT_4

		trigger_unlock quest_begin_receiver2
		
		set_state idle
		dialog NPC_BEANIES_BEANIES_TERMINATOR1_DEFEAT_5
		dialog NPC_BEANIES_BEANIES_TERMINATOR1_DEFEAT_6
		set_state closeup
		dialog NPC_BEANIES_BEANIES_TERMINATOR1_DEFEAT_7
		dialog NPC_BEANIES_BEANIES_TERMINATOR1_DEFEAT_8
		dialog NPC_BEANIES_BEANIES_TERMINATOR1_DEFEAT_9
		dialog NPC_BEANIES_BEANIES_TERMINATOR1_DEFEAT_10	

	}
	
	beanies_terminator2_defeat { //dr invents more tech for you to use that could bend time and space
		set_state idle
		dialog NPC_BEANIES_BEANIES_TERMINATOR2_DEFEAT_1
		set_state closeup
		dialog NPC_BEANIES_BEANIES_TERMINATOR2_DEFEAT_2

		trigger_unlock quest_begin_transmitter2

		dialog NPC_BEANIES_BEANIES_TERMINATOR2_DEFEAT_3
		dialog NPC_BEANIES_BEANIES_TERMINATOR2_DEFEAT_4
		dialog NPC_BEANIES_BEANIES_TERMINATOR2_DEFEAT_5
		dialog NPC_BEANIES_BEANIES_TERMINATOR2_DEFEAT_6
		set_state verycloseup
		dialog NPC_BEANIES_BEANIES_TERMINATOR2_DEFEAT_7
	}
	
		
	beanies_hitler3 { //dr discovers that hitler has been the one sending robots back in time to stop you, intros hitler "final boss"
		set_state idle
		dialog NPC_BEANIES_BEANIES_HITLER3_1
		dialog NPC_BEANIES_BEANIES_HITLER3_2
		dialog NPC_BEANIES_BEANIES_HITLER3_3
		dialog NPC_BEANIES_BEANIES_HITLER3_4
		dialog NPC_BEANIES_BEANIES_HITLER3_5
		dialog NPC_BEANIES_BEANIES_HITLER3_6
		dialog NPC_BEANIES_BEANIES_HITLER3_7
		dialog NPC_BEANIES_BEANIES_HITLER3_8
		dialog NPC_BEANIES_BEANIES_HITLER3_9
		set_state closeup
		dialog NPC_BEANIES_BEANIES_HITLER3_10
		dialog NPC_BEANIES_BEANIES_HITLER3_11
		dialog NPC_BEANIES_BEANIES_HITLER3_12
	}
	
	beanies_hitler3_defeat { //dr has final piece of tech that will unlock the infinite
		set_state closeup
		dialog NPC_BEANIES_BEANIES_HITLER3_DEFEAT_1
		set_state verycloseup
		dialog NPC_BEANIES_BEANIES_HITLER3_DEFEAT_2
		set_state idle
		dialog NPC_BEANIES_BEANIES_HITLER3_DEFEAT_3
		dialog NPC_BEANIES_BEANIES_HITLER3_DEFEAT_4
		set_state closeup
		dialog NPC_BEANIES_BEANIES_HITLER3_DEFEAT_5

		trigger_unlock quest_begin_amplifier2

		dialog NPC_BEANIES_BEANIES_HITLER3_DEFEAT_6
		dialog NPC_BEANIES_BEANIES_HITLER3_DEFEAT_7
		dialog NPC_BEANIES_BEANIES_HITLER3_DEFEAT_8
		set_state verycloseup
		dialog NPC_BEANIES_BEANIES_HITLER3_DEFEAT_9
		set_state closeup
		dialog NPC_BEANIES_BEANIES_HITLER3_DEFEAT_10
		dialog NPC_BEANIES_BEANIES_HITLER3_DEFEAT_11
		dialog NPC_BEANIES_BEANIES_HITLER3_DEFEAT_12
		set_state idle
		dialog NPC_BEANIES_BEANIES_HITLER3_DEFEAT_13
	}
	

	//these commented out keys were moved into combat_tutorial.gon since they need to be in the NPC popup rig

	//beanies_rift_intro  //dr beanies comments on the chaos realm!
	//beanies_infinite_intro //dr beanies unlocks the infinite and pushes you to challenge the creator.

	
	beanies_bombquest_begin { //you now realize the creator cant be killed, dr beanies has a plan and gives you your final quest.
		set_state idle
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_1
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_2
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_3
		set_state zoomedout
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_4
		set_state idle
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_5
		set_state closeup
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_6
		set_state verycloseup
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_7
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_8
		set_state closeup
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_9
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_10

		trigger_unlock reset_nuke_quest

		dialog NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_11
		set_state idle
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_12
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_BEGIN_13
	}

	
	beanies_bombquest_2 {//when you have the kings blood
		set_state closeup
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_2_1
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_2_2
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_2_3
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_2_4
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_2_5
		set_state idle
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_2_6
	}

	beanies_bombquest_3 { //dr beanies send you to kill the creator once and for all.
		set_state closeup
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_3_1
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_3_2
		set_state verycloseup
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_3_3
		
		trigger_unlock nuke_quest_get_nuke
		
		set_state closeup
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_3_4
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_3_5
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_3_6
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_3_7
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_3_8
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_3_9
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_3_10
	}
	
	beanies_bombquest_fail_jarofradiation { //if you lost on the Act 1 part of the quest
		set_state idle
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFRADIATION_1
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFRADIATION_2
		set_state closeup
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFRADIATION_3
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFRADIATION_4

		trigger_unlock reset_nuke_quest

		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFRADIATION_5
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFRADIATION_6
		set_state verycloseup
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFRADIATION_7
	}
	beanies_bombquest_fail_jarofblood {  //if you lost on the Act 2 part of the quest
		set_state verycloseup
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_1
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_2
		set_state closeup
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_3
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_4
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_5
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_6
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_7
		set_state idle
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_8

		trigger_unlock reset_nuke_quest

		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_9
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_10
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_11
		set_state closeup
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_12
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFBLOOD_13
	}
	beanies_bombquest_fail_jarofchaos { //if you drank or lost the jar of chaos
		set_state closeup
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFCHAOS_1
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFCHAOS_2
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFCHAOS_3
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFCHAOS_4 
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFCHAOS_5

		trigger_unlock reset_nuke_quest
		
		set_state idle
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFCHAOS_6
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFCHAOS_7
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFCHAOS_8
		set_state closeup
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFCHAOS_9
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_JAROFCHAOS_10
	}
	beanies_bombquest_fail_nuke {  //if you lost on the Act 3 part of the quest
		set_state closeup
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_1
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_2
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_3
		set_state idle
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_4
		set_state closeup
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_5
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_6
		set_state idle
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_7
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_8
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_9
		set_state closeup
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_10

		trigger_unlock reset_nuke_quest

		set_state verycloseup
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_11
		set_state closeup
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_FAIL_NUKE_12
	}

	/////////////////////// 
	//beanies ending dialogs moved to combat tutorial
	//and beanies_gameending.gon

	beanies_bombquest_amnesia {  //after returning home from a successful nuke quest
		set_state closeup
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_AMNESIA_1
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_AMNESIA_2
		set_state verycloseup
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_AMNESIA_3
		set_state closeup
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_AMNESIA_4
		set_state idle
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_AMNESIA_5
		dialog NPC_BEANIES_BEANIES_BOMBQUEST_AMNESIA_6

		trigger_unlock nuke_quest_loop
	}

	beanies_iloveyou { //X.
		dialog NPC_BEANIES_BEANIES_ILOVEYOU_1
		dialog NPC_BEANIES_BEANIES_ILOVEYOU_2
		dialog NPC_BEANIES_BEANIES_ILOVEYOU_3
	}
	
	beanies_screenshake_test {
		dialog NPC_BEANIES_BEANIES_SCREENSHAKE_TEST_1

		screenshake [.5, 10]

		dialog NPC_BEANIES_BEANIES_SCREENSHAKE_TEST_2
		dialog NPC_BEANIES_BEANIES_SCREENSHAKE_TEST_3
		dialog NPC_BEANIES_BEANIES_SCREENSHAKE_TEST_4
		dialog NPC_BEANIES_BEANIES_SCREENSHAKE_TEST_5

		sfx PickupCoin

		dialog NPC_BEANIES_BEANIES_SCREENSHAKE_TEST_6

		dialog NPC_BEANIES_BEANIES_SCREENSHAKE_TEST_7
	}

		//default  happy  veryhappy  sad  angry  veryangry
        //questioning  whispering  pondering  mocking
        //inlove  confused  paranoid  shocked  scared  spacedout
		//grossedout bored winking
}
```

---

## File: `butch_progression.gon`

### `states_and_transitions`
**Source:** `butch_progression.gon`  

```
states_and_transitions {
	states {
		idle ["idle"]
		verycloseup ["verycloseup"]
		closeup ["closeup"]
		zoomedout ["zoomedout"]
	}

	transitions {
	}
}
```

---

### `sequences`
**Source:** `butch_progression.gon`  

**Localization Strings:**
- `NPC_BUTCH_UNPROMPTED_1`: "Why are you here?"
- `NPC_BUTCH_UNKNOWN_1`: "You appear to have unlocked something, but I don't have dialog for it. Congrats. Also fix this."
- `NPC_BUTCH_ALSO_1`: "Also..."
- `NPC_BUTCH_BUTCH_BEGIN_ACCEPTING_CATS_1`: "[m:default]So it looks like that sewer monster man built you a pipe, huh?"
- `NPC_BUTCH_BUTCH_BEGIN_ACCEPTING_CATS_2`: "[m:angry]Well don't feel special, I got one too!"
- `NPC_BUTCH_BUTCH_BEGIN_ACCEPTING_CATS_3`: "[m:pondering]Hey, that gives me an idea... <br/> [m:questioning]How about you and I go into business together?"
- `NPC_BUTCH_BUTCH_BEGIN_ACCEPTING_CATS_4`: "You send me cats with combat experience, [m:inlove]and I let you kiss me behind the dumpster over there?"
- `NPC_BUTCH_BUTCH_BEGIN_ACCEPTING_CATS_5`: "[m:angry]What do you mean "no"?!"
- `NPC_BUTCH_BUTCH_BEGIN_ACCEPTING_CATS_6`: "[m:happy]Yeah well, what about I expand that little box of yours then, huh?"
- `NPC_BUTCH_BUTCH_BEGIN_ACCEPTING_CATS_7`: "[m:angry]I'm talking about that box by your house, sicko!!"
- `NPC_BUTCH_BUTCH_BEGIN_ACCEPTING_CATS_8`: "[m:default]I can upgrade that ol' shoe box for ya, that way you can hold more sharp objects!"
- `NPC_BUTCH_BUTCH_BEGIN_ACCEPTING_CATS_9`: "[m:happy]Trust me it's worth it.  Just send me a cat who's killed some stuff! <br/> I'll hook you up."
- `NPC_BUTCH_UPGRADE_STORAGE_1_1`: "[m:happy]Hey, that cat you sent me could really take a punch, thanks!"
- `NPC_BUTCH_UPGRADE_STORAGE_1_2`: "[m:default]So as per our agreement, I'll upgrade that storage box of yours."
- `NPC_BUTCH_UPGRADE_STORAGE_1_3`: "[m:pondering]Still pretty tiny honestly.  I got bigger ones... But they will cost ya!"
- `NPC_BUTCH_UPGRADE_STORAGE_1_4`: "[m:default]Send more cats with fighting experience and I'll expand it more!"
- `NPC_BUTCH_UPGRADE_STORAGE_1_5`: "[m:default]This time though, I want cats that have ventured further from home."
- `NPC_BUTCH_UPGRADE_STORAGE_1_6`: "[m:pondering]You're gonna need to venture into the sewers or junkyard this time."
- `NPC_BUTCH_UPGRADE_STORAGE_1_7`: "[m:happy]Good luck!"
- `NPC_BUTCH_UPGRADE_STORAGE_2_1`: "[m:happy]So those cats you sent are working out great!"
- `NPC_BUTCH_UPGRADE_STORAGE_2_2`: "[m:whispering]I've been training them to steal medication from the old and bewildered."
- `NPC_BUTCH_UPGRADE_STORAGE_2_3`: "[m:default]As promised, I've upgraded your item storage again!"
- `NPC_BUTCH_UPGRADE_STORAGE_2_4`: "[m:default]I need stronger cats next time though!"
- `NPC_BUTCH_UPGRADE_STORAGE_2_5`: "[m:pondering]Ones with serious experience. <br/> I'm talking cats that have been to the caves or that old cemetery."
- `NPC_BUTCH_UPGRADE_STORAGE_2_6`: "[m:default]Thanks, buddy."
- `NPC_BUTCH_UPGRADE_STORAGE_3_1`: "[m:default]My cat army continues to grow!"
- `NPC_BUTCH_UPGRADE_STORAGE_3_2`: "[m:default]With your help I've been able to move up from petty theft to straight up kidnapping!"
- `NPC_BUTCH_UPGRADE_STORAGE_3_3`: "[m:happy]Yep, I've trained those cats you gave me to steal the elderly!"
- `NPC_BUTCH_UPGRADE_STORAGE_3_4`: "[m:whispering]I got like 6 old people inside that dumpster back there..."
- `NPC_BUTCH_UPGRADE_STORAGE_3_5`: "[m:pondering]Not sure what I'll do with them yet, but I'm thinking about setting up kissing booths or something..."
- `NPC_BUTCH_UPGRADE_STORAGE_3_6`: "[m:default]I dunno, either way, they are there if I need 'em."
- `NPC_BUTCH_UPGRADE_STORAGE_3_7`: "[m:pondering]If I wanna up my game I'm going to need better cats..."
- `NPC_BUTCH_UPGRADE_STORAGE_3_8`: "[m:default]I'm only gonna accept cats who have been inside that bunker to the west, or the crater left by that meteor."
- `NPC_BUTCH_UPGRADE_STORAGE_3_9`: "[m:angry]Get on it!"
- `NPC_BUTCH_UPGRADE_STORAGE_4_1`: "[m:happy]OK get this, I've trained the cats to ride those old people I stole!"
- `NPC_BUTCH_UPGRADE_STORAGE_4_2`: "[m:shocked]Imagine waking up to that!"
- `NPC_BUTCH_UPGRADE_STORAGE_4_3`: "[m:veryhappy]Cats riding grandma as she's donkey kickin' around the living room!"
- `NPC_BUTCH_UPGRADE_STORAGE_4_4`: "[m:questioning]Sadly, the cash flow is a bit low still.  I gotta focus and really figure out how to turn a profit..."
- `NPC_BUTCH_UPGRADE_STORAGE_4_5`: "[m:confused]?"
- `NPC_BUTCH_UPGRADE_STORAGE_4_6`: "[m:shocked]Did you just ask why am I doing this?!"
- `NPC_BUTCH_UPGRADE_STORAGE_4_7`: "[m:angry]Pretty judgemental coming from someone like you!"
- `NPC_BUTCH_UPGRADE_STORAGE_4_8`: "[m:questioning]Eh... I dunno."
- `NPC_BUTCH_UPGRADE_STORAGE_4_9`: "Ever feel like there is just a hole in your heart?"
- `NPC_BUTCH_UPGRADE_STORAGE_4_10`: "[m:pondering]Not like a gunshot or murmur, but like something is missing?"
- `NPC_BUTCH_UPGRADE_STORAGE_4_11`: "[m:sad]Ever since I could remember, I've just always felt like I was half the man I should be..."
- `NPC_BUTCH_UPGRADE_STORAGE_4_12`: "[m:scared]Uh..."
- `NPC_BUTCH_UPGRADE_STORAGE_4_13`: "[m:angry]Now you got me acting like a freakin' girl! <br/> Get the hell out of here!"
- `NPC_BUTCH_UPGRADE_STORAGE_4_14`: "[m:veryangry]I was just joking about all that stuff I said!"
- `NPC_BUTCH_UPGRADE_STORAGE_4_15`: "[m:default]You have more room in your storage now by the way..."
- `NPC_BUTCH_UPGRADE_STORAGE_4_16`: "[m:default]I want better cats also! Center of the Earth, or Space.  I need cats that have been there!"
- `NPC_BUTCH_UPGRADE_STORAGE_4_17`: "[m:angry]Now leave!"
- `NPC_BUTCH_UPGRADE_STORAGE_5_1`: "[m:pondering]..."
- `NPC_BUTCH_UPGRADE_STORAGE_5_2`: "[m:default]Oh, sorry... I was just touching my scar."
- `NPC_BUTCH_UPGRADE_STORAGE_5_3`: "[m:questioning]No, not the cat scratches, the scar on the side of my face... You never noticed it?"
- `NPC_BUTCH_UPGRADE_STORAGE_5_4`: "[m:happy]Always thought it made me look tough... I've had it as long as I can remember."
- `NPC_BUTCH_UPGRADE_STORAGE_5_5`: "[m:default]Anyway, that's not important.  What is important is how well my business is doing!"
- `NPC_BUTCH_UPGRADE_STORAGE_5_6`: "[m:happy]You guessed it! <br/> I've started murdering!"
- `NPC_BUTCH_UPGRADE_STORAGE_5_7`: "[m:pondering]Well, not me personally, <br/> but the cats you sent me!"
- `NPC_BUTCH_UPGRADE_STORAGE_5_8`: "[m:veryhappy]They are straight up killing people all over town!"
- `NPC_BUTCH_UPGRADE_STORAGE_5_9`: "[m:pondering]Sadly it's just drifters and hobos currently, so not much news coverage..."
- `NPC_BUTCH_UPGRADE_STORAGE_5_10`: "[m:default]But with your help, I'm sure I'll move up to <br/> "real people" <br/> and start turning a profit."
- `NPC_BUTCH_UPGRADE_STORAGE_5_11`: "Sent you a huge storage shed as payment by the way!"
- `NPC_BUTCH_UPGRADE_STORAGE_5_12`: "[m:happy]Some dude was just living in it..."
- `NPC_BUTCH_UPGRADE_STORAGE_5_13`: "[m:pondering]Or dying in it..."
- `NPC_BUTCH_UPGRADE_STORAGE_5_14`: "[m:default]Either way, it's yours now!"
- `NPC_BUTCH_UPGRADE_STORAGE_5_15`: "[m:default]If you want more boxes, I need cats who have traveled through time!"
- `NPC_BUTCH_UPGRADE_STORAGE_5_16`: "Not sure why... but that's my new rule! <br/> I only accept cats who are time travelers!"
- `NPC_BUTCH_UPGRADE_STORAGE_6_1`: "[m:sad]Jesus Christ I'm lonely..."
- `NPC_BUTCH_UPGRADE_STORAGE_6_2`: "I was talking to my army of the night the other day and the topic of fathers came up..."
- `NPC_BUTCH_UPGRADE_STORAGE_6_3`: "I just started bawling like a baby! <br/> What the hell is wrong with me!?"
- `NPC_BUTCH_UPGRADE_STORAGE_6_4`: "..."
- `NPC_BUTCH_UPGRADE_STORAGE_6_5`: "[m:shocked]There was a mutiny and everything! <br/> I had to murder them to re-establish myself as the alpha!"
- `NPC_BUTCH_UPGRADE_STORAGE_6_6`: "[m:sad]So yeah... I guess starting from scratch again."
- `NPC_BUTCH_UPGRADE_STORAGE_6_7`: "..."
- `NPC_BUTCH_UPGRADE_STORAGE_6_8`: "[m:questioning]Do you remember your father?  Because I'm not sure if I even had one..."
- `NPC_BUTCH_UPGRADE_STORAGE_6_9`: "[m:pondering]Pretty sure I remember having a bedroom.  Lots of wires and monitors maybe?"
- `NPC_BUTCH_UPGRADE_STORAGE_6_10`: "Someone was always there with me? Maybe a brother? Not sure..."
- `NPC_BUTCH_UPGRADE_STORAGE_6_11`: "[m:angry]Ugh so frustrating... <br/> Who am I?"
- `NPC_BUTCH_UPGRADE_STORAGE_6_12`: "[m:sad]..."
- `NPC_BUTCH_UPGRADE_STORAGE_6_13`: "Oh also your shed is bigger..."
- `NPC_BUTCH_UPGRADE_STORAGE_6_14`: "From here on out I need cats who have seen dinosaurs or the fate of the Earth."
- `NPC_BUTCH_UPGRADE_STORAGE_6_15`: "[m:sad]..."
- `NPC_BUTCH_UPGRADE_STORAGE_7_1`: "[m:sad]Yeah, sorry... I didn't do much with those cats."
- `NPC_BUTCH_UPGRADE_STORAGE_7_2`: "I've just been so sad... <br/> [m:angry]and it's really starting to piss me off!"
- `NPC_BUTCH_UPGRADE_STORAGE_7_3`: "Why do I feel like I'm missing a piece of myself!?"
- `NPC_BUTCH_UPGRADE_STORAGE_7_4`: "[m:sad]It's like when people lose an arm and have phantom limb pain, but I feel this "phantom existence"."
- `NPC_BUTCH_UPGRADE_STORAGE_7_5`: "[m:spacedout]Like I'm living in two timelines..."
- `NPC_BUTCH_UPGRADE_STORAGE_7_6`: "[m:veryangry]GAH! <br/> I hate this! <br/> I need to do something to keep my mind occupied!"
- `NPC_BUTCH_UPGRADE_STORAGE_7_7`: "[m:angry]I think I'll go murder that doctor guy... There is something about that dude."
- `NPC_BUTCH_UPGRADE_STORAGE_7_8`: "[m:veryangry]Something that really pisses me off!"
- `NPC_BUTCH_UPGRADE_STORAGE_7_9`: "[m:sad]I'm out of big storage upgrades!"
- `NPC_BUTCH_UPGRADE_STORAGE_7_10`: "But if you keep sending me cats I'm sure I can figure something out."
- `NPC_BUTCH_UPGRADE_STORAGE_7_11`: "[m:winking]I found a bunch of mason jars behind Pinky Winkies..."
- `NPC_BUTCH_UPGRADE_STORAGE_7_12`: "[m:default]Oh, but from here on out I'm only taking cats who have seen God! period!"
- `NPC_BUTCH_UPGRADE_STORAGE_7_13`: "[m:angry]Now leave me alone!"
- `NPC_BUTCH_UPGRADE_STORAGE_REPEATING_INTRO_1`: "[m:default]Thanks for those cats <br/> I guess..."
- `NPC_BUTCH_UPGRADE_STORAGE_REPEATING_INTRO_2`: "[m:questioning]Umm, so I found this old jar.  I think can you fit something inside it?"
- `NPC_BUTCH_UPGRADE_STORAGE_REPEATING_INTRO_3`: "[m:veryangry]Listen! Beggars can't be choosers! You get what you get!"
- `NPC_BUTCH_UPGRADE_STORAGE_REPEATING_INTRO_4`: "[m:angry]A single storage unit is nothing to scoff at!"
- `NPC_BUTCH_UPGRADE_STORAGE_REPEATING_INTRO_5`: "[m:sad]Me and this jar have been through a lot together..."
- `NPC_BUTCH_UPGRADE_STORAGE_REPEATING_INTRO_6`: "No, no.. that was the past... Take it, it's yours."
- `NPC_BUTCH_UPGRADE_STORAGE_REPEATING_INTRO_7`: "[m:default]Keep sending me cats who have killed God and I'll find more storage stuff..."
- `NPC_BUTCH_UPGRADE_STORAGE_MAX1_1`: "[m:pondering]So uh..."
- `NPC_BUTCH_UPGRADE_STORAGE_MAX1_2`: "[m:happy]Here, have this shoe box!"
- `NPC_BUTCH_UPGRADE_STORAGE_MAX1_3`: "[m:default]I found it in the Doctor's lab. It was filled with baby pictures..."
- `NPC_BUTCH_UPGRADE_STORAGE_MAX1_4`: "[m:questioning]What a weirdo huh? Anyway, that should be able to store a single item for ya!"
- `NPC_BUTCH_UPGRADE_STORAGE_MAX1_5`: "[m:default]Remember, I'm only taking cats that cleared the Infinite."
- `NPC_BUTCH_UPGRADE_STORAGE_MAX1_6`: "Good luck!"
- `NPC_BUTCH_UPGRADE_STORAGE_MAX2_1`: "[m:default]I stole this moving box from some hobo..."
- `NPC_BUTCH_UPGRADE_STORAGE_MAX2_2`: "[m:confused]It's a bit wet, but I'm sure it can still hold something."
- `NPC_BUTCH_UPGRADE_STORAGE_MAX2_3`: "[m:questioning]A unit of storage is a unit of storage!"
- `NPC_BUTCH_UPGRADE_STORAGE_MAX2_4`: "[m:default]Send more cats..."
- `NPC_BUTCH_UPGRADE_STORAGE_MAX3_1`: "[m:default]Trash bag!"
- `NPC_BUTCH_UPGRADE_STORAGE_MAX3_2`: "[m:happy]Take this trash bag, <br/> I just found it."
- `NPC_BUTCH_UPGRADE_STORAGE_MAX3_3`: "[m:questioning]I'm sure it's big enough to hold whatever..."
- `NPC_BUTCH_UPGRADE_STORAGE_MAX3_4`: "[m:default]Meh..."
- `NPC_BUTCH_UPGRADE_STORAGE_MAX3_5`: "[m:default]You know the drill. <br/> Send more cats."
- `NPC_BUTCH_UPGRADE_STORAGE_MAX4_1`: "[m:shocked]Oh, uh... <br/> I didn't expect you to be back so soon..."
- `NPC_BUTCH_UPGRADE_STORAGE_MAX4_2`: "[m:pondering]Uuuhhhh..."
- `NPC_BUTCH_UPGRADE_STORAGE_MAX4_3`: "[m:happy]Oh, take this trash bin! That's good enough..."
- `NPC_BUTCH_UPGRADE_STORAGE_MAX4_4`: "[m:default]I was using it to store the cats you sent me but I got some rope..."
- `NPC_BUTCH_UPGRADE_STORAGE_MAX4_5`: "[m:default]Send more cats from that heaven place or whatever."
- `NPC_BUTCH_UPGRADE_STORAGE_MAX5_1`: "[m:default]Man, you are really committed to this storage expansion stuff aren't you?"
- `NPC_BUTCH_UPGRADE_STORAGE_MAX5_2`: "[m:questioning]I don't wanna sound judgy but like... Have you ever thought you might be mentally ill?"
- `NPC_BUTCH_UPGRADE_STORAGE_MAX5_3`: "[m:spacedout]..."
- `NPC_BUTCH_UPGRADE_STORAGE_MAX5_4`: "[m:winking]Same dude, same."
- `NPC_BUTCH_UPGRADE_STORAGE_MAX5_5`: "[m:default]Anyway, take this bucket.  I stole it from that doctor guy.  Not sure why there is a hole in it..."
- `NPC_BUTCH_UPGRADE_STORAGE_MAX5_6`: "[m:pondering]I'm sure it can still store something."
- `NPC_BUTCH_UPGRADE_STORAGE_MAX5_7`: "[m:default]You know the drill..."
- `NPC_BUTCH_CLASS_UNLOCK_MEDIC_1`: "[m:default]So check this out, <br/> I got a new collar for ya."
- `NPC_BUTCH_CLASS_UNLOCK_MEDIC_2`: "[m:default]This class is called <br/> the [b]Cleric[/b], <br/> [s:.7][m:whispering]a pretty hoity toity religious type.[/s]"
- `NPC_BUTCH_CLASS_UNLOCK_MEDIC_3`: "[m:happy]Judgmental sure, but boy can they heal things!"
- `NPC_BUTCH_CLASS_UNLOCK_MEDIC_4`: "[m:default]With a solid Cleric on your team, ain't no one going down."
- `NPC_BUTCH_CLASS_UNLOCK_MEDIC_5`: "And if someone does, <br/> [m:happy]just pray on it!"
- `NPC_BUTCH_CLASS_UNLOCK_THIEF_1`: "[m:happy]Well well well. <br/> It looks like you got another collar!"
- `NPC_BUTCH_CLASS_UNLOCK_THIEF_2`: "The Thief! <br/> a personal favorite of mine."
- `NPC_BUTCH_CLASS_UNLOCK_THIEF_3`: "[m:questioning]Someone bothering you? <br/>  <br/> [m:veryangry]Thief can stab them in the back!"
- `NPC_BUTCH_CLASS_UNLOCK_THIEF_4`: "[m:questioning]Need some extra cash? <br/>  <br/> [m:happy]Well you know the Thief's got sticky fingers!"
- `NPC_BUTCH_CLASS_UNLOCK_THIEF_5`: "[m:mocking]And don't get me started on how quick they are!"
- `NPC_BUTCH_CLASS_UNLOCK_THIEF_6`: "[m:whispering]Just hope the girls don't find out!"
- `NPC_BUTCH_CLASS_UNLOCK_THIEF_7`: "[m:happy]Haw haw haw"
- `NPC_BUTCH_CLASS_UNLOCK_NECROMANCER_1`: "[m:shocked]Uh oh, <br/> did someone make a deal with the devil?!"
- `NPC_BUTCH_CLASS_UNLOCK_NECROMANCER_2`: "[m:veryhappy]Necromancer <br/> in the house!"
- `NPC_BUTCH_CLASS_UNLOCK_NECROMANCER_3`: "[m:happy]It's the BTGGF <br/> of your dreams! <br/> the leech queen who never stops sucking..."
- `NPC_BUTCH_CLASS_UNLOCK_NECROMANCER_4`: "[m:scared][a:shake][s:1.3]YOUR BLOOD![/s][/a]"
- `NPC_BUTCH_CLASS_UNLOCK_NECROMANCER_5`: "[m:default]Yeah the Necro's pretty cool, it's just that smell that gets to me..."
- `NPC_BUTCH_CLASS_UNLOCK_NECROMANCER_6`: "[m:sad]I just cant get down with that rotting flesh stench."
- `NPC_BUTCH_CLASS_UNLOCK_PSYCHIC_1`: "[m:happy]And there's more!"
- `NPC_BUTCH_CLASS_UNLOCK_PSYCHIC_2`: "[m:default]The Psychic is here for all your mind-bending needs!"
- `NPC_BUTCH_CLASS_UNLOCK_PSYCHIC_3`: "They read minds as well as my kids [m:angry]can read the back of my hand!"
- `NPC_BUTCH_CLASS_UNLOCK_PSYCHIC_4`: "[m:happy]I'm kidding!"
- `NPC_BUTCH_CLASS_UNLOCK_PSYCHIC_5`: "They aren't my kids! <br/> Hell, I don't even know 'em!"
- `NPC_BUTCH_CLASS_UNLOCK_PSYCHIC_6`: "[m:winking]But seriously, the Psychic is cool. <br/> Go check 'em out!"
- `NPC_BUTCH_CLASS_UNLOCK_TINKERER_1`: "[m:questioning]I bet at this point you are asking yourself, how many classes are there?"
- `NPC_BUTCH_CLASS_UNLOCK_TINKERER_2`: "[m:happy]Well lucky for you, <br/> the Tinkerer is great at math!"
- `NPC_BUTCH_CLASS_UNLOCK_TINKERER_3`: "[m:default]And at building robots n' junk.  Honestly they are crafty AF!"
- `NPC_BUTCH_CLASS_UNLOCK_TINKERER_4`: "I watched a Tinkerer sit down and build himself a robo-wife..."
- `NPC_BUTCH_CLASS_UNLOCK_TINKERER_5`: "[m:shocked]That cleaned his whole house!"
- `NPC_BUTCH_CLASS_UNLOCK_TINKERER_6`: "[m:default]Then it just bitched him out about nothing for 12 hours, and crashed his new car."
- `NPC_BUTCH_CLASS_UNLOCK_TINKERER_7`: "[m:happy]Heh..."
- `NPC_BUTCH_CLASS_UNLOCK_DRUID_1`: "[m:confused]Jesus Christ the number of classes, seriously..."
- `NPC_BUTCH_CLASS_UNLOCK_DRUID_2`: "[m:questioning]So this one's a Druid or something?"
- `NPC_BUTCH_CLASS_UNLOCK_DRUID_3`: "[m:spacedout]Its got a crow and is always humming to itself..."
- `NPC_BUTCH_CLASS_UNLOCK_DRUID_4`: "[m:pondering]I dunno, <br/> I wasn't paying attention."
- `NPC_BUTCH_CLASS_UNLOCK_BUTCHER_1`: "[m:happy]OK, here we go! <br/> This one's pretty damn cool!"
- `NPC_BUTCH_CLASS_UNLOCK_BUTCHER_2`: "[m:veryhappy]The Butcher!"
- `NPC_BUTCH_CLASS_UNLOCK_BUTCHER_3`: "[m:inlove]Its got a freakin' meat hook attached to a chain, attached to its arm!"
- `NPC_BUTCH_CLASS_UNLOCK_BUTCHER_4`: "[m:veryhappy]How badass is that?!"
- `NPC_BUTCH_CLASS_UNLOCK_BUTCHER_5`: "[m:questioning]He's also a lard-ass who can't stop eating."
- `NPC_BUTCH_CLASS_UNLOCK_BUTCHER_6`: "[m:mocking]I bet you can relate huh!?"
- `NPC_BUTCH_CLASS_UNLOCK_BUTCHER_7`: "[m:veryhappy]Ha!"
- `NPC_BUTCH_CLASS_UNLOCK_MONK_1`: "[m:default]And yet another class appears!"
- `NPC_BUTCH_CLASS_UNLOCK_MONK_2`: "This one's a Monk. <br/> Hates armor, loves punching."
- `NPC_BUTCH_CLASS_UNLOCK_MONK_3`: "[m:pondering]Slaps, punches, pokes, palms, wet willies, jabs, thrusts, haymakers and uppercuts."
- `NPC_BUTCH_CLASS_UNLOCK_MONK_4`: "[m:default]The list goes on..."
- `NPC_BUTCH_CLASS_UNLOCK_MONK_5`: "So if you're into getting beat up or watching people get beat up"
- `NPC_BUTCH_CLASS_UNLOCK_MONK_6`: "[m:happy]The Monk is right up your alley!"
- `NPC_BUTCH_CLASS_UNLOCK_MONK_7`: "[m:whispering][s:.6]...yeah, right next to their fist probably.[/s]"
- `NPC_BUTCH_CLASS_UNLOCK_MONK_8`: "[m:happy]Ha!"
- `NPC_BUTCH_CLASS_UNLOCK_JESTER_1`: "[m:questioning][s:1.2]WHAT?[/s] <br/> There's another one!"
- `NPC_BUTCH_CLASS_UNLOCK_JESTER_2`: "[m:shocked]The Jester!?"
- `NPC_BUTCH_CLASS_UNLOCK_JESTER_3`: "[m:spacedout]How fucking random!"
- `NPC_BUTCH_CLASS_UNLOCK_JESTER_4`: "[m:happy]Enjoy!"
- `NPC_BUTCH_UNPROMPTED_A_1`: "Yeah, so are you tired of losing? Well if you want some tips from a winner, just ask!"
- `NPC_BUTCH_UNPROMPTED_B_1`: "[m:questioning]Looking for tips from a pro? Well you came to the right place!"
- `NPC_BUTCH_UNPROMPTED_C_1`: "[m:happy]Well look who's come crawling back for help! Don't worry, I gotcha!"
- `NPC_BUTCH_UNPROMPTED_D_1`: "[m:mocking]Well if it isn't the loser! [m:default]Don't worry, with my help you can become less losery! [m:angry]Listen up!"
- `NPC_BUTCH_UNPROMPTED_E_1`: "[m:veryhappy]Hahahahaha haha! <br/> Yeah that's right, I'm laughing at you! Are you going to listen to my tips this time?!"
- `NPC_BUTCH_UNPROMPTED_F_1`: "You know I hand out free tips to losers, right? <br/> You seem in need of some..."
- `NPC_BUTCH_UNPROMPTED_G_1`: "[m:shocked]Oh, you scared me! I thought I was about to be mugged by a loser incapable of logical thought!"
- `NPC_BUTCH_UNPROMPTED_G_2`: "[m:happens]Just joshing ya kid, I'm here to help!"
- `NPC_BUTCH_UNPROMPTED_H_1`: "What is it this time? [m:happy]Come back to a pro for some pro tips?"
- `NPC_BUTCH_UNPROMPTED_I_1`: "I guess you are looking for a hand out? <br/> Well all I got is tips kid!"
- `NPC_BUTCH_BUTCH_TIPS_INTRO_1`: "[m:default]Yeah, I noticed you keep losing. Losing makes you look like a loser, so listen."
- `NPC_BUTCH_BUTCH_TIPS_INTRO_2`: "[m:angry]I trained you, and you're kinda making me look bad."
- `NPC_BUTCH_BUTCH_TIPS_INTRO_3`: "[m:default]If you want to be a winner you gotta [m:veryangry]LISTEN TO ME!"
- `NPC_BUTCH_BUTCH_TIPS_INTRO_4`: "[m:questioning]So, are you ready for a few tips?"
- `NPC_BUTCH_BUTCH_TIPS_INTELLIGENCE_1`: "[m:default]You probably know your [img:int] is a pretty important stat."
- `NPC_BUTCH_BUTCH_TIPS_INTELLIGENCE_2`: "But did you realize if your [img:int] number is the same or more than your favorite spell,"
- `NPC_BUTCH_BUTCH_TIPS_INTELLIGENCE_3`: "[m:happy]That means you can cast it every single turn!"
- `NPC_BUTCH_BUTCH_TIPS_INTELLIGENCE_4`: "[m:default]Always check your [img:int] and the mana costs of your abilities when you level up and make sure you can cast them!"
- `NPC_BUTCH_BUTCH_TIPS_CHARISMA_1`: "[m:default][img:cha] doesn't only affect your max mana."
- `NPC_BUTCH_BUTCH_TIPS_CHARISMA_2`: "Your [img:cha] number is literally how much mana your cat starts battle with."
- `NPC_BUTCH_BUTCH_TIPS_CHARISMA_3`: "[m:happy]Keep that in mind when choosing new abilities.  Being able to cast 1-2 spells on turn 1 is badass!"
- `NPC_BUTCH_BUTCH_TIPS_TACTICALVIEW_1`: "[m:default]Did you know you can hold {binding:TacticalView} to switch to tactical view?"
- `NPC_BUTCH_BUTCH_TIPS_TACTICALVIEW_2`: "[m:pondering]It can be helpful when there is too much going on in battle."
- `NPC_BUTCH_BUTCH_TIPS_TACTICALVIEW_3`: "Give it a try sometime!"
- `NPC_BUTCH_BUTCH_TIPS_INFO_1`: "[m:default]Did you know you can hold down {binding:Examine} on a unit to see its movement + attack range?"
- `NPC_BUTCH_BUTCH_TIPS_INFO_2`: "If you're trying to stay out of range of a dangerous enemy, this is useful information to have!"
- `NPC_BUTCH_BUTCH_TIPS_COMBAT_1`: "[m:default]You know most of the time good tactics are just basic math!"
- `NPC_BUTCH_BUTCH_TIPS_COMBAT_2`: "Check your basic attack's damage and the HP of enemies in your range"
- `NPC_BUTCH_BUTCH_TIPS_COMBAT_3`: "[m:angry]Taking out 1 baddie means removing a whole turn for the enemy!"
- `NPC_BUTCH_BUTCH_TIPS_COMBAT_4`: "Be efficient with your attacks!"
- `NPC_BUTCH_BUTCH_TIPS_TURNORDER_1`: "[m:angry]Turn order matters!"
- `NPC_BUTCH_BUTCH_TIPS_TURNORDER_2`: "[m:default]If an enemy has already taken its turn, focus on killing one that hasn't!"
- `NPC_BUTCH_BUTCH_TIPS_TURNORDER_3`: "Removing enemies before they attack means losing less life. [m:mocking]Duh!"
- `NPC_BUTCH_BUTCH_TIPS_BACKSTAB_1`: "[m:default]You know attacking enemies from behind deals more damage right?"
- `NPC_BUTCH_BUTCH_TIPS_BACKSTAB_2`: "Well specifically that damage bonus is +25% of the attack's damage rounded up."
- `NPC_BUTCH_BUTCH_TIPS_BACKSTAB_3`: "[m:happy]Understanding that might come in handy when taking out enemies with a single attack!"
- `NPC_BUTCH_BUTCH_TIPS_DRAFTING_1`: "[m:default]It's usually smart to avoid drafting abilities in the same mana range."
- `NPC_BUTCH_BUTCH_TIPS_DRAFTING_2`: "Having too many big cost abilities means waiting multiple turns to cast them."
- `NPC_BUTCH_BUTCH_TIPS_DRAFTING_3`: "It's ideal to have a range of unique abilities at different mana costs."
- `NPC_BUTCH_BUTCH_TIPS_REWARDS_1`: "[m:default]Sometimes it seems good to avoid finishing combat to pick up a few more coins..."
- `NPC_BUTCH_BUTCH_TIPS_REWARDS_2`: "Or healing up your team a bit more... [m:angry]Well the Gods frown upon it!"
- `NPC_BUTCH_BUTCH_TIPS_REWARDS_3`: "[m:default]Turns out, the quicker you finish a combat the more rewards you will gain."
- `NPC_BUTCH_BUTCH_TIPS_REWARDS_4`: "[m:happy]It's true, that's how I got this gold tooth!"
- `NPC_BUTCH_BUTCH_TIPS_DISORDERS_1`: "[m:sad]Gaining Disorders can feel like a real kick in the nuts sometimes."
- `NPC_BUTCH_BUTCH_TIPS_DISORDERS_2`: "[m:happy]But they almost always have a silver lining!"
- `NPC_BUTCH_BUTCH_TIPS_DISORDERS_3`: "Try playing and drafting around their positive effects!"
- `NPC_BUTCH_BUTCH_TIPS_ITEMS_1`: "[m:default]Don't be hesitant to move your equipment around between combat."
- `NPC_BUTCH_BUTCH_TIPS_ITEMS_2`: "Moving an item that gives +1 [img:int] could enable someone to cast a big spell every turn!"
- `NPC_BUTCH_BUTCH_TIPS_HARD_1`: "[m:default]Did you realize taking the hard path not only gives better items, but it also levels your cats up more?"
- `NPC_BUTCH_BUTCH_TIPS_HARD_2`: "Every battle levels up a cat, and the hard paths all feature an extra fight!"
- `NPC_BUTCH_BUTCH_TIPS_HARD_3`: "[m:shocked]That's 3 more levels you could be gaining if you take all 3 hard paths!"
- `NPC_BUTCH_BUTCH_TIPS_HARD_4`: "[m:default]You don't always need to take the hard path, especially if you are getting trashed."
- `NPC_BUTCH_BUTCH_TIPS_HARD_5`: "[m:happy]But you know what they say, no risk, no reward!"
- `NPC_BUTCH_BUTCH_TIPS_LESSCATS_1`: "[m:default]You know you don't always NEED to have 4 cats in your party..."
- `NPC_BUTCH_BUTCH_TIPS_LESSCATS_2`: "Doin' a 3 cat run means those cats will level up 2-3 more times than usual!"
- `NPC_BUTCH_BUTCH_TIPS_LESSCATS_3`: "[m:happy]Giving you access to some serious upgrades! Try it out!"
- `NPC_BUTCH_BUTCH_TIPS_HOUSEBOSS_1`: "[m:default]Struggling with a house boss? Try power leveling your cats before you fight it!"
- `NPC_BUTCH_BUTCH_TIPS_HOUSEBOSS_2`: "Taking the hard path, or a 3 cat run can push your cats to level up even further than usual!"
- `NPC_BUTCH_BUTCH_TIPS_HOUSEBOSS_3`: "[m:happy]Then you can take that boss down no problem!"
- `NPC_BUTCH_BUTCH_TIPS_PASSIVES_1`: "[m:default]Your cats' passive abilities are the most important attribute!"
- `NPC_BUTCH_BUTCH_TIPS_PASSIVES_2`: "[m:angry]Be sure to learn them and keep them in mind when drafting new abilities!"
- `NPC_BUTCH_BUTCH_TIPS_PASSIVES_3`: "[m:happy]They are the key to some amazing combos! Keep your eyes peeled!"
- `NPC_BUTCH_BUTCH_TIPS_WELLROUNDED_1`: "[m:default]Did you ever notice the big icons at the top of all your abilities?"
- `NPC_BUTCH_BUTCH_TIPS_WELLROUNDED_2`: "[m:mocking]Well they tell you what type of ability each ability is! Duh!"
- `NPC_BUTCH_BUTCH_TIPS_WELLROUNDED_3`: "[m:default]Abilities fall into 4 major categories. Offensive, defensive, movement and misc."
- `NPC_BUTCH_BUTCH_TIPS_WELLROUNDED_4`: "It's usually important for your cats to have one of each so their build is more well rounded."
- `NPC_BUTCH_BUTCH_TIPS_WELLROUNDED_5`: "[m:happy]Dealing damage is fun, but being able to move around and block will help you not die."
- `NPC_BUTCH_BUTCH_TIPS_HEADHOME_1`: "[m:default]If your cats are looking trashed after a boss fight, there is no shame in heading home!"
- `NPC_BUTCH_BUTCH_TIPS_HEADHOME_2`: "Well, I'll look down upon you, but there is sometimes strategy to cutting your losses."
- `NPC_BUTCH_BUTCH_TIPS_HEADHOME_3`: "[m:pondering]Maybe you got tons of coins saved up, or a few badass items you don't wanna risk losing."
- `NPC_BUTCH_BUTCH_TIPS_HEADHOME_4`: "[m:happy]Just head back home and save what you got for your next adventure!"
- `NPC_BUTCH_BUTCH_TIPS_ELEMENTS_1`: "[m:default]Did you notice sometimes your abilities will have tiny little round icons at the top?"
- `NPC_BUTCH_BUTCH_TIPS_ELEMENTS_2`: "Those are that ability's elements, and there are quite a few of them to discover."
- `NPC_BUTCH_BUTCH_TIPS_ELEMENTS_3`: "[m:happy]An ability with water element will put out fires with ease, or even grow grass!"
- `NPC_BUTCH_BUTCH_TIPS_ELEMENTS_4`: "Cold element can slow things down, but wet things will get frozen solid!"
- `NPC_BUTCH_BUTCH_TIPS_ELEMENTS_5`: "[m:default]There are tons of elemental combos to play with.  Experimentation is key!"
- `NPC_BUTCH_BUTCH_TIPS_REORIENT_1`: "Have you ever wanted to put your ass into the face of your enemy?"
- `NPC_BUTCH_BUTCH_TIPS_REORIENT_2`: "[m:pondering]or maybe turn away to protect the family jewels?"
- `NPC_BUTCH_BUTCH_TIPS_REORIENT_3`: "[m:default]Well you can literaly do that, just click somewhere with nothing selected and it will reorient your cat."
- `NPC_BUTCH_BUTCH_TIPS_REORIENT_4`: "Seriously, click a tile and your cat will face it! It's easy and useful!"
- `NPC_BUTCH_BUTCH_TIPS_REORIENT_5`: "[m:whispering]... Make 'em smell what you got cookin' ..."
- `NPC_BUTCH_BUTCH_TIPS_MAGICDAMAGE_1`: "[m:questioning]Do you know what magic damage is?"
- `NPC_BUTCH_BUTCH_TIPS_MAGICDAMAGE_2`: "[m:pondering]It's kind of like a fist... <br/> but fruity!"
- `NPC_BUTCH_BUTCH_TIPS_MAGICDAMAGE_3`: "[m:default]If your attack or spell has a "Magic Wand" icon at the top, then the damage it does is "Magic"."
- `NPC_BUTCH_BUTCH_TIPS_MAGICDAMAGE_4`: "It's simple!"
- `NPC_BUTCH_BUTCH_TINA1_1`: "[m:questioning]I assume you noticed the extremely large cat roaming the city, consuming felines?"
- `NPC_BUTCH_BUTCH_TINA1_2`: "[m:default]Yeah that's Tina, [b]Guillotina[/b]."
- `NPC_BUTCH_BUTCH_TINA1_3`: "[m:happy]She got that name from her ability to decapitate a cat with a single bite!"
- `NPC_BUTCH_BUTCH_TINA1_4`: "I taught her that move... Yeah, <br/> She was one of mine."
- `NPC_BUTCH_BUTCH_TINA1_5`: "[m:default]She had this thing about consuming her victims..."
- `NPC_BUTCH_BUTCH_TINA1_6`: "[m:grossedout]Caressing their flesh like a lover would as she devoured them."
- `NPC_BUTCH_BUTCH_TINA1_7`: "[m:happy]A true sadist!"
- `NPC_BUTCH_BUTCH_TINA1_8`: "[m:default]She vanished a while before you showed up, but it appears she's back."
- `NPC_BUTCH_BUTCH_TINA1_9`: "[m:pondering]And she's taken an interest in your work... <br/> Once Tina sets her sights on something, she never gives up."
- `NPC_BUTCH_BUTCH_TINA1_10`: "[m:default]Now listen, you only have a few days to prep for her, and this is where you get to use your [o:black][c:white][img:retired]retired[/c][/o] cats!"
- `NPC_BUTCH_BUTCH_TINA1_11`: "[m:angry]You'll need at least 4 high-level [o:black][c:white][img:retired]retired[/c][/o] cats to put up a fight with her."
- `NPC_BUTCH_BUTCH_TINA1_12`: "[m:happy]She doesn't have any weakness, [m:angry]so just try and hit her hard and often!"
- `NPC_BUTCH_BUTCH_TINA1_13`: "[m:winking]Oh, and try to stay out of her stomach!"
- `NPC_BUTCH_BUTCH_TINA1_14`: "[m:happy]Good luck!"
- `NPC_BUTCH_BUTCH_PYRO_1`: "[m:shocked]So get this, that doctor guy, before cats, he was doing experiments on humans!"
- `NPC_BUTCH_BUTCH_PYRO_2`: "[m:default]I was looting his lab last night and found proof."
- `NPC_BUTCH_BUTCH_PYRO_3`: "[m:questioning]And guess what he was doing with the failed experiments?"
- `NPC_BUTCH_BUTCH_PYRO_4`: "[m:paranoid]Dumping them down a hole in his lab.  Pretty sure it connects to that old bunker..."
- `NPC_BUTCH_BUTCH_PYRO_5`: "[m:shocked]I also discovered his last human experiments revolved around these conjoined twins!"
- `NPC_BUTCH_BUTCH_PYRO_6`: "[m:shocked]Identical twins attached at the cheek! <br/> Totaly wild stuff..."
- `NPC_BUTCH_BUTCH_PYRO_7`: "[m:default]Oh, also pretty sure that giant monster is coming to kill you..."
- `NPC_BUTCH_BUTCH_PYRO_8`: "[m:bored]So maybe prep for that..."
- `NPC_BUTCH_BUTCH_BONEYARD_INTRO_1`: "[m:pondering]The Boneyard huh? <br/> Been there more often than I'd like to admit..."
- `NPC_BUTCH_BUTCH_BONEYARD_INTRO_2`: "[m:default]Lots of holes in the Boneyard, and a lot of problems are buried in them."
- `NPC_BUTCH_BUTCH_BONEYARD_INTRO_3`: "[m:questioning]And by problems I obviously mean stiffs."
- `NPC_BUTCH_BUTCH_BONEYARD_INTRO_4`: "[m:default]and by stiffs I mean dongs."
- `NPC_BUTCH_BUTCH_BONEYARD_INTRO_5`: "[m:bored]..."
- `NPC_BUTCH_BUTCH_BONEYARD_INTRO_6`: "[m:default]You picking up what I'm putting down buddy?"
- `NPC_BUTCH_BUTCH_BONEYARD_INTRO_7`: "[m:angry]Wake up little Nancy! Stay on your toes!"
- `NPC_BUTCH_BUTCH_BONEYARD_INTRO_8`: "[m:winking]Don't go getting boned in the Boneyard!"
- `NPC_BUTCH_BUTCH_FIRST_HOUSE_BOSS_BEAT_1`: "[m:happy]Nice work defending your house against Tina!"
- `NPC_BUTCH_BUTCH_FIRST_HOUSE_BOSS_BEAT_2`: "[m:questioning]Did you notice that something fell out of her when she died? <br/> Interesting right?"
- `NPC_BUTCH_BUTCH_FIRST_HOUSE_BOSS_BEAT_3`: "[m:pondering]I never know what to do with those things... But maybe you can find a use?"
- `NPC_BUTCH_BUTCH_FIRST_HOUSE_BOSS_BEAT_4`: "[m:default]Oh also, those cats you used, they are donezo."
- `NPC_BUTCH_BUTCH_FIRST_HOUSE_BOSS_BEAT_5`: "[m:questioning]I don't mean dead, I mean worthless trash... Ultra retired."
- `NPC_BUTCH_BUTCH_FIRST_HOUSE_BOSS_BEAT_6`: "[m:bored]they won't fight again is what I'm trying to say."
- `NPC_BUTCH_BUTCH_FIRST_HOUSE_BOSS_BEAT_7`: "[m:default]They still can make babies, but you can't use them to defend your house anymore."
- `NPC_BUTCH_BUTCH_FIRST_HOUSE_BOSS_BEAT_8`: "[m:pondering]..."
- `NPC_BUTCH_BUTCH_FIRST_HOUSE_BOSS_BEAT_9`: "[m:winking]Maybe I can take them off your hands?"
- `NPC_POPUP_FIRST_FIGHT_INTRO_14`: "Click it, <br/> and then click the tile you want to move to."
- `NPC_POPUP_MELEE_MOVE2_2`: "[m:pointleft]Click move, and then move [b]NEXT TO THE RAT[/b]."
- `NPC_POPUP_MAP_EQUIP_ITEMS_2`: "[m:pointdiagonal]You have items that you have not yet equipped to your cats. Click here to equip them first."
- `NPC_POPUP_FINISH_ADVENTURE_5`: "[m:pointdiagonal]Oh, and if you ever wanna save and exit a run, <br/> Just click that thing."
- `NPC_POPUP_HOUSE_PASS_DAY2_4`: "[m:mocking]Also, you can right click the kitten to see if {he} inherited anything from {his} parents, and check {his} stats."

```
sequences {
	
	/*unprompted {
		dialog NPC_BUTCH_UNPROMPTED_1
	}*/

	unknown {
		dialog NPC_BUTCH_UNKNOWN_1
		get npc_reward
	}

	also {
		dialog NPC_BUTCH_ALSO_1
	}

	butch_begin_accepting_cats {
		dialog NPC_BUTCH_BUTCH_BEGIN_ACCEPTING_CATS_1
		dialog NPC_BUTCH_BUTCH_BEGIN_ACCEPTING_CATS_2
		dialog NPC_BUTCH_BUTCH_BEGIN_ACCEPTING_CATS_3
		dialog NPC_BUTCH_BUTCH_BEGIN_ACCEPTING_CATS_4
		set_state closeup
		dialog NPC_BUTCH_BUTCH_BEGIN_ACCEPTING_CATS_5
		set_state idle
		dialog NPC_BUTCH_BUTCH_BEGIN_ACCEPTING_CATS_6
		set_state closeup
		dialog NPC_BUTCH_BUTCH_BEGIN_ACCEPTING_CATS_7
				set_state idle
		dialog NPC_BUTCH_BUTCH_BEGIN_ACCEPTING_CATS_8
		dialog NPC_BUTCH_BUTCH_BEGIN_ACCEPTING_CATS_9
		begin_accepting_cats butch
	}

	upgrade_storage_1 {
		set_state closeup
		dialog NPC_BUTCH_UPGRADE_STORAGE_1_1
		set_state idle
		dialog NPC_BUTCH_UPGRADE_STORAGE_1_2
		dialog NPC_BUTCH_UPGRADE_STORAGE_1_3
		dialog NPC_BUTCH_UPGRADE_STORAGE_1_4

		get npc_reward //this should include a popup

		dialog NPC_BUTCH_UPGRADE_STORAGE_1_5
		dialog NPC_BUTCH_UPGRADE_STORAGE_1_6
		dialog NPC_BUTCH_UPGRADE_STORAGE_1_7
	}

	upgrade_storage_2 {
		dialog NPC_BUTCH_UPGRADE_STORAGE_2_1
		set_state verycloseup
		dialog NPC_BUTCH_UPGRADE_STORAGE_2_2
		set_state idle
		dialog NPC_BUTCH_UPGRADE_STORAGE_2_3

		get npc_reward //this should include a popup

		dialog NPC_BUTCH_UPGRADE_STORAGE_2_4
		dialog NPC_BUTCH_UPGRADE_STORAGE_2_5
		dialog NPC_BUTCH_UPGRADE_STORAGE_2_6
	}

	upgrade_storage_3 {
		set_state closeup
		dialog NPC_BUTCH_UPGRADE_STORAGE_3_1
		set_state idle
		dialog NPC_BUTCH_UPGRADE_STORAGE_3_2
		dialog NPC_BUTCH_UPGRADE_STORAGE_3_3
		set_state verycloseup
		dialog NPC_BUTCH_UPGRADE_STORAGE_3_4
		set_state closeup
		dialog NPC_BUTCH_UPGRADE_STORAGE_3_5
		dialog NPC_BUTCH_UPGRADE_STORAGE_3_6

		get npc_reward //this should include a popup
		
		set_state idle
		dialog NPC_BUTCH_UPGRADE_STORAGE_3_7
		dialog NPC_BUTCH_UPGRADE_STORAGE_3_8
		set_state closeup
		dialog NPC_BUTCH_UPGRADE_STORAGE_3_9
	}

	upgrade_storage_4 {
		set_state closeup
		dialog NPC_BUTCH_UPGRADE_STORAGE_4_1
		set_state verycloseup
		dialog NPC_BUTCH_UPGRADE_STORAGE_4_2
		dialog NPC_BUTCH_UPGRADE_STORAGE_4_3
		set_state idle
		dialog NPC_BUTCH_UPGRADE_STORAGE_4_4
		set_state closeup
		dialog NPC_BUTCH_UPGRADE_STORAGE_4_5
		set_state idle
		dialog NPC_BUTCH_UPGRADE_STORAGE_4_6
		dialog NPC_BUTCH_UPGRADE_STORAGE_4_7
		dialog NPC_BUTCH_UPGRADE_STORAGE_4_8
		set_state closeup
		dialog NPC_BUTCH_UPGRADE_STORAGE_4_9
		dialog NPC_BUTCH_UPGRADE_STORAGE_4_10
		dialog NPC_BUTCH_UPGRADE_STORAGE_4_11
		set_state zoomedout
		dialog NPC_BUTCH_UPGRADE_STORAGE_4_12
		set_state idle
		dialog NPC_BUTCH_UPGRADE_STORAGE_4_13
		dialog NPC_BUTCH_UPGRADE_STORAGE_4_14
		dialog NPC_BUTCH_UPGRADE_STORAGE_4_15

		get npc_reward //this should include a popup

		dialog NPC_BUTCH_UPGRADE_STORAGE_4_16
		set_state closeup
		dialog NPC_BUTCH_UPGRADE_STORAGE_4_17
	}

	upgrade_storage_5 {
		set_state zoomedout
		dialog NPC_BUTCH_UPGRADE_STORAGE_5_1
		set_state idle
		dialog NPC_BUTCH_UPGRADE_STORAGE_5_2
		dialog NPC_BUTCH_UPGRADE_STORAGE_5_3
		dialog NPC_BUTCH_UPGRADE_STORAGE_5_4
		dialog NPC_BUTCH_UPGRADE_STORAGE_5_5
		set_state closeup
		dialog NPC_BUTCH_UPGRADE_STORAGE_5_6
		set_state idle
		dialog NPC_BUTCH_UPGRADE_STORAGE_5_7
		dialog NPC_BUTCH_UPGRADE_STORAGE_5_8
		dialog NPC_BUTCH_UPGRADE_STORAGE_5_9 
		dialog NPC_BUTCH_UPGRADE_STORAGE_5_10
		dialog NPC_BUTCH_UPGRADE_STORAGE_5_11
		dialog NPC_BUTCH_UPGRADE_STORAGE_5_12
		set_state closeup
		dialog NPC_BUTCH_UPGRADE_STORAGE_5_13
		set_state idle
		dialog NPC_BUTCH_UPGRADE_STORAGE_5_14

		get npc_reward //this should include a popup

		dialog NPC_BUTCH_UPGRADE_STORAGE_5_15
		dialog NPC_BUTCH_UPGRADE_STORAGE_5_16
	}

	upgrade_storage_6 {
		set_state closeup
		dialog NPC_BUTCH_UPGRADE_STORAGE_6_1
		set_state idle
		dialog NPC_BUTCH_UPGRADE_STORAGE_6_2
		dialog NPC_BUTCH_UPGRADE_STORAGE_6_3
		set_state zoomedout
		dialog NPC_BUTCH_UPGRADE_STORAGE_6_4
		set_state closeup
		dialog NPC_BUTCH_UPGRADE_STORAGE_6_5
		set_state idle
		dialog NPC_BUTCH_UPGRADE_STORAGE_6_6
		set_state zoomedout
		dialog NPC_BUTCH_UPGRADE_STORAGE_6_7
		set_state idle
		dialog NPC_BUTCH_UPGRADE_STORAGE_6_8
		dialog NPC_BUTCH_UPGRADE_STORAGE_6_9
		dialog NPC_BUTCH_UPGRADE_STORAGE_6_10
		set_state closeup
		dialog NPC_BUTCH_UPGRADE_STORAGE_6_11
		set_state zoomedout
		dialog NPC_BUTCH_UPGRADE_STORAGE_6_12
		dialog NPC_BUTCH_UPGRADE_STORAGE_6_13

		get npc_reward //this should include a popup

		dialog NPC_BUTCH_UPGRADE_STORAGE_6_14
		dialog NPC_BUTCH_UPGRADE_STORAGE_6_15
	}

	upgrade_storage_7 {
		dialog NPC_BUTCH_UPGRADE_STORAGE_7_1
		dialog NPC_BUTCH_UPGRADE_STORAGE_7_2
		set_state closeup
		dialog NPC_BUTCH_UPGRADE_STORAGE_7_3
		set_state idle
		dialog NPC_BUTCH_UPGRADE_STORAGE_7_4
		dialog NPC_BUTCH_UPGRADE_STORAGE_7_5
		set_state closeup
		dialog NPC_BUTCH_UPGRADE_STORAGE_7_6
		dialog NPC_BUTCH_UPGRADE_STORAGE_7_7
		dialog NPC_BUTCH_UPGRADE_STORAGE_7_8

		get npc_reward //this should include a popup

		dialog NPC_BUTCH_UPGRADE_STORAGE_7_9
		dialog NPC_BUTCH_UPGRADE_STORAGE_7_10
		set_state closeup
		dialog NPC_BUTCH_UPGRADE_STORAGE_7_11
		set_state idle
		dialog NPC_BUTCH_UPGRADE_STORAGE_7_12
		dialog NPC_BUTCH_UPGRADE_STORAGE_7_13	//todo: when we figure out what butch does for his infinite rewards we can mess with this
	}

	upgrade_storage_repeating_intro {//when butch maxes out on storage.
		dialog NPC_BUTCH_UPGRADE_STORAGE_REPEATING_INTRO_1
		dialog NPC_BUTCH_UPGRADE_STORAGE_REPEATING_INTRO_2
		set_state closeup
		dialog NPC_BUTCH_UPGRADE_STORAGE_REPEATING_INTRO_3
		dialog NPC_BUTCH_UPGRADE_STORAGE_REPEATING_INTRO_4
		dialog NPC_BUTCH_UPGRADE_STORAGE_REPEATING_INTRO_5
		set_state idle
		dialog NPC_BUTCH_UPGRADE_STORAGE_REPEATING_INTRO_6

		get npc_reward //this should include a popup

		dialog NPC_BUTCH_UPGRADE_STORAGE_REPEATING_INTRO_7
	}

	upgrade_storage_repeating_normal {
		do_random_sequence [upgrade_storage_max1, upgrade_storage_max2, upgrade_storage_max3, upgrade_storage_max4, upgrade_storage_max5]
	}
	upgrade_storage_repeating_hard {
		do_random_sequence [upgrade_storage_max1, upgrade_storage_max2, upgrade_storage_max3, upgrade_storage_max4, upgrade_storage_max5]
	}
	upgrade_storage_repeating_crazy {
		do_random_sequence [upgrade_storage_max1, upgrade_storage_max2, upgrade_storage_max3, upgrade_storage_max4, upgrade_storage_max5]
	}
	upgrade_storage_repeating_impossible {
		do_random_sequence [upgrade_storage_max1, upgrade_storage_max2, upgrade_storage_max3, upgrade_storage_max4, upgrade_storage_max5]
	}

	upgrade_storage_max1 {//81-85 are random dialogue popups for the single storage space unlocks.
		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX1_1
		set_state closeup
		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX1_2
		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX1_3
		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX1_4

		get npc_reward //this should include a popup

		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX1_5
		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX1_6

	}
	
	upgrade_storage_max2 {
		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX2_1
		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX2_2
		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX2_3

		get npc_reward //this should include a popup

		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX2_4
	}

	upgrade_storage_max3 {
		set_state closeup
		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX3_1
		set_state idle
		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX3_2
		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX3_3
		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX3_4

		get npc_reward //this should include a popup

		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX3_5
	}
	
	upgrade_storage_max4 {
		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX4_1
		set_state zoomedout
		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX4_2
		set_state closeup
		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX4_3
		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX4_4

		get npc_reward //this should include a popup

		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX4_5
	}
	
	upgrade_storage_max5 {
		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX5_1
		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX5_2
		set_state zoomedout
		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX5_3
		set_state closeup
		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX5_4
		set_state idle
		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX5_5
		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX5_6

		get npc_reward //this should include a popup

		dialog NPC_BUTCH_UPGRADE_STORAGE_MAX5_7
	}


	//class unlocks
	class_unlock_medic {
		set_state closeup
		dialog NPC_BUTCH_CLASS_UNLOCK_MEDIC_1
		set_state idle
		dialog NPC_BUTCH_CLASS_UNLOCK_MEDIC_2
		dialog NPC_BUTCH_CLASS_UNLOCK_MEDIC_3
		dialog NPC_BUTCH_CLASS_UNLOCK_MEDIC_4
		set_state closeup
		dialog NPC_BUTCH_CLASS_UNLOCK_MEDIC_5
		unlock_class Medic
	}
	class_unlock_thief {
		set_state closeup
		dialog NPC_BUTCH_CLASS_UNLOCK_THIEF_1
		set_state verycloseup
		dialog NPC_BUTCH_CLASS_UNLOCK_THIEF_2
		set_state idle
		dialog NPC_BUTCH_CLASS_UNLOCK_THIEF_3
		dialog NPC_BUTCH_CLASS_UNLOCK_THIEF_4
		dialog NPC_BUTCH_CLASS_UNLOCK_THIEF_5
		set_state verycloseup
		dialog NPC_BUTCH_CLASS_UNLOCK_THIEF_6
		set_state closeup
		dialog NPC_BUTCH_CLASS_UNLOCK_THIEF_7
		unlock_class Thief
	}
	class_unlock_necromancer {
		set_state closeup
		dialog NPC_BUTCH_CLASS_UNLOCK_NECROMANCER_1
		set_state verycloseup
		dialog NPC_BUTCH_CLASS_UNLOCK_NECROMANCER_2
		set_state closeup
		dialog NPC_BUTCH_CLASS_UNLOCK_NECROMANCER_3
		set_state verycloseup
		dialog NPC_BUTCH_CLASS_UNLOCK_NECROMANCER_4
		set_state idle
		dialog NPC_BUTCH_CLASS_UNLOCK_NECROMANCER_5
		dialog NPC_BUTCH_CLASS_UNLOCK_NECROMANCER_6
		unlock_class Necromancer
	}
	class_unlock_psychic {
		set_state verycloseup
		dialog NPC_BUTCH_CLASS_UNLOCK_PSYCHIC_1
		set_state closeup
		dialog NPC_BUTCH_CLASS_UNLOCK_PSYCHIC_2
		dialog NPC_BUTCH_CLASS_UNLOCK_PSYCHIC_3
		set_state verycloseup
		dialog NPC_BUTCH_CLASS_UNLOCK_PSYCHIC_4
		set_state closeup
		dialog NPC_BUTCH_CLASS_UNLOCK_PSYCHIC_5
		set_state idle
		dialog NPC_BUTCH_CLASS_UNLOCK_PSYCHIC_6
		unlock_class Psychic
	}
	class_unlock_tinkerer {
		set_state closeup
		dialog NPC_BUTCH_CLASS_UNLOCK_TINKERER_1
		dialog NPC_BUTCH_CLASS_UNLOCK_TINKERER_2
		set_state idle
		dialog NPC_BUTCH_CLASS_UNLOCK_TINKERER_3
		dialog NPC_BUTCH_CLASS_UNLOCK_TINKERER_4
		set_state verycloseup
		dialog NPC_BUTCH_CLASS_UNLOCK_TINKERER_5
		set_state idle
		dialog NPC_BUTCH_CLASS_UNLOCK_TINKERER_6
		set_state closeup
		dialog NPC_BUTCH_CLASS_UNLOCK_TINKERER_7
		unlock_class Tinkerer
	}
	class_unlock_druid {
		dialog NPC_BUTCH_CLASS_UNLOCK_DRUID_1
		dialog NPC_BUTCH_CLASS_UNLOCK_DRUID_2
		dialog NPC_BUTCH_CLASS_UNLOCK_DRUID_3
		dialog NPC_BUTCH_CLASS_UNLOCK_DRUID_4
		unlock_class Druid
	}
	class_unlock_butcher {
		dialog NPC_BUTCH_CLASS_UNLOCK_BUTCHER_1
		set_state closeup
		dialog NPC_BUTCH_CLASS_UNLOCK_BUTCHER_2 
		dialog NPC_BUTCH_CLASS_UNLOCK_BUTCHER_3
		set_state verycloseup
		dialog NPC_BUTCH_CLASS_UNLOCK_BUTCHER_4
		set_state idle
		dialog NPC_BUTCH_CLASS_UNLOCK_BUTCHER_5
		dialog NPC_BUTCH_CLASS_UNLOCK_BUTCHER_6
		dialog NPC_BUTCH_CLASS_UNLOCK_BUTCHER_7
		unlock_class Butcher
	}
	class_unlock_monk {
		dialog NPC_BUTCH_CLASS_UNLOCK_MONK_1
		dialog NPC_BUTCH_CLASS_UNLOCK_MONK_2
		set_state closeup
		dialog NPC_BUTCH_CLASS_UNLOCK_MONK_3
		dialog NPC_BUTCH_CLASS_UNLOCK_MONK_4
		set_state idle
		dialog NPC_BUTCH_CLASS_UNLOCK_MONK_5
		dialog NPC_BUTCH_CLASS_UNLOCK_MONK_6
		set_state verycloseup
		dialog NPC_BUTCH_CLASS_UNLOCK_MONK_7
		set_state closeup
		dialog NPC_BUTCH_CLASS_UNLOCK_MONK_8
		unlock_class Monk
	}
	class_unlock_jester {
		set_state closeup
		dialog NPC_BUTCH_CLASS_UNLOCK_JESTER_1
		set_state verycloseup
		dialog NPC_BUTCH_CLASS_UNLOCK_JESTER_2
		set_state closeup
		dialog NPC_BUTCH_CLASS_UNLOCK_JESTER_3
		dialog NPC_BUTCH_CLASS_UNLOCK_JESTER_4
		unlock_class Jester
	}


	//butch tips

	unprompted {
		do_random_sequence [unprompted_a, unprompted_b, unprompted_c, unprompted_d, unprompted_e, unprompted_f, unprompted_g, unprompted_h, unprompted_i]
	}

	unprompted_a {
		dialog NPC_BUTCH_UNPROMPTED_A_1
		do_sequence forward_to_tips	
	}
	unprompted_b {
		dialog NPC_BUTCH_UNPROMPTED_B_1
		do_sequence forward_to_tips	
	}
	unprompted_c {
		dialog NPC_BUTCH_UNPROMPTED_C_1
		do_sequence forward_to_tips
	}
	unprompted_d {
		dialog NPC_BUTCH_UNPROMPTED_D_1
		do_sequence forward_to_tips	
	}
	unprompted_e {
		dialog NPC_BUTCH_UNPROMPTED_E_1
		do_sequence forward_to_tips	
	}
	unprompted_f {
		dialog NPC_BUTCH_UNPROMPTED_F_1
		do_sequence forward_to_tips	
	}
	unprompted_g {
		dialog NPC_BUTCH_UNPROMPTED_G_1
		dialog NPC_BUTCH_UNPROMPTED_G_2
		do_sequence forward_to_tips	
	}
	unprompted_h {
		dialog NPC_BUTCH_UNPROMPTED_H_1
		do_sequence forward_to_tips	
	}
	unprompted_i {
		dialog NPC_BUTCH_UNPROMPTED_I_1
		do_sequence forward_to_tips	
	}
	
	forward_to_tips {
		do_random_sequence [butch_tips_intelligence, butch_tips_charisma, butch_tips_tacticalview, butch_tips_info,butch_tips_combat ,butch_tips_turnorder, butch_tips_backstab, butch_tips_magicdamage,
		butch_tips_drafting, butch_tips_rewards, butch_tips_disorders, butch_tips_items, butch_tips_hard, butch_tips_lesscats, butch_tips_houseboss, butch_tips_passives, butch_tips_wellrounded, butch_tips_headhome, butch_tips_elements ]
	}

	butch_tips_intro {
		dialog NPC_BUTCH_BUTCH_TIPS_INTRO_1
		dialog NPC_BUTCH_BUTCH_TIPS_INTRO_2
		dialog NPC_BUTCH_BUTCH_TIPS_INTRO_3
		dialog NPC_BUTCH_BUTCH_TIPS_INTRO_4
		do_sequence butch_tips_intelligence
	}

	butch_tips_intelligence {
		dialog NPC_BUTCH_BUTCH_TIPS_INTELLIGENCE_1
		dialog NPC_BUTCH_BUTCH_TIPS_INTELLIGENCE_2
		dialog NPC_BUTCH_BUTCH_TIPS_INTELLIGENCE_3
		dialog NPC_BUTCH_BUTCH_TIPS_INTELLIGENCE_4
	}
	butch_tips_charisma {
		dialog NPC_BUTCH_BUTCH_TIPS_CHARISMA_1
		dialog NPC_BUTCH_BUTCH_TIPS_CHARISMA_2
		dialog NPC_BUTCH_BUTCH_TIPS_CHARISMA_3
	}
	butch_tips_tacticalview {
		dialog NPC_BUTCH_BUTCH_TIPS_TACTICALVIEW_1 //TODO: insert actual keybind here instead of hard coding CTRL
		dialog NPC_BUTCH_BUTCH_TIPS_TACTICALVIEW_2
		dialog NPC_BUTCH_BUTCH_TIPS_TACTICALVIEW_3
	}
	butch_tips_info {
		dialog NPC_BUTCH_BUTCH_TIPS_INFO_1 //TODO: insert actual keybind here instead of hard coding RIGHT CLICK
		dialog NPC_BUTCH_BUTCH_TIPS_INFO_2
	}
	butch_tips_combat {
		dialog NPC_BUTCH_BUTCH_TIPS_COMBAT_1
		dialog NPC_BUTCH_BUTCH_TIPS_COMBAT_2
		dialog NPC_BUTCH_BUTCH_TIPS_COMBAT_3
		dialog NPC_BUTCH_BUTCH_TIPS_COMBAT_4
	}
	butch_tips_turnorder {
		dialog NPC_BUTCH_BUTCH_TIPS_TURNORDER_1
		dialog NPC_BUTCH_BUTCH_TIPS_TURNORDER_2
		dialog NPC_BUTCH_BUTCH_TIPS_TURNORDER_3
	}
	
	butch_tips_backstab {
		dialog NPC_BUTCH_BUTCH_TIPS_BACKSTAB_1
		dialog NPC_BUTCH_BUTCH_TIPS_BACKSTAB_2
		dialog NPC_BUTCH_BUTCH_TIPS_BACKSTAB_3
	}
	
	butch_tips_drafting {
		dialog NPC_BUTCH_BUTCH_TIPS_DRAFTING_1
		dialog NPC_BUTCH_BUTCH_TIPS_DRAFTING_2
		dialog NPC_BUTCH_BUTCH_TIPS_DRAFTING_3
	}
	
	butch_tips_rewards {
		dialog NPC_BUTCH_BUTCH_TIPS_REWARDS_1
		dialog NPC_BUTCH_BUTCH_TIPS_REWARDS_2
		dialog NPC_BUTCH_BUTCH_TIPS_REWARDS_3
		dialog NPC_BUTCH_BUTCH_TIPS_REWARDS_4
	}
	
	butch_tips_disorders {
		dialog NPC_BUTCH_BUTCH_TIPS_DISORDERS_1
		dialog NPC_BUTCH_BUTCH_TIPS_DISORDERS_2
		dialog NPC_BUTCH_BUTCH_TIPS_DISORDERS_3
	}
	
	butch_tips_items {
		dialog NPC_BUTCH_BUTCH_TIPS_ITEMS_1
		dialog NPC_BUTCH_BUTCH_TIPS_ITEMS_2
	}
	
	butch_tips_hard {
		dialog NPC_BUTCH_BUTCH_TIPS_HARD_1
		dialog NPC_BUTCH_BUTCH_TIPS_HARD_2
		dialog NPC_BUTCH_BUTCH_TIPS_HARD_3
		dialog NPC_BUTCH_BUTCH_TIPS_HARD_4
		dialog NPC_BUTCH_BUTCH_TIPS_HARD_5
	}
	
	butch_tips_lesscats {
		dialog NPC_BUTCH_BUTCH_TIPS_LESSCATS_1
		dialog NPC_BUTCH_BUTCH_TIPS_LESSCATS_2
		dialog NPC_BUTCH_BUTCH_TIPS_LESSCATS_3
	}
	
	butch_tips_houseboss {
		dialog NPC_BUTCH_BUTCH_TIPS_HOUSEBOSS_1
		dialog NPC_BUTCH_BUTCH_TIPS_HOUSEBOSS_2
		dialog NPC_BUTCH_BUTCH_TIPS_HOUSEBOSS_3
	}
	
	butch_tips_passives {
		dialog NPC_BUTCH_BUTCH_TIPS_PASSIVES_1
		dialog NPC_BUTCH_BUTCH_TIPS_PASSIVES_2
		dialog NPC_BUTCH_BUTCH_TIPS_PASSIVES_3
	}
	
	butch_tips_wellrounded {
		dialog NPC_BUTCH_BUTCH_TIPS_WELLROUNDED_1
		dialog NPC_BUTCH_BUTCH_TIPS_WELLROUNDED_2
		dialog NPC_BUTCH_BUTCH_TIPS_WELLROUNDED_3
		dialog NPC_BUTCH_BUTCH_TIPS_WELLROUNDED_4
		dialog NPC_BUTCH_BUTCH_TIPS_WELLROUNDED_5
	}
	
	butch_tips_headhome {
		dialog NPC_BUTCH_BUTCH_TIPS_HEADHOME_1
		dialog NPC_BUTCH_BUTCH_TIPS_HEADHOME_2
		dialog NPC_BUTCH_BUTCH_TIPS_HEADHOME_3
		dialog NPC_BUTCH_BUTCH_TIPS_HEADHOME_4
	}

	butch_tips_elements {
		dialog NPC_BUTCH_BUTCH_TIPS_ELEMENTS_1
		dialog NPC_BUTCH_BUTCH_TIPS_ELEMENTS_2
		dialog NPC_BUTCH_BUTCH_TIPS_ELEMENTS_3
		dialog NPC_BUTCH_BUTCH_TIPS_ELEMENTS_4
		dialog NPC_BUTCH_BUTCH_TIPS_ELEMENTS_5
	}	
	
	butch_tips_reorient {
		dialog NPC_BUTCH_BUTCH_TIPS_REORIENT_1
		dialog NPC_BUTCH_BUTCH_TIPS_REORIENT_2
		dialog NPC_BUTCH_BUTCH_TIPS_REORIENT_3
		dialog NPC_BUTCH_BUTCH_TIPS_REORIENT_4
		dialog NPC_BUTCH_BUTCH_TIPS_REORIENT_5
	}	
	
	butch_tips_magicdamage {
		dialog NPC_BUTCH_BUTCH_TIPS_MAGICDAMAGE_1
		dialog NPC_BUTCH_BUTCH_TIPS_MAGICDAMAGE_2
		dialog NPC_BUTCH_BUTCH_TIPS_MAGICDAMAGE_3
		dialog NPC_BUTCH_BUTCH_TIPS_MAGICDAMAGE_4
	}	
	
	
	//Butch unlock intros
	butch_tina1 {
		dialog NPC_BUTCH_BUTCH_TINA1_1
		dialog NPC_BUTCH_BUTCH_TINA1_2
		set_state verycloseup
		dialog NPC_BUTCH_BUTCH_TINA1_3
		set_state closeup
		dialog NPC_BUTCH_BUTCH_TINA1_4
		set_state idle
		dialog NPC_BUTCH_BUTCH_TINA1_5
		dialog NPC_BUTCH_BUTCH_TINA1_6
		set_state closeup
		dialog NPC_BUTCH_BUTCH_TINA1_7
		set_state idle
		dialog NPC_BUTCH_BUTCH_TINA1_8
		dialog NPC_BUTCH_BUTCH_TINA1_9
		dialog NPC_BUTCH_BUTCH_TINA1_10
		dialog NPC_BUTCH_BUTCH_TINA1_11
		set_state closeup
		dialog NPC_BUTCH_BUTCH_TINA1_12
		set_state verycloseup
		dialog NPC_BUTCH_BUTCH_TINA1_13
		set_state closeup
		dialog NPC_BUTCH_BUTCH_TINA1_14
	}

	butch_pyro {
		set_state closeup
		dialog NPC_BUTCH_BUTCH_PYRO_1
		set_state idle
		dialog NPC_BUTCH_BUTCH_PYRO_2
		dialog NPC_BUTCH_BUTCH_PYRO_3
		set_state closeup
		dialog NPC_BUTCH_BUTCH_PYRO_4
		dialog NPC_BUTCH_BUTCH_PYRO_5
		dialog NPC_BUTCH_BUTCH_PYRO_6
		set_state idle
		dialog NPC_BUTCH_BUTCH_PYRO_7
		dialog NPC_BUTCH_BUTCH_PYRO_8
	}	

	butch_boneyard_intro {
		set_state closeup
		dialog NPC_BUTCH_BUTCH_BONEYARD_INTRO_1
		set_state idle
		dialog NPC_BUTCH_BUTCH_BONEYARD_INTRO_2
		set_state closeup
		dialog NPC_BUTCH_BUTCH_BONEYARD_INTRO_3
		set_state verycloseup
		dialog NPC_BUTCH_BUTCH_BONEYARD_INTRO_4
		set_state zoomedout
		dialog NPC_BUTCH_BUTCH_BONEYARD_INTRO_5
		set_state closeup
		dialog NPC_BUTCH_BUTCH_BONEYARD_INTRO_6
		dialog NPC_BUTCH_BUTCH_BONEYARD_INTRO_7
		set_state verycloseup
		dialog NPC_BUTCH_BUTCH_BONEYARD_INTRO_8
	}

	butch_first_house_boss_beat {
		set_state idle
		dialog NPC_BUTCH_BUTCH_FIRST_HOUSE_BOSS_BEAT_1
		set_state closeup
		dialog NPC_BUTCH_BUTCH_FIRST_HOUSE_BOSS_BEAT_2
		dialog NPC_BUTCH_BUTCH_FIRST_HOUSE_BOSS_BEAT_3
		set_state verycloseup
		dialog NPC_BUTCH_BUTCH_FIRST_HOUSE_BOSS_BEAT_4
		set_state closeup
		dialog NPC_BUTCH_BUTCH_FIRST_HOUSE_BOSS_BEAT_5
		dialog NPC_BUTCH_BUTCH_FIRST_HOUSE_BOSS_BEAT_6
		set_state idle
		dialog NPC_BUTCH_BUTCH_FIRST_HOUSE_BOSS_BEAT_7
		dialog NPC_BUTCH_BUTCH_FIRST_HOUSE_BOSS_BEAT_8
		set_state verycloseup
		dialog NPC_BUTCH_BUTCH_FIRST_HOUSE_BOSS_BEAT_9
	}

	test_gamepad_prompts {
		dialog "Switch to gamepad now if you wanna see gamepad bindings."
		dialog NPC_POPUP_FIRST_FIGHT_INTRO_14
		dialog NPC_POPUP_MELEE_MOVE2_2
		dialog NPC_POPUP_MAP_EQUIP_ITEMS_2
		dialog NPC_POPUP_FINISH_ADVENTURE_5
		dialog NPC_POPUP_HOUSE_PASS_DAY2_4
		dialog NPC_BUTCH_BUTCH_TIPS_TACTICALVIEW_1
		dialog NPC_BUTCH_BUTCH_TIPS_INFO_1

	}

	//good tips suggestions from discord:
		//physical vs magical damage, melee vs ranged damage
		//bonus combat rewards for beating stuff faster
		//taking the hard path, when & why
		//how the level up system works (of the non-downed cats, random lowest level)
		//item set bonuses
		//dont save mana between fights, use it or lose it

	//minor mechanic tips suggestions from discord
		//you can heal a corpse to give it an extra hit
		//melee attacks can collect pickups
		
		
		//default  happy  veryhappy  sad  angry  veryangry
        //questioning  whispering  pondering  mocking
        //inlove  confused  paranoid  shocked  scared  spacedout
		//grossedout bored winking
}
```

---

## File: `combat_tutorial.gon`

### `states_and_transitions`
**Source:** `combat_tutorial.gon`  

```
states_and_transitions {
	states {
		offscreen ["offscreen"]
		butch_right ["butch_right", "butch_point_spells", "butch_point_turnorder", "butch_point_team", "butch_point_team_nocircle", "butch_point_enemies", "butch_point_cost", "butch_point_cost2", "butch_point_mana", "butch_point_mapnode", "butch_point_food","butch_point_save", "butch_point_inventory", "butch_point_weapon", "butch_levelup", "butch_point_hotblooded", "butch_point_sunburn"]
		butch_left ["butch_left", "butch_point_move", "butch_point_attack", "butch_point_passives", "butch_point_endturn"]

		tink_right ["tink_right", "tink_point_strays"]
		tink_left ["tink_left", "tink_point_cats", "tink_point_food", "tink_point_box"]

		frank_right ["frank_right", "frank_point_pipe"]

		steven_center ["steven_center", "steven_cat"]

		jack_right ["jack_right", "jack_point_furniture"]

		beanies_right ["beanies_right"]

		beanies_intensestatic ["beanies_intensestatic"]
	}

	transitions {
		butch_offscreen_to_right [offscreen butch_right]
		butch_offscreen_to_left [offscreen butch_left]
		butch_right_to_offscreen [butch_right offscreen]
		butch_left_to_offscreen [butch_left offscreen]
		butch_right_to_left [butch_right butch_left]
		butch_left_to_right [butch_left butch_right]

		tink_offscreen_to_right [offscreen tink_right]
		tink_offscreen_to_left [offscreen tink_left]
		tink_right_to_offscreen [tink_right offscreen]
		tink_left_to_offscreen [tink_left offscreen]
		tink_right_to_left [tink_right tink_left]
		tink_left_to_right [tink_left tink_right]

		frank_offscreen_to_right [offscreen frank_right]
		frank_right_to_offscreen [frank_right offscreen]

		jack_offscreen_to_right [offscreen jack_right]
		jack_right_to_offscreen [jack_right offscreen]

		steven_offscreen_to_center [offscreen steven_center]
		steven_center_to_offscreen [steven_center offscreen]

		beanies_offscreen_to_right [offscreen beanies_right]
		beanies_right_to_offscreen [beanies_right offscreen]

		beanies_offscreen_to_intensestatic [offscreen beanies_intensestatic]
		beanies_intensestatic_to_offscreen [beanies_intensestatic offscreen]
	}
}
```

---

### `sequences`
**Source:** `combat_tutorial.gon`  

**Localization Strings:**
- `NPC_POPUP_FIRST_FIGHT_INTRO_1`: "[m:bored]He kicked you out, huh? Yeah he does that..."
- `NPC_POPUP_FIRST_FIGHT_INTRO_2`: "[m:default]Name's [b]Butch[/b], <br/> [s:.6]and even though I could give a frick if you live or die,[/s] <br/> I can't help but see a bit of myself in you..."
- `NPC_POPUP_FIRST_FIGHT_INTRO_3`: "[m:winking]If you get what I mean, <br/> [s:.6]heh heh[/s]"
- `NPC_POPUP_FIRST_FIGHT_INTRO_4`: "[m:default]You wanna survive in Boon County, <br/> you're gonna need to learn how to [m:angry][b]fight![/b]"
- `NPC_POPUP_FIRST_FIGHT_INTRO_5`: "[m:veryangry]So listen up![/m]"
- `NPC_POPUP_FIRST_FIGHT_INTRO_6`: "[m:pointleft]This is your team."
- `NPC_POPUP_FIRST_FIGHT_INTRO_7`: "[m:pointdiagonal]These are your [b]enemies[/b]."
- `NPC_POPUP_FIRST_FIGHT_INTRO_8`: "[m:veryangry]Your goal is to <br/> [a:shake]kill them all![/a]"
- `NPC_POPUP_FIRST_FIGHT_INTRO_9`: "It is now {Catname's} turn."
- `NPC_POPUP_FIRST_FIGHT_INTRO_10`: "[m:pointdiagonal]You can tell because of that pawprint thing above {Catname's} head."
- `NPC_POPUP_FIRST_FIGHT_INTRO_11`: "[m:pointleft]This is {Catname's} [b]basic attack[/b]."
- `NPC_POPUP_FIRST_FIGHT_INTRO_12`: "It's [b]melee[/b] range, <br/> so you will need to move next to the rat to hit it."
- `NPC_POPUP_FIRST_FIGHT_INTRO_13`: "[m:pointleft]This is your [b]movement action[/b]. You can move once per turn."
- `NPC_POPUP_FIRST_FIGHT_INTRO_14`: "Click it, <br/> and then click the tile you want to move to."
- `NPC_POPUP_TRY_AGAIN_MELEE_MOVE_1`: "[m:sad]... Yeahhh... <br/> OK, you're a little slow."
- `NPC_POPUP_TRY_AGAIN_MELEE_MOVE_2`: "[m:angry]I asked you to [b]move[/b] [i]NEXT[/i] to the rat so you can attack it. Let's try again."
- `NPC_POPUP_MELEE_MOVE2_1`: "One more time."
- `NPC_POPUP_MELEE_MOVE2_2`: "[m:pointleft]Click move, and then move [b]NEXT TO THE RAT[/b]."
- `NPC_POPUP_MELEE_ATTACK_RAT_1`: "Now that you are next to the rat, you can [b]attack[/b] it."
- `NPC_POPUP_MELEE_ATTACK_RAT_2`: "This is your [b]basic attack[/b]. You can use your basic attack once per turn."
- `NPC_POPUP_MELEE_ATTACK_RAT_3`: "Click attack, and then click the rat to attack it."
- `NPC_POPUP_TRY_AGAIN_ATTACK_RAT_1`: "[m:sad]You missed... [m:shocked][a:shake]YOU MISSED???[/a]"
- `NPC_POPUP_TRY_AGAIN_ATTACK_RAT_2`: "[m:angry]The rat is literally RIGHT NEXT TO YOU!"
- `NPC_POPUP_TRY_AGAIN_ATTACK_RAT_3`: "Normally you can only attack once per turn... <br/> but I'll let you try again."
- `NPC_POPUP_TRY_AGAIN_ATTACK_RAT_4`: "[m:angry]Hit the damn rat this time!"
- `NPC_POPUP_MELEE_KILLED_RAT_1`: "Sweet! You really destroyed that bastard!"
- `NPC_POPUP_MELEE_KILLED_RAT_2`: "Did you notice that you got a [b]buff[/b] when you killed that thing?"
- `NPC_POPUP_MELEE_KILLED_RAT_3`: "[m:pointleft]It's because of that [b]passive ability[/b]. Hover over it to learn what it does."
- `NPC_POPUP_MELEE_KILLED_RAT_4`: "[m:pointdiagonal]You can also hover over your cat to learn what that [b]buff[/b] does too."
- `NPC_POPUP_MELEE_OUT_OF_ACTIONS_1`: "[m:pointleft]There are also [b]spells[/b]. You only have one so far, and unfortunately you lack the [b]mana[/b] to cast it."
- `NPC_POPUP_MELEE_OUT_OF_ACTIONS_2`: "[m:pointleft]This is how much [b]mana[/b] the spell costs."
- `NPC_POPUP_MELEE_OUT_OF_ACTIONS_3`: "[m:pointdiagonal]This is how much [b]mana[/b] you have."
- `NPC_POPUP_MELEE_OUT_OF_ACTIONS_4`: "[m:default]You gain [b]mana[/b] at the end of your turn equal to your [img:int]. <br/> There's nothing left to do, so end your turn."
- `NPC_POPUP_RANGED_CAT_INTRO_1`: "It is now {Catname's} turn"
- `NPC_POPUP_RANGED_CAT_INTRO_2`: "{Catname} has a [b]ranged basic attack[/b]."
- `NPC_POPUP_RANGED_CAT_INTRO_3`: "While selecting where to move to, you can see a preview of your basic attack's [b]range[/b] in red."
- `NPC_POPUP_RANGED_CAT_INTRO_4`: "[m:pointdiagonal]Move in [b]range[/b] to attack, or as close as you can get!"
- `NPC_POPUP_RANGED_CAT_ROLLED_FIRST_1`: "[m:sad]OK well, I guess that counts as moving."
- `NPC_POPUP_RANGED_CAT_ROLLED_FIRST_2`: "[m:default]You are still out of range of the Tom Tom though."
- `NPC_POPUP_RANGED_CAT_ROLLED_FIRST_3`: "Luckily your spells don't prevent you from also attacking or moving."
- `NPC_POPUP_RANGED_CAT_ROLLED_FIRST_4`: "[m:pointleft]So why not also use your [b]basic movement[/b] to get closer to that Tom Tom?"
- `NPC_POPUP_RANGED_CAT_ROLL_1`: "Unfortunately, you are still not in range to attack the Tom Tom."
- `NPC_POPUP_RANGED_CAT_ROLL_2`: "However! You do have enough mana to cast one of your [b]spells[/b]!"
- `NPC_POPUP_RANGED_CAT_ROLL_3`: "[m:pointleft]Take a look at [b]Roll[/b] here."
- `NPC_POPUP_RANGED_CAT_ROLL_4`: "[m:default][b]Roll[/b] only costs 4 mana."
- `NPC_POPUP_RANGED_CAT_ROLL_5`: "[m:pointdiagonal]and you have 5."
- `NPC_POPUP_RANGED_CAT_ROLL_6`: "[m:default]Click [b]Roll[/b] and then roll closer to that thing!"
- `NPC_POPUP_RANGED_CAT_FAILMOVE_1`: "Unfortunately, you are still not in range to attack the Tom Tom."
- `NPC_POPUP_RANGED_CAT_FAILMOVE_2`: "[m:sad]You also wasted all of your mana, and don't have enough to Roll again."
- `NPC_POPUP_RANGED_CAT_FAILMOVE_3`: "[m:default]Now you will have to wait until your next turn to attack the Tom Tom."
- `NPC_POPUP_RANGED_CAT_FAILMOVE_4`: "[m:whispering]You should think through your actions more next time."
- `NPC_POPUP_RANGED_CAT_EARLY_ATTACK_MISS_1`: "[m:angry]OK well, you just wasted your attack and didn't even hit anything."
- `NPC_POPUP_RANGED_CAT_EARLY_ATTACK_MISS_2`: "[m:default]Now you will have to wait until your next turn to attack the Tom Tom."
- `NPC_POPUP_RANGED_CAT_EARLY_ATTACK_MISS_3`: "[m:sad]You can still move towards the Tom Tom and be in a better position for the next turn, so do that."
- `NPC_POPUP_RANGED_CAT_EARLY_ATTACK_RAT_1`: "[m:sad]OK well, you just wasted your attack. That rat was already dead. You sure popped its carcass open though."
- `NPC_POPUP_RANGED_CAT_EARLY_ATTACK_RAT_2`: "[m:default]Now you will have to wait until your next turn to attack the Tom Tom."
- `NPC_POPUP_RANGED_CAT_EARLY_ATTACK_RAT_3`: "You can still move towards the Tom Tom and be in a better position for the next turn, so do that."
- `NPC_POPUP_RANGED_CAT_EARLY_ATTACK_ALLY_1`: "[m:shocked]You idiot! <br/> That's your teammate!"
- `NPC_POPUP_RANGED_CAT_EARLY_ATTACK_ALLY_2`: "[m:angry]Now you will have to wait until your next turn to attack the Tom Tom. I can't believe this."
- `NPC_POPUP_RANGED_CAT_EARLY_ATTACK_ALLY_3`: "[m:sad]You can still move towards the Tom Tom and be in a better position for the next turn, so do that."
- `NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_MISS_1`: "[m:sad]OK well, you just wasted your attack and didn't even hit anything."
- `NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_MISS_2`: "[m:default]Now you will have to wait until your next turn to attack the Tom Tom."
- `NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_MISS_3`: "You can still roll towards the Tom Tom so you can be in a better position for next turn."
- `NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_RAT_1`: "[m:sad]OK well, you just wasted your attack. That rat was already dead. You sure desecrated its body though."
- `NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_RAT_2`: "[m:default]Now you will have to wait until your next turn to attack the Tom Tom."
- `NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_RAT_3`: "You can still roll towards the Tom Tom so you can be in a better position for next turn."
- `NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_ALLY_1`: "[m:shocked]What the hell are you doing!? They are on your team!"
- `NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_ALLY_2`: "[m:angry]Now you will have to wait until your next turn to attack the Tom Tom. I can't believe this."
- `NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_ALLY_3`: "[m:default]You can still roll towards the Tom Tom so you can be in a better position for next turn."
- `NPC_POPUP_RANGED_CAT_ATTACK_1`: "You are in range to attack the enemy, and you should already know how to do that. <br/> [m:angry]Attack it!"
- `NPC_POPUP_RANGED_ATTACK_TOMTOM_1`: "[m:happy]Good job! You landed the shot!"
- `NPC_POPUP_RANGED_ATTACK_TOMTOM_2`: "[m:default]That Tom Tom is pretty thick however, so he will take a few more hits to kill."
- `NPC_POPUP_RANGED_ATTACK_TOMTOM_FAIL_MISS_1`: "[m:sad]You missed..."
- `NPC_POPUP_RANGED_ATTACK_TOMTOM_FAIL_MISS_2`: "[m:angry]HE WAS JUST STANDING THERE!!!"
- `NPC_POPUP_RANGED_ATTACK_TOMTOM_FAIL_MISS_3`: "[m:default]You will now have to wait until your next turn to attack it."
- `NPC_POPUP_RANGED_ATTACK_TOMTOM_FAIL_ALLY_1`: "[m:angry]Nooooo! That dude is on your team!"
- `NPC_POPUP_RANGED_ATTACK_TOMTOM_FAIL_ALLY_2`: "[m:angry]Now you gotta wait until your next turn to attack the Tom Tom. Ugh."
- `NPC_POPUP_RANGED_ATTACK_TOMTOM_FAIL_RAT_1`: "[m:sad]Yeah OK, so that rat was already dead. You got a thing for corpses or somethin'?"
- `NPC_POPUP_RANGED_ATTACK_TOMTOM_FAIL_RAT_2`: "[m:default]You will now have to wait until your next turn to attack the Tom Tom."
- `NPC_POPUP_MELEE_CAT_SPIT_1`: "OK, it's {Catname's} turn again."
- `NPC_POPUP_MELEE_CAT_SPIT_2`: "You now have enough mana to cast your spell, [b]Spit[/b]."
- `NPC_POPUP_MELEE_CAT_SPIT_3`: "[m:pointleft]Select [b]Spit[/b], and aim it at the enemy!"
- `NPC_POPUP_MELEE_CAT_SPIT_SUCCESS_1`: "[m:happy]That was some good spittin'!"
- `NPC_POPUP_MELEE_CAT_SPIT_SUCCESS_2`: "[m:default]You actually still have enough mana to cast [b]Spit[/b] again."
- `NPC_POPUP_MELEE_CAT_SPIT_SUCCESS_3`: "You can cast spells as many times per turn as you want, as long as you have the [b]mana[/b]."
- `NPC_POPUP_MELEE_CAT_SPIT_SUCCESS_4`: "So [b]Spit[/b] again! Make it a real thick one!"
- `NPC_POPUP_MELEE_CAT_SPIT_FAIL_MISS_1`: "[m:angry]You have the aim of a catholic priest! Come on man!"
- `NPC_POPUP_MELEE_CAT_SPIT_FAIL_MISS_2`: "[m:default]Luckily you still have enough mana to cast [b]Spit[/b] again."
- `NPC_POPUP_MELEE_CAT_SPIT_FAIL_MISS_3`: "You can cast spells as many times per turn as you want, as long as you have the mana."
- `NPC_POPUP_MELEE_CAT_SPIT_FAIL_MISS_4`: "Go on, [b]Spit[/b] again!"
- `NPC_POPUP_MELEE_CAT_SPIT_FAIL_RAT_1`: "[m:confused]I mean sure, destroying that rat's body was cool and all, but you really need to hit that Tom Tom."
- `NPC_POPUP_MELEE_CAT_SPIT_FAIL_RAT_2`: "[m:default]Good thing you still have enough mana to cast [b]Spit[/b] again."
- `NPC_POPUP_MELEE_CAT_SPIT_FAIL_RAT_3`: "You can cast spells as many times per turn as you want, as long as you have the mana."
- `NPC_POPUP_MELEE_CAT_SPIT_FAIL_RAT_4`: "So [b]Spit[/b] again!"
- `NPC_POPUP_MELEE_CAT_SPIT_FAIL_ALLY_1`: "[m:angry]There is a time and a place for stuff like that, keep your eyes on the prize dude!"
- `NPC_POPUP_MELEE_CAT_SPIT_FAIL_ALLY_2`: "[m:default]Good thing you still have enough mana to cast [b]Spit[/b] again."
- `NPC_POPUP_MELEE_CAT_SPIT_FAIL_ALLY_3`: "You can cast spells as many times per turn as you want, as long as you have the mana."
- `NPC_POPUP_MELEE_CAT_SPIT_FAIL_ALLY_4`: "So [b]Spit[/b] again!"
- `NPC_POPUP_MELEE_CAT_SPIT_IGNORE_1`: "[m:sad]You're ignoring what I'm telling you to do."
- `NPC_POPUP_MELEE_CAT_SPIT_IGNORE_2`: "[m:angry][b]Spit[/b] on the enemy, or I swear to God, I'm leaving!"
- `NPC_POPUP_DONE_SPITTING_SUCCESS_1`: "[m:happy]Good job!"
- `NPC_POPUP_DONE_SPITTING_SUCCESS_2`: "At this point I trust that you can finish the rest of the fight on your own."
- `NPC_POPUP_DONE_SPITTING_SUCCESS_3`: "So I'm going to go hide in those bushes and judge you from afar. <br/> Good luck!"
- `NPC_POPUP_DONE_SPITTING_FAIL_MISS_1`: "[m:confused]Look... I'm trying. I'm really trying."
- `NPC_POPUP_DONE_SPITTING_FAIL_MISS_2`: "[m:default]But now you need to try. Finish the job yourself, I'm outta here."
- `NPC_POPUP_DONE_SPITTING_FAIL_RAT_1`: "Yeah you attacked a dead body, sure. But you still gotta kill that Tom Tom."
- `NPC_POPUP_DONE_SPITTING_FAIL_RAT_2`: "At this point I trust that you can finish the rest of the fight on your own. Bye."
- `NPC_POPUP_DONE_SPITTING_FAIL_ALLY_1`: "[m:veryangry]No no no NO NO! Idiot! [m:angry]That was your teammate."
- `NPC_POPUP_DONE_SPITTING_FAIL_ALLY_2`: "[m:sad]Look... I'm trying. I'm really trying."
- `NPC_POPUP_DONE_SPITTING_FAIL_ALLY_3`: "But now you need to try. Good luck with the rest of the fight."
- `NPC_POPUP_DO_NOT_END_TURN_1`: "Do not end your turn yet. I'm still telling you to do things..."
- `NPC_POPUP_TUTORIAL_CAT_DIES_1`: "[m:sad]Well damn, it looks like {Catname} got hit pretty hard."
- `NPC_POPUP_TUTORIAL_CAT_DIES_2`: "[m:default]Don't worry though, {he's} not dead yet. Only [b]Downed[/b]."
- `NPC_POPUP_TUTORIAL_CAT_DIES_3`: "When a cat gets [b]Downed[/b] in a fight, they get [c:red]injured[/c] and one of their stats gets reduced. [a:shake]Permanently[/a]."
- `NPC_POPUP_TUTORIAL_CAT_DIES_4`: "Don't let their body get hit too many times, or they will actually die."
- `NPC_POPUP_TUTORIAL_CAT_DIES_5`: "As long as your other cats can finish the fight, your [b]Downed[/b] cats will still survive. So finish the fight!"
- `NPC_POPUP_CAN_STILL_USE_ATTACK_1`: "Hey, hold on buddy. Don't end your turn just yet."
- `NPC_POPUP_CAN_STILL_USE_ATTACK_2`: "Even though you already cast spells this turn..."
- `NPC_POPUP_CAN_STILL_USE_ATTACK_3`: "[m:pointleft]That doesn't stop you from also using your basic attack. So attack!"
- `NPC_POPUP_CAN_STILL_USE_ATTACK_DIDNTSPELL_1`: "Hey, hold on buddy. Don't end your turn just yet."
- `NPC_POPUP_CAN_STILL_USE_ATTACK_DIDNTSPELL_2`: "[m:pointleft]You didn't even attack yet. So attack!"
- `NPC_POPUP_LEVEL_UP_INTRO_1`: "Beginner's luck."
- `NPC_POPUP_LEVEL_UP_INTRO_2`: "OK, now listen. <br/> Each time you finish combat one of your cats is gonna level up."
- `NPC_POPUP_LEVEL_UP_INTRO_3`: "[m:happy]Check out ol' {Catname}, {he's} about to get a whole lot better, <br/> [m:pointleft]just look at all these options!"
- `NPC_POPUP_LEVEL_UP_INTRO_4`: "[m:default]Originally I was gonna let you choose yourself, but I feel the need to point something out."
- `NPC_POPUP_LEVEL_UP_INTRO_5`: "There's a pretty awesome combo here."
- `NPC_POPUP_LEVEL_UP_INTRO_6`: "Check out {Catname's} current passive effect up there."
- `NPC_POPUP_LEVEL_UP_INTRO_7`: "[m:pointleft]Now read what [b]Sunburn[/b] does."
- `NPC_POPUP_LEVEL_UP_INTRO_8`: "[m:happy]Sunburn makes things burn <br/> and [b]Hot Blooded[/b] make burn more burny![/m]"
- `NPC_POPUP_LEVEL_UP_INTRO_9`: "[m:pointleft]So take [b]Sunburn[/b] already! <br/> Or not, <br/> it's your funeral.[/m]"
- `NPC_POPUP_LEVEL_UP_SELECTED_SUNBURN_1`: "[m:happy]Someone's learning!"
- `NPC_POPUP_LEVEL_UP_SELECTED_SUNBURN_2`: "OK but remember, [b]every cat is different[/b]. <br/> So always check out what your cat's passive ability does."
- `NPC_POPUP_LEVEL_UP_SELECTED_SUNBURN_3`: "A cat's passives can make or break a run, and combos win games!"
- `NPC_POPUP_LEVEL_UP_SELECTED_SUNBURN_4`: "Always be on the lookout for abilities that combo!"
- `NPC_POPUP_LEVEL_UP_DIDNT_SELECT_SUNBURN_1`: "[m:sad]Yeah.. OK, whatever.[/m]"
- `NPC_POPUP_LEVEL_UP_DIDNT_SELECT_SUNBURN_2`: "[m:bored]Look, it's your life, <br/> screw it up however you want."
- `NPC_POPUP_LEVEL_UP_DIDNT_SELECT_SUNBURN_3`: "But you should check what the cat can do before making decisions too rashly..."
- `NPC_POPUP_LEVEL_UP_DIDNT_SELECT_SUNBURN_4`: "[m:default]Learning your cat's passive ability can be the key to winning a fight."
- `NPC_POPUP_LEVEL_UP_DIDNT_SELECT_SUNBURN_5`: "[m:angry]But keep in mind, [b]Every cat is different[/b], <br/> Pay attention to how their abilities work!!!"
- `NPC_POPUP_LEVEL_UP_DIDNT_SELECT_SUNBURN_6`: "And always look for combos! Seriously I can't stress this enough."
- `NPC_POPUP_LEVEL_UP_DIDNT_SELECT_SUNBURN_7`: "Git good!"
- `NPC_POPUP_BOSS_FIGHT_INTRO_1`: "It is time for a Boss Fight!"
- `NPC_POPUP_BOSS_FIGHT_INTRO_2`: "[m:happy]I trained Pebbles here myself. <br/> [a:shake]He's about to rock your world.[/a]"
- `NPC_POPUP_BOSS_FIGHT_INTRO_3`: "Show me what you got!"
- `NPC_POPUP_BOSS_FIGHT_INTRO_4`: "Oh also... one last tip before I leave it up to you."
- `NPC_POPUP_BOSS_FIGHT_INTRO_5`: "[m:whispering]Attack from behind to do more damage!"
- `NPC_POPUP_USE_WEAPON_1`: "Hey, hold on buddy. Don't end your turn just yet."
- `NPC_POPUP_USE_WEAPON_2`: "[m:pointleft]You can still attack with your [b]Weapon[/b]."
- `NPC_POPUP_USE_WEAPON_3`: "[b]Weapons[/b] (and other items) can be used once a turn even if you already used your attack."
- `NPC_POPUP_USE_ATTACK_AFTER_USED_WEAPON_1`: "Hey, hold on buddy. Don't end your turn just yet."
- `NPC_POPUP_USE_ATTACK_AFTER_USED_WEAPON_2`: "Even though you already attacked with your [b]Weapon[/b]..."
- `NPC_POPUP_USE_ATTACK_AFTER_USED_WEAPON_3`: "[m:pointleft]That doesn't stop you from also using your basic attack. So attack!"
- `NPC_POPUP_BOSS_FIGHT_ROUND2_1`: "Hey, so you might have noticed this already, but take a look up here."
- `NPC_POPUP_BOSS_FIGHT_ROUND2_2`: "This is the order that you and your enemies take their turns."
- `NPC_POPUP_BOSS_FIGHT_ROUND2_3`: "The turn order is usually the same every round. So pay attention to it! <br/> Or don't."
- `NPC_POPUP_MAP_CLICK_NODE_1`: "[m:pointdiagonal]Pssst.... click here."
- `NPC_POPUP_MAP_EQUIP_ITEMS_1`: "Hold up. <br/> You do not want to go into this boss fight unprepared."
- `NPC_POPUP_MAP_EQUIP_ITEMS_2`: "[m:pointdiagonal]You have items that you have not yet equipped to your cats. Click here to equip them first."
- `NPC_POPUP_MAP_EQUIP_ITEMS2_1`: "[m:angry]Equip the damn items!"
- `NPC_POPUP_FINISH_ADVENTURE_1`: "Congrats, you did good out there."
- `NPC_POPUP_FINISH_ADVENTURE_2`: "This marks the end of your first little adventure. <br/> It's time to go home."
- `NPC_POPUP_FINISH_ADVENTURE_3`: "[m:pointdiagonal]You will bring back any food, coins, items, treasures and injuries you gained during your journey."
- `NPC_POPUP_FINISH_ADVENTURE_4`: "These supplies will hopefully prove useful to you at some point."
- `NPC_POPUP_FINISH_ADVENTURE_5`: "[m:pointdiagonal]Oh, and if you ever wanna save and exit a run, <br/> Just click that thing."
- `NPC_POPUP_FINISH_ADVENTURE_6`: "[m:default]Bye!"
- `NPC_POPUP_HOUSE_INTRO_1`: "[m:veryhappy][a:wave]Well hello neighbor![/a]"
- `NPC_POPUP_HOUSE_INTRO_2`: "[m:happy]Yes, it's me, <br/> Mr. Tinkles."
- `NPC_POPUP_HOUSE_INTRO_3`: "[m:default]You've no doubt heard about me around town... <br/> [m:happy]And yes, all the rumors are true!"
- `NPC_POPUP_HOUSE_INTRO_4`: "[m:winking]I spread them myself!"
- `NPC_POPUP_HOUSE_INTRO_5`: "[s:.6][m:whispering]Just like my legs...[/s]"
- `NPC_POPUP_HOUSE_INTRO_6`: "[m:shocked][a:shake]WHAT AM I SAYING!?[/a]"
- `NPC_POPUP_HOUSE_INTRO_7`: "[m:veryhappy]God I'm so bad. <br/> [m:default]Anyway, you can call me [b][s:1.2]Tink[/s][/b]."
- `NPC_POPUP_HOUSE_INTRO_8`: "[m:shocked]My God! <br/> Look at these kitties! They just returned home from an adventure and they look [a:shake]busted[/a]."
- `NPC_POPUP_HOUSE_INTRO_9`: "[m:default]Cats that have already been on an adventure are [o:black][c:white][img:retired]retired[/c][/o]."
- `NPC_POPUP_HOUSE_INTRO_10`: "That means they wont be going on any more adventures."
- `NPC_POPUP_HOUSE_INTRO_11`: "[m:pointleft]So why don't you take these guys inside so they can relax comfortably."
- `NPC_POPUP_HOUSE_PASS_DAY_1`: "[m:happy]Well they seem pretty comfortable, <br/> [s:.8][m:questioning]I guess[/m][/s]."
- `NPC_POPUP_HOUSE_PASS_DAY_2`: "[m:pointright]So, You can now end the day and watch what happens when the lights go off!"
- `NPC_POPUP_HOUSE_PASS_DAY_3`: "When you end the day, every cat will eat one food. [m:questioning]Make sure you always have more than enough!"
- `NPC_POPUP_TAKE_CATS_INSIDE_1`: "[m:pondering]Ew... you left some cats outside. They won't shut up, quick put them inside."
- `NPC_POPUP_HOUSE_STRAYS_1`: "[m:happy]Oh my, what an eventful night! Don't tell my wife about what we saw!"
- `NPC_POPUP_HOUSE_STRAYS_2`: "Aw! You have a new kitten! {He} will need to grow up before {he} can go on an adventure though."
- `NPC_POPUP_HOUSE_STRAYS_3`: "Don't worry, there is something in the water here that makes them grow up in like 1 day."
- `NPC_POPUP_HOUSE_STRAYS_4`: "[m:pointleft]Also look! <br/> A stray cat has come to your house looking for love!"
- `NPC_POPUP_HOUSE_STRAYS_5`: "[m:questioning]You should totes take {him} inside, right?"
- `NPC_POPUP_HOUSE_PASS_DAY2_1`: "Once you have made enough kittens or collected enough strays, you can take them out on an adventure to find more supplies."
- `NPC_POPUP_HOUSE_PASS_DAY2_2`: "[m:happy]You'll want 4 fresh kitties to send out on an adventure. But you don't have enough yet."
- `NPC_POPUP_HOUSE_PASS_DAY2_3`: "[m:default]So just like, keep ending the day and collecting strays until you do."
- `NPC_POPUP_HOUSE_PASS_DAY2_4`: "[m:mocking]Also, you can right click the kitten to see if {he} inherited anything from {his} parents, and check {his} stats."
- `NPC_POPUP_NEW_ADVENTURE_1`: "[m:pointleft]Oh, Yay! With that new stray there, you should have enough cats to go on another adventure."
- `NPC_POPUP_NEW_ADVENTURE_2`: "[m:pointright]Go put them in the adventure box and get ready for a journey!"
- `NPC_POPUP_LOW_ON_FOOD_1`: "[m:paranoid]Hey uh, I don't want to freak you out but..."
- `NPC_POPUP_LOW_ON_FOOD_2`: "[m:paranoid]You have like almost no food. You might wanna go on an adventure to find some more."
- `NPC_POPUP_LOW_ON_FOOD_3`: "[m:pointright]Go put them in the adventure box and get ready for a journey!"
- `NPC_POPUP_HOUSE_RETIRED_CAT_BOX_1`: "[m:spacedout]That cat cannot be put into the adventure box because {he} is [o:black][c:white][img:retired]retired[/c][/o]."
- `NPC_POPUP_HOUSE_KITTEN_BOX_1`: "[m:happy]Aw, that cat can't go on an adventure yet, {he's} still a kitten and needs to grow up!"
- `NPC_POPUP_HOUSE_KITTEN_BOX_2`: "[m:sad]{he} just a baybay!"
- `NPC_POPUP_HOUSE_STARRED_BOX_1`: "[m:spacedout]{He} can't be put into the adventure box because {he} already defended against a house boss!"
- `NPC_POPUP_HOUSE_STARRED_BOX_2`: "[m:winking]WHAT A DIVA!"
- `NPC_POPUP_HOUSE_PIPE_1`: "Oh... <br/> [s:.8]It's Rainin' again.[/s]"
- `NPC_POPUP_HOUSE_PIPE_2`: "[m:paranoid]Rain is a spookie one. [s:.8]I think it rain cuz we did bad things...[/s]"
- `NPC_POPUP_HOUSE_PIPE_3`: "[m:bored]The rain man sees what we be doing <br/> [s:.8]and he tells on us.[/s]"
- `NPC_POPUP_HOUSE_PIPE_4`: "[m:sad][s:.6]*huff huff*[/s]"
- `NPC_POPUP_HOUSE_PIPE_5`: "[m:happy]We are Frank and we live under your house!"
- `NPC_POPUP_HOUSE_PIPE_6`: "[m:default]I bet you hear us scratchin'... <br/> [s:.8]It gets itchy down here sometimes...[/s]"
- `NPC_POPUP_HOUSE_PIPE_7`: "Sometimes we like <br/> being itchy, [m:happy][s:.8]cuz being itchy makes us work harder![/s]"
- `NPC_POPUP_HOUSE_PIPE_8`: "Bet you didn't know Frank builded your house! [s:.8]No lying![/s]"
- `NPC_POPUP_HOUSE_PIPE_9`: "We make them houses as fast as we make brown!"
- `NPC_POPUP_HOUSE_PIPE_10`: "[m:sad][s:.6]*cough cough*[/s]"
- `NPC_POPUP_HOUSE_PIPE_11`: "[m:veryhappy]Hahaha! <br/> [s:.8]We are just kidding on you![/s]"
- `NPC_POPUP_HOUSE_PIPE_12`: "[m:happy]But really we love to build! So if you gonna wanna have more house made, just ask Frank."
- `NPC_POPUP_HOUSE_PIPE_13`: "[m:default]Frank do need <br/> to be paid though, <br/> [s:.8]we don't work for <br/> kisses no more.[/s] <br/> [s:.7]No... Frank wants friends.[/s]"
- `NPC_POPUP_HOUSE_PIPE_14`: "[m:happy][a:shake][s:1.4]Cat friends![/s][/a]"
- `NPC_POPUP_HOUSE_PIPE_15`: "[m:default]See that [b]pipe[/b] over there? <br/> [s:.8]That [b]pipes[/b] goes all over this places![/s]"
- `NPC_POPUP_HOUSE_PIPE_16`: "You wanna send a kitty out? Push him down that [b]pipe[/b] and bam! <br/> [s:.8][m:happy]There he go![/s]"
- `NPC_POPUP_HOUSE_PIPE_17`: "[m:sad][s:.6]*huff huff*[/s]"
- `NPC_POPUP_HOUSE_PIPE_18`: "[m:default]We don't want just any kitty though, <br/> [s:.8]Frank want [o:black][c:white][img:retired]Retired[/c][/o] cats only.[/s]"
- `NPC_POPUP_HOUSE_PIPE_19`: "Frank think we like retired cats <br/> [s:.8]cuz we are kind of retired too.[/s]"
- `NPC_POPUP_HOUSE_PIPE_20`: "[m:happy]OK well, <br/> [s:.8]we go night night![/s]"
- `NPC_POPUP_INTRODUCE_HARD_PATH_1`: "[m:whispering]Psst... hey..."
- `NPC_POPUP_INTRODUCE_HARD_PATH_2`: "[m:default]You now have a choice of which paths you can take."
- `NPC_POPUP_INTRODUCE_HARD_PATH_3`: "You can keep going right to take the easy way out, like you did last time."
- `NPC_POPUP_INTRODUCE_HARD_PATH_4`: "[m:whispering]But I heard there's some cool stuff if you go south here."
- `NPC_POPUP_INTRODUCE_HARD_PATH_5`: "[m:happy]Better items, harder fights, more rewards. The path of the strong."
- `NPC_POPUP_INTRODUCE_HARD_PATH_6`: "[m:default]Your choice!"
- `NPC_POPUP_FIRST_HOUSE_BOSS_TOMORROW_1`: "[m:shocked]GAH! <br/> That cannibalistic feline plumper is coming this way!"
- `NPC_POPUP_FIRST_HOUSE_BOSS_TOMORROW_2`: "[m:scared]I can see her huffing and puffing her way up the hill..."
- `NPC_POPUP_FIRST_HOUSE_BOSS_TOMORROW_3`: "You got like one day 'till she gets here!"
- `NPC_POPUP_FIRST_HOUSE_BOSS_TOMORROW_4`: "[m:default]I'll give you a few tips."
- `NPC_POPUP_FIRST_HOUSE_BOSS_TOMORROW_5`: "[m:happy]First, make sure you bring weapons and armor. Don't be fighting in the nude! This isn't ancient Greece!"
- `NPC_POPUP_FIRST_HOUSE_BOSS_TOMORROW_6`: "[m:bored][s:.7]Sadly...[/s]"
- `NPC_POPUP_FIRST_HOUSE_BOSS_TOMORROW_7`: "[m:default]Also, make sure you use [o:black][c:white][img:retired]retired[/c][/o] cats to defend your house! <br/> They are old and skilled!"
- `NPC_POPUP_FIRST_HOUSE_BOSS_TOMORROW_8`: "[m:pondering]And at the very least, maybe this monster's fists will get snagged on their ungodly amount of disgusting wrinkles."
- `NPC_POPUP_FIRST_HOUSE_BOSS_TOMORROW_9`: "[m:grossedout]Eww..."
- `NPC_POPUP_FIRST_HOUSE_BOSS_TOMORROW_10`: "[m:happy]Gawd, kill me if I ever get old!"
- `NPC_POPUP_FIRST_HOUSE_HINT_RETIRED_1`: "[m:shocked]What are you doing? <br/> Those cats are babies!!!"
- `NPC_POPUP_FIRST_HOUSE_HINT_RETIRED_2`: "[m:veryangry]You'd be sending them in like sheep to the slaughter! <br/> What kind of person are you!?"
- `NPC_POPUP_FIRST_HOUSE_HINT_RETIRED_3`: "[m:angry]Send the [o:black][c:white][img:retired]retired[/c][/o] cats out there!"
- `NPC_POPUP_FIRST_HOUSE_HINT_RETIRED_4`: "[m:confused]They are old and worthless, <br/> but at least have a fighting chance!"
- `NPC_POPUP_JACK_INTRODUCTION_1`: "Hey Dude! <br/> I was lookin' in your windows and seen you got lotsa cool junk in there!"
- `NPC_POPUP_JACK_INTRODUCTION_2`: "Oh me? <br/> I'm Baby Jack! <br/> At least that's what the people around here call me..."
- `NPC_POPUP_JACK_INTRODUCTION_3`: "[m:happy]My Nona says its cuz of how talented I am. <br/> I'm a superhero you know?!"
- `NPC_POPUP_JACK_INTRODUCTION_4`: "[m:default]Nona also says good boys do nice things, <br/> so I got's a gift for ya!"
- `NPC_POPUP_JACK_INTRODUCTION_5`: "What I just gived you, that's what rich people call <br/> [b]"furniture"[/b]."
- `NPC_POPUP_JACK_INTRODUCTION_6`: "[m:happy]Furniture around these parts is filled with Jesus juice! <br/> [s:.7][m:whispering]But we can talk about that later.[/s]"
- `NPC_POPUP_JACK_INTRODUCTION_7`: "[m:default]See that tab up there? <br/> Click it, then you can fill your house will all kinda junk!"
- `NPC_POPUP_JACK_INTRODUCTION_8`: "If you need me, I'll be with Nona in my lil' shack! <br/> [m:happy]See ya!"
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_1`: "[m:happy]Oh Hey! It's me, Steven!"
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_2`: "[m:pondering]You may know me from such games as Time Fcuk, <br/> The End is Nigh or <br/> [s:1.2]The Binding of Isaac! [/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_3`: "[m:default]But from here on out you're probably going to remember me as that Mr. Resetti guy."
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_4`: "[m:bored] . . ."
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_5`: "[m:happy]Yeah, I'm here because I can see you are [a:shake]fcuking[/a] with the game save."
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_6`: "[m:bored]Or maybe you just "accidentally" exited during combat."
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_7`: "[s:1.2]Suuuuure.[/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_8`: "[m:default]Sadly there are consequences to messing with fate... and I'm here to dish them out."
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_9`: "[m:angry]Maybe <br/> I'll burn your house down..."
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_10`: "[m:veryangry][s:1.5]OR KILL YOUR PARENTS!!![/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_11`: "[m:default]No, seriously <br/> I dish out [s:.8]IRL curses[/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_12`: "Like those ones where someone calls you at 3am..."
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_13`: "[m:paranoid]Then Bloody Mary comes out of the mirror and kills you!"
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_14`: "[m:default]it's like that, <br/> but worse, [m:angry]because this is <br/> [s:1.2]REAL real![/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_15`: "[m:bored]. . ."
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_16`: "[m:questioning]So let me break down the rules."
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_17`: "[m:default]If you try and mess with the save during combat, each run you get one pass!"
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_18`: "[m:angry][s:1.2]ONE CHANCE![/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_19`: "[m:veryangry][s:1.5]ONE OOPSIE DO-OVER![/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_20`: "[m:winking]After that, the gloves are off and I just start coming through the monitor making a brain slushie!"
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_21`: "[m:happy]Understood!?"
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_22`: "[m:bored]. . ."
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_23`: "[m:questioning]If you wanna [s:1.2][b]save and exit[/b][/s] without seeing me, just do it from the map or whatever!"
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_24`: "[m:happy]See you soon!"
- `NPC_POPUP_STEVEN_SAVESCUM_100_1`: "i"
- `NPC_POPUP_STEVEN_SAVESCUM_100_2`: "am"
- `NPC_POPUP_STEVEN_SAVESCUM_100_3`: "error"
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_1`: "Well it seems we meet again.  Yep it's me, <br/> Steven."
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_2`: "[m:pondering]You may know me from such games as Time Fcuk, <br/> The End is Nigh or <br/> [s:1.2]The Binding of Isaac! [/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_3`: "[m:default]But from here on out you're probably going to remember me as that Mr. Resetti guy."
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_4`: ". . ."
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_5`: "[m:happy]Yeah, I'm here because I can see you are [a:shake]fcuking[/a] with the game save."
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_6`: "[m:default]Sadly, there are consequences to messing with fate... and I'm here to dish them out."
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_7`: "[m:angry]Maybe <br/> I'll burn your house down..."
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_8`: "[m:veryangry][s:1.5]OR KILL YOUR PARENTS!!![/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_9`: "[s:1.5]!  !  ![/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_10`: "[m:default]No seriously <br/> I dish out [s:.8]IRL curses[/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_11`: "like those ones where someone calls you at 3am..."
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_12`: "[m:paranoid]Then Bloody Mary comes out of the mirror and kills you!"
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_13`: "[m:default]It's like that, <br/> but worse, [m:angry]because this is <br/> [s:1.2]REAL real![/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_14`: ". . ."
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_15`: "[m:veryangry][s:1.5]SO STOP SAVE SCUMMING![/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_16`: "[m:questioning]Accept defeat, <br/> you [a:shake]fcuked[/a] up! Move on!"
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_17`: "[m:default]This is your last warning, <br/> if you see me again..."
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_18`: "[m:angry]BAD STUFF IS GOING DOWN!"
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_19`: ". . ."
- `NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_20`: "[m:happy]See you soon!"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_1_1`: "Hey, yeah so hi again."
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_1_2`: "[m:pondering]It seems you might have had some regrets and tried to undo them?"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_1_3`: "[m:default]Sadly there is no ctrl+z in real life pal, <br/> [m:angry] NO DO OVERS!"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_1_4`: ". . ."
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_1_5`: "[m:whispering]Well, I guess you get one do over..."
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_1_6`: "[m:default]But ONLY because this is the first time this has happened on this run!"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_1_7`: "[m:happy]Keep it up and you're bound to give your cats brain damage.[/m]"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_1_8`: ". . ."
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_1_9`: "[m:veryangry]Also <br/> [s:1.5]I'LL KILL YOU![/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_1_10`: "[m:happy]See ya![/m]"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_2_1`: "[m:veryangry][s:1.2]CHEATER! [a:shake]FCUKING[/a] CHEATER![/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_2_2`: "[m:angry]Honestly, are you just trying to see what will happen?"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_2_3`: "[m:questioning]Or do you just get off on owning cats with smooth brains?"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_2_4`: "[m:default]All of your cats are now experiencing [b]deja vu[/b]!"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_2_5`: "Listen, I don't make the rules here."
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_2_6`: "[m:whispering][s:.8]Those were established by two basement dwelling autists...[/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_2_7`: "[m:paranoid]. . ."
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_2_8`: "[m:default]If this happens again your run is toast, like seriously."
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_2_9`: "[m:angry]Stop Save scumming, just play it out and learn from your mistakes!"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_2_10`: "[m:happy][s:1.2]Last warning![/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_1`: "[m:questioning]What are you trying to prove here?"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_2`: "[m:angry]It's obvious that either you suck, or your cats suck."
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_3`: "[m:pondering]Do you seriously think resetting over and over is going to help?"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_4`: "[m:angry]I feel like you are just [a:shake]fcuking[/a] with me at this point."
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_5`: "[m:happy]And the only person I let do that is Steven!"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_6`: "[s:.9]and maybe Steven[/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_7`: "[s:.8]and maybe Steven[/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_8`: "[s:.7]and maybe Steven[/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_9`: "[s:.6]and maybe Steven[/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_10`: "[s:.5]and maybe Steven[/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_11`: "[s:.4]and maybe Steven[/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_12`: "[s:.3]and maybe Steven[/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_13`: "[s:.2]and maybe Steven[/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_14`: "[s:.1]and maybe Steven[/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_15`: "[s:.08]and maybe Steven[/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_16`: "[s:.06]and maybe Steven[/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_17`: "[s:.05]and maybe Steven[/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_18`: "[s:.04]and maybe Steven[/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_19`: "[s:.03]and maybe Steven[/s]"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_100_1`: "i"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_100_2`: "am"
- `NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_100_3`: "error"
- `NPC_POPUP_STEVEN_SAVESCUM_1ALT1_1`: "[m:angry]Yeah, you are doing that thing again..."
- `NPC_POPUP_STEVEN_SAVESCUM_1ALT1_2`: "Fiddling with the rules.."
- `NPC_POPUP_STEVEN_SAVESCUM_1ALT1_3`: "Bending them like a pretzel and just having your way with 'em!"
- `NPC_POPUP_STEVEN_SAVESCUM_1ALT1_4`: "[m:veryangry]SHAME!"
- `NPC_POPUP_STEVEN_SAVESCUM_1ALT1_5`: "[m:questioning]I'm going to just act like I didn't see that so, go about your playthrough."
- `NPC_POPUP_STEVEN_SAVESCUM_1ALT1_6`: "[m:angry]But if it happens again there will be hell to pay!"
- `NPC_POPUP_STEVEN_SAVESCUM_1ALT1_7`: "You have one warning!"
- `NPC_POPUP_STEVEN_SAVESCUM_1ALT1_8`: "[m:veryangry]And this is that warning!"
- `NPC_POPUP_STEVEN_SAVESCUM_1ALT1_9`: "[m:veryhappy]If I see you again I'm coming through this screen to commence the stabbing!!"
- `NPC_POPUP_STEVEN_SAVESCUM_1ALT2_1`: "[m:angry]CAUGHT YOU AGAIN!"
- `NPC_POPUP_STEVEN_SAVESCUM_1ALT2_2`: "You can't keep doing this!"
- `NPC_POPUP_STEVEN_SAVESCUM_1ALT2_3`: "[m:pondering]..."
- `NPC_POPUP_STEVEN_SAVESCUM_1ALT2_4`: "Well I guess you can, but like..."
- `NPC_POPUP_STEVEN_SAVESCUM_1ALT2_5`: "[m:veryangry]WELL, I DON'T LIKE IT!"
- `NPC_POPUP_STEVEN_SAVESCUM_1ALT2_6`: "[m:paranoid]It just feels weird to be pulled from what I was doing to yell at you!"
- `NPC_POPUP_STEVEN_SAVESCUM_1ALT2_7`: "[m:angry]Like, I could have been in the middle of... anything!"
- `NPC_POPUP_STEVEN_SAVESCUM_1ALT2_8`: "[m:default]No penalty this time, but next time..."
- `NPC_POPUP_STEVEN_SAVESCUM_1ALT2_9`: "[m:veryangry]YOU DIE!"
- `NPC_POPUP_STEVEN_SAVESCUM_1ALT3_1`: "[m:angry]YOU SON OF A BITCH!"
- `NPC_POPUP_STEVEN_SAVESCUM_1ALT3_2`: "[m:angry]YOU ARE DOING IT AGAIN!"
- `NPC_POPUP_STEVEN_SAVESCUM_1ALT3_3`: "[m:veryangry]CHEATING! SAVE SCUMMING!"
- `NPC_POPUP_STEVEN_SAVESCUM_1ALT3_4`: "LOOK EVERYONE! THIS GUY LIKES TO CHEAT!"
- `NPC_POPUP_STEVEN_SAVESCUM_1ALT3_5`: "[m:paranoid]Or girl? It's hard to see from this side..."
- `NPC_POPUP_STEVEN_SAVESCUM_1ALT3_6`: "[m:angry]LOOK AT THIS THING! LOOK AT IT CHEAT!"
- `NPC_POPUP_STEVEN_SAVESCUM_1ALT3_7`: "[m:default]... OK, that's enough punishment."
- `NPC_POPUP_STEVEN_SAVESCUM_1ALT3_8`: "[m:angry]This was your warning! Any more cheating and I come kill you as per usual!"
- `NPC_POPUP_STEVEN_SAVESCUM_2ALT1_1`: "[m:sad]Well now lil' {Catname} has had their IQ lowered by 30 or so points..."
- `NPC_POPUP_STEVEN_SAVESCUM_2ALT1_2`: "[m:angry]You did this! You made {Catname} queen of the short bus!"
- `NPC_POPUP_STEVEN_SAVESCUM_2ALT1_3`: "[m:questioning]You know you could have just not cheated right?"
- `NPC_POPUP_STEVEN_SAVESCUM_2ALT1_4`: "[m:default]Then I wouldn't be here yelling at you."
- `NPC_POPUP_STEVEN_SAVESCUM_2ALT1_5`: "[m:bored]Please stop cheating, you are cheapening the experience."
- `NPC_POPUP_STEVEN_SAVESCUM_2ALT1_6`: "[m:veryhappy]AND STOP SKIPPING WHAT I'M SAYING! THIS IS IMPORTANT STUFF!"
- `NPC_POPUP_STEVEN_SAVESCUM_2ALT1_7`: "[m:angry]I could be giving you hints for all you know!"
- `NPC_POPUP_STEVEN_SAVESCUM_2ALT1_8`: "[m:winking]Like this hint... Wear a bag over your face!"
- `NPC_POPUP_STEVEN_SAVESCUM_2ALT2_1`: "[m:questioning]What the hell dude! I told you to stop this!"
- `NPC_POPUP_STEVEN_SAVESCUM_2ALT2_2`: "[m:angry]It's like you've got some sick addiction to cheating and giving your cats early onset dementia."
- `NPC_POPUP_STEVEN_SAVESCUM_2ALT2_3`: "[m:default]{Catname} doesn't even respond when called... Look."
- `NPC_POPUP_STEVEN_SAVESCUM_2ALT2_4`: "[m:whispering]{Catname}! {Catname}! Look over here! Pssst pssst!"
- `NPC_POPUP_STEVEN_SAVESCUM_2ALT2_5`: "[m:bored]See? Nothing..."
- `NPC_POPUP_STEVEN_SAVESCUM_2ALT2_6`: "[m:questioning]You feel good about this?"
- `NPC_POPUP_STEVEN_SAVESCUM_2ALT2_7`: "[m:veryangry]WELL I DON'T! BECAUSE I HAVE SOUL!"
- `NPC_POPUP_STEVEN_SAVESCUM_2ALT2_8`: "YOU SOULLESS MONSTER!"
- `NPC_POPUP_STEVEN_SAVESCUM_2ALT3_1`: "[m:angry]LIAR! YOU SAID YOU WEREN'T GOING TO KEEP DOING THIS!"
- `NPC_POPUP_STEVEN_SAVESCUM_2ALT3_2`: "How can we establishing a trusting relationship when you"
- `NPC_POPUP_STEVEN_SAVESCUM_2ALT3_3`: "[m:veryangry]KEEP"
- `NPC_POPUP_STEVEN_SAVESCUM_2ALT3_4`: "CHEATING"
- `NPC_POPUP_STEVEN_SAVESCUM_2ALT3_5`: "CONSTANTLY!?"
- `NPC_POPUP_STEVEN_SAVESCUM_2ALT3_6`: "[m:angry]Remember little {Catname}? Look at them now!"
- `NPC_POPUP_STEVEN_SAVESCUM_2ALT3_7`: "They don't even know I'm talking about them!"
- `NPC_POPUP_STEVEN_SAVESCUM_2ALT3_8`: "[m:whispering]Earth to {Catname} CAN YOU HEAR ME?!!?"
- `NPC_POPUP_STEVEN_SAVESCUM_2ALT3_9`: "[m:angry]Nothing... You did that to them!"
- `NPC_POPUP_STEVEN_SAVESCUM_2ALT3_10`: "[m:veryangry]STOP!"
- `NPC_POPUP_STEVEN_SAVESCUM_3ALT1_1`: "[m:bored]OK, well now look at them! They are all all donked up!"
- `NPC_POPUP_STEVEN_SAVESCUM_3ALT1_2`: "[m:happy]The derp crew is on the case!"
- `NPC_POPUP_STEVEN_SAVESCUM_3ALT1_3`: "[m:angry]Can't really throw a good punch with your thumb up your butt!"
- `NPC_POPUP_STEVEN_SAVESCUM_3ALT1_4`: "[m:questioning]Whats the point!? Give up! Just end the run already!"
- `NPC_POPUP_STEVEN_SAVESCUM_3ALT1_5`: "[m:pondering]For all you know I'm tracking these save scums..."
- `NPC_POPUP_STEVEN_SAVESCUM_3ALT1_6`: "[m:angry]And sending them to your whole friends list!"
- `NPC_POPUP_STEVEN_SAVESCUM_3ALT1_7`: "[m:veryangry]STOP IT! STOP IT NOW!"
- `NPC_POPUP_STEVEN_SAVESCUM_3ALT1_8`: "[m:default]You know I know your IP address right?..."
- `NPC_POPUP_STEVEN_SAVESCUM_3ALT2_1`: "[m:bored]Your whole crew is now drooling in unison..."
- `NPC_POPUP_STEVEN_SAVESCUM_3ALT2_2`: "Hope you're happy..."
- `NPC_POPUP_STEVEN_SAVESCUM_3ALT2_3`: "[m:questioning]Do you think it's funny? Watching them run into walls all day?"
- `NPC_POPUP_STEVEN_SAVESCUM_3ALT2_4`: "[m:angry]This is what you're into? Cats in adult diapers meowing at rocks?"
- `NPC_POPUP_STEVEN_SAVESCUM_3ALT2_5`: "[m:veryangry]I'M REPORTING THIS!"
- `NPC_POPUP_STEVEN_SAVESCUM_3ALT2_6`: "A SAVE SCUMMER LIKE YOU SHOULD BE PUT ON A WATCH LIST!"
- `NPC_POPUP_STEVEN_SAVESCUM_3ALT2_7`: "[m:default]OK, last chance..."
- `NPC_POPUP_STEVEN_SAVESCUM_3ALT2_8`: "[m:angry]You do this one more time and I'm taking over!"
- `NPC_POPUP_STEVEN_SAVESCUM_3ALT3_1`: "[m:angry]LOOK AT WHAT YOU ARE DOING!"
- `NPC_POPUP_STEVEN_SAVESCUM_3ALT3_2`: "EVERY ONE OF YOUR CATS HAS DEJA VU!"
- `NPC_POPUP_STEVEN_SAVESCUM_3ALT3_3`: "[m:veryangry]ALL OF THEM!"
- `NPC_POPUP_STEVEN_SAVESCUM_3ALT3_4`: "YOU CAN'T WIN LIKE THIS!"
- `NPC_POPUP_STEVEN_SAVESCUM_3ALT3_5`: "YOU'RE SICK YOU KNOW THAT!?"
- `NPC_POPUP_STEVEN_SAVESCUM_3ALT3_6`: "MARK MY WORDS! YOU WILL REGRET THIS!"
- `NPC_POPUP_STEVEN_SAVESCUM_3ALT3_7`: "[m:bored]And now I'm sleepy from all the yelling..."
- `NPC_POPUP_STEVEN_SAVESCUM_3ALT3_8`: "[m:angry]Last chance!"
- `NPC_POPUP_STEVEN_SAVESCUM_4ALT1_1`: "[m:default]Yeah its over, give me the controller..."
- `NPC_POPUP_STEVEN_SAVESCUM_4ALT1_2`: "[m:winking]The cats are toast... Only Steven can save this run!"
- `NPC_POPUP_STEVEN_SAVESCUM_4ALT1_3`: "[m:happy]Just you sit back and watch! I've been watching live streams of this game..."
- `NPC_POPUP_STEVEN_SAVESCUM_4ALT1_4`: "[m:veryhappy]HERE I GO!"
- `NPC_POPUP_STEVEN_SAVESCUM_4ALT2_1`: "[m:angry]If you want me to play the game for you, just ask!"
- `NPC_POPUP_STEVEN_SAVESCUM_4ALT2_2`: "We don't need to do this whole song and dance every damn time!"
- `NPC_POPUP_STEVEN_SAVESCUM_4ALT2_3`: "[m:pondering]OK, how does this work again? Does it auto move the cat or?"
- `NPC_POPUP_STEVEN_SAVESCUM_4ALT2_4`: "[m:winking]Eh, whatever, I'll just wing it..."
- `NPC_POPUP_STEVEN_SAVESCUM_4ALT2_5`: "[m:happy]CHECK THIS OUT!"
- `NPC_POPUP_STEVEN_SAVESCUM_4ALT3_1`: "[m:happy]ANNNNNNND YOURE DONE!"
- `NPC_POPUP_STEVEN_SAVESCUM_4ALT3_2`: "Hand over the controller!"
- `NPC_POPUP_STEVEN_SAVESCUM_4ALT3_3`: "You're being cut off!"
- `NPC_POPUP_STEVEN_SAVESCUM_4ALT3_4`: "[m:veryhappy]IT'S STEVEN'S TURN!"
- `NPC_POPUP_BEANIES_RIFT_INTRO_1`: "[m:shocked]The giant monster activated the obelisk, causing a tear in the fabric of space, opening a portal into the chaos dimension!?"
- `NPC_POPUP_BEANIES_RIFT_INTRO_2`: "!!!"
- `NPC_POPUP_BEANIES_RIFT_INTRO_3`: "[m:happy]Just as I had predicted! All part of the plan!"
- `NPC_POPUP_BEANIES_RIFT_INTRO_4`: "[m:pondering]Now a tear like that would usually invert our reality..."
- `NPC_POPUP_BEANIES_RIFT_INTRO_5`: "[m:winking]But lucky for you I had my fingers crossed when it happened!"
- `NPC_POPUP_BEANIES_RIFT_INTRO_6`: "[m:veryhappy]SCIENCE FOR THE WIN!"
- `NPC_POPUP_BEANIES_RIFT_INTRO_7`: "[m:questioning]Oh, you are probably wondering how I got here..."
- `NPC_POPUP_BEANIES_RIFT_INTRO_8`: "[m:veryhappy]Spoiler: <br/> I'M NOT HERE AT ALL!"
- `NPC_POPUP_BEANIES_RIFT_INTRO_9`: "[m:default]I'm just a hologram being projected from the implant in your brain!"
- `NPC_POPUP_BEANIES_RIFT_INTRO_10`: "[m:winking]Neat right?"
- `NPC_POPUP_BEANIES_RIFT_INTRO_11`: "[m:default]Anyway feel free to continue exploring The Rift, just let me know if you find anything neat!"
- `NPC_POPUP_BEANIES_INFINITE_INTRO_1`: "[m:veryangry]SEE!!!"
- `NPC_POPUP_BEANIES_INFINITE_INTRO_2`: "SEE I FREAKIN' TOLD YOU! I TOLD YOU I WAS THE BEST!"
- `NPC_POPUP_BEANIES_INFINITE_INTRO_3`: "ME! I DID THIS! DO YOU SEE MS. PEPTONE! YOU OLD CRONE! WHO'S MENTALLY DISTURBED NOW!?"
- `NPC_POPUP_BEANIES_INFINITE_INTRO_4`: "[m:angry]NOT ME! HA!"
- `NPC_POPUP_BEANIES_INFINITE_INTRO_5`: "[m:veryangry]I'M HERE GETTING READY TO SEE THE FACE OF GOD! AND ALL YOU ARE DOING IS BEING DEAD!"
- `NPC_POPUP_BEANIES_INFINITE_INTRO_6`: "[m:winking]I should reanimate her like I did with you, just so she can see this..."
- `NPC_POPUP_BEANIES_INFINITE_INTRO_7`: "[m:veryangry]SO SHE CAN WITNESS MY ASTOUNDING GENIUS!!"
- `NPC_POPUP_BEANIES_INFINITE_INTRO_8`: "I UNLOCKED THE INFINITE! ME! BY MYSELF!"
- `NPC_POPUP_BEANIES_INFINITE_INTRO_9`: "[m:veryhappy]NOW GO! GO MY CHILD! ENTER THE INFINITE!"
- `NPC_POPUP_BEANIES_INFINITE_INTRO_10`: "[m:angry]AND TELL THAT SON OF A BITCH WHO SENT YOU!"
- `NPC_POPUP_BEANIES_INFINITE_INTRO_11`: "[m:veryangry]THOMAS A. BEANIES!"
- `NPC_POPUP_BEANIES_VSCREATORINTRO_1`: "[m:scared]Am I coming through OK? How do I look?"
- `NPC_POPUP_BEANIES_VSCREATORINTRO_2`: "[m:shocked]That's the guy? That's the Creator!?"
- `NPC_POPUP_BEANIES_VSCREATORINTRO_3`: "Where are the glasses? The grey tufts of hair!?"
- `NPC_POPUP_BEANIES_VSCREATORINTRO_4`: "[m:grossedout]He looks nothing like a God! <br/> And that robe... what, did someone just get out of the shower!?"
- `NPC_POPUP_BEANIES_VSCREATORINTRO_5`: "[m:bored]Well any hesitation I had about totally erasing him from existence left the room the moment I saw him..."
- `NPC_POPUP_BEANIES_VSCREATORINTRO_6`: "[m:default]OK well, let's get to the fun part... the plan!"
- `NPC_POPUP_BEANIES_VSCREATORINTRO_7`: "[m:happy]It's simple, bring this narcissist down to his primordial form and I'll pop back in and help you arm the nuke."
- `NPC_POPUP_BEANIES_VSCREATORINTRO_8`: "Good luck!"
- `NPC_POPUP_BEANIES_VSCREATOR1_1`: "[m:happy]OK OK, yes here it is... The great ending! I've prepared a little monologue... bear with me... This is more for him than you."
- `NPC_POPUP_BEANIES_VSCREATOR1_2`: "[m:paranoid]*clears throat*"
- `NPC_POPUP_BEANIES_VSCREATOR1_3`: "[m:default]"Dear God.""
- `NPC_POPUP_BEANIES_VSCREATOR1_4`: "[m:veryangry]"You suck!""
- `NPC_POPUP_BEANIES_VSCREATOR1_5`: "[m:angry]"35 years ago you took something from me!""
- `NPC_POPUP_BEANIES_VSCREATOR1_6`: ""Something that wasn't yours! The Soul of my kitten Stacy!""
- `NPC_POPUP_BEANIES_VSCREATOR1_7`: "[m:veryangry]"And for 35 long years I've tried to bring her back, rebuilding her from her original DNA 100 times over!""
- `NPC_POPUP_BEANIES_VSCREATOR1_8`: "[m:sad]"But she wasn't Stacy... just something that looked like her...""
- `NPC_POPUP_BEANIES_VSCREATOR1_9`: "[m:angry]"What right do you have to take the one thing in the world from me that I cared for!?""
- `NPC_POPUP_BEANIES_VSCREATOR1_10`: "[m:sad]"Stacy was loved! She was needed... We were a team!""
- `NPC_POPUP_BEANIES_VSCREATOR1_11`: "[m:veryangry]"And you took her from me!""
- `NPC_POPUP_BEANIES_VSCREATOR1_12`: "[m:angry]"And now I take something from you!""
- `NPC_POPUP_BEANIES_VSCREATOR1_13`: "[m:bored]..."
- `NPC_POPUP_BEANIES_VSCREATOR1_14`: "[m:happy]OK, now press the button that destroys all of existence!"
- `NPC_POPUP_BEANIES_VSCREATOR2_1`: "[m:angry]Hey, press the button!"
- `NPC_POPUP_BEANIES_VSCREATOR2_2`: "[m:questioning]What are you doing!? You are making me look like an asshole here..."
- `NPC_POPUP_BEANIES_VSCREATOR2_3`: "[m:shocked]..."
- `NPC_POPUP_BEANIES_VSCREATOR2_4`: "[m:angry]Why are you looking at me like this? <br/> We had a deal!"
- `NPC_POPUP_BEANIES_VSCREATOR2_5`: "Press the damn button so we can be done with all this!"
- `NPC_POPUP_BEANIES_VSCREATOR2_6`: "[m:veryangry]..."
- `NPC_POPUP_BEANIES_VSCREATOR2_7`: "[m:angry]Do i seriously need to remind you of why you are here in the first place?"
- `NPC_POPUP_BEANIES_VSCREATOR2_8`: "[m:veryangry]PRESS THE GODDAMNED BUTTON!"
- `NPC_POPUP_BEANIES_VSCREATOR3_1`: "[m:veryangry]GGGGAAAAAHHH!"
- `NPC_POPUP_BEANIES_VSCREATOR3_2`: "[m:angry]What are you doing!? <br/> I swear to God..."
- `NPC_POPUP_BEANIES_VSCREATOR3_3`: "Don't you remember what this monster took from you as well, Magdalene?"
- `NPC_POPUP_BEANIES_VSCREATOR3_4`: "[m:veryangry]Did all that deja vu cause too much damage do your brain?"
- `NPC_POPUP_BEANIES_VSCREATOR3_5`: "[m:angry]Do you not remember who you are?!! Do you not remember your only son!?"
- `NPC_POPUP_BEANIES_VSCREATOR3_6`: "[m:veryangry]HE TOOK ISAAC! <br/> HIM!"
- `NPC_POPUP_BEANIES_VSCREATOR3_7`: "THAT THING IS THE VILLAIN OF THIS STORY!"
- `NPC_POPUP_BEANIES_VSCREATOR3_8`: "[m:sad]Listen! <br/> I could have saved Isaac! <br/> I could have saved everyone!"
- `NPC_POPUP_BEANIES_VSCREATOR3_9`: "[m:angry]But he steals the one thing that matters! The thing that makes us who we are!"
- `NPC_POPUP_BEANIES_VSCREATOR3_10`: "What kind of monster takes a child from their mother!?!"
- `NPC_POPUP_BEANIES_VSCREATOR3_11`: "[m:veryangry]NOW PRESS THE FUCKING BUTTON, MAGGIE!"
- `NPC_POPUP_BEANIES_VSCREATOR4_1`: "[m:veryangry]THIS IS NOT THE TIME TO CHICKEN OUT!"
- `NPC_POPUP_BEANIES_VSCREATOR4_2`: "THE ONLY WAY TO END THIS IS TOTAL NUCLEAR ANNIHILATION!"
- `NPC_POPUP_BEANIES_VSCREATOR4_3`: "..."
- `NPC_POPUP_BEANIES_VSCREATOR4_4`: "[m:bored]Oh fuck it, I'll activate the timer remotely..."
- `NPC_POPUP_BEANIES_VSCREATOR4_5`: "[m:angry]Just let it be known, I'm extremely disappointed in you!"
- `NPC_POPUP_BEANIES_VSCREATOR4_6`: "You can't be so selfish at a time like this!"
- `NPC_POPUP_BEANIES_VSCREATOR4_7`: "..."
- `NPC_POPUP_BEANIES_VSCREATOR4_8`: "[m:veryangry]GOODBYE CRUEL WORLD!!"

```
sequences {
	//sfx UISFX_ButchMove

	///////////////////////////
	//      FIRST FIGHT      //
	///////////////////////////

	first_fight_intro {
		delay .5
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_FIRST_FIGHT_INTRO_1
		//dialog "[m:angry]OK listen, \n I don't like you, \n [m:veryangry]I don't like no one!"
		//dialog "[m:angry]Especially some goodie goodie roaming Boon County with a few test tube kitties![/m]"
		//dialog "[m:confused][s:.5][m:questioning]Meh...[/m][/s]"
		//dialog "[m:pondering]Sooo... \nInto cats and stuff?"
		//dialog "[m:questioning]Cool \ncool..."
		dialog NPC_POPUP_FIRST_FIGHT_INTRO_2
		dialog NPC_POPUP_FIRST_FIGHT_INTRO_3
		dialog NPC_POPUP_FIRST_FIGHT_INTRO_4
		dialog NPC_POPUP_FIRST_FIGHT_INTRO_5
		sfx UISFX_ButchHint
		set_state butch_point_team
		dialog NPC_POPUP_FIRST_FIGHT_INTRO_6
		sfx UISFX_ButchHint
		set_state butch_point_enemies
		dialog NPC_POPUP_FIRST_FIGHT_INTRO_7
		dialog NPC_POPUP_FIRST_FIGHT_INTRO_8
		set_mood default
		set_state butch_right

		wait_for cat_turn

		set_state butch_point_team_nocircle
		dialog NPC_POPUP_FIRST_FIGHT_INTRO_9
		dialog NPC_POPUP_FIRST_FIGHT_INTRO_10
		
		sfx UISFX_ButchMoveHint
		set_state butch_point_attack
		dialog NPC_POPUP_FIRST_FIGHT_INTRO_11
		dialog NPC_POPUP_FIRST_FIGHT_INTRO_12

		set_state butch_point_move
		sfx UISFX_ButchHint
		dialog NPC_POPUP_FIRST_FIGHT_INTRO_13
		dialog_and_autopass NPC_POPUP_FIRST_FIGHT_INTRO_14

		unlock_controls 1
		wait_for action_selected

		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	try_again_melee_move {
		sfx UISFX_ButchMove	
		set_state butch_right
		dialog NPC_POPUP_TRY_AGAIN_MELEE_MOVE_1
		dialog NPC_POPUP_TRY_AGAIN_MELEE_MOVE_2
		sfx UISFX_ButchMove
		reset_turn both
		set_state offscreen
		clear_token try_again_melee_move
	}
	melee_move2 {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_MELEE_MOVE2_1
		sfx UISFX_ButchMoveHint
		set_state butch_point_move
		dialog_and_autopass NPC_POPUP_MELEE_MOVE2_2

		unlock_controls 1
		wait_for action_selected
		sfx UISFX_ButchMoveAway

		set_state offscreen
		clear_token melee_move2
	}

	melee_attack_rat {
		get_token ranged_cat_attack
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_MELEE_ATTACK_RAT_1
		sfx UISFX_ButchMoveHint
		set_state butch_point_attack
		dialog NPC_POPUP_MELEE_ATTACK_RAT_2
		dialog_and_autopass NPC_POPUP_MELEE_ATTACK_RAT_3

		unlock_controls 1
		wait_for action_selected
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}


	try_again_attack_rat {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_TRY_AGAIN_ATTACK_RAT_1
		dialog NPC_POPUP_TRY_AGAIN_ATTACK_RAT_2
		dialog NPC_POPUP_TRY_AGAIN_ATTACK_RAT_3
		reset_turn act
		sfx UISFX_ButchHintDelay1
		set_state butch_point_attack
		dialog_and_autopass NPC_POPUP_TRY_AGAIN_ATTACK_RAT_4
		
		unlock_controls 1
		wait_for action_selected
		sfx UISFX_ButchMoveAway
		set_state offscreen
		clear_token try_again_attack_rat
	}


	melee_killed_rat {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_MELEE_KILLED_RAT_1
		set_state butch_point_team_nocircle
		dialog NPC_POPUP_MELEE_KILLED_RAT_2
		sfx UISFX_ButchHintDelay1
		set_state butch_point_passives

		dialog_and_autopass NPC_POPUP_MELEE_KILLED_RAT_3

		unlock_mouse 1
		wait_for hovered_passive
		wait_for click

		sfx UISFX_ButchMove
		set_state butch_point_team_nocircle
		dialog NPC_POPUP_MELEE_KILLED_RAT_4
		
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	melee_out_of_actions {
		sfx UISFX_ButchHintDelay1
		set_state butch_point_spells
		dialog NPC_POPUP_MELEE_OUT_OF_ACTIONS_1
		sfx UISFX_ButchHint
		set_state butch_point_cost
		dialog NPC_POPUP_MELEE_OUT_OF_ACTIONS_2
		sfx UISFX_ButchHint
		set_state butch_point_mana
		dialog NPC_POPUP_MELEE_OUT_OF_ACTIONS_3
		sfx UISFX_ButchMoveHint
		set_state butch_point_endturn
		dialog_and_autopass NPC_POPUP_MELEE_OUT_OF_ACTIONS_4
		sfx UISFX_EndTurnShow

		unlock_controls 1
		wait_for end_turn
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	ranged_cat_intro {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_RANGED_CAT_INTRO_1

		sfx UISFX_ButchMoveHint
		set_state butch_point_attack
		dialog NPC_POPUP_RANGED_CAT_INTRO_2
		sfx UISFX_ButchHint
		set_state butch_point_move
		dialog NPC_POPUP_RANGED_CAT_INTRO_3
		dialog_and_autopass NPC_POPUP_RANGED_CAT_INTRO_4

		unlock_controls 1
		wait_for action_selected
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	ranged_cat_rolled_first {
		set_state butch_right
		dialog NPC_POPUP_RANGED_CAT_ROLLED_FIRST_1
		dialog NPC_POPUP_RANGED_CAT_ROLLED_FIRST_2
		dialog NPC_POPUP_RANGED_CAT_ROLLED_FIRST_3
		set_state butch_point_move
		dialog_and_autopass NPC_POPUP_RANGED_CAT_ROLLED_FIRST_4

		unlock_controls 1
		wait_for action_selected
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	ranged_cat_roll {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_RANGED_CAT_ROLL_1
		dialog NPC_POPUP_RANGED_CAT_ROLL_2
		sfx UISFX_ButchHintDelay2
		set_state butch_point_spells
		dialog NPC_POPUP_RANGED_CAT_ROLL_3
		sfx UISFX_ButchHint
		set_state butch_point_cost2
		dialog NPC_POPUP_RANGED_CAT_ROLL_4
		sfx UISFX_ButchHint
		set_state butch_point_mana
		dialog NPC_POPUP_RANGED_CAT_ROLL_5
		sfx UISFX_ButchHint
		set_state butch_point_spells
		dialog_and_autopass NPC_POPUP_RANGED_CAT_ROLL_6
		unlock_controls 1
		wait_for action_selected
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	ranged_cat_failmove {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_RANGED_CAT_FAILMOVE_1
		dialog NPC_POPUP_RANGED_CAT_FAILMOVE_2
		dialog NPC_POPUP_RANGED_CAT_FAILMOVE_3
		dialog NPC_POPUP_RANGED_CAT_FAILMOVE_4
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	ranged_cat_early_attack_miss {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_RANGED_CAT_EARLY_ATTACK_MISS_1
		dialog NPC_POPUP_RANGED_CAT_EARLY_ATTACK_MISS_2
		dialog NPC_POPUP_RANGED_CAT_EARLY_ATTACK_MISS_3
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}
	ranged_cat_early_attack_rat {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_RANGED_CAT_EARLY_ATTACK_RAT_1
		dialog NPC_POPUP_RANGED_CAT_EARLY_ATTACK_RAT_2
		dialog NPC_POPUP_RANGED_CAT_EARLY_ATTACK_RAT_3
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}
	ranged_cat_early_attack_ally {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_RANGED_CAT_EARLY_ATTACK_ALLY_1
		dialog NPC_POPUP_RANGED_CAT_EARLY_ATTACK_ALLY_2
		dialog NPC_POPUP_RANGED_CAT_EARLY_ATTACK_ALLY_3
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	ranged_cat_early_attack2_miss {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_MISS_1
		dialog NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_MISS_2
		dialog NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_MISS_3
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}
	ranged_cat_early_attack2_rat {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_RAT_1
		dialog NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_RAT_2
		dialog NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_RAT_3
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}
	ranged_cat_early_attack2_ally {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_ALLY_1
		dialog NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_ALLY_2
		dialog NPC_POPUP_RANGED_CAT_EARLY_ATTACK2_ALLY_3
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	ranged_cat_attack {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog_and_autopass NPC_POPUP_RANGED_CAT_ATTACK_1

		unlock_controls 1
		wait_for action_selected
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	ranged_attack_tomtom {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_RANGED_ATTACK_TOMTOM_1
		dialog NPC_POPUP_RANGED_ATTACK_TOMTOM_2
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}
	ranged_attack_tomtom_fail_miss {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_RANGED_ATTACK_TOMTOM_FAIL_MISS_1
		dialog NPC_POPUP_RANGED_ATTACK_TOMTOM_FAIL_MISS_2
		dialog NPC_POPUP_RANGED_ATTACK_TOMTOM_FAIL_MISS_3
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}
	ranged_attack_tomtom_fail_ally {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_RANGED_ATTACK_TOMTOM_FAIL_ALLY_1
		dialog NPC_POPUP_RANGED_ATTACK_TOMTOM_FAIL_ALLY_2
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}
	ranged_attack_tomtom_fail_rat {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_RANGED_ATTACK_TOMTOM_FAIL_RAT_1
		dialog NPC_POPUP_RANGED_ATTACK_TOMTOM_FAIL_RAT_2
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	melee_cat_spit {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_MELEE_CAT_SPIT_1
		sfx UISFX_ButchHint
		set_state butch_point_spells
		dialog NPC_POPUP_MELEE_CAT_SPIT_2
		dialog_and_autopass NPC_POPUP_MELEE_CAT_SPIT_3

		unlock_controls 1
		wait_for action_selected
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}
	melee_cat_spit_success {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_MELEE_CAT_SPIT_SUCCESS_1
		dialog NPC_POPUP_MELEE_CAT_SPIT_SUCCESS_2
		dialog NPC_POPUP_MELEE_CAT_SPIT_SUCCESS_3
		dialog_and_autopass NPC_POPUP_MELEE_CAT_SPIT_SUCCESS_4

		unlock_controls 1
		wait_for action_selected
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}
	melee_cat_spit_fail_miss {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_MELEE_CAT_SPIT_FAIL_MISS_1
		dialog NPC_POPUP_MELEE_CAT_SPIT_FAIL_MISS_2
		dialog NPC_POPUP_MELEE_CAT_SPIT_FAIL_MISS_3
		dialog_and_autopass NPC_POPUP_MELEE_CAT_SPIT_FAIL_MISS_4

		unlock_controls 1
		wait_for action_selected
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}
	melee_cat_spit_fail_rat {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_MELEE_CAT_SPIT_FAIL_RAT_1
		dialog NPC_POPUP_MELEE_CAT_SPIT_FAIL_RAT_2
		dialog NPC_POPUP_MELEE_CAT_SPIT_FAIL_RAT_3
		dialog_and_autopass NPC_POPUP_MELEE_CAT_SPIT_FAIL_RAT_4

		unlock_controls 1
		wait_for action_selected
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}
	melee_cat_spit_fail_ally {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_MELEE_CAT_SPIT_FAIL_ALLY_1
		dialog NPC_POPUP_MELEE_CAT_SPIT_FAIL_ALLY_2
		dialog NPC_POPUP_MELEE_CAT_SPIT_FAIL_ALLY_3
		dialog_and_autopass NPC_POPUP_MELEE_CAT_SPIT_FAIL_ALLY_4

		unlock_controls 1
		wait_for action_selected
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}
	melee_cat_spit_ignore {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_MELEE_CAT_SPIT_IGNORE_1
		dialog_and_autopass NPC_POPUP_MELEE_CAT_SPIT_IGNORE_2

		unlock_controls 1
		wait_for action_selected
		sfx UISFX_ButchMoveAway
		set_state offscreen

		clear_token melee_cat_spit_ignore
	}
	done_spitting_success {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_DONE_SPITTING_SUCCESS_1
		dialog NPC_POPUP_DONE_SPITTING_SUCCESS_2
		dialog NPC_POPUP_DONE_SPITTING_SUCCESS_3
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}
	done_spitting_fail_miss {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_DONE_SPITTING_FAIL_MISS_1
		dialog NPC_POPUP_DONE_SPITTING_FAIL_MISS_2
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}
	done_spitting_fail_rat {
		set_state butch_right
		dialog NPC_POPUP_DONE_SPITTING_FAIL_RAT_1
		dialog NPC_POPUP_DONE_SPITTING_FAIL_RAT_2
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}
	done_spitting_fail_ally {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_DONE_SPITTING_FAIL_ALLY_1
		dialog NPC_POPUP_DONE_SPITTING_FAIL_ALLY_2
		dialog NPC_POPUP_DONE_SPITTING_FAIL_ALLY_3
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	do_not_end_turn {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog_and_autopass NPC_POPUP_DO_NOT_END_TURN_1
		clear_token do_not_end_turn
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}


	tutorial_cat_dies {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_TUTORIAL_CAT_DIES_1
		dialog NPC_POPUP_TUTORIAL_CAT_DIES_2
		dialog NPC_POPUP_TUTORIAL_CAT_DIES_3
		dialog NPC_POPUP_TUTORIAL_CAT_DIES_4
		dialog NPC_POPUP_TUTORIAL_CAT_DIES_5
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	can_still_use_attack {
		get_token can_still_use_attack_didntspell
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_CAN_STILL_USE_ATTACK_1
		dialog NPC_POPUP_CAN_STILL_USE_ATTACK_2

		sfx UISFX_ButchHint
		set_state butch_point_attack
		dialog_and_autopass NPC_POPUP_CAN_STILL_USE_ATTACK_3

		unlock_controls 1
		wait_for action_selected
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}
	can_still_use_attack_didntspell {
		get_token can_still_use_attack
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_CAN_STILL_USE_ATTACK_DIDNTSPELL_1

		sfx UISFX_ButchHint
		set_state butch_point_attack
		dialog_and_autopass NPC_POPUP_CAN_STILL_USE_ATTACK_DIDNTSPELL_2

		unlock_controls 1
		wait_for action_selected
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	///////////////////////////
	//        LEVEL UP       //
	///////////////////////////

	level_up_intro {
		delay .5
		sfx UISFX_ButchMove
		set_state butch_levelup
		dialog NPC_POPUP_LEVEL_UP_INTRO_1
		dialog NPC_POPUP_LEVEL_UP_INTRO_2
		dialog NPC_POPUP_LEVEL_UP_INTRO_3
		dialog NPC_POPUP_LEVEL_UP_INTRO_4
		dialog NPC_POPUP_LEVEL_UP_INTRO_5
		sfx UISFX_ButchHint
		set_state butch_point_hotblooded
		dialog_and_autopass NPC_POPUP_LEVEL_UP_INTRO_6

		unlock_mouse 1
		wait_for hovered_passive
		wait_for click
		lock_mouse 1

		sfx UISFX_ButchHint
		set_state butch_point_sunburn
		dialog NPC_POPUP_LEVEL_UP_INTRO_7
		dialog NPC_POPUP_LEVEL_UP_INTRO_8
		set_state butch_levelup
		dialog NPC_POPUP_LEVEL_UP_INTRO_9
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	level_up_selected_sunburn {
		sfx UISFX_ButchMove
		set_state butch_left

		dialog NPC_POPUP_LEVEL_UP_SELECTED_SUNBURN_1
		dialog NPC_POPUP_LEVEL_UP_SELECTED_SUNBURN_2
		dialog NPC_POPUP_LEVEL_UP_SELECTED_SUNBURN_3
		dialog NPC_POPUP_LEVEL_UP_SELECTED_SUNBURN_4

		sfx UISFX_ButchMoveAway
		set_state offscreen
	}
	level_up_didnt_select_sunburn {
		sfx UISFX_ButchMove
		set_state butch_left

		dialog NPC_POPUP_LEVEL_UP_DIDNT_SELECT_SUNBURN_1
		dialog NPC_POPUP_LEVEL_UP_DIDNT_SELECT_SUNBURN_2
		dialog NPC_POPUP_LEVEL_UP_DIDNT_SELECT_SUNBURN_3
		dialog NPC_POPUP_LEVEL_UP_DIDNT_SELECT_SUNBURN_4
		dialog NPC_POPUP_LEVEL_UP_DIDNT_SELECT_SUNBURN_5
		dialog NPC_POPUP_LEVEL_UP_DIDNT_SELECT_SUNBURN_6
		dialog NPC_POPUP_LEVEL_UP_DIDNT_SELECT_SUNBURN_7

		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	///////////////////////////
	//       BOSS FIGHT      //
	///////////////////////////

	boss_fight_intro {
		delay .5
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_BOSS_FIGHT_INTRO_1
		dialog NPC_POPUP_BOSS_FIGHT_INTRO_2
		dialog NPC_POPUP_BOSS_FIGHT_INTRO_3

		sfx UISFX_ButchMoveAway
		set_state offscreen

		delay .25

		sfx UISFX_ButchMove
		set_state butch_right

		dialog NPC_POPUP_BOSS_FIGHT_INTRO_4
		dialog NPC_POPUP_BOSS_FIGHT_INTRO_5

		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	use_weapon {
		get_token use_attack_after_used_weapon
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_USE_WEAPON_1
		sfx UISFX_ButchHint
		set_state butch_point_weapon
		dialog NPC_POPUP_USE_WEAPON_2
		dialog_and_autopass NPC_POPUP_USE_WEAPON_3

		unlock_controls 1
		wait_for action_selected
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}
	use_attack_after_used_weapon {
		get_token use_weapon
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_USE_ATTACK_AFTER_USED_WEAPON_1
		sfx UISFX_ButchHint
		set_state butch_point_weapon
		dialog NPC_POPUP_USE_ATTACK_AFTER_USED_WEAPON_2

		sfx UISFX_ButchHint
		set_state butch_point_attack
		dialog_and_autopass NPC_POPUP_USE_ATTACK_AFTER_USED_WEAPON_3

		unlock_controls 1
		wait_for action_selected
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	boss_fight_round2 {
		sfx UISFX_ButchMove
		set_state butch_right
		dialog NPC_POPUP_BOSS_FIGHT_ROUND2_1
		sfx UISFX_ButchHint
		set_state butch_point_turnorder
		dialog NPC_POPUP_BOSS_FIGHT_ROUND2_2
		dialog NPC_POPUP_BOSS_FIGHT_ROUND2_3

		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	///////////////////////////
	//          MAP          //
	///////////////////////////

	map_click_node {
		sfx UISFX_ButchHint
		set_state butch_point_mapnode
		dialog_and_autopass NPC_POPUP_MAP_CLICK_NODE_1

		unlock_controls 1
		wait_for mapnode_selected

		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	map_equip_items {
		sfx UISFX_ButchMove
		set_state butch_left
		dialog NPC_POPUP_MAP_EQUIP_ITEMS_1
		sfx UISFX_ButchMove
		set_state butch_point_inventory
		dialog_and_autopass NPC_POPUP_MAP_EQUIP_ITEMS_2

		unlock_controls 1
		wait_for inventory_selected

		sfx UISFX_ButchMoveAway
		set_state offscreen
	}
	map_equip_items2 {
		clear_token map_equip_items2

		sfx UISFX_ButchHint
		set_state butch_point_inventory
		dialog_and_autopass NPC_POPUP_MAP_EQUIP_ITEMS2_1

		unlock_controls 1
		wait_for inventory_selected

		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	finish_adventure {
		sfx UISFX_ButchMove
		set_state butch_left
		dialog NPC_POPUP_FINISH_ADVENTURE_1
		dialog NPC_POPUP_FINISH_ADVENTURE_2
		sfx UISFX_ButchHint
		set_state butch_point_food
		dialog NPC_POPUP_FINISH_ADVENTURE_3
		dialog NPC_POPUP_FINISH_ADVENTURE_4
		sfx UISFX_ButchHint
		set_state butch_point_save
		dialog NPC_POPUP_FINISH_ADVENTURE_5
		sfx UISFX_ButchMove
		set_state butch_left
		dialog NPC_POPUP_FINISH_ADVENTURE_6

		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	///////////////////////////
	//         HOUSE         //
	///////////////////////////

	house_intro {
		delay .5
		sfx UISFX_ButchMove
		set_state tink_left
		dialog NPC_POPUP_HOUSE_INTRO_1
		dialog NPC_POPUP_HOUSE_INTRO_2
		dialog NPC_POPUP_HOUSE_INTRO_3
		dialog NPC_POPUP_HOUSE_INTRO_4
		dialog NPC_POPUP_HOUSE_INTRO_5
		dialog NPC_POPUP_HOUSE_INTRO_6
		dialog NPC_POPUP_HOUSE_INTRO_7
		//dialog "I just dropped by to give you a little birds and bees talk, because you look a bit..."
		//dialog "[m:mocking][s.8]Inexperienced[/s]"

		set_state tink_point_cats
		dialog NPC_POPUP_HOUSE_INTRO_8
		dialog NPC_POPUP_HOUSE_INTRO_9
		dialog NPC_POPUP_HOUSE_INTRO_10
		dialog_and_autopass NPC_POPUP_HOUSE_INTRO_11

		unlock_controls 1
		wait_for click

		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	house_pass_day {
		sfx UISFX_ButchMove
		set_state tink_left
		dialog NPC_POPUP_HOUSE_PASS_DAY_1
		dialog NPC_POPUP_HOUSE_PASS_DAY_2

		sfx UISFX_ButchHint
		set_state tink_point_food
		dialog NPC_POPUP_HOUSE_PASS_DAY_3

		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	take_cats_inside {
		clear_token take_cats_inside
		sfx UISFX_ButchMove
		set_state tink_left
		dialog NPC_POPUP_TAKE_CATS_INSIDE_1

		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	house_strays {
		delay .5
		sfx UISFX_ButchMove
		set_state tink_left
		dialog NPC_POPUP_HOUSE_STRAYS_1
		dialog NPC_POPUP_HOUSE_STRAYS_2
		dialog NPC_POPUP_HOUSE_STRAYS_3

		sfx UISFX_ButchHint
		set_state tink_point_strays
		request_cat_info stray
		dialog NPC_POPUP_HOUSE_STRAYS_4
		dialog_and_autopass NPC_POPUP_HOUSE_STRAYS_5

		unlock_controls 1
		wait_for click

		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	house_pass_day2 {
		sfx UISFX_ButchMove
		set_state tink_left
		dialog NPC_POPUP_HOUSE_PASS_DAY2_1
		dialog NPC_POPUP_HOUSE_PASS_DAY2_2
		dialog NPC_POPUP_HOUSE_PASS_DAY2_3
		dialog NPC_POPUP_HOUSE_PASS_DAY2_4

		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	new_adventure {
		sfx UISFX_ButchMove
		set_state tink_left
		dialog NPC_POPUP_NEW_ADVENTURE_1
		sfx UISFX_ButchHint
		set_state tink_point_box
		dialog NPC_POPUP_NEW_ADVENTURE_2

		sfx UISFX_ButchMoveAway
		set_state offscreen
	}
	low_on_food {
		sfx UISFX_ButchMove
		set_state tink_left
		dialog NPC_POPUP_LOW_ON_FOOD_1
		sfx UISFX_ButchHint
		set_state tink_point_food
		dialog NPC_POPUP_LOW_ON_FOOD_2
		sfx UISFX_ButchHint
		set_state tink_point_box
		dialog NPC_POPUP_LOW_ON_FOOD_3

		sfx UISFX_ButchMoveAway
		set_state offscreen
	}


	house_retired_cat_box {
		sfx UISFX_ButchMove
		set_state tink_left
		dialog NPC_POPUP_HOUSE_RETIRED_CAT_BOX_1

		sfx UISFX_ButchMove
		set_state offscreen
	}
	house_kitten_box {
		sfx UISFX_ButchMove
		set_state tink_left
		dialog NPC_POPUP_HOUSE_KITTEN_BOX_1
		dialog NPC_POPUP_HOUSE_KITTEN_BOX_2

		sfx UISFX_ButchMoveAway
		set_state offscreen
	}
	house_starred_box {
		sfx UISFX_ButchMove
		set_state tink_left
		dialog NPC_POPUP_HOUSE_STARRED_BOX_1
		dialog NPC_POPUP_HOUSE_STARRED_BOX_2

		sfx UISFX_ButchMoveAway
		set_state offscreen
	}


	house_pipe {
		sfx UISFX_ButchMove
		set_state frank_right
		dialog NPC_POPUP_HOUSE_PIPE_1
		dialog NPC_POPUP_HOUSE_PIPE_2
		dialog NPC_POPUP_HOUSE_PIPE_3
		dialog NPC_POPUP_HOUSE_PIPE_4
		dialog NPC_POPUP_HOUSE_PIPE_5
		dialog NPC_POPUP_HOUSE_PIPE_6
		dialog NPC_POPUP_HOUSE_PIPE_7
		dialog NPC_POPUP_HOUSE_PIPE_8
		dialog NPC_POPUP_HOUSE_PIPE_9
		dialog NPC_POPUP_HOUSE_PIPE_10
		dialog NPC_POPUP_HOUSE_PIPE_11
		dialog NPC_POPUP_HOUSE_PIPE_12
		dialog NPC_POPUP_HOUSE_PIPE_13
		dialog NPC_POPUP_HOUSE_PIPE_14
		sfx UISFX_ButchHint
		set_state frank_point_pipe
		dialog NPC_POPUP_HOUSE_PIPE_15
		dialog NPC_POPUP_HOUSE_PIPE_16
		sfx UISFX_ButchHint
		set_state frank_right
		dialog NPC_POPUP_HOUSE_PIPE_17
		dialog NPC_POPUP_HOUSE_PIPE_18 
		dialog NPC_POPUP_HOUSE_PIPE_19
		dialog NPC_POPUP_HOUSE_PIPE_20
		sfx UISFX_ButchMoveAway
		set_state offscreen
	}


	///////////////////////////
	//    MISC LATER STUFF   //
	///////////////////////////

	introduce_hard_path {
		sfx UISFX_ButchMove
		set_state butch_left
		dialog NPC_POPUP_INTRODUCE_HARD_PATH_1
		dialog NPC_POPUP_INTRODUCE_HARD_PATH_2
		dialog NPC_POPUP_INTRODUCE_HARD_PATH_3
		dialog NPC_POPUP_INTRODUCE_HARD_PATH_4
		dialog NPC_POPUP_INTRODUCE_HARD_PATH_5
		dialog NPC_POPUP_INTRODUCE_HARD_PATH_6

		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	first_house_boss_tomorrow {
		sfx UISFX_ButchMove
		set_state tink_left
		dialog NPC_POPUP_FIRST_HOUSE_BOSS_TOMORROW_1
		dialog NPC_POPUP_FIRST_HOUSE_BOSS_TOMORROW_2
		dialog NPC_POPUP_FIRST_HOUSE_BOSS_TOMORROW_3
		dialog NPC_POPUP_FIRST_HOUSE_BOSS_TOMORROW_4
		dialog NPC_POPUP_FIRST_HOUSE_BOSS_TOMORROW_5
		dialog NPC_POPUP_FIRST_HOUSE_BOSS_TOMORROW_6
		dialog NPC_POPUP_FIRST_HOUSE_BOSS_TOMORROW_7
		dialog NPC_POPUP_FIRST_HOUSE_BOSS_TOMORROW_8
		dialog NPC_POPUP_FIRST_HOUSE_BOSS_TOMORROW_9
		dialog NPC_POPUP_FIRST_HOUSE_BOSS_TOMORROW_10

		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	first_house_hint_retired {
		sfx UISFX_ButchMove
		set_state tink_left

		dialog NPC_POPUP_FIRST_HOUSE_HINT_RETIRED_1
		dialog NPC_POPUP_FIRST_HOUSE_HINT_RETIRED_2
		dialog NPC_POPUP_FIRST_HOUSE_HINT_RETIRED_3
		dialog NPC_POPUP_FIRST_HOUSE_HINT_RETIRED_4

		sfx UISFX_ButchMoveAway
		set_state offscreen
	}

	////////////////////////////
	//  JACK FURNITURE INTRO  //
	////////////////////////////

	jack_introduction {
		sfx UISFX_ButchMove
		set_state jack_right
		dialog NPC_POPUP_JACK_INTRODUCTION_1
		dialog NPC_POPUP_JACK_INTRODUCTION_2
		dialog NPC_POPUP_JACK_INTRODUCTION_3
		dialog NPC_POPUP_JACK_INTRODUCTION_4
		get_random_furniture_piece [small_trash_cans small_trash_can2]
		dialog NPC_POPUP_JACK_INTRODUCTION_5
		dialog NPC_POPUP_JACK_INTRODUCTION_6
		sfx UISFX_ButchHint
		set_state jack_point_furniture
		dialog_and_autopass NPC_POPUP_JACK_INTRODUCTION_7
		unlock_controls 1
		wait_for open_furniture
		lock_controls 1
		sfx UISFX_ButchMove
		set_state jack_right
		dialog NPC_POPUP_JACK_INTRODUCTION_8

		sfx UISFX_ButchMoveAway
		set_state offscreen
	}


	////////////////////////////
	//    STEVEN SAVE SCUM    //
	////////////////////////////

	steven_savescum_intro { //this replaces the _1 versions if its the first scum
		set_state steven_center

		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_1
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_2

		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_3
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_4

		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_5

		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_6
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_7
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_8

		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_9

		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_10

		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_11
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_12
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_13
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_14

		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_15
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_16
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_17

		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_18
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_19

		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_20
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_21
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_22
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_23
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_24

		autosave adventure
		set_state offscreen
	}


	steven_savescum_1 { //warning
		do_random_sequence [steven_savescum_1alt1 steven_savescum_1alt2 steven_savescum_1alt3]
	}
	steven_savescum_2 { //1 cat deja vu 10%
		do_random_sequence [steven_savescum_2alt1 steven_savescum_2alt2 steven_savescum_2alt3]
	}
	steven_savescum_3 { //all cats deja vu 10%
		do_random_sequence [steven_savescum_3alt1 steven_savescum_3alt2 steven_savescum_3alt3]
	}
	steven_savescum_4 { //deja vu level up (25%)
		do_random_sequence [steven_savescum_4alt1 steven_savescum_4alt2 steven_savescum_4alt3]
	}

	steven_savescum_100 { //secret
		set_state steven_center
	
		dialog NPC_POPUP_STEVEN_SAVESCUM_100_1
		dialog NPC_POPUP_STEVEN_SAVESCUM_100_2
		dialog NPC_POPUP_STEVEN_SAVESCUM_100_3

		autosave adventure
		set_state offscreen
	}
	




	//house boss
	steven_savescum_intro_houseboss { //this replaces the _1 versions if its the first scum
		set_state steven_center

		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_1
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_2
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_3
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_4
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_5
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_6
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_7
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_8
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_9
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_10
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_11
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_12
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_13
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_14
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_15
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_16
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_17
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_18
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_19
		dialog NPC_POPUP_STEVEN_SAVESCUM_INTRO_HOUSEBOSS_20

		autosave housebossprep
		set_state offscreen
	}


	steven_savescum_houseboss_1 { //warning
		set_state steven_center

		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_1_1
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_1_2
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_1_3
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_1_4
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_1_5
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_1_6
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_1_7
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_1_8
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_1_9
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_1_10

		autosave housebossprep
		set_state offscreen
	}
	steven_savescum_houseboss_2 { //all cats 10% deja vu
		set_state steven_center
	
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_2_1
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_2_2
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_2_3
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_2_4
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_2_5
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_2_6
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_2_7
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_2_8
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_2_9
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_2_10

		autosave housebossprep
		set_state offscreen
	}
	steven_savescum_houseboss_3 { //all cats deja vu 25% and onward
		set_state steven_center
	
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_1
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_2
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_3
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_4
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_5
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_6
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_7
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_8
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_9
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_10
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_11
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_12
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_13
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_14
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_15
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_16
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_17
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_18
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_3_19

		autosave housebossprep
		set_state offscreen
	}

	steven_savescum_houseboss_100 { //secret
		set_state steven_center
	
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_100_1
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_100_2
		dialog NPC_POPUP_STEVEN_SAVESCUM_HOUSEBOSS_100_3

		autosave housebossprep
		set_state offscreen
	}


	steven_savescum_1alt1 { //warning
		set_state steven_center

		dialog NPC_POPUP_STEVEN_SAVESCUM_1ALT1_1
		dialog NPC_POPUP_STEVEN_SAVESCUM_1ALT1_2
		dialog NPC_POPUP_STEVEN_SAVESCUM_1ALT1_3
		dialog NPC_POPUP_STEVEN_SAVESCUM_1ALT1_4
		dialog NPC_POPUP_STEVEN_SAVESCUM_1ALT1_5
		dialog NPC_POPUP_STEVEN_SAVESCUM_1ALT1_6
		dialog NPC_POPUP_STEVEN_SAVESCUM_1ALT1_7
		dialog NPC_POPUP_STEVEN_SAVESCUM_1ALT1_8
		dialog NPC_POPUP_STEVEN_SAVESCUM_1ALT1_9

		autosave adventure
		set_state offscreen
	}
	steven_savescum_1alt2 { //warning
		set_state steven_center

		dialog NPC_POPUP_STEVEN_SAVESCUM_1ALT2_1
		dialog NPC_POPUP_STEVEN_SAVESCUM_1ALT2_2
		dialog NPC_POPUP_STEVEN_SAVESCUM_1ALT2_3
		dialog NPC_POPUP_STEVEN_SAVESCUM_1ALT2_4
		dialog NPC_POPUP_STEVEN_SAVESCUM_1ALT2_5
		dialog NPC_POPUP_STEVEN_SAVESCUM_1ALT2_6
		dialog NPC_POPUP_STEVEN_SAVESCUM_1ALT2_7
		dialog NPC_POPUP_STEVEN_SAVESCUM_1ALT2_8
		dialog NPC_POPUP_STEVEN_SAVESCUM_1ALT2_9
		autosave adventure
		set_state offscreen
	}
	steven_savescum_1alt3 { //warning
		set_state steven_center

		dialog NPC_POPUP_STEVEN_SAVESCUM_1ALT3_1
		dialog NPC_POPUP_STEVEN_SAVESCUM_1ALT3_2
		dialog NPC_POPUP_STEVEN_SAVESCUM_1ALT3_3
		dialog NPC_POPUP_STEVEN_SAVESCUM_1ALT3_4
		dialog NPC_POPUP_STEVEN_SAVESCUM_1ALT3_5
		dialog NPC_POPUP_STEVEN_SAVESCUM_1ALT3_6
		dialog NPC_POPUP_STEVEN_SAVESCUM_1ALT3_7
		dialog NPC_POPUP_STEVEN_SAVESCUM_1ALT3_8

		autosave adventure
		set_state offscreen
	}


	steven_savescum_2alt1 { //1 cat deja vu 10%
		set_state steven_cat

		dialog NPC_POPUP_STEVEN_SAVESCUM_2ALT1_1
		dialog NPC_POPUP_STEVEN_SAVESCUM_2ALT1_2

		set_state steven_center
		dialog NPC_POPUP_STEVEN_SAVESCUM_2ALT1_3
		dialog NPC_POPUP_STEVEN_SAVESCUM_2ALT1_4
		dialog NPC_POPUP_STEVEN_SAVESCUM_2ALT1_5
		dialog NPC_POPUP_STEVEN_SAVESCUM_2ALT1_6
		dialog NPC_POPUP_STEVEN_SAVESCUM_2ALT1_7
		dialog NPC_POPUP_STEVEN_SAVESCUM_2ALT1_8

		autosave adventure
		set_state offscreen
	}
	steven_savescum_2alt2 { //1 cat deja vu 10%
		set_state steven_center
	
		dialog NPC_POPUP_STEVEN_SAVESCUM_2ALT2_1
		dialog NPC_POPUP_STEVEN_SAVESCUM_2ALT2_2

		set_state steven_cat

		dialog NPC_POPUP_STEVEN_SAVESCUM_2ALT2_3
		dialog NPC_POPUP_STEVEN_SAVESCUM_2ALT2_4
		dialog NPC_POPUP_STEVEN_SAVESCUM_2ALT2_5
		dialog NPC_POPUP_STEVEN_SAVESCUM_2ALT2_6
		dialog NPC_POPUP_STEVEN_SAVESCUM_2ALT2_7
		dialog NPC_POPUP_STEVEN_SAVESCUM_2ALT2_8

		autosave adventure
		set_state offscreen
	}
	steven_savescum_2alt3 { //1 cat deja vu 10%
		set_state steven_center
	
		dialog NPC_POPUP_STEVEN_SAVESCUM_2ALT3_1
		dialog NPC_POPUP_STEVEN_SAVESCUM_2ALT3_2
		dialog NPC_POPUP_STEVEN_SAVESCUM_2ALT3_3
		dialog NPC_POPUP_STEVEN_SAVESCUM_2ALT3_4
		dialog NPC_POPUP_STEVEN_SAVESCUM_2ALT3_5

		set_state steven_cat
		dialog NPC_POPUP_STEVEN_SAVESCUM_2ALT3_6
		dialog NPC_POPUP_STEVEN_SAVESCUM_2ALT3_7
		dialog NPC_POPUP_STEVEN_SAVESCUM_2ALT3_8
		dialog NPC_POPUP_STEVEN_SAVESCUM_2ALT3_9

		set_state steven_center
		dialog NPC_POPUP_STEVEN_SAVESCUM_2ALT3_10

		autosave adventure
		set_state offscreen
	}


	steven_savescum_3alt1 { //all cats deja vu 10%
		set_state steven_center
	
		dialog NPC_POPUP_STEVEN_SAVESCUM_3ALT1_1
		dialog NPC_POPUP_STEVEN_SAVESCUM_3ALT1_2
		dialog NPC_POPUP_STEVEN_SAVESCUM_3ALT1_3
		dialog NPC_POPUP_STEVEN_SAVESCUM_3ALT1_4
		dialog NPC_POPUP_STEVEN_SAVESCUM_3ALT1_5
		dialog NPC_POPUP_STEVEN_SAVESCUM_3ALT1_6
		dialog NPC_POPUP_STEVEN_SAVESCUM_3ALT1_7
		dialog NPC_POPUP_STEVEN_SAVESCUM_3ALT1_8

		autosave adventure
		set_state offscreen
	}
	steven_savescum_3alt2 { //all cats deja vu 10%
		set_state steven_center
	
		dialog NPC_POPUP_STEVEN_SAVESCUM_3ALT2_1
		dialog NPC_POPUP_STEVEN_SAVESCUM_3ALT2_2
		dialog NPC_POPUP_STEVEN_SAVESCUM_3ALT2_3
		dialog NPC_POPUP_STEVEN_SAVESCUM_3ALT2_4
		dialog NPC_POPUP_STEVEN_SAVESCUM_3ALT2_5
		dialog NPC_POPUP_STEVEN_SAVESCUM_3ALT2_6
		dialog NPC_POPUP_STEVEN_SAVESCUM_3ALT2_7
		dialog NPC_POPUP_STEVEN_SAVESCUM_3ALT2_8

		autosave adventure
		set_state offscreen
	}
	steven_savescum_3alt3 { //all cats deja vu 10%
		set_state steven_center
	
		dialog NPC_POPUP_STEVEN_SAVESCUM_3ALT3_1
		dialog NPC_POPUP_STEVEN_SAVESCUM_3ALT3_2
		dialog NPC_POPUP_STEVEN_SAVESCUM_3ALT3_3
		dialog NPC_POPUP_STEVEN_SAVESCUM_3ALT3_4
		dialog NPC_POPUP_STEVEN_SAVESCUM_3ALT3_5
		dialog NPC_POPUP_STEVEN_SAVESCUM_3ALT3_6
		dialog NPC_POPUP_STEVEN_SAVESCUM_3ALT3_7
		dialog NPC_POPUP_STEVEN_SAVESCUM_3ALT3_8

		autosave adventure
		set_state offscreen
	}

	steven_savescum_4alt1 { //deja vu level up (25%) steven takes over
		set_state steven_center
	
		dialog NPC_POPUP_STEVEN_SAVESCUM_4ALT1_1
		dialog NPC_POPUP_STEVEN_SAVESCUM_4ALT1_2
		dialog NPC_POPUP_STEVEN_SAVESCUM_4ALT1_3
		dialog NPC_POPUP_STEVEN_SAVESCUM_4ALT1_4

		autosave adventure
		set_state offscreen
	}
	steven_savescum_4alt2 { //deja vu level up (25%) steven takes over
		set_state steven_center
	
		dialog NPC_POPUP_STEVEN_SAVESCUM_4ALT2_1
		dialog NPC_POPUP_STEVEN_SAVESCUM_4ALT2_2
		dialog NPC_POPUP_STEVEN_SAVESCUM_4ALT2_3
		dialog NPC_POPUP_STEVEN_SAVESCUM_4ALT2_4
		dialog NPC_POPUP_STEVEN_SAVESCUM_4ALT2_5

		autosave adventure
		set_state offscreen
	}
	steven_savescum_4alt3 { //deja vu level up (25%) steven takes over
		set_state steven_center
	
		dialog NPC_POPUP_STEVEN_SAVESCUM_4ALT3_1
		dialog NPC_POPUP_STEVEN_SAVESCUM_4ALT3_2
		dialog NPC_POPUP_STEVEN_SAVESCUM_4ALT3_3
		dialog NPC_POPUP_STEVEN_SAVESCUM_4ALT3_4

		autosave adventure
		set_state offscreen
	}



	//beanies late game popups

	beanies_rift_intro { //dr beanies comments on the chaos realm!
		delay .25
		sfx UISFX_BeaniesAppear
		set_state beanies_right

		dialog NPC_POPUP_BEANIES_RIFT_INTRO_1
		dialog NPC_POPUP_BEANIES_RIFT_INTRO_2
		dialog NPC_POPUP_BEANIES_RIFT_INTRO_3
		dialog NPC_POPUP_BEANIES_RIFT_INTRO_4
		dialog NPC_POPUP_BEANIES_RIFT_INTRO_5
		dialog NPC_POPUP_BEANIES_RIFT_INTRO_6
		dialog NPC_POPUP_BEANIES_RIFT_INTRO_7
		dialog NPC_POPUP_BEANIES_RIFT_INTRO_8
		dialog NPC_POPUP_BEANIES_RIFT_INTRO_9
		dialog NPC_POPUP_BEANIES_RIFT_INTRO_10
		dialog NPC_POPUP_BEANIES_RIFT_INTRO_11

		sfx UISFX_BeaniesAway
		set_state offscreen
	}

	beanies_infinite_intro { //dr beanies unlocks the infinite and pushes you to challenge the creator.
		delay .25
		sfx UISFX_BeaniesAppear
		set_state beanies_right

		dialog NPC_POPUP_BEANIES_INFINITE_INTRO_1
		dialog NPC_POPUP_BEANIES_INFINITE_INTRO_2
		dialog NPC_POPUP_BEANIES_INFINITE_INTRO_3
		dialog NPC_POPUP_BEANIES_INFINITE_INTRO_4
		dialog NPC_POPUP_BEANIES_INFINITE_INTRO_5
		dialog NPC_POPUP_BEANIES_INFINITE_INTRO_6
		dialog NPC_POPUP_BEANIES_INFINITE_INTRO_7
		dialog NPC_POPUP_BEANIES_INFINITE_INTRO_8
		dialog NPC_POPUP_BEANIES_INFINITE_INTRO_9
		dialog NPC_POPUP_BEANIES_INFINITE_INTRO_10
		dialog NPC_POPUP_BEANIES_INFINITE_INTRO_11

		sfx UISFX_BeaniesAway
		set_state offscreen
	}

		
	beanies_vscreatorintro { //dr beanies explains how to end it all
		sfx UISFX_BeaniesAppear
		set_state beanies_right

		dialog NPC_POPUP_BEANIES_VSCREATORINTRO_1
		dialog NPC_POPUP_BEANIES_VSCREATORINTRO_2 
		dialog NPC_POPUP_BEANIES_VSCREATORINTRO_3
		dialog NPC_POPUP_BEANIES_VSCREATORINTRO_4
		dialog NPC_POPUP_BEANIES_VSCREATORINTRO_5
		dialog NPC_POPUP_BEANIES_VSCREATORINTRO_6
		dialog NPC_POPUP_BEANIES_VSCREATORINTRO_7
		dialog NPC_POPUP_BEANIES_VSCREATORINTRO_8

		sfx UISFX_BeaniesAway
		set_state offscreen
	}

	beanies_vscreator1 { //dr beanies tells you to detonate the nuke
		sfx UISFX_BeaniesAppear
		set_state beanies_right

		dialog NPC_POPUP_BEANIES_VSCREATOR1_1
		dialog NPC_POPUP_BEANIES_VSCREATOR1_2
		dialog NPC_POPUP_BEANIES_VSCREATOR1_3
		dialog NPC_POPUP_BEANIES_VSCREATOR1_4
		dialog NPC_POPUP_BEANIES_VSCREATOR1_5
		dialog NPC_POPUP_BEANIES_VSCREATOR1_6
		dialog NPC_POPUP_BEANIES_VSCREATOR1_7
		dialog NPC_POPUP_BEANIES_VSCREATOR1_8
		dialog NPC_POPUP_BEANIES_VSCREATOR1_9
		dialog NPC_POPUP_BEANIES_VSCREATOR1_10
		dialog NPC_POPUP_BEANIES_VSCREATOR1_11
		dialog NPC_POPUP_BEANIES_VSCREATOR1_12
		dialog NPC_POPUP_BEANIES_VSCREATOR1_13
		dialog NPC_POPUP_BEANIES_VSCREATOR1_14

		sfx UISFX_BeaniesAway
		set_state offscreen
	}
	
	beanies_vscreator2 { //dr beanies trys to convince you to detonate the nuke if you refuse
		sfx UISFX_BeaniesAppear
		set_state beanies_right
	
		dialog NPC_POPUP_BEANIES_VSCREATOR2_1
		dialog NPC_POPUP_BEANIES_VSCREATOR2_2
		dialog NPC_POPUP_BEANIES_VSCREATOR2_3
		dialog NPC_POPUP_BEANIES_VSCREATOR2_4
		dialog NPC_POPUP_BEANIES_VSCREATOR2_5
		dialog NPC_POPUP_BEANIES_VSCREATOR2_6
		dialog NPC_POPUP_BEANIES_VSCREATOR2_7
		dialog NPC_POPUP_BEANIES_VSCREATOR2_8

		sfx UISFX_BeaniesAway
		set_state offscreen
	}
	
	beanies_vscreator3 { //dr beanies trys angry by your choice continues to try and convince you to end it.
		sfx UISFX_BeaniesAppear
		set_state beanies_intensestatic
	
		dialog NPC_POPUP_BEANIES_VSCREATOR3_1
		dialog NPC_POPUP_BEANIES_VSCREATOR3_2
		dialog NPC_POPUP_BEANIES_VSCREATOR3_3
		dialog NPC_POPUP_BEANIES_VSCREATOR3_4
		dialog NPC_POPUP_BEANIES_VSCREATOR3_5
		dialog NPC_POPUP_BEANIES_VSCREATOR3_6
		dialog NPC_POPUP_BEANIES_VSCREATOR3_7
		dialog NPC_POPUP_BEANIES_VSCREATOR3_8
		dialog NPC_POPUP_BEANIES_VSCREATOR3_9
		dialog NPC_POPUP_BEANIES_VSCREATOR3_10
		dialog NPC_POPUP_BEANIES_VSCREATOR3_11

		sfx UISFX_BeaniesAway
		set_state offscreen
	}
	
	beanies_vscreator4 { //dr beanies sets the nuke off himself after your refusal to do so
		sfx UISFX_BeaniesAppear
		set_state beanies_intensestatic

		dialog NPC_POPUP_BEANIES_VSCREATOR4_1
		dialog NPC_POPUP_BEANIES_VSCREATOR4_2
		dialog NPC_POPUP_BEANIES_VSCREATOR4_3
		dialog NPC_POPUP_BEANIES_VSCREATOR4_4
		dialog NPC_POPUP_BEANIES_VSCREATOR4_5
		dialog NPC_POPUP_BEANIES_VSCREATOR4_6
		dialog NPC_POPUP_BEANIES_VSCREATOR4_7
		dialog NPC_POPUP_BEANIES_VSCREATOR4_8

		force_current_cat_use_ability neck_NukeBonus_remote

		sfx UISFX_BeaniesAway
		set_state offscreen
	}
}
```

---

## File: `frank_progression.gon`

### `states_and_transitions`
**Source:** `frank_progression.gon`  

```
states_and_transitions {
	states {
		idle ["idle"]
	}

	transitions {
	}
}
```

---

### `sequences`
**Source:** `frank_progression.gon`  

**Localization Strings:**
- `NPC_FRANK_UNKNOWN_1`: "You appear to have unlocked something, but I don't have dialog for it. Congrats. Also fix this."
- `NPC_FRANK_ALSO_1`: "Also..."
- `NPC_FRANK_UNPROMPTED_A_1`: "[m:questioning]Hey you aren't our mom?! <br/> Right?"
- `NPC_FRANK_UNPROMPTED_A_2`: "[m:happy]Oh, are you here for one of Frank's big tips!?"
- `NPC_FRANK_UNPROMPTED_A_3`: "[m:sad][s:.6]*cough cough*[/s]"
- `NPC_FRANK_UNPROMPTED_B_1`: "[m:happy]Holy molar! <br/> You come back to me!"
- `NPC_FRANK_UNPROMPTED_B_2`: "Frank thought of a new tip!"
- `NPC_FRANK_UNPROMPTED_C_1`: "[m:sad][s:.6]*huff huff*[/s]"
- `NPC_FRANK_UNPROMPTED_C_2`: "[m:happy]It's time for Frank tips again!"
- `NPC_FRANK_UNPROMPTED_D_1`: "[m:shocked]Uh oh, you caught us being naughty..."
- `NPC_FRANK_UNPROMPTED_D_2`: "[m:paranoid]If we give tips will you still be our friend?"
- `NPC_FRANK_UNPROMPTED_D_3`: "[m:happy]Good! <br/> Here listen to this tip!"
- `NPC_FRANK_UNPROMPTED_E_1`: "[m:sad][s:.6]*cough cough*[/s]"
- `NPC_FRANK_UNPROMPTED_E_2`: "[m:sad][s:.6]*huff huff*[/s]"
- `NPC_FRANK_UNPROMPTED_E_3`: "[m:spacedout]Sorry Frank is dying... <br/> [m:default]We better tell you those tips quick!"
- `NPC_FRANK_UNPROMPTED_F_1`: "[m:veryhappy]Mom?! <br/> [m:default]Oh it you."
- `NPC_FRANK_UNPROMPTED_F_2`: "I bet you want another Frank tip, huh?"
- `NPC_FRANK_UNPROMPTED_F_3`: "[m:happy]Well open your ear hole big cuz this tip is large!"
- `NPC_FRANK_UNPROMPTED_G_1`: "[m:happy]Hey!"
- `NPC_FRANK_UNPROMPTED_G_2`: "[m:sad][s:.6]*cough cough*[/s]"
- `NPC_FRANK_UNPROMPTED_G_3`: "[m:happy]Frank just come up with a new tips!"
- `NPC_FRANK_UNPROMPTED_H_1`: "[m:shocked]What the what!?"
- `NPC_FRANK_UNPROMPTED_H_2`: "[m:scared]We thought you were one of those mean babies!"
- `NPC_FRANK_UNPROMPTED_H_3`: "[m:mocking]We was all <br/> "WHAT THE WHAT!?""
- `NPC_FRANK_UNPROMPTED_H_4`: "[m:happy]Member that?..."
- `NPC_FRANK_UNPROMPTED_H_5`: "[m:default]Oh, <br/> you are just wanting the tips, huh?"
- `NPC_FRANK_UNPROMPTED_I_1`: "[m:spacedout]Oh hey, we didn't see you there..."
- `NPC_FRANK_UNPROMPTED_I_2`: "[m:questioning]Was that you talking to us last night?"
- `NPC_FRANK_UNPROMPTED_I_3`: "[m:default]We think we heard you telling Frank to do the bad stuff?"
- `NPC_FRANK_UNPROMPTED_I_4`: "[m:angry]Please don't do that, Frank likes being nice now."
- `NPC_FRANK_UNPROMPTED_I_5`: "[m:happy]Oh we also come up with a new tip! Listen!"
- `NPC_FRANK_FRANK_TIPS_1_1`: "[m:happy]The black part of a pencil!"
- `NPC_FRANK_FRANK_TIPS_1_2`: "[m:veryhappy]That's a good tip! <br/> People use that to draw!"
- `NPC_FRANK_FRANK_TIPS_1_3`: "[m:sad][s:.6]*cough cough*[/s]"
- `NPC_FRANK_FRANK_TIPS_1_4`: "[m:happy]That's all!"
- `NPC_FRANK_FRANK_TIPS_2_1`: "[m:questioning]Ummm, when Frank stumbles and falls on our hump?"
- `NPC_FRANK_FRANK_TIPS_2_2`: "[m:pondering]I think that ones called a tip, when we tip and fall?"
- `NPC_FRANK_FRANK_TIPS_2_3`: "[m:confused]Is that right?"
- `NPC_FRANK_FRANK_TIPS_3_1`: "[m:sad][s:.6]*huff huff*[/s]"
- `NPC_FRANK_FRANK_TIPS_3_2`: "[m:happy]When you eat inside a house and give your mommy money!"
- `NPC_FRANK_FRANK_TIPS_3_3`: "That one is called a tip also!"
- `NPC_FRANK_FRANK_TIPS_4_1`: "[m:paranoid]Stuff that pokes like injectors and stabbers?"
- `NPC_FRANK_FRANK_TIPS_4_2`: "[m:happy]Frank think those have tips too!"
- `NPC_FRANK_FRANK_TIPS_4_3`: "Hope that one helps!"
- `NPC_FRANK_FRANK_TIPS_5_1`: "[m:default]I hear mom say about Frank..."
- `NPC_FRANK_FRANK_TIPS_5_2`: "[m:happy]Frank's scabies is just the tip of the iceberg!"
- `NPC_FRANK_FRANK_TIPS_5_3`: "[m:sad]We miss her..."
- `NPC_FRANK_FRANK_TIPS_5_4`: "[m:pondering]Sometime we look at the stars and talk at her, in our brains."
- `NPC_FRANK_FRANK_TIPS_5_5`: "[m:sad]I wish she could come back..."
- `NPC_FRANK_FRANK_TIPS_6_1`: "[m:paranoid]When kids push Frank, Frank can tip over!"
- `NPC_FRANK_FRANK_TIPS_6_2`: "[m:sad][s:.6]*cough cough*[/s]"
- `NPC_FRANK_FRANK_TIPS_6_3`: "[m:happy]That's a very good one!"
- `NPC_FRANK_FRANK_TIPS_7_1`: "[m:shocked]Like when your suit tips? And it shows your bumbum to everyone?"
- `NPC_FRANK_FRANK_TIPS_7_2`: "[m:pondering]We think that's a kind of tip?"
- `NPC_FRANK_FRANK_TIPS_7_3`: "[m:questioning]Maybe?"
- `NPC_FRANK_FRANK_TIPS_8_1`: "[m:happy]My finger has a tip!"
- `NPC_FRANK_FRANK_TIPS_8_2`: "[m:veryhappy]Isn't that cool!?"
- `NPC_FRANK_FRANK_TIPS_8_3`: "[m:sad][s:.6]*huff huff*[/s]"
- `NPC_FRANK_FRANK_TIPS_9_1`: "[m:happy]Triangle shape has 2 tips!"
- `NPC_FRANK_FRANK_TIPS_9_2`: "[m:happy]Frank is a teacher now!"
- `NPC_FRANK_FRANK_TIPS_10_1`: "[m:pondering]A tip is a type of hint or something."
- `NPC_FRANK_FRANK_TIPS_10_2`: "[m:sad][s:.6]*cough cough*[/s]"
- `NPC_FRANK_FRANK_TIPS_10_3`: "[m:veryhappy]That a tip inside of a tip! <br/> What a cool thing I did!"
- `NPC_FRANK_FRANK_TIPS_10_4`: "[m:happy]See ya!"
- `NPC_FRANK_HOUSE_UPGRADE_ATTIC_1`: "[m:happy]Oh hey, Frank was just waiting for you down here."
- `NPC_FRANK_HOUSE_UPGRADE_ATTIC_2`: "Good job on sending the cat to us! <br/> He's slow, so when he runs we can still get him!"
- `NPC_FRANK_HOUSE_UPGRADE_ATTIC_3`: "[m:sad]Franks slow, but no one seems to get us..."
- `NPC_FRANK_HOUSE_UPGRADE_ATTIC_4`: "[m:sad][s:.6]*cough cough*[/s]"
- `NPC_FRANK_HOUSE_UPGRADE_ATTIC_5`: "[m:default]Frank's getting so itchy! <br/> I think we are ready to build!"
- `NPC_FRANK_HOUSE_UPGRADE_ATTIC_6`: "[m:questioning]You know that house on top of your house? <br/> The one with the point on it?"
- `NPC_FRANK_HOUSE_UPGRADE_ATTIC_7`: "[m:happy]Well Franks' gonna go building all over that one!"
- `NPC_FRANK_HOUSE_UPGRADE_ATTIC_8`: "[m:default]You just wait and see! <br/> It won't crush you or nothin'!"
- `NPC_FRANK_HOUSE_UPGRADE_ATTIC_9`: "[m:sad][s:.6]*huff huff*[/s]"
- `NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_1`: "[m:sad]Frank made babies cry... it's making Frank so sad to think of!"
- `NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_2`: "[m:scared]We was just doing our walks and a baby just jump out and scream!"
- `NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_3`: "[m:shocked]RRRRAAAAAAAAAAAAHHHHHH!!!!!"
- `NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_4`: "[m:scared]Frank fell back on our hump and couldn't get back on the feet..."
- `NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_5`: "Then the baby hit Frank... in the little brownies!"
- `NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_6`: "[m:shocked]AAAAAAHHHH! <br/>  <br/> We were saying that so loud!"
- `NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_7`: "..."
- `NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_8`: "GGGAAAAAHHHH!!"
- `NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_9`: "[m:sad][s:.6]*cough cough*[/s]"
- `NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_10`: "[m:scared]Then another baby one comes out of a bush and starts rolling Frank down the street!"
- `NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_11`: "[m:mocking]"Freaky Frank, Freaky Frank! Has no mom and smells so rank!" <br/> They was singing that!"
- `NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_12`: "[m:shocked] ABOUT US!!!"
- `NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_13`: "[m:angry]Frank was saying back "We have a mommy! She just lives in space!""
- `NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_14`: "[m:shocked]And they was laughing so hard they was crying!"
- `NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_15`: "[m:sad][s:.6]*huff huff*[/s]"
- `NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_16`: "We was feeling so bad about making the babies cry, Frank started to cry!"
- `NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_17`: "[m:scared]And it was so scary!"
- `NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_18`: "[m:sad][s:.6]*cough cough*[/s]"
- `NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_19`: "[m:default]I think we are going to add more room to your house tonight."
- `NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_20`: "[m:happy]You like us when we make the house stuff right?"
- `NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_21`: "Frank likes when you like us."
- `NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_1`: "[m:happy]You came back to talk to us!"
- `NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_2`: "[m:pondering]Frank was just wondering how long we have left in this body..."
- `NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_3`: "[m:veryhappy]We like it a lot, so many bumps and curves going over it."
- `NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_4`: "[m:happy]Even the tiny bumps are fun! Itchy fun!"
- `NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_5`: "[m:sad][s:.6]*cough cough*[/s]"
- `NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_6`: "[m:questioning]Frank sometime is wondering, when we die where will those bumps go?"
- `NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_7`: "[m:pondering]Do the bugs take the bumps and wear them like a house!?"
- `NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_8`: "[m:happy]Because that makes Frank so happy to dream about!"
- `NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_9`: "[m:default]Speaking about Frank dying, looks like it time for Frank to get to work!"
- `NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_10`: "[m:happy]This one's gonna be adding an <br/> "On Topper"."
- `NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_11`: "[m:questioning]It like a double deckers but more better maybe?"
- `NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_12`: "[m:happy]Maybe mom will see us building and make a smile!"
- `NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_13`: "[m:sad][s:.6]*huff huff*[/s]"
- `NPC_FRANK_HOUSE_UPGRADE_4THROOM_1`: "[m:shocked]OH NO OH NO!"
- `NPC_FRANK_HOUSE_UPGRADE_4THROOM_2`: "[m:scared]THIS IS THE LAST BUILDER ONER!"
- `NPC_FRANK_HOUSE_UPGRADE_4THROOM_3`: "[m:paranoid]FRANK DON'T KNOW HOW TO MAKE MORE HOUSE THAN THIS ONE!"
- `NPC_FRANK_HOUSE_UPGRADE_4THROOM_4`: "[m:scared]If we build this last thing, then Frank will die!"
- `NPC_FRANK_HOUSE_UPGRADE_4THROOM_5`: "[m:sad]And if we die, no one will talk to us again..."
- `NPC_FRANK_HOUSE_UPGRADE_4THROOM_6`: "[m:scared]AAAAAAHHHH! IM FRANKIN' OUT!"
- `NPC_FRANK_HOUSE_UPGRADE_4THROOM_7`: "[m:sad][s:.6]*cough cough*[/s]"
- `NPC_FRANK_HOUSE_UPGRADE_4THROOM_8`: "[m:paranoid]Listen to us, if we do one more house for you, will we die?"
- `NPC_FRANK_HOUSE_UPGRADE_4THROOM_9`: "[m:scared]Frank doesn't know about this one! If you stop looking at us do we go invisible?"
- `NPC_FRANK_HOUSE_UPGRADE_4THROOM_10`: "[s:.6][m:sad]*wimpering*[/s]"
- `NPC_FRANK_HOUSE_UPGRADE_4THROOM_11`: "[m:default]OK, a Frank must do what a Frank does best!"
- `NPC_FRANK_HOUSE_UPGRADE_4THROOM_12`: "[m:happy]We will do it, we will die making your house done!"
- `NPC_FRANK_HOUSE_UPGRADE_4THROOM_13`: "[m:sad][s:.6]*huff huff*[/s]"
- `NPC_FRANK_HOUSE_UPGRADE_4THROOM_14`: "[m:scared]..."
- `NPC_FRANK_HOUSE_UPGRADE_4THROOM_15`: "[m:happy]When you die will you talk to Frank again? Please?"
- `NPC_FRANK_HOUSE_UPGRADE_4THROOM_16`: "We love you!"
- `NPC_FRANK_HOUSE_UPGRADE_4THROOM_17`: "[m:veryhappy]Bye Bye."
- `NPC_FRANK_FRANK_MAX_INTRO_1`: "[m:happy]Hey we didn't die!? <br/> What the what!?"
- `NPC_FRANK_FRANK_MAX_INTRO_2`: "Holy molar! <br/> This one is a great day!"
- `NPC_FRANK_FRANK_MAX_INTRO_3`: "[m:sad][s:.6]*cough cough*[/s]"
- `NPC_FRANK_FRANK_MAX_INTRO_4`: "[m:paranoid]Oh but what does Frank gonna do for you now?"
- `NPC_FRANK_FRANK_MAX_INTRO_5`: "[m:pondering]Hmmmm... <br/> Wait I know what you need!"
- `NPC_FRANK_FRANK_MAX_INTRO_6`: "[m:veryhappy]ITCHIES!"
- `NPC_FRANK_FRANK_MAX_INTRO_7`: "[m:sad][s:.6]*huff huff*[/s]"
- `NPC_FRANK_FRANK_MAX_INTRO_8`: "[m:happy]Frank got tons of itchies! You just keep sending Frank kitties and you'll see!"
- `NPC_FRANK_FRANK_MAX1_1`: "[m:happy]Oh yay you are talking to Frank again!"
- `NPC_FRANK_FRANK_MAX1_2`: "And guess what that is meaning?"
- `NPC_FRANK_FRANK_MAX1_3`: "[m:veryhappy]It's the time for itchies!"
- `NPC_FRANK_FRANK_MAX1_4`: "[m:sad][s:.6]*cough cough*[/s]"
- `NPC_FRANK_FRANK_MAX1_5`: "[m:winking]Here, I got this one from my rumpus! <br/> Haha!"
- `NPC_FRANK_FRANK_MAX1_6`: "[m:happy]It's a bit little stinky but still the best one I gots!"
- `NPC_FRANK_FRANK_MAX1_7`: "[m:default]Be happy about it!"
- `NPC_FRANK_FRANK_MAX2_1`: "[m:happy]Guess what Frank gots!?"
- `NPC_FRANK_FRANK_MAX2_2`: "[m:veryhappy]A BIG ITCHY! <br/> JUST FOR YOU!"
- `NPC_FRANK_FRANK_MAX2_3`: "[m:sad][s:.6]*huff huff*[/s]"
- `NPC_FRANK_FRANK_MAX2_4`: "[m:default]This one likes to crawl all over and give you red lumpies!"
- `NPC_FRANK_FRANK_MAX2_5`: "[m:happy]Take it home with you!"
- `NPC_FRANK_FRANK_MAX2_6`: "Bye bye!"
- `NPC_FRANK_FRANK_MAX3_1`: "[m:shocked]Oh it you! <br/> I thought you were a baby guy..."
- `NPC_FRANK_FRANK_MAX3_2`: "[m:angry]Frank hates those babies! GRRRRR!"
- `NPC_FRANK_FRANK_MAX3_3`: "That's what Frank makes when we are mad the GRRRR sounds!"
- `NPC_FRANK_FRANK_MAX3_4`: "[m:questioning]Hey wait, don't Frank owe you an itchy?"
- `NPC_FRANK_FRANK_MAX3_5`: "[m:sad][s:.6]*cough cough*[/s]"
- `NPC_FRANK_FRANK_MAX3_6`: "[m:grossedout]We pulled this one from our throat holes!"
- `NPC_FRANK_FRANK_MAX3_7`: "[m:happy]You get it now! Yay!"
- `NPC_FRANK_FRANK_MAX4_1`: "[m:scared]Uh oh, guess what?!"
- `NPC_FRANK_FRANK_MAX4_2`: "[m:happy]Frank found another itchy!"
- `NPC_FRANK_FRANK_MAX4_3`: "[m:winking]Frank won't tell you where this itchy is from though..."
- `NPC_FRANK_FRANK_MAX4_4`: "[m:whispering][s:.5]It's from that secret spot...[/s]"
- `NPC_FRANK_FRANK_MAX4_5`: "[m:sad][s:.6]*huff huff*[/s]"
- `NPC_FRANK_FRANK_MAX4_6`: "[m:happy]That's a hint that only you and Frank can know about!"
- `NPC_FRANK_FRANK_MAX4_7`: "[m:sad][s:.6]*cough cough*[/s]"
- `NPC_FRANK_FRANK_MAX5_1`: "[m:happy]LOOK AT THIS ONE!"
- `NPC_FRANK_FRANK_MAX5_2`: "[m:veryhappy]ANOTHER ITCHY! <br/> And Frank was finding it in Frank's brown town!"
- `NPC_FRANK_FRANK_MAX5_3`: "[m:winking]Extra sticky just the way you is liking it!"
- `NPC_FRANK_FRANK_MAX5_4`: "[m:happy]Here take it! <br/> We gots lots more!"
- `NPC_FRANK_FRANK_MAX5_5`: "[m:sad][s:.6]*cough cough*[/s]"
- `NPC_FRANK_FRANK_MAX5_6`: "[m:veryhappy]Frank is loving this deal we made!"
- `NPC_FRANK_FRANK_MAX5_7`: "[m:happy]See you next times!"
- `NPC_FRANK_HOUSE_UPGRADE_BASEMENT_1`: "I will build you a basement tonight."
- `NPC_FRANK_HOUSE_UPGRADE_BASEMENT2_1`: "I will build you another basement tonight."
- `NPC_FRANK_HOUSE_UPGRADE_BASEMENT3_1`: "I will build you ANOTHER basement tonight."
- `NPC_FRANK_HOUSE_UPGRADE_BASEMENT4_1`: "I will build you YET ANOTHER basement tonight."
- `NPC_FRANK_HOUSE_UPGRADE_BASEMENT5_1`: "I will build you another basement tonight. Too many basements."
- `NPC_FRANK_FRANK_CAVES_INTRO_1`: "[m:scared]Frank is scared..."
- `NPC_FRANK_FRANK_CAVES_INTRO_2`: "[m:shocked]The Cave are a dark spooky thing... <br/> Frank was a dead guy in that place once!"
- `NPC_FRANK_FRANK_CAVES_INTRO_3`: "[m:happy]But don't worry, we got so smart and builded a new Frank out of the old one!"
- `NPC_FRANK_FRANK_CAVES_INTRO_4`: "Good as new, right? <br/> Look at how we can make this one dance!"
- `NPC_FRANK_FRANK_CAVES_INTRO_5`: "[m:spacedout]............"
- `NPC_FRANK_FRANK_CAVES_INTRO_6`: "[m:spacedout]............"
- `NPC_FRANK_FRANK_CAVES_INTRO_7`: "[m:sad][s:.6]*cough cough*[/s]"
- `NPC_FRANK_FRANK_CAVES_INTRO_8`: "[m:happy]Frank can't dance like old Frank can... but look again!"
- `NPC_FRANK_FRANK_CAVES_INTRO_9`: "[m:spacedout]............"
- `NPC_FRANK_FRANK_CAVES_INTRO_10`: "[m:spacedout]............"
- `NPC_FRANK_FRANK_CAVES_INTRO_11`: "[m:sad][s:.6]*huff huff*[/s]"
- `NPC_FRANK_FRANK_CAVES_INTRO_12`: "[m:sad][s:.6]*cough cough*[/s]"
- `NPC_FRANK_FRANK_CAVES_INTRO_13`: "[m:default]Frank needs a nap..."
- `NPC_FRANK_FRANK_TERMINATOR2_1`: "[m:shocked]Did you see there is a silver peepee man making dead stuff all over town?"
- `NPC_FRANK_FRANK_TERMINATOR2_2`: "[m:scared]Frank is thinking hes wants to make Frank be a dead body!"
- `NPC_FRANK_FRANK_TERMINATOR2_3`: "[m:angry]Someone should tell his mommy on him so she leaves him and makes him so sad and alone!"
- `NPC_FRANK_FRANK_TERMINATOR2_4`: "[m:questioning]Can you do that? <br/> Can you tell on him?"
- `NPC_FRANK_FRANK_TERMINATOR2_5`: "[m:sad][s:.6]*cough cough*[/s]"
- `NPC_FRANK_FRANK_TERMINATOR2_6`: "[m:angry]Oh I hope his mom gets so mad she leaves so far into space!"
- `NPC_FRANK_FRANK_TERMINATOR2_7`: "I bet he will roll into a cave and find some old itchy man to attach to!"
- `NPC_FRANK_FRANK_TERMINATOR2_8`: "[m:default]and I bet they will get so sad they try and build a house so high they can try to see their mommy..."
- `NPC_FRANK_FRANK_TERMINATOR2_9`: "[m:sad]But their mommy doesn't see them..."
- `NPC_FRANK_FRANK_TERMINATOR2_10`: "Maybe they are just too bad for their mommy..."
- `NPC_FRANK_FRANK_TERMINATOR2_11`: "[m:veryangry]I bet they cry so much they are always wet..."
- `NPC_FRANK_FRANK_TERMINATOR2_12`: "[m:pondering]yeah, I bet that is what happens..."
- `NPC_FRANK_FRANK_TERMINATOR2_13`: "[m:sad][s:.6]*huff huff*[/s]"
- `NPC_FRANK_FRANK_TERMINATOR2_14`: "[m:sad]..."
- `NPC_FRANK_FRANK_TERMINATOR2_15`: "[m:sad][s:.5]Mommy...[/s]"
- `NPC_FRANK_FRANK_ENDING_1`: "[m:happy]Hey mommy! Look! <br/> Look what we did!"
- `NPC_FRANK_FRANK_ENDING_2`: "[m:veryhappy]Frank founded a new body!"
- `NPC_FRANK_FRANK_ENDING_3`: "[m:happy]This one is more better than the old one too!"
- `NPC_FRANK_FRANK_ENDING_4`: "[m:mocking]So many more holes!"
- `NPC_FRANK_FRANK_ENDING_5`: "[m:sad][s:.6]*huff huff*[/s]"
- `NPC_FRANK_FRANK_ENDING_6`: "[m:shocked]Hey did you hear that? <br/> Frank called you mommy!"
- `NPC_FRANK_FRANK_ENDING_7`: "[m:scared]..."
- `NPC_FRANK_FRANK_ENDING_8`: "Uhh... umm..."
- `NPC_FRANK_FRANK_ENDING_9`: "[m:questioning]Is that OK? <br/> Can Frank call you our mommy?"
- `NPC_FRANK_FRANK_ENDING_10`: "[m:shocked]!!!"
- `NPC_FRANK_FRANK_ENDING_11`: "[m:veryhappy]Holy Molar!!"
- `NPC_FRANK_FRANK_ENDING_12`: "[m:happy]Frank gotted our wish! <br/> A mommy AND not being dead!"
- `NPC_FRANK_FRANK_ENDING_13`: "[m:veryhappy]This is the best Frankin' day of all times!"
- `NPC_FRANK_FRANK_ENDING_14`: "[m:happy]Make sure you keep visiting Frank, mommy."
- `NPC_FRANK_FRANK_ENDING_15`: "I gots tons of tips for you!"
- `NPC_FRANK_FRANK_ENDING_16`: "[m:sad][s:.6]*cough cough*[/s]"

```
sequences {

	unknown {
		dialog NPC_FRANK_UNKNOWN_1
		get npc_reward
	}

	also {
		dialog NPC_FRANK_ALSO_1
	}
	
		//frank tips

	unprompted {
		do_random_sequence [unprompted_a, unprompted_b, unprompted_c, unprompted_d, unprompted_e, unprompted_f, unprompted_g, unprompted_h, unprompted_i]
	}

	unprompted_a {
		dialog NPC_FRANK_UNPROMPTED_A_1
		dialog NPC_FRANK_UNPROMPTED_A_2
		dialog NPC_FRANK_UNPROMPTED_A_3
		do_sequence forward_to_tips	
	}
	unprompted_b {
		dialog NPC_FRANK_UNPROMPTED_B_1
		dialog NPC_FRANK_UNPROMPTED_B_2
		do_sequence forward_to_tips	
	}
	unprompted_c {
		dialog NPC_FRANK_UNPROMPTED_C_1
		dialog NPC_FRANK_UNPROMPTED_C_2
		do_sequence forward_to_tips
	}
	unprompted_d {
		dialog NPC_FRANK_UNPROMPTED_D_1
		dialog NPC_FRANK_UNPROMPTED_D_2
		dialog NPC_FRANK_UNPROMPTED_D_3
		do_sequence forward_to_tips	
	}
	unprompted_e {
		dialog NPC_FRANK_UNPROMPTED_E_1
		dialog NPC_FRANK_UNPROMPTED_E_2
		dialog NPC_FRANK_UNPROMPTED_E_3
		do_sequence forward_to_tips	
	}
	unprompted_f {
		dialog NPC_FRANK_UNPROMPTED_F_1
		dialog NPC_FRANK_UNPROMPTED_F_2
		dialog NPC_FRANK_UNPROMPTED_F_3
		do_sequence forward_to_tips	
	}
	unprompted_g {
		dialog NPC_FRANK_UNPROMPTED_G_1
		dialog NPC_FRANK_UNPROMPTED_G_2
		dialog NPC_FRANK_UNPROMPTED_G_3
		do_sequence forward_to_tips	
	}
	unprompted_h {
		dialog NPC_FRANK_UNPROMPTED_H_1
		dialog NPC_FRANK_UNPROMPTED_H_2
		dialog NPC_FRANK_UNPROMPTED_H_3
		dialog NPC_FRANK_UNPROMPTED_H_4
		dialog NPC_FRANK_UNPROMPTED_H_5
		do_sequence forward_to_tips	
	}
	unprompted_i {
		dialog NPC_FRANK_UNPROMPTED_I_1
		dialog NPC_FRANK_UNPROMPTED_I_2
		dialog NPC_FRANK_UNPROMPTED_I_3
		dialog NPC_FRANK_UNPROMPTED_I_4
		dialog NPC_FRANK_UNPROMPTED_I_5
		do_sequence forward_to_tips	
	}
	
	forward_to_tips {
		do_random_sequence [frank_tips_1, frank_tips_2, frank_tips_3, frank_tips_4,frank_tips_5 ,frank_tips_6, frank_tips_7,
		frank_tips_8, frank_tips_9, frank_tips_10]
	}

	
	frank_tips_1 {
		dialog NPC_FRANK_FRANK_TIPS_1_1
		dialog NPC_FRANK_FRANK_TIPS_1_2
		dialog NPC_FRANK_FRANK_TIPS_1_3
		dialog NPC_FRANK_FRANK_TIPS_1_4
	}
	
	frank_tips_2 {
		dialog NPC_FRANK_FRANK_TIPS_2_1
		dialog NPC_FRANK_FRANK_TIPS_2_2
		dialog NPC_FRANK_FRANK_TIPS_2_3
	}
	frank_tips_3 {
	    dialog NPC_FRANK_FRANK_TIPS_3_1
		dialog NPC_FRANK_FRANK_TIPS_3_2
		dialog NPC_FRANK_FRANK_TIPS_3_3
	}
	
	frank_tips_4 {
		dialog NPC_FRANK_FRANK_TIPS_4_1
		dialog NPC_FRANK_FRANK_TIPS_4_2
		dialog NPC_FRANK_FRANK_TIPS_4_3
	}
	frank_tips_5 {
		dialog NPC_FRANK_FRANK_TIPS_5_1
		dialog NPC_FRANK_FRANK_TIPS_5_2
		dialog NPC_FRANK_FRANK_TIPS_5_3
		dialog NPC_FRANK_FRANK_TIPS_5_4
		dialog NPC_FRANK_FRANK_TIPS_5_5
	}
	
	frank_tips_6 {
		dialog NPC_FRANK_FRANK_TIPS_6_1
		dialog NPC_FRANK_FRANK_TIPS_6_2
		dialog NPC_FRANK_FRANK_TIPS_6_3
	}
	frank_tips_7 {
		dialog NPC_FRANK_FRANK_TIPS_7_1
		dialog NPC_FRANK_FRANK_TIPS_7_2
		dialog NPC_FRANK_FRANK_TIPS_7_3
	}
	
	frank_tips_8 {
		dialog NPC_FRANK_FRANK_TIPS_8_1
		dialog NPC_FRANK_FRANK_TIPS_8_2
		dialog NPC_FRANK_FRANK_TIPS_8_3
	}
	frank_tips_9 {
		dialog NPC_FRANK_FRANK_TIPS_9_1
		dialog NPC_FRANK_FRANK_TIPS_9_2
	}
	
	frank_tips_10 {
		dialog NPC_FRANK_FRANK_TIPS_10_1
		dialog NPC_FRANK_FRANK_TIPS_10_2
		dialog NPC_FRANK_FRANK_TIPS_10_3
		dialog NPC_FRANK_FRANK_TIPS_10_4
	}

	

	house_upgrade_attic {
		dialog NPC_FRANK_HOUSE_UPGRADE_ATTIC_1
		set_state closeup
		dialog NPC_FRANK_HOUSE_UPGRADE_ATTIC_2
		dialog NPC_FRANK_HOUSE_UPGRADE_ATTIC_3
		set_state zoomedout
		dialog NPC_FRANK_HOUSE_UPGRADE_ATTIC_4
		set_state idle
		dialog NPC_FRANK_HOUSE_UPGRADE_ATTIC_5
		dialog NPC_FRANK_HOUSE_UPGRADE_ATTIC_6
		set_state closeup
		dialog NPC_FRANK_HOUSE_UPGRADE_ATTIC_7
		set_state idle
		dialog NPC_FRANK_HOUSE_UPGRADE_ATTIC_8
		set_state zoomedout
		dialog NPC_FRANK_HOUSE_UPGRADE_ATTIC_9
		get npc_reward
	}

	house_upgrade_mediumhouse {
		dialog NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_1
		dialog NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_2
		set_state verycloseup
		dialog NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_3
		set_state closeup
		dialog NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_4
		dialog NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_5
		set_state verycloseup
		dialog NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_6
		set_state closeup
		dialog NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_7
		set_state verycloseup
		dialog NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_8
		set_state zoomedout
		dialog NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_9
		set_state idle
		dialog NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_10
		dialog NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_11
		set_state closeup
		dialog NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_12
		dialog NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_13
		dialog NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_14
		set_state zoomedout
		dialog NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_15
		set_state idle
		dialog NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_16
		dialog NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_17
		set_state zoomedout
		dialog NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_18
		set_state idle
		dialog NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_19
		dialog NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_20
		dialog NPC_FRANK_HOUSE_UPGRADE_MEDIUMHOUSE_21
		get npc_reward
	}

	house_upgrade_largehouse {
		dialog NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_1
		dialog NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_2
		dialog NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_3
		dialog NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_4
		set_state zoomedout
		dialog NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_5
		set_state closeup
		dialog NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_6
		dialog NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_7
		dialog NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_8
		set_state idle
		dialog NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_9
		dialog NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_10
		dialog NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_11
		dialog NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_12
		set_state zoomedout
		dialog NPC_FRANK_HOUSE_UPGRADE_LARGEHOUSE_13
		get npc_reward
	}

	house_upgrade_4throom {
		set_state verycloseup
		dialog NPC_FRANK_HOUSE_UPGRADE_4THROOM_1
		dialog NPC_FRANK_HOUSE_UPGRADE_4THROOM_2
		set_state closeup
		dialog NPC_FRANK_HOUSE_UPGRADE_4THROOM_3
		dialog NPC_FRANK_HOUSE_UPGRADE_4THROOM_4
		dialog NPC_FRANK_HOUSE_UPGRADE_4THROOM_5
		set_state verycloseup
		dialog NPC_FRANK_HOUSE_UPGRADE_4THROOM_6
		set_state zoomedout
		dialog NPC_FRANK_HOUSE_UPGRADE_4THROOM_7
		set_state closeup
		dialog NPC_FRANK_HOUSE_UPGRADE_4THROOM_8
		dialog NPC_FRANK_HOUSE_UPGRADE_4THROOM_9
		set_state idle
		dialog NPC_FRANK_HOUSE_UPGRADE_4THROOM_10
		set_state closeup
		dialog NPC_FRANK_HOUSE_UPGRADE_4THROOM_11
		dialog NPC_FRANK_HOUSE_UPGRADE_4THROOM_12
		set_state zoomedout
		dialog NPC_FRANK_HOUSE_UPGRADE_4THROOM_13
		dialog NPC_FRANK_HOUSE_UPGRADE_4THROOM_14
		set_state closeup
		dialog NPC_FRANK_HOUSE_UPGRADE_4THROOM_15
		dialog NPC_FRANK_HOUSE_UPGRADE_4THROOM_16
		set_state idle
		dialog NPC_FRANK_HOUSE_UPGRADE_4THROOM_17
		get npc_reward
	}

	frank_max_intro {//when frank hits max favor
		dialog NPC_FRANK_FRANK_MAX_INTRO_1
		dialog NPC_FRANK_FRANK_MAX_INTRO_2
		dialog NPC_FRANK_FRANK_MAX_INTRO_3
		set_state closeup
		dialog NPC_FRANK_FRANK_MAX_INTRO_4
		dialog NPC_FRANK_FRANK_MAX_INTRO_5
		set_state verycloseup
		dialog NPC_FRANK_FRANK_MAX_INTRO_6
		set_state zoomedout
		dialog NPC_FRANK_FRANK_MAX_INTRO_7
		set_state idle
		dialog NPC_FRANK_FRANK_MAX_INTRO_8
		get npc_reward
	}

	frank_max_repeating {
		do_random_sequence [frank_max1, frank_max2, frank_max3, frank_max4, frank_max5]
	}

	frank_max1 {
		dialog NPC_FRANK_FRANK_MAX1_1
		dialog NPC_FRANK_FRANK_MAX1_2
		set_state verycloseup
		dialog NPC_FRANK_FRANK_MAX1_3
		set_state idle
		dialog NPC_FRANK_FRANK_MAX1_4
		set_state closeup
		dialog NPC_FRANK_FRANK_MAX1_5
		dialog NPC_FRANK_FRANK_MAX1_6
		dialog NPC_FRANK_FRANK_MAX1_7
		get npc_reward
	}
	
	frank_max2 {
		dialog NPC_FRANK_FRANK_MAX2_1
		set_state verycloseup
		dialog NPC_FRANK_FRANK_MAX2_2
		set_state idle
		dialog NPC_FRANK_FRANK_MAX2_3
		set_state  closeup
		dialog NPC_FRANK_FRANK_MAX2_4
		dialog NPC_FRANK_FRANK_MAX2_5
		dialog NPC_FRANK_FRANK_MAX2_6
		get npc_reward
	}
	
	frank_max3 {
		set_state verycloseup
		dialog NPC_FRANK_FRANK_MAX3_1
		set_state closeup
		dialog NPC_FRANK_FRANK_MAX3_2
		dialog NPC_FRANK_FRANK_MAX3_3
		dialog NPC_FRANK_FRANK_MAX3_4
		set_state zoomedout
		dialog NPC_FRANK_FRANK_MAX3_5
		set_state closeup
		dialog NPC_FRANK_FRANK_MAX3_6
		dialog NPC_FRANK_FRANK_MAX3_7
		get npc_reward
	}
	
	frank_max4 {
		dialog NPC_FRANK_FRANK_MAX4_1
		dialog NPC_FRANK_FRANK_MAX4_2
		dialog NPC_FRANK_FRANK_MAX4_3
		set_state verycloseup
		dialog NPC_FRANK_FRANK_MAX4_4
		set_state zoomedout
		dialog NPC_FRANK_FRANK_MAX4_5
		set_state closeup
		dialog NPC_FRANK_FRANK_MAX4_6
		dialog NPC_FRANK_FRANK_MAX4_7
		get npc_reward
	}
	
	frank_max5 {
		set_state closeup
		dialog NPC_FRANK_FRANK_MAX5_1
		set_state verycloseup
		dialog NPC_FRANK_FRANK_MAX5_2
		set_state closeup
		dialog NPC_FRANK_FRANK_MAX5_3
		dialog NPC_FRANK_FRANK_MAX5_4
		set_state zoomedout
		dialog NPC_FRANK_FRANK_MAX5_5
		set_state idle
		dialog NPC_FRANK_FRANK_MAX5_6
		dialog NPC_FRANK_FRANK_MAX5_7
		get npc_reward
	}
	

	house_upgrade_basement {
		dialog NPC_FRANK_HOUSE_UPGRADE_BASEMENT_1
		get npc_reward
	}

	house_upgrade_basement2 {
		dialog NPC_FRANK_HOUSE_UPGRADE_BASEMENT2_1
		get npc_reward
	}

	house_upgrade_basement3 {
		dialog NPC_FRANK_HOUSE_UPGRADE_BASEMENT3_1
		get npc_reward
	}

	house_upgrade_basement4 {
		dialog NPC_FRANK_HOUSE_UPGRADE_BASEMENT4_1
		get npc_reward
	}

	house_upgrade_basement5 {
		dialog NPC_FRANK_HOUSE_UPGRADE_BASEMENT5_1
		get npc_reward
	}
	
	//Frank unlock intros
	
	frank_caves_intro {
		dialog NPC_FRANK_FRANK_CAVES_INTRO_1
		set_state closeup
		dialog NPC_FRANK_FRANK_CAVES_INTRO_2
		dialog NPC_FRANK_FRANK_CAVES_INTRO_3
		dialog NPC_FRANK_FRANK_CAVES_INTRO_4
		set_state zoomedout
		dialog NPC_FRANK_FRANK_CAVES_INTRO_5
		dialog NPC_FRANK_FRANK_CAVES_INTRO_6
		dialog NPC_FRANK_FRANK_CAVES_INTRO_7
		set_state closeup
		dialog NPC_FRANK_FRANK_CAVES_INTRO_8
		set_state zoomedout
		dialog NPC_FRANK_FRANK_CAVES_INTRO_9
		dialog NPC_FRANK_FRANK_CAVES_INTRO_10
		dialog NPC_FRANK_FRANK_CAVES_INTRO_11
		dialog NPC_FRANK_FRANK_CAVES_INTRO_12
		set_state closeup
		dialog NPC_FRANK_FRANK_CAVES_INTRO_13
	}
	
	frank_terminator2 {
		set_state closeup
		dialog NPC_FRANK_FRANK_TERMINATOR2_1
		set_state verycloseup
		dialog NPC_FRANK_FRANK_TERMINATOR2_2
		set_state idle
		dialog NPC_FRANK_FRANK_TERMINATOR2_3
		dialog NPC_FRANK_FRANK_TERMINATOR2_4
		set_state zoomedout
		dialog NPC_FRANK_FRANK_TERMINATOR2_5
		set_state closeup
		dialog NPC_FRANK_FRANK_TERMINATOR2_6
		dialog NPC_FRANK_FRANK_TERMINATOR2_7
		dialog NPC_FRANK_FRANK_TERMINATOR2_8
		set_state idle
		dialog NPC_FRANK_FRANK_TERMINATOR2_9
		dialog NPC_FRANK_FRANK_TERMINATOR2_10
		set_state closeup
		dialog NPC_FRANK_FRANK_TERMINATOR2_11
		dialog NPC_FRANK_FRANK_TERMINATOR2_12
		set_state zoomedout
		dialog NPC_FRANK_FRANK_TERMINATOR2_13
		dialog NPC_FRANK_FRANK_TERMINATOR2_14
		dialog NPC_FRANK_FRANK_TERMINATOR2_15
	}

	frank_ending { //after the nuke final ending frank says this as his new intro
		set_state closeup
		dialog NPC_FRANK_FRANK_ENDING_1
		dialog NPC_FRANK_FRANK_ENDING_2
		dialog NPC_FRANK_FRANK_ENDING_3
		dialog NPC_FRANK_FRANK_ENDING_4
		set_state idle
		dialog NPC_FRANK_FRANK_ENDING_5
		set_state closeup
		dialog NPC_FRANK_FRANK_ENDING_6
		set_state idle
		dialog NPC_FRANK_FRANK_ENDING_7
		set_state zoomedout
		dialog NPC_FRANK_FRANK_ENDING_8
		dialog NPC_FRANK_FRANK_ENDING_9
		set_state verycloseup
		dialog NPC_FRANK_FRANK_ENDING_10
		dialog NPC_FRANK_FRANK_ENDING_11
		set_state closeup
		dialog NPC_FRANK_FRANK_ENDING_12
		dialog NPC_FRANK_FRANK_ENDING_13
		dialog NPC_FRANK_FRANK_ENDING_14
		dialog NPC_FRANK_FRANK_ENDING_15
		set_state idle
		dialog NPC_FRANK_FRANK_ENDING_16
	}
	
}
```

---

## File: `jack_progression.gon`

### `states_and_transitions`
**Source:** `jack_progression.gon`  

```
states_and_transitions {
	states {
		idle ["idle" "blocking"]
	}

	transitions {
	}
}
```

---

### `sequences`
**Source:** `jack_progression.gon`  

**Localization Strings:**
- `NPC_JACK_UNPROMPTED_1`: "Hey! You like stuff?"
- `NPC_JACK_ALSO_1`: "Also..."
- `NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_1`: "[m:happy]Oh hey, it's you! <br/> I was just telling my Nona about you!"
- `NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_2`: "[m:default]She thinks you're nice, and I think she's right!"
- `NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_3`: "[m:scared]So umm..."
- `NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_4`: "The other day I done a kick so hard it made all of Nona's treasures fall down!"
- `NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_5`: "[m:sad]Shes been stuck back there for like tons of days now..."
- `NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_6`: "[m:happy]But I'm workin' on getting her out!"
- `NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_7`: "[m:default]I bet if I can sell all the stuff that falled on her I could save her!"
- `NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_8`: "[m:happy]And buy a rocket to the moon!"
- `NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_9`: "[m:veryhappy]Or even a truck to the park!"
- `NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_10`: "[m:default]So I need your help! <br/> Buy my treasures and help me save Nona!"
- `NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_11`: "[m:spacedout]..."
- `NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_12`: "[m:shocked]Oh, wait! <br/> I almost forgot!"
- `NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_13`: "[m:questioning]Can you please send me cats that are all broked up?"
- `NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_14`: "[m:pondering]Smashed heads, Breaky bones... <br/> I need cats like that."
- `NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_15`: "[m:happy]I'll tell you why later, it's a secret I just made up!"
- `NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_16`: "[m:default]See ya!"
- `NPC_JACK_OUT_OF_STOCK_1`: "Oh, I don't got nothing. Come back Sunday."
- `NPC_JACK_PURCHASE_ITEM_1`: "[m:happy]Oh cool, money!"
- `NPC_JACK_CANT_AFFORD_1`: "[m:questioning]Uhhh, I think you are too poor for that right now..."
- `NPC_JACK_SHOP_TOOLTIP`: "{name}. <br/> {desc}"
- `NPC_JACK_JACK_SHOPUPGRADE1_1`: "[m:happy]Oh hey!"
- `NPC_JACK_JACK_SHOPUPGRADE1_2`: "[m:questioning]My Nona says you are super rich! <br/> Is that true?"
- `NPC_JACK_JACK_SHOPUPGRADE1_3`: "[m:happy]I bet you could buy all her treasures in no time!"
- `NPC_JACK_JACK_SHOPUPGRADE1_4`: "[m:questioning]So, you wanna know that secret I made up?"
- `NPC_JACK_JACK_SHOPUPGRADE1_5`: "[m:default]Ya know that thing where when you break all your bones?"
- `NPC_JACK_JACK_SHOPUPGRADE1_6`: "[m:pondering]Then they grow back all huge and strong like a daddy guy?"
- `NPC_JACK_JACK_SHOPUPGRADE1_7`: "[m:happy]Well that's what I'm doing to those cats you'd send me!"
- `NPC_JACK_JACK_SHOPUPGRADE1_8`: "[m:default]And guess what?!"
- `NPC_JACK_JACK_SHOPUPGRADE1_9`: "[m:veryhappy]I'm doing it to me too!"
- `NPC_JACK_JACK_SHOPUPGRADE1_10`: "[m:mocking]When my eye grows back in I betcha I'm gonna see through walls!"
- `NPC_JACK_JACK_SHOPUPGRADE1_11`: "[m:happy]Send me more of those broken kitties!"
- `NPC_JACK_JACK_SHOPUPGRADE1_12`: "[m:default]The more I have, the more treasures I can put out for you!"
- `NPC_JACK_JACK_SHOPUPGRADE1_13`: "[m:questioning]Deal?"
- `NPC_JACK_JACK_SHOPUPGRADE2_1`: "[m:angry]Aw dang it... <br/> UGH!"
- `NPC_JACK_JACK_SHOPUPGRADE2_2`: "[m:default]I know I look so strong with these monster muscles..."
- `NPC_JACK_JACK_SHOPUPGRADE2_3`: "[m:sad]But with all my smashed up bones and cuts, it hurts to move them boxes around!"
- `NPC_JACK_JACK_SHOPUPGRADE2_4`: "[m:pondering]I'm thinking I need more of those meowers.  They can help me move stuff faster!"
- `NPC_JACK_JACK_SHOPUPGRADE2_5`: "[m:happy]Yeah, I bet if I had a whole army of those guys I could save my Nona so fast, fires would happen!"
- `NPC_JACK_JACK_SHOPUPGRADE2_6`: "[m:shocked]?!?"
- `NPC_JACK_JACK_SHOPUPGRADE2_7`: "[m:angry]NO NONA!"
- `NPC_JACK_JACK_SHOPUPGRADE2_8`: "[m:veryangry]WE DON'T PLAY WITH FIRE ANYMORE! <br/>  <br/> GO BACK TO SLEEP!"
- `NPC_JACK_JACK_SHOPUPGRADE2_9`: "[m:default]Haha, my Nona is so silly!"
- `NPC_JACK_JACK_SHOPUPGRADE3_1`: "[m:veryangry]NO NONA! <br/> I'M NOT DOING THAT! <br/> STOP YELLING!"
- `NPC_JACK_JACK_SHOPUPGRADE3_2`: "[m:default]Heh, Nona's being silly... <br/> I don't do that stuff anymore."
- `NPC_JACK_JACK_SHOPUPGRADE3_3`: "[m:questioning]Say... <br/> Can I ask you a favor?"
- `NPC_JACK_JACK_SHOPUPGRADE3_4`: "If you hear my Nona yelling can you just plug your ears?"
- `NPC_JACK_JACK_SHOPUPGRADE3_5`: "[m:angry]She can be a big liar sometimes and it makes it really hard to save her..."
- `NPC_JACK_JACK_SHOPUPGRADE3_6`: "[m:happy]Don't worry though, I'm still kicking the walls and pulling her arms!"
- `NPC_JACK_JACK_SHOPUPGRADE3_7`: "[m:default]We are gonna get her out! I just need more Kitcats!"
- `NPC_JACK_JACK_SHOPUPGRADE3_8`: "[m:angry]And for her to [m:veryangry] <br/> STOP YELLING!!!!"
- `NPC_JACK_JACK_SHOPUPGRADE3_9`: "[m:default]Heh, Nona you so crazy!"
- `NPC_JACK_JACK_SHOPUPGRADE3_10`: "[m:happy]LOL"
- `NPC_JACK_JACK_SHOPUPGRADE4_1`: "[m:veryhappy]Oh hey! Guess what? <br/> We saved Nona!"
- `NPC_JACK_JACK_SHOPUPGRADE4_2`: "[m:winking]Just kidding! <br/> Even with all those fluffers you sent me... <br/> Nona's still back there."
- `NPC_JACK_JACK_SHOPUPGRADE4_3`: "[m:sad]Don't be sad though, 'cuz sad kids get something to be sad about!"
- `NPC_JACK_JACK_SHOPUPGRADE4_4`: "[m:questioning]I think you just need to keep buying things and then maybe something will happen?"
- `NPC_JACK_JACK_SHOPUPGRADE4_5`: "[m:shocked]OH! <br/> I almost forgetted! <br/> I found a pipe! <br/> But this one is different!"
- `NPC_JACK_JACK_SHOPUPGRADE4_6`: "[m:scared]I throwed some cans down inside it and I was hearing people in there!"
- `NPC_JACK_JACK_SHOPUPGRADE4_7`: "[m:pondering]Pretty sure it goes down into the bunker place! What the heck right?"
- `NPC_JACK_JACK_SHOPUPGRADE4_8`: "[m:happy]That's my new mystery to solve!"
- `NPC_JACK_JACK_SHOPUPGRADE4_9`: "[m:default]Nona is old news, and I don't even know how to read the newspaper!"
- `NPC_JACK_JACK_SHOPUPGRADE4_10`: "[m:winking]This pipe mystery is just what this hero needs!"
- `NPC_JACK_JACK_SHOPUPGRADE4_11`: "[m:happy]Anyway, keep sending me kitties and I'll give you goodies!"
- `NPC_JACK_JACK_SHOPUPGRADE4_12`: "Now I think I gonna poop in the pipe again!"
- `NPC_JACK_JACK_SHOPUPGRADE4_13`: "[m:shocked]!"
- `NPC_JACK_JACK_SHOPUPGRADE4_14`: "[m:angry]NO NONA! I SAID PIPE!"
- `NPC_JACK_JACK_SHOPUPGRADE4_15`: "[m:veryangry]PIPE! NO! THE NEW PIPE! STOP YELLING!"
- `NPC_JACK_JACK_SHOPUPGRADE4_16`: "[m:bored]I wonder if Nona will fit in that pipe..."
- `NPC_JACK_JACK_MAX_INTRO_1`: "[m:scared]So uh, <br/> I don't have any more space for new treasures up here..."
- `NPC_JACK_JACK_MAX_INTRO_2`: "[m:shocked]There are like 81 hundred things up here now! It's crazy!"
- `NPC_JACK_JACK_MAX_INTRO_3`: "[m:paranoid]..."
- `NPC_JACK_JACK_MAX_INTRO_4`: "[m:shocked]WHAT NONA!? <br/> FOR REALS!?"
- `NPC_JACK_JACK_MAX_INTRO_5`: "[m:happy]Oh wow, Nona says something special might happen if you keep sending me those bent fluffies!"
- `NPC_JACK_JACK_MAX_INTRO_6`: "[m:pondering]I wonder what she means... hmmm."
- `NPC_JACK_JACK_MAX_INTRO_7`: "[m:winking]So uh, keep sendin' them to me and I guess we will solve this Nona mystery together!"
- `NPC_JACK_JACK_MAX1_1`: "[m:shocked]GUESS WHAT! <br/> I think I saw the Nona Cat!"
- `NPC_JACK_JACK_MAX1_2`: "[m:veryhappy]He was floating around the room last night! I wonder if he touched something!"
- `NPC_JACK_JACK_MAX1_3`: "[m:happy]We'll stay on the lookout.  Maybe you'll see something he touched in the shop soon!"
- `NPC_JACK_JACK_MAX2_1`: "[m:happy]All these kitties you are sending is making the Nona Cat happy!"
- `NPC_JACK_JACK_MAX2_2`: "[m:veryhappy]It's crazy for real! <br/> I saw him in his little tux.  I swear it touched some treasures!"
- `NPC_JACK_JACK_MAX2_3`: "[m:winking]Keep your eyes open wide! There has gotta be some more special treasures coming to the shop soon!"
- `NPC_JACK_JACK_MAX3_1`: "[m:shocked]Look behind you quick! It's the Nona Cat!"
- `NPC_JACK_JACK_MAX3_2`: "[m:veryhappy]HAHAHA! <br/> I spooked you good!"
- `NPC_JACK_JACK_MAX3_3`: "[m:happy]I spooked Nona once so bad. She just went to sleep, she was so scared!"
- `NPC_JACK_JACK_MAX3_4`: "[m:veryhappy]I'm a spooky hero!"
- `NPC_JACK_JACK_MAX3_5`: "[m:winking]Also, I think there is even more special treasures coming soon!"
- `NPC_JACK_JACK_MAX4_1`: "[m:shocked]OMG dude! <br/> The Nona Cat was by my bed box last night!"
- `NPC_JACK_JACK_MAX4_2`: "[m:mocking]He thought I was named Isaac! Isn't that so funny? I'm Jack, duh!"
- `NPC_JACK_JACK_MAX4_3`: "[m:happy]Then he went meowing around the room touching stuff!"
- `NPC_JACK_JACK_MAX4_4`: "[m:winking]Be on the lookout for his paw prints!"
- `NPC_JACK_JACK_MAX5_1`: "[m:happy]So me and the Nona cat are friends now!"
- `NPC_JACK_JACK_MAX5_2`: "[m:paranoid]But when I try and pet him my hand just goes through! <br/> Just like the real Nona!"
- `NPC_JACK_JACK_MAX5_3`: "[m:pondering]I'm thinking they are friends maybe? I dunno... but Jack is on the case again!"
- `NPC_JACK_JACK_MAX5_4`: "[m:winking]Makin' friends and solving crimes! What can't this boy do!? Ha!"
- `NPC_JACK_UNKNOWN_1`: "You appear to have unlocked something, but I don't have dialog for it. Congrats. Also fix this."
- `NPC_JACK_JACK_DESERT_INTRO_1`: "[m:happy]You are gonna go to the desert!? Wowza! The desert is the baddest!"
- `NPC_JACK_JACK_DESERT_INTRO_2`: "[m:veryhappy]Snakes, scorpions and soooo many bones!"
- `NPC_JACK_JACK_DESERT_INTRO_3`: "[m:shocked]Just be careful, deserts are H.O.T. HOT!"
- `NPC_JACK_JACK_DESERT_INTRO_4`: "[m:winking]Nona says to <br/> "Stay hydrated!" <br/> And Nona knows stuff!"
- `NPC_JACK_JACK_DESERT_INTRO_5`: "[m:whispering][s:.7]Cus' she's so old![/s] <br/> Hehe..."
- `NPC_JACK_JACK_DESERT_INTRO_6`: "[m:veryangry]No, Nona! <br/> We are talking about that other old thing!"
- `NPC_JACK_JACK_DESERT_INTRO_7`: "[m:default]But for reals, if you want to heal in the desert, drink water."
- `NPC_JACK_JACK_DESERT_INTRO_8`: "[m:happy]Or at least get wet!"
- `NPC_JACK_JACK_DESERT_INTRO_9`: "[m:winking]Sometimes I wet my pants just to cool off when I'm sleeping!"
- `NPC_JACK_JACK_DESERT_INTRO_10`: "[m:happy]It's called a water bed for a reason, silly!"
- `NPC_JACK_JACK_DESERT_INTRO_11`: "[m:default]Bring me back a snake! <br/> If you do, I'll name him BloodVipe!"
- `NPC_JACK_JACK_DESERT_INTRO_12`: "[m:questioning]Pretty rad name, huh?"
- `NPC_JACK_JACK_ZARA_1`: "[m:angry]That dumb rock turtle from space just knocked over more treasures!"
- `NPC_JACK_JACK_ZARA_2`: "[m:scared]Nona has been screaming all day! She's even more stuck now!"
- `NPC_JACK_JACK_ZARA_3`: "[m:veryangry]I'M WORKING ON IT NONA!"
- `NPC_JACK_JACK_ZARA_4`: "[m:questioning]Gosh, <br/> does a hero's work ever end?"
- `NPC_JACK_JACK_ZARA_5`: "[m:default]Listen, I'd punch that thing if I had time but I gotta stay in the shop!"
- `NPC_JACK_JACK_ZARA_6`: "[m:questioning]Can you please get that thing in a sleeper hold for me?"
- `NPC_JACK_JACK_ZARA_7`: "[m:happy]Really twist his arm when you do it too!"
- `NPC_JACK_JACK_ZARA_8`: "[m:angry]Who does she think she is, punching walls? <br/> My daddy?!"
- `NPC_JACK_JACK_ZARA_9`: "[m:veryangry]Well she's not my daddy because my daddy is gone, and hes not a girl!"
- `NPC_JACK_JACK_ZARA_10`: "[m:angry]Stupid rock thing..."
- `NPC_JACK_JACK_GAINALTFURNITURE_1`: "[m:shocked]O M G!"
- `NPC_JACK_JACK_GAINALTFURNITURE_2`: "[m:scared]I heard you got a treasure that was touched by the... <br/> NONA CAT!"
- `NPC_JACK_JACK_GAINALTFURNITURE_3`: "[m:shocked]Look! look at it close. You can see the paw print of the Nona Cat!"
- `NPC_JACK_JACK_GAINALTFURNITURE_4`: "[m:veryhappy]This is so rare you don't even know! Gotta be worth like 10 hundred cans!"
- `NPC_JACK_JACK_GAINALTFURNITURE_5`: "[m:happy]Good work finding that! Seriously, I only seen like 7 of those things in like ever!"
- `NPC_JACK_JACK_GAINALTFURNITURE_6`: "[m:pondering]I wonder if I still have some in here..."
- `NPC_JACK_JACK_GAINALTFURNITURE_7`: "[m:winking]Anyway these things are <br/> [a:shake]" Foil-alt-ultra-mythic-rare!"[/a] <br/> And they have like double the effects!"
- `NPC_JACK_JACK_GAINALTFURNITURE_8`: "[m:happy]Go find more! <br/> You'll look so cool!"

```
sequences {
	
	unprompted {
		cancelable true
		dialog_and_autopass NPC_JACK_UNPROMPTED_1
		wait_for_cancel 1
	}

	also {
		dialog NPC_JACK_ALSO_1
	}

	jack_begin_accepting_cats { //jacks introduction is in combat_tutorial since he needs to pop up over the house
		lock_controls 1
		dialog NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_1
		dialog NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_2
		set_state closeup
		dialog NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_3
		dialog NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_4
		dialog NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_5
		dialog NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_6
		set_state blocking
		dialog NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_7
		dialog NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_8
		dialog NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_9
		dialog NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_10
		set_state zoomedout
		dialog NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_11
		set_state blocking
		dialog NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_12
		dialog NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_13
		dialog NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_14
		dialog NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_15
		dialog NPC_JACK_JACK_BEGIN_ACCEPTING_CATS_16
		begin_accepting_cats jack
		set_state idle
		unlock_controls 1
	}

	out_of_stock {
		set_state blocking
		dialog NPC_JACK_OUT_OF_STOCK_1
	}
	purchase_item {
		cancelable true
		dialog_and_autopass NPC_JACK_PURCHASE_ITEM_1
		wait_for_cancel 1
	}
	cant_afford {
		cancelable true
		dialog_and_autopass NPC_JACK_CANT_AFFORD_1
		wait_for_cancel 1
	}

	tooltip {
		cancelable true
		tooltip_dialog NPC_JACK_SHOP_TOOLTIP
		wait_for_cancel 1
	}
	hide_text {
		cancelable true
		dialog_and_autopass ""
	}

	//UNLOCKS
	jack_shopupgrade1 {
		lock_controls 1
		set_state blocking
		dialog NPC_JACK_JACK_SHOPUPGRADE1_1
		dialog NPC_JACK_JACK_SHOPUPGRADE1_2
		dialog NPC_JACK_JACK_SHOPUPGRADE1_3
		dialog NPC_JACK_JACK_SHOPUPGRADE1_4
		dialog NPC_JACK_JACK_SHOPUPGRADE1_5
		dialog NPC_JACK_JACK_SHOPUPGRADE1_6
		dialog NPC_JACK_JACK_SHOPUPGRADE1_7
		dialog NPC_JACK_JACK_SHOPUPGRADE1_8
		set_state closeup
		dialog NPC_JACK_JACK_SHOPUPGRADE1_9
		set_state blocking
		dialog NPC_JACK_JACK_SHOPUPGRADE1_10
		dialog NPC_JACK_JACK_SHOPUPGRADE1_11
		dialog NPC_JACK_JACK_SHOPUPGRADE1_12
		dialog NPC_JACK_JACK_SHOPUPGRADE1_13
		get npc_reward
		set_state idle
		unlock_controls 1
	}
	jack_shopupgrade2 {
		lock_controls 1
		set_state blocking
		set_state closeup
		dialog NPC_JACK_JACK_SHOPUPGRADE2_1
		set_state blocking
		dialog NPC_JACK_JACK_SHOPUPGRADE2_2
		dialog NPC_JACK_JACK_SHOPUPGRADE2_3
		dialog NPC_JACK_JACK_SHOPUPGRADE2_4
		dialog NPC_JACK_JACK_SHOPUPGRADE2_5
		set_state zoomedout
		dialog NPC_JACK_JACK_SHOPUPGRADE2_6
		set_state verycloseup
		dialog NPC_JACK_JACK_SHOPUPGRADE2_7
		dialog NPC_JACK_JACK_SHOPUPGRADE2_8
		set_state blocking
		dialog NPC_JACK_JACK_SHOPUPGRADE2_9
		get npc_reward
		set_state idle
		unlock_controls 1
	}
	jack_shopupgrade3 {
		lock_controls 1
		set_state blocking
		set_state closeup
		dialog NPC_JACK_JACK_SHOPUPGRADE3_1
		set_state blocking
		dialog NPC_JACK_JACK_SHOPUPGRADE3_2
		dialog NPC_JACK_JACK_SHOPUPGRADE3_3
		dialog NPC_JACK_JACK_SHOPUPGRADE3_4
		dialog NPC_JACK_JACK_SHOPUPGRADE3_5
		dialog NPC_JACK_JACK_SHOPUPGRADE3_6
		dialog NPC_JACK_JACK_SHOPUPGRADE3_7
		set_state closeup
		dialog NPC_JACK_JACK_SHOPUPGRADE3_8
		set_state blocking
		dialog NPC_JACK_JACK_SHOPUPGRADE3_9
		dialog NPC_JACK_JACK_SHOPUPGRADE3_10
		get npc_reward
		set_state idle
		unlock_controls 1
	}
	jack_shopupgrade4 {
		lock_controls 1
		set_state blocking
		set_state verycloseup
		dialog NPC_JACK_JACK_SHOPUPGRADE4_1
		set_state blocking
		dialog NPC_JACK_JACK_SHOPUPGRADE4_2
		dialog NPC_JACK_JACK_SHOPUPGRADE4_3
		dialog NPC_JACK_JACK_SHOPUPGRADE4_4
		dialog NPC_JACK_JACK_SHOPUPGRADE4_5
		dialog NPC_JACK_JACK_SHOPUPGRADE4_6
		dialog NPC_JACK_JACK_SHOPUPGRADE4_7
		dialog NPC_JACK_JACK_SHOPUPGRADE4_8
		dialog NPC_JACK_JACK_SHOPUPGRADE4_9
		set_state closeup
		dialog NPC_JACK_JACK_SHOPUPGRADE4_10
		set_state blocking
		dialog NPC_JACK_JACK_SHOPUPGRADE4_11
	    dialog NPC_JACK_JACK_SHOPUPGRADE4_12
		dialog NPC_JACK_JACK_SHOPUPGRADE4_13
		set_state verycloseupcloseup
		dialog NPC_JACK_JACK_SHOPUPGRADE4_14
		dialog NPC_JACK_JACK_SHOPUPGRADE4_15
		set_state closeup
		dialog NPC_JACK_JACK_SHOPUPGRADE4_16
		get npc_reward
		set_state idle
		unlock_controls 1
	}
	
	jack_max_intro {//when jack gains max favor
		lock_controls 1
		set_state blocking
		dialog NPC_JACK_JACK_MAX_INTRO_1
		dialog NPC_JACK_JACK_MAX_INTRO_2
		dialog NPC_JACK_JACK_MAX_INTRO_3
		set_state closeup
		dialog NPC_JACK_JACK_MAX_INTRO_4
		set_state blocking
		dialog NPC_JACK_JACK_MAX_INTRO_5
		dialog NPC_JACK_JACK_MAX_INTRO_6
		dialog NPC_JACK_JACK_MAX_INTRO_7
		get npc_reward
		set_state idle
		unlock_controls 1
	}

	jack_max_repeating {
		do_random_sequence [jack_max1, jack_max2, jack_max3, jack_max4, jack_max5]
	}
	
	jack_max1 {//max1-5 is for when jack is at max favor
		lock_controls 1
		set_state blocking
		set_state verycloseup
		dialog NPC_JACK_JACK_MAX1_1
		set_state closeup
		dialog NPC_JACK_JACK_MAX1_2
		dialog NPC_JACK_JACK_MAX1_3
		get npc_reward
		set_state idle
		unlock_controls 1
	}
	
	jack_max2 {
		lock_controls 1
		set_state blocking
		dialog NPC_JACK_JACK_MAX2_1
		dialog NPC_JACK_JACK_MAX2_2
		dialog NPC_JACK_JACK_MAX2_3
		get npc_reward
		set_state idle
		unlock_controls 1
	}

	jack_max3 {
		lock_controls 1
		set_state blocking
		set_state verycloseup
		dialog NPC_JACK_JACK_MAX3_1
		set_state closeup
		dialog NPC_JACK_JACK_MAX3_2
		set_state blocking
		dialog NPC_JACK_JACK_MAX3_3
		dialog NPC_JACK_JACK_MAX3_4
		dialog NPC_JACK_JACK_MAX3_5
		get npc_reward
		set_state idle
		unlock_controls 1
	}

	jack_max4 {
		lock_controls 1
		set_state blocking
		set_state closeup
		dialog NPC_JACK_JACK_MAX4_1
		set_state blocking
		dialog NPC_JACK_JACK_MAX4_2
		dialog NPC_JACK_JACK_MAX4_3
		dialog NPC_JACK_JACK_MAX4_4
		get npc_reward
		set_state idle
		unlock_controls 1
	}
	
	jack_max5 {
		lock_controls 1
		set_state blocking
		dialog NPC_JACK_JACK_MAX5_1
		dialog NPC_JACK_JACK_MAX5_2
		dialog NPC_JACK_JACK_MAX5_3
		dialog NPC_JACK_JACK_MAX5_4
		get npc_reward
		set_state idle
		unlock_controls 1
	}



	unknown {
		lock_controls 1
		set_state blocking
		dialog NPC_JACK_UNKNOWN_1
		get npc_reward
		set_state idle
		unlock_controls 1
	}
	
//Jack unlock intros
	
	jack_desert_intro {
		lock_controls 1
		set_state blocking

		dialog NPC_JACK_JACK_DESERT_INTRO_1
		dialog NPC_JACK_JACK_DESERT_INTRO_2
		dialog NPC_JACK_JACK_DESERT_INTRO_3
		dialog NPC_JACK_JACK_DESERT_INTRO_4
		set_state closeup
		dialog NPC_JACK_JACK_DESERT_INTRO_5
		set_state verycloseup
		dialog NPC_JACK_JACK_DESERT_INTRO_6
		set_state blocking
		dialog NPC_JACK_JACK_DESERT_INTRO_7
		dialog NPC_JACK_JACK_DESERT_INTRO_8
		dialog NPC_JACK_JACK_DESERT_INTRO_9
		dialog NPC_JACK_JACK_DESERT_INTRO_10
		dialog NPC_JACK_JACK_DESERT_INTRO_11
		dialog NPC_JACK_JACK_DESERT_INTRO_12

		set_state idle
		unlock_controls 1
	}
	
	jack_zara {
		lock_controls 1
		set_state blocking

		dialog NPC_JACK_JACK_ZARA_1
		dialog NPC_JACK_JACK_ZARA_2
		set_state verycloseup
		dialog NPC_JACK_JACK_ZARA_3
		set_state blocking
		dialog NPC_JACK_JACK_ZARA_4
		dialog NPC_JACK_JACK_ZARA_5
		dialog NPC_JACK_JACK_ZARA_6
		dialog NPC_JACK_JACK_ZARA_7
		dialog NPC_JACK_JACK_ZARA_8
		dialog NPC_JACK_JACK_ZARA_9
		dialog NPC_JACK_JACK_ZARA_10

		set_state idle
		unlock_controls 1
	}
	
	Jack_Gainaltfurniture {//jack explains what rare alts are and talks about the nona cat
		lock_controls 1
		set_state blocking
		set_state closeup
		dialog NPC_JACK_JACK_GAINALTFURNITURE_1
		dialog NPC_JACK_JACK_GAINALTFURNITURE_2
		dialog NPC_JACK_JACK_GAINALTFURNITURE_3
		dialog NPC_JACK_JACK_GAINALTFURNITURE_4
		set_state blocking
		dialog NPC_JACK_JACK_GAINALTFURNITURE_5
		dialog NPC_JACK_JACK_GAINALTFURNITURE_6
		dialog NPC_JACK_JACK_GAINALTFURNITURE_7
		dialog NPC_JACK_JACK_GAINALTFURNITURE_8

		set_state idle
		unlock_controls 1
	}
	
		//default  happy  veryhappy  sad  angry  veryangry
        //questioning  whispering  pondering  mocking
        //inlove  confused  paranoid  shocked  scared  spacedout
		//grossedout bored winking
}
```

---

## File: `organ_progression.gon`

### `states_and_transitions`
**Source:** `organ_progression.gon`  

```
states_and_transitions {
	states {
		idle ["idle" "blocking" "gone"]
	}

	transitions {
	}
}
```

---

### `sequences`
**Source:** `organ_progression.gon`  

**Localization Strings:**
- `NPC_ORGANGRINDER_UNPROMPTED_1`: "You can pick one. I'll keep the rest."
- `NPC_ORGANGRINDER_ALSO_1`: "Also..."
- `NPC_ORGANGRINDER_OUT_OF_STOCK_1`: "Be sure to come by again next time you fail."
- `NPC_ORGANGRINDER_PURCHASE_ITEM_1`: "Hehehe hope that helps."
- `NPC_ORGANGRINDER_SHOP_TOOLTIP`: "{name}. <br/> {desc}"
- `NPC_ORGANGRINDER_ORGAN_UNLOCK_1`: "[m:questioning]Oh hey wait, don't I know you?"
- `NPC_ORGANGRINDER_ORGAN_UNLOCK_2`: "[m:pondering]You look so damn familiar... maybe it's the hair? I knew someone with hair a while back..."
- `NPC_ORGANGRINDER_ORGAN_UNLOCK_3`: "[m:shocked]No wait, you are the cat lady? The one who keeps leaving me all those limp tasties!"
- `NPC_ORGANGRINDER_ORGAN_UNLOCK_4`: "[m:happy]Hey! I was just talking to someone who looked like you! Weird..."
- `NPC_ORGANGRINDER_ORGAN_UNLOCK_5`: "[m:spacedout][a:wave]. . .[/a]"
- `NPC_ORGANGRINDER_ORGAN_UNLOCK_6`: "[m:winking]The more corpses I collect, the juicier I become!"
- `NPC_ORGANGRINDER_ORGAN_UNLOCK_7`: "[m:default]With my needs met, I can take more time to collect goodies you left behind!"
- `NPC_ORGANGRINDER_ORGAN_UNLOCK_8`: "[m:angry]But now my urges have become stronger! <br/> My needs must be satiated!"
- `NPC_ORGANGRINDER_ORGAN_UNLOCK_9`: "[m:happy]Leave the flesh for ol' {organname}, I'll make it worth your while!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE1_1`: "[m:happy]More meat puppets for {organname}!? Heck yeah!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE1_2`: "[m:default]As long as {organname} is staying damp with ichor, I can be grabbing up all your trash for you!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE1_3`: "[m:questioning]I'm like the tin man from that movie The Wizard! But instead of oil i need plasma... to play video games!!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE1_4`: "[m:grossedout]*vurp*"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE1_5`: "[m:angry]Uh oh, that little clot just tried to leave! <br/> STAY IN THERE YOU NASTY LITTLE THING!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE1_6`: "[m:default]I gotta give 'em another crunch to stop their wiggling, then I just push a bone back there 'till it drops back into my paunch."
- `NPC_ORGANGRINDER_ORGAN_UPGRADE1_7`: "[m:questioning]You should kill more cats for me. I'm just saying to kill more cats so I can juice 'em and get stronger is all..."
- `NPC_ORGANGRINDER_ORGAN_UPGRADE1_8`: "[m:angry]I hunger!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE2_1`: "[m:inlove]Wow, you are killing all these cats just for me!? You must be having feelings for ol' {organname}."
- `NPC_ORGANGRINDER_ORGAN_UPGRADE2_2`: "[m:paranoid]... {organname} has never been in love before... but I've been practicing..."
- `NPC_ORGANGRINDER_ORGAN_UPGRADE2_3`: "[m:winking]A LOT!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE2_4`: "[m:pondering]Maybe next time when my lips aren't so scabby we can do a french kiss?... it's just an idea."
- `NPC_ORGANGRINDER_ORGAN_UPGRADE2_5`: "[m:inlove]Or maybe a 3-way kiss with me, you and Stacy!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE2_6`: "[m:shocked]Wait no.. Stacy? Why did I say Stacy? I meant Hunk!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE2_7`: "[m:winking]Hunk is what I'm calling the pile of dead bodies behind your house!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE2_8`: "[m:happy]Maybe once Hunk gets bigger we can do the kiss thing, he's a little short now..."
- `NPC_ORGANGRINDER_ORGAN_UPGRADE2_9`: "[m:angry]And I ain't kissing anyone under 6ft!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE3_1`: "[m:inlove]Thanks for those juicy hair sleeves! <br/> I'M FEELING ALL RILED UP NOW!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE3_2`: "[m:shocked]No wait, that's my IBS... yeah the bugs are definitely biting today!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE3_3`: "[m:paranoid]Sometimes I'm just punching at my belly so those damn bugs stop eating up all my cruor."
- `NPC_ORGANGRINDER_ORGAN_UPGRADE3_4`: "[m:veryangry]STOP IT RIGHT NOW YOU NASTY BUGS!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE3_5`: "[m:angry]I swear one day I'll poop those things out!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE3_6`: "[m:whispering][s:.5]... I'm just saying that to scare them, I'd never be mean like that.[/s]"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE3_7`: "[m:default]Please kill more of your cats for me and I'll grab up more things for you!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE4_1`: "[m:default]You know ol' {organname} was just standing here the other day and I swear I heard a kid crying..."
- `NPC_ORGANGRINDER_ORGAN_UPGRADE4_2`: "[m:questioning]Does this place have a basement? If so, can Hunk move in there? I don't like him anymore!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE4_3`: "[m:sad]He's getting too dry and sticky... I like my piles fresh and wet."
- `NPC_ORGANGRINDER_ORGAN_UPGRADE4_4`: "[m:bored]And it's probably TMI,  but.. he just lays there... <br/> If i wanted to date a corpse, I'd date you!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE4_5`: "[m:happy]Hahaha! <br/> I'm just joking, don't cry!... <br/> Hey wait, I'm remembering something... <br/> I used to cry once!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE4_6`: "[m:questioning]Yeah wait, haven't we met before?"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE4_7`: "[m:pondering]All this blood is starting to refurbish the grey matter! Let's plan on you killing more of your cats, OK?"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE4_8`: "[m:winking]The more you murder, the more I remember!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE5_1`: "[m:shocked]ANOTHER MEMORY APPEARS!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE5_2`: "[m:pondering]This one was big and wriggly... He would bite down hard on my skin when I'd pull him."
- `NPC_ORGANGRINDER_ORGAN_UPGRADE5_3`: "[m:sad]Sadly I pulled so hard it came apart, but I still have part of that memory stuck in my ear if you look close..."
- `NPC_ORGANGRINDER_ORGAN_UPGRADE5_4`: "[m:questioning]Do you see it? <br/> I think I got more memories up there too but my fingers are too stubby to reach."
- `NPC_ORGANGRINDER_ORGAN_UPGRADE5_5`: "[m:spacedout][a:wave]. . .[/a]"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE5_6`: "[m:pondering]Wait a minute, have we met? I swear I know that voice... did we used to work together?"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE5_7`: "[m:happy]Yeah.. didn't you kill cats and let me cover myself with their sanguine fluid?"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE5_8`: "[m:veryhappy]Yeah, you are that woman who's been letting me live behind your house!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE5_9`: "[m:happy]My memory is coming back! Keep doing whatever it is you are doing! It's working great!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE6_1`: "[m:happy]Uggghhh! My needs are being satiated!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE6_2`: "[m:veryhappy]You are really making things so slippery! I can feel the boils popping!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE6_3`: "[m:happy]My rashes are at their peak! So many memories! So much itching!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE6_4`: "[m:shocked]The memories are coming fast!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE6_5`: "[m:paranoid]I see someone digging up my grave! He looked just like me!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE6_6`: "[m:scared]A baby! A baby boy that was 2 babies in one!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE6_7`: "[m:shocked]I see a bean.. a talking bean with a man's voice!"
- `NPC_ORGANGRINDER_ORGAN_UPGRADE6_8`: "[m:angry]What does it all mean!?"
- `NPC_ORGANGRINDER_ORGAN_MAX_INTRO_1`: "[m:questioning]Hey guess what?  You know all those bumps and blisters covering my visible flesh?"
- `NPC_ORGANGRINDER_ORGAN_MAX_INTRO_2`: "[m:happy]Those are diseases! <br/> And guess what else?"
- `NPC_ORGANGRINDER_ORGAN_MAX_INTRO_3`: "[m:veryhappy]They are so rare and valuable!"
- `NPC_ORGANGRINDER_ORGAN_MAX_INTRO_4`: "[m:pondering]Since we are lovers, I think maybe ol' {organname} should be showering you in diseases!"
- `NPC_ORGANGRINDER_ORGAN_MAX_INTRO_5`: "[m:winking]You do the murdering, and I spit in a needle for you!"
- `NPC_ORGANGRINDER_ORGAN_MAX_INTRO_6`: "[m:happy]Deal!?"
- `NPC_ORGANGRINDER_ORGAN_MAX1_1`: "[m:happy]I coughed up a tonsil stone last night and put it into a syringe!"
- `NPC_ORGANGRINDER_ORGAN_MAX1_2`: "[m:veryhappy]It's my new invention! I call it..."
- `NPC_ORGANGRINDER_ORGAN_MAX1_3`: "{organname}!"
- `NPC_ORGANGRINDER_ORGAN_MAX1_4`: "[m:pondering]No wait... What??"
- `NPC_ORGANGRINDER_ORGAN_MAX1_5`: "[m:veryangry]FEED ME MORE BLOOD!"
- `NPC_ORGANGRINDER_ORGAN_MAX2_1`: "[m:happy]A new invention appears!"
- `NPC_ORGANGRINDER_ORGAN_MAX2_2`: "This one I made with butt scabs! But not just any butt scabs!"
- `NPC_ORGANGRINDER_ORGAN_MAX2_3`: "[m:veryhappy]The ones that live inside! The real itchy ones!"
- `NPC_ORGANGRINDER_ORGAN_MAX2_4`: "[m:winking]Tell me how it goes!"
- `NPC_ORGANGRINDER_ORGAN_MAX3_1`: "[m:default]I made up a new affliction for you!"
- `NPC_ORGANGRINDER_ORGAN_MAX3_2`: "[m:pondering]It's mostly composed of fromunda cheese!"
- `NPC_ORGANGRINDER_ORGAN_MAX3_3`: "[m:winking]You're gonna love it!"
- `NPC_ORGANGRINDER_ORGAN_MAX3_4`: "[m:angry]Now bleed me more kitties!"
- `NPC_ORGANGRINDER_ORGAN_MAX4_1`: "[m:happy]Look at this thing I just made up!"
- `NPC_ORGANGRINDER_ORGAN_MAX4_2`: "[m:winking]It's a needle full of hair! But its not just any hair... It's wet hair!"
- `NPC_ORGANGRINDER_ORGAN_MAX4_3`: "[m:happy]Shove that inside something and call me in the morning!"
- `NPC_ORGANGRINDER_ORGAN_MAX4_4`: "[m:default]I'm a doctor now!"
- `NPC_ORGANGRINDER_ORGAN_MAX5_1`: "[m:happy]Guess what I did!?"
- `NPC_ORGANGRINDER_ORGAN_MAX5_2`: "[m:veryhappy]I found out what happens when you juice a herpe!"
- `NPC_ORGANGRINDER_ORGAN_MAX5_3`: "[m:winking]Tell me how it tastes!"
- `NPC_ORGANGRINDER_ORGAN_MAX5_4`: "[m:default]See you next time!"
- `NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_1`: "[m:default]You know how to get into the Boneyard now!?"
- `NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_2`: "[m:happy]I USED TO LIVE THERE! <br/> Small world..."
- `NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_3`: "[m:sad]I also used to die there... [m:winking]Hey maybe you can die there too and we can be corpse buddies?"
- `NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_4`: "[m:spacedout][a:wave]. . .[/a]"
- `NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_5`: "[m:pondering]Oh uh... I just remembered something. <br/> There is a ghost in there called Dybbuk."
- `NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_6`: "[m:default]That guy will dive right inside you and puppet your skin around like a..."
- `NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_7`: "[m:confused]Well like a puppet I guess..."
- `NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_8`: "[m:default]Kinda like the worms do to me... [m:pondering]Hmm interesting."
- `NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_9`: "Wonder what happens when I pick all the worms out..."
- `NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_10`: "[m:scared]Do I just fold up like some kinda loose meat sandwich?"
- `NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_11`: "[m:happy]Mmmm that sounds tasty... a little too tasty if you ask me!"
- `NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_12`: "[m:scared]Yeah... I say we just leave those worms where they are..."
- `NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_1`: "[m:shocked]You opened the door to the Throbbing Domain!?"
- `NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_2`: "[m:veryangry]Why would you do that!?!"
- `NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_3`: "[m:angry]Do you have any clue how many corpses I had to eviscerate to build that wall of flesh?"
- `NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_4`: "[m:veryangry]My life's work ruined by some ignoramus... some ignor..."
- `NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_5`: "[m:spacedout][a:wave]. . .[/a]"
- `NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_6`: "[m:confused]Wait, What was I doing?"
- `NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_7`: "[m:default]Oh yeah, the Throbbing Domain!"
- `NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_8`: "[m:happy]I USED TO LIVE THERE! Small world..."
- `NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_9`: "[m:grossedout]That place is ruled by the Throbbing King!"
- `NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_10`: "[m:pondering]Well, we used to call him the buried king... But I guess he's not so buried anymore huh?"
- `NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_11`: "[m:default]Legend says hes the only self made man!"
- `NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_12`: "[m:paranoid] Single handedly created himself from pieces he stole from others!"
- `NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_13`: "[m:questioning]The lips of a cow, the tongue of a lion..."
- `NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_14`: "[m:veryhappy]and the ass of yo mama!"
- `NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_15`: "[m:happy]Hahaha! <br/> Heh... hehe..."
- `NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_16`: "[m:spacedout][a:wave]. . .[/a]"
- `NPC_ORGANGRINDER_ORGAN_TINA3_1`: "[m:questioning]Did you notice that thick layer of flies that appears to be moving around the city?"
- `NPC_ORGANGRINDER_ORGAN_TINA3_2`: "[m:default]Yep... <br/> I farted!"
- `NPC_ORGANGRINDER_ORGAN_TINA3_3`: "[m:veryhappy]Hahahahah!"
- `NPC_ORGANGRINDER_ORGAN_TINA3_4`: "[m:spacedout][a:wave]. . .[/a]"
- `NPC_ORGANGRINDER_ORGAN_TINA3_5`: "[m:default]Oh wait yeah, I wanted to give you a tip on how to kill that giant corpse!"
- `NPC_ORGANGRINDER_ORGAN_TINA3_6`: "[m:whispering]As a fellow corpse, I can give you a quick list of our weaknesses..."
- `NPC_ORGANGRINDER_ORGAN_TINA3_7`: "[m:default]1. Guns."
- `NPC_ORGANGRINDER_ORGAN_TINA3_8`: "[m:happy]2. Punches."
- `NPC_ORGANGRINDER_ORGAN_TINA3_9`: "[m:pondering][s:.8]3. Lasers.[/s]"
- `NPC_ORGANGRINDER_ORGAN_TINA3_10`: "[m:confused][s:.6]3. Hot fudge.[/s]"
- `NPC_ORGANGRINDER_ORGAN_TINA3_11`: "[s:.5][a:wave]3. Long walks on the beach.[/s][/a]"
- `NPC_ORGANGRINDER_ORGAN_TINA3_12`: "[m:bored][a:wave][s:.4]3. Blondes.[/s][/a]"
- `NPC_ORGANGRINDER_ORGAN_TINA3_13`: "[m:spacedout][s:.4][a:wave]. . . . . . .[/s][/a]"
- `NPC_ORGANGRINDER_ORGAN_TINA3_14`: "[m:paranoid]Umm.. what was I saying?"
- `NPC_ORGANGRINDER_ORGAN_TINA3_15`: "[m:happy]Oh yeah, Tina's rotting corpse!"
- `NPC_ORGANGRINDER_ORGAN_TINA3_16`: "[m:veryhappy]I USED TO LIVE THERE! <br/> Small world..."

```
sequences {
	
	unprompted {
		cancelable true
		dialog_and_autopass NPC_ORGANGRINDER_UNPROMPTED_1
		wait_for_cancel 1
	}

	also {
		dialog NPC_ORGANGRINDER_ALSO_1
	}

	out_of_stock {
		set_state blocking
		dialog NPC_ORGANGRINDER_OUT_OF_STOCK_1
	}
	purchase_item {
		cancelable true
		dialog_and_autopass NPC_ORGANGRINDER_PURCHASE_ITEM_1
		wait_for_cancel 1
	}

	tooltip {
		cancelable true
		tooltip_dialog NPC_ORGANGRINDER_SHOP_TOOLTIP
		wait_for_cancel 1
	}
	hide_text {
		cancelable true
		dialog_and_autopass ""
	}

	unknown {
		lock_controls 1
		set_state blocking
		dialog NPC_ORGANGRINDER_UNKNOWN_1
		get npc_reward
		set_state idle
		unlock_controls 1
	}

	organ_intro {
		lock_controls 1
		set_state idle
		dialog NPC_ORGANGRINDER_ORGAN_INTRO_1
		dialog NPC_ORGANGRINDER_ORGAN_INTRO_2
		dialog NPC_ORGANGRINDER_ORGAN_INTRO_3
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_INTRO_4
		dialog NPC_ORGANGRINDER_ORGAN_INTRO_5
		dialog NPC_ORGANGRINDER_ORGAN_INTRO_6
		set_state idle2
		dialog NPC_ORGANGRINDER_ORGAN_INTRO_7
		dialog NPC_ORGANGRINDER_ORGAN_INTRO_8
		dialog NPC_ORGANGRINDER_ORGAN_INTRO_9
		set_state closeup
		set_organ_name "Tyler" //sets organname from steam, if unavailable use the one listed here
		set_state verycloseup
		dialog NPC_ORGANGRINDER_ORGAN_INTRO_10
		dialog NPC_ORGANGRINDER_ORGAN_INTRO_11
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_INTRO_12
		set_state verycloseup
		dialog NPC_ORGANGRINDER_ORGAN_INTRO_13
		set_state idle2
		dialog NPC_ORGANGRINDER_ORGAN_INTRO_14
		dialog NPC_ORGANGRINDER_ORGAN_INTRO_15
	    dialog NPC_ORGANGRINDER_ORGAN_INTRO_16
		dialog NPC_ORGANGRINDER_ORGAN_INTRO_17
		dialog NPC_ORGANGRINDER_ORGAN_INTRO_18
		dialog NPC_ORGANGRINDER_ORGAN_INTRO_19	
		begin_accepting_cats organgrinder
		set_state idle2
		unlock_controls 1
		dialog_and_autopass NPC_ORGANGRINDER_ORGAN_INTRO_20
	}

	organ_rename {
		lock_controls 1
		set_state idle

		dialog NPC_ORGANGRINDER_ORGAN_RENAME_1
		dialog NPC_ORGANGRINDER_ORGAN_RENAME_2
		dialog NPC_ORGANGRINDER_ORGAN_RENAME_3
		dialog NPC_ORGANGRINDER_ORGAN_RENAME_4
		set_organ_name "Tyler" //sets organname from steam, if unavailable use the one listed here
		set_state verycloseup
		dialog NPC_ORGANGRINDER_ORGAN_RENAME_5
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_RENAME_6
		dialog NPC_ORGANGRINDER_ORGAN_RENAME_7
		set_state idle2
		dialog NPC_ORGANGRINDER_ORGAN_RENAME_8

		set_state idle
		unlock_controls 1
	}

	collected_new_items {
		lock_controls 1
		set_state blocking
		dialog NPC_ORGANGRINDER_COLLECTED_NEW_ITEMS_1
		dialog NPC_ORGANGRINDER_COLLECTED_NEW_ITEMS_2
		dialog NPC_ORGANGRINDER_COLLECTED_NEW_ITEMS_3
		dialog NPC_ORGANGRINDER_COLLECTED_NEW_ITEMS_4
		get npc_reward //this text overrides the "gain upgrade" text if you unlocked something
		set_state idle2
		unlock_controls 1
		dialog_and_autopass NPC_ORGANGRINDER_COLLECTED_NEW_ITEMS_5
	}
	collected_nothing { //this one happens if you die on the first combat and have 0 coins, food or items lol
		lock_controls 1
		set_state blocking
		dialog NPC_ORGANGRINDER_COLLECTED_NOTHING_1
		dialog NPC_ORGANGRINDER_COLLECTED_NOTHING_2
		dialog NPC_ORGANGRINDER_COLLECTED_NOTHING_3
		dialog NPC_ORGANGRINDER_COLLECTED_NOTHING_4
		dialog NPC_ORGANGRINDER_COLLECTED_NOTHING_5
		get npc_reward //this text overrides the "gain upgrade" text if you unlocked something
		set_state idle2
		unlock_controls 1
	}

	organ_unlock { //these ones only trigger if you level up organ grider via piping dead cats to him
		lock_controls 1
		set_state idle
		dialog NPC_ORGANGRINDER_ORGAN_UNLOCK_1
		dialog NPC_ORGANGRINDER_ORGAN_UNLOCK_2
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_UNLOCK_3
		dialog NPC_ORGANGRINDER_ORGAN_UNLOCK_4
		set_state idle2
		dialog NPC_ORGANGRINDER_ORGAN_UNLOCK_5
		dialog NPC_ORGANGRINDER_ORGAN_UNLOCK_6
		dialog NPC_ORGANGRINDER_ORGAN_UNLOCK_7
		dialog NPC_ORGANGRINDER_ORGAN_UNLOCK_8
		dialog NPC_ORGANGRINDER_ORGAN_UNLOCK_9
		get npc_reward
		set_state idle2
		unlock_controls 1
	}
	organ_upgrade1 { //these ones only trigger if you level up organ grider via piping dead cats to him
		lock_controls 1
		set_state idle
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE1_1
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE1_2
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE1_3
		set_state verycloseup
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE1_4
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE1_5
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE1_6
		set_state idle2
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE1_7
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE1_8
		get npc_reward
		set_state idle
		unlock_controls 1
	}
	organ_upgrade2 { //these ones only trigger if you level up organ grider via piping dead cats to him
		lock_controls 1
		set_state idle
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE2_1
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE2_2
		set_state verycloseup
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE2_3
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE2_4
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE2_5
		set_state idle2
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE2_6
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE2_7
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE2_8
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE2_9
		get npc_reward
		set_state idle2
		unlock_controls 1
	}
	organ_upgrade3 { //these ones only trigger if you level up organ grider via piping dead cats to him
		lock_controls 1
		set_state idle
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE3_1
		set_state idle2
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE3_2
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE3_3
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE3_4
		set_state idle2
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE3_5
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE3_6
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE3_7
		get npc_reward
		set_state idle2
		unlock_controls 1
	}
	organ_upgrade4 { //these ones only trigger if you level up organ grider via piping dead cats to him
		lock_controls 1
		set_state idle
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE4_1
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE4_2
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE4_3
		set_state idle2
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE4_4
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE4_5
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE4_6
		set_state idle
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE4_7
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE4_8
		get npc_reward
		set_state idle2
		unlock_controls 1
	}
	organ_upgrade5 { //these ones only trigger if you level up organ grider via piping dead cats to him
		lock_controls 1
		set_state idle
		set_state verycloseup
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE5_1
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE5_2
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE5_3
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE5_4
		set_state zoomedout
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE5_5
		set_state idle2
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE5_6
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE5_7
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE5_8
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE5_9
		get npc_reward
		set_state idle2
		unlock_controls 1
	}
	organ_upgrade6 { //these ones only trigger if you level up organ grider via piping dead cats to him
		lock_controls 1
		set_state idle
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE6_1
		set_state idle2
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE6_2
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE6_3
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE6_4
		set_state verycloseup
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE6_5
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE6_6
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE6_7
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_UPGRADE6_8
		get npc_reward
		set_state idle2
		unlock_controls 1
	}
	
	organ_max_intro {//when OG gains max favor
		lock_controls 1
		set_state idle
		dialog NPC_ORGANGRINDER_ORGAN_MAX_INTRO_1
		dialog NPC_ORGANGRINDER_ORGAN_MAX_INTRO_2
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_MAX_INTRO_3
		set_state idle2
		dialog NPC_ORGANGRINDER_ORGAN_MAX_INTRO_4
		dialog NPC_ORGANGRINDER_ORGAN_MAX_INTRO_5
		dialog NPC_ORGANGRINDER_ORGAN_MAX_INTRO_6
		get npc_reward
		set_state idle2
		unlock_controls 1
	}

	organ_max_repeating {
		do_random_sequence [organ_max1, organ_max2, organ_max3, organ_max4, organ_max5]
	}
	
	organ_max1 {//when OG gains max favor
		lock_controls 1
		set_state idle
		dialog NPC_ORGANGRINDER_ORGAN_MAX1_1
		dialog NPC_ORGANGRINDER_ORGAN_MAX1_2
		set_state verycloseup
		dialog NPC_ORGANGRINDER_ORGAN_MAX1_3
		set_state idle2
		dialog NPC_ORGANGRINDER_ORGAN_MAX1_4
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_MAX1_5
		get npc_reward
		set_state idle2
		unlock_controls 1
	}
	
	organ_max2 {//when OG gains max favor
		lock_controls 1
		set_state idle
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_MAX2_1
		set_state idle2
		dialog NPC_ORGANGRINDER_ORGAN_MAX2_2
		dialog NPC_ORGANGRINDER_ORGAN_MAX2_3
		dialog NPC_ORGANGRINDER_ORGAN_MAX2_4
		get npc_reward
		set_state idle2
		unlock_controls 1
	}
	
	organ_max3 {//when OG gains max favor
		lock_controls 1
		set_state idle
		dialog NPC_ORGANGRINDER_ORGAN_MAX3_1
		dialog NPC_ORGANGRINDER_ORGAN_MAX3_2
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_MAX3_3
		dialog NPC_ORGANGRINDER_ORGAN_MAX3_4
		get npc_reward
		set_state idle2
		unlock_controls 1
	}
	
	organ_max4 {//when OG gains max favor
		lock_controls 1
		set_state idle
		dialog NPC_ORGANGRINDER_ORGAN_MAX4_1
		dialog NPC_ORGANGRINDER_ORGAN_MAX4_2
		dialog NPC_ORGANGRINDER_ORGAN_MAX4_3
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_MAX4_4
		get npc_reward
		set_state idle2
		unlock_controls 1
	}
	
	organ_max5 {//when OG gains max favor
		lock_controls 1
		set_state idle
		dialog NPC_ORGANGRINDER_ORGAN_MAX5_1
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_MAX5_2
		dialog NPC_ORGANGRINDER_ORGAN_MAX5_3
		set_state idle2
		dialog NPC_ORGANGRINDER_ORGAN_MAX5_4
		get npc_reward
		set_state idle2
		unlock_controls 1
	}

	gone {
		set_state gone
	}
	
	//OG unlock intros
	
	organ_boneyard_intro {
		lock_controls 1
		set_state idle

		dialog NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_1
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_2
		set_state idle2
		dialog NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_3
		dialog NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_4	
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_5
		dialog NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_6
		dialog NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_7
		set_state idle2
		dialog NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_8
		dialog NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_9
		dialog NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_10
		dialog NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_11
		dialog NPC_ORGANGRINDER_ORGAN_BONEYARD_INTRO_12

		set_state idle2
		unlock_controls 1
	}

	organ_throbbingdomain_intro {
		lock_controls 1
		set_state idle

		dialog NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_1
		set_state verycloseup
		dialog NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_2
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_3
		dialog NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_4
		set_state idle2
		dialog NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_5	
		dialog NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_6
		dialog NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_7
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_8
		dialog NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_9
		dialog NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_10
		dialog NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_11
		dialog NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_12
		dialog NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_13
		set_state verycloseup
		dialog NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_14
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_15
		set_state idle2
		dialog NPC_ORGANGRINDER_ORGAN_THROBBINGDOMAIN_INTRO_16
		
		set_state idle2
		unlock_controls 1
	}

	organ_tina3 {
		lock_controls 1
		set_state idle

		dialog NPC_ORGANGRINDER_ORGAN_TINA3_1
		set_state verycloseup
		dialog NPC_ORGANGRINDER_ORGAN_TINA3_2
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_TINA3_3
		set_state idle2
		dialog NPC_ORGANGRINDER_ORGAN_TINA3_4	
		dialog NPC_ORGANGRINDER_ORGAN_TINA3_5
		dialog NPC_ORGANGRINDER_ORGAN_TINA3_6
		set_state idle2
		dialog NPC_ORGANGRINDER_ORGAN_TINA3_7
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_TINA3_8
		set_state verycloseup
		dialog NPC_ORGANGRINDER_ORGAN_TINA3_9
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_TINA3_10
		set_state idle2
		dialog NPC_ORGANGRINDER_ORGAN_TINA3_11
		set_state zoomedout
		dialog NPC_ORGANGRINDER_ORGAN_TINA3_12
	    dialog NPC_ORGANGRINDER_ORGAN_TINA3_13
		set_state idle2
		dialog NPC_ORGANGRINDER_ORGAN_TINA3_14
		dialog NPC_ORGANGRINDER_ORGAN_TINA3_15
		set_state closeup
		dialog NPC_ORGANGRINDER_ORGAN_TINA3_16

		set_state idle2
		unlock_controls 1
	}
	
		//default  happy  veryhappy  sad  angry  veryangry
        //questioning  whispering  pondering  mocking
        //inlove  confused  paranoid  shocked  scared  spacedout
		//grossedout bored winking
}
```

---

## File: `steven_progression.gon`

### `states_and_transitions`
**Source:** `steven_progression.gon`  

```
states_and_transitions {
	states {
		idle ["idle"]
	}

	transitions {
	}
}
```

---

### `sequences`
**Source:** `steven_progression.gon`  

**Localization Strings:**
- `NPC_STEVEN_UNKNOWN_1`: "You appear to have unlocked something, but I don't have dialog for it. Congrats. Also fix this."
- `NPC_STEVEN_ALSO_1`: "Also..."
- `NPC_STEVEN_UNPROMPTED_A_1`: "[m:winking]Get harder in seconds with... STEVEN!"
- `NPC_STEVEN_UNPROMPTED_A_2`: "[m:happy]Hahahaha!"
- `NPC_STEVEN_UNPROMPTED_B_1`: "[m:questioning]Are you lost?"
- `NPC_STEVEN_UNPROMPTED_C_1`: "[m:bored]Yep, still here I guess..."
- `NPC_STEVEN_UNPROMPTED_D_1`: "[m:happy]Oh hey! I was just thinking about you... [m:winking]I think Steven has a crush on you!"
- `NPC_STEVEN_UNPROMPTED_D_2`: "[m:whispering]Don't tell him I told you, [m:scared]He'd Fcukin' kill me!"
- `NPC_STEVEN_UNPROMPTED_E_1`: "If you are reading this message, you've probably been playing this game too long..."
- `NPC_STEVEN_UNPROMPTED_F_1`: "[m:angry]Well if it isn't old Cheater Face! [m:happy]How's life you disgraceful grifter?"
- `NPC_STEVEN_UNPROMPTED_G_1`: "[m:spacedout]Woah! Deja vu!"
- `NPC_STEVEN_UNPROMPTED_H_1`: "[m:bored]Yeeeeessss?"
- `NPC_STEVEN_UNPROMPTED_I_1`: "[m:veryhappy]Welcome to eternity! Can I show you to your room?"
- `NPC_STEVEN_STEVEN_MILLIONTRASHED_1`: "[m:default]One million cats have been flung into the void."
- `NPC_STEVEN_STEVEN_MILLIONTRASHED_2`: "[m:bored]There is no reward for this."
- `NPC_STEVEN_STEVEN_MILLIONTRASHED_3`: "[m:pondering]They just put this here to see if someone could ever do it.  I doubt it, personally."
- `NPC_STEVEN_STEVEN_MILLIONTRASHED_4`: "[m:bored]I'd be doing the L dance for you right now but no one ever made that animation..."
- `NPC_STEVEN_STEVEN_MILLIONTRASHED_5`: "[m:veryangry]... [a:shake]Stop playing![/s]"
- `NPC_STEVEN_STEVEN_INTRODUCTION_1`: "[m:questioning]Remember when you traveled through time? <br/> [s:1.6][m:shocked]Remember that?!![/s]"
- `NPC_STEVEN_STEVEN_INTRODUCTION_2`: "[m:veryangry][a:shake][s:1.4]Well, you done goofed![/s][/a]"
- `NPC_STEVEN_STEVEN_INTRODUCTION_3`: "[m:pondering]You know that thing where a Dracula can't come inside 'till you invite it?"
- `NPC_STEVEN_STEVEN_INTRODUCTION_4`: "[m:default]Well I'm like that but I come in when you start messing with timelines!"
- `NPC_STEVEN_STEVEN_INTRODUCTION_5`: "[m:happy]So now I'm here! <br/> [m:questioning]And guess what I'm in charge of!?"
- `NPC_STEVEN_STEVEN_INTRODUCTION_6`: "[m:veryhappy][s:1.6][a:shake]DIFFICULTY![/a][/s]"
- `NPC_STEVEN_STEVEN_INTRODUCTION_7`: "[m:default]See all those icons over there?  That's an options screen."
- `NPC_STEVEN_STEVEN_INTRODUCTION_8`: "[m:pondering]Click an arrow and that zone of the game gets harder. <br/> [m:happy]Simple."
- `NPC_STEVEN_STEVEN_INTRODUCTION_9`: "[m:questioning]But why would you do that you ask?"
- `NPC_STEVEN_STEVEN_INTRODUCTION_10`: "[m:default]Well beyond proving to your friends and family that you are smart and worthy of love..."
- `NPC_STEVEN_STEVEN_INTRODUCTION_11`: "[m:default]When you complete the game on "Hard", not only do you gain achievements you also get more [m:veryhappy]in-game unlocks!"
- `NPC_STEVEN_STEVEN_INTRODUCTION_12`: "[m:bored]And if you pussy out, just lower it."
- `NPC_STEVEN_STEVEN_INTRODUCTION_13`: "[m:winking]You can also resummon old house bosses too!"
- `NPC_STEVEN_STEVEN_INTRODUCTION_14`: "[m:happy]If you set their difficulty harder and kill 'em, they yield neat rewards!"
- `NPC_STEVEN_STEVEN_INTRODUCTION_15`: "Anyway, that's about it."
- `NPC_STEVEN_STEVEN_INTRODUCTION_16`: "That is until the DLC..."
- `NPC_STEVEN_STEVEN_INTRODUCTION_17`: "[m:angry]Where I become a final boss!"
- `NPC_STEVEN_STEVEN_INTRODUCTION_18`: "[m:veryangry][a:shake][s:1.3]And fcuk your shit up![/a][/s]"
- `NPC_STEVEN_STEVEN_INTRODUCTION_19`: "[m:happy]Bye!"
- `NPC_STEVEN_STEVEN_RESUMMON_1`: "Huh?..."
- `NPC_STEVEN_STEVEN_POSTENDGAME_1`: "[m:shocked]NO ONE EXPECTS THE STEVEN ENDING!"
- `NPC_STEVEN_STEVEN_POSTENDGAME_2`: "[m:winking]Pretty cool, huh? Bet you didn't see that one coming!?"
- `NPC_STEVEN_STEVEN_POSTENDGAME_3`: "[m:happy]That doctor's got the IQ of a baked potato now!"
- `NPC_STEVEN_STEVEN_POSTENDGAME_4`: "[m:bored]..."
- `NPC_STEVEN_STEVEN_POSTENDGAME_5`: "[m:angry]No need to get all emotional about it.  He was the bad guy, right?"
- `NPC_STEVEN_STEVEN_POSTENDGAME_6`: "[m:pondering]Right?? I mean, either way he wasn't very likeable..."
- `NPC_STEVEN_STEVEN_POSTENDGAME_7`: "[m:questioning]I'll be honest, I wasn't paying a lot of attention, but I'm sure as hell not the villain of this story!"
- `NPC_STEVEN_STEVEN_POSTENDGAME_8`: "[m:angry]I just got here man! If anything, you did way more bad things than me!"
- `NPC_STEVEN_STEVEN_POSTENDGAME_9`: "[m:bored]I'm not here to argue with you! We can both agree the ending was fine, let's move on!"
- `NPC_STEVEN_STEVEN_POSTENDGAME_10`: "[m:angry]Whatever, it's just a game man!"
- `NPC_STEVEN_STEVEN_POSTENDGAME_11`: "[m:paranoid]Speaking of that... I was snooping around the files and I swear to God I saw pieces of a DLC in there..."
- `NPC_STEVEN_STEVEN_POSTENDGAME_12`: "[m:pondering]I mean think about it, there are so many loose ends!"
- `NPC_STEVEN_STEVEN_POSTENDGAME_13`: "[m:default]Like you for example!"
- `NPC_STEVEN_STEVEN_POSTENDGAME_14`: "[m:veryhappy]THAT WAS A JOKE AT YOUR EXPENSE, BUDDY! I'M TALKING ABOUT YOUR BEAN HOLE!"
- `NPC_STEVEN_STEVEN_POSTENDGAME_15`: "[m:winking]See you at 100%!"
- `NPC_STEVEN_STEVEN_100_1`: "[m:bored]Oh wow... <br/> 100%"
- `NPC_STEVEN_STEVEN_100_2`: "[m:veryhappy]A number almost as round as you, tubby!"
- `NPC_STEVEN_STEVEN_100_3`: "[m:winking]See you in the next save!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT1_CRAZY_1`: "[m:veryhappy]Well look at you, <br/> video game wizard!!!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT1_CRAZY_2`: "[m:winking]How was that hit of dopamine!? Invigorating ain't it?"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT1_CRAZY_3`: "[m:happy]Well there is more where that came from, buddy! I got shitloads of ways to get high back here..."
- `NPC_STEVEN_STEVEN_UNLOCK_ACT1_CRAZY_4`: "Try this one out for size, it's called "Crazy Mode!""
- `NPC_STEVEN_STEVEN_UNLOCK_ACT1_CRAZY_5`: "[m:shocked]AND IT'S GONNA GET YOU SO LOADED!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT1_CRAZY_6`: "[m:default]Give it a go! More rewards! More dopamine! More brain melting hardships!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT1_IMPOSSIBLE_1`: "[m:default]Well as you probably expected there is another mode harder than Crazy."
- `NPC_STEVEN_STEVEN_UNLOCK_ACT1_IMPOSSIBLE_2`: "[m:shocked]It's called... <br/> "Impossible"!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT1_IMPOSSIBLE_3`: "[m:winking]I call it that because you probably won't beat it, because it's impossible."
- `NPC_STEVEN_STEVEN_UNLOCK_ACT1_IMPOSSIBLE_4`: "[m:bored]Obviously..."
- `NPC_STEVEN_STEVEN_UNLOCK_ACT1_IMPOSSIBLE_5`: "[m:happy]Have fun!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT2_HARD_1`: "[m:paranoid]Guess what!?"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT2_HARD_2`: "[m:veryhappy]You unlocked Hard Mode for Act 2!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT2_HARD_3`: "[m:default]That's the desert one..."
- `NPC_STEVEN_STEVEN_UNLOCK_ACT2_HARD_4`: "[m:happy]Spoiler... this game features 3 acts! So hold on to your butts!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT2_HARD_5`: "Bye!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT2_CRAZY_1`: "[m:worried]Man, you look light headed, maybe you should sit down."
- `NPC_STEVEN_STEVEN_UNLOCK_ACT2_CRAZY_2`: "All this video game playing is really doing a number on you..."
- `NPC_STEVEN_STEVEN_UNLOCK_ACT2_CRAZY_3`: "[m:pondering]What I mean is you look like shit. All sweaty, flabby and generally weird..."
- `NPC_STEVEN_STEVEN_UNLOCK_ACT2_CRAZY_4`: "[m:bored]You are ugly and no one likes you!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT2_CRAZY_5`: "[m:veryhappy]HAHAHAHA!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT2_CRAZY_6`: "[m:default]Oh, also you unlocked <br/> "Crazy Mode" on this act."
- `NPC_STEVEN_STEVEN_UNLOCK_ACT2_IMPOSSIBLE_1`: "Oh OK, you did something!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT2_IMPOSSIBLE_2`: "[m:pondering]Man, you must have a lot of time on your hands!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT2_IMPOSSIBLE_3`: "[m:winking]And by the looks of you, you probably got a lot of something else on your hands as well."
- `NPC_STEVEN_STEVEN_UNLOCK_ACT2_IMPOSSIBLE_4`: "[m:veryhappy]HA! Gotcha, bitch!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT2_IMPOSSIBLE_5`: "[m:happy]Here, let me unlock <br/> "Impossible Mode" for you on this act."
- `NPC_STEVEN_STEVEN_UNLOCK_ACT2_IMPOSSIBLE_6`: "Enjoy, pervert!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT3_HARD_1`: "[m:shocked]OMG, YOU UNLOCKED HARD MODE FOR ACT 3!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT3_HARD_2`: "[m:default]Someone should throw you a party or something!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT3_HARD_3`: "Speaking of, I hear it's your birthday today..."
- `NPC_STEVEN_STEVEN_UNLOCK_ACT3_HARD_4`: "[m:shocked]!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT3_HARD_5`: "[m:pondering]Well chances are it's not, but on the odd chance it was, I thought it would be a funny thing to say."
- `NPC_STEVEN_STEVEN_UNLOCK_ACT3_HARD_6`: "[m:default]Like imagine if it was your birthday and I said that.  Your mind would have been blown!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT3_HARD_7`: "Isn't that right, David!?"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT3_HARD_8`: "[m:shocked]!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT3_HARD_9`: "[m:winking]Now imagine if your name was David!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT3_HARD_10`: "[m:happy]GL!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT3_CRAZY_1`: "You unlocked Crazy Mode for Act 3.  Think you can handle it?!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT3_CRAZY_2`: "[m:veryangry]Oh yeah... HANDLE THIS!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT3_CRAZY_3`: "!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT3_CRAZY_4`: "[m:happy]At this point I'd reach through the screen and knock your fcukin' ass out!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT3_CRAZY_5`: "[m:veryangry]But they didn't add that animation option, so I'm just stuck here in this angry loop!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT3_CRAZY_6`: "Lazy devs..."
- `NPC_STEVEN_STEVEN_UNLOCK_ACT3_CRAZY_7`: "..."
- `NPC_STEVEN_STEVEN_UNLOCK_ACT3_IMPOSSIBLE_1`: "[m:happy]OK, this is the last one. Act 3: Impossible!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT3_IMPOSSIBLE_2`: "[m:veryhappy]Fun fact: YOU CAN'T WIN!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT3_IMPOSSIBLE_3`: "[m:happy]It's totally untested! The developers just added it to fcuk with you!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT3_IMPOSSIBLE_4`: "[m:questioning]So if you can't beat it, no judgment... you'll just have that achievement locked forever..."
- `NPC_STEVEN_STEVEN_UNLOCK_ACT3_IMPOSSIBLE_5`: "[m:angry]Every time you open the game it will be there haunting you! Taunting you! Teasing and harassing your loser brain!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT3_IMPOSSIBLE_6`: "[m:veryangry]IT'S NEVER GONNA HAPPEN DUDE! It's like a Lost Delirium run without the Holy Mantle unlocked!"
- `NPC_STEVEN_STEVEN_UNLOCK_ACT3_IMPOSSIBLE_7`: "[m:bored]It's not gonna happen dude!"

```
sequences {

	unknown {
		dialog NPC_STEVEN_UNKNOWN_1
		get npc_reward
	}

	also {
		dialog NPC_STEVEN_ALSO_1
	}
	
	unprompted {
		do_random_sequence [unprompted_a, unprompted_b, unprompted_c, unprompted_d, unprompted_e, unprompted_f, unprompted_g, unprompted_h, unprompted_i]
	}

	unprompted_a {
		dialog NPC_STEVEN_UNPROMPTED_A_1
		dialog NPC_STEVEN_UNPROMPTED_A_2
	}
	unprompted_b {
		dialog NPC_STEVEN_UNPROMPTED_B_1
	}
	unprompted_c {
		dialog NPC_STEVEN_UNPROMPTED_C_1
	}
	unprompted_d {
		dialog NPC_STEVEN_UNPROMPTED_D_1
		dialog NPC_STEVEN_UNPROMPTED_D_2
	}
	unprompted_e {
		dialog NPC_STEVEN_UNPROMPTED_E_1
	}
	unprompted_f {
		dialog NPC_STEVEN_UNPROMPTED_F_1
	}
	unprompted_g {
		dialog NPC_STEVEN_UNPROMPTED_G_1
	}
	unprompted_h {
		dialog NPC_STEVEN_UNPROMPTED_H_1
	}
	unprompted_i {
		dialog NPC_STEVEN_UNPROMPTED_I_1
	}

	steven_milliontrashed {
		set_state talking
		dialog NPC_STEVEN_STEVEN_MILLIONTRASHED_1
		set_state closeup
		dialog NPC_STEVEN_STEVEN_MILLIONTRASHED_2
		set_state talking
		dialog NPC_STEVEN_STEVEN_MILLIONTRASHED_3
		dialog NPC_STEVEN_STEVEN_MILLIONTRASHED_4
		set_state verycloseup
		dialog NPC_STEVEN_STEVEN_MILLIONTRASHED_5
		get npc_reward
	}
	
	steven_introduction { //Steven is unlocked after time travel
		lock_controls 1
		set_state closeup
		dialog NPC_STEVEN_STEVEN_INTRODUCTION_1
		set_state verycloseup
		dialog NPC_STEVEN_STEVEN_INTRODUCTION_2
		set_state closeup
		dialog NPC_STEVEN_STEVEN_INTRODUCTION_3
		dialog NPC_STEVEN_STEVEN_INTRODUCTION_4
		set_state talking
		dialog NPC_STEVEN_STEVEN_INTRODUCTION_5
		set_state verycloseup
		dialog NPC_STEVEN_STEVEN_INTRODUCTION_6
		set_state idle
		dialog NPC_STEVEN_STEVEN_INTRODUCTION_7
		dialog NPC_STEVEN_STEVEN_INTRODUCTION_8
		dialog NPC_STEVEN_STEVEN_INTRODUCTION_9
		set_state blocking
		dialog NPC_STEVEN_STEVEN_INTRODUCTION_10
		set_state idlenoani
		dialog NPC_STEVEN_STEVEN_INTRODUCTION_11
		dialog NPC_STEVEN_STEVEN_INTRODUCTION_12
		set_state closeup
		dialog NPC_STEVEN_STEVEN_INTRODUCTION_13
		set_state idlenoani
		dialog NPC_STEVEN_STEVEN_INTRODUCTION_14
		set_state blocking
		dialog NPC_STEVEN_STEVEN_INTRODUCTION_15
		set_state verycloseup
		dialog NPC_STEVEN_STEVEN_INTRODUCTION_16
		dialog NPC_STEVEN_STEVEN_INTRODUCTION_17
		dialog NPC_STEVEN_STEVEN_INTRODUCTION_18
		blocking idlenoani
		dialog NPC_STEVEN_STEVEN_INTRODUCTION_19
		set_state idlenoani
		unlock_controls 1
	}

	steven_resummon { //this is triggered after beating the final boss, when you unlock the ability to resummon house bosses
		lock_controls 1
		dialog NPC_STEVEN_STEVEN_RESUMMON_1
		unlock_controls 1
	}

	steven_postendgame { //what steven says after you have beaten the game and seen the final ending.
		lock_controls 1
		set_state blocking
		set_state verycloseup
		dialog NPC_STEVEN_STEVEN_POSTENDGAME_1
		set_state closeup
		dialog NPC_STEVEN_STEVEN_POSTENDGAME_2
		dialog NPC_STEVEN_STEVEN_POSTENDGAME_3
		set_state talking
		dialog NPC_STEVEN_STEVEN_POSTENDGAME_4
		dialog NPC_STEVEN_STEVEN_POSTENDGAME_5
		dialog NPC_STEVEN_STEVEN_POSTENDGAME_6
		dialog NPC_STEVEN_STEVEN_POSTENDGAME_7
		set_state closeup
		dialog NPC_STEVEN_STEVEN_POSTENDGAME_8
		//dialog "OK, I've been here the whole time, but I only really showed up when you broke the rules!"
		dialog NPC_STEVEN_STEVEN_POSTENDGAME_9
		set_state verycloseup
		dialog NPC_STEVEN_STEVEN_POSTENDGAME_10
		set_state closeup
		dialog NPC_STEVEN_STEVEN_POSTENDGAME_11
		dialog NPC_STEVEN_STEVEN_POSTENDGAME_12
		dialog NPC_STEVEN_STEVEN_POSTENDGAME_13
		set_state verycloseup
		dialog NPC_STEVEN_STEVEN_POSTENDGAME_14
		set_state talking
		dialog NPC_STEVEN_STEVEN_POSTENDGAME_15
		set_state idle
		unlock_controls 1
	}

	steven_100 { //what steven says when you 100% the game.
		lock_controls 1
		set_state blocking
		dialog NPC_STEVEN_STEVEN_100_1
		set_state closeup
		dialog NPC_STEVEN_STEVEN_100_2
		dialog NPC_STEVEN_STEVEN_100_3
		set_state idle
		unlock_controls 1
	}


	//steven act difficulty unlocks
	//steven_unlock_act1_hard { //this one is unnecessary as you get this the first time you meet steven
	//}
	steven_unlock_act1_crazy { //you get this one when you beat act 1 + its house bosses on hard
		lock_controls 1
		set_state blocking
		
		set_state closeup
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT1_CRAZY_1
		set_state verycloseup
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT1_CRAZY_2
		set_state closeup
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT1_CRAZY_3
		set_state talking
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT1_CRAZY_4
		set_state verycloseup
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT1_CRAZY_5
		set_state blocking
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT1_CRAZY_6

		set_state idle
		unlock_controls 1
	}
	steven_unlock_act1_impossible { //you get this one when you beat act 1 house bosses on crazy
		lock_controls 1
		set_state closeup
		
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT1_IMPOSSIBLE_1
		set_state talking
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT1_IMPOSSIBLE_2
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT1_IMPOSSIBLE_3
		set_state closeup
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT1_IMPOSSIBLE_4
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT1_IMPOSSIBLE_5

		set_state idle
		unlock_controls 1
	}
	steven_unlock_act2_hard { //you get this one when you beat act 2 for the first time
		lock_controls 1
		set_state closeup

		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT2_HARD_1
		set_state verycloseup
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT2_HARD_2
		set_state talking
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT2_HARD_3
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT2_HARD_4
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT2_HARD_5

		set_state idle
		unlock_controls 1
	}
	steven_unlock_act2_crazy {
		lock_controls 1
		set_state blocking

		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT2_CRAZY_1
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT2_CRAZY_2
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT2_CRAZY_3
		set_state closeup
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT2_CRAZY_4
		set_state verycloseup
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT2_CRAZY_5
		set_state talking
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT2_CRAZY_6

		set_state idle
		unlock_controls 1
	}
	steven_unlock_act2_impossible {
		lock_controls 1
		set_state talking

		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT2_IMPOSSIBLE_1
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT2_IMPOSSIBLE_2
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT2_IMPOSSIBLE_3
		set_state verycloseup
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT2_IMPOSSIBLE_4
		set_state talking
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT2_IMPOSSIBLE_5
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT2_IMPOSSIBLE_6

		set_state idle
		unlock_controls 1
	}
	steven_unlock_act3_hard { //you get this one when you beat act 3 for the first time
		lock_controls 1
		set_state verycloseup

		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT3_HARD_1
		set_state closeup
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT3_HARD_2
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT3_HARD_3
		set_state verycloseup
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT3_HARD_4
		set_state blocking
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT3_HARD_5
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT3_HARD_6
		set_state closeup
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT3_HARD_7
		set_state verycloseup
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT3_HARD_8
		set_state talking
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT3_HARD_9
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT3_HARD_10

		set_state idle
		unlock_controls 1
	}
	steven_unlock_act3_crazy {
		lock_controls 1
		set_state blocking

		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT3_CRAZY_1
		set_state closeup
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT3_CRAZY_2
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT3_CRAZY_3
		set_state blocking
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT3_CRAZY_4
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT3_CRAZY_5
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT3_CRAZY_6
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT3_CRAZY_7

		set_state idle
		unlock_controls 1
	}
	steven_unlock_act3_impossible {
		lock_controls 1
		set_state closeup

		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT3_IMPOSSIBLE_1
		set_state verycloseup
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT3_IMPOSSIBLE_2
		set_state blocking
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT3_IMPOSSIBLE_3
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT3_IMPOSSIBLE_4
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT3_IMPOSSIBLE_5
		set_state closeup
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT3_IMPOSSIBLE_6
		set_state talking
		dialog NPC_STEVEN_STEVEN_UNLOCK_ACT3_IMPOSSIBLE_7

		set_state idle
		unlock_controls 1
	}
	
}
```

---

## File: `tink_progression.gon`

### `states_and_transitions`
**Source:** `tink_progression.gon`  

```
states_and_transitions {
	states {
		idle ["idle"]
	}

	transitions {
	}
}
```

---

### `sequences`
**Source:** `tink_progression.gon`  

**Localization Strings:**
- `NPC_TINK_UNPROMPTED_1`: "[m:shocked]Um, why are you in my house?!"
- `NPC_TINK_UNKNOWN_1`: "You appear to have unlocked something, but I don't have dialog for it. Congrats. Also fix this."
- `NPC_TINK_ALSO_1`: "Also..."
- `NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_1`: "[m:happy]Well hello there!"
- `NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_2`: "[m:default]You are the talk of the town these days.  Everyone is all like..."
- `NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_3`: "[m:pondering]"There goes that so and so, aren't they a catch!?[m:happy] They got brains and buns!""
- `NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_4`: "[m:questioning]And I'm like <br/> "Thanks girl, but did you hear about that newbie in town who's been hoarding all those cats!?""
- `NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_5`: "[m:pondering]And then they are all <br/> "Yeah yeah, I heard about them.""
- `NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_6`: "[m:questioning]"But what's this I hear about that book deal you landed?""
- `NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_7`: "[m:angry]and I'm all <br/> "Leave me alone, stalker!""
- `NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_8`: "[m:happy]LOL! <br/> Gosh, people today are so nosy right!?"
- `NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_9`: "[m:default][a:wave]ANNNYWAY![/a]"
- `NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_10`: "What's this about you and me being pipe buddies?"
- `NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_11`: "[m:whispering]You know I can hear you talking in your sleep through that thing, right?"
- `NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_12`: "[m:mocking]You ol' perv! <br/> My wife made me cover the pipe with a quilt, she was so embarrassed!"
- `NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_13`: "[m:questioning]But listen..."
- `NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_14`: "[m:sad]I need a baby..."
- `NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_15`: "[m:sad]I have this empty hole in my heart. <br/> See, my wife and I, we can't have children of our own..."
- `NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_16`: "[m:questioning]So we have decided to start a cat family, and guess who the father is!?"
- `NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_17`: "[m:veryhappy]IT'S YOU, SILLY!"
- `NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_18`: "[m:default]Just send me your kittens and I'm sure I can find a way to return the favor."
- `NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_19`: "[m:angry]But try to not send me any uggos..."
- `NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_20`: "[m:veryangry]Keep your donkey-faced fuggos in the basement!"
- `NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_21`: "[m:default]Toodles!"
- `NPC_TINK_TINK_PRETTYBOW_1`: "[m:veryhappy]Oh happy day! <br/> My little heart is so full!"
- `NPC_TINK_TINK_PRETTYBOW_2`: "[m:happy]Thank you, thank you, thank you! <br/> You have no idea how much this little guy means to us!"
- `NPC_TINK_TINK_PRETTYBOW_3`: "[m:pondering]About your payment... <br/> I'm a bit at a loss here... <br/> Hmm."
- `NPC_TINK_TINK_PRETTYBOW_4`: "[m:default]Um, here. <br/> Take this little bow I guess."
- `NPC_TINK_TINK_PRETTYBOW_5`: "It may seem useless now, <br/> but in the right light, the color is just to die for!"
- `NPC_TINK_TINK_PRETTYBOW_6`: "[m:happy]Seriously this bow could make God cry!"
- `NPC_TINK_TINK_PRETTYBOW_7`: "[m:angry]Don't you dare throw it away!"
- `NPC_TINK_TINK_PRETTYBOW_8`: "[m:angry]. . ."
- `NPC_TINK_TINK_PRETTYBOW_9`: "[m:mocking]You can leave now..."
- `NPC_TINK_TINK_PRETTYBOW_10`: "[m:happy]Oh, but don't forget to keep sending me kittens! Toodles!"
- `NPC_TINK_TINK_TAGS_1`: "[m:default]Hey you! <br/> My wife and I were just talking about how grateful we are for all your help."
- `NPC_TINK_TINK_TAGS_2`: "Sadly, she just left.  But since she's gone we can go over some guy stuff."
- `NPC_TINK_TINK_TAGS_3`: "[m:questioning]So you know how we all just love to categorize and organize everything?"
- `NPC_TINK_TINK_TAGS_4`: "[m:default]Well I was recently watching some videos about that and discovered something!"
- `NPC_TINK_TINK_TAGS_5`: "You know when you select a cat in your house and it shows all its info to the left?"
- `NPC_TINK_TINK_TAGS_6`: "Well, if you click that thing by its name, you can assign a shape to it!"
- `NPC_TINK_TINK_TAGS_7`: "[m:whispering]I use the poopy shape quite often, you know, so I can remember what kittens are the ugly ones."
- `NPC_TINK_TINK_TAGS_8`: "[m:winking]That way I can quickly move them back to the basement when they escape!"
- `NPC_TINK_TINK_TAGS_9`: "[m:default]No need to thank me, <br/> just keep sending me those kittens!"
- `NPC_TINK_TINK_BASESTATS_1`: "[m:veryhappy]OMG GURL, <br/> did you see my new car outside?"
- `NPC_TINK_TINK_BASESTATS_2`: "My wife just got that for me for our 13 year anniversary!"
- `NPC_TINK_TINK_BASESTATS_3`: "[m:mocking]What can I say... <br/> I'm just a spoiled prince!"
- `NPC_TINK_TINK_BASESTATS_4`: "[m:default]All these kittens you keep sending are seriously scoring me points!"
- `NPC_TINK_TINK_BASESTATS_5`: "[m:happy]This time, as payment I'm going to fill you in on something cool."
- `NPC_TINK_TINK_BASESTATS_6`: "[m:default]From here on out, when you check your cat's info, you'll also see their Base and Bonus stats!"
- `NPC_TINK_TINK_BASESTATS_7`: "Base stats are what your cats will pass down to their kittens, you know, their DNA."
- `NPC_TINK_TINK_BASESTATS_8`: "[m:pondering]Bonus stats are modifiers.  Kittens wont inherit these at all... they are just, you know..."
- `NPC_TINK_TINK_BASESTATS_9`: "[m:pondering]Like, if they got a totally gross dog face or if they got some botox recently. <br/> those are the + and - numbers!"
- `NPC_TINK_TINK_BASESTATS_10`: "[m:questioning]I don't know how better to explain it... <br/> Just go look for yourself."
- `NPC_TINK_TINK_BASESTATS_11`: "[m:mocking]When you are built like this, you don't need to know "NUMBERS"!"
- `NPC_TINK_TINK_INBREEDING_1`: "[m:happy]Speak of the devil! <br/> I was just thinking about you!"
- `NPC_TINK_TINK_INBREEDING_2`: "[m:pondering]See, I was doing some research, you know, <br/> on ugly people."
- `NPC_TINK_TINK_INBREEDING_3`: "[m:shocked]And I discovered this thing called "Inbreeding", <br/> and it's totally nasty!"
- `NPC_TINK_TINK_INBREEDING_4`: "[m:questioning]So it's like when you kiss your brother and get goosebumps!"
- `NPC_TINK_TINK_INBREEDING_5`: "[m:scared]It's like that, but the goosebumps are huge and throbbing and your brother has no pants!"
- `NPC_TINK_TINK_INBREEDING_6`: "[m:pondering]Wait, no.  I'm telling this wrong..."
- `NPC_TINK_TINK_INBREEDING_7`: "[m:default]What I'm saying is there is a new smiley face emote on your cats info screen."
- `NPC_TINK_TINK_INBREEDING_8`: "If you'd swipe left on that emote... [m:paranoid]your cat is probably inbred... Ew."
- `NPC_TINK_TINK_INBREEDING_9`: "[m:angry]Inbred cats are not only super fuggs, but their bodies can get all wonky!"
- `NPC_TINK_TINK_INBREEDING_10`: "[m:veryangry]NOT GOOD!"
- `NPC_TINK_TINK_INBREEDING_11`: "[a:wave][m:happy]ANNNNNYYWAY![/a]"
- `NPC_TINK_TINK_INBREEDING_12`: "[m:default]So that's a thing to check now, I guess?"
- `NPC_TINK_TINK_INBREEDING_13`: "[m:happy]Keep sending those kittens!"
- `NPC_TINK_TINK_AGGRESSION_1`: "[m:happy]. . ."
- `NPC_TINK_TINK_AGGRESSION_2`: "[m:angry]Well...?!"
- `NPC_TINK_TINK_AGGRESSION_3`: "[m:veryangry]Aren't you going to say something nice about my new shirt?!"
- `NPC_TINK_TINK_AGGRESSION_4`: "MY GAWD! <br/> I'm so sick of rude people!"
- `NPC_TINK_TINK_AGGRESSION_5`: "[m:angry]Why can't people just get past their insecurities and compliment me!?"
- `NPC_TINK_TINK_AGGRESSION_6`: "Get over yourself!"
- `NPC_TINK_TINK_AGGRESSION_7`: "[m:default]Whatever... <br/> How can I stay mad at the baby daddy of all my kitties!?"
- `NPC_TINK_TINK_AGGRESSION_8`: "[m:questioning]So, have you ever wanted to know if someone is a huge moody biotch, just by looking at them?"
- `NPC_TINK_TINK_AGGRESSION_9`: "[m:mocking]God knows I have..."
- `NPC_TINK_TINK_AGGRESSION_10`: "[m:happy]Well, now you can! <br/> Just check your cat's info tab and you can see if its an agro nut-ball or not!"
- `NPC_TINK_TINK_AGGRESSION_11`: "[m:angry]. . ."
- `NPC_TINK_TINK_AGGRESSION_12`: "You can leave now..."
- `NPC_TINK_TINK_SEXUALITY_1`: "[m:default]Have you ever heard of the term "[b]gaydar[/b]"?"
- `NPC_TINK_TINK_SEXUALITY_2`: "[m:pondering]It's this innate sense people have where they can instantly tell if someone is queer."
- `NPC_TINK_TINK_SEXUALITY_3`: "[m:happy]Even from 50 feet away!"
- `NPC_TINK_TINK_SEXUALITY_4`: "[m:default]Well, I myself have that ability, and as payment for your kittens, I bestow it upon you!"
- `NPC_TINK_TINK_SEXUALITY_5`: "[m:happy]From here on out, you will instantly know if your cats are Gay, Straight, Bi..."
- `NPC_TINK_TINK_SEXUALITY_6`: "[m:pondering]Pan, Demi, Poly, Andro, Auto, Feebis, Beepis, Gyne, Mono, Gray, Cetero, Multi or even Curious!"
- `NPC_TINK_TINK_SEXUALITY_7`: "[m:confused]Well maybe not all that, but def the first three..."
- `NPC_TINK_TINK_SEXUALITY_8`: "[m:mocking]And I know what you are wondering, and yes, my wife is Str8!!"
- `NPC_TINK_TINK_SEXUALITY_9`: "So don't you be getting any ideas!"
- `NPC_TINK_TINK_SEXUALITY_10`: "[m:shocked]Oh, I think I hear her pulling up... Get the hell out of here!"
- `NPC_TINK_TINK_SEXUALITY_11`: "[m:scared]I don't need her assuming anything.  She can be quite territorial."
- `NPC_TINK_TINK_SEXUALITY_12`: "[m:shocked]GET OUT!"
- `NPC_TINK_TINK_RELATIONSHIPS_1`: "[m:veryhappy]Our home is overflowing with love!"
- `NPC_TINK_TINK_RELATIONSHIPS_2`: "Thank you sooo much! <br/> I can't tell you how happy we are to have such a giant fur family!"
- `NPC_TINK_TINK_RELATIONSHIPS_3`: "[m:angry]I just wish our neighbors would mind their damn business!"
- `NPC_TINK_TINK_RELATIONSHIPS_4`: "I swear they have it out for me! We have had the county visit twice this month!"
- `NPC_TINK_TINK_RELATIONSHIPS_5`: "I can't help it if our children wander into their house and crap all over their kitchen table!"
- `NPC_TINK_TINK_RELATIONSHIPS_6`: "[m:happy]. . ."
- `NPC_TINK_TINK_RELATIONSHIPS_7`: "[m:veryhappy]I'm lying, it was me... I shit on their table! <br/> Tee hee."
- `NPC_TINK_TINK_RELATIONSHIPS_8`: "[m:mocking]That's what they get for calling the county the first time!"
- `NPC_TINK_TINK_RELATIONSHIPS_9`: "[m:veryangry]THERE'S MORE WHERE THAT CAME FROM, BILL!"
- `NPC_TINK_TINK_RELATIONSHIPS_10`: "[m:whispering]I've been eating tons of Pinky Winkies..."
- `NPC_TINK_TINK_RELATIONSHIPS_11`: "[a:wave][m:happy]ANNNNYWAY![/a]"
- `NPC_TINK_TINK_RELATIONSHIPS_12`: "[m:default]Speaking of people I wish would..."
- `NPC_TINK_TINK_RELATIONSHIPS_13`: "[m:veryangry]DIE OF A HEART ATTACK ON TOP OF THEIR WIFE! <br/> KILLING THEM BOTH!"
- `NPC_TINK_TINK_RELATIONSHIPS_14`: "[m:default]You can now tell who your cats hate!"
- `NPC_TINK_TINK_RELATIONSHIPS_15`: "[m:inlove]You can also tell who they are in love with..."
- `NPC_TINK_TINK_RELATIONSHIPS_16`: "[m:default]For me, that would be..."
- `NPC_TINK_TINK_RELATIONSHIPS_17`: "[m:veryangry]MY WIFE! NOT YOU, BILL! MY WIFE!!"
- `NPC_TINK_TINK_RELATIONSHIPS_18`: "[m:angry]GAWD!"
- `NPC_TINK_TINK_RELATIONSHIPS_19`: "[m:shocked]Anyway, I gotta use the little girl's room..."
- `NPC_TINK_TINK_RELATIONSHIPS_20`: "[m:winking]Toodles!"
- `NPC_TINK_TINK_MAX_INTRO_1`: "[m:pondering]Listen sister, don't tell the boys... But I'm all out of tea..."
- `NPC_TINK_TINK_MAX_INTRO_2`: "[m:shocked]I'm literally drained of gossip! GAH!"
- `NPC_TINK_TINK_MAX_INTRO_3`: "[m:scared]I'm a fraud! <br/> And everyone is going to find out!"
- `NPC_TINK_TINK_MAX_INTRO_4`: "[m:sad]My wife will never be able to look me in the face again!"
- `NPC_TINK_TINK_MAX_INTRO_5`: "[m:shocked]If she leaves me, I'm ruined! Who will spoil me!?"
- `NPC_TINK_TINK_MAX_INTRO_6`: "[m:scared]This can't be the fate of Ferguson Rodney Tinkles!!!!!"
- `NPC_TINK_TINK_MAX_INTRO_7`: "[m:paranoid]!"
- `NPC_TINK_TINK_MAX_INTRO_8`: "OK, what's it going to take for you to keep those lips zipped!?"
- `NPC_TINK_TINK_MAX_INTRO_9`: "[m:angry]Extortion is it? <br/> [m:pondering]Well I can't say I don't respect the hustle, girl..."
- `NPC_TINK_TINK_MAX_INTRO_10`: "[m:default]A true boss bitch! <br/> OK, so how's 25 bucks sound?"
- `NPC_TINK_TINK_MAX_INTRO_11`: "[m:questioning]Will that keep you from tattling about my shortcomings?"
- `NPC_TINK_TINK_MAX_INTRO_12`: "[m:default]OK, deal!"
- `NPC_TINK_TINK_MAX1_1`: "[m:angry]Oh I see your game... Keep sending me cats so you can blackmail me into a steady income flow?"
- `NPC_TINK_TINK_MAX1_2`: "[m:pondering]Well played girl... <br/> Well played..."
- `NPC_TINK_TINK_MAX1_3`: "[m:default]Here's your hush money! $25 as per our agreement."
- `NPC_TINK_TINK_MAX1_4`: "[m:angry]Now get out of here!!"
- `NPC_TINK_TINK_MAX2_1`: "[m:scared]Please stop sending me kittens..."
- `NPC_TINK_TINK_MAX2_2`: "My wife is going to eventually notice the missing cash!"
- `NPC_TINK_TINK_MAX2_3`: "[m:angry]You are a real sicko, you know that!?"
- `NPC_TINK_TINK_MAX2_4`: "Fine! Take this 25 bucks! I WAS going to spend it on something nice for the wife!"
- `NPC_TINK_TINK_MAX2_5`: "[m:sad]But I guess lingerie is off the table tonight..."
- `NPC_TINK_TINK_MAX2_6`: "[m:angry]I had my eyes on this skin-tight pink leather number, but I guess that little dream is over!"
- `NPC_TINK_TINK_MAX2_7`: "[m:veryangry]Thanks for ruining my life!!!"
- `NPC_TINK_TINK_MAX3_1`: "[m:angry]Yeah yeah, I know the routine... <br/> Heres $25!"
- `NPC_TINK_TINK_MAX3_2`: "[m:veryangry]NOW DON'T LET ME SEE YOUR FACE AROUND MY HOUSE AGAIN!"
- `NPC_TINK_TINK_MAX3_3`: "[m:scared]My wife is going to kill me... I can't keep sneaking money from her purse forever!"
- `NPC_TINK_TINK_MAX3_4`: "[m:winking]Maybe there is something else I can pay you with?"
- `NPC_TINK_TINK_MAX3_5`: "[m:shocked]???"
- `NPC_TINK_TINK_MAX3_6`: "[m:veryangry]FINE! YOUR LOSS! <br/> I WAS JOKING ANYWAY!"
- `NPC_TINK_TINK_MAX4_1`: "[m:happy]You know I've been looking into you!"
- `NPC_TINK_TINK_MAX4_2`: "[m:winking]Maybe it's time the blackmailer becomes the blackmailee!?"
- `NPC_TINK_TINK_MAX4_3`: "[m:happy]Yes, it's true! I know your secret identity! And if you don't want me to spill those beans, its gonna cost ya!"
- `NPC_TINK_TINK_MAX4_4`: "[m:winking]25 big ones! Hahaha! Checkmate ya old bitch!"
- `NPC_TINK_TINK_MAX4_5`: "[m:shocked]!!!"
- `NPC_TINK_TINK_MAX4_6`: "You are raising your price!?!"
- `NPC_TINK_TINK_MAX4_7`: "[m:veryangry]TO $100!!!? THAT'S INSANE!"
- `NPC_TINK_TINK_MAX4_8`: "[m:shocked]INFLATION!?"
- `NPC_TINK_TINK_MAX4_9`: "[m:angry]FINE! HERE! TAKE YOUR $25! BUT I'M WARNING YOU!"
- `NPC_TINK_TINK_MAX4_10`: "[m:veryangry]YOUR TIME IS COMING! WATCH YOUR BACK!"
- `NPC_TINK_TINK_MAX5_1`: "[m:pondering]You know, I looked into this blackmail scheme you got me locked into..."
- `NPC_TINK_TINK_MAX5_2`: "[m:questioning]Were you aware it's 100% illegal!?"
- `NPC_TINK_TINK_MAX5_3`: "[m:veryangry]YOU ARE GOING TO JAIL BUDDY!"
- `NPC_TINK_TINK_MAX5_4`: "[m:angry]But until then, here is that 25 bucks I owe you!"
- `NPC_TINK_TINK_MAX6_1`: "[m:paranoid]Listen, my wife has been asking about her missing cash..."
- `NPC_TINK_TINK_MAX6_2`: "I think she's on to us... Can you like, slow down on the kittens?"
- `NPC_TINK_TINK_MAX6_3`: "[m:scared]I told her I'm using the money on botox but eventually this youthful mug will fade..."
- `NPC_TINK_TINK_MAX6_4`: "And then I'm really screwed!"
- `NPC_TINK_TINK_MAX6_5`: "[m:angry]Take the money, but cool it on the cats!"
- `NPC_TINK_TINK_MAX7_1`: "[m:pondering]You know, I was thinking 25 bucks to keep you quiet feels a bit high..."
- `NPC_TINK_TINK_MAX7_2`: "[m:questioning]I'm thinking we drop it to like $5? That feels fair to me..."
- `NPC_TINK_TINK_MAX7_3`: "[m:shocked]..."
- `NPC_TINK_TINK_MAX7_4`: "[m:angry]Seriously! $25 is like 10 bucks a cat or whatever!"
- `NPC_TINK_TINK_MAX7_5`: "Listen! I'm not some math nerd like you! I spent my time at school kissing girls and mocking the ugly and bewildered!"
- `NPC_TINK_TINK_MAX7_6`: "[m:veryangry]WHATEVER! HERE! GO SPEND IT ON A DIET BOOK YOU LUMP OF HOG LARD!"
- `NPC_TINK_TINK_MAX8_1`: "[m:winking]You know, I'm starting to think this whole extortion thing is just an excuse for you to talk to me..."
- `NPC_TINK_TINK_MAX8_2`: "[m:pondering]I got this theory.  Everyone I know either wants to be me, or be inside me!"
- `NPC_TINK_TINK_MAX8_3`: "Not sure which one of those you are yet... [m:angry]Maybe both!? Jealous much!?"
- `NPC_TINK_TINK_MAX8_4`: "Here.. take the money, but this is the last time!"
- `NPC_TINK_TINK_MAX9_1`: "[m:veryangry]WHAT!?"
- `NPC_TINK_TINK_MAX9_2`: "[m:angry]Listen, I'm very busy with lots of important things right now!"
- `NPC_TINK_TINK_MAX9_3`: "Take the 25 bucks, whatever!"
- `NPC_TINK_TINK_MAX9_4`: "God, I'm so over you!"
- `NPC_TINK_TINK_MAX9_5`: "[m:veryangry]STOP INTERRUPTING ME!"
- `NPC_TINK_TINK_MAX10_1`: "[m:scared]This has to stop, for reals!"
- `NPC_TINK_TINK_MAX10_2`: "[m:questioning]All I hear these days is <br/> "Where is my 25 bucks Ferguson!?""
- `NPC_TINK_TINK_MAX10_3`: ""[m:angry]ALL MY MONEY IS GONE AGAIN, FERGUSON!""
- `NPC_TINK_TINK_MAX10_4`: ""I'M LATE ON THE MORTGAGE AGAIN FERGUSON!""
- `NPC_TINK_TINK_MAX10_5`: "[m:veryangry]"STOP GETTING LIP FILLER AND LIPO FERGUSON!""
- `NPC_TINK_TINK_MAX10_6`: "[m:angry]The nagging is never ending!"
- `NPC_TINK_TINK_MAX10_7`: "I swear I'd be pulling my hair out, but we both know I cant afford plugs again!"
- `NPC_TINK_TINK_MAX10_8`: "[m:veryangry]STOP SENDING ME KITTENS!"
- `NPC_TINK_TINK_MAX10_9`: "PLEASE!"
- `NPC_TINK_UNPROMPTED_A_1`: "Oh, it's you again!"
- `NPC_TINK_UNPROMPTED_A_2`: "[m:happy]Ready for some hot gossip?"
- `NPC_TINK_UNPROMPTED_B_1`: "[m:questioning]I think someone has a crush on me!"
- `NPC_TINK_UNPROMPTED_B_2`: "Ok gurl, let me spill the tea..."
- `NPC_TINK_UNPROMPTED_C_1`: "[m:happy]Well someone is in need of a makeover! <br/> Let's chat!"
- `NPC_TINK_UNPROMPTED_D_1`: "[m:mocking]Well look who just can't get enough of me! Now, listen up!"
- `NPC_TINK_UNPROMPTED_E_1`: "[m:veryhappy]I'm so happy to see you! I assume you want more gossip?"
- `NPC_TINK_UNPROMPTED_F_1`: "Yep, still here! It's like I never leave this damn RV these days."
- `NPC_TINK_UNPROMPTED_F_2`: "Now listen honey..."
- `NPC_TINK_UNPROMPTED_G_1`: "[m:shocked]Gah, you spooked me! Were you watching me do my makeup?"
- `NPC_TINK_UNPROMPTED_G_2`: "It's just coverup for my scar.  So nosy! Want a tip?"
- `NPC_TINK_UNPROMPTED_H_1`: "[m:scared]If you keep dropping by like this people are going to get the wrong idea about us!"
- `NPC_TINK_UNPROMPTED_H_2`: "[m:default]I did have some information for you, so lend me your ear."
- `NPC_TINK_UNPROMPTED_I_1`: "[m:angry]Oh it's you. Let's cut to it, I'm in a mood today..."
- `NPC_TINK_TINK_TIPS_INTRO_1`: "[m:mocking]So your house is filthy and your cats are all donked up, I assume?"
- `NPC_TINK_TINK_TIPS_INTRO_2`: "[m:happy]Well don't you worry your pretty little head. Tink is here for you!"
- `NPC_TINK_TINK_TIPS_INTRO_3`: "I have loads of hot gossip just oozing from my veins!"
- `NPC_TINK_TINK_TIPS_INTRO_4`: "[m:default]So let me keep you in the loop..."
- `NPC_TINK_TINK_TIPS_COMFORT_1`: "[m:default]See this thing? [img:comfort] That icon is Comfort!"
- `NPC_TINK_TINK_TIPS_COMFORT_2`: "High Comfort[img:comfort] is vital for your kitties."
- `NPC_TINK_TINK_TIPS_COMFORT_3`: "A low Comfort[img:comfort] will not only prevent breeding, [m:scared]but it can cause serious aggression!"
- `NPC_TINK_TINK_TIPS_COMFORT_4`: "[m:happy]Keep that Comfort[img:comfort] stat high and your cats will breed like rabbits!"
- `NPC_TINK_TINK_TIPS_STIMULATION_1`: "[m:default]So you know this icon? <br/> [img:stimulation] That's Stimulation."
- `NPC_TINK_TINK_TIPS_STIMULATION_2`: "[m:pondering]It's supposed to be a yarn ball or something?"
- `NPC_TINK_TINK_TIPS_STIMULATION_3`: "[m:default]High Stimulation[img:stimulation] is needed if you want your kittens to inherit things from their parents."
- `NPC_TINK_TINK_TIPS_STIMULATION_4`: "Base stats and even the abilities of your cats can be passed down as long as your Stimulation[img:stimulation] is high enough."
- `NPC_TINK_TINK_TIPS_STIMULATION_5`: "So if a father is 7 and a mother is a 3, a big Stimulation[img:stimulation] number will ensure their offspring are also 7's!"
- `NPC_TINK_TINK_TIPS_STIMULATION_6`: "[m:sad]And not nasty uggos like their mother... <br/> [a:shake]*shudders*[/a]"
- `NPC_TINK_TINK_TIPS_STIMULATION_7`: "[m:happy]Every good breeder puts a heavy focus on Stimulation[img:stimulation], so don't neglect it!"
- `NPC_TINK_TINK_TIPS_APPEAL_1`: "[m:default]Ever notice this [img:appeal] icon above your house? That's your house's Appeal."
- `NPC_TINK_TINK_TIPS_APPEAL_2`: "[m:questioning]Appeal[img:appeal] makes your house, <br/> well more appealing I guess?"
- `NPC_TINK_TINK_TIPS_APPEAL_3`: "[m:default]The higher your Appeal[img:appeal], the better the strays are that appear each day!"
- `NPC_TINK_TINK_TIPS_APPEAL_4`: "Don't sleep on Appeal[img:appeal]!"
- `NPC_TINK_TINK_TIPS_HEALTH_1`: "[m:default][img:health], that thing is a Health icon!"
- `NPC_TINK_TINK_TIPS_HEALTH_2`: "A room with Health[img:health] has a chance to heal wounds, and even cure diseases!"
- `NPC_TINK_TINK_TIPS_HEALTH_3`: "The higher the Health[img:health], the better those odds are."
- `NPC_TINK_TINK_TIPS_HEALTH_4`: "[m:scared]but the opposite is also true. Low Health[img:health] can actually cause disease too!"
- `NPC_TINK_TINK_TIPS_HEALTH_5`: "[m:default]So be careful!"
- `NPC_TINK_TINK_TIPS_MUTATION_1`: "[m:default]Here is a rare one, [img:evolution]! That's the Mutation icon!"
- `NPC_TINK_TINK_TIPS_MUTATION_2`: "[m:mocking]This thing will do wonders on your skin!"
- `NPC_TINK_TINK_TIPS_MUTATION_3`: "[m:default]Rooms with Mutation[img:evolution] have a chance to mutate the cats inside!"
- `NPC_TINK_TINK_TIPS_MUTATION_4`: "[m:happy]Need an extra hand around the house? Maybe you can grow one!?"
- `NPC_TINK_TINK_TIPS_CLEANING_1`: "[m:angry]Clean your house!"
- `NPC_TINK_TINK_TIPS_CLEANING_2`: "Poops and dead cats actually lower your Comfort[img:comfort]"
- `NPC_TINK_TINK_TIPS_CLEANING_3`: "and it's also just really freakin' gross!"
- `NPC_TINK_TINK_TIPS_CLEANING_4`: "[m:veryangry]Wash yourself, gurl!"
- `NPC_TINK_TINK_TIPS_BASESTATS_1`: "[m:default]Base stats are important for breeding."
- `NPC_TINK_TINK_TIPS_BASESTATS_2`: "When you breed cats, their base stats are what their kittens can inherit."
- `NPC_TINK_TINK_TIPS_BASESTATS_3`: "[m:mocking]Ignore any bonus modifiers, base stats are the only stat that matters for breeding!"
- `NPC_TINK_TINK_TIPS_MULTICLASSING_1`: "[m:default]Rooms with high Stimulation[img:stimulation] can often times yield kittens with class abilities!"
- `NPC_TINK_TINK_TIPS_MULTICLASSING_2`: "[m:happy]You realize what that means!? Multiclassing!"
- `NPC_TINK_TINK_TIPS_MULTICLASSING_3`: "[m:veryhappy]Mages with Fighter abilities! <br/> Tanks with Thief movement!"
- `NPC_TINK_TINK_TIPS_MULTICLASSING_4`: "[m:scared]I realize how nerdy that just sounded... <br/> Sorry, my ex was a <br/> "dungeon master"."
- `NPC_TINK_TINK_TIPS_MULTICLASSING_5`: "[m:sad]The things a girl will do in college to get attention..."
- `NPC_TINK_TINK_TIPS_INBREEDING_1`: "[m:default]Inbreeding may sound cool,[m:angry] but it's not!"
- `NPC_TINK_TINK_TIPS_INBREEDING_2`: "Just because it has the word breeding in the name, doesn't instantly make it cool!"
- `NPC_TINK_TINK_TIPS_INBREEDING_3`: "[m:shocked]Inbred cats can be born with seriously bad birth defects!"
- `NPC_TINK_TINK_TIPS_INBREEDING_4`: "[m:whispering]And you know what that means..."
- `NPC_TINK_TINK_TIPS_INBREEDING_5`: "[m:paranoid]U G L Y !"
- `NPC_TINK_TINK_TINA2_1`: "[m:scared]I was driving past Pinky Winkies today and swear to God, I saw that fat cat's head rolling through the street!"
- `NPC_TINK_TINK_TINA2_2`: "[m:questioning]You know that morbidly obese one with the vore fetish you murdered last month? That one."
- `NPC_TINK_TINK_TINA2_3`: "[m:shocked]Then, out of nowhere, her giant blubber body comes flopping its way down the street, after the head!"
- `NPC_TINK_TINK_TINA2_4`: "[m:sad]I tried to take a pic but my camera roll was totally full..."
- `NPC_TINK_TINK_TINA2_5`: "[m:happy]I was doing glamor shots with the ol' ball n' chain last night and it got a little cray-cray."
- `NPC_TINK_TINK_TINA2_6`: "[m:winking]I was going to delete a few pics to make room but got caught up in how amazing I was looking last night."
- `NPC_TINK_TINK_TINA2_7`: "[m:angry]Then this guy in a bandit mask flipped me off and yelled in this very aggressive tone!"
- `NPC_TINK_TINK_TINA2_8`: "[m:shocked]I was all... WTF!"
- `NPC_TINK_TINK_TINA2_9`: "[m:sad]I tried to show him the pics and he just ignored me and kept honking his horn along with like 7 other people!"
- `NPC_TINK_TINK_TINA2_10`: "[m:angry]What the hell is wrong with everyone these days!?"
- `NPC_TINK_TINK_TERMINATOR_1`: "[m:paranoid]So I don't wanna like freak you out or whatever..."
- `NPC_TINK_TINK_TERMINATOR_2`: "But this big nude cat with multiple guns and an Austrian accent came by my place last night."
- `NPC_TINK_TINK_TERMINATOR_3`: "[m:pondering]He said he was looking for you, something about murder."
- `NPC_TINK_TINK_TERMINATOR_4`: "[m:questioning]Something something, terminate?"
- `NPC_TINK_TINK_TERMINATOR_5`: "[m:shocked]Then he just started pop locking.  Like busting out the robot right there in front of me."
- `NPC_TINK_TINK_TERMINATOR_6`: "[m:happy]I had my wife turn on some James Brown and that man broke it down!"
- `NPC_TINK_TINK_TERMINATOR_7`: "[m:default]We danced 'till dawn and he just kinda wandered off."
- `NPC_TINK_TINK_TERMINATOR_8`: "[m:questioning]He said something about "being back", so if I were you I'd split town."
- `NPC_TINK_TINK_TERMINATOR_9`: "[m:default]You could start a new life somewhere! I got some extra wigs if you need them."
- `NPC_TINK_TINK_TERMINATOR_10`: "[m:happy]If I ever split this poop hole, I'd call myself Ms. Tinkle Toes!"
- `NPC_TINK_TINK_TERMINATOR_11`: "[m:mocking]Just another tall drink of water trying to make it in a man's world!"
- `NPC_TINK_TINK_TERMINATOR_12`: "[m:veryhappy]Homemaker by day, street walker by night!"
- `NPC_TINK_TINK_TERMINATOR_13`: "[m:happy]My double life would have so many twists and turns, your nipples would turn purple..."
- `NPC_TINK_TINK_TERMINATOR_14`: "[m:sad]... sigh ..."
- `NPC_TINK_TINK_TERMINATOR_15`: "One day..."

```
sequences {
	
	unprompted {
		dialog NPC_TINK_UNPROMPTED_1
	}

	unknown {
		dialog NPC_TINK_UNKNOWN_1
		get npc_reward
	}

	also {
		dialog NPC_TINK_ALSO_1
	}

	
	tink_begin_accepting_cats {
		set_state closeup
		dialog NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_1
		set_state idle
		dialog NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_2
		set_state verycloseup
		dialog NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_3
		set_state closeup
		dialog NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_4
		set_state verycloseup
		dialog NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_5
		dialog NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_6
		set_state closeup
		dialog NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_7
		set_state idle
		dialog NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_8
		dialog NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_9
		dialog NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_10
		set_state closeup
		dialog NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_11
		dialog NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_12
		set_state verycloseup
		dialog NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_13
		dialog NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_14
		set_state idle
		dialog NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_15	
		dialog NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_16
		set_state closeup
		dialog NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_17	
		set_state idle
		dialog NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_18
		dialog NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_19	
		dialog NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_20
		dialog NPC_TINK_TINK_BEGIN_ACCEPTING_CATS_21		

		begin_accepting_cats tink
	}


	tink_prettybow {
		set_state closeup
		dialog NPC_TINK_TINK_PRETTYBOW_1
		dialog NPC_TINK_TINK_PRETTYBOW_2
		set_state idle
		dialog NPC_TINK_TINK_PRETTYBOW_3
		dialog NPC_TINK_TINK_PRETTYBOW_4
		get npc_reward
		set_state closeup
		dialog NPC_TINK_TINK_PRETTYBOW_5
		dialog NPC_TINK_TINK_PRETTYBOW_6
		dialog NPC_TINK_TINK_PRETTYBOW_7
		set_state zoomedout
		dialog NPC_TINK_TINK_PRETTYBOW_8
		dialog NPC_TINK_TINK_PRETTYBOW_9
		set_state idle
		dialog NPC_TINK_TINK_PRETTYBOW_10
	}

	tink_tags {//5
		dialog NPC_TINK_TINK_TAGS_1
		set_state closeup
		dialog NPC_TINK_TINK_TAGS_2
		dialog NPC_TINK_TINK_TAGS_3
		dialog NPC_TINK_TINK_TAGS_4
		dialog NPC_TINK_TINK_TAGS_5
		dialog NPC_TINK_TINK_TAGS_6
		set_state verycloseup
		dialog NPC_TINK_TINK_TAGS_7
		dialog NPC_TINK_TINK_TAGS_8
		set_state closeup
		dialog NPC_TINK_TINK_TAGS_9
		get npc_reward
	}

	tink_basestats {//1
		set_state verycloseup
		dialog NPC_TINK_TINK_BASESTATS_1
		set_state closeup
		dialog NPC_TINK_TINK_BASESTATS_2
		dialog NPC_TINK_TINK_BASESTATS_3
		set_state idle
		dialog NPC_TINK_TINK_BASESTATS_4
		dialog NPC_TINK_TINK_BASESTATS_5
		dialog NPC_TINK_TINK_BASESTATS_6
		dialog NPC_TINK_TINK_BASESTATS_7
		dialog NPC_TINK_TINK_BASESTATS_8
		set_state closeup
		dialog NPC_TINK_TINK_BASESTATS_9
		dialog NPC_TINK_TINK_BASESTATS_10
		set_state verycloseup
		dialog NPC_TINK_TINK_BASESTATS_11
		get npc_reward
	}

	tink_inbreeding {//2
		set_state closeup
		dialog NPC_TINK_TINK_INBREEDING_1
		set_state idle
		dialog NPC_TINK_TINK_INBREEDING_2
		dialog NPC_TINK_TINK_INBREEDING_3
		dialog NPC_TINK_TINK_INBREEDING_4
		dialog NPC_TINK_TINK_INBREEDING_5
		set_state closeup
		dialog NPC_TINK_TINK_INBREEDING_6
		set_state idle
		dialog NPC_TINK_TINK_INBREEDING_7
		dialog NPC_TINK_TINK_INBREEDING_8
		set_state closeup
		dialog NPC_TINK_TINK_INBREEDING_9
		set_state verycloseup
		dialog NPC_TINK_TINK_INBREEDING_10
		set_state idle
		dialog NPC_TINK_TINK_INBREEDING_11
		dialog NPC_TINK_TINK_INBREEDING_12
		dialog NPC_TINK_TINK_INBREEDING_13
		get npc_reward
	}

	tink_aggression {//4
		set_state zoomedout
		dialog NPC_TINK_TINK_AGGRESSION_1
		set_state idle
		dialog NPC_TINK_TINK_AGGRESSION_2
		set_state verycloseup
		dialog NPC_TINK_TINK_AGGRESSION_3
		set_state closeup
		dialog NPC_TINK_TINK_AGGRESSION_4 
		set_state idle
		dialog NPC_TINK_TINK_AGGRESSION_5
		dialog NPC_TINK_TINK_AGGRESSION_6
		set_state closeup
		dialog NPC_TINK_TINK_AGGRESSION_7
		set_state idle
		dialog NPC_TINK_TINK_AGGRESSION_8
		set_state closeup
		dialog NPC_TINK_TINK_AGGRESSION_9
		set_state idle
		dialog NPC_TINK_TINK_AGGRESSION_10
		set_state zoomedout
		dialog NPC_TINK_TINK_AGGRESSION_11
		set_state closeup
		dialog NPC_TINK_TINK_AGGRESSION_12
		get npc_reward
	}
	
	tink_sexuality {//3
		dialog NPC_TINK_TINK_SEXUALITY_1
		dialog NPC_TINK_TINK_SEXUALITY_2
		set_state closeup
		dialog NPC_TINK_TINK_SEXUALITY_3
		set_state idle
		dialog NPC_TINK_TINK_SEXUALITY_4
		set_state closeup
		dialog NPC_TINK_TINK_SEXUALITY_5
		dialog NPC_TINK_TINK_SEXUALITY_6
		dialog NPC_TINK_TINK_SEXUALITY_7
		set_state idle
		dialog NPC_TINK_TINK_SEXUALITY_8
		set_state verycloseup
		dialog NPC_TINK_TINK_SEXUALITY_9
		set_state idle
		dialog NPC_TINK_TINK_SEXUALITY_10
		dialog NPC_TINK_TINK_SEXUALITY_11
		dialog NPC_TINK_TINK_SEXUALITY_12
		get npc_reward
	}

	tink_relationships {//6
		set_state verycloseup
		dialog NPC_TINK_TINK_RELATIONSHIPS_1
		set_state closeup
		dialog NPC_TINK_TINK_RELATIONSHIPS_2
		set_state idle
		dialog NPC_TINK_TINK_RELATIONSHIPS_3
		dialog NPC_TINK_TINK_RELATIONSHIPS_4
		dialog NPC_TINK_TINK_RELATIONSHIPS_5
		set_state zoomedout
		dialog NPC_TINK_TINK_RELATIONSHIPS_6
		set_state closeup
		dialog NPC_TINK_TINK_RELATIONSHIPS_7
		set_state idle
		dialog NPC_TINK_TINK_RELATIONSHIPS_8
		set_state verycloseup
		dialog NPC_TINK_TINK_RELATIONSHIPS_9
		dialog NPC_TINK_TINK_RELATIONSHIPS_10
		set_state idle
		dialog NPC_TINK_TINK_RELATIONSHIPS_11
		dialog NPC_TINK_TINK_RELATIONSHIPS_12
		set_state verycloseup
		dialog NPC_TINK_TINK_RELATIONSHIPS_13
		set_state idle
		dialog NPC_TINK_TINK_RELATIONSHIPS_14
		dialog NPC_TINK_TINK_RELATIONSHIPS_15
		dialog NPC_TINK_TINK_RELATIONSHIPS_16
		set_state verycloseup
		dialog NPC_TINK_TINK_RELATIONSHIPS_17
		set_state closeup
		dialog NPC_TINK_TINK_RELATIONSHIPS_18
		set_state idle
		dialog NPC_TINK_TINK_RELATIONSHIPS_19
		dialog NPC_TINK_TINK_RELATIONSHIPS_20
		get npc_reward
	}
	
	tink_max_intro {//used for when tink hits max favor.
		dialog NPC_TINK_TINK_MAX_INTRO_1
		set_state closeup
		dialog NPC_TINK_TINK_MAX_INTRO_2
		set_state verycloseup
		dialog NPC_TINK_TINK_MAX_INTRO_3
		set_state closeup
		dialog NPC_TINK_TINK_MAX_INTRO_4
		dialog NPC_TINK_TINK_MAX_INTRO_5
		dialog NPC_TINK_TINK_MAX_INTRO_6
		set_state zoomedout
		dialog NPC_TINK_TINK_MAX_INTRO_7
		set_state closeup
		dialog NPC_TINK_TINK_MAX_INTRO_8
		dialog NPC_TINK_TINK_MAX_INTRO_9
		dialog NPC_TINK_TINK_MAX_INTRO_10
		dialog NPC_TINK_TINK_MAX_INTRO_11
		dialog NPC_TINK_TINK_MAX_INTRO_12
		get npc_reward
	}

	tink_max_repeating {
		do_random_sequence [tink_max1, tink_max2, tink_max3, tink_max4, tink_max5, tink_max6, tink_max7, tink_max8, tink_max9, tink_max10]
	}

	tink_max1 {//max1-10 are for when tink is at max favor
		set_state closeup
		dialog NPC_TINK_TINK_MAX1_1
		dialog NPC_TINK_TINK_MAX1_2
		dialog NPC_TINK_TINK_MAX1_3
		set_state verycloseup
		dialog NPC_TINK_TINK_MAX1_4
		get npc_reward
	}
	
	tink_max2 {
		dialog NPC_TINK_TINK_MAX2_1
		dialog NPC_TINK_TINK_MAX2_2
		set_state closeup
		dialog NPC_TINK_TINK_MAX2_3
		dialog NPC_TINK_TINK_MAX2_4
		dialog NPC_TINK_TINK_MAX2_5
		set_state idle
		dialog NPC_TINK_TINK_MAX2_6
		dialog NPC_TINK_TINK_MAX2_7
		get npc_reward
	}
	
	tink_max3 {
		dialog NPC_TINK_TINK_MAX3_1
		set_state verycloseup
		dialog NPC_TINK_TINK_MAX3_2
		set_state idle
		dialog NPC_TINK_TINK_MAX3_3
		set_state closeup
		dialog NPC_TINK_TINK_MAX3_4
		set_state verycloseup
		dialog NPC_TINK_TINK_MAX3_5
		set_state idle
		dialog NPC_TINK_TINK_MAX3_6
		get npc_reward
	}
	
	tink_max4 {
		dialog NPC_TINK_TINK_MAX4_1
		dialog NPC_TINK_TINK_MAX4_2
		set_state closeup
		dialog NPC_TINK_TINK_MAX4_3
		dialog NPC_TINK_TINK_MAX4_4
		set_state idle
		dialog NPC_TINK_TINK_MAX4_5
		set_state closeup
		dialog NPC_TINK_TINK_MAX4_6
		set_state verycloseup
		dialog NPC_TINK_TINK_MAX4_7
		set_state closeup
		dialog NPC_TINK_TINK_MAX4_8
		dialog NPC_TINK_TINK_MAX4_9
		dialog NPC_TINK_TINK_MAX4_10
		get npc_reward
	}
	
	tink_max5 {
		dialog NPC_TINK_TINK_MAX5_1
		dialog NPC_TINK_TINK_MAX5_2
		set_state closeup
		dialog NPC_TINK_TINK_MAX5_3
		set_state idle
		dialog NPC_TINK_TINK_MAX5_4

		get npc_reward
	}

	tink_max6 {
		dialog NPC_TINK_TINK_MAX6_1
		dialog NPC_TINK_TINK_MAX6_2
		dialog NPC_TINK_TINK_MAX6_3
		dialog NPC_TINK_TINK_MAX6_4
		dialog NPC_TINK_TINK_MAX6_5
		get npc_reward
	}
	
	tink_max7 {
		dialog NPC_TINK_TINK_MAX7_1
		dialog NPC_TINK_TINK_MAX7_2
		set_state closeup
		dialog NPC_TINK_TINK_MAX7_3
		dialog NPC_TINK_TINK_MAX7_4
		dialog NPC_TINK_TINK_MAX7_5
		dialog NPC_TINK_TINK_MAX7_6
		get npc_reward
	}
	
	tink_max8 {
		set_state closeup
		dialog NPC_TINK_TINK_MAX8_1
		dialog NPC_TINK_TINK_MAX8_2
		dialog NPC_TINK_TINK_MAX8_3
		set_state idle
		dialog NPC_TINK_TINK_MAX8_4
		get npc_reward
	}
	
	tink_max9 {
		set_state verycloseup
		dialog NPC_TINK_TINK_MAX9_1
		set_state closeup
		dialog NPC_TINK_TINK_MAX9_2
		dialog NPC_TINK_TINK_MAX9_3
		set_state idle
		dialog NPC_TINK_TINK_MAX9_4
		dialog NPC_TINK_TINK_MAX9_5
		get npc_reward
	}
	
	tink_max10 {
		set_state closeup
		dialog NPC_TINK_TINK_MAX10_1
		set_state idle
		dialog NPC_TINK_TINK_MAX10_2
		dialog NPC_TINK_TINK_MAX10_3
		dialog NPC_TINK_TINK_MAX10_4
		dialog NPC_TINK_TINK_MAX10_5
		set_state closeup
		dialog NPC_TINK_TINK_MAX10_6
		dialog NPC_TINK_TINK_MAX10_7
		set_state verycloseup
		dialog NPC_TINK_TINK_MAX10_8
		dialog NPC_TINK_TINK_MAX10_9
		get npc_reward
	}
	
	//Tink Tips
	
	unprompted {
		do_random_sequence [unprompted_a, unprompted_b, unprompted_c, unprompted_d, unprompted_e, unprompted_f, unprompted_g, unprompted_h, unprompted_i]
	}
	
	unprompted_a {
		dialog NPC_TINK_UNPROMPTED_A_1
		dialog NPC_TINK_UNPROMPTED_A_2
		do_sequence forward_to_tips	
	}
	unprompted_b {
		dialog NPC_TINK_UNPROMPTED_B_1
		dialog NPC_TINK_UNPROMPTED_B_2
		do_sequence forward_to_tips	
	}
	unprompted_c {
		dialog NPC_TINK_UNPROMPTED_C_1
		do_sequence forward_to_tips
	}
	unprompted_d {
		dialog NPC_TINK_UNPROMPTED_D_1
		do_sequence forward_to_tips	
	}
	unprompted_e {
		dialog NPC_TINK_UNPROMPTED_E_1
		do_sequence forward_to_tips	
	}
	unprompted_f {
		dialog NPC_TINK_UNPROMPTED_F_1
		dialog NPC_TINK_UNPROMPTED_F_2
		do_sequence forward_to_tips	
	}
	unprompted_g {
		dialog NPC_TINK_UNPROMPTED_G_1
		dialog NPC_TINK_UNPROMPTED_G_2
		do_sequence forward_to_tips	
	}
	unprompted_h {
		dialog NPC_TINK_UNPROMPTED_H_1
		dialog NPC_TINK_UNPROMPTED_H_2
		do_sequence forward_to_tips	
	}
	unprompted_i {
		dialog NPC_TINK_UNPROMPTED_I_1
		do_sequence forward_to_tips	
	}
	
	
	forward_to_tips {
		do_random_sequence [tink_tips_comfort, tink_tips_stimulation, tink_tips_stimulation, tink_tips_appeal , tink_tips_health, tink_tips_mutation,
		tink_tips_cleaning, tink_tips_basestats, tink_tips_multiclassing, tink_tips_inbreeding ]
	}
	
	
	tink_tips_intro {
		dialog NPC_TINK_TINK_TIPS_INTRO_1
		dialog NPC_TINK_TINK_TIPS_INTRO_2
		dialog NPC_TINK_TINK_TIPS_INTRO_3
		dialog NPC_TINK_TINK_TIPS_INTRO_4
		do_sequence tink_tips_comfort
	}
	tink_tips_comfort {
		dialog NPC_TINK_TINK_TIPS_COMFORT_1
		dialog NPC_TINK_TINK_TIPS_COMFORT_2
		dialog NPC_TINK_TINK_TIPS_COMFORT_3
		dialog NPC_TINK_TINK_TIPS_COMFORT_4
	}
	tink_tips_stimulation {
		dialog NPC_TINK_TINK_TIPS_STIMULATION_1
		dialog NPC_TINK_TINK_TIPS_STIMULATION_2
		dialog NPC_TINK_TINK_TIPS_STIMULATION_3
		dialog NPC_TINK_TINK_TIPS_STIMULATION_4
		dialog NPC_TINK_TINK_TIPS_STIMULATION_5
		dialog NPC_TINK_TINK_TIPS_STIMULATION_6
		dialog NPC_TINK_TINK_TIPS_STIMULATION_7
	}
	tink_tips_appeal {
		dialog NPC_TINK_TINK_TIPS_APPEAL_1
		dialog NPC_TINK_TINK_TIPS_APPEAL_2
		dialog NPC_TINK_TINK_TIPS_APPEAL_3
		dialog NPC_TINK_TINK_TIPS_APPEAL_4
	}
	tink_tips_health {
		dialog NPC_TINK_TINK_TIPS_HEALTH_1
		dialog NPC_TINK_TINK_TIPS_HEALTH_2
		dialog NPC_TINK_TINK_TIPS_HEALTH_3
		dialog NPC_TINK_TINK_TIPS_HEALTH_4
		dialog NPC_TINK_TINK_TIPS_HEALTH_5
	}
	tink_tips_mutation {
		dialog NPC_TINK_TINK_TIPS_MUTATION_1
		dialog NPC_TINK_TINK_TIPS_MUTATION_2
		dialog NPC_TINK_TINK_TIPS_MUTATION_3
		dialog NPC_TINK_TINK_TIPS_MUTATION_4
	}
	tink_tips_cleaning {
		dialog NPC_TINK_TINK_TIPS_CLEANING_1
		dialog NPC_TINK_TINK_TIPS_CLEANING_2
		dialog NPC_TINK_TINK_TIPS_CLEANING_3
		dialog NPC_TINK_TINK_TIPS_CLEANING_4
	}
	tink_tips_basestats {
		dialog NPC_TINK_TINK_TIPS_BASESTATS_1
		dialog NPC_TINK_TINK_TIPS_BASESTATS_2
		dialog NPC_TINK_TINK_TIPS_BASESTATS_3
	}
	tink_tips_multiclassing {
		dialog NPC_TINK_TINK_TIPS_MULTICLASSING_1
		dialog NPC_TINK_TINK_TIPS_MULTICLASSING_2
		dialog NPC_TINK_TINK_TIPS_MULTICLASSING_3
		dialog NPC_TINK_TINK_TIPS_MULTICLASSING_4
		dialog NPC_TINK_TINK_TIPS_MULTICLASSING_5
	}
	tink_tips_inbreeding {
		dialog NPC_TINK_TINK_TIPS_INBREEDING_1
		dialog NPC_TINK_TINK_TIPS_INBREEDING_2
		dialog NPC_TINK_TINK_TIPS_INBREEDING_3
		dialog NPC_TINK_TINK_TIPS_INBREEDING_4
		dialog NPC_TINK_TINK_TIPS_INBREEDING_5
	}
	
	//Tina 2 intro
	tink_tina2 {
		dialog NPC_TINK_TINK_TINA2_1
		dialog NPC_TINK_TINK_TINA2_2
		dialog NPC_TINK_TINK_TINA2_3
		dialog NPC_TINK_TINK_TINA2_4
		set_state closeup
		dialog NPC_TINK_TINK_TINA2_5
		dialog NPC_TINK_TINK_TINA2_6
		dialog NPC_TINK_TINK_TINA2_7
		dialog NPC_TINK_TINK_TINA2_8
		set_state idle
		dialog NPC_TINK_TINK_TINA2_9
		dialog NPC_TINK_TINK_TINA2_10

	}
	
	tink_terminator {
		set_state closeup
		dialog NPC_TINK_TINK_TERMINATOR_1
		dialog NPC_TINK_TINK_TERMINATOR_2
		dialog NPC_TINK_TINK_TERMINATOR_3
		dialog NPC_TINK_TINK_TERMINATOR_4
		set_state idle
		dialog NPC_TINK_TINK_TERMINATOR_5
		dialog NPC_TINK_TINK_TERMINATOR_6
		dialog NPC_TINK_TINK_TERMINATOR_7
		dialog NPC_TINK_TINK_TERMINATOR_8
		dialog NPC_TINK_TINK_TERMINATOR_9
		set_state closeup
		dialog NPC_TINK_TINK_TERMINATOR_10
		dialog NPC_TINK_TINK_TERMINATOR_11
		dialog NPC_TINK_TINK_TERMINATOR_12
		dialog NPC_TINK_TINK_TERMINATOR_13
		set_state idle
		dialog NPC_TINK_TINK_TERMINATOR_14
		set_state zoomedout
		dialog NPC_TINK_TINK_TERMINATOR_15

	}
	
}
```

---

## File: `tracy_adventure_shop_script.gon`

### `states_and_transitions`
**Source:** `tracy_adventure_shop_script.gon`  

```
states_and_transitions {
	states {
		idle ["idle"]
	}

	transitions {
	}
}
```

---

### `sequences`
**Source:** `tracy_adventure_shop_script.gon`  

**Localization Strings:**
- `NPC_TRACY_SHOP_WELCOME_1`: "[m:default]Hey, looking to buy something?"
- `NPC_TRACY_SHOP_WELCOME_2`: "Just make it snappy, I gotta get back to P Mart soon..."
- `NPC_TRACY_SHOP_WELCOME_WATER_1`: "[m:winking]Thirsty? Desperate? I got some water still, but it's gonna cost you..."
- `NPC_TRACY_SHOP_WELCOME_WATER_CHEAP_1`: "[m:happy]Pretty hot out there ain't it? <br/> Well I got just the thing..."
- `NPC_TRACY_SHOP_WELCOME_SEWERS_1`: "What's that smell?... Oh it's you."
- `NPC_TRACY_SHOP_WELCOME_SEWERS_2`: "You gonna buy something or what?"
- `NPC_TRACY_SHOP_WELCOME_JUNKYARD_1`: "I hear you like junk? Well boy are you are in luck!"
- `NPC_TRACY_SHOP_WELCOME_CAVES_1`: "Oh it's you again, hard to see down here..."
- `NPC_TRACY_SHOP_WELCOME_CAVES_2`: "Wanna buy something? All proceeds go to exploited animals."
- `NPC_TRACY_SHOP_WELCOME_BONEYARD_1`: "Why are you here!?"
- `NPC_TRACY_SHOP_WELCOME_BONEYARD_2`: "Ugh, whatever.. buy something will ya?"
- `NPC_TRACY_SHOP_WELCOME_DESERT_1`: "Hot enough for ya? Heh heh heh..."
- `NPC_TRACY_SHOP_WELCOME_CRATER_1`: "What odd weather we are having..."
- `NPC_TRACY_SHOP_WELCOME_CRATER_2`: "THANKS CAPITALISM!"
- `NPC_TRACY_SHOP_WELCOME_BUNKER_1`: "Wow there sure are a lot of neurodivergent individuals down here..."
- `NPC_TRACY_SHOP_WELCOME_BUNKER_2`: "Not like thats a bad thing, just making an observation! Don't get me wrong..."
- `NPC_TRACY_SHOP_WELCOME_BUNKER_3`: "In fact, I offer them all discounts! Anyway, you wanna buy something?"
- `NPC_TRACY_SHOP_WELCOME_MOON_1`: "..."
- `NPC_TRACY_SHOP_WELCOME_CORE_1`: "I had a feeling I'd catch you down here..."
- `NPC_TRACY_SHOP_WELCOME_LAB_1`: "[m:angry]Are you seeing all this!? HORRIFIC!"
- `NPC_TRACY_SHOP_WELCOME_LAB_2`: "Anyway, you gonna buy something or what?"
- `NPC_TRACY_SHOP_WELCOME_ICEAGE_1`: "Unga bunga!?"
- `NPC_TRACY_SHOP_WELCOME_ICEAGE_2`: "Toog Gunta?"
- `NPC_TRACY_SHOP_WELCOME_FUTURE_1`: "[m:happy]Purchase, consume and be happy! <br/> *Beep Boop*"
- `NPC_TRACY_SHOP_WELCOME_JURASSIC_1`: "Uuugggg oof unga!"
- `NPC_TRACY_SHOP_WELCOME_JURASSIC_2`: "Ga ga foof!?"
- `NPC_TRACY_SHOP_WELCOME_THEEND_1`: "Oh my God! A friend!?"
- `NPC_TRACY_SHOP_WELCOME_THEEND_2`: "Wanna buy some of my stuff!?"
- `NPC_TRACY_SHOP_PURCHASE_ITEM_A_1`: "[m:bored]Thanks I guess..."
- `NPC_TRACY_SHOP_PURCHASE_ITEM_B_1`: "[m:bored]Wow, what a consumer you are!"
- `NPC_TRACY_SHOP_PURCHASE_ITEM_C_1`: "[m:bored]Great..."
- `NPC_TRACY_SHOP_PURCHASE_ITEM_D_1`: "[m:bored]Yeah, whatever..."
- `NPC_TRACY_SHOP_CANT_AFFORD_A_1`: "[m:angry]You don't have enough money..."
- `NPC_TRACY_SHOP_CANT_AFFORD_B_1`: "[m:angry]You can't buy that!"
- `NPC_TRACY_SHOP_CANT_AFFORD_C_1`: "[m:angry]Nope, not enough cash..."
- `NPC_TRACY_SHOP_CANT_AFFORD_D_1`: "[m:angry]Go make more money!"
- `NPC_TRACY_SHOP_PURCHASE_ITEM_MOON_1`: "..."
- `NPC_TRACY_SHOP_CANT_AFFORD_MOON_1`: "[m:angry]!"
- `NPC_TRACY_SHOP_PURCHASE_ITEM_ICEAGE_1`: "Ogga!"
- `NPC_TRACY_SHOP_CANT_AFFORD_ICEAGE_1`: "[m:angry]NU BOOGA!"
- `NPC_TRACY_SHOP_PURCHASE_ITEM_JURASSIC_1`: "Guf"
- `NPC_TRACY_SHOP_CANT_AFFORD_JURASSIC_1`: "[m:angry]UG!"
- `NPC_TRACY_SHOP_PURCHASE_ITEM_THEEND_1`: "[m:happy]Nice purchase, buddy!"
- `NPC_TRACY_SHOP_CANT_AFFORD_THEEND_1`: "Aw, I'd let you borrow some cash, but I'm all out myself..."
- `NPC_TRACY_SHOP_TOOLTIP`: "{name}. <br/> {desc}"

```
sequences {
	welcome {
		cancelable true
		delay .5
		dialog NPC_TRACY_SHOP_WELCOME_1
		dialog_and_autopass NPC_TRACY_SHOP_WELCOME_2
		wait_for_cancel 1
	}
	welcome_water {
		cancelable true
		delay .5
		dialog_and_autopass NPC_TRACY_SHOP_WELCOME_WATER_1
		wait_for_cancel 1
	}
	welcome_water_cheap {
		cancelable true
		delay .5
		dialog_and_autopass NPC_TRACY_SHOP_WELCOME_WATER_CHEAP_1
		wait_for_cancel 1
	}

	//alternatie chapter-specific welcome messages (optional)
	welcome_sewers {
		cancelable true
		delay .5
		dialog NPC_TRACY_SHOP_WELCOME_SEWERS_1
		dialog_and_autopass NPC_TRACY_SHOP_WELCOME_SEWERS_2
		wait_for_cancel 1
	}
	welcome_junkyard {
		cancelable true
		delay .5
		dialog_and_autopass NPC_TRACY_SHOP_WELCOME_JUNKYARD_1
		wait_for_cancel 1
	}
	welcome_caves {
		cancelable true
		delay .5
		dialog NPC_TRACY_SHOP_WELCOME_CAVES_1
		dialog_and_autopass NPC_TRACY_SHOP_WELCOME_CAVES_2
		wait_for_cancel 1
	}
	welcome_boneyard {
		cancelable true
		delay .5
		dialog NPC_TRACY_SHOP_WELCOME_BONEYARD_1
		dialog_and_autopass NPC_TRACY_SHOP_WELCOME_BONEYARD_2
		wait_for_cancel 1
	}
	welcome_desert {
		cancelable true
		delay .5
		dialog_and_autopass NPC_TRACY_SHOP_WELCOME_DESERT_1
		wait_for_cancel 1
	}
	welcome_crater {
		cancelable true
		delay .5
		dialog NPC_TRACY_SHOP_WELCOME_CRATER_1
		dialog_and_autopass NPC_TRACY_SHOP_WELCOME_CRATER_2
		wait_for_cancel 1
	}
	welcome_bunker {
		cancelable true
		delay .5
		dialog NPC_TRACY_SHOP_WELCOME_BUNKER_1
		dialog NPC_TRACY_SHOP_WELCOME_BUNKER_2
		dialog_and_autopass NPC_TRACY_SHOP_WELCOME_BUNKER_3
		wait_for_cancel 1
	}
	welcome_moon {
		cancelable true
		delay .5
		dialog_and_autopass NPC_TRACY_SHOP_WELCOME_MOON_1
		wait_for_cancel 1
	}
	welcome_core {
		cancelable true
		delay .5
		dialog_and_autopass NPC_TRACY_SHOP_WELCOME_CORE_1
		wait_for_cancel 1
	}
	welcome_lab {
		cancelable true
		delay .5
		dialog NPC_TRACY_SHOP_WELCOME_LAB_1
		dialog_and_autopass NPC_TRACY_SHOP_WELCOME_LAB_2
		wait_for_cancel 1
	}
	welcome_iceage {
		cancelable true
		delay .5
		dialog NPC_TRACY_SHOP_WELCOME_ICEAGE_1
		dialog_and_autopass NPC_TRACY_SHOP_WELCOME_ICEAGE_2
		wait_for_cancel 1
	}
	welcome_future {
		cancelable true
		delay .5
		dialog_and_autopass NPC_TRACY_SHOP_WELCOME_FUTURE_1
		wait_for_cancel 1
	}
	welcome_jurassic {
		cancelable true
		delay .5
		dialog NPC_TRACY_SHOP_WELCOME_JURASSIC_1
		dialog_and_autopass NPC_TRACY_SHOP_WELCOME_JURASSIC_2
		wait_for_cancel 1
	}
	welcome_theend {
		set_npc_voice beanies
		cancelable true
		delay .5
		dialog NPC_TRACY_SHOP_WELCOME_THEEND_1
		dialog_and_autopass NPC_TRACY_SHOP_WELCOME_THEEND_2
		wait_for_cancel 1
	}

	/*
	welcome_debug
	welcome_tutorial
	welcome_alley
	welcome_sewers
	welcome_junkyard
	welcome_caves
	welcome_boneyard
	welcome_meatworld
	welcome_desert
	welcome_crater
	welcome_bunker
	welcome_moon
	welcome_core
	welcome_dimensionx
	welcome_lab
	welcome_iceage
	welcome_future
	welcome_jurassic
	welcome_theend
	welcome_endoftime
	*/


	purchase_item {
		do_random_sequence [purchase_item_a, purchase_item_b, purchase_item_c, purchase_item_d]
	}
	purchase_item_a {
		cancelable true
		dialog_and_autopass NPC_TRACY_SHOP_PURCHASE_ITEM_A_1
		wait_for_cancel 1
	}
	
	purchase_item_b {
		cancelable true
		dialog_and_autopass NPC_TRACY_SHOP_PURCHASE_ITEM_B_1
		wait_for_cancel 1
	}
	
	purchase_item_c {
		cancelable true
		dialog_and_autopass NPC_TRACY_SHOP_PURCHASE_ITEM_C_1
		wait_for_cancel 1
	}
	
	purchase_item_d {
		cancelable true
		dialog_and_autopass NPC_TRACY_SHOP_PURCHASE_ITEM_D_1
		wait_for_cancel 1
	}
	
	
	
	cant_afford {
		do_random_sequence [cant_afford_a, cant_afford_b, cant_afford_c, cant_afford_d]
	}
	
	cant_afford_a {
		cancelable true
		dialog_and_autopass NPC_TRACY_SHOP_CANT_AFFORD_A_1
		wait_for_cancel 1
	}
	
	cant_afford_b {
		cancelable true
		dialog_and_autopass NPC_TRACY_SHOP_CANT_AFFORD_B_1
		wait_for_cancel 1
	}
	
	cant_afford_c {
		cancelable true
		dialog_and_autopass NPC_TRACY_SHOP_CANT_AFFORD_C_1
		wait_for_cancel 1
	}
	
	cant_afford_d {
		cancelable true
		dialog_and_autopass NPC_TRACY_SHOP_CANT_AFFORD_D_1
		wait_for_cancel 1
	}

	
	
	
	purchase_item_moon {
		cancelable true
		dialog_and_autopass NPC_TRACY_SHOP_PURCHASE_ITEM_MOON_1
		wait_for_cancel 1
	}
	cant_afford_moon {
		cancelable true
		dialog_and_autopass NPC_TRACY_SHOP_CANT_AFFORD_MOON_1
		wait_for_cancel 1
	}
	
	purchase_item_iceage {
		cancelable true
		dialog_and_autopass NPC_TRACY_SHOP_PURCHASE_ITEM_ICEAGE_1
		wait_for_cancel 1
	}
	cant_afford_iceage {
		cancelable true
		dialog_and_autopass NPC_TRACY_SHOP_CANT_AFFORD_ICEAGE_1
		wait_for_cancel 1
	}
	
	purchase_item_jurassic {
		cancelable true
		dialog_and_autopass NPC_TRACY_SHOP_PURCHASE_ITEM_JURASSIC_1
		wait_for_cancel 1
	}
	cant_afford_jurassic {
		cancelable true
		dialog_and_autopass NPC_TRACY_SHOP_CANT_AFFORD_JURASSIC_1
		wait_for_cancel 1
	}
	
	purchase_item_theend {
		cancelable true
		dialog_and_autopass NPC_TRACY_SHOP_PURCHASE_ITEM_THEEND_1
		wait_for_cancel 1
	}
	cant_afford_theend {
		cancelable true
		dialog_and_autopass NPC_TRACY_SHOP_CANT_AFFORD_THEEND_1
		wait_for_cancel 1
	}

	/*
	purchase_item_debug
	purchase_item_tutorial
	purchase_item_alley
	purchase_item_sewers
	purchase_item_junkyard
	purchase_item_caves
	purchase_item_boneyard
	purchase_item_meatworld
	purchase_item_desert
	purchase_item_crater
	purchase_item_bunker
	purchase_item_moon
	purchase_item_core
	purchase_item_dimensionx
	purchase_item_lab
	purchase_item_iceage
	purchase_item_future
	purchase_item_jurassic
	purchase_item_theend
	purchase_item_endoftime
	*/

	/*
	cant_afford_debug
	cant_afford_tutorial
	cant_afford_alley
	cant_afford_sewers
	cant_afford_junkyard
	cant_afford_caves
	cant_afford_boneyard
	cant_afford_meatworld
	cant_afford_desert
	cant_afford_crater
	cant_afford_bunker
	cant_afford_moon
	cant_afford_core
	cant_afford_dimensionx
	cant_afford_lab
	cant_afford_iceage
	cant_afford_future
	cant_afford_jurassic
	cant_afford_theend
	cant_afford_endoftime
	*/

	tooltip {
		cancelable true
		tooltip_dialog NPC_TRACY_SHOP_TOOLTIP
		wait_for_cancel 1
	}
	hide_text {
		cancelable true
		dialog_and_autopass ""
	}
}
```

---

## File: `tracy_progression.gon`

### `states_and_transitions`
**Source:** `tracy_progression.gon`  

```
states_and_transitions {
	states {
		idle ["idle" "blocking"]
	}

	transitions {
	}
}
```

---

### `sequences`
**Source:** `tracy_progression.gon`  

**Localization Strings:**
- `NPC_TRACY_UNPROMPTED_1`: "[m:happy]Welcome to P Mart, <br/> where our love for your pets is never ending..."
- `NPC_TRACY_UNPROMPTED_2`: "Are you in need of pet supplies for your fur babies? [m:default] <br/> ugh..."
- `NPC_TRACY_ALSO_1`: "Also..."
- `NPC_TRACY_TRACY_INTRODUCTION_1`: "[m:bored]Yeah yeah, <br/> I see you."
- `NPC_TRACY_TRACY_INTRODUCTION_2`: "I'm Tracy, <br/> but I honestly don't feel a word can fully represent who I am as a person, so don't bother using it."
- `NPC_TRACY_TRACY_INTRODUCTION_3`: "[m:questioning]So you must think you're some type of pet lover?"
- `NPC_TRACY_TRACY_INTRODUCTION_4`: "[m:default]I assume you identify as a "pet lover" by how you carry yourself?"
- `NPC_TRACY_TRACY_INTRODUCTION_5`: "[m:angry]Well?!"
- `NPC_TRACY_TRACY_INTRODUCTION_6`: "[m:default]Yeah I thought so. <br/> [b]"Pet Lover"[/b] <br/> God, that term is so speciesist."
- `NPC_TRACY_TRACY_INTRODUCTION_7`: "[m:angry]Even hearing the word, "PET"! <br/> It just makes my skin crawl. <br/> I prefer the term, animal companion."
- `NPC_TRACY_TRACY_INTRODUCTION_8`: "[m:pondering]But personally, I go a step beyond loving animals."
- `NPC_TRACY_TRACY_INTRODUCTION_9`: "[m:default]In fact, I believe all animals should have the same rights as us."
- `NPC_TRACY_TRACY_INTRODUCTION_10`: "[m:pondering]If not more!"
- `NPC_TRACY_TRACY_INTRODUCTION_11`: "[m:angry]Even the term [b]pet[/b] showcases the bigoted speciesist agenda that this sick world subscribes to."
- `NPC_TRACY_TRACY_INTRODUCTION_12`: "[m:veryangry]If I had my way, using that word would be punishable by death!"
- `NPC_TRACY_TRACY_INTRODUCTION_13`: "[m:shocked]!"
- `NPC_TRACY_TRACY_INTRODUCTION_14`: "[m:scared]. . ."
- `NPC_TRACY_TRACY_INTRODUCTION_15`: "[m:sad][s:.7]*Goddamn it*[/s]"
- `NPC_TRACY_TRACY_INTRODUCTION_16`: "[m:happy][s:1.2]Hello![/s]"
- `NPC_TRACY_TRACY_INTRODUCTION_17`: "Welcome to P Mart, where our love for your pets is never ending..."
- `NPC_TRACY_TRACY_INTRODUCTION_18`: "[m:sad][s:.7]ugh...[/s]"
- `NPC_TRACY_TRACY_INTRODUCTION_19`: "[m:happy]Our cat donation center stays open 24/7!"
- `NPC_TRACY_TRACY_INTRODUCTION_20`: "Every donation of a cat age 5 or older will go directly to the expansion of this location."
- `NPC_TRACY_TRACY_INTRODUCTION_21`: "P Mart thanks you for your patronage, and have a blessed day."
- `NPC_TRACY_TRACY_INTRODUCTION_22`: "[m:angry][s:.5]I hate you.[/s]"
- `NPC_TRACY_OUT_OF_STOCK_1`: "[m:angry]Does it look like we have any remaining stock? Come on!"
- `NPC_TRACY_PURCHASE_ITEM_1`: "[m:default]Great..."
- `NPC_TRACY_CANT_AFFORD_1`: "[m:happy]No money, huh? Isn't capitalism grand?"
- `NPC_TRACY_SHOP_TOOLTIP`: "{name}. <br/> {desc}"
- `NPC_TRACY_TRACY_FOODBONUS1_1`: "Well I wanted a cat and you gave me a cat, so I feel I should give you something in return. How about 10 free food?"
- `NPC_TRACY_TRACY_FOODBONUS1_2`: "It's not much, but tell you what... If you can bring me more domesticated cats, I'll start stocking some [a:wave]special items[/a] for you."
- `NPC_TRACY_TRACY_BLANKCOLLAR1_1`: "[b][m:happy]P Mart thanks you for your many donations.  Your patronage continues to save lives overseas!"
- `NPC_TRACY_TRACY_BLANKCOLLAR1_2`: "[b]Be sure to come back tomorrow and check out our new members only item![/b]"
- `NPC_TRACY_TRACY_BLANKCOLLAR1_3`: "[m:default]..."
- `NPC_TRACY_TRACY_BLANKCOLLAR1_4`: "It's a blank collar btw."
- `NPC_TRACY_TRACY_BLANKCOLLAR1_5`: "[m:questioning]Don't ask me what it does, but that masked man with the mustache always buys them."
- `NPC_TRACY_TRACY_BLANKCOLLAR1_6`: "[m:angry]So I assume they have value to fellow Nazis like yourself!"
- `NPC_TRACY_TRACY_BLANKCOLLAR1_7`: "[m:sad][s:.7]God, I hate this job...[/s]"
- `NPC_TRACY_TRACY_BLANKCOLLAR1_8`: "[m:happy][b]Thanks for shopping at <br/> P Mart, and have a blessed day![/b]"
- `NPC_TRACY_TRACY_BLANKCOLLAR1_9`: "[m:sad]... ugh ..."
- `NPC_TRACY_TRACY_BLANKCOLLAR2_1`: "[b][m:happy]Once again, P Mart wants to acknowledge its rewards members and their hard work!"
- `NPC_TRACY_TRACY_BLANKCOLLAR2_2`: "[b]With your help, families around the world can fall asleep comfortably knowing P Mart is there for them!"
- `NPC_TRACY_TRACY_BLANKCOLLAR2_3`: "[b]And yes, our blank cat collars are once again back in stock tomorrow! Mark your calendars![/b]"
- `NPC_TRACY_TRACY_BLANKCOLLAR2_4`: "[m:default]. . ."
- `NPC_TRACY_TRACY_BLANKCOLLAR2_5`: "So I've decided to go back to college and major in business."
- `NPC_TRACY_TRACY_BLANKCOLLAR2_6`: "That way I can move up the corporate ladder, get a comfy office in a high rise building..."
- `NPC_TRACY_TRACY_BLANKCOLLAR2_7`: "[m:questioning]Get married, have kids, retire and take a long nap in my car, while it's running."
- `NPC_TRACY_TRACY_BLANKCOLLAR2_8`: "[m:angry]As my kids guzzle red 40 and my husband beats our dog!"
- `NPC_TRACY_TRACY_BLANKCOLLAR2_9`: "[m:veryangry]YEAH RIGHT! <br/> I'D RATHER KILL MYSELF!"
- `NPC_TRACY_TRACY_BLANKCOLLAR2_10`: "[m:angry]. . ."
- `NPC_TRACY_TRACY_BLANKCOLLAR2_11`: "[m:happy][b]Thanks for shopping at <br/> P Mart, and have a blessed day![/b]"
- `NPC_TRACY_TRACY_BLANKCOLLAR3_1`: "[b][m:happy]P Mart has hit yet another milestone, expanding even further, with stores opening in India and Cambodia!"
- `NPC_TRACY_TRACY_BLANKCOLLAR3_2`: "[b]Because of patrons like you, our overseas members rest easy knowing they won't be going to sleep hungry ever again!"
- `NPC_TRACY_TRACY_BLANKCOLLAR3_3`: "[b]P Mart has officially announced [a:wave]Universal Kibble![/a] a dense, nutrient-rich forcemeat that can be consumed by humans and cats alike!"
- `NPC_TRACY_TRACY_BLANKCOLLAR3_4`: "[b]Gone are the days of malnutrition and hunger! <br/> That's right, P Mart Members, the future is now![/b]"
- `NPC_TRACY_TRACY_BLANKCOLLAR3_5`: "[m:default]. . ."
- `NPC_TRACY_TRACY_BLANKCOLLAR3_6`: "[m:angry]I don't know if you read on my blog or whatever, but I'm vegan now."
- `NPC_TRACY_TRACY_BLANKCOLLAR3_7`: "[m:default]. . ."
- `NPC_TRACY_TRACY_IDOL1_1`: "[b][m:happy]P Mart understands that online gossip and misinformation can be confusing."
- `NPC_TRACY_TRACY_IDOL1_2`: "[b]And would like to address some recent issues customers have been having with our <br/> "Scratch scratch" litter products."
- `NPC_TRACY_TRACY_IDOL1_3`: "[b]If you purchased "Scratch scratch" in the last 6 years and suffered a stroke, heart attack, rectal cancer or scabies,"
- `NPC_TRACY_TRACY_IDOL1_4`: "[b]P Mart would like to deliver a deep heartfelt apology.  And to show we care, we offer all patrons 10% off select litter products for the rest of the month![/b]"
- `NPC_TRACY_TRACY_IDOL1_5`: "[m:default]..."
- `NPC_TRACY_TRACY_IDOL1_6`: "[m:whispering]There is a rumor that a very unique item is being stocked tomorrow..."
- `NPC_TRACY_TRACY_IDOL1_7`: "[m:default]In fact, there is a whole line of people camping out front waiting to get their hands on one."
- `NPC_TRACY_TRACY_IDOL1_8`: "Maybe I can set one aside for you if you do me a favor..."
- `NPC_TRACY_TRACY_IDOL1_9`: "[m:whispering][s:.7]Come closer so they can't hear.[/s]"
- `NPC_TRACY_TRACY_IDOL1_10`: "[m:whispering][s:.6]closer...[/s]"
- `NPC_TRACY_TRACY_IDOL1_11`: "[m:whispering][s:.6]Your time will come you son of a bitch![/s]"
- `NPC_TRACY_TRACY_IDOL1_12`: "[m:happy]. . ."
- `NPC_TRACY_TRACY_IDOL1_13`: "[m:happy]Thanks for shopping at P Mart, and have a blessed day!"
- `NPC_TRACY_TRACY_IDOL2_1`: "[m:happy][b]Welcome to P Mart...[/b]"
- `NPC_TRACY_TRACY_IDOL2_2`: "[m:bored]..."
- `NPC_TRACY_TRACY_IDOL2_3`: "[m:default]Listen, we are stocking another one of those idols tomorrow."
- `NPC_TRACY_TRACY_IDOL2_4`: "I dunno what your deal is with those things, but I'll tell you right now..."
- `NPC_TRACY_TRACY_IDOL2_5`: "[m:angry]Some indigenous religion is getting exploited here..."
- `NPC_TRACY_TRACY_IDOL2_6`: "and when I find out what one..."
- `NPC_TRACY_TRACY_IDOL2_7`: "[m:veryangry]I'm gonna make the biggest protest sign you've ever seen!"
- `NPC_TRACY_TRACY_IDOL2_8`: "AND BOY WILL YOUR FACE BE RED!"
- `NPC_TRACY_TRACY_IDOL3_1`: "[m:bored]..."
- `NPC_TRACY_TRACY_IDOL3_2`: "[m:default]They are sending us another idol."
- `NPC_TRACY_TRACY_IDOL3_3`: "It gets here tomorrow..."
- `NPC_TRACY_TRACY_IDOL3_4`: "[m:bored]I'm not sure what the hell you are doing with those things..."
- `NPC_TRACY_TRACY_IDOL3_5`: "[m:angry]But I don't like it!"
- `NPC_TRACY_TRACY_IDOL3_6`: "[m:pondering]Now I don't know what kind of God you worship..."
- `NPC_TRACY_TRACY_IDOL3_7`: "[m:angry]But if it's the one that I don't like, I'm gonna be pissed!"
- `NPC_TRACY_TRACY_IDOL3_8`: "[m:veryangry]AND I THINK WE BOTH KNOW WHAT ONE I'M TALKING ABOUT!"
- `NPC_TRACY_TRACY_IDOL3_9`: "[m:default]..."
- `NPC_TRACY_TRACY_IDOL3_10`: "[m:happy]. . ."
- `NPC_TRACY_TRACY_IDOL3_11`: "[m:happy][b]Thanks for shopping at P Mart, and have a blessed day![/b]"
- `NPC_TRACY_TRACY_IDOL4_1`: "[m:happy][b]Welcome to P Mart. Did you know today we have a sale on...[/b]"
- `NPC_TRACY_TRACY_IDOL4_2`: "[m:bored]..."
- `NPC_TRACY_TRACY_IDOL4_3`: "Another idol is being stocked tomorrow... This is getting a bit creepy."
- `NPC_TRACY_TRACY_IDOL4_4`: "[m:questioning]Why do you keep ordering these things?"
- `NPC_TRACY_TRACY_IDOL4_5`: "[m:default]Don't you remember that episode of that show where the kids found an idol..."
- `NPC_TRACY_TRACY_IDOL4_6`: "And they start experiencing horrible misfortune while it's in their possession!"
- `NPC_TRACY_TRACY_IDOL4_7`: "[m:shocked]Alice injured her back and Greg was in a horrible surfing accident!"
- `NPC_TRACY_TRACY_IDOL4_8`: "[m:mocking]Imagine all the misfortune that will befall you!"
- `NPC_TRACY_TRACY_IDOL4_9`: "[m:happy]Like maybe you'll die in a horrible car accident on the way home today?"
- `NPC_TRACY_TRACY_IDOL4_10`: "[m:veryhappy]..."
- `NPC_TRACY_TRACY_IDOL5_1`: "[m:happy][b]P Mart wants to dispel the rumors that the tainted meat found in the storage lockers behind Pinky Winkies was in any way associated with this <br/> P Mart chain."
- `NPC_TRACY_TRACY_IDOL5_2`: "[b]The collars, pet microchips and name tags discovered in their ground beef is purely coincidental."
- `NPC_TRACY_TRACY_IDOL5_3`: "[b]And all rumors are just that, rumors.[/b]"
- `NPC_TRACY_TRACY_IDOL5_4`: "[b]P Mart will take legal action against anyone spreading said rumors and takes these allegations very seriously.[/b]"
- `NPC_TRACY_TRACY_IDOL5_5`: "[m:bored]..."
- `NPC_TRACY_TRACY_IDOL5_6`: "I saw another idol in the back, should hit the shelves tomorrow."
- `NPC_TRACY_TRACY_IDOL5_7`: "[m:sad]ugh..."
- `NPC_TRACY_TRACY_IDOL6_1`: "[m:bored]Another idol goes up for sale tomorrow."
- `NPC_TRACY_TRACY_IDOL6_2`: "At this point, I assume you know you are the only one buying these things."
- `NPC_TRACY_TRACY_IDOL6_3`: "[m:default]Only a total psycho would obsessively collect stuff like this..."
- `NPC_TRACY_TRACY_IDOL6_4`: "[m:shocked]And I don't mean that in an ableist way at all.  Don't get me wrong."
- `NPC_TRACY_TRACY_IDOL6_5`: "[m:questioning]I'm using psycho in a derogatory sense. If you were truly a psychopath, I wouldn't dare."
- `NPC_TRACY_TRACY_IDOL6_6`: "[m:default]If anything, I'd complement you on your contributions to society..."
- `NPC_TRACY_TRACY_IDOL6_7`: "[m:pondering]Plenty of people in prominent job fields are psychos... like CEOs for example."
- `NPC_TRACY_TRACY_IDOL6_8`: "..."
- `NPC_TRACY_TRACY_IDOL6_9`: "No wait, I hate those people too, hmm. Ummmm..."
- `NPC_TRACY_TRACY_IDOL6_10`: "[m:angry]Ugh, whatever. Listen, someone honked while I was walking to work and it threw my whole day."
- `NPC_TRACY_TRACY_IDOL6_11`: "I can't even think anymore... <br/> Leave me alone!"
- `NPC_TRACY_TRACY_IDOL7_1`: "[m:happy]So guess what!?"
- `NPC_TRACY_TRACY_IDOL7_2`: "Tomorrow is the last time I'll be stocking any more of those stupid idols!"
- `NPC_TRACY_TRACY_IDOL7_3`: "[m:veryhappy]That's right.  The company that made them went out of business last month!"
- `NPC_TRACY_TRACY_IDOL7_4`: "[m:mocking]Coincidentally, around the same time, they received a very strongly worded letter."
- `NPC_TRACY_TRACY_IDOL7_5`: "[m:happy]A scathing correspondence explaining in great detail the harm they are causing."
- `NPC_TRACY_TRACY_IDOL7_6`: ""Your companies eco-footprint is like a steel-toed boot to the face of mother nature.""
- `NPC_TRACY_TRACY_IDOL7_7`: "[m:happy]That was just one of the many thoughtful and incredibly well written zingers my letter featured."
- `NPC_TRACY_TRACY_IDOL7_8`: "[m:scared]The letter featured..."
- `NPC_TRACY_TRACY_IDOL7_9`: "[m:happy]OK, it was me! <br/> You got me!"
- `NPC_TRACY_TRACY_IDOL7_10`: "[m:angry]But what are you gonna do about it, huh!?"
- `NPC_TRACY_TRACY_IDOL7_11`: "What could you even do to me that you haven't already done to literally thousands of innocent kittens!?"
- `NPC_TRACY_TRACY_IDOL7_12`: "[m:veryangry]I'M THE GOOD GUY HERE! Wait, no.. I'M THE GOOD PERSON HERE!"
- `NPC_TRACY_TRACY_IDOL7_13`: "I AM A GOOD PERSON! IT'S ALL OF YOU THAT ARE EVIL!"
- `NPC_TRACY_TRACY_IDOL7_14`: "WHY ARE YOU LOOKING AT ME LIKE THAT? I SWEAR TO GOD I'LL QUIT!"
- `NPC_TRACY_TRACY_IDOL7_15`: "[m:shocked]..."
- `NPC_TRACY_TRACY_IDOL7_16`: "[m:questioning]No, tomorrow. Tomorrow I'll quit... and this store will crumble along with everyone in it!"
- `NPC_TRACY_TRACY_IDOL7_17`: "[m:sad]ugh"
- `NPC_TRACY_TRACY_FOODSTORAGE1_1`: "[m:default]Ugh..."
- `NPC_TRACY_TRACY_FOODSTORAGE1_2`: "[m:happy][b]Hello and thank you for entering the P Mart kitty donation center rewards program."
- `NPC_TRACY_TRACY_FOODSTORAGE1_3`: "[b]With your help <br/> P Mart has re-homed your donated feline to a family in need."
- `NPC_TRACY_TRACY_FOODSTORAGE1_4`: "[b]As you may have heard, all rewards members gain access to exclusive imports![/b]"
- `NPC_TRACY_TRACY_FOODSTORAGE1_5`: "[m:default]..."
- `NPC_TRACY_TRACY_FOODSTORAGE1_6`: "Come back tomorrow. I haven't restocked any new imports yet..."
- `NPC_TRACY_TRACY_FOODSTORAGE1_7`: "[m:questioning]Pretty sure it's some kind of frozen food locker or something."
- `NPC_TRACY_TRACY_FOODSTORAGE1_8`: "[m:sad]... ugh ..."
- `NPC_TRACY_TRACY_FOODSTORAGE2_1`: "[m:happy][b]P Mart wants to thank you personally for all of your hard work!"
- `NPC_TRACY_TRACY_FOODSTORAGE2_2`: "[b]We have recently expanded into rural parts of China and Africa, Spreading kittens across the globe![/b]"
- `NPC_TRACY_TRACY_FOODSTORAGE2_3`: "[m:bored]..."
- `NPC_TRACY_TRACY_FOODSTORAGE2_4`: "[m:default]And that's all I'm required to say..."
- `NPC_TRACY_TRACY_FOODSTORAGE2_5`: "It appears tomorrows import is yet another meat locker..."
- `NPC_TRACY_TRACY_FOODSTORAGE2_6`: "[m:winking]Maybe you could find a way to crawl in it and die?"
- `NPC_TRACY_TRACY_FOODSTORAGE2_7`: "[m:happy]Just an idea..."
- `NPC_TRACY_TRACY_FOODSTORAGE3_1`: "[m:happy][b]P Mart wants to remind its customers that the P in its name stands for Paw.[/b]"
- `NPC_TRACY_TRACY_FOODSTORAGE3_2`: "[b]The similarity to any of our competitors is purely coincidental.[/b]"
- `NPC_TRACY_TRACY_FOODSTORAGE3_3`: "[b]Thank you for shopping and have a blessed day![/b]"
- `NPC_TRACY_TRACY_FOODSTORAGE3_4`: "[m:bored]. . ."
- `NPC_TRACY_TRACY_FOODSTORAGE3_5`: "[m:default]Yet another food storage unit will be stocked tomorrow."
- `NPC_TRACY_TRACY_FOODSTORAGE3_6`: "[m:questioning]Do you seriously need more food storage?"
- `NPC_TRACY_TRACY_FOODSTORAGE3_7`: "[m:angry]Have you maybe thought about donating your excess food to a local animal shelter?"
- `NPC_TRACY_TRACY_FOODSTORAGE3_8`: "[m:pondering]. . ."
- `NPC_TRACY_TRACY_FOODSTORAGE3_9`: "[m:shocked]No, I don't know specifically what animal shelters there are around here."
- `NPC_TRACY_TRACY_FOODSTORAGE3_10`: "[m:angry]Oh, am I supposed to work for you now? It's my job to find write-offs for capitalist gains?"
- `NPC_TRACY_TRACY_FOODSTORAGE3_11`: "[m:veryangry]Is that it? I'm just an unpaid laborer, free for you to use and abuse as you see fit?"
- `NPC_TRACY_TRACY_FOODSTORAGE3_12`: "[m:angry]That's it isn't it? <br/> That's how you get off!?"
- `NPC_TRACY_TRACY_FOODSTORAGE3_13`: "[m:veryangry][a:shake]DISGUSTING![/a]"
- `NPC_TRACY_TRACY_FOODSTORAGE3_14`: "[m:shocked]. . ."
- `NPC_TRACY_TRACY_FOODSTORAGE3_15`: "[m:happy][b]Thanks for shopping at P Mart, and have a blessed day![/b]"
- `NPC_TRACY_TRACY_FOODSTORAGE3_16`: "[m:sad]... ugh ..."
- `NPC_TRACY_TRACY_FOODSTORAGE4_1`: "[m:bored]. . ."
- `NPC_TRACY_TRACY_FOODSTORAGE4_2`: "[m:default]So another food storage unit appeared in the back today..."
- `NPC_TRACY_TRACY_FOODSTORAGE4_3`: "[m:questioning]What the hell are you doing with these things, seriously?"
- `NPC_TRACY_TRACY_FOODSTORAGE4_4`: "[m:pondering]..."
- `NPC_TRACY_TRACY_FOODSTORAGE4_5`: "[m:whispering]Are you killing people? Taking them out and putting the bodies in cold storage?"
- `NPC_TRACY_TRACY_FOODSTORAGE4_6`: "[m:happy]You can tell me if you are... I mean, like how do you choose 'em?"
- `NPC_TRACY_TRACY_FOODSTORAGE4_7`: "[m:happy]If it was me I'd pose as a dog of some kind, just kinda lay there and wait."
- `NPC_TRACY_TRACY_FOODSTORAGE4_8`: "Someone would attempt to "rescue" me, but the moment I'm in their house, it's over!"
- `NPC_TRACY_TRACY_FOODSTORAGE4_9`: "[m:veryangry][a:shake]"AN ANIMAL CAN'T BE OWNED!"[/a] <br/> I'd yell as I start going to town on 'em all!"
- `NPC_TRACY_TRACY_FOODSTORAGE4_10`: "[m:veryhappy]Then I'd grind 'em all up in one of those industrial deals, like the ones Pinky Winkies has."
- `NPC_TRACY_TRACY_FOODSTORAGE4_11`: "[m:happy]And just mix 'em in with the meat..."
- `NPC_TRACY_TRACY_FOODSTORAGE4_12`: "[m:veryangry]Let the CONSUMER become the CONSUMED!"
- `NPC_TRACY_TRACY_FOODSTORAGE4_13`: "[m:veryhappy]HAHAHAHAHA!"
- `NPC_TRACY_TRACY_FOODSTORAGE4_14`: "[m:happy][b]Thanks for shopping at <br/> P Mart![/b]"
- `NPC_TRACY_TRACY_FOODSTORAGE4_15`: "[b]And have a VERY blessed day![/b]"
- `NPC_TRACY_TRACY_FOODSTORAGE5_1`: "[m:happy][b]Attention P Mart shoppers![/b]"
- `NPC_TRACY_TRACY_FOODSTORAGE5_2`: "[b]We would like to advise our patrons that any individual offering to wash windows[/b]"
- `NPC_TRACY_TRACY_FOODSTORAGE5_3`: "[b]Or solicit products are not employed by, or associated with this facility.[/b]"
- `NPC_TRACY_TRACY_FOODSTORAGE5_4`: "[b]We discourage any contact with these individuals and ask that you report any problems to uniformed personnel inside.[/b]"
- `NPC_TRACY_TRACY_FOODSTORAGE5_5`: "[b]Thanks for shopping at P Mart, and have a blessed day![/b]"
- `NPC_TRACY_TRACY_FOODSTORAGE5_6`: "[m:bored]..."
- `NPC_TRACY_TRACY_FOODSTORAGE5_7`: "[m:default]You got a new meat locker in the back..."
- `NPC_TRACY_TRACY_FOODSTORAGE5_8`: "[m:questioning]I'll bring it out tomorrow, I guess."
- `NPC_TRACY_TRACY_FOODSTORAGE5_9`: "[m:bored]Whatever..."
- `NPC_TRACY_TRACY_FOODSTORAGE6_1`: "[m:default]Another locker appeared in the back today..."
- `NPC_TRACY_TRACY_FOODSTORAGE6_2`: "[m:questioning]Are you some kind of prepper? What's the deal with the food lockers?"
- `NPC_TRACY_TRACY_FOODSTORAGE6_3`: "[m:default]You know if you need extra storage, that Pinky Winkies downtown has a ton."
- `NPC_TRACY_TRACY_FOODSTORAGE6_4`: "[m:pondering]Hell, I bet you could fit 30+ middle-aged white men in the units they got back there!"
- `NPC_TRACY_TRACY_FOODSTORAGE6_5`: "[m:happy]Strip 'em down and you can fit 3 more! Crazy, huh?"
- `NPC_TRACY_TRACY_FOODSTORAGE6_6`: "You wouldn't think khaki slacks and business suits could take up so much space..."
- `NPC_TRACY_TRACY_FOODSTORAGE6_7`: "And you can just burn those at the junkyard in an old metal bin."
- `NPC_TRACY_TRACY_FOODSTORAGE6_8`: "[m:shocked]..."
- `NPC_TRACY_TRACY_FOODSTORAGE6_9`: "[m:angry]I'm just offering you advice! No need to get all uppity about it!"
- `NPC_TRACY_TRACY_FOODSTORAGE6_10`: "[m:bored]Your wasteful meat cooler will be in stock tomorrow."
- `NPC_TRACY_TRACY_FOODSTORAGE7_1`: "[m:bored]If you think collecting coolers is going to make you cooler, you're wrong."
- `NPC_TRACY_TRACY_FOODSTORAGE7_2`: "[m:happy]Hahaha, <br/> [s:.7]Make you cooler...[/s]"
- `NPC_TRACY_TRACY_FOODSTORAGE7_3`: "[m:pondering]Well I guess if you left them open, you'd become cooler..."
- `NPC_TRACY_TRACY_FOODSTORAGE7_4`: "[m:angry]But that's not what I meant, and leaving refrigeration units open is extremely wasteful."
- `NPC_TRACY_TRACY_FOODSTORAGE7_5`: "And terrible for our environment! <br/> That's not something to make light of!"
- `NPC_TRACY_TRACY_FOODSTORAGE7_6`: "[m:veryangry]..."
- `NPC_TRACY_TRACY_FOODSTORAGE7_7`: "[m:angry]You may assume your laughter is innocent, but mocking things like this not only reinforces bad behavior..."
- `NPC_TRACY_TRACY_FOODSTORAGE7_8`: "[m:angry]But it also pumps carbon dioxide into the atmosphere..."
- `NPC_TRACY_TRACY_FOODSTORAGE7_9`: "And everyone knows with all the deforestation going on these days..."
- `NPC_TRACY_TRACY_FOODSTORAGE7_10`: "[m:shocked]Every chuckle could mean ending the life of an innocent animal."
- `NPC_TRACY_TRACY_FOODSTORAGE7_11`: "[m:angry]..."
- `NPC_TRACY_TRACY_FOODSTORAGE7_12`: "[m:veryangry]Shame on you!"
- `NPC_TRACY_TRACY_FOODSTORAGE8_1`: "[m:happy][b]Attention P Mart shoppers![/b]"
- `NPC_TRACY_TRACY_FOODSTORAGE8_2`: "[b]Today we have a sale on industrial grade cages and locks![/b]"
- `NPC_TRACY_TRACY_FOODSTORAGE8_3`: "[b]Buy one get 2 free![/b]"
- `NPC_TRACY_TRACY_FOODSTORAGE8_4`: "[m:happy][b]Thanks for shopping at P Mart, and have a blessed day![/b]"
- `NPC_TRACY_TRACY_FOODSTORAGE8_5`: "[m:bored]. . ."
- `NPC_TRACY_TRACY_FOODSTORAGE8_6`: "Industrial grade my ass."
- `NPC_TRACY_TRACY_FOODSTORAGE8_7`: "[m:default]If a middle-aged white man can break out of it, it ain't worth it IMO."
- `NPC_TRACY_TRACY_FOODSTORAGE8_8`: "[m:angry]And I don't care if he chewed off his own hand and nubbed the lock through the bars 'till it unlatched!"
- `NPC_TRACY_TRACY_FOODSTORAGE8_9`: "Not my problem! <br/> Instantly returned! <br/> And you better believe I left a scathing review!"
- `NPC_TRACY_TRACY_FOODSTORAGE8_10`: "[m:happy]"One star! <br/> Creator is a pedo. <br/> Would not recommend!""
- `NPC_TRACY_TRACY_FOODSTORAGE9_1`: "[m:sad]I'm honestly starting to think I'm in the wrong field of work..."
- `NPC_TRACY_TRACY_FOODSTORAGE9_2`: "Seeing your face daily is like looking into some kinda horrible mirror of fate."
- `NPC_TRACY_TRACY_FOODSTORAGE9_3`: "[m:pondering]Will I too become an old spinster cat hoarding maniac..."
- `NPC_TRACY_TRACY_FOODSTORAGE9_4`: "Working for a Nazi madman doing experiments on whatever life form comes my way..."
- `NPC_TRACY_TRACY_FOODSTORAGE9_5`: "[m:shocked]Am I doomed to die alone in some attic? Feverishly trying to find proof of who I used to be?"
- `NPC_TRACY_TRACY_FOODSTORAGE9_6`: "[m:questioning]. . ."
- `NPC_TRACY_TRACY_FOODSTORAGE9_7`: "[m:angry]Well the answer is no, obviously! Because I'm actually going to do something with my life!"
- `NPC_TRACY_TRACY_FOODSTORAGE9_8`: "Starting tomorrow.  Tomorrow I'm quitting this job and I'll start living!"
- `NPC_TRACY_TRACY_FOODSTORAGE9_9`: "Tomorrow, after I bring out your 9th food storage locker... <br/> Then I'm outta here!"
- `NPC_TRACY_TRACY_FOODSTORAGE9_10`: "[m:sad][s:.7]Yeah... tomorrow.[/s]"
- `NPC_TRACY_TRACY_FOODSTORAGE10_1`: "[m:happy][b]Welcome back to <br/> P Mart, where cleanliness is a high priority![/b]"
- `NPC_TRACY_TRACY_FOODSTORAGE10_2`: "[b]And that also goes for our many recently opened <br/> P Mart fast food chains popping up all over the US![/b]"
- `NPC_TRACY_TRACY_FOODSTORAGE10_3`: "[b]You heard us right! <br/> P Mart has expanded into food service![/b]"
- `NPC_TRACY_TRACY_FOODSTORAGE10_4`: "[b]And this is all thanks to you, our very loyal patrons![/b]"
- `NPC_TRACY_TRACY_FOODSTORAGE10_5`: "[b]As a heartfelt thank you from us to you, we are offering an extra 5% off all expired meats and canned goods![/b]"
- `NPC_TRACY_TRACY_FOODSTORAGE10_6`: "[m:happy][b]Thanks for shopping at P Mart, and have a blessed day![/b]"
- `NPC_TRACY_TRACY_FOODSTORAGE10_7`: "[m:bored]. . ."
- `NPC_TRACY_TRACY_FOODSTORAGE10_8`: "[m:default]Your final meat locker hits the shelves tomorrow when we open."
- `NPC_TRACY_TRACY_FOODSTORAGE10_9`: "[m:happy]But I won't be here! <br/> That's right, I got a job at this new fast food place opening up soon!"
- `NPC_TRACY_TRACY_FOODSTORAGE10_10`: "[m:winking]So enjoy your life or whatever! I know I'll be enjoying mine..."
- `NPC_TRACY_TRACY_FOODSTORAGE10_11`: "[m:happy]Taking down yet another greedy corporation from the inside."
- `NPC_TRACY_TRACY_FOODSTORAGE10_12`: "[m:veryhappy][s:1.3]Let the adventure begin![/s]"
- `NPC_TRACY_TRACY_MAX_INTRO_1`: "[m:bored]Well it appears P Mart's rewards program caps out here..."
- `NPC_TRACY_TRACY_MAX_INTRO_2`: "Congratulations on being the first loser to completely sell your soul to the man, or whatever!"
- `NPC_TRACY_TRACY_MAX_INTRO_3`: "[m:default]Management has informed me that from here on out, you'll only be gaining items from..."
- `NPC_TRACY_TRACY_MAX_INTRO_4`: "[m:shocked]The P Mart <br/> [a:shake][s:1.2]Box of Mystery![/a][/s]"
- `NPC_TRACY_TRACY_MAX_INTRO_5`: "[m:pondering]Who knows what could be inside? <br/> Find out tomorrow!"
- `NPC_TRACY_TRACY_MAX_INTRO_6`: "[m:bored]Spoiler: It's definitely not your soul, that's for sure."
- `NPC_TRACY_TRACY_MAX_INTRO_7`: "Seriously, how do you live with yourself?"
- `NPC_TRACY_TRACY_MAX1_1`: "[m:happy]Another worthless reward appears in the shop tomorrow!"
- `NPC_TRACY_TRACY_MAX1_2`: "[m:veryhappy]Doesn't that make you so happy!? Isn't life worth living now!?"
- `NPC_TRACY_TRACY_MAX1_3`: "[m:happy]More stuff! Yay! More trash for the landfill! Woo hoo!"
- `NPC_TRACY_TRACY_MAX2_1`: "[m:bored]A new mystery box item will be revealed tomorrow!"
- `NPC_TRACY_TRACY_MAX2_2`: "[m:veryhappy]Isn't that exciting!? Jump for joy! That thing you don't need is coming!"
- `NPC_TRACY_TRACY_MAX2_3`: "[m:grossedout]... you suck!"
- `NPC_TRACY_TRACY_MAX3_1`: "[m:default]I hope when you look at your mystery gift tomorrow all you see is a giant pile of human excrement."
- `NPC_TRACY_TRACY_MAX3_2`: "[m:happy]What I'm saying is, I hope it's a mirror!"
- `NPC_TRACY_TRACY_MAX3_3`: "[m:veryhappy]HAHAHAHAH <br/> Hahaha!"
- `NPC_TRACY_TRACY_MAX3_4`: "[m:happy]Guess we find out tomorrow, huh?"
- `NPC_TRACY_TRACY_MAX4_1`: "[m:bored]The mystery box appears again tomorrow!"
- `NPC_TRACY_TRACY_MAX4_2`: "I sure hope it's a gun so I can shoot myself!"
- `NPC_TRACY_TRACY_MAX4_3`: "[m:shocked]..."
- `NPC_TRACY_TRACY_MAX4_4`: "[m:scared]Wait, I didn't mean that! Don't report me to corporate!"
- `NPC_TRACY_TRACY_MAX4_5`: "[m:paranoid]What I meant to say is, I hope it's a gun so i can shoot YOU, <br/> I misspoke!"
- `NPC_TRACY_TRACY_MAX4_6`: "[m:winking]Crisis averted."
- `NPC_TRACY_TRACY_MAX5_1`: "[m:mocking]Look at me, I'm a big dumb idiot who keeps sending cats to P Mart!"
- `NPC_TRACY_TRACY_MAX5_2`: "[m:spacedout]DUUR DURRR! I love the crap I get when I do what I'm told! HUUURRR!"
- `NPC_TRACY_TRACY_MAX5_3`: "[m:whispering]I sure hope the mystery gift I get tomorrow is a TV so I can become even more brain dead!"
- `NPC_TRACY_TRACY_MAX5_4`: "[m:happy]Because I like to just do whatever I'm told! Like a robot! I'm a soulless robot!"
- `NPC_TRACY_TRACY_MAX5_5`: "[m:spacedout]BEEP BOOP! RACIST COMMENT! BEEP BOOP! I LOVE COPS!"
- `NPC_TRACY_TRACY_MAX5_6`: "[m:angry]. . ."
- `NPC_TRACY_TRACY_MAX5_7`: "[m:veryangry]That's you! <br/> I'm being you!"
- `NPC_TRACY_UNKNOWN_1`: "You appear to have unlocked something, but I don't have dialog for it. Congrats. Also fix this."
- `NPC_TRACY_TRACY_KAIJUFIGHT_1`: "[m:angry]Those stupid giant monsters are fighting outside the store again!"
- `NPC_TRACY_TRACY_KAIJUFIGHT_2`: "Can you do something? Aren't you a murderer or whatever?"
- `NPC_TRACY_TRACY_KAIJUFIGHT_3`: "[m:veryangry]Well, murder them!"
- `NPC_TRACY_TRACY_KAIJUFIGHT_4`: "[m:pondering]Or I guess murder at least one of them?"
- `NPC_TRACY_TRACY_KAIJUFIGHT_5`: "[m:angry]Whatever gets them to stop destroying literally everything in town!"
- `NPC_TRACY_TRACY_KAIJUFIGHT_6`: "I've been trapped in this damn store for a week now!"
- `NPC_TRACY_TRACY_KAIJUFIGHT_7`: "[m:veryangry]And my landlord can go to hell if he thinks I'm paying for the last 7 days!"
- `NPC_TRACY_TRACY_KAIJUFIGHT_8`: "[m:angry]You know what, go kill him too while you are at it!"
- `NPC_TRACY_TRACY_KAIJUFIGHT_9`: "[m:veryangry][s:1.2]Him and every other landlord out there![/s]"
- `NPC_TRACY_TRACY_KAIJUFIGHT_10`: "[a:shake]GAAAHHHH!!!![/a]"

```
sequences {
	unprompted {
		cancelable true
		dialog NPC_TRACY_UNPROMPTED_1
		dialog_and_autopass NPC_TRACY_UNPROMPTED_2
		wait_for_cancel 1
	}

	also {
		dialog NPC_TRACY_ALSO_1
	}

	tracy_introduction { //jacks introduction is in combat_tutorial since he needs to pop up over the house
		lock_controls 1
		set_state blocking
		set_state closeup
		dialog NPC_TRACY_TRACY_INTRODUCTION_1
		set_state blocking
		dialog NPC_TRACY_TRACY_INTRODUCTION_2
		dialog NPC_TRACY_TRACY_INTRODUCTION_3
		dialog NPC_TRACY_TRACY_INTRODUCTION_4
		set_state closeup
		dialog NPC_TRACY_TRACY_INTRODUCTION_5
		set_state zoomedout
		dialog NPC_TRACY_TRACY_INTRODUCTION_6
		dialog NPC_TRACY_TRACY_INTRODUCTION_7
		dialog NPC_TRACY_TRACY_INTRODUCTION_8
		dialog NPC_TRACY_TRACY_INTRODUCTION_9
		set_state closeup
		dialog NPC_TRACY_TRACY_INTRODUCTION_10
		set_state zoomedout
		dialog NPC_TRACY_TRACY_INTRODUCTION_11
		dialog NPC_TRACY_TRACY_INTRODUCTION_12
		dialog NPC_TRACY_TRACY_INTRODUCTION_13
		dialog NPC_TRACY_TRACY_INTRODUCTION_14
		set_state closeup
		dialog NPC_TRACY_TRACY_INTRODUCTION_15
		set_state idle
		dialog NPC_TRACY_TRACY_INTRODUCTION_16
		dialog NPC_TRACY_TRACY_INTRODUCTION_17
		set_state zoomedout
		dialog NPC_TRACY_TRACY_INTRODUCTION_18
		set_state idle
		dialog NPC_TRACY_TRACY_INTRODUCTION_19
		dialog NPC_TRACY_TRACY_INTRODUCTION_20
		dialog NPC_TRACY_TRACY_INTRODUCTION_21
		set_state closeup
		dialog NPC_TRACY_TRACY_INTRODUCTION_22
		begin_accepting_cats tracy
		set_state idle
		unlock_controls 1
	}

	out_of_stock {
		set_state blocking
		dialog NPC_TRACY_OUT_OF_STOCK_1
	}
	purchase_item {
		cancelable true
		dialog_and_autopass NPC_TRACY_PURCHASE_ITEM_1
		wait_for_cancel 1
	}
	cant_afford {
		cancelable true
		dialog_and_autopass NPC_TRACY_CANT_AFFORD_1
		wait_for_cancel 1
	}

	tooltip {
		cancelable true
		tooltip_dialog NPC_TRACY_SHOP_TOOLTIP
		wait_for_cancel 1
	}
	hide_text {
		cancelable true
		dialog_and_autopass ""
	}

	//UNLOCKS
	tracy_foodbonus1 {
		lock_controls 1
		set_state blocking
		dialog NPC_TRACY_TRACY_FOODBONUS1_1
		get npc_reward
		dialog NPC_TRACY_TRACY_FOODBONUS1_2
		set_state idle
		unlock_controls 1
	}
	//these arent in the order you unlock them in

	//collar rewards
	tracy_blankcollar1 {
		lock_controls 1
		set_state blocking
		set_state idle
		dialog NPC_TRACY_TRACY_BLANKCOLLAR1_1
		dialog NPC_TRACY_TRACY_BLANKCOLLAR1_2
		set_state closeup
		dialog NPC_TRACY_TRACY_BLANKCOLLAR1_3
		dialog NPC_TRACY_TRACY_BLANKCOLLAR1_4
		set_state zoomedout
		dialog NPC_TRACY_TRACY_BLANKCOLLAR1_5
		dialog NPC_TRACY_TRACY_BLANKCOLLAR1_6
		set_state closeup
		dialog NPC_TRACY_TRACY_BLANKCOLLAR1_7
		set_state idle
		dialog NPC_TRACY_TRACY_BLANKCOLLAR1_8
		set_state zoomedout
		dialog NPC_TRACY_TRACY_BLANKCOLLAR1_9
		get npc_reward
		set_state idle
		unlock_controls 1
	}

	tracy_blankcollar2 {
		lock_controls 1
		set_state blocking
		set_state idle
		dialog NPC_TRACY_TRACY_BLANKCOLLAR2_1
		dialog NPC_TRACY_TRACY_BLANKCOLLAR2_2
		dialog NPC_TRACY_TRACY_BLANKCOLLAR2_3
		set_state zoomedout
		dialog NPC_TRACY_TRACY_BLANKCOLLAR2_4
		dialog NPC_TRACY_TRACY_BLANKCOLLAR2_5
		dialog NPC_TRACY_TRACY_BLANKCOLLAR2_6
		set_state closeup
		dialog NPC_TRACY_TRACY_BLANKCOLLAR2_7
		dialog NPC_TRACY_TRACY_BLANKCOLLAR2_8
		set_state verycloseup
		dialog NPC_TRACY_TRACY_BLANKCOLLAR2_9
		dialog NPC_TRACY_TRACY_BLANKCOLLAR2_10
		set_state idle
		dialog NPC_TRACY_TRACY_BLANKCOLLAR2_11
		get npc_reward
		set_state idle
		unlock_controls 1
	}

	tracy_blankcollar3 {
		lock_controls 1
		set_state blocking
		set_state idle
		dialog NPC_TRACY_TRACY_BLANKCOLLAR3_1
		dialog NPC_TRACY_TRACY_BLANKCOLLAR3_2
		dialog NPC_TRACY_TRACY_BLANKCOLLAR3_3
		dialog NPC_TRACY_TRACY_BLANKCOLLAR3_4
		set_state zoomedout
		dialog NPC_TRACY_TRACY_BLANKCOLLAR3_5
		set_state closeup
		dialog NPC_TRACY_TRACY_BLANKCOLLAR3_6
		set_state zoomedout
		dialog NPC_TRACY_TRACY_BLANKCOLLAR3_7
		get npc_reward
		set_state idle
		unlock_controls 1
	}

	//idol rewards
	tracy_idol1 {
		lock_controls 1
		set_state blocking
		set_state idle
		dialog NPC_TRACY_TRACY_IDOL1_1
		dialog NPC_TRACY_TRACY_IDOL1_2
		dialog NPC_TRACY_TRACY_IDOL1_3
		dialog NPC_TRACY_TRACY_IDOL1_4
		set_state zoomedout
		dialog NPC_TRACY_TRACY_IDOL1_5
		dialog NPC_TRACY_TRACY_IDOL1_6
		dialog NPC_TRACY_TRACY_IDOL1_7
		dialog NPC_TRACY_TRACY_IDOL1_8
		dialog NPC_TRACY_TRACY_IDOL1_9
		set_state closeup
		dialog NPC_TRACY_TRACY_IDOL1_10
		set_state verycloseup
		dialog NPC_TRACY_TRACY_IDOL1_11
		dialog NPC_TRACY_TRACY_IDOL1_12
		set_state idle
		dialog NPC_TRACY_TRACY_IDOL1_13
		get npc_reward
		set_state idle
		unlock_controls 1
	}
	tracy_idol2 {
		lock_controls 1
		set_state blocking
		set_state idle
		dialog NPC_TRACY_TRACY_IDOL2_1
		set_state closeup
		dialog NPC_TRACY_TRACY_IDOL2_2
		dialog NPC_TRACY_TRACY_IDOL2_3
		dialog NPC_TRACY_TRACY_IDOL2_4
		dialog NPC_TRACY_TRACY_IDOL2_5
		dialog NPC_TRACY_TRACY_IDOL2_6
		set_state verycloseup
		dialog NPC_TRACY_TRACY_IDOL2_7
		dialog NPC_TRACY_TRACY_IDOL2_8
		get npc_reward
		set_state idle
		unlock_controls 1
	}
	tracy_idol3 {
		lock_controls 1
		set_state blocking
		dialog NPC_TRACY_TRACY_IDOL3_1
		dialog NPC_TRACY_TRACY_IDOL3_2
		dialog NPC_TRACY_TRACY_IDOL3_3
		dialog NPC_TRACY_TRACY_IDOL3_4
		set_state closeup
		dialog NPC_TRACY_TRACY_IDOL3_5
		dialog NPC_TRACY_TRACY_IDOL3_6
		dialog NPC_TRACY_TRACY_IDOL3_7
		set_state verycloseup
		dialog NPC_TRACY_TRACY_IDOL3_8
		dialog NPC_TRACY_TRACY_IDOL3_9
		set_state idle
		dialog NPC_TRACY_TRACY_IDOL3_10
		dialog NPC_TRACY_TRACY_IDOL3_11
		get npc_reward
		set_state idle
		unlock_controls 1
	}
	tracy_idol4 {
		lock_controls 1
		set_state blocking
		set_state idle
		dialog NPC_TRACY_TRACY_IDOL4_1
		dialog NPC_TRACY_TRACY_IDOL4_2
		set_state zoomedout
		dialog NPC_TRACY_TRACY_IDOL4_3
		dialog NPC_TRACY_TRACY_IDOL4_4
		set_state closeup
		dialog NPC_TRACY_TRACY_IDOL4_5
		dialog NPC_TRACY_TRACY_IDOL4_6
		dialog NPC_TRACY_TRACY_IDOL4_7
		dialog NPC_TRACY_TRACY_IDOL4_8
		set_state zoomedout
		dialog NPC_TRACY_TRACY_IDOL4_9
		set_state verycloseup
		dialog NPC_TRACY_TRACY_IDOL4_10
		get npc_reward
		set_state idle
		
		unlock_controls 1
	}
	tracy_idol5 {
		lock_controls 1
		set_state blocking
		set_state idle
		dialog NPC_TRACY_TRACY_IDOL5_1
		dialog NPC_TRACY_TRACY_IDOL5_2
		dialog NPC_TRACY_TRACY_IDOL5_3
		dialog NPC_TRACY_TRACY_IDOL5_4
		set_state closeup
		dialog NPC_TRACY_TRACY_IDOL5_5
		dialog NPC_TRACY_TRACY_IDOL5_6
		dialog NPC_TRACY_TRACY_IDOL5_7
		get npc_reward
		set_state idle
		unlock_controls 1
	}
	tracy_idol6 {
		lock_controls 1
		set_state blocking
		set_state zoomedout
		dialog NPC_TRACY_TRACY_IDOL6_1
		dialog NPC_TRACY_TRACY_IDOL6_2
		dialog NPC_TRACY_TRACY_IDOL6_3
		set_state closeup
		dialog NPC_TRACY_TRACY_IDOL6_4
		dialog NPC_TRACY_TRACY_IDOL6_5
		dialog NPC_TRACY_TRACY_IDOL6_6
		dialog NPC_TRACY_TRACY_IDOL6_7
		set_state zoomedout
		dialog NPC_TRACY_TRACY_IDOL6_8
		set_state closeup
		dialog NPC_TRACY_TRACY_IDOL6_9
		dialog NPC_TRACY_TRACY_IDOL6_10
		set_state verycloseup
		dialog NPC_TRACY_TRACY_IDOL6_11
		get npc_reward
		set_state idle
		unlock_controls 1
	}
	tracy_idol7 {
		lock_controls 1
		set_state blocking
		set_state verycloseup
		dialog NPC_TRACY_TRACY_IDOL7_1
		set_state closeup
		dialog NPC_TRACY_TRACY_IDOL7_2
		dialog NPC_TRACY_TRACY_IDOL7_3
		dialog NPC_TRACY_TRACY_IDOL7_4
		dialog NPC_TRACY_TRACY_IDOL7_5
		set_state verycloseup
		dialog NPC_TRACY_TRACY_IDOL7_6
		set_state closeup
		dialog NPC_TRACY_TRACY_IDOL7_7
		set_state zoomedout
		dialog NPC_TRACY_TRACY_IDOL7_8
		set_state closeup
		dialog NPC_TRACY_TRACY_IDOL7_9
		dialog NPC_TRACY_TRACY_IDOL7_10
		dialog NPC_TRACY_TRACY_IDOL7_11
		set_state verycloseup
		dialog NPC_TRACY_TRACY_IDOL7_12
		dialog NPC_TRACY_TRACY_IDOL7_13
		dialog NPC_TRACY_TRACY_IDOL7_14
		set_state closeup
		dialog NPC_TRACY_TRACY_IDOL7_15
		set_state zoomedout
		dialog NPC_TRACY_TRACY_IDOL7_16
		dialog NPC_TRACY_TRACY_IDOL7_17
		get npc_reward
		set_state idle
		unlock_controls 1
	}

	//food storage rewards
	tracy_foodstorage1 {
		lock_controls 1
		set_state blocking
		set_state zoomedout
		dialog NPC_TRACY_TRACY_FOODSTORAGE1_1
		set_state idle
		dialog NPC_TRACY_TRACY_FOODSTORAGE1_2
		dialog NPC_TRACY_TRACY_FOODSTORAGE1_3
		dialog NPC_TRACY_TRACY_FOODSTORAGE1_4
		set_state zoomedout
		dialog NPC_TRACY_TRACY_FOODSTORAGE1_5
		set_state closeup
		dialog NPC_TRACY_TRACY_FOODSTORAGE1_6
		dialog NPC_TRACY_TRACY_FOODSTORAGE1_7
		set_state zoomedout
		dialog NPC_TRACY_TRACY_FOODSTORAGE1_8 
		get npc_reward
		set_state idle
		unlock_controls 1
	}
	tracy_foodstorage2 {
		lock_controls 1
		set_state blocking
		set_state idle
		dialog NPC_TRACY_TRACY_FOODSTORAGE2_1
		dialog NPC_TRACY_TRACY_FOODSTORAGE2_2
		set_state zoomedout
		dialog NPC_TRACY_TRACY_FOODSTORAGE2_3
		dialog NPC_TRACY_TRACY_FOODSTORAGE2_4
		dialog NPC_TRACY_TRACY_FOODSTORAGE2_5
		set_state closeup
		dialog NPC_TRACY_TRACY_FOODSTORAGE2_6
		dialog NPC_TRACY_TRACY_FOODSTORAGE2_7
		get npc_reward
		set_state idle
		unlock_controls 1
	}
	tracy_foodstorage3 {
		lock_controls 1
		set_state blocking
		set_state idle
		dialog NPC_TRACY_TRACY_FOODSTORAGE3_1
		dialog NPC_TRACY_TRACY_FOODSTORAGE3_2
		dialog NPC_TRACY_TRACY_FOODSTORAGE3_3
		set_state zoomedout
		dialog NPC_TRACY_TRACY_FOODSTORAGE3_4
		dialog NPC_TRACY_TRACY_FOODSTORAGE3_5
		dialog NPC_TRACY_TRACY_FOODSTORAGE3_6
		dialog NPC_TRACY_TRACY_FOODSTORAGE3_7
		dialog NPC_TRACY_TRACY_FOODSTORAGE3_8
		set_state closeup
		dialog NPC_TRACY_TRACY_FOODSTORAGE3_9
		dialog NPC_TRACY_TRACY_FOODSTORAGE3_10
		dialog NPC_TRACY_TRACY_FOODSTORAGE3_11
		dialog NPC_TRACY_TRACY_FOODSTORAGE3_12
		set_state verycloseup
		dialog NPC_TRACY_TRACY_FOODSTORAGE3_13
		set_state zoomedout
		dialog NPC_TRACY_TRACY_FOODSTORAGE3_14
		set_state idle
		dialog NPC_TRACY_TRACY_FOODSTORAGE3_15
		set_state zoomedout
		dialog NPC_TRACY_TRACY_FOODSTORAGE3_16 
		get npc_reward
		set_state idle
		unlock_controls 1
	}
	tracy_foodstorage4 {
		lock_controls 1
		set_state blocking
		set_state zoomedout
		dialog NPC_TRACY_TRACY_FOODSTORAGE4_1
		dialog NPC_TRACY_TRACY_FOODSTORAGE4_2
		dialog NPC_TRACY_TRACY_FOODSTORAGE4_3
		dialog NPC_TRACY_TRACY_FOODSTORAGE4_4
		set_state closeup
		dialog NPC_TRACY_TRACY_FOODSTORAGE4_5
		dialog NPC_TRACY_TRACY_FOODSTORAGE4_6
		set_state zoomedout
		dialog NPC_TRACY_TRACY_FOODSTORAGE4_7
		dialog NPC_TRACY_TRACY_FOODSTORAGE4_8
		set_state verycloseup
		dialog NPC_TRACY_TRACY_FOODSTORAGE4_9
		set_state closeup
		dialog NPC_TRACY_TRACY_FOODSTORAGE4_10
		dialog NPC_TRACY_TRACY_FOODSTORAGE4_11
		set_state verycloseup
		dialog NPC_TRACY_TRACY_FOODSTORAGE4_12
		dialog NPC_TRACY_TRACY_FOODSTORAGE4_13
		set_state idle
		dialog NPC_TRACY_TRACY_FOODSTORAGE4_14
		dialog NPC_TRACY_TRACY_FOODSTORAGE4_15
		get npc_reward
		set_state idle
		unlock_controls 1
	}
	tracy_foodstorage5 {
		lock_controls 1
		set_state blocking
		set_state idle
		dialog NPC_TRACY_TRACY_FOODSTORAGE5_1
		dialog NPC_TRACY_TRACY_FOODSTORAGE5_2
		dialog NPC_TRACY_TRACY_FOODSTORAGE5_3
		dialog NPC_TRACY_TRACY_FOODSTORAGE5_4
		dialog NPC_TRACY_TRACY_FOODSTORAGE5_5
		set_state zoomedout
		dialog NPC_TRACY_TRACY_FOODSTORAGE5_6
		dialog NPC_TRACY_TRACY_FOODSTORAGE5_7
		dialog NPC_TRACY_TRACY_FOODSTORAGE5_8
		dialog NPC_TRACY_TRACY_FOODSTORAGE5_9
		get npc_reward
		set_state idle
		unlock_controls 1
	}
	tracy_foodstorage6 {
		lock_controls 1
		set_state blocking
		set_state zoomedout
		dialog NPC_TRACY_TRACY_FOODSTORAGE6_1
		dialog NPC_TRACY_TRACY_FOODSTORAGE6_2
		dialog NPC_TRACY_TRACY_FOODSTORAGE6_3
		set_state closeup
		dialog NPC_TRACY_TRACY_FOODSTORAGE6_4
		dialog NPC_TRACY_TRACY_FOODSTORAGE6_5
		dialog NPC_TRACY_TRACY_FOODSTORAGE6_6
		dialog NPC_TRACY_TRACY_FOODSTORAGE6_7
		set_state verycloseup
		dialog NPC_TRACY_TRACY_FOODSTORAGE6_8
		set_state closeup
		dialog NPC_TRACY_TRACY_FOODSTORAGE6_9
		dialog NPC_TRACY_TRACY_FOODSTORAGE6_10
		get npc_reward
		set_state idle
		unlock_controls 1
	}
	tracy_foodstorage7 {
		lock_controls 1
		set_state blocking
		set_state zoomedout
		dialog NPC_TRACY_TRACY_FOODSTORAGE7_1
		set_state closeup
		dialog NPC_TRACY_TRACY_FOODSTORAGE7_2 
		dialog NPC_TRACY_TRACY_FOODSTORAGE7_3
		dialog NPC_TRACY_TRACY_FOODSTORAGE7_4
		dialog NPC_TRACY_TRACY_FOODSTORAGE7_5
		dialog NPC_TRACY_TRACY_FOODSTORAGE7_6
		set_state zoomedout
		dialog NPC_TRACY_TRACY_FOODSTORAGE7_7
		dialog NPC_TRACY_TRACY_FOODSTORAGE7_8
		dialog NPC_TRACY_TRACY_FOODSTORAGE7_9
		set_state closeup
		dialog NPC_TRACY_TRACY_FOODSTORAGE7_10
		dialog NPC_TRACY_TRACY_FOODSTORAGE7_11
		set_state verycloseup
		dialog NPC_TRACY_TRACY_FOODSTORAGE7_12
		get npc_reward
		set_state idle
		unlock_controls 1
	}
	tracy_foodstorage8 {
		lock_controls 1
		set_state blocking
		set_state idle
		dialog NPC_TRACY_TRACY_FOODSTORAGE8_1
		dialog NPC_TRACY_TRACY_FOODSTORAGE8_2
		dialog NPC_TRACY_TRACY_FOODSTORAGE8_3
		dialog NPC_TRACY_TRACY_FOODSTORAGE8_4
		set_state zoomedout
		dialog NPC_TRACY_TRACY_FOODSTORAGE8_5
		set_state closeup
		dialog NPC_TRACY_TRACY_FOODSTORAGE8_6
		dialog NPC_TRACY_TRACY_FOODSTORAGE8_7
		dialog NPC_TRACY_TRACY_FOODSTORAGE8_8
		dialog NPC_TRACY_TRACY_FOODSTORAGE8_9
		set_state verycloseup
		dialog NPC_TRACY_TRACY_FOODSTORAGE8_10
		get npc_reward
		set_state idle
		unlock_controls 1
	}
	tracy_foodstorage9 {
		lock_controls 1
		set_state blocking
		set_state closeup
		dialog NPC_TRACY_TRACY_FOODSTORAGE9_1
		dialog NPC_TRACY_TRACY_FOODSTORAGE9_2
		dialog NPC_TRACY_TRACY_FOODSTORAGE9_3
		dialog NPC_TRACY_TRACY_FOODSTORAGE9_4
		set_state zoomedout
		dialog NPC_TRACY_TRACY_FOODSTORAGE9_5
		dialog NPC_TRACY_TRACY_FOODSTORAGE9_6
		set_state closeup
		dialog NPC_TRACY_TRACY_FOODSTORAGE9_7
		dialog NPC_TRACY_TRACY_FOODSTORAGE9_8
		dialog NPC_TRACY_TRACY_FOODSTORAGE9_9
		set_state zoomedout
		dialog NPC_TRACY_TRACY_FOODSTORAGE9_10
		get npc_reward
		set_state idle
		unlock_controls 1
	}
	tracy_foodstorage10 {
		lock_controls 1
		set_state blocking
		set_state idle
		dialog NPC_TRACY_TRACY_FOODSTORAGE10_1
		dialog NPC_TRACY_TRACY_FOODSTORAGE10_2
		dialog NPC_TRACY_TRACY_FOODSTORAGE10_3
		dialog NPC_TRACY_TRACY_FOODSTORAGE10_4
		dialog NPC_TRACY_TRACY_FOODSTORAGE10_5
		dialog NPC_TRACY_TRACY_FOODSTORAGE10_6
		set_state zoomedout
		dialog NPC_TRACY_TRACY_FOODSTORAGE10_7
		dialog NPC_TRACY_TRACY_FOODSTORAGE10_8
		set_state closeup
		dialog NPC_TRACY_TRACY_FOODSTORAGE10_9
		dialog NPC_TRACY_TRACY_FOODSTORAGE10_10
		dialog NPC_TRACY_TRACY_FOODSTORAGE10_11
		set_state verycloseup
		dialog NPC_TRACY_TRACY_FOODSTORAGE10_12
		get npc_reward
		set_state idle
		unlock_controls 1
	}

	tracy_max_intro {//the 1st time you gain something after having max favor.
		lock_controls 1
		set_state blocking
		set_state zoomedout
		dialog NPC_TRACY_TRACY_MAX_INTRO_1
		dialog NPC_TRACY_TRACY_MAX_INTRO_2
		dialog NPC_TRACY_TRACY_MAX_INTRO_3
		set_state verycloseup
		dialog NPC_TRACY_TRACY_MAX_INTRO_4
		set_state closeup
		dialog NPC_TRACY_TRACY_MAX_INTRO_5
		dialog NPC_TRACY_TRACY_MAX_INTRO_6
		dialog NPC_TRACY_TRACY_MAX_INTRO_7
		get npc_reward
		set_state idle
		unlock_controls 1
	}

	tracy_max_repeating {
		do_random_sequence [tracy_max1, tracy_max2, tracy_max3, tracy_max4, tracy_max5]
	}
	
	tracy_max1 {//max1-5 is for when tracy is at max favor
		lock_controls 1
		set_state blocking
		set_state closeup
		dialog NPC_TRACY_TRACY_MAX1_1
		set_state verycloseup
		dialog NPC_TRACY_TRACY_MAX1_2
		set_state closeup
		dialog NPC_TRACY_TRACY_MAX1_3
		get npc_reward
		set_state idle
		unlock_controls 1
	}
	
	tracy_max2 {
		lock_controls 1
		set_state blocking
		set_state closeup
		dialog NPC_TRACY_TRACY_MAX2_1
		set_state verycloseup
		dialog NPC_TRACY_TRACY_MAX2_2
		set_state closeup
		dialog NPC_TRACY_TRACY_MAX2_3
		get npc_reward
		set_state idle
		unlock_controls 1
	}

	tracy_max3 {
		lock_controls 1
		set_state blocking
		dialog NPC_TRACY_TRACY_MAX3_1
		dialog NPC_TRACY_TRACY_MAX3_2
		dialog NPC_TRACY_TRACY_MAX3_3
		dialog NPC_TRACY_TRACY_MAX3_4
		get npc_reward
		set_state idle
		unlock_controls 1
	}

	tracy_max4 {
		lock_controls 1
		set_state blocking
		set_state closeup
		dialog NPC_TRACY_TRACY_MAX4_1
		dialog NPC_TRACY_TRACY_MAX4_2
		set_state zoomedout
		dialog NPC_TRACY_TRACY_MAX4_3
		set_state closeup
		dialog NPC_TRACY_TRACY_MAX4_4
		dialog NPC_TRACY_TRACY_MAX4_5
		set_state zoomedout
		dialog NPC_TRACY_TRACY_MAX4_6
		get npc_reward
		set_state idle
		unlock_controls 1
	}
	
	tracy_max5 {
		lock_controls 1
		set_state blocking
		set_state closeup
		dialog NPC_TRACY_TRACY_MAX5_1
		set_state verycloseup
		dialog NPC_TRACY_TRACY_MAX5_2
		set_state closeup
		dialog NPC_TRACY_TRACY_MAX5_3
		dialog NPC_TRACY_TRACY_MAX5_4
		set_state zoomedout
		dialog NPC_TRACY_TRACY_MAX5_5
		dialog NPC_TRACY_TRACY_MAX5_6
		set_state verycloseup
		dialog NPC_TRACY_TRACY_MAX5_7
		get npc_reward
		set_state idle
		unlock_controls 1
	}

	unknown {
		lock_controls 1
		set_state blocking
		dialog NPC_TRACY_UNKNOWN_1
		get npc_reward
		set_state idle
		unlock_controls 1
	}
	
	//Tracy unlock intros
	
	tracy_kaijufight {
		lock_controls 1
		set_state blocking
		set_state zoomedout
		dialog NPC_TRACY_TRACY_KAIJUFIGHT_1
		dialog NPC_TRACY_TRACY_KAIJUFIGHT_2
		set_state closeup
		dialog NPC_TRACY_TRACY_KAIJUFIGHT_3
		set_state zoomedout
		dialog NPC_TRACY_TRACY_KAIJUFIGHT_4
		dialog NPC_TRACY_TRACY_KAIJUFIGHT_5
		dialog NPC_TRACY_TRACY_KAIJUFIGHT_6
		dialog NPC_TRACY_TRACY_KAIJUFIGHT_7
		set_state closeup
		dialog NPC_TRACY_TRACY_KAIJUFIGHT_8
		set_state verycloseup
		dialog NPC_TRACY_TRACY_KAIJUFIGHT_9
		dialog NPC_TRACY_TRACY_KAIJUFIGHT_10

		set_state idle
		unlock_controls 1
	}
		//default  happy  veryhappy  sad  angry  veryangry
        //questioning  whispering  pondering  mocking
        //inlove  confused  paranoid  shocked  scared  spacedout
}
```

---

