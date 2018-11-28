.. _tools: 
   
Drawing Tools
-------------

The drawing tools are used to create and modify entities such as lines, circles, etc in a drawing... yada, yada, yada


.. csv-table:: Line 
   :header: "Tool", "Icon", "Command", "Description"
   :widths: 40, 10, 20, 110
   
   "2 points", |icon01| ,"l, li, line","Draw a line between two assigned points."
   "Angle", |icon02| ,,"Draw a line from an assigned point defining the start, middle or end of the line and with an assigned length and angle."
   "Horizontal", |icon03| ,,"Draw a horizontal line from an assigned point defining the start, middle or end of the line and with an assigned length."
   "Vertical", |icon04| ,"ver, vertical","Draw a vertical line from an assigned point defining the start, middle or end of the line and with an assigned length."
   "Freehand Line", |icon05| ,"fhl, free","Draw a non-geometric line."
   "Parallel through point", |icon06| ,"pp, ptp","Draw a given number of lines parallel to a selected existing line through an assigned point."
   "Parallel", |icon07| ,"o, pa, offset, parallel","Draw a given number of lines parallel to a selected existing line with a given distance between lines."
   "Rectangle", |icon08| ,"rec, rect, rectangle","Draw a rectagle by assigning the points of two diagonally opposite corners. "
   "Bisector", |icon09| ,"bi, bisect","Draw a given number of lines bisecting two existing non-parallel lines (e.g. at an angle to each other with or without a common point). "
   "Tangent (P,C)", |icon10| ,"tanpc, tangentpc","Draw a line from an assigned point tangent to an existing circle."
   "Tangent (C,C)", |icon11| ,,"Draw a line tangent to two existing circles."
   "Tangent Orthogonal", |icon12| ,,"Draw a line tangent to an existing circle and perpendicular to an existing line."
   "Orthogonal", |icon13| ,"ortho, perp","Draw a line of a given length perpendicular to an existing line placing the centre at an assigned point."
   "Relative Angle", |icon14| ,,"Draw a line with a given length and at a given angle relative to an existing line placing the centre of the line at an assigned point."
   "Polygon (Cen,Cor)", |icon15| ,"pl, polyline","Draw a polygon with a given number of sides assigning the centre point and point of one vertex."
   "Polygon (Cen,Tan)", |icon16| ,,"Draw a polygon with a given number of sides assigning the centre point and point of the centre of one side. "
   "Polygon (Cor,Cor)", |icon17| ,"poly2, polygon2v","Draw a polygon with a given number of sides assigning the two points of one side."

.. csv-table:: Circle
   :header: "Tool", "Icon", "Command", "Description"
   :widths: 40, 10, 20, 110

   "Centre, Point", |icon18| ,"ci, circle","Draw a circle with a given radius by assigning a centre point and a point on the circumference."
   "Centre, Radius", |icon19| ,,"Draw a circle with a given radius centred at an assigned point on the circumference."
   "2 Points", |icon20| ,"c2, circle2","Draw a circle with a given diameter by assigning two opposite points on the circumference."
   "2 Points, Radius", |icon21| ,,"Draw a circle with two points on the circumference and with an assigned radius. "
   "3 Points", |icon22| ,"c3, circle3","Draw a circle assigning three points on the circumference."
   "Concentric", |icon23| ,,"Draw a circle concentric, with the same centre point, to an existing circle."
   "Circle Inscribed", |icon24| ,,"Draw a circle inside an existing polygon of four sides or more."
   "Tangential 2 Circles, Radius", |icon25| ,,"Draw a circle tangential to two circles with a given radius."
   "Tangential, 2 Circles, 1 Point", |icon26| ,,"Draw a circle tangential to two existing circles and assigning a centre point to establish the radius."
   "Tangential, 2 Points", |icon27| ,,"Draw a circle tangential to an existing circle and define the diameter and placement by assigning two points on the circumference."
   "Tangential, 2 Circles, Radius", |icon28| ,,"Draw a circle tangential to two existing circles with a given radius."
   "Tangential, 3 Circles", |icon29| ,"ct3, tan3","Draw a circle tangential to three existing circles and/or lines."

.. csv-table:: Curve
   :header: "Tool", "Icon", "Command", "Description"
   :widths: 40, 10, 20, 110

   "Center, Point, Angles", |icon30| ,,"Draw a curve (arc) with a given radius defined by a center point and a point on the circumference, the direction of rotation (clockwise or counter-clockwise), a point defining the start position of the arc and a point defining the end position of the arc."
   "3 Points", |icon32| ,"a, ar, arc","Draw a curve (arc) by assigning three points on the circumference of the arc defining the start position, a point on the circumference and end position of the arc."
   "Concentric", |icon33| ,,"Draw a curve (arc) concentric, with the same centre point, to an existing curve (arc) with a defined offset.(*)"
   "Arc Tangential", |icon34| ,,"Draw a curve (arc) tangential to the end of an exsiting line segment with a defined radius or angle (deg)."


