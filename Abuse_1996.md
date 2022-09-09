## Source Port:
# Abuse_1996

Game(s): *Abuse*

Homepage: https://antonior-software.blogspot.com/2016/05/abuse-1996-sdl-port-09a.html

GitHub: https://github.com/antrad/Abuse_1996

MSP GitHub: https://github.com/MacSourcePorts/Abuse_1996

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
brew install cmake sdl2 sdl_mixer
```
### Data situation
Comes with full game data

### Notes:
The port was trying to save to a location inside the app bundle which wasn't working, so I modified the code using `SDL_GetPrefPath` to save games and the config to `~/Library/Application Support/abuse`. Turns out you can null out the org and it skips it.

I had skipped this game for a long time since it wasn't available commercially and I didn't want to anger any of the existing developers, especially since there's been [precedent set in this area](http://indiegameproducer.blogspot.com/2009/08/abuse-abuse.html), but on closer inspection the Abuse_1996 project has been distributing the full game for years and the [Abuse-SDL](http://abuse.zoy.org) project actually [claims](http://abuse.zoy.org/wiki/download) they were given permission to redistribute it, so I figure it's OK to redistrubte it too, seeing as how I'm not profiting off of it or claiming ownership. 

If I'm wrong I get a nasty email and I take it down. Done and done.

### MSP Fork differences:
```
src/sdlport/setup.cpp
```