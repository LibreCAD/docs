.. User Manual, LibreCAD v2.2.x

.. Default include
.. include:: /inclFiles/notice.rst


.. _annotate:

Annotating a Drawing
====================

A drawing in and of itself provides an image of what the object might look like, but it doesn’t provide a complete description of the object. Knowing how big the object is also very important, thus the need to provide the measurements and other textual information to describe the drawn object.  Together, dimensions and text is called *annotating* a drawing.

Dimensioning an object on a drawing provides the information necessary to be able to interpret the object and ultimately produce the it, whether it be a building or a widget.  Other textual information in the form of notes, call-outs, etc. provide further details for the drawn object.


.. _dimensioning:

Dimensioning
------------

Dimensions are used to define length, width, height, and/or angle of a line entity, the diameter of circle entity, or radius of arc entity.  A drawing's dimensions must be:

   - Accurate
   - Legible
   - Complete


Types of Dimensions
~~~~~~~~~~~~~~~~~~~
LibreCAD supports the following types of dimensions:

    - Aligned - parallel to a line
    - Linear - distance between two points from any angle of interest.  The default is 0 (horizontal) and is changed via "Properties" toolbar
    - Horizontal - horizontal distance between two points.
    - Vertical - vertical distance between two points.
    - Radial - radius of an arc.
    - Diametric - diameter of a circle.
    - Angular - angle between two lines or linear parts of objects.
    - Leader - not a dimension per se, but used for notes in drawings.

A dimension consists of several parts:

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
    :class: fix-table

    "Dimension Component", "mm", "Decimal Inch", "Fractional Inch"
    "Dimension text height", "2.5", ".100", "3/32"
    "Dimension line gap", "1.5", ".0625", "1/16"
    "Extension line - Offset", "1.5", ".0625", "1/16"
    "Extension line - Enlarge", "3", ".125", "1/8"
    "Arrow size", "3", ".125", "1/8"

.. note::
    The size of each dimension component: "Text Height", "Arrow size", etc. should be set to the desired "real world" size in the configuration.  That is to say if the desired text height is 2.5 mm when printed, the "Text Height" should remain set as 2.5 mm.  If the drawing is printed full scale (1:1) the dimension text will appear correctly.  However if the drawing is scaled up or down the "General Scale" needs to be adjusted accordingly.  The "General Scale" is set to the *inverse* of the printing scale.  For example, if the printed scale is determined to be 1:4, the "General Scale" should be set to 4 (4:1).

    Additional information can be found in the :ref:`Drawing Setup <drawing-setup>` and :ref:`Printing <printing-guide>` guides.


Rules for Dimensioning
~~~~~~~~~~~~~~~~~~~~~~

A few rules will help to ensure dimensions are accurate, legible and complete:

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

.. note::
   The minimum spacing between dimension lines needs to be scaled with the drawing.  For example, if the drawing is 1:10, the spacing will need to be adjusted to 60 mm between dimension lines and 100 mm from the entity.


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

While leaders do not dimension an entity, they are closely related to dimensioning as they are important for annotating and adding clarity to entities.  Leaders provide the ability to place pointers to identify a specific area of interest when adding a note and linking it to a particulate object.  Leaders take their settings from the :ref:`Dimensions <dimn-prefs>`.

.. figure:: /images/leaderEg.png
    :width: 748px
    :height: 278px
    :align: center
    :scale: 75
    :alt: Leader example


.. _text:

Text
----

Adding text to a drawing provides addition information; build notes, drawing title and related details, and so forth.  Text can be added using either of the two types of text tools:

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

|
|
|
|
|
|
|
|
|
|

Both tools proved several options for the appearance and placement of text, however a couple are unique to the single-line **Text** tool, as shown below:

.. table::
    :widths: 30, 50, 10, 10
    :class: table-fix-width

    +------------------------+------------------------------------------------+-------+-------+
    | Option                 | Description                                    | Text  | MText |
    +========================+================================================+=======+=======+
    | **Font Settings:**                                                                      |
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
    | **Alignment:**                                                                          | 
    +------------------------+------------------------------------------------+-------+-------+
    |                        | Place text aligned to *handle*:                | |     | |     |
    |                        |                                                | |     | |     |
    |                        | - top, left/center/right                       | | X   | | X   |
    |                        | - middle, left/center/right                    | | X   | | X   |
    |                        | - baseline, left/center/right                  | | X   |       |
    |                        | - bottom, left/center/right                    | | X   | | X   |
    +------------------------+------------------------------------------------+-------+-------+
    | - *Fit*                | | Places text between specified points while   |   X   |   X   |
    |                        | | maintaining set height                       |       |       |
    +------------------------+------------------------------------------------+-------+-------+
    | - *Aligned*            | | Places text between specified points while   |   X   |   X   |
    |                        | | maintaining width to height ratio (scales    |       |       |
    |                        | | text)                                        |       |       |
    +------------------------+------------------------------------------------+-------+-------+
    | - *Middle*             | | Places text with equidistant above and       |   X   |   X   |
    |                        | | below, left and right of text as defined by  |       |       |
    |                        | | text box                                     |       |       |
    +------------------------+------------------------------------------------+-------+-------+
    | Insert symbol          | | Insert predefined symbol (Diameter, Degree,  |   X   |   X   |
    |                        | | Plus / Minus, At, Hash, Dollar, Copyright,   |       |       |
    |                        | | Registered, Paragraph, Pi, Pound, Yen, Times,|       |       |
    |                        | | Division)                                    |       |       |
    +------------------------+------------------------------------------------+-------+-------+
    | **Insert Unicode:**                                                                     |
    +------------------------+------------------------------------------------+-------+-------+
    | - Page                 | Select Unicode page to select character from   |   X   |   X   |
    +------------------------+------------------------------------------------+-------+-------+
    | - Char                 | Select character to insert into text           |   X   |   X   |
    +------------------------+------------------------------------------------+-------+-------+
    | - **Insert** button    | | Click button to insert Unicode character     |   X   |   X   |
    |                        | | into text input field                        |       |       |
    +------------------------+------------------------------------------------+-------+-------+
    | **Icons:**                                                                              |
    +------------------------+------------------------------------------------+-------+-------+
    | - Clear text           | Clear text field   |i01|                       |   X   |   X   |
    +------------------------+------------------------------------------------+-------+-------+
    | - Load Text From File  | | Select text file and insert contents into    |   X   |   X   |
    |                        | | field   |i02|                                |       |       |
    +------------------------+------------------------------------------------+-------+-------+
    | - Save Text To File    | Save text in text field to file   |i03|        |   X   |   X   |
    +------------------------+------------------------------------------------+-------+-------+
    | - Edit                 | Cut  |i04| / Copy  |i05| / Paste  |i06|        |   X   |   X   |
    +------------------------+------------------------------------------------+-------+-------+


..  Icon mapping:

.. |i00| image:: /images/icons/librecad.png
            :height: 24
            :width: 24
.. |i01| image:: /images/icons/new.svg
            :height: 24
            :width: 24
.. |i02| image:: /images/icons/open.svg
            :height: 24
            :width: 24
.. |i03| image:: /images/icons/save.svg
            :height: 24
            :width: 24
.. |i04| image:: /images/icons/cut.svg
            :height: 24
            :width: 24
.. |i05| image:: /images/icons/copy.svg
            :height: 24
            :width: 24
.. |i06| image:: /images/icons/paste.svg
            :height: 24
            :width: 24
