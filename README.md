# WololoKingdoms
A program for converting AOE2HD expansions files (The Forgotten, African Kingdoms and Rise of the Rajas) to the original AOC engine format.

Note: This is a continuation of Jineapple's WololoKingdoms (https://github.com/Jineapple/WololoKingdoms). For personal reasons he has step down from this project, and I will be carrying over with his permission.

## Why ?
People who play AOE2:HD are probably aware of all the issues currently affecting the game : lobbies not starting, desyncs, lag issues etc.
The original AOC version with UserPatch doesn't suffer from as many issues, and is overall a way more stable and usable version of the engine.
However, people playing on this version of the engine are missing out on great contents provided by the expansions released for AOE2HD.
This program is an (early) attempt at providing the best of both worlds, while waiting for an even better game engine (either openage or AoE 2: DE)
Usage of the converter should hopefully be intuitive, but there are more detailed instructions below if needed.

## Requirements

To run it, you will need to own HD and its expansions. If you don't own all expansions, civilizations of DLCs that you don't own and and civs of any DLCs released later will not be available to you. That means:
1. If you don't own the Forgotten Empires (FE) DLC, you can't use this mod
2. If you don't own African Kingdoms (AK), you will only have access to AoC and FE civs (regardless if you own Rise of the Rajas or not)
3. If you don't own Rise of the Rajas (RotR), you won't have access to RotR civs.

In multiplayer, there will be three different Data Mods available, WololoKingdoms (with all civs), as well as WololoKingdoms FE and WololoKingdoms AK with limited civ pools. You will have to use one of the latter ones if you do not own all DLCs.

It's heavily recommended to get all 3 DLCs though to be able to join all games.