.. csv-table:: Ellipse
   :header: "Tool", "Icon", "Command", "Description"
   :widths: 40, 10, 20, 110

   "Ellipse (Axis)", |icon35| ,,"Draw an ellipse by assigning a centre point, a point on the circumference of major access and a point on the circumference the minor access."
   "Ellipse Arc (Axis)", |icon36| ,,"N/A"
   "Ellipse Foci Point", |icon37| ,,"Draw an ellipse by assigning two foci points and a point  on the circumference."
   "Ellipse 4 Point", |icon38| ,,"Draw an ellipse assigning four points on the circumference."
   "Ellipse Center and 3 Points", |icon39| ,,"Draw an ellipse by assigning a centre point three points on the circumference."
   "Ellipse Inscribed", |icon40| ,," Draw a Ellipse constrained by four existing non-parallel line segments."


.. csv-table:: Spline
   :header: "Tool", "Icon", "Command", "Description"
   :widths: 40, 10, 20, 110

   "Spline", |icon41| ,"spl, spline","Draw an open or closed spline (curve) by assigning control points and a given degree of freedom (1 - 3)."
   "Spline through points", |icon42| ,"stp, spline2","Draw an open or closed spline (curve) by defining points on the spline."


.. csv-table:: Polyline
   :header: "Tool", "Icon", "Command", "Description"
   :widths: 40, 10, 20, 110

   "Polyline", |icon43| ,"pl, polyline","Draw an open or closed continuous line consisting of one or more straight line or arc segments defined by endpoints and / or radius or angle for arcs."
   "Add node", |icon44| ,,"Add node to existing polyline. (Use ""Snap on Entity"" to place new node on segment.)"
   "Append node", |icon45| ,,"Add one or more segments to an existing polyline by selecting polyine and adding new node endpoint."
   "Delete node", |icon46| ,,"Delete selected node of an existing polyline."
   "Delete between two nodes", |icon47| ,,"Delete one or more nodes between selected nodes of an existing polyline."
   "Trim segments", |icon48| ,,"Extend two seperate non-parallel segments of an existing polyline to intersect at a new node."
   "Create Equidistant Polylines", |icon49| ,,"Draw a given number of polylines parallel to a selected existing polyline with a given distance between lines."
   "Create Polyline from Existing Segments", |icon50| ,,"Create polyline from two or more existing seperate line or arc segments forming a continuous line."


.. csv-table:: Select
   :header: "Tool", "Icon", "Command", "Description"
   :widths: 40, 10, 20, 110

   "Select Entity", |icon51| ,,"Select, or deselect, one or more entities (default cursor action)."
   "Select Window", |icon52| ,,"Select one or more enties enclosed by selection window (L to R), or crossed by selection window (R to L) (default cursor ""drag"" action)."
   "Deselect Window", |icon53| ,,"Deselect one or more enties enclosed by selection window (L to R), or crossed by selection window (R to L)."
   "(De-)Select Contour", |icon54| ,,"Select or deselected entities connected by shared points."
   "Select Intersected Entities", |icon55| ,,"Select on or more entities crossed by selection line."
   "Deselect Intersected Entities", |icon56| ,,"Deselect on or more entities crossed by selection line."
   "(De-)Select Layer", |icon57| ,,"Select or deselected all entities on the layer of the selected entity."
   "Select All", |icon58| ,"sa","Select all entities on visible layers ([Ctrl]-[A])."
   "Deselect all", |icon59| ,"tn"," Deselect all entities on visible layers ([Ctrl]-[K] or default [Esc] action)."
   "Invert Selection", |icon60| ,,"Select all un-selected entities will deselecting all selected entities."


.. csv-table:: Dimension
   :header: "Tool", "Icon", "Command", "Description"
   :widths: 40, 10, 20, 110

   "Aligned", |icon61| ,"da","Apply dimension lines and text aligned to an existing entity by selecting start and end points on a line segment and placement point for the text."
   "Linear", |icon62| ,"dr","Apply dimension lines and text at an defined angle to an entity by selecting start and end points on a line segment and placement point for the text."
   "Horizontal", |icon63| ,"dh","Apply dimension lines and text aligned to an entity by selecting start and end points on a line segment and placement point for the text."
   "Vertical", |icon64| ,"dv","Apply dimension lines and text aligned to an entity by selecting start and end points on a line segment and placement point for the text."
   "Radial", |icon65| ,,"Apply dimension lines and text a circle's or arc's radius by selecting entity and placement point for the text."
   "Diametric", |icon66| ,,"Apply dimension lines and text a circle's or arc's diameter by selecting entity and placement point for the text."
   "Angular", |icon67| ,,"Apply angular dimension by selecting two existing non-parallel line segments and placement point for the text."
   "Leader", |icon68| ,"ld","Draw a text leader by by selecting start (arrow location), intermediate and end points."


