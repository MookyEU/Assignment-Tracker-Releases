# Assignment Tracker — downloads

Releases for [Assignment Tracker](https://github.com/MookyEU/Assignment-Tracker),
a local-first coursework tracker for Windows. It reads a Brightspace (D2L)
calendar feed and sorts your work by how soon it is due.

No account, no server, nothing sent anywhere.

## Download

**[Latest release →](../../releases/latest)**

There is one file on it, `…_x64-setup.exe`, and that is the one you want. It is
large — about 950 MB — because it carries everything the app needs, including
the language model that rewrites each posting in plainer words. You install it
once and it works offline immediately, with nothing left to fetch.

## Updating

You will not need to come back here. The app checks once each time it starts and
offers the update in **Settings → Updates**; it takes about 10 MB and a few
seconds.

Every update is signed, and the app refuses anything not carrying a signature it
recognises.

## Windows may warn you

The installer is not signed with a code-signing certificate, so SmartScreen may
say the publisher is unknown. **More info → Run anyway.** If you would rather
not, that is a reasonable thing to decide.

## `updates/`

That folder is how the app updates itself. It holds `latest.json`, which says
what the current version is, and the update package the app downloads when it
finds one.

**It is not a download.** The package is the same program with the model and the
Windows WebView2 runtime left out, because a machine that already has the app
already has both — which is how an update is 10 MB instead of 950. Installed on
its own it produces a broken app: no model, and on a clean machine no way to draw
its own window.

Take the installer from the releases page instead.

## Source

The source lives in a separate, private repository. This one holds release files
and nothing else.
