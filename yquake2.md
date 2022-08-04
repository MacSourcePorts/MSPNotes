## Source Port:
# yquake2

Game(s): *GameName*

Homepage: https://www.yamagi.org/quake2/

GitHub: https://github.com/yquake2/yquake2

MSP GitHub: https://github.com/MacSourcePorts/yquake2

#
### Why is Mac Source Ports doing a build of this port?
The port did not offer Mac builds at all.

### Build System: 
Make

### Language(s):
C/C++

### Homebrew Requirements:

```
brew install sdl2 openal-soft
```
### Data situation
Looks for data in `~/.yq2/` (`baseq2`, `music` folders, etc.)

### Notes:
Mostly straighforward Makefile routine. I had to specify locations of certain things per-platform, in hindsight there might have been better ways to do this but this was like my third port ever so I was still getting used to things. 

I have to run `dylibbundler` on the renderer and rules `.dylib` files directly because the `MSPScripts` script is designed to run on the main executable but nothing else. Same for the `lipo` routine. 

### MSP Fork differences:
```
macsourceports_universal2.sh
.gitignore
build_macos.sh
stuff/quake2.icns
```