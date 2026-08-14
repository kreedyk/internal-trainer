# Internal Trainer — Changelog

---

## v0.9.9

### Bug Fixes
- Fixed LIT sideload crash
- Fixed config not loading melees correctly
- Fixed bow mine-dart going out of control when playing with Luis
- Fixed explosive and flame bullets not working with the bow
- Fixed Alt+Tab sometimes freezing the game
- Fixed back weapons potentially causing a black screen during loading (safeguards added)
- Fixed crash when Ashley was decapitated by a chainsaw
- Fixed crash when breaking glass with the RPG
- Fixed back weapons not installing through the mod installer
- Fixed no-aim/knife cam crashing on new game
- Fixed parry overlay and camera features not saving to config
- Fixed item overlay flashing infinitely when picking up an item
- Fixed enemy not falling when shot while kneeling
- Fixed Hunk breaking when using the knife (again)

### Removed
- Removed `arrows.nia` (old drop file)
- Removed disable music feature — replaced by volume control
- Removed code that allowed changing FPS and texture quality in-game (gray block in ESC options); restored automatically when RE4Tweaks is not present
- Removed VRAM cleaner — replaced with a better memory-cleaning implementation
- Removed AU Codes
- Removed Ashley Warning HUD Effect
- Removed Mercenaries Insta Text (Disable Text remained)
- Removed Enemy Randomizer
- Removed rainbow interface

