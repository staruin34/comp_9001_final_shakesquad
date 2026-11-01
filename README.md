# Snake Squad 2.0 — COMP9001 Final Project

This repository hosts version 2.0 of Snake Squad for the COMP9001 final project submission.

Snake Squad is a top-down desktop squad shooter written in Python with Pygame. Choose a hero, rescue allies who follow in a snake formation, switch between pistol and sword combat, and clear three dungeon levels. A hidden fourth level offers a three-minute survival challenge.

## Download the complete project

**[Download SnakeSquad_Final_2.0.zip](https://raw.githubusercontent.com/staruin34/comp_9001_final_shakesquad/3a3e2d5fbbbd32faae86b701022afa2274df9ac7/SnakeSquad_Final_2.0.zip)**

[Alternative GitHub file page](https://github.com/staruin34/comp_9001_final_shakesquad/blob/3a3e2d5fbbbd32faae86b701022afa2274df9ac7/SnakeSquad_Final_2.0.zip)

The archive contains all Python source files, artwork, music, runtime requirements, run instructions, and the original AI usage and asset attribution statement. Extract it before running the game.

- Archive size: **21,267,690 bytes** (approximately 21 MB).
- Fixed archive version: `3a3e2d5fbbbd32faae86b701022afa2274df9ac7`.
- SHA-256: `92ac83c79bf2526405b9637271ecc915561713e24987b7732292b46418201409`.

Both links were checked without signing in on 1 November 2026. The downloaded ZIP matched the local submission archive byte-for-byte.

## Requirements and Ed compatibility

- Tested with **Python 3.13.15** and **pygame 2.6.1** on Windows.
- Third-party runtime dependency: `pygame==2.6.1`, specified in `requirements.txt`.
- Desktop GUI: a **1280 × 720** Pygame window; keyboard and mouse required.
- Loads PNG artwork and plays `assets/audio/bgm_battle.mp3` through `pygame.mixer`.
- No video processing, web services, or networking during gameplay. Internet access is needed only to download the archive and install Pygame.
- **Run the game locally outside Ed**, because it requires graphics and audio support.
- `pytest` is a development tool and is not required to play. `tkinter`, when available with Python, is used only for an optional startup-error dialog.

## Install and run

1. Download and extract `SnakeSquad_Final_2.0.zip`.
2. Open a terminal inside `SnakeSquad_Final/SnakeSquad/`, where `main.py` is located.
3. Install the dependency with the same Python interpreter that will run the game:

   ```sh
   python -m pip install -r requirements.txt
   ```

4. Start the game:

   ```sh
   python main.py
   ```

5. Click a character card or press **1** or **2** to begin.

On Windows, `py -3.13` can replace `python` in both commands. After installing the dependency, `run_game.bat` is another way to start the game.

**Entry point: `main.py`.** Keep the `game/` and `assets/` folders beside it. Do not run modules inside `game/` individually.

## Version 2.0 changes

- The world view covers 1408 × 792 world units in the same 1280 × 720 window, increasing both visible dimensions by 10%. Mouse aiming is adjusted to the wider view.
- Teammates recruited through fish-egg deposits in the hidden survival level now receive a randomly selected portrait from the four normal squad portraits.

## Controls

| Key / mouse | Action |
| --- | --- |
| W / A / S / D | Move |
| Mouse | Aim |
| Left mouse button | Fire pistol / perform sword combo |
| Space | Dash |
| F | Switch weapons after obtaining the sword |
| 1 / 2 | Select a hero on the selection screen |
| Esc | Pause / resume |
| R | Restart the current level |
| N | Advance after victory in levels 1 and 2 |
| Hold Tab | Show melee range preview |
| O | Toggle the debug parameter panel |
| F1 | Toggle path debug drawing |
| Window close button | Quit |

The gear button in the top-right corner opens the music volume slider.

## Quick play guide

Touch a weapon station in the rest area to equip that weapon. Move right through the corridor to enter combat. Rescue waiting allies to build your squad, then defeat all enemies to clear the arena. After winning levels 1 and 2, press **N** to continue.

There are three normal levels. On level three, enter the top-left corner of the rest area to reach the hidden three-minute survival level.

Optional developer benchmark:

```sh
python main.py --stress-test
```

## Folder structure of the runnable project

The runnable project is inside `SnakeSquad_Final/SnakeSquad/` in the ZIP.

```text
SnakeSquad/
├── main.py
├── README.txt
├── README_en.md
├── requirements.txt
├── run_game.bat
├── SOURCE_FILES.txt
├── AI_Usage_Statement.docx
├── game/
│   ├── __init__.py
│   ├── game.py
│   ├── level.py
│   ├── settings.py
│   ├── combat/
│   ├── entities/
│   ├── squad/
│   └── ui/
└── assets/
    ├── README_en.md
    ├── sprite_index.json
    ├── sprites/
    ├── characters/
    ├── maps/
    └── audio/
```

`SOURCE_FILES.txt` lists all **48 Python files** and their relative paths.

## Troubleshooting

- **`ModuleNotFoundError: pygame`**: install the dependency with the same Python interpreter used to start the game.
- **Missing artwork or asset files**: fully extract the archive and check that `assets/` is next to `main.py`, without an extra nested `assets/` folder.
- **No music**: check the in-game volume slider and system audio output. The game can continue without a working audio device.
- **Unexpected startup error**: check the terminal output and `crash_report.txt`, which is saved beside `main.py` when that folder is writable.

## Verification

Automated checks passed for Python syntax, both hero selections, level 1–4 loading and rendering, pause/resume, weapon switching, level progression, survival settlement, and stress-mode startup. All 120 PNG files and the MP3 loaded successfully.

These smoke checks used SDL dummy display and audio drivers; they do not replace a complete manual playthrough or verification of physical input and audible output.

## AI usage and asset attribution

The included `AI_Usage_Statement.docx` records AI assistance with code writing, refactoring, debugging, and expanding character sketches into artwork and animation frames. It also describes the character-design references, third-party environment placeholders, and external background music.

The original asset notes are included in `assets/README_en.md`. Asset redistribution and commercial licences have not been independently verified; this README does not grant such licences.

## Ed submission

The complete archive exceeds Ed's 2 MB limit, so this repository provides the external download described in the course submission instructions.

For the Ed submission, upload **all 48 Python files and `README.txt`**, preserve the Python package directories, and include the external archive link in `README.txt`. The external download supplements the Python source submission.

The course deadline is **1 November 2026, 11:59 pm, Sydney time**. Do not modify the submitted GitHub or OneDrive files after the deadline.
