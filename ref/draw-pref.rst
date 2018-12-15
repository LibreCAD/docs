.. _draw-pref:


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

Set the **Main drawing unit** to the prefered unit of measure to over-ride the default established during LibreCAD's :ref:`initial application configuration <configure>`.  The same units of measures are as noted in the :ref:`appendix <measurements>` are available for the drawing's preferences.

In addition the length and angle formats and precision can be set to suit the type of drawing.  Depnding on the format used, decimal or fractional, the precision is 

|
|
|
|
|

Length Format
~~~~~~~~~~~~~

.. csv-table:: 
   :header: "Format", "Example", "Maximum Precision", "Description"
   :widths: 30, 30, 30, 60
   
    "**Scientific**", "1.44311E+1", "0.00000000E+1", "Significand x 10 :superscript:`n`"
    "**Decimal**", "14.43112", "0.00000000",  "Integer part seperated from the fractional part of a number by a decimal"
    "**Engineering**", "1'-2.43112'' ", "0'-0.00000000'' ",  "Feet and decimal inches"
    "**Architectural**", "1'-2 7/16'' ", "0'-0 1/128'' ",  "Feet and fractional inches"
    "**Fractional**", "14 7/16'' ", "1/128'' ", "Fractional inches"
    "**Architectural (metric)**", "14.43112 :superscript:`5`", "0.00000000",  "Decimal metric units (mm, cm, etc...)"


Angle Format
~~~~~~~~~~~~

.. csv-table:: 
   :header: "Format", "Example", "Maximum Precision", "Description"
   :widths: 30, 30, 30, 60

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

Dimensions
----------

.. figure:: /images/drawPref4.png
    :width: 785px
    :height: 623px
    :align: right
    :scale: 50
    :alt: LibreCAD Drawing Preferences - Dimensions

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


Splines
-------

.. figure:: /images/drawPref5.png
    :width: 785px
    :height: 623px
    :align: right
    :scale: 50
    :alt: LibreCAD Drawing Preferences - Splines

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

