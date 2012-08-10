Libvisual
=========

What's Libvisual?
------------------

Libvisual is a library that acts as a middle layer between
applications that want audio visualisation and audio visualisation
plugins. It is aimed at providing a common interface between
applications developers with a need for audio visualisation and
developers who write visualisations.

Why Libvisual?
--------------

As an application developer, using libvisual provides you an easy way
to do audio visualisation. When using libvisual you'll have easy
access to all the visualizations that are written for libvisual.

As a plugin writer, libvisual provides a nice host for your plugin.
It runs analysis over the audio input usage and handles all everything
necessary for display in any libvisual-using application.

License
-------

The libvisual library that is in libvisual/ is licensed under the
LGPL.

The example applications in examples/ are licensed under the GPL.

The tools in tools/ are licensed under the GPL.

Development
-----------

If you would like to use libvisual for your applications, write
plugins or hack on the core. Please read HACKING. It contains some
very useful information regarding our coding policies and such.

Requirement
-----------

The core library is fairly self-contained and requires almost no
external dependency other than the standard C99 and C++11
libraries. GNU Gettext required for internationalization (note: it is
integrated into glibc on Linux).

The bundled examples, benchmarks and test programs mostly require SDL.

Compiling and installing
------------------------

####Configuration####

Building Libvisual requires CMake 2.8 or above. The command to
configure the build is:

    cmake .

To set a installation prefix, add `-DCMAKE_INSTALL_PREFIX=<prefix>` to
the commandline.

CMake comes with a wizard mode that hand holds you through the entire
configuration process, prompting you for each option. To use it, run:

    cmake -i .

Alternatively, CMake has a neat GUI that can be run with:

    cmake-gui .

####Building####

Once CMake configuration is completed, run Make to compile:

    make

####Installing####

After compilation is finished, install the built library with:

    make install