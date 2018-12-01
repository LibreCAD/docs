.. _install: 

Installation Instructions
=========================

Linux
-----

Ubuntu
~~~~~~

Package in the official ubuntu repository
`````````````````````````````````````````
For ubuntu, LibreCAD is available in the "Ubuntu Software Center" as "librecad" on Ubuntu 11.04 (Natty) and later. Just search and install the package "librecad", and it will be automatically installed and configured for your system.

To install it by command line:

   $ sudo apt-get install librecad

Daily and Stable Builds in Ubuntu PPA
`````````````````````````````````````
For those users who want to live on the bleeding edge and try out the newest features as they are pushed to our github repository, you can use our Daily Build PPA, available for Ubuntu 10.10 (Maverick) and later. First, install LibreCAD as per above directions. Then:

   $ sudo add-apt-repository ppa:librecad-dev/librecad-daily

If you are not willing to take the risks, but want to be more up to date than the distribution packages, use the Stable Build PPA instead::

   $ sudo add-apt-repository ppa:librecad-dev/librecad-stable

To stay up to date with the newest build, simply use Ubuntu's "Update Manager" or::

   $ sudo apt-get update
   $ sudo apt-get install librecad

That command will install the most recent code from our GitHub repository. Please report any bugs at https://github.com/LibreCAD/LibreCAD/issues.


Debian
~~~~~~

LibreCAD is available in the main repository of Debian 7.0 (Wheezy) and later as "librecad". Use your favorite package manager (e.g. aptitude, synaptic, etc.) or simply from command line::

   $ sudo apt-get install librecad

will install and configure it for you for every architecture. You can always find the latest release in Debian unstable.

If you are not running unstable/sid, and still want to upgrade LibreCAD to a newer version in unstable/sid, you may download the LibreCAD debs from Debian unstable, and manually install them in your system by "dpkg -i"::

   $ sudo dpkg -i /path/to/librecad_1.0.0~rc3+nolibs-1_i386.deb

   $ sudo dpkg -i /path/to/librecad-data_1.0.0~rc3+nolibs-1_i386.deb


Other Distributions
~~~~~~~~~~~~~~~~~~~

Packages are also available for the following Linux distributions:
    - Arch Linuxx
    - Fedora
    - Gentoo
    - OpenSUSE


Windows
-------

Stable releases
~~~~~~~~~~~~~~~

Installers can be downloaded from LibreCAD's Official` Release page <https://github.com/LibreCAD/LibreCAD/releases>`_ on GitHub.  Installers are also available from `SourceForge <https://sourceforge.net/projects/librecad/files/Windows/>`_.

Nightly builds
~~~~~~~~~~~~~~

"Nightly builds" are pre-release versions for people interested in testing updates.  These versions represent the bleeding edge of LibreCAD development and *might* contain bugs or new features under development.  New features may or may not be included in next release version.


Mac OS/X
--------

OS/X installers for OS/X 10.9 are available at `SourceForge <http://sourceforge.net/projects/librecad/files/OSX/>`_.

For other versions of OS/X, please follow instructions to build LibreCAD from source code (see appendix XXX)

.. note::
    If you an OS/X developer, please help us to improve DMG installers and MacPorts LibreCAD package.

Other
-----

FreeBSD
~~~~~~~

LibreCAD is available from [ports], and can be installed as a binary package::

   # pkg install librecad


Android via Ubuntu Chroot
~~~~~~~~~~~~~~~~~~~~~~~~~


Build from Source Code
----------------------

For the most current up-to-date version of LibreCAD with the latest enhancments and fixes, it can be built for source.

