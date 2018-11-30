.. _coordinates: 

The Coordinate system
=====================

In order to get the best out of LibreCAD it is wise to have a good understanding of the coordinate system and how 
coordinates work. Everything that you draw in LibreCAD will be exact and precise and will be placed there accurately 
based on the X,Y coordinate system.

The **absolute origin** or **Zero** point in your drawing is where the X and Y axes cross each other (represented by a 
Red cross), every entity you draw is located in relation to this origin.

In LibreCAD there is also the option to set the **Relative Zero Point** (small red circle).  This Relative zero point 
can be temporarily set to a new location in a drawing so that all subsequent X and Y coordinates of entities drawn or 
blocks placed for example will be relative to this newly set Relative Zero Point.

In libreCAD`s 2D coordinate system all **X** units are measured horizontally and all **Y** units are measured 
vertically.  Coordinates can also be shown as 'Positive' (+) or 'Negative'(-) values.

Examples of X and Y coordinates:
Selection 011.png

Types of Coordinates
--------------------
Basically there are two types of Coordinates: **Cartesian** and **Polar**.


Cartesian
~~~~~~~~~

The *Cartesian* coordinate system is generally the standard system used in most CAD programs. A specific point in a 
drawing is located by exact distances from both the X and Y axes - for example a point in a drawing could be 60,45 
(note the comma -, separates the two numbers).See example Image below.

Coordinates 60,45.png


Polar
~~~~~

The *Polar* coordinate system uses one distance and one angle to define a point in a drawing -for example a point in a 
drawing could be 50 < 45, so 50 units long and at an angle of 45 degrees (note the < sign is used for the angle). see 
example image below.

Selection 024.png


Defining Coordinate Locations
-----------------------------

Absolute
~~~~~~~~

Absolute coordinates - using this method,coordinate points are entered in direct relation to the Origin 0,0. To do this 
in LibreCAD just enter in the exact point e.g. 60,45.


Relative
~~~~~~~~

Relative coordinates - using this method, coordinate points are entered in relation to the previous point entered (not 
the origin), so for example - if your first point is 20,45, to then enter your next point 'relative' to this - you 
would use the '@' symbol - e.g @50,50 would then enter the second point 50 units horizontally along the x axis and 50 
units vertically along the Y axis to give this second point relative to your last point (20,45).See image below.

Selection 026.png


Relative Polar coordinates - this is a very useful way of drawing entities of which you know the exact length and angle.

For example you could draw a 100mm long line from start point 50,50 (absolute coordinate) and specify your second point 
at 100<45 (relative 'polar' coordinate).

You can see from this example that the second point is based on our 'distance' of 100mm and at an angle of 45 degrees. 
See example image below.

Selection 028.png


Angles in LibreCAD
``````````````````

It is worth mentioning here a brief explanation of how angles work in LibreCAD.

All angles in LibreCAD are measured in 360 degrees in an anti-clockwise direction (see image below) beginning from 0 
degrees (the 3 o'clock position). The < symbol is used before the angle - e.g.50<45.

Selection 030.png


.. _locating-entities: 

Locating Entities
-----------------

Keyboard
~~~~~~~~
In LibreCAD lines, points, arcs, polylines, circles and many more entities can be drawn and placed in a drawing using 
either *Absolute* or *Relative* coordinate input.

To input coordinate value points in LibreCAD you can type the values in the command line or inside a 'text input 
box' (presented by tool options requiring distance,angle etc...).  This method is 100% accurate.


Mouse
~~~~~

You can 'manually', move the mouse cursor around and visually pick a coordinate point, but obviously this method is 
less accurate but may be acceptable for some 'rough' sketch or freehand work!  The accuracy of using the mouse it enhanced through the use of :ref:`snaps`.


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
    "Restrict Horizontal", |icon10|, "rh", "Restricts cursor to ..."
    "Restrict Vertical", |icon11|, "rv", ""
    "Restrict Orthogonal", |icon12|, "rr", ""
    "Restrict Nothing", , "rn", "Turns off restricted cursor movements."
    "Set relative zero position", |icon13|, "", ""
    "Lock relative zero position", |icon14|, "", ""



..  Icon mapping:

.. |icon00| image:: /images/icons/
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
.. |icon15| image:: /images/icons/

