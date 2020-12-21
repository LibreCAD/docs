.. User Manual, LibreCAD v2.2.x

.. Default include
.. include:: /inclFiles/notice.rst


.. _console-tool:

The Console Tool
================

LibreCAD's console tool gives users certain functionality without having to open the actual GUI version of LibreCAD. To use it, users need to specify options in their console: ``librecad [options] ...``. Running ``librecad --help`` or ``librecad -h`` is a basic option that should show a list of all possible options. Running ``librecad --debug <level>`` or ``librecad -d <level>`` allows launchin LibreCAD in various debug levels from 0 being in no debug level whatsoever and 6 being the debugging level.


DXF2PDF Tool
----------------------

LibreCAD allows convertion of DXF drawings to PDF in console without any need to run the GUI. To do so, users can run ``librecad dxf2pdf [options] ...`` in their command line or terminal. This tool has its own set of options and its own help option which can be obtained by running `librecad dxf2pdf --help`` or `librecad dxf2pdf -h`` (or `librecad dxf2pdf`` with no options at all).