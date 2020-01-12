.. User Manual, LibreCAD v2.2.x


.. _blocks:

Blocks
======

*Blocks* are a small reusable drawings of commonly used objects such as bolts, furniture, electronic components, title blocks, etc.  Inserted blocks, also called *inserts*, are composed of geometric shapes (lines, arcs, etc.) and can also include text and dimensions.  LibreCAD includes several libraries of blocks that can be inserted into a drawing or users can create their own.

.. Insert image example:

The are two "dock widgets" for managing blocks.  The :ref:`Block List <widget-blockList>` dock for managing blocks *within the current drawing* and the :ref:`Library Browser <widget-libBrowser>` dock that shows the *collection of blocks available*.  Both widgets allow users to insert blocks into the current drawing, but there are a couple of important differences:

   #. Blocks inserted from the **Library Browser**:

      #. Each block can be placed at a different location, rotation angle and/or scale.
      #. Blocks inserted multiple times will create a new instance of the block in the **Block List** each time it is inserted.  The blocks will numbered sequentially (*BlockName1*, *BlockName2*, ...)
      #. The inserted blocks will be independent of each other.

   #. Blocks inserted from the **Block List**:

      #. Each block can be placed at a different locations, scale, rotation angle, and can be placed in an array.
      #. Blocks inserted into a drawing from the **Library Browser** once and then subsequently inserted from the **Block List** multiple times are linked.  **Changes to one inserted block will be reflected in all instances of that block.**


Creating a Block
----------------

The are a couple of different ways to create a block:

   #. From an Existing Drawing

        - Draw the object to be converted to a block.
        - Select all the entities that make up the object.
        - Click on the **Create Block** |icon12|.
        - Specify the reference point for the block.  The reference point is used to locate the object when it is inserted into the drawing.
        - Provide a unique name for the new block and click **OK**.  The new block will appear in the **Block List** dock.


   #. From an Empty Block

        - Click on the **Add an empty block** icon |icon13|.  Provide a unique name for the new block and click **OK**.  The new block will appear in the **Block List** dock.
        - Select the new block in the **Block List** and click the **Edit the active block in a separate window** icon |icon16|.
        - Draw the object.  The drawing's origin (0, 0) will become the reference point for the block.
        - Close the new block's drawing window and the block will be saved.

.. tip::
    Create blocks on their own layer.


Inserting Blocks
----------------

Basic
~~~~~

    - Select a block in the **Block List**.
    - Click on the **Insert the active block** icon |icon18|.
    - Place the block at the desired location within the drawing.

Advanced
~~~~~~~~

Inserting block capability can be expanded through the *Tool Option* bar features before the block is inserted. 

.. figure:: /images/toolOptions/toBlockInsert.png
    :width: 617px
    :height: 34px
    :align: center
    :scale: 75
    :alt: Block insert tool option bar

These features can be of two types:
    - Related to block transformations: *Angle* of rotation and scale *Factor*.
    - Related to block patterns: *Array* (grid size) and *Spacing* between columns and rows of the array.

In the same block insertion, it is possible to combine transformations and pattern: a pattern of defined size and spacing is created then the pattern is rotated and finally the block entities are scaled but the spacing distances remain as defined.

    - Select a block in the **Block List**.
    - Click on the **Insert the active block** icon |icon18|.
    - Set the angle of rotation in *Angle* field as required. See :ref:`Angles in LibreCAD <angles>`.
    - Set the scale factor in *Factor* field as required. It is the same scale factor as in :ref:`Modify <tools>`.
    - Define the numbers of columns and rows in *Array* area to create a pattern.  Otherwise keep 1 for columns and rows to insert a single block.
    - Type the *Column spacing* distance between each column of the array. This is the distance between 2 block insertion points of 2 adjacent columns. 
    - Type the *Row spacing* distance between each row of the array. This is the distance between 2 block insertion points of 2 adjacent rows. 
    - Place the block at the desired location within the drawing. The insertion point of the pattern is the insertion point of the extreme lower and extreme left item in the array.

