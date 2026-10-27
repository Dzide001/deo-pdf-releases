# Deo PDF

A PDF reader and editor for Android. Everything it does happens on your device.

**There is no public release yet.** This page is where the download will appear
when there is one. Watch the repository to be told when that happens — the app
itself cannot tell you, for the reason given under *Updates* below.

What the first release will contain, and what is known to be limited about it,
is written up in [CHANGELOG.md](CHANGELOG.md).

## Download

Releases are listed on the [Releases page](../../releases). Each one has an
`app-release.apk` attached, along with its SHA-256 checksum.

## Check what you downloaded

An app installed this way does not come through a store, so nothing checks the
file for you. Compare the checksum before installing:

```bash
# macOS / Linux
shasum -a 256 app-release.apk

# Windows (PowerShell)
Get-FileHash app-release.apk -Algorithm SHA256
```

It should match the checksum published with that release. If it does not, do not
install it.

## Install

1. Open the `.apk` on your device.
2. Android will say the file came from an unknown source. Allow installation for
   whichever app you opened it from — your browser or file manager.
3. Install.

You may see a warning from Play Protect because the app was not downloaded from
the Play Store. That is what the checksum above is for.

## Requirements

- Android 8.0 (Oreo) or newer
- About 120 MB of free space
- A camera, only if you want to scan paper into a PDF

## Updates

**The app will never tell you an update exists.** It has no internet
permission — it cannot reach the network at all, which is also why the privacy
policy below is as short as it is. The trade is deliberate: nothing leaves your
device, and nothing checks for new versions either.

To find out about a new version, watch this repository or check the Releases
page.

## Privacy

Deo PDF collects nothing, sends nothing, and has no way to do either. No
accounts, no analytics, no advertising, no crash reporting, no tracking. The
only permission it requests is the camera, and only for scanning paper.

The full policy is in [PRIVACY.md](PRIVACY.md).

Questions about it go to **deodevs001@gmail.com**.

## Open source components

Deo PDF is built on permissively licensed libraries. Every one of them is
acknowledged in the app, with its full licence text, under **Settings → Open
source licences**.

## Source

The source is not public. This repository exists only to distribute the built
app and its release notes.

© Deo. All rights reserved.
