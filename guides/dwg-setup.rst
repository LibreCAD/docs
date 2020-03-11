.. User Manual, LibreCAD v2.2.x

.. Default include
.. include:: /inclFiles/notice.rst


.. _drawing-setup:

Setting up a Drawing
====================

As with other software; word processors, spreadsheets, etc, there are many ways a user can to setup or configure a new document.  With LibreCAD, that document is a drawing.  Some of the preferences for a drawing will be governed by drafting conventions, some will be determined by organizational requirements, and others might just be personal preferences.  The drawing's setup is largely determined by the :ref:`Drawing Preferences <draw-prefs>`.

Under normal circumstances, after the initial installation and :ref:`configuration <configure>`, little if any configuration needs to done when starting a new drawing.  There are a many drawing parameters to be considered to suit the drawing requirements and final appearance.  The majority of these settings can be left as the defaults as LibreCAD's defaults reflect normal drafting conventions and practices, such as the "Text Height" of 2.5mm / .10" / 3/32", etc.  Other preferences and attributes, such as layer, line thickness and type, pen colors, etc. can also be changed to suit users' requirements.

Some of the key considerations for setting up the drawing include:

    - Units, text and scale
    - Layers
    - Line color, width and type


Drawing Unit
------------

During the initial setup, the default :ref:`unit of measure <measurements>` was set (defaulting to *millimeter*).  The unit of measure should be set to the unit most frequently used as it is used for all new drawings and doesn't need to be changed.  If necessary, the default unit of measure can be changed in the :ref:`Application Preferences <app-prefs>` or overridden for a single drawing in the Drawing Preferences.


.. _ug-scale:

Scale
-----

Setting the scale of a drawing is the easy part, drawings should be created *full-scale* (1:1)!  The zooming abilities of LibreCAD will make the whole drawing fit in the drawing window or magnify sections to view fine detail.  On the other hand, when producing output the drawing will need to be adjusted in size to fit the *page size*.  Generally, output is a printed page, but it can also be a pdf, or :ref:`exported to another image format <file>`.  

As an example, for an annotated drawing of a floor plan to appear correctly when the drawing is reduced in size, or *scaled down*, to print on an "A4" page (210 x 297 mm), the dimension text would need to be proportional to the floorplan itself prior to being reduced to fit the page.  Trying to determine the dimension text size for scaling such a large object would be tedious at best, but a feature of LibreCAD makes it simple.  The "General Scale" is used to adjust the dimension text, arrows and related parameters to the sizes suitable for the required page size.  Both the page size, and the dimensioning parameters - including the "General Scale" - are configured in the **Drawing Preferences**.

There are two tabs in **Drawing Preferences**, "Paper" and "Dimensions", that require attention when starting a new drawing.  Specifically the tabs that need to be addressed are:

      1. The "Paper" tab: Selecting a paper size and orientation will determine the *print scale* used for final output.  The print scale is used to determine the "General Scale" mentioned above.
      2. The "General Scale" on the "Dimensions" tab: Setting the "General Scale" will adjust the dimension text and related parameters to suit the page size after establishing the page size.

The paper format, orientation, and margins to be used is an important to consideration when setting the drawing preferences.  The page size is entirely up to the user to determine, based on what is available (depending on the printer or printing service that is being used).  While it can be done at anytime, establishing the page size sooner than later will help determine the "General Scale".

.. tip::

   If multiple options are available for the paper size, setting the paper *after drawing the object but prior to dimensioning a drawing* will help determine the print scale, the "General scale", and subsequently the appropriate line spacing for dimensions.  See :ref:`Dimensioning <dimensioning>` for additional information.

   Be sure to allow room on the drawing for dimension lines and text when determining the print scale.  More details on printing a drawing are found in the :ref:`Printing Guide <printing-guide>` for more details.

   While any scale can be used when printing a drawing there are commonly used scales for different types of drawings.  Refer to  :ref:`Scales <scales>` in the appendix for some examples.


.. _ug-layers:

Layers
------

One of LibreCAD's basic features is the abiltiy to use layers.  Layers help organize drawings by allowing users to place and manage related entities.  Traditional manual drafting used a similar approach.  Whether for engineering, architectural, construction, manufactuing or other types, layers were used to show different aspects on the drawing.  Layers could be added to show centre lines or dimensions on an engineering or manufacuring drawings, or to show different building systems on architectural drawings such as exterior walls, partitions, electrical, HVAC, grid lines, etc.  The layers were often drawn on separate transparent sheets of paper. These sheets were then overlaid one on top of another to produce final drawings.  While one layer can contain multiple entities, every entity in a drawing can only be associated with single layer.  Typically entities with common *functions* or attributes are put on the same layer. For example, all the walls in a floor plan drawing would be put on a layer named "Walls".  

Layers have an added advantage that all the :ref:`pen <entity-pen>` attributes can be assigned to a layer.  Every entity on that layer will adopt the attributes that have been assigned to the layer.  However, the attributes assigned by the layer can be overridden for entities if necessary.  In the above example a line thickness can capplied to all entities on the "Walls" layer by changing the "Layer Settings" for that layer.

.. tip::

    Note that layer **0** is a special layer and should not be used for general drawing purposes.  Create at least one additional layer for the drawing.


