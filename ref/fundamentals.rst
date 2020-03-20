.. User Manual, LibreCAD v2.2.x

.. Default include
.. include:: /inclFiles/notice.rst


.. _fundamentals: 

Fundamentals
============

To be able to use LibreCAD effectively, there are a few concepts that need to be understood.  While a basic drawing or sketch can be created after the initial setup, as drawings become more complex further consideration to the elements of a complete drawing is important.  This section offers an introduction to some concepts that are required to create a drawing, but by no means is it exhaustive.  The  rest of the Reference section provides a description of the tools used to configure, create and modify drawings.  Further general examples and guidance is offered in the :ref:`User Guide <guides>` section.

LibreCAD supports two drawing perspectives; orthogonal and isometric projections.  Orthogonal projection is the default perspective for creating two dimensional (2D) drawings.  An :ref:`isometric <isometric>` projection allows LibreCAD to represent a three-dimensional object in two dimensions, sometimes referred to as "2.5D".  Both projections use coordinates to locate drawing elements.


.. _coordinates: 

The Coordinate System
---------------------

Understanding the coordinate systems and how coordinates work in LibreCAD is necessary to produce precise drawings.  Points are used to describe an aspect of an entity (e.g. the end of a line, the center of a circle, etc.), and can be placed accurately using coordinates.

There are two coordinate systems used in LibreCAD to place a point in a drawing.  A point can be placed by specifying:
 
    - a horizontal distance and vertical distance from a reference point (:ref:`Cartesian <cartesian-coords>`), or
    - an angle and distance from a reference point (:ref:`Polar <polar-coords>`).

All coordinates in a drawing are relative to the *origin* or *absolute zero*.  It is where the X and Y axes cross each other and is represented by crossed red lines.  The coordinates of this point are **0,0**.  Coordinates to the right and above the origin are positive.  Coordinates to the left or below are negative.  Every entity drawn can be located in relation to the origin.

LibreCAD also uses a *Relative Zero* point.  It is the last point set having created an entity.  It is represented within the drawing by a small red circle with a cross in it.  The Relative Zero point is set temporarily to a new position in a drawing so that a subsequent coordinates of the next entity can be placed using :ref:`relative coordinates <relative>`.

.. only:: html

    .. figure:: /images/coords.png
        :align: center
        :scale: 67
        :alt: Coordinate

.. only:: latex

    .. figure:: /images/coords.png
        :align: center
        :scale: 50
        :alt: Coordinate

.. actual image size 768px x 576px

.. Force end of left / right text wrap
.. include:: /inclFiles/eoWrap.rst


.. _angles: 

Angles
~~~~~~

.. only:: html

    .. figure:: /images/angles.png
        :align: right
        :scale: 75
        :alt: Polar Coordinates

.. only:: latex

    .. figure:: /images/angles.png
        :align: center
        :scale: 50
        :alt: Polar Coordinates

.. actual image size 362px x 339px

Angles are also used in LibreCAD.  While horizontal or vertical distances are measured in the specified :ref:`unit <measurements>`, angles in LibreCAD are always measured in degrees, beginning from 0 degrees horizontally to the right of the origin, or at the 3 o'clock position.  Angles entered as a positive value are measured in an anti-clockwise direction.  Angles entered as a negative value are measure in a clockwise direction.

.. Force end of left / right text wrap
.. include:: /inclFiles/eoWrap.rst


Types of Coordinates
~~~~~~~~~~~~~~~~~~~~

.. _cartesian-coords:

Cartesian
`````````

The *Cartesian* coordinate system is commonly used in most CAD programs.  Cartesian coordinates take the form *X,Y* where X is measured along the horizontal axis and Y on the vertical axis.  Coordinates can also be shown as "positive" (+) or "negative" (-) values.  A specific point in a drawing is located by exact distances from the X and Y axis - for example a point in a drawing could be "100,75", as shown here.

.. only:: html

    .. figure:: /images/byCartesian.png
        :align: center
        :scale: 67
        :alt: Cartesian Coordinates

.. only:: latex

    .. figure:: /images/byCartesian.png
        :align: center
        :scale: 50
        :alt: Cartesian Coordinates

.. actual image size 768px x 576px


.. _polar-coords:

Polar
`````

The *Polar* coordinate system uses a distance and an angle to locate a point in a drawing.  In LibreCAD the *<* symbol is used to designate an angle when using polar coordinates.  Polar coordinates take the form *100<45*, indicating a line 100 units long and with an angle of 45 degrees as shown.

.. only:: html

    .. figure:: /images/byPolar.png
        :align: center
        :scale: 67
        :alt: Polar Coordinates

