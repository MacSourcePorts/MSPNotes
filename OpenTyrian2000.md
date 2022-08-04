## Source Port:
# OpenTyrian2000

Game(s): *Tyrian 2000*

Homepage: https://github.com/opentyrian/opentyrian2000

GitHub: https://github.com/opentyrian/opentyrian2000

MSP GitHub: https://github.com/MacSourcePorts/opentyrian2000

#
### Why is Mac Source Ports doing a build of this port?
The port did not offer Mac builds at all.

### Build System: 
Make

### Language(s):
C/C++

### Homebrew Requirements:

```
brew install sdl2 sdl2_net pkg_config
```
### Data situation
The data can be found at

https://www.camanis.net/tyrian/tyrian2000.zip

And can be placed in a subdirectory called "data" which will not get added to source control. Despite being freeware I figure there's a reason the authors decided not to include it with the source code so I'm honoring that. 

The build script will make a full packaged app bundle including the game data.

### Notes:
This port is straightforward, just have the dependencies and you'll be able to fire off the makefile no issues.

Note that this is a different project from [OpenTyrian](OpenTyrian.md). OpenTyrian runs version *Tyrian* (up to 2.1), *OpenTyrian2000* runs *Tyrian 2000* (which is *Tyrian* at version 3.0 with a new episode and a new name)

### MSP Fork differences:
```
.gitignore
Makefile
macos/tyrian.icns
macsourceports_universal2.sh
src/file.c
src/msputils.h
src/msputils.m
```

Changes are minimal but partially required to find the info in the bundle. This might be a good candidate to stay as a fork.