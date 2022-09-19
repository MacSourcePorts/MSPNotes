## Source Port:
# vcni

Game(s): *Heroes of Might and Magic III*

Homepage: https://vcmi.eu

GitHub: https://github.com/vcmi/vcmi

MSP GitHub: n/a

#
### Why is Mac Source Ports doing a build of this port?
Port releases Mac builds but command-line only, not bundled (though they have that scripted out), not Universal 2 and not signed or notarized

### Versioning/Release strategy:
Numbered release versions

### Build System: 
Cmake

### Language(s):
C/C++

### Homebrew Requirements:

```
brew install cmake smpeg2 libpng freetype qt5 ffmpeg ninja boost tbb luajit sdl2 sdl2_ttf sdl2_image sdl2_mixer
```

### Data situation
Files go in `~/Library/Application Support/fheroes2`, needs the `ANIM`, `DATA`, `MAPS` and `MUSIC` directories from homm2. The instructions say it's ok if some are missing, I've noticed the GOG version doesn't have an ART directory. Seems to run fine. 

### Notes:
This one is simple, the only tricky part was their app bundling process sticks everything in the `Contents/libs` folder instead of a standard location so the code signing step doesn't catch them (or at least I guess that's why) and we have to `lipo` them manually as a result too. 

I had postponed this one since the release was loose files and the build guide gave no indication that it built a bundle or could look outside of the bundle, but the installation guide (which I would have guessed is just for end users) has better build instructions and the info I needed. So this was a go.

### MSP Fork differences:
n/a