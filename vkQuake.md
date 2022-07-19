## Source Port:
# vkQuake

Game(s): *Quake*

Homepage: https://github.com/Novum/vkQuake

GitHub: https://github.com/Novum/vkQuake

MSP GitHub: https://github.com/MacSourcePorts/vkQuake

#
### Build System: 
Make

### Language(s):
C/C++

### Homebrew Requirements:

```
brew install molten-vk vulkan-headers sdl2 libvorbis flac mad
```
### Data situation
Looks for the `id1` directory parallel to the executable, or parallel to the app bundle

### Notes:
As this is one of the first ports MSP did, there are modifications to the Makefile which in the future would be avoided. 

There are also unresolved issues with this port on earlier versions of macOS.