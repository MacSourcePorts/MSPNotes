## Source Port:
# EDuke32

Game(s): *Ion Fury* (also other Build Engine game)

Homepage: https://www.eduke32.com

GitHub: https://voidpoint.io/terminx/eduke32

MSP GitHub: https://github.com/MacSourcePorts/eduke32

#
### Why is Mac Source Ports doing a build of this port?
The port did not offer Mac builds at all.

### Versioning/Release strategy:
None.

### Build System: 
Make

### Language(s):
C/C++

### Homebrew Requirements:

```
brew install sdl2 libvpx
```
### Data situation
Data goes in `/Users/tomkidd/Library/Application Support/EDuke32`

### Notes:
Builds simply enough but it's having issues on my M1 Max MBP that it wasn't having on my M1 Mini. Needs further investigation, possibly more up to date code. 

### MSP Fork differences:
Too many to list. This project required a lot of work to build on Mac at all (it used to build fine) and it might be worth revisiting to see if the main project still has so many issues. 