.. User Manual, LibreCAD v2.2.x

.. Default include
.. include:: /inclFiles/notice.rst


.. _annotate:

Annotating a Drawing
====================

A drawing in and of itself provides an image of what the object might look like, but it doesn’t provide a complete description of the object. Knowing the size of the object is also very important.  The size of the drawn object is shown with measurements, *dimensioning*, and other textual information to describe the drawn object.  Together, dimensions and text is called *annotating* a drawing.

Dimensioning an object on a drawing provides the information necessary to be able to interpret the object and ultimately create it, whether it be a building or a *doohickey*.  Other textual information in the form of notes, symbols, call-outs, etc. provide further details for the object drawn.


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

.. csv-table:: 
    :widths: 15, 65
    :align: center
    :header-rows: 1
    :stub-columns: 0
    :class: table-fix-width

    "Type", "Description"
    "Aligned", "Places the dimension parallel to a line between the two endpoints of the dimension."
    "Linear", "Dimension between two points from any angle of interest.  The default is 0 (horizontal) and is changed via **Tool Options** toolbar."
    "Horizontal", "Horizontal Dimension between two points."
    "Vertical", "Vertical Dimension between two points."
    "Radial", "Radius of an arc."
    "Diametric", "Diameter of a circle."
    "Angular", "Angle between two lines or linear parts of objects."
    "Leader", "Not a dimension per se, but used for notes in drawings."

Complete descriptions of the :ref:`dimensioning tools and related options <tool-dimension>` are found in **Drawing Tools** of the **Reference** section.

Dimensioning Appearance
~~~~~~~~~~~~~~~~~~~~~~~

A dimension consists of several parts:

.. figure:: /images/dimnPrefDesc.png
    :align: center
    :scale: 67
    :alt: Dimension parts

.. actual image size 768px x 288px

The appearance of the dimensions are configured in the :ref:`Dimensions <dimn-prefs>` tab in the **Drawing Preferences**.  As with many other aspects of a :ref:`drawing's setup <drawing-setup>`, there are some generally accepted values for dimensioning:

.. csv-table:: 
    :widths: 35, 20, 20, 25
    :align: center
    :header-rows: 1
    :stub-columns: 0
    :class: table-fix-width

    "Dimension Component", "mm", "Decimal Inch", "Fractional Inch"
    "Dimension text height", "2.5", ".100", "3/32"
    "Dimension line gap", "1.5", ".0625", "1/16"
    "Extension line - Offset", "1.5", ".0625", "1/16"
    "Extension line - Enlarge", "3", ".125", "1/8"
    "Arrow size", "3", ".125", "1/8"

.. _adjust-dim:

.. admonition:: Note - Adjusting Dimensions for Printing

    The size of each dimension component: "Text Height", "Arrow size", etc. should be set to the desired "real world" size in the configuration.  That is to say if the desired text height is 2.5 mm when printed, the "Text Height" should remain set as 2.5 mm.  If the drawing is printed full scale (1:1) the dimension text will appear correctly.  However if the drawing is scaled up or down the "General Scale" needs to be adjusted accordingly.  The "General Scale" is set to the *inverse* of the printing scale.  For example, if the printed scale is determined to be 1:4, the "General Scale" should be set to 4 (4:1).

    The minimum spacing between dimension lines needs to be scaled with the drawing.  For example, if the drawing is 1:10, the spacing will need to be adjusted to 60 mm between dimension lines and 100 mm from the entity.

    Additional information can be found in the :ref:`Drawing Setup <drawing-setup>` and :ref:`Printing <complete&print>` guides.


.. admonition:: Tip - Rules for Dimensioning

    A few rules will help to ensure dimensions are accurate, legible and complete:

        - There should be only one way to interpret any one dimension.
        - Dimension and extension lines should not cross.
        - Extension lines and entity lines should not overlap.
        - Provide space between dimensions to ensure legibility.
        - The view that best shows an entity is the view that should be dimensioned.
        - Each entity on the drawing should be dimensioned and dimensioned only once.
        - There should be no need to calculate or scale a dimension of an entity.
        - A dimension should be referenced to a logical origin point.
        - When there are multiple lines of dimensions, the longer dimensions are to be placed outside of shorter ones.
        - Except for large circles and arcs, all dimensions should be placed outside the part and spaced 10mm / 3/8" from the entity.
        - Dimension circles with diameters and arcs with radiuses.
        - Center lines or center marks should be used on all circles and arcs.
        - Extended a circle's or arc's center lines and use as extensions line when possible.
        - Multiple lines of dimensions are spaced uniformly with a minimum of 6mm / 1/4” between dimension lines (see note above).
        - Use arrow heads or slash marks at the end of the dimension lines.

    To improve legiblity, make corrections, or make adjustments after scaling a drawing, dimension labels, dimension lines and extension lines can be repositioned using :ref:`Entity Handles <entity-handles>`.

    Dimensioning drawings is beyond the scope of the **LibreCAD User Manual**, but additional resources and examples are available in LibreCAD's `wiki <https://dokuwiki.librecad.org/>`_ or elsewhere on the web.

    **Dimensioning Example**
    
    .. image:: /images/doohickeyDimnEg.png
        :align: center
        :scale: 100
        :alt: Dimensioning example
    .. actual image size 800px x 366px


Leaders
-------

While leaders do not dimension an entity, they are closely related to dimensioning as they are important for annotating and adding clarity to entities.  Leaders provide the ability to place pointers to identify a specific area of interest when adding a note and linking it to a particulate object.  Leaders take their settings from the :ref:`dimension settings <dimn-prefs>` in **Drawing Preferences**.

