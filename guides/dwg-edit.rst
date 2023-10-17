.. User Manual, LibreCAD v2.2.x

.. Default include
.. include:: /inclFiles/notice.rst


.. _dwg-edit:

Creating and Editing Entities
=============================

Drawing geometric shapes, or *entities* is familiar to many people that have used drawing and paint programs.  
As with many programs, there are a multitude of ways to generate the desired results.  LibreCAD is the same - there are many ways to obtain the same results in a completed drawing - far too many to be able document an example for each one in a User Guide.  For users it is important know what tools are available and how to apply them.

This section of the **User Guide** brings together many other parts of the LibreCAD manual and will show how to use a variety tools to *create* and *modify* drawings.  Be sure to read through the **Reference** section, particularly the :ref:`Fundamentals <fundamentals>`, the :ref:`Drawing Tools <tools>` and the :ref:`Snapping <snaps>` sections to obtain an understanding of the basic operation of LibreCAD and its various tools.  It is also helpful to understand the different :ref:`View <view>` tools and commands.

.. note::
    The examples below use both the the command line and the mouse for input.  In cases where the command line is used and additional input is required because of a **Tool Option** (see **Drawing Tools**) see the *note* below the command text.  Where the mouse is the primary form of input, the instructions are provided in a numbered list.


Creating Entities
-----------------

Creating new geometric entities all use similar methods.  Generally, creating an entity requires placement of a minimum of two points (Well, unless the entity being drawn is a point), or a single point and an additional parameter such as length or radius.  In some case the same result can be obtained using several different methods.  For example, drawing a vertical line can be done via keyboard entry using the :ref:`command line <widget-cmdLine>` to select a tool and then define two points with the *absolute* or *relative* *Cartesian* coordinates:

Using absolute Cartesian coordinates::

	li
	10,10
	10,110
	k

The first set of coordinates place the starting point of the line at 10 units horizontally and 10 units vertically from the origin (0,0).  The second set places the end point of the line at 10 units horizontally and 110 units vertically from the origin (0,0), resulting in a vertical line 100 units long.

Or, using relative Cartesian coordinates::

	li
	10,10
	@0,100
	k

The "**@**" designates *relative coordinates*.  The *@0,100* relative Cartesian coordinates places the next point 0 units horizontally (X axis) and 100 units vertically (Y axis) from the point previously placed at 10,10.

It can also be done with relative *polar* coordinates::

	li
	10,10
	@100<90
	k

The "**<**" designates a *polar coordinate*.  The *@100<90* polar coordinate places the next point 100 units 90 degrees from the X axis of the point previously placed at 10,10.

The same line can also be drawn using just the mouse:

    #. Enabled **Snap on Grid** |icon03a|.
    #. Select the **2 Points** line tool |icon01|.
    #. Click at *10,10* (use the :ref:`Status Bar <statusbar>` to locate the absolute coordinates)
    #. Click at *10,110*
    #. Press [Esc] or right-click twice to exit the command.

Other tools can also be used achieve the same result::

    ver   
    10,10

.. note::
    Ensure the *Length* is set to "100" and the *Snap Point:* is "Start" in the "Tool Options" text box.

All the above examples create a line of the same length with the same start and end points.  These examples help illustrate the multiple ways to achieve the same result.  The use of a particular tool may be determined by the next operation that allows the drawing to be quickly extended.  A good understanding of the available tools allows the user to select the appropriate tool for the current operation.

While the above example always start at *10,10*, the initial point can be placed anywhere::

	li
	10,110
	10,10
	k

Drawings are generally created with multiple lines segments with the end of one segment being the start of another.  Lines can be drawn with multiple connected segments by using the end of the current segment as the starting point and defining the end point of the next segment.  Further, additional points can be defined using any of the methods previously shown::

    li
    10,110
    10,10
    @125,0
    @50<90
    k

.. figure:: /images/doohickey01.png
    :align: center
    :scale: 67
    :alt: Doohickey Example #1

    Example #1

