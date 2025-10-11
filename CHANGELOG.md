# Changelog

## RetroBat 7.5
<details>

### Emulators\cores:
- Bump libretro-stella
- Bump libretro-LRPS2
- Bump BigPEmu
- Bump Bizhawk
- Bump Dolphin
- Bump Duckstation
- Bump ForceEngine
- Bump Gopher64
- Bump JGenesis
- Bump MAME (standalone & libretro) to 0.281
- Bump melonDS
- Bump mGBA
- Bump pcsx2
- Bump PPSSPP
- Bump shadps4
- Bump Supermodel
- Bump Xenia and Xenia-canary
- Bump Xemu
- Bump Ymir
- Add namco3xx with Teknoparrot

### Fixes:
- BIZHAWK: fix core selection for PCE and Gameboy
- BIZHAWK: fix launch error for ngpc and supergrafx
- CONTROLLERS: fix Dualsense controller spamming when connected in bluetooth
- EDUKE: send -j command by default if not specified in .eduke32 file
- HBMAME: fix error on launch
- MAME: fix an issue where START and SELECT were not assigned (standalone MAME)
- MESEN: fix json config
- PCSX2: messages and notifications are now centered to not be hidden below bezels
- RETROARCH: default video driver to 'gl' if user has set to auto
- RETROARCH: try to fix case where all controllers are assigned to a single player with dinput controllers
- TEKNOPARROT: fix some buttons not mapped (particular extension buttons for few games)
- TEKNOPARROT: when using wiimote as gun, allow setting buttons on another keyboard (e.g. Test and Service)
- XROAR: fix "exec" command for coco

### Features:
- BIZHAWK: add Microphone on L2 button for nds
- CEMU: add toggle screen button
- DOLPHIN: change mapping of wii gun setting to remove dual action of mouse middle click
- DOLPHIN: add nunchuk shake on R2 button when using a profile of emulated wiimote with nunchuk
- DOLPHIN: add option to define if R2/L2 for nunchuk simulates shake or swing
- FLYCAST: add possibility to define mappings for arcade layouts in yml file (8buttons, 8buttons variation and 6buttons)
- LR-CAP32: add some options
- LR-DOSBOX_PURE: add option to save per content when loading an OS
- LR-GAMBATTE: add more palette options (with management of TWB64 and PixelShift)
- LR-GENESIS_PLUS_GX: add some options
- LR-MUPEN64: add some options
- LR-NESTOPIA: add more flexible crop options
- LR-OPERA: add options
- LR-MAME: add option to disable artworks located in saves\mame\artwork
- MAME: add additional games autoconfig
- MAME and LR-MAME: RetroBat will now backup the .cfg files before overriding them (avoid loosing your self-made config !)
- MAME and LR-MAME: Add bios selection for NEOGEO64 system
- MESEN: add option to select rumble controller
- MESS: autoconfig for casloopy, advision and gamecom
- MGBA: add interframe blending option
- MGBA: add controller autoconfiguration
- MUPEN64 (RMG): add overscan options
- PSX: add memcard options in libretro
- RETROARCH: add option to allow shader override saved by user
- RETROARCH: add option to allow global config override
- SATURN: add memcard options in libretro
- SCUMMVM: add padtokeyboard
- SHADPS4: assigns retrobat p1 controller to shadps4 default controller
- SNES9x: add few features (stretch, filters)
- STEAM: if the option "scan non-installed games" is enabled and no api key is provided, try user public profile
- SUPERMODEL: add possibility to manage game mappings in yml file, also add layout option (for arcade sticks)
- VITA3K: if the game ID is missing in the gamefile name, RetroBat will still run vita3k without autoloading a game

### Other stuff:
- add mouse option to playstation emulators
- DS4 and DUALSENSE CONTROLLERS: add option to enable SDL enhanced feature : when enabled - controller will not be compatible with emulators using directinput until you switch it off and on again
- RETROARCH: do not override nor delete inputremap file when controller autoconfig is disabled and back it up when enabling autoconfig
- Retrieve retroarch error from retroarch logs to display in RetroBat
- Installer is now able to give the filesize before installing an emulator
- RetroBat.exe: fix error message when path has a space
- RetroBat.exe: fix false positive when executable name has been changed
- RetroBat.exe: warning if an instance of RetroBat is already running
- RetroBat.exe: fix quick show of desktop by adding a blackscreen on top
- RetroBat.exe: fix monitor where video and blackscreens are displayed
- Input mapping: add few fbneo and MAME default input mappings
</details>

