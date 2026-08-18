# Arpeggi

An iOS client for OpenSubsonic and Navidrome servers, built in SwiftUI.

## What's this app about?

NOTE: Issues created by AI that are long winded, blocks of text may be closed without reading them.

Arpeggi is a solo developer project which I started as a way to learn iOS and Swift development back in 2023. I work on it in my free time. I wanted a player that was as close to the Apple Music app experience as possible. It is not easy to recreate Apple's interfaces, but I have given it my best shot. Everything has been achieved through trial and error and the occasional brainwave, I've read countless books on SwiftUI, SwiftData, followed tutorials, Hacking with Swift. While the App has added more and more features over the past while, I am still trying to keep everything as simplified as possible. A lot of the direction for features has come from feedback from people using it day to day. Thank you to all who have tested and provided feedback!

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

Arpeggi is currently in beta through TestFlight and in the App Store.

[Join the beta](https://testflight.apple.com/join/LDWqgjAs) · [App Store](https://apps.apple.com/it/app/arpeggi/id6503619183?l=en-GB)

## Roadmap

- CrossFade
- iCloud Sync
- watchOS
- tvOS
- macOS

## Known Issues

Some issues that I am aware of that currently don't have a fix. 

- Streaming RAW FLAC/OPUS files can sometimes go out of sync with the progress bar. This is due to AVQueuePlayer needing a timing key which is not possible to provide when streaming. Downloaded or Cached FLAC/OPUS files do not have this issue. This issue does not occur when transcoding to OPUS.
- Occasionally the lock screen image can fail to update when changing songs from the lock screen. I have narrowed this down to being a concurrency issue but I haven't found a fix yet.

## Recommended Settings

The following App and Navidrome settings are recommended for best compatibility

In Navidrome make sure:
- Transcoding Cache and Image Cache are enabled with decent allowances
- Also that the correct permissions are set for Music Folders.

In the app it is recommended to:
- turn on pre-cache. This will help provide consistent playback in spotty network conditions.
- Transcode on Cellular to OPUS 160kbps (iOS 26+). OPUS tends to maintain gapless playback.
- Transcode downloads to OPUS 160kbps
- Apple Music Style Player View for the most authentic Apple Experience.

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

**Is the app open source? Can I contribute?**
The App is currently closed source. The reasons for this are that I use this app as a learning tool for myself. Also for my mental sanity, I am not prepared or have any experience with maintaining open source projects.

## AI Usage

I write and maintain all of the code myself. I occasionally use AI tools for code review and catching bugs. There are no AI agents writing or committing code on their own. Every part of the app is meticulously understood and written by hand.

## Privacy

Arpeggi does not collect analytics or usage data. All communication happens directly between the app and the server you connect it to.

## Built With

- SwiftUI
- SwiftData
- Swift 6.2
- AVQueuePlayer
- a mix of architectures where needed. I learned about SwiftUI Architectures from Nick Sarno's advanced architecture video series. I can't recommend it highly enough. 

