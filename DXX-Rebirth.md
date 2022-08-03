## Source Port:
# DXX-Rebirth

Game(s): *Descent*, *Descent II*

Homepage: https://www.dxx-rebirth.com/

GitHub: https://github.com/dxx-rebirth/dxx-rebirth

MSP GitHub: https://github.com/MacSourcePorts/dxx-rebirth

#
### Why is Mac Source Ports doing a build of this port?
This project does not release official Mac builds at all.

### Build System: 
SConstruct (scons)

### Language(s):
C/C++

### Homebrew Requirements:

```
brew install python sdl physfs sdl_image sdl_mixer scons
```
### Data situation
*Descent* data goes in `/Volumes/tomkidd/Library/Preferences/D1X Rebirth`

*Descent II* data goes in `/Volumes/tomkidd/Library/Preferences/D2X Rebirth`

Note that those folder have spaces in the names

### Notes:
This one's not a big deal other than it uses a build system I've not seen before or since (`scons`). It also builds two different apps for the two different games, `D1X-Rebirth` and `D2X-Rebirth`.