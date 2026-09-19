# Assignment Tracker | downloads

Releases for **Assignment Tracker**, a local-first coursework tracker for
**Windows and macOS**. It reads a Brightspace (D2L) calendar feed and sorts your
work by how soon it is due.

No account, no server, nothing sent anywhere.

## Download

**[Latest release →](../../releases/latest)**

| | file | size |
|---|---|---|
| Windows | `AssignmentTracker_<version>_x64-setup.exe` | about 210 MB |
| macOS (Apple silicon) | `AssignmentTracker_<version>_macOS.dmg` | about 7 MB |

Take the one for your system. Both are the same application and the same
version.

The Windows installer is the larger of the two because it carries Microsoft's
WebView2 runtime, which macOS does not need — the machine may not have it, and
without it the app has no way to draw its own window. Installing it once, from
the file, means the install works on a machine that has never been online.

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

**It is not a download.** The package leaves out the WebView2 runtime, because a
machine that already has the app already has it — which is why an update is a
few megabytes rather than a few hundred. Installed on its own it produces a
broken app on a clean machine, with no way to draw its own window.

Take the installer from the releases page instead.

## Source

Not public. This repository holds release files and nothing else.
