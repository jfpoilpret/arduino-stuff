arduino-stuff
=============

This repository contains all my Arduino projects and libraries.

All projects are created on [Eclipse](http://www.eclipse.org/) with an [Arduino plugin](http://www.baeyens.it/eclipse/), which I find easier to use when coding more than a dozen lines of C++ as errors are more easily found and fixed through Eclipse.
Hence every project can be directly compiled under the same environment but will need some adaptations to be compiled by the usual Arduino IDE. These adaptations are always the same for every project:

1. change the main project .CPP file extension into .INO
2. in the new .INO file, remove the first include line #include "ProjectName.h"

Also, for easy project software build, I use [arduino-cmake](https://github.com/queezythegreat/arduino-cmake).

Using arduino-cmake is easy but has 3 pre-requisites:

1. Install CMake and add it to your path
2. Install a CMake-supported build tool and add it to your path (I use Unix make, even in Windows)
3. Install Arduino IDE (this is required by arduino-cmake)

In order to build projects from command line, follow those instructions:

1. open a Windows command-line or Unix shell
2. cd build
3. cmake -G "Unix Makefiles" ..
4. make clean install

Command 3. above is needed the first time or after a change in one of CMakeLists.txt in the directory hierarchy.

In command 3. **-G "Unix Makefiles"** is necessary only the first time cmake is called. Afterwards, cmake will remember which kind of makefiles it has to generate.

CMake generates the following Make targets for every library:

TODO

CMake generates the following Make targets for every example project:

TODO

For my electronics circuits design, I use 2 useful applications, they are not free but they are quite cheap and very easy (and quick) to use:

- for diagrams, I use [sPlan 7.0](http://www.abacom-online.de/uk/html/splan.html) 
- for stripboards design and wiring, I use [LochMaster 4.0](http://www.abacom-online.de/uk/html/lochmaster.html) for the stripboard circuit. 

If you don't want to buy sPlan or LochMaster, you can still open these files with free viewers for [sPlan](http://www.abacom-online.de/updates/sPlan70_Viewer.exe) and [LochMaster](http://www.abacom-online.de/updates/LochMaster40_Viewer.zip).
