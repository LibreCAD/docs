.. User Manual, LibreCAD v2.2.0

.. Default include
.. include:: /inclFiles/notice.rst


.. _drawing-setup:

Setting up a Drawing
====================

As with other software; word processors, spreadsheets, etc, there are many ways a user can to setup or configure preferences for a new document.  With LibreCAD, that document is a drawing.  Some of the preferences for a drawing will be governed by drafting conventions, some will be determined by organizational requirements, and others might just be personal preferences.  The drawing's configuration is largely determined by the :ref:`Drawing Preferences <draw-prefs>`.

Under normal circumstances, after the initial installation and configuration of LibreCAD, little if any additional configuration needs to done before creating a drawing. However, there are a many drawing parameters that can be changed to suit the user's requirements and the drawing’s final appearance. The majority of these settings can be left as the defaults as LibreCAD's defaults reflect normal drafting conventions and practices, such as the “Text Height” of 2.5 mm / .10” / 3/32”, etc. However, these and many other preferences and drawing elements, such as fonts, layer, line thickness and type, pen colors, etc. can be set to suit users’ requirements.

Some of the key considerations for setting up the drawing include:

    - Drawing units
    - Page size
    - Scale and dimensioning format
    - Layers and "pens"


Drawing Unit
------------

During the initial setup, the default :ref:`unit of measure <measurements>` was set (defaulting to *millimeter*).  The unit of measure should be set to the unit most frequently used as it is used for all new drawings and doesn't need to be changed.  If necessary, the default unit of measure can be changed in the :ref:`Application Preferences <app-prefs>` or overridden for a single drawing in the :ref:`Drawing Preferences <draw-prefs>`.


.. _ug-scale:

Scale and Dimensioning
----------------------

Setting the scale of a drawing is the easy part, drawings should be created *full-scale* (1:1)!  The zooming abilities of LibreCAD will make the whole drawing fit in the drawing window or magnify sections to view fine detail.  On the other hand, when producing output the drawing will need to be adjusted in size to fit the *page size*.  Generally, output is a printed page, but it can also be a pdf, or :ref:`exported to another image format <file>`.  

As an example, for an annotated drawing of a floor plan to appear correctly when the drawing is reduced in size, or *scaled down*, to print on an "A4" page (210 x 297 mm), the dimension text would need to be proportional to the floor plan itself prior to being reduced to fit the page.  Trying to determine the dimension text size for scaling such a large object would be tedious at best, but a feature of LibreCAD makes it simple.  The "General Scale" is used to adjust the dimension text, arrows and related parameters to the sizes suitable for the required page size.  Both the page size, and the dimensioning parameters - including the "General Scale" - are configured in the :ref:`Drawing Preferences <draw-prefs>`.

There are two tabs in **Drawing Preferences**, "Paper" and "Dimensions", that require attention for a new drawing.  Specifically the items that need to be addressed are:

      1. On the "Paper" tab: Selecting a paper size and orientation will determine the *print scale* used for final output.  The print scale is used to determine the "General Scale".
      2. On the "Dimensions" tab: Setting the "General Scale" will adjust the dimension text and related parameters to suit the page size.

The paper format, orientation, and margins to be used is an important to consideration when setting the drawing preferences.  The page size is entirely up to the user to determine based on what is available (depending on the printer or printing service that is being used).  While it can be done at anytime, establishing the page size sooner than later will help determine the "General Scale".

.. admonition:: Tip - Determining Scale

    If multiple options are available for the paper size, setting the paper size *after drawing the object but prior to dimensioning the drawing* will help determine the print scale, the "General scale", and subsequently the appropriate line spacing for dimensions.  See :ref:`Dimensioning <dimensioning>` for additional information.

    While any scale can be used when printing a drawing there are commonly used scales for different types of drawings.  Refer to  :ref:`Scales <scales>` in the appendix for some examples.

    Be sure to allow room on the drawing for dimension lines and text when determining the print scale.  More details on printing a drawing are found in the :ref:`Printing Guide <complete&print>`.


.. _ug-layers:

Layers
------

Using layers to organize drawings and assign :ref:`pen <entity-pen>` attributes to the entities on the layer is an important concept.  Refer to :ref:`Layers <entity-layers>` in **Fundamentals** and the :ref:`Layer List Dock <widget-layerList>` under **Dock Widgets** in the **Reference** section for additional details on using layers.

