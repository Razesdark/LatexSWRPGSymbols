# LatexSWRPGSymbols
Macros to simplify inline dice and other symbols as well as skillchecks when writing Star Wars RPG modules or adventures.

# Installation
To use the package copy ``icons.tex`` and the ``icons`` folder to the root of the tex document folder.
Then add the following lines to your master document
```
 \usepackage{tikz}
 \usepackage{ifthen}
 \usepackage{keycommand}
 \input{icons}
```

# Using the package
This package allows you to inline add the most used dice and other symbols inside of your document. 

__The currently supported dices__
  * ``\dability{n}`` - ![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_ability.png?raw=true) 
  * ``\dproficiency{n}`` - ![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_prof.png?raw=true)
  * ``\ddifficulty{n}`` - ![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_difficulty.png?raw=true)
  * ``\dchallenge{n}`` - ![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_challenge.png?raw=true)
  * ``\dboost{n}`` - ![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_boost.png?raw=true)
  * ``\dsetback{n}`` - ![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_setback.png?raw=true)
  * ``\dforce{n}`` - ![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_force.png?raw=true)
  
  For example, if you want to show 3 dice (![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_ability.png?raw=true)![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_ability.png?raw=true)![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_ability.png?raw=true)) can be added using the command ``\dability{3}``.

__The currently supported other symbols__
* ``\success{n}`` - ![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/sym_success.png?raw=true)
* ``\failure{n}`` - ![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/sym_failure.png?raw=true)
* ``\advantage{n}`` - ![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/sym_advantage.png?raw=true)
* ``\threat{n}`` - ![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/sym_threat.png?raw=true)
* ``\triumph{n}`` - ![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/sym_triumph.png?raw=true)
* ``\despair{n}`` - ![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/sym_despair.png?raw=true)

# The skillcheck command
The skillcheck command is a way to quickly add skillchecks to the document. For example, if you want to add an medium _computer check_. You can do that with the command ``\skillcheck[difficulty=2]{Medium}{computer check}``. That will add the text  

__Medium(![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_difficulty.png?raw=true)![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_difficulty.png?raw=true)) computer check__

to your document, in line with many of the skillchecks listed in the core rule book. 
You can mix and match several types of dice, for example an opposed charm check  ``\skillcheck[difficulty=1,challenge=2,setback=1]{Opposed}{charm check}`` which would look like this:

__Opposed(![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_difficulty.png?raw=true)![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_challenge.png?raw=true)![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_challenge.png?raw=true)![Ability](https://github.com/Razesdark/LatexSWRPGSymbols/blob/master/icons/dice_setback.png?raw=true)) charm check__

