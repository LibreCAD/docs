.. _fundamentals: 


Fundamentals
============

To be able to use LibreCAD effectively, there are a few concepts that need to be understood.  While drawings can be created with very little setup, as they become more complex further consideration to the elements of an entity is important.  This section offers an introduction to some concepts that are important to the creation of a drawing, but by no means is exhaustive.  The :ref:`Reference <reference>` section provides a description of the tools used to create and modify drawings.  General examples and guidence is offered in the :ref:`User Guide <guides>` section.


Entities
--------

An entity is a geometric shape; a line, circle, arc, etc. within a drawing.  A collection of entities form a drawing.

In addition to the basic information that describes the geometry of an entity, there are two more properties that further define the entity; the *Pen* and *Layers*.


Pen
---

A *pen* provides three additional properties to descibe a drawing entity:

    - color
    - width
    - type

Layers
------

Layers provide a means to organize drawing.  



A basic concept in computer aided drafting is the use of layers to organize a drawing. Every entity in a drawing is on exactly one layer and a layer can contain lots of entities. Typically entities with a common ‘function’ or common attributes are put on the same layer. E.g. you might want to put all axes in a drawing on a layer named ‘axes’ (see Figure 1 below). Layers can have their own attributes also (colour, line width, line style etc.). Each entity can have its own attributes or have its attributes defined by the layer it is placed on. In the latter case for example you can change the colour of all the entities on the “axes” layer by setting the colour (red for example) for that layer.

In traditional manual drafting, a similar approach was used. Whether for Engineering, Architectural, Construction drawing, etc. layers were used to show different aspects of a drawing — for example this could be a layer set up for showing centre lines on an engineering drawing or to show different building systems, such as wiring and air conditioning. The layers were often drawn on separate transparent sheets of paper. These sheets were then overlaid one on top of another to produce final drawings.


