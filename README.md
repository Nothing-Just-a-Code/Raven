<div align="center">

<img src="https://i.ibb.co/TqrPMyJm/i-Raven-Logo.png" alt="Raven Download Manager" width="800" />

**A modern download manager for Windows.**

Fast. Reliable. Built for people who download things.

[![Latest Release](https://img.shields.io/github/v/release/Nothing-Just-a-Code/Raven?style=flat-square)](https://github.com/Nothing-Just-a-Code/Raven/releases/latest)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue?style=flat-square)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-lightgrey?style=flat-square)]()

</div>

---

## Overview

Raven is a download manager that accelerates transfers through multi-threaded downloading, resumes cleanly after interruptions, and integrates directly with your browser. It handles everything from a single file to a queue of hundreds without slowing down.

It runs quietly in the system tray, captures downloads from Firefox, and keeps everything organized by category. Nothing intrusive. No ads. No telemetry. Just a fast, reliable downloader.

---

## Features

### Speed and Reliability

- **Multi-threaded downloads** — splits files into parallel connections for maximum speed
- **Crash-safe resume** — picks up exactly where it left off after a restart, power loss, or crash
- **Smart retry** — handles transient network errors automatically with exponential backoff
- **Adaptive connection tuning** — learns the optimal connection count per server

### Browser Integration

- **Firefoxe** — captures downloads directly from the browser
- **Right-click menu** — "Download with Raven" on any link, video, or image
- **Inline button** — a small R button next to downloadable links
- **Session transfer** — cookies, referrer, and headers carried from the browser so gated files work

### YouTube Downloads

- **Video + audio** — downloads both tracks and merges them into a single MP4
- **Configurable** — enable only if you want it; FFmpeg installed on demand

### User Experience

- **System tray** — runs in the background, stays out of your way
- **Modern interface** — clean design with light and dark themes
- **Notifications** — Windows toasts on completion with inline actions
- **Categories** — automatic organization by file type (Video, Music, Compressed, Documents, Programs)
- **Scheduler** — queue downloads to start at a specific time
- **Clipboard monitor** — detects copied URLs and offers to download
- **Queue management** — control concurrency, priority, and per-host limits

### Automation

- **Command-line support** — queue downloads from scripts or other applications
- **Incremental updates** — the app updates itself efficiently by downloading only changed files

---

## Screenshots

<div align="center">

| Main Window | Download Dialog |
|:---:|:---:|
| *placeholder* | *placeholder* |

| Settings | Update Available |
|:---:|:---:|
| *placeholder* | *placeholder* |

</div>

> Replace the placeholder images above with real screenshots before publishing.

---

## Installation

### Requirements

- Windows 10 (version 2004 or later) or Windows 11
- 64-bit processor
- ~150 MB of disk space

### Steps

1. Download the latest `RavenSetup.exe` from the [Releases page](https://github.com/Nothing-Just-a-Code/Raven/releases/latest).
2. Run the installer and follow the prompts.
3. Optionally install the browser extension during setup (recommended).
4. Launch Raven from the Start Menu or system tray.

Raven installs to `C:\Program Files\Raven\`. Settings and data live in `%AppData%\Raven\`.

### Browser Extension

The installer offers to install the Firefox extension automatically. For manual installation:

- **Firefox** — the signed `.xpi` file is bundled with the installer under `extensions\`. Double-click it or drag it into Firefox.
- **Chrome, Edge, Brave** — coming soon.

---

## First Run

On first launch, Raven:

1. Creates its data folder at `%AppData%\Raven\`
2. Runs database migrations
3. Registers the native messaging host for your browsers
4. Detects available categories and default save folders

You'll see the main window with an empty downloads list. Start a download by:

- Clicking the **+** button in the ribbon
- Right-clicking any link in your browser and choosing **Download with Raven**
- Copying a URL — Raven will offer to download it
- Dragging a link onto the Raven window

---

## Configuration

Raven ships with sensible defaults. Everything is configurable from **Settings** (ribbon menu or tray icon).

| Section | What you can change |
|---|---|
| **Downloads** | Connection count, buffer size, retry attempts, global speed limit |
| **Queue** | Max concurrent downloads, per-host limits |
| **Categories** | Save folder for each file type |
| **YouTube** | Enable/disable the feature, install or remove FFmpeg |
| **Behavior** | Startup, tray, clipboard, desktop shortcuts |
| **Advanced** | User agent, log level, update channel |

Settings are stored at `%AppData%\Raven\user-settings.json`.

---

## Updates

Raven checks for updates automatically on startup. When a new version is available, a dialog shows the release notes and total download size. Only the files that changed are downloaded — typically a few hundred kilobytes rather than the full installer.

You can disable automatic checks in **Settings → Advanced**, or trigger a manual check at any time.

---

## Data and Privacy

- **No telemetry.** Raven does not collect or transmit any data about your usage.
- **No analytics.** No third-party services are contacted except for update checks and downloads you initiate.
- **Local only.** All settings, history, and credentials are stored on your machine.
- **Encrypted cookies.** Browser session data used for downloads is encrypted with Windows DPAPI.

See [PRIVACY.md](PRIVACY.md) for full details.

---

## Roadmap

| Status | Feature |
|:---:|:---|
| ✅ | Multi-threaded downloads with resume |
| ✅ | Firefox browser integration |
| ✅ | YouTube downloads with audio merging |
| ✅ | Incremental auto-update |
| 🔄 | Site grabber |
| 🔄 | Download scheduler |
| 📋 | Cross-device sync |

---

## Reporting Issues

Found a bug? Please open an [issue](https://github.com/Nothing-Just-a-Code/Raven/issues) with:

- A clear title and description
- Steps to reproduce
- Expected vs. actual behavior
- Raven version (visible in **About**)
- Windows version

For feature requests, describe the use case — not just the feature.

---

## License

Raven is released under the [Apache License 2.0](LICENSE).

You are free to use, modify, and redistribute the software under the terms of the license. The software is provided without warranty.

---

<div align="center">

**Made by NJAC**

[Report Bug](https://github.com/Nothing-Just-a-Code/Raven/issues) · [Request Feature](https://github.com/Nothing-Just-a-Code/Raven/issues) · [Releases](https://github.com/Nothing-Just-a-Code/Raven/releases)

</div>
