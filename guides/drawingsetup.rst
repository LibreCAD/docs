.. User Manual, LibreCAD v2.2.x


.. _drawing-setup:

Setting up a Drawing
====================

As with other software; word processors, spreadsheets, etc, there are many ways a user can to setup or configure a new document.  With LibreCAD, that document is a drawing.  Some of the preferences for a drawing will be governed by drafting conventions, some will be determined by organizational requirements, and others might just be personal preferences.  The drawing's setup is largely determined by the :ref:`Drawing Preferences <draw-prefs>`.

Under normal circumstances, after the initial installation and :ref:`configuration <configure>`, little if any configuration needs to done to be able to *create* a new drawing.  During the initial setup, the default :ref:`unit of measure <measurements>` was set (defaulting to *millimeter*) and doesn't need to be changed.  The unit of measure should be set to the unit most frequently used as it is used for all new drawings.  If necessary, the default unit of measure can be changed in the :ref:`Application Preferences <app-prefs>` or overridden for a single drawing in the Drawing Preferences.

As noted, there are a many drawing parameters to be considered to suit the drawing requirements and final appearance.  The majority of these settings can be left as the defaults as LibreCAD's defaults reflect normal drafting conventions and practices, such as the "Text Height" of 2.5mm / .10" / 3/32", etc.  Other preferences and attributes, such as layer, line thickness and type, pen colors, etc. can also be changed to suit users' requirements.


Scale
-----

Setting the scale of a drawing is the easy part, drawings should be created **full-scale** (1:1)!  The zooming abilities of LibreCAD will make the whole drawing fit in the display window or zoom into the fine detail.  On the other hand, when producing output the drawing will need to be scaled to fit the "page".  Generally output is a printed page, but it can also be a pdf, or :ref:`exported to another image format <file>`.

While these two points seem contradict each other as a full-scale drawing of something very large, like a building, would require equally large text size for notes and dimensions when the drawing is scaled down to print on an "A1" page.  Trying to determine the text size for a large object would be tedious at best, but the features available in  LibreCAD makes it simple.  It is addressed by the "General Scale" on the *Dimensions* tab.

Two of the tabs, *Paper* and *Dimensions* require attention prior to generating output.  Specifically, the two parameters are:

    1. "Paper format" on the *Paper* tab: Selecting a paper size and orientation will determine the "print scale" used for final output.  The print scale also used to determine the "General Scale".
    2. "General Scale" on the *Dimensions* tab: The dimension text and related parameters can be adjusted to suit the output.

The "Paper format", e.g. paper size and orientation, to be used is an important to consideration when setting the drawing preferences.  The Paper Format is entirely up to the user to determine, based on what is available (depending on the printer or printing service that is being used).  While it can be done at anytime, determining the Paper Format sooner than later will help determine the "General Scale".  

.. Tip::
   Setting the General Scale prior to dimensioning a drawing is a suggested as it will determine the appropriate line spacing for dimensions.  See :ref:`Dimensioning <dimensioning>` for additional information.

Determining the General Scale parameter for the best results is simple, it is the *inverse* of the printing scale obtained prior to printing.  For example, if a print scale is determined to be "1:4", the General Scale is "4" (4:1).  Setting the General Scale to the inverse of the print scale results in the dimension text being the defined size, e.g. 2.5mm, on the printed drawing.  The drawing is scaled down to fit the page and the dimension text is scaled up to be legible.  See the :ref:`Printing Guide <printing-guide>` for details.


While any scale factor can be used, there are common scales used when **printing** different types of drawings.  Refer to  :ref:`Scales <scales>` in the appendix for some examples.


.. _entity-attributes:

Attributes
----------

Attributes are the charteristics of an entity and include:

   - Layers provide a means to organize a drawing and manage the properties of multiple entities.
   - "Pen" describes the appearance of an entity, either on screen or in printed output with three additional properties:

      - Color
      - Width
      - Line type


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
	- Optionally specify the Color, Width and Line Type for the layer.
	- Click **Ok**. 


