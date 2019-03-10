GrayFace MM8 Patch v2.1
By Sergey Rozhenko <mailto:sergroj@mail.ru>
https://grayface.github.io/

Mok's patch is included.
Save files are, of course, fully compatible with the unpatched game in both directions.

([+] - feature, [-] - fixed bug, [*] - other)

New in version 2.2:
  << Fixes in maps >>
[-] Castle of Air (d27) - 100k experience was given upon exiting the Plane of Air after getting the Heart of Air, so using Town Portal could lead to it getting skipping.
[-] Castle of Fire (d29) - same as above.
[-] Alvar (out03) - upon entering the Ogre Raiding Fort the party was facing in a wrong direction.
[-] Dagger Wound Islands (out01) - upon entering the Uplifted Library the party was facing in a wrong direction.

New in version 2.1:
  << MM6 - MM8 >>
[+] High resolution rendering in Hardware 3D in 32 bit color mode. 32 bit color is supported in windowed and borderless modes. Can be turned off by adding "SupportTrueColor=0" to INI. You can specify RenderMaxWidth and RenderMaxHeight options to limit maximum rendering resolution if you experience problems with FPS. Hidden options ScalingParam1 (3 by default) and ScalingParam2 (0.2 by default) control crispness of UI scaling.
[+] BorderlessFullscreen option makes the game run in your standard resolution, stretched to full screen (with black borders when needed). Set it to 0 to disable.
[+] WindowWidth and WindowHeight options control window size in windowed mode. Value of -1 means calculate automatically based on aspect ratio.
[+] Movies are smoothly stretched to any window size. To turn off in old full screen mode, add "SmoothMovieScaling=0" to INI, for windowed mode add "CompatibleMovieRender=0" (not recommended!).
[+] Custom SND and VID archives that work just like custom LOD archives.
[+] TurnBasedSpeed (for monsters' turn) and TurnBasedPartySpeed (for party turn) can help you speed up the combat.
[+] When switching from mouse look to 'standard mode' the mouse would start at screen center if over 10 seconds have passed since last switch. Otherwise it will return to its last position. Number of seconds is controlled by hidden MouseLookRememberTime option.
[+] While right mouse button is pressed the mouse look is now deactivated, letting you easily check active spells, current time or perform an action by pressing left mouse button while still holding the right button. Set MouseLookWhileRightClick=1 to keep mouse look active.
[+] PlayMP3 option now supports WAV files in Music folder. WAVs always loop properly.
[+] Another approach to fixing chests: now chest contents are reordered to make most valuable items be put into the chest first. This can be disabled by setting FixChestsByReorder=0.
[+] Black potion isn't wasted if it has no effect.
[+] Infinite view distance in dungeons (monsters don't disappear when they are too far).
[+] FixInfiniteScrolls hidden option controls corresponding fix.
[-] Fixed problems with timers: timer countdown was reset if you visited the location before the timer period passes; in MM6, upon revisiting the map late into in the game, wells could be used a huge number of times; in MM8 timers not related to refill were working differently than in other games. Add "FixTimers=0" to INI to disable the fix.
[-] My bug: *.evt and *.str weren't loaded correctly from DataFiles.
[-] Monsters are unlikely to jump from a bridge into lava now. Hidden "MonsterJumpDownLimit" controls the height from which they won't jump (500 by default).
[-] Jumping height reduced a bit, because the party started jumping too high after movement rounding fix. Also, "FixMovement=0" hidden option added that returns vanilla movement.
[-] Dragons and some spells couldn't target rats.
[-] Crash with sprites with scale too small (happens with MM6HD).
[-] Town Portal wasting player's turn even if you cancel the dialog.
[-] EVT commands couldn't operate on some skills.
[-] Crash on exit.
[*] Some options made 'hidden' to reduce INI clutter.
  << MM7, MM8 >>
[+] Mipmapping in D3D, controlled by "MipmapsCount" option. Value of 3 is optimal. Bigger values lead to less flickering at distance, but reduce resolution too much. Set to 1 to disable, as it was in original game. Set to -1 to generate a lot of mipmaps.
[-] There was a small semi-transparent black contour around sprites and sea shore in Hardware 3D mode.
[-] Broken but unidentified items were green instead of red if you go to a shop to repair them.
[-] Casting Telepathy spell or stealing from a monster used to prevent you from finding random items in its corpse.
[-] Light gray blinking in full screen on some computers.
[-] Arcomage crashing, hanging.
[-] Loading game while in movement phase of turn based mode leading to inability to cast spells.
[-] Monsters summoned by other monsters had wrong monster as their ally.
[-] The game was using "asynchronous" mouse handling incompatible with mouse look of the patch if "D3D Device" = 1 in the registry. Hidden "DisableAsyncMouse" patch option controls this.
[-] items.txt: now special items accept standard English "of ..." strings. This should fix them missing their attributes in some localizations.
[-] Shops were unable to fix some artifacts.
[-] Lava was hurting players in air.
[-] Memory leak in mipmaps generation code.
[*] ReputationNumber option now shows positive values for good reputation. It showed negative values before, just like it's represented internally in the game.
  << MM8 >>
[-] Sky bitmap getting reset each time the game is loaded. To turn off the fix, add FixSkyBitmap=0 line to mm8.ini.
[-] Flute was making Heal sound.
[-] Opening spell book and pressing "Quick Spell" key used to set quick spell to -1, causing a crash when you enter character screen.
[-] My semi-bug: roster.txt and pcnames.txt weren't loaded from DataFiles.
[-] Monsters couldn't cast Paralyze spell, but were wasting their turn.
[-] My bug: Since some version of my patch movies were immediately cancelled when shown by a dialog option click, as in original MM8.
[-] My bug: ProgressiveDaggerTrippleDamage fix didn't work in MM8.
[-] Unicorn King was appearing before obelisks are taken and respawning. Add FixObelisks=0 to INI to disable the fix.
  << Fixes in maps >>
[-] Smuggler's Cove, Dragon Hunter's Camp, Dragon Cave, Necromancers' Guild, Temple of the Sun (d07, d16, d17, d19, d22): Making guards mad, saving and then reloading was making them peaceful again, until you exit the map once.
[-] Smuggler's Cove (d07): Wererats were aggressive after you deliver the Blackmail letter and reenter.
[-] Trash Heap required Repair skill instead of Perception to loot safely. Some kinds of "Trash Heap" outputting "Poisoned!" and "Nothing Here" instead of "Diseased!".
[-] Dagger Wound Island, Ravenshore, Alvar, Ironsand Desert, Shadowspire (out01, out02, out03, out04, out06): Some trees/flowers/rocks with secrets required Repair skill instead of Perception to loot successfully.
[-] Ravenshore (out02): Pirates invasion was happening right away if you return from Regna to Ravenshore before sinking the fleet, now it happens if 2 months pass, as it was supposed to. Now you don't have to take all items from the Vault of Time at once as it doesn't disappear anymore.
[-] Plane of Earth, Abandoned Pirate Keep (eleme, d32): Duplicate chest.
[-] Church of Eep (d46): front side of the chest didn't react to mouse.

Other Changes:
[+] Multiple Quick Saves. (see below for details)
[+] F2 toggles Double Speed mode. DoubleSpeedKey option controls the key.
[+] PlayMP3 option lets you play MP3 files instead of CDAudio. Default is 0 (disabled). (see below for details)
[+] MusicLoopsCount option controls loops count of music. Set it to 0 for infinite loop.
[+] Mouse look. (see below for details)
[+] ToggleCharacterScreenKey opens or closes character screen. The default key is '~'. Set it to 0 to disable.
[+] InventoryKey option lets you open character's inventory screen by pressing 'I' instead of clicking a character portrait. Set it to 0 to disable.
[+] AutorunKey (F3 by default) turns on/off autorun, like in MMORPGs.
[+] TurnSpeedNormal and TurnSpeedDouble options control speed of smooth turning. Default is 100% for normal speed and 120% for double speed. Turn Delta is set to Smooth by default.
[+] MouseWheelFly option lets you fly up and down by scrolling your wheel.
[+] AlwaysStrafe option inverts the behavior of right/left arrows - strafing becomes the standard behavior and turning is done when Ctrl is pressed. Strafing is always on while in mouse look mode, unless you set NormalStrafe=1.
[+] AutorunKey (F3 by default) turns on/off autorun, like in MMORPGs.
[+] InventoryKey option lets you open character's inventory screen by pressing 'I' instead of clicking a character portrait. Set it to 0 to disable.
[+] ToggleCharacterScreenKey opens or closes character screen. The default key is '~'. Set it to 0 to disable.
[+] FreeTabInInventory lets you select dead characters by Tab key while in character screen. Default is 1 (enabled).
[+] Recovery Time value is displayed in Attack and Shoot descriptions.
[+] NoDeathMovie option makes your death quicker by disabling the movie. Default is 0 (disabled).
[+] NoCD option. Works only if "Anims\Magicdod.vid" is present. Default is 1 (enabled).
[+] NoIntro option disables starting movies. Default is 0 (disabled).
[+] HardenArtifacts options lets you use Harden Item on artifacts. Default is 1 (enabled).
[+] Harden Item, Recharge Item and other similar potions don't disappear when you try to use them on improper items.
[+] NoVideoDelays disables delays before and after a video is shown. Default is 1 (enabled).
[+] ReputationNumber shows numerical reputation value together with category name. Default is 1 (enabled).
[+] MouseLookBorder option lets you can change size of area used to rotate by pressing right mouse button. Set it to -1 to return MM6 and MM7 behavior with right button pausing the game.
[+] PaletteSMul and PaletteVMul options let you change how bright or colorful the game looks. HSV representation of colors is used.
[+] Now monsters are colored properly in Direct3D, no more tinting. d3dsprite.hwl isn't used anymore.
[+] Monster contours are taken into account in Direct3D when you click on them.
[+] "NoBitmapsHwl" enables textures to be taken from bitmaps.lod instead of d3dbitmap.hwl in Direct3D. This leads to better quality of textures, but too much sharpness in the distance. Default is 1 (enabled).
[+] HDWTRCount and HDWTRDelay options control number of water frames (up to 15) and delay between them in D3D.
[+] Smoother D3D water frames included.
[+] HorsemanSpeakTime and BoatmanSpeakTime options control time needed for horseman or boatman to say "Let's go" before new map starts loading.
[+] You can rest on shipyards.
[+] When run in 32 bits color mode automatically switches to 16 bits in Windowed mode.
[+] Identify Monster shows monster resistances numbers now.
[+] StartupCopyrightDelay option lets you change the time for which the copyright window is shown when the game starts.
[+] Custom LODs (for mods). For example, Data\*.icons.lod archives would be loaded after icons.lod, possibly replacing its content. Same with every other archive.
[+] Extracted files from EnglishT.lod are loaded from DataFiles folder. Useful for modders. (see below for details)
[+] Loads all .dll files from ExeMods directory (this is used by MMExtension and you can use it to add your patch).
[+] Improved errors reporting. (see below)
[+] Door state switching command extended. Now modders can pass 3 instead of 2 to switch door state even if it's moving.
[-] There were glitches of smack animation in houses and even crashes sometimes.
[-] Events were executed incorrectly if all party members are inactive.
[-] You could attack with inactive party members. Setting FixInactivePlayersActing=0 would disable this fix.
[-] Now save/load slot is preserved.
[-] No need to set compatibility on Win XP anymore.
[-] Inactive characters could use scrolls.
[-] Items bonuses to weapon skills were ignored in recovery time calculation.
[-] Protection from Magic didn't protect from Poison.
[-] 'of Feather Falling' enchantment didn't work (and Archangel Wings too).
[-] Dagger in second hand used to do triple damage even on Expert level.
[-] Daggers had 10% chance to do triple damage no matter what Dagger skill you have. ProgressiveDaggerTrippleDamage option makes daggers do triple damage with probability equal to skill. Default is 1 (enabled).
[-] Haste didn't work when some members are dead and weak at the same time.
[-] Buggy autosave/quicksave filenames localization removed.
[-] Temporary resistance bonuses didn't work. (they are actually never given in the game, but this fix may be useful for mods)
[-] Added code to suppress a strange bug leading to crash in the Temple Of The Sun.
[-] Mok's delay before showing video is replaced with a better solution.
[-] There were wrong artifacts bonus damage ranges (4-9 instead of 4-10 and so on).
[-] Elderaxe had wrong damage type: Fire instead of Water.
[-] Herald's Boots swiftness didn't work.
[-] Now items that didn't fit into a chest appear in it when you free space for them and reopen the chest. (FixChests option)
[-] DirectDraw errors reporting is disabled.
[-] Attacking big monsters in melee in Direct3D was a problem before. Players tended to shoot in them.
[-] Credits speed is now limited.
[-] Party generation screen animation speed is now limited.
[-] Uncompressed sounds weren't loaded correctly.
[-] 'Invalid ID reached!' that was spamming the ErrorLog.txt is now ignored.
[-] In Plane of Air FPS was very low and ErrorLog.txt was spammed with 'Too many stationary lights!' messages.
[-] Fixed a couple of index-out-of-bounds errors.
[-] Death on arena no longer causes a crash.
[-] Autosave was done after the cost of transport is withdrawn.
[-] Waiting (using Rest dialog) used to recover characters twise as fast.
[-] Key strokes could potentially be ignored if some other programs run at the same time and use the same keyboard access method.
[-] Town Portal and Lloyd Beacon dialogs used to react spell book click in mouse look mode.
[-] A rare case of "negative/0" caused a crash in stats screen.
[-] Lloyd Beacon used to autosave game after decreasing spell points and adding recovery delay.
[-] Town Portal used to autosave game after adding recovery delay.
[-] Some players experienced a beam of Prismatic Light that doesn't disappear. Now the real cause is fixed.
[-] Movement rounding issues fixed properly. Walking and strafes weren't precise because of these issues and jump height was lower than it should be. JumpSpeed option has been removed.
[-] Save game failure on some computers. Actually caused by a bug of some system software, not the game itself.
[-] Games.lod archive required very special sorting.

Changes of Mok's patch:
- no need to use compatibility modes anymore (Windows 2K/XP)
- better sound & video support (more recent Bink, Smacker and Miles Sound System libraries)
- added small delay before displaying bink movies (on fast machines it was too easy to skip a movie just by pressing mouse button)
- removed buggy hard drive free space check.
- fixed rare crash after playing Arcomage duel (on fast machines sound buffers were released before MSS finished playing them)
- fixed Hour of Power spell (Haste part wasn�t working). Thanks to Mike Kienenberger for the fix.
- fixed Psychic Shock spell (damage 12 + 1-12 instead of 12 + 1).
- you can toggle running mode by pressing caps lock key.

All options are controlled by mm8.ini. It is created when the game is run the first time.
Some localization options are kept in mm8lang.ini. You can change them or translate to your language. If you create the same options in mm8.ini they will override those from mm8lang.ini.

--------------------------------------------------------------------------------
Quick Saves:
Press F11 to use quick save. You will see "Game saved!" message. "QuickSavesKey" option in mm8.ini controls the key used to save the game.
"QuickSavesCount" option controls the number of quick saves.
"QuickSavesName" option controls names of quick saves. Default is "Quicksave".
"SpaceBeforeQuicksaveDigit" controls whether there should be a space between "Quicksave" and the number of quick save.
"QuickLoadKey" option controls the quick load key.

--------------------------------------------------------------------------------
How to use MP3 Music:
Create "Music" folder in the game directory and place there files from "2.mp3" to "16.mp3" corresponding to CD tracks. Set "PlayMP3" to 1. Unlike CD music, MP3 music volume is affected by Sound volume you set in Settings menu, so it's a good idea to keep it at maximum.

--------------------------------------------------------------------------------
DataFiles:
Create "DataFiles" folder in the game directory. To modify a file in EnglishT.lod extract it and place into the "DataFiles" folder. It will be used by the game instead of original file. So, you don't need to insert files into EnglishT.lod each time you modify them.
"DataFiles" option controls this. Default is 1 (enabled).

--------------------------------------------------------------------------------
Mouse Look

To enable mouse look set MouseLook option to 1.
Mouse look can work in two modes. The default mode is like in 3D actions and alternative mode is closer to World of Warcraft and similar games.
Here is my preset for 3D action mode: http://sites.google.com/site/sergroj/mm/MM6MouseLook.rar

You can activate alternative mode by setting MouseLookUseAltMode option to 1 or by pressing Caps Lock if the CapsLockToggleMouseLook option is set to 1.
MouseLookChangeKey is used to switch mode (turn off mouse look in normal mode or turn it on in activate mode). The mode is restored if you open any other screen.
MouseLookTempKey changes mode while you hold it. Best fit for alternative (WoW) mode.
MouseSensitivityX and MouseSensitivityY control mouse sensitivity. If you want, you can invert Y axis by making its sensitivity negative. Note that you can set values over 100.
MouseSensitivityAltModeX and MouseSensitivityAltModeY are similar, but used for alternative mode.
MouseLookFly option lets you fly up/down by pointing your view in the desired direction.
MouseWheelFly option lets you fly up and down by scrolling your wheel. This is particularly useful for take off in mouse look mode.

Cursor used in mouse look mode is located in Data\MouseLookCursor.bmp

--------------------------------------------------------------------------------
Wide Screens
This isn't related to the patch, but note that on wide screens you can set up your video card properties not to stretch the image. At least Nvidia drivers allow setting this in Nvidia control panel.

--------------------------------------------------------------------------------
Video in Hardware Accelerated Mode
If the videos aren't playing in hardware accelerated mode, try the following:
Press Win+R, type Regedit, locate the following key in it:
HKEY_LOCAL_MACHNE/Software/New World Computing/Might and Magic Day of the Destroyer/1.0 
Or on 64-bit versions of Windows:
HKEY_LOCAL_MACHNE/Wow6432Node/New World Computing/Might and Magic Day of the Destroyer/1.0 
Set 2dacceloff to 1.

--------------------------------------------------------------------------------
Errors Reporting
If an error occurs, send me a report, describing how and when it happened. Attach a savegame if possible. In case of a crash attach ErrorLog.txt file which which would be created in the game directory.