.. User Manual, LibreCAD v2.2.x


.. _build: 

Building from Source
====================

Building from the source code allows users to run the cutting-edge version of LibreCAD that includes bug fixes and possibly new features.  LibreCAD can be compiled to run on multiple operating systems; Linux, Microsoft Windows, and macOS.  The process differs depending on the OS.

 .. important::
    The instructions are as complete as possible to provide the necessary steps to allow any user to build LibreCAD from the source code, however some understanding of the operating system and installation of the required tools and dependencies is required.  The instructions are intended for users that want to try the cutting-edge version of LibreCAD and are **not** intended to replace the instructions for building packages or contributing to the LibreCAD project.

    If you are a developer and want to contribute to LibreCAD see the :ref:`Contributing <contributing>` section in the **Appendices**.

The tools and dependencies required to build LibreCAD are:

    - C++ compiler and related utilities
    - Qt development framework
    - Boost C++ source library
    - muParser math expression parser library
    - git distributed version control system (optional)


Download the Source Code
------------------------

The source code is hosted on GitHub and is common to all three operating systems.  It can be download as a "zip" archive or cloned using "git".  These instructions use the download option.

Go to the `LibreCAD GitHub page <https://github.com/LibreCAD/LibreCAD>`_ to download the source code.  On the **<> Code** tab, click on the "Clone or Download" button and then click "Download ZIP".  Save the zip file; `LibreCAD-master.zip`.

Cloning is suggested if users want to build LibreCAD more frequently as the source code is updated.  More information about GitHub, git tools, and creating a local source code repository can be found on `LibreCAD's Developer's wiki <https://github.com/LibreCAD/LibreCAD/wiki>`_.


.. _buildLinux:

Building on Linux
-----------------

.. note::

    These instructions are for building LibreCAD on **Debian** and other derivatives.  Further instructions for building LibreCAD on other Linux distributions (openSUSE, Red Hat, FreeBSD) and generic Unix can be found in LibreCAD's GitHub Developer's wiki in the **Build from source** section. 


Install Tools and Dependencies
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Install the required tools and libraries (compiler, Qt, boost, muparser, etc.):

::

   $ sudo apt install g++ gcc make qtbase5-dev libqt5svg5-dev qttools5-dev\
    qtchooser qttools5-dev-tools libboost-dev libmuparser-dev librsvg2-bin\
    libfreetype6-dev libicu-dev pkg-config

You also have to either install the qt5-default package; ``apt install qt5-default``, or use qtchooser prior to running qmake; ``qtchooser -qt5``. 


Build LibreCAD
~~~~~~~~~~~~~~

Create a development directory for the source code and related libraries; e.g ``~/dev/``.  Extract the contents of the source code zip file, `LibreCAD-master.zip`, to the development directory.  When complete a complete copy of the source code will found in the `~/dev/LibreCAD-master` directory.  Compiled LibreCAD with the following commands:

::

   $ cd ~/dev/LibreCAD-master/
   $ qmake -r
   $ make -j4

If the build is successful an executable is created, `~/dev/LibreCAD-master/unix/librecad`, and LibreCAD can be launched by typing:

::

   $ ./unix/librecad &


.. _buildWin:

Building on Windows
-------------------

Building LibreCAD on Windows is a little more involved and requires a few additional steps.  Please read these instructions carefully.