Construction Layers
```````````````````

A construction layer is designed to hold geometry construction lines:

	- A construction layer won't appear on printout.
	- All lines of a construction layer are infinite in length.

You can toggle between construction and normal mode three ways:

	- When creating or modifying a layer, click the *Construction Layer* checkbox in the *Layer Settings* dialog.
	- Right-click on a named layer in the *Layer List* and choose "Toggle Construction Layer".
	- Click the "Toggle construction lines" icon |icon04| / |icon05| in the *Layer List*.

For more details on hiding, locking and deleting layers, refer to **Layer List Dock** in :ref:`Dock Widgets <widgets>`


.. _pens:

Pen
~~~

As with many other aspects of drafting line color, thickness and type assigned to an entity, such as a line or circle are determined by drafting conventions or common practices.  Within LibreCAD, the three attributes are grouped together as a "Pen":

    - **Color** - LibreCAD has 16 default colors, but supports the RGB color space (#000000 to #FFFFFF or 16,777,215 colors).  The initial color for entities is black.
    - **Width** - The default line width is 0.00mm.  Line widths of up to 2.11mm are supported.
    - **Line Type** - The default line type is "Continuous" (e.g. solid).  Other line types included with LibreCAD are Dot, Dash, Divide, Center, and Border.

The pen attributes can be defined for a single entity (via the *Properties* tool) , by a group of selected entities (via the *Attribute* tool), or by layer.


Color
`````

.. csv-table::
   :widths: 70 30
   :class: table-no-borders

   "The color for an entity can be selected from the ”Color” selection drop-down menu.  The drop-down menu allows the color to be selected ”By Layer”, ”By Block”, from the ”Custom” color selector, or chosen quickly from one of the 16 pre-defined colors: 

   Selecting ”By Layer” will assign the color that was defined for the layer (see above) to the entity.  If the layer's selected color is subsequently changed all entities on the layer will be assigned the layer's color.

   When editing a :ref:`block <blocks>`, selecting ”By Block” will assign the color that was defined for the block to the added entity.  If the block's color is subsequently changed all entities in the block will be assigned the block's color.", " |image01| "

Selecting ”Custom” will allow a selection from a palette of 36 colors and shades of grey or from a user defined colors.  User defined colors are created by clicking the Add button |image10| and then selecting the *hue* and *value* from the color selection tool.  User defined colors can be modified by right-clicking on a user defined color and selecting a new *hue* and *value*.  A maximum of eight user defined colors can be added.

.. csv-table::
   :widths: 50 50
   :class: table-no-borders

   |image02|, |image03|



Width
`````

Line width or thickness should also be addressed when creating a new drawing.  The default line thickness is 0.00mm and results in a hairline on a printed page.  General practices may vary by drawing type; technical, arcitectural, etc, and by drawing size; larger drawings utilize thicker lines.  A variety of sources can be found on the internet by searching for "CAD standards".  The following table provides suggested line widths for ISO A4/A3/A2 or ANSI A/B/C paper sizes:

.. csv-table:: 
    :widths: 15, 20, 40, 25
    :header-rows: 1
    :stub-columns: 0
    :class: table-wrap-text

    "Line Weights", "Pen Size (mm)", "Purpose", "Recommended"
    "Extra Thin", "0.00, 0.05, 0.09", "- Hidden lines", "0.00 mm"
    "", "", "- Hatching", ""
    "", "", "- Reference line", ""
    "Thin", "**0.13**, 0.15, **0.18**, 0.20, **0.25**", "- Outlines", "0.18 mm"
    "", "", "- Centre lines", ""
    "", "", "- Dimension lines", ""
    "", "", "- Leader and extension", ""
    "", "", "- Phantom lines", ""
    "", "", "- Grid lines", ""
    "", "", "- Text", ""
    "Medium", "0.30, **0.35**, 0.40, **0.50**", "- Hidden lines", "0.35 mm"
    "", "", "- Text normal (0.30 mm)", ""
    "", "", "- Text - sub-headings (0.50 mm)", ""
    "", "", "- Visible object outlines", ""
    "Thick", "**0.70**", "- Cutting lines", "0.70 mm"
    "", "", "- Match lines", ""
    "", "", "- Section lines", ""
    "", "", "- Text - titles/major headings", ""
    "", "", "- Viewing planes", ""
    "Extra Thick", "**1.00**", "- Title sheet border", ""


Note: Pen sizes shown in **bold** are ISO standard sizes.


Line Type
`````````