Using the Layer List Dock
~~~~~~~~~~~~~~~~~~~~~~~~~

In LibreCAD, layers are managed using the :ref:`Layer List Dock <widget-layerList>`.  Use the Layer List Dock to add and remove, show and hide and modify the layer's attributes.  Creating a layer is simple:

    - Click the **Add a layer** icon |icon01|.
	- Specify a *Layer Name*.
	- Optionally specify the Color, Width and Line Type for the layer.
	- Click **Ok**.

The first layer added defaults to the layer name "noname", but the name can be replace with any alpha-numeric text.  Additional layers add will adopt the name of the currently selected layer and append a sequential number.  

.. tip::

    Prefix the layer name with a sequential number when naming the layer to help organize the layers in the dock list.  Layers are listed in alpha-numeric order, e.g. 1a, 1b, 2a, 2b, etc.

Layers that have been completed can be *locked*.  Locking layers prevents accidental changes and can improve the performance when working with very large complex drawings.

Hiding layers while drawing reduces the *visual complexity* and makes it easier to focus on the current drawing efforts.

Refer to the :ref:`Dock Widgets <widgets>` in the **Reference** section for additional details on using other functions of the "Layer List Dock".


Construction Layers
```````````````````

A layer designated as a "Construction Layer" is special layer used to create reference geometry to help align other drawing entities.  A construction layer:

    - contains lines that are an infinite length, and
    - won't appear on printed drawings.


Ordering Layers and Entities
````````````````````````````

Layers are displayed in alpha-numeric order in the layer list.  However, the order of the layers do not relate to the order that entities appear in the drawing.  Each entity can be raised, *moved up*, or lowered, *moved down*, with respect to others.  Each layer can contain entities that are at different points.  Use the commands in **Tools -> Modify -> Order** to move entities up or down.

.. csv-table:: 
    :widths: 25, 25, 75
    :header-rows: 1
    :stub-columns: 0
    :class: table-fix-width

    "Action", "Key", "Result"
    "move to top", "[Home]", "Moves the selected entity to the *top* most position."
    "move to bottom", "[End]",  "Moves the selected entity to the *bottom* most position."
    "raise over entity", "[Page Up]",  "Moves the selected entity *up* one relative position."
    "lower after entity", "[Page Down]",  "Moves the selected entity *down* one relative position."


.. _ug-templates:

Templates
---------

Having to set the unit, page size and scale and layers each time a new drawing is created can be avoided by using *templates*.  Templates are *prototype* drawings that provide the means to save basic parameters and settings so a drawing does not have to be configured each time a new one is started.  The parameters and settings include the settings defined in the **Drawing Preferences**, such as the page size, main unit of measure, and the dimensioning format.  Templates can also include layers and layer attributes (line type, thickness, pen color) and other drawing elements such as a border. These settings are inherited by the new drawings created from the template.

When LibreCAD is launched it creates a new drawing using a *default template*.  The default template is also used when a new drawing is created within LibreCAD by selecting **File -> New** or clicking the **New** icon |icon02|.  The new document is initially called "unnamed document 1".  Any addition new drawings created while LibreCAD is still open will be number sequentially; "unnamed document 1", "unnamed document 2", and so on.  New drawings do not take the template's name as a file name, but only the template drawing contents.  Users are prompted for a file name when saving the drawing.

The default template, "empty.dxf", is installed with LibreCAD in the resources directory.  If only a single template is used, the default can be modified as needed.  The path to the default template depends on the operating system.  See the :ref:`Download and Install <install>` in the **Getting Started** section for the default installation locations.

User-defined templates can be created to suit various purposes such as different page sizes or orientation, unit of measure, etc.  User-defined templates can be used by selecting **File -> New From Template** or clicking the **New from Template** icon |icon03| and then selecting the desired template file.


Creating Templates
~~~~~~~~~~~~~~~~~~

Templates are created by creating a new drawing, setting the desired :ref:`Drawing Preferences <draw-prefs>`, and adding any required drawing elements (e.g. layers, borders, etc).  To create a template, starting with a blank drawing:

    - Set the the Drawing Preferences by selecting **Edit** from the menu bar and then **Current Drawing Preferences**.

        - On the "Paper" tab set the paper size, orientation and margins as desired.
        - Select the "Units" tab and set the "Main Drawing Unit".  (Note the "Length" and "Angle" configure the format of the :ref:`status bar <statusbar>` and not the dimensions that appear on the drawing.)
        - Click the "Dimensions" tab and adjust the values.  Refer to :ref:`Dimensions <dimn-prefs>` in **Drawing Preferences** for details.
        - Check the remaining tabs and adjust those settings as necessary.
        - Click "OK" when done.

    - Add the layers and other drawing elements as required.  Refer to :ref:`Layers <su-layers>` for details on using layers and setting the attributes.
    - Save the temmplate as a "dxf", e.g. "myTemplate.dxf", to any location with read / write permissions.

As an alternative to the default template, a user-defined template can be configured in the :ref:`Application Preferences <app-prefs>` on the **Paths** tab.  The specified template is used instead of the default LibreCAD template when the application is launched and for new drawings.


..  Icon mapping:

.. |icon01| image:: /images/icons/add.svg
            :height: 24
            :width: 24
