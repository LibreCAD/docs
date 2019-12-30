.. User Manual, LibreCAD v2.2.x


.. _drawing:

Creating and Modifying Entities
===============================

Drawing geometric shapes, or *entities* is familiar to many people that have used drawing and paint programs.  
As with many programs, there are a multitude of ways to generate the desired results.  LibreCAD is the same - there are many ways to obtain the same results in a completed drawing - far too many to be able document an example for each one in a User Guide.  For users it is important know what tools are available and how to apply them.

This section of the User Guide brings together many other parts of the LibreCAD manual and will show how to use a variety tools to **create** and **modify** drawings.  Be sure to read through the **Reference** section, particularly the :ref:`Fundamentals <fundamentals>`, the :ref:`Drawing Tools <tools>` and the :ref:`Snapping <snaps>` sections to obtain an understanding of the basic operation of LibreCAD and its various tools.

.. note::
   The examples below use both the the command line and the mouse for input.  In cases where the command line is used and additional input is required because of a **Tool Option** (see Drawing Tools) see the *note* below the command text.  Where the mouse is the primary form of input, the instruction are provided in bullet point form.


Creating Entities
-----------------

Creating new geometric entities all use similar methods.  Generally,  creating an entity requires placement of a minimum of two points (Well, unless the entity being drawn is a point), or a single point and an additional parameter such as length or radius.  In some case the same result can be obtained using several different methods.  For example, drawing a vertical line can be done via keyboard entry using the :ref:`command line<widget-cmdLine>` to select a tool and then define two points with the *absolute* or *relative* *Cartesian* coordinates:

Absolute Cartesian coordinates:

::

   li
   0,0
   0,500
   k


Or, relative Cartesian coordinates: 

::

   li
   0,0
   @0,500
   k

.. topic:: Info
   *@0,500* places the next point 0 units horinzonatally (X axis) and 500 units vertically (Y axis) from the previously placed point.

It can also be done with relative *polar* coordinates:

::

   li
   0,0
   500<90
   k

.. topic:: Info
   *500<90* places the next point 500 units 90 degrees from the previously placed point.

The same line can also be drawn using just the mouse.  With **Snap on Grid** |icon03| enabled:

   - Select the **2 Points** line tool [icon]
   - Click at *0,0* and then
   - Click at *0,500* (use the **Status Bar** to locate the correct coordinates).

Other tools can also be used achieve the same result:

::

   ver   
   0,0

.. note::
   Ensure the *Length* is set to "500" and the *Snap Point:* is "Start" in the **Tool Options** textbox.

The tool and method used is entirely up to the user to obtain the desired results. The use of a particular tool may be determined by the next operation that allows the drawing to be quickly extended.  A good understanding of the available tools allows the user to select the appropriate tool for the current operation.

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

   - Click the **2 Points** line tool icon.
   - Enable the "Snap on Endpoints" snap tool and click close to the end of the line at *absolute coordinate* 0,500.
   - Drag the mouse to the right and, with the "Snap on Grid" snap enabled, place a point at 400,500.  Clicking the mouse should result in a horizontal line ending at precisely at 400,500.
   - Press [Esc] to exit the complete the command.

.. hint::
   It may be necessary to "Zoom In" to ensure the grid is at the correct resolution to be able to accurately place a line's start or end point.

A combination of the **2 Points** line tool the "Restrict Horizontal" snap tool can also be use as an alternative to "Snap on Grid". 

Alternatively, a horizontal line can be added:

   - Click the **Horizontal** line tool icon.
   - On the "Tool Options" tool bar specify a length of 400 units and the "Snap Point" at the "Start".
   - With the "Snap on Endpoints" enabled click close to the end of the line at *absolute coordinate* 0,500.  Clicking the mouse should result in a horizontal line ending at 400,500.
   - Press [Esc] to exit the complete the command.

Being that the end points of the existing lines have been established, the outline can be  completed quickly with the addition of a line:

   - Click the **2 Points** line tool icon.
   - Enable the "Snap on Endpoints" snap tool and click close to the end of the line at *absolute coordinate* 400,500.
   - Drag the mouse to the right and down and place a point close to 600,300.  Clicking the mouse should result in a line angled down and to the right, closing the object's outline.
   - Press [Esc] to exit the command.

