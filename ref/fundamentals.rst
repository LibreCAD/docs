.. User Manual, LibreCAD v2.2.x


.. _fundamentals: 

Fundamentals
============

To be able to use LibreCAD effectively, there are a few concepts that need to be understood.  While basic drawings can be created with very little setup, as they become more complex further consideration to the elements of a complete drawing is important.  This section offers an introduction to some concepts that are important to creating a complex drawing, but by no means is it exhaustive.  The  rest of the Reference section provides a description of the tools used to create and modify drawings.  General examples and guidence is offered in the :ref:`User Guide <guides>` section.


Entities
--------

An entity is a geometric shape; a line, circle, arc, etc.  A collection of entities is what forms a drawing.  In addition to the basic information that describes the geometry of an entity, there are two more elements that further define an entity:

    - :ref:`Pens <pens>` describes the appearance of an entity, either on screen or in printed output with three additional properties:

        - Color
        - Width
        - Line Type

    - :ref:`Layers <layers>` provide a means to organize drawing and manage the properties of multiple entities.
    - *Pen* or *Layers* properties *can* have a specific meaning, but vary by industry or an organization's standards and a complete description is beyond the scope of this manual.


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

When using cartesian coordinates for example, to set a 75 units above and 65 units to the right of the previous point, use "@75,65".  In this example, if the previous point was set at 20 units and 45 vertically (20,45) from the origin (0,0), setting the next point @75,65 relative to 20,45, using @75,65 would result in a point at 100 units horizontally and 100 vertically (100,100 absolute).

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


.. _placing-entities: 

Placing Entities
~~~~~~~~~~~~~~~~

There are two methods for defining coordinates when drawing entities in LibreCAD.  Users can use either the keyboard and type coordinates, or by using a mouse or other pointing devices.

.. _keyboard:

Keyboard
````````

Coordinate values, whether cartesian or polar, can be typed at the :ref:`command line <commandline>` in the formats as previously noted.  LibreCAD offers an additional method for typing cartesian coordinates when using the numeric keypad; type two decimal points (".") in lieu of the comma between the X and Y values.  For example, "10..20" is equivelent to typing "10,20".  This method can also be used for relative cartesian coordinates, e.g. @15..25.

Text input is also required by tool options where distance, angle, etc. are needed.

Mouse
`````

Entities' coordinates can also be located graphically using a mouse or other pointing device.  Using a mouse is less precise, but may be acceptable for 'rough' sketches or other freehand work.  However, the accuracy of using a mouse can be enhanced through the use of :ref:`snaps`.  



.. _isometric:

Isometric Drawings
~~~~~~~~~~~~~~~~~~

LibreCAD can also be used to create drawings with an **isometric** projection.  Creating isometric drawings is similar to creating orthaganol drawings, but with an additional consideration towards the perspective of the drawing.  The **Grid** tab of :ref:`Drawing Preferences <draw-prefs>` allows users to set the grid to suit isomentric drawings.  Setting the "Snap Indicator Lines" on the **Appearance** tab on the :ref:`Application Preferences <app-prefs>` to *Isometric* will also assist in with locating entities.

