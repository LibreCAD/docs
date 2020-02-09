.. User Manual, LibreCAD v2.2.x

.. Default include
.. include:: /notice.rst


.. _fundamentals: 

Fundamentals
============

To be able to use LibreCAD effectively, there are a few concepts that need to be understood.  While basic drawings can be created with very little setup, as they become more complex further consideration to the elements of a complete drawing is important.  This section offers an introduction to some concepts that are important to creating a complex drawing, but by no means is it exhaustive.  The  rest of the Reference section provides a description of the tools used to create and modify drawings.  General examples and guidence is offered in the :ref:`User Guide <guides>` section.


.. _coordinates: 

The Coordinate System
---------------------

Understanding the coordinates systems and how coordinates work in LibreCAD is necessary to produce precise and accurate drawings.  Every entity (e.g. a line, circle, etc.) that is drawn in LibreCAD can be drawn with precision, placed accurately using coordinates.  LibreCAD supports two drawing perspectives; orthaganol and isometric.  Orthaganol is the default perspective for creating two dimensional (2D) drawings.  An :ref:`isometric <isometric>` projection allows LibreCAD to represent a three-dimensional object in two dimensions, sometimes refered to as "2.5D".

In libreCAD`s 2D coordinate system *X* units are measured horizontally and *Y* units are measured vertically.  Coordinates can also be shown as "Positive" (+) or "Negative" (-) values.  All coordinates are relative to the *absolute origin* in the drawing.  It is where the X and Y axes cross each other and represented by a red cross.  The coordinates at this point are 0,0.  Every entity drawn can be located in relation to this origin.

LibreCAD also uses a *Relative Zero Point*.  It is the last point set when creating an entity.  It is represented by a small red circle within the drawing.  The Relative Zero Point is set temporarily to a new location in a drawing so that a subsequent X and Y coordinates of the next entity can be placed using :ref:`relative coordinates <relative>`.  

Examples of X and Y coordinates:

.. figure:: /images/coords.png
    :width: 880px
    :height: 660px
    :align: center
    :scale: 67
    :alt: Coordinate


Types of Coordinates
~~~~~~~~~~~~~~~~~~~~

There are two coordinate systems used in LibreCAD, *Cartesian* and *Polar*.

Cartesian
`````````

.. figure:: /images/byCartesian.png
    :width: 800px
    :height: 660px
    :align: right
    :scale: 45
    :alt: Cartesian Coordinates

The *Cartesian* coordinate system is commonly used in most CAD programs.  Cartesian coordinates take the form *X,Y* where X is the horizontal axis and Y is the vertical axis.  A specific point in a drawing is located by exact distances from the X and Y axis - for example a point in a drawing could be "100,75", as shown here.


Polar
`````

.. figure:: /images/byPolar.png
    :width: 800px
    :height: 660px
    :align: right
    :scale: 45
    :alt: Polar Coordinates

The *Polar* coordinate system uses one distance and one angle to locate a point in a drawing.  In LibreCAD the polar coordinates take the form *100 < 45*, indicating a line 100 units long and at an angle of 45 degrees as shown.

|
|
|
|
|
|
|


Defining Coordinate Locations
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In LibreCAD lines, points, arcs, polylines, circles, and many more entities can be placed in a drawing using either *Absolute* or *Relative* coordinate input.

.. _absolute:

Absolute
````````

When using Absolute coordinates, whether cartisian or polar, points are entered in direct relation to the origin (0,0). To do this in LibreCAD, enter in the desired point, e.g. "100,75" or "100<45" as shown in the two images above.

.. _relative:

Relative
````````

The last coordinate defined when creating an entity becomes a temporary reference for the next point.  The newly set temporary reference is the "Relative Zero Point", and coordinates can be entered relative to the Relative Zero Point.  To define the next point relative to the Relative Zero Point coordinates, either cartesian or polar, are prefixed with the '@' symbol when entered.  Points without the @ prefix are always interpreted as absolute coordinates.

.. figure:: /images/byAbsCoorRelCoor.png
    :width: 800px
    :height: 660px
    :align: right
    :scale: 45
    :alt: Absolute & Relative Cartesian Coordinates

When using cartesian coordinates for example, to set a 65 units above and 75 units to the right of the previous point, use "@75,65".  In this example, if the previous point was set at 20 units and 45 vertically (20,45) from the origin (0,0), setting the next point @75,65 relative to 20,45, using @75,65 would result in a point at 100 units horizontally and 100 vertically (100,100 absolute).

|

.. note::

   Relative coordinates can also be written as 10..20 (equivalent to @10,20) which allows for :ref:`numeric keypad <keyboard>` input when using the :ref:`command line<widget-cmdLine>`.


.. figure:: /images/byAbsCoorRelPolar.png
    :width: 800px
    :height: 660px
    :align: right
    :scale: 45
    :alt: Absolute Cartesian & Relative Polar Coordinates


As an example when using a polar coordinates, to draw a line 100mm and 45 degrees from the last point drawn at 25,45 (absolute cartesian coordinate) use "@100<45" (relative polar coordinate).

|
|
|
|
|
|
|


.. _angles: 

Angles in LibreCAD
``````````````````

.. figure:: /images/angles.png
    :width: 800px
    :height: 660px
    :align: right
    :scale: 50
    :alt: Polar Coordinates

All angles in LibreCAD are measured in 360 degrees in an anti-clockwise direction beginning from 0 degrees (the 3 o'clock position). The *<* symbol is used toi designat e an angle whn using polar coordinates, e.g.50<45.

|
|
|
|
|
|
|
|



.. _entities: 

.. _attributes: 

Entities
--------

An entity is a geometric shape; a line, circle, arc, etc.  A collection of entities is what forms a drawing.  In addition to the basic information that describes the geometry of an entity, there are two more *attributes* that further define an entity:

    - :ref:`Layers <entity-layers>` provide a means to organize drawing and manage the properties of multiple entities.
    - :ref:`Pens <entity-pen>` describes the appearance of an entity, either on screen or in printed output with three additional properties:

        - Color
        - Width
        - Line Type

.. note::
   *Pen* or *Layers* properties *can* have a specific meaning, but vary by industry or an organization's standards and a complete description is beyond the scope of this manual.


.. _entity-layers:

Layers
~~~~~~

A basic feature of CAD is the use of layers to organize a drawing. Every entity in a drawing is on exactly one layer, however one layer can contain multiple entities. Typically entities with a common 'function' or common attributes are put on the same layer. For example, it might be might necessary to put all axis in a drawing on a layer named 'axis'.  Each layer can be defined with a "Default Pen" (see :ref: `Pens <entity-pen>` below). Each entity can have its own attributes or have its attributes defined by the layer it is placed on. In the latter case for example you can change the colour of all the entities on the "axes" layer by setting the colour (red for example) for that layer.

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

For more details on hiding, locking and deleting layers, refer to :ref:`Layer List Dock <widget-layerList>` in the Dock Widgets Reference section.


.. _entity-pen:

Pen
~~~

As with many other aspects of drafting line color, thickness and type assigned to an entity, such as a line or circle are determined by drafting conventions or common practices.  Within LibreCAD, the three attributes are grouped together as a "Pen":

    - **Color** - LibreCAD has 16 default colors, but supports the RGB color space (#000000 to #FFFFFF or 16,777,215 colors).  The initial color for entities is black.
    - **Width** - The default line width is 0.00mm.  Line widths of up to 2.11mm are supported.
    - **Line Type** - The default line type is "Continuous" (e.g. solid).  Other line types included with LibreCAD are Dot, Dash, Divide, Center, and Border.

The pen attributes can be defined for a single entity (via the *Properties* tool) , by a group of selected entities (via the *Attribute* tool), or by layer.

.. note::
   Just as with entities, "pens" can also be applied to layers.  See :ref:`Layer List Dock <widget-layerList>` for details on setting a layer's attributes.


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

Other than ”Continuous”, the other non-continuous lines are available in default, ”tiny” (1/6x default), ”small” (1/2x) and ”large (2x)”.  A complete list of :ref:`line types <lineTypes>` are shown in the appendix.

.. Note::
   Intervals for non-continuous line types with white spaces remain constant when scaled.  ”Tiny” should be used in most cases.


Creating Entities
~~~~~~~~~~~~~~~~~

There are two methods for defining coordinates when drawing entities in LibreCAD.  Users can use either the keyboard and type coordinates, or by using a mouse or other pointing devices.


Using a Mouse
`````````````

