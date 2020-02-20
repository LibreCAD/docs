.. User Manual, LibreCAD v2.2.x

.. Default include
.. include:: /inclFiles/notice.rst


.. _about:

About
=====

**LibreCAD**, the `web site <http://librecad.org>`_, `wiki <https://dokuwiki.librecad.org/>`_ and the `User Manual <https://librecad.readthedocs.io/>`_ are all user supported and represents the efforts numerous *volunteers* committing countless hours of time to create, improve and support the application and documentation.  Support is free directly from the large dedicated community of users, contributors and developers.


The Application
---------------

History
~~~~~~~

**LibreCAD** is a **free Open Source** 2D CAD application using the cross-platform framework **Qt**.  That means it works with multiple operating systems; Windows, Apple and Linux. 

The project started around 2010 as a fork of QCAD 2.0.5.0. It began as a project to build CAM capabilities into the community version of QCAD for use with a Mechmate CNC router.  This gave rise to CADuntu.  The project was known as CADuntu only for a couple of months before the community decided that the name was inappropriate.  After some discussion within the community and research on existing names, CADuntu was renamed to **LibreCAD**.

Since QCAD CE was built around the outdated Qt3 library, it had to be ported to Qt4 before additional enhancements.  Porting the rendering engine to Qt4 proved to be a large task, so initially LibreCAD, the 1.0.0 series, still depended on the Qt3 support library. Thanks to our master developer Rallaz, the Qt4 porting was completed during the development of 2.0.0 series and LibreCAD has become Qt3 free.  The latest version of LibreCAD, the 2.2.0 series, requires the Qt5 framework.


Features
~~~~~~~~

LibreCAD has the following features: 

   - reads DWG and DXF files
   - writes DXF, SVG, PDF, and more...
   - drawing entities include line, polyline, spline, circle, ellipse, text, dimension, blocks and hatches
   - advanced snapping system
   - custom toolbars and menus
   - highly customizable user interface
   - plugin system

As free software you can redistribute it and/or modify it under the terms of the see :ref:`GNU General Public License <gpl-license>` version 2 (GPLv2) as published by the Free Software Foundation.


The User Manual
---------------

The user manual is a compilation from many sources.  The manual includes detailed instructions on obtaining, installing and configuring LibreCAD in the :ref:`Getting Started <getstart>` section.  It contains the technical descriptions of the tools, functions, widgets, etc. in the :ref:`Reference <reference>` section and generic instructions on how to do a few things with LibreCAD in the :ref:`User Guide <guides>` section. There is also further information and links to additional resources in the :ref:`appendices <appendix>`.

The manual is best viewed with a minimum screen width of about 1100 pixels to display the menu and content in a browser.  Clicking the “LibreCAD” text or icon at the top of the menu will return to the User Manual’s home page.  On smaller devices, such as a mobile device, a minimum screen width of 800 pixels is recommended to display to content.  At screen resolutions of 800 pixels or less, the navigation menu is hidden.  It can be made visible by clicking the “hamburger” icon.  Clicking the “LibreCAD” text top of the window will return to the home page.

This manual uses screen captures of LibreCAD installed on Linux. While the images may appear slightly different on Windows or MacOS, the application layout and menu commands will be the same.


Conventions
~~~~~~~~~~~

   - Internal and external links appear in blue.
   - Clicking on the embedded images will display them full size. Click the browser’s “back button ” to return to the manual.
   - Application menu paths are shown in bold and levels are separated with “->”, e.g. **File -> New.**
   - Dialogue box titles are shown in **bold** with matching case.
   - Dialogue box labels are enclosed in quotes, ” ”, with matching case.
   - Tab titles are enclosed in quotes with matching case.
   - Button labels are enclosed in quotes with matching case.
   - Key combinations are shown with the keyboard labels enclosed in square brackets with a “+” between keys, e.g. [Ctrl]+[C].
   - Text typed at the command line (OS commands, CAD commands or coordinates) is shown in a text box:

      ::

         li
         0,0
         0,50
         k
      


Contributors
~~~~~~~~~~~~

There are many people who have contributed to the **LibreCAD User Manual**.  Those contributions have come via LibreCAD's forum, wiki and source code.

Some of those that have contributed, directly or indirectly, include:

.. list-table::
   :align: center
   :widths: 50, 50

   *  - Armin Stebich
      - Bob Woltz
   *  - Chris G
      - Clive Tubb
   *  - David Huff
      - dellus
   *  - Dli, 
      - Fabrice
   *  - Ferdi
      - Gary S  (Maintainer)
   *  - R\. van Twisk
      - Ravas
   *  - Richard M Brown
      - Stano Sitar


Copyright
~~~~~~~~~

This work is licensed under the Creative Commons Attribution 4.0 International License. To view a copy of this license, visit http://creativecommons.org/licenses/by/4.0/ or send a letter to Creative Commons, PO Box 1866, Mountain View, CA 94042, USA.


.. toctree::
   :maxdepth: 1

