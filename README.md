# EmuELEC TESTS 

The files included in this repository are meant to be a TEST (beta) version of EmuELEC that might contain erros/bugs/issues!    
While we do our best to test every change some changes might break your installation!  
**DO NOT INSTALL IF YOU DO NOT FEEL COMFORTABLE DEALING WITH POTENTIAL BUGS**  
For stable releases visit https://github.com/EmuELEC/EmuELEC
For support join us at discord: https://discord.gg/cbgtJTu


## CHANGELOG

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
