# Mac Source Ports project notes

This is a repo of notes related to the various projects built by Mac Source Ports. 

## General notes
* [Setting up development system](setup.md)

## Port notes
* [augustus](augustus.md) (Caesar III)
* [CorsixTH](CorsixTH.md) (Theme Hospital)
* [DevilutionX](DevilutionX.md) (Diablo)
* [dhewm3](dhewm3.md) (DOOM 3)
* [disasteroids3d](disasteroids3d.md) (Disasteroids 3D)
* [DXX-Rebirth](DXX-Rebirth.md) (Descent, Descent II)
* [ECWolf](ECWolf.md) (Wolfenstein 3-D, Spear of Destiny)
* [EDuke32](EDuke32.md) (Ion Fury)
* [GemRB](GemRB.md) (Baldur's Gate, Baldur's Gate II, Icewind Dale)
* [ioquake3](ioquake3.md) (Quake III: Arena)
* [iortcw](iortcw.md) (Return to Castle Wolfenstein)
* [jk2mv](jk2mv.md) (Jedi Knight II: Jedi Outcast multiplayer)
* [julius](julius.md) (Caesar III)
* [Maelstrom](Maelstrom.md) (Maelstrom)
* [OpenJK/OpenJO](OpenJK.md) (Jedi Knight II: Jedi Outcast single player, Jedi Knight: Jedi Academy)
* [OpenJKDF2](OpenJKDF2.md) (Jedi Knight: Dark Forces II)
* [OpenRCT2](OpenRCT2.md) (RollerCoaster Tycoon 2)
* [OpenTyrian](OpenTyrian.md) (Tyrian)
* [OpenTyrian2000](OpenTyrian2000.md) (Tyrian 2000)
* [OpenXcom](OpenXcom.md) (X-COM: UFO Defense, X-COM: Terror from the Deep)
* [RBDOOM-3-BFG](RBDoom3BFG.md) (DOOM 3: BFG Edition)
* [shockolate](shockolate.md) (System Shock)
* [rottexpr](rottexpr.md) (Rise of the Triad)
* [The Ur-Quan Masters](uqm.md) (Star Control II)
* [vkQuake](vkQuake.md) (Quake)
* [yquake2](yquake2.md) (Quake II)


## Extra notes
* vkQuake at one point had issues running from the app bundle. Need to figure out what's going on there. 
* ETLegacy: did not make a MSP build, offered help in the form of the Daggolin-derived entry point logic for id Tech 3 ports on Apple Silicon
* World of Padman: Project builds for Universal 2 but can't connect to most live servers. Reasons unknown.
* Daikatana: This fork lives on my personal account as a private thing, need to figure out what the deal was on the latest compiling version on Intel Mac. 
* Ion Fury: has serious performance issues on my M1 MBP that it's not having on my M1 Mini. Needs further investigation.
* shockolate: Need to make it use `MSPUtils` for path discovery
* rottexpr: Need to make it use `MSPUtils` for path discovery
* ECWolf: needs PAToken from tomkidd account, check to see if I have that written down before making a new one.