In LibreCAD, layers are managed using the **Layer List Dock**.  Use the **Layer List Dock** to add and remove, show and hide and modify the layer's attributes.  Creating a layer is simple:

    #. Click the **Add a layer** icon |icon01|.
    #. Specify a *Layer Name*.
    #. Optionally specify the Pen Color, Width and Line Type for the layer.
    #. Click **Ok**.

The first layer added defaults to the layer name "noname", but the name can be replace with any alpha-numeric text.  Additional layers add will adopt the name of the currently selected layer and append a sequential number, but can also be renamed.  

.. admonition:: Tip - Using Layers

    Layer **0** is a special layer and should not be used for general drawing purposes.  Create at least one additional layer for the drawing.

    Prefix the layer name with a sequential number when naming the layer to help sort the layers in the dock list.  Layers are listed in alpha-numeric order, e.g. 1a, 1b, 2a, 2b, etc.

    Use "Construction Layer" to create reference geometry to help align other drawing entities.

    Layers that have been completed can be *locked*.  Locking layers prevents accidental changes and can improve the performance when working with very large complex drawings.

    Hiding layers while drawing reduces the *visual complexity* and makes it easier to focus on the current drawing efforts.


.. _ug-templates:

Templates
---------

Having to set the unit, page size, layers, etc. each time a new drawing is created can be avoided by using *templates*.  Templates are *prototype* drawings that provide a method to save a drawing's configuration so it does not need to be defined each time a new drawing is started.  A template's configuration can include the settings defined in the **Drawing Preferences**, such as the page size, unit of measure, and the dimensioning format.  Templates can also include layers and other drawing elements such as a border and / or a title block. These settings and drawing elements are inherited by a new drawings created from the template.

When LibreCAD is launched it creates a new drawing using a *default template*.  The default template is also used when a new drawing is created within LibreCAD by selecting **File -> New** or clicking the **New** icon |icon02|.  The new document is initially called "unnamed document 1".  Any addition new drawings created while LibreCAD is still open will be number sequentially; "unnamed document 1", "unnamed document 2", and so on.  New drawings inherit the template drawing contents, but do not take the template's name as a file name.  Users are prompted for a file name when saving the drawing.

*User-defined* templates can be created to suit various purposes such as different page sizes or orientation, unit of measure, etc.  User-defined templates can be used by selecting **File -> New From Template** or clicking the **New from Template** icon |icon03| and then selecting the desired template file.  See "Creating Templates" below.

Creating Templates
~~~~~~~~~~~~~~~~~~

Templates are created starting with a new drawing, setting the desired :ref:`Drawing Preferences <draw-prefs>`, and adding any required drawing elements (e.g. layers, borders, etc).  To create a template, starting with a blank drawing:

    #. Set the the drawing preferences by selecting **Options** from the menu bar and then **Current Drawing Preferences**.

        #. On the "Paper" tab set the paper size, orientation and margins as desired.
        #. Select the "Units" tab and set the "Main Drawing Unit".  (Note the "Length" and "Angle" settings configure the :ref:`status bar <statusbar>` format and not the dimensioning format that appear on the drawing.)
        #. Click the "Dimensions" tab and adjust the values.
        #. Check the remaining tab, "Grid" and "Splines" and adjust those settings if necessary.
        #. Click "OK" when done.

    #. Add any layers as needed.  See :ref:`Layers <ug-layers>` for details on using layers and setting the attributes.
    #. Add any other drawing elements (borders, title boxes, etc) as required.
    #. Save the template as a "dxf", e.g. "myTemplate.dxf", to any location with read / write permissions.

LibreCAD supports the use of multiple templates.  A user that plans on creating similar drawings may require only a default template created to suit their needs.  Users that create several different types of drawings may desire multiple templates.  For example, templates can be created for each paper size available and / or for each paper orientation.

Default Template
~~~~~~~~~~~~~~~~

LibreCAD includes a default template, "empty.dxf", that is installed with the application and found in the resources directory.  It is used initially as the default template for all new drawings.  A user-defined template can be used instead of the default by specifying the new template in the :ref:`Application Preferences <app-prefs>`.  From the  **Options** menu select **Application Preferences** and click on the "Paths" tab.  Enter the path and filename of the template to be used as the default.  The specified template is used instead of the default LibreCAD template when the application is launched and for new drawings.



..  Icon mapping:

.. |icon01| image:: /images/icons/add.svg
            :height: 18
            :width: 18
.. |icon02| image:: /images/icons/new.svg
            :height: 18
            :width: 18
.. |icon03| image:: /images/icons/new_from_template.svg
            :height: 18
            :width: 18
