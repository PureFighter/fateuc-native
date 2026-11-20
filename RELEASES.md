# Releases

## Release 1.2 (test 24), 20 November 2026

Fixes for the first reports, thank you for them. **Both players need Release 1.2**: it doesn't play with Release 1 or
1.1 (the game's simulation changed), with codes or in rooms.

- **Practice no longer freezes when you choose a stage** (issues #1 and #2), and **quitting no longer leaves the game
  stuck** in Windows until Task Manager ends it. Both came from one wait in the game's drawing queue that could miss
  its wake-up while a stage loaded. It's fixed, and a game that still hasn't closed 8 seconds after you quit now ends
  itself (exit code 8), with what was still running in its log.
- **The launcher (0.7.0) and the game stay in step.** A game started by hand (`ps2run.exe`), or one stuck after
  quitting, no longer makes the launcher's starts do nothing: the launcher says so and offers to close it. Requests
  and replies left over from an earlier start are set aside and never act on a later game. When the game doesn't
  start, the launcher says why and what to do.
- **Your controls and settings** are saved whole at each change, a save that fails says so on screen, and controller
  files work in folders with non-English letters. **Older settings** at the first start now also brings your
  controller's button layout. The game's own **OPTION > BUTTON CONFIG** is not kept yet: use **F1 > Change keys** or
  **F1 > Controllers**, which are kept and work online too. The game tells you once when you change its BUTTON CONFIG.
- **Choppy sound at moves like Saber's 236L:** we couldn't make it happen here, but a likely cause is handled: the
  graphics card's programs for the effects a run meets are kept in `data\hw\pipelines.txt` and made before the game
  starts, from the second start on. If you still hear it, please report it: the log now says what each stutter
  waited for.
- **11 more of the game's VU1 programs are built in** (met on stages 1, 3, 4, 5 and 10), instead of running in
  the slower interpreter.
- **Rooms and Host/Join:** a player back from a dropped connection gets the seat that waited; a match whose opponent
  left first ends instead of holding the room; a comeback the room service refuses leaves the room at once, with
  words; Sit, Accept or a start pressed twice counts once.

**Download** [`builds/FateUC-RollbackTest-24.zip`](builds/FateUC-RollbackTest-24.zip). To update, close the game and the launcher, then
either copy the new folder's files over your Release 1.1 folder (your keys, settings, name and history stay), or
extract it into a new folder: at its first start, **4. Older settings** brings your keys, controller settings and disc
choice from the old one. This release contains none of the game's files or data either: it runs from your own disc
image.

**Try first:** Practice, choosing different stages from the practice menu; quitting the game, from the launcher and
from a game started by hand; then a session or a room with a friend.

**SHA-256** of `FateUC-RollbackTest-24.zip` (32,328,231 bytes): `476a4a265f4c68729f55c7e45fa202a3a26e37c9911a51636f3574f16429d003`

## Release 1.1 (test 23), 20 November 2026

A small update of Release 1. **It plays with Release 1**, with codes and in rooms, so nobody has to update at the
same time.

- **Quieter sound by default:** 75% of Release 1's level. Set your own with a line in `data\keys.ini`, from
  `volume = 0` to `volume = 100` (100 is Release 1's level); the game reads it when it starts. The key tones (F5, F8,
  F9) follow it too.
- **Shorter credits** in `CREDITS.txt`, which the launcher's Settings > About shows.

**Download** [`builds/old/FateUC-RollbackTest-23-1.1.zip`](builds/old/FateUC-RollbackTest-23-1.1.zip). To update a Release 1 folder, copy the zip's
files over it: your keys, settings, name and history stay. This release contains none of the game's files or data
either: it runs from your own disc image.

**SHA-256** of `FateUC-RollbackTest-23-1.1.zip` (31,463,935 bytes): `541355d65bdeb4c0430bfcf9f71cec15d5e0223d96abb36e0808a72c99be47a2`

## Release 1 (test 23), 20 November 2026

> [!IMPORTANT]
> **No game files here.** This release contains **none of *Fate/unlimited codes'* files or data**: no disc image, no
> graphics, sound, music, movies, text or saves. **You need your own copy of the game.** The port runs from **your
> own disc image** every time it starts, and it does nothing without it. Please don't ask for, share or link game
> files or disc images here.
>
> *How it works:* `ps2run.exe` is the game's program, recompiled into a native PC program with
> [ps2-native-recomp](https://github.com/exoteric33/ps2-native-recomp). Everything it shows and plays is read from
> your disc image.

The first public release of the native PC port of *Fate/unlimited codes* (PS2, Japan, SLPM-55108) with rollback
netplay. Both players need Release 1: older test builds don't connect to it.

**Download** [`builds/old/FateUC-RollbackTest-23.zip`](builds/old/FateUC-RollbackTest-23.zip), then follow
[Get started](https://github.com/PureFighter/fateuc-native#get-started) and the
[tester guide](https://github.com/PureFighter/fateuc-native/blob/main/TESTER-GUIDE.md).

### What it has
- Rollback netplay (GekkoNet) with an automatic input delay in two feels, **Responsive** and **Smooth**; 5-digit
  codes to play one other player, with no port forwarding in most homes.
- **Rooms** for up to 8 players: two seats, a queue, Accept, sets of first to 1, 2 or 3, and everyone else watching
  live in their own window; practice while you wait for your turn.
- **Practice mode** with the dummy's settings, recordings, frame data, English move lists and input history.
- **Widescreen** for every screen shape, controllers and arcade sticks, and a launcher with your profile and
  match history.

### New since the last test build
- **A clean screen:** no test labels, no connection report after each match (it is on the launcher's Reports tab),
  and messages such as "controller connected" go to the log only. F4 still shows or hides the session line.
- **Report a problem** in the launcher: it opens a new issue here with the build, your setup, the ping and your PC
  filled in, and shows your report zip to drag in.
- The code server has a new address; older test builds can't use its codes or rooms any more.

### What to try first
- A room with three or more players: Sit and Accept, watching, practice while you wait, and who stays after a set.
- Report a problem after a session: is everything in the new issue right, and nothing private in it?
- Responsive and Smooth at your distance: which feels better?

Rooms have been tested in the lab and against the live service, but not yet by players on several PCs: tell us how
it goes, good or bad.

**SHA-256** of `FateUC-RollbackTest-23.zip` (31,462,875 bytes): `4df57bf8b9615a122e45ae9bc291b8c665660ca82024a45ed8ee1acef848aab9`
