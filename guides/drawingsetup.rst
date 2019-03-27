.. User Manual, LibreCAD v2.2.x


.. _drawing-setup:

Setting up a Drawing
====================

As with other software; word processors, spreadsheets, etc, there are many ways a user can to setup or configure a new document.  With LibreCAD, that document is a drawing.  Some of the preferences for a drawing will be governed by drafting conventions, some will be determined by organizational requirements, and others might just be personal preferences.  The drawing's setup is largely determined by the :ref:`Drawing Preferences <draw-prefs>`.

Under normal circumstances, after the initial installation and :ref:`configuration <configure>`, little if any configuration needs to done to be able to *create* a new drawing.  During the initial setup, the default :ref:`unit of measure <measurements>` was set (defaulting to *millimeter*) and doesn't need to be changed.  The unit of measure should be set to the unit most frequently used as it is used for **all** new drawings.  If necessary, the default unit of measure can be changed in the :ref:`Application Preferences <app-prefs>` or overridden for a single drawing in the :ref:`Drawing Preferences <draw-prefs>`.

As noted, there are a many drawing parameters to be considered to suit the drawing requirements and final appearance.  The majority of these settings can be left as the defaults as LibreCAD's defaults reflect normal drafting conventions, such as the "Text Height" of 2.5mm / .10" / 3/32", etc.  Other preferences and attributes, such as layer, line thickness and type, pen colors, etc. can also be changed to suit users' requirements.


Determining Scale
-----------------

Setting the scale of a drawing is the easy part, drawings should be created **full-scale** (1:1)!  The zooming abilities of LibreCAD will make the whole drawing fit in the display window or zoom into the fine detail.  On the other hand, when producing output the drawing will need to be scaled to fit the "page".  Generally output is a printed page, but it can also be a pdf, or :ref:`exported to another image format <file>`.

While these two points seem contradict each other as a full-scale drawing of something very large, like a building, would require equally large text size for notes and dimensions when the drawing is scaled down to print on an "A1" page.  Trying to determine the text size for a large object would be tedious at best, but the features within LibreCAD simplifies it.  It is addressed by the "General Scale" on the *Dimensions* tab.

Two of the tabs, *Paper* and *Dimensions* require attention prior to generating output.  Specifically, the two parameters are:

    1. "Paper format" on the *Paper* tab: Selecting a paper size and orientation will determine the "print scale" used for final output.  The print scale also used to determine the "General Scale".
    2. "General Scale" on the *Dimensions* tab: The dimension text and related parameters can be adjusted to suit the output.

The "Paper format", e.g. paper size and orientation, to be used is an important to consideration when setting the drawing preferences.  While it can be done at anytime, determining the Paper Format sooner than later will help determine the "General Scale".  The Paper Format is entirely up to the user to determine, based on what is available (depending on the printer or printing service that is being used).

Determining the General Scale parameter for the best results is simple, it is the *inverse* of the printing scale obtained prior to printing.  For example, if a print scale is determined to be "1:4", the General Scale is "4" (4:1).  See the :ref:`Printing Guide <printing-guide>` for details.  Setting the General Scale to the inverse of the print scale results in the dimension text being the defined size, e.g. 2.5mm, on the printed drawing.  The drawing is scaled down to fit the page and the dimension text is scaled up to be legible.  More details can be found in the :ref:`Printing Guides <printing>`.

While any scale factor can be used, there are common scales are used for different types of drawings:

Architect's Scale
~~~~~~~~~~~~~~~~~

Metric units
````````````

.. csv-table:: 
   :header: "Drawing Scale", "Common Use"
   :widths: 30, 50

	"1:1", "Mockups / Samples / Small details"
	"1:2", "Construction details"
	"1:5", "Construction details"
	"1:10", "Construction details / Wall sections"
	"1:20", "Building sections"
	"1:50", "Building sections / Floor plans / Elevations"
	"1:100", "Floor plans / Elevations"
	"1:200", "Floor plans / Elevations / Site plans"
	"1:500", "Site plans"
	"1:1000", "Area plans"


Imperial units
``````````````

