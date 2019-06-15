.. User Manual, LibreCAD v2.2.x


.. _printing-guide: 

Printing Guide
==============

These steps for printing assume the drawing to be printed was drawn full-scale (1:1).


Printing, Quick and Easy
------------------------

To print a drawing without a drawing border / title block template or a specific scale is relatively quick and easy.  With a drawing opened in LibreCAD:

1. Select **File -> Print Preview** or click the **Print Preview** button |icon02|.
2. Set or confirm the paper layout for the current drawing:

    a. Select **Options -> Current Drawing Preferences**.
    b. Set format as desired, e.g. A4, Landscape, and click **OK**.
    c. The page is represented by the shadowed rectangle in the print preview.

3. Click the **Fit to Page** button |icon05| on the toolbar.  This ensure the drawing is scaled to fit and centered on the page.
4. Select **File -> Print** or click the *Print button |icon01|.
5. Select the printer on the *Print* dialogue and confirm the properties by clicking the **Properties** button.  Adjust the properties if necessary and then click **OK**.
6. Click the **Print** button.


Printing to Scale
-----------------

To print a drawing without a drawing border / title block template but to a specific scale requires a couple of additional steps.  With a drawing opened in LibreCAD:

1. Select **File -> Print Preview** or click the **Print Preview** button |icon02|.
2. Set or confirm the paper layout for the current drawing:

    a. Select **Options -> Current Drawing Preferences**.
    b. Set format as desired, e.g. A4, Landscape, and click **OK**.
    c. The page is represented by the shadowed rectangle in the print preview.

3. Click the **Fit to Page** button |icon05| on the tool bar.  This establish the largest scale the can be used for the paper size defined in step 2 above.
4. Select the desired scaled from the drop-down box on the toolbar.
5. Click the **Center to Page** button |icon04| from the toolbar.  
6. The drawing can be re-positioned on the page by moving the page behind the drawing.  Click and hold anywhere in the drawing space and drag the paper to the desired position.  Pressing [Shift] allows only *horizontal* movements of paper and pressing [Ctrl] allows only *vertical* movements.
7. Select **File -> Print** or click the **Print** button |icon01|.
8. Select the printer on the *Print* dialogue and confirm the properties by clicking the **Properties** button.  Adjust the properties if necessary and then click **OK.**
9. Click the **Print** button.


Printing to Scale with dimensions
---------------------------------

.. important:: For a drawing drawn full scale (1:1) with dimensions, the size of dimensioning text and arrows needs to be adjusted for the print output. These sizes will depend on the desired scale of the print output. If they are not adjusted then the defined text size will apply and it may not be appropriate for large or small scale drawings.

Once the printing scale is defined (see previous section), the size of dimensions can be adjusted in :ref:`Drawing Preferences <draw-prefs>` with the parameter *General Scale*. It is recommended to enter the printing scale number as input value for *General Scale* (i.e. 50 for a printing scale of 1:50). Since the printing scale of the drawing is 1:50, the dimension *General Scale* is 50 and the default text size is 2.5 mm, the printing size of the dimension text will be : 1/50 * 50 *2.5 = 2.5 mm.

Setting the *General Scale* adjusts dimension text to the correct size for the print output. The *General Scale* does NOT adjust the dimension line spacing. The dimension line spacing may need to be adjusted after changing the *General Scale*.

.. note:: The size of annotations, which are not dimensions, cannot be modified through Dimension Drawing Preferences. So it has to be adjusted with the same factor using **Tools -> Modify -> Properties**.


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

    a. Click the **Fit to Page** button |icon05| on the tool bar and note the drawing scale shown in the drop-down box on the toolbar.  The is the largest scale that can be used for the current paper size.
    b. Adjust the scale to ensure the drawing will fit on the printed page and accommodate a border that will be added in a later step. For example, if the *Fit to Page* ration is 1:1.5, adjust the ration to 1:2.
    c. Fix the scale by clicking the *Fixed* checkbox.
    d. Close *Print Preview* (click the **Print Preview** button  |icon01| ) and return to the drawing window.

