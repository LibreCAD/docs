.. User Manual, LibreCAD v2.2.x


.. _tools: 
   
Drawing Tools
=============

The drawing tools are used to create and modify entities such as lines, circles, etc. in a drawing.  Commands can be selected from the menu, toolbars or entered via the :ref:`command line <cmdline>`.

Several drawing tools require additional parameters and will provide prompts on the **Tool Options** toolbar.  *This toolbar should always be enabled.*  If the tool options do not appear, from the menu select **Widgets -> Toolbar ->** and enable **Tool Options**.  If using the :ref:`command line<widget-cmdLine>`, the same tool options are available via the toolbar or the command line.  The tools that have options are shown in the table below.


Line
----
.. csv-table::  
    :widths: 15, 10, 15, 60
    :header-rows: 1
    :stub-columns: 0
    :class: fix-table

    "Tool", "Icon", "Command", "Description"
    "2 points", |icon01|, "l, li, line", "
        | Draw a line between two assigned points.
        |
        | **Tool Options:** 
        | |tlopt14|"
    "Angle", |icon02|, "", "
        | Draw a line from an assigned point defining the start, middle or end of the line and with an assigned length and angle.
        | 
        | **Tool Options:** 
        | |tlopt07|"
    "Horizontal", |icon03|, "", "
        | Draw a horizontal line from an assigned point defining the start, middle or end of the line and with an assigned length.
        | 
        | **Tool Options:** 
        | |tlopt10|"
    "Vertical", |icon04|, "ver, vertical", "
        | Draw a vertical line from an assigned point defining the start, middle or end of the line and with an assigned length.
        | 
        | **Tool Options:** 
        | |tlopt10|"
    "Rectangle", |icon06|, "rec, rect, rectangle", "
        | Draw a rectagle by assigning the points of two diagonally opposite corners. "
    "Parallel through point", |icon07|, "pp, ptp", "
        | Draw a given number of lines parallel to a selected existing line through an assigned point.
        | 
        | **Tool Options:** 
        | |tlopt13|"
    "Parallel", |icon08|, "o, pa, offset, parallel", "
        | Draw a given number of lines parallel to a selected existing line with a given distance between lines.
        | 
        | **Tool Options:** 
        | |tlopt12|"
    "Bisector", |icon09|, "bi, bisect", "
        | Draw a given number of lines bisecting two existing non-parallel lines (e.g. at an angle to each other with or without a common point). 
        | **Tool Options:** 
        | |tlopt09|"
    "Tangent (P,C)", |icon10|, "tanpc, tangentpc", "
        | Draw a line from an assigned point tangent to an existing circle."
    "Tangent (C,C)", |icon11|, "", "
        | Draw a line tangent to two existing circles."
    "Tangent Orthogonal", |icon12|, "", "
        | Draw a line tangent to an existing circle and perpendicular to an existing line."
    "Orthogonal", |icon13|, "ortho, perp", "
        | Draw a line of a given length perpendicular to an existing line placing the centre at an assigned point.
        | 
        | **Tool Options:** 
        | |tlopt11|"
    "Relative Angle", |icon14|, "", "
        | Draw a line with a given length and at a given angle relative to an existing line placing the centre of the line at an assigned point.
        | 
        | **Tool Options:** 
        | |tlopt08|"
    "Polygon (Cen,Cor)", |icon15|, "pl, polyline", "
        | Draw a polygon with a given number of sides assigning the centre point and point of one vertex.
        | 
        | **Tool Options:** 
        | |tlopt15|"
    "Polygon (Cen,Tan)", |icon16|, "", "
        | Draw a polygon with a given number of sides assigning the centre point and point of the centre of one side.
        | 
        | **Tool Options:** 
        | |tlopt15|"
    "Polygon (Cor,Cor)", |icon17|, "poly2, polygon2v", "
        | Draw a polygon with a given number of sides assigning the two points of one side.
        | 
        | **Tool Options:** 
        | |tlopt15|"


