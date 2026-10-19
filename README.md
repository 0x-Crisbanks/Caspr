<div align="center">

<img src="assets/hero.png" alt="Caspr: mission control for AI coding agents, in your Mac's notch" width="100%" />

<br />

[![Download Caspr for macOS](https://img.shields.io/badge/Download-Caspr%20for%20macOS-7c3aed?style=for-the-badge&logo=apple&logoColor=white)](https://github.com/0x-Crisbanks/Caspr/releases/latest)

![Latest release](https://img.shields.io/github/v/release/0x-Crisbanks/Caspr?style=flat-square&color=7c3aed&label=latest)
![macOS 14+](https://img.shields.io/badge/macOS-14%2B-0a84ff?style=flat-square&logo=apple&logoColor=white)
![Notarized by Apple](https://img.shields.io/badge/signed%20%26%20notarized-Apple-22c55e?style=flat-square)
![Local first](https://img.shields.io/badge/local--first-no%20cloud-f97316?style=flat-square)

**English** · [Español](README.es.md)

</div>

---

## Your agents work. You stay in flow.

AI coding agents run for minutes, ask for permission, and finish while you are in another window. Caspr puts all of that in the one place your eyes already pass: the notch.

- **See everything at a glance.** Every Claude Code, Cursor and Codex session, what it is doing, how much context and quota it has left.
- **Decide without switching windows.** Approve or deny a permission, answer a question, or queue a reply right from the notch.
- **Never miss the moment.** The panel opens by itself when an agent needs you, and you get a notification when it finishes.
- **A great notch even when you are not coding.** Music, a developer Pomodoro, timers, a file tray with AirDrop recents, calendar and more.

<br />

## Claude Code, live

<img src="assets/card-claude.png" alt="Claude Code sessions with a live feed in the notch" width="100%" />

Open any session and watch it work exactly like in the terminal: edits with line-by-line diffs, shell commands and their output, Claude's text and a live timer. See your account quota (5 h and 7 d windows) and the context used by each session.

- Approve **Deny / Allow Once / Allow All** for tool permissions and plans, or answer questions, without leaving what you are doing. Nothing is ever approved by default: if Caspr is closed or fails, Claude Code falls back to its normal terminal prompt.
- Reply to a session from the notch (Terminal, iTerm, Warp and other window-per-session terminals).
- Jump to the exact terminal of a session with one click.

<br />

## Cursor and Codex, same notch

<img src="assets/card-cursor.png" alt="Cursor session with live edits and shell commands" width="100%" />

One tab per tool, with a card per session: prompts, thoughts, file edits with diffs, shell commands with output, and the final answer.

- **Cursor** (IDE and `cursor-agent`): approve or deny shell and MCP commands from the notch, queue follow-up replies, and optionally see **how much of your Cursor plan is left** this billing cycle.
- **Codex** (CLI and app, beta): sessions and alerts through its lifecycle hooks.
- Connecting only adds clearly-marked entries to each tool's config, after showing you a preview and making a backup. **Disconnect** removes exactly those entries.

<br />

## Home: music, focus and timers

<img src="assets/card-home.png" alt="Music player and developer Pomodoro in the notch home tab" width="100%" />

Real album art and controls for Apple Music and Spotify, plus a **developer Pomodoro** whose ring fades as your session runs and shows how many agents are active. Switch between several styles, set any length from 1 to 240 minutes, or use countdown and stopwatch.

<br />

## Tray, AirDrop and everything else

<img src="assets/card-tray.png" alt="File tray with AirDrop recents" width="100%" />

Drop files on the tray to keep them one hover away, or onto AirDrop to send them. The ten most recent photos and videos you received by AirDrop show up as a swipeable carousel you can clear without deleting anything from your Mac.

There is also a clipboard history (memory only), snippets, calendar, app launcher, camera mirror, a volume and brightness HUD that replaces the system one, and a closed notch that adapts to what is happening:

<div align="center">
<img src="assets/notch-closed.png" alt="The closed notch showing album art, the Caspr ghost with active sessions, and music bars" width="640" />
</div>

<br />

## Install in 30 seconds

1. **[Download the latest `.dmg`](https://github.com/0x-Crisbanks/Caspr/releases/latest)**. No account needed.
2. Open it and drag **Caspr** to **Applications**.
3. Launch Caspr and follow the three-step welcome. Hover the notch to open the panel, or press **⌥⌘O**.

Caspr is signed with a Developer ID and notarized by Apple, so macOS opens it without warnings. It updates itself: when a new version is out, a button appears in the notch and installs it after verifying the signature.

> **Requires** macOS 14 Sonoma or later. Built for Macs with a notch; on other Macs it draws a simulated one at the top of the screen (not extensively tested).

<br />

## Private by design

Caspr reads your sessions and files **on your Mac** and sends them nowhere. The only network connections are:

| Connection | Why | Can be turned off |
| :-- | :-- | :-- |
| GitHub | Check for and download updates | Settings → About |
| Spotify cover URL | The cover image Spotify already provides | n/a |
| iTunes public search | Cover for streamed Apple Music tracks (title and artist only) | Settings → General |
| cursor.com | Your Cursor plan usage, using your own Cursor session; off by default | Settings → Cursor |

Permissions are requested the first time you use each feature, never at launch, and every feature keeps working if you say no.

<br />

## FAQ

**Is Caspr free?** Yes. Download it and use it.

**Do I need Claude Code, Cursor or Codex?** None of them individually. Caspr shows the tools you have; the music, timers, tray and the rest work on their own.

**Does Caspr see my code?** Caspr reads session activity (prompts, replies, tool calls) locally to show it to you. Nothing leaves your Mac except the connections listed above.

**Will it break my Claude Code, Cursor or Codex setup?** Connecting is optional, additive and reversible. Caspr shows exactly what it will add, makes a backup first, and only ever removes its own entries.

**Is the source code available?** No. This repository contains the signed builds and documentation.

**Something is wrong or missing.** Open an [issue](https://github.com/0x-Crisbanks/Caspr/issues) and tell me what you saw.

<br />

<div align="center">

**[Download Caspr](https://github.com/0x-Crisbanks/Caspr/releases/latest)** · Made by [Crisbanks](https://github.com/0x-Crisbanks)

<sub>© 2026 Crisbanks. All rights reserved. Free for personal use; redistribution and reverse engineering are not permitted.</sub>

</div>
