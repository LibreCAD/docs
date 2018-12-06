.. _install: 

Download and Install
====================

LibreCAD is available in two ways; as a general release, or as a "daily" release.  The general release is the most stable and is recommended for most users.  The daily, or "unstable", build represents the cutting edge of LibreCAD development and *might* contain bugs or new, incomlplete features under development.  The new features may or may not be included in next general release version.  LibreCAD can also be built from the source code so users can compile the most current code base for their platform.


Windows
-------

Links to the MS Windows installers can be found in the :ref:`Resources <downloads>`.


Mac OS/X
--------

Links to the installers for OS/X 10.9 can be found in the :ref:`Resources <downloads>`.

For other versions of OS/X, please follow build instructions in the :ref:`appendix <build>`.

.. note::
    If you an OS/X developer, please help us to improve DMG installers and MacPorts LibreCAD package.


Linux
-----

Ubuntu
~~~~~~

Official Ubuntu Repository
``````````````````````````
LibreCAD is available in the "Ubuntu Software Center" as "librecad" on Ubuntu 11.04 (Natty) and later. Just search and install the package "librecad", and it will be automatically installed and configured for your system, or to install it from the command line type::

   $ sudo apt-get install librecad


Daily and Stable Builds in Ubuntu PPA
`````````````````````````````````````
For those users who want a more current version of LibreCAD you can use the Stable or Daily Build PPAs, available for Ubuntu 10.10 (Maverick) and later.

For those that want to be more up to date than the distribution packages can use the Stable Build PPA.  First add the repository via the command line::

   $ sudo add-apt-repository ppa:librecad-dev/librecad-stable

And then update the software sources and install LibreCAD::

   $ sudo apt-get update
   $ sudo apt-get install librecad

For those that want to live on the bleeding edge and try out the newest features as they are pushed from the GitHub repository, First use the following repository::

   $ sudo add-apt-repository ppa:librecad-dev/librecad-daily
   $ sudo apt-get update
   $ sudo apt-get install librecad


Debian
~~~~~~

LibreCAD is available in the main repository of Debian 7.0 (Wheezy) and later as "librecad".  Use your favorite package manager (e.g. aptitude, synaptic, etc.) to install and configure it, or simply from command line type::

   $ sudo apt install librecad

You can always find the latest release in Debian Unstable.

If you are not running unstable/Sid, and still want to upgrade LibreCAD to a newer version in unstable/Sid, you may download the LibreCAD debs from Debian unstable, and manually install them in your system by "dpkg -i"::

   $ sudo dpkg -i /path/to/librecad_1.0.0~rc3+nolibs-1_i386.deb
   $ sudo dpkg -i /path/to/librecad-data_1.0.0~rc3+nolibs-1_i386.deb


Linux Application Repositories
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Packages are also available for the following Linux distributions through their respective repositories:

    - Debian (Stable and Unstable)
    - Ubuntu (Stable and Daily PPAs)
    - Arch Linux
    - Fedora
    - Gentoo
    - OpenSUSE

Links to the repository can be found in the :ref:`Resources <downloads>`_.


Other
-----

FreeBSD
~~~~~~~

LibreCAD is available from [ports], and can be installed as a binary package::

   # pkg install librecad


Build from Source Code
----------------------

For the most current up-to-date version of LibreCAD with the latest enhancments and fixes, it can be built for source.

