## Source Port:
# dhewm3

Game(s): *DOOM 3*

Homepage: https://dhewm3.org/

GitHub: https://github.com/dhewm/dhewm3

MSP GitHub: https://github.com/MacSourcePorts/dhewm3

#
### Why is Mac Source Ports doing a build of this port?
This project actually prefers we do the build as the main dev does not own a Mac

### Build System: 
Cmake

### Language(s):
C/C++

### Homebrew Requirements:

```
brew install sdl2 openal-soft
```
### Data situation
Looks for data in `~/Library/Application Support/dhewm3/`

### Notes:
Similar deal to yquake2 - mostly straighforward Makefile, manual need to reference `openal-soft`, and manual `lipo` on `.dylib` files. 

### MSP Fork differences:
```
.gitignore
doom3.icns
macsourceports_universal2.sh
CMakeLists.txt
neo/framework/Common.cpp
```

`neo/framework/Common.cpp` changes appear to be to enable the finding of the `.dylib` files int the bundle itself. I should discuss it with @Doomed_Daniel about doing a PR for it. 