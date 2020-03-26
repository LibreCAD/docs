.. User Manual, LibreCAD v2.2.x

.. Default include
.. include:: /inclFiles/notice.rst


.. _draw-prefs:

Drawing Preferences
===================

Drawing preferences have two purposes, they allow users to :
    1. override the application defaults on a drawing by drawing basis.
    2. define specifics for the drawing's output, format and other drawing specific configuration.

The preferences can be configured by selecting **Options -> Current Drawing Preferences**.  There are five tabs for managing the drawing preferences: *Paper*, *Units*, *Grid*, *Dimensions* and *Splines*.


Paper
-----

.. only:: html

	.. figure:: /images/drawPref1.png
		:align: right
		:scale: 40
		:alt: LibreCAD Drawing Preferences - Paper

.. only:: latex

	.. figure:: /images/drawPref1.png
		:align: center
		:scale: 40
		:alt: LibreCAD Drawing Preferences - Paper

.. actual image size 785px x 623px

The *Paper* tab is used to define the size, orientation and margins of the page used when generating output.  The output can be as a physical printed page or an electronic form such as a PDF.  Layout of the page with specified settings may be checked in Preview section.  The paper format is also used when previewing a drawing (**File -> Print Preview**).

To be able to generate output, users must select a paper size and orientation.  Paper sizes include ISO, ANSI and other sizes.  Sizes of the select page are shown in the current unit of measurement.  Custom sizes can also be select by choosing *Custom* from the drop-down box and specifying the paper width and height.

Orientation can be selected for any page size and is either *Landscape* (long edge horizontal) or *Portrait* (long edge vertical).

Margins determine the printable area of a page.  Specified fields at the edges of the page are marked with gray color and always stay empty on the output.

If tiled printing is used to output the drawing, use *Number of pages* section to set a horizontal and a vertical number of pages.  For more details about the tiled printing see :ref:`Printing Guide <complete&print>`.

.. Force end of left / right text wrap
.. include:: /inclFiles/eoWrap.rst

Units
-----

.. only:: html

	.. figure:: /images/drawPref2.png
		:align: right
		:scale: 40
		:alt: LibreCAD Drawing Preferences - Units

.. only:: latex

	.. figure:: /images/drawPref2.png
		:align: center
		:scale: 40
		:alt: LibreCAD Drawing Preferences - Units

.. actual image size 785px x 623px


The **Units** tab allows users to set the *Main drawing unit* to the preferred unit of measure and the format of linear and angular dimensions.  The "Main Unit" setting overrides the default set during LibreCAD's initial application :ref:`configuration <configure>`.  The same units of measures are as noted in the :ref:`appendix <measurements>` are available for the drawing's preferences.

.. Force end of left / right text wrap
.. include:: /inclFiles/eoWrap.rst

.. note::

   These preferences format the display of linear and angular units on the *status bar*.  They *do not* affect the appearance of dimensions in the drawing.  See :ref:`Dimensions <dimn-prefs>` below for configuring dimensions' format.

.. Force end of left / right text wrap
.. include:: /inclFiles/eoWrap.rst


Length Format
~~~~~~~~~~~~~

.. csv-table:: 
    :widths: 15, 15, 15, 55
    :header-rows: 1
    :stub-columns: 0
    :class: table-fix-width
   
    "Format", "Example", "Maximum Precision", "Description"
    "**Scientific**", "1.44311E+1", "0.00000000E+1", "Significant x 10 :superscript:`n`"
    "**Decimal**", "14.43112", "0.00000000",  "Integer part separated from the fractional part of a number by a decimal"
    "**Engineering**", "1'-2.43112'' ", "0'-0.00000000'' ",  "Feet and decimal inches"
    "**Architectural**", "1'-2 7/16'' ", "0'-0 1/128'' ",  "Feet and fractional inches"
    "**Fractional**", "14 7/16'' ", "1/128'' ", "Fractional inches"
    "**Architectural (metric)**", "14.43112 :sup:`5`", "0.00000000",  "Decimal metric units (mm, cm, etc...)"

.. sup = superscript

