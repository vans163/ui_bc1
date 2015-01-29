Enhanced User Interface DLC Version 1.25c (January 27th 2015)

--------
OVERVIEW
--------

1.	make the game more convenient to use: fewer clicks, more icons, information organized more efficiently
2.	make it easier to understand the interactions of game objects: more mouseover actions and tooltips, use game XML data - not hardcoded blurbs
3.	no changes to gameplay, no effect on game saves, can earn achievements, works in multiplayer, and no additional information that is not already available somewhere

-------------------
CHANGES VS ORIGINAL
-------------------

(January 28th, 2013)
Gift Unit to city-state from leaderpanel, appears while having Arsonal of Democracy. (custom gift icon needed)

Purchase landsknecht from banner, second click selects the landsknecht in the city, so doubleclick for best effect. (A single click ATM cannot happen because city:PurchaseUnit(..) returns before the unit is purchased and offers no callback, *shame firaxis hire better devs*, so calling selectUnit right after fails, hence the need to doubleclick. Custom landsknecht icon needed)

Removed "Are you sure?" popup for gifting a unit, and building over an improvement.
Removed recommended worker suggestions. (useless because often the game will recommend building a road when your standing on an unimproved luxury, and if you misclick you will waste a turn)

Ignore all trade requests from AI. 50% complete (Cannot figure out how to prevent the leaderscreen for poping up for a split second). AI often requests to trade with you when you can see what they have anyways. Significantly slowing down turn times.

Show tradeable Luxuries/Strategics even with only 1 copy for yourself.

----------------------
INSTRUCTIONS FOR LINUX
----------------------

1.Basically copy the ui_bc1 folder into your civ5 assets/dlc folder. 


cd ~/.steam/steam/SteamApps/common/Sid\ Meier\'s\ Civilization\ V/steamassets/assets/dlc/
git clone https://github.com/vans163/ui_bc1.git


EXTRA:
Dont forget to check permissions on the files. Everything should be readable by the owning user of the steam folder.

chown steamuser:steamuser ui_bc1
chown -R steamuser:steamuser ui_bc1
chmod -R 755 ui_bc1

restart steam + civ5 completely.

------------
INSTRUCTIONS
------------

http://www.youtube.com/watch?v=Ud_wH4Q8W9I
1.	make sure your game is up to date at version 1.0.3.144 or later (EUI DLC is incompatible with older game versions)
2.	exit the game (make sure Civ V is NOT running)
3.	download the file from http://forums.civfanatics.com/downloads.php?do=file&id=21929
4.	open the game's DLC folder:
	- on a PC usually it's C:\Steam\SteamApps\common\sid meier's civilization v\assets\DLC (replace C: by whatever drive and/or directory where Steam is installed)
	- on a MAC (thanks AlanH) it's in the Civ5 application package at Civilization V.app/Contents/Home/assets/DLC
		You have to right click the app icon and select Show package contents. The application package location is EITHER:
		in case of MAC Steam installation: /Users/<user_name>/Library/Application Support/Steam/SteamApps/common/Sid Meier's Civilization V/Civilization V.app
		OR
		in case of MAC AppStore installation: /Applications/Civilization V Campaign Edition.app