### New Features
- Added Invisible Enemy feature
- Added Enemy Spawn hotkey
- Added 3 interface themes: classic, obsidian and crimson. Changed the default theme to obsidian
- Added Discord Rich Presence. Displays information about what you are doing in the game within Discord
- Added Death Auto Restart feature for Ashley
- Added Knife in Merchant feature, it replaces the treasure. Once activated, the Knife Animation Fix is ​​enabled automatically
- Added Mirrored World and Mirror audio. Completely experimental, may cause headaches
- Added back Ashley's CG Physics via checkbox. It still has the same issue that caused its initial removal, can randomly become distorted (requested by insidecat)
- Added compatibility with the "You Cannot Escape" mod (other mods should also work unless the executable is heavily modified)
- Added feature to survive a chainsaw attack
- Added checkbox to pause the game while switching weapons in the real-time inventory
- Added `Custom plxx` folder inside `kreed\sideload\User\` — allows editing animations used by Character Swap (requested by shin)
- Added more items to the drop system
- Added auto heal for Ashley
- Added new default animation for Ashley low melee
- Added presets to the drop system
- Added addon support for the mod installer (similar to Fluffy Manager)
- Added high melee anytime
- Added no-cam state for the explore cutscene feature
- Added mine thrower to the item manager
- Added new game custom loadout (similar to mercenaries loadout)
- Added volume control
- Added Silence Armored Ashley
- Added Ashley Audio Fix as a simple checkbox toggle (no longer requires custom files)
- Added new auto-save system inspired by modern games — select the save slot and optionally auto-save on room change
- Added support for user custom back weapons file
- Added 3 extra slots for Melee Anytime (default keys: 3, 4, 5) so original melees are not replaced
- Added smaller HUD feature
- Added HUD repositioning feature
- Added free cam with custom toggles
- Added the PRL 412 Nerf feature a way to make the PRL less overpowered by using flash grenade ammo
- Added hotkey setting to the Manual Checkpoint feature
- Added new Kill Aura feature
- Added Character, Melee and Randomizer Studio with custom renders in the UI
- Added outfits setup for character randomizer
- Added a new stage selection window with screenshots of locations instead of just names
- Added new UI for mercenaries loadout
- Added new UI for merchant price editor
- Added custom merchant unlock items
- Added a proper memory cleaner with a memory guard that warns when the game is running low on resources during long gameplay sessions

### Changes
- The trainer now works in all languages, but English is still recommended since merchant features (knife parry, durability, upgrade) rely on English text and textures
- All UI sounds redone — minimalist and optional, but worth trying
- Reduced DLL size by approximately 5 MB; most assets moved to `k_assets.pak` inside the utils folder
- Back weapon checkbox is now only available when playing as Leon with the no-jacket outfit
- Camera no longer moves when switching weapons in the real-time inventory
- Replaced the standard .cfg system with a professional implementation using toml++
- Improved auto-load configuration loading time
- Updated config section UI
- Ashley Jump Alone no longer requires custom files or HD Project
- Default bow animations changed to a toggle checkbox in the trainer menu
- Aimbot rewritten — now includes vertical adjustment; currently focused on a future fixed-camera feature but usable standalone
- Enemy ESP rewritten with several visual adjustments
- Character and melee swap no longer requires been in-game to swap (outside of menus)
- Modloader improved and simplified. Now no longer need to worry about whether the file has .lfs compression
- UIScale now saves at user config
- The Flaming Knife feature now only works with the wep16 equipped (which can be obtained from the merchant via the "Knife in Merchant" feature)
- The default key to open the menu has been changed to F2

### Default Melee Anytime Key Changes
| Action | New Key |
|---|---|
| Low Kick | F |
| High Kick | X |
| Thrust Punch | C |
| Double Kick | G |

Keys can still be changed in the Hotkeys section.

---

## v0.9.8

### Bug Fixes
- Fixed Disable Collision not working with RE4Tweaks
- Fixed Armored Ashley (Special 2) crashing on cutscenes (UI warning removed — fully fixed)
- Fixed Character Swap Ashley crashing in R209 (temporary restriction removed — fully fixed)
- Fixed crash when saving at the end of chapters while using Character Swap; the need for automatic checkpoint restart after saving has been eliminated
- Fixed game randomly crashing on startup
- Fixed Auto-Save accidentally skipping the cabin fight when a save occurred there
- Fixed Infinite Parry not working
- Fixed crash using Krauser's bow with Ashley (UI block removed — fully fixed)
- Fixed crash when loading a save with Krauser's bow equipped
- Fixed item overlay appearing during cutscenes
- Fixed Current Health slider killing the player when set to 0
- Fixed incompatibility with the new version of RE4Tweaks

### Removed
- Removed True 120FPS (emoose's new RE4Tweaks version covers this)

### New Features
- New item and weapon management system — add items, modify weapon stats, change upgrade prices, and more
- Added multi-byte paste and freeze/override to the Memory Editor
- Added Texture Element Editor (ID Inspector) — manipulate textures in real time: size, position, color, etc.
- Added Mercenaries loadout — customize starting items and weapons in mercenaries mode
- Added merchant discount system — change item prices or dynamically adjust them based on gameplay
- Added Flaming Knife at the merchant (read the in-game help marker for details)
- Added Knife Upgrade at the merchant (balance testing needed)
- Added fully configurable enemy size and speed with an anti-loop system
- Added bone manipulation — resize and reposition bones, including individual body parts
- Added Custom Drop Sideload — configure enemy drops through a UI
- Added YouTube player (experimental but stable — supports search or direct URL)
- Added FCV sideload for previewing animations; usable with Melee Anytime
- Added Custom Melee with custom FCV (high melee)
- Super Punisher reworked with a dedicated settings window
- Added Back Weapons with custom physics
- Added custom breast physics for Ada and Ashley
- Added Bow Mine-dart
- Added Melee Explosive
- Added new menu subtabs for better organization

### When RE4Tweaks Is Not Detected
- Added HD Project text resize
- Added Custom Frame Limiter
- Added Raw Mouse Input

Combined with previous additions, it is now fully possible to play with the HD Project without RE4Tweaks.

---

## v0.9.7.1

> Update focused exclusively on bug fixes — no new features.

**Important:** Memory allocation for inventory (`pzzl`), `pl.udas`, and `ss_wep` has been increased, allowing heavier models to work both in-game and in the inventory. If you experience random crashes when opening the inventory or equipping a weapon (especially after long sessions), please report it so the previous allocation can be restored if necessary.

- `pl.udas` now supports up to 10 MB
- `ss_wep` should work correctly with up to 2 MB
- Mods that previously required the Companion DLL should now work with the trainer alone (unless the mod is extremely poorly optimized)

### Bug Fixes
- Fixed Krauser Beret and Krauser Boss features not working
- Fixed Disable QTE crashing the game
- Fixed Knife Durability and Knife Parry not being repaired at the merchant
- Removed castle and island price controls from the UI — treasure pricing is no longer used; a single price now controls everything
- Fixed crash when loading a save made with a non-Leon character — Character Swap config is no longer required before loading
- Fixed animation issue when switching characters outside of Character Swap (e.g., male animations playing on Ashley's chapter when using a male character)
- Fixed mod installer issues encountered when installing the Piers mod; error messages are now clearer if a problem occurs
- Removed sideload from `wep29` (Custom TMP) — when using Hunk, the knife is now deactivated while Custom TMP is equipped (parrying also disabled); this only affects Hunk with Custom TMP, other characters are unaffected
- Gradient sideload is no longer enabled by default; it activates only when needed (via FX Freeze Enemies)
- Fixed game freezing when activating HUD color change
- Fixed Krauser Aura not applying immediately when swapping to Krauser (previously took 5+ seconds)

---

## v0.9.7

> Version 0.9.6 was skipped — changes were too significant and the pre-0.9.6 build had been in use for too long.

### Bug Fixes
- Fixed Hunk becoming completely deformed after using the knife while the TMP was equipped
  - Note: this fix causes the Hunk TMP to appear as a standard TMP without a stock. To revert, delete `kreed\sideload\Weapons\Hunk TMP Fix`
- Fixed in-game detection function causing certain features to stop working inside mercenaries
- Fixed "Show Only HP Bar" still partially displaying when the HP bar was very large
- Fixed Ashley randomly becoming deformed during cutscenes
- Fixed softlock on the first stage (R100) when Explosive Bullets were active
- Fixed crash with high-poly models introduced after MemoryCompatibility (pre-0.9.6)
- Fixed automatic checkpoint restart after saves — it was incorrectly triggering without Character Swap active
- Fixed incompatibility with mods such as Medieval Era and Wake in the Dark
- Fixed game lag after Alt+Tab for an extended period
- Fixed game forcing fullscreen (no longer necessary)
- Fixed Ashley outfit swap not working
- Fixed crash when calling hidden Ashley
- Fixed "Internal Trainer" string appearing in the first cutscene
- Fixed some features disappearing from the menu after activation
- Fixed enemies having infinite health when using the Razor Companion DLL
- Fixed rare crash when opening the menu while the game was loading
- Fixed user custom menu colors not being saved or restored
- Fixed FOV, Lit Sideload, and Brightness not saving to user config
- Fixed arrow keys moving the character vertically even with Disable Collision off
- Fixed crash when calling Save/Merchant in mercenaries
- Fixed severe race condition when both high and low melee randomizers were enabled simultaneously — the old timer-based system has been replaced with an event-driven system (pauses, inventory open/close, room changes), eliminating random melee-related crashes

### New Features
- Added `MemoryCompatibility` to main INI settings — previously a temporary workaround for mods like Medieval Era by Hevilz; the trainer now auto-detects when it's needed, making manual use rare. Enable manually only if picking up an item from the ground crashes the game
- Added `trainer_sos.ini` — bypasses automatic allocations; use only in specific incompatibility cases
- Added `EnemyExtraMemory` to main INI settings — enabled by default; useful for spawning more enemies in a scene. Automatically disabled for mods like Rising of Evil and other mods by Luis Webber
- Added Krauser Boss feature
- Added Combat Knife animation fix
- Added Knife Durability with overlay, custom sounds, and repair via merchant or timer
- Added Blood Knife — allows using a broken knife at the cost of character health per use, with increased damage
- Added overlay system to Knife Parry (removed old on-screen message system)
- Added Knife Parry repair via merchant
- Rewritten sound system to support multiple simultaneous sounds
- Added real-time inventory system inspired by the remakes — switch weapons efficiently via hotkeys or mouse without opening the inventory; old scroll-based fast-switch removed
- Added basic hotkey control via Xbox controller
- Added FastMath, ThreadFix, and VertexBuffer when RE4Tweaks is not detected — enabled by default
- Added Enemy ESP (also usable for tracking items and objects)
- Added Enemy Aimbot (experimental — no height adjustment, horizontal offset may need manual tuning; may be improved or removed)
- Added Experimental 120FPS — functional and faithfully implemented; some issues (duplicate sound, accelerated physics) may occur; the trainer restores 60FPS at specific moments automatically
- Added Custom Checkpoint — press one key to create a checkpoint anywhere
- Added EVD sideload — removes Leon's jacket in cutscenes (same behavior as Razor DLL); disabled by default. To enable, remove the underscore from `_Cutscenes` folder
- Added File Monitor — lists every file read by the game and its path (useful for modloader debugging)
- Added fast loading — removes all types of fades; focused on auto-save but usable standalone
- Added ability to create "Open" points anywhere in real time with custom coordinates (saved to a JSON file)

### Changes & Removals
- Removed Stage Randomizer — Duke's implementation is more complete; his Patreon is recommended for randomizer support. The escape point system was kept independently and is now more powerful (create "Open" anywhere, configurable via JSON, useful for modders)
- Many internal functions rewritten to use in-game functions instead of direct memory manipulation — safer and more extensible
- Game now drops to 8–14 FPS when out of focus to preserve CPU usage
- Game no longer needs to run in windowed mode and no longer forces borderless fullscreen
- `useHDTexture 1` is now always set (can be disabled in `trainer_sos`)
- Numerous UI improvements — features reorganized into multiple categories
- Camera no longer spins when closing the menu
- Area Jump UI rewritten — supports teleportation to custom coordinates, saved to JSON
- Enemy HP display fully rewritten — shows multiple enemies with extended distance options (legacy version still available)
- FPS and texture quality can now be changed in-game — the gray lock has been removed
- Hotkey system now supports real key names instead of decimal numbers
- When RE4Tweaks is detected, both DLLs now share and cooperate on shared features (e.g., enabling infinite ammo activates RE4Tweaks' debug flag instead of writing to memory)
- Melee system reworked — event-driven instead of timer-based; a queue system prevents repetitive melees (if "Reverse Kick" appears, it only reappears after all others in the queue have been used)
- Removed `re4_launcher` executable from utils folder (to avoid false positives) — replaced by a PowerShell script with the same functionality (replaces incorrect executable with 1.0.6)
- Modloader system completely redesigned — mods can now be installed without modifying files. **Note:** the modloader folder structure has changed; previously installed mods should be moved to the `modInstaller` folder

---

## v0.9.5

> Update focused on crash and bug fixes.

### Bug Fixes
- Fixed a regression introduced in v0.9.4 where a removed line of code disabled the automatic checkpoint restart after using a typewriter with Character Swap active, causing more frequent crashes than usual

### Notes
- 96% of the trainer now uses the translation system. Community translations are welcome via the repository below:
  `https://github.com/kreedyk/internal-trainer-lang`

