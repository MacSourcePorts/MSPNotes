## Source Port:
# uHexen2 (Hammer of Thyrion)

Game(s): *Hexen II*

Homepage: https://sourceforge.net/projects/uhexen2/

GitHub: https://github.com/sezero/uhexen2

MSP GitHub: https://github.com/MacSourcePorts/uhexen2

#
### Why is Mac Source Ports doing a build of this port?
The last build from the site is from 2018, so not signed/notarized and not Apple Silkicon

### Versioning/Release strategy:
Versioned release numbers 

### Build System: 
Make

### Language(s):
C/C++

### Homebrew Requirements:

```
brew install sdl2 flac opus opusfile libvorbis 
```
### Data situation
Looks for data in `/Users/tomkidd/Library/Application Support/Hexen2`

### Notes:
This port was already using `Application Support` for game data, however the Makefile had to be modified (not using CMake) to allow for different architectures. Their build scripts already do some amount of work to make Universal 1 builds, the project has just gone stale long before Apple Silicon.

### MSP Fork differences:
```
Makefile
```