**What's New with pydice?**
===========================

New in pydice 3.13.0
--------------------
**S10** rolls return the number of successes (a 6 or higher was rolled on a die). More than one die can be rolled together as a dice pool, such as 7S10 (for rolling seven S10 dice).


New in pydice 3.12.9

**S6** rolls return the number of successes (a 6 was rolled on a die). More than one die can be rolled together as a dice pool, such as 5S6 (for rolling five S6 dice).


New in pydice 3.12.8

Just an incremental update to be made aware of Python 3.11.6.


New in pydice 3.12.7

Fixed crash caused when the amount of high or low number of dice to keep was missing.


New in pydice 3.12.6

FATE rolls were using the wrong random(). Fixed.


New in pydice 3.12.5

**EHEX** rolls will generate the extended hexadecimal values of **0 - Z** used in Traveller5. These are strings rather than integers.


New in pydice 3.12.4

The new **D01** roll generates values **0 - 1**.

.. note::
  The older **D1** roll has been deprecated. This will give a ``WARNING``.


New in pydice 3.12.3

**HEX** dice rolls have been added to generate values **0 - F**. These are strings rather than integers.


New in pydice 3.12.2

**D09**, **D100**, **D099**, **D1000**, and **D0999** rolls have better ``DEBUG`` logging now.


New in pydice 3.12.1

**SICHERMAN** dice rolls have been added.


New in pydice 3.12.0

**pydice** has been updated for **Python 3.11.0**.


New in pydice 3.11.8

**FLUX, GOODFLUX**, and **BADFLUX** will ignore **dice roll modifiers**.

.. note::
   Dice roll modifiers are no longer ignored when using **H** or **L**.


New in pydice 3.11.7

**pydice** now checks for version of Python installed. Will display
a warning on screen and in the log.


New in pydice 3.11.6

Error-trapping for invalid dice modifiers now.


New in pydice 3.11.5

The new **D1** roll generates a range of **0 - 1**.

**D2** rolls now generate a range of **1 - 2**.


New in pydice 3.11.0

**H** and **L** have been added for keeping higher or lower dice.

``roll('3D6H2')`` -- roll 3D6 and keep the higher 2 dice.

``roll('2D20L1')`` -- roll 2D20 and keep the lower die.

.. note::
   Dice roll modifiers are ignored when using **H** or **L**.


New in pydice 3.10.6

Comments can be entered with die rolls, such as ``roll('2D8 # weapon damage')``
Any comments used will appear in the ``pydice.log`` file.


New in pydice 3.10.5

The **D666** roll has been added. The result is D6*100 + D6*10 + D6.


New in pydice 3.10.0

The **D0999** roll has been added. It generates a range of **0 - 999**.

The **D1000** roll has been added. It generates a range of **1 - 1000**.


New in pydice 3.9.0

**pydice** now uses ``int(random() * n + 1)`` instead of ``randint(1, n)`` to generation its random numbers much faster.


New in pydice 3.8.0

PyDiceroll is now **pydice**. PyDiceroll has been discontinued.
Modified **DEBUG** level logging for **BOON**, **BANE**, **ADVANTAGE**, and **DISADVANTAGE** rolls.
The newly introduced default roll performs a **2D6** roll.
Added error-trapping when performing **MINMAXAVG** rolls at the CMD prompt.


New in PyDiceroll 3.7.2

**MINMAXAVG** calculates negative averages correctly now.


New in PyDiceroll 3.7.1

A new secret roll has been added. This is a beta test of the Fate roll type where dice mods can be added. As well as number of Fate dice to roll.


New in PyDiceroll 3.7.0

**ADVANTAGE** and **DISADVANTAGE** rolls, for d20 systems, are now do-able.


New in PyDiceroll 3.6.0

PyDiceroll no longer requires **colorama**.


New in PyDiceroll 3.5.0

More than one **D09** can be rolled at a time now. Added to the **MINMAXAVG** list.


New in PyDiceroll 3.4.0

The **MINMAXAVG** roll has been added. Just doing:

>>> roll('MINMAXAVG')

will output the Min, Max, and Averages for various
rolls. Mostly for testing. Nothing is returned from this roll. So print or variable assignment is not needed.

.. figure:: minmaxavg.png


New in PyDiceroll 3.3.1

Fixed error if non-numbers are entered.


New in PyDiceroll 3.3.0

Input errors for ``roll()`` will now return a value of -9999 instead of 0.


New in PyDiceroll 3.2.1

New **D44** and **D88** rolls have been added. These are table rolls, similar to the **D66** roll.


Parsing

The ``roll()`` function has improved parsing that allows for spaces from other program sources. Error-checking understands this
and will even check for negative numbers of dice. This improved feature works whether **PyDiceroll** is being used in a Python
program or at a CMD prompt.


Refactored for Python 3.9

**PyDiceroll's** code has been updated from 2.5 to 3.9 standards.

The **D5** has been added to **PyDiceroll**. It is basically a **D10** divided by 2, much like how the **D3** die is a **D6** that is divided by 2.
