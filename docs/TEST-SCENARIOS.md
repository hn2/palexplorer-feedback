# Palexplorer — Tester Scenarios

Concrete things to try, grouped by area. Pick one, use it for real, and report
what breaks or confuses you. You do not need to complete everything.

For each scenario: **Goal** → **Steps** → **Working looks like**. If what you
see differs, report it (see [../README.md](../README.md)). A short report that
something worked is also useful — use the "Scenario result" template.

Setup that helps: two devices (two computers, or computer plus phone), ideally
on different networks for scenarios L and M.

---

## A. Install and first run (desktop)

**Goal:** first launch works without help.

1. Download from https://palexplorer.com/download and install.
2. Open the app and create an identity.
3. Write down the recovery phrase, then confirm it when asked.

**Working looks like:** install completes (a SmartScreen warning is expected); the app opens without errors; identity creation finishes in under a minute; nothing in the first-run flow is a dead end.

## B. Identity and recovery

**Goal:** the recovery phrase restores an identity.

1. On a second device (or after removing the app data on the first), choose to recover.
2. Enter the 24-word phrase.

**Working looks like:** the same identity appears with the same pals; a wrong word is rejected with a clear message.

## C. Adding pals

**Goal:** every way of adding a pal works.

1. Create an invite link (and QR code) on one device; add it on the other.
2. On two computers on the same network, use nearby discovery.
3. Optional: register an @handle and add by handle.

**Working looks like:** the pal appears on both sides; the display name is correct; removing the pal works.

## D. Sharing files and folders

**Goal:** access controls do what they say.

1. Share a file with one pal, with an expiry date of a few minutes.
2. Share a folder with a download limit of 1.
3. Share with a password; try a wrong one, then the right one.
4. Share to a group of two pals.
5. Revoke a share while the other side is downloading.

**Working looks like:** access stops after expiry; the limit is enforced; the wrong password is refused; revocation takes effect; the receiving side sees a clear reason when blocked.

## E. Receiving and resuming

**Goal:** downloads finish and survive interruption.

1. Download a file of at least 1 GB.
2. Midway, switch Wi-Fi off and on, or close the app and reopen it.
3. Download a folder with many small files.

**Working looks like:** the download resumes without starting over; the finished file opens and matches the original; progress and speed readouts stay sensible.

## F. Folder sync and changes

**Goal:** edits propagate efficiently.

1. Share a large folder, download it, then change one file on the source.
2. Fetch the update.

**Working looks like:** only the changed data moves; unchanged files are left alone.

## G. Streaming

**Goal:** playback starts quickly and stays smooth.

1. Stream a song and then a video from a pal on the same network.
2. Seek forward and backward.
3. Open one of the demo radio or TV stations if listed in `#announcements`.

**Working looks like:** playback begins within a few seconds; seeking does not restart the stream; no audio or video stutter on a normal home network.

## H. Own devices and machine share

**Goal:** your own computers show up without per-folder setup.

1. Use the same identity on two of your computers.
2. Browse the second computer from the first.

**Working looks like:** the other computer is labelled with its own name; browsing, opening and copying files work; a computer that is off is shown as offline, not as an error.

## I. Command-line tool

**Goal:** the terminal path works end to end.

1. Open Help → Command Line in the desktop app (or install the tool) and run `pal status`.
2. `pal share <folder>` with a pal, then `pal serve`.
3. On the other device: `pal browse <pal>:<share>` and download a file.
4. `pal transfers` while a download runs.

**Working looks like:** commands finish with readable output and clear errors; the command-line and desktop app agree on shares and pals.

## J. Web

**Goal:** the web side is consistent with the apps.

1. Sign in on palexplorer.com.
2. Open the player for a stream and play something.
3. Check that your account, devices and shares match the desktop app.

**Working looks like:** sign-in completes without loops; the player starts and seeks; pages read clearly on a phone as well.

## K. Mobile (Android)

**Goal:** the phone reaches your computers and streams.

1. Ask for the build in Discord `#general` and install it.
2. Sign in with the identity from your computer.
3. Browse a computer's share; play a song and a video.

**Working looks like:** your computers and shares appear; playback works over Wi-Fi; the app survives going to the background and coming back.

## L. Different networks and awkward connections

**Goal:** find where connections fail. This is the most valuable area.

Try each pairing and note which work, and how fast:

1. Both devices on the same home network.
2. Home network and a phone hotspot.
3. Two different home internet providers.
4. A computer behind a VPN.
5. A workplace or school network.
6. Wi-Fi with a weak signal, or moving between Wi-Fi and mobile data.

**Working looks like:** connections form on every pairing or fail with a clear message; transfer speed is close to the slower side's link speed; the connection indicator describes what is happening.

## M. Large transfers

**Goal:** stability under load.

1. Send a single file of 10 GB or more between two networks.
2. Send a folder with tens of thousands of small files.
3. Run two transfers at once and one stream.

**Working looks like:** no crashes, no memory growth that slows the computer, speeds hold steady, the final data matches. Please report sizes and times even when it works.

## N. Updates

**Goal:** the app updates itself safely.

1. Leave the app running when a new build is announced in `#announcements`.
2. Accept the update.

**Working looks like:** the update downloads, installs and relaunches with identity, pals and shares intact.
