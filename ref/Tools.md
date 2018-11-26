### Tools ###

The drawing tools are used to create and modify entities such as lines, circles, etc in a drawing... yada, yada, yada

#### Line ####
|**Tool**|**Icon**|**Menu Path**|**Description**|
|-----|-----|-----|-----|
|**2 points**|||Draw a line between two assigned points.|
|**Angle**|||Draw a line from an assigned point defining the start, middle or end of the line and with an assigned length and angle.|
|**Horizontal**|||Draw a horizontal line from an assigned point defining the start, middle or end of the line and with an assigned length.|
|**Vertical**|||Draw a vertical line from an assigned point defining the start, middle or end of the line and with an assigned length.|
|**Freehand Line**|||Draw a non-geometric line.|
|**Parallel through point**|||Draw a given number of lines parallel to a selected existing line through an assigned point.|
|**Parallel**|||Draw a given number of lines parallel to a selected existing line with a given distance between lines.|
|**Rectangle**|||Draw a rectagle by assigning the points of two diagonally opposite corners.|
|**Bisector**|||Draw a given number of lines bisecting two existing non-parallel lines (e.g. at an angle to each other with or without a common point).|
|**Tangent (P,C)**|||Draw a line from an assigned point tangent to an existing circle.|
|**Tangent (C,C)**|||Draw a line tangent to two existing circles.|
|**Tangent Orthogonal**|||Draw a line tangent to an existing circle and perpendicular to an existing line.|
|**Orthogonal**|||Draw a line of a given length perpendicular to an existing line placing the centre at an assigned point.|
|**Relative Angle**|||Draw a line with a given length and at a given angle relative to an existing line placing the centre of the line at an assigned point.|
|**Polygon (Cen,Cor)**|||Draw a polygon with a given number of sides assigning the centre point and point of one vertex.|
|**Polygon (Cen,Tan)**|||Draw a polygon with a given number of sides assigning the centre point and point of the centre of one side.|
|**Polygon (Cor,Cor)**|||Draw a polygon with a given number of sides assigning the two points of one side.|

#### Circle ####
|**Tool**|**Icon**|**Menu Path**|**Description**|
|-----|-----|-----|-----|
|**Centre, Point**|||Draw a circle with a given radius by assigning a centre point and a point on the circumference.|
|**Centre, Radius**|||Draw a circle with a given radius centred at an assigned point.|
|**2 Points**|||Draw a circle with a given diameter by assigning two opposite points on the circumference.|
|**2 Points, Radius**|||Draw a circle with two points on the circumference and with an assigned radius.|
|**3 Points**|||Draw a circle assigning three points on the circumference.|
|**Concentric**|||Draw a circle concentric, with the same centre point, to an existing circle.|
|**Circle Inscribed**|||Draw a circle inside an existing polygon of four sides or more.|
|**Tangential 2 Circles, Radius**|||Draw a circle tangential to two circles with a given radius.|
|**Tangential, 2 Circles, 1 Point**|||Draw a circle tangential to two existing circles and assigning a centre point to establish the radius.|
|**Tangential, 2 Points**|||Draw a circle tangential to an existing circle and define the diameter and placement by assigning two points on the circumference.|
|**Tangential, 2 Circles, Radius**|||Draw a circle tangential to two existing circles with a given radius.|
|**Tangential, 3 Circles**|||Draw a circle tangential to three existing circles and/or lines.|

#### Curve ####
|**Tool**|**Icon**|**Menu Path**|**Description**|
|-----|-----|-----|-----|
|**Center, Point, Angles**|||Draw a curve (arc) with a given radius defined by a center point and a point on the circumference, the direction of rotation (clockwise or counter-clockwise), a point defining the start position of the arc and a point defining the end position of the arc.|
|**3 Points**|||Draw a curve (arc) by assigning three points on the circumference of the arc defining the start position, a point on the circumference and end position of the arc.|
|**Concentric**|||Draw a curve (arc) concentric, with the same centre point, to an existing curve (arc) with a defined offset.(*)|
|**Arc Tangential**|||Draw a curve (arc) tangential to the end of an exsiting line segment with a defined radius or angle (deg).|