.. actual image size 490px x 365px

Using the mouse, or another pointing device, along with the snapping tools provide an alternative to using the command line for creating drawings.  As with the command line, there are multiple line tools that can be used to produce the same result.  For example, adding the to the the previous example, a horizontal line can be added using various methods:

    #. Click the **2 Points** line tool icon |icon01|.
    #. Enable the **Snap on Endpoints** |icon04| and click close to the end of the line at *absolute coordinate* 10,110.
    #. Drag the mouse to the right and, with the **Snap on Grid** |icon03a| enabled, place a point at *absolute coordinate* 85,110.  Clicking the mouse should result in a horizontal line ending at precisely at 85,110.
    #. Press [Esc] or right-click to exit the command.


.. hint::
    It may be necessary to "Zoom In" to ensure the grid is at the correct resolution to be able to accurately place a line's start or end point.

A combination of the **2 Points** line tool |icon01| the **Restrict Horizontal** tool |icon10| can also be use as an alternative to **Snap on Grid** |icon03a|. 

Alternatively, a horizontal line can be added:

    #. Click the **Horizontal** line tool icon |icon03|.  On the "Tool Options" tool bar specify a length of 75 units and the "Snap Point" at the "Start".
    #. With the **Snap on Endpoints** |icon04| enabled click close to the end of the line at *absolute coordinate* 10,110.  Clicking the mouse should result in a horizontal line ending at 85,110.
    #. Press [Esc] or right-click to exit the command.


.. figure:: /images/doohickey02.png
    :align: center
    :scale: 67
    :alt: Doohickey Example #2

    Example #2

.. actual image size 490px x 365px

Being that the end points of the existing lines have been established, the outline can be  completed quickly with the addition of a line:

    #. Click the **2 Points** line tool icon |icon01|.
    #. Enable the **Snap on Endpoints** |icon04| and click close to the end of the line at *absolute coordinate* 85,110.
    #. Drag the mouse to the right and down and place a point close to 135,60.  Clicking the mouse should result in a line angled down and to the right, closing the object's outline.
    #. Press [Esc] or right-click twice to exit the command.


Whichever of the above methods is used, the result should be similar to:

.. figure:: /images/doohickey03.png
    :align: center
    :scale: 67
    :alt: Doohickey Example #3

    Example #3

.. actual image size 490px x 365px

Another option is to draw the line at the desired angle:

    #. Click the **Angle** line tool icon |icon02|.  On the "Tool Options" tool bar specify an *Angle* of "135", a *Length* of "80" units and the *Snap Point* at the "Start".
    #. With the **Snap on Endpoints** |icon04| enabled, click close to the end of the line at *absolute coordinate* 135,60.  Clicking the mouse should result in a line angled up and to the left.
    #. Press [Esc] to exit the command.

This option will result in a image similar to what is shown above, but with the diagonal line being a bit too long.  The line can be *trimmed* to suit (see "*Modifying Entities*" below):

.. figure:: /images/doohickey03a.png
    :align: center
    :scale: 67
    :alt: Doohickey Example #3a

    Example #3a

.. actual image size 490px x 365px

.. admonition:: Alternate Approach

    .. figure:: /images/doohickeyAlt01.png
        :align: right
        :scale: 50
        :alt: Doohickey Example #1 - Alternate Approach

        Alternate Approach

    .. actual image size 490px x 365px

    All of the above examples create the object by drawing individual lines.  A completely different approach is to start with a *rectangle*::

        rec
        10,10
        @125,100
        k

    And then modify it with the "Bevel" tool (**see below**).

    .. Force end of left / right text wrap
    .. include:: /inclFiles/eoWrap.rst

.. eo-admonition

Circles can be added in a similar fashion.  It can be drawn with the "Center, Point" tool by specifying the coordinates for the centre of the circle and of a point on the circumference::

    ci
    50,70
    @0,20
    k


