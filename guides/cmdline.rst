.. User Manual, LibreCAD v2.2.x


.. _cmdline:

The Command Line
================

LibreCAD's command line offers users an alternative to using the mouse to select tools and draw.  Using the keyboard to select tools and enter coordinates can provide greater speed and accuracy when creating drawings.  The command line provides other useful features not available using the mouse:

   - Multi-command input
   - A calculator

The command line is displayed in its own :ref:`dock widget <widget-cmdLine>` and consists of three components

   1. Command prompt.
   2. Command output window.
   3. Button that displays a drop-down menu that includes:

      - Toggle *Keycode Mode* off or on.
      - Load a Command file.
      - Paste commands.
      - Toggle whitespace use within the command text.


Command Line Functions
----------------------

The commands available to use are shown in the :ref:`Drawing Tools <tools>` reference.  Additional prompts will indicate the next input required such as coordinates or an action.  The command line is activated by in a variety of ways:

   1. Start typing any command, e.g. li, rect, etc. and then [Enter] or the [Space bar].
   2. Press the [Space bar], type any command and then [Enter] or the [Space bar].
   3. Press [Ctrl + M], any command and then [Enter] or the [Space bar].
   4. With the *Keycode Mode* on, type a **two letter** command, e.g. li, ci.  Pressing [Enter] is not required.

When the command line is activated the prompt above the input text box, initially showing "Command:", turns blue.  After typing a command the prompt will indicate the next input required such as coordinates and / or the next action available.  For example, after drawing at least two segments of a line the prompt reads "Specify next point or [close/undo]".  LibreCAD is expecting another set of coordinates to be entered, or the shape (with a minumum of two segments) can be closed or the last actions can be reversed.  "Close" or "undo" can be entered on the command line or by clicking on buttons on the :ref:`Tool Options<tools>` toolbar.  For example, to draw a square using the "2 points line" tool from the command line:

::

   Command:
   li
   Specify first point
   0,0
   Specify next point
   @10,0
   Specify next point or [close/undo]
   @0,10
   Specify next point or [close/undo]
   @-10,0
   close

.. tip::
   In addition to the comma separated :ref:`coordinates<coordinates>`, *relative* coordinates can also be entered using the numeric keypad using the format *X..Y*, i.e. typing *10..20* is equivalent to *@10,20*.  Using the two decimals is faster than typing the comma.

   The *Keycode Mode* permits the use of **two letter** commands and eliminates the need to press [Enter] after typing the command. 

   Pressing the [Space bar] is an alternative to pressing [Enter] after each command.

   Pressing [c] or [u] followed by [Enter] can be used instead of typing "close" or "undo".

*Tab completion* can be used on the command line when entering commands.  Enter a partial command such as "cir" followed by press [Tab] will complete the command to "circle".  If text entered is not unique to a single command the command output will show all the possible commands starting with the text provided.  For example, typing [c] and pressing [Tab] will list "circle", "circle2", "circle3", "circlecr" and "cut" in the command output.

The available commands are shown in the :ref:`Tools<tools>` reference.  Many of the commands have multiple forms.  For exmple the *2 points* line tools can be selected on the command line by typing "l", "li" or "line".  Some tools will provide command line prompts in addition to the **Tool Options**.  For example the "Parallel" line tools displays:

   - a **Tool Options** toolbar: |tlopt12|
   - A command prompt: '''Specify Distance <10> or select entity or [through]'''

Either can be used.

.. Next edit:
*************

When there is some value already set and valid, for example when you use command offset, the current value is in sharp brackets, like so: Specify distance <5> or select entity or [Through]. So you see that value for offset is 5 and you can either set a new value by typing it into the command line or using the Tool Options toolbar or you can start drawing parallel entities.


Clear the Command Line
~~~~~~~~~~~~~~~~~~~~~~

To clear the list of commands from the command output window - type "clear" in the command line.


Multi-Command Input
-------------------

Multi-command input can be separated by semicolons: ci;0,0;10
Command files (command input separated by newlines) can be loaded from the new command-line button
Multi-command input can be assigned to a variable; values can also contain variables (they are read recursively)

::

   a=ci;0,0;10
   b=ci;10,0;10
   c=\a;\b;kill
   \c

A variable file can be set to load at startup via Application Preferences -> Paths -> Variable File



Calculator
----------

The 'cal' command now toggles a calculator mode.

"cal", use command line as a math expression calculator. Some examples:

   cal 1+1
   cal sin(pi/6)
   cal log(2)

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


Command Alias File
------------------

You can define command aliases by changing the alias configuration file and restarting LibreCAD.

Linux:

    $HOME/.local/share/data/LibreCAD/librecad.alias

Windows:

    C:\Users\[USERNAME]\AppData\Local\LibreCAD\librecad.alias

Mac:

    $HOME/Library/Application Support/LibreCAD/librecad.alias



.. images:

.. |tlopt12| image:: /images/toolOptions/toLineParlOff.png
            :height: 32
            :width: 231
