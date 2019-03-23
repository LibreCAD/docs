.. User Manual, LibreCAD v2.2.x


.. _drawing-setup:

Setting up a Drawing
====================

As with other software; word processors, spreadsheets, etc, there are many ways a user can to setup a new document.  With LibreCAD, that new document is a drawing.  The drawing's setup is largely determined by the :ref:`Drawing Preferences <draw-prefs>`.  Some preferences will be governed by drafting conventions, some will be determined by organizational requirements, and others might just be personal preferences.  However, one particularly important consideration is the output as it will determine some of the preferences, the most important of those being the page size of a printed drawing.

Under normal circumstances, after the initial installation and :ref:`configuration <configure>`, little if any configuration needs to done to be able to *create* a new drawing.  During the initial setup, the default :ref:`unit of measure <measurements>` was set (defaulting to *millimeter*) and doesn't need to be changed.  The unit of measure should be set to the unit most frequently used as it is used for **all** new drawings.  If necessary, the default can be changed in the :ref:`Application Preferences <app-prefs>` or overridden for a single drawing in the :ref:`Drawing Preferences <draw-prefs>`.

Other preferences and attributes, such as line thickness, layer, pen colors, etc. can be changed to suit users' requirements.


General Guidance
----------------

As noted above, there are a many drawing parameters that can be considered to suit the drawing requirements and final appearance.  The majority of these settings can be left as the defaults as the defaults reflect drafting conventions, such as the "Text Height" of 2.5mm / .10" / 3/32".  Two of the tabs, *Paper* and *Dimensions* require particular attention prior to generating output.  There are two parameters that are significant the two tabs:

    1. "Paper format" on the *Paper* tab: Selecting a paper size and orientation will determine the "print scale" used for final output.  It also used to determine the "General Scale" (next).
    2. "General Scale" on the *Dimensions* tab: The dimension text and related parameters can be adjusted to suit the output.

The "Paper format", e.g. paper size and orientation, or media, to be used is important to consider when setting the drawing preferences.  While it can be done at anytime, determining the media sooner than later will be helpful as the size and orientation will help determine the "General Scale".  The media size is entirely up to the user to determine what is available, depending on the printer or printing service that is being used.  More details can be founds in the :ref:`Printing Guides <printing>`.


Determining Scale
~~~~~~~~~~~~~~~~~

Setting the scale of a drawing is the easy part, drawings should be created **full-scale** (1:1)!  The zooming abilities of LibreCAD will make the whole drawing fit in the display window or zoom into the fine detail.   On the other hand, when producing output the drawing will need to be scaled to fit the "page".  Generally output is a printed page, but it can also be a pdf, or :ref:`exported to another image format <file>`.

These two points contradict each other as a full-scale drawing of something very large, like a building, would require equally large text size for notes and dimensions when the drawing is scaled down to print on an "A1" page.  Trying to determine the text size for a large object would be tedious at best, but the features within LibreCAD simplifies it.  It is addressed by the "General Scale" on the *Dimensions* tab.

Determining the General Scale parameter for the best result is simple, it is the *inverse* of the printing scale obtained prior to printing.  For example, if a print scale is determined to be "1:4", the General Scale is "4" (4:1).  See the :ref:`Printing Guide <printing-guide>` for details.  Setting the General Scale to the inverse of the print scale results in the dimension text being the defined size, e.g. 2.5mm, on the printed drawing.  The drawing is scaled down to fit the page and the dimension text is scaled up to be legible.

Normal defined scales are used 

:ref:`Dimensioning <dimensioning>`


.. _entity-attribute:

Line Attributes
===============

