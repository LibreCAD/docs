.. User Manual, LibreCAD v2.2.x


.. _cmdline:

Using the Command Line
======================

LibreCAD's command line offers users an alternative to using the mouse to draw.  Using the keyboard to select tools and enter coordinates can provide greater speed and accuracy when creating drawings.  The command line provides other usefull feature not available using the mouse:

   - a Calculator
   - 

Using the Command line

You can press the Space-bar or [Ctrl + M] to activate the command line.

When the command line is active the "Command:" (left of where input appears) turns blue. So now when you press a key you are entering commands.

You press the Escape key to leave the command line and another Escape to cancel what you have written on the command line.

It is possible to enter a partial command, like cir and press Tab to have the command completed to circle. If you type too short a segment of a command, such as c and press Tab, the command output will show "ch, circle, cut" because the command segment you typed in isn't unique.

Many commands prompt you on the command line asking for further input. They tell you what input they expect - a point for example - and list other possibilities in the square bracket. For example if you type command polyline and draw at least two segments you get prompted Specify next point or [undo/close]. This means that the program is expecting a point (from the command line or by clicking on drawing area), or you can select the Undo or Close option. You can do that by typing on the command line or by clicking on buttons on the context toolbar called Tool Options.

When there is some value already set and valid, for example when you use command offset, the current value is in sharp brackets, like so: Specify distance <5> or select entity or [Through]. So you see that value for offset is 5 and you can either set a new value by typing it into the command line or using the Tool Options toolbar or you can start drawing parallel entities.

Every command I describe below has a long format and a short format. For example the command for drawing a line has three formats:
line
li
l

To use the two letter format li you do not have to activate the commandline. Just type li and LibreCAD displays the prompt. If you wish to continue drawing with just mouse input, you click on drawing to enter the point, or click on the tools palette to select the snap mode or whatever.

Clear commands from commands window

To clear the list of commands from the command window - type "clear" in the command line.

Drawing
-------


Drawing entities
Drawing a point

point
po
Specify location

You type point or po on the command line. LibreCad prompts you to with "Specify Location".

After selecting any desired snapping options on the main toolbar you can respond by clicking with the mouse on the drawing area to enter points. Or you can produce points by entering into the command line:

    10,20[enter] - to place point at coordinates x=10, y=20 from the origin - point x=0, y=0
        @30,40[enter] - to place point at coordinates that are at distance x=30, y=40 from the last drawn point. So x=10+30=40 and y=20+40=60.

    50<45[enter] - to place point at the distance 50 from origin, at 45 angle degree. The positive x axis is at 0 degrees, the positive y axis is at 90 degrees. So degrees are measured at counter clockwise direction from horizontal.

    @60<15[enter] - to place point at the distance 60 at 15 angle degree from the last drawn point.

Drawing a line

line
li
l
Specify first point
Specify next point
Specify next point or [undo]

Produce points as described in the point section. After producing a line segment, any following points create a line segment with the point that precedes them.

If there are at least two segments drawn, you can close the line (draw a segment to the point where you started) by entering close into the command line. To finish drawing lines you press [Esc]

All line segments created can be selected individually. With Polyline all seg

Calculator
----------

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


https://wiki.librecad.org/index.php?title=A_short_manual_for_use_from_the_command_line
https://wiki.librecad.org/index.php?title=LibreCAD_users_Manual#Using_Command_Line
