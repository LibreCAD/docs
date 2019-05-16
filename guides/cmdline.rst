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


Command Line Functions
----------------------

The commands available to use are shown in the :ref:`Drawing Tools <tools>` reference.  The command line is activated by in a variety of ways:

   1. Start typing any command, e.g. li, rect, etc. and then [Enter] or the [Space bar].
   2. Press the [Space bar], type any command and then [Enter] or the [Space bar].
   3. Press [Ctrl + M], any command and then [Enter] or the [Space bar].
   4. With the *Keycode Mode* on, type a **two letter** command, e.g. li, ci.  Pressing [Enter] is not required.

When the command line is activated the prompt above the input text box, initially showing "Command:", turns blue.  After typing a command the prompt will indicate the next input required such as coordinates and / or the next action available.  Pressing [Esc] will cancel the current action and pressing it a second time will cancel the operation.

For example, when using the **2 Points** line tool the first prompt shows "Specify first point" and the second "Specify next point".  After drawing at least two segments of a line the next prompt reads "Specify next point or [close/undo]".  LibreCAD is expecting another set of coordinates to be entered, or the shape (with a minimum of two segments) can be closed or the last actions can be reversed.  "Close" or "undo" can be entered on the command line or by clicking on buttons on the :ref:`Tool Options<tools>` toolbar.  For example, to draw a square using the "2 Points line" tool from the command line:

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
   In addition to the comma separated coordinates`, :ref:`relative* coordinates<coordinates> can also be entered using the numeric keypad using the format *X..Y*, i.e. typing *10..20* is equivalent to *@10,20*.  Using the two decimals is faster than typing the comma.

   The *Keycode Mode* permits the use of **two letter** commands and eliminates the need to press [Enter] after typing the command. 

   Pressing the [Space bar] is an alternative to pressing [Enter] after each command.

   Pressing [c] or [u] followed by [Enter] can be used instead of typing "close" or "undo".


*Tab completion* can be used on the command line when entering commands.  Enter a partial command such as "cir" followed by press [Tab] will complete the command to "circle".  If text entered is not unique to a single command the command output will show all the possible commands starting with the text provided.  For example, typing [c] and pressing [Tab] will list "circle", "circle2", "circle3", "circlecr" and "cut" in the command output.

The available commands are shown in the :ref:`Tools<tools>` reference.  Many of the commands have multiple forms.  For example the *2 Points* line tools can be selected on the command line by typing "l", "li" or "line".  Many tools display the **Tool Options** toolbar when selected.  Some tools will also provide command line prompts in addition to the **Tool Options**.  For example the "Parallel" line tools displays:

   - a command prompt: ``Specify Distance <10> or select entity or [through]``
   - a **Tool Options** toolbar: |tlopt12|

Either can be used can be used to enter new values.  The current value on the command line is displayed in angle brackets as shown above.  To change the value from the command line, type the value and press [Enter].

The command output window displays the command history, error messages, and other output (see **Calculator** below).  The text in the output window can be copied simply by highlighting it.  The text is automatically copied to the clipboard and can be pasted into another document.  The output window can be cleared of all text by typing "clear" in the command line.


Command Aliases
---------------

As previously noted many of the commands in LibreCAD have multiple forms.  The long *untranslated* form is the native command and the short forms are *aliases* to the long form.  For example, "l" and "li" are aliases to "line".  The aliases are defined in the ``librecad.alias`` configuration file.
The format of the configuration file is ``<alias>[Tab]<command-untranslated>``.  The default aliases for the **2 Points** line appears as:

::

   ...
   l	line
   li	line
   ...

Aliases can be added or modified to suit users' preferences.  The file is found in the following locations:

   - **Linux**: $HOME/.local/share/LibreCAD/LibreCAD/librecad.alias
   - **Windows**: C:\\Users\\ *{UserName}*\\AppData\\Local\\LibreCAD\\librecad.alias
   - **macOS**: $HOME/Library/Application Support/LibreCAD/librecad.alias

.. note:: Only change the alias and *not* the long *untranslated* form.


Multi-Command Input
-------------------

Command input can be combined and entered on a single line by separating the commands and other input with semicolons.  Entering ``li;0,0;10..0;0..10;-10..0;c;k`` on the command line will draw a 10 x 10 square.  

Command input can also be loaded from text files.  Entering the commands and other input into a text file separating each with a newline.  For example, create a text file and enter the following commands:

::

   li
   0,0
   @10,0
   @0,10
   @-10,0
   c
   k

Save the file as "multiCmd.txt". In LibreCAD select "Load Command File" from the the drop-down menu by clicking the command line button (lower right corner of the **Command Line Dock**).  Locate the file and click the **Open** button.  The above commands will draw a 10 x 10 square.

Multi-command input can be assigned to a variable and variables can also contain other variables (they are read recursively):

::

   a=ci;0,0;10
   b=ci;10,0;10
   c=\a;\b;kill
   \c

Enter each line of the text above on the command line.  When ``\c`` is entered, two overlappiing circles with a radius of 10 are drawn.  The ``\`` character is an escape character that allows the command line to interpret the variable name as an action.  In the above example ``\c`` expands to ``ci;0,0;10;ci;10,0;10;kill``.

A "variable file" can be set to load at startup via :ref:`Application Preferences<app-prefs>` **-> Paths -> Variable File**.  Save the first three line of the above example to a text file and configure the path to the text file.  Restart LibreCAD and when ``\c`` is entered at the command line the two circles are drawn.


Calculator
----------

LibreCAD includes a built-in calculator that uses the command line interface.  Typing "cal" on the command line toggles the *calculator mode* on and off.  With the calculator mode on, math expressions typed on the command line will display the results in the output window, e.g. typing ``1+1`` displays ``1+1 = 2`` in the output window.  Some other examples are:

|   ``sqrt(3^2 + 4^2) = 5``
|   ``sin(pi/6) = 0.5``
|   ``6^5 = 7776``

If the cal mode is *off* entering a math expression will result in an error message such as ``Unknown command: 1+1``.

A complete list of operators and functions can be found in the :ref:`appendix<calc>`.

.. note:: The constant pi is defined in LibreCAD as 3.14159265359.

.. note:: Trigonometric functions use radians (radians = degrees*pi/180).


.. images:

.. |tlopt12| image:: /images/toolOptions/toLineParlOff.png
            :height: 32
            :width: 231
