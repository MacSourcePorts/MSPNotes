## Source Port:
# dhewm3

Game(s): *DOOM 3*

Homepage: https://dhewm3.org/

GitHub: https://github.com/dhewm/dhewm3

MSP GitHub: https://github.com/MacSourcePorts/dhewm3

#
### Build System: 
Cmake

### Language(s):
C/C++

### Homebrew Requirements:

```
brew install sdl2 openal-soft
```
### Data situation
Looks for data in `~/Library/Application Support/dhewm3/`

### Notes:
Similar deal to yquake2 - mostly straighforward Makefile, manual need to reference `openal-soft`, and manual `lipo` on `.dylib` files. 