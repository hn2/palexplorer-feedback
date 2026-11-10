# Palexplorer — Beta Feedback

This repository is the public home for beta testing of the whole Palexplorer
ecosystem: the PAL/3 protocol, the desktop app, the command-line tool, the web
experience and the mobile app. It contains no source code — it is an issue
tracker plus testing guides.

Palexplorer is file discovery, sharing and streaming with full control.
Product site: https://palexplorer.com

## Join the conversation

**Discord:** https://discord.gg/VrCcGmNJ8Q

| Channel | Used for |
|---|---|
| `#announcements` | New beta builds and known issues |
| `#bug-reports` | Quick bug reports, before or instead of a GitHub issue |
| `#feature-requests` | Ideas and wishes |
| `#general` | Questions, setup help, showing what you built |

## What can be tested

| Surface | Status in the beta | How to get it |
|---|---|---|
| Desktop app (Windows) | Released, updates itself | https://palexplorer.com/download |
| Command-line tool (`pal`) | Included with the desktop app (Help → Command Line); the npm package can lag behind, so prefer the desktop install | See [docs/KNOWLEDGE-BASE.md](docs/KNOWLEDGE-BASE.md) |
| PAL/3 protocol (device-to-device transport) | Used by the desktop app, the command-line tool and mobile | Test it through those, see scenarios L and M |
| Web | Account area and the in-browser player on palexplorer.com | https://palexplorer.com |
| Mobile (Android) | Early build, shared on request in Discord | Ask in `#general` |
| macOS, Linux, headless servers, iOS | Coming; not testable yet | — |

## Before you start

- [docs/KNOWLEDGE-BASE.md](docs/KNOWLEDGE-BASE.md) — what each part does, what is solid and what is still rough.
- [docs/TEST-SCENARIOS.md](docs/TEST-SCENARIOS.md) — step-by-step scenarios per surface. Pick one area, use it for real, report what breaks or confuses you.
- Two devices make the most useful test: a second computer, a phone, or a friend on another network.

## Reporting

1. Quick report: post in `#bug-reports` on Discord.
2. Tracked report: open a GitHub issue here and choose a template — Bug report, Feature request, UX feedback or Scenario result.
3. Finished a scenario without problems? A short "Scenario result" issue saying what you tried and on which setup is just as valuable as a bug.

Please include:

1. Steps to reproduce
2. Expected versus actual behavior
3. Environment: operating system, app version (Help → About), and for network problems the kind of connection on both sides (same network, different networks, mobile hotspot, VPN, corporate network)
4. Screenshots or logs, after checking they contain no private information

Do not post recovery phrases, private keys, share links to private files, access tokens or personal data in public places. Security and privacy reports go through the private route in [SECURITY.md](SECURITY.md).

## What the beta is for

- Whether setup works the first time on ordinary home and office networks.
- Whether transfers and streaming hold up on slow, flaky and restricted connections.
- Whether the wording and layout make sense without explanation.
- Whether two or more devices under one identity stay in step.

Feedback is read by the developer directly. Replies usually arrive within a day.
