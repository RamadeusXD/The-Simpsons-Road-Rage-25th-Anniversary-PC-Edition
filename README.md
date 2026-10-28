# The Simpsons Road Rage – 25th Anniversary PC Edition

An unofficial PC version of **The Simpsons Road Rage** (Xbox, 2001). It runs the original game code from **your own copy of the Xbox game** on Windows. Windows replaces the Xbox's graphics, sound and controller parts, and the game gets modern PC features on top.

**No part of the game is included in this download.** You need your own copy of the Xbox game.

---

## What you need

- Windows 10 or 11 (64-bit) or Linux through the proton layer.
- Your own **The Simpsons Road Rage for the original Xbox, North American (NTSC) version**, copied to your PC in one of two ways:
  - a folder with the disc's files (`default.xbe` and the `.rcf` archives), or
  - a disc image (`.iso`) you made of your disc
- About 1 GB of free space
- An internet connection the first time you install (see "Why does the installer download Python?")

## Install

1. Download **`RoadRage-1.0-Setup.exe`** from the [Releases](https://github.com/RamadeusXD/The-Simpsons-Road-Rage-25th-Anniversary-PC-Edition/releases) page and run it.
2. On its one page:
   - choose where the game goes (default: `C:\Games\The Simpsons Road Rage`, not Program Files)
   - choose your copy of the game with **Game folder...** or **Disc image (.iso)...**
3. Press **Install**. It takes a couple of minutes.
4. Press **Play**. The installer closes and the game starts with a Welcome message, then a **Setup menu**, then you create your profile.

The Setup menu offers:

- Desktop and Start menu shortcuts
- **Add to Steam** (as a non-Steam game)
- **Skip Opening Logos**
- **HD Textures** (see below)
- With a controller plugged in: your controller layout and button icons
- The changelog

Shortcuts, Add to Steam, Skip Opening Logos and HD Textures can be changed later in **Settings › Startup Options › Post Setup**.

**Using the zip instead** (`RoadRage-1.0-Windows.zip`, also works with Quiver): unzip it into a folder of its own and start `RoadRage.exe`. The first time, it opens the same setup, without the folder choice.

### Why does the installer download Python?

The game's menus, signs and button prompts need pictures that are made **from your own game files**, so they can't be shipped. The installer downloads a small private copy of Python (from python.org and pypi.org, about 75 MB) to make them, then deletes it again. The game itself never uses Python.

### The icon

The game's logo is copyrighted, so this download comes with its own **RR** sign icon. While installing, the setup makes the game's icon on your PC from the title picture inside **your own** `default.xbe`, and gives it to `RoadRage.exe`, `RoadRageSetup.exe` and the shortcuts.

## HD textures (optional)

The game can make sharper copies of its own textures on your PC: about 2,200 of them, for the menus, cars, characters, the five neighbourhoods and the cut-scenes. Open **HD Textures** in the Setup menu (or **Settings › Startup Options › Post Setup**). Its page shows a progress bar, explains what happens, and has these settings:

| Setting | What it does |
|---|---|
| **Make HD Textures** | Start, Pause or Resume |
| **Works** | **Only in Menus** (the default: it waits during races and stops when the game closes), **Menus and Races**, or **Also When Closed** (it carries on after you quit until all are made) |
| **Delete HD Textures** | Removes them again to free the space |

- **Why it takes a few hours:** an AI upscaler (Real-ESRGAN) redraws each texture at 2 to 4 times its size. It runs on your processor and takes a few seconds per texture, so the whole set takes about 1 to 4 hours, depending on your PC.
- **While it works:** it runs in the background at a low priority, but the game can still run slower, which is why it waits during races by default.
- **Breaking it up:** every finished texture is kept, so you can pause, quit or switch off and it carries on where it stopped. Each part (menus and HUD, cars and characters, neighbourhoods, cut-scenes) is used from the next race once it's done, and the main menu shows how far it is.
- **Downloads and space:** the first start downloads Python and the upscaler (about 80 MB). The textures take about 500 MB. Everything it needed is deleted again when it's finished.

As with the menu pictures, nothing from the game is downloaded: the textures are made from your own copy.

## Updating

- In the game: **Settings › Support and Updates › Check for Updates**. If there is a newer release, **Download and Install** downloads its installer, starts it for your game's folder and closes the game. Press **Update** in the installer.
- Or in `RoadRageSetup.exe` (in the game's folder): **Check for updates** does the same.
- Or download the new `RoadRage-x.x-Setup.exe` yourself and pick the folder the game is already in.

Updating replaces the program and makes any new menu pictures. Your game files, saves and settings stay. The first time a new version starts, its changelog is shown once.

## Repairing

Run `RoadRageSetup.exe` in the game's folder and choose **Repair current build**. This makes every menu picture (about 500) again from the game files already installed, for example if some were deleted. You don't need your disc files again.

## Removing

**Windows Settings › Apps › The Simpsons Road Rage (PC recompile)**. Your saved games are kept unless you tick the box to delete them.

## What this PC version adds

The full list is in the game under **Settings › Changelog**. Highlights:

- Any resolution up to 8K, refresh rates up to 360 Hz, any screen shape, fullscreen (the default) or windowed (F11), FPS counter (F2), anti-aliasing, sharper text and pictures
- Xbox, PlayStation DualSense (light bar, trackpad, speaker audio), Steam and Nintendo-style controllers, plus keyboard and mouse
- Modern and Classic control layouts, and a first-person driver's view
- Achievements, screenshots (F12), profiles with their own saves, and save folders in Documents or cloud folders
- Optional HD textures, made on your PC from your own game files
- Skippable logos, much shorter loading, and redesigned menus

## Controls (keyboard)

| Action | Key |
|---|---|
| Steer / menus | Arrow keys or A / D |
| Accept | Enter, Space or Z |
| Back | Esc |
| Fullscreen | F11 |
| FPS counter | F2 |
| Screenshot | F12 |

Controllers work as they are. The layouts are shown in **Settings › Controller Layout**.

## Files

| Folder / file | What it is |
|---|---|
| `RoadRage.exe` | the game |
| `RoadRage.ini` | settings (most can be changed in the game) |
| `Game Data\` | the copy of your game files, plus the pictures made from them |
| `Save Data\` | your profiles and saved games |
| `Screenshots\` | F12 screenshots |
| `RoadRage.log` | what happened in the last run: attach it when reporting a bug |
| `RoadRageHD.log` | what the HD textures job did (only once you've started it) |

## Known issues and plans

- Performance can suffer on PCs with little free memory, or on laptops running on battery.
- German, French and Spanish can't be added yet because of encryption in the game's files.
- Planned for later updates:
  - native VR support, once its performance issues and bugs are resolved
  - The Simpsons Hit & Run soundtrack option
  - the Hit & Run map
  - the Road Rage beta map
- **Steam Deck / SteamOS**: run the installer and the game through Proton like any Windows game. This is not tested yet.

## Reporting bugs

Open an [issue](https://github.com/RamadeusXD/The-Simpsons-Road-Rage-25th-Anniversary-PC-Edition/issues) and attach `RoadRage.log` from the game's folder, or `RoadRageSetup.log` for problems with the setup.

## Legal

The Simpsons Road Rage is a trademark of its respective owners. This is an unofficial, non-commercial fan project. It is not made, endorsed or supported by them. No game files, logos or other copyrighted material from the game are distributed here; everything the game needs is made on your PC from your own copy. Please support the original by owning it.

Fonts: DejaVu and Lora (free licences, included in `setup\fonts`). Controller icons: a free icon pack.

Recompiled by **RamadeusXD**.
