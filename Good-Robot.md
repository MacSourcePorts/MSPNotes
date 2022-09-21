## Source Port:
# Good-Robot

Game(s): *Good Robot*

Homepage: https://pyrodactyl.com/good-robot/

GitHub: https://github.com/arvindrajayadav/Good-Robot

MSP GitHub: https://github.com/MacSourcePorts/Good-Robot

#
### Why is Mac Source Ports doing a build of this port?
This game is not otherwise available on the Mac

### Versioning/Release strategy:
Numbered release versions

### Build System: 
Cmake

### Language(s):
C/C++

### Homebrew Requirements:

```
brew install sdl boost glew freetype freealut devil
```
### Data situation
Looks for data in `~/Library/Application Support/Good-Root/`

### Notes:
This mostly worked out of the box, except I had to tweak one of the shader scripts for the in-game characters. Then I had to do work to be able to use `Application Support` instead of everything in the same directory as the executable. Also neutered Steam support.

### MSP Fork differences:
```
.gitignore
CMakeLists.txt
ImageManager.cpp
InputManager.cpp
SteamLeaderboard.cpp
SteamLeaderboardMenu.cpp
TextManager.cpp
audio.cpp
env.cpp
font.cpp
fragment_macos.cg
hud.cpp
interface.cpp
main.cpp
map.cpp
master.h
menu.cpp
page_pattern.cpp
render.cpp
resource.cpp
resource.h
steam_data.cpp
steamworks/public/steam/steam_api.h
system.cpp
ui_credits.cpp
ui_hatshop.cpp
ui_highscore.cpp
ui_mainmenu.cpp
ui_news.cpp
ui_opt.cpp
ui_store.cpp
ui_upgrade.cpp
```