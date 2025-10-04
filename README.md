# OpenApocalypse [![Tweet](https://img.shields.io/twitter/url/http/shields.io.svg?style=social)](https://twitter.com/intent/tweet?text=Are%20you%20a%20fan%20of%20X-Com%20Apocalypse?%20OpenApoc%20is%20a%20clone%20of%20this%20great%20game%20-%20contribute!%20https://github.com/OpenApoc/OpenApoc&hashtags=games,openapoc,xcom)

> OpenApoc is an open-source re-implementation of the original [X-COM: Apocalypse](https://www.ufopaedia.org/index.php/Apocalypse), that requires the original files to run, licensed under the GPL3 and written in C++ / SDL2. It was originally founded by PmProg in July 2014, and has since grown a significant [community](https://www.ufopaedia.org/index.php/Credits_(OpenApoc)).

[![Linux Build Status](https://img.shields.io/travis/OpenApoc/OpenApoc?branch=master&label=Travis%20Linux&logo=Travis%20CI&logoColor=ffffff&labelColor=282828)](https://travis-ci.com/github/OpenApoc/OpenApoc)
[![Windows Build Status](https://img.shields.io/appveyor/build/OpenApoc/openapoc?branch=master&label=AppVeyor%20Windows&logo=appveyor&logoColor=ffffff&labelColor=282828)](https://ci.appveyor.com/project/openapoc/openapoc/branch/master)
[![Openapoc issues](https://img.shields.io/github/issues-raw/OpenApoc/OpenApoc?color=1182c3&logo=GitHub&labelColor=282828)](https://github.com/openapoc/openapoc/issues)
[![Translate OpenApoc](https://img.shields.io/badge/Translate-Openapoc-blue.svg)](https://www.transifex.com/x-com-apocalypse/apocalypse/)
[![OpenApoc GPL3 license](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://github.com/OpenApoc/OpenApoc/blob/master/LICENSE)\
[![Openapoc forum](https://img.shields.io/badge/Visit%20our-forum-orange.svg)](http://openapoc.org)
[![Openapoc IRC chat](https://img.shields.io/badge/IRC-devs%20chat-brightgreen.svg)](http://webchat.freenode.net/?channels=openapoc)
[![Openapoc Discord](https://img.shields.io/discord/142798944970211328?label=Discord&logo=discord&logoColor=ffffff&labelColor=7289DA&color=2c2f33)](https://discord.gg/d6DAHEb) 
[![Openapoc Facebook](https://img.shields.io/static/v1?label=FB&logo=Facebook&logoColor=ffffff&message=Subscribe%20|%20755&color=282828&labelColor=1877f2)](https://fb.com/openapoc)
[![Openapoc Vkontakte](https://img.shields.io/static/v1?label=VK&logo=vk&logoColor=ffffff&message=Vstupaj%20|%20447&color=282828&labelColor=2787f5)](https://vk.com/openapoc)
[![Openapoc Reddit](https://img.shields.io/reddit/subreddit-subscribers/OpenApoc?color=orange&logo=Reddit&logoColor=ffffff&labelColor=282828)](https://reddit.com/r/openapoc)
[![Openapoc Youtube](https://img.shields.io/static/v1?label=Youtube&logo=Youtube&logoColor=ffffff&message=Subscribe%20|%20365&color=282828&labelColor=FF0000)](https://www.youtube.com/c/openapoc)

<p align="center"><img src="https://i.imgur.com/XxudxVj.jpg"/></p>

## Table of Contents

* [Copyright](#copyright)
* [Key Features](#key-features)
* [What's left to finish?](#whats-left)
* [Contribute and FAQ](#contribute-and-faq)
* [Building](#building)
  * [Building on Windows](#building-on-windows)
  * [Building on Linux](#building-on-linux)
  * [Building on macOS](#building-on-macos)  
* [OpenApoc Coding Style](#openapoc-coding-style)
* [How to setup OpenApoc](#how-to-setup-openapoc)
* [Contact us](#contact-us)


## Copyright
All rights for the original game and its resources belong to their respective owners.
We do not encourage and do not support any form of illegal usage of the original game.
We strongly advise to purchase the original game on STEAM or another platform of your choosing.
Pirated disc images and archives are not supported and will cause issues such as crashes and map problems with OpenApoc.

## Key Features

* [![Julian Gollop](https://img.shields.io/reddit/user-karma/combined/JulianGollop?style=social)](https://www.reddit.com/user/JulianGollop/) "Yes, I am aware of the openApoc project and I very much do support it." 
* Full modding capability - You can add or change almost anything!
* Options for modding that allow opportunity to make OpenApoc:
  * More balanced
  * More diverse
  * More immersive
* Human-Readable Savegame editing - It's all XML in a ZIP archvive so you can edit/tweak in progress games to your liking!
* Support for modern screen resolutions and display scaling at a silky smooth 60fps
* Added a 'More Options' menu that allows players to select dozens of new optional improvements and enhancements
* Added a full debug system ([Hot Keys](https://github.com/OpenApoc/OpenApoc/blob/master/README_HOTKEYS.txt), etc.)
* Port the game to any platform you like (Windows, Linux, Etc.)
* Added a Skirmish Mode for quick fights and custom battles (Experimental)
* The new engine has ample opportunities for expansion and refinements including:
  * High FPS
  * Smooth sound playback with none of the pop/clicks/stutters of the original game
* The potential to add cut and missing features from the Original Game - some of these are already included even at current Alpha state or with the handful of mods already available!

## What's left?

1. [TO HAVE A TRULY PLAYABLE ALPHA STATE](https://github.com/OpenApoc/OpenApoc/issues/263)
2. [TO REACH A BETA STATE (All core Original Game features implemented)](https://github.com/OpenApoc/OpenApoc/issues/264)
3. [TO REACH OPENAPOC RELEASE 1.0 (Final polishing and testing to match or exceed Original Game state)](https://github.com/OpenApoc/OpenApoc/issues/265)
4. [Modding Functions, Extra Features, Enhancements and Quality of Life Updates](https://github.com/OpenApoc/OpenApoc/issues/941)


## Contribute and FAQ

http://openapoc.org/#contribute  - Currently Offline, please use [Discord](https://discord.gg/f8Rayre)
>Here you find news, detailing how you can participate in project. 
You can support the project by testing, translating, modding, drawing, modeling, concepting etc..

http://openapoc.org/#faq  - Currently Offline, please use [Discord](https://discord.gg/f8Rayre)
>Here you find the detailed FAQ (Frequently Asked Questions)


## Building

OpenApocalypse is built leveraging a number of libraries - to provide needed functionality (and save us the time of implementing it badly ourselves). 
Note: The following libraries will be fetched and built with vcpkg in a later step, ensuring you get the correct version.

* [SDL2](https://www.libsdl.org)
* [Boost](https://boost.org) - We specifially use the 'locale' library, used for localisation, 'algorithm' for some small stuff in string handling, 'program-options' for settings management, 'date-time' for some formatting, and parts of 'UUID' and 'CRC' for their hash functions and some temporary filename stuff.
* [Qt](https://www.qt.io/) - needed for the launcher, can be disabled with 'BUILD_LAUNCHER'.
* [Libunwind](https://nongnu.org/libunwind/download.html) - debug backtracing on linux - not needed on windows.
* [LibVorbis](https://xiph.org/vorbis/) - Ogg vorbis music decoder library.

The following libraries are also used, but are shipped as submodules in the repository and directly included in the build, so you don't need to install these dependencies to build or use OpenApoc.

* [GLM](https://glm.g-truc.net) - Math library.
* [libsmacker](https://sourceforge.net/projects/libsmacker/) - Decoder for .smk video files.
* [lodepng](https://github.com/lvandeve/lodepng) - Reading/writing PNG image files.
* [Lua](https://www.lua.org/) - Scripting language.
* [miniz](https://github.com/richgel999/miniz) - Zlib-comptible compression library.
* [physfs](https://icculus.org/physfs/) - Library for reading data from .iso files or directory trees (Note: We use a patched version, available on [GitHub](https://github.com/JonnyH/physfs-hg-import/tree/fix-iso) - required to read the .iso files we use).
* [pugixml](https://pugixml.org) - XML library used for reading/writing the game data files.
* [fmtlib](https://github.com/fmtlib/fmt) - A c++ string formatting library - proposed for c++20 standard.
* [magic_enum](https://github.com/Neargye/magic_enum) - Header-only C++17 library provides static reflection for enums, work with any enum type without any macro or boilerplate code.


### Building on Windows

* Install [Visual Studio](https://visualstudio.microsoft.com/vs/) (2017 or later) with "Desktop Development with C++" workload.
* Install a Git client eg. [Github Desktop](https://desktop.github.com/).
* Checkout OpenApoc from GitHub.
* If you are using the GitHub Desktop client, the submodules should already be setup at first checkout. If not, or if the submodules have been updated, run the following commands in the 'git shell' from the root of the OpenApoc repository. This should reset the submodule checkouts to the latest versions (NOTE: This will overwrite any changes to code in the dependencies/ directory).

```cmd
git submodule update --init --recursive
```

* All the other dependencies (Boost, SDL2, Qt) need to be supplied separately. Install [Vcpkg](https://github.com/Microsoft/vcpkg) and integrate with Visual Studio. If you'd rather install them manually, run the following command:

  * For x64 builds:

```cmd
vcpkg --triplet x64-windows install sdl2 boost-locale boost-program-options boost-uuid boost-crc qt-base6-dev libvorbis
```

  * For x86 builds:

```cmd
vcpkg --triplet x86-windows install sdl2 boost-locale boost-program-options boost-uuid boost-crc qt-base6-dev libvorbis
```

  * For list of all supported by Vcpkg architectures: `vcpkg help triplet`

* Copy the original XCom:Apocalypse .iso file into the "data/" directory. This could also be a directory containing all the extracted files from the CD, and it should be named the same (IE the directory should be data/cd.iso/). This is used during the build to extract some data tables.
* Open the OpenApoc directory in Visual Studio (if you don't have an Open Folder option, generate a project with [CMake](https://cmake.org/)).
* Set your configuration to x64-Release or x86-Release (must match your Vcpkg dependencies). Release is recommended as Debug is very slow.

* Visual Studio should automatically detect and configure CMake appropriately. If you didn't integrate Vcpkg, you will need to manually add it to your CMake Settings file:
  * Visual Studio 2017:

```json
"variables": [
    {
        "name": "CMAKE_TOOLCHAIN_FILE",
        "value": "<path to vcpkg>\\scripts\\buildsystems\\vcpkg.cmake"
    }
]
```
  * Visual Studio 2019: Build > CMake Settings > Toolchain file > `<path to vcpkg>\\scripts\\buildsystems\\vcpkg.cmake`

* Build OpenApoc. This will take a while on the first build, especially if Vcpkg hasn't installed all the dependencies yet. If you get errors, clear your cache from the Project/CMake menu and try again.
* When running OpenApoc from the Visual Studio UI, the working directory is set to the root of the project, so the data folder should already be in the right place. If you want to run outside of Visual Studio, you need to copy the whole 'data' folder (including the cd.iso file) into the folder openapoc.exe resides in.


### Building on Linux

(Tested on Ubuntu 22.04 and 24.04)

* On Ubuntu, install the following packages:

```sh
sudo apt-get install libsdl2-dev cmake build-essential git libunwind8-dev libboost-locale-dev libboost-program-options-dev qtbase5-dev libvorbis-dev
```

* On Mageia, install the following packages as root:

```sh
urpmi "cmake(sdl2)" libstdc++-static-devel boost-devel boost unwind-devel task-c++-devel cmake git qt6-devel libvorbis-devel
```

* On Fedora or other RedHat distro, install the folowing packages as root:

```sh
yum groupinstall "Development Tools" "Development Libraries"
yum install git SDL2-devel cmake libunwind-devel qt6-qtbase-devel libvorbis-devel
```

* Checkout OpenApoc from GitHub.
* Fetch the dependencies from git with the following terminal command (run from the just-created OpenApoc folder).

```sh
git submodule update --init --recursive
```

* Copy the cd.iso file to the 'data' directory under the repository root (Note - despite dosbox having good linux support, the steam version of X-Com Apocalypse will only install if Steam Play is enabled).

```sh
cp /path/to/cd.iso data/
```

* Create a subdirectory ('build' in this example) in the OpenApoc checkout directory, and from that use cmake to configure OpenApoc.

```sh
cd /path/to/OpenApoc
mkdir build
cd build
cmake -DCMAKE_BUILD_TYPE=RelWithDebInfo ..
```

* This cmake command will fail if we're missing a dependency, or your system is for some other reason unable to build - if you have any issues please contact us (see above for links).
* Build the project with the following command.

```sh
make -j4
```

* This should create a directory 'bin' under the build directory, with the 'OpenApoc' executable file. OpenApoc by default expects the data folder to be in the current working directory, so running the executable from the root of the git checkout should work.

```sh
./build/bin/OpenApoc
```


### Building on macOS

(Tested on macOS Sequoia 15.6 (24G84)

* On macOS, install the [Homebrew](https://brew.sh):

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

* Checkout OpenApoc from GitHub:

```sh
git clone https://github.com/OpenApoc/OpenApoc.git
```

* Fetch the dependencies from git with the following terminal command (run from the just-created OpenApoc folder):

```sh
cd /path/to/OpenApoc
git submodule update --init --recursive
```

* Use the homebrew install the following dependencies:

```sh
brew install cmake boost pkg-config sdl2 qt@6 libvorbis
```

* Add the Qt install to path.

* If using zsh (MacOS default since Catalina 10.15):
```sh
echo 'export PATH="/opt/homebrew/opt/qt@6/bin:$PATH"' >> ~/.zprofile
```
* Or if using bash:
```sh
echo 'export PATH="/opt/homebrew/opt/qt@6/bin:$PATH"' >> ~/.bashrc
```

* Copy the cd.iso file to the 'data' directory under the repository root (Note - despite dosbox having good linux support, the steam version of X-Com Apocalypse will only install if Steam Play is enabled).

```sh
cp /path/to/cd.iso data/
```

* Create a subdirectory ('build' in this example) in the OpenApoc checkout directory, and from that use cmake to configure OpenApoc.

```sh
cd /path/to/OpenApoc
mkdir build
cd build
cmake -DCMAKE_BUILD_TYPE=RelWithDebInfo ..
```

* This cmake command will fail if we're missing a dependency, or your system is for some other reason unable to build - if you have any issues please contact us (see above for links).
* Build the project with the following command:

```sh
make -j4
```

* This should create a directory 'bin' under the build directory, with the 'OpenApoc' executable file. OpenApoc by default expects the data folder to be in the current working directory, so running the executable from the root of the git checkout should work.

```sh
cd ..
open ./build/bin/OpenApoc.app
```


## OpenApoc Coding Style

https://www.ufopaedia.org/index.php/Coding_Style_(OpenApoc)
>This document specifies the guidelines for writing and formatting the c++ code that forms the core of OpenApoc.


## How to setup OpenApoc

OPENGL 2.0 SUPPORTIVE VIDEO CARDS ARE REQUIRED

WINDOWS USERS: You will require the LATEST Visual C++ Libraries obtained from windows update to run OpenApoc
https://docs.microsoft.com/en-US/cpp/windows/latest-supported-vc-redist?view=msvc-170

Simple steps to play OpenApoc on Windows right now
(Keep in mind that it is ALPHA - this means bugs, crushes and not all features implemented, use our bug-tracker at https://github.com/OpenApoc/OpenApoc/issues to report bugs and navigate known ones)

1) Download the OpenApoc core files from https://github.com/OpenApoc/OpenApoc/releases
- For experimental builds visit  https://ci.appveyor.com/project/OpenApoc/openapoc/history
- If you see a green bar next to the latest build then you can download it, click a build that is green, or use "Show More" to list all builds
- Click ARTIFACTS (Currently only Windows x64)
- Download the option that ends with a ".exe" (and without "debug" in it)
- Run the downloaded exe installer, this will guide you through the installation
- Use "portable install" if you want saves and settings to remain in the install directory

2) Acquire the original X-Com Apocalypse CD-ROM and create an ISO Image of that, or use Steam's "cd.iso" or GOGs "xcom.cue"/"xcom.bin"
- If you have already specified the "cd.iso" location in the installer, you don't need to do this step
- You need have all files in the disc ISO file including MUSIC so only legit ISOs will work and not torrents that often lack the music
- If the disc image is in .iso format, rename it to "cd.iso"
- We also support the GOG .cue / .bin files!

3) Put cd.iso (image or folder) into the "data" folder under the specified OpenApoc install folder
- If you have already specified the "cd.iso" location in the installer, you don't need to do this step
- To use GOG .cue/.bin you rename the XCOM.cue file to "cd.iso", put that in the OpenApoc data folder, then put the XCOM.BIN, without renaming it, into the data folder too

4) Run and enjoy!


## Contact us

If you're interested, please visit our [website](http://openapoc.org) (Currently Offline, please use [Discord](https://discord.gg/f8Rayre)).
* We have a [Discord](https://discord.gg/f8Rayre) - MOST ACTIVE PLACE FOR ALL THINGS OPENAPOC!
* We have a [Youtube](https://www.youtube.com/c/OpenApoc) channel.
* We have a [forum](http://openapoc.org/forum/) (Currently Offline, please use [Discord](https://discord.gg/f8Rayre))

## Unnofficial and Community Contacts

* We have a [Facebook](https://www.facebook.com/openapoc) page.
* We have a [Reddit](https://reddit.com/r/openapoc) page.
* All VK Presence is currently unofficial
* 
