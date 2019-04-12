.. User Manual, LibreCAD v2.2.x


.. _annotate:

Annotating a Drawing
====================

A drawing in and of itself provides an image of what an object might look like, but it doesn’t provide a complete description of the object. Knowing how big the object is also very important, thus the need to provide the measurements and other textual information to describe the drawn object.  Together, dimensions and text is called *annotating* a drawing.

Dimensioning an object on a drawing provides the information necessary to be able to interpret the object and ultimately produce the it, whether it be a building or a widget.  Other textual information in the form of notes, or call-outs, etc. provide further details for the object.


.. _dimensioning:

Dimensioning
------------

Dimensions are used to define length, width, height of a line entity, or the diameter of circle entity or radius of arc entity.  A drawing's dimensions must be:

   - Accurate
   - Legible
   - Complete


Types of Dimensions
~~~~~~~~~~~~~~~~~~~
LibreCAD supports the following type of dimensions:

    - Aligned - parallel to a line between two points
    - Linear - distance between two points from any angle of interest, default is 0 (horizontal) and is changed via *Properties* toolbar
    - Horizontal - horizontal distance between two points, Linear with a starting angle of 0°
    - Vertical - vertical distance between two points, Linear with a starting angle of 90°
    - Radial - radius of an arc
    - Diametric - diameter of a circle
    - Angular - angle between two lines or linear parts of objects
    - Leader - not a dimension per se, but used for notes in drawings

A dimension consists of a few parts:

.. figure:: /images/dimnDesc.png
    :width: 1441px
    :height: 504px
    :align: right
    :scale: 50
    :alt: Dimension parts

The appearance of the dimensions are configured on the :ref:`Dimensions <dimn-prefs>` tab in the **Drawing Preferences** and as with many other aspects of a :ref:`drawing's setup <drawing-setup>`, there are some generally accepted values for dimensioning:

.. csv-table:: 
   :widths: 40, 20, 20, 20
   :header-rows: 1
   :stub-columns: 0

    "Dimension Component", "mm", "Decimal Inch", "Fractional Inch"
    "Dimension text height", "2.5", ".100", "3/32"
    "Dimension line gap", "1.5", ".0625", "1/16"
    "Extension line - Offset", "1.5", ".0625", "1/16"
    "Extension line - Enlarge", "3", ".125", "1/8"
    "Arrow size", "3", ".125", "1/8"


The size of each dimension component is the 'real world' size.  That is to say that if the text height is set to 2.5 mm, even if the drawing is scaled down when printed the text would remain as 2.5 mm on the printed drawing.  The value for the *General Scale* will need to be adjusted when generating a print.  Additional information can be found in the :ref:`Drawing Setup <drawing-setup>` and :ref:`Printing <printing-guide>` guides.


Rules for Dimensioning
~~~~~~~~~~~~~~~~~~~~~~

A few rules will help ensure dimensions must be accurate, legible and complete:

   - There should be only one way to interpret any one dimension.
   - Dimension and extension lines should not cross.
   - Extension lines and entity lines should not overlap.
   - Provide space between dimensions to ensure legibility.
   - The view that best shows an entity is the view that should be dimensioned.
   - Each entity on the drawing should be dimensioned and dimensioned only once.
   - There is no need to calculate or scale a dimension of an entity.
   - A dimension should be referenced to a logical origin point.
   - When there are multiple lines of dimensions, the longer dimensions are to be placed outside of shorter ones.
   - Except for large circles and arcs, all dimensions should be placed outside the part and spaced 10mm / 3/8" from the entity (*).
   - Dimensioned circles diameters and arcs with radiuses.
   - Center lines or center marks should be used on all circles and arcs.
   - Extended a circle's or arc's center lines and use as extensions line when possible.
   - Multiple lines of dimensions are spaced uniformly with a minimum of 6mm / 1/4” between dimension lines (*).
   - Use arrow heads or slash marks at the end of the dimension lines.

*: The minimum spacing need to be scaled with the drawing.  For example, if the drawing is 1:10, the spacing will need to be 60 mm between dimension lines and 100 mm from the entity.


Examples
````````

.. figure:: /images/dimnEg.png
    :width: 948px
    :height: 492px
    :align: center
    :scale: 75
    :alt: Dimension example

Leaders
-------

While leaders do not a dimension an entity, they are closely related to dimensioning as they are important for annotating and adding clarity to entities.  Leaders provide the ability to place pointers to identify a specific area of interest when adding a note and linking it to a particulate object.  Leaders take their setting from the :ref:`Dimensions <dimn-prefs>`.

.. figure:: /images/leaderEg.png
    :width: 748px
    :height: 278px
    :align: center
    :scale: 75
    :alt: Leader example

.. _text:

Text
----

Adding text to a drawing provides addition information; build notes, drawing title and related details, and so forth.  Text can be added using two either of the two types of text tools:
	- Text: Single line of text
	- MText: Multi-line text