Circle
------
.. csv-table:: 
    :widths: 15, 10, 15, 60
    :header-rows: 1
    :stub-columns: 0
    :class: fix-table

    "Tool", "Icon", "Command", "Description"
    "Centre, Point", |icon18|, "ci, circle", "
        | Draw a circle with a given radius by assigning a centre point and a point on the circumference."
    "2 Points", |icon20|, "c2, circle2", "
        | Draw a circle with a given diameter by assigning two opposite points on the circumference."
    "2 Points, Radius", |icon21|, "", "
        | Draw a circle with two points on the circumference and with an assigned radius.
        | 
        | **Tool Options:** 
        | |tlopt01|"
    "3 Points", |icon22|, "c3, circle3", "
        | Draw a circle assigning three points on the circumference."
    "Centre, Radius", |icon19|, "", "
        | Draw a circle with a given radius centred at an assigned point on the circumference.
        | 
        | **Tool Options:** 
        | |tlopt01|"
    "Tangential, 2 Circles, 1 Point", |icon26|, "", "
        | Draw a circle tangential to two existing circles and assigning a centre point to establish the radius."
    "Tangential, 2 Points", |icon27|, "", "
        | Draw a circle tangential to an existing circle and define the diameter and placement by assigning two points on the circumference."
    "Tangential, 2 Circles, Radius", |icon28|, "", "
        | Draw a circle tangential to two existing circles with a given radius.
        | 
        | **Tool Options:** 
        | |tlopt01|"
    "Tangential, 3 Circles", |icon29|, "ct3, tan3", "
        | Draw a circle tangential to three existing circles and/or lines."
..
    "Concentric", |icon23|, "", "Draw a circle concentric, with the same centre point, to an existing circle."
    "Circle Inscribed", |icon24|, "", "Draw a circle inside an existing polygon of four sides or more."


Curve
-----
.. csv-table:: 
    :widths: 15, 10, 15, 60
    :header-rows: 1
    :stub-columns: 0
    :class: fix-table

    "Tool", "Icon", "Command", "Description"
    "Center, Point, Angles", |icon30|, "", "
        | Draw a curve (arc) with a given radius defined by a center point and a point on the circumference, the direction of rotation (clockwise or counter-clockwise), a point defining the start position of the arc and a point defining the end position of the arc.
        | 
        | **Tool Options:** 
        | |tlopt03|"
    "3 Points", |icon32|, "a, ar, arc", "
        | Draw a curve (arc) by assigning three points on the circumference of the arc defining the start position, a point on the circumference and end position of the arc."
    "Arc Tangential", |icon34|, "", "
        | Draw a curve (arc) tangential to the end of an exsiting line segment with a defined radius or angle (deg).
        | 
        | **Tool Options:** 
        | |tlopt02| 
        | or
        | |tlopt04|"
    "Spline", |icon41|, "spl, spline", "
        | Draw an open or closed spline (curve) by assigning control points and a given degree of freedom (1 - 3).
        | 
        | **Tool Options:** 
        | |tlopt22|"
    "Spline through points", |icon42|, "stp, spline2", "
        | Draw an open or closed spline (curve) by defining points on the spline.
        | 
        | **Tool Options:** 
        | |tlopt23|"
    "Ellipse Arc (Axis)", |icon36|, "", "
        | N/A"
    "Freehand Line", |icon05|, "fhl, free", "
        | Draw a non-geometric line."
..
    "Concentric", |icon33|, "", "Draw a curve (arc) concentric, with the same centre point, to an existing curve (arc) with a defined offset.(*)"


