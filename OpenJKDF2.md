## Source Port:
# OpenJKDF2

Game(s): *Jedi Knight: Dark Forces II*

Homepage: https://github.com/shinyquagsire23/OpenJKDF2

GitHub: https://github.com/shinyquagsire23/OpenJKDF2

MSP GitHub: https://github.com/MacSourcePorts/OpenJKDF2

#
### Why is Mac Source Ports doing a build of this port?
This port's author requested it. 

### Versioning/Release strategy:
None. Latest code only. 

### Build System: 
Cmake

### Language(s):
C/C++

### Homebrew Requirements:

```
brew install openal-soft sdl2 sdl2_mixer glew python3 imagemagick
pip3 install cogapp generate-iconset
```
### Data situation
Asks for data location on first run

### Notes:
So this one requires both the `brew` items and some Python plugins via the `pip3` command. 

Also I just tried it on my new M1 Max MBP and the mouse look is broken or something. Not what I experienced on my M1 mini. I'll update later and see if it still happens. 

### MSP Fork differences:
```
.gitignore
combine_macos_appbundles.sh
distpkg_macos.sh
macsourceports_universal2.sh
packaging/macos/Contents/Info.plist
```

This one does a lot of the work for packaging so I should either do a PR or maintain it as a fork. 