A circle of a given size can also be drawn with a known radius:

    #. Click the *Circle, Radius* tool icon |icon19|.  On the "Tool Options" tool bar specify a *Radius* of "40".
    #. With the **Snap on Grid** |icon03a| enabled, place the centre of the circle at *absolute coordinate* 50,70.
    #. Press [Esc] or right-click to exit the command.

The drawing should now appear as: 

.. figure:: /images/doohickey04.png
    :align: center
    :scale: 67
    :alt: Doohickey Example #4

    Example #4

.. actual image size 490px x 365px


Modifying Entities
------------------

There are a variety of tools that can be used to edit and modify existing entities.  The tools are found in the **Tools -> Modify** menu or as a drawing tool :ref:`dock widget <widgets>`.  These tools allow entities, depending on the type, to be moved, rotated, scaled, mirrored, lengths increased or decreased, divided (i.e. split), etc.  A complete list and descriptions of the tools can be found in the :ref:`Drawing Tools - Modify <tool-modify>` reference section.

.. admonition:: Alternate Approach

    .. figure:: /images/doohickeyAlt02.png
        :align: right
        :scale: 50
        :alt: Doohickey Example #2 - Alternate Approach

        Alternate Approach - with the circle

    .. actual image size 490px x 365px

    Continuing with the alternate example - starting with a rectangle - the shape can be modified as required with the **Bevel** (or "chamfer") tool.  Its operation is similar to the fillet tool:

    #. Click the **Bevel** tool icon |icon80|.  Ensure with "Trim" is checked, and "Length 1" and "Length 2" is set at "50" in the "Tool Options".
    #. As prompted on the Status Bar, select the first entity (the top horizontal line of the rectangle), and then
    #. the second entity (the right vertical line of the rectangle).
    #. Press [Esc] or right-click to exit the command.

    .. Force end of left / right text wrap
    .. include:: /inclFiles/eoWrap.rst

.. eo-admonition

A rounded corner can be added to the drawing's the lower left corner with the **Fillet** tool:

    #. Click the **Fillet** tool icon |icon81|.  Ensure with "Trim" is checked and "Radius" is set at "10" in the "Tool Options".
    #. As prompted in the "Command Line" dock, and on the Status Bar, select the first entity (the bottom horizontal line of the rectangle), and then 
    #. Select the second entity (the left vertical line of the rectangle).
    #. Press [Esc] or right-click to exit the command.

The drawing should appear as:

.. figure:: /images/doohickey05.png
    :align: center
    :scale: 67
    :alt: Doohickey Example #5

    Example #5

.. actual image size 490px x 365px

*Example 3a* above left a diagonal line that is too long.  The length can be easily trimmed:

    #. Click the "Trim" icon |icon76|
    #. Click the top horizontal line.  This line is the "limiting entity" that determines where the second line is going to be trimmed to.
    #. Click the line to be trimmed, the "entity to trim" anywhere along the line that is to be kept (below the top horizontal line).
    #. Press [Esc] or right-click to exit the command.

.. important::

    These examples do not provide an example of every tool available in LibreCAD, but is intended to show the basic operation of some of the drawing and modifications tools.  Most of the other drawing and modifying tools work in a similar manner.  Being familiar with the :ref:`Drawing <tools>` and :ref:`Modify <tool-modify>` tools in the **Reference** section will help determine what tool can be used in a particular situation.

    These examples also illustrate that there are multiple ways to achieve the same result using a variety of methods.  There is no one best method.  The particular method used may depend on the state of the drawing and how existing entities can be used to build on, or perhaps it is a simple matter of using a preferred drawing / modifying tool.


Changing Attributes and Properties
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

As shown in the :ref:`Entities <entities>` section in **Fundamentals**, an entity consists of "Pens" (color, width, line type) and "Layers".  These *attributes* can be changed using one of two :ref:`Modify <tool-modify>` tools:

    - **Attributes**: allows the "Pen" or "Layers" to be modified for one or more entities.
    - **Properties**: allows the "Pen", "Layers" or geometry *of a single entity* to be modified.

