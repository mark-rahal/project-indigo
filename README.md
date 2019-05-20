# Project Indigo
## Setup
Install CMake.  
Install MinGW gcc and g++ compiler. *Make sure it's the correct version!*  
MinGW install instructions:
- Download [MinGW 7.3.0 32-bit](https://sourceforge.net/projects/mingw-w64/files/Toolchains%20targetting%20Win32/Personal%20Builds/mingw-builds/7.3.0/threads-posix/dwarf/i686-7.3.0-release-posix-dwarf-rt_v5-rev0.7z/download).  
- Create a directory for MinGW (Recommended to use `C:\MinGW`)  
- Copy the contents of MinGW to this directory.
- Edit the system Path variable (add `C:\MinGW\bin`)  
Download the SFML GCC 32-bit package.  
- Create sfml directory in base directory.  
- Copy /bin /lib /include to sfml directory in project.  
Run CMake build.  
Executable will be in /build directory.  