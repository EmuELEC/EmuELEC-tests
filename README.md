# EmuELEC TESTS 

The files included in this repository are meant to be a TEST (beta) version of EmuELEC that might contain erros/bugs/issues!    
While we do our best to test every change some changes might break your installation!  
**DO NOT INSTALL IF YOU DO NOT FEEL COMFORTABLE DEALING WITH POTENTIAL BUGS**  
For stable releases visit: https://github.com/EmuELEC/EmuELEC  
For support: join us at discord: https://discord.gg/cbgtJTu
A new forum has been open for emuelec: https://emuelec.org

## CHANGELOG

# 4.3-TEST-09062021

* Fix Stadia Gamepad. Thanks to amuzulo#1322 
* Fix issue with lzdoom loading .doom files and sound on mods
* Update some sound packages
* Fix es_systems.cfg: Add extensions to c64/c128 and Amiga (#677)
* Add Cdogs-sdl to ports
* Add Abuse to ports NOTE: WIP controls
* Add Streets of Rage Remake
* Fix Retroarch display of CJK characters
* Fix SFC not scraping
* Updated most emulators and cores
* Create folders for fbneo consoles

Amlogic-ng: 

* Add RTL8761 Bluetooth Support (#698)
* Include ssv6xxx-aml drivers

# 4.3-TEST-07312021

* Fix create /storage/roms/amstradgx4000 on boot
* Cleanup es_systems.cfg remove and add some extentions
* Add Hurrican port (Handhelds currently have no working controls) 
* Atomiswave: Remove workaround for nvmem

# 4.3-TEST-07222021
General:

* Add Flycast Stand Alone 
* Add Alternate version of Mupen64plus-nx
* Replace old filemanager for 351Files
* Fix Amstrad GX4000



# 4.3-TEST-07112021

General: 

* Fix Autoupdate
* Fix no backup restore if EEROMS was set to fat32
* Fix no external ROMS if EEROMS was set to fat32
* Fix typo on Parallel N64 32b core name
* Unify Brightness between ES and RA
* Fix advmame.sh: unset DISPLAY for Amlogic and Amlogic-ng
* Fix SuperTux2: Fix sed in launch script
* Fix vertical mode not respecting index ratio
* Fix Connect to WiFi on first boot if using es_defaults.txt
* Fix volume resets to 98% using AV
* Fix Do not redirect stdout/stderr to /dev/null in maxperf and normperf. (#661)
* emuelecRunEmu.sh: remove hardcoded bin path, this allows to use most of the binaries/scripts be called from `/emuelec/bin` or `/usr/bin` in that order
* Add Megadrive MSU to es_systems.cfg
* Add fceumm-mod libretro core to play some additional NES ROM hacks. (#658)
* New Packages: Box64, Box86, GL4es, Axe11, libglu (for future use)
* Bump most cores and emulators to current versions
* Bump Retroarch to 1.9.6

Amlogic-ng: 

* Add preliminary support for Raxda Zero 



# 4.2-TEST-06062021

General: 
* Bump Retroarch to 1.9.4
* Add auto gamepad configuration for Hypseus
* Add Non-Commercial Duckstation core (untested)
* always update es_systems.cfg on system update

Odroid Go Advance/Super & GameForce: 

* Convert screenshots from pbm to png

GameForce:
* Update U-boot and Kernel
* Fix Opentyrian
* Fix Advancemame


# 4.2-TEST-06032021

General
* Hypseus replaced by Hypseus-singe

Odroid Go Advance/Super & GameForce: 
* Update U-boot and Kernel

GameForce:
* Fix hypseus controls (#622)


# 4.2-TEST-05312021

General
* Fix latest test missing libs
* Bump RigelEnfgine to fix a bug

Odroid Go Advance/Super & GameForce: 
* Use gptokeyb for controls on Solarus
* Fix reboot while charging
* Fix retrorun reversed analogs

# 4.2-TEST-05272021

* bump Retroarch to v1.9.3
* Switch Duckstation name to Swanstation
* Rework 32bit core detection on emuelecRunEmu.sh
* Yabasanshiro: Revert back to 7ae0de7 as it gives much better performance
* Added freej2me Java games emulator, it accepts .jar files and they should go into /storage/roms/freej2me. Internet is required only on first run to download the Java JDK.
* Update most cores and emulators to latest versions

Amlogic-ng: 
* Enable qca6174 drivers (Fixes issues #611)

Odroid Go Advance/Super & GameForce: 

* Introduce RetroRun, available for Flycast for the moment

GameForce:
* Move global hotkey to button 1 to avoid conflicting hotkeys in retroarch, 1+Dpad up/down for volume, 1+Dpad lef/right for brightness
* Brightness was not correctly calculated on GameForce (PR #619)

# 4.2-TEST-05142021

General: 

* Add ee_fstype to set the EEROMS partitions to the desired file system, between FAT32 (default), EXT4, EXFAT and NTFS (read the warning about using NTFS). Instructions coming soon to Wiki/forum
* Fix OGG background music
* Update setres.sh and advmame.sh for resolution 1280x1024p60hz (PR #600)
* Fix drastic game saves & save states erased when resetting scripts & binaries to default (PR #595) 
* Add Potator a Watara Supervision emulator core (not tested)
* gptokeyb bump and fix missing trigger actions
* Crystal bump to latest
* emuelec-emulationstation bump to latest

Odroid Go Advance/Super & GameForce: 

* Bump kernel to use latest Mali G31 blobs
* Introduce RetroRun (not yet fully enabled)




# 4.1-TEST-03302021
General:
 
* Use gptokeyb as a fake keyboard for OpenBOR
* Bump Retroarch to 1.9.1

Additions: 

* Added Chocolate-Doom with support for mods
* Added Flycast 32bit as core option for Dreamcast/Atomiswave/Naomi
* Added Amstrad GX4000

Fixes: 

* Fixed OpenBor would not work after playing one game
* Fixed DevilutionX character voices were wrong
* ARM32 interpreter is now symlinked so no need for patchelf
* 
### 4.1-TEST-03142021
General:  
* Use DinguxFileManager as default on all platforms
* Bump Crystal theme which now includes a new panel (boxart), 16:9, 4:3 and CRT versions

Additions:  
* Added Ecwolf with support for mods
* Added supermariowar to ports, on the first run a fake keyboard will be used, make sure you set your gamepad and restart the game, if you need to run the fake keyboard again delete /emuelec/configs/smw/nofakekeyb and run the game again.


### 4.1-TEST-03072021

General:
 
* Enable bezels on OGS, not fully tested yet
* Bump Genesis-plus-gx and Genesis-plus-gx-wide to support FM music

Additions: 

* Added vertical aspect ratio option to OGA/S
* Added gptokeyb to enable video controls on all devices with SDL support!
* Replace jslisten with gptokeyb to kill emulators
* Added easyrpg to es_systems.cfg

Fixes: 

* Fixed an issue with ES not playing .ogg music files in BGM
* Fixed some errors messages were not wrapped and could not be read


### 4.1-TEST-02262021

General:
 
* Emulationstation: While in a game list, pressing X will move to a random game, holding X will mark it as favorite (thanks to @lethal-guitar)
* Bump PPSSPPSDL to v1.11
* Bump Duckstation to abb7631
* Pico-8: Allow saving favorite carts, include binary in backup
* Update Sonic 1 and 2 so that they work with multiple gamepads
* Bump most emulators and cores to newest git hash (check commits for specifics)
* Bump Crystal theme which now includes a new panel (boxart)

Additions: 

* Added Chocolate-Doom
* Added SuperTux and SuperTuxKart to ports
* Added Imagemagick (mainly for screenshot manipulation from CLI)
* Added logos to the ports (Thanks to Dim!)

Fixes: 

* Removed unused scripts, and fixed many small issues with scripts
* Fixed many script that were causing hangups or other issues
* Fixed gamecontrollerdb.sh it will now replace the UUID from the one in the db, this fixes weird controllers that use the same UUID as others (but are not the same)
* Fixed an issue with unicode characters not displaying correctly on the EEROMS partition (CN, JP, etc)
* Fix SonicCD Gamepad for the OGS
* Fix Pico-8 disappearing splore file
* Fix Scummvm game scan
* Fix brightness not restored after reboot on OGA/S, thanks to @miwasp, fixes issue #470
* Fixed issue with OGA/S OC not beeing applied correctly (this does not solve the random lockups on some devices)
* Fix backup/restore issues
* Fixed Retroach video recording
* Fixed Eduke not running when having lots or ROMS in ES, by enabling swap (much testing needed!)

# IMPORTANT!

This version includes a big change on how binaries and scripts are stored, basically to deal with the issue of people not reading how to properly update 
and since I am getting tired of answering the same question over and over again, lets just move all binaries and scripts to RO /usr/bin, this will force 
update all of these and make updating much simpler.

If you use custom scripts /emuelec/bin and /emuelec/lib are still in the path so you will have to deal with it accordingly. 

All configurations regarding emuelec will still be handled in /emuelec/config

**Note that this is probably not final, I still need to do a lot of testing, but keep that in mind if you want to update**


### 4.1-TEST-02182021

* Emulationstation: While in a game list, pressing X will move to a random game, holding X will mark it as favorite (thanks to @lethal-guitar)
* Fixed many script that were causing hangups or other issues
* Fixed gamecontrollerdb.sh it will now replace the UUID from the one in the db, this fixes weird controllers that use the same UUID as others (but are not the same)
* Fixed an issue with unicode characters not displaying correctly on the EEROMS partition (CN, JP, etc)
* Added SuperTux and SuperTuxKart to ports
* Fix SonicCD Gamepad for the OGS
* Fix Pico-8 disappearing splore file
* Added Imagemagick (mainly for screenshot manipulation from CLI)
* Bump PPSSPPSDL to v1.11
* Bump Duckstation to abb7631
* Fix Scummvm game scan
* Fix brightness not restored after reboot on OGA/S, thanks to @miwasp, fixes issue #470
* Removed unusued scripts, and fixed many small issues with scripts
* Fixed issue with OGA/S OC not beeing applied correctly (this does not solve the random lockups on some devices)
* Added Chocolate-Doom


### v4.0-TEST-02022021

Just a small release fixing some big bugs from last release

* Fixed ES slow downs when scrolling and changing settings
* Fixed gamepad not closing error/message window
* Fixed Pico-8 on OGS
* Fixed hotkeys not working on OGA
* Fixed ROMS on external HDD might not mount on boot
* Fixed snapshot manager (read important note)

A bug that was causing ES to lag on scrolling was fixed, but there has been a change on how ROM settings are saved, if you previously saved emuoptions.conf in a backup, you need to merge it with emuelec.conf. 

After setting the gamepad in ES it will be automatically be added to the gamecontrollerdb.txt file making them work on all SDL2 programs that support it, including PPSSPPSDL.

Important note: To properly support the new snapshot (savestate) manager, save states are now saved/loaded from /storage/roms/savestates/[system]  (example: /storage/roms/savestates/nes/) 


### Sep 11 2020

* Add DOSBox scan script (#292) - Easier way to add DOSBox games (untested)
* Use GCC optim -O3 system-wide - Squeeze a bit more performance on some cases 
* OdroidGoAdvance: use internal terminal to display error  - Uses proper rotation and error message will properly close!
* Emulationstation: bump to 4416716 
* S922x/A311D: Use a service to handle small cores - Fixes the reboot issue
* Add pcenginecd to bios check
* Add .mdf for Sega Saturn (#288)
* Odroid Go Advance: Enable rs97-commander-sdl2 (not yet properly implemented)
* VLC: bump to 3.0.11.1
* Fix MSX2 platform for scrapping
* Retroarch: Added some default core settings
* Amlogic-ng: Goodbye libhybris! - Use proper GLES headers, this fixes some gfx errors on some cores, like Mupen64


### Aug 29 2020

* Fix ports show error even on gracious exit 
* SDLPoP: Fix settings not being  saved
* Mupen64plus-nx: Use Gles3 for OdroidGoAdvance fixes #260
* emuelec-utils: Unify some small scripts for easy management
* Bios check will now be performed AFTER and ONLY if a game crashes
* OdroidGoAdvance: Added vertical mode for some cores (mostly arcade cores)
* Added a timezone selection to make it easier to set your current time
* S922x: Disabled small cores for a little performance boost
* Remove some unused cores for space
---beetle-lynx
---crocods
---dosbox-x (still available on aarch64)
---easyrpg
---xow
---libretro-bash-launcher
They can be brought back if demand exists
* re-add ssv6xxx-aml: fixes #261 (hopefully) 
* Bumped Retroarch
* Many other small under the hood fixes

Happy retrogaming! 

### Jul 13 2020

* advmame: Another attempt at auto config joysticks that should work on 
* Parallel64: bump to 76193f8
* fbterm.sh: add "error" to display a dialog box with an error for 10 secs
* emuelec-emulationstation: Bump to 7a19660
* emustation-config: make sure the BT agent is not running (this one is important)
* Add sanity checks when launching Cave Story (#218)
* missing-bios: add --filter
* updatecheck.sh: Add forceupdate test

For a more in depth list of changes check https://github.com/EmuELEC/EmuELEC/commits/dev 


### Jul 08 2020

* Added NEC PC-9800 to es_systems.cfg
* Ports: Include OpenTyrian, HodeSDL, Bermuda but only OpenTyrian has a launch script, as soon as I test the others I will add the launch script
* Added a missing core "Quicknes"
* OdroidGoAdvance: Enable 3do and Saturn, I have no idea why people want to play these systems on the OGA, but by popular demand, here they are.
* Fix/improve Bluetooth pairing
* Enable auto-updates: This will be hard to test as they are only available for stable releases, still not sure if I should enable them for beta/test releases
* Bluetooth: Try to pair gamepads at boot, to make this work you need to set your game-pad in pairing mode when EmuELEC is booting
* Initial Bluetooth management menu (#209) under setup scripts you will find a new menu driven Bluetooth pairing method, by coach1988, very useful if the regular method does not work for you. 
* YouTube search: Add default search word to ES. under the EmuELEC settings menu there is a new option to set the default word to search, in case you don't have a keyboard this can be used, not idea, but it works
* Remove tiggerhappy, was planing on using it but never got to, so it was just wasting space
* ES can now show PDF manuals from games. 
set_advmame_joy.sh: force button "a" as "ui_select" 

### Jun 28 2020

This test includes many new features some of them that will require a bit of setting up if you are upgrading. The biggest change  is that the getcores.sh file that was responsible for showing what emulators was used for what platform is no longer in use, this means that emuelec.conf and emuoptions.conf from earlier versions will no longer will compatible (well only the core/emulator part) so if you previously had set some games to run on certain emulators this needs to be redone. 

It is always suggested to do a new install for tests releases and this is required before you report a bug/issue. 

* New ES grouping by manufacturer, if you press B on the main screen of ES you will now get a group selection that will quick jump you to that manufacturer and all of its platforms.
* Added netplay to ES, although I tested it as much as I could it was a hit and miss, but I assume this is just how it works 
* Fixed retro-achievements (cheevos)
* Bumped PPSSPPSDL to 1.10
* Many small fixes are also included.

### Jun 11 2020

* OdroidGoAdvance: Add support for V1.1 with extra buttons and WiFi module, buttons might have changed a bit, taking suggestions on how to best set them up!
* Fixed AdvanceMame gamepad auto-configuration, a new option to enable/disable this has been set in the Main Menu - EmuELEC Settings  
* Removed steam controller support, I don't think anyone was using it and it was just eating resources, if many people ask for it I will enable it again. 
* Added small youtube search engine (needs a keyboard) for now its included in the Setup menu script #14
* Mplayer: Added support for .twi and .ytb files, if you include a file with a twitch or youtube address it will be played by mplayer (need internet)
* OdroidGoAdvance: Use upstream PPSSPPSDL instead of PPSSPPSDL-GO, there might be gamepad issues (NOT PROPERLY TESTED YET!)
* Bumped many emulators to latest versions (NOT PROPERLY TESTED YET!)
* Small script cleanups and bug fixes.

**WARNING:** Force copy of es_systems.cfg, when changes are made upstream to es_systems.cfg the update does not copy the new file, this version fixes that.  
 This will **REPLACE** the es_systems.cfg file if you manually changed this file those changes will need to be redone, sorry can't seem to find a better way yet. 
 
 For older release information read CHANGELOG.md