Ellipse
-------
.. csv-table:: 
    :widths: 15, 10, 15, 60
    :header-rows: 1
    :stub-columns: 0
    :class: fix-table

    "Tool", "Icon", "Command", "Description"
    "Ellipse (Axis)", |icon35|, "", "
        | Draw an ellipse by assigning a centre point, a point on the circumference of major access and a point on the circumference the minor access."
    "Ellipse Foci Point", |icon37|, "", "
        | Draw an ellipse by assigning two foci points and a point  on the circumference."
    "Ellipse 4 Point", |icon38|, "", "
        | Draw an ellipse assigning four points on the circumference."
    "Ellipse Center and 3 Points", |icon39| , "", "
        | Draw an ellipse by assigning a centre point three points on the circumference."
    "Ellipse Inscribed", |icon40| , "ei, ie", "
        | Draw a Ellipse constrained by four existing non-parallel line segments."


Polyline
--------
.. csv-table:: 
    :widths: 15, 10, 15, 60
    :header-rows: 1
    :stub-columns: 0
    :class: fix-table

    "Tool", "Icon", "Command", "Description"
    "Polyline", |icon43|, "pl, polyline", "
        | Draw an open or closed continuous line consisting of one or more straight line or arc segments defined by endpoints and / or radius or angle for arcs.
        | 
        | **Tool Options:** 
        | |tlopt19|"
    "Add node", |icon44|, "", "
        | Add node to existing polyline. (Use ""Snap on Entity"" to place new node on segment.)"
    "Append node", |icon45|, "", "
        | Add one or more segments to an existing polyline by selecting polyine and adding new node endpoint."
    "Delete node", |icon46|, "", "
        | Delete selected node of an existing polyline."
    "Delete between two nodes", |icon47|, "", "
        | Delete one or more nodes between selected nodes of an existing polyline."
    "Trim segments", |icon48|, "", "
        | Extend two seperate non-parallel segments of an existing polyline to intersect at a new node."
    "Create Equidistant Polylines", |icon49|, "", "
        | Draw a given number of polylines parallel to a selected existing polyline with a given distance between lines.
        | 
        | **Tool Options:** 
        | |tlopt20|"
    "Create Polyline from Existing Segments", |icon50|, "", "
        | Create polyline from two or more existing seperate line or arc segments forming a continuous line."


Select
------
.. csv-table:: 
    :widths: 15, 10, 15, 60
    :header-rows: 1
    :stub-columns: 0
    :class: fix-table

    "Tool", "Icon", "Command", "Description"
    "Deselect all", |icon59|, "tn", "
        | Deselect all entities on visible layers ([Ctrl]-[K] or default [Esc] action)."
    "Select All", |icon58|, "sa", "
        | Select all entities on visible layers ([Ctrl]-[A])."
    "Select Entity", |icon51|, "", "
        | Select, or deselect, one or more entities (default cursor action)."
    "(De-)Select Contour", |icon54|, "", "
        | Select or deselected entities connected by shared points."
    "Select Window", |icon52|, "", "
        | Select one or more enties enclosed by selection window (L to R), or crossed by selection window (R to L) (default cursor ""drag"" action)."
    "Deselect Window", |icon53|, "", "
        | Deselect one or more enties enclosed by selection window (L to R), or crossed by selection window (R to L)."
    "Select Intersected Entities", |icon55|, "", "
        | Select on or more entities crossed by selection line."
    "Deselect Intersected Entities", |icon56|, "", "
        | Deselect on or more entities crossed by selection line."
    "(De-)Select Layer", |icon57|, "", "
        | Select or deselected all entities on the layer of the selected entity."
    "Invert Selection", |icon60|, "", "
        | Select all un-selected entities will deselecting all selected entities."