.. Force end of left / right text wrap
.. include:: /inclFiles/eoWrap.rst


Angle Format
~~~~~~~~~~~~

.. csv-table:: 
    :widths: 15, 15, 15, 55
    :header-rows: 1
    :stub-columns: 0
    :class: table-fix-width

    "Format", "Example", "Maximum Precision", "Description"
	"**Decimal Degrees**", "30.5 |deg|", "0.00000000", "Integer part separated from the fractional part of a number by a decimal"
	"**Deg/Min/Sec**", "30 |deg| 32' 0'' ", "0 |deg| 00' 00.0000'' ", "Degrees [ |deg| ] / Minutes ( ', 1/60 of a degree) / Seconds ( '', 1/60 of a minute)"
	"**Gradians**", "33.9g", "0.00000000g", "1/100 of a right angle"
	"**Radians**", "0.5r", "0.00000000r", "SI unit of measure where the arc of a circle is measured by the length of the radius"
	"**Surveyor's units**", "N30d32'E", "N0d00'00.0000''E", "Cardinal directions measure in deg/min/sec from North and East"

.. Force end of left / right text wrap
.. include:: /inclFiles/eoWrap.rst

Grid
----

.. only:: html

	.. figure:: /images/drawPref3.png
		:align: right
		:scale: 40
		:alt: LibreCAD Drawing Preferences - Grid

.. only:: latex

	.. figure:: /images/drawPref3.png
		:align: center
		:scale: 40
		:alt: LibreCAD Drawing Preferences - Grid

.. actual image size 785px x 623px

The grid provides an evenly spaced guides to assist with placing entities.  When used with :ref:`snaps <snaps>` place can be precise.  The **Grid** tab has the following options:

    - *Show Grid*: Toggles the grid markers between visible or not visible. The grid can also be toggled with [Ctrl]-g or by using the grid button of the :ref:`view <view>` toolbar.  This setting does not affect the use of "Snap to Grid".
    - Grid X and Y Spacing: Sets the minimum frequency of the grid markers.  Values can be selected from the drop-down box.  Other values can be typed directly into the text box.  *Auto* sets the frequency of markers to a spacing suitable to the current zoom level.
    - *Orthogonal* or *Isometric Grid*: Selects the grid to use.  *Orthogonal* place the grid at right angles to the X and Y axis.  *Isometric* places the grid at 120 |deg| intervals for guiding :ref:`isometric drawings <isometric>`.
    - Cross-hair: Toggles the orientation of the cross-hairs (right, left, or top) when used with *Isometric Snap indicator lines* (see :ref:`Application Preferences <app-prefs>`).

.. Force end of left / right text wrap
.. include:: /inclFiles/eoWrap.rst

.. _dimn-prefs:

Dimensions
----------

.. only:: html

	.. figure:: /images/drawPref4.png
		:align: right
		:scale: 40
		:alt: LibreCAD Drawing Preferences - Dimensions

.. only:: latex

	.. figure:: /images/drawPref4.png
		:align: center
		:scale: 40
		:alt: LibreCAD Drawing Preferences - Dimensions

.. actual image size 785px x 623px

The dimension preferences affect how dimensions appear on the drawings.  Settings include:

    - General scale: 
    - Text & position: 
    - Extension lines: 
    - Dimension lines, arrows & ticks:
    - Format units: setting for linear and angular dimensions.  These settings are independent of the preference defined in the :ref:`Drawing Prefences <draw-prefs>`.

