# SCOREC Core #

[![Coverity Scan Build Status](https://scan.coverity.com/projects/6698/badge.svg)](https://scan.coverity.com/projects/scorec-core)

The SCOREC Core is a set of C/C++ libraries for unstructured mesh
simulations on supercomputers.

For more information, start at our
[wiki page](https://github.com/SCOREC/core/wiki)

### What is in this repository? ###

* PCU: Communication and file IO built on MPI 
* APF: Abstract definition of meshes, fields, and related operations
* GMI: Common interface for geometric modeling kernels
* MDS: Compact but flexible array-based mesh data structure
* PARMA: Scalable partitioning and load balancing procedures
* SPR: Superconvergent Patch Recovery error estimator
* MA: Anisotropic mixed mesh adaptation and solution transfer
* SAM: Sizing anisotropic meshes
* STK: Conversion from APF meshes to Sandia's STK meshes
* ZOLTAN: Interface to run Sandia's Zoltan code on APF meshes
* PHASTA: Tools and file formats related to the PHASTA fluid solver
* MTH: Math containers and routines
* CRV: Support for curved meshes with Bezier Shapes

### How do I get set up? ###

* Dependencies: CMake for compiling and MPI for running
* Configuration: Typical CMake configure and build.
  The `example_config.sh` shows common options to select,
  use a front-end like `ccmake` to see a full list of options
* Tests: the test/ subdirectory has tests and standalone
  tools that can be compiled by explicitly listing them as targets
  to `make`.
* Users: `make install` places libraries and headers in
  a specified prefix, application code can use these
  in their own compilation process.
  We also install pkg-config files for all libraries.

### Contribution guidelines ###

* Don't break the build
* See the `STYLE` file
* If in doubt, make a branch
* Run the ctest suite

### Who do I talk to? ###

* mailing list <scorec-pumi@lists.rpi.edu>
  (subscribe at https://lists.sympa.rpi.edu/wws/subscribe/scorec-pumi)
* Dan Ibanez <ibaned@rpi.edu>
* [Cameron Smith](https://www.scorec.rpi.edu/~cwsmith)
