.. User Manual, LibreCAD v2.2.x


.. _build: 

Building from Source
====================

Building from the source code allows users to run the cutting-edge version of LibreCAD that includes bug fixes and possibly new features.  LibreCAD can compiled to run on multiple operating systems; Linux, Microsoft Windows and macOS.    The process differs depending on the OS.  The instructions are as complete as possible to provide the necessary steps to allow any user to build LibreCAD from the source code, however some understanding of the operating system and installing of the required tools and dependencies is required.

The source code is hosted on GitHub and is common to all three operating systems.  It can be download as a "zip" archive or cloned using "git".  These instructions use the download option, however cloning is recommended if users want to update and build LibreCAD as the source code is updated.  See below for instructions for using :ref:`cloning <cloning>`.

The tools and dependencies required to build LibreCAD are:

    - c++ compiler and related utilities
    - Qt development framework
    - Boost C++ source library
    - muParser math expression parser library
    - git distributed version control system (optional)

If you are a developer and want to contribute to LibreCAD see the :ref:`Contributing <contributing>` section in the **Appendics**.


Download the Source Code
------------------------

Go to the LibreCAD Github page (https://github.com/LibreCAD/LibreCAD).  On the **<> Code** tab, click on the "Clone or Download" button and then click "Download ZIP".  Save the zip file "LibreCAD-master.zip".  When to download is complete, open the zip file and extract the contents to a suitable directory (e.g ~/dev/LibreCAD for Linux / macOS or C:\\dev\\LibreCAD for windows).


.. _buildLinux:

Building on Linux
-----------------

.. note::

    These instructions are for Debian based Linux distributions.

Install Tools and Dependencies
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Install the required tools and libraries (compiler, Qt, boost, muparser, etc.):

::

   $ sudo apt install g++ gcc make git-core qtbase5-dev libqt5svg5-dev\
    qttools5-dev qtchooser qttools5-dev-tools libboost-dev libmuparser-dev\
    librsvg2-bin libfreetype6-dev libicu-dev pkg-config

You also have to either install the qt5-default package ("apt install qt5-default") or use qtchooser prior to running qmake (e.g., "qtchooser -qt5"). 


Build LibreCAD
~~~~~~~~~~~~~~

Extract the contents of the source code zip file, "LibreCAD-master.zip", to a build directory (e.g ~/dev/LibreCAD).  Once the source code has been extracted compiled it with the following commands:

::

   $ cd ~/dev/LibreCAD/
   $ qmake -r
   $ make -j4

If the build is successful an executable is created, ~/dev/LibreCAD/unix/librecad, and LibreCAD can be launched by typing:

::

   $ ./unix/librecad &


.. _buildWin:

Building on Windows
-------------------

.. note::

    *This section is currently being updated.*  Please provide any feedback on the build process on the LibreCAD forum: http://forum.librecad.org/Help-wanted-to-build-on-Windows-td5717272.html

Also see:

   https://wiki.librecad.org/index.php/LibreCAD_Installation_from_Source#Building_LibreCAD_2.0_on_Windows


Install Tools and Dependencies
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Qt Framework
`````````````

The Windows version of Qt includes both the required framework library and the compiler.  Download the open source version of the **Qt Offline Installer** from Qt download <https://www.qt.io/download>.  Install Qt to the default path prompted by the installer.  On the *Select Components* page include the latest version of the compiler, **MinGW**, under the most recent version of Qt, e.g. `MinGW 7.3.0 32-bit` and `Qt 5.12.3` respectively.  No other components are needed.


Boost
`````

Download the current release of the boost library "zip" file from `Boost downloads <https://www.boost.org/users/download/>`_.  Create a folder named `boost` on `C:\\` and unzip the files to the folder.  Note the folder name the boost library was extracted to, e.g. `C:\\boost\\boost_1_70_0\\`.

*After* extracting the LibreCAD source code (below), open the `custom.pro` file in ` \\dev\\LibreCAD\\librecad\\src` folder and add the following two lines (**note the forward slashes in the path.**):

::

   BOOST_DIR = C:/boost/boost_1_70_0/
   BOOST_LIBDIR = C:/boost/boost_1_70_0/


muParser
````````

muParser is not required to build LibreCAD on Windows as a patched version of the muParser library has been included in the LibreCAD source code since LibreCAD version 2.0.4.


Build LibreCAD in Qt Creator
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Extract the contents of the source code zip file, "LibreCAD-master.zip", to a build directory (e.g C:\\dev\\LibreCAD).

.. note::

   Prior to building, update the `custom.pro` file with the boost paths as noted previously.

Launch Qt Creator (**Start -> All Programs -> Qt -> Qt Creator**) and open the `librecad.pro` project file within the LibreCAD source folder (**File -> Open File or Project**).  If the project is not yet configured accept the Qt paths detected by Qt Creator by clicking **Configure Project** button.

Click the **Project** icon on the left side of the Qt Creator window.  Disable the "Shadow build" option in Debug, Profile and Release configurations, and save the project (**File -> Save All**).

If everything is good up to this point, you can build and run LibreCAD in Qt Creator by clicking the **Build** icon on the lower left side.

If the build is successful an executable is created, `C:\dev\LibreCAD\Windows\librecad.exe`, and LibreCAD can be launched by Clicking **Start -> Run** and typing:

::

   > C:\dev\LibreCAD\windows\librecad.exe


.. _buildMac:

Building on macOS
-----------------

.. note::

    *This section is currently being updated.*  Please provide any feedback on the build process on the LibreCAD forum: http://forum.librecad.org/Help-wanted-to-build-on-MacOS-td5717273.html 



Install Tools and Dependencies
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Install QT and a new gcc, which should be version 4.7 or later (gcc-4.8 or later is recommended).

Install a version of Qt, boost and freetype, for example:

::

   $ sudo port install gcc48 qt4-creator-mac qt4-mac boost freetype

or

::

   $ sudo port install gcc49 qt5-creator-mac qt5-mac boost freetype

Again, if you are running a macOS version before Mavericks(10.9), you may have to select gcc-4.8 (or later) as the default compiler:

::

   $ sudo port select gcc

Accept mp-gcc48(or later) as the current active gcc.

Please note LibreCAD uses a patched version muparser, and the muparser package from MacPorts is not a required dependency any more.


Get the Source Code
~~~~~~~~~~~~~~~~~~~

Cloning the repository only needs to be done once to create the initial cloned repository.  If local LibreCAD repository already exists continue to "**Update the Repository**" below.


Cloning the Repository
``````````````````````

To test the latest LibreCAD version, you may clone the official repository, and this cloning only needs to be done once.

Alternatively, you may download source code zipballs/tarballs from github: https://github.com/LibreCAD/LibreCAD/releases:

::

    $ sudo port install git-core
    $ mkdir -p ~/github
    $ cd ~/github
    $ git clone https://github.com/LibreCAD/LibreCAD.git

The last git command will clone the official LibreCAD repository to a folder ~/github/LibreCAD/ 


Update the Repository
`````````````````````

Once a local repository has been created it can be updated as changes (bug fixes and / or new features) are added to the source code.  If you have a previous cloned repository, say, in ~/github/LibreCAD/ , you can update the code by:

::

   $ cd ~/github/LibreCAD/
   $ git fetch origin
   $ git checkout master
   $ git rebase origin/master


Build LibreCAD
~~~~~~~~~~~~~~

To be able to rely on pkg-config to find libraries, you may add the following to custom.pro

::

   $ echo "QT_CONFIG -= no-pkg-config" >> custom.pro


Select the right compiler
`````````````````````````

LibreCAD doesn't build with the default llvm-gcc42. For example you may choose gcc48 by:

::

   $ sudo port install gcc48
   $ sudo port select --set gcc mp-gcc48


On OS/X 10.9 or newer, use spec macx-g++ is the default. Alternatively, you may use the system default clang++ compiler instead of gcc:

::

   $ qmake librecad.pro -r -spec macx-g++

On OS/X version 10.8 or older, run the following command to build a makefile in the LibreCAD source folder (as in our example, ~/github/LibreCAD/ ):

::

   $ qmake librecad.pro -r -spec mkspec/macports

If the previous step is successful, you can build LibreCAD by issuing:

   $ make -j4

After a successful build, the generated executible of LibreCAD can be found as:

::

   LibreCAD.app/Contents/MacOS/LibreCAD


By the building script
``````````````````````

Alternatively, you may try the building script comes with LibreCAD at scripts/build-osx.sh to build an DMG file. On OS/X 10.9 or newer:

::

   $ cd ~/github/LibreCAD/
   $ cd scripts/
   $ ./build-osx.sh

On OS/X 10.8 or older, you may have to edit the build-osx.sh to qmake command lines like:

::

   qmake -r -spec mkspec/macports

to use the qmake mkspec shipped within LibreCAD source code.


.. _cloning:

Cloning the Source Code
-----------------------

"Git" is a *open source distributed version control system*, or for the purposes here, the means to obtain the source code needed to build LibreCAD.

Cloning the repository only needs to be done once to create the initial cloned repository.  If local LibreCAD repository already exists continue to "**Update the Repository**" below.


Clone the Repository (Linux and macOS)
````````````````````

Create a directory for the repository in the *home* directory:

::

   $ mkdir -p ~/dev/LibreCAD 

Clone the LibreCAD source code repository:

::

   $ cd ~/dev/
   $ git clone https://github.com/LibreCAD/LibreCAD.git

When this steps is finished a complete copy of the source code will found in the ~/dev/LibreCAD directory.


Update the Repository
`````````````````````

Once a local repository has been created it can be updated as changes (bug fixes and / or new features) are added to the source code with:

::

   $ cd ~/dev/LibreCAD/
   $ git checkout master
   $ git pull -r





Windows

Cloning thGit
```

There are several git clients available for MS Windows.  These build instructions utilize the "almost official" `Git for Windows <https://gitforwindows.org>`_ client.  Download the installer from https://git-scm.com/download/win and install it accepting the default values.

Another option is to use the `GitHub Desktop <https://desktop.github.com/>`_.e repository only needs to be done once to create the initial cloned repository.  If local LibreCAD repository already exists continue to "**Update the Repository**" below.


Cloning the Repository
``````````````````````


Via the Git GUI
^^^^^^^^^^^^^^^

To create the initial cloned repository, launch the Git GUI (**Start -> All Programs -> Git -> Git GUI**):

   - Select **Clone Existing Repository**
   - Enter the `Source Location`: git://github.com/LibreCAD/LibreCAD.git
   - Enter a 'Target Directory`: e.g. `C:\\dev\\LibreCAD`
   - Click **Clone** and then wait a few moments the download to complete (The Git GUI window will appear with the LibreCAD repository open)
   - Close the Git GUI window (**Repository -> Quit**)


Via the Git Command Line
^^^^^^^^^^^^^^^^^^^^^^^^

To clone LibreCAD source code open the Git command line (**Start -> All Programs -> Git -> Git CMD**) and type:

::

   > md \dev\LibreCAD
   > cd \dev
   > git clone https://github.com/LibreCAD/LibreCAD.git


Update the Repository
`````````````````````

Once a local repository has been created it can be updated as changes (bug fixes and / or new features) are added to the source code.  To update LibreCAD source code open the Git command line (**Start -> All Programs -> Git -> Git CMD**) and type:

::

   > cd \dev\LibreCAD
   > git pull -r



