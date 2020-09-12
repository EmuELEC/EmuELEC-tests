# EmuELEC TESTS 

The files included in this repository are meant to be a TEST (beta) version of EmuELEC that might contain erros/bugs/issues!    
While we do our best to test every change some changes might break your installation!  
**DO NOT INSTALL IF YOU DO NOT FEEL COMFORTABLE DEALING WITH POTENTIAL BUGS**  
For stable releases visit: https://github.com/EmuELEC/EmuELEC  
For support: join us at discord: https://discord.gg/cbgtJTu


## CHANGELOG

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
