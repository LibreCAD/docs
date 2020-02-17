.. User Manual, LibreCAD v2.2.x

.. Default include
.. include:: /inclFiles/notice.rst


.. _customize:

Customizing LibreCAD's Interface
================================

Custom menus and toolbars can be created to suit the users' preferences.  


.. _menu-creator:

Menu Creator
------------

To create, modify, or delete a custom menu, select **Widgets -> Menu Creator**


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

    #. Input a name into the **Name** drop down box
    #. Double-click on an action to add it
    #. Drag and drop to arrange actions
    #. Click the **Create** button

To edit an existing menu:

    #. Select the menu from the **Name** drop down box
    #. Double-click to remove actions
    #. Drag and drop to arrange actions
    #. Click the **Create** button

To delete an existing menu:

    #. Select the menu from the **Name** drop down menu
    #. Click the **Destroy** button


Custom menus can also be assigned to a keyboard short-cut to make them easily accessible:

.. figure:: /images/menuAssign.png
    :align: right
    :scale: 100
    :alt: LibreCAD Menu Assigner

.. actual image size 208px x 188px

To assign a menu to a keyboard short-cut:

    #. Click the **Assign** button
    #. Select the desired activator(s); "Double-Click", "Right-Click", "Ctrl-Right-Click", and / or "Shift-Right-Click"
    #. Click the **Save** button

To remove assignment:

    #. Click the **Assign** button
    #. DeSelect the desired activator(s)
    #. Click the **Save** button


.. _toolbar-creator:

Toolbar Creator
---------------

To create a custom toolbars, select **Widgets -> Toolbar Creator**

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

    #. Input a name into the **Name** drop down box
    #. Double-click on an action to add it
    #. Drag and drop to arrange actions
    #. Click the **Create** button

To edit an existing toolbar:

    #. Select the toolbar from the **Name** drop down box
    #. Double-click to remove actions
    #. Drag and drop to arrange actions
    #. Click the **Create** button

To delete an existing toolbar:

    #. Select the toolbar from the **Name** drop down box
    #. Click the **Destroy** button


.. _widget-options:

Widget Options
--------------

.. figure:: /images/widgetOptions.png
	:align: right
	:scale: 67
	:alt: Widget Options

.. actual image size 328px x 438px

Widget Options change the appearance of LibreCAD.  Options are available for:

    - General: LibreCAD's application window decorations (borders, buttons, etc.) and permits the use of custom *style sheets* (see below).
    - Toolbar: the *Theme* and size of the toolbars' icons.
    - Statusbar: the overall height of the statusbar and the size of the font used.


.. _style-sheets: 

Style Sheets
------------

In “Widget Options” you can choose a style; the style list is dependent on your operating system and the version of Qt used to build LibreCAD.  For example on Windows 7 and using Qt 5 the list is: ("Windows", "Fusion").  More information can be found at http://doc.qt.io/qt-5/stylesheet.html and http://blog.qt.io/blog/2012/10/30/cleaning-up-styles-in-qt5-and-adding-fusion/

Any style of a “Style Sheet” can be modified, but it is recommended that the “Fusion” style (Qt 5) be used as a base, because it is intended to be a cross platform style.  After setting a style sheet you can edit it & save and then switch back to LibreCAD and use “Reload Style Sheet” (Ctrl+T).

Tips:

    - Play around with the example below for an easy start.
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

