.. User Manual, LibreCAD v2.2.x


.. _drawing-setup:

Setting up a Drawing
====================

As with other software; word processors, spreadsheets, etc, there are many ways a user can to setup or configure a new document.  With LibreCAD, that document is a drawing.  Some of the preferences for a drawing will be governed by drafting conventions, some will be determined by organizational requirements, and others might just be personal preferences.  The drawing's setup is largely determined by the :ref:`Drawing Preferences <draw-prefs>`.

Under normal circumstances, after the initial installation and :ref:`configuration <configure>`, little if any configuration needs to done to be able to *create* a new drawing.  During the initial setup, the default :ref:`unit of measure <measurements>` was set (defaulting to *millimeter*) and doesn't need to be changed.  The unit of measure should be set to the unit most frequently used as it is used for all new drawings.  If necessary, the default unit of measure can be changed in the :ref:`Application Preferences <app-prefs>` or overridden for a single drawing in the Drawing Preferences.

As noted, there are a many drawing parameters to be considered to suit the drawing requirements and final appearance.  The majority of these settings can be left as the defaults as LibreCAD's defaults reflect normal drafting conventions and practices, such as the "Text Height" of 2.5mm / .10" / 3/32", etc.  Other preferences and attributes, such as layer, line thickness and type, pen colors, etc. can also be changed to suit users' requirements.


Scale
-----

Setting the scale of a drawing is the easy part, drawings should be created **full-scale** (1:1)!  The zooming abilities of LibreCAD will make the whole drawing fit in the display window or zoom into the fine detail.  On the other hand, when producing output the drawing will need to be scaled to fit the "page".  Generally output is a printed page, but it can also be a pdf, or :ref:`exported to another image format <file>`.

While these two points seem contradict each other as a full-scale drawing of something very large, like a building, would require equally large text size for notes and dimensions when the drawing is scaled down to print on an "A1" page.  Trying to determine the text size for a large object would be tedious at best, but the features available in  LibreCAD makes it simple.  It is addressed by the "General Scale" on the *Dimensions* tab.

Two of the tabs, *Paper* and *Dimensions* require attention prior to generating output.  Specifically, the two parameters are:

    1. "Paper format" on the *Paper* tab: Selecting a paper size and orientation will determine the "print scale" used for final output.  The print scale also used to determine the "General Scale".
    2. "General Scale" on the *Dimensions* tab: The dimension text and related parameters can be adjusted to suit the output.

The "Paper format", e.g. paper size and orientation, to be used is an important to consideration when setting the drawing preferences.  The Paper Format is entirely up to the user to determine, based on what is available (depending on the printer or printing service that is being used).  While it can be done at anytime, determining the Paper Format sooner than later will help determine the "General Scale".  

.. Tip::
   Setting the General Scale *prior to dimensioning a drawing* will help determine the appropriate line spacing for dimensions.  See :ref:`Dimensioning <dimensioning>` for additional information.

Determining the General Scale parameter for the best results is simple, it is the *inverse* of the printing scale obtained prior to printing.  For example, if a print scale is determined to be "1:4", the General Scale is "4" (4:1).  Setting the General Scale to the inverse of the print scale results in the dimension text being the defined size, e.g. 2.5mm, on the printed drawing.  The drawing is scaled down to fit the page and the dimension text is scaled up to be legible.  See the :ref:`Printing Guide <printing-guide>` for details.


While any scale can be used when **printing** a drawing there are commonly used scales for different types of drawings.  Refer to  :ref:`Scales <scales>` in the appendix for some examples.


Using Layers
------------



.. _templates:

Templates
---------

Templates are *prototype* drawings that provide the means to save basic parameters and settings so a drawing does not have to be configured each time a new one is started.  The parameters and settings include the settings defined in the Drawing Preferences, such as the paper format, main unit of measure and format, and dimension format.  Templates can also include layers and layer configuration, line type and thickness, pen color, and other drawing elements such as a border. These settings are inherited by the drawings created from the template.

Templates are created by starting a new drawing, setting the desired :ref:`Drawing Preferences <draw-prefs>`, and adding any required drawing elements (e.g. layers, borders, etc).  Starting with a blank drawing in LibreCAD, select "Edit" from the menu bar and then "Current Drawing Preferences".  On the first tab labeled "Paper", set the paper size and orientation as desired.  Next, select the "Units" tab and set the options as desired.  Click the "Dimensions" tab and adjust the values as desired.  Check the remaining tabs and adjust those settings as necessary.  Click "OK" when done.  Add the layers and other drawing elements as required.  Refer to :ref:`Layers <layers>` for details on using layers and setting the attributes.

Once the template has been prepared, it can be saved to any location where the user has read / write permissons.

LibreCAD supports the use of multiple templates. A LibreCAD user that plans on creating similar drawings may require only one or two templates.  A user that plans on several different types of drawings may desire multiple templates.  For example, templates can be setup for each paper size available and / or for each paper orientation.

To use the newly created template, select "File" from the top menu bar and then select "New From Template" option. This will start a new drawing using the template drawing. Note that the new document is called "unnamed document" as any newly created drawing; it does not take the template name, only the template drawing contents.


Default Templates
~~~~~~~~~~~~~~~~~

When LibreCAD is first launched it creates a new drawing using a *default template*.  Further, when a new drawing is created within LibreCAD, either from the **File -> New** menu or when the "New" icon on the toolbar is clicked, the default template is used.  The default template can be either the template included with LibreCAD or a user-specified template.

When installing LibreCAD, a resource directory is created including, among other things, a default template named *empty.dxf*.  On MS Windows, the template is found in *C:\Program Files (x86)\LibreCAD\resources\library\templates\*.  

As an alternative to the LibreCAD provided template, a user-specified template can be configured in the :ref:`Application Preferences <app-prefs>` on the **Paths** tab.  The specified template is used instead of the default LibreCAD template when the application is launched and for new drawings.


..  Image mapping (no "align" allowed/required):

.. |image20| image:: /images/ltContinuous.png
             :width: 160
             :height: 20
             :scale: 100
             :alt: Continuous
.. |image21| image:: /images/ltDot.png
             :width: 160
             :height: 20
             :scale: 100
             :alt: Dot
.. |image22| image:: /images/ltDash.png
             :width: 160
             :height: 20
             :scale: 100
             :alt: Dash
.. |image23| image:: /images/ltDashDot.png
             :width: 160
             :height: 20
             :scale: 100
             :alt: Dash Dot
.. |image24| image:: /images/ltDivide.png
             :width: 160
             :height: 20
             :scale: 100
             :alt: Divide
.. |image25| image:: /images/ltCenter.png
             :width: 160
             :height: 20
             :scale: 100
             :alt: Center
.. |image26| image:: /images/ltBorder.png
             :width: 160
             :height: 20
             :scale: 100
             :alt: Border

