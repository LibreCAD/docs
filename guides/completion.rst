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


.. _print-preview: 

Print Preview Window
--------------------

LibreCAD’s **Print Preview** displays the drawing on a virtual piece of paper and allows adjustments to the layout prior to committing the drawing to paper. To switch to the print preview window, click the **Print Preview** icon |icon02| or select **File -> Print Preview**:

   
.. figure:: /images/doohickeyPrintPreview.png
    :align: center
    :scale: 50
    :alt: LibreCAD's Print Preview window

    LibreCAD's Print Preview window displaying the *Doohickey* drawing

.. actual image size 1280px x 960px

Opening the print preview window also displays the **Print Preview Tool Options** toolbar:

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

#. Starting with the drawing open in the drawing window, switch to print preview window by clicking the **Print Preview** icon |icon02|.  
#. Click the **Fit to Page** icon |icon13| on the toolbar.  This will ensure the drawing displayed correctly in the print preview.  Note that "fixed" needs to be *unchecked*.
#. Open the **Drawing Preferences** (**Options -> Current Drawing Preferences**) and check the paper layout ("Format", "Orientation" and "Margins") for the current drawing: e.g. A4, Landscape, Top, Bottom Left and Right Margins each at 10.  Adjust the layout if necessary and click **OK**.
#. Click the **Fit to Page** icon |icon13| on the toolbar.  This will ensure the drawing is scaled to fit the current paper format and centered on the page.  Note the scale in the text-box of the print preview toolbar.
#. Adjust the scale using a *smaller* ratio than the "Fit to Page" scale.  For example use "1:2" if "1:1.18" is the calculated scale.  Change the print scale by:

    - Selecting a predefined scale ratio from the drop-down, or type the required scale ratio in the text-box and press [Enter].
    - Lock the print scale by placing a checkmark in the "fixed" checkbox.

#. Adjust the position of the drawing image on the paper by:

    - Clicking the **Center to Page** icon |icon12|, or 
    - repositioning the paper by dragging it as needed (the drawing stays centered on the screen).

#. Close the print preview window by clicking the **Print Preview** icon |icon02|.
#. If necessary, adjust the dimensions "General Scale" and dimension line placement.  Refer to :ref:`Dimensioning <dimensioning>` for details.
#. If using a border / title page block, insert the block from the **Library Browser**:

    - Insert a block from *sheets* that matches the paper format and orientation, e.g. "A4H" for a landscape A4 page.
    - Set the blocks scale "Factor" suit the scale determined above, e.g. "2" for a drawing scale of 1:2.  See  **Inserting Blocks** in :ref:`Using the Library Browser <ug-LibBrowser>` for details.
    - "Explode" the border block and add/modify text using the "Properties" tool.  Refer to the :ref:`Modify <tool-modify> tools.

#. Switch to the print preview window and check the completed drawing.  If necessary, click "Fit to Page" to align the drawing to the paper.


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
