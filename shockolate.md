## Source Port:
# shockolate

Game(s): *System Shock*

Homepage: https://github.com/Interrupt/systemshock

GitHub: https://github.com/Interrupt/systemshock

MSP GitHub: https://github.com/MacSourcePorts/systemshock

#
### Why is Mac Source Ports doing a build of this port?
This port didn't offer a Mac app bundle.

### Versioning/Release strategy:
Numbered release versions but the most recent one is pretty old (2019)

### Build System: 
Cmake

### Language(s):
C/C++

### Homebrew Requirements:

```
brew install sdl2 sdl2_mixer
```
### Data situation
Data goes in `/Users/tomkidd/Library/Application Support/systemshock/res`

### Notes:
I had to (just now) modify the CMakeLists.txt to remove the check to make sure SDL2_Mixer was 2.0.4 or higher. Looks like SDL2 2.0.4 was the last version for a long time but 2.5 and beyond (currently 2.6.1) were released within the last two weeks. The check should work but (since 2.6.1 > 2.0.4) but it's not for some reason. 

Also the `macsourceports_universal2.sh` script makes two versions, one with hardware rendering and one without. Hardware accelleration has some issues on Apple Silicon so there's options for those who want it. I list it as two different downloads on MacSourcePorts.com.

Also this project I've added some logic to in order to find the game data outside of the bundle. It probably should be modified further to use the new `MSPUtils` code to unify the process of finding the folder. 

### MSP Fork differences:
Too many to list. The code needed for a couple of things are just grafted in. This one might be tricky to migrate because it's both requiring a bunch of stuff as well as using a tag-based release system. 