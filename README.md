# Arpeggi

An iOS client for OpenSubsonic and Navidrome servers, built entirely in SwiftUI.

## About

Arpeggi is a solo project. I started the app as a demo project to learn iOS and Swift development back in 2023, and I keep working on it in my free time. I wanted a player that is as close to the Apple Music app as possible. It is not easy as a layman to recreate Apple's interfaces, but I have given it my best shot. Everything has been achieved by trial and error and the occasional brainwave. A lot of the direction for features has come from feedback from people using it day to day.

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

[Join the beta](link) · [Landing page](link)

## Roadmap

A rough idea of what's coming next. This list will change as things get built or reprioritised.

- [Add your current roadmap items here]

## FAQ

**Which servers does Arpeggi support?**
Any OpenSubsonic compliant server. It's built and tested primarily against Navidrome, there may be some quirks with other server types that I haven't been able to test properly.

**Is Arpeggi free?**
[Describe your freemium plan here, e.g. the app is free with a one time purchase to unlock certain features.]

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
[State your current stance on this.]

## AI Usage

I write and maintain all of the code myself. I occasionally use AI tools for code review and catching bugs, the same way I'd use a linter or ask someone to look over a diff. There are no AI agents writing or committing code on their own. Every part of the app is understood and written by hand.

## Feedback

Bug reports, feature requests, and general feedback are welcome. [Point people to the right channel: Issues, Discussions, email, Discord, etc.]

## Privacy

Arpeggi does not collect analytics or usage data. All communication happens directly between the app and the server you connect it to.

## Built With

- SwiftUI
- SwiftData
- AVQueuePlayer

## License

[State your license, or note that the project is currently closed source.]