.. csv-table:: Modify
   :header: "Tool", "Icon", "Command", "Description"
   :widths: 40, 10, 20, 110

   "Attributes", |icon69| ,"ma, attr","Modify the common attributes of ''one or more'' selected entities, including Layer, Pen color, Pen width, and Pen Line type."
   "Delete", |icon70| ,"er"," Mark one or more entities to be deleted, press [Enter] to complete operation."
   "Delete selected", |icon71| ,,"Delete one or more selected entities."
   "Delete Freehand", |icon72| ,,"Delete segment within a polyline define by two points. (Use ""Snap on Entity"" to place points.)"
   "Move / Copy", |icon73| ,"mv","Move a selected entity by defining a reference point and a relative target point. Optionally keep the original entity (Copy), create mulitple copies and / or alter attributes and layer."
   "Revert direction", |icon74| ,,"Swap start and end points of one or more selected entities."
   "Rotate", |icon75| ,"ro","Rotate a selected entity around a rotation point, moving the entity from a reference point to a target point. Optionally keep the original entity, create multiple copies and / or alter attributes and layer."
   "Scale", |icon76| ,"sz","Increase or decrease the size of a selected entity from a reference point by a defined factor for both axis.  Optionally keep the original entity, create mulitple copies and / or alter attributes and layer."
   "Mirror", |icon77| ,"mi","Create a mirror image of a selected entity around an axis defined by two points.  Optionally keep the original entity and / or alter attributes and layer."
   "Move and Rotate", |icon78| ,,"Move a selected entity by defining a reference point and a relative target point and rotataing the entity at a given angle.  Optionally keep the original entity, create mulitple copies and / or alter attributes and layer."
   "Rotate Two", |icon79| ,,"Rotate a selected entity around an absolute rotation point, while rotating the entity around a relative reference point to a target point. Optionally keep the original entity, create multiple copies and / or alter attributes and layer."
   "Stretch", |icon80| ,"ss","Move a selected portion of a drawing by defining a reference point and a relative target point."
   "Bevel", |icon81| ,"ch, fillet (bug)","Create a sloping edge between two intersecting line segments with defined by a setback on each segment."
   "Fillet", |icon82| ,"fi, fillet","Create a rounded edge between two intersecting line segments with defined radius."
   "Explode Text into Letters", |icon83| ,,"Separate a string of text into individual character entities."
   "Explode", |icon84| ,"xp","Separate one or more selected blocks into individual entities."


.. csv-table:: Info
   :header: "Tool", "Icon", "Command", "Description"
   :widths: 40, 10, 20, 110

   "Point inside contour", |icon85| ,,"Provides indication of point being inside or outside of the selected ''closed'' contour (polygon, circle, ployline, etc)."
   "Distance Point to Point", |icon86| ,"dpp, dist","Provides distance, cartesian and polar coordinates between two specified points."
   "Distance Entity to Point", |icon87| ,,"Provides shortest distance selected entity and specified point."
   "Angle between two lines", |icon88| ,"ang, angle","Provides angle between two selected line segments, measured counter-clockwise."
   "Total length of selected entities", |icon89| ,,"Provides total length of one or more selected entities (length of line segment, circle circimference, etc)."
   "Polygonal Area", |icon90| ,"ar, area","Provides area of polygon defined by three or more specified points."


.. csv-table:: Misc
   :header: "Tool", "Icon", "Command", "Description"
   :widths: 40, 10, 20, 110

   "MText", |icon91| ,"mtxt, mtext","Insert multi-line text into drawing at a specified base point.  Optionally define font, text height, angle, width factor, alignment, angle, special symbols and character set."
   "Text", |icon92| ,"txt, text","Insert single-line text into drawing at a specified base point.  Optionally define font, text height,  alignment, angle, special symbols and character set."
   "Hatch", |icon93| ,"ha, hatch","Fill a closed entity (polygon, circle, polyline, etc) with a defined pattern or a solid fill.  Optionally define scale and angle."
   "Insert Image", |icon94| ,,"Insert an image, bitmapped or vector, at a specified point.  Optionally define angle, scale factor and DPI."
   "Points", |icon95| ,"po, point","Draw a point at the assigned coordinates."
