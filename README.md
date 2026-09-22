<img src="sybl.png" alt="" width="72" align="left">

# Sybl | downloads

**A coursework tracker for Windows and macOS.** It reads your Brightspace (D2L)
calendar and sorts your work by how soon it is due. Your coursework lives on your
own machine.

<br clear="left">

## Download

Current version: **1.0.8**

| | download | size |
|---|---|---|
| **Windows** (10 or 11, 64-bit) | **[Sybl_1.0.8_x64-setup.exe](https://github.com/MookyEU/Assignment-Tracker-Releases/releases/download/v1.0.8/Sybl_1.0.8_x64-setup.exe)** | 6 MB |
| **macOS** (Apple silicon) | **[Sybl_1.0.8_macOS.dmg](https://github.com/MookyEU/Assignment-Tracker-Releases/releases/download/v1.0.8/Sybl_1.0.8_macOS.dmg)** | 8 MB |

Take the one for your system. Both are the same application, built from the same
source at the same version. The [latest release page](../../releases/latest) has
the notes and the checksums, and is always the newest even if the two links above
have fallen behind.

**Apple silicon only on the Mac.** That is any Mac with an M1 chip or later,
which is every Mac sold since late 2020. There is no Intel build.

## Before you install

**The first time you open it, it asks you to sign in with your email.** A window
of its own opens instead of the app: your email address, a code sent to it, and
then your calendar address. There is no way past that step, so have your email to
hand. Signing in is what lets your work follow you from one computer to another.

Then it asks for your Brightspace calendar address, which you copy from
Brightspace itself: **Calendar → Subscribe**, and copy the link it gives you.

**Neither installer is signed with a certificate**, because those cost several
hundred dollars a year, so each system will say so once:

- **Windows** shows SmartScreen saying the publisher is unknown. Choose **More
  info**, then **Run anyway**.
- **macOS** refuses a double-click. **Control-click** Sybl in Applications,
  choose **Open**, then **Open** again in the dialog. You do this once, on the
  first open only.

On Windows the app draws its window with Microsoft's WebView2 runtime. Windows 11
includes it and almost every Windows 10 machine has it already; on a machine
without it, the installer fetches it.

## What is on your machine, and what is not

Your coursework, your notes and your ticks are kept on your own machine, in a
database it keeps ten daily backups of. What your calendar says never leaves it.

**When you sign in**, and only then, these go to the account so your other
computer can have them: your email address, what you ticked, what you typed (your
notes and the names of items you added by hand), and the address of your
calendar. Not what your calendar says, and nothing about grades. It is stored in
Canada. The sign-in emails pass through Twilio SendGrid in the United States,
which sees your address and the code and nothing else.

From **Settings** you can download everything the account holds, sign a device
out, or delete the account and everything in it.

## Updating

You will not need to come back here. The app checks each time it starts and
offers the update in **Settings**. It takes a few seconds and about 7 MB.

Every update is signed, and the app refuses anything not carrying a signature it
recognises.

## Older versions

Every release is on the [releases page](../../releases). Note that **a newer
version's data cannot be opened by an older one**: going back means restoring one
of the app's own daily backups, not just installing an older file.

## `updates/`

That folder is how the app updates itself. It holds the manifests saying what the
current version is on each platform, and the macOS packages the Mac build
fetches. **Nothing in it is a download**; take the installer from the link above.

## About this repository

It holds release files and nothing else. The source is not public. The repository
is still called *Assignment-Tracker-Releases*: the app was renamed to Sybl at
1.0.8, and the address stayed as it was so that every installed copy keeps
finding its updates.
