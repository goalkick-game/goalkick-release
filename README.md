# GoalKick

**A fast arcade football game — cross-platform online 1v1, 48 national teams,
penalty shootouts.** Windows, Linux, Android (macOS and iOS in progress).

> ### ⚠️ This is an ALPHA release
> GoalKick is under active development. Expect rough edges, and expect online
> matches to require **everyone on the same version** — an alpha build only
> plays online against a build from the same release. Things will break and
> change. This is the place to tell us when they do.

## Download

Get the latest build from the [**Releases**](../../releases/latest) page:

| Platform | File | How to run |
|----------|------|------------|
| **Windows** | `goalkick-windows.zip` | Unzip anywhere, run `goalkick.exe`. Nothing to install. |
| **Linux** | `goalkick-linux.tar.gz` | Extract, run `goalkick/goalkick.x86_64`. |
| **macOS** | `goalkick-mac-silicon.dmg` (Apple silicon) / `goalkick-mac-intel.dmg` (Intel) | Open the disk image, drag to Applications. Right-click → Open the first time. |
| **Android** | `goalkick-android.apk` | Enable "install from this source" on first install. |

Because this is an alpha, **online play needs both players on the same
release**. Update all your devices together before playing online.

## Reporting a problem

Open an [**issue**](../../issues/new) here. The most useful bug reports say:

- which platforms were involved (e.g. *Windows host vs Android*),
- what you did and what happened,
- and — for an online match — roughly when it happened, so we can match it to
  the server logs.

---

## Contributing a team

GoalKick's teams are **community-editable**. If your country, club, or a team
you care about is missing (or its kit is wrong), you can add or fix it and open
a pull request. **Approved teams are merged and ship in the next release of the
game.**

You do not need to write any code or build the game. You need the **GoalKick
Editor** and a GitHub account.

### 1. Get the editor

Download the **GoalKick Editor** for your platform from the
[Releases](../../releases/latest) page:

- **Windows** — `GoalKickEditor-windows-x86_64.exe`
- **Linux** — `GoalKickEditor-linux-x86_64` (`chmod +x` it first)
- **macOS** — `GoalKickEditor-macos-arm64.zip` (Apple silicon; unzip, right-click → Open the first time)

It is a standalone app: no Python, no installation.

### 2. Make the team

Open the editor and point it at a copy of this repository's `data/` folder
(or start a fresh bundle — the editor writes a self-contained team folder).
For each team you set:

- **Name, short name (3 letters), and league/zone.**
- **Colours and two kits** — home and away. The editor draws the shirts.
- **A crest/logo** and, for a national team, a **flag** (the editor has a flag
  painter and a shirt-logo importer built in).
- **A squad** — 16+ players with positions and simple ratings. The editor can
  generate a plausible squad you then tune.

Every team is one folder of plain text and images under `data/teams/<slug>/`.
The editor is the friendly way to write that folder; you can also read a few of
the existing ones to see the shape.

### 3. Open a pull request

Fork this repo, drop your `data/teams/<slug>/` folder in, and open a PR. Tell
us in the description what you added and, if the team is real, where the crest
and kit designs came from (see **Legal** below). A maintainer reviews it, and
once merged it goes into the next game release — you'll see it in the download.

### Legal — please read before contributing art

We can only accept teams whose artwork is safe to ship. **Do not upload
copyrighted club crests, sponsor logos, or official kit designs you do not have
the right to distribute.** Real clubs' badges and kit graphics are trademarked.

What is safe:

- **National flags** — a flag's *design* is not anyone's private property; a
  particular drawing of it can be, so draw your own (the editor's flag painter
  produces original renderings). The shipped 48 national flags are drawn from
  each flag's public geometry for exactly this reason.
- **Original crests and kits** you designed yourself, or artwork explicitly
  released under a permissive/open licence (say which, in the PR).
- **Names and squads** — player and team names are facts, not artwork.

What is not:

- A real club's badge, wordmark, or sponsor logos.
- A scan or trace of an official kit.
- Anything you found online without a licence that permits redistribution.

If in doubt, make an original crest in the editor — a distinctive mark in the
team's colours reads as that team in-game, and it is unambiguously yours to
give. By opening a PR you confirm the artwork is yours to contribute, and that you
grant the project the right to include it in GoalKick's releases.

---

## What GoalKick is

A modern port of a deterministic football simulation to the Godot engine, with
a C++ core. The same simulation runs bit-identically on every platform, which
is what makes cross-platform online lockstep possible. The game, the team
editor, and the master server are developed by David Zambrano and Juan Fajardo,
supported by [BitPointer](https://bitpointer.co). Learn more at
[goalkick.co](https://goalkick.co).
