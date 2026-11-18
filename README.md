# Arbiter

A companion for Watcher of Realms on Windows. It reads the game running on the same PC and shows your account:
heroes, Demon Soldiers, gear, artifacts, the Pantheon and your collection, with a Fight Simulator, a BP
Calculator and Gear Plans built on it.

A fan project, not affiliated with Moonton.

## What it does with the game

- It **reads** the game's memory while the game runs, and **never writes** to it or injects anything.
- **Your account stays on your computer.** Arbiter keeps it in `%LOCALAPPDATA%\Arbiter\` and sends it nowhere.
  From the internet it only fetches the game's public data (names, art, skills) and, when you open Settings, which
  version is the latest one published here.
- If the game runs as administrator, Arbiter asks Windows for administrator as you bring it to the front; say yes (or press
  **Give admin rights** in Arbiter later). Arbiter starts its reader as administrator, which reads the game for Arbiter's window
  and writes no file; the window itself runs as you, and keeps what was read.

## Install

1. Download `arbiter-setup-<version>.exe` from the [latest release](../../releases/latest).
2. Check the download (optional): in PowerShell,
   `Get-FileHash "arbiter-setup-<version>.exe" -Algorithm SHA256`, and compare it with the release's
   `SHA256SUMS.txt`.
3. Run it and say yes to Windows' administrator prompt. Arbiter installs once for the PC, in
   `C:\Program Files\Arbiter`, with a Start menu entry. Only an administrator can change that folder, so no other
   program can change what Arbiter's reader runs as administrator. Each Windows user keeps their own account.

Arbiter is not signed yet, so Windows SmartScreen may say "Windows protected your PC". Choose **More info**, then
**Run anyway**.

## Updates

Settings says when a newer version is out, with its link. Install it over the one you have when you want (Windows
asks for administrator again): your account stays. Arbiter never updates itself.

## Uninstall

Windows Settings → Apps → Arbiter → Uninstall, as administrator. Your account stays in `%LOCALAPPDATA%\Arbiter\` until you delete it
(or use Forget in Arbiter's Settings first).
