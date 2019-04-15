.. User Manual, LibreCAD v2.2.x


.. _widgets: 

Dock Widgets
=============

Dock widgets serve two purposes; they provide alternative method to access drawing tools, and additional tools or features:

    - Block List
    - Command Line
    - Layer List
    - Library Browser, and
    - Pen Wizard.

.. figure:: /images/dock-lines.png
    :figwidth: 200px
    :width: 172px
    :height: 172px
    :align: right
    :scale: 100
    :alt: Lines Dock

    Drawing tool dock example; Line

Dock widgets are available for these :ref:`Drawing Tools <tools>`:

    - Circle
    - Curve
    - Dimension
    - Ellipse
    - Info
    - Line
    - Modify, and
    - Polyline.


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

.. See icon mapping a eof

Docked widgets can be dragged to different areas by "grabbing" (click and drag) the title bar of the widget.  Widgets will snap into place when released in a dock area.  Widgets in the left, right, top or bottom areas can either be placed on top of existing widgets, creating tabs for each category of widget placed in that area, or place above or below the existing widget dividing the area in sections.  Dock widgets can also be resized by clicking on and dragging the edge of the widget's box to a minumum of five icons width and no shorter than the default height.

.. _block-list:

Block List Dock
---------------

.. figure:: /images/dock-blockList01.png
    :width: 272px
    :height: 590px
    :align: right
    :scale: 67
    :alt: Block List Dock

The Block List Dock provides the functions to manage blocks and a list of blocks that are active in the drawing.  Block functions include:

.. csv-table:: 
   :header: "Icon", "Description"
   :widths: 10, 90

    |icon10|, "''Show all blocks'' - Makes all the blocks in the current drawing visible."
    |icon11|, "''Hide all blocks'' - Hides all blocks in the active drawing."
    |icon12|, "''Create a block'' - Creates a block from the selected items."
    |icon13|, "''Add an empty block'' - Creates an empty block that can then be edited is a separate window (see below)."
    |icon14|, "''Remove the active block'' - Deletes the highlighted block."
    |icon15|, "''Rename the active block'' - Rename the hightlighted block"
    |icon16|, "''Edit the active block in a separate window'' - Open a new drawing window to edit a new or  existing block."
    |icon17|, "''Save the active block to a file'' - Saves the highlighted block to a file."
    |icon18|, "''Insert the active block''. - Inserts the highlighted block in the current drawing at the specified reference point"

The lower portion of the dock shows a list of blocks in the current drawing.  The blocks in the above example are named "a3", "d1", "d2", and "d4".  More details on creating and using :ref:`blocks <blocks>` can be found in the **User Guides**.

.. See icon mapping a eof


Command Line Dock
-----------------

.. dock-cmdLine0.png  271 591

.. figure:: /images/dock-cmdLine.png  
    :width: 544px
    :height: 227px
    :align: right
    :scale: 67
    :alt: Command Line Dock

The *Command Line* is for users that want to draw by using keyboard commands. Commands, such as "li" for a line, "cir" for a circle, etc, are entered at the command line along with the required parameters (e.g. start and end coordinates for a line).  Using the command line can be faster and/or more precise than drawing using exclusively a mouse and toolbars.  The available commands are listed with the :ref:`Drawing Tools <tools>` and :ref:`Snapping <snaps> tools`.  There are also commands available for :ref:`Edit <edit>` and :ref:`View <view>` operations.

Note that LibreCAD is designed with emphasis on mouse input and at the moment some options can be only selected by using the mouse as there is no equivalent command.

In addition to command input, the command line provides access to a built in calculator.  The calculator can be invoked with the *cal* command.  The available :ref:`operators and functions <calc>` can be found in the **Appendix**.

Further details on using the :ref:`command line <commandline>` are in the **User Guides**.


Layer List Dock
---------------

.. figure:: /images/dock-layerList01.png
    :width: 270px
    :height: 590px
    :align: right
    :scale: 67
    :alt: Layer List Dock


The Layer List Dock provides the functions to manage layers and a list of layers in the current drawing. The entry line on top of the dock allows to filter by layer names (e.g. "*01" would show all names ending by "01").  Layer functions include:

.. csv-table:: 
   :header: "Icon", "Description"
   :widths: 10, 90

    |icon10|, "''Show all layers'' - Makes all the layers in the current drawing visible. (*: ''Freeze'')"
    |icon11|, "''Hide all layers'' - Hides all layers in the active drawing.  (*: ''Defreeze'')"
    |icon13|, "''Add a layer'' - Add a new layer. *"
    |icon14|, "''Remove the current layer'' - Remove the highlighted layer. *"
    |icon15|, "''Modify layer attributes / rename'' - Modify the layer's attributes and / or rename the layer. *"

.. See icon mapping a eof

|

..  figure:: /images/layerAttributes01.png
    :width: 251px
    :height: 215px
    :scale: 100
    :align: left
    :alt: LibreCAD Layers Attributes

|
|
|
|
|

Clicking the *Attribute* icon allows users to change the attributes of all entities on the selected layer.  The attribute include:

+---------------------+---------------------------------------------------------------------------+
| Attribute           | Description                                                               |
+=====================+===========================================================================+
| Layer Name          | The default layer name is "O", but any alpha-numeric label can be used.   |
|                     | New layers are created with the name of the hightlighted layer with a     |
|                     | sequence number appended.  Layers are sorted in the list alpha-           |
|                     | numerically.                                                              |
+---------------------+---------------------------------------------------------------------------+
| Construction Layer  | Toggle the construction lines off / on.  Construction lines are intended  |
|                     | as temporary lines and drawn to ''infinity''".                            |
+---------------------+---------------------------------------------------------------------------+
| Default Pen:        | - Color: Select from default or custom colors.                            |
|                     | - Width: Select from predefined line widths from 0.00 to 2.11 mm.         |
|                     | - Type: Select from predefined line types: Continuous, or Dot, Dash, Dash |
|                     |   Dot, Divide, Center, or Border (normal, "tiny", "small", or "large").   |
+---------------------+---------------------------------------------------------------------------+

