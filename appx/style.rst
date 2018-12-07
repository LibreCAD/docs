.. _style-sheets: 

Style Sheets
============

In “Widget Options” you can choose a style; the style list is dependent on your operating system and the version of Qt used to build LibreCAD.  For example on Windows 7 and using Qt 5 the list is: ("Windows", "Fusion").  More information can be found at http://doc.qt.io/qt-5/stylesheet.html and http://blog.qt.io/blog/2012/10/30/cleaning-up-styles-in-qt5-and-adding-fusion/

Any style of a “Style Sheet” can be modified, but it is recommended that the “Fusion” style (Qt 5) be used as a base, because it is intended to be a cross platform style.  After setting a style sheet you can edit it & save and then switch back to LibreCAD and use “Reload Style Sheet” (Ctrl+T).

Tips:

    - Play around with the example below for an easy start.
    - Look at the examples for “Color” and “Gradient” in the list of property types.
    - Check out the widget specific examples at: http://doc.qt.io/qt-5/stylesheet-examples.html


Example
-------

    A style sheet can be as simple as:: QMenu { font-size: 16px; }



    Or as a more complex example, save the following as alpha.qss or alpha.txt, and then choose it in “Widget Options”:

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


