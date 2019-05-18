.. User Manual, LibreCAD v2.2.x


.. _toolbars:

Toolbars
========

Toolbars provide alternatives to menus for accessing application functions and drawing tools.  See :ref:`Application Menu <menu>` or :ref:`Drawing Tools <tools>` for complete descriptions.

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


.. _preview:

Print Preview
-------------

The **Print Preview** toolbar enables to set the print output up as desired regardless of output format (pdf or paper). The print view can be configured after selecting **File -> Print Preview** through the menu. A combination of scale value, color status and drawing position relative to paper allows customed print output. The steps are detailed in :ref:`printing guide <printing>`.

 .. important::
    You cannot set the print output up with the menus nor by typing commands. Please make sure the *Tool Option* toolbar is visible.

.. csv-table:: 
    :widths: 20, 10, 70
    :header-rows: 1
    :stub-columns: 0
    :class: fix-table
    
    "Option Item", "Icon", "Description"
    "Scale", |icon00|, "Defines the scale of the drawing based on its size and the paper size selected in :ref:`Drawing Preferences <draw-prefs>`. It is also possible to freely adjust the scale to a specific value proposed in the list or enter a custom value with colon (:). Check the *Fixed Scale* checkbox locks the actual scale."
    "Toggle Black/White", |icon01|, "Toggles all the colors of entities from colored to Black/White."
    "Center to page", |icon02|, "Centers the drawing to the paper size selected in *Drawing Preferences*."
    "Fit to page", |icon03|, "Fit the drawing to the paper size selected."
    "Multipages", |icon04|, "Determines the number of pages needed to print the drawing based on the defined scale and the paper size selected in *Drawing Preferences*."


..  Icon mapping:

.. |icon00| image:: /images/icons/printscale.png
            :height: 24
            :width: 24    
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