Dimension
---------
.. csv-table:: 
    :widths: 15, 10, 15, 60
    :header-rows: 1
    :stub-columns: 0
    :class: fix-table

    "Tool", "Icon", "Command", "Description"
    "Aligned", |icon61|, "da", "
        | Apply dimension lines and text aligned to an existing entity by selecting start and end points on a line segment and placement point for the text.
        | 
        | **Tool Options:** 
        | |tlopt06|"
    "Linear", |icon62|, "dr", "
        | Apply dimension lines and text at an defined angle to an entity by selecting start and end points on a line segment and placement point for the text.
        | 
        | **Tool Options:** 
        | |tlopt05|"
    "Horizontal", |icon63|, "dh", "
        | Apply dimension lines and text aligned to an entity by selecting start and end points on a line segment and placement point for the text.
        | 
        | **Tool Options:** 
        | |tlopt06|"
    "Vertical", |icon64|, "dv", "
        | Apply dimension lines and text aligned to an entity by selecting start and end points on a line segment and placement point for the text.
        | 
        | **Tool Options:** 
        | |tlopt06|"
    "Radial", |icon65|, "dimradial", "
        | Apply dimension lines and text a circle's or arc's radius by selecting entity and placement point for the text.
        | 
        | **Tool Options:** 
        | |tlopt06|"
    "Diametric", |icon66|, "dimdiameter", "
        | Apply dimension lines and text a circle's or arc's diameter by selecting entity and placement point for the text.
        | 
        | **Tool Options:** 
        | |tlopt06|"
    "Angular", |icon67|, "dimangular", "
        | Apply angular dimension by selecting two existing non-parallel line segments and placement point for the text.
        | 
        | **Tool Options:** 
        | |tlopt06|"
    "Leader", |icon68|, "ld", "
        | Draw a text leader by by selecting start (arrow location), intermediate and end points."


.. _tool-modify:

Modify
------
.. csv-table:: 
    :widths: 15, 10, 15, 60
    :header-rows: 1
    :stub-columns: 0
    :class: fix-table

    "Tool", "Icon", "Command", "Description"
    "Order", "", "", "
        | Order entities within a layer.  Selected entities can be moved to top, bottom, *raised* (moved forward) over another entity or *lowered* (moved backwards) behind an entity."
    "Move / Copy", |icon69|, "mv", "
        | Move a selected entity by defining a reference point and a relative target point. Optionally keep the original entity (Copy), create mulitple copies and / or alter attributes and layer."
    "Rotate", |icon70|, "ro", "
        | Rotate a selected entity around a rotation point, moving the entity from a reference point to a target point. Optionally keep the original entity, create multiple copies and / or alter attributes and layer."
    "Scale", |icon71|, "sz", "
        | Increase or decrease the size of a selected entity from a reference point by a defined factor for both axis.  Optionally keep the original entity, create mulitple copies and / or alter attributes and layer."
    "Mirror", |icon72|, "mi", "
        | reate a mirror image of a selected entity around an axis defined by two points.  Optionally keep the original entity and / or alter attributes and layer."
    "Move and Rotate", |icon73|, "", "
        | Move a selected entity by defining a reference point and a relative target point and rotataing the entity at a given angle.  Optionally keep the original entity, create mulitple copies and / or alter attributes and layer."
    "Rotate Two", |icon74|, "", "
        | Rotate a selected entity around an absolute rotation point, while rotating the entity around a relative reference point to a target point. Optionally keep the original entity, create multiple copies and / or alter attributes and layer."
    "Revert direction", |icon75|, "revert", "
        | Swap start and end points of one or more selected entities."
    "Trim",  |icon76| , "tm, trim", "
        | Cut the length of a line entity to an intersecting line entity."
    "Trim Two",  |icon77| , "t2, tm2", "
        | Cut the lengthes of two intersecting lines to the point of intersection."
    "Lengthen",  |icon78| , "le", "
        | Extend the length of a line entity to an intersecting line entity.
        | 
        | **Tool Options:** 
        | |tlopt18|"
    "Offset",  |icon79| , "o, pa, offset, parallel", "
        | Copy a selected entity to a defined distance in the specified direction."
    "Bevel", |icon80|, "ch, bevel", "
        | Create a sloping edge between two intersecting line segments with defined by a setback on each segment.
        | 
        | **Tool Options:** 
        | |tlopt16|"
    "Fillet", |icon81|, "fi, fillet", "
        | Create a rounded edge between two intersecting line segments with defined radius.
        | 
        | **Tool Options:** 
        | |tlopt17|"
    "Divide",  |icon82| , "di, div, cut", "
        | Divide, or break, al line at the selected ''cutting'' point."
    "Stretch", |icon83|, "ss", "
        | Move a selected portion of a drawing by defining a reference point and a relative target point."
    "Properties", |icon84|, "mp, prop", "
        | Modify the attributes of ''one or more'' selected entities, including Layer, Pen color, Pen width, and Pen Line type."
    "Attributes", |icon85|, "ma, attr", "
        | Modify the common attributes of ''one or more'' selected entities, including Layer, Pen color, Pen width, and Pen Line type."
    "Explode Text into Letters", |icon86|, "", "
        | Separate a string of text into individual character entities."
    "Explode", |icon87|, "xp", "
        | Separate one or more selected blocks or compound entities into individual entities."
    "Delete selected", |icon88| , "[Del], er", "
        | Delete one or more selected entities."
