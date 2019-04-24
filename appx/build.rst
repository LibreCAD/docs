.. User Manual, LibreCAD v2.2.x


.. _build: 

Building from Source
====================

Building from the source code allows users to run the cutting-edge version of LibreCAD that includes fixes and possibly new features.  The instructions are as complete as possible to provide the necessary steps to allow any user to build LibreCAD from the source code, however some understanding of the operating system and installing of the required tools and dependencies is required.

The tools and dependencies required to build LibreCAD are:

    - git distributed version control system
    - Qt development framework
    - boost software library
    - muParser math expression parser library


Git and GitHub
--------------

The source code for LibreCAD is hosted on GitHub (https://github.com/LibreCAD/LibreCAD/).  The source can be download or cloned.  These instruction use "cloning" to allow users to update and build LibreCAD as the source code is updated.


Building on Linux
-----------------

Install Tools and Dependencies
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Install the required tools and libraries (Qt, boost, muparser, etc.):

::

   $ sudo apt install g++ gcc make git-core qtbase5-dev libqt5svg5-dev\
    qttools5-dev qtchooser qttools5-dev-tools libmuparser-dev librsvg2-bin\
    libboost-dev libfreetype6-dev libicu-dev pkg-config

You also have to either install the qt5-default package ("apt install qt5-default") or use qtchooser prior to running qmake (e.g., "qtchooser -qt5"). 


Clone the Repository
~~~~~~~~~~~~~~~~~~~~

This step only needs to be done once to create the initial cloned repository.  If local LibreCAD repository already exists continue to "**Update a Local Repository**" below.

Create a directory for the repository in the *home* directory:

::

   $ mkdir -p ~/develop/LibreCAD 

Clone the LibreCAD source code repository:

::

   $ cd ~/develop/
   $ git clone https://github.com/LibreCAD/LibreCAD.git

When this steps is finished a complete copy of the source code will found in the ~/develop/LibreCAD directory.


Update a Local Repository
~~~~~~~~~~~~~~~~~~~~~~~~~

Once a local repository has been created it can be updated as changes (bug fixes and / or new features) are added to the source code with:

::

   $ cd ~/develop/LibreCAD/
   $ git checkout master
   $ git pull -r


Build LibreCAD
~~~~~~~~~~~~~~

When the source code is copied to the local repository, ~/develop/LibreCAD/, it can be compiled with the following commands:

::

   $ cd ~/develop/LibreCAD/
   $ qmake -r
   $ make -j4

If the build is successful an executable is created, ~/develop/LibreCAD/unix/librecad, and LibreCAD can be launched by typing:

::

   $ ./unix/librecad &


Building on Windows
-------------------

https://wiki.librecad.org/index.php?title=How_to_built_LibreCAD_(master_branch)_on_Windows.
https://wiki.librecad.org/index.php/LibreCAD_Installation_from_Source#Building_LibreCAD_2.0_on_Windows


Install Tools and Dependencies
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Qt Framework
`````````````

Download Qt from : Qt download. Offline installer with MinGW is recommended instead of the Windows online installer. Qt-5.4.1 for Windows 32 bit (MinGW 4.9.1) is used as an example in this article.

Install Qt (including Qt-Creator) to C:\Qt\5.4\ (the default path prompted by Qt installer). The MinGW tools will be in C:\Qt\5.4\mingw491_32\bin by default.


muParser
````````

On Windows, muParser is not required to build LibreCAD since LibreCAD-2.0.4, because LibreCAD uses by default a patched version of muParser included within LibreCAD source.

boost and custom.pro
~~~~~

Download boost from: boost download.

Unzip the boost files to the directory:

::

  md C:\boost\

 -- the extracted folder would be: C:\boost\boost_1_60_0\ .

Verify that you have the file C:\boost\boost_1_60_0\booststrap.bat. You don't have to build boost in order to build LibreCAD, because LibreCAD only uses headers.

In librecad/src edit the custom.pro (or custom.pri) file accordingly :

   BOOST_DIR = C:/boost/boost_1_60_0/
   BOOST_LIBDIR = C:/boost/boost_1_60_0/




Cloning the source package
~~~~~~~~~~~~~~~~~~~~~~~~~~

To clone LibreCAD source code by command line:

::

   git clone https://github.com/LibreCAD/LibreCAD.git

On Windows, you may alternatively:

    - download and install msysgit
    - press the windows-key and then type git
    - select "Git GUI"
    - after the program loads select "Clone existing repository"

        - enter source location: git://github.com/LibreCAD/LibreCAD.git
        - enter target directory: where you want the project on your hard drive

    - press clone and then wait for it to download

Updating local source

    - press the windows-key and then type git
    - select "Git Bash"
    - input: cd /c/your_project_folder
    - input: git pull -r


Install dependencies
~~~~~~~~~~~~~~~~~~~~

Qt Framework
`````````````

Download Qt from : Qt download. Offline installer with MinGW is recommended instead of the Windows online installer. Qt-5.4.1 for Windows 32 bit (MinGW 4.9.1) is used as an example in this article.

Install Qt (including Qt-Creator) to C:\Qt\5.4\ (the default path prompted by Qt installer). The MinGW tools will be in C:\Qt\5.4\mingw491_32\bin by default.


muParser
````````

On Windows, muParser is not required to build LibreCAD since LibreCAD-2.0.4, because LibreCAD uses by default a patched version of muParser included within LibreCAD source.


Custom files
````````````

If you only care about building with Qt Creator, then you only need to read the boost and custom.pro section. The other custom files are for when you want to create an installer.

If you are planning to contribute, don't edit the librecad.pro, build-windows.bat and nsis-5.4.nsi files to fit your local settings. This would result in changes for git you have to care about in each commit, pull and push. Instead create the files custom.pro, custom-windows.bat and custom.nsh, which are ignored by git, and set your local settings there.


boost and custom.pro
````````````````````
Download boost from: boost download.

Unzip the boost files to the directory: C:\boost\ -- the extracted folder would be: C:\boost\boost_1_60_0\ .

Verify that you have the file C:\boost\boost_1_60_0\booststrap.bat. You don't have to build boost in order to build LibreCAD, because LibreCAD only uses headers.

In librecad/src edit the custom.pro (or custom.pri) file accordingly :

   BOOST_DIR = C:/boost/boost_1_60_0/
   BOOST_LIBDIR = C:/boost/boost_1_60_0/


custom-windows.bat
``````````````````

A command line building script file is added as scripts/build-windows.bat. To be able to use this batch file, you need to have your Qt and NSIS directories set up first. Default values for Qt_Dir, MINGW_VER and NSIS_DIR are set in file scripts/set-windows-env.bat:

   set Qt_DIR=C:\Qt\Qt5.3.2\5.3
   set NSIS_DIR=C:\Program Files (x86)\NSIS
   set MINGW_VER=mingw482_32

To change these default settings you have to create the file scripts/custom-windows.bat and overwrite the different settings without effect to the SCM (git).

Example for scripts/custom-windows.bat:

   set Qt_DIR=C:\Qt\5.4
   set NSIS_DIR=C:\PROGRA~2\NSIS
   set MINGW_VER=mingw491_32

There are issues with the NSIS_DIR path on 64 Bit Windows. When NSIS is installed in the Program Files (x86) folder and NSIS_DIR is added to the PATH, something goes wrong in the build process.  In this case use the command dir /X \ and get an output like this:

   09/02/2014  09:50 PM    <DIR>          PROGRA~1     Program Files
   10/27/2014  12:33 PM    <DIR>          PROGRA~2     Program Files (x86)
   08/16/2014  10:49 PM    <DIR>                       Qt

You need the short name of the Program Files (x86) folder. With that information set NSIS_DIR like following in scripts/custom-windows.bat to avoid the issues:

   set NSIS_DIR=C:\PROGRA~2\NSIS

custom.nsh

By default, LibreCAD uses NSIS to generate installers in Windows.

If you would like to build an installer for Windows, you will need the tool. You can use the lastest NSIS version.

You need to setup your Qt_Dir, Mingw_Ver and Qt_Version in the scripts\postprocess-windows\custom.nsh file if they don't match the default settings in scripts\postprocess-windows\nsis-5.4.nsi.
Example for scripts\postprocess-windows\custom.nsh:

   !define Qt_Dir "C:\Qt"
   !define Qt_Version "5.4"
   !define Mingw_Ver "mingw491_32"

These settings indicate Qt-5.4 is installed at C:\Qt\5.4 and it comes with Qt-Creator in C:\Qt\Tools\QtCreator and qmake.exe in C:\Qt\5.4\mingw491_32\bin

If you use an other Qt Version, e.g. Qt 5.4, where the master branch default is Qt 5.3.x, you have to use scripts\postprocess-windows\nsis-5.4.nsi for building the installer package.  Then you have to add this line to scripts/custom-windows.bat:

   set LC_NSIS_FILE=nsis-5.4.nsi

This line tells the build-win-setup.bat script to use nsis-5.4.nsi instead of nsis-5.3.nsi, which is currently default setting on master branch.


Building LibreCAD in Qt-Creator
```````````````````````````````

Launch Qt-Creator and open the librecad.pro project file within the LibreCAD source folder. Accept Qt path detected by Qt-Creator by clicking "Configure Project" button, if the project is not configured yet.

Take care about the Shadow build option in Debug and Release configuration. Disable this option in both configurations and save the project.

Select librecad as building target in Qt Creator (instead of tff2lff, which is another choice)

If everything is good up to this point, you can build and run LibreCAD within Qt-Creator.

Note that adding -j to the make arguments can significantly improve build time.
Building Windows installer

    press the windows-key and type qt
    select Qt 5.4 for desktop
    input: cd "C:\librecad\scripts" (or where ever your local source is)
    input: build-windows.bat

The last step of build-windows.bat is calling NSIS to create the LibreCAD-Installer.exe.
If everything was OK, the installer (LibreCAD-installer.exe) can be found in the generated folder within LibreCAD source folder.

(When LibreCAD Release version was built from Qt Creator, use build-win-setup.bat to create the windows installer.)

Other instructions:

    How_to_built_LibreCAD_(master_branch)_on_Windows.
    LibreCad from source


Building on macOS
-----------------

LibreCAD in MacPorts

Starting from version 2.0.2, LibreCAD is included MacPorts, which can be downloaded from http://www.macports.org/install.php

To install LibreCAD by MacPorts:

Optional, update package list

   $ sudo port selfupdate

Install the LibreCAD package

   $ sudo port install librecad

Following steps describe steps to build LibreCAD manually.
Alternative: Building from Downloaded Source Code
Install dependecies

Install QT and a new gcc, which should be version 4.7 or later (gcc-4.8 or later is recommended).

Install a version of Qt, boost and freetype, for example

   $ sudo port install gcc48 qt4-creator-mac qt4-mac boost freetype

or

   $ sudo port install gcc49 qt5-creator-mac qt5-mac boost freetype

Again, if you are running an OS/X version before Mavericks(10.9), you may have to select gcc-4.8 (or later) as the default compiler:

   $ sudo port select gcc

Accept mp-gcc48(or later) as the current active gcc.

Please note LibreCAD uses a patched version muparser, and the muparser package from MacPorts is not a required dependency any more.
Get Latest LibreCAD Source Code

To test the latest LibreCAD version, you may clone the official repository, and this cloning only needs to be done once. The latest development version of LibreCAD-2.0 is the master branch.

Alternatively, you may download source code zipballs/tarballs from github: https://github.com/LibreCAD/LibreCAD/releases

    $ sudo port install git-core
    $ mkdir -p ~/github
    $ cd ~/github
    $ git clone https://github.com/LibreCAD/LibreCAD.git

The last git command will clone the official LibreCAD repository to a folder ~/github/LibreCAD/ If you have a previous cloned repository, say, in ~/github/LibreCAD/ , you can update the code by:

   $ cd ~/github/LibreCAD/
   $ git fetch origin
   $ git checkout master
   $ git rebase origin/master

To be able to rely on pkg-config to find libraries, you may add the following to custom.pro

   $ echo "QT_CONFIG -= no-pkg-config" >> custom.pro

Select the right compiler

LibreCAD doesn't build with the default llvm-gcc42. For example you may choose gcc48 by:

   $ sudo port install gcc48
   $ sudo port select --set gcc mp-gcc48

Building LibreCAD

On OS/X 10.9 or newer, use spec macx-g++ is the default. Alternatively, you may use the system default clang++ compiler instead of gcc。

   $ qmake librecad.pro -r -spec macx-g++

On OS/X version 10.8 or older, run the following command to build a makefile in the LibreCAD source folder (as in our example, ~/github/LibreCAD/ )

   $ qmake librecad.pro -r -spec mkspec/macports

If the previous step is successful, you can build LibreCAD by issuing:

   $ make -j4

After a successful build, the generated executible of LibreCAD can be found as

   LibreCAD.app/Contents/MacOS/LibreCAD

By the building script

Alternatively, you may try the building script comes with LibreCAD at scripts/build-osx.sh to build an DMG file. On OS/X 10.9 or newer::

   $ cd ~/github/LibreCAD/
   $ cd scripts/
   $ ./build-osx.sh

On OS/X 10.8 or older, you may have to edit the build-osx.sh to qmake command lines like::

   qmake -r -spec mkspec/macports

to use the qmake mkspec shipped within LibreCAD source code. 
