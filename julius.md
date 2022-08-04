## Source Port:
# julius

Game(s): *Caesar III*

Homepage: https://github.com/bvschaik/julius

GitHub: https://github.com/bvschaik/julius

MSP GitHub: n/a

#
### Why is Mac Source Ports doing a build of this port?
The port does make a Mac build but it's Intel-only and unsigned

### Versioning/Release strategy:
Numbered release versions

### Build System: 
Cmake

### Language(s):
C/C++

### Homebrew Requirements:

```
brew install sdl2 sdl2_mixer libpng
```
### Data situation
Asks for the location of the data on first run. 

### Notes:
So, here's the deal. 

[`augustus`](augustus.md) is a fork of [`julius`](julius.md) (this port). Both `augustus` and `julius` play *Ceasar III*. 

`julius` aims to be as close to the original game and source code as possible, both for the sake of recreation/preservation but also because it maintains compatibility with saved game files (so, theoretically if you had an old *Caesar III* save from somewhere it would work with `julius`, but I haven't tested this. )

`augustus` is a fork of `julius` that offers several quality of life improvements (like being able to zoom in) but at the cost of saved game compatiblity. 

I forked `augustus` and then later realized that I couldn't fork `julius` because GitHub does not allow you to fork two different repos that are forks of each other (despite the name change). 

Therefore in the case of `julius`, I'm just cloning the original repo and only adding the `macsourceports_universal2.sh` file to it. The only difference is the names used in the scripts. 

Other than this fork nonsense the two ports are straightforward. 

### MSP Fork differences:
```
macsourceports_universal2.sh
res/julius.icns
```

This is the one that we only clone but the only changes are the icons and the build script