## Source Port:
# OpenRCT2

Game(s): *RollerCoaster Tycoon 2*

Homepage: https://openrct2.org

GitHub: https://github.com/OpenRCT2/OpenRCT2

MSP GitHub: https://github.com/MacSourcePorts/OpenRCT2

#
### Why is Mac Source Ports doing a build of this port?
The port does make a Mac build but it's Intel-only and unsigned

### Build System: 
Cmake

### Language(s):
C/C++

### Homebrew Requirements:

Unclear, I think it downloads its own stuff unless you tell it otherwise. 

### Data situation
Asks for data on first run

### Notes:
This one's simple enough, though I do notice that it apparently has its own service to check for updates and then prompts the user to go to their download page. Probably a good incentive to keep up with the latest code more often. Their build is Universal 2 but not signed/notarized. 

Could also just modify the code to send them to MSP but I dunno if that's a dick move or not. 