.. User Manual, LibreCAD v2.2.x

.. Default include
.. include:: /inclFiles/notice.rst


.. _toolbars:

Toolbars
========

Toolbars provide an alternative to the menus for accessing application functions and drawing tools.  See :ref:`Application Menu <menu>` or :ref:`Drawing Tools <tools>` for complete descriptions.  

Toolbars can be moved any where on the display and left floating, or docked to any of the four sides of the drawing window, similar to :ref:`Dock Widgets <widgets>`.  Unlike Dock Widgets, icons on a Toolbar are a single row when floating or docked to the top or bottom of the drawing window and verticle when docked to either side.  Also, Toolbars cannot be resized.


Drawing Tools Toolbars
----------------------

.. csv-table:: 
    :widths: 20, 80
    :header-rows: 1
    :stub-columns: 0
    :class: table-fix-width

    "Menu Item", "Description and/or *Menu Equivalent*"
    "Categories", "
        | Groups commonly used drawing tools; *Tools -> Line / Circle / Curve / Ellipse / Polyline / Select / Dimension / Modify* and *Info*.  Clicking an icon will display the drawing tool in the category.  See :ref:`Drawing Tools <tools>` for details on each tool.
        |
        | **Toolbar:** 
        | |tlbar01|"
    "Circles", "
        | Drawing tools for circles.  See :ref:`Tools -> Circle <tool-circle>`.
        |
        | **Toolbar:** 
        | |tlbar02|"
    "Creators",  "
        | Access menu and toolbar creators to modify LibreCAD's interface. *Widgets -> Menu Creator* / *Toolbar Creator*.  Also see :ref:`Customizing LibreCAD’s Interface <customize>`.
        |
        | **Toolbar:** 
        | |tlbar03|"
    "Curves", "
        | Drawing tools for curves.  See :ref:`Tools -> Curve <tool-curve>`.
        |
        | **Toolbar:** 
        | |tlbar04|"
    "DefaultCustom", "
        | Custom toolbar example.  Includes MText, Hatch, Insert Image, Create Block, and Points.
        |
        | **Toolbar:** 
        | |tlbar05|"
    "Dimension", "
        | Drawing tools for dimensioning.  See :ref:`Tools -> Dimension <tool-dimension>`.
        |
        | **Toolbar:** 
        | |tlbar06|"
    "Dock Areas",  "
        | Show or hide widgets. *Widgets -> Dock Areas*.  See :ref:`Dock Widget Areas <widget-dockAreas>`.
        |
        | **Toolbar:** 
        | |tlbar07|"
    "Edit", "
        | :ref:`Edit <edit>` functions; select, Undo, Redo, Cut, Copy and Paste.
        |
        | **Toolbar:** 
        | |tlbar08|"
    "Ellipse", "
        | Drawing tools for ellipses.  See :ref:`Tools -> Ellipse <tool-ellipse>`.
        |
        | **Toolbar:** 
        | |tlbar09|"
    "File", "
        | :ref:`File <file>` operations.
        |
        | **Toolbar:** 
        | |tlbar10|"
    "Info", "
        | Tools for determinig information about entities.  See :ref:`Tools -> Info <tool-info>`.
        |
        | **Toolbar:** 
        | |tlbar11|"
    "Line", "
        | Drawing tools for lines.  See :ref:`Tools -> Line <tool-line>`.
        |
        | **Toolbar:** 
        | |tlbar12|"
    "Modify", "
        | Drawing tools to modify entities.  See :ref:`Tools -> Modify <tool-modify>`.
        |
        | **Toolbar:** 
        | |tlbar13|"
    "Order", "
        | Reorder drawing entities.  *See Tools -> Modify -> Order*.
        |
        | **Toolbar:** 
        | |tlbar14|"
    "Pen", "
        | Change entity color, width and / or line type.  :ref:`Pen <entity-pen>` attributes.
        |
        | **Toolbar:** 
        | |tlbar15|"
    "Polyline", "
        | Drawing tools for Polylines.  See :ref:`Tools -> Polyline <tool-polyline>`.
        |
        | **Toolbar:** 
        | |tlbar16|"
    "Select", "
        | Select entities.  See :ref:`Tools -> Select <tool-select>`.
        |
        | **Toolbar:** 
        | |tlbar17|"
    "Snap Selection", "
        | Toggle snap tools off/on.  See :ref:`Snapping <snaps>`.
        |
        | **Toolbar:** 
        | |tlbar18|"
    "Tool Options",  "
        | Displays input boxes for the parameters required by the currently selected tool.  See **Tool Options** below.  **This option should always be enabled.**
        |
        | **Toolbar:** 
        | Varies by tool selected.  See :ref:`Drawing Tools <tools>`."
    "View", "
        | Toggle grid and draft mode, force redraw, and select zoom.  See :ref:`View <view>` options.
        |
        | **Toolbar:** 
        | |tlbar19|"


.. _tool-options:

Tool Options
------------

A variety of LibreCAD's tools require additional parameters or have options that are shown on the **Tool Options** toolbar.  Several drawing tools use tool options.  Those toolbars are shown in the :ref:`Drawing Tools <tools>` reference.  Two additional operations that require the use of the **Tool Options** toolbar are **Print Preview** and block operations.

.. important::
    Print Preview and Block operations require the use of the **Tool Options** toolbar as there are no menu or command line equivalencies. Ensure the Tool Option toolbar is enabled.

