.. User Manual, LibreCAD v2.2.x


.. _drawing-setup:

Setting up a Drawing
====================

There are many, many ways to setup a drawing and establish the drawing preferences.  Some will be governed by generally accepted practices, some will be determined by organizational requirements, and others might just be personal preferences.  One particularly important consideration is the output, e.g. printed drawing, as the output destination will determine some of the preferences.

Under normal circumstances, after the initial installation and :ref:`configuration <configure>`, little if any configuration needs to done to be able to *start* a drawing.  During the initial setup, a default :ref:`unit of measure <measurements>` was set (defaulting to *millimeter*).  The default to the unit of measure should be set to the unit most frequently used as it is used for **all** new drawings.  If necessary, it can be changed in the :ref:`Application Preferences <app-prefs>` or over-ridden in the :ref:`Drawing Preferences <draw-prefs>`.


Determining Scale
-----------------

Setting the scale of a drawing is the easy part, drawings should be created **full-scale** (1:1)!  The zooming abilities of LibreCAD will make the drawing fit in the display window or zoom into the fine detail.   On the other hand, when producing output the drawing will need to be scaled to fit the "page".  Generally output is a printed page, but it can also be a pdf, or :ref:`exported to another image format <file>`.

These two points contradict each other as a full-scale drawing of something very large, like a building, would require equally large text size for notes and dimensions when the drawing is scaled down to print on an "A1" page.  Trying to determine the text size for a large object would be tedious at best, but the features within LibreCAD simplifies it tremendously.  This contradiction is addressed by the "General Scale" on the *Dimensions* tab when the drawing is ready to :ref:`print <printing-guide>`.


General Guidance
----------------

As stated above, there are a many drawing parameters that can be considered to suit the drawing requirements and fianl appearance.  These settings are found in the :ref:`Drawing Preferences <draw-prefs>`.  The majority of these settings can be left as the defaults as the defaults reflect generally accepted drafting standards, such as the "Text Height" of 2.5mm / .10" / 3/32".  Two of the tabs, *Paper* and *Dimensions* require particular attention.  The settings on these two tabs affect the output, and there are two parameters that are significant:

    1. "Paper format" on the *Paper* tab: Selecting a paper size and orientation will determine the "print scale" used for final output.  It also used to determine the "General Scale" (next).
    2. "General Scale" on the *Dimensions* tab: The dimension text and related parameters can be adjusted to suit the output.

The "Paper format", e.g. paper size and orientation, or media, to be used is important to consider when setting the drawing preferences.  While it can be done at anytime, determining the media sooner than later will be helpful as the size and orientation will help determine the "General Scale".  The media size is entirely up to the user to determine what is available, depending on the printer or printing service that is being used.

Determining the General Scale parameter for the best result is simple, it is the *inverse* of the printing scale obtained prior to printing.  For example, if a print scale is determined to be "1:4", the General Scale is "4" (4:1).  See the :ref:`Printing Guide <printing-guide>` for details.  Setting the General Scale to the inverse of the print scale results in the dimension text being the defined size, e.g. 2.5mm, of the printed drawing.



.. _pens:

Pens
----

    - Color - LibreCAD has 16 default colors, but supports the RGB color space (#000000 to #FFFFFF or 16,777,215 colors).  The initial color for entities is black.
    - Width - The default line width is 0.00mm.  Line widths supported are up to 2.11mm.
    - Line Type - The default line type is "Continuous" (e.g. solid).  Other line types included with LibreCAD are Dot, Dash, Divide, Center, and Border.

The pens properties can be defined by entity, by a group of selected entities (via the *Attribute* tool) or by layer.


.. _templates:

Templates
---------

Simply stated templates are nothing more than a simple drawing file that especially contain various settings and components that can be used repetitively. These settings can be as simple as the paper definition and unit specifications but can include layers, block devices and drawing elements like any other drawing. These settings are however limited to the drawing only. Template drawings are unable to alter application preferences or other global settings within LibreCAD.

LibreCAD supports the use of a default template and the use of multiple templates. A LibreCAD user that plans on creating similar drawings may require only a single template. A user that plans on several different types of drawings may desire multiple templates. LibreCAD will remember the last directory used when saving and opening a drawing file. So a convenient location for your templates are within your drawing folder location. This folder for drawings could be within your default Documents folder or a separate Drawings folder or a part of a Projects folder as you may desire. The idea here being to locate the drawings folder in an area where it is convenient to move freely back and forth from the storage locations. To use your current Documents folder would be convenient to include in a current backup schedule easily as well. Simply create a new folder called Drawings inside your current Documents folder. This location can be anywhere within your user permission level. Once a common area is created a template can be saved easily within the area or another folder for templates can be created as well to provide separation as desired for convenience. A LibreCAD user will also desire to create a folder for library symbols and blocks that is usually named "library". These should be created where the user has full write permission, probably inside their desired drawings folder. The path to this folder will be discussed near the end under the "Default Template" section below.

To create your first template start LibreCAD. Select "Edit" on the top menu bar and then select "Current Drawing Preferences". On the first tab labeled "Paper" please select paper size and page mode desired. Then select the "Units" tab and set the options as desired. Proceed through all the tabs and set or skip the settings as desired. Please note the settings so that you know where they are and can return to modify them as required in the future. Any changes here in the future will require the template to be updated again in order to maintain the new settings. Once completed click the OK button to save the changes.

You may create other settings as desired or create and label layers, etc. To save the current settings as a template click on the "File" menu option on the top menu bar and then select "Save" or "Save As". In the file dialog box please select your drawing folder and then enter a file name in the box directly below the folder contents. The file type should be "Drawing Exchange 2007". Click the "Save" button to save the file. If an existing file name is used then you will be prompted to replace the file.

To use the newly created template, select "File" from the top menu bar, then select "New From Template" option. This will start a new drawing using everything saved in the template drawing. Note, the new document is called "unnamed document"; it does not take the template name, only the template drawing contents. Change the new document as you like. When you save it, you will be prompted for a folder location and filename.


Default Template
~~~~~~~~~~~~~~~~

When LibreCAD is first executed it opens a default drawing. This drawing can be specified as a template in the "Application Preferences" under the "Paths" tab. Select "Edit" from the top menu bar and then "Application Preferences" followed by the "Paths" tab. The last field listed is the "template" field. This should contain the full path and filename of the desired template to use as a default. The drawing specified here as a template will be used from three locations. The first is when LibreCAD is first executed and the default drawing is created. The second is when "File->New" is selected. The third is wehn the icon on the toolbar for "New" is clicked. Each time it will create a new drawing document. Each of the new drawings can be selected from the "Window" option on the top menu bar if they have been created or any drawing that may have been opened.

In the "Paths" tab there are other file paths to be specified. The symbol or library folder location is called "Parts Library". This folder specification should contain the full path and name of the folder mentioned earlier in regard to parts libraries. The library folder can contain additional folders to categorize the items. For instance: floor plan, electric, electronic, landscape, flow diagram, plumbing, hardware, etc. The subfolders are required. LibreCAD does not provide a mechanism to use the library directory directly. A user could use it for template storage if they desired and then the templates could be used by the "New From Template" option or for the default template setting. The LibreCAD "Library Browser" will only present the created folders (and subfolders) with the drawings within the browser. 

