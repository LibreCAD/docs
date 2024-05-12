.. User Manual, LibreCAD v2.2.0

.. Default include
.. include:: /inclFiles/notice.rst


.. _customize:

Customizing LibreCAD's Interface
================================

In addition to be able to :ref:`move and reorganize menus and toolbars <app-layout>`, LibreCAD can be customized with user-defined pop-up menus, custom toolbars and alternative "window decorations".


.. _menu-creator:

Menu Creator
------------

The Menu Creator is used to create, modify, or delete custom **pop-up menus**.  The pop-up menu is actived by using the mouse assigments described below.  Open the Menu Creator by selecting **Options -> Widgets -> Menu Creator**


.. only:: html

	.. figure:: /images/menuCreator.png
			:align: center
			:scale: 67
			:alt: LibreCAD Menu Creator

.. only:: latex

 	.. figure:: /images/menuCreator.png
		:align: center
		:scale: 50
		:alt: LibreCAD Menu Creator

.. actual image size 728px x 404px
	

To create a new menu:

    #. Input a name for the menu into the **Name** drop-down box.
    #. Select an action from the left-hand list and use the right arrow (or double-click on the action) to add it to the new menu (right-hand list).
    #. Drag and drop the items on the right-hand list to arrange the actions in the menu.
    #. Click the **Create** button.

To edit an existing menu:

    #. Select the menu from the **Name** drop-down box.
    #. Add additional items as described above.
    #. To remove an item from the menu, select an action from the right-hand list and use the left arrow (or double-click on the action) to remove it from the menu.
    #. Drag and drop the items on the right-hand list to arrange the actions.
    #. Click the **Update** button.

To delete an existing menu:

    #. Select the menu from the **Name** drop-down menu.
    #. Click the **Destroy** button.

.. only:: html

	.. figure:: /images/menuAssign.png
		:align: right
		:scale: 100
		:alt: LibreCAD Menu Assigner

.. only:: latex

	.. figure:: /images/menuAssign.png
		:align: right
		:scale: 67
		:alt: LibreCAD Menu Assigner

.. actual image size 208px x 188px

A custom pop-up menu needs to be assigned to a mouse button to make them accessible:

    #. Click the **Assign** button
    #. Enable one or more of the activators ("Double-Click", "Right-Click", "Ctrl-Right-Click", and / or "Shift-Right-Click") with a check in the check-box.
    #. Click the **Save** button


.. _toolbar-creator:

Toolbar Creator
---------------

Custom toolbars can be created, modified and deleted using the Toolbar Creator.  From the menubar, select **Options ->Widgets -> Toolbar Creator**.

.. only:: html

	.. figure:: /images/toolbarCreator.png
		:align: center
		:scale: 67
		:alt: LibreCAD Toolbar Creator

.. only:: latex

	.. figure:: /images/toolbarCreator.png
		:align: center
		:scale: 50
		:alt: LibreCAD Toolbar Creator

.. actual image size 728px x 404px

To create a new toolbar:

    #. Input a name into the **Name** drop-down box
    #. Double-click on an action to add it
    #. Drag and drop to arrange actions
    #. Click the **Create** button

To modify an existing toolbar:

    #. Select the toolbar from the **Name** drop-down box
    #. Double-click to remove actions
    #. Drag and drop to arrange actions
    #. Click the **Create** button

To delete an existing toolbar:

    #. Select the toolbar from the **Name** drop-down box
    #. Click the **Destroy** button


.. _widget-options:

Widget Options
--------------

.. only:: html

	.. figure:: /images/widgetOptions.png
		:align: right
		:scale: 67
		:alt: Widget Options

.. only:: latex

	.. figure:: /images/widgetOptions.png
		:align: right
		:scale: 50
		:alt: Widget Options

.. actual image size 328px x 438px

"Widgets" in this context refer to appearance of LibreCAD's border and title bar, icons and the statusbar.  Select **Options - > Widget Options** from the menubar to change these options.  The following options are available for:

    - General: LibreCAD's application window decorations (borders, buttons, etc.) and permits the use of custom *style sheets* (see below).
    - Toolbar: change the *Theme* and size of the toolbars' icons.
    - Statusbar: change the height of the statusbar and the size of the font used.

To enable an option, place a check in the checkbox and specify the desired option.

.. _style-sheets: 

Style Sheets
------------

In “Widget Options” you can also choose a style; the style list is dependent on your operating system and the version of Qt used to build LibreCAD.  For example on Windows 7 and using Qt 5 the list is: ("Windows", "Fusion").  More information can be found at http://doc.qt.io/qt-5/stylesheet.html and http://blog.qt.io/blog/2012/10/30/cleaning-up-styles-in-qt5-and-adding-fusion/

Any style of a “Style Sheet” can be modified, but it is recommended that the “Fusion” style (Qt 5) be used as a base, because it is intended to be a cross platform style.  After setting a style sheet you can edit it & save and then switch back to LibreCAD and use “Reload Style Sheet” (Ctrl+T).

Tips:

    - Start with the example below to obtain and understanding of how style sheet affect the appearance of LibreCAD.
    - Look at the examples for “Color” and “Gradient” in the list of property types.
    - Check out the widget specific examples at: http://doc.qt.io/qt-5/stylesheet-examples.html


Example
```````

A style sheet can be as simple as:

:: 

    QMenu { font-size: 16px; }

Or as a more complex example, save the following text as alpha.qss or alpha.txt, and then load the file with Options -> Widget Options -> Style Sheet:

::

    /* alpha.qss v.01 a modification of the Fusion style */

    /* Layer List */
    QTableView
    {
        selection-background-color: #ccffcc;
        selection-color: Blue;
        font-size: 16px;
        font-family: "Arial";
    }

    QMenu 
    {
        padding: 4px;
        font-size: 16px;
    }

    QMenu::item 
    {
        padding: 2px 25px 2px 20px;
        border: 1px solid transparent; /* reserve space for selection border */
    }

    QMenu::item:selected 
    {
        border-color: darkblue;
        background: rgba(240, 255, 255, 150);
    }

    QMenu::icon:selected 
    {
        border-color: darkblue;
        background: rgba(255, 255, 255, 255);
    }

    QToolBar 
    {
        background-color: rgb(230, 230, 230);
        spacing: 3px;
        padding: 4px;
    }

    QToolButton 
    {
        background-color: #eeeeee;
        border-style: outset;
        border-width: 2px;
        border-radius: 2px;
        border-color: beige;
        font: 12px;
        padding: 2px;
    }

    QToolButton:checked 
    {
        border-color: grey;
        background-color: qlineargradient(x1: 0, y1: 0, x2: 0, y2: 1,
	                                  stop: 0 #dadbde, stop: 1 #f6f7fa);
    }

    QToolButton:hover 
    {
        border-color: grey;
        background-color: qlineargradient(x1: 0, y1: 0, x2: 0, y2: 1,
	                                  stop: 0 #dadbde, stop: 1 #f6f7fa);
    }

    QStatusBar { background-color: azure;}

    QMenuBar { background-color: #fefefe; }

    QTextEdit { background-color: honeydew; }

    QToolTip { background-color: white; }