Another option is to draw the line at the desired angle:

   - Click the **Angle** line tool icon.
   - On the "Tool Options" tool bar specify an *Angle* of "135", a *Length* of "300" units and the *Snap Point* at the "Start".
   - With the "Snap on Endpoints" enabled, click close to the end of the line at *absolute coordinate* 600,300.  Clicking the mouse should result in a line angled up and to the left.  The line is too long, but can be *trimmed* to suit (see "*Modifying Entities*" below).

Whichever of the above methods is used, the result should be:   (Insert image)


All of the above examples create the object by drawing individual lines.  A completely different approach is to start with a rectangle:

::

   rec
   0,0
   600,500
   k

And then modify it (see below).

Circles can be added in a similar fashion.  It can be drawn by specifying the coordinates of the centre and of a point on the circumference:

::

   ci
   200,300
   @0,100
   k


A circle of a given size can also be drawn with a known radius:

   - Click the *Circle, Radius* tool icon.
   - On the "Tool Options" tool bar specify a *Radius* of "100".
   - With the "Snap on grid" place the centre of the circle at *absolute coordinate* 200,300.
   - Press [Esc] to exit the command, or click the right mouse button once.

The drawing should now appear as: (insert image)


Modifying Entities
------------------

There are a variety of tools that can be used to modify existing entities.  The tools cam be found in the **Tools -> Modify** menu or as a :ref:`dock widget <widgets>`.  These tools allow entities, depending on the type, to be moved, rotated, scaled, mirrored, lengths increased or decreased, divided (i.e. split), etc.  A complete list and descriptions of the tools can be found in the :ref:`Drawing Tools - Modify <tool-modify>` reference section.

Continuing with the previous example - starting with a rectangle - the shape can be modified as required with the **Bevel** (or "chamfer") tool:

::

   ch

.. note::
   Ensure with "Trim" is checked and "Length 1" and "Length 2" is set at "200" in the **Tool Options**.

As prompted in the "Command Line" dock, and on the Status Bar, select the first entity (the top horizontal line of the rectangle) and then the second entity (the right vertical line of the rectangle).  Press [Esc] to exit the command.

**Fillets** (rounding a corner) are done in a similar manner:

::

   fi

.. note::
   Ensure with "Trim" is checked and "Radius" is set at "50" in the **Tool Options**.

- As prompted in the "Command Line" dock, and on the Status Bar, select the first entity (the bottom horizontal line of the rectangle) and then 
- select the second entity (the left vertical line of the rectangle).
- Press [Esc] to exit the command.

The drawing should appear as: (Insert image)
  
A previous example above left a diagonal line that is too long.  The length can be easily trimmed:

   - Click the "Trim" icon |icon76|
   - Click the top horizontal line.  This line is the "limiting entity" that determines where the second line is going to be trimmed to.
   - Click the line to be trimmed, the "entitiy to trim" anywhere along the line that is to be kept (below the top horizontal line).
   - Press [Esc] to exit the command.


Many of the other tools work in a similar manner.  


Attributes and Properties
~~~~~~~~~~~~~~~~~~~~~~~~~

As shown in the :ref:`Entities <entities>` section in **Fundamentals**, an entitiy consist of "Pens" (color, width, line type) and "Layers".  These attributes can be changed using one of two :ref:`Modify <tool-modify>` tools:

   - Attributes: allows the "Pen" or "Layers" to be modified for one or more entities.
   - Properties: allows the "Pen", "Layers" or geometry to modified *one* entity.

Both tools operate in a similar fashion and for similar purposes but there are a couple of key differences.  The **Attributes** tool allows a change to the attibutes to be applied to *one or more selected entities* while the **Properities** tool can only be used for a *single selected entity*.  In addition, the **Properties** tool allows the *geometry* to be edited.  The geometry of an entity will vary be the type of entity.  For example a line's geometry consist of the X and Y coordinates of the endpoints, while a circles geometry consists of the X /Y coordinates of the centre of the circle and its radius.  


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

..  Icon mapping:
.. |icon03| image:: /images/icons/snap_grid.svg
            :height: 24
            :width: 24
.. |icon76| image:: /images/icons/trim.svg
            :height: 24
            :width: 24

