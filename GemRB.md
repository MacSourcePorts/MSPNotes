## Source Port:
# GemRB

Game(s): *Baldur's Gate*, *Baldur's Gate II* and *Icewind Dale*

Homepage: https://gemrb.org

GitHub: https://github.com/gemrb/gemrb

MSP GitHub: https://github.com/MacSourcePorts/gemrb

#
### Why is Mac Source Ports doing a build of this port?
The port does make a Mac build but it's Intel-only and unsigned

### Build System: 
Cmake

### Language(s):
C/C++

### Homebrew Requirements:

```
brew install sdl2 python@3.9
```
### Data situation
The gam launches a Cocoa window that allows the user to choose what game data to use. 

### Notes:
This port uses a number of plugins compiled into UNIX `.so` files, a common denominator for both the Linux and macOS builds. Because there is not a Universal concept for `.so` files like there is for `.dylib` files on macOS, the code has been modified to look for the files in `x86_64` and `arm64` subdirectories in the app bundle in order to be a Universal 2 app.

In hindsight I'm questioning the logic of having done this. The Windows version is designed to use `.dll` as a format so I'm wondering if the `.so` files could be compiled into `.dylib` files on macOS and forego the whole process. Or if individual Intel and Apple Silicon apps would have been a more prudent usage of time. 

In any event, I guess `codesign --deep` only code signs executables and `.dylib` files because it didn't codesign `.so` files so the build script has a nutty number of manual `codesign` commands as a result. 

This source port uses the `com.apple.security.cs.disable-library-validation` `com.apple.security.files.user-selected.read-write` entitlements

This source port specifies the Python paths as cmake arguments. 