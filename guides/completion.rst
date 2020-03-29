.. User Manual, LibreCAD v2.2.x

.. Default include
.. include:: /inclFiles/notice.rst


.. _complete&print: 

Completing and Printing
=======================

Completed drawings are normally printed to scale and include a border and title block.  However, drawings without a border can be useful for drafts, sketches, exporting to CNC software or a bitmapped image, and so on.  In addition to supporting a large variety of paper sizes; ISO, ANSI, Arch (Architectural), custom, etc., LibreCAD also has the ability to print drawings across several pages using *tiled printing*, allowing a drawing to be printed on smaller paper and assembled into a large format print.

Completing a drawing and making it ready for printing includes a few steps:

    - Finalizing the page size and drawing scale,
    - adjusting the dimensions and spacing, and
    - adding page border and title block as required.


.. admonition:: Tip - Using Border and Title Blocks

    Adding a border provides a finished look and title blocks include important information for the drawing.  Title blocks vary widely in content and layout, but can include:

    - Drawing name
    - Project name
    - Scale
    - Drawing perspective
    - Date
    - Revision
    - Page number
    - Paper size
    - Name of organization
    - Name of draftsperson, approvers, etc
    - Others as required


.. _printPreview: 

Print Preview Window
--------------------

LibreCAD’s **Print Preview** displays the drawing on a virtual piece of paper.  It allows adjustments to the layout prior to committing the drawing to paper. Click the **Print Preview** icon |icon02| or select **File -> Print Preview** and the print preview window is opened:

   
.. figure:: /images/doohickeyPrintPreview.png
    :align: center
    :scale: 50
    :alt: LibreCAD's Print Preview window

    LibreCAD's Print Preview window displaying the *Doohickey* drawing

.. actual image size 1280px x 960px

Opening the **Print Preview** also displays the **Print Preview Tool Options** toolbar:

.. figure:: /images/toolOptions/toPrintPreview.png
    :align: center
    :scale: 100
    :alt: Print Preview Toolbar
.. actual image size 388px x 35px

More details for :ref:`Print Preview Tool Options <print-preview-toolopt>` can be found in the **Reference** / **Toolbars / Tool Options** section.

The print preview window shows the virtual paper as a white rectangle with a black border and a drop shadow.  The black border represents the paper format and orientation as it is configured on the "Paper" tab of the :ref:`Drawing Preferences <draw-prefs>`.  If margins are specified on the "Paper" tab, they are shown as a dark grey border.

A drawing can be printed directly without setting the scale or adding title block by confirming the layout in the print preview and then continuing with :ref:`Printing <print>`.


.. _completion: 

Completing the Drawing
----------------------

A finished drawing will include a border / title block and be scaled to suit the paper format and orientation.  See :ref:`Scale and Dimensioning <ug-scale>` in the **Drawing Setup** for more details on determining the suitable scale for a drawing.

.. important::

    These steps assume a drawing that is drawn to full-scale (1:1).

#. Starting with the drawing open in the drawing window and switch to print preview window by clicking the **Print Preview** icon |icon02|.  The drawing will automatically adjust to "fit the page" as it is currently configured.
#. Open the **Drawing Preferences** (**Options -> Current Drawing Preferences**) and check the paper layout ("Format", "Orientation" and "Margins") for the current drawing: e.g. A4, Landscape, Top, Bottom Left and Right Margins each at 10.  Adjust the layout if necessary and click **OK**.
#. Click the **Fit to Page** icon |icon13| on the toolbar.  This will ensure the drawing is scaled to fit the current paper format and centered on the page.  Note the scale in the text-box of the print preview toolbar.
#. Adjust the scale using a *smaller* ratio than the "Fit to Page" scale.  For example use "1:2" if "1:1.18" is the calculated scale.  Change the print scale by:

    - Selecting a predefined scale ratio from the drop-down, or
    - type the required scale ratio in the text-box and press [Enter].