As with many other aspect of drafting, line color, thickness and type assigned to an entity, such as a line or circle are determined by drafting convention or common practices.  Within LibreCAD, the three attributes are grouped together as a "Pen":

    - Color - LibreCAD has 16 default colors, but supports the RGB color space (#000000 to #FFFFFF or 16,777,215 colors).  The initial color for entities is black.
    - Width - The default line width is 0.00mm.  Line widths of up to 2.11mm are supported.
    - Line Type - The default line type is "Continuous" (e.g. solid).  Other line types included with LibreCAD are Dot, Dash, Divide, Center, and Border.

The pen attributes can be defined for a single entity (via the *Properties* tool) , by a group of selected entities (via the *Attribute* tool), or by layer.


Line Type & Thickness
---------------------

Line thickness should also be addressed when creating a new drawing.  The default line thickness is 0.00mm and results in a hairline on a printed page.  General practices may vary by drawing type; technical, arcitectural, etc, and by drawing size; larger drawings utilize thicker lines.  A variety of sources can be found on the internet by searching for "CAD standards".  The following table provides suggested line widths for ISO A4/A3/A2 or ANSI A/B/C paper sizes:

.. csv-table:: 
   :header: "Line Weights", "Width Range", "Purpose", "Width"
   :widths: 20, 30, 60, 30

    "Extra Thin", "0.00 to 0.10 mm", "- Hidden lines", "0.00 mm"
    "", "", "- Hatching", ""
    "", "", "- Reference line", ""
    "Thin", "0.15 to 0.25 mm", "- Outlines", "0.18 mm"
    "", "", "- Centre lines", ""
    "", "", "- Dimension lines", ""
    "", "", "- Leader and extension", ""
    "", "", "- Phantom lines", ""
    "", "", "- Grid lines", ""
    "", "", "- Text", ""
    "Medium", "0.30 mm to 0.50 mm", "- Hidden lines", "0.35 mm"
    "", "", "- Text normal (0.3 mm)", ""
    "", "", "- Text - sub-headings (0.5 mm)", ""
    "", "", "- Visible object outlines", ""
    "Thick", "0.70 mm", "- Cutting lines", "0.70 mm"
    "", "", "- Match lines", ""
    "", "", "- Section lines", ""
    "", "", "- Text - titles/major headings", ""
    "", "", "- Viewing planes", ""
    "Extra Thick", "1.00 mm", "- Title sheet border", "1.00 mm"


.. _templates:

Templates
---------

Templates are *prototype* drawings that provide the means to save basic parameters and settings so a drawing does not have to be configured each time a new one is started.  The parameters and settings include the settings defined in the :ref:`Drawing Preferences <draw-prefs>`, such as the paper format, main unit of measure and format, and dimension format.  Templates can also include layers and layer configuration, line type and thickness, pen color, and other drawing elements such as a border. These settings are inherited by the drawings created from the template.

Templates are created by starting a new drawing, setting the desired :ref:`Drawing Preferences <draw-prefs>`, and adding any required drawing elements (e.g. layers, borders, etc).  Starting with a blank drawing in LibreCAD, select "Edit" from the menu bar and then "Current Drawing Preferences".  On the first tab labeled "Paper", set the paper size and orientation as desired.  Next, select the "Units" tab and set the options as desired.  Click the "Dimensions" tab and adjust the values as desired.  Check the remaining tabs and adjust those settings as necessary.  Click "OK" when done.  Add the layers and other drawing elements as required.  Refer to :ref:`Layers <layers>` for details on using layers and setting the attributes.

Once the template has been prepared, it can be saved to any location where the user has read / write permissons.

LibreCAD supports the use of multiple templates. A LibreCAD user that plans on creating similar drawings may require only one or two templates.  A user that plans on several different types of drawings may desire multiple templates.  For example, templates can be setup for each paper size available and / or for each paper orientation.

To use the newly created template, select "File" from the top menu bar and then select "New From Template" option. This will start a new drawing using the template drawing. Note that the new document is called "unnamed document" as any newly created drawing; it does not take the template name, only the template drawing contents.

**************
empty.dxf

Open the file ..\library\templates\empty.dxf
Set your preferred settings in Current Drawing Preferences and save the file.
Then, next time you open a new file, the settings are there.

empty.dxf is the default template, loaded when you start up LibreCAD.
Also, when you create a frame inside empty.dxf, you will always start with that.
You can have more templates e.g. for different paper size or orientation and use New From Template to open them. 

Replacing the default drawing on startup (and New) has been resolved by adding a real drawing name to the end of the path for the template directory.   I located this answer under the forum for CAD-templates-blocks.
James


Default Template
~~~~~~~~~~~~~~~~

When LibreCAD is first launched it opens a default drawing. This drawing can be specified as a template in the "Application Preferences" under the "Paths" tab. Select "Edit" from the top menu bar and then "Application Preferences" followed by the "Paths" tab. The last field listed is the "template" field. This should contain the full path and filename of the desired template to use as a default. The drawing specified here as a template will be used from three locations. The first is when LibreCAD is first executed and the default drawing is created. The second is when "File->New" is selected. The third is when the icon on the toolbar for "New" is clicked. Each time it will create a new drawing document. Each of the new drawings can be selected from the "Window" option on the top menu bar if they have been created or any drawing that may have been opened.

In the "Paths" tab there are other file paths to be specified. The symbol or library folder location is called "Parts Library". This folder specification should contain the full path and name of the folder mentioned earlier in regard to parts libraries. The library folder can contain additional folders to categorize the items. For instance: floor plan, electric, electronic, landscape, flow diagram, plumbing, hardware, etc. The subfolders are required. LibreCAD does not provide a mechanism to use the library directory directly. A user could use it for template storage if they desired and then the templates could be used by the "New From Template" option or for the default template setting. The LibreCAD "Library Browser" will only present the created folders (and subfolders) with the drawings within the browser.

