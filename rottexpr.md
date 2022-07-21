## Source Port:
# rottexpr

Game(s): *Rise of the Triad*

Homepage: https://github.com/LTCHIPS/rottexpr

GitHub: https://github.com/LTCHIPS/rottexpr

MSP GitHub: https://github.com/MacSourcePorts/rottexpr

#
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