# Assignment Tracker | downloads

Releases for **Assignment Tracker**, a local-first coursework tracker for
**Windows and macOS**. It reads a Brightspace (D2L) calendar feed and sorts your
work by how soon it is due.

No account, no server, nothing sent anywhere.

## Download

**[Latest release →](../../releases/latest)**

| | file | size |
|---|---|---|
| Windows | `AssignmentTracker_<version>_x64-setup.exe` | about 6 MB |
| macOS (Apple silicon) | `AssignmentTracker_<version>_macOS.dmg` | about 7 MB |

Take the one for your system. Both are the same application and the same
version.

The app draws its window with Microsoft's WebView2 runtime on Windows. Windows 11
includes it, and almost every Windows 10 machine already has it. On the rare
machine without it the installer fetches it for you, which needs a working
internet connection — the same connection the app needs to read your calendar.

## Updating

You will not need to come back here. The app checks once each time it starts and
offers the update in **Settings → Updates**. It takes a few seconds and a few
megabytes: about 4 MB on Windows, about 6 MB on macOS.

Every update is signed, and the app refuses anything not carrying a signature it
recognises.

## Windows may warn you

The installer is not signed with a code-signing certificate, so SmartScreen may
say the publisher is unknown. **More info → Run anyway.** A certificate that
removes this warning costs several hundred dollars a year.

## `updates/`

That folder is how the app updates itself. It holds the manifest saying what the
current version is, and the update package the app downloads when it finds one.

**It is not a download.** The package assumes the machine already runs the app,
so it does nothing about the WebView2 runtime. Installed on its own, on a machine
that does not have one, it produces an app that cannot draw its own window.

Take the installer from the releases page instead.

## Source

Not public. This repository holds release files and nothing else.