.. only:: latex

    .. figure:: /images/byPolar.png
        :align: center
        :scale: 50
        :alt: Polar Coordinates

.. actual image size 768px x 576px

.. Force end of left / right text wrap
.. include:: /inclFiles/eoWrap.rst


Defining Coordinate Locations
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In LibreCAD lines, points, arcs, polylines, circles, and many more entities can be placed in a drawing using either *absolute* or *relative* coordinate input.  

.. _absolute:

Absolute
````````

When using absolute coordinates, whether Cartesian or polar, points are entered in direct relation to the origin (0,0). To do this in LibreCAD enter in the desired point, e.g. "100,75" or "100<45" as shown in the two images above.


.. _relative:

Relative
````````

The next point can also be placed *relative to the previously placed* point.  The last point placed when creating an entity becomes a temporary reference for the next point.  The newly set temporary reference is the "*Relative Zero* point" and the next coordinates can be entered relative to that point.  To define the next point relative to the Relative Zero point, either cartesian or polar, prefix the coordinates with the "@".  Points without the @ prefix are always interpreted as absolute coordinates.

For example, when using cartesian coordinates to set a point 75 units to the right and 65 units above of the previous point, use "@75,65".  In the example shown, the previous point was set at 25 units horizontally and 35 vertically (25,35) from the origin (0,0).  The next point can be set @75,65 from the Relative Zero point at 25,35, resulting in a point at 100,100 absolute (100 units horizontally and 100 vertically from the origin).

.. hint::

   Relative coordinates can also be entered using the "*x..y*" format.  This format is equivalent to prefixing the coordinates with the "@" symbol, but allows for :ref:`numeric keypad <keyboard>` input when using the :ref:`command line<widget-cmdLine>`.  As an example, entering coordinates as "75..65" is equivalent to "@75,65".

.. only:: html

    .. figure:: /images/byAbsCoorRelCoor.png
        :align: center
        :scale: 67
        :alt: Absolute & Relative Cartesian Coordinates

        Absolute & Relative Cartesian Coordinates

.. only:: latex

    .. figure:: /images/byAbsCoorRelCoor.png
        :align: center
        :scale: 50
        :alt: Absolute & Relative Cartesian Coordinates

        Absolute & Relative Cartesian Coordinates

.. actual image size 768px x 576px

As an example when using a polar coordinates, to place a point 100mm and 45 degrees from the last point drawn at 25,35 (absolute cartesian coordinate) use "@100<45" (relative polar coordinate).

.. only:: html

    .. figure:: /images/byAbsCoorRelPolar.png
        :align: center
        :scale: 67
        :alt: Absolute Cartesian & Relative Polar Coordinates

        Absolute Cartesian & Relative Polar Coordinates

.. only:: latex

    .. figure:: /images/byAbsCoorRelPolar.png
        :align: center
        :scale: 50
        :alt: Absolute Cartesian & Relative Polar Coordinates

        Absolute Cartesian & Relative Polar Coordinates

.. actual image size 768px x 576px

.. Force end of left / right text wrap
.. include:: /inclFiles/eoWrap.rst


.. _entities: 

.. _attributes: 

Entities
--------

An entity is a geometric shape; a line, circle, arc, etc.  A collection of entities is what forms a drawing.  In addition to the basic information that describes the geometry of an entity, there are two more *attributes* that further define an entity:

    - :ref:`Pens <entity-pen>` describes the appearance of an entity, either on screen or in printed output with three additional properties:

        - Color
        - Width
        - Line Type

    - :ref:`Layers <entity-layers>` provide a means to organize drawing and manage the properties of multiple entities.

.. note::
   *Pen* or *Layers* properties *can* have a specific meaning, but vary by industry or an organization's standards and a complete description is beyond the scope of this manual.

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

.. only:: html

	.. image:: /images/coloursStd.png
		:align: right
		:scale: 100
		:alt: Standard color selector

.. only:: latex

	.. image:: /images/coloursStd.png
		:align: right
		:scale: 67
		:alt: Standard color selector

.. actual image size 140px x 439px

The color for an entity can be selected from the ”Color” selection drop-down menu.  The drop-down menu allows the color to be selected ”By Layer”, ”By Block”, from the ”Custom” color selector, or chosen quickly from one of the 16 pre-defined colors: 

Selecting ”By Layer” will assign the color that was defined for the layer (see above) to the entity.  If the layer's selected color is subsequently changed all entities on the layer will be assigned the layer's color.

