.. User Manual, LibreCAD v2.2.x


.. _configure: 

Configuration
=============

LibreCAD's "Welcome" dialog is shown the first time LibreCAD is launched after installation.  The dialog prompts the user to select the :ref:`Default Unit <measurements>` and the languages to be used for the GUI and for the commands: 

.. figure:: /images/LC_welcome.png
    :width: 705px
    :height: 410px
    :align: center
    :scale: 75
    :alt: LibreCAD Welcome


LibreCAD then starts with its default configuration and is ready use.  The user interface consists of several elements as shown below:

    - *Menu*: provides access to application functions (open, close, etc.) and drawing tools.  Menus can be customized to suit user preferences.
    - *Toolbars*: provides access to drawing tools and functions.  
    - *Docks*:  provides access to drawing tools and functions. 
    - *Status bar*: displays coordinates (absolute and relative), active mouse button, selected entity information and grid status.
    - *Drawing window*: displays the active drawing.


.. figure:: /images/LC_default_annotated.png
    :width: 1280px
    :height: 960px
    :align: center
    :scale: 50
    :alt: LibreCAD Application Window


.. _app-layout:

Layout
------

LibreCAD's layout and appearance is highly configurable:

    - *Menus*: drop down from the menu bar or can be "torn off" and float anywhere on the display. Click the dashed line at the top of a menu to detach it.
    - *Toolbars*: can be dragged and dropped to the top, bottom, left, right, or float anywhere on the display.
    - *Docks Widgets*: (e.g. command line or layer list) can also be dragged and dropped to the top, bottom, left, right, or float within the drawing window.  In addition they can be stacked in the same region of the application window where they will be "tabbed".  Optionally docks can be placed outside of the application window, such as when using multiple monitors.  Drawing tools are also available as dock widgets, but are suited as floating "toolboxes".  Widgets can also be resized by dragging their edges.
    - *Style sheets*: allow users to change the visual elements of the application's window decorations; title bars, fonts, colours, etc.  Refer to the :ref:`appendix <style-sheets>` for more details.

.. figure:: /images/LC_everything2.png
    :width: 1280px
    :height: 960px
    :align: center
    :scale: 50
    :alt: LibreCAD Application Window - custom layout


.. _app-prefs:

Application Preferences
-----------------------

In addition to the layout, LibreCAD has many preferences that will change other aspects of the appearance or behavior of the application. The preferences can be configured by selecting *Options -> Application Preferences*.  Different elements of the preferences can be set; Appearance, Paths and Defaults.


Appearance
~~~~~~~~~~

.. Text for describing images follow image directive.

.. figure:: /images/appPref1.png
    :width: 785px
    :height: 623px
    :align: right
    :scale: 50
    :alt: LibreCAD Application Preferences - Appearance

There are three categories on the "Appearence" tab that allows the user to change the look and behaviour of LibreCAD.

The *Graphic View* category has options for the snap indicator style and shape, scrollbars and grid.  Use the *Snap Indicator Lines* to select the style for orthogonal (Crosshair, Crosshair 2 or Spiderweb) or isometric (Isometric) projections.  The *Anti-alias* setting, if supported by the hardware, when checked will reduce jagged edgdes of diagonal lines, circles, etc.

The *Language* categories allows the the user to select the language used in the GUI and command line.  Supported languages can be found in the :ref:`appendix <languages>`.

Thirdly, the *Graphic Colors* section allow custom colors to be selected for the snap indicator, drawing background,  grid, and other indicators (selections, highlighted items and Handlles).  Users can select predefined colors from the drop down menu or select their own from the color selector.


Path
~~~~

.. figure:: /images/appPref2.png
    :width: 785px
    :height: 623px
    :align: right
    :scale: 50
    :alt: LibreCAD Application Window - Paths

The *Path* tab allows users to specify the directory paths to additional resources; language ("Translations") and user created or installed Hatch Patterns, Fonts, Parts libraries and Templates and a "Variable file".  These paths do not override the defaults paths, but are appended so the default resources are still available.  It is recommended that user defined resource be placed in a user directory (e.g. home directory on Linux: ~/LibreCAD/Translations, etc.)

    - *Translations*: Language files for the GUI and / or command languages.
    - *Hatch Patterns, Fonts, Parts Libraries*: user created or obtained from other sources such as the Parts Library wiki
    - *Template*: load the user-defined template drawing when starting the application
    - *Variable File*: load a user-defined variable file when starting the application (see the :ref:`Command Line <commandline>` guide for details on using commands / variables files.)


Defaults
~~~~~~~~

.. figure:: /images/appPref3.png
    :width: 785px
    :height: 623px
    :align: right
    :scale: 50
    :alt: LibreCAD Application Window - Defaults

Drawing Defaults
````````````````

    *Unit*: Defines the :ref:`default unit of measure <measurements>` for all new drawings.  The default can be over-ridden by setting the unit of measure in the Drawing preferences or template.  {{Add links}}


Program Defaults
````````````````

    - *Auto backup*: When check, a backup will be created when closing the file.  Backup files are saved to the same directory as the drawing file with a tilde (~) appended to the file name.
    - *Auto save time*: The time in minutes to perform an automatice save of the open files.  Auto files are saved to the same directory as the drawing file with a hash symbol (#) prefixed to the file name.
    - *Don't use native OS file open dialog*: When checked, LibreCAD's file open dialog is displayed when opening files.
    - *Modify layer of selected entities, at layer activation*: ??

Clear Settings
``````````````
LibreCAD's configuration can be partially or entirely reset back to a defaults:

    - *Layout*: Resets the application window *layout* to the default configuration.
    - *All*: Resets the application to the default configuration.  Window layout, color settings, custom menus and toolbars, etc. are all reset.  The "Welcome" dialog will be displayed next time the application is launched.

Startup
```````
When checked the following items will:

    - *Display loading screen*: LibreCAD's load screen (e.g. splash screen) is displayed when launching the application.
    - *Start in tab mode*: the drawing window is tabbed (same as selecting Drawings -> Tab mode from the main menu).
    - *Start with main window maximized*: LibreCAD will start with the application window full screen. 
    - *Enable CAD dockwidgets*: show drawing tools (Circle, Curve, etc.) in the widget menu (Widgets -> Dockwidgets)  
    - *Enable CAD toolbars*: show drawing tools (Circle, Curve, etc.) in the toolbar menu (Widgets -> Toolbars)

