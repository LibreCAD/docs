.. _menu: 

Main Menu
=========

Many of LibreCAD's commands are accessible through the menu bar.  Each drop down menu provides access commands, configurations and yada, yada, yada, 

Each menu has a dashed line at the top.  Clicking in the dashed line allows the menu to be "torn off" as used as a floating menu.  Clicking the dot on the upper right corner of the floating menu closes it.


File
----

.. csv-table:: 
   :header: "Menu Item", "Icon", "Short-cut", "Description"
   :widths: 40, 10, 20, 110

    "New", |icon01|, "[Ctrl]-n", "Creates a new drawing file."
    "New from Template", |icon02|, "", "Creates a new drawing file from a template."
    "Open", |icon03|, "[Ctrl]-o", "Open existing drawing file."
    "Save", |icon04|, "[Ctrl]-s", "Save current drawing file."
    "Save as", |icon05|, "[Ctrl] [Shift]-q ", "Save current drawing file with a new file name or to a different location."
    "Import", |icon06|, "", "Import a :ref:`block <blocks>`, or bit mapped or vector images into the current drawing.  Supported bit mapped formats include: bmp, cur, gif, ico, jpeg, pbm, pgm, png, ppm, xbm, and xpm.  Vector images supported include svg, and svgz."
    "Export", |icon07|, "", "Export the current drawing as a CAM, pdf or image file. Supported bitmapped formats include: cur, jpeg, pbm, pgm, png, ppm, bmp, ico, xbm, and xpm.  Vector images supported include svg, and svgz.  Use the ''CAM'' export to save SVG (Scalable Vector Graphics) suitable for MakerCAM, EleskCAM, LaserWeb, ..."
    "Print", |icon08|, "[Ctrl]-p  ", "Produce output of the the current drawing.  See **Printing** in the :ref:`User Guides <printing-guide>` section."
    "Print Preview", |icon09|, "", "Preview output of the the current drawing on screen."
    "Close", |icon10|, "[Ctrl]-w", "Close the active drawing."
    "Quit", |icon11|, "[Ctrl]-q", "Close the application."
    "Recent Files", , "", "Open existing drawing file from a list of previously opened drawing files."


Options
-------
.. csv-table:: 
   :header: "Menu Item", "Icon", "Short-cut", "Description"
   :widths: 40, 10, 20, 110

    "Application Preferences", |icon13|, "", "See :ref:`Application Preferences <app-pref>` in **Getting Started** for details."
    "Current Drawing Preferences", |icon14|, "", "See :ref:`Drawing Preferences <draw-pref>` for details."
    "Widget Options", , "", "See :ref:`Widget Options <widget-options>` for in **Customizing** details."
    "Device Options", , "", "Select input device; mouse, tablet, trackpad or touchscreen."
    "Reload Style Sheet", , "[Ctrl]-t", "See :ref:`Style Sheets <style-sheets>` in **Appendices** for details."
 

Edit
----
.. csv-table:: 
   :header: "Menu Item", "Icon", "Short-cut", "Description"
   :widths: 40, 10, 20, 110

    "Selection Pointer", |icon18|, "[Esc]", "Reverts from current operation to selection pointer (e.g. cancels the current operation)"
    "Undo", |icon19|, "[Ctrl]-z", "Reverses the previous operations sequentially."
    "Redo", |icon20|, "[Ctrl]-[Shift]-z", "Reverses the previously reversed operations sequentially."
    "Cut", |icon21|, "[Ctrl]-x", "Removes the selected entity (or entities) and places it in temporary memory to be recalled.  A reference point needs to be placed for subsequent paste operations."
    "Copy", |icon22|, "[Ctrl]-c", "Creates a copy of the selected entity (or entities) in temporary memory to be recalled."
    "Paste", |icon23|, "[Ctrl]-v", "Recalls the entity (or entities) from temporary memory at a location defined by the reference point."
    "Delete Selected", |icon24|, "[Del]", "Removes the selected entity (or entities) from the current drawing."


View
----

.. csv-table:: 
   :header: "Menu Item", "Icon", "Short-cut", "Description"
   :widths: 40, 10, 20, 110

    "Fullscreen", , "[F11]", "Hides the application title bar and toggles LibreCAD to use the entire display."
    "Statusbar", , "[Ctrl]-i", "Toggles the visibilty of the status bar at the bottom of the application window."
    "Grid", |icon27|, "[Ctrl]-g", "Toggles the visibilty of the grid."
    "Draft", |icon28|, "[Ctrl]-d", "Toggles to or from ''Draft Mode''."
    "Redraw", |icon29|, "[Ctrl]-r", ""
    "Zoom In", |icon30|, "", "Increase view of drawing by 25% steps."
    "Zoom Out", |icon31|, "", "Decrease view of drawing by 25% steps."
    "Auto Zoom", |icon32|, "", "Resize the view of the drawing to fill the drawing window."
    "Previous View", |icon33|, "", "Revert to the previous zoom level of the drawing."
    "Window Zoom", |icon34|, "", "Increase the view of the selecteed area to fill the drawing window."
    "Zoom Panning", |icon35|, "", "Move the view of the drawing."