When editing a :ref:`block <blocks>`, selecting ”By Block” will assign the color that was defined for the block to the added entity.  If the block's color is subsequently changed all entities in the block will be assigned the block's color.

Selecting ”Custom” will allow a selection from a palette of 36 colors and shades of grey or from a user defined colors.  User defined colors are created by clicking the Add button |image10| and then selecting the *hue* and *value* from the color selection tool.  User defined colors can be modified by right-clicking on a user defined color and selecting a new *hue* and *value*.  A maximum of eight user defined colors can be added.

.. Force end of left / right text wrap
.. include:: /inclFiles/eoWrap.rst

.. table::
   :align: center
   :widths: auto
   :class: table-no-borders
   
   +----------+-----+----------+
   | |01Lcol| |     | |01Rcol| |
   +----------+-----+----------+

.. |01Lcol| image:: /images/coloursCustom.png
         :scale: 67
         :alt: Custom colors
.. actual image size 490px x 295px

.. |01Rcol| image:: /images/colourCustom.png
         :scale: 67
         :alt: Custom color selector
.. actual image size 436px x 426px


Width
`````
Line width or thickness have a particular purpose and should be considered when creating a new drawing.  The default line thickness is 0.00mm and results in a hairline on a printed page.  Line widths vary by drawing type; mechanical, architectural, etc, and by drawing size; larger drawings utilize thicker lines.  LibreCAD has the following line thicknesses:

.. list-table::
   :widths: 15, 15
   :header-rows: 0

    * - 0.00mm
      - 0.05mm
    * - 0.09mm
      - 0.13mm (ISO)
    * - 0.15mm
      - 0.18mm (ISO)
    * - 0.20mm
      - 0.25mm (ISO)
    * - 0.30mm
      - 0.35mm (ISO)
    * - 0.40mm
      - 0.50mm (ISO)
    * - 0.53mm
      - 0.60mm
    * - 0.70mm (ISO)
      - 0.80mm
    * - 0.90mm
      - 1.00mm (ISO)
    * - 1.06mm
      - 1.20mm
    * - 1.40mm (ISO)
      - 1.58mm
    * - 2.00mm (ISO)
      - 2.11mm

Refer to :ref:`Line widths <lineWidths>` in the appendix for common line widths for use with a particular a page size.


Line Type
`````````

LibreCAD includes several commonly used line types:

.. csv-table:: 
    :widths: 15, 30, 55
    :header-rows: 1
    :stub-columns: 0
    :class: table-fix-width

    "Line Type", "Example", "Purpose"
    "Continuous", |image20|, "Object or visible, dimension, extension and construction lines."
    "Dot", |image21|, ""
    "Dash", |image22|, "Hidden lines and phantom lines (long dash)."
    "Dash Dot", |image23|, ""
    "Divide", |image24|, "Marks location (cross) section of object."
    "Center", |image25|, "Marks center of circle, arc or any symmetrical object."
    "Border", |image26|, "Used for drawing border around perimeter of sheet."

Other than ”Continuous”, the other non-continuous lines are available in default, ”tiny” (1/6x default), ”small” (1/2x) and ”large (2x)”.  As with line thickness, different types of lines are used for different purposes.  A complete list of :ref:`line types <lineTypes>` are shown in the appendix.

.. Note::
   Intervals for non-continuous line types with white spaces remain constant when scaled.  ”Tiny” should be used in most cases.


.. _entity-layers:

Layers
~~~~~~

One of LibreCAD’s key features is the ability to use layers. Layers help organize drawings by allowing users to place and manage related entities. Traditional manual drafting used a similar approach. The layers were often drawn on separate transparent sheets of paper. These sheets were then overlaid one on top of another to produce final drawings.

Whether for engineering, architectural, construction, manufacturing or other types, layers were used to show different aspects on the drawing. Layers could be added to show centre lines or dimensions on an engineering or manufacturing drawings, or to show different building systems on architectural drawings such as exterior walls, partitions, electrical, HVAC, grid lines, etc. While one layer can contain multiple entities, every entity in a drawing can only be associated with single layer. Typically entities with common functions or attributes are put on the same layer. For example, all the walls in a floor plan drawing would be put on a layer named “Walls”.

Layers have an added advantage that all the pen attributes can be assigned to a layer. Every entity on that layer will adopt the attributes that have been assigned to that layer. However, the attributes assigned by the layer can be overridden for entities if necessary. In the above example a line thickness can applied to all entities on the “Walls” layer by changing the “Layer Settings” for that layer.

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


Drawing and Editing Entities
----------------------------

Creating Entities
~~~~~~~~~~~~~~~~~

