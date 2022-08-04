## Source Port:
# OpenXcom

Game(s): *GameName*

Homepage: https://openxcom.org/

GitHub: https://github.com/OpenXcom/OpenXcom

MSP GitHub: https://github.com/MacSourcePorts/OpenXcom

#
### Why is Mac Source Ports doing a build of this port?
The port did not offer Mac builds at all.

### Versioning/Release strategy:
Version tags only, but the latest one is really old (2014)

### Build System: 
Cmake

### Language(s):
C/C++

### Homebrew Requirements:

```
brew install sdl sdl_mixer sdl_gfx sdl_image yaml-cpp
```
### Data situation
X-COM: UFO Defense goes in `~/Library/Application Support/OpenXcom/UFO`

X-COM: Terror from the Deep goes in `~/Library/Application Support/OpenXcom\TFTD`

### Notes:
Yes this one needs SDL1 stuff. Yes SDL1 exists on Homebrew for Apple Silicon. Yes, Homebrew will now constantly remind you SDL1 is deprecated. 

### MSP Fork differences:
```
.gitignore
macsourceports_universal2.sh
```