## How to use (with Voobly)
[Download the latest release](https://github.com/Jineapple/WololoKingdoms/releases), extract the Zip, make sure Steam is running and launch the WololoKingdoms.exe inside (It should find your HD installation automatically, otherwise copy the entire WololoKingdoms folder into your Age2HD folder and try again).
You can then use it as a mod in Voobly (To do that, click the "Settings" button next to "Launch", click the "Mod" checkbox, then select "WololoKingdoms". Make sure to select 1.5 as the patch. You can then launch as normal).  

## How to use (without Voobly)
[Download the latest release](https://github.com/Jineapple/WololoKingdoms/releases), extract it, make sure Steam is running and launch as usual.
Select the "Create an offline installation" checkbox and let the program run.
You can launch the game using the "WK.exe" in the "age2_x1/" folder.
Rarely there can be issues with creating the language_x1_p1.dll file. Usually when you get an error message regarding this, restarting the program and running it again is enough.
If this error happens every time, your original language file may be corrupt.

## Troubleshooting/Known issues/FAQ

I've done my best to make the installer stable, but sometimes it can still have issues.
Generally, if you encounter problems: Make sure you run the installer as administrator (right click the exe -> run as administrator). If you get a message about an exception, often just closing the installer and running it again helps
- **Q**: The installer can't read/write the language_x1_p1.dll when creating an offline installation! What's going on?
**A**: Creating a language_x1_p1.dll language file for offline use without Voobly can be unstable unfortunately. You may need to rerun it a few times, but it should eventually work. 
If you don't need to use an offline installation though, make sure that checkbox is unchecked, to avoid potential issues.
- **Q**: Why is my interface is messed up? It looks like this: https://imgur.com/a/xouXF
**A**: This happens if you reinstalled an older version of the compatibility patch after installing WololoKingdoms. To fix it, you can go into the Age2HD folder and delete the "compatslp" subfolder.
- **Q**: This doesn't work with Linux/Wine
**A**: I made a shell script that should create missing symlinks that don't get created under wine: https://1drv.ms/u/s!Ark-SUz3-qr5qUcUahqd95ULA_sa
Put this into your aoc folder (so next to the Voobly Mods directory) and run it. 
Note that it's possible there's a seperate, unfixed crashing issue with the offline installation, I have only managed to get the Voobly version running. It's not clear if that's an issue with WololoKingdoms or my Wine/Linux installation.

## New maps

There is a number of new maps. Many of these have a ZR@ prefix, which replace the graphics of some terrains.
ZR@sm_ maps are the special maps from the HD expansions
ZR@rw_ maps are the real world maps from the HD expansions
ZR@CtR maps are capture the relic maps. When playing these, make sure to select "Relics" as the victory condition
SD_ maps are sudden death maps, with only one TC being allowed, and losing that will make you lose the game.
NoCut_Black_Forest is a concept map, showing off the possibility to disable regular Onager cutting and enabling mangonel/onager cutting with a seperate imperial age technology.

## Regional Monks, Independent Architecture, Custom Mods

The WololoKingdoms supports Independent Architecture like this HD Data Mod: http://steamcommunity.com/sharedfiles/filedetails/?id=893953860
To replace a civ's architecture, download an IA mod for that civ from the steam workshop, find the folder you just downloaded in the steam workshop folder (usually C:\Program Files (x86)\Steam\steamapps\workshop\content\221380) and copy that folder.
You can then paste it into the /mod_override folder you'll find next to the installer.
Alternatively you can use a Voobly mod like this one: http://www.voobly.com/gamemods/mod/858/WK-Architectures-showcase
You can also paste any graphics/sound mod you want to use offline into this folder.

There's also a "new_terrain_override" folder, should you wish to use different terrain slps for the expansion terrains. You can look at "/resources/new terrains" to see the naming convention.

There are also additional monk skins for Middle Eastern/African and Asian Monks. If you don't like these, you can uncheck "Regional monks" in the installer.

## Data Mods or old patches

There are some data mods based on the regular WololoKingdoms that can be selected for installation (the regular WololoKingdoms mod needs to be installed first for it to work):
- The WK Hippo mod moves Stone Walls&Gates to the Castle Age (with full HP) and makes players start with -370 stone (30 with medium resources. At request of Tsu_Nilpferd for the Clash of the Hippo tournament.
- The WK No Wall or BBT mod - surprise, surprise - disables all walls and BBTs.
- The other mods are for watching recordings played on older versions. Make sure you also select the proper version of UP 1.5 that the game was played on (You can check that on the Voobly match page)

It's also possible for other data mods based on WK to be added to the installer. With the exception of older patches for rec viewing, you need to own all DLCs to be able to install a data mod.

## Limitations
Because of the features missing from the original AOC engine, not everything from the expansions can be replicated, this includes :
- As of now, the aim of this program is multiplayer random maps, converting campaigns etc. isn't planned. (It should be fine to play them on HD)
- There is a version of the [Bruteforce A.I](http://aok.heavengames.com/blacksmith/showfile.php?fileid=12236&f=&st=10&ci=) included and set as the default computer AI. It's not fully updated so there might be issues with the new civs.
- The hotkey menu is hardcoded, but this shouldn't be a big deal, as most of the new units are either unique units, or in the existing unit lines. Use the following hotkeys:
	- Turtle Ships use the same hotkey as Longboat/Caravels now (they used to have their own)
	- Genitours and Siege Towers use the old Turtle Ship hotkey that has become free
	- Camel hotkey for Battle Elephants
	- Wonder hotkey for Palisade Gates and Feitorias
	(The in-game hotkey menu has been adjusted accordingly)
- Everything else should be working identically to the HD version, but it's possible I've overlooked something.

## Keep in mind
The Forgotten team has made a fantastic work with their expansions and, while this is probably not the way they expected their expansions to be played, I hope they can understand that many people are disapointed with the current state of AOE2HD engine.
If you want to share this with other people so you can play together, send them this page, everyone needs to generate their files by themselves using this program and the files from their copy of AOE2HD with the expansions. If there are problems with this, report the issue and I will try to fix it.

## How to build

The project is made of two parts: a library `libwololokingdoms` and the installer application. The library creates a `libwololokingdoms.dll` that contains the conversion logic and is used by the installer application.

You need a C++17 capable compiler because this project uses the new `<filesystem>` API.

Some dependencies are added as git submodules. To get them, do:

```bash
git submodule init
git submodule update --recursive
```

### libwololokingdoms

libwololokingdoms can be built with Make. It depends on genieutils which requires CMake as well. When building the installer application, libwololokingdoms is built automatically.

If you want to build libwololokingdoms without the installer application, do this in the root of this repository:

```bash
# Build a .so file for linux:
make -C libwololokingdoms linux
# Build a .dll file for Windows:
make -C libwololokingdoms win32
```

The Makefile will build libwololokingdoms, and genieutils and its dependencies. It outputs two files into `libwololokingdoms/bin/PLATFORM`: `libwololokingdoms` and `libgenieutils`.

**TODO add build instructions for Windows host**

### Installer Application

The installer application is a Qt app. You can use Qt Creator to build it, or use the Qt command line tools and Make.

The installer requires the Steamworks SDK, which it uses to check if and where HD Edition is installed. Get it from [Steam](https://partner.steamgames.com/doc/gettingstarted).

To build the project on the command line:

```bash
qmake WololoKingdoms.pro
make
```

libwololokingdoms will be built automatically if it wasn't already.

## Special thanks
- Tails8521 for the African Kingdoms version of this installer. Without him this would never have happened.
- Jineapple for reviving this program when Rise of Rajas came out, for all the countless hours he spent programming and fixing bugs for the WK experience to be as good (if not better) as HD.
- The UserPatch team for making the new bonuses possible to use and all other great improvements that Userpatch brings.
- The folks at Voobly for the support offered and a great platform to play the mod on.
- Apre, Tapsa and sandsmark for the genieutils library
- Tapsa for Advanced Genie Editor
- Alqualunte for advices and testing
- CheeseOnToast for making his [A.I](http://aok.heavengames.com/blacksmith/showfile.php?fileid=12236&f=&st=10&ci=) compatible with this project
- Phoenix1vs for converting the interfaces for AK and RotR civilizations.
- Saint_Michaels for creating the Independent Architecture mod on Steam which served as a template for this function on WololoKingdoms.
- Shulker for creating an in-game logo for WololoKingdoms
- The Forgotten Empires team for three great expansions!

## License

[GPL-3.0](./COPYING)
