## Source Port:
# CorsixTH

Game(s): *Theme Hospital*

Homepage: https://corsixth.com/

GitHub: https://github.com/CorsixTH/CorsixTH

MSP GitHub: https://github.com/MacSourcePorts/CorsixTH

#
### Build System: 
Cmake

### Language(s):
C/C++/Lua

### Homebrew Requirements:

```
brew install sdl2 sdl2_mixer openssl lua luarocks wxwidgets freetype2 yasm ffmpeg

luarocks install luafilesystem
luarocks install lpeg
luarocks install luasocket --from=http://luarocks.org/dev
luarocks install luasec OPENSSL_DIR=/opt/Homebrew/opt/openssl

/usr/local/bin/luarocks install luafilesystem
/usr/local/bin/luarocks install lpeg
/usr/local/bin/luarocks install luasocket --from=http://luarocks.org/dev
/usr/local/bin/luarocks install luasec OPENSSL_DIR=/usr/local/opt/openssl

```
### Data situation
Asks for location of data on first run

### Notes:
So this one uses Lua and LuaRocks, which seems to be a Homebrew-like package manager for Lua. So you not only need to install Lua and LuaRocks via Homebrew but then you need to use LuaRocks to install some other packages. 

Above I have listed the two sets of commands. You'll need to run the `brew` command twice (once for Intel, once for Apple Silicon) and then you'll need to run all eight `luarocks` commands, for each for each environment (similar to Homebrew, Luarocks has its own separate folders)

Also this is the first and (as of this writing) only app I've done parallel apps for. Similar to [GemRB](GemRB.md), LuaRocks uses `.so` files for macOS and since I don't have visibility or insight into the part of LuaRocks that maintains that I just decided to leave it be and have two apps instead of one Universal one. If I ever figure out how to overcome that I'll address it but the GemRB experience left me thinking this wasn't worth the effort. 