Different types of lines are used for different purposes.  LibreCAD includes several commonly used line types:

.. csv-table:: 
    :widths: 20, 20, 60
    :header-rows: 1
    :stub-columns: 0
    :class: table-wrap-text

    "Line Type", "Example", "Purpose"
    "Continuous", |image20|, "Object or visible, dimension, extention and construction lines."
    "Dot", |image21|, ""
    "Dash", |image22|, "Hidden lines and phantom lines (long dash)."
    "Dash Dot", |image23|, ""
    "Divide", |image24|, "Marks location (cross) section of object."
    "Center", |image25|, "Marks center of circle, arc or any symmetrical object."
    "Border", |image26|, "Used for drawing border around perimeter of sheet."

Other than ”Continuous”, the other non-continuous lines are available in default, ”tiny” (1/6x default), ”small” (1/2x) and ”large (2x)”.  A complete list of :ref:`line types <lineTypes>` are shwon in the appendix.

.. Note::
   Intervals in non-continuous line types with white spaces remain constant when scaled.  ”tiny” should be used in most cases.


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

When installing LibreCAD, a resource directory is created including, among other things, a default template named *empty.dxf*.  On MS Windows, the template is found in *C:\Program Files (x86)\LibreCAD\resources\library\templates\*.  

As an alternative to the LibreCAD provided template, a user-specified template can be configured in the :ref:`Application Preferences <app-prefs>` on the **Paths** tab.  The specified template is used instead of the default LibreCAD template when the application is launched and for new drawings.


..  Icon mapping:

.. |icon01| image:: /images/icons/add.svg
            :height: 18
            :width: 18
.. |icon02| image:: /images/icons/attributes.svg
            :height: 18
            :width: 18
.. |icon03| image:: /images/icons/rename_active_block.svg
            :height: 18
            :width: 18
.. |icon04| image:: /images/icons/construction_layer.svg
            :height: 18
            :width: 18
.. |icon05| image:: /images/icons/noconstruction.svg
            :height: 18
            :width: 18


..  Image mapping (no "align" allowed/required):

.. |image01| image:: /images/coloursStd.png
             :width: 140px
             :height: 439px
             :scale: 100
             :alt: Standard color selector
.. |image02| image:: /images/coloursCustom.png
             :width: 490px
             :height: 295px
             :scale: 67
             :alt: Custom colors
.. |image03| image:: /images/colourCustom.png
             :width: 436px
             :height: 426px
             :scale: 67
             :alt: Custom color selector
.. |image10| image:: /images/coloursCustomAdd.png
             :width: 48
             :height: 32
             :scale: 50
.. |image20| image:: /images/ltContinuous.png
             :width: 160
             :height: 20
             :scale: 100
             :alt: Continuous
.. |image21| image:: /images/ltDot.png
             :width: 160
             :height: 20
             :scale: 100
             :alt: Dot
.. |image22| image:: /images/ltDash.png
             :width: 160
             :height: 20
             :scale: 100
             :alt: Dash
.. |image23| image:: /images/ltDashDot.png
             :width: 160
             :height: 20
             :scale: 100
             :alt: Dash Dot
.. |image24| image:: /images/ltDivide.png
             :width: 160
             :height: 20
             :scale: 100
             :alt: Divide
.. |image25| image:: /images/ltCenter.png
             :width: 160
             :height: 20
             :scale: 100
             :alt: Center
.. |image26| image:: /images/ltBorder.png
             :width: 160
             :height: 20
             :scale: 100
             :alt: Border