4. Add the border and title block around the original drawing:

    a. Draw lines defining the page perimeter, e.g. draw a rectangle 297 mm x 210 mm for an A4 paper.
    b. Draw lines for a page border offset from the perimeter line drawn above.
    c. Or, insert a border / title block from the Library (predefined borders are in the *sheets* directory for ISO paper sizes) and scale it using the ration determined above, e.g for a 1:2 ration, scale the border by 2.  Note: Setting the *Scale Factor* when inserting a block didn’t work for me, but the block can be scaled after inserting by using *Scale* (**Tools -> Modify -> Scale**).

5. Re-confirm the layout in the *Print Preview*:

    a. Click the **Print Preview** button |icon02|.
    b. Reset the scale to the ration determined in step 3b, i.e. 1:2.
    c. Click the **Center to Page** button |icon04|.

6. Select **File -> Print** or click the **Print** button |icon01|.
7. Select the printer on the *Print* dialogue and confirm the properties by clicking the **Properties** button.  Adjust the properties if necessary and then click **OK**.
8. Click the **Print** button |icon01|.


Tiled Printing
-----------------

To print a drawing to the specific scale that greater than an available paper, use so-called "tiled printing".  In this case, the drawing is outputted in parts that can be glued together to get the original drawing.  With a drawing opened in LibreCAD:

1. Select **File -> Print Preview** or click the **Print Preview** button |icon02|.
2. Set or confirm the paper layout for the current drawing:

    a. Select **Options -> Current Drawing Preferences**.
    b. Set format as desired, e.g. A4, Landscape, and click **OK**.
    c. The page is represented by the shadowed rectangle in the print preview.

3. Select the desired scale from the drop-down box on the toolbar.
4. Click the **Calculate number of pages...** button |icon07| from the toolbar.  In print preview will be shown the multiple pages placed side by side and the drawing in the center of it.  Note: *Number of pages* may be changed through **Options -> Current Drawing Preferences** on *Paper* tab.
5. The drawing can be re-positioned on the pages by moving the pages behind the drawing.  Click and hold anywhere in the drawing space and drag the paper to the desired position. Pressing [Shift] allows only *horizontal* movements of paper and pressing [Ctrl] allows only *vertical* movements.
6. Select **File -> Print** or click the **Print** button |icon01|.
7. Select the printer on the *Print* dialogue and confirm the properties by clicking the **Properties** button.  Adjust the properties if necessary and then click **OK**.
8. Click the **Print** button.

In case when a page has the margins (margins > 0) the print preview takes on a special look.  Namely the margins between a neighbor pages aren't shown.  It makes possible to represent the printable areas of all pages as one whole area and to show an undivided drawing.  Or in other words, the print preview looks like the drawing was outputted and glued together without excess margins.

Next example shows the print preview (left) and the output of tiled printing with the margins (right):

.. figure:: /images/tiledPrint.png
    :width: 650px
    :height: 300px
    :align: center
    :scale: 100
    :alt: Tiled print preview and output

The sequence of the output is from bottom left page to top right page.  In the picture above the order of the output is marked by numbers.


..  Icon mapping:

.. |icon01| image:: /images/icons/print.svg
            :height: 18
            :width: 18
.. |icon02| image:: /images/icons/print_preview.svg
            :height: 18
            :width: 18
.. |icon03| image:: /images/icons/printbw.png
            :height: 18
            :width: 18
.. |icon04| image:: /images/icons/printcenter.png
            :height: 18
            :width: 18
.. |icon05| image:: /images/icons/printfit.png
            :height: 18
            :width: 18
.. |icon06| image:: /images/icons/printscale.png
            :height: 18
            :width: 18
.. |icon07| image:: /images/icons/multi_pages.svg
            :height: 18
            :width: 18