.. 
    "Delete", |iconNN|, "er", "Mark one or more entities to be deleted, press [Enter] to complete operation."
    "Delete Freehand", |iconNN|, "", "Delete segment within a polyline define by two points. (Use ''Snap on Entity'' to place points.)"


Info
----
.. csv-table:: 
    :widths: 15, 10, 15, 60
    :header-rows: 1
    :stub-columns: 0
    :class: fix-table

    "Tool", "Icon", "Command", "Description"
    "Distance Point to Point", |icon90|, "dpp, dist", "
        | Provides distance, cartesian and polar coordinates between two specified points."
    "Distance Entity to Point", |icon91|, "", "
        | Provides shortest distance selected entity and specified point."
    "Angle between two lines", |icon92|, "ang, angle", "
        | Provides angle between two selected line segments, measured counter-clockwise."
    "Total length of selected entities", |icon93|, "", "
        | Provides total length of one or more selected entities (length of line segment, circle circimference, etc)."
    "Polygonal Area", |icon94|, "ar, area", "
        | Provides area and circumference of polygon defined by three or more specified points."
..
    "Point inside contour", |icon89|, "", "Provides indication of point being inside or outside of the selected ''closed'' contour (polygon, circle, ployline, etc)."


Others
------
.. csv-table:: 
    :widths: 15, 10, 15, 60
    :header-rows: 1
    :stub-columns: 0
    :class: fix-table

    "Tool", "Icon", "Command", "Description"
    ":ref:`MText <text>`", |icon96|, "mtxt, mtext", "
        | Insert multi-line text into drawing at a specified base point.  Optionally define font, text height, angle, width factor, alignment, angle, special symbols and character set.
        | 
        | **Tool Options:** 
        | |tlopt24|"
    ":ref:`Text <text>`", |icon96|, "txt, text", "
        | Insert single-line text into drawing at a specified base point.  Optionally define font, text height,  alignment, angle, special symbols and character set.
        | 
        | **Tool Options:** 
        | |tlopt24|"
    "Hatch", |icon97|, "ha, hatch", "
        | Fill a closed entity (polygon, circle, polyline, etc) with a defined pattern or a solid fill.  Optionally define scale and angle."
    "Points", |icon99|, "po, point", "
        | Draw a point at the assigned coordinates."

..
    "Insert Image", |icon98|, "", "Insert an image, bitmapped or vector, at a specified point.  Optionally define angle, scale factor and DPI."


..  Icon mapping:

.. |icon00| image:: /images/icons/librecad.ico
            :height: 24
            :width: 24
.. |icon01| image:: /images/icons/line_2p.svg
            :height: 24
            :width: 24
.. |icon02| image:: /images/icons/line_angle.svg
            :height: 24
            :width: 24
.. |icon03| image:: /images/icons/line_horizontal.svg
            :height: 24
            :width: 24
.. |icon04| image:: /images/icons/line_vertical.svg
            :height: 24
            :width: 24
