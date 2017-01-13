# LatexSWRPGSymbols
This project has been my attempt to make a latex template similar to the SWRPG books from Fantasy Flight. Built to serve my  own needs, i've primarily for Force and Destiny, starting as a simple icon pack for inline icons, it quickly was expanded to text boxes, backgrounds and similar.
# Installation
To use the package copy ``swrpg.sty``, the ``lib/`` folder, as well as the ``images/``folder to the root of the tex document.
Then add the following lines to your master document
```
 \usepackage{swrpg}
```

# Icons
This package allows you to inline add the most used dice and other symbols inside of your document. 

__The currently supported dices__
  * ``\dability{n}`` - ![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_ability.png?raw=true) 
  * ``\dproficiency{n}`` - ![Proficiency](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_prof.png?raw=true)
  * ``\ddifficulty{n}`` - ![difficulty](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_difficulty.png?raw=true)
  * ``\dchallenge{n}`` - ![challenge](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_challenge.png?raw=true)
  * ``\dboost{n}`` - ![boost](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_boost.png?raw=true)
  * ``\dsetback{n}`` - ![setback](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_setback.png?raw=true)
  * ``\dforce{n}`` - ![f](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_force.png?raw=true)
  * ``\dforce{n}`` - ![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_force.png?raw=true)  
  For example, if you want to show 3 dice (![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_ability.png?raw=true)![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_ability.png?raw=true)![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_ability.png?raw=true)) can be added using the command ``\dability{3}``.

__The currently supported result symbols__
* ``\success{n}`` - ![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/sym_success.png?raw=true)
* ``\failure{n}`` - ![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/sym_failure.png?raw=true)
* ``\advantage{n}`` - ![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/sym_advantage.png?raw=true)
* ``\threat{n}`` - ![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/sym_threat.png?raw=true)
* ``\triumph{n}`` - ![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/sym_triumph.png?raw=true)
* ``\despair{n}`` - ![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/sym_despair.png?raw=true)
* ``\lforce{n}`` - ![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/sym_lightforce.png?raw=true)
* ``\dforce{n}`` - ![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/sym_darkforce.png?raw=true)


# The skillcheck command
The skillcheck command is a way to quickly add skillchecks to the document. For example, if you want to add an medium _computer check_. You can do that with the command ``\skillcheck[difficulty=2]{Medium}{computer check}``. That will add the text  

__Medium(![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_difficulty.png?raw=true)![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_difficulty.png?raw=true)) computer check__

to your document, in line with many of the skillchecks listed in the core rule book. 
You can mix and match several types of dice, for example an opposed charm check  ``\skillcheck[difficulty=1,challenge=2,setback=1]{Opposed}{charm check}`` which would look like this:

__Opposed(![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_difficulty.png?raw=true)![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_challenge.png?raw=true)![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_challenge.png?raw=true)![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_setback.png?raw=true)) charm check__

# Background images
The odd and even backgrounds used are ``images/bf_odd.jpg`` and ``images/bg_even.jpg``. There are some other files in the directory that could be used instead, but that would require you to manually adjust the page numbers.


# Stats
I also added some macros that I use in character creation for stats. ``\stats{STR}{AGI}{INT}{CUN}{WILL}{PRES}`` and ``\secondarystats[soak=,wound=,strain=,mdef=,rdef=]``. 

I also made some simple macros for a skill grid. Here is an example on how it is used 
``
\statsgrid{
 	\hline
 	\statentry{Skills}{
		\skentry{Brawl}{+3}
		\skentry{Resilience}{+4}
		\skentry{Perception}{+2} 
		\skentry{Survival}{+2}	
 	}
 	\hline
 		\statentry{Talents}{\skentry{Adversary}{1}}
 	\hline
 		\statentry{Abilities}{
 			\equipmententry{Flamebreath}{Described below}
 			\equipmententry{Screech}{Described below}
 			\equipmententry{Immolation Aura}{Described Below}
 		}
 		
 	\hline
 	\statentry{Equipment}{
		\equipmententry{Teeth}{Brawl; Engaged \\ Dmg: 6; Crit; 3; Stun 1}
		\equipmententry{Feelers}{Ranged(Light); Medium \\ Dmg: 3, Crit: 3; Poison 1}
		\equipmententry{Flamebreath}{Ranged(Light); Medium \\ Dmg: 8, Crit: 4; Limited Ammo 1}
 	}
 	\hline
 }
``

The ``\statsgrid{}`` holds all the data in the table. Each entry in the table should be an ``\statentry{Name}{Data}`` and if you need to list things within the statentry you can either use ``\equipmententry{Name}{Data}`` or ``\skentry{Name}{Data}``. 
``\equipmententry`` will let Name be bolded, and put Data on the next line, whilst ``skentry`` will be smaller text and on one line. So its mostly useful for skills.

# Tables
This is currently lacking a lot of functionality, It is currently a 2 row table available using ``\begin{swtable}``, ``\end{swtable}``.

# Boxes
You have two enviroments you can use to make a red(ment for read text) and black(tips, tricks) box. ``\begin{swredbox}``, ``\begin{swblackbox}`` will create either of them.

# Frontpage
The ``\swfrontpage{image}``, will create a frontpage and a linebreak. You need to make sure the image works cause its very unflexible atm.