.. figure:: /images/leaderEg.png
    :align: center
    :scale: 50
    :alt: Leader example

.. actual image size 768px x 324px


.. _text:

Text
----

Adding text to a drawing provides addition information; build notes, drawing title and related details, and so forth.  Text can be added using either of the two types of text tools:

.. table::
   :align: center
   :widths: auto
   :class: table-no-borders
   
   +-----------------------+-----+-----------------------+
   | "Text":               |     | "MText" (multi-line): |
   | |01Ltext|             |     | |01Rtext|             |
   +-----------------------+-----+-----------------------+

.. |01Ltext| image:: /images/textText.png
    :scale: 50
    :alt: Text dialogue
.. actual image size 557px x 462px

.. |01Rtext| image:: /images/textMText.png
    :scale: 50
    :alt: MText (multi-line) dialogue
.. actual image size 621px x 475px

Both tools proved several options for the appearance and placement of text, however a couple are unique to the single-line **Text** tool as shown below:

.. table::
    :widths: 30, 50, 10, 10
    :class: table-fix-width

    +------------------------+----------------------------------------------------------+-------+-------+
    | Option                 | Description                                              | Text  | MText |
    +========================+==========================================================+=======+=======+
    | **Font Settings:**                                                                                |
    +------------------------+----------------------------------------------------------+-------+-------+
    | - Font                 | Select font for text                                     |   X   |   X   |
    +------------------------+----------------------------------------------------------+-------+-------+
    | - Height               | Set font height                                          |   X   |   X   |
    +------------------------+----------------------------------------------------------+-------+-------+
    | - Angle                | Places text at specified :ref:`angle <angles>`           |   X   |   X   |
    +------------------------+----------------------------------------------------------+-------+-------+
    | - Oblique              | *Inactive*                                               |   X   |   X   |
    +------------------------+----------------------------------------------------------+-------+-------+
    | - Width factor         |                                                          |   X   |   X   |
    +------------------------+----------------------------------------------------------+-------+-------+
    | - Default line spacing | Use default line spacing for specified font              |   X   |   X   |
    +------------------------+----------------------------------------------------------+-------+-------+
    | - Line spacing         |                                                          |   X   |   X   |
    +------------------------+----------------------------------------------------------+-------+-------+
    | **Alignment:**                                                                                    | 
    +------------------------+----------------------------------------------------------+-------+-------+
    |                        | Place text aligned to *handle*:                          | |     | |     |
    |                        |                                                          |       |       |
    |                        | - top, left/center/right                                 | | X   | | X   |
    |                        | - middle, left/center/right                              | | X   | | X   |
    |                        | - baseline, left/center/right                            | | X   |       |
    |                        | - bottom, left/center/right                              | | X   | | X   |
    +------------------------+----------------------------------------------------------+-------+-------+
    | - *Fit*                | | Places text between specified points while             |   X   |   X   |
    |                        | | maintaining set height                                 |       |       |
    +------------------------+----------------------------------------------------------+-------+-------+
    | - *Aligned*            | | Places text between specified points while             |   X   |   X   |
    |                        | | maintaining width to height ratio (scales text)        |       |       |
    +------------------------+----------------------------------------------------------+-------+-------+
    | - *Middle*             | | Places text with equidistant above and below, left and |   X   |   X   |
    |                        | | right of text as defined by text box                   |       |       |
    +------------------------+----------------------------------------------------------+-------+-------+
    | Insert symbol          | | Insert predefined symbol (Diameter, Degree, Plus /     |   X   |   X   |
    |                        | | Minus, At, Hash, Dollar, Copyright, Registered,        |       |       |
    |                        | | Paragraph, Pi, Pound, Yen, Times, Division)            |       |       |
    +------------------------+----------------------------------------------------------+-------+-------+
    | **Insert Unicode:**                                                                               |
    +------------------------+----------------------------------------------------------+-------+-------+
    | - Page                 | Select Unicode page to select character from             |   X   |   X   |
    +------------------------+----------------------------------------------------------+-------+-------+
    | - Char                 | Select character to insert into text                     |   X   |   X   |
    +------------------------+----------------------------------------------------------+-------+-------+
    | - **Insert** button    | | Click button to insert Unicode character into text     |   X   |   X   |
    |                        | | input field                                            |       |       |
    +------------------------+----------------------------------------------------------+-------+-------+
    | **Icons:**                                                                                        |
    +------------------------+----------------------------------------------------------+-------+-------+
    | - Clear text           | Clear text field   |i01|                                 |   X   |   X   |
    +------------------------+----------------------------------------------------------+-------+-------+
    | - Load Text From File  | | Select text file and insert contents into field |i02|  |   X   |   X   |
    +------------------------+----------------------------------------------------------+-------+-------+
    | - Save Text To File    | Save text in text field to file   |i03|                  |   X   |   X   |
    +------------------------+----------------------------------------------------------+-------+-------+
    | - Edit                 | Cut  |i04| / Copy  |i05| / Paste  |i06|                  |   X   |   X   |
    +------------------------+----------------------------------------------------------+-------+-------+


..  Icon mapping:

.. |i00| image:: /images/icons/librecad.png
            :height: 18
            :width: 18
.. |i01| image:: /images/icons/new.svg
            :height: 18
            :width: 18
.. |i02| image:: /images/icons/open.svg
            :height: 18
            :width: 18
.. |i03| image:: /images/icons/save.svg
            :height: 18
            :width: 18
.. |i04| image:: /images/icons/cut.svg
            :height: 18
            :width: 18
.. |i05| image:: /images/icons/copy.svg
            :height: 18
            :width: 18
.. |i06| image:: /images/icons/paste.svg
            :height: 18
            :width: 18
