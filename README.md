# Mac Source Ports project notes

This is a repo of notes related to the various projects built by Mac Source Ports. 

## General notes
* [Setting up development system](setup.md)

## Port notes
* [Abuse_1996](Abuse_1996.md) (*Abuse*)
* [ArxLibertatis](ArxLibertatis.md) (*Arx Fatalis*)
* [augustus](augustus.md) (*Caesar III*)
* [bstone](bstone.md) (*Blake Stone: Aliens of Gold*, *Blake Stone: Planet Strike*)
* [CorsixTH](CorsixTH.md) (*Theme Hospital*)
* [DevilutionX](DevilutionX.md) (*Diablo*)
* [dhewm3](dhewm3.md) (*DOOM 3*)
* [disasteroids3d](disasteroids3d.md) (*Disasteroids 3D*)
* [DXX-Rebirth](DXX-Rebirth.md) (*Descent*, *Descent II*)
* [ECWolf](ECWolf.md) (*Wolfenstein 3-D*, *Spear of Destiny*)
* [EDuke32](EDuke32.md) (*Ion Fury*)
* [fheroes2](fheroes2.md) (*Heroes of Might and Magic II*)
* [GemRB](GemRB.md) (*Baldur's Gate*, *Baldur's Gate II*, *Icewind Dale*)
* [Good-Robot](Good-Robot.md) (*Good Robot*)
* [ioquake3](ioquake3.md) (*Quake III: Arena*)
* [iortcw](iortcw.md) (*Return to Castle Wolfenstein*)
* [jk2mv](jk2mv.md) (*Jedi Knight II: Jedi Outcast* multiplayer)
* [julius](julius.md) (*Caesar III*)
* [Maelstrom](Maelstrom.md) (*Maelstrom*)
* [OpenJK/OpenJO](OpenJK.md) (*Jedi Knight II: Jedi Outcast* single player, *Jedi Knight: Jedi Academy*)
* [OpenJKDF2](OpenJKDF2.md) (*Jedi Knight: Dark Forces II*)
* [OpenRCT2](OpenRCT2.md) (*RollerCoaster Tycoon 2*)
* [OpenTyrian](OpenTyrian.md) (*Tyrian*)
* [OpenTyrian2000](OpenTyrian2000.md) (*Tyrian 2000*)
* [OpenXcom](OpenXcom.md) (*X-COM: UFO Defense*, *X-COM: Terror from the Deep*)
* [RBDOOM-3-BFG](RBDoom3BFG.md) (*DOOM 3: BFG Edition*)
* [Serious-Engine (INCOMPLETE)](Serious-Engine.md) (*Serious Sam: The First Encounter*, *Serious Sam: The Second Encounter*)
* [rottexpr](rottexpr.md) (*Rise of the Triad*)
* [shockolate](shockolate.md) (*System Shock*)
* [uHexen2](uHexen2.md) (*Hexen II*)
* [The Ur-Quan Masters](uqm.md) (*Star Control II*)
* [vkQuake](vkQuake.md) (*Quake*)
* [yquake2](yquake2.md) (*Quake II*)


## Extra notes
* vkQuake at one point had issues running from the app bundle. Need to figure out what's going on there. 
* ETLegacy: did not make a MSP build, offered help in the form of the Daggolin-derived entry point logic for id Tech 3 ports on Apple Silicon
* *World of Padman*: Project builds for Universal 2 but can't connect to most live servers. Reasons unknown.
* *Daikatana*: This fork lives on my personal account as a private thing, need to figure out what the deal was on the latest compiling version on Intel Mac. 
* *Ion Fury*: has serious performance issues on my M1 MBP that it's not having on my M1 Mini. Needs further investigation.
* shockolate: Need to make it use `MSPUtils` for path discovery
* rottexpr: Need to make it use `MSPUtils` for path discovery
* ECWolf: needs PAToken from tomkidd account, check to see if I have that written down before making a new one. Also we should link to their Universal 1 port
* iortcw: We should link to their Universal 1 port

## Third Party Ports
* Raze [[github](https://github.com/coelckers/Raze)] (*Duke Nukem 3D* and other Build engine games)
* [GZDoom/ZDoom](https://zdoom.org/) [[github](https://github.com/coelckers/gzdoom)] (*DOOM* and other id Tech 1 games)
* [Aleph One](https://alephone.lhowon.org/) [[github](https://github.com/Aleph-One-Marathon)] (*Marathon* trilogy of games)
* [OpenTTD](https://www.openttd.org/) [[github](https://github.com/OpenTTD/OpenTTD)] (*OpenTTD*/*Transport Tycoon Deluxe*)
* *Bugdom* [[github](https://github.com/jorio/Bugdom)]
* *Otto Matic* [[github](https://github.com/jorio/OttoMatic)]
* *Nanosaur* [[github](https://github.com/jorio/Nanosaur)]
* *Mighty Mike* [[github](https://github.com/jorio/MightyMike)] 
* *Cro-Mag Rally* [[github](https://github.com/jorio/CroMagRally)] 
* [*The Battle for Wesnoth*](https://www.wesnoth.org/) [[github](https://github.com/wesnoth/wesnoth)]
* [OpenRA](https://www.openra.net/) [[github](https://github.com/OpenRA/OpenRA)] (*Command & Conquer*, *Red Alert*, *Dune 2000*)
* [*Warzone 2100*](https://wz2100.net/) [[github](https://github.com/Warzone2100/warzone2100)] (Ad Hoc Signed)
* [RVGL](https://rvgl.org/) [no source] (*Re-Volt*) *Ad Hoc Signed*
* [RuneLite](https://runelite.net/) [[github](https://github.com/runelite)] (*Old School Runescape*)
* [*Unreal Tournament*](https://www.oldunreal.com/) [no source]
* Fallout 2 CE [[github](https://github.com/alexbatalov/fallout2-ce)] (*Fallout 2*)
* [Exult](http://exult.sourceforge.net/) [[github](http://prdownloads.sourceforge.net/exult/exult-1.8.tar.gz)] (*Ultima VII*, *Ultima VII Part Two*)
* [vcmi](https://vcmi.eu) [[github](https://github.com/vcmi/vcmi)] (*Heroes of Might and Magic III*)
* [OpenMW](https://openmw.org/)[[gitlab](https://gitlab.com/OpenMW/openmw)] (*The Elder Scrolls III: Morrowind*)

## Ports we're not currenly building
* [fallout2-ce](fallout2-ce.md) (the project now makes its own builds)
* [vcmi](vcmi.md) (project now makes is own ad hoc signed builds)


## Warnings
GemRB: as of 8/10/2022, the CMake files for GemRB in the master branch were modifying the identifier of my SDL2 libraries. The issue was that they were being changed to `@loader_path/../Frameworks/libSDL2.dylib` and this causes dylibbundler to get stuck. 

If this happens in the future the following commands can fix it

```
install_name_tool -id /usr/local/lib/libSDL2.dylib /usr/local/lib/libSDL2.dylib
install_name_tool -id /opt/homebrew/lib/libSDL2.dylib /opt/homebrew/lib/libSDL2.dylib
```