Both tools operate in a similar fashion and for similar purposes, but there are a couple of key differences.  The **Attributes** tool allows a change to the attributes to be applied to *one or more selected entities* while the **Properties** tool can only be used for a *single entity*.  In addition, the **Properties** tool allows the *geometry* to be edited.  The geometry of an entity will vary be the type of entity.  For example a line's geometry consist of the X and Y coordinates of the endpoints, while a circles geometry consists of the X/Y coordinates of the centre of the circle and its radius.  


Layers and Pens
```````````````

Change an entity's layer is similar with both the **Attributes** and **Properties** tools.

Using the **Attributes** to change an entity's layer:

    #. Select the entity (or entities) to be moved to a different layer.
    #. From the menu select **Tools -> Modify -> Attributes**, or click the **Attributes** icon |icon85|.
    #. In the *Attributes* dialog, select the desired layer from the drop-down *Layer* selection box.
    #. Click **Ok**.

.. hint::

    Entities can also be moved from one layer to another by selecting one or more entities and then selecting the new *destination* layer in the **Layer List** dock.  To use this method the *Modify layer of selected entities, at layer activation* option on the **Application Preferences** **Defaults** tab must be enabled.

In a similar manner the color, width and/or line type can be changed:

    #. Select the entity (or entities) to be moved to a different layer.
    #. From the menu select **Tools -> Modify -> Attributes**, or click the **Attributes** icon |icon85|.
    #. In the *Attributes* dialog, select the desired pen attribute from the drop-down *Color, Width* and/or *Line type* selection box.
    #. Click **Ok**.

The **Properties** tool operates in a similar manner, but the tool need to be selected *before* selecting an entity:

    #. From the menu select **Tools -> Modify -> Properties**, or click the **Properties** icon |icon84|.
    #. Select the entity.
    #. In the *Properties* dialog, select the desired layer or pen attribute from the appropriate selection box.
    #. Click **Ok**.


Geometry (Properties)
`````````````````````

The **Properties** tool also allows the *geometry* of an entity to be changed.  The geometry is the information used to describe the entity.  The geometry available depends on the type of entity, for example:


.. table::
   :align: center
   :widths: auto
   :class: table-no-borders
   
   +-----------+-----+-----------+
   | |01Lprop| |     | |01Rprop| |
   +-----------+-----+-----------+

.. |01Lprop| image:: /images/propLine.png
        :scale: 50
        :alt: Properties - Line
.. actual image size 550px x 291px

.. |01Rprop| image:: /images/propMText.png
        :scale: 50
        :alt: Properties - MText
.. actual image size 693px x 478px

Some entities, such as a polyline, have limited properties available that can be changed.  Other entities, such as Text, have many properties that can be changes (including the text itself).

Also, the properties of a specific entity type, e.g. line, does not vary even if the specific tool used to create the entity varies.  A line drawn with the **2 Point** line tool will have the same properties as a line drawn with **Angle** tool. 

.. csv-table::
    :widths: 15, 25, 60
    :header-rows: 1
    :stub-columns: 0
    :class: table-fix-width

    "Entity Type", "Drawing Tool", "Properties"
    "Line", "2 points, Angle, Horizontal, etc", "Start and end point X/Y coordinates"
    "Circle", "”Centre, Point”, 2 Points, etc", "Center point X/Y coordinates, radius"
    "Curve", "”Center, Point, Angles”, 3 Points, etc", "| Center point X/Y coordinates, radius,
                                                          start/end angle"
    "Ellipse", "Ellipse (Axis), Ellipse Foci Point, etc", "| Center point X/Y coordinates, 
                                                             major/minor axis, rotation, start/end angle"
    "Polyline", "Polyline, Rectangle", "Open or closed"
    "Text", "Text", "| Text, font, text height/angle/width factor,
                       alignment, special characters"
    "MText", "MText", "| Text, font, text height/angle/line spacing,
                         alignment, special characters"
    "Dimension", "Aligned, Linear, etc", "Label, special symbol"
    "Blocks", "Block List, Library Browser", "| Insertion point X/Y coordinates, scale X/Y,
                                                rotation angle, array rows / columns and spacing"