#. Adjust the position of the drawing image on the paper by:

    - Clicking the **Center to Page** icon |icon12|, or
    - repositioning the paper by dragging it as needed (the drawing stays centered on the screen).

#. Close the print preview window by clicking the **Print Preview** icon |icon02|.
#. If necessary, adjust dimension line placement.  Refer to :ref:`Dimensioning <dimensioning>` for details.
#. If using a border / title page block, insert the block from the **Library Browser**:

    - Insert a block from *sheets* that matches the paper format and orientation, e.g. "A4H" for a landscape A4 page.
    - Set the blocks scale "Factor" suit the scale determined above, e.g. "2" for a drawing scale of 1:2.  See  **Inserting Blocks** in :ref:`Using the Library Browser <ugLibBrowser>` for details.
    - "Explode" the border block and add/modify text using the "Properties" tool.  Refer to the :ref:`Modify <tool-modify> tools.

#. Switch to the print preview window and check the completed drawing. Click Fit to Page or Zoom All if necessary


.. _print:

Printing
--------

While a drawing can be printed directly by clicking the **Print** icon |icon01| or selecting  **File -> Print**, the recommended approach is to print drawings from the **Print Preview** window:

#. Starting with the drawing open in the drawing window, switch to print preview window by clicking the **Print Preview** icon |icon02|.  The drawing will automatically adjust to "fit the page" as it is currently configured.
#. Click the **Print** icon |icon01| or select **File -> Print**.
#. Select the printer on the *Print* dialogue and confirm the properties by clicking the **Properties** icon.  Adjust the properties if necessary and then click **OK**.
#. Click the **Print** icon.


.. _print-tiled:

Tiled Printing
~~~~~~~~~~~~~~

*Tiled printing* provides the ability to print a scaled drawing that is larger than the available paper.  It uses the paper as defined by the "Format" and "Orientation", and lays it out in a grid defined by pattern defined by "Number of pages".  As an example, an portrait A4 page with 2 pages horizontally and 1 vertically would result in a *page space* of 420 x 297 mm, or landscape A4 in a 2 x 2 pattern would be a page space of 594 x 420 mm.  Both examples use a margin of 0.  If a margin is defined the page space would be reduced the margin width on the edge of the paper where they are assembled.

In this case, the drawing is outputted in parts that can be assembled into a full-sized drawing.  

With a drawing opened in LibreCAD:

1. Select **File -> Print Preview** or click the **Print Preview** button |icon02|.
2. Set or confirm the paper layout for the current drawing:

    a. Select **Options -> Current Drawing Preferences**.
    b. Set format as desired, e.g. A4, Landscape, and click **OK**.
    c. The page is represented by the shadowed rectangle in the print preview.

3. Select the desired scale from the drop-down box on the toolbar.
4. Click the **Calculate number of pages...** button |icon14| from the toolbar.  In print preview will be shown the multiple pages placed side by side and the drawing in the center of it.  Note: *Number of pages* may be changed through **Options -> Current Drawing Preferences** on *Paper* tab.
5. The drawing can be re-positioned on the pages by moving the pages behind the drawing.  Click and hold anywhere in the drawing space and drag the paper to the desired position. Pressing [Shift] allows only *horizontal* movements of paper and pressing [Ctrl] allows only *vertical* movements.
6. Select **File -> Print** or click the **Print** button |icon01|.
7. Select the printer on the *Print* dialogue and confirm the properties by clicking the **Properties** button.  Adjust the properties if necessary and then click **OK**.
8. Click the **Print** button.

In case when a page has the margins (margins > 0) the print preview takes on a special look.  Namely the margins between a neighbor pages aren't shown.  It makes possible to represent the printable areas of all pages as one whole area and to show an undivided drawing.  Or in other words, the print preview looks like the drawing was outputted and glued together without excess margins.

Next example shows the print preview (left) and the output of tiled printing with the margins (right):

.. figure:: /images/tiledPrint.png
    :align: center
    :scale: 100
    :alt: Tiled print preview and output

.. actual image size 650px x 300px

The sequence of the output is from bottom left page to top right page.  In the picture above the order of the output is marked by numbers.

.. OLD STUFF



    .. _print-scale:

    Printing to Scale
    -----------------

    To print a drawing without a drawing border / title block template but to a specific scale requires a couple of additional steps.  With a drawing opened in LibreCAD:

    1. Select **File -> Print Preview** or click the **Print Preview** button |icon02|.
    2. Set or confirm the paper layout for the current drawing:

        a. Select **Options -> Current Drawing Preferences**.
        b. Set format as desired, e.g. A4, Landscape, and click **OK**.
        c. The page is represented by the shadowed rectangle in the print preview.

    3. Click the **Fit to Page** button |icon13| on the tool bar.  This establish the largest scale the can be used for the paper size defined in step 2 above.
    4. Select the desired scaled from the drop-down box on the toolbar.
    5. Click the **Center to Page** button |icon12| from the toolbar.  
    6. The drawing can be re-positioned on the page by moving the page behind the drawing.  Click and hold anywhere in the drawing space and drag the paper to the desired position.  Pressing [Shift] allows only *horizontal* movements of paper and pressing [Ctrl] allows only *vertical* movements.
    7. Select **File -> Print** or click the **Print** button |icon01|.
    8. Select the printer on the *Print* dialogue and confirm the properties by clicking the **Properties** button.  Adjust the properties if necessary and then click **OK.**
    9. Click the **Print** button.


    .. _print-dimensions:

    Printing to Scale with Dimensions
    ---------------------------------

    .. important:: For a drawing drawn full scale (1:1) with dimensions, the size of dimensioning features needs to be adjusted for the print output. These sizes will depend on the desired scale of the print output. If they are not adjusted then the defined text size will apply and it may not be appropriate for large or small scale drawings.

    Once the printing scale is defined (see previous section), the size of dimensions can be adjusted in :ref:`Drawing Preferences <draw-prefs>` with the parameter *General Scale*. It is recommended to enter the printing scale number as input value for *General Scale* (i.e. 50 for a printing scale of 1:50). Since the printing scale of the drawing is 1:50, the dimension *General Scale* is 50 and the default text size is 2.5 mm, the printing size of the dimension text will be : 1/50 ``*`` 50 ``*`` 2.5 = 2.5 mm.

    .. note:: The size of annotations, which are not dimensions, cannot be modified through Dimension Drawing Preferences. So it has to be adjusted with the same factor using **Tools -> Modify -> Properties**.

    It is recommended to check that the final appearance of dimensioning features for the print output suits your need.


    .. _print-border:

    Printing to Scale with a Border and Title Block
    -----------------------------------------------

    To print a drawing with a drawing border / title block template, but to a specific scale requires several steps:

    - Starts with a drawing drawn full scale (1:1),
    - Select the paper size for the print and adjust the drawing scale to suit,
    - Insert the page border and title block,
    - Print.

    Specifically, the process is as follows.  Starting with a full-scale (1:1) drawing:

    1. Open the drawing file to be printed and select **File -> Print Preview** or click the **Print Preview** button |icon02|.  The page is represented by the shadowed rectangle in the print preview.  Zoom out if necessary.
    2. Set or confirm the paper layout for the current drawing:

        a. Select **Options -> Current Drawing Preferences**.
        b. Set format as desired, e.g. A4, Landscape, and click **OK**.

    3. To establish the largest scale the can be used for the paper size:

        a. Click the **Fit to Page** button |icon13| on the tool bar and note the drawing scale shown in the drop-down box on the toolbar.  The is the largest scale that can be used for the current paper size.
        b. Adjust the scale to ensure the drawing will fit on the printed page and accommodate a border that will be added in a later step. For example, if the *Fit to Page* ratio is 1:1.5, adjust the ratio to 1:2.
        c. Fix the scale by clicking the *Fixed* checkbox.
        d. Close *Print Preview* (click the **Print Preview** button  |icon01| ) and return to the drawing window.

    4. Add the border and title block around the original drawing:

        a. Draw lines defining the page perimeter, e.g. draw a rectangle 297 mm x 210 mm for an A4 paper.
        b. Draw lines for a page border offset from the perimeter line drawn above.
        c. Or, insert a border / title block from the Library (predefined borders are in the *sheets* directory for ISO paper sizes) and scale it using the ratio determined above, e.g for a 1:2 ratio, scale the border by 2.  Note: Setting the *Scale Factor* when inserting a block didn’t work for me, but the block can be scaled after inserting by using *Scale* (**Tools -> Modify -> Scale**).

    5. Re-confirm the layout in the *Print Preview*:

        a. Click the **Print Preview** button |icon02|.
        b. Reset the scale to the ratio determined in step 3b, i.e. 1:2.
        c. Click the **Center to Page** button |icon12|.

    6. Select **File -> Print** or click the **Print** button |icon01|.
    7. Select the printer on the *Print* dialogue and confirm the properties by clicking the **Properties** button.  Adjust the properties if necessary and then click **OK**.
    8. Click the **Print** button |icon01|.


    .. _print-tiled:

    Tiled Printing
    --------------

    To print a drawing to the specific scale that greater than an available paper, use so-called "tiled printing".  In this case, the drawing is outputted in parts that can be glued together to get the original drawing.  With a drawing opened in LibreCAD:

    1. Select **File -> Print Preview** or click the **Print Preview** button |icon02|.
    2. Set or confirm the paper layout for the current drawing:

        a. Select **Options -> Current Drawing Preferences**.
        b. Set format as desired, e.g. A4, Landscape, and click **OK**.
        c. The page is represented by the shadowed rectangle in the print preview.

    3. Select the desired scale from the drop-down box on the toolbar.
    4. Click the **Calculate number of pages...** button |icon15| from the toolbar.  In print preview will be shown the multiple pages placed side by side and the drawing in the center of it.  Note: *Number of pages* may be changed through **Options -> Current Drawing Preferences** on *Paper* tab.
    5. The drawing can be re-positioned on the pages by moving the pages behind the drawing.  Click and hold anywhere in the drawing space and drag the paper to the desired position. Pressing [Shift] allows only *horizontal* movements of paper and pressing [Ctrl] allows only *vertical* movements.
    6. Select **File -> Print** or click the **Print** button |icon01|.
    7. Select the printer on the *Print* dialogue and confirm the properties by clicking the **Properties** button.  Adjust the properties if necessary and then click **OK**.
    8. Click the **Print** button.

    In case when a page has the margins (margins > 0) the print preview takes on a special look.  Namely the margins between a neighbor pages aren't shown.  It makes possible to represent the printable areas of all pages as one whole area and to show an undivided drawing.  Or in other words, the print preview looks like the drawing was outputted and glued together without excess margins.

    Next example shows the print preview (left) and the output of tiled printing with the margins (right):

    .. figure:: /images/tiledPrint.png
        :align: center
        :scale: 100
        :alt: Tiled print preview and output

    .. actual image size 650px x 300px

    The sequence of the output is from bottom left page to top right page.  In the picture above the order of the output is marked by numbers.


..  Icon mapping:

.. |icon01| image:: /images/icons/print.svg
            :height: 18
            :width: 18
.. |icon02| image:: /images/icons/print_preview.svg
            :height: 18
            :width: 18

.. |icon10| image:: /images/icons/scaleLineWidth.svg
            :height: 18
            :width: 18
.. |icon11| image:: /images/icons/black_n_white_mode.svg
            :height: 18
            :width: 18
.. |icon12| image:: /images/icons/center_to_page.svg
            :height: 18
            :width: 18
.. |icon13| image:: /images/icons/fit_to_page.svg
            :height: 18
            :width: 18
.. |icon14| image:: /images/icons/multi_pages.svg
            :height: 18
            :width: 18
