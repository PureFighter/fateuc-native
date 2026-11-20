# Fate/unlimited codes: native PC port with rollback netplay

> [!IMPORTANT]
> **No game files here.** This repository and its downloads contain **none of *Fate/unlimited codes'* files or
> data**: no disc image, no graphics, sound, music, movies, text or saves. **You need your own copy of the game.** The
> port runs from **your own disc image** every time it starts, and it does nothing without it.
>
> Please don't ask for, share or link game files or disc images here. Issues and comments that do are deleted.
>
> *How it works:* `ps2run.exe` is the game's program, recompiled into a native PC program with
> [ps2-native-recomp](https://github.com/exoteric33/ps2-native-recomp). Everything it shows and plays is read from
> your disc image.

A fan-made native PC port of the PS2 fighting game *Fate/unlimited codes* (Japan, SLPM-55108), with:

- **Rollback netplay** (GekkoNet), with an automatic input delay in two feels, Responsive and Smooth;
- **Rooms** for up to 8 players: two seats, a queue, Accept, and everyone else watches live;
- **Practice mode** with frame data, move lists in English, input history and recordings;
- **Widescreen** for every screen shape, and a launcher with your profile and match history.

It is not affiliated with or endorsed by Type-Moon, Cavia, Eighting or Capcom.

**Current release: Release 1** (test 23):
[`builds/FateUC-RollbackTest-23.zip`](builds/FateUC-RollbackTest-23.zip). What's in it and its SHA-256:
[RELEASES.md](RELEASES.md). Both players need the same release: different releases don't connect, and the screens
say so.

## Get started

You need Windows 10 or 11 (64-bit), **your own disc image** of *Fate/unlimited codes* (Japan, SLPM-55108) as an `.iso`
file, and a controller, an arcade stick or the keyboard.

1. Download the current release's zip from [`builds`](builds): click it, then **Download raw file** (top right).
2. Right-click the zip, **Properties**, tick **Unblock**, **OK**. Then extract it into a folder of its own.
3. Put your `.iso` into that folder, or into the folder above it so that every release finds it.
4. Double-click **`FateUC.exe`**, the launcher. The programs are not signed, so Windows may say "Windows protected
   your PC": press **More info**, then **Run anyway**. If Windows asks whether `ps2run.exe` may use the network,
   allow it.
5. The first start checks the game and your disc, and asks for your name: the one other players see.

The [tester guide](TESTER-GUIDE.md) has the rest: playing online, rooms, reporting, and what to do when something
goes wrong. The zip's `README.txt` is the full manual (every setting, key and file).

## Play

| In the launcher | What it does |
| --- | --- |
| **Home** | Play offline, or Practice against the dummy with the characters and stage you pick |
| **Host** | Online as player 1: your game shows a 5-digit code; send it to the other player only |
| **Join** | Online as player 2: type the code |
| **Room** | Rooms for up to 8: two seats, a queue, Accept, and everyone else watches live; practice while you wait |
| **History** | Your online sessions and matches |
| **Reports** | The last session's connection report, your report zips, and **Report a problem** |
| **Settings** | Profile (your name and stats), Game (picture, controllers), Online (Responsive or Smooth), About (credits) |

- No port forwarding is needed in most homes: the games meet through a small code server, ask the router to open
  the port, or call each other at once. When they can't get through, the windows say why.
- In the game: **F1** opens the menu (**Start** in practice), **F4** shows or hides the session line (ping, input
  delay, rollbacks), **F11** switches full screen.

## Report a problem

Press **Report a problem** in the launcher (on the Reports tab, or after a session). It opens a new issue here with
the build, your setup, the ping and your PC already filled in, and it shows your report zip. Write what happened,
then drag **both players'** report zips into the box. You can also open an issue yourself with the **Report** template.

**Issues are public.** The report zips hide IP addresses, codes and your Windows user folder, but anyone can read
what you write and attach. Never attach game files, disc images or `.state` files.

## Credits

- **PureFighter**: the idea and the direction, every test, and every decision.
- **Claude** (Anthropic): the code, written by a team of Claude agents, each with its own part:
  - **W1**, the lead: the plan, the reviews, putting the parts together, the builds and the releases.
  - **W2**: online play, the game's own launcher window, the settings and the F1 menu, controllers, the code server
    and the rooms, the practice menu, the move lists and the stick display.
  - **W3**: the benchmark.
  - **W4**: fast saved states, GekkoNet rollback, hunting down desyncs, widescreen for every screen shape, practice
    mode, the vote after a match, the automatic input delay and watching live matches.
  - **W4B**: the second opinion on rollback's saved states.
  - **W5**: the survey of other ports and the first measurements.
  - **W6**: the launcher (`FateUC.exe`): its design, settings, profile, history, the Room tab and Report a problem.
  - **W7**: replays: keeping, playing and checking them.
  - **W8**: the design for watching online matches.
  - **OBS**: the match observer, which knows the rounds, the wins and the characters.
- Built on, with thanks: [ps2-native-recomp](https://github.com/exoteric33/ps2-native-recomp) by Samir Nuri and
  exoteric33 (MIT), and ran-j's [PS2Recomp](https://github.com/ran-j/PS2Recomp), which recompiled the game first;
  GekkoNet (BSD-2), miniupnpc (BSD-3), zpp_bits (MIT), SDL2 and SDL_GameControllerDB (zlib), wgpu-native (MIT and
  Apache-2.0), the DirectX Shader Compiler, Play!'s MPEG tables (BSD-2); nemesis2000's 16:9 patch, where our
  widescreen started; the Mizuumi wiki's Fate/unlimited codes pages, for the names of the moves. Their licences are
  in the zip's `licenses` folder.
- *Fate/unlimited codes* is by Type-Moon, Cavia, Eighting and Capcom, and its names and marks are theirs. This
  project contains none of the game's files or data.
