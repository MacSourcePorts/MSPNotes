## Source Port:
# Serious-Engine (not a MSP port yet)

Game(s): *Serious Sam: The First Encounter*, *Serious Sam: The Second Encounter*

Homepage: https://github.com/ptitSeb/Serious-Engine

GitHub: https://github.com/ptitSeb/Serious-Engine

MSP GitHub: https://github.com/MacSourcePorts/Serious-Engine

#
### Why is Mac Source Ports doing a build of this port?
The port did not offer Mac builds at all. But even then we haven't figured this one out all the way.

### Build System: 
Cmake

### Language(s):
C/C++

### Homebrew Requirements:

unclear

### Data situation
Also unclear

### Notes:
So I'm not sure what the deal is with this yet. I haven't sussed out what's involved yet with the game data - it builds on macOS and all but when you try and start a game it's looking for files in particular places and it tries to start levels with filenames that don't match anything I have from GOG, so something's going on. 

Complicating things is months ago I kinda sorta had it running but things like doors weren't working, etc. 

And yet the existence of scripts with names like `build-macarm.sh` and `build-mac64.sh` imply someone either has it working on Apple Silicon and/or Intel or at least tried to. Like a lot of source ports the documentation and/or releases are for Windows and Linux and not Mac. 

I do want to get this one working since these would be cool additions but it may require more work. 