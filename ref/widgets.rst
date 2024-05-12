.. User Manual, LibreCAD v2.2.0

.. Default include
.. include:: /inclFiles/notice.rst


.. _widgets: 

Dock Widgets
=============

Dock widgets are small movable windows that serve two purposes: (1) quick access to the drawing tools, and (2) access to additional features not available from a menu including:

    - Block List,
    - Command Line,
    - Layer List,
    - Library Browser, and
    - Pen Wizard.

.. figure:: /images/dock-lines.png
    :figwidth: 200px
    :align: right
    :scale: 100
    :alt: Lines Dock

    Drawing tool dock example: Line

.. actual image size 172px x 183px

As an alternative to the **Tools** menu, the Dock widgets provide more convenient way to access the :ref:`Drawing Tools <tools>`:

    - Circle,
    - Curve,
    - Dimension,
    - Ellipse,
    - Info,
    - Line,
    - Modify, and
    - Polyline.

.. Force end of left / right text wrap
.. include:: /inclFiles/eoWrap.rst


.. _widget-dockAreas:

Dock Widget Areas
-----------------

Dock widgets can be moved to different areas by "grabbing" (left clicking and dragging) the title bar of the widget and releasing it in a new location.  A widget can be left *floating* inside or outside of the drawing window, or placed in one of the four dock areas (left, right, top or bottom).  The Dock Areas :ref:`toolbar <toolbars>` allows widgets to be hidden or made visible depending on their location:

.. csv-table::  
    :widths: 15, 10, 75
    :header-rows: 1
    :stub-columns: 0
    :class: table-fix-width

    "Tool", "Icon", "Description"
    "Left", |icon01|, "Shows / hide the dock widgets located on the left side of the drawing window."
    "Right", |icon02|, "Shows / hide the dock widgets located on the right side of the drawing window."
    "Top", |icon03|, "Shows / hide the dock widgets located on the top of the drawing window."
    "Bottom", |icon04|, "Shows / hide the dock widgets located on the bottom of the drawing window."
    "Floating", |icon05|, "Shows / hide the dock widgets floating within the drawing window or outside of the drawing window."

.. See icon mapping a eof

Widgets can be placed either on top of an existing widget in any of the dock areas creating a tab for each of the widgets.  Widgets can also be place above or below an existing widget dividing the area into multiple sections.  

In addition, dock widgets can be resized by clicking and dragging the edge of the widget's box.  A widget has a minimum width of five icons and can be no shorter than the default height.

.. Force end of left / right text wrap
.. include:: /inclFiles/eoWrap.rst


.. _widget-blockList:

Block List Dock
---------------

The Block List Dock provides the functions to manage blocks and a list of blocks that are active in the drawing.  Block functions include:

.. figure:: /images/dock-blockList01.png
    :figwidth: 200px
    :align: right
    :scale: 67
    :alt: Block List Dock

    Block List dock example - 3 blocks

.. actual image size 260px x 340px

.. csv-table:: 
    :widths: 10, 90
    :header-rows: 1
    :stub-columns: 0
    :class: table-fix-width

    "Icon", "Description"
    |icon10|, "”Show all blocks” - *Defreeze*, makes all the blocks in the current drawing visible."
    |icon11|, "”Hide all blocks” - *Freeze*, hides all blocks in the active drawing."
    |icon12|, "”Create a block” - Creates a block from the selected items."
    |icon13|, "”Add an empty block” - Creates an empty block that can then be edited is a separate window (see below)."
    |icon14|, "”Remove the active block” - Deletes the highlighted block."
    |icon15|, "”Rename the active block” - Rename the highlighted block."
    |icon16|, "”Edit the active block in a separate window” - Open a new drawing window to edit a new or  existing block."
    |icon17|, "”Save the active block to a file” - Saves the highlighted block to a file."
    |icon18|, "”Insert the active block”. - Inserts the highlighted block in the current drawing at the specified reference point"

The lower portion of the dock shows a list of blocks in the current drawing.  The blocks in the above example are named "a3", "d1", and "d3".  More details on creating and using :ref:`blocks <blocks>` can be found in the **User Guides**.

.. Force end of left / right text wrap
.. include:: /inclFiles/eoWrap.rst


.. _widget-cmdLine:

Command Line Dock
-----------------

