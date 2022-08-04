## Source Port:
# rottexpr

Game(s): *Rise of the Triad*

Homepage: https://github.com/LTCHIPS/rottexpr

GitHub: https://github.com/LTCHIPS/rottexpr

MSP GitHub: https://github.com/MacSourcePorts/rottexpr

#
### Why is Mac Source Ports doing a build of this port?
The port did not offer Mac builds at all.

### Versioning/Release strategy:
There's a couple of "releases" but it doesn't look formal. 

### Build System: 
Make

### Language(s):
C/C++

### Homebrew Requirements:

```
brew install sdl2 sdl2_mixer
```
### Data situation
Looks for data in `/Users/tomkidd/Library/Application Support/rott`

### Notes:
Straightforward, but like `shockolate` I've added some logic to in order to find the game data outside of the bundle. It probably should be modified further to use the new `MSPUtils` code to unify the process of finding the folder. 

### MSP Fork differences:
```
.gitignore
icons/rott.icns
macsourceports_universal2.sh
src/rt_main.c
```
After integrating the `MSPUtils` this might be a good one to keep as a fork beause of its infrequent updates. 