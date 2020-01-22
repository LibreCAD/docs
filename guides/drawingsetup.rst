.. User Manual, LibreCAD v2.2.x


.. _drawing-setup:

Setting up a Drawing
====================

As with other software; word processors, spreadsheets, etc, there are many ways a user can to setup or configure a new document.  With LibreCAD, that document is a drawing.  Some of the preferences for a drawing will be governed by drafting conventions, some will be determined by organizational requirements, and others might just be personal preferences.  The drawing's setup is largely determined by the :ref:`Drawing Preferences <draw-prefs>`.

Under normal circumstances, after the initial installation and :ref:`configuration <configure>`, little if any configuration needs to done when starting a new drawing.  During the initial setup, the default :ref:`unit of measure <measurements>` was set (defaulting to *millimeter*).  The unit of measure should be set to the unit most frequently used as it is used for all new drawings and doesn't need to be changed.  If necessary, the default unit of measure can be changed in the :ref:`Application Preferences <app-prefs>` or overridden for a single drawing in the Drawing Preferences.

There are a many drawing parameters to be considered to suit the drawing requirements and final appearance.  The majority of these settings can be left as the defaults as LibreCAD's defaults reflect normal drafting conventions and practices, such as the "Text Height" of 2.5mm / .10" / 3/32", etc.  Other preferences and attributes, such as layer, line thickness and type, pen colors, etc. can also be changed to suit users' requirements.


Scale
-----

Setting the scale of a drawing is the easy part, drawings should be created *full-scale* (1:1)!  The zooming abilities of LibreCAD will make the whole drawing fit in the display window or zoom into the fine detail.  On the other hand, when producing output the drawing will need to be scaled to fit the *page*.  Generally output is a printed page, but it can also be a pdf, or :ref:`exported to another image format <file>`.  While these two points seem contradict each other as a full-scale drawing of something very large, like a building, would require an equally large text size for notes and dimensions to appear correctly , for example, when the drawing is scaled down to print on an "A1" page.  Trying to determine the dimension text size for a large object would be tedious at best, but a feature of LibreCAD makes it simple.  It is addressed by the "General Scale" on the "Dimensions" tab of the **Drawing Preferences**.  The "General Scale" is used to adjust the dimension text, arrows and related parameters to the sizes suitable for the required page format.

Determining the value for the "General Scale" for the best results is simple, it is the *inverse* of the print scale obtained prior to printing.  For example, if a print scale is determined to be "1:10", the "General Scale" is 10 (10:1).  Setting the "General Scale" to the inverse of the print scale results in the dimension text being the defined size, e.g. 2.5mm, on the printed drawing.  The drawing is scaled down to fit the page and the dimension text is scaled up to be legible.  The print scale can be determined by using LibreCAD's print preview feature.  See :ref:`Printing to Scale <print-scale>` in the Printing Guide for more details.

There are two tabs in **Drawing Preferences**, "Paper" and "Dimensions", require attention when determining and setting the scale values.  Specifically the parameters that need to be addressed are:

      1. "Format" on the "Paper" tab: Selecting a paper size and orientation will determine the *print scale* used for final output.  The print scale is used to determine the "General Scale" as noted above.
      2. "General Scale" on the "Dimensions" tab: Setting the "General Scale" will adjust the dimension text and related parameters to suit the output.

The "Format", e.g. paper size and orientation, to be used is an important to consideration when setting the drawing preferences.  The format is entirely up to the user to determine, based on what is available (depending on the printer or printing service that is being used).  While it can be done at anytime, establishing the format sooner than later will help determine the "General Scale".  

.. tip::
   Setting the paper size *after drawing the object but prior to dimensioning a drawing* will help determine the print scale, the "General scale", and subsequently the appropriate line spacing for dimensions.  See :ref:`Dimensioning <dimensioning>` for additional information.

   Be sure to allow room on the drawing for dimension lines and text when determining the print scale.

   While any scale can be used when **printing** a drawing there are commonly used scales for different types of drawings.  Refer to  :ref:`Scales <scales>` in the appendix for some examples.


Using Layers
------------

Layers help organize drawings by allowing users to place and manage related entites.  Layers can be thought of transparent drawing sheets inserted and placed on top of one another and temporarily or permanently removed.  Layers have the added advantage in that the :ref:`pen <entity-pen>` attributes can be modified for all entities on the layer.  Layers are added, removed, hidden and modified using the :ref:`Layer List Dock <widget-layerList>`.

.. note::
   Note that layer **0** is a special layer and should not be used.  Create at least one new layer for the drawing.

Hiding layers while drawing reduces the *visual complexity* and makes it easier to focus on the current drawing efforts.

.. _layers:

Layers
~~~~~~