.. figure:: /images/dock-cmdLine.png
    :figwidth: 200px
    :align: right
    :scale: 67
    :alt: Command Line Dock

    Command Line dock

.. actual image size 260px x 340px

The *Command Line* is for users that want to draw by using keyboard commands. Commands, such as "li" for a line, "cir" for a circle, etc, are entered at the command line along with the required parameters (e.g. start and end coordinates for a line).  Using the command line can be faster and/or more precise than drawing using exclusively a mouse and toolbars.  The available commands are listed with the :ref:`Drawing Tools <tools>` and :ref:`Snapping <snaps>` tools.  There are also commands available for :ref:`Edit <edit>` and :ref:`View <view>` operations.

.. Force end of left / right text wrap
.. include:: /inclFiles/eoWrap.rst

.. figure:: /images/dock-cmdLine01a.png
    :figwidth: 200px
    :align: right
    :scale: 67
    :alt: Command Line Dock

    Command Line dock drop-down menu

.. actual image size 242px x 90px

The dock includes a drop-down menu that offers additional functions:

    - Toggle Keycode Mode off or on.
    - Load a Command file.
    - Paste commands.

Further details on using the :ref:`command line <cmdline>` are in the **User Guides**.
In addition to command input, the command line provides access to a built in calculator.  The calculator can be invoked with the *cal* command.  The available :ref:`operators and functions <calc>` can be found in the **Appendix**.

.. note::
    LibreCAD is designed with emphasis on mouse input and at the moment some options can be only selected by using the mouse as there is no equivalent command.

.. Force end of left / right text wrap
.. include:: /inclFiles/eoWrap.rst


.. _widget-layerList:

Layer List Dock
---------------

.. figure:: /images/dock-layerList01.png
    :figwidth: 200px
    :align: right
    :scale: 67
    :alt: Layer List Dock

    Layer List dock example with 4 layers

.. actual image size 260px x 340px

The Layer List Dock provides a list of layers in the current drawing and the functions required to manage them.  There are three sections in the dock:

    - the list filter,
    - the list operators and functions, and 
    - the layer operators and functions.

The list filter is the input box at the top of the dock.  It provides the ability to filter a long list of layer names to help locate a layer.  Enter a text string, the name or partial name of a layer, in the input box to filter the layer or layers.  Wildcards ("\*" or "?") can be used to filter the list to locate similar layer names (e.g. "\*01" would show all names ending by "01").

The icons on the top of the layer list allow operations to the entire list of layers.  Those operations include:

.. csv-table:: 
    :widths: 10, 25, 65
    :header-rows: 1
    :stub-columns: 0
    :class: table-fix-width

    "Icon", "Function", "Description"
    |icon10|, "Show all layers", "*Defreeze*, makes all the layers in the current drawing visible."
    |icon11|, "Hide all layers", "*Freeze*, hides all layers in the current drawing."
    |icon20|, "Unlock all layer", "Unlock all layers to allow changes to the entities in the layer. (\*)"
    |icon21|, "Lock all layer", "Lock all layers to prevent unintentional changes. (\*)"
    |icon13|, "Add a layer", "Add a new layer to the list. (Shortcut [Ctrl]+[L]) (\*)"
    |icon14|, "Remove layer", "Remove the highlighted layer from the list. (\*)"
    |icon15|, "Modify layer attributes / rename", "Modify the selected layer's attributes and / or rename the layer. (\*)"

The lower portion of the dock shows a list of layers in the current drawing and are listed in alpha-numeric order.  In the example above the layers are named "Layer01", "Layer02", and "Layer03".  Note that layer **0** is a special layer and should not be used for general drawing purposes.

Icons to the left of each layer act on the layers individually.  The layer operations are:

.. csv-table:: 
    :widths: 15, 85
    :header-rows: 1
    :stub-columns: 0
    :class: table-fix-width

    "Icon", "Description"
    "|icon10| / |icon11|", "Show / hide the selected layer. (*Defreeze* / *Freeze*)"
    "|icon20| / |icon21|", "Lock / unlock the selected layer. (\*)"
    "|icon22| / |icon23|", "Print / don't print the selected layer. (\*)"
    "|icon24| / |icon25|", "Toggle construction lines. (\*)  A layer designated as a ”Construction Layer” is special layer used to create reference geometry to help align other drawing entities.  Construction lines are intended as temporary guide lines and drawn to ”infinity”."
    "|icon26|", "Shows the layer's assigned color (the default is Black)."

