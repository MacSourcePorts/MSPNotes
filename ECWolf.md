## Source Port:
# ECWolf

Game(s): *Wolfenstein 3-D, Spear of Destiny*

Homepage: http://maniacsvault.net/ecwolf/

BitBucket: https://bitbucket.org/ecwolf/ecwolf

MSP GitHub: https://bitbucket.org/macsourceports/ecwolf/ / https://github.com/MacSourcePorts/ECWolf

#
### Build System: 
Cmake

### Language(s):
C/C++

### Homebrew Requirements:

```
brew install sdl sdl_mixer sdl_net
```
### Data situation
Looks for data in `/Users/tomkidd/Library/Application Support/ECWolf`

### Notes:
This is one of the rare source ports we do that's on something other than GitHub. To play along I made a BitBucket account and forked it from there but also set up a GitHub Repo as a second remote. 

Also this is one of the few projects that can use SDL1 or SDL2. I had it building with SDL2 before, but on my new MBP the script it uses can't find SDL2_Mixer. I think it's because within the last two weeks SDL2_Mixer upgraded to a new version for the first time in many years - it was 2.0.4 forever now it's 2.6.0. In addition, ECWolf has its own fork of SDL_Mixer you're supposed to use. Whatever, it works with SDL_Mixer (for SDL1). 