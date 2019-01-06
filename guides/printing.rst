.. User Manual, LibreCAD v2.2.x


.. _printing-guide: 

Printing Guide
==============

These steps for printing assume the drawing to be printed was drawn full-scale (1:1).


Printing, Quick and Easy
------------------------

To print a drawing without a drawing border / title block template or a specific scale is relatively quick and easy.  With a drawing opened in LibreCAD:

1. Select File -> Print Preview or click the ‘Print Preview’ icon.
2. Set or confirm  the paper layout for the current drawing:
    a. Select Options -> Current Drawing Preferences.
    b. Set format as desired, e.g. A4, Landscape, and click ‘OK’
    c. The page is represented by the shadowed rectangle in the print preview.
3. Click the ‘Fit to Page’ button on the toolbar.  This ensure the drawing is scaled to fit and centered on the page.
4. Select File -> Print or click the ‘Print’ icon.
5. Select the printer on the Print dialogue and confirm the properties by clicking the ‘Properties’ button.  Adjust the properties if necessary and then click ‘OK’.
6. Click the ‘Print’ button.


Printing to Scale
-----------------

To print a drawing without a drawing border / title block template but to a specific scale requires a couple of additional steps.  With a drawing opened in LibreCAD:

1. Select File -> Print Preview or click the ‘Print Preview’ icon.
2. Set or confirm the paper layout for the current drawing:
    a. Select Options -> Current Drawing Preferences.
    b. Set format as desired, e.g. A4, Landscape, and click ‘OK’
    c. The page is represented by the shadowed rectangle in the print preview.
3. Click the ‘Fit to Page’ button on the tool bar.  This establish the largest scale the can be used for the paper size defined in step 2 above.
4. Select the desired scaled from the drop-down box on the toolbar.
5. Click the ‘Center to Page’ icon from the toolbar.  
6. The drawing can be re-positioned on the page by moving the page behind the drawing.  Click and hold anywhere in the drawing space and drag the paper to the desired position.
7. Select File -> Print or click the ‘Print’ icon.
8. Select the printer on the Print dialogue and confirm the properties by clicking the ‘Properties’ button.  Adjust the properties if necessary and then click ‘OK’.
9. Click the ‘Print’ button.


Printing to Scale with a Border and Title Block
-----------------------------------------------

To print a drawing with a drawing border / title block template, but to a specific scale requires several steps:

* Starts with a drawing drawn full scale (1:1),
* Select the paper size for the print and adjust the drawing scale to suit,
* Insert the page border and title block,
* Print.

Specifically, the process is as follows.  Starting with a full-scale (1:1) drawing:

1. Open the drawing file to be printed and select File -> Print Preview or click the ‘Print Preview’ icon.  The page is represented by the shadowed rectangle in the print preview.  Zoom out if necessary.
2. Set or confirm the paper layout for the current drawing:

    a. Select Options -> Current Drawing Preferences.

    b. Set format as desired, e.g. A4, Landscape, and click ‘OK’

3. To establish the largest scale the can be used for the paper size:

    a. Click the ‘Fit to Page’ button on the tool bar and note the drawing scale shown in the drop-down box on the toolbar.  The is the largest scale that can be used for the current paper size.
    b. Adjust the scale to ensure the drawing will fit on the printed page and accommodate a border that will be added in a later step. For example, if the ‘Fit to Page’ ration is 1:1.5, adjust the ration to 1:2.
    c. Fix the scale by clicking the ‘fixed’ checkbox.
    d. Close Print Preview (click the ‘Print Preview’ icon) and return to the drawing window.

4. Add the border and title block around the original drawing:

    a. Draw lines defining the page perimeter, e.g. draw a rectangle 297 mm x 210 mm for an A4 paper.
    b. Draw lines for a page border offset from the perimeter line drawn above.
    c. Or, insert a border / title block from the Library (predefined borders are in the ‘sheets’ directory for ISO paper sizes) and scale it using the ration determined above, e.g for a 1:2 ration, scale the border  by 2.  Note: Setting the ‘Scale Factor’ when inserting a block didn’t work for me, but the block can be scaled after inserting by using ‘Scale’ (Tools -> Modify -> Scale).

5. Re-confirm the layout in the Print Preview:

    a. Click the ‘Print Preview’ icon.
    b. Reset the scale to the ration determined in step 3b, i.e. 1:2.
    c. Click the ‘Center to Page’ icon.

6. Select File -> Print or click the ‘Print’ icon.
7. Select the printer on the Print dialogue and confirm the properties by clicking the ‘Properties’ button.  Adjust the properties if necessary and then click ‘OK’.
8. Click the ‘Print’ button.