#### Ellipse ####
|**Tool**|**Icon**|**Menu Path**|**Description**|
|-----|-----|-----|-----|
|**Ellipse (Axis)**|||Draw an ellipse by assigning a centre point, a point on the circumference of major access and a point on the circumference the minor access.|
|**Ellipse Arc (Axis)**|||N/A|
|**Ellipse Foci Point**|||Draw an ellipse by assigning two foci points and a point  on the circumference.|
|**Ellipse 4 Point**|||Draw an ellipse assigning four points on the circumference.|
|**Ellipse Center and 3 Points**|||Draw an ellipse by assigning a centre point three points on the circumference.|
|**Ellipse Inscribed**||| Draw a Ellipse constrained by four existing non-parallel line segments.|

#### Spline ####
|**Tool**|**Icon**|**Menu Path**|**Description**|
|-----|-----|-----|-----|
|**Spline**|||Draw an open or closed spline (curve) by assigning control points and a given degree of freedom (1 - 3).|
|**Spline through points**|||Draw an open or closed spline (curve) by defining points on the spline.|

#### Polyline ####
|**Tool**|**Icon**|**Menu Path**|**Description**|
|-----|-----|-----|-----|
|**Polyline**|||Draw an open or closed continuous line consisting of one or more straight line or arc segments defined by endpoints and / or radius or angle for arcs.|
|**Add node**|||Add node to existing polyline. (Use "Snap on Entity" to place new node on segment.)|
|**Append node**|||Add one or more segments to an existing polyline by selecting polyine and adding new node endpoint.|
|**Delete node**|||Delete selected node of an existing polyline.|
|**Delete between two nodes**|||Delete one or more nodes between selected nodes of an existing polyline.|
|**Trim segments**|||Extend two seperate non-parallel segments of an existing polyline to intersect at a new node.|
|**Create Equidistant Polylines**|||Draw a given number of polylines parallel to a selected existing polyline with a given distance between lines.|
|**Create Polyline from Existing Segments**|||Create polyline from two or more existing seperate line or arc segments forming a continuous line.|

#### Select ####
|**Tool**|**Icon**|**Menu Path**|**Description**|
|-----|-----|-----|-----|
|**Select Entity**|||Select, or deselect, one or more entities (default cursor action).|
|**Select Window**|||Select one or more enties enclosed by selection window (L to R), or crossed by selection window (R to L) (default cursor "drag" action).|
|**Deselect Window**|||Deselect one or more enties enclosed by selection window (L to R), or crossed by selection window (R to L).|
|**(De-)Select Contour**|||Select or deselected entities connected by shared points.|
|**Select Intersected Entities**|||Select on or more entities crossed by selection line.|
|**Deselect Intersected Entities**|||Deselect on or more entities crossed by selection line.|
|**(De-)Select Layer**|||Select or deselected all entities on the layer of the selected entity.|
|**Select All**|||Select all entities on visible layers ([Ctrl]-[A]).|
|**Deselect all**||| Deselect all entities on visible layers ([Ctrl]-[K] or default [Esc] action).|
|**Invert Selection**|||Select all un-selected entities will deselecting all selected entities.|

#### Dimension ####
|**Tool**|**Icon**|**Menu Path**|**Description**|
|-----|-----|-----|-----|
|**Aligned**|||Apply dimension lines and text aligned to an existing entity by selecting start and end points on a line segment and placement point for the text.|
|**Linear**|||Apply dimension lines and text at an defined angle to an entity by selecting start and end points on a line segment and placement point for the text.|
|**Horizontal**|||Apply dimension lines and text aligned to an entity by selecting start and end points on a line segment and placement point for the text.|
|**Vertical**|||Apply dimension lines and text aligned to an entity by selecting start and end points on a line segment and placement point for the text.|
|**Radial**|||Apply dimension lines and text a circle's or arc's radius by selecting entity and placement point for the text.|
|**Diametric**|||Apply dimension lines and text a circle's or arc's diameter by selecting entity and placement point for the text.|
|**Angular**|||Apply angular dimension by selecting two existing non-parallel line segments and placement point for the text.|
|**Leader**|||Draw a text leader by by selecting start (arrow location), intermediate and end points.|