.. csv-table:: 
   :header: "Drawing Scale", "Ratio", "Common Use"
   :widths: 30, 20, 50

    "Full scale", "1:1", "Mockups / Samples / Small details"
    "3″=1′-0″", "1:4", "Small details"
	​"1 1⁄2″=1′-0″", "1:8", "Small details"
    "1″=1′-0″", "1:12", "Small details / Construction details"
    ​"3⁄4″=1′-0″", "1:16", "Construction details / Wall sections"
	​"1⁄2″=1′-0″", "1:24", "Building sections"
	​"3⁄8″=1′-0″", "1:32", "Wall sections / Building sections"
    "1⁄4″=1′-0″", "1:48", "Building sections / Floor plans / Elevations"
    ​"3⁄16″=1′-0″", "1:64", "Floor plans / Elevations"
	​"1⁄8″=1′-0″", "1:96", "Floor plans / Elevations / Site plans"
	​"3⁄32″=1′0″", "1:128", ""
    ​"1⁄16″=1′-0″", "1:192", "Site plan"


Engineer's scale
~~~~~~~~~~~~~~~~

.. csv-table:: 
   :header: "Drawing Scale", "Ratio", "Common Use"
   :widths: 30, 50

	"1″=10′-0″", "120", "Details"
	"1″=20′-0″", "240", "Details / Working plans"
	"1″=30′-0″", "360", "Working plans"
	"1″=40′-0″", "480", "Working plans"
	"1″=50′-0″", "600", "Working plans"
	"1″=60′-0″", "720", "Working plans"
	"1″=100′-0″", "1200", "Area plans"

Also see :ref:`Dimensioning <dimensioning>` for additional information on scales and scaling drawings.


.. _layers:

Layers
------

A basic concept in computer aided drafting is the use of layers to organize a drawing. Every entity in a drawing is on exactly one layer and a layer can contain lots of entities. Typically entities with a common 'function' or common attributes are put on the same layer. For example, it might be might necessary to put all axis in a drawing on a layer named 'axis'.  Each layer can be defined with a "Default Pen" (color, line width, line style). Each entity can have its own attributes or have its attributes defined by the layer it is placed on. In the latter case for example you can change the colour of all the entities on the "axes" layer by setting the colour (red for example) for that layer.

In traditional manual drafting, a similar approach was used. Whether for Engineering, Architectural or Construction drawing etc. layers were used to show different aspects of a drawing — for example this could be a layer set up for showing centre lines on an engineering drawing or to show different building systems, such as wiring and air conditioning. The layers were often drawn on separate transparent sheets of paper. These sheets were then overlaid one on top of another to produce final drawings.


Creating a Layer
~~~~~~~~~~~~~~~~

Layers are usually created to hold objects with common attributes. Creating a layer is simple:.

    From the menu select Layer -> Add Layer
    Specify a Layer Name
    Optionally specify the Color, Width and Line Type
	Click Ok


Changing an Entity's Layer
~~~~~~~~~~~~~~~~~~~~~~~~~~

Sometimes it is necessary to change an enitiy's layer. This describes how to move one or more objects between layers.

    From the menu select Modify->Attributes
    Select the objects you want to change the layer of. See Selections for a detailed description of how to select objects
    Select the continue action button (double right arrow)
    In the Attributes dialog, drop down the Layer selection box and choose the desired layer.

Alternatively you can activate the option Application Preferences → Defaults → Modify layer of selected entities, at layer activation
With this option enabled you can move objects to a layer by selecting the objects and then selecting the destination layer.


Construction Layers
~~~~~~~~~~~~~~~~~~~

A construction layer is designed to hold geometry construction lines:

    A construction layer won't appear on printout;
    All lines of a construction layer are infinite in length.

You can toggle between construction and normal mode three ways:

    the right most layer icon Layer icons.png
    right-click on a layer and choose "Toggle Construction Layer".
    the checkbox in the layer settings window


Ordering Layers
~~~~~~~~~~~~~~~

Layers are displayed in alphabetical order in the layer list, and this is does not relate to the order that entities appear in the z-axis of the drawing. Each entity can be raised or lowered with respect to others, and each layer can contain entities that are at different points on the z-axis.

Use the four Draw Order commands (under the Edit → Draw Order menu) to move entities up or down the z-axis. 


.. _entity-attribute:

Line Attributes
---------------

