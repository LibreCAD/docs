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




Command Line Calculator
-----------------------

The command line also offers a simple calculator for performing quick calculations without leaving the application.  To use the command line as a math expression calculator type "cal" and the math expression.  Some examples:

   cal 1+1
   cal sin(pi/6)
   cal log(2)

