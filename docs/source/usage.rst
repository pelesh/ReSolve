Usage
=====

.. _installation:

Installation
------------

Dependencies:

- KLU, AMD and COLAMD libraries from SuiteSparse
- CUDA >= 11.4
- CMake >= 3.20

To build it:

.. code-block:: console

    $ git clone https://code.ornl.gov/peles/resolve.git
    $ mkdir build && cd build
    $ cmake ../resolve
    $ make


To install the library
In the directory where you built the library run

.. code-block:: console

    $ make install


Important Notes
----------------

You can find default Cmake Configurations in the CMakePresets.json file, which allows for easy switching 
between different CMake Configs. To create your own CMake Configuration we encourage you to utlize a 
`CmakeUserPresets.json` file. To learn more about cmake-presets please checkout the cmake docs
For example if you wanted to build and install ReSolve on a High Performance Computing Cluster such 
as PNNL's Deception or ORNL's Ascent we encourage you to utilize our cluster preset. Using this preset 
will set CMAKE_INSTALL_PREFIX to an install folder. To use this preset simply call the preset flag in 
the cmake build step.

.. code-block:: console

    cmake -B build --preset cluster

