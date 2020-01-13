.. User Manual, LibreCAD v2.2.x


.. _blocks:

Blocks
======

*Blocks* are a small reusable drawings of commonly used objects such as bolts, furniture, electronic components, title blocks, etc.  Inserted blocks, also called *instances* or *inserts*, are composed of geometric shapes (lines, arcs, etc.) and can also include text and dimensions.  Blocks can be created within the current drawing and used within the drawing repeatedly.  LibreCAD also includes several libraries of blocks that can be inserted into a drawing.

.. figure:: /images/blockSample.png
    :width: 677px
    :height: 423px
    :align: center
    :scale: 75
    :alt: Block sample

    Block sample (Library Browser -> misc -> t-part)

There are two dock widgets for managing blocks.  The :ref:`Block List <widget-blockList>` dock for managing blocks *within the current drawing* and the :ref:`Library Browser <widget-libBrowser>` dock that displays a *collection of available blocks*.  Both widgets allow users to insert blocks into the current drawing, but there are a couple of important differences:

   - Blocks inserted from the **Block List**:

      #. Each block can be placed at a different locations, scale, rotation angle, and/or can be placed in an array.
      #. Blocks inserted from the same block in the **Block List** is called an *instance*.  If a block is inserted from the same block multiple times the *instances*  of the block are linked.  **Changes to one instance of the block will be reflected in all instances of that block.**

   - Blocks inserted from the **Library Browser**:

      #. Each block can be placed at a different location, rotation angle and/or scale.
      #. Blocks inserted multiple times will create a new instance of the block in the **Block List** each time it is inserted.  The blocks will numbered sequentially (*BlockName1*, *BlockName2*, ...)
      #. The inserted blocks will be independent of each other.


.. _ugblockslist:

Using the Block List
--------------------

Creating a Block
~~~~~~~~~~~~~~~~

Blocks can be created in the current drawing for use within the drawing.  There are two ways to create a block:

   #. From an existing object:

        - Select layer "0" and draw the object to be converted to a block.
        - Select all the entities that make up the object.
        - Click on the **Create Block** |icon12|.
        - Specify the reference point for the block.  The reference point is used to locate the object when it is inserted into the drawing.
        - Provide a unique name for the new block and click **OK**.  The new block will appear in the **Block List** dock.

   #. From an empty block:

        - Click on the **Add an empty block** icon |icon13|.  Provide a unique name for the new block and click **OK**.  The new block will appear in the **Block List** dock.
        - Select the new block in the **Block List** and click the **Edit the active block in a separate window** icon |icon16|.
        - Select layer "0" and draw the object.  The drawing's origin (0, 0) will become the reference point for the block.
        - Close the new block's drawing window and the block will be saved.


.. important::

    Layer "0" is a special layer that is equivalent to "no layer", similar to *color "By Block"* is equal to no specified color and *line type "By Block"* is equal to no specified line type.  It is also the default layer for new drawings.  **Genarally layer "0" should only be used when creating blocks and should be the only layer in the drawing.**

    Pay particular attention to the :ref:`Attributes <attributes>` when creating blocks.  In addition to the specific attributes, pen attributes (Color, Width, Line Type) also include "By Layer" and "By Block".

    #. Blocks with specific attributes (e.g. color set to blue, width set to 0.18 mm, etc) will retain those attributes when inserted.  The block needs to be edited to change any attribute.
    #. Blocks with the attributes set to "By Layer" will adopt the attributes of the layer they are inserted to.
    #. Blocks with the attributes set to "By Block" will intially adopt the attributes assigned to the layer.  The attributes can be changed with the **Attribute** tool.


Inserting Blocks
~~~~~~~~~~~~~~~~

.. note::

    Blocks will be inserted on the current layer.  Do not use layer "0".

Blocks can be inserted from the **Block List** or from the **Library Browser** (see :ref:`below <uglibbrowser>`).  Additional options are available when inserting blocks from the **Block List**.

To insert a block:

    - Select a layer.
    - Select a block in the **Block List**.
    - Click on the **Insert the active block** icon |icon18|.
    - Set the rotation angle, scale and array columns, rows and spacing as needed.
    - Place the block at the desired location within the drawing.
    - Place additional copies of the block or press [Esc] to exit the command.