A basic feature of CAD is the use of layers to organize a drawing. Every entity in a drawing is on exactly one layer, however one layer can contain multiple entities. Typically entities with a common 'function' or common attributes are put on the same layer. For example, it might be might necessary to put all axis in a drawing on a layer named 'axis'.  Each layer can be defined with a "Default Pen" (see :ref: `Pens <pens>` below). Each entity can have its own attributes or have its attributes defined by the layer it is placed on. In the latter case for example you can change the colour of all the entities on the "axes" layer by setting the colour (red for example) for that layer.

In traditional manual drafting, a similar approach was used. Whether for Engineering, Architectural or Construction drawing etc. layers were used to show different aspects of a drawing — for example this could be a layer set up for showing centre lines on an engineering drawing or to show different building systems, such as wiring and air conditioning. The layers were often drawn on separate transparent sheets of paper. These sheets were then overlaid one on top of another to produce final drawings.

Layers are displayed in alpha-numerical order in the layer list.  However this is does not relate to the order that each entity appears on the z-axis of the drawing.  Each entity can be raised or lowered with respect to others, and each layer can contain entities that are at different points on the z-axis.  Use the four Draw Order commands (under the **Tools -> Modify -> Order menu**) to move entities up or down the z-axis. 

Creating a Layer
````````````````

Layers are usually created to hold entities with common attributes. Creating a layer is simple:

	- Click the **Add a layer** icon |icon01|.
	- Specify a *Layer Name*.
	- Optionally specify the Color, Width and Line Type.
	- Click **Ok**. 
  
Layers that have been completed can be *locked*.  Locking layers prevents accidental changes and can improve the performance when working with very large complex drawings.


Construction Layers
~~~~~~~~~~~~~~~~~~~

A layer designated as a "Construction Layer" is special layer used to create reference geometry to help align other drawing entities.  A contruction layer:

    - contains lines that are an infinite length, and
    - won't appear on printed drawings.


Ordering Layers and Entities
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Layers are displayed in alpha-numeric order in the layer list.  However, the order of the layers do not relate to the order that entities appear in the drawing.  Each entity can be raised, *moved up*, or lowered, *moved down*, with respect to others.  Each layer can contain entities that are at different points.  Use the commands in **Tools -> Modify -> Order** to move entities up or down.

.. csv-table:: 
    :widths: 25, 25, 75
    :header-rows: 1
    :stub-columns: 0
    :class: fix-table

    "Action", "Key", "Result"
    "move to top", "[Home]", "Moves the selected entity to the *top* most position."
    "move to bottom", "[End]",  "Moves the selected entity to the *bottom* most position."
    "raise over entity", "[Page Up]",  "Moves the selected entity *up* one relative position."
    "lower after entity", "[Page Down]",  "Moves the selected entity *down* one relative position."


.. _templates:

Templates
---------

Templates are *prototype* drawings that provide the means to save basic parameters and settings so a drawing does not have to be configured each time a new one is started.  The parameters and settings include the settings defined in the Drawing Preferences, such as the paper format, main unit of measure and format, and dimension format.  Templates can also include layers and layer configuration, line type and thickness, pen color, and other drawing elements such as a border. These settings are inherited by the drawings created from the template.

Templates are created by starting a new drawing, setting the desired :ref:`Drawing Preferences <draw-prefs>`, and adding any required drawing elements (e.g. layers, borders, etc).  Starting with a blank drawing in LibreCAD, select "Edit" from the menu bar and then "Current Drawing Preferences".  On the first tab labeled "Paper", set the paper size and orientation as desired.  Next, select the "Units" tab and set the options as desired.  Click the "Dimensions" tab and adjust the values as desired.  Check the remaining tabs and adjust those settings as necessary.  Click "OK" when done.  Add the layers and other drawing elements as required.  Refer to :ref:`Layers <layers>` for details on using layers and setting the attributes.

Once the template has been prepared, it can be saved to any location where the user has read / write permissons.

LibreCAD supports the use of multiple templates. A LibreCAD user that plans on creating similar drawings may require only one or two templates.  A user that plans on several different types of drawings may desire multiple templates.  For example, templates can be setup for each paper size available and / or for each paper orientation.

To use the newly created template, select "File" from the top menu bar and then select "New From Template" option. This will start a new drawing using the template drawing. Note that the new document is called "unnamed document" as any newly created drawing; it does not take the template name, only the template drawing contents.


Default Templates
~~~~~~~~~~~~~~~~~

When LibreCAD is first launched it creates a new drawing using a *default template*.  Further, when a new drawing is created within LibreCAD, either from the **File -> New** menu or when the "New" icon on the toolbar is clicked, the default template is used.  The default template can be either the template included with LibreCAD or a user-specified template.

When installing LibreCAD, a resource directory is created including, among other things, a default template named *empty.dxf*.  On MS Windows, the template is found in *C:\\Program Files (x86)\\LibreCAD\\resources\\library\\templates\\*.

As an alternative to the LibreCAD provided template, a user-specified template can be configured in the :ref:`Application Preferences <app-prefs>` on the **Paths** tab.  The specified template is used instead of the default LibreCAD template when the application is launched and for new drawings.


..  Image mapping (no "align" allowed/required):