The lower portion of the dock shows a list of layers in the current drawing and are listed in alpha-numeric order.  In the example above the layers are named "Layer01", "Layer02", and "Layer03".  Note that layer **0** is a special layer and should not be used.

Icons to the left of each layer act on the layers individually.  The layer operations are:

.. csv-table:: 
   :header: "Icon", "Description"
   :widths: 25, 75

    "|icon10| / |icon11|", "Show / hide layer. *"
    "|icon20| / |icon21|", "Lock / unlock layer."
    "|icon22| / |icon23|", "Print / don't print layer. *"
    "|icon24| / |icon25|", "Toggle construction lines. *"
    "|icon26|", "Shows the current layer color (Default is Black)."

.. See icon mapping a eof

.. figure:: /images/dock-layerContextMenu.png
    :width: 219px
    :height: 186px
    :align: right
    :scale: 100
    :alt: Layer Context Menu

Right-clicking on a layer opens a pop-up menu that provides equivalent operations to the item marked with an asterix (*).

More details on creating and using :ref:`layers <layers>` can be found in the **User Guides**.

|
|


Library Browser Dock
--------------------

.. figure:: /images/dock-libraryBrowser01.png
    :width: 270px
    :height: 590px
    :align: right
    :scale: 67
    :alt: Library Browser Dock

The Library Browser Dock shows blocks available from the defined libraries and allows users to insert blocks into the current drawing.  To insert a block, select a block from one of the categories by clicking on it, e.g. "d1" and click the "Insert" button.  Specify a reference point in the drawing window with a mouse click or by entering coordinates at the command prompt.  Once inserted into the drawing, the block is shown in the :ref:`Block List Dock <block-list>`.

LibreCAD includes several libraries and additional libraries can be specified by defining a path to user libraries in the :ref:`Application Preferences <app-prefs>`, "Path" tab as shown in **Getting Started**.

|
|
|
|
|
|


Pen Wizard Dock
---------------

.. figure:: /images/dock-penWizard01.png
    :width: 272px
    :height: 590px
    :align: right
    :scale: 67
    :alt: Pen Wizard Dock

The Pen Wizard allows users to create a palette of favorite colors for the drawing tools.  Colors can be selected from the existing colors via the drop-down list or created as a custom colors via the |icon31| button to the right of the drop-down list.  Pressing the "Add to favorites" [ |icon30| ] button to the left will add the color to the list of favorites below.  Drag-and-drop the colors in the list to arrange them in the prefered order.

Once colors have been added to the list, set the active pen color by double-clicking a favorite color.

Right-clicking a favorite color allows users to:

    - Select all objects of a specific color and clicking on "Select objects"
    - Change the color of all selected objects by  clicking on "Apply to selected"
    - Delete  a favorite color by clicking "Remove"


..  Icon mapping:

.. |icon00| image:: /images/icons/librecad.ico
            :height: 24
            :width: 24
.. |icon01| image:: /images/icons/dockwidgets_left.svg
            :height: 24
            :width: 24
.. |icon02| image:: /images/icons/dockwidgets_right.svg
            :height: 24
            :width: 24
.. |icon03| image:: /images/icons/dockwidgets_top.svg
            :height: 24
            :width: 24
.. |icon04| image:: /images/icons/dockwidgets_bottom.svg
            :height: 24
            :width: 24
.. |icon05| image:: /images/icons/dockwidgets_floating.svg
            :height: 24
            :width: 24

.. |icon10| image:: /images/icons/visible.svg
            :height: 24
            :width: 24
.. |icon11| image:: /images/icons/invisible.svg
            :height: 24
            :width: 24
.. |icon12| image:: /images/icons/create_block.svg
            :height: 24
            :width: 24
.. |icon13| image:: /images/icons/add.svg
            :height: 24
            :width: 24
.. |icon14| image:: /images/icons/remove.svg
            :height: 24
            :width: 24
.. |icon15| image:: /images/icons/rename_active_block.svg
            :height: 24
            :width: 24
.. |icon16| image:: /images/icons/properties.svg
            :height: 24
            :width: 24
.. |icon17| image:: /images/icons/save.svg
            :height: 24
            :width: 24
.. |icon18| image:: /images/icons/insert_active_block.svg
            :height: 24
            :width: 24

.. |icon20| image:: /images/icons/locked.svg
            :height: 24
            :width: 24
.. |icon21| image:: /images/icons/unlocked.svg
            :height: 24
            :width: 24
.. |icon22| image:: /images/icons/print.svg
            :height: 24
            :width: 24
.. |icon23| image:: /images/icons/noprint.svg
            :height: 24
            :width: 24
.. |icon24| image:: /images/icons/construction_layer.svg
            :height: 24
            :width: 24
.. |icon25| image:: /images/icons/noconstruction.svg
            :height: 24
            :width: 24
.. |icon26| image:: /images/icons/color07.png
            :height: 24
            :width: 24

.. |icon30| image:: /images/icons/char_pm.png
            :height: 18
            :width: 18
.. |icon31| image:: /images/icons/colorxx.png
            :height: 18
            :width: 18