#### Modify ####
|**Tool**|**Icon**|**Menu Path**|**Description**|
|-----|-----|-----|-----|
|**Attributes**|||Modify the common attributes of **''one or more**'' selected entities, including Layer, Pen color, Pen width, and Pen Line type.|
|**Delete**||| Mark one or more entities to be deleted, press [Enter] to complete operation.|
|**Delete selected**|||Delete one or more selected entities.|
|**Delete Freehand**|||Delete segment within a polyline define by two points. (Use "Snap on Entity" to place points.)|
|**Move / Copy**|||Move a selected entity by defining a reference point and a relative target point. Optionally keep the original entity (Copy), create mulitple copies and / or alter attributes and layer.|
|**Revert direction**|||Swap start and end points of one or more selected entities.|
|**Rotate**|||Rotate a selected entity around a rotation point, moving the entity from a reference point to a target point. Optionally keep the original entity, create multiple copies and / or alter attributes and layer.|
|**Scale**|||Increase or decrease the size of a selected entity from a reference point by a defined factor for both axis.  Optionally keep the original entity, create mulitple copies and / or alter attributes and layer.|
|**Mirror**|||Create a mirror image of a selected entity around an axis defined by two points.  Optionally keep the original entity and / or alter attributes and layer.|
|**Move and Rotate**|||Move a selected entity by defining a reference point and a relative target point and rotataing the entity at a given angle.  Optionally keep the original entity, create mulitple copies and / or alter attributes and layer.|
|**Rotate Two**|||Rotate a selected entity around an absolute rotation point, while rotating the entity around a relative reference point to a target point. Optionally keep the original entity, create multiple copies and / or alter attributes and layer.|
|**Stretch**|||Move a selected portion of a drawing by defining a reference point and a relative target point.|
|**Bevel**|||Create a sloping edge between two intersecting line segments with defined by a setback on each segment.|
|**Fillet**|||Create a rounded edge between two intersecting line segments with defined radius.|
|**Explode Text into Letters**|||Separate a string of text into individual character entities.|
|**Explode**|||Separate one or more selected blocks into individual entities.|

#### Info ####
|**Tool**|**Icon**|**Menu Path**|**Description**|
|-----|-----|-----|-----|
|**Point inside contour**|||Provides indication of point being inside or outside of the selected ''closed'' contour (polygon, circle, ployline, etc).|
|**Distance Point to Point**|||Provides distance, cartesian and polar coordinates between two specified points.|
|**Distance Entity to Point**|||Provides shortest distance selected entity and specified point.|
|**Angle between two lines**|||Provides angle between two selected line segments, measured counter-clockwise.|
|**Total length of selected entities**|||Provides total length of one or more selected entities (length of line segment, circle circimference, etc).|
|**Polygonal Area**|||Provides area of polygon defined by three or more specified points.|

#### Miscellaneous ####
|**Tool**|**Icon**|**Menu Path**|**Description**|
|-----|-----|-----|-----|
|**MText**|||Insert multi-line text into drawing at a specified base point.  Optionally define font, text height, angle, width factor, alignment, angle, special symbols and character set.|
|**Text**|||Insert single-line text into drawing at a specified base point.  Optionally define font, text height,  alignment, angle, special symbols and character set.|
|**Hatch**|||Fill a closed entity (polygon, circle, polyline, etc) with a defined pattern or a solid fill.  Optionally define scale and angle.|
|**Insert Image**|||Insert an image, bitmapped or vector, at a specified point.  Optionally define angle, scale factor and DPI.|
|**Points**|||Draw a point at the assigned coordinates.|
