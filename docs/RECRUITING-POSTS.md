# Beta tester recruiting — post drafts

Rules for every post: say the developer is the poster, describe what exists
today, list the caveats, invite criticism, link the feedback repo and Discord.
No unshipped claims. Check each community's self-promotion rules first, and
answer comments quickly in the first hours.

Links used in every post:
- Feedback repo and guides: https://github.com/hn2/palexplorer-feedback
- Discord: https://discord.gg/VrCcGmNJ8Q
- Download: https://palexplorer.com/download

## Short version (BetaList, Product Hunt, Peerlist, Uneed, AlternativeTo)

**Name:** Palexplorer
**Tagline:** File discovery, sharing and streaming with full control
**Description:** Palexplorer shares files and folders directly between devices with per-share access controls (people and groups, expiry, download limits, password), end-to-end encryption for private shares, and streaming of music and video. It runs as a Windows desktop app, a command-line tool and an early Android app, over a new post-quantum device-to-device transport called PAL/3. The beta is open to everyone; testing guides and scenarios are in the feedback repository.

## Reddit — r/selfhosted, r/DataHoarder

**Title:** Beta testers wanted: device-to-device file sharing and streaming with access controls (desktop, command line, Android early build)

Solo developer here. Palexplorer lets you share files and folders directly between your devices and with other people: per-share expiry, download limits, passwords, groups, end-to-end encryption for private shares, and streaming of music and video from a share without downloading first. Local-network streaming is free; internet streaming is planned as a paid option.

What I am asking for: install it on two devices, ideally on different networks, move real files, and tell me what fails. Large transfers, flaky Wi-Fi, VPNs, phone hotspots and workplace networks are the most useful tests.

Available now: Windows desktop app, command-line tool (shipped inside the app), early Android build on request. Coming: macOS, Linux, headless servers. Windows may show a SmartScreen warning on first run. The source is not public; the transport protocol is documented.

Test scenarios, known issues and how to report: https://github.com/hn2/palexplorer-feedback — quick chat and bug reports on Discord: https://discord.gg/VrCcGmNJ8Q

## Reddit — r/privacy

**Title:** Looking for people to poke holes in a device-to-device file sharing app with post-quantum encryption

Palexplorer creates an identity as a key pair on your device, protected by a 24-word recovery phrase. Private shares are end-to-end encrypted; public shares are not, and the app says so. The PAL/3 transport combines X25519 with ML-KEM-768 for key exchange and Ed25519 with ML-DSA-65 for signatures. Peers see each other's IP address, as in any direct connection; a relay option exists for hostile networks.

I would value threat-model criticism as much as bug reports. Protocol documentation and test scenarios are linked below. Security findings should go through the private route in the repository's SECURITY.md, not public issues.

https://github.com/hn2/palexplorer-feedback — https://discord.gg/VrCcGmNJ8Q

## Reddit — r/SideProject, r/alphaandbetatesting, r/betatests

**Title:** Palexplorer beta: file sharing and streaming between your own devices and friends

Same text as the r/selfhosted post, shortened to three paragraphs, with the tester-and-feedback links first.

## Hacker News (PAL/3 only, after the WAN speed fix is on main)

**Title:** Show HN: PAL/3 – post-quantum, device-to-device transport for file sharing and streaming

**First comment:** Say what PAL/3 is (UDP, hybrid X25519 + ML-KEM-768, Ed25519 + ML-DSA-65, session resumption, path-MTU discovery, connectivity ladder from direct IPv6 to relay). State what is measured and what is not. Link the feedback repo for scenario L and M testers. Stay in the thread for the first three hours.

## Communities (Discord servers, Slack groups, Indie Hackers, Lobsters)

Post the short version, adapted to the room's rules, in the channel meant for projects or testing. Ask a moderator first where self-promotion is restricted.

## Per-channel tracking

Use a reference tag on the download link per channel (for example `?ref=reddit-selfhosted`) so sign-ups can be compared. Record each post, date, link and reply count in a row below.

| Date | Channel | Link | Notes |
|---|---|---|---|