Additional options are available when inserting a block through the *Tool Option* bar. 

.. figure:: /images/toolOptions/toBlockInsert.png
    :width: 617px
    :height: 34px
    :align: center
    :scale: 75
    :alt: Block insert tool option bar

    - Block can be rotated by the specified *Angle* and scaled by the *Factor*.
    - A pattern of blocks can be created by specifying an *Array* (number of columns and rows) and *Spacing* (space between the columns and rows).

In the same block insertion, it is possible to combine transformations and pattern: a pattern of defined size and spacing is created then the pattern is rotated and finally the block entities are scaled but the spacing distances remain as defined.

    - Select a block in the **Block List**.
    - Click on the **Insert the active block** icon |icon18|.
    - Set the angle of rotation in *Angle* field as required. (See :ref:`Angles<angles>` in **Fundamentals**.)
    - Set the scale factor in *Factor* field as required.  It is the same scale factor as in :ref:`Modify <tool-modify>`.
    - Define the numbers of columns and rows in *Array* area to create a pattern as required.  Otherwise keep 1 in both fields to insert a single block.
    - Set the *Column spacing* distance between each column of the array. This is the distance between 2 block insertion points of 2 adjacent columns. 
    - Set the *Row spacing* distance between each row of the array. This is the distance between 2 block insertion points of 2 adjacent rows. 
    - Place the block at the desired location within the drawing. The insertion point of the pattern is the insertion point of the lower-left item in the array.

.. note::
    Using an array will treat all blocks in the array as a *single block instance*.  Selecting one entity of the array will select the all blocks in the array. If this is not the intent, insert multiple copies from the block list or create additional copies with the "Move / Copy" tool.

.. note::
    Blocks can also be cut, copied, and pasted using the normal edit commands.  For example, to copy a block from one drawing to another:

    - Select a block in the current drawing.
    - Press [Ctrl]+[c] (or **Edit -> Copy** from the menu)
    - Within the current drawing or switch to a new drawing and press [Ctrl]+[v] (or **Edit -> Paste**)
    - Specified a point in the drawing to place the block.


Editing a Block
~~~~~~~~~~~~~~~

    - Select a block in the **Block List** and click the **Edit the active block in a separate window** icon |icon16|.
    - Edit the block as necessary.
    - Close the block's drawing window and the block will be saved and all instances of the block will be updated in the current drawing.


Saving Blocks
~~~~~~~~~~~~~

Blocks can be saved to a separate file and used in other drawings or added to a user library.  To save the block:

    - Select a block in the **Block List**.
    - Click the **Save the active block to a file** icon |icon17|.
    - Select a file location, specify a file name and click **Save**.

.. admonition:: Saving blocks

    When saving blocks to be added to the block library it is *recommended that the block's entities be placed on* **layer "0"** and layer "0" is the only layer in the drawing.  Blocks adopt the attributes of the layer they are inserted on.  If multiple layers are used when creating the block, those layers will be added to the drawing with unintended consequences.


.. _uglibbrowser:

Using the Library Browser
-------------------------

LibreCAD includes several categories of blocks in its library; algorithm, elektro, plan/air_water, plan/architect, etc.  To use blocks from the :ref:`Block Library <widget-libBrowser>`, select the block from the tree view, click **Insert** and specify a point in the drawing to place the block.


.. admonition:: Recommendation

    When using blocks from the library, insert a *single* *insert* from the **Library Browser** and then insert subsequent *instances* from the **Block List**.  Inserting the block from the **Block List** retains the link between instances of the same block insert.  If a block is edited from the **Block List**, all instances of the block will show the changes.

    Only insert multiple *inserts* of a block from the **Library Browser** if they are to be independent.


Blocks located in a library can be rotated and scaled through the *Tool Option* bar when inserted. The rotation angle and the scale factor behave as they do for a block inserted from the **Block List**.

.. figure:: /images/toolOptions/toBlockLib.png
    :width: 317px
    :height: 33px
    :align: center
    :scale: 75
    :alt: Block from library insertion tool option bar

To insert a block:

    - Select a layer.
    - Select a block in the **Library Browser**.
    - Click on the **Insert** button.
    - Set the rotation angle and scale as needed. 
    - Place the block at the desired location within the drawing.
    - Place additional copies of the block or press [Esc] to exit the command.


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
