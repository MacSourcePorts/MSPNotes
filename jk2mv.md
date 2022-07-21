## Source Port:
# jk2mv

Game(s): *Jedi Knight II: Jedi Outcast (multiplayer)*

Homepage: https://jk2mv.org/

GitHub: https://github.com/mvdevs/jk2mv / https://github.com/mvdevs/mvsdk

MSP GitHub: https://github.com/MacSourcePorts/jk2mv / https://github.com/MacSourcePorts/mvsdk

#
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