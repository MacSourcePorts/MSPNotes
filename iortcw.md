## Source Port:
# iortcw

Game(s): *Return to Cast*

Homepage: https://github.com/iortcw/iortcw

GitHub: https://github.com/iortcw/iortcw

MSP GitHub: https://github.com/MacSourcePorts/iortcw

#
### Why is Mac Source Ports doing a build of this port?
The port does make a Mac build but it's Intel-only and unsigned

### Build System: 
Make

### Language(s):
C/C++

### Homebrew Requirements:

None. Only thing it needs is SDL2 and it comes with it. 

### Data situation
Data goes in `~/Library/Application Support/RTCW/`

### Notes:
Similar to [ioquake3](ioquake3.md) (in fact technically this source port is ioquake3 with the RTCW changes grafted in) this one is straightforward and the only library it needs comes with it. I did have to copy over the same new library for libSDL2 from ioquake3. 