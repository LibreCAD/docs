.. User Manual, LibreCAD v2.2.x


.. _draw-prefs:

Drawing Preferences
===================

Drawing preferences two purposes, they allow users to :
    1. over-ride the application defaults on a drawing by drawing basis.
    2. define specifics for the drawing's ouput, format and other drawing specific configuration.

The preferences can be configured by selecting Options -> Current Drawing Preferences.  There are five tabs for managing the drawing preferences; Paper, Units, Grid, Dimensions and Splines.


Paper
-----

.. Text for describing images follow image directive.

.. figure:: /images/drawPref1.png
    :width: 785px
    :height: 623px
    :align: right
    :scale: 50
    :alt: LibreCAD Drawing Preferences - Paper

The paper tab is used to define the size and orientation of the page used when generating outpot.  The output can be as a physical printed page or a electronic form such as a PDF.  The paper format is also used when previewing a drawing (File -> Print Preview).

To be able to generate output, users must select a paper size and orientation.  Paper sizes include ISO, ANSI and other sizes.  Sizes of the select page are shown in the current unit of measurement.  Custom sizes can also be select by choosing "Custom" from the dropdown box and specifying the paper width and height.

Orientation can be selected for any page size and is either "Landscape" (long edge horizontal) or "Portrait" (long edge vertical).


Units
-----

.. figure:: /images/drawPref2.png
    :width: 785px
    :height: 623px
    :align: right
    :scale: 50
    :alt: LibreCAD Drawing Preferences - Units

The **Units** tab allows users to set the *Main drawing unit* to the prefered unit of measure.  The setting over-rides the default set during LibreCAD's initial application :ref:`configuration <configure>`.  The same units of measures are as noted in the :ref:`appendix <measurements>` are available for the drawing's preferences.

In addition, the Length and Angle formats and precision, as shown below, can be set to suit the type of drawing.

|

Length Format
~~~~~~~~~~~~~

.. csv-table:: 
   :header: "Format", "Example", "Maximum Precision", "Description"
   :widths: 15, 15, 15, 55
   
    "**Scientific**", "1.44311E+1", "0.00000000E+1", "Significand x 10 :superscript:`n`"
    "**Decimal**", "14.43112", "0.00000000",  "Integer part seperated from the fractional part of a number by a decimal"
    "**Engineering**", "1'-2.43112'' ", "0'-0.00000000'' ",  "Feet and decimal inches"
    "**Architectural**", "1'-2 7/16'' ", "0'-0 1/128'' ",  "Feet and fractional inches"
    "**Fractional**", "14 7/16'' ", "1/128'' ", "Fractional inches"
    "**Architectural (metric)**", "14.43112 :sup:`5`", "0.00000000",  "Decimal metric units (mm, cm, etc...)"

.. sup = superscript

Angle Format
~~~~~~~~~~~~

.. csv-table:: 
   :header: "Format", "Example", "Maximum Precision", "Description"
   :widths: 15, 15, 15, 55

	"**Decimal Degrees**", "30.5 |deg|", "0.00000000", "Integer part separated from the fractional part of a number by a decimal"
	"**Deg/Min/Sec**", "30 |deg| 32' 0'' ", "0 |deg| 00' 00.0000'' ", "Degrees [ |deg| ] / Minutes ( ', 1/60 of a degree) / Seconds ( '', 1/60 of a minute)"
	"**Gradians**", "33.9g", "0.00000000g", "1/100 of a right angle"
	"**Radians**", "0.5r", "0.00000000r", "SI unit of measure where the arc of a circle is measured by the length of the radius"
	"**Surveyor's units**", "N30d32'E", "N0d00'00.0000''E", "Cardinal directions measure in deg/min/sec from North and East"


Grid
----

.. figure:: /images/drawPref3.png
    :width: 785px
    :height: 623px
    :align: right
    :scale: 50
    :alt: LibreCAD Drawing Preferences - Grid

