.. _widgets: 

Dock Widgets
=============

Dock widgets serve two purposes; they provide alternative method to access drawing tools, and additional tools or features (Block List, Command Line, Layer List, Library Browser, and Pen Wizard).

Dock widgets are available for these :ref:`drawing tools <tools>`: Circle, Curve, Dimension, Ellipse, Info, Line, Modify, and Polyline.


Dock Widget Areas
-----------------

.. csv-table::  
   :header: "Tool", "Icon", "Description"
   :widths: 20, 10, 120

    "Left", |icon01|, "Shows / hide the dock widgets located on the left side of the drawing window."
    "Right", |icon02|, "Shows / hide the dock widgets located on the right side of the drawing window."
    "Top", |icon03|, "Shows / hide the dock widgets located on the top of the drawing window."
    "Bottom", |icon04|, "Shows / hide the dock widgets located on the bottom of the drawing window."
    "Floating", |icon05|, "Shows / hide the dock widgets floating within the drawing window or out side of the drawing applications."

..  Icon mapping:

.. |icon00| image:: /images/icons/librecad.ico
.. |icon01| image:: /images/icons/dockwidgets_left.svg
.. |icon02| image:: /images/icons/dockwidgets_right.svg
.. |icon03| image:: /images/icons/dockwidgets_top.svg
.. |icon04| image:: /images/icons/dockwidgets_bottom.svg
.. |icon05| image:: /images/icons/dockwidgets_floating.svg

Docked widgets can be dragged to different areas by "grabbing" (click and drag) the title bar of the widget.  Widgets will snap into place when released in a dock area.  Widgets in the left, right, top or bottom areas can either be placed on top of existing widgets, creating tabs for each category of widget placed in that area, or place above or below the existing widget dividing the area in sections.  Dock widgets can also be resized by clicking on and dragging the edge of the widget's box to a minumum of five icons width and no shorter than the default height.


Block List Dock
---------------

.. figure:: /images/dock-blockList.png
    :width: 272px
    :height: 590px
    :align: right
    :scale: 67
    :alt: Block List Dock

The Block List Dock provides the functions to manage blocks and a list of :ref:`Blocks <blocks>` that are active in the drawing.  Block functions include:

.. csv-table:: 
   :header: "Icon", "Description"
   :widths: 10, 60

    |icon01|, "''Show all blocks'' - makes all the blocks in the current drawing visible."
    |icon02|, "''Hide all blocks'' - hides all blocks in the active drawing."
    |icon03|, "''Create a block'' - creates a block from the selected items."
    |icon04|, "''Add an empty block'' - creates an empty block that can then be edited is a separate window (see below)."
    |icon05|, "''Remove the active block'' - Deletes the highlighted block."
    |icon06|, "''Rename the active block''. - Rename the hightlighted block"
    |icon07|, "''Edit the active block in a separate window'' - Open a new drawing window to edit a new or  existing block."
    |icon08|, "''Save the active block to a file'' - Saves the highlighted block to a file."
    |icon09|, "''Insert the active block''. - Inserts the highlighted block in the current drawing at the specified reference point"

The lower portion of the dock shows a list of blocks in the current drawing.  The blocks in the above example are named "a3", "d1", "d2", and "d4".

..  Icon mapping:

.. |icon01| image:: /images/icons/visible.svg
.. |icon02| image:: /images/icons/invisible.svg
.. |icon03| image:: /images/icons/create_block.svg
.. |icon04| image:: /images/icons/add.svg
.. |icon05| image:: /images/icons/remove.svg
.. |icon06| image:: /images/icons/rename_active_block.svg
.. |icon07| image:: /images/icons/properties.svg
.. |icon08| image:: /images/icons/save.svg
.. |icon09| image:: /images/icons/insert_active_block.svg

Command Line Dock
-----------------

.. dock-cmdLine0.png  271 591

.. figure:: /images/dock-cmdLine.png  
    :width: 544px
    :height: 227px
    :align: right
    :scale: 67
    :alt: Command Line Dock

For a quick reference list of commands see: Commands

This is intended for people that want to draw by entering commands. This can be faster and/or more precise than drawing using exclusively a mouse and tool bars.

LibreCAD is designed with emphasis on mouse-clicking input, and some options can be at the moment only selected by clicking, not by typing on command line.

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


Layer List Dock
---------------

.. figure:: /images/dock-layerList.png
    :width: 270px
    :height: 590px
    :align: right
    :scale: 67
    :alt: Layer List Dock

|
|
|
|
|
|
|
|
|
|
|
|


Library Browser Dock
--------------------

.. figure:: /images/dock-libraryBrowser.png
    :width: 270px
    :height: 590px
    :align: right
    :scale: 67
    :alt: Library Browser Dock

|
|
|
|
|
|
|
|
|
|
|
|


Pen Wizard Dock
---------------

.. figure:: /images/dock-penWizard.png
    :width: 272px
    :height: 590px
    :align: right
    :scale: 67
    :alt: Pen Wizard Dock

This widget allows users to:

    - Maintain a list of favorite colors

        - select a color via the drop-down list or the button on its right
        - add the color by pressing the button with the tooltip "Add to favorites"
        - drag-and-drop colors to arrange them

    - Change the active pen color

        - double-click a favorite color

    - Change the color of all selected objects

        - right-click a favorite and choose "Apply to selected"

    - Select all objects of a specific color

        - right-click a favorite and choose "Select objects"


