.. User Manual, LibreCAD v2.2.x


.. _commandline:

Using the Command Line
======================

The command line is an alternative to using the mouse and selecting tools from the menus or toolbars.  Using the  command line can be faster and/or more precise than drawing using exclusively with a mouse.  LibreCAD is designed with emphasis on mouse input and at the moment and not all tools are available with a command.  The available commands are listed in the :ref:`Drawing Tools <tools>` reference.

Any key stroke will activate the command line.  Once active, the command prompt ("Command:", above of where input appears) turns blue.  A mouse click on the drawing window will return the focus.


:: continue here


Pressing the [Esc] will cancel the current command.

It is possible to enter a partial command, like "li" for line and press [Tab] to have the command completed to "line". If you type too short a segment of a command, such as "l" and press [Tab], the command output will show "ch, circle, cut" because the command segment you typed in isn't unique.

Many commands prompt you on the command line asking for further input. They tell you what input they expect, a point for example, and list other possibilities in the square bracket.  For example if you type command polyline and draw at least two segments you get prompted "Specify next point" or [undo/close]. This means that the program is expecting a point (from the command line or by clicking on drawing area), or you can select the Undo or Close option. You can do that by typing on the command line or by clicking on buttons on the context toolbar called Tool Options.

When there is some value already set and valid, for example when you use command offset, the current value is in sharp brackets, like so: Specify distance <5> or select entity or [Through]. So you see that value for offset is 5 and you can either set a new value by typing it into the command line or using the Tool Options toolbar or you can start drawing parallel entities.

Commands have a long and a short format. For example the command for drawing a line has three formats\:

    line
    li
    l

To use the **two** letter format li you do not have to activate the commandline. Just type "li" and LibreCAD displays the prompt.  If you wish to continue drawing with just mouse input, you click on drawing to enter the point, or click on the tools palette to select the snap mode or whatever.


Clear the Commands Window
-------------------------

To clear the list of commands from the command window - type "clear" in the command line.


Drawing Entities
----------------

Using the command line replace the need to select tools for m the menus or toolbars.  By using the command line, it is possible to switch tools, change snaps or the view quickly.


Command Variables
-----------------

Multi-command input can be assigned to a variable; values can also contain variables (they are read recursively)

    a=ci;0,0;10
    b=ci;10,0;10
    c=\a;\b;kill
    \c

A variable file can loaded from the command line dock using the drop down or be set to load at startup via Application Preferences -> Paths -> Variable File.


Calculator
----------

The command line also offers a simple calculator for performing quick calculations without leaving the application.  To use the command line as a math expression calculator type "cal" and the math expression.  Typing "cal" again will toggle the calculator mode off.

.. csv-table:: 
   :header: "Name", "Function / Operation", "Usage"
   :widths: 20, 60, 30 
    
    "\+", "addition", "x+y"
    "\-", "subtraction", "x-y"
    "\*", "multiplication", "x*y"
    "/", "division", "x/y"
    "^", "raise x to the power of y", "x^y"
    "sin", "sine function", "sin(x)"
    "cos", "cosine function", "cos(x)"
    "tan", "tangens function", "tan(x)"
    "asin", "arcus sine function", "asin(x)"
    "acos", "arcus cosine function", "acos(x)"
    "atan", "arcus tangens function", "atan(x)"
    "sinh", "hyperbolic sine function", "sinh(x)"
    "cosh", "hyperbolic cosine", "cosh(x)"
    "tanh", "hyperbolic tangens function", "tanh(x)"
    "asinh", "hyperbolic arcus sine function", "asinh(x)"
    "acosh", "hyperbolic arcus tangens function", "acosh(x)"
    "atanh", "hyperbolic arcur tangens function", "atanh(x)"
    "log2", "logarithm to the base 2", "log2(x)"
    "log10", "logarithm to the base 10", "log10(x)"
    "log", "logarithm to base e (2.71828...)", "log(x)"
    "ln", "logarithm to base e (2.71828...)", "ln(x)"
    "exp", "e raised to the power of x", "exp(x)"
    "sqrt", "square root of a value", "sqrt(x)"
    "sign", "sign function -1 if x<0; 1 if x>0", "sign(x)"
    "rint", "round to nearest integer", "rint(x)"
    "abs", "absolute value", "abs(x)"
    "min", "min of all arguments", "min(x, y, ...n)"
    "max", "max of all arguments", "max(x, y, ...n)"
    "sum", "sum of all arguments", "sum(x, y, ...n)"
    "avg", "mean value of all arguments", "avg(x, y, ...n)"