The grid provides an evenly spaced guides to assist with placing entities.  When used with :ref:`snaps <snaps>` place can be precise.  The **Grid** tab has the following options:

    - Show Grid: Toggles the grid markers between visible or not visible. The grid can also be toggled with [Ctrl]-g or by using the grid button of the :ref:'view <view>' toolbar.  This setting does not affect the use of "Snap to Grid".
    - Grid X and Y Spacing: Sets the minumum frequency of the grid markers.  Values can be selected from the dropdown box.  Other values can be typed directly into the text box.  "Auto" sets the frequency of markers to a spacing suitable to the current zoom level.
    - Orthogonal or Isometric Grid: Selects the grid to use.  *Orthogonal* place the grid at right angles to the X and Y axis.  *Isometric* places the markers at 30 |deg| to horizontal for guiding :ref:`isometric drawings <isometric>`.
    - Crosshair: Toggles the orientation of the crosshairs (right, left, or top) when used with *Isometric Snap indicator lines* (see :ref:`Application Preferences <app-prefs>`).


Dimensions
----------

.. figure:: /images/drawPref4.png
    :width: 785px
    :height: 623px
    :align: center
    :scale: 50
    :alt: LibreCAD Drawing Preferences - Dimensions


.. csv-table::
    :header: "Setting", "Description"
    :widths: 30, 70

    "General Scale", "Adjusts the **sizes** of the text and arrows by the factor provided."

.. csv-table:: **Text size & position**
    :header: "Setting", "Description"
    :widths: 30, 70

    "Length factor", "Adjusts the *dimension value* by the factor provided.  The entity remains the length as drawn."
    "Text Style", "Sets the :ref:`font <fonts>` used for dimension text."
    "Text Height", "Sets the text height, measured in the  units defined on the *Units* tab."
    "Text alignment", "Aligns the text parallel and offset to the dimension line or horizontal centered on the dimension line."
    "Dimension line gap", "Sets the space between the dimension line and the dimension text."
    "Color", "Set the color of the dimension lines and text."

.. csv-table:: **Extension lines**
    :header: "Setting", "Description"
    :widths: 30, 70

    "Offset", "Gap beetween entity and dimension extention line."
    "Enlarge", "Length of extention line beyond dimension line."
    "Fixed length", "Fixed length of extension line measured from the dimension line towards the dimensioned entity."
    "Color", "Extension line color, independent of layer settings."
    "Width", "Extension line width, independent of layer settings."

.. csv-table:: **Dimension lines, arrows and ticks**
    :header: "Setting", "Description"
    :widths: 30, 70

    "Arrow size", "Length of dimension (and leader) arrow."
    "Tick size", "Length of dimension tick to from end of dimension line in each direction, e.g. a length of 1 will result in a total length of 2 units. (Anything greater than ''0'' will result in a *tick* instead of a dimension *arrow*)."
    "Color", "Tick line color, independent of layer settings."
    "Width", "Tick line width, independent of layer settings."

.. csv-table:: **Format units**
    :header: "Setting", "Description"
    :widths: 30, 70

    "Linear units", "(See *Length Format* under **Units** above.)"
    "Linear precision", "(See *Length Format* under **Units** above.)"
    "Linear zeros", "Remove leading, trailing, 0' oand / or 0'' from linear dimensions."
    "Decimal separators", "Set the dDecimal separator to a period [.], or comma [,]."
    "Angular units", "(See *Length Format* under **Units** above.)"
    "Angular precision", "(See *Length Format* under **Units** above.)"
    "Angular zeros", "Remove leading or trailing zeros from angular dimensions."


Splines
-------

.. figure:: /images/drawPref5.png
    :width: 785px
    :height: 623px
    :align: right
    :scale: 50
    :alt: LibreCAD Drawing Preferences - Splines

The single parameter, "Number of line segments per spline patch", affects the 'smoothness' of a spline.  The greater the value, the 'smoother the spline will be drawn.

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
|
|


.. Symbols

.. |deg| unicode:: U+00B0

