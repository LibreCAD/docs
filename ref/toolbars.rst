.. User Manual, LibreCAD v2.2.x

.. Default include
.. include:: /notice.rst


.. _toolbars:

Toolbars
========

Toolbars provide an alternative to the menus for accessing application functions and drawing tools.  See :ref:`Application Menu <menu>` or :ref:`Drawing Tools <tools>` for complete descriptions.

.. csv-table:: 
    :widths: 30, 70
    :header-rows: 1
    :stub-columns: 0
    :class: fix-table

    "Menu Item", "Description and/or *Menu Equivalent*"
    "Categories", "Groups commonly used drawing tools; *Tools -> Line / Circle / Curve / Ellipse / Polyline / Select / Dimension / Modify* and *Info*."
    "Circles", "*Tools -> Circle*."
    "Creators",  "Access menu and toolbar Creators. *Widgets -> Menu Creator* / *Toolbar Creator*.  Also see :ref:`Customizing LibreCAD’s Interface <customize>`."
    "Curves", "*Tools -> Curve*."
    "DefaultCustom", "Custom toolbar example."
    "Dimension", "*Tools -> Dimension*."
    "Dock Areas",  "*Widgets -> Dock Areas*."
    "Edit", ":ref:`Edit <edit>` functions."
    "Ellipse", "*Tools -> Ellipse*."
    "File", ":ref:`File <file>` operations."
    "Info", "*Tools -> Info*."
    "Line", "*Tools -> Line*."
    "Modify", "*Tools -> Modify*."
    "Order", "Reorder drawing entities. *Tools -> Modify -> Order*."
    "Pen", "Change entity color, width and / or style."
    "Polyline", "*Tools -> Polyline*."
    "Select", "Select entities. *Tools -> Select*."
    "Snap Selection", "See :ref:`Snapping <snaps>` in **The Coordinate System**."
    "Tool Options",  "Displays input boxes for the parameters required by the currently selected tool.  **This option should always be enabled.**"
    "View", ":ref:`View <view>` options."


Other Toolbars
--------------

 .. important::
    Print Preview and Block operations require the use of the **Tool Options** toolbar as there are no menu or command line equivalencies. Ensure the Tool Option toolbar is enabled (**Widgets -> Toolbars** and check **Tool Options**).


.. _print-preview-toolopt:

Print Preview
~~~~~~~~~~~~~

The **Print Preview** toolbar is used to set up the print output as desired regardless of output format (pdf or paper). The print preview can be configured after selecting **File -> Print Preview** through the menu.  A combination of scale value, color status and drawing position relative to paper allows customed print output. The steps are detailed in :ref:`printing guide <printing-guide>`.


.. figure:: /images/toolOptions/toPrtPreview.png
    :width: 316px
    :height: 35px
    :align: center
    :scale: 100
    :alt:  Print Preview tool option bar


.. csv-table:: 
    :widths: 20, 10, 70
    :header-rows: 1
    :stub-columns: 0
    :class: fix-table
    
    "Option Item", "Icon", "Description"
    "Scale", , "Displays the scale of the drawing based on its size and the paper size selected in :ref:`Drawing Preferences <draw-prefs>`. It is also possible to adjust the scale to a specific value to a value in the drop down  list or enter a custom values separated by the colon (:). Checking the *fixed* checkbox locks the scale to the set value."
    "Toggle Black/White", |icon01|, "Toggles the colors of all entities from color to black/white."
    "Center to page", |icon02|, "Centers the drawing to the paper size selected in *Drawing Preferences*."
    "Fit to page", |icon03|, "Fits the drawing to the paper size selected."
    "Multipages", |icon04|, "Determines the number of pages needed to print the drawing based on the defined scale and the paper size selected in *Drawing Preferences*."


.. _blk-insert-toolopt:

Inserting Blocks
~~~~~~~~~~~~~~~~

There are two block insert operations with corresponding Tool Option toolbars.  For further details on using blocks refer to :ref:`Blocks <blocks>` in the User Guides.


From Block List
```````````````

The **Block Insert** capability can be expanded through the *Tool Option* bar features before the block is inserted. 

.. figure:: /images/toolOptions/toBlockInsert.png
    :width: 617px
    :height: 34px
    :align: center
    :scale: 100
    :alt: Block insert tool option bar


.. csv-table:: 
    :widths: 30, 70
    :header-rows: 1
    :stub-columns: 0
    :class: fix-table
    
    "Option Item", "Description"
    "Angle", "Defines the angle of rotation, if any. See :ref:`Angles in LibreCAD <fundamentals>`."
    "Factor", "Defines the scale factor, if any. It is the same scale factor as in :ref:`Modify <tools>`."
    "Array", "Defines the numbers of columns and rows to create a pattern of selected block. Otherwise keep 1 for columns and rows."
    "Spacing", "Defines the distance between each column of the array and the distance between each row. The distance is measured between 2 insertion points of 2 adjacent blocks."


From Block Library
``````````````````

Inserting a block from a library can be enhanced through the *Tool Option* bar features before the block is inserted.

.. figure:: /images/toolOptions/toBlockLib.png
    :width: 317px
    :height: 33px
    :align: center
    :scale: 100
    :alt: Block from library insertion tool option bar


.. csv-table:: 
    :widths: 30, 70
    :header-rows: 1
    :stub-columns: 0
    :class: fix-table
    
    "Option Item", "Description"
    "Angle", "Defines the angle of rotation, if any. See :ref:`Angles in LibreCAD <fundamentals>`."
    "Factor", "Defines the scale factor, if any. It is the same scale factor as in :ref:`Modify <tools>`."


..  Icon mapping:

.. |icon01| image:: /images/icons/black_n_white_mode.svg
            :height: 24
            :width: 24        
.. |icon02| image:: /images/icons/center_to_page.svg
            :height: 24
            :width: 24           
.. |icon03| image:: /images/icons/fit_to_page.svg
            :height: 24
            :width: 24   
.. |icon04| image:: /images/icons/multi_pages.svg
            :height: 24
            :width: 24   
