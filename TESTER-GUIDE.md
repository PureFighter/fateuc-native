# Tester guide

Thanks for testing the native PC port of *Fate/unlimited codes* with rollback netplay. This page is all you need:
installing, playing a session with friends, and reporting. The zip's `README.txt` is the full manual (every setting,
key and file).

> [!IMPORTANT]
> This project contains **none of the game's files or data**. You play from **your own disc image**, made from your
> own copy of the game. Nobody here can give you the game: please don't ask for it, and never share disc images or
> game files in issues or comments.

## 1. What you need

- Windows 10 or 11 (64-bit).
- Your own disc image of *Fate/unlimited codes* (Japan, SLPM-55108) as an `.iso` file.
- A controller, an arcade stick or the keyboard.
- For online: a normal home connection. Port forwarding is not needed in most homes. A cable beats Wi-Fi.
- To report: a free GitHub account.

## 2. Install (about 5 minutes)

1. Open the current release's zip in [`builds`](builds) (the front page names it) and press **Download raw file**
   (the download button at the top right of the file's page).
2. Right-click the zip, **Properties**, tick **Unblock**, **OK**.
3. Extract it into a folder of its own, for example `Documents\FateUC\FateUC-RollbackTest-23` (not inside Program
   Files).
4. Put your `.iso` into that folder, or one level up (`Documents\FateUC`) so that every release finds it.
5. Double-click **`FateUC.exe`**, the launcher. The programs are not signed, so Windows may say "Windows protected
   your PC": press **More info**, then **Run anyway**. If Windows asks whether `ps2run.exe` may use the network,
   allow it.
6. The first start checks the game and your disc, can bring your keys and controller settings over from an older
   folder, and asks for your name: the one other players see. You can change it later in **Settings > Profile**.

## 3. Play

- **Start with practice:** **Home > Practice** puts you straight into a fight against the dummy. Check your
  controller and the picture there first.
- **1 against 1:** one player presses **Host** and gets a 5-digit code, and sends it to the other player only. The
  other player presses **Join** and types it.
- **Rooms:** one player makes a room in the **Room** tab and shares its 6-digit code. Up to 8 players join. Two of
  them **Sit**, both press **Accept**, and the match starts by itself. Everyone else watches it live, and anyone
  waiting can press **Practice** until their turn.
- **In the game:** **F1** opens the menu (**Start** in practice), **F4** shows or hides the session line (ping, input
  delay, rollbacks), **F11** switches full screen.
- **Feel:** in **Settings > Online**, **Responsive** has the least input delay, and **Smooth** adds a frame where
  that steadies the picture. Try both and tell us which you prefer at your distance.

## 4. A test session

1. Agree on a time with your friends. Everyone uses the **same release**: different releases don't connect.
2. The release's notes in [RELEASES.md](RELEASES.md) say what to try first; then just play.
3. Keep the launcher open while you play. When a game closes, the launcher packs a **report zip** for that session
   (see its **Reports** tab).
4. Afterwards, each player reports (section 5). A session where everything went well is worth a report too.

## 5. Report

1. Press **Report a problem** in the launcher: on the **Reports** tab, or in the summary after a session or a room
   match. Your browser opens a new issue here with the build, your setup, the ping and your PC filled in, and a
   folder opens with your report zip selected.
2. Write what happened, when, and whether it happened again.
3. Drag **both players'** report zips into the box. Pictures or a short video help a lot: drag them in too.
4. One problem per issue. Without the launcher, open **Issues > New issue** and choose **Report**.

Good to know:

- **Issues are public.** The report zips hide IP addresses, codes and your Windows user folder, but anyone can read
  what you write and attach.
- If a game freezes, wait about **10 seconds** before closing it. Its log then says what each part of the program
  was doing.
- If a game closes by itself, the launcher says how it ended. Run **`Check why the game closed.bat`** in the release's
  folder and attach the text file it writes.
- Never attach your disc image, game files or `.state` files.

## 6. When a new release comes out

- The front page names it, and [RELEASES.md](RELEASES.md) says what changed. PureFighter announces new releases.
- Both players need the new release: older and newer releases don't connect.
- Extract the new zip into a new folder next to the old one. Its first start brings your settings and your name
  over. Keep the old folder until the new one works for you.

## 7. If something goes wrong

| What you see | What to do |
| --- | --- |
| "Windows protected your PC" | **More info**, then **Run anyway** |
| The launcher can't find the disc | Put the `.iso` in the release's folder or the folder above, or pick it in the launcher |
| Can't connect | Check that you're both on the same release, read what the window says, swap who hosts, try again; then report with both zips |
| The controller does nothing, or shows up twice | In **Settings > Game** (or the F1 menu), set Controllers to **XInput only** or **DirectInput only** |
| Hitches, slowdown, input lag, characters jumping | Note the ping and input delay (F4) and when it happened, and report |
| "DESYNC" | Write down what each screen showed, and report with both zips |

## 8. Who's who

- **PureFighter** runs the project and decides what comes next.
- The code is written by a team of Claude agents (Anthropic). The [front page](README.md#credits) has the credits.
