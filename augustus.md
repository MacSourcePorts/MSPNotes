## Source Port:
# augustus

Game(s): *Caesar III*

Homepage: https://github.com/Keriew/augustus

GitHub: https://github.com/Keriew/augustus

MSP GitHub: https://github.com/MacSourcePorts/augustus

#
### Why is Mac Source Ports doing a build of this port?
The port does make a Mac build but it's Intel-only and unsigned

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

[`augustus`](augustus.md) (this port) is a fork of [`julius`](julius.md) (and so, our fork is a fork of `augustus`). Both `augustus` and `julius` play *Ceasar III*. 

`julius` aims to be as close to the original game and source code as possible, both for the sake of recreation/preservation but also because it maintains compatibility with saved game files (so, theoretically if you had an old *Caesar III* save from somewhere it would work with `julius`, but I haven't tested this. )

`augustus` is a fork of `julius` that offers several quality of life improvements (like being able to zoom in) but at the cost of saved game compatiblity. 

I forked `augustus` and then later realized that I couldn't fork `julius` because GitHub does not allow you to fork two different repos that are forks of each other (despite the name change). 

Therefore in the case of `julius`, I'm just cloning the original repo and only adding the `macsourceports_universal2.sh` file to it. The only difference is the names used in the scripts. 

Other than this fork nonsense the two ports are straightforward. 