## Source Port:
# disasteroids3d

Game(s): *Disasteroids 3D*

Homepage: http://www.lmnopc.com/disasteroids3d/

GitHub: https://github.com/tomkidd/disasteroids3d

MSP GitHub: https://github.com/MacSourcePorts/disasteroids3d

#
### Why is Mac Source Ports doing a build of this port?
This one is more or less my bidding and just for kicks since I have it on the App Store too.

### Versioning/Release strategy:
None, just the latest version/code (updates are infrequent)

### Build System: 
Make

### Language(s):
C/C++

### Homebrew Requirements:

```
brew install sdl2 sdl2_mixer
```
### Data situation
Comes with data, full game

### Notes:
Easiest/quickest port to build hands down.

### MSP Fork differences:
```
.gitignore
Makefile
disasteroids3d.icns
macsourceports_universal2.sh
```

This is the rare fork we can continue to maintain in light of the new process since we control the base game. 