## RetroBat 7.4
<details>

### Emulators\cores:
- Bump MAME & lr-mame to 0.280
- Bump HBMAME to 0.245.26
- Bump MESEN to 2.1.1
- Bump YMIR to 0.1.7.0
- Bump Azahar to 2123.1 (and add compressed file extension)
- Bump RPCS3 to 0.0.37-18022
- Bump retroarch cores: picodrive
- Add MAME for zinc and model2
- Add XRoar for Tandy CoCo (with support of .autorun files)
- Add standalone DesMuMe emulator (Nintendo DS)
- Add Power Bomberman (port section)
- Add .tap extension to VICE cores

### Fixes:
- EMULATIONSTATION: fix reading of .cbz files
- LR-KRONOS: fix resolution
- MAME: when started from RetroBat menu, add command lines in order to use the same folders
- MAME: fix potential null pointer
- MAME, MODEL2, SUPERMODEL: implemented a new way of defining controller index, hoping it will fix the default indexes sometimes being incorrect
- RETROARCH: disable core config override ON by default
- RETROARCH: fix saves paths that were in subfolders with latest update (you might have to check your saves...)
- CONTROLLERS: fix 8BitDo n64 controller select button
- PADTOKEY: fix an issue with joystick mapping
- SWITCH (EDEN, SUDACHI, CITRON, YUZU, SUYU): fix controller guid retrieval, should not need controllerinfo.yml file anymore

### Features:
- EDUKE32: align game format with batocera (.eduke32 files)
- FBNEO: enable hiscore and align with libretro-fbneo
- LR-GAMBATTE: add coloration feature
- LR (NES): add "Region" setting from RetroBat
- MAME: add option to select segastv bios
- MAME and libretro-MAME: initiated controller autoconfiguration database (for now only a few games have been set)
- MAME (standalone): implement GUNs management
- STEAM: add logic to wait for Steam game installation (if game is not installed)
- STEAM: add logic to get also games that are not installed
- CONTROLLERS: add autoconfiguration of 8bitdo M30 2.4ghz version to megadrive and saturn systems
- RETROARCH: add mechanism to update libretro cores when update is available on FTP
- NDS: add microphone options for Melonds and lr-melonds
- WII: add some profiles to manage bongos, drums, guitar...

### Other stuff:
- Ensure emulatorlauncher code can work with regional system names (genesis, turbografx, turbografxcd, famicom, sfc, segacd)
- gamecontrollerdb: add 2 models of 8BitDo ultimate 2C
- MAME version detector: optimize speed
- RetroBat.exe is now the new RetroBat launcher
- STORE GAMES will not be scanned by default, option is OFF on install
- Improve performance on loading store games (threading) - should be a lot faster
- Better management of regional consoles in EmulatorLauncher (sfc, famicom, genesis, turbografx, turbografxcd, segacd)
- Additional translations (french mostly - if you want to translate to your own language do not hesitate to contact us)
</details>

## RetroBat 7.3.2
<details>
  
### Emulators\cores:
- Add chihiro-gun emulator (chihiro-ds)
- Bump hypseus to 2.11.6
- Update Demulshooter to version 16

### Fixes:
- EMULATIONSTATION: fix reading of .cbz (7.3.2.1)
- MAME: change cfg directory to "saves\mame\cfg" (previously was "bios\mame\cfg")
- MAME: when started from RetroBat menu, add command lines in order to use the same folders (7.3.2.1)
- MAME: fix potential null pointer (7.3.2.1)
- RETROARCH: disable core config override ON by default (7.3.2.1)
- RETROARCH: fix saves paths that were in subfolders with previous update (7.3.2.1)

### Features:
- DEMULSHOOTER: add some changes for detection of windows games
- EDEN: align features with more recent version
- FBNEO: enable hiscore and align with libretro-fbneo (7.3.2.1)
- GOG: now launch games through GOG launcher instead of executable
- LIBRETRO-VICE: add option to set true drive emulation
- WINDOW STORE GAMES: add icons to shortcuts