.. table::
    :widths: 30, 70
    :class: table-fix-width

    +-----------------------------+-------------------------------------------------------------------+
    | Setting                     | Description                                                       |
    +=============================+===================================================================+
    | General Scale               | Adjusts the *sizes* of the text and arrows by the factor          |
    |                             | provided.                                                         |
    +-----------------------------+-------------------------------------------------------------------+
    | **Text size & position**                                                                        |
    +-----------------------------+-------------------------------------------------------------------+
    | Length factor               | Adjusts the *dimension value* by the factor provided.  The        |
    |                             | entity remains the length as drawn.                               |
    +-----------------------------+-------------------------------------------------------------------+
    | Text Style                  | Sets the :ref:`font <fonts>` used for dimension text.             |
    +-----------------------------+-------------------------------------------------------------------+
    | Text Height                 | Sets the text height, measured in the  units defined on the       |
    |                             | *Units* tab.                                                      |
    +-----------------------------+-------------------------------------------------------------------+
    | Text alignment              | Aligns the text parallel and offset to the dimension line or      |
    |                             | horizontal centered on the dimension line.                        |
    +-----------------------------+-------------------------------------------------------------------+
    | Dimension line gap          | Sets the space between the dimension line and the dimension text. |
    +-----------------------------+-------------------------------------------------------------------+
    | Color                       | Set the color of the dimension lines and text.                    |
    +-----------------------------+-------------------------------------------------------------------+
    | **Extension lines**                                                                             |
    +-----------------------------+-------------------------------------------------------------------+
    | Offset                      | Gap between entity and dimension extension line.                  |
    +-----------------------------+-------------------------------------------------------------------+
    | Enlarge                     | Length of extension line beyond dimension line.                   |
    +-----------------------------+-------------------------------------------------------------------+
    | Fixed length                | Fixed length of extension line measured from the dimension line   |
    |                             | towards the dimensioned entity.                                   |
    +-----------------------------+-------------------------------------------------------------------+
    | Color                       | Extension line color, independent of layer settings.              |
    +-----------------------------+-------------------------------------------------------------------+
    | Width                       | Extension line width, independent of layer settings.              |
    +-----------------------------+-------------------------------------------------------------------+
    | **Dimension lines, arrows and ticks**                                                           |
    +-----------------------------+-------------------------------------------------------------------+
    | Arrow size                  | Length of dimension (and leader) arrow.                           |
    +-----------------------------+-------------------------------------------------------------------+
    | Tick size                   | Length of dimension tick to from end of dimension line in each    |
    |                             | direction, e.g. a length of 1 will result in a total length of 2  |
    |                             | units. (Anything greater than ''0'' will result in a *tick*       |
    |                             | instead of a dimension *arrow*).                                  |
    +-----------------------------+-------------------------------------------------------------------+
    | Color                       | Tick line color, independent of layer settings.                   |
    +-----------------------------+-------------------------------------------------------------------+
    | Width                       | Tick line width, independent of layer settings.                   |
    +-----------------------------+-------------------------------------------------------------------+
    | **Format units**                                                                                |
    +-----------------------------+-------------------------------------------------------------------+
    | Linear units                | (See *Length Format* under **Units** above.)                      |
    +-----------------------------+-------------------------------------------------------------------+
    | Linear precision            | (See *Length Format* under **Units** above.)                      |
    +-----------------------------+-------------------------------------------------------------------+
    | Linear zeros                | Remove leading, trailing, 0' and / or 0'' from linear dimensions. |
    +-----------------------------+-------------------------------------------------------------------+
    | Decimal separators          | Set the decimal separator to a period [.], or comma [,].          |
    +-----------------------------+-------------------------------------------------------------------+
    | Angular units               | (See *Length Format* under **Units** above.)                      |
    +-----------------------------+-------------------------------------------------------------------+
    | Angular precision           | (See *Length Format* under **Units** above.)                      |
    +-----------------------------+-------------------------------------------------------------------+
    | Angular zeros               | Remove leading or trailing zeros from angular dimensions.         |
    +-----------------------------+-------------------------------------------------------------------+


Splines
-------

.. only:: html

	.. figure:: /images/drawPref5.png
		:align: right
		:scale: 40
		:alt: LibreCAD Drawing Preferences - Splines

.. only:: latex

	.. figure:: /images/drawPref5.png
		:align: center
		:scale: 40
		:alt: LibreCAD Drawing Preferences - Splines

.. actual image size 785px x 623px

The single parameter *Number of line segments per spline patch* affects the 'smoothness' of a spline.  The greater the value, the 'smoother' the spline will be drawn.

.. Force end of left / right text wrap
.. include:: /inclFiles/eoWrap.rst


.. Symbols

.. |deg| unicode:: U+00B0

