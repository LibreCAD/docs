.. _tools: 

Drawing Tools
-------------

The drawing tools are used to create and modify entities such as lines, circles, etc in a drawing... yada, yada, yada

Line
~~~~

+----------+----------+---------------+---------------------------------------------+
| **Tool** | **Icon** | **Menu Path** | **Description**                             |
+==========+==========+===============+=============================================+
| **2 points** | icon | path | Draw a line between two assigned points. |
| **Angle**  |  icon  |  path |   Draw a line from an assigned point defining the start, middle or end of the line and with an assigned length and angle.|
| **Horizontal**  |  icon  |  path    Draw a horizontal line from an assigned point defining the start, middle or end of the line and with an assigned length.|
| **Vertical**  |  icon  |  path    Draw a vertical line from an assigned point defining the start, middle or end of the line and with an assigned length.|

Simple table:

=====  =====  ======
   Inputs     Output
------------  ------
  A      B    A or B
=====  =====  ======
False  False  False
True   False  True
False  True   True
True   True   True
=====  =====  ======
