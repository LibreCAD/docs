.. User Manual, LibreCAD v2.2.x


.. _blocks:

Blocks
======

*Blocks* are a small reusable drawings of commonly used objects such as bolts, furniture, electronic components, title blocks, etc.  Inserted blocks, also called *inserts*, are composed of geometric shapes (lines, arcs, etc.) and can also include text and dimensions.  LibreCAD includes several libraries of blocks that can be inserted into a drawing or users can create their own.

.. Insert image example:

The are two "dock widgets" for managing blocks.  The :ref:`Block List <widget-blockList>` dock for managing blocks *within the current drawing* and the :ref:`Library Browser <widget-libBrowser>` dock that shows the *collection of blocks available* and allows users to insert blocks into the current drawing.  See :ref:`Dock Widgets <widgets>` in the **Reference** section for more details.

When inserted into a drawing, a block is treated as a single entity.  Blocks can be inserted from the **Block List** into the same drawing more than once with different locations, scale and rotation angle.  Inserted blocks are all linked. Changes to one inserted block will be reflected in all instances of the block.


Creating a Block
----------------

The are a couple of different ways to create a block.

.. tip::
    Create blocks on their own layer.  The layer will be added to the drawing when a block is inserted.


From an Existing Drawing
~~~~~~~~~~~~~~~~~~~~~~~~

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
    - Specified a point in the drawing to place the block.


Saving Blocks
-------------

Blocks can be saved to a separate file and used in other drawings or added to a user library.  To save the block:

    - Select a block in the **Block List**.
    - Click the **Save the active block to a file** icon |icon17|.
    - Select a file location, specify a file name and Click **Save**.


Block Libraries
---------------

LibreCAD includes several categories of blocks in its library; algorithm, elektro, plan/air_water, plan/architect, etc.  To use blocks from the :ref:`Block Library <widget-libBrowser>`, select the block from the tree view, click **Insert** and specify a point in the drawing to place the block.

.. note::
    Insert a block from the library into the drawing only once.  If the same block is needed more than once, add  subsequent blocks from the **Block List**.  Inserting a block from the **Library Browser** multiple times will create multiple *independent* copies of the block in the **Block List**.


Adding to the Library
~~~~~~~~~~~~~~~~~~~~~

Additional part libraries can be added for blocks created by users, libraries downloaded from the LibreCAD wiki (https://wiki.librecad.org/index.php?title=Part_Libraries) or from other internet resources.  LibreCAD can be configured to show user-defined blocks in the library browser *in addition* to the blocks included with LibreCAD.  

The easiest method of installation, which does not require or Linux Root privileges or Windows Administrator access, is to create a new directory such as "PartsLibrary" in the home directory or "Documents" folder.  The path to this directory would be something similar to "/home/*UserName*/PartsLibrary/" or "C:\\Users\\ *UserName*\\Documents\\PartsLibrary\\ ".  Blocks and libraries can then be placed under the parent "PartsLibrary" directory.  The sub-directories will create categories that will appear in the tree view of the **Library Browser**.  

.. important::
    Do not place blocks directly in the parent parts library directory.  Blocks must be  placed in sub-directories to the parent libraries directory to appear in the **Library Browser**.

To include the new blocks in the **Library Browser** tree view, edit LibreCAD's :ref:`Application Preferences <app-prefs>` to add the path to the directory or folder with the user-defined blocks.  From the menus, select **Options -> Application Preferences** and select the **Paths** tab.  Type the full path to the part library, e.g. /home/*UserName*/PartsLibrary/ or C:\\Users\\ *UserName*\\Documents\\PartsLibrary\\ , into the text-box labelled "Part Libraries" and click "OK".  Click the **Rebuild** button on the **Library Browser** dock and the new libraries will appear in the tree view.


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