.. |icon05| image:: /images/icons/line_freehand.svg
            :height: 24
            :width: 24
.. |icon06| image:: /images/icons/line_rectangle.svg
            :height: 24
            :width: 24
.. |icon07| image:: /images/icons/line_parallel_p.svg
            :height: 24
            :width: 24
.. |icon08| image:: /images/icons/line_parallel.svg
            :height: 24
            :width: 24
.. |icon09| image:: /images/icons/line_bisector.svg
            :height: 24
            :width: 24
.. |icon10| image:: /images/icons/line_tangent_pc.svg
            :height: 24
            :width: 24
.. |icon11| image:: /images/icons/line_tangent_cc.svg
            :height: 24
            :width: 24
.. |icon12| image:: /images/icons/line_tangent_perpendicular.svg
            :height: 24
            :width: 24
.. |icon13| image:: /images/icons/line_perpendicular.svg
            :height: 24
            :width: 24
.. |icon14| image:: /images/icons/line_relative_angle.svg
            :height: 24
            :width: 24
.. |icon15| image:: /images/icons/line_polygon_cen_cor.svg
            :height: 24
            :width: 24
.. |icon16| image:: /images/icons/line_polygon_cen_tan.svg
            :height: 24
            :width: 24
.. |icon17| image:: /images/icons/line_polygon_cor_cor.svg
            :height: 24
            :width: 24
.. |icon18| image:: /images/icons/circle_center_point.svg
            :height: 24
            :width: 24
.. |icon19| image:: /images/icons/circle_center_radius.svg
            :height: 24
            :width: 24
.. |icon20| image:: /images/icons/circle_2_points.svg
            :height: 24
            :width: 24
.. |icon21| image:: /images/icons/circle_2_points_radius.svg
            :height: 24
            :width: 24
.. |icon22| image:: /images/icons/circle_3_points.svg
            :height: 24
            :width: 24
.. icon23
.. icon24 
.. |icon25| image:: /images/icons/circle_tangential_2circles_radius.svg
            :height: 24
            :width: 24
.. |icon26| image:: /images/icons/circle_tangential_2circles_point.svg
            :height: 24
            :width: 24
.. |icon27| image:: /images/icons/circle_tangential_2points.svg
            :height: 24
            :width: 24
.. |icon28| image:: /images/icons/circle_tangential_2circles_radius.svg
            :height: 24
            :width: 24
.. |icon29| image:: /images/icons/circle_tangential_2circles_radius.svg
            :height: 24
            :width: 24
.. |icon30| image:: /images/icons/arc_center_point_angle.svg
            :height: 24
            :width: 24
.. |icon32| image:: /images/icons/arc_3_points.svg
            :height: 24
            :width: 24
.. icon33 
.. |icon34| image:: /images/icons/arc_continuation.svg
            :height: 24
            :width: 24
.. |icon35| image:: /images/icons/ellipse_axis.svg
            :height: 24
            :width: 24
.. |icon36| image:: /images/icons/ellipse_arc_axis.svg
            :height: 24
            :width: 24
.. |icon37| image:: /images/icons/ellipse_foci_point.svg
            :height: 24
            :width: 24
.. |icon38| image:: /images/icons/ellipse_4_points.svg
            :height: 24
            :width: 24
.. |icon39| image:: /images/icons/ellipse_center_3_points.svg
            :height: 24
            :width: 24
.. |icon40| image:: /images/icons/ellipse_inscribed.svg
            :height: 24
            :width: 24
.. |icon41| image:: /images/icons/spline.svg
            :height: 24
            :width: 24
.. |icon42| image:: /images/icons/spline_points.svg
            :height: 24
            :width: 24
.. |icon43| image:: /images/icons/polylines.svg
            :height: 24
            :width: 24
.. |icon44| image:: /images/icons/polylineadd.png
            :height: 24
            :width: 24