The **Tool Options** toolbar should always be enabled.  If the tool options do not appear, from the menu select **Widgets -> Toolbar** and enable **Tool Options** (place checkmark in checkbox).  If using the :ref:`command line <cmdline>`, the same tool options are available via a command line prompt or the **Tool Options** toolbar.


.. _print-preview-toolopt:

Print Preview Tool Options
~~~~~~~~~~~~~~~~~~~~~~~~~~

The **Print Preview Tool Options** toolbar is used to set up the print output regardless of output format (pdf or paper). The toolbar is displayed after clicking the **Print Preview** icon |icon00| or selecting **File -> Print Preview** from the menu.  A combination of scale value, color status and drawing position relative to paper allows for customized print output. The steps are detailed in :ref:`printing guide <complete&print>`.


.. figure:: /images/toolOptions/toPrintPreview.png
    :width: 316px
    :height: 35px
    :align: center
    :scale: 100
    :alt:  Print Preview tool option bar


.. csv-table:: 
    :widths: 20, 10, 70
    :header-rows: 1
    :stub-columns: 0
    :class: table-fix-width
    
    "Option Item", "Icon", "Description"
    "Scale", , "Displays the current scale of the drawing.  The scale can also be changed to a predefined value selected from the drop-down list, or entered as a custom ratio."
    "”fixed”", , "Checking the ”fixed” checkbox locks the scale to value shown in the text-box."
    "Apply Print Scale to line width", |icon01|, "When enabled, line width is scaled on *reduced* drawings (drawings reduced in size to fit a smaller page)."
    "Toggle Black/White", |icon02|, "Toggles the colors of all entities from color to black/white."
    "Center to page", |icon03|, "Centers the drawing and paper to the Print Preview window."
    "Fit to page", |icon04|, "Fits the drawing to the margins of the paper and centers page to the Print Preview window. (Not available when ”fixed” is selected.)"
    "Multipages", |icon05|, "Determines the number of pages needed to print the drawing based on the defined scale and the paper size selected in *Drawing Preferences*."


.. _blk-insert-toolopt:

Block Operations Tool Options
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

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
    :widths: 20, 80
    :header-rows: 1
    :stub-columns: 0
    :class: table-fix-width
    
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
    :widths: 20, 80
    :header-rows: 1
    :stub-columns: 0
    :class: table-fix-width
    
    "Option Item", "Description"
    "Angle", "Defines the angle of rotation, if any. See :ref:`Angles in LibreCAD <fundamentals>`."
    "Factor", "Defines the scale factor, if any. It is the same scale factor as in :ref:`Modify <tools>`."


..  Icon mapping:

.. |icon00| image:: /images/icons/print_preview.svg
            :height: 18
            :width: 18

.. |icon01| image:: /images/icons/scaleLineWidth.svg
             :height: 24
             :width: 24        
.. |icon02| image:: /images/icons/black_n_white_mode.svg
             :height: 24
             :width: 24        
.. |icon03| image:: /images/icons/center_to_page.svg
             :height: 24
             :width: 24           
.. |icon04| image:: /images/icons/fit_to_page.svg
             :height: 24
             :width: 24   
.. |icon05| image:: /images/icons/multi_pages.svg
             :height: 24
             :width: 24

..  Toolbar mapping:

.. |tlbar01| image:: /images/toolBars/tbCategories.png
             :height: 39
             :width: 313
.. |tlbar02| image:: /images/toolBars/tbCircle.png
             :height: 39
             :width: 313
.. |tlbar03| image:: /images/toolBars/tbCreators.png
             :height: 39
             :width: 82
.. |tlbar04| image:: /images/toolBars/tbCurves.png
             :height: 39
             :width: 247
.. |tlbar05| image:: /images/toolBars/tbCustomDefault.png
             :height: 39
             :width: 181
.. |tlbar06| image:: /images/toolBars/tbDimn.png
             :height: 39
             :width: 280
.. |tlbar07| image:: /images/toolBars/tbDockAreas.png
             :height: 39
             :width: 181
.. |tlbar08| image:: /images/toolBars/tbEdit.png
             :height: 39
             :width: 228
.. |tlbar09| image:: /images/toolBars/tbEllipse.png
             :height: 39
             :width: 181
.. |tlbar10| image:: /images/toolBars/tbFile.png
             :height: 39
             :width: 247
.. |tlbar11| image:: /images/toolBars/tbInfo.png
             :height: 39
             :width: 181
.. |tlbar12| image:: /images/toolBars/tbLine.png
             :height: 39
             :width: 544
.. |tlbar13| image:: /images/toolBars/tbModify.png
             :height: 39
             :width: 676
.. |tlbar14| image:: /images/toolBars/tbOrder.png
             :height: 39
             :width: 148
.. |tlbar15| image:: /images/toolBars/tbPen.png
             :height: 39
             :width: 436
.. |tlbar16| image:: /images/toolBars/tbPolyline.png
             :height: 39
             :width: 280
.. |tlbar17| image:: /images/toolBars/tbSelect.png
             :height: 39
             :width: 346
.. |tlbar18| image:: /images/toolBars/tbSnapSel.png
             :height: 39
             :width: 492
.. |tlbar19| image:: /images/toolBars/tbView.png
             :height: 39
             :width: 320
