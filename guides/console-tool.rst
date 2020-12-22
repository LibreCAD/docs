.. User Manual, LibreCAD v2.2.x

.. Default include
.. include:: /inclFiles/notice.rst


.. _console-tool:

The Console Tool
================

LibreCAD's console tool gives users certain functionality without having to open the actual GUI version of LibreCAD. To use it, users need to specify options in their console: ``librecad [options] ...``. Running ``librecad --help`` or ``librecad -h`` is a basic option that should show a list of all possible options. Running ``librecad --debug <level>`` or ``librecad -d <level>`` allows launchin LibreCAD in various debug levels from 0 being in no debug level whatsoever and 6 being the debugging level.


DXF2PDF Tool
----------------------

LibreCAD allows convertion of DXF drawings to PDF in console without any need to run the GUI. To do so, users can run ``librecad dxf2pdf [options] ...`` in their command line or terminal. This tool has its own set of options and its own help option which can be obtained by running `librecad dxf2pdf --help`` or ``librecad dxf2pdf -h`` (or simply ``librecad dxf2pdf`` with no options at all).

In a nutshell, users can use it to convert a DXF file or multiple DXF files to a single multi-page PDF or multiple PDFs. It can be done without specifying any options other than the input filename: ``librecad dxf2pdf file_name.dxf``. The output file is saved in the executable folder under the name of ``file_name.pdf``. If multiple (N) DXF files are selecred (``librecad dxf2pdf file_name1.dxf file_name2.dxf ... file_nameN.dxf``) then N PDF files are made. It is also possible to convert DXF files to PDF and put the results in a single multipage PDF ``outfile.pdf`` as follows: ``librecad dxf2pdf -o outfile.pdf file_name1.dxf file_name2.dxf ... file_nameN.dxf``. The same approach can be used if there is a single DXF file input but the outpit filename needs specification.

There are other options available which can be obtained by running ``librecad dxf2pdf --help`` and at this stage include

``
  -h, --help                  Displays help.
  -v, --version               Displays version information.
  -a, --fit                   Auto fit and center drawing to page.
  -c, --center                Auto center drawing on page.
  -k, --grayscale             Print grayscale.
  -m, --monochrome            Print monochrome (black/white).
  -p, --paper <WxH>           Paper size (Width x Height) in mm.
  -r, --resolution <integer>  Output resolution (DPI).
  -s, --scale <double>        Output scale. E.g.: 0.01 (for 1:100 scale).
  -f, --margins <L,T,R,B>     Paper margins in mm (integer or float).
  -z, --pages <HxV>           Print on multiple pages (Horiz. x Vert.).
  -o, --outfile <file>        Output PDF file.
  -t, --directory <path>      Target output directory.
``