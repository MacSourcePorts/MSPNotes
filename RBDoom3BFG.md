## Source Port:
# RBDoom3BFG

Game(s): *DOOM 3: BFG Edition*

Homepage: https://github.com/RobertBeckebans/RBDOOM-3-BFG

GitHub: https://github.com/RobertBeckebans/RBDOOM-3-BFG

MSP GitHub: https://github.com/MacSourcePorts/RBDOOM-3-BFG

#
### Why is Mac Source Ports doing a build of this port?
The port did not offer Mac builds at all.

### Versioning/Release strategy:
Numbered release versions

### Build System: 
Cmake

### Language(s):
C/C++

### Homebrew Requirements:

```
brew install cmake sdl2 openal-soft ffmpeg
```
### Data situation
Looks in `~/Library/Application Support/RBDOOM-3-BFG/` for data

### Notes:
This one is simple enough

### MSP Fork differences:
```
.gitignore
macsourceports_universal2.sh
neo/.DS_Store
neo/CMakeLists.txt
neo/doom3bfg.icns
```
~~Not sure if the CMakeLists changes are required. Some of it is debugging info.~~

I was able to switch to just using the project's repo in the build system by specifying `-DCMAKE_PREFIX_PATH=/usr/local`. It also allows me to just use the arm64 `cmake` instead of the x86_64 one.
