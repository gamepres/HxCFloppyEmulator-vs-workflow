# Purpose

The following files are meant to be used with https://github.com/gamepres/HxCFloppyEmulator

Tested with Visual Studio Community 2022

Simply copy/paste its contents at the root of the HxCFloppyEmulator project

Then edit the file `vs/launch.vs.json` to set the `miDebuggerPath` value to point to your local installation of gdb.

The file `tasks.vs.json` defines several custom tasks to call `make` under wsl with various variables set.

# Workflow

## Setup
* Open Visual Studio
* Select to open a folder
* Choose the HxCFloppyEmulator folder

## Build:
* Right click on the top folder inside the Solution Explorer
* Select the task to build (x86 debug/release, x64 debug/release)

## Clean
You have two targets: clean and mrproper (second deletes more stuff than the first)

## Launch/Debug
* Make sure you have built the binaries first (or else, the options won't appear)
* On the toolbar at the top of the IDE, there is a `"Select Startup Item"` dropdown list where you can choose the target to launch/debug
    * GDB: HxCFloppyEmulator.exe
    * GDB: hxcfe.exe
* If the options do not appear immediately, try to reload the `launch.vs.json` file (simply save it to force a refresh)
* Debugging information and breakpoints should be available if you have selected a debug build
