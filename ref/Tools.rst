.. _tools: 

Drawing Tools
-------------

The drawing tools are used to create and modify entities such as lines, circles, etc in a drawing... yada, yada, yada

Line
~~~~
.. table:: Line Tools
    :widths: 15 10 75
+---------------------------------+------+-----------------------------------------------------------------------------+
| Tool                            | Icon | Description                                                                 |
+=================================+======+=============================================================================+
| 2 points                        | icon | Draw a line between two assigned points.                                    |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Angle                           | icon | Draw a line from an assigned point defining the start, middle or end of the | |                                 |      | line and with an assigned length and angle.                                 |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Horizontal                      | icon | Draw a horizontal line from an assigned point defining the start, middle or |
|                                 |      | end of the line and with an assigned length.                                |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Vertical                        | icon | Draw a vertical line from an assigned point defining the start, middle or   |
|                                 |      | end of the line and with an assigned length.                                |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Freehand Line                   | icon | Draw a non-geometric line.                                                  |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Parallel through point          | icon | Draw a given number of lines parallel to a selected existing line through   |
|                                 |      | an assigned point.                                                          |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Parallel                        | icon | Draw a given number of lines parallel to a selected existing line with a    |
|                                 |      | given distance between lines.                                               |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Rectangle                       | icon | Draw a rectagle by assigning the points of two diagonally opposite corners. |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Bisector                        | icon | Draw a given number of lines bisecting two existing non-parallel lines (e.g.| 
|                                 |      | at an angle to each other with or without a common point).                  |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Tangent (P,C)                   | icon | Draw a line from an assigned point tangent to an existing circle.           |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Tangent (C,C)                   | icon | Draw a line tangent to two existing circles.                                |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Tangent Orthogonal              | icon | Draw a line tangent to an existing circle and perpendicular to an existing  |
|                                 |      | line.                                                                       |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Orthogonal                      | icon | Draw a line of a given length perpendicular to an existing line placing the |
|                                 |      | centre at an assigned point.                                                |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Relative Angle                  | icon | Draw a line with a given length and at a given angle relative to an existing|
|                                 |      | line placing the centre of the line at an assigned point.                   |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Polygon (Cen,Cor)               | icon | Draw a polygon with a given number of sides assigning the centre point and  | 
|                                 |      | point of one vertex.                                                        |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Polygon (Cen,Tan)               | icon | Draw a polygon with a given number of sides assigning the centre point and  | 
|                                 |      | point of the centre of one side.                                            |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Polygon (Cor,Cor)               | icon | Draw a polygon with a given number of sides assigning the two points of one |
|                                 |      | side.                                                                       |
+---------------------------------+------+-----------------------------------------------------------------------------+

Circle
~~~~~~
.. table:: Circle Tools
    :widths: 15 10 75
+---------------------------------+------+-----------------------------------------------------------------------------+
| Tool                            | Icon | Description                                                                 |
+=================================+======+=============================================================================+
| Centre, Point                   | icon | Draw a circle with a given radius by assigning a centre point and a point on|
|                                 |      | the circumference.                                                          |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Centre, Radius                  | icon | Draw a circle with a given radius centred at an assigned point.             |
+---------------------------------+------+-----------------------------------------------------------------------------+
| 2 Points                        | icon | Draw a circle with a given diameter by assigning two opposite points on the |
|                                 |      |circumference.                                                               |
+---------------------------------+------+-----------------------------------------------------------------------------+
| 2 Points, Radius                | icon | Draw a circle with two points on the circumference and with an assigned     |
|                                 |      | radius.                                                                     |
+---------------------------------+------+-----------------------------------------------------------------------------+
| 3 Points                        | icon | Draw a circle assigning three points on the circumference.                  |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Concentric                      | icon | Draw a circle concentric, with the same centre point, to an existing circle.|
+---------------------------------+------+-----------------------------------------------------------------------------+
| Circle Inscribed                | icon | Draw a circle inside an existing polygon of four sides or more.             |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Tangential 2 Circles, Radius    | icon | Draw a circle tangential to two circles with a given radius.                |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Tangential, 2 Circles, 1 Point  | icon | Draw a circle tangential to two existing circles and assigning a centre     |
|                                 |      | point to establish the radius.                                              |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Tangential, 2 Points            | icon | Draw a circle tangential to an existing circle and define the diameter and  |
|                                 |      |placement by assigning two points on the circumference.                      |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Tangential, 2 Circles, Radius   | icon | Draw a circle tangential to two existing circles with a given radius.       |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Tangential, 3 Circles           | icon | Draw a circle tangential to three existing circles and/or lines.            |
+---------------------------------+------+-----------------------------------------------------------------------------+

Curve
~~~~~
.. table:: Curve Tools
    :widths: 15 10 75
+---------------------------------+------+-----------------------------------------------------------------------------+
| Tool                            | Icon | Description                                                                 |
+=================================+======+=============================================================================+
| Center, Point, Angles           | icon | Draw a curve (arc) with a given radius defined by a center point and a point|
|                                 |      | on the circumference, the direction of rotation (clockwise or               |
|                                 |      | counter-clockwise), a point defining the start position of the arc and a    |
|                                 |      | point defining the end position of the arc.                                 |
+---------------------------------+------+-----------------------------------------------------------------------------+
| 3 Points                        | icon | Draw a curve (arc) by assigning three points on the circumference of the arc|
|                                 |      |  defining the start position, a point on the circumference and end position |
|                                 |      | of the arc.                                                                 |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Concentric                      | icon | Draw a curve (arc) concentric, with the same centre point, to an existing   |
|                                 |      | curve (arc) with a defined offset.(*)                                       |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Arc Tangential                  | icon | Draw a curve (arc) tangential to the end of an exsiting line segment with a |
|                                 |      | defined radius or angle (deg).                                              |
+---------------------------------+------+-----------------------------------------------------------------------------+

Ellipse
~~~~~~
.. table:: Ellipse Tools
    :widths: 15 10 75
+---------------------------------+------+-----------------------------------------------------------------------------+
| Tool                            | Icon | Description                                                                 |
+=================================+======+=============================================================================+
| Ellipse (Axis)                  | icon | Draw an ellipse by assigning a centre point, a point on the circumference of|
|                                 |      | major access anda point on the circumference the minor access.              |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Ellipse Arc (Axis)              | icon | N/A                                                                         |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Ellipse Foci Point              | icon | Draw an ellipse by assigning two foci points and a point  on the            |
|                                 |      | circumference.                                                              |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Ellipse 4 Point                 | icon | Draw an ellipse assigning four points on the circumference.                 |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Ellipse Center and 3 Points     | icon | Draw an ellipse by assigning a centre point three points on the             |
|                                 |      | circumference.                                                              |
+---------------------------------+------+-----------------------------------------------------------------------------+
| Ellipse Inscribed               | icon |  Draw a Ellipse constrained by four existing non-parallel line segments.    |
+---------------------------------+------+-----------------------------------------------------------------------------+


toolname
~~~~~~
.. table:: toolname Tools
    :widths: 15 10 75
+---------------------------------+------+-----------------------------------------------------------------------------+
| Tool                            | Icon | Description                                                                 |
+=================================+======+=============================================================================+
|                                 |      |                                                                             |
|                                 |      |                                                                             |
+---------------------------------+------+-----------------------------------------------------------------------------+

