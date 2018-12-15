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

Use **Main drawing unit** to over-ride the default established during LibreCAD's :ref:`initial application configuration <configure>`.  The same units of measure as nmoted in the :ref:`appendix <measurements>` are available for the drawing's preferences.

|
|
|

Length Format:

.. csv-table:: 
   :header: "Format","Example","Description"
   :widths: 30, 30, 90
   
    "**Scientific**", "1.44311E+1", "Significand x 10 :superscript:`n`"
    "**Decimal**", "14.43112", "Integer part seperated from the fractional part of a number by a decimal"
    "**Engineering**", "1'-2.43112\" ", "Feet and decimal inches"

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


.. Symbols

.. |deg| unicode:: U+00B0

