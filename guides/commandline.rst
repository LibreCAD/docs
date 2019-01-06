.. User Manual, LibreCAD v2.2.x


.. _commandline:

Using the Command Line
======================

The command line is an alternative to using the mouse and selecting tools from the menus or toolbars.  The command line can be faster and/or more precise than drawing using exclusively a mouse.  LibreCAD is designed with emphasis on mouse input and at the moment not all tools are available with a command.  The available commands are listed in the :ref:`Drawing Tools <tools>` reference.

You can press the Spacebar or [Ctrl]-M to activate the command line.  Once it is active, the command prompt ("Command:", left of where input appears) turns blue.  So now when you press a key you are entering commands.

Press the [Esc] key to leave the command line and another [Esc] to cancel what you have written on the command line.

It is possible to enter a partial command, like "cir" and press [Tab] to have the command completed to circle. If you type too short a segment of a command, such as "c" and press [Tab], the command output will show "ch, circle, cut" because the command segment you typed in isn't unique.

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
   :widths: 30, 60, 50 
    
    "+", "addition", "x+y"
    "-", "subtraction", "x-y"
    "*", "multiplication", "x*y"
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

   cal *turns the calculator mode* On
   1+1  *returns the result of*  2
   sin(pi/6)  *returns the result of*  0.5
   sqrt(3^2+4^2)  *returns the result of*  5
   cal *turns the calculator mode* Off


Other
-----

 A new button with a drop-down menu has been added to the command-line
    Keycode mode was rewritten and the toggle is now accessed by the new command-line button.

Toggling keycode mode no longer requires restarting LibreCAD. If a 2 character command is not recognized, you can continue with a longer command.


    Multi-command input can be separated by semicolons: ci;0,0;10
    Command files (command input separated by newlines) can be loaded from the new command-line button
    Multi-command input can be assigned to a variable; values can also contain variables (they are read recursively)

a=ci;0,0;10
b=ci;10,0;10
c=\a;\b;kill
\c