Plugins
-------

.. csv-table:: 
   :header: "Menu Item", "Icon", "Short-cut", "Description"
   :widths: 40, 10, 20, 110

    "Align", , "", ""
    "Read ascii points", , "", ""
    "Divide", , "", ""
    "Gear plugin", , "", ""
    "ESRI Shapefile", , "", ""
    "List entities", , "", ""
    "Read PIC file", , "", ""
    "Plot plugin", , "", ""
    "Same properties", , "", ""
    "Sample plugin", , "", ""


Tools
-----

See :ref:`tools` for a description of the drawing tools.


Widgets
-------

.. csv-table:: 
   :header: "Menu Item", "Icon", "Short-cut", "Description"
   :widths: 40, 10, 20, 110

    "Dock Areas", , "", "Toggles the visibility of the left, right, top, bottom and /or floating *Dock Widgets*."
    "Dock Widgets", , "", "See :ref:`widgets` for descriptions."
    "Toolbars", , "", "Toggles the visibility of the :ref:`toolbars <toolbars>`."
    "Menu Creator", |icon36|, "", "Create custom menus.  See :ref:`menu-creator` in **Getting Started** for details."
    "Toolbar Creator", |icon37|, "", "Create custom toolbars.  See :ref:`toolbar-creator` in **Getting Started** for details."


Drawings
--------

.. csv-table:: 
   :header: "Menu Item", "Icon", "Short-cut", "Description"
   :widths: 40, 10, 20, 110

        "Tab mode", , "", "Toggles LibreCAD to a tabbed drawing space.  Each open drawing is on its own tabbed drawing window when the tabbed mode is active (checked)."
        "*Currently opened drawings*", , "", "List the current open drawing(s).  The item with the checked box is the active drawing."


Help
----

.. csv-table:: 
   :header: "Menu Item", "Icon", "Short-cut", "Description"
   :widths: 40, 10, 20, 110

        "Online", , "", "Displays links to online resources; Wiki, User's Manual, Command, Style Sheets, Widgets, Forum and Release Information."
        "About", |icon00|, "", "Displays with information about the current version of LibreCAD and web links: to the ''Contibutors'', License and ''The Code'' repository."
        "License", , "", "Displays the license text (GNU General Public License version 2)."


..  Icon mapping:

.. |icon00| image:: /images/icons/librecad.png
.. |icon01| image:: /images/icons/new.svg
.. |icon02| image:: /images/icons/new_from_template.svg
.. |icon03| image:: /images/icons/open.svg
.. |icon04| image:: /images/icons/save.svg
.. |icon05| image:: /images/icons/save_as.svg
.. |icon06| image:: /images/icons/import.svg
.. |icon07| image:: /images/icons/export.svg
.. |icon08| image:: /images/icons/print.svg
.. |icon09| image:: /images/icons/print_preview.svg
.. |icon10| image:: /images/icons/close.svg
.. |icon11| image:: /images/icons/quit.svg
.. |icon12| image /images/icons/
.. |icon13| image:: /images/icons/settings.svg
.. |icon14| image:: /images/icons/drawing_settings.svg
.. |icon15| image /images/icons/
.. |icon16| image /images/icons/
.. |icon17| image /images/icons/
.. |icon18| image:: /images/icons/cursor.svg
.. |icon19| image:: /images/icons/undo.svg
.. |icon20| image:: /images/icons/redo.svg
.. |icon21| image:: /images/icons/cut.svg
.. |icon22| image:: /images/icons/copy.svg
.. |icon23| image:: /images/icons/paste.svg
.. |icon24| image:: /images/icons/delete.svg
.. |icon25| image /images/icons/
.. |icon26| image /images/icons/
.. |icon27| image:: /images/icons/grid.svg
.. |icon28| image:: /images/icons/draft.svg
.. |icon29| image:: /images/icons/redraw.svg
.. |icon30| image:: /images/icons/zoom_in.svg
.. |icon31| image:: /images/icons/zoom_out.svg
.. |icon32| image:: /images/icons/zoom_auto.svg
.. |icon33| image:: /images/icons/zoom_previous.svg
.. |icon34| image:: /images/icons/zoom_window.svg
.. |icon35| image:: /images/icons/zoom_pan.svg
.. |icon36| image:: /images/icons/create_menu.svg
.. |icon37| image:: /images/icons/create_toolbar.svg
.. |icon38| image /images/icons/
.. |icon39| image /images/icons/
.. |icon40| image /images/icons/
