## Source Port:
# DevilutionX

Game(s): *Diablo*

Homepage: https://github.com/diasurgical/devilutionX

GitHub: https://github.com/diasurgical/devilutionX

MSP GitHub: https://github.com/MacSourcePorts/devilutionX

#
### Why is Mac Source Ports doing a build of this port?
The port does make a Mac build but it's Intel-only and unsigned. They're interested in linking to our builds for Apple Silicon/Universal 2 if we can get the process set up for tagged releases.

### Versioning/Release strategy:
Numbered release versions

### Build System: 
Cmake

### Language(s):
C/C++

### Homebrew Requirements:
This project comes with a `brewfile` so you can just run 
```
brew bundle install
```

But the direct equivalent seems to be

```
brew cmake fmt sdl2 libsodium pkg-config googletest
```

Also looks like you need

```
brew install SDL2_image
```

### Data situation
Game data needs to go to `~/Library/Application Support/diasurgical/devilution`. Apparently only the .MPQ files are needed. 

### Notes:
For this partocilar source port, error messages about `PNG_ARM_NEON_FILE` or `png_have_neon` mean that `SDL2_image` is not installed.

```
/Users/tomkidd/Documents/GitHub/MacSourcePorts/devilutionX/build-arm64/_deps/libpng-src/arm/arm_init.c:49:4: error: "PNG_ARM_NEON_FILE undefined: no support for run-time ARM NEON checks"
#  error "PNG_ARM_NEON_FILE undefined: no support for run-time ARM NEON checks"
   ^
/Users/tomkidd/Documents/GitHub/MacSourcePorts/devilutionX/build-arm64/_deps/libpng-src/arm/arm_init.c:86:27: error: implicit declaration of function 'png_have_neon' is invalid in C99 [-Werror,-Wimplicit-function-declaration]
               no_neon = !png_have_neon(pp);
                          ^
```

Also for some reason the `googletest` thing doesn't allow the unit test targets for `x86_64` to build, but that's not required to work to make a functioning Universal 2 build. 

### MSP Fork differences:
```
macsourceports_universal2.sh
CMakeLists.txt
```

`CMakeLists.txt` changes may be unneccessary now