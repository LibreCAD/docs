.. User Manual, LibreCAD v2.2.x


.. _dimensioning:

Dimensioning
============

Dimensioning an object on a drawing provides the information necessary to be able to interpet the drawn object. Dimensioning must be:

   - Accurate
   - Legible
   - Complete

Dimensions are used to define length, width, height of a line entity, or the diameter of circle entity or radius of arc entity.  Types of dimensioning include:

   - Linear
   - Aligned
   - Vertical and horizontal
   - Angular
   - Radius / Diameter
   - Reference


Other than "Reference", each of the type of dimension have a corresponding dimension :ref:`tool <tools>`.  A reference dimension can be of any type, but not used to to define an entity.  It might be for information purposes only or  an accumulation of other dimensions, etc.  The text for a reference dimension is typically enclosed in parentheses ().

A dimension consists of a few parts:

.. figure:: /images/dimnDesc.png
    :width: 1441px
    :height: 504px
    :align: right
    :scale: 50
    :alt: Dimension parts

Dimension Defaults

.. csv-table:: 
   :widths: 55, 15, 15, 15
   :width: 80

    "Dimension Component", "mm", "Decimal Inch", "Fractional Inch"
    "Dimension text height", "2.5", ".100", "3/32"
    "Dimension line gap", "1.5", ".0625", "1/16"
    "Arrow head", "3", ".125", "1/8"
    "Extension line - Enlarge", "3", ".125", "1/8"
    "Extension line - Offset", "1.5", ".0625", "1/16"


Refer to :ref:`Dimensions <dimn-prefs>` in the **Drawing Preferences** in the reference section to change the dimensioning configuration.  The default values are acceptable for most drawings and reflect the generally accepted practices for drafting.  The value for the *General Scale* will need to be adjusted when generating a print.  Additional information can be found in the :ref:`Drawing Setup <drawing-setup>` and :ref:`Printing <printing-guide>` guides.


Rules for Dimensioning
----------------------

   - Dimensions must be clear, concise and complete.
   - Provide space between dimensions to ensure legibility.
   - There should be only one way to interprete any one dimension.
   - The view that best shows an entity is the view that should be dimensioned.
   - Each entity on the drawing should be dimensioned and dimensioned only once.
   - There is no need to calculate or scale a dimension of an entity.
   - A dimension should be referenced to a logical origin point.
   - When there are multiple lines of dimensions, the longer dimensions are to be placed outside of shorter ones.
   - Except for large circles and arcs, all dimensions should be placed outside the part and spaced 10mm / 3/8" from the entity.
   - Dimensioned circles diameters and arcs with radiuses.
   - Center lines or center marks should be used on all circles.
   - Extended center lines and use as the extension line when possible.
   - Multiple lines of dimensions are spaced uniformly with a minimum of 6mm / 1/4” between dimension lines.
   - Dimension and extension lines should not cross.
   - Extension lines and entity lines should not overlap.
   - Use arrow heads or slash marks at the end of the dimension lines.

