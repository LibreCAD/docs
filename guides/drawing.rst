.. User Manual, LibreCAD v2.2.x


.. _drawing:

Drawing
=======

As with many programs, there are a multitude of ways to generate the final output.  LibreCAD is the same - there are many ways to obtain the same results - far too many to be able document an example for each one in a User Guide.  For users it is inmportant know what tools are available and how to apply them.

This section of the User Guide brings together many other parts of the LibreCAD manual and will show how to use a variety tools to **create** and **modify** drawings.  Be sure to reads through the **Reference** section, particularly the :ref:`Fundamentals <fundamentals>`, the :ref:`Drawing Tools <tools>` and the :ref: `Snapping <snaps>` sections to obtain an understanding of the basic operation of LibreCAD and its various tools.

 Drawing geometric shapes, or *entities* is familiar to many people that have used drawing and paint programs, but CAD (Computer Aided Drafting) offers greater precision and other advantages over the other types of programs.  



Creating Entities
-----------------

Creating new geometric entities all use similar methods.  Generally,  creating an entity requires placement of a minimum of two points (Well, unless the entity being drawn is a point), or a single point and an additional parameter such as length or radius.  In some case the same result can be obtained using several different methods.  For example, drawing a vertical line can be done via keyboard entry to select a tool and then define two points with the *absolute* or *relative* *Cartesian* coordinates:

Absolute Cartesian coordinates:

::

   li
   0,0
   0,500
   k


Or, Relative Cartesian coordinates: 

::

   li
   0,0
   @0,500
   k

It can also be done with relative *polar* coordinates:

::

   li
   0,0
   500<90
   k

The same line can also be drawn using just the mouse; with "Snap on Grid" [icon] turned on, select the "2 Point" line tool [icon], and click at *0,0* and then *0,500* (use the **Status Bar** to locate the correct coordinates).

Or, other tools can also be used achieve the same result:

::

   ver (with a the "Length" set at "500" in the **Tool Options** textbox.)
   0,0

The tool and method used is entirely up to the user to obtain the desired results. The use of a particular tool may be determined by the next operation to quickly extend or repeat the entity.  A good understanding of the available tools allows the user to select the appropriate tool for the current operation.

While the above example always start at *0,0*, the initial point can be placed anywhere:

::

   li
   0,500
   0,0
   k

Drawings are generally created with multiple lines segments with the end of one segment being the start of another.  Lines can be drawn with multiple connected segments by using the end of the current segment as the starting point and defining the end point of the next segment.  Further, additional points can be defined using any of the methods previously shown:

::

li
0,500
0,0
@600,0
@300<90
k

Using the mouse, or another pointing device, along with the "Snaps" provide an alternative to using the command line for creating drawings.  As with the command line, there are multiple line tools that can be used to produce the same result.  For example, adding the to the the previous example, a horizontal line can be added using various methods:

::

   Click the "2 points" line tool icon.
   Enable the "Snap on Endpoints" snap tool and click close to the end of the line at *absolute coordinate* 0,500.
   Drag the mouse to the right and, with the "Snap on Grid" snap enabled, place a point at 400,500.  It may be necessary to "Zoom In" to ensure the grid is at the correct resolution to be able to accurately place the line's end point.  Clicking the mouse should result in a horizontal line ending at 400,500.
   Press [Esc] to exit the complete the command.

A combination of the "2 Points" line tool the "Restrict Horizontal" snap tool can also be use as an alternative to "Snap on Grid". 

Alternatively, the line can be drawn with the "Horizontal" line tool:

::
   Click the "Horizontal" line tool icon.
   On the "Tool Options" tool bar specify a length of 400 units and the "Snap Point" at the "Start".
   With the "Snap on Endpoints" enabled click close to the end of the line at *absolute coordinate* 0,500.  Clicking the mouse should result in a horizontal line ending at 400,500.
   Press [Esc] to exit the complete the command.

Being that the end points of the existing lines have been defined, the "2 Point" line tool and "Snap on Endpoints" can quickly complete the outline:

::

   Click the "2 points" line tool icon.
   Enable the "Snap on Endpoints" snap tool and click close to the end of the line at *absolute coordinate* 400,500.
   Drag the mouse to the right and down and place a point close to 600,300.  Clicking the mouse should result in a line angled down and to the right, closing the object's outline.
   Press [Esc] to exit the complete the command.

Another option is to draw the line at the desired angle:

::
   Click the "Angle" line tool icon.
   On the "Tool Options" tool bar specify an angle of 135, a length of 200 units and the "Snap Point" at the "Start".
   With the "Snap on Endpoints" enabled click close to the end of the line at *absolute coordinate* 600,300.  Clicking the mouse should result in a line angled up and to the left.  The line is too long, but can be *trimmed* to suit (see "Modifying Entities" below).

All of the above examples create the oblect by drawing individual lines.  A completely different approach is to start with a rectangle:

::

   rec
   0,0
   600,500
   k




Modifying Entities
------------------

Not to be confused with the "Modify" tools, but for using 'handles', attribute and properties.  To follow...

Also, "selecting" entities.  To follow...


Changing Attributes
~~~~~~~~~~~~~~~~~~~

More to follow...

Changing an Entity's Layer
``````````````````````````

Sometimes it is necessary to change an entity's layer. To move one or more entities between layers:

	- Select the entities to be moved to a different layer.
	- From the menu select **Tools -> Modify -> Attributes**, or click the **Attributes** icon |icon02|.
	- In the *Attributes* dialog, select the desired layer from the drop-down the Layer selection box.
	- Click **Ok**.

Alternatively activate the option *Modify layer of selected entities, at layer activation* in the **Application Preferences, Defaults** tab .  With this option enabled entities can be assigned to a layer by selecting the entities and then selecting the destination layer.




Changing Properties
~~~~~~~~~~~~~~~~~~~

To follow...