.. note::

	Detailed instructions for building LibreCAD on Windows, including instructions for building LibreCAD in **Visual Studio 2013** and newer, can be found on the GitHub Developers wiki (https://github.com/LibreCAD/LibreCAD/wiki) in the **Build from source** section.


Install Tools and Dependencies
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Qt Framework
`````````````

The Windows version of Qt includes both the required framework library and the compiler.  Download the *open source* version of the **Qt Online Installer** from Qt download <https://www.qt.io/download>.  Launch the installer accepting the defaults.  Install Qt to the default path prompted by the installer, e.g. `C:\\Qt`.  On the *Select Components* page expand the tree view under the most recent version of Qt, e.g. `Qt 5.12.3`, and select the latest version of the **MinGW** compiler; `MinGW 7.3.0 (32-bit or 64 bit as required)`.  No other components are needed.


Boost
`````

Download the current release of the boost library "zip" file from Boost downloads <https://www.boost.org/users/download/>.  Click on the link to download the current Windows library, e.g. `boost_1_70_0.zip` and save the file. 


muParser
````````

muParser is not required to build LibreCAD on Windows as the library is now included with the LibreCAD source code.


Build LibreCAD in Qt Creator
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Create a development folder for the source code and related libraries, e.g `C:\\dev\\`.  Extract the contents of the source code zip file, "LibreCAD-master.zip".  When complete a copy of the source code will found in the `C:\\dev\\LibreCAD-master` folder.

Extract the boost library the files to the development folder.  Note the folder name the boost library was extracted to, e.g. `C:\\dev\\boost_1_70_0\\`.

	*After* extracting the LibreCAD source code, open the `custom.pro` file in `.\\LibreCAD-master\\librecad\\src` under the development folder and add the following two lines (**note the forward slashes in the path.**):

	::

	   BOOST_DIR = C:/dev/boost_1_70_0/
	   BOOST_LIBDIR = C:/dev/boost_1_70_0/


After completing the required edit, launch Qt Creator (**Start -> All Programs -> Qt -> Qt Creator**) and open the `librecad.pro` project file from the LibreCAD source folder (**File -> Open File or Project** and go to `C:\\dev\\LibreCAD-master\\`).  The project should open to **Configure Project**.  Ensure a "kit", e.g. `Desktop Qt 5.12.3 MinGW 32-bit` is checked and click the **Configure Project** button.  It will take a few moments for the project to open and parse.

Click the **Project** icon on the left side of the Qt Creator window.  Disable the "Shadow build" option in the *Debug*, *Profile* and *Release*  build configurations.  Each build configuration can be selected from the drop down below **Build Settings**. Save the project (**File -> Save All**).

With the configuration complete, run the build process in Qt Creator by clicking the **Build** icon on the lower left side.  If the build is successful an executable is created: .\\LibreCAD-master\\windows\\librecad.exe.


.. important::

	Several *Dynamic-link libraries (DLL)* are required to run LibreCAD.  The DLLs are found in the C:\\Qt\\5.12.3\\mingw73_32\\bin folder (or mingw73_64) and need to be copied to the same directory as the executable (or included in the path). The DLLs are:

	   - libgcc_s_dw2-1.dll
	   - libstdc++-6.dll
	   - libwinpthread-1.dll
	   - Qt5Core.dll
	   - Qt5Gui.dll
	   - Qt5PrintSupport.dll
	   - Qt5Svg.dll
	   - Qt5Widgets.dll

Once the DLLs have been copied to the executable folder, LibreCAD can be launched by Clicking **Start -> Run** and typing:

::

   > C:\dev\LibreCAD-master\windows\librecad.exe


.. _buildMac:

Building on macOS
-----------------

There are a few options for compiling LibreCAD for the macOS.  This method uses the **LLVM Compiler Infrastructure** and the **Homebrew Package Manager**.  Refer to the `Github Developer's wiki <https://github.com/LibreCAD/LibreCAD/wiki/Build-from-source#macos>`_ for additional methods.

Install Tools and Dependencies
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

From the command prompt, download and install Homebrew with:

::

    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"

Further details are available on the `Homebrew website <https://brew.sh/>`_.

Install the latest versions of boost and qt5 with Homebrew:

::

    brew install boost qt5


Build LibreCAD
~~~~~~~~~~~~~~

Create a development directory for the source code and related libraries; e.g ``~/dev/``.  Extract the contents of the source code zip file, `LibreCAD-master.zip`, to the development directory.  When complete a complete copy of the source code will found in the `~/dev/LibreCAD-master` directory.  Change to the source code directory with:

::

    cd ~/dev/LibreCAD-master/

Build LibreCAD by running qmake.  Note that during the installation step above (brew install qt5), the binaries have not been linked to `/usr/local`.  In order to use qmake, either:

::

    use the full path: ``/usr/local/Cellar/qt5/5.7.0/bin/qmake librecad.pro -r -spec macx-clang

Or run ``brew link qt5 --force``, which will allow you to simply write qmake at the prompt:

::
    qmake librecad.pro -r -spec macx-clang

Now build the application.  At the prompt run:

::

    make -j4

If the previous steps were successful, an application named **LibreCAD.app** will be in the build directory.  Run it at the command prompt by typing either:

::

    open LibreCAD.app, or
    LibreCAD.app/Contents/MacOS/LibreCAD

.. note::

    *The macOS build section been revised, but not tested.*  Please provide any feedback on the build process on the LibreCAD forum: http://forum.librecad.org/Help-wanted-to-build-on-MacOS-td5717273.html 