Entities' coordinates can also be located graphically using a mouse or other pointing device.  Using a mouse is less precise, but may be acceptable for 'rough' sketches or other freehand work.  However, the accuracy of using a mouse can be enhanced through the use of :ref:`snaps`.  

.. _keyboard: 

Using the Keyboard
```````````````````

Coordinate values, whether cartesian or polar, can be typed at the :ref:`command line <cmdline>` in the formats as previously noted.  LibreCAD offers an additional method for typing cartesian coordinates when using the numeric keypad; type two decimal points (".") in lieu of the comma between the X and Y values.  For example, "10..20" is equivelent to typing "10,20".  This method can also be used for relative cartesian coordinates, e.g. @15..25.

Text input is also required by tool options where distance, angle, etc. are needed.


Selecting Entities
~~~~~~~~~~~~~~~~~~

Selecting entities allow them to be modified or deleted.  Some operations can be applied to groups of selected entities and other can only be applied to one entity at a time.  There are a variety of ways that entities can be selected:

   - Single click on an entity.  Holding the [Shift] key while clicking will allow additional entities to be selected.
   - Click and drag a selection box:

      - Left to right while moving down or up to select entities enclosed within the selection window’s boundary (blue selection box).
      - Right to left  while moving down or up toselect entities enclosed within the window’s boundary and crossed by the selection boundary (green selection box)

   -  type “sa” at the command line to select all entities.

Deselect selected entities by typing “tn” at the command line or pressing [Esc].  Note that it might be might be necessary to press [Esc] twice if a command it active.

Also see the :ref:`Select<tool-select>` tools for additional methods to select and deselect entities.


Entity Handles
~~~~~~~~~~~~~~

Selected entities display “handles”.  Handles allow the entities to be manipulated; lengthened, moved or enlarged depending on the type of entity:

.. figure:: /images/handleEg.png
    :width: 1364px
    :height: 547px
    :align: right
    :scale: 50
    :alt: Entity Handles


- Entities that consist of a single segment, such as lines, arcs and polyline segments, have a start handle and an end handle.  Either handle can be clicked and dragged into a new position.
- Handles on circles or other entities that consist of multiple segments allow it to be manipulated in a variety of ways depending on the type of entity.  For example:

   - A rectangle’s corner can be dragged to a new position creating other quadrilaterals.
   - A circle can be increased or decreased in size.
   - The end points of the edges of a polygon can be be repositioned.
   - Dimension text and lines can be repositioned


.. _isometric:

Isometric Drawings
------------------

LibreCAD can also be used to create drawings with an **isometric** projection.  Creating isometric drawings is similar to creating orthaganol drawings, but with an additional consideration towards the perspective of the drawing.  The **Grid** tab of :ref:`Drawing Preferences <draw-prefs>` allows users to set the grid to suit isomentric drawings.  Setting the "Snap Indicator Lines" on the **Appearance** tab on the :ref:`Application Preferences <app-prefs>` to *Isometric* will also assist in with locating entities.


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