---

## v0.9.4

> Update focused on security improvements and fixes for issues introduced in v0.9.3.

### Improvements
- Updated ImGui from v1.89.2 (2023) to v1.91.9b (2025) — improvements include better responsiveness and reduced memory usage; several visual changes to the menu were also made
- Recreated the environment preparation DLL — `xinput1_3.dll` should no longer trigger false positive antivirus warnings
  - **Note:** The trainer DLL itself still shows 2 false positives on VirusTotal (ClamAV for embedded `plxx.udas`; Trapmine for being an unknown binary). Windows Defender and most reliable antivirus solutions will not flag or delete the files

### Bug Fixes
- Fixed crash when activating Color HUD with qingsheng DLL or Razor DLL present
- Fixed upside-down image preview in the modloader
- Fixed modloader not correctly installing audio files (`.xsb`)
- Fixed auto-load not loading high kick melees
- Fixed random low melee crash on character swap
- Fixed Leon Outfit Swap not working when switching stages
- Fixed Leon's size not persisting when switching stages
- Fixed issue with Razor DLL causing problems when damaging enemies (tested with Rising of Evil Definitive by kteo)
- Fixed missing hotkey for regular Freeze Enemies

### Other Changes
- VRAM Cleaner notifications are no longer enabled by default
- NiaSplit (speedrun timer) redesigned
- Removed hardcoded optimizations to Razor DLL — these were causing issues with certain mods. Razor DLL is outdated; new mods should not be built around it

