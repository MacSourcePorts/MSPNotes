## Source Port:
# ioquake3

Game(s): *Quake III: Arena*

Homepage: https://ioquake3.org

GitHub: https://github.com/ioquake/ioq3

MSP GitHub: https://github.com/MacSourcePorts/ioq3

#
### Why is Mac Source Ports doing a build of this port?
This is the one that basically started the project (MSP)

### Versioning/Release strategy:
None. Latest code only. 

### Build System: 
Make

### Language(s):
C/C++

### Homebrew Requirements:

None. Only thing it needs is SDL2 and it comes with it. 

### Data situation
Data goes in `~/Library/Application Support/Quake3/`

### Notes:
This one is straightforward and the only library it needs comes with it. I did have to make a new library version since the one with PPC support no longer satisfies Xcode. This will probably be a similar issue with other id Tech 3 ports. On my personal `tomkidd` account I should probably lend assistance, but for `MacSourcePorts` project I'll probably just replace the library and drive on. 

### MSP Fork differences:
```
.gitignore
Makefile
code/libs/macosx-universal/libSDL2-2.0.0.dylib
code/libs/macosx-universal/libSDL2main.a
code/libs/macosx-universal2/libSDL2-2.0.0.dylib
code/libs/macosx-universal2/libSDL2main.a
macsourceports_universal2.sh
make-macosx-app.sh
make-macosx-ub.sh
make-macosx-ub2.sh
```

So this one is tied up with the changes needed to happen in the main project. I need to hammer that one out first since I'm a contributor. 