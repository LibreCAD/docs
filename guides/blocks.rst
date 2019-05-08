.. User Manual, LibreCAD v2.2.x


.. _blocks:

Blocks
======

*Blocks* are a small reusable drawings of commonly used objects such as bolts, furniture, electronic components, title blocks, etc.  Inserted blocks, also called *inserts*, are composed of geometric shapes (lines, arcs, etc.) and can also include text and dimensions.  When inserted into a drawing, a block is treated as a single entity with common attributes (layer and pen).  Blocks can be inserted into the same drawing more than once with different locations, scale and rotation angle.

.. Insert image example:

The are two "dock widgets" for managing blocks.  The :ref:`Block List Dock <widget-blockList> for managing blocks *within the current drawing*.  The :ref:`Library Browser Dock <widget-libBrowser>` that shows the *collection of blocks available* and allows users to insert blocks into the current drawing.  See :ref:`Dock Widgets <widgets>` in the **Reference** section for more details.  LibreCAD includes several libraries of blocks that can be inserted into a drawing.  

Blocks can also be created and used within the current drawing or saved to a *user library*.  

Inserted blocks are all linked. Changes to one inserted block will be reflected in all instances of the block.


Creating a Block
----------------

The are a couple of different ways to create a block.

.. tip::
    Create blocks on their own layer.  The layer will bew added to the drawing when a block is inserted.


From a Drawing
~~~~~~~~~~~~~~

    - Draw the object to be converted to a block
    - Select all the entities that make up the object
    - Click on the **Create Block** |icon12|.
    - Specify the reference point for the block.  The reference point is used to locate the object when it is inserted into the drawing.
    - Provide a unique name for the new block and click "OK".  The new block will appear in the **Block List** dock.


From an Empty Block
~~~~~~~~~~~~~~~~~~~

    - Click on the "Add an empty block" icon |icon12|.  Provide a unique name for the new block and click "OK".  The new block will appear in the **Block List** dock.
    - Select the new block in the **Block List** and click the **Edit the active block in a separate window** icon |icon16|.
    - Draw the object.  The drawing's origin (0, 0) will become the reference point for the block.
    - Close the new block's drawing window and the block will be saved.


Using Blocks
------------

    - Select a block in the **Block List**.
    - Click on the "Insert the active block" |icon18|.
    - Place the block at the desired location within the drawing.  optionally specify a rotation angle and / or a scale factor for the block.

Blocks can also be cut, copied, and pasted using the normal edit commands.  For example, to copy a block from one drawing to another:

    - Select a block in the current drawing.
    - Press [Ctrl]+[c] (or **Edit -> Copy** from the menu)
    - Within the current drawing or switch to a new drawing and press [Ctrl]+[v] (or **Edit -> Paste**)
    - Specified point to place the block.


Saving Blocks
-------------

Blocks can be saved to a seperate file and used in other drawings or added to a user library.  To save the block:

    - Select a block in the **Block List**.
    - Click the **Save the active block to a file** icon |icon17|.
    - Select a file location, specify a file name and Click **Save**.


Block Libraries
===============

You can also use the library browser. Set the path in Application Preferences, and have blocks in sub-directories of that path.
Part Libraries and Symbols for 2D CAD systems

In the "Paths" tab there are other file paths to be specified. The symbol or library folder location is called "Parts Library". This folder specification should contain the full path and name of the folder mentioned earlier in regard to parts libraries. The library folder can contain additional folders to categorize the items. For instance: floor plan, electric, electronic, landscape, flow diagram, plumbing, hardware, etc. The subfolders are required. LibreCAD does not provide a mechanism to use the library directory directly. A user could use it for template storage if they desired and then the templates could be used by the "New From Template" option or for the default template setting. The LibreCAD "Library Browser" will only present the created folders (and subfolders) with the drawings within the browser.

Once installed, these Part Libraries can be viewed with the Library Browser so that parts can be inserted into your drawings (start LibreCAD, then select: "View > Toolbars > Library Browser"). On insertion, each part is converted into a block which can be re-inserted many times.


Installation
------------

The easiest method of installation, which does not require Windows Administrator or Linux Root privileges, is to create a new folder named "library" on your Desktop or in your Documents. Download any of these Part Libraries and unzip (Extract) them into the new "library" folder, then go up a level, right-click on the folder's icon and select "Properties". The path to this folder (Location) should be something similar to "C:\Documents and Settings\Guest\Desktop" or "/home/guest/Documents", therefore the full path to the unzipped Part Libraries within it would be "C:\Documents and Settings\Guest\Desktop\library\" or "/home/guest/Documents/library/" (remember to include the final "\" or "/" after "library"). Make a note of this full path, Restore LibreCAD, select: "Edit > Application Preferences > Paths", type the full path into the box marked "Part Libraries", select "OK", then re-start LibreCAD.

These Part Libraries are universal, that is, they have been tested on 32-bit and 64-bit systems, Windows and Linux: 


..  Icon mapping:

.. |icon10| image:: /images/icons/visible.svg
            :height: 24
            :width: 24
.. |icon11| image:: /images/icons/invisible.svg
            :height: 24
            :width: 24
.. |icon12| image:: /images/icons/create_block.svg
            :height: 24
            :width: 24
.. |icon13| image:: /images/icons/add.svg
            :height: 24
            :width: 24
.. |icon14| image:: /images/icons/remove.svg
            :height: 24
            :width: 24
.. |icon15| image:: /images/icons/rename_active_block.svg
            :height: 24
            :width: 24
.. |icon16| image:: /images/icons/properties.svg
            :height: 24
            :width: 24
.. |icon17| image:: /images/icons/save.svg
            :height: 24
            :width: 24
.. |icon18| image:: /images/icons/insert_active_block.svg
            :height: 24
            :width: 24


..    |icon10|, Show all blocks
..    |icon11|, Hide all blocks
..    |icon12|, Create Block
..    |icon13|, Add an empty block
..    |icon14|, Remove the active block
..    |icon15|, Rename the active block
..    |icon16|, Edit the active block in a separate window
..    |icon17|, Save the active block to a file
..    |icon18|, Insert the active block
