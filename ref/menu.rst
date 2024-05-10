.. User Manual, LibreCAD v2.2.x

.. Default include
.. include:: /inclFiles/notice.rst


.. _menu: 

Main Menu
=========

Most of LibreCAD's commands are accessible through the menu bar.  Drop-down menus provides access to file and print operations, application and drawing configurations, drawing and editing tools, and other functions.

The drop-down menus can be changed into a floating menu.  Each drop-down menu has a dashed line at the top.  Clicking the dashed line allows the menu to be "torn off" and moved to another location anywhere on-screen.  Clicking the ``x`` on the upper right corner of the floating menu closes it.

.. hint::
    | The windows top bar is created and handled by your operating system.
    | Thus appearance and handling may vary.
    | If just click doesn't work, try to drag the dashed line to create the floating menu.
    | The ``x`` may be any other symbol and it may also be on the left side, just follow your intuition and close the menu like any other window on your system.

.. _file:

File
----

.. csv-table:: 
    :widths: 20, 7, 15, 58
    :header-rows: 1
    :stub-columns: 0
    :class: table-fix-width

    "Menu Item", "Icon", "Short-cut", "Description"
    "New", |icon01|, "[Ctrl]+n", "Creates a new drawing file."
    "New from Template", |icon02|, "", "Creates a new drawing file from a template.  See :ref:`Templates <ug-templates>` in **User Guides** for details."
    "Open", |icon03|, "[Ctrl]+o", "Open existing drawing file."
    "Save", |icon04|, "[Ctrl]+s", "Save current drawing file."
    "Save as", |icon05|, "[Ctrl] [Shift]+s ", "Save current drawing file to a different location or with a new file name."
    "Import", |icon06|, "", "Import a :ref:`block <blocks>`, or bit mapped or vector images into the current drawing.  Supported bit mapped formats include: bmp, cur, gif, ico, jpeg, pbm, pgm, png, ppm, xbm, and xpm.  Vector images supported include svg, and svgz."
    "Export", |icon07|, "", "Export the current drawing as a CAM, pdf or image file. Supported bitmapped formats include: cur, jpeg, pbm, pgm, png, ppm, bmp, ico, xbm, and xpm.  Vector images supported include svg, and svgz.  Use the ''CAM'' export to save SVG (Scalable Vector Graphics) suitable for MakerCAM, EleskCAM, LaserWeb, ..."
    "Print", |icon08|, "[Ctrl]+p  ", "Produce output of the current drawing.  See :ref:`Printing <complete&print>` in the **User Guides** section."
    "Print Preview", |icon09|, "", "View output on screen of the current drawing."
    "Close", |icon10|, "[Ctrl]+w", "Close the active drawing."
    "Quit", |icon11|, "[Ctrl]+q", "Close the application."
    "Recent Files", , "", "Open existing drawing file from a list of previously opened drawing files."


Options
-------
.. csv-table:: 
    :widths: 20, 7, 15, 58
    :header-rows: 1
    :stub-columns: 0
    :class: table-fix-width

    "Menu Item", "Icon", "Short-cut", "Description"
    "Application Preferences", |icon13|, "", "See :ref:`Application Preferences <app-prefs>` in **Getting Started** for details."
    "Current Drawing Preferences", |icon14|, "", "See :ref:`Drawing Preferences <draw-prefs>` for details."
    "Widget Options", , "", "See :ref:`Widget Options <widget-options>` for in **Customizing** details."
    "Device Options", , "", "Select input device: mouse, tablet, trackpad or touchscreen."
    "Reload Style Sheet", , "[Ctrl]+t", "See :ref:`Style Sheets <style-sheets>` in **Customizing** for details."

 
.. _edit:

Edit
----
.. csv-table:: 
    :widths: 20, 7, 15, 58
    :header-rows: 1
    :stub-columns: 0
    :class: table-fix-width

    "Menu Item", "Icon", "Short-cut / *Command*", "Description"
    "Selection Pointer", |icon18|, "[Esc] / *k, kill*", "Reverts from current operation to the selection pointer (e.g. cancels the current operation)"
    "Undo", |icon19|, "[Ctrl]+z / *u, undo, oo*", "Sequentially reverses the previous operations."
    "Redo", |icon20|, "[Ctrl]+[Shift]+z / *r, redo, uu*", "Sequentially reverses the previously reversed operations."
    "Cut", |icon21|, "[Ctrl]+x", "Removes the selected entity (or entities) and places it in temporary memory, e.g. ''clipboard'' for later recall.  A reference point needs to be placed for subsequent paste operations."
    "Copy", |icon22|, "[Ctrl]+c", "Creates a copy of the selected entity (or entities) in temporary memory to be recalled.  A reference point needs to be placed for subsequent paste operations."
    "Paste", |icon23|, "[Ctrl]+v", "Recalls the entity (or entities) from temporary memory and place it at a location defined by a reference point."
    "Delete Selected", |icon24|, "[Del]", "Removes the selected entity (or entities) from the current drawing."


