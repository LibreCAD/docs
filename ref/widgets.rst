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

The lower portion of the dock shows a list of blocks in the current drawing.

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