.. note::
    Using a pattern of 3x2 blocks will gather all entities of the 6 array items in *one block instance*. So selecting one entity of the 6-pattern will select the 6 array items. If this is not the intent then use the Rotate and Move commands with *Multiple copies*.

.. note::
    Blocks can also be cut, copied, and pasted using the normal edit commands.  For example, to copy a block from one drawing to another:

    - Select a block in the current drawing.
    - Press [Ctrl]+[c] (or **Edit -> Copy** from the menu)
    - Within the current drawing or switch to a new drawing and press [Ctrl]+[v] (or **Edit -> Paste**)
    - Specified a point in the drawing to place the block.


Editing a Block
~~~~~~~~~~~~~~~

    - Select a block in the **Block List** and click the **Edit the active block in a separate window** icon |icon16|.
    - Edit the block drawing.
    - Close the block's drawing window and the block will be saved and all instances of the block will be updated in the current drawing.

.. note::
    Currently only blocks created in the drawing as a new block can be edited.  Blocks inserted from the library Browser cannot be edited.


Saving Blocks
-------------

Blocks can be saved to a separate file and used in other drawings or added to a user library.  To save the block:

    - Select a block in the **Block List**.
    - Click the **Save the active block to a file** icon |icon17|.
    - Select a file location, specify a file name and click **Save**.


Block Libraries
---------------

LibreCAD includes several categories of blocks in its library; algorithm, elektro, plan/air_water, plan/architect, etc.  To use blocks from the :ref:`Block Library <widget-libBrowser>`, select the block from the tree view, click **Insert** and specify a point in the drawing to place the block.

.. note::
    Insert a block from the library into the drawing only once.  If the same block is needed more than once, add  subsequent blocks from the **Block List**.  Inserting a block from the **Library Browser** multiple times will create multiple *independent* copies of the block in the **Block List**.

Blocks located in a library can be rotated and scaled through the *Tool Option* bar features before their insertion. The rotation angle and the scale factor behave as for regular block.

.. figure:: /images/toolOptions/toBlockLib.png
    :width: 317px
    :height: 33px
    :align: center
    :scale: 75
    :alt: Block from library insertion tool option bar


Adding to the Library
~~~~~~~~~~~~~~~~~~~~~

Additional part libraries can be added for blocks created by users, libraries downloaded from the LibreCAD wiki (https://wiki.librecad.org/index.php?title=Part_Libraries) or from other internet resources.  LibreCAD can be configured to show user-defined blocks in the library browser *in addition* to the blocks included with LibreCAD.  

The easiest method of installation, which does not require or Linux Root privileges or Windows Administrator access, is to create a new directory such as "PartsLibrary" in the home directory or "Documents" folder.  The path to this directory would be something similar to "/home/*{Username}*/PartsLibrary/" or "C:\\Users\\ *{Username}*\\Documents\\PartsLibrary\\ ".  Blocks and libraries can then be placed under the parent "PartsLibrary" directory.  The sub-directories will create categories that will appear in the tree view of the **Library Browser**.  

.. important::
    Do not place blocks directly in the parent parts library directory.  Blocks must be  placed in sub-directories to the parent libraries directory to appear in the **Library Browser**.

To include the new blocks in the **Library Browser** tree view, edit LibreCAD's :ref:`Application Preferences <app-prefs>` to add the path to the directory or folder with the user-defined blocks.  From the menus, select **Options -> Application Preferences** and select the **Paths** tab.  Type the full path to the part library, e.g. /home/*{Username}*/PartsLibrary/ or C:\\Users\\ *{Username}*\\Documents\\PartsLibrary\\ , into the text-box labelled "Part Libraries" and click "OK".  Click the **Rebuild** button on the **Library Browser** dock and the new libraries will appear in the tree view.


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
