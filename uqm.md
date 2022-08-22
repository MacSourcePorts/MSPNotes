## Source Port:
# The Ur-Quan Masters

Game(s): *Star Control II: The Ur-Quan Masters*

Homepage: http://sc2.sourceforge.net

GitHub: http://sc2.sourceforge.net/downloads.php

MSP GitHub: https://github.com/MacSourcePorts/uqm

#
### Why is Mac Source Ports doing a build of this port?
The port did not offer Mac builds at all.

### Versioning/Release strategy:
Version numbers but very infrequent releases (latest version, 0.8, was first one in a decade)

### Build System: 
Proprietary

### Language(s):
C/C++

### Homebrew Requirements:

```
brew install sdl2 libogg libvorbis libpng libvorbisfile
```
### Data situation
Game is free/public domain, can be built to be full game. Data can be found on the downloads page above in the form of three .uqm files. They can be put in the `dist-packages` folder which is excluded from git. 

### Notes:
Once the libraries are in place it's easy enough... except this one decided to do its own proprietary build system. For now it can't be 100% automated because you have to select what to build. 

When running, pick "1" to choose what kind of build, then choose "1" again to pick a release build, then hit "enter" when you get back to the first list of options to proceed. You will need to do this a second time for the other architecture. It's a pain, but I think this project predated a number of best practices. 

### MSP Fork differences:
```
.gitignore
build/unix/config_proginfo_build
macsourceports_universal2.sh
src/libs/mikmod/mikmod.h
src/libs/mikmod/mikmod_internals.h
```

Thia one is a good candidate to remain a fork because it rarely updates and it isn't on GitHub.