5.	remove any previous version of EUI DLC (delete the entire UI_bc1 folder if one already exists, don't just overwrite)
6.	extract from the downloaded zip and copy the UI_bc1 folder to the game's DLC folder. ONLY if your OS is Linux, all of these files / folders must be renamed to lower case equivalent ( find ui_bc1 -depth -exec rename 's/(.*)\/([^\/]*)/$1\/\L$2/' {} \; )
7.	EUI DLC is modular: if there are things you don't like or need or which conflict with mods you want to use (check the known "mods compatibility" list at http://forums.civfanatics.com/showthread.php?p=12847246), you can disable that part by removing the corresponding subfolder from the UI_bc1 folder. Check the feature list below to determine which module includes which feature to be disabled. Please note that EUI DLC will break if its Art* or Core folder are removed.
8.	in the game menu - options - interface options - UNcheck "single player score list" if you want to use the civilization ribbon and bundled notifications
9.	in the game menu - options - game options - set the desired delays (or no delay) for the map plot mouse over help / tooltips to appear using the big horizontal sliders (there are now 2 delays - basic and detailed plot help)
10.	in the game menu - options - game options - check if the "No Basic Tooltip Help" option matches the level of mouse over info desired (this has more effects than before)
11.	in the game menu - options - game options - check whether you want a clock displayed on the top panel
12.	silent install: althought this is a DLC, it will not appear in the game's DLC menu, because it does not have a Firaxis Key. This package is a DLC because I could not get things to work as I wanted as a mod (legal screens, map highlights), and it works in multiplayer and you can still earn achievements... The main drawback is that EUI's folder needs to be moved manually in/out of the game's DLC folder to enable/disable
13.	please report bugs or suggest improvements at http://forums.civfanatics.com/showthread.php?p=12847246

------------------
GAME COMPATIBILITY
------------------

Compatible ONLY with game version 1.0.3.144 or later
No effect on saved game load
No effect on game saves
Can still earn achievements
Works with Brave New World
Works in multiplayer (any number of players can have or not have)
Should work with Gods and Kings and Vanilla, but there may be a few odd kinks
Works on Windows, Linux, and MAC (there are install procedure differences)
Compatibility with tablet / touchscreen / windows 8/8.1: unknown, expect problems
Localization: EUI DLC relies almost entirely on Civ5 built-in text, using your selected language. Some of the unit & building tags have no built-in text, however, and would need to be translated. However, I don't know how to make DLC without Firaxis key manage new localized text, so this may never get done.

------------------
MODS COMPATIBILITY
------------------

Should work fine with mods which do not change game UI files.

Would actually be very convenient with mods that change gameplay, since mouse over tooltips now provide actual XML info as updated by mods (not harcoded blurbs).

EUI DLC is modular: in case of incompatibility, try disabling conflicting EUI DLC component by removing the corresponding subfolder from EUI DLC's UI_bc1 folder (please note that EUI DLC will break if its Art* or Core folder are removed).

Please check compatibility for some other mods at http://forums.civfanatics.com/showthread.php?p=12847246

If you have tested mods with EUI, please share your experience I will update the list when I get the time.

-------------------
IN CASE OF PROBLEMS
-------------------

1.	Please read the instructions carefully
2.	Make sure your game is up to date (EUI DLC is compatible ONLY with game version 1.0.3.144 or later)
3.	Make sure your EUI DLC version is up to date: download latest version from http://forums.civfanatics.com/downloads.php?do=file&id=21929
4.	Make sure any previous EUI DLC version has been deleted before installing a new version !
5.	Make sure the UI_bc1 folder has been installed in the correct game folder (see instructions)
6.	If you are using mods, try disabling mods to check for conflicts. Some early mods were folders starting with "z" that were put in the game's ...\assets\UI folder, those are not detected by the game's install or integrity check, you have to manually look for them.
7.	In case of conflicts, try disabling conflicting EUI DLC components by removing the corresponding subfolder from the UI_bc1 folder (please note that EUI DLC will break if its Art* or Core folder are removed)
8.	If problem persists, please report bugs at http://forums.civfanatics.com/showthread.php?t=512263

How to report a bug

1.	Report bugs at http://forums.civfanatics.com/showthread.php?t=512263
2.	What game version do you have?
3.	What expansions and DLC do you have?
4.	Do you play on PC or Mac? 
5.	Describe the problem 
6.	Attach a screenshot and/or a save game if you think it might help
7.	To attach a file to your post: click "go advanced", then click "manage attachments"
8.	If the problem is caused by a mod, what's the mod's name, version, and where did you get it (url)
9.	Post your lua.log error messages (or better yet, the entire lua.log), either as an attachment (compressed to zip or renamed to lua.txt) or within a spoiler markup
10.	The lua.log file is usually in ...\Documents\My Games\Sid Meier's Civilization 5\Logs. If it's missing or almost empty, you need to enable logging for debugging
11.	Non-trivial problem reports without lua.log will get no response

How to enable logging for debugging

1.	Close civilization V
2.	Open config.ini with a simple text editor such as notepad (usually in ...\Documents\My Games\Sid Meier's Civilization 5)
3.	Search for the line "LoggingEnabled = 0" and replace it with "LoggingEnabled = 1"
4.	Do the same with "EnableLuaDebugLibrary = 0": set it to 1. If this line does not exist, add it before LoggingEnabled
5.	Save config.ini and close 
6.	Start civilization V and reproduce the problem

--------
FEATURES
--------

FrontEnd: no more legal screen nuisances at game launch (by Temudjin)
GameSetup: supports unlimited UU/UB/UI (mods such as 3rd Unique Component Project at http://forums.civfanatics.com/showthread.php?t=504425)
GameSetup: can right click on stuff to access pedia (pre-game)
ToolTips: when setting up a game, there are mouse over tooltips for unique civilization units and buildings - when you need them most
ToolTips: in-game mouse over tooltips for units and buildings provide more info, all based on game XML data (reflecting changes made by mods)
ToolTips: show the current active Pantheon/Religion beliefs & effects when mousing over the city banner Faith icon
NotificationPanel: diplo corner artwork by Zyxpsilon
NotificationPanel: if and only if game menu - options - interface options - "single player score list" ("multiplayer score list" when playing multiplayer) is UNchecked:
1.	a vertical ribbon shows known civilizations and city states with mouse over tooltips, right click and left click actions
		- Civilizations are sorted by score. Their icon frame color shows the way they feel about you (friendly, neutral, guarded, denouncing, hostile). Small icons around the leader portrait indicate war, friendship (flower), open borders < >, research agreement, defense pact, and active player. To the right are their score and either total gold or gold per turn, depending on what you can trade with them. Icons shows available duplicate luxury resources they are willing to trade (theirs above & yours below), so you don't have to visit each leader to see if they have anything for trade (mouse over tooltips provides more details)
		- City states are sorted by influence, then by distance to capital. Each icon shows city state type and status relative to you (allied, friends, afraid, angry, neutral). Mouse over the icons shows detailed tooltips. To the right are ally flag and icons for quests in progress (clicking on quest icons will jump to encampment if relevant), also with mouse over tooltips.
		- civilization ribbon is available within leader screens
		  can get diplomatic info about everyone while talking to a leader using civilization ribbon mouse over tooltips
		  can switch talking from one leader to another directly from within the leader screen by clicking on civilization ribbon icon, or return to the game by clicking on either your own icon or the one of the currently displayed leader (this function is disabled when your turn is not active, i.e. during other civilization's turns)
		- civilization ribbon player connection indicator: yellow = connecting, green = connected, red = host, mouse over tooltip shows ping, click to kick player (host only)
		- control-click action on civilization ribbon leader icon to declare war (BNW only)
2.	notifications are bundled by type: this means each notification icon may correspond to several notifications, and you need to left click to cycle through bundled notifications to see each one. Left click on a notification icon may also jump to the appropriate location on the map, this location corresponds to the next cycled notification. Right click on a notification icon dismisses all of the notifications bundled with the icon.
NotificationPanel: display notifications for player's city population growth beyond 5 and for player's city border growth
NotificationPanel: when city acquires new tiles, resource is shown in border expansion notification
NotificationPanel: shrink size of the large top right buttons (culture, tourism, diplo, espionage...) they're pretty but waste space
NotificationPanel: align the large turn blocking notifications horizontally to save space (they have no "finger" anyways)
NotificationPanel: open religion popup immediately when creating or enhancing a religion with a great prophet
NotificationPanel: added Zyxpsilon's excellent artwork for diplo corner
TopPanel: top panel bar no longer takes up the whole screen width (only on screens more than 1900 pixels wide)
TopPanel: top panel bar now shows meters and remaining turns for tech, policies, faith purchase, great person
TopPanel: more top panel mouse over tooltips, exisiting ones give more info, such as extra resources that player and AI has, AI gold per turn, so you don't have to visit each leader to see if they have anything for trade (this info is also on the right side civilization ribbon)
TopPanel: strategic resource mouse over tooltip details how resources are used, local production, imports, exports (the numbers don't always add up, but this is a game bug)
TopPanel: happiness mouse over tooltip details how luxuries are used local production, imports, exports
TopPanel: the tech meter mouse over tooltip shows tech overflow cues
TopPanel: right click civilopedia actions
TopPanel: optional clock & alarm (click on clock to set alarm time or change clock format - note alarm time entry is in 24H format regardless)
PlotHelp: map plot mouse over tooltip indicates basic unit stats (moves, strength, ranged strengthrange)
PlotHelp: map plot mouse over tooltip indicates possible terrain improvements with their yields (and whatever yields are added by mods), technology prerequisites, possible effect of constructing buildings, adopting a social policy / tenet, or a pantheon / religion belief. These are all based on game XML data and work with mods that change these data.
PlotHelp: map plot mouse over tooltip gives more details when checking off the "No Basic Tooltip Help" option
PlotHelp: map plot mouse over tooltip details filtered according to unit currently selected (or not)
PlotHelp: map plot mouse over tooltip extended details with longer mouse over (adjusted using the interface option panel "Tooltip2Seconds" slider)
PlotHelp: map plot tooltip only under mouse over, no more duplicate clutter in the right corner above the minimap
PlotHelp: when a settler is selected, plot mouse over shows potential city max work limits (dark) and highlight overlapping plots (orange)
TechTree: tech selection will always use the tech tree, no more tech panel
TechTree: most tech bonus "star" icons are replanced by more explicit icons (e.g. trade route icon instead of star), requires less mouse over to find out what everything does
TechTree: when entering the tech tree, it automatically scrolls to (somewhat) appropriate location
TechTree: much faster loading - tooltips are evaluated only when required by mouse over
TechTree: supports "OR" tech prerequistes (mods only)
CityBanners: city banners have extra icons showing selected focus, requested luxury, love the king status, population growth lock
CityBanners: city banner growth meter turns red when city is starving, and shows turns to population decrease
CityBanners: mouse over city HP bar tooltip shows the exact numerical values
CityBanners: more city banner mouse over tooltips
CityBanners: help with micromanagement: show predicted overflow at build / growth completion, and how much is missing the turn just before
CityBanners: mouse over city banner highlights worked plots (green), unworked city plots (orange), city max work limits (dark), and plots targeted by culture (magenta)
CityBanners: city banner production button works for Venice puppets
CityBanners: puppet city banner click enters city view
CityBanners: city banner mouse over tooltip shows resources within city plots - red not hooked up, green hooked up
CityBanners: city state banners show quest icons in place of cryptic meter, clicking on them will jump to encampment if relevant
CityBanners: city state banner mouse over tooltip shows influence and resources available or granted
CityBanners: when allied, replace the city state banner icon with the flag of the ally
CityBanners: hide range strike icon when no more ennemy units are in range following a kill
CityBanners: click on spy icon -> espionage overview, click on puppet icon -> annex popup
CityView: production button automatically opens city view
CityView: city screen features new production queue mechanisms:
	items may be added directly to production queue: left click = end of queue, ctrl + left click = top of queue, shift + left click = replace entire queue, right click = pedia
	items may be purchased directly (e.g. great people), if the relevant purchase button (faith or gold) is displayed and not disabled (insufficient funds)
	production queue items may be shuffled around by dragging to appropriate location (no more clunky arrows)
	production queue may have more than 6 items (tooltip not updated), but the elevator is the only way to scroll the list (mouse scroll wheel does not work)
	current production queue item can be cleared (but next turn will not be possible until another selection has been made)
	city advisor production recommendation icons can be turned off in the game option menu
CityView: city screen shows remaining turns to great people creation
CityView: city view buttons disabling / enabling works correctly, even when switching cities while inside city view by clicking on other cities
CityView: city screen includes annex button for non-Venice puppets
CityView: city screen highlights worked plots (green), unworked plots (light blue) and plots used by your other cities (dark blue), purchasable plots (gold, only in buy plot mode)
CityView: fewer surprises with worker allocation changing automatically after leaving city screen
CityView: remove empty bottom bar and use wasted space
CityView: supports modded buildings with unlimited specialists & great works (mods only)
CityView: can edit any city name (including puppets) with a right click
CityView: much faster loading - tooltips are evaluated only when required by mouse over
CityView: automatically open city screen when founding city
CityView: buy plot mode can now be toggled (check coin in upper left corner)
CityStatePopup: when encountering city states for the first time, skip directly to the dialog screen (which allows interactions)
TradeLogic: trade screen shows missing gold for research agreement, if any (mouse over tooltip)
MiniMap: UI is compatible with custom minimap sizes (can be changed in config.ini / [MiniMap] Width & Height )
UnitPanel: shows remaining unit movement with decimals
UnitPanel: all available unit commands are shown in a single column (no more "show more actions")
UnitPanel: can edit unit name at any time with a right click
UnitPanel: unit ribbon lists player's units and status icons. When selecting a unit, units are sorted by distance to selected unit. Filter unit ribbon by unit type (several types can be selected): click on the >>> button at the bottom of the ribbon to select units to display. Your choices are saved from one session to the other. Settings are common to all hotseat players, though.
Options: add the plot help extended mouse over tooltip delay slider in the interface option panel (Tooltip2Seconds)
Options: add the "no city screen citizen warning option" which allows the city screen citizen management header to be open by default (strange name  )
Options: add a clock on / off check box (for display on top panel)
Options: add a checkbox to disable city view advisor production recommendation icons
BugFixes: fix Firaxis diplomacy bug with spinning globe mouse cursor
BugFixes: submarines are a bit more invisible than before (no more red blob in move mode)
City state status color now only blue when actually allied
More city state status info for vanilla game
and more...

---------------
VERSION HISTORY
---------------
Version 1.25c (January 27th 2015)
CityView: buy plot mode can now be toggled (check coin in upper left corner)
CityView: removed city view hex highlights in strategic mode
Core: full game info database dynamic caching for speed and to improve useability on low end PCs
Fixed some bugs
Miscellaneous improvements

Version 1.24 (November 7th 2014)
Core: partial game info database caching to improve useability on low end PCs
Fixed some bugs
Minor tweak for game version 1.0.3.276
Miscellaneous improvements

Version 1.23 (October 19th 2014)
Fixed some bugs
Significant additions to unit, building and improvement tooltips
Filter unit ribbon by unit type (several types can be selected): click on the >>> button at the bottom of the ribbon to select units to display. Your choices are saved from one session to the other. Settings are common to all hotseat players, though.
Add civilization ribbon player connection indicator: yellow = connecting, green = connected, red = host, mouse over tooltip shows ping, click to kick player (host only)
Add control-click action on civilization ribbon leader icon to declare war (BNW only)
Miscellaneous improvements

Version 1.22 (July 28th 2014)
Fixed some bugs
NotificationPanel: added Zyxpsilon's excellent artwork for diplo corner
CityBanners: when mousing over the city banner, show city max work limits
CityView: when inside city screen, show city max work limits and highlight plots used by your other cities
PlotHelp: when a settler is selected, plot mouse over shows potential city max work limits (dark) and highlight overlapping plots (orange)
UnitPanel: first version of unit ribbon, which lists player's units and status icons. When selecting a unit, units are sorted by distance to selected unit. Some mouse over actions are operational. Filtering / sort options are not yet implemented

Version 1.21 (July 2nd 2014)
Fixed some bugs
CityView: current production queue item can be cleared (but next turn will not be possible until another selection has been made)
TechTree: most tech bonus "star" icons are replanced by more explicit icons (e.g. trade route icon instead of star), requires less mouse over to find out what everything does
TechTree: much faster loading - tooltips are evaluated only when required by mouse over

Version 1.20 (full moon Friday June 13th 2014)
Fixed a regression in 1.19

Version 1.19 (full moon Friday June 13th 2014)
Fixed some bugs

Version 1.18 (June 1st, 2014)
Fixed a minor unit mouse over tooltip bug

Version 1.17 (May 29th, 2014)
Fixes bugs found in previous versions
Tech tree eras are correctly displayed with Hulfgars's mods - works only if mod's included "AttilaResourcesTooltip" (entire folder) and "TechTree.lua" (one file) are removed
Compatible with CSD v23 - only if you remove CSD's own CityView.lua, TopPanel.lua, and InfoTooltipInclude.lua from its ...\Assets\UI\... folder (EUI DLC's CityView.lua and TopPanel.lua are compatible with CSD, the reverse is not true)
Civilization mouse over tooltips show active deals and trade routes, and remaining turns for friendships & denouncements correctly scale with game speed
Civilization ribbon now available within leader screens (if enabled)
	can get diplomatic info about everyone while talking to a leader using civilization ribbon mouse over tooltips
	can switch talking from one leader to another directly from within the leader screen by clicking on civilization ribbon icon, or return to the game by clicking on either your own icon or the one of the currently displayed leader (this function is disabled when your turn is not active, i.e. during other civilization's turns)
City view advisor build recommendation icons are now disabled when corresponding game options checkbox is unchecked (checked by default)

Version 1.16 (May 13th, 2014)
Fixes minor bugs found in v1.15
Features new city queue mechanisms:
items may be added directly to production queue if not dimmed: left click = end of queue, ctrl + left click = top of queue, shift + left click = replace entire queue, right click = pedia
items may be purchased directly (e.g. great people), if the relevant purchase button (faith or gold) is displayed and not disabled (insufficient funds)
production queue items may be shuffled around by dragging (like in 1.15)
production queue may have more than 6 items, but the elevator is the only way to scroll the list (mouse scroll wheel does not work)
NotificationPanel: bundle notifications together by type when civilization ribbon is displayed, to reduce clutter on right side of screen. This means each notification icon may correspond to several notifications, and you need to left click to cycle through bundled notifications to see each one. Left click on a notification icon may also jump to the appropriate location on the map, this location corresponds to the next cycled notification. Right click on a notification icon dismisses all of the notifications bundled with the icon.
Compatibility with Communitas Expansion Pack: work around GameInfo.Yields() iterator broken by Communitas
PlotHelp: unit strength in red when decreased due to lacking strategic resource

Version 1.15 (March 7th, 2014)
Fixed some bugs (including one that broke some custom maps)
Compatibility with City-State Diplomacy Mod (CSD) v21: should work provided you remove CSD's own CityView.lua from its ...\Assets\UI\InGame\CityView folder (EUI's CityView.lua is now compatible with CSD, the reverse is not true)
Compatibility with Civ IV Diplomacy Features Mod v10: should work provided you remove CDM's TopPanel.lua from its ...\UI\InGame folder (EUI's TopPanel.lua is now compatible with CDM, the reverse is not true)

Version 1.14 (February 19th, 2014)
BugFixes: fix Firaxis diplomacy bug with spinning globe mouse cursor
NotificationPanel: open religion popup immediately when creating or enhancing a religion with a great prophet

Version 1.13 (February 17th, 2014)
Fixed some bugs (including one that broke hot seat)
Change folder structure: no more UI subfolder, components are directly in UI_bc1 folder (please note that EUI DLC will break if Art* or Base folder are removed)
CityView: added code for compatibility with CSD v19
TopPanel: happiness mouse over details how luxuries are used local production, imports, exports

Version 1.12 (February 1st, 2014)
Fixed some MP & SP bugs
Significant code optimizations
CityBanners: click on spy icon -> espionage overview, click on puppet icon -> annex popup
ToolTips: Show the current active Pantheon/Religion beliefs & effects when mousing over the city banner Faith icon
CityView: supports modded buildings with unlimited specialists & great works (mods only)
CityView: production queue items can now be dragged to appropriate location (no more clunky arrows)
NotificationPanel: when city acquires new tiles, resource is shown in border expansion notification
NotificationPanel: shrink size of the large top right buttons (culture, tourism, diplo, espionage...) they're pretty but waste space
NotificationPanel: align the large turn blocking notifications horizontally to save space (they have no "finger" anyways)
TechTree: supports "OR" tech prerequistes (mods only)
UnitPanel: removed the ugly "edit" button, but unit name can now be changed with a right click
GameSetup: supports unlimited UU/UB/UI (mods such as 3rd Unique Component Project at http://forums.civfanatics.com/showthread.php?t=504425)
GameSetup: can right click on stuff to access pedia (pre-game)

Version 1.11 (January 8th, 2013)
Fixed some annoying bugs

Version 1.10 (January 5th, 2013)
Fixed some bugs
Tweaks in response to user requests
UnitPanel: can edit unit name at any time

Version 1.9 (December 20th, 2013)
Fixed some bugs

Version 1.8 (December 14th, 2013)
Fixed some bugs
TopPanel: strategic resource mouse over provide details on how resources are used, local production, imports, exports (the numbers don't always add up, but this is a game bug)
CityBanners: hide range strike icon when no more ennemy units are in range following a kill
CityView: remove empty bottom bar and use wasted space
Change folder structure: some components are broken down further (more modularity)

Version 1.7 (November 22nd, 2013)
Fixed some bugs
Tentative fix for compatibitity issues when the G&K and/or BNW extensions are not installed
Change folder structure: all components are now located inside the UI_bc1\UI folder (used to be UI_bc1), more independent modules
Options: add a clock on / off check box
TopPanel: optional clock & alarm (click on clock to set alarm time or change clock format - note alarm time entry is in 24H format regardless)
TopPanel: right click civilopedia actions
NotificationPanel: sort the city state ribbon list by decreasing influence, then by distance to capital
CityBanners: major civ city banner mouse over shows resources within city plots - red not hooked up, green hooked up

Version 1.6 (November 13th, 2013)
Fixed some bugs
CityBanners: expand rival civilization's tooltip

Version 1.5 (November 8th, 2013)
Fixed some bugs

Version 1.4 (November 5th, 2013)
Fixed some bugs
CitieBanners: clicking on city state banner's quest icons will jump to encampment if relevant
NotificationPanel: show ally flag on city state ribbon, clicking on quest icons will jump to encampment if relevant
NotificationPanel: sort the city state ribbon list by decreasing influence
NotificationPanel: sort the civilization ribbon list by decreasing score
NotificationPanel: add open borders icons on civilization ribbon, add a player icon, change friendship icon to a flower
NotificationPanel: expanded the mouse over tooltips
PlotHelp: improved the filtering of what gets displayed, now taking into account the unit currently selected (no more info on farms and mines while making war, effect of academies etc only shown if appropriate great person is selected )
TopPanel: expanded the mouse over tooltips, and the large tech meter mouse over will now show tech overflow cues

Version 1.3 (October 30th, 2013)
Fix a bug which broke compatibility with vanilla and gods & kings
Bug: plot mouse over shows incorrect yield for building improvements which remove features (fixed in 1.4)

Version 1.2 (October 29th, 2013)
Fixed some bugs
DiploList: put the diplo list back
Options: add the plot help extra tooltip delay in the interface option panel (Tooltip2Seconds)
Options: add the "no city screen citizen warning option" which allows the city screen citizen management header to be open by default (strange name  )
ToolTips: able to decode more of the game's XML tags
CityView: automatically open city screen when founding city (Duh! amazed at the time and effort required to make this work around "features" of game unit auto cycling. Still need to open manually when founding city on very 1st turn)
CityBanners: when allied, replace the city state banner icon with the flag of the ally
CityBanners: city state banner mouseover shows influence and resources available or granted

Version 1.1 (October 21st, 2013)
Minor changes for small screens (less than 1900 wide) in city banner tooltip & top panel
Bug: incompatible with the "single player score list" option (and "multiplayer player score list" as well) - fixed in 1.2
Minor bug: in vanilla, when selecting peace / war in city state popup, it is not refreshed correctly. Workaround: close and re-open the popup. Fixed in 1.6

Version 1.0 (October 19th, 2013)
Initial public release