Drawing Views
-------------

LibreCAD supports two drawing views to represent three-dimensional objects:

    - Orthogonal: Uses multiple two-dimensional views.
    - Isometric: Represents a three-dimensional view in two dimensions.


.. _dwg-orthogonal:

Orthogonal View
~~~~~~~~~~~~~~~

.. figure:: /images/doohickeyOrtho.png
    :align: right
    :figwidth: 350
    :scale: 52
    :alt: Doohickey - Orthogonal View

    Doohickey - Orthogonal View with Construction Lines (blue)

.. actual image size 670px x 555px

Orthogonal drawings use multiple views to provide a complete description of an object.  Each view of an orthogonal drawing is parallel to the axes.  Normally a front (the most complex view), top and right view are added to the drawing.  Additional views; back, left and bottom can be added if necessary.

Orthogonal drafting beyond the scope of the **LibreCAD User Manual**, but additional resources and examples are available in LibreCAD's `wiki <https://dokuwiki.librecad.org/>`_ or elsewhere on the web.

.. Force end of left / right text wrap
.. include:: /inclFiles/eoWrap.rst


.. _dwg-isometric:

Isometric View
~~~~~~~~~~~~~~

.. figure:: /images/doohickeyIso.png
    :align: right
    :figwidth: 350
    :scale: 67
    :alt: Doohickey - Isometric View

    Doohickey - Isometric View

.. actual image size 515px x 515px

:ref:`Isometric <isometric>` drawings represent an object on three axes in a two-dimensional drawing.  Isometric drawings uses the same tools for creating, modifying and changing attributes as an orthogonal drawings, but on a grid configuration specific for an isometric perspective.  Set the grid to suit an isometric perspective on the **Grid** tab of :ref:`Drawing Preferences <draw-prefs>`.  Selecting "Isometric Grid" displays the grid on three axes (X,Y,Z) allowing 3 dimensional drawings to be drawn in a 2D view.

In addition to setting the grid for isometric drawings, the "Snap indicator lines" on the **Appearance** tab of :ref:`Application Preferences <app-prefs>` can be set to "Isometric" to assist in with locating entities on the grid.  The "Isometric" crosshairs can be configured to Left, Top or Right to further aid in locating points on the grid.

Isometric drafting does require some techniques unique to isometric projection and is beyond the scope of the **LibreCAD User Manual**, but additional resources and examples are available in LibreCAD's `wiki <https://dokuwiki.librecad.org/>`_ or elsewhere on the web.

.. Force end of left / right text wrap
.. include:: /inclFiles/eoWrap.rst


..  Icon mapping:
.. |icon01| image:: /images/icons/line_2p.svg
            :height: 18
            :width: 18
.. |icon02| image:: /images/icons/line_angle.svg
            :height: 18
            :width: 18
.. |icon03| image:: /images/icons/line_horizontal.svg
            :height: 18
            :width: 18
.. |icon03a| image:: /images/icons/snap_grid.svg
            :height: 18
            :width: 18
.. |icon04| image:: /images/icons/snap_endpoints.svg
            :height: 18
            :width: 18
.. |icon10| image:: /images/icons/restr_hor.svg
            :height: 18
            :width: 18
.. |icon19| image:: /images/icons/circle_center_radius.svg
            :height: 18
            :width: 18
.. |icon76| image:: /images/icons/trim.svg
            :height: 18
            :width: 18
.. |icon80| image:: /images/icons/bevel.svg
            :height: 18
            :width: 18
.. |icon81| image:: /images/icons/fillet.svg
            :height: 18
            :width: 18
.. |icon84| image:: /images/icons/properties.svg
            :height: 18
            :width: 18
.. |icon85| image:: /images/icons/attributes.svg
            :height: 18
            :width: 18

