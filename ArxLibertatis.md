## Source Port:
# Arx Libertatis

Game(s): *Arx Fatalis*

Homepage: https://arx-libertatis.org

GitHub: https://github.com/arx/ArxLibertatis

MSP GitHub: https://github.com/MacSourcePorts/ArxLibertatis

#
### Build System: 
Cmake

### Language(s):
C/C++

### Homebrew Requirements:

```
brew install cmake boost freetype sdl2 libepoxy qt5 cppunit glm openal-soft
```

Granted it seems to build without `libepoxy` or `cppunit`. I assume `qt5` is really `qt@5`

### Data situation
Files go in `~/Library/Application Support/ArxLibertatis`

### Notes:
This one is actually pretty simple - I'm guessing since someone also makes a command line version for Homebrew, the work of finding the data in `Application Support` has already in place. Everything is down to one executable and once I got it in a faux bundle (no info.plist) the scripts took over.

One issue is that the localization placeholder strings show up in the settings screen and I'm not sure why. Their instructions don't mention anything about needing to build differently but they might be out of date. 

### MSP Fork differences:
```
macsourceports_universal2.sh
.gitignore
data/icons/arx-libertatis.icns
```