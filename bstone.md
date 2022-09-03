## Source Port:
# bstone

Game(s): *Blake Stone: Aliens of Gold*, *Blake Stone: Planet Strike*

Homepage: https://bibendovsky.github.io/bstone/

GitHub: https://github.com/bibendovsky/bstone

MSP GitHub: https://github.com/MacSourcePorts/bstone

#
### Why is Mac Source Ports doing a build of this port?
The port did not offer Mac builds at all.

### Versioning/Release strategy:
Versioned release numbers 

### Build System: 
CMake

### Language(s):
C/C++

### Homebrew Requirements:

```
brew install sdl2 
```
### Data situation
Looks for data in `/Users/tomkidd/Library/Application Support/bibendovsky/bstone`

### Notes:
The port was already using an `Application Support` directory for saving preferences, scores, etc. so it wasn't too hard to find the spot that's gathering the search paths for data and add that directory to it. 

The use of `bibendovsky/bstone` seems to be because it's using the `SDL_GetPrefPath` function of SDL (which I hadn't seen before) and that function, while it keeps you from having to shell out to Objective-C, really wants both an org name and a project name, thus the buried directory. I'm seeing some code on GitHub sending `NULL` for the org name, so that might be a way to keep from having to use a subdirectory. 

### MSP Fork differences:
```
src/jm_free.c
```