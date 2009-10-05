This repo contains the (upstream) sources of most necessary packages to build
matplotlib on windows. It also contains scons scripts to easily customize the
building process and 'install' the necessary files into one directory (install
by default, following the usual lib/include/bin UNIX convention). The goal is
to easily build the dependencies from scratch, for both 32 and 64 (amd64) bits
versions.

What's included::

        * png (version 1.2.40)
        * zlib (version 1.2.3)
        * freetype (version 2.3.9)

What will not be included::

        * python
        * numpy

TODO
====

wxpython.