.. _view:

View
----

.. csv-table:: 
    :widths: 20, 7, 15, 58
    :header-rows: 1
    :stub-columns: 0
    :class: table-fix-width

    "Menu Item", "Icon", "Short-cut / *Command*", "Description"
    "Fullscreen", , "[F11]", "Hides the application title bar and toggles LibreCAD to use the entire display."
    "Statusbar", , "[Ctrl]+[I]", "Toggles the visibility of the status bar at the bottom of the application window."
    "Grid", |icon27|, "[Ctrl]+[G]", "Toggles the visibility of the grid."
    "Draft", |icon28|, "[Ctrl]+[D]", "Toggles to or from ''Draft Mode''. Draft mode displays hatches as invisible, and only displays bounding boxes for images and text. Drawings will display faster, particularly on slow computers."
    "Redraw", |icon29|, "[Ctrl]+[R] / *zr, rg, regen, redraw*", "Refreshes the view of the current drawing."
    "Zoom In", |icon30|, "[Ctrl]+[+]", "Increase view of drawing by 25% increments."
    "Zoom Out", |icon31|, "[Ctrl]+[-]", "Decrease view of drawing by 20% increments."
    "Auto Zoom", |icon32|, "*za*", "Resize the view of the drawing to fill the drawing window."
    "Previous View", |icon33|, "*zv*", "Revert to the previous zoom level of the drawing."
    "Window Zoom", |icon34|, "*zw*", "Increase the view of the selected area to fill the drawing window."
    "Zoom Panning", |icon35|, "*zp*", "Move the view of the drawing in the window."



Plugins
-------

.. csv-table:: 
    :widths: 20, 7, 15, 58
    :header-rows: 1
    :stub-columns: 0
    :class: table-fix-width

    "Menu Item", "Icon", "Short-cut", "Description"
    "Align", , "", "Align selected entities to a reference by defining the final positions of 2 initial points."
    "Read ascii points", , "", "Read points from a text file. Each line of the file is a point defined by an ID, X coordinate, Y coordinate, Z coordinate and an optional code. Each field can be separated by a comma, a tab or a space. The decimal separator is the point (.). The points can be connected with a line, ID, or coordinate and code fields can be plotted as text."
    "Divide", , "", "Divide a line or a circle with *n* sections. A tick can be located at the limit of each section to show each limit.  The size of this tick can be defined as a percentage of the segment length. The line or the circle can be broken at the limit of each section using :ref:`Divide <tool-modify>` tool."
    "Gear plugin", , "", "Draw a gear by selecting the center of gear and defining parameters such as number of teeth, modulus, etc."
    "ESRI Shapefile", , "", "Import GIS geospatial vector data shapefile (i.e. maps). **Warning:** The import process will lock LibreCAD until it is complete and large files can be very time consuming."
    "List entities", , "", "List the selected entities along with their properties such as ID, layer, color, line type, line thickness, coordinates."
    "Read PIC file", , "", "Import Pic graphics language diagrams."
    "Plot plugin", , "", "Plot a mathematical function or a parametric function using the drawing coordinate system. The formula, start value, end value and step value are required. The plot can be lines, a polyline or a spline."
    "Same properties", , "", "Apply the properties of a reference entity to selected entities. The modified properties are layer, color, line type and line thickness."
    "Sample plugin", , "", "Draw a line by specifying the X and Y coordinates of end points."


Tools
-----

See :ref:`tools` for a description of the drawing tools.


Widgets
-------

.. csv-table:: 
    :widths: 20, 7, 15, 58
    :header-rows: 1
    :stub-columns: 0
    :class: table-fix-width

    "Menu Item", "Icon", "Short-cut", "Description"
    "Dock Areas", , "", "Toggles the visibility of the left, right, top, bottom and /or floating *Dock Widgets*."
    "Dock Widgets", , "", "See :ref:`widgets` for descriptions."
    "Toolbars", , "", "Toggles the visibility of the :ref:`toolbars <toolbars>`."
    "Menu Creator", |icon36|, "", "Create custom menus.  See :ref:`menu-creator` in **Getting Started** for details."
    "Toolbar Creator", |icon37|, "", "Create custom toolbars.  See :ref:`toolbar-creator` in **Getting Started** for details."


Drawings
--------

