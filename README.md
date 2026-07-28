# Arpeggi

An iOS client for OpenSubsonic and Navidrome servers, built entirely in SwiftUI.

## What's this app about?

Arpeggi is a solo developer project which I started the app as a demo project to learn iOS and Swift development back in 2023, and I keep working on it in my free time. I wanted a player that was as close to the Apple Music app experience as possible. It is not easy as a layman to recreate Apple's interfaces, but I have given it my best shot. Everything has been achieved by trial and error and the occasional brainwave. While the App has added more features, I am still trying to keep everything as simplified as possible. A lot of the direction for features has come from feedback from people using it day to day. Thank you to all who have tested and provided feedback for.

## Features

The app is written completely in SwiftUI with SwiftData as the backend cache. The music player is built on AVQueuePlayer with a custom queue implementation. My goals as a developer are to keep it intuitive and optimised for performance.

- Gapless playback for supported formats (AAC, FLAC, ALAC, Opus)
- Transcoding
- ReplayGain
- Continuous queue system
- Offline mode
- Multiple servers
- Multiple music folder support
- Concurrent background downloads
- Offline scrobble caching with timestamps
- Create and edit playlists
- Song and artist station mode
- Customisable design
- CarPlay

## Requirements

- iOS 17 or later
- A Navidrome server or any OpenSubsonic compatible server

## Getting Started

1. Install the app
2. Enter your server URL and login on first launch
3. Arpeggi does a light initial sync of some data then everything is ready

You can add more servers or music folders later from Settings.

## Download

Arpeggi is currently in beta through TestFlight.

[Join the beta][(link)](https://testflight.apple.com/join/LDWqgjAs) · [App Store]([link](https://apps.apple.com/it/app/arpeggi/id6503619183?l=en-GB))

## Roadmap

- CrossFade
- iCloud Sync
- watchOS
- tvOS
- macOS

## Known Issues



## FAQ

**Which servers does Arpeggi support?**
Any OpenSubsonic compliant server. It's built and tested primarily against Navidrome, there may be some quirks with other server types that I haven't been able to test properly.

**Is Arpeggi free?**
Arpeggi is free.

**Does it work offline?**
Yes. Downloaded songs play without a connection, and any scrobbles made offline are cached with their original timestamp and synced once you're back online. Playlists can be created offline.

**Why isn't gapless playback available for every format?**
This is dictated by AVQueuePlayer. As far as I have tested, currently supported formats are AAC, FLAC, ALAC, and Opus. MP3 format is not supported

**Can I use more than one server or music library?**
Yes, Arpeggi supports multiple servers and multiple music folders per server.

**Is my data sent anywhere besides my own server?**
No. Arpeggi only communicates with the server you connect it to.

**How do I report a bug or request a feature?**
[Describe your preferred channel: GitHub Issues, Discussions, TestFlight feedback, Discord, etc.]

**Is the app open source? Can I contribute?**
The App is currently closed source. The reasons for this are that I use this app as a learning tool for myself. Also for my mental sanity, I am not prepared or have any experience with maintaining open source projects.

## AI Usage

I write and maintain all of the code myself. I occasionally use AI tools for code review and catching bugs. There are no AI agents writing or committing code on their own. Every part of the app is meticulously understood and written by hand.

## Feedback

Bug reports, feature requests, and general feedback are welcome. [Point people to the right channel: Issues, Discussions, email, Discord, etc.]

## Privacy

Arpeggi does not collect analytics or usage data. All communication happens directly between the app and the server you connect it to.

## Built With

- SwiftUI
- SwiftData
- AVQueuePlayer
- a mix of architectures where needed. I learned about SwiftUI Architectures from Nick Sarno's advanced architecture video series. I can't recommend it highly enough. 