### Additions
- Added Hall of Fame wall — accessible via Settings > Trainer. Names are managed manually and updated with each trainer release

---

## v0.9.3

> This version introduces support for the Companion DLL (Razor's DLL) with several compatibility and stability improvements. Also notable: `profapi.dll` is no longer used — the trainer now only requires `xinput1_3.dll`, eliminating dual injection.

**Important:** Hotkeys are reset in this version. Auto-update is disabled in this beta release to ensure it reaches only active supporters; it will return in the public release.

### Bug Fixes
- Fixed not being able to start NG+ with Character Swap
- Fixed wrong grenade hand texture with Ada's cinematic physics
- Fixed crash when launching the game without internet
- Fixed freeze when downloading updates
- Fixed crash when swapping character/melee in Separate Ways
- Fixed Krauser bow crash when used on other characters (pressing the swap button at least once is required for it to work with Leon)
- Fixed Bowgun crash when used by other characters
- Fixed trainer not opening on some computers
- Fixed Kill Tracker not showing correct stats across saves (especially deaths)
- Fixed VRAM overlay always appearing on screen

> **Known Issue:** Character Swap with Ashley crashes the game when using Krauser's bow — getting the bow as Ashley has been blocked. Do not attempt to obtain it via RE4Tweaks. Bowgun is unaffected.

### General Improvements
- Fully restructured menu layout — new sub-tabs added to accommodate the growing feature set
- Auto-load system rewritten — now loads in steps, separating sensitive functions for better stability and performance
- `plxx.udas` is now embedded inside the DLL — the sideload folder is no longer needed
- HUD color system reworked for more reliable memory detection
- Health Bar and Kill Tracker now work properly at 2K (and likely at 4K)
- Notification system improved — cleaner appearance and better behavior at higher resolutions
- Visual improvements to Health Bar and Kill Tracker
- Stage and inventory names improved for clarity
- Stage Jump UI improved — character coordinates and positions can now be adjusted (useful for future randomizer expansions)
- Quick Restart no longer activates on death (this was a bug); replaced by the new Death Auto Restart feature
- Female Animations checkbox removed — now automatically applied based on the active character
- Hotkeys now only trigger in-game, preventing accidental activation
- Hotkey detection improved (e.g., F4 no longer toggles collision if the feature is inactive)
- VRAM Cleaner now displays how much VRAM was freed (NVIDIA only); uses memory cache on fast stage reloads
- Simplified parry notifications; parry sound volume reduced
- Improved checkpoint detection after saving with Character Swap — now only triggers on actual saves, not on simply opening the typewriter menu
- Super Punisher improvements:
  - Now includes 5 effects: flame, knockback, strong knockback, knockdown, trip shot
  - Penetration increased from 3 → 5 (base) and 5 → 8 (exclusive)
- Character/Melee Randomizer now allows choosing what to randomize (minimum 2 characters)
- Modloader code improved — now supports `.xsb` and `.xwb` sound files
- Stage Randomizer improvements:
  - Removed "Randomizing…" screen when switching rooms (still shown for the character randomizer for now)
  - New "Open" command added for dead-end maps (R30A, R10D, R11F, etc.) — uses the default key or E if not found (controller not yet supported)
  - Improved key priority system to avoid softlocks (e.g., lifts require visiting the barn and collecting the false eye first)
  - Added seed input field to save and load used seeds
  - Manual Checkpoint restart no longer triggers the randomizer; a new Emergency Tools tab allows manually forcing the next stage if stuck
- Razor DLL load delay removed — major performance improvement when using the Companion DLL

### Always-On Features
These features are always active and require no INI changes or manual toggles:
- Fast save/load at typewriters (similar to RE4Tweaks skip fades)
- Removed Razor DLL startup overlay (stars screen)
- Disabled Razor DLL 4GB patch check
- Removed Razor DLL's 2x memory extension (caused restart crashes)
- Prevented Razor DLL from loading files twice (fixes checkpoint restart crash)
- Leon (and other characters) can now interact in Ashley-only stages (R20E, R20D) — pressing buttons, throwing lanterns, crawling
- FixX3DAudio always enabled — improves memory usage, allows HD Project without RE4Tweaks, and significantly reduces random crashes (especially impactful on difficulty mods with many enemies)
- Max enemies on screen raised from 60 → 255
- Max explosion targets raised from 20 → 255
- Mini-bosses like JJ now disappear like regular enemies
- Tactical Vest is now purchasable on Professional difficulty
- CompanionToX3DAudio (previously INI-only) is now always active

### New Features
- **Panic Mode** — disables everything with one click (useful if something breaks or you want to go back to vanilla)
- **Auto Skip Cutscenes** — skips all cutscenes automatically
- **Kill Aura** — kills nearby enemies
- **No Melee Cam / No Aim Cam / No Knife Cam** — disables camera lock during these actions
- **Camera Swap** — switch between Leon solo and Leon with Ashley camera
- **Rainbow HUD** — HUD cycles through 3 random colors after each room change
- **Matilda Quickturn** — useful for non-RE4Tweaks users
- **ESL On Retry** — reloads enemies from `.esl` files; useful for modders testing mods
- **Allow Killing Ashley** — removes the mission failed condition when she dies
- **Typewriter Info** — displays Stage ID and Room Name at typewriters
- **No Enemies Disappear** — enemies won't vanish when the village bell rings (R101) or after the castle cannon (R202); useful for modders
- **Cinematic Bars** — adds black bars like in cutscenes
- **Disable Shadow** — removes all game shadows
- **Remove Drops / Remove Knife** — useful for testing scenarios
- **Max Health Slider + Yellow Herb Simulation (G+R+Y)** — especially useful when playing as Ashley
- **Inventory Editor + Tracker** — edit inventory and view live item counts without opening the case
- **Melee Heavy Ganados** — enables melee attacks on JJ and Mega
- **Death Auto Restart** — detects death and auto-restarts without showing the "You Are Dead" screen; the death is not counted since the chapter end was completely skipped
- **Ashley Jumps Alone** — lets her jump down by herself (requires extra modloader file for HD Project only)
- **Freeze Enemies** — blue tint and slowed sound effect; toggle with F7. Hotkeys are now required to apply the freeze — activating the feature alone does not freeze immediately
- **Krauser Aura Color Changer** — real-time aura color editing (also works with the Krauser Arm feature)
- **Auto Heal** — automatically uses herbs, sprays, or eggs when in danger (fully configurable)
- **Krauser Beret** — integrated with the modloader
- **Arrows-Only Drops** — removes ammo drops by default; only arrows, grenades, heals, and money drop (ammo version available on request)
- **Add Krauser's Bow to Inventory** — button to add the bow directly
- **Load Krauser's Mercs Inventory** — button to load Krauser's mercenaries loadout
- **Sound Hitmark** — visual indicator and sound on hit; adds a mini crosshair for less than one second when a shot connects (great with rifles)
- **Character Size** — changes character size (e.g., Ashley resize)
- **Visual Optimizations:**
  - Removed death effects from enemy corpses
  - Removed chainsaw smoke effect
  - Removed dynamite effects
- **Speedrun System:**
  - Smart timer that pauses during loading and ESC pause
  - Auto-split support
  - Tracks PB, best segments, and gold times
  - Everything saved automatically — no setup required
- **New Launcher:** Added `RE4_Launcher` in `kreed > utils`. Includes the 1.0.6 executable, applies a 4GB+base patch, and can manually inject the trainer if the game was opened without it. GitHub (open-source): `https://github.com/kreedyk/re4launcher`
  - If the game doesn't launch, use this launcher (wrong `.exe` likely)
  - To play without the trainer and inject later, use the DLL Injector tab

### Installation
1. Remove the old `profapi.dll`
2. Place the new `xinput1_3.dll` along with the `kreed` folder inside your `Bin32` folder

The trainer will attempt to replace an incorrect executable automatically. If this does not happen or the trainer does not open, use the new launcher at least for the first run.

---

## v0.9.2

### Known Issues
1. Ada Cinematic Physics causes part of her dress to be missing in the inventory. This occurs because the Ada Cinematic file (`pl02`) is used directly instead of the Separate Ways file (`pl16`) as in the old trainer. A fix is known but would be too intrusive to justify.
2. Grenade explosions and crate breaking are muted when playing as Ashley — a limitation of `plxx.udas`. To fix, go to the Modloader tab and install Ashley Audio Fix from online mode (HD Project only).
3. Playing as Ashley with the Armored outfit (Special 2) crashes the game during cutscenes — another `plxx.udas` limitation. This outfit was removed from the randomizer to prevent unexpected crashes; a warning popup was added to Character Swap if you choose to use it.

### Bug Fixes
- Fixed melees failing — the previous code relied entirely on the game choosing melees based on the character; now the trainer explicitly calls the correct melees per character
  - Note: Ashley will now execute her special Ashley Push melee instead of Leon's default kick. When Melee Swap or Melee Randomizer is active, this system is disabled to avoid conflicts. If playing as Leon with Character Swap, High Kick and Low Kick are used — Suplex will not trigger for Zealots or Island Ganados. Enable Melee Swap to restore that behavior
- Removed visual-affecting components from VRAM Cleaner (pixelation, blue artifacts, distorted effects) while retaining ~90% of memory cleaning effectiveness
- Stage and Character Randomizer now shows a black "Randomizing…" screen during randomization instead of a repeated loading screen
- Fixed false positives that incorrectly detected the game as paused while in-game, causing some features to malfunction
- Optimized thread and timer systems — reduced overhead and minimized potential freezes (directly affects parry and randomizer background timers)
- Added protection for R209 (1-2-3-4 puzzle and Salazar cutscene) — automatically switches to Ada to avoid crashes (discovered by InsideCat)
- Improved female animation system stability (was breaking due to crashes)
- Improved injection system — the trainer should open reliably without needing to rename to `xinput`. Please report if renaming is still required
- Fixed Camera Freeze not working
- Fixed Flash Freeze and Flash Pulverize not working

### New Features
- Added outfit swapper for Ashley
- Added VRAM Overlay Monitor — accurate and real-time for NVIDIA cards (uses NVIDIA API); AMD cards use a generic DirectX fallback (less accurate)
- Added overlay statistics — displays enemies killed in total and per chapter, shots fired, deaths, and hit ratio; includes a streak version with a kill bar
- Added pistol upgrade values at the merchant to the Weapon Modifier (except Matilda; only addresses that are available have been added). Changes are saved to config alongside other attributes

### Update Instructions
No need to remove old files — just replace the DLL. An in-game notification will inform you of new updates; press F9 to manually check. The downloaded update will be placed in the `kreed` folder as `update.zip`.

---

## v0.9.1

### Major Fixes
- **Save Game Crash:** Fixed crash after saving while using Character/Melee Swap (thanks to Veskercon for tracking this down)
- **New Safety Function:** Added an automatic checkpoint restart every time you exit a typewriter machine. This activates when features that require the confirmation popup are in use (Character/Melee Swap, Randomizer, Melee Anytime, Wesker Power) — necessary to prevent crashes caused by memory values changed after typewriter interactions
- **Character Swap Saves — Important:** Saving with a non-Leon character and then loading that save after closing the game will crash the game. Use a config with auto-load to handle this automatically, or manually load the config before loading the save
- **Feature Conflict Fixed:** Fixed conflict between Fast Switch and Show Enemy HP causing a crash when both were active; mutual blocking is now enforced so both cannot be enabled simultaneously
- **Krauser Arm & Character Swap:** Fixed conflict where Krauser Arm (mixed herb grants arm on any character) combined with Character Swap made it impossible to control Ashley while playing as Krauser. A new "Krauser Controls Ashley" option was added to the Character Swap tab — enabling it automatically blocks the Krauser Arm feature
  - To control Ashley with Krauser: stand completely still and press the call button (default: Z)
  - To use the arm: press the button while walking
  - Bonus: Krauser's arm will no longer kill Ashley
- **Improved Compatibility:** Fixed crash when using Krauser Arm with Character Swap and Remake Parry simultaneously

### Minor Fixes
- Fixed all (likely) sound issues related to Ashley on her playable version
- Fixed Krauser knife animation
- Fixed wrong camera when using Krauser's arm after loading a config
- Fixed wrong Ashley presence help marker
- Fixed Ada TMP crosshair getting locked after activating the stable laser
- Fixed Ada Cinematic Physics with audio not working
- Fixed crash when using Ada Cinematic Physics in the first cutscene
- Fixed language not saving to config
- Fixed modloader not properly installing local `.zip` files
- Fixed modloader not updating the mods folder in real time when using local mode
- Fixed Flash Freeze feature making the game slow
- Fixed Wesker Power feature not deactivating properly
- Fixed false positive in HD Project detection — now correctly detects whether HD Project is in use and which version

### New Features & Improvements
- Added more female animations for Ashley (including knife animation)
- Added button to increase UI scale in settings (useful for TV or very large screens)
- Added code to prevent Ashley from dying after Krauser's arm is used
- Added stronger executable check — the trainer now includes the correct 1.0.6 executable and offers an installation option if the wrong version is detected
- Added update system — checks on every game launch (or manually from the Settings menu), notifies of available updates, and offers download. The update file (`update.zip`) is saved to the `kreed` folder
- VRAM Cleaner considered stable enough to be enabled by default — disable and report if issues occur
- Enemy HP code fully rewritten:
  - Custom HP bar with configurable appearance and position
  - Displays both numeric HP values and percentages
  - Option to hide the original in-game HP bar
  - Dynamic color system based on enemy type

> **Important:** If you have an existing configuration file, please create a new one — a lot has changed, especially in `.cfg` files. Loading an old config may result in invalid values being applied.