.. csv-table:: 
    :widths: 20, 7, 15, 58
    :header-rows: 1
    :stub-columns: 0
    :class: table-fix-width

    "Menu Item", "Icon", "Short-cut", "Description"
    "Tab mode", , "", "When selected, each open drawing is in its own tabbed drawing or preview window.  Tabbed windows cannot be moved, resized or arranged with in the LibreCAD application window.  The selected tab is the active window."
    "Window mode", , "", "When selected, each open drawing is in its own independent drawing or preview window that can be moved, resized or otherwise arranged (see below).  ”Window mode” is the default mode."
    "Layout", , "", "*Tab mode only*.  Allows the selection of the tab's appearance (”Rounded” or ”Triangular”) and the location of the drawing windows tab (”North”, ”South”, ”East” or ”West” (top, bottom, right, or left respectively))."
    "Arrange", , "", "*Window mode only*.  Drawing windows can be ”Maximize”, ”Cascade”, ”Tiled”,  ”Tiled Vertically”, ”Tiled Horizontally”"
    "*Currently opened drawings*", , "", "List the current open drawing(s).  The item with the checked box is the active drawing."




Help
----

.. csv-table:: 
    :widths: 20, 7, 15, 58
    :header-rows: 1
    :stub-columns: 0
    :class: table-fix-width

    "Menu Item", "Icon", "Short-cut", "Description"
    "Online", , "", "Displays links to online resources; Wiki, User's Manual, Command, Style Sheets, Widgets, Forum and Release Information."
    "About", |icon00|, "", "Displays with information about the current version of LibreCAD and web links: to the ''Contributors'', License and ''The Code'' repository."
    "License", , "", "Displays the license text (GNU General Public License version 2)."


..  Icon mapping:

.. |icon00| image:: /images/icons/librecad.png
            :height: 24
            :width: 24
.. |icon01| image:: /images/icons/new.svg
            :height: 24
            :width: 24
.. |icon02| image:: /images/icons/new_from_template.svg
            :height: 24
            :width: 24
.. |icon03| image:: /images/icons/open.svg
            :height: 24
            :width: 24
.. |icon04| image:: /images/icons/save.svg
            :height: 24
            :width: 24
.. |icon05| image:: /images/icons/save_as.svg
            :height: 24
            :width: 24
.. |icon06| image:: /images/icons/import.svg
            :height: 24
            :width: 24
.. |icon07| image:: /images/icons/export.svg
            :height: 24
            :width: 24
.. |icon08| image:: /images/icons/print.svg
            :height: 24
            :width: 24
.. |icon09| image:: /images/icons/print_preview.svg
            :height: 24
            :width: 24
.. |icon10| image:: /images/icons/close.svg
            :height: 24
            :width: 24
.. |icon11| image:: /images/icons/quit.svg
            :height: 24
            :width: 24

.. |icon13| image:: /images/icons/settings.svg
            :height: 24
            :width: 24
.. |icon14| image:: /images/icons/drawing_settings.svg
            :height: 24
            :width: 24

.. |icon18| image:: /images/icons/cursor.svg
            :height: 24
            :width: 24
.. |icon19| image:: /images/icons/undo.svg
            :height: 24
            :width: 24
.. |icon20| image:: /images/icons/redo.svg
            :height: 24
            :width: 24
.. |icon21| image:: /images/icons/cut.svg
            :height: 24
            :width: 24
.. |icon22| image:: /images/icons/copy.svg
            :height: 24
            :width: 24
.. |icon23| image:: /images/icons/paste.svg
            :height: 24
            :width: 24
.. |icon24| image:: /images/icons/delete.svg
            :height: 24
            :width: 24

.. |icon27| image:: /images/icons/grid.svg
            :height: 24
            :width: 24
.. |icon28| image:: /images/icons/draft.svg
            :height: 24
            :width: 24
.. |icon29| image:: /images/icons/redraw.svg
            :height: 24
            :width: 24
.. |icon30| image:: /images/icons/zoom_in.svg
            :height: 24
            :width: 24
.. |icon31| image:: /images/icons/zoom_out.svg
            :height: 24
            :width: 24
.. |icon32| image:: /images/icons/zoom_auto.svg
            :height: 24
            :width: 24
.. |icon33| image:: /images/icons/zoom_previous.svg
            :height: 24
            :width: 24
.. |icon34| image:: /images/icons/zoom_window.svg
            :height: 24
            :width: 24
.. |icon35| image:: /images/icons/zoom_pan.svg
            :height: 24
            :width: 24
.. |icon36| image:: /images/icons/create_menu.svg
            :height: 24
            :width: 24
.. |icon37| image:: /images/icons/create_toolbar.svg
            :height: 24
            :width: 24
