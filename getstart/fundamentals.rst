.. _fundamentals: 


Fundamentals
============

To be able to use LibreCAD effectively, there are a few concepts that need to be understood.  While drawings can be created with very little setup, as they become more complex further consideration to the elements of an entity is important.  This section offers an introduction to some concepts that are important to the creation of a drawing, but by no means is exhaustive.  The :ref:`Reference <reference>` section provides a description of the tools used to create and modify drawings.  General examples and guidence is offered in the :ref:`User Guide <guides>` section.


Entities
--------

An entity is a geometric shape; a line, circle, arc, etc. within a drawing.  A collection of entities form a drawing.

In addition to the basic information that describes the geometry of an entity, there are two more properties that further define the entity:

    - *Pen* - describes the appearance of an entity, either on screen or in printed output.
    - *Layers* - organize and manage the drawing's entities.


Pen
---

A *pen* provides three additional properties to descibe a drawing entity:

    - Color - LibreCAD has 16 default colors, but supports the RGB color space (#000000 to #FFFFFF).  The initial color for entities is black.
    - Width - The default line width is 0.00mm.  Line widths supported are up to 2.11mm.
    - Line Type - The default line type is "Continuous" (e.g. solid), but other line types included with LibreCAD are Dot, Dash, Divide, Center, and Border.

Each of these properties *can* have a specific meaning, but a complete description is beyond the scope of this manual and variy by industry or an organizations standards.  Additonal information for setting the pen can be found ...somewhere.


Layers
------

Layers provide a means to organize drawing and manage the properties of multiple entities.  See :ref:`Layers <layers>` in the **User Guides** for more details.