There are two methods for defining coordinates when drawing entities in LibreCAD.  Users can use either use a mouse or other pointing devices, or the keyboard and enter coordinates.

Using a Mouse
`````````````

Entities' coordinates can also be located graphically using a mouse or other pointing device.  Using a mouse is less precise, but may be acceptable for rough sketches or other freehand work.  However, the accuracy of using a mouse can be enhanced through the use of :ref:`snaps <snaps>`.  

.. _keyboard:

Using the Keyboard
``````````````````

The keyboard can be used to select tools and enter coordinates using the *command line*.  Tools can be selected by typing a command and then entering the coordinate values.  The commands are shown in the :ref:`Drawing Tools <tools>`.  Coordinates can be entered at the command line after selecting a drawing tool using the formats as shown previously; "100,75" (:ref:`Cartesian <cartesian-coords>`) or "100<45" (:ref:`polar <polar-coords>`), :ref:`absolute <absolute>` or :ref:`relative <relative>` (prefixed with "@").

LibreCAD offers an additional method for entering *relative coordinates* when using the numeric keypad; type two decimal points ("**..**") in lieu of the comma between the X and Y values.  For example, "10..20" is equivalent to typing "@10,20".  Refer to the **User Guides** for more details on using the :ref:`command line <cmdline>`.

Text input may also be required for **Tool Options** where distance, angle, etc. are needed with some of the **Drawing Tools**.

Selecting Entities
~~~~~~~~~~~~~~~~~~

Selecting entities allow them to be modified or deleted.  Some operations can be applied to groups of selected entities and other can only be applied to one entity at a time.  There are a variety of ways that entities can be selected:

   - Single click on an entity.  Holding the [Shift] key while clicking will allow additional entities to be selected.
   - Click and drag a selection box:

      - Left to right while moving down or up to select entities enclosed within the selection window’s boundary (blue selection box).
      - Right to left  while moving down or up to select entities enclosed within the window’s boundary and crossed by the selection boundary (green selection box)

   -  type “sa” at the command line to select all entities.

Deselect selected entities by typing “tn” at the command line or pressing [Esc].  Note that it might be might be necessary to press [Esc] twice if a command it active.

Also see the :ref:`Select<tool-select>` tools for additional methods to select and deselect entities.

Entity Handles
~~~~~~~~~~~~~~

Selected entities display “handles”.  Handles allow the entities to be manipulated; lengthened, moved or enlarged depending on the type of entity:


.. only:: html

    .. figure:: /images/handleEg.png
        :align: right
        :scale: 75
        :alt: Entity Handles

.. only:: latex

    .. figure:: /images/handleEg.png
        :align: center
        :scale: 50
        :alt: Entity Handles

.. actual image size 768px x 341px

.. Force end of left / right text wrap
.. include:: /inclFiles/eoWrap.rst

- Entities that consist of a single segment, such as lines, arcs and polyline segments, have a start handle and an end handle.  Either handle can be clicked and dragged into a new position.
- Handles on circles or other entities that consist of multiple segments allow it to be manipulated in a variety of ways depending on the type of entity.  For example:

   - A rectangle’s corner can be dragged to a new position creating other quadrilaterals.
   - A circle can be increased or decreased in size.
   - The end points of the edges of a polygon can be repositioned.
   - Dimension text and lines can be repositioned

Ordering Entities
`````````````````
Entities are drawn on a 2D plane, but can overlay each other and have levels that are independent of layers.  Entity can be raised, *moved up*, or lowered, *moved down*, with respect to other entities.  Each layer can contain entities that are at different levels.  Use the commands in **Tools -> Modify -> Order** to move entities up or down.

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


.. _isometric:

Isometric Drawings
------------------

.. figure:: /images/isometric.png
    :align: right
    :scale: 67
    :alt: Isometric Axes

    Isometric X, Y ,Z Axes

.. actual image size 365px x 273px

LibreCAD can also be used to create drawings with an *isometric perspective*.  Creating isometric drawings is similar to creating orthogonal drawings, but with an additional consideration towards combining multiple views in a single perspective.  Instead of the two axes (X,Y) used with orthogonal drawings, isometric drawing are represented in a two dimensional drawing on three axes (X,Y,Z) with 120 |deg| between each axis.

See :ref:`Drawing an Isometric View <dwg-isometric>` in **Drawing and Editing** section of the **User Guide** for details on configuring LibreCAD for isometric drafting.

.. Force end of left / right text wrap
.. include:: /inclFiles/eoWrap.rst


.. Symbols

.. |deg| unicode:: U+00B0


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
