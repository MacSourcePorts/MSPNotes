## Source Port:
# fallout2-ce

Game(s): *Fallout 2*

Homepage: https://github.com/alexbatalov/fallout2-ce

GitHub: https://github.com/alexbatalov/fallout2-ce

MSP GitHub: https://github.com/MacSourcePorts/fallout2-ce

#
### Why is Mac Source Ports doing a build of this port?
We did one but then the original developer started doing it so we're no longer doing one. 

### Build System: 
Cmake

### Language(s):
C/C++

### Homebrew Requirements:

```
brew install sdl2
```
### Data situation
It looks for the game data to be in the same directory as the `fallout2-ce.app` app bundle. 

### Notes:
This is a straightforward port, especially since it makes its own no-frills bundle. The one kinda weird thing is it relies on some sort of SDL filesystem that only supports Big Sur (11.0) or later. It also required a special thing in the `Info.plist` that I could probably work into our standard output but I just figured it's quicker to use the one that comes with the project. 