## Source Port:
# vkQuake

Game(s): *Quake*

Homepage: https://github.com/Novum/vkQuake

GitHub: https://github.com/Novum/vkQuake

MSP GitHub: https://github.com/MacSourcePorts/vkQuake

#
### Why is Mac Source Ports doing a build of this port?
The port did not offer Mac builds at all.

### Versioning/Release strategy:
Numbered release versions

### Build System: 
Meson

### Language(s):
C/C++

### Homebrew Requirements:

```
brew install molten-vk vulkan-headers sdl2 libvorbis flac mad
```
### Data situation
Looks for the `id1` directory parallel to the executable, or parallel to the app bundle

### Notes:
This project has a rudimentary Makefile and supports macOS in the respect that the author gives instructions on how to build it for the Mac and even shows how to use MoltenVK to bridge the gap, but does not do any Mac app bundling themselves. 

As this is one of the first ports MSP did, there are modifications to the Makefile which in the future would be avoided. 

There are also unresolved issues with this port on earlier versions of macOS.

### MSP Fork differences:
```
.gitignore
macsourceports_universal2.sh
Misc/quake.icns
Misc/vkQuake.icns
Quake/Makefile
Quake/build_macos.sh
macsourceports_universal2.sh
```

`build_macos.sh` is leftover from initial attempts, can be removed. The chnages to `Makefile` may be necessary to do a multiple arch build, not sure how to migrate that

UPDATE: The project has moved to a new build system called Meson which means the MSP fork is no longer necessary. This should help us update more often. 
