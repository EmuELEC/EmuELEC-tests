# EmuELEC TESTS 

## CHANGELOG

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


*** OLDER UPDATES

May 13th 2020

* Added Skip Song to ES, using the left thumb button (l3) you can skip the current song
* Added a small (VERY BETA) way to view videos directly from ES, drop your .mp4, .mkv, mpg, .mov videos to /storage/roms/mplayer and they will appear in ES, it still needs theming, so they will show up withouth an image/icon
* Fixed a bug that would trigger a black screen on the OGA 10 min after waking up the device
* Fixed splash screen on 720p resolution or below
* Other small bug fixes

*** OLDER UPDATES

* Enabled CEC support and Remote support, but note that I have NOT tested it, I have no real idea on how it works, this is there for people that want to use the remote to turn on and off the device, but please do not ask me how to use it asa I do not know.
* ES now has some new options to play with including hiding extensions per platform, so if you have .bin/.cue files you can hide one of them and now have no doubles, its available on the "select" menu from a gamelist, under "view customisation" (which has a typo, but thats besides the point) 
* Flycast is now working again, plus added PSP to the no rewind list so it should work even with no rewind enabled globally (it didn't before)
As with all test releases a new clean install is HIGLY recommended, but if you insist on upgrading, remember to run "Update scripts and binaries" from the "Danger Zone" menu in "EmuELEC Settings"
* Most emulators have been updated to the latest git
a few other tweaks I am forgetting probably
* Oga has besides all the changes mentioned above a sleep mode added by @KiwiHop (many thanks!) still in need of proper testing. 
*as all tests, it is highly recommended to use a clean install, but if you insist on upgrading remember to run "Reset emuelec scripts and binaries to default" from the danger zone menu in EmuELEC settings.*
Enjoy and keep safe!