.. |icon45| image:: /images/icons/polylineappend.png
            :height: 24
            :width: 24
.. |icon46| image:: /images/icons/polylinedel.png
            :height: 24
            :width: 24
.. |icon47| image:: /images/icons/polylinedelbetween.png
            :height: 24
            :width: 24
.. |icon48| image:: /images/icons/polylinetrim.png
            :height: 24
            :width: 24
.. |icon49| image:: /images/icons/polylineequidstant.png
            :height: 24
            :width: 24
.. |icon50| image:: /images/icons/polylinesegment.png
            :height: 24
            :width: 24
.. |icon51| image:: /images/icons/select_entity.svg
            :height: 24
            :width: 24
.. |icon52| image:: /images/icons/select_window.svg
            :height: 24
            :width: 24
.. |icon53| image:: /images/icons/deselect_window.svg
            :height: 24
            :width: 24
.. |icon54| image:: /images/icons/deselect_contour.svg
            :height: 24
            :width: 24
.. |icon55| image:: /images/icons/select_intersected_entities.svg
            :height: 24
            :width: 24
.. |icon56| image:: /images/icons/deselect_intersected_entities.svg
            :height: 24
            :width: 24
.. |icon57| image:: /images/icons/deselect_layer.svg
            :height: 24
            :width: 24
.. |icon58| image:: /images/icons/select_all.svg
            :height: 24
            :width: 24
.. |icon59| image:: /images/icons/deselect_all.svg
            :height: 24
            :width: 24
.. |icon60| image:: /images/icons/select_inverted.svg
            :height: 24
            :width: 24
.. |icon61| image:: /images/icons/dim_aligned.svg
            :height: 24
            :width: 24
.. |icon62| image:: /images/icons/dim_linear.svg
            :height: 24
            :width: 24
.. |icon63| image:: /images/icons/dim_horizontal.svg
            :height: 24
            :width: 24
.. |icon64| image:: /images/icons/dim_vertical.svg
            :height: 24
            :width: 24
.. |icon65| image:: /images/icons/dim_radial.svg
            :height: 24
            :width: 24
.. |icon66| image:: /images/icons/dim_diametric.svg
            :height: 24
            :width: 24
.. |icon67| image:: /images/icons/dim_angular.svg
            :height: 24
            :width: 24
.. |icon68| image:: /images/icons/dim_leader.svg
            :height: 24
            :width: 24
.. |icon69| image:: /images/icons/move_copy.svg
            :height: 24
            :width: 24
.. |icon70| image:: /images/icons/move_rotate.svg
            :height: 24
            :width: 24
.. |icon71| image:: /images/icons/rotate2.svg
            :height: 24
            :width: 24
.. |icon72| image:: /images/icons/mirror.svg
            :height: 24
            :width: 24
.. |icon73| image:: /images/icons/move_rotate.svg
            :height: 24
            :width: 24
.. |icon74| image:: /images/icons/rotate2.svg
            :height: 24
            :width: 24
.. |icon75| image:: /images/icons/revert_direction.svg
            :height: 24
            :width: 24
.. |icon76| image:: /images/icons/trim.svg
            :height: 24
            :width: 24
.. |icon77| image:: /images/icons/trim2.svg
            :height: 24
            :width: 24
.. |icon78| image:: /images/icons/trim_value.svg
            :height: 24
            :width: 24
.. |icon79| image:: /images/icons/offset.svg
            :height: 24
            :width: 24
.. |icon80| image:: /images/icons/bevel.svg
            :height: 24
            :width: 24
.. |icon81| image:: /images/icons/fillet.svg
            :height: 24
            :width: 24
.. |icon82| image:: /images/icons/divide.svg
            :height: 24
            :width: 24
.. |icon83| image:: /images/icons/stretch.svg
            :height: 24
            :width: 24
.. |icon84| image:: /images/icons/properties.svg
            :height: 24
            :width: 24
.. |icon85| image:: /images/icons/attributes.svg
            :height: 24
            :width: 24
