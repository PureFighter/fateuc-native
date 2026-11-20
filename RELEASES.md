# Releases

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

**Download** [`builds/FateUC-RollbackTest-23.zip`](builds/FateUC-RollbackTest-23.zip), then follow
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