### Other stuff:
- New RetroBat-New executable to start RetroBat
- First version of bluetooth module allowing to sync bluetooth devices from RetroBat directly (might not work yet with bluetooth-le devices)
- DEV: add more logs to Libretro controller configuration to be able to debug controller issues better
- SCRIPTS: all scripts are now async (you can force sync/async behavior by naming your script with -wait/-nowait at the end (before the extension)
</details>

## RetroBat 7.3.1
<details>
  
### Emulators\cores:
- Bump Xenia-Manager to version 3
- libretro-fbneo is now the default core for CPS1, CPS2 and CPS3 systems

### Fixes:
- EMULATIONSTATION: fix some issues with script (sync vs async)
- EMULATIONSTATION: fix downloads of some heavy bezel projects (MAME...)
- MAME64: fix autofire plugin option linked with layout plugin
- OPENGOAL: check presence of config files before trying to modify them
- TEKNOPARROT: fix default mapping for coin button in contra
- TSUGARU: update way of checking for bios file before launching a game
- WINDOWS: fixed running games as bat and cmd

### Features:
- CHIHIRO: default to EMS Top Gun controller when "use_guns" option is set
- N64: add autoconfiguration of new 8BitDo N64 controller
- RETROARCH: add ability to define controller mapping as per a json file for any controller (example provided for new 8bitDo N64 gamepad)

### Other stuff:
- DEV: new tool RetroBuild.exe to build RetroBat
- DEV: first version that uses the new upgrade executable
</details>


## RetroBat 7.3
<details>

### Emulators\cores:
- Add old CXBX version for CHIHIRO and choice to use newer CXBX also
- Add Teknoparrot to Triforce and Namco2x6 systems
- Add epic, amazon, eagames and gog systems (grouped with windows by default)
- Bump Dolphin to 2506a
- Bump Gopher64
- Bump libretro cores : kronos, mupen64, fceumm
- Bump mame (standalone and core) to 0.278
- Bump Opengoal
- Bump pcsx2 to 2.4 stable
- Bump pdark
- Bump shadps4 to 0.10.0.0
- Bump Ymir to 0.1.5.0
- Bump Zesarux
- Add .m3u extension to pcfx and pcenginecd

### Fixes:
- AZAHAR: fix placement of screen when using default bezels
- AZAHAR: fix update check setting
- BIZHAWK: fix bezels with direct3D
- CHIHIRO: change gun mapping for start from "ENTER" to "1"
- DOLPHIN: fix microphone feature
- DOLPHIN: fix disc change shortcuts
- LIBRETRO: fix gun buttons for start and select (assigned to 1 and 5)
- LIBRETRO: fix monitor index
- LIBRETRO-MAME: fix mess boot commands not working
- LR-GEARGRAFX: add pad layout options and tattoos
- LR-GENESIS_PLUS_GX: add monogun option
- MODEL2: fix guns configuration
- RYUJINX: fix resolution setting breaking settings
- TRIFORCE: fix default GameSettings files
- VPINBALL: fix use of .ini file when running from RetroBat wheel menu
- YMIR: fix tattoos and align controller layout options with other emulators

### Features:
- ARES: add sync options
- BIZHAWK: add turbo option for GBA
- DOLPHIN: gamecube saves folder to "saves\gamecube\dolphin-emu\User\GC\<region>"
- DOLPHIN: align wii nand path folder to "saves\wii\dolphin-emu\User\Wii" (standalone & Libretro)
- DOLPHIN: add option to disable wiimote continuous scanning
- DOLPHIN: add option for bluetooth passthrough
- GAMECUBE: add option to sync saves between standalone and libretro core
- GOPHER64: add controller profiles
- LIBRETRO-DOLPHIN: add retroachievements
- LIBRETRO-DOLPHIN: libretro gamecube saves folder to "saves\gamecube\dolphin-emu\User\GC\<region>\Card A"
- MAME: add -pedal_device command line option
- MEDNAFEN: add bezel for GBA
- MEGADRIVE: add new controller layout option
- PCSX2: add option to set stick buttons as pressure modifiers
- PLAY!: add possibility to perform specific mapping for arcade games based on yml file
- PSXMAME: add some options in RetroBat (video driver, windowed, sleep)
- REDREAM: add .m3u support
- RETROARCH: add option to force configuration of arcade sticks based on json file
- STEAM: add new method to monitor running game with registry and focused window
- TEKNOPARROT: add some games in controller autoconfiguration database
- TEKNOPARROT: add option to show mouse cursor
- WINDOWS: add steam, amazon, gog, epic and eagames as systems and perform automatic creation of game shorcuts at startup of RetroBat for installed games
- WINDOWS: for .lnk and .game, RetroBat will now launch with arguments if arguments are specified
- YMIR: add 3DPad option
- YMIR: add autoconfiguration of 8bitdo M30 controller

### Other stuff:
- Achievements: add switch to enable unofficial achievements
- Fix french translations
- Do not show tattoos when disable controller autoconfig is ON
- New Update systems (more flexible) ==> will be active starting with next update
- move user-made tattoos to "user" folder in RetroBat root
- Bump SDL2
- RetroBat will not update nvram files anymore with new update (starting with next update)
- Wheels: add configuration of Thrustmaster T300 to model2 emulator
</details>

## RetroBat 7.2
<details>

### Emulators\cores:
- Add DICE
- Add EDEN
- Add Geargrafx core for SuperGrafx
- Add SOLARUS 2.0 as an emulator option for Solarus (keep 1.6 as default until games are updated)
- Add Ymir (saturn)
- Remove Lime3DS
- Bump ARES to 144
- Bump Azahar to 2121.2
- Bump Cemu to 2.6
- Bump CXBX-Reloaded
- Bump Duckstation
- Bump FBNEO and lr-fbneo to version from april 2025
- Bump Flycast and libretro-flycast to 2.5
- Bump Hypseus to 2.11.5 (extension .daphne does not work anymore, you must switch to .hypseus)
- Bump JGenesis to 0.10.0.0
- Bump MAME & lr-mame to 0.277
- Bump MESEN to 2.1.0
- Bump Mupen64 (RMG) to 0.7.8
- Bump Play! to 0.70
- Bump PPSSPP to 1.19.1
- Bump ScummVM to 2.9.1.0
- Bump ShadPS4 to 0.9.0
- Bump Vita3K
- Bump xenia-canary
- Add mesen standalone for colecovision, gba and pcenginecd systems
- Recommanded ryujinx version: greemdev canary (1.3.1 or above)
- Recommanded citron version: version from 16/03/2025 (0.6.1)
- Recommanded sudachi version: version from 25/03/2025 (1.0.15)

### Fixes:
- CITRON: fix some controller autoconfiguration issues
- LIBRETRO FLYCAST: fix controls issues & generate per-game mapping from yml file
- MAME: fix ti99 launch when speech synthesizer is enabled (MAME 0.276 required change)
- MEDNAFEN: fix null pointer when no controller is connected
- MELONDS: fix configuration file for standalone emulator
- MELONDS: fix toggle fullscreen shortcut (assign to TAB instead of F9)
- PCSX2: fix RetroBat deleting multiple binds
- PHOENIX: fix saving nvram on exit
- RYUJINX: fix controllers and settings in some specific cases
- LIBRETRO-SCUMMVM: fix screen positioning when video driver is not openGL
- SHADPS4: fix issues with config file paths
- SUDACHI: fix some controller autoconfiguration issues
- TEKNOPARROT: Fix option to use test/service on keyboard when using lightguns
- TEKNOPARROT & FLYCAST: Fix issues when using multiple wiimotes (crash in flycast and potential inversion in teknoparrot)
- Fix sinden lightgun software button mapping and add global option
- ZX81: fix extensions
- Fix kid mode not showing games in certain cases

### Features:
- LIBRETRO-FBNEO: add arcade controller layouts
- LIBTRETRO-OPERA: add logic to autoconfigure megadrive-like controllers (active for 8bitdo m30 so far)
- LIBTRETRO-VIRTUALJAGUAR: add option to map jaguar pro controller
- CHIHIRO: add option to launch demulshooter for vcop3
- DOLPHIN: add default iso feature
- DOLPHIN: add mouse to control IR movement when using keyboard
- DOLPHIN: add .dol extension
- DOLPHIN: add gba capability (rom choice, controller, microphone, bios path)
- DOLPHIN: re-added the possibility to set the wiimote layout based on rom filename
- DOLPHIN: add option to hide or show mouse cursor
- DUCKSTATION: remove -portable argument (new duckstation versions removed this argument)
- FBNEO: add option to enable IPS patches
- FBNEO: additional games automatic mapping
- MAME: enable "layout" plugin per default (and option to disable it)
- MAME: update mapping for BUTTON7 and BUTTON8
- MUPEN64: Add SavestateWatcher to Mupen64(RMG)
- PCSX2: add option to select in which port to plug multitap (to use for some games like def jam)
- SATURN STANDALONE EMULATORS: add option to select bios to use
- STEAM: add steamexecutables database (steamexecutables.json) for the community to fill the executable names of games with the gameID
- TRIFORCE: add mapping options for some triforce games
- VPINMAME: add sound_mode option
- XENIA-CANARY:  add option to specify profile to use from Retrobat

### Other stuff:
- align all features submenu order
- Bump SDL3.dll
- Kill javaw process when closing free2jme core (this should solve issue with the core where sound continues after exit)
- Move ryujinx from dynamicjson to NewtonSoftJson (will fix issues for some controllers when guid was fully numerical)
- Moved files for retroarch inputmapping (cores & hotkeys) override, fbneo and teknoparrot mappings in retrobat\user\inputmapping, so they don't get overriden with updates
- Remove april fools code (you can delete your roms\ps5 folder)
- Add a readme document in tattoos folder
- Update installer information for developers
- Fix errors in full build
- Refactor code for 7zip, now use dll instead of exe
- Geolith - allow .zip files and check if zip file contains .neo file
- Colecovision: add .7z extension
- Emulationstation: some performance fixes
- Update gamecontrollerdb file (used to map dinput controllers) & add ability to enter same guid with variants when dpad allows digital and analog
</details>

## RetroBat 7.1
<details>
  
### Emulators\cores:
- Update VPinball to 10.8 (including Pup)
- Update RetroArch to 1.20
- Update Hypseus to 2.11.4
- Add Singe system
- Add j2me
- Add Altirra (atari800,atari5200,xegs)
- Add gopher64 (N64)
- Add dragon32 with xroar
- Add azahar to Nintendo 3DS
- Bump Dolphin to 2503
- Bump Yabasanshiro to 1.16.7
- Bump MAME and libretro:mame to 0.276
- Bump theforceengine (settings.ini needs to be moved from Documents to emulator folder)
- Bump Duckstation to 0.1.8773
- Bump PCSX2 to 2.3.232
- Bump Shadps4 to 0.7
- Bump RPCS3

### Fixes:
- AQUARIUS: add missing folder
- DOLPHIN: fix controller configuration bug when using multiple Switch Pro controllers - Thanks RESET_YANG for identification
- DOLPHIN: align saves .cgi files with libretro (saves will move from saves\dolphin\User\GC\<region> to the \Card A subfolder)
- DOLPHIN-TRIFORCE: Fix a bug with switch Pro Controller - Thanks to stoffies | CHERRY XTRFY for identification
- FLYCAST: fix features for texture upscaling
- FLYCAST: automate lightgun device type when using guns + fix button mapping for guns
- MODEL2: fix use of gamepad for gun games
- MODEL3: add generation of Supermodel.ini file in case it does not exist (user-deletion) - Thanks Grobius for pointing that out
- MODEL3: multiple fixes in controller indexing - thanks nkvoll for the contribution
- lr-pcsx2: set default video driver to glcore instead of gl
- RPCS3: fix controller config when using DS3 with dshidmini in xinput mode
- SNES9X: fix controller of player 1 disabled when only keyboard is connected
- SNES9X: align save folder with other snes emulators (mednafen, mesen, retroarch)
- TEKNOPARROT: write APM3ID only if the value entered in RetroBat is different from the value already specified in TP
- TEKNOPARROT: fix option for test and service on keyboard not working for Gungames
- XENIA-CANARY: fix features with newer canary versions
- XENIA-MANAGER: fix RetroBat not using game specific config file - Thanks mrEOXD for identification

### Features:
- 3DS: add ability to load touchprofiles on standalone emulators
- FPINBALL: add dmdext
- HYPSEUS: added management of zip files and useAlt for multipack games
- Libretro boom3: add some features
- Libretro-Flycast: add wheel management
- Libretro-x1: add features
- Libretro-lrps2: add parallel-gs options
- MELONDS: add shortcut to toggle fullscreen (F9 or hotkey+L1)
- Model2: add pad2key - can be useful when using guns with low number of buttons, to map start and coin to the gamepad
- PCSX2: add option to use left stick as dpad
- RETROARCH: add option to force only 1 player (can be useful for some nes games such as arkanoid)
- RETROARCH: add option for alternative hotkeys layout
- RETROARCH: add analog to dpad option
- RETROARCH: core input remap is not deleted but modified
- RETROARCH: when running an arcade system with keyboard, force 1 and 5 for start and credits
- RETROARCH: add ability to override controller shortcuts with a yml file
- RPCS3: add RSX FIFO accuracy option
- RPCS3: first tentavise of lightguns with raw mouse
- RYUJINX: add possibility to override controller guid with file
- SHADPS4: add a few features, enable launching from .m3u and .lnk files
- TEKNOPARROT: renamed "teknoparrotExecutables.yml" to "teknoparrotInfo.yml" and add ability to force GameProfile in the file
- VG5K: add -ramsize option
- VPINBALL: add a few features

### Other stuff:
- Change way to manage singe and actionmax games - no more symlinks, use -singedir argument : you need to add the frameworks in the roms folder
- Rename segacd to megacd
- Add global option to select preferred fullscreen mode (exclusive or borderless) for emulators
- Sinden Software is now killed when exiting a game
- Add option to configure sinden gun in joypad mode
- Add autoconfiguration of sinden gun buttons
- guns: enhancement of controls based on type of gun in several emulators
- Add some wheels in the internal database
- Add shadPS4 to the Retrobat menu
- Add ps4 screenscraper id
- Add detection of lightguns in RetroBat interface : Blamcon, RetroShooters, Aimtrak, AELightgun
- Add some explanations in header of controllerinfo.yml file
- RETROBAT menu : fix lime3ds executable, add shadps4 and remove citra-canary and yuzu-ea
- Bump 7-zip to 24.9
- Bump SDL to 2.32
- Add SDL3 joysticks management
- SHADPS4: remove unnecessary -g argument
- Interface: RetroBat will now list interlaced resolutions (next step is to work on emulator integration)
- Add ability to select the path for decompression of zipped games
</details>

## RetroBat 7.0
<details>
  
### Emulators/Cores:
- Add openjazz (Jazz JackRabbit engine)
- Add Philips VG5000 (with MAME)
- Add MAME to Odyssey2 – Videopac
- Add Mattel Aquarius
- Add libretro:yabasanshiro (SATURN)
- Add libretro:gpsp (GBA)
- Add yabasanshiro for Saturn
- Add kronos for Saturn
- Add Holani core (Lynx)
- Add Noods core
- Add Philips P2000T with libretro:m2000
- Add Mandarine for 3DS
- Add Perfect Dark port (requires the right ROMs)
- Add Bizhawk for Intellivision
- Add Bizhawk for ChannelF
- Add B2 core for BBC Micro
- Add Citron emulator
- Add Vitaquake2-zaero, Vitaquake2-rogue, and Vitaquake2-xatrix (select automatically the right core based on ROM path)
- Add Ardens core (Arduboy)
- Add Steam system
- Add DoubleCherryGB (GB/GBC)
- Add CorsixTH (Theme Hospital port)
- Add Dhewm3 (Doom 3)
- Add CDogs
- Add libretro core doukutsu_rs (Cave Story)
- Add PS4 (shadPS4)
- Bump ScummVM to 2.9.0
- Bump CEMU to 2.5
- Bump BIGPEMU to 1.18
- Bump Citra to latest pablomk7 version
- Bump JGenesis generator for compatibility with version 0.8.2
- Bump PCSX2 to version 2.3.83
- Bump Vita3K
- Bump xemu
- Bump Lime3DS to 2119.1
- Bump Melonds (standalone)
- Bump LRPS2 core
- Bump PPSSPP standalone and core
- Bump Bizhawk
- Bump MAME64 and libretro-MAME to 0.273
- Add Xenia-manager as emulator
- Set Xenia-canary as default for Xbox360

### Fixes:
- BIGPEMU: Fix SDL2 plugin when multiple controllers of the same type (needs BigPEmu 1.18)
- BIZHAWK: Fix RetroAchievements login (encrypt token)
- CEMU: Disable gameprofiles when running Cemu from RetroBat
- DOLPHIN: Fix configuration of Dualsense and Switch Pro controllers
- FLYCAST: Fix guns on Flycast standalone
- Libretro:Gambatte: Fix auto colorization value
- MEDNAFEN: Fix controller automapping for XInput controllers
- MODEL2: Fix option for using shoulder buttons to accelerate/brake, fix controller when not XInput
- PCSX2: Fix SDL order (enable SDL raw input)
- PCSX2: Fix savestates folder to enable savestates in RetroBat interface
- RETROARCH: Fix possibility to use Monitor Index 1
- RPCS3: Previously, RPCS3 would use the game custom config file if it exists in the emulator config folder, now it always uses the default config by default, and a switch needs to be activated to use custom config
- RPCS3: Fix XInput controller mapping when using the option to force SDL driver
- SOH: Fix controls when controller does not have all buttons required
- STEAM: Fix shortcuts and detection of executable when shortcut has a command line argument
- SUPERMODEL: Fix Sinden border appearing behind the bezel
- SWITCH (Yuzu, Suyu, Sudachi): Fix controller applet feature
- TEKNOPARROT: Fix gamepath search for games without executables
- VPINBALL: Fix location of zip ROMs (VPinMame) when using subfolders for tables
- XENIA: Fix VSync option
- Gameboy & Gameboy Color: Fix autodetection of model based on system
- Fix Genesis-like controllers setting for 8BitDo M30 controller to make it work in both DPad and axis mode
- Fix Dolphin hotkeys when using “force SDL” option
- Fix Switch Pro controller in MESEN and MEDNAFEN
- Fix Xbox Series X controller mapping on BigPemu and Lime3DS
- Fix shaders not appearing in some cases in RetroArch (GBA and NDS)

### Features:
- DEMUL: Add hotkey to switch to fullscreen (Hotkey + L1) and hotkey for savestate
- DOLPHIN: Added pad layout options to Wii system when using GameCube controller emulation
- DOLPHIN: Add “store XFB copies to texture only” setting
- FUTURE PINBALL: Add pad2key when using BAM
- HYPSEUS: Add ability to add command line arguments with a .commands file
- MAME Standalone: Add feature to invert player 1 and 2 (might fix some arcade setups in XInput)
- MAME Standalone: Add better management of existing .ini file (including MESS autolaunch in .ini if ini is found)
- MELONDS Standalone: Add hotkeys
- MODEL2: Add management of multi-gun with automation of Demulshooter
- MUPEN64 and SIMPLE64: Add possibility to override gamepad name in config file
- NAMCO 2×6: Add .m3u extension (to manage arcade games that don’t use .zip)
- PC Engine: Added feature to control audio volumes from RetroBat (Mednafen standalone and libretro Mednafen)
- PCSX2: Add emulation speed feature
- PCSX2: Fix widescreen and no-interlace patches options with newer PCSX2 versions + add option to show emulator GUI
- PPSSPP: Add language feature
- PROJECT64: Add features and controller configuration
- REDREAM: Add alpha-sorting option
- RETROARCH: Add option to choose mouse index for guns
- RPCS3: Added option to run games from m3u file specifying GAMEID
- RPCS3: Add option to show or hide GUI
- RPCS3: Add .lnk extension
- SCUMMVM Standalone: Add better detection of games through –auto-detect command line when .scummvm file is not found or empty
- SNES9X: Add shortcuts and rewind feature
- TEKNOPARROT: Finally implemented controller & guns autoconfiguration (please test!)
- TEKNOPARROT: Add automation of Sinden border with Reshade (the YML database file needs to be community-filled!)
- TEKNOPARROT: Add Demulshooter with outputs option
- XENIA: Add feature to not break on unimplemented instructions
- Add option to force gamepad index for Model2, MAME standalone & ZINC

### Other Stuff:
- Add Demulshooter and Mamehooker management for guns for a few emulators
- Refactored way of managing wheels for Flycast, PCSX2, Model2, and Model3: users can now map their wheel through a YML file
- Renamed folder and system boom3 to Doom3
- Remove Citra-canary and Yuzu-early-access
- Add generator for WinArcadia (not yet added as available emulator)
- Added groups for many systems: Windows, NES, GB, GBA, SNES, Megadrive, WSwan, PCEngine, NeoGeo, NeoGeo Pocket, N64, Jaguar, Apple2
- Add ability to set RetroBat to work without the new shader effects in the interface (with OpenGL 2.1 compatibility)
- Bump SDL version to 2.30.9
- Remove Xenia Manager from download store and add it as an emulator option
- Test a lot of controllers and validate they are working in most emulators (see spreadsheet)
</details>

## RetroBat 6.4
<details>

### Emulators/cores/systems:
    Lime3DS : move to new version with new .exe name
    Add libretro-SNES9X2005 for compatibility with older rom hacks
    Add JGenesis for sega32x
    Update Bizhawk and add 3ds core
    Update OpenMSX
    Add CGenius (Commander Keen port)
    Add bsnes-jg core
    Add Ship of Harkidian (Zelda Ocarina of Time port)
    Add Vircon32
    Add RAZE

### Fixes:
    Fixed some missing bezels in new “DEFAULT” bezel sets
    Libretro: stop generating a core input remap file when disable controller autoconfig is enabled
    Lime3DS and Citra : fixed error when bezels are set to none
    Tattoos : fixed wrong bezels when bezel file is not 96dpi and tattoos are activated
    Fixed global disable controller autoconfigure feature not working
    Fix some libretro n64 options
    Fix a potential null call in citra generator
    Fix issue with controller autoconfiguration in BigPemu
    Try to map exit combo to Future Pinball (to test if this solves issue some are having to exit)
    Change exit message to Cemu (to test if this solves issue some or having to exit)
    Remove .m3u extension for 3do
    OpenBor : fixes running .exe (when games do not have separate .pak files)
    Fix exit of bigpemu, ares, bizhawk and jgenesis to ensure saves are made (replace kill process with proper closing)

### Features:
    Future Pinball : mapped exit to R3 (right stick press), can be used if select+start does not work
    PCSX2: add decompression of zip & 7z
    N64 : add a controller configuration profile that puts A & B according to xbox layout
    Xenia Canary : add the resolution option (same as xenia)
    Switch emulators & Cemu : add deadzone feature
    Tattoos : added activation per system
    MAME64 : add keyboard focus feature
    Windows : added .gameexe ability also for .url (e.g. Steam games)
    Add savestates to OpenMSX
    Add simple .m3u compatibility to SSF (saturn)
    Allow .bin extension for lr-melondsds to run dsi games
    Add rewind option to lr-mame
    Steam : add more solid / alternative way to find game executable to wait for (also for non-Steam games added through Steam)
    Steam : RetroBat will automatically add -silent to shortcuts to prevent Steam to pop in front of game
    Add use_gun option to cxbx/chihiro, this can be used to make the sinden bezel appear
    Add savesstate manager to BigPemu (does not automatically load the save, but sets to the correct slot to load with hotkey)
    Add SaveState Manager & hotkeys to Bizhawk
    Add SaveState Manager & hotkeys to Flycast
    Add SaveState Manager & hotkeys to JGenesis
    Copy saves of ports to retrobat\saves (cgenius, sonic engines for now)
    SNES9X : add gun options
    model2 : add option to use shoulders to brake and accelerate instead of L2 and R2
    Add feature for retroarch to select where to put patches for softmodding (near rom, in patch folder, in folder with rom name, or disable autoloading)
    RPCS3 : add possibility to use variables at the beginning of the line in .m3u files (SAVESPATH, EMULATORPATH, ROMPATH), they will be replaced by the relevant path
    mesen : add option to disable/enable softpatching autoload
    RETROARCH : add option to set fast forward shortcut as “toggle” and to define speed

### Other stuff
    add newtonSoftJson to better manage json files
    add a 3-position switch and a slider preset for options
    N64-style controllers – will now detect automatically the controllers known based on the json file only for specific guid, a switch must be activated for controllers sharing guid with non-N64-style controllers
    Tattoos correct scaling in most cases
    Add tattoos for atari lynx & neogeo pocket
    Fix update not working (for next update)
    Additional fbneo standalone control autoconfig
    For megadrive & saturn: automapping of controllers from a file for genesis-like/saturn-like controllers (so far only 8BitDo M30 in bluetooth is added to the file)
    Update Spain translation
</details>
