## Source Port:
# OpenJK/OpenJO

Game(s): *Jedi Knight II: Jedi Outcast, Jedi Knight: Jedi Academy*

Homepage: https://github.com/JACoders/OpenJK

GitHub: https://github.com/JACoders/OpenJK

MSP GitHub: https://github.com/MacSourcePorts/OpenJK

#
### Why is Mac Source Ports doing a build of this port?
This port, or its users at least, requested it. 

### Versioning/Release strategy:
None. Latest code only.

### Build System: 
Cmake

### Language(s):
C/C++

### Homebrew Requirements:

None. Like most ioquake3-derived ports it just needs its own SDL

### Data situation
OpenJK Data goes in `/Users/tomkidd/Library/Application Support/OpenJK`
OpenJO Data goes in `/Users/tomkidd/Library/Application Support/OpenJO`

### Notes:
The `macsourceports_universal2.sh` script makes three apps from two projects from one repo. 

`OpenJK` is the name of the repo.

`OpenJK` is also the name of the project that handles the game *Jedi Knight: Jedi Academy* (aka *Jedi Knight III*). It makes two different executables, `OpenJK-SP.app` for single player and `OpenJK-MP.app` for multiplayer. This is how the original game shipped for both security and development purposes. 

`OpennJO` is the name of the project that handles the game *Jedi Knight II: Jedi Outcast*, but only the single player aspect, which is in `OpenJO-SP.app`. For multiplayer see the [jk2mv](jk2mv.md) project. 

So, 
- `OpenJO-SP.app`: plays *Jedi Knight II: Jedi Outcast* single player
- `OpenJK-SP.app`: plays *Jedi Knight: Jedi Academy* single player
- `OpenJK-MP.app`: plays *Jedi Knight: Jedi Academy* multiplayer

### MSP Fork differences:
```
.gitignore
CMakeLists.txt
code/client/cl_cgame.cpp
code/client/vmachine.cpp
code/client/vmachine.h
codeJK2/game/bg_pmove.cpp (formatting change only, nonessential)
macsourceports_universal2.sh
shared/qcommon/q_platform.h
```

This is another id Tech 3 project that needs the specific changes to be Apple Silicon. I should do a PR with the main project. 