.. figure:: /images/textText.png
    :width: 557px
    :height: 462px
    :align: left
    :scale: 50
    :alt: Text dialogue

.. figure:: /images/textMText.png
    :width: 621px
    :height: 475px
    :align: right
    :scale: 50
    :alt: MText (multi-line) dialogue

Both text tools proved several options for the appearance an placement ofthe test, however a couple are unique to the single-line, **Text** tool:

.. csv-table:: 
   :widths: 25, 40, 8, 8
   :header-rows: 1
   :stub-columns: 0

    "Option", "Description", "Text", "MText"
    "Font", "Select font for text", "X", "X"
    "Font - Height", "Set font height", "X", "X"
    "Font - Angle", "Places text at specified :ref:` angle <angles>`", "X", "X"
    "Font - Oblique", "*Inactive*", "X", " "
    "Font - Width factor", "", "X", " "
    "Font - Default line spacing", "Use default line spacing for specified font", " ", "X"
    "Font - Line spacing", "", " ", "X"
    "Alignment", "Place text aligned to *handle*; top, left/center/right,", "X", "X"
    "Alignment", "Place text aligned to *handle*; middle, left/center/right,", "X", "X"
    "Alignment", "Place text aligned to *handle*; baseline, left/center/right,", "X", " "
    "Alignment", "Place text aligned to *handle*; bottom, left/center/right,", "X", "X"
    "Alignment - *Fit*", "Places text between specified points while maintaining set height", "X", ""
    "Alignment - *Aligned*", "Places text between specified points while maintaining width to height ratio (scales text)", "X", ""
    "Alignment - *Middle*", "Places text with equidistance above and below, left and right of text as defined by text box", "X", ""
    "Insert symbol", "", "X", "X"
    "Insert Unicode - Page", "Select unicode page to select character from", "X", "X"
    "Insert Unicode - Char", "Select character to insert into text", "X", "X"
    "Insert Unicode **Insert** button", "Click button to insert iunicode character into text input field", "X", "X"


.. table::
    :widths: 30, 50, 10, 10
+------------------------+------------------------------------------------+-------+-------+
| Option                 | Description                                    | Text  | MText |
+========================+================================================+=======+=======+
| **Font Settings**                                                                       |
+------------------------+------------------------------------------------+-------+-------+
| - Font                 | Select font for text                           |   X   |   X   |
+------------------------+------------------------------------------------+-------+-------+
| - Height               | Set font height                                |   X   |   X   |
+------------------------+------------------------------------------------+-------+-------+
| - Angle                | Places text at specified :ref:`angle <angles>` |   X   |   X   |
+------------------------+------------------------------------------------+-------+-------+
| - Oblique              | *Inactive*                                     |   X   |   X   |
+------------------------+------------------------------------------------+-------+-------+
| - Width factor         |                                                |   X   |   X   |
+------------------------+------------------------------------------------+-------+-------+
| - Default line spacing | Use default line spacing for specified font    |   X   |   X   |
+------------------------+------------------------------------------------+-------+-------+
| - Line spacing         |                                                |   X   |   X   |
+------------------------+------------------------------------------------+-------+-------+
| **Alignment**                                                                           | 
+------------------------+------------------------------------------------+-------+-------+
|                        | Place text aligned to *handle*:                |       |       |
|                        |                                                |       |       |
|                        | - top, left/center/right                       |  X \| |   X   |
|                        | - middle, left/center/right                    |   X   |   X   |
|                        | - baseline, left/center/right                  |   X   |       |
|                        | - bottom, left/center/right                    |   X   |   X   |
+------------------------+------------------------------------------------+-------+-------+
| - *Fit*                | Places text between specified points while     |   X   |   X   |
|                        | maintaining set height                         |       |       |
+------------------------+------------------------------------------------+-------+-------+
| - *Aligned*            | Places text between specified points while     |   X   |   X   |
|                        | maintaining width to height ratio (scales text)|       |       |
+------------------------+------------------------------------------------+-------+-------+
| - *Middle*             | Places text with equidistance above and below, |   X   |   X   |
|                        | left and right of text as defined by text box  |       |       |
+------------------------+------------------------------------------------+-------+-------+
| Insert symbol          | Insert predefined symbol (Diameter, Degree,    |   X   |   X   |
|                        | Plus / Minus, At, Hash, Dollar, Copyright,     |       |       |
|                        | Registered, Paragraph, Pi, Pound, Yen, Times,  |       |       |
|                        | Division)                                      |       |       |
+------------------------+------------------------------------------------+-------+-------+
| **Insert Unicode**                                                                      |
+------------------------+------------------------------------------------+-------+-------+
| - Page                 | Select unicode page to select character from   |   X   |   X   |
+------------------------+------------------------------------------------+-------+-------+
| - Char                 | Select character to insert into text           |   X   |   X   |
+------------------------+------------------------------------------------+-------+-------+
| - **Insert** button    | Click button to insert unicode character into  |   X   |   X   |
|                        | text input field                               |       |       |
+------------------------+------------------------------------------------+-------+-------+

