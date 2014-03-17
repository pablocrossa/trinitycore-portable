# ![logo](http://www.trinitycore.org/f/public/style_images/1_trinitycore.png) TrinityCore-Portable


## Introduction

TrinityCore is a *MMORPG* Framework based mostly in C++.

It is derived from *MaNGOS*, the *Massive Network Game Object Server*, and is
based on the code of that project with extensive changes over time to optimize,
improve and cleanup the codebase at the same time as improving the in-game
mechanics and functionality.

It is completely open source; community involvement is highly encouraged.

If you wish to contribute ideas or code please visit our site linked below or
make pull requests to our [Github repository](https://github.com/TrinityCore/TrinityCore).

For further information on the TrinityCore project, please visit our project
website at [TrinityCore.org](http://www.trinitycore.org).

Modifications for portability by Pablo Crossa
trinitycore-portable.patch attached to allow patching of newer versions easily

## Requirements

+ Platform: Linux, Windows or Mac
+ Processor with SSE2 support (Unless you compile with cmake option "SKIP_SSE2")
+ ACE ≥ 5.8.3 (included for Windows)
+ MySQL ≥ 5.1.0 (included for Windows)
+ CMake ≥ 2.8.0
+ OpenSSL ≥ 1.0.0
+ GCC ≥ 4.7.2 (Linux only)
+ MS Visual Studio ≥ 12 (2013) (Windows only)


## Install

Detailed installation guides are available in the wiki for
[Windows](http://collab.kpsn.org/display/tc/How-to_Win),
[Linux](http://collab.kpsn.org/display/tc/How-to_Linux) and
[Mac OSX](http://collab.kpsn.org/display/tc/How-to_Mac).


For compilation on other architectures than x86/x64 you must use the cmake option "STANDARDIZE_ASM" (This will automatically enable SKIP_SSE2).

Example for compilation/installation:
cd ~
mkdir TCP
cd TCP
git clone https://github.com/pablocrossa/trinitycore-portable.git
mkdir build
mkdir server
cd build
cmake ../trinitycore-portable -DSKIP_SSE2=1 -DSTANDARDIZE_ASM=1 -DPREFIX=~/TCP/server
make
make install

This compiles on the Raspberry Pi's 'Raspbian' following the Wiki from TrinityCore with mild variations, mainly using unrar-free instead of unrar and using the libace-dev from Raspbian instead of compiling (compiling is slow)

I haven't tested this in any architecture other than ARM (it does compile on PowerPC) but others might work with GCC/ICC/MINGW

Just don't use CLANG (untested)...


## Reporting issues

Issues can be reported via the [Github issue tracker](https://github.com/TrinityCore/TrinityCore/issues?labels=Branch-3.3.5a).

Please take the time to review existing issues before submitting your own to
prevent duplicates.

In addition, thoroughly read through the [issue tracker guide](http://www.trinitycore.org/f/topic/37-the-trinitycore-issuetracker-and-you/) to ensure
your report contains the required information. Incorrect or poorly formed
reports are wasteful and are subject to deletion.


## Submitting fixes

Fixes are submitted as pull requests via Github. For more information on how to
properly submit a pull request, read the [how-to: maintain a remote fork](http://www.trinitycore.org/f/topic/6037-howto-maintain-a-remote-fork-for-pull-requests-tortoisegit/).


## Copyright

License: GPL 2.0

Read file [COPYING](COPYING)


## Authors &amp; Contributors

Read file [THANKS](THANKS)


## Links

[Site](http://www.trinitycore.org)

[Wiki](http://trinitycore.info)

[Documentation](http://www.trinitycore.net) (powered by Doxygen)

[Forums](http://www.trinitycore.org/f/)