.. |icon86| image:: /images/icons/explode_text_to_letters.svg
            :height: 24
            :width: 24
.. |icon87| image:: /images/icons/explode.svg
            :height: 24
            :width: 24
.. |icon88| image:: /images/icons/delete.svg
            :height: 24
            :width: 24
.. |icon89| image:: /images/icons/
.. |icon90| image:: /images/icons/distance_point_to_point.svg
            :height: 24
            :width: 24
.. |icon91| image:: /images/icons/distance_point_to_point.svg
            :height: 24
            :width: 24
.. |icon92| image:: /images/icons/angle_line_to_line.svg
            :height: 24
            :width: 24
.. |icon93| image:: /images/icons/total_length_selected_entities.svg
            :height: 24
            :width: 24
.. |icon94| image:: /images/icons/polygonal_area.svg
            :height: 24
            :width: 24
.. |icon95| image:: /images/icons/
.. |icon96| image:: /images/icons/text.svg
            :height: 24
            :width: 24
.. |icon97| image:: /images/icons/hatch.svg
            :height: 24
            :width: 24
.. |icon98| image:: /images/icons/
.. |icon99| image:: /images/icons/points.svg
            :height: 24
            :width: 24


..  Tool Options mapping:

.. |tlopt01| image:: /images/toolOptions/toCircleRad.png
            :height: 32
            :width: 178
.. |tlopt02| image:: /images/toolOptions/toCurveAng.png
            :height: 32
            :width: 283
.. |tlopt03| image:: /images/toolOptions/toCurve.png
            :height: 32
            :width: 139
.. |tlopt04| image:: /images/toolOptions/toCurveRad.png
            :height: 32
            :width: 283
.. |tlopt05| image:: /images/toolOptions/toDimnLin.png
            :height: 32
            :width: 681
.. |tlopt06| image:: /images/toolOptions/toDimn.png
            :height: 32
            :width: 424
.. |tlopt07| image:: /images/toolOptions/toLineAngle.png
            :height: 32
            :width: 338
.. |tlopt08| image:: /images/toolOptions/toLineAngRel.png
            :height: 32
            :width: 288
.. |tlopt09| image:: /images/toolOptions/toLineBisct.png
            :height: 32
            :width: 317
.. |tlopt10| image:: /images/toolOptions/toLineHorzVert.png
            :height: 32
            :width: 338
.. |tlopt11| image:: /images/toolOptions/toLineOrtho.png
            :height: 32
            :width: 231
.. |tlopt12| image:: /images/toolOptions/toLineParlOff.png
            :height: 32
            :width: 231
.. |tlopt13| image:: /images/toolOptions/toLineParlPt.png
            :height: 32
            :width: 143
.. |tlopt14| image:: /images/toolOptions/toLine.png
            :height: 32
            :width: 179
.. |tlopt15| image:: /images/toolOptions/toLinePoly.png
            :height: 32
            :width: 159
.. |tlopt16| image:: /images/toolOptions/toModBevel.png
            :height: 32
            :width: 404
.. |tlopt17| image:: /images/toolOptions/toModFillet.png
            :height: 32
            :width: 210
.. |tlopt18| image:: /images/toolOptions/toModLen.png
            :height: 32
            :width: 168
.. |tlopt19| image:: /images/toolOptions/toPoly1.png
            :height: 32
            :width: 348
.. |tlopt20| image:: /images/toolOptions/toPoly2.png
            :height: 32
            :width: 192
.. |tlopt21| image:: /images/toolOptions/toPrtPreview.png
            :height: 32
            :width: 289
.. |tlopt22| image:: /images/toolOptions/toSpline1.png
            :height: 32
            :width: 261
.. |tlopt23| image:: /images/toolOptions/toSpline2.png
            :height: 32
            :width: 231
.. |tlopt24| image:: /images/toolOptions/toText.png
            :height: 32
            :width: 307


