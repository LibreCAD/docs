.. _blocks:


Blocks
======

A block is a group of entities. Blocks can be inserted into the same drawing more than once with different attributes, locations, scale and rotation angle (see image below). Such an instance of a block is usually called an "insert". Inserts have attributes just like entities and layers. An entity that is part of an insert can have its own attributes or share the attributes of the insert. Once created, inserts are still linked to the block they instantiate. The power of inserts is, that you can modify the block once and all inserts will be updated accordingly.

Creating and saving blocks is a useful way of inserting frequently used symbols e.g windows and doors in a house plan.

Blocks can contain useful text, dimensions and reference notes.

..  figure:: /images/guide_block.png
    :width: 740px
    :height: 402px
    :scale: 100
    :align: right
    :alt: LibreCAD Blocks


Creating a Block
----------------

Blocks can be created from scratch or they can be created from existing entities.
From Existing Entities

If you have already drawn the entities that you want to convert into a block use the following steps.

    #. From the menu select Block->Create Block
    #. Select the entities that will make up the block
    #. Specify the reference point of the block

        - The reference point is the base of the object when it is inserted

    #. Provide a unique name for the new block


From Scratch
------------

A block can also be created before placing it in the main drawing.

    #. From the menu select Block->Add Block. Alternately click the green plus (+) above the block list
    #. Provide a unique name for the new block
    #. The new, empty block will appear in the block list
    #. Select the new, empty block in the block list
    #. Select Block->Edit Block or click the edit block button in above the block list
    #. The new block will open in a new sub-window within the current drawing
    #. Draw new entities that will compose the new block.
    #. Close the window to return to your main drawing

.. note::

    The reference point for the newly created block is the origin of the coordinate system.
    The block must be inserted for it to appear in the main drawing.


Reusing blocks
--------------

    #. Create a block
    #. Select the block in the block list
    #. Press the save button in the block list
    #. Choose the location for saving
    #. Open a new drawing
    #. File -> Import -> Block
    #. Place the block.

You can also use the library browser. Set the path in Application Preferences, and have blocks in sub-directories of that path.

If you have the other drawing open, you can use:

    #. Press [ctrl]-c
    #. Select reference point
    #. Switch drawing
    #. [ctrl]-v
    #. Place the block.