http://beltoforion.de/article.php?a=muparser


Examples of using the command line calculator::

   1+1  =  2
   sin(pi/6)  =  0.5
   sqrt(3^2+4^2)  =  5


Other
-----

A new button with a drop-down menu has been added to the command-line
Keycode mode was rewritten and the toggle is now accessed by the new command-line button.  Toggling keycode mode no longer requires restarting LibreCAD. If a 2 character command is not recognized, you can continue with a longer command.


Multi-command input can be separated by semicolons: ci;0,0;10

Command files (command input separated by newlines) can be loaded from the new command-line button

Multi-command input can be assigned to a variable; values can also contain variables (they are read recursively)::

a=ci;0,0;10
b=ci;10,0;10
c=\a;\b;kill
\c




Using the Command line
~~~~~~~~~~~~~~~~~~~~~~

Press the [Space] or [Ctrl]+m to activate the command line.  When the command line is active the **Command:** prompt (left of where input appears) turns blue.  Press [Esc] to leave the command line and a second [Esc] to cancel the current operation.

It is possible to enter a partial command, like "cir" and press [Tab] to have the command completed to circle. If you type too short a segment of a command, such as c and press [Tab], the command output will show "ch, circle, cut" because the command segment you typed in isn't unique.

Many commands prompt you on the command line asking for further input. They tell you what input they expect - a point for example - and list other possibilities in the square bracket. For example if you type command polyline and draw at least two segments you get prompted Specify next point or [undo/close]. This means that the program is expecting a point (from the command line or by clicking on drawing area), or you can select the Undo or Close option. You can do that by typing on the command line or by clicking on buttons on the context toolbar called *Tool Options*.

When there is some value already set and valid, for example when you use command offset, the current value is in sharp brackets, like so: Specify distance <5> or select entity or [Through]. So you see that value for offset is 5 and you can either set a new value by typing it into the command line or using the Tool Options toolbar or you can start drawing parallel entities.

To use the two letter format li you do not have to activate the commandline. Just type "li" and LibreCAD displays the prompt. To continue drawing with just mouse input, click on drawing to enter the point, or click on the tools palette to select the snap mode or 


Clear commands from commands window
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To clear the list of commands from the command window - type "clear" in the command line. 


Edit commands
~~~~~~~~~~~~~

Kill the command has no further prompt
This command when called on the command line kills or clears all actions inputed at the command line. At times when you have entered a command, zoomed the drawing, used the command line repetitively besides hitting the ESC key to exit out of the loaded commands you can run the kill command to clear the cache. It does not seem to do anything but if you open up the command line window you will see it clear out all active commands. Most of the time you would not need to use this command but there are times when it seems like the app gets confused at what action to take, using the kill command clears out everything and cleans the slate.

You can use Ctrl+z and Ctrl+y to undo and redo changes. This is quicker and more convenient than using the next two commands.
Undo

undo
u
the command has no further prompt
You type undo on the commandline. LibreCAD reverts the last change you have made to the drawing. You can repeat the undo command, and every time you use it it takes you one step back through the history of your drawing/edit. Unlike other programs (AutoCAD) the undo command doesn't revert the zoom and pan commands.
Redo

redo
r
the command has no further prompt
You type undo on the commandline. LibreCAD cancels the last undo you have made. When you use the undo, it is easy to do one step too much undo. Using redo you can revert undo. This lets you go back and forth in the edit history. 

Command Line Calculator
~~~~~~~~~~~~~~~~~~~~~~~

Type "cal", use command line as a math expression calculator. Some examples:


The command line has a built in calculator that can be accessed with the cal command.

Constants:

    pi = 3.14159265359

Operators:

addition:
cal 6+5

subtraction:
cal 6-5

multiplication:
cal 6*5

division:
cal 6/5

six to the fifth power:
cal 6^5

Functions:

square root:
cal sqrt(5)
cal sqrt(3^2 + 4^2)

average:
cal avg(6,5)

Trigonometric functions:

Note these functions take radians.
degrees*pi/180 = radians

sine:
cal sin(6*pi/180)

cosine:
cal cos(6d)

tangent:
cal tan(6deg)

   cal 1+1
   cal sin(pi/6)
   cal log(2)

