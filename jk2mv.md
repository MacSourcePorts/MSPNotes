## Source Port:
# jk2mv

Game(s): *Jedi Knight II: Jedi Outcast (multiplayer)*

Homepage: https://jk2mv.org/

GitHub: https://github.com/mvdevs/jk2mv / https://github.com/mvdevs/mvsdk

MSP GitHub: https://github.com/MacSourcePorts/jk2mv / https://github.com/MacSourcePorts/mvsdk

#
### Why is Mac Source Ports doing a build of this port?
This port (or at least users of it) requested it. 

### Versioning/Release strategy:
Numbered release versions (but the latest one is old)

### Build System: 
Cmake

### Language(s):
C/C++

### Homebrew Requirements:

None. Like most ioquake3-derived ports it just needs its own SDL

### Data situation
Data goes in `/Users/tomkidd/Library/Application Support/jk2mv`

### Notes:
Easy enough port except for one thing - it puts its game code in a submodule, `mvsdk`. Long story short I had to make a fork of that too and then point the `jk2mv` main repo to it. So any changes that occur in there need to have both checked in. 

### MSP Fork differences:
In `jk2mv`:
```
.gitignore
.gitmodules
CMakeLists.txt
build/jk2mv.entitlements
libs/zlib/gzguts.h
macsourceports_universal2.sh
src/qcommon/q_shared.h
src/qcommon/vm_local.h
src/sys/sys_public.h
src/sys/sys_unix.cpp
src/sys/sys_win32.cpp
```

In `mvsdk`:
```
CMakeLists.txt
code/cgame/cg_players.c
code/game/q_shared.h
tools/qcommon/q_platform.h
```

The changes to these are the typical stuff needed for id Tech 3 to be on Apple Silicon. I need to do a PR with the main project, or check to see if they have Apple Silicon support yet. 