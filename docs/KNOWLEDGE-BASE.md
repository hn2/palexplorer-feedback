# Palexplorer — Knowledge Base for Testers

What each part of the ecosystem does, and what is solid or rough in the beta.
Scenarios to try are in [TEST-SCENARIOS.md](TEST-SCENARIOS.md).

## The pieces

**PAL/3** is the transport the apps use to talk to each other: device to
device over UDP, with end-to-end encryption and post-quantum key exchange.
Testers do not use it directly; every transfer, browse and stream in the
desktop app, command-line tool and mobile app runs over it.

**Desktop app (Windows)** is the main way to use Palexplorer: choose files and
folders, decide who gets access, browse what others share with you, and
stream music and video.

**Command-line tool (`pal`)** does the same things from a terminal and is meant
for everyone, not only developers. It ships inside the desktop app (Help →
Command Line). The npm package `pal-explorer-cli` is published less often and
can be older than the desktop app, so use the desktop app's copy when versions
differ.

**Web** covers the account area on palexplorer.com and an in-browser player
for streams.

**Mobile (Android)** browses and streams from your own computers and from pals.
Early build, shared on request in Discord. iOS is not available yet.

## Core ideas

- **Identity**: a key pair created on your device, protected by a 24-word recovery phrase. One identity can be used on several of your own devices.
- **Pals**: people you have added. Added by invite link, QR code, @handle, or automatically when on the same local network.
- **Shares**: files or folders you offer. Each share can go to any combination of people and groups, with an expiry date, a download limit and an optional password. Private shares are end-to-end encrypted; public shares are not.
- **Machine share and own devices**: browse your own other computers without setting up shares one by one.
- **Streaming**: play music and video from a pal's share without downloading it first. Local-network streaming is free; streaming over the internet is a planned paid feature.
- **Optional account features**: @handle lookup and sign-in with email or an online account. The core works without them.

## Solid and rough

| Area | State |
|---|---|
| Windows install, identity, pals on the same network | Solid |
| Private and public shares, expiry, download limits, passwords | Solid |
| Transfers between devices on different networks | Mostly solid; speed varies by network type, the most useful area to test |
| Resume after a dropped connection | Solid; edge cases welcome |
| Local-network streaming (music, video, radio and TV stations) | Solid |
| Web player | Works; segment caching issues are known |
| Mobile (Android) | Early; browsing screens need the most testing |
| Command-line tool | Solid; the npm package can lag behind the desktop app |
| macOS, Linux, servers, iOS | Not available yet |

## Known issues

Open issues that are already tracked do not need a new report, but extra
detail on them helps. Check the existing issues in this repository first.

- Windows may show a SmartScreen warning on first run.
- A transfer can pause when a computer goes to sleep; it resumes when the device wakes.
- Connecting over restrictive networks (some corporate firewalls, strict mobile carriers) can fall back to a slower path.

## What not to share publicly

Recovery phrases, private keys, private share links, tokens, and anything
personal. Use the private route in [../SECURITY.md](../SECURITY.md).