As with many other aspect of drafting, line color, thickness and type assigned to an entity, such as a line or circle are determined by drafting convention or common practices.  Within LibreCAD, the three attributes are grouped together as a "Pen":

    - Color - LibreCAD has 16 default colors, but supports the RGB color space (#000000 to #FFFFFF or 16,777,215 colors).  The initial color for entities is black.
    - Width - The default line width is 0.00mm.  Line widths of up to 2.11mm are supported.
    - Line Type - The default line type is "Continuous" (e.g. solid).  Other line types included with LibreCAD are Dot, Dash, Divide, Center, and Border.

The pen attributes can be defined for a single entity (via the *Properties* tool) , by a group of selected entities (via the *Attribute* tool), or by layer.


Line Type & Thickness
~~~~~~~~~~~~~~~~~~~~~

Line thickness should also be addressed when creating a new drawing.  The default line thickness is 0.00mm and results in a hairline on a printed page.  General practices may vary by drawing type; technical, arcitectural, etc, and by drawing size; larger drawings utilize thicker lines.  A variety of sources can be found on the internet by searching for "CAD standards".  The following table provides suggested line widths for ISO A4/A3/A2 or ANSI A/B/C paper sizes:

.. csv-table:: 
   :header: "Line Weights", "Width Range", "Purpose", "Width"
   :widths: 20, 30, 60, 30

    "Extra Thin", "0.00 to 0.10 mm", "- Hidden lines", "0.00 mm"
    "", "", "- Hatching", ""
    "", "", "- Reference line", ""
    "Thin", "0.15 to 0.25 mm", "- Outlines", "0.18 mm"
    "", "", "- Centre lines", ""
    "", "", "- Dimension lines", ""
    "", "", "- Leader and extension", ""
    "", "", "- Phantom lines", ""
    "", "", "- Grid lines", ""
    "", "", "- Text", ""
    "Medium", "0.30 mm to 0.50 mm", "- Hidden lines", "0.35 mm"
    "", "", "- Text normal (0.3 mm)", ""
    "", "", "- Text - sub-headings (0.5 mm)", ""
    "", "", "- Visible object outlines", ""
    "Thick", "0.70 mm", "- Cutting lines", "0.70 mm"
    "", "", "- Match lines", ""
    "", "", "- Section lines", ""
    "", "", "- Text - titles/major headings", ""
    "", "", "- Viewing planes", ""
    "Extra Thick", "1.00 mm", "- Title sheet border", "1.00 mm"


.. _templates:

Templates
---------

Templates are *prototype* drawings that provide the means to save basic parameters and settings so a drawing does not have to be configured each time a new one is started.  The parameters and settings include the settings defined in the :ref:`Drawing Preferences <draw-prefs>`, such as the paper format, main unit of measure and format, and dimension format.  Templates can also include layers and layer configuration, line type and thickness, pen color, and other drawing elements such as a border. These settings are inherited by the drawings created from the template.

Templates are created by starting a new drawing, setting the desired :ref:`Drawing Preferences <draw-prefs>`, and adding any required drawing elements (e.g. layers, borders, etc).  Starting with a blank drawing in LibreCAD, select "Edit" from the menu bar and then "Current Drawing Preferences".  On the first tab labeled "Paper", set the paper size and orientation as desired.  Next, select the "Units" tab and set the options as desired.  Click the "Dimensions" tab and adjust the values as desired.  Check the remaining tabs and adjust those settings as necessary.  Click "OK" when done.  Add the layers and other drawing elements as required.  Refer to :ref:`Layers <layers>` for details on using layers and setting the attributes.

Once the template has been prepared, it can be saved to any location where the user has read / write permissons.

LibreCAD supports the use of multiple templates. A LibreCAD user that plans on creating similar drawings may require only one or two templates.  A user that plans on several different types of drawings may desire multiple templates.  For example, templates can be setup for each paper size available and / or for each paper orientation.

To use the newly created template, select "File" from the top menu bar and then select "New From Template" option. This will start a new drawing using the template drawing. Note that the new document is called "unnamed document" as any newly created drawing; it does not take the template name, only the template drawing contents.


Default Templates
~~~~~~~~~~~~~~~~~

When LibreCAD is first launched it creates a new drawing using a *default template*.  Further, when a new drawing is created within LibreCAD, either from the **File -> New** menu or when the "New" icon on the toolbar is clicked, the default template is used.  The default template can be either the template included with LibreCAD or a user-specified template.

When installing LibreCAD, a resource directory is created including, among other things, a default template named *empty.dxf*.  On MS Windows, the template is found in *C:\Program Files (x86)\LibreCAD\resources\library\templates\*.  

As an alternative to the LibreCAD provided template, a user-specified template can be configured in the :ref:`Application Preferences <app-prefs>` on the **Paths** tab.  The specified template is used instead of the default LibreCAD template when the application is launched and for new drawings.

