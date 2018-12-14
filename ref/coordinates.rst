.. _coordinates: 

The Coordinate System
=====================

In order to get the best out of the application it is necessary to understand the coordinate systems used in LibreCAD and how coordinates work.  Every entity (e.g. a line, circle, etc.) that is drawn in LibreCAD can be drawn with precision, placed accurately using coordinates.

In libreCAD`s 2D coordinate system *X* units are measured horizontally and *Y* units are measured vertically.  Coordinates can also be shown as "Positive" (+) or "Negative" (-) values.  All coordinates are relative to the *absolute origin* in the drawing.  It is where the X and Y axes cross each other and represented by a red cross.  The coordinates at this point are 0,0.  Every entity drawn can be located in relation to this origin.

LibreCAD also uses a *Relative Zero Point*.  It is the last point set when creating an entity.  It is represented by a small red circle within the drawing.  The Relative Zero Point is set temporarily to a new location in a drawing so that a subsequent X and Y coordinates of the next entity can be placed using :ref:`relative coordinates <relative>`.  

Examples of X and Y coordinates:

.. figure:: /images/coords.png
    :width: 880px
    :height: 660px
    :align: center
    :scale: 80
    :alt: Coordinate


Types of Coordinates
--------------------

There are two coordinate systems used in LibreCAD, *Cartesian* and *Polar*.

Cartesian
~~~~~~~~~

.. figure:: /images/byCartesian.png
    :width: 800px
    :height: 660px
    :align: right
    :scale: 40
    :alt: Cartesian Coordinates

The *Cartesian* coordinate system is commonly used in most CAD programs.  Cartesian coordinates take the form *X,Y* where X is the horizontal axis and Y is the vertical axis.  A specific point in a drawing is located by exact distances from the X and Y axis - for example a point in a drawing could be "100,75", as shown here.

.. note:

Coordinates can also be written as 10..20 which allows for :ref:`numeric keypad <keyboard>` input.


|
|
|
|

Polar
~~~~~

.. figure:: /images/byPolar.png
    :width: 800px
    :height: 660px
    :align: right
    :scale: 40
    :alt: Polar Coordinates

The *Polar* coordinate system uses one distance and one angle to locate a point in a drawing.  In LibreCAD the polar coordinates take the form *100 < 45*, indicating a line 100 units long and at an angle of 45 degrees as shown.

|
|
|
|
|


Defining Coordinate Locations
-----------------------------

Locating a point for an entity can be  done in two ways; *Absolute* or *Relative*.

.. _absolute:

Absolute
~~~~~~~~

When using Absolute coordinates, whether cartisian or polar, points are entered in direct relation to the origin (0,0). To do this in LibreCAD, enter in the desired point, e.g. "100,75" or "100<45" as shown in the two images above.

.. _relative:

Relative
~~~~~~~~

Relative coordinates are entered in relation to the last point set, not the origin.  To set a relative point the coordinates, either cartesian or polar, are prefixed with the '@' symbol.  

.. figure:: /images/byAbsCoorRelCoor.png
    :width: 800px
    :height: 660px
    :align: right
    :scale: 40
    :alt: Absolute & Relative Cartesian Coordinates

When using cartesian coordinates for example, to set a 75 units above and 65 units to the right of the previous point, use "@75,65".  In this example, if the previous point was set at 20 units and 45 vertically (20,45) from the origin (0,0), setting the next point @75,65 relative to 20,45, using @75,65 would result in a point at 100 units horizontally and 100 vertically (100,100 absolute).


.. figure:: /images/byAbsCoorRelPolar.png
    :width: 800px
    :height: 660px
    :align: right
    :scale: 40
    :alt: Absolute Cartesian & Relative Polar Coordinates

As an example when using a polar coordinates, to draw a line 100mm and 45 degrees from the last point drawn at 25,45 (absolute cartesian coordinate) use "@100<45" (relative polar coordinate).

|
|

Angles in LibreCAD
~~~~~~~~~~~~~~~~~~

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


.. _placing-entities: 

Placing Entities
-----------------

.. _keyboard:

Keyboard
~~~~~~~~
In LibreCAD lines, points, arcs, polylines, circles and many more entities can be drawn and placed in a drawing using either *Absolute* or *Relative* coordinate input.

To input coordinate value points in LibreCAD you can type the values in the command line or inside a 'text input box' (presented by tool options requiring distance,angle etc...).  This method is 100% accurate.


Mouse
~~~~~

You can 'manually', move the mouse cursor around and visually pick a coordinate point, but obviously this method is less accurate but may be acceptable for some 'rough' sketch or freehand work!  HYowever, the accuracy of using the mouse it enhanced through the use of :ref:`snaps`.


.. _snaps:

Snapping
~~~~~~~~

.. csv-table:: 
   :header: "Menu Item", "Icon", "Command", "Description"
   :widths: 40, 10, 20, 110

    "Exclusive Snap Mode", |icon01|, "", "**On**: only one snap mode is allowed.  **Off**: multiple snap modes are allowed The snap modes are remembered in each state."
    "Free Snap", |icon02|, "os, sf", "Allows for the crosshair to move freely while other snap modes are enabled."
    "Snap on Grid", |icon03|, "sg", "Snap to a grid intersection."
    "Snap on Endpoints", |icon04|, "se", "Snap to the endpoints of a line segment, the quadrants of a circle, a point, or the alignment point of a text or mtext object."
    "Snap on Entity", |icon05|, "np, sn", "Snap to the path of an entity."
    "Snap Center", |icon06|, "sc", "Snap to the center of a circle or ellipse. It will also snap to the foci of an ellipse."
    "Snap Middle", |icon07|, "sm", "Snap to the middle of a path. Enabling this mode displays a ''Middle points'' input. If you change the value to 2 then you can snap to the trisection points of a line segment."
    "Snap Distance", |icon08|, "sd", "If you snap to the endpoint of a line segment then activate ''snap distance'' and input 50, then it will snap to a point 50 units from the endpoint on the line segment. However, it will also snap to a point that is 50 units from the other endpoint."
    "Snap Intersection", |icon09|, "si", "Snap to the intersection of two entities. This does not currently work for polylines."
    "Restrict Horizontal", |icon10|, "rh", "Restricts the crosshairs to the x-axis (horizontal movement)."
    "Restrict Vertical", |icon11|, "rv", "Restricts the crosshairs to the y-axis  (vertical movement)."
    "Restrict Orthogonal", |icon12|, "rr", "Restricts the crosshairs to the x **or** y-axis. (either horizontal **or** vertical movement)."
    "Restrict Nothing", , "rn", "Turns off restricted cursor movements."
    "Set relative zero position", |icon13|, "", ""
    "Lock relative zero position", |icon14|, "", ""



..  Icon mapping:

.. icon00
.. |icon01| image:: /images/icons/exclusive.svg
.. |icon02| image:: /images/icons/snap_free.svg
.. |icon03| image:: /images/icons/snap_grid.svg
.. |icon04| image:: /images/icons/snap_endpoints.svg
.. |icon05| image:: /images/icons/snap_free.svg
.. |icon06| image:: /images/icons/snap_center.svg
.. |icon07| image:: /images/icons/snap_middle.svg
.. |icon08| image:: /images/icons/snap_distance.svg
.. |icon09| image:: /images/icons/snap_intersection.svg
.. |icon10| image:: /images/icons/restr_hor.svg
.. |icon11| image:: /images/icons/restr_ver.svg
.. |icon12| image:: /images/icons/restr_ortho.svg
.. |icon13| image:: /images/icons/set_rel_zero.svg
.. |icon14| image:: /images/icons/lock_rel_zero.svg
.. icon15