.. Multiple layer can be selected and then deleted with [Shift]-[left-mouse-button] to select a contiguous group of layers.  Use [Ctrl]-[left-mouse-button] to select individual layers in a noncontiguous group.  After making a selection, click the "Remove layer" icon |icon14|.

.. Force end of left / right text wrap
.. include:: /inclFiles/eoWrap.rst

.. figure:: /images/dock-layerContextMenu.png
    :figwidth: 200px
    :align: right
    :scale: 67
    :alt: Layer Context Menu

.. actual image size 219px x 186px

Layer list or individual layer operations can also be accessed by right-clicking on a layer.  Right-clicking in the list window opens a popup menu that provides equivalent operations to the item marked with an asterisk (*).

.. Force end of left / right text wrap
.. include:: /inclFiles/eoWrap.rst

..  figure:: /images/layerSettings01.png
    :figwidth: 200px
    :align: right
    :scale: 67
    :alt: LibreCAD Layers Settings

.. actual image size 276px x 258px

.. _widget-layerList-attributes:

Clicking the *Attribute* icon |icon15| allows users to change the :ref:`pen attributes <entity-pen>` of all entities on the selected layer.  Entities that have their own pen attribute set differently will override the layer's attributes.

.. Force end of left / right text wrap
.. include:: /inclFiles/eoWrap.rst

The attributes include:

.. table::
    :align: center
    :widths: 20, 80
    :class: table-fix-width

    +----------------------+--------------------------------------------------------------------------+
    | Attribute            | Description                                                              |
    +======================+==========================================================================+
    | Layer Name           |  The default layer name is "O", but any alpha-numeric label can be used. |
    |                      |  New layers are created with the name of the highlighted layer with a    |
    |                      |  sequence number appended.  Layers are sorted in the list alpha-         |
    |                      |  numerically.                                                            |
    +----------------------+--------------------------------------------------------------------------+
    | Construction Layer   |  Toggle the construction lines off / on.                                 |
    +----------------------+--------------------------------------------------------------------------+
    | Default Pen:         |  - Color: Select from default or custom colors.                          |
    |                      |  - Width: Select from predefined line widths from 0.00 to 2.11 mm.       |
    |                      |  - Type: Select from predefined line types: Continuous, or Dot, Dash,    |
    |                      |    Dash Dot, Divide, Center, or Border (normal, "tiny", "small", or      |
    |                      |    "large").                                                             |
    +----------------------+--------------------------------------------------------------------------+


More details on creating and using :ref:`layers <ug-layers>` can be found in the "Drawing Setup" section of the **User Guides**.


.. _widget-libBrowser:

Library Browser Dock
--------------------

.. figure:: /images/dock-libraryBrowser01.png
    :figwidth: 200px
    :align: right
    :scale: 67
    :alt: Library Browser Dock

    Library Browser dock example

.. actual image size 284px x 340px

The Library Browser Dock shows blocks available from the defined libraries and allows users to insert blocks into the current drawing.  To insert a block, select a block from one of the categories by clicking on it, e.g. "d1" and click the "Insert" button.  Specify a reference point in the drawing window with a mouse click or by entering coordinates at the command prompt.  Once inserted into the drawing, the block is shown in the :ref:`Block List Dock <ug-BlockList>`.

LibreCAD includes several libraries and additional libraries can be specified by defining a path to user libraries in the :ref:`Application Preferences <app-prefs>`, "Path" tab as shown in **Getting Started**.

.. Force end of left / right text wrap
.. include:: /inclFiles/eoWrap.rst


.. _widget-penWiz:

Pen Wizard Dock
---------------

.. figure:: /images/dock-penWizard01.png
    :figwidth: 200px
    :align: right
    :scale: 67
    :alt: Pen Wizard Dock

    Pen Wizard dock example

.. actual image size 284px x 340px

The Pen Wizard allows users to create a palette of favorite colors for the drawing tools.  Colors can be selected from the existing colors via the drop-down list or created as a custom colors via the |icon31| button to the right of the drop-down list.  Pressing the "Add to favorites" [ |icon30| ] button to the left will add the color to the list of favorites below.  Drag-and-drop the colors in the list to arrange them in the preferred order.

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
