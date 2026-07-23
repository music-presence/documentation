---
title: Media Player Setup
icon: lucide/music
hide:
    - tags
tags:
    - Setup
---

<style>
[data-md-color-scheme="slate"] img[src*="/_static/media/media-controls-"] {
    border-radius: 1em;
    border: 1px solid #222;
}
[data-md-color-scheme="default"] img[src*="/_static/media/media-controls-"] {
    border-radius: 1em;
    border: 1px solid #ccc;
}
th:nth-child(1) {
    min-width: 0 !important;
}
th:nth-child(2), td:not([colspan="2"]) + td:nth-child(2) {
    padding-left: 0 !important;
}
table {
    border-radius: 1em !important;
}
mark.pill:not([data-md-highlight]) {
    border-radius: 1em;
    padding: 1pt 6pt;
    margin-right: .25em;
    margin-left: -.25em;
}
[data-md-color-scheme="slate"] mark.pill:not([data-md-highlight]) {
    background-color: #323232 !important;
    color: #bbb;
}
[data-md-color-scheme="default"] mark.pill:not([data-md-highlight]) {
    background-color: #eaeaea !important;
    color: #444;
    font-weight: 500;
}
.tabbed-set-table-next {
    display: none;
}
.tabbed-set-table-next + .tabbed-set .tabbed-content {
    padding: 0;
}
.tabbed-set-table-next + .tabbed-set .tabbed-content .md-typeset__scrollwrap {
    margin: 0;
}
.tabbed-set-table-next + .tabbed-set .tabbed-content .md-typeset__table {
    display: flex;
    padding: 0;
    margin-top: .25em;
    border-top: 0;
    margin-bottom: 0;
}
.tabbed-set-table-next + .tabbed-set table {
    border: 0;
    border-radius: 0 !important;
}
.tabbed-set-table-next + .tabbed-set table thead {
    display: none;
}
.tabbed-set-table-next + .tabbed-set table {
    background-color: transparent;
}
.tabbed-set-table-next + .tabbed-set table tbody tr:hover {
    background-color: transparent;
    box-shadow: none;
}
.tabbed-set-table-next + .tabbed-set table tbody tr:nth-of-type(1) td {
    border-top: 0;
}
img[src*="/logo-128.png"] {
    min-width: 23px;
    width: 23px;
}
</style>

This guide covers how to set up Music Presence with your media player.

## Supported media players

Check the list of [supported media players](../media-players/index.md){ target="_blank" }, to know if your media player is supported.

If your media player is not listed, then follow the [instructions](#adding-support-for-a-media-player) below on how you can help with adding support for it to Music Presence.

## Minimum requirements

For Music Presence to detect media playback, other applications must report information about what media they are playing to your operating system. You can see if other applications do this, by checking the [media control interface](#media-control-interfaces) of your device.

If the media does not show up, refer to the [next section](#media-player-configuration). Make sure you are playing something, paused media may not always appear.

<h2 id="media-control-interfaces" class="anchor-target">Media control interfaces</h2>

=== ":fontawesome-brands-windows:&ensp;Windows"

    ==Windows 11=={ .pill } Click on the section on the right of your task bar that is highlighted in the screenshot to see whether an application reports what it is playing.
    
    ![Windows 11 media controls](/_static/media/media-controls-win-win11-dark.png#only-dark)
    ![Windows 11 media controls](/_static/media/media-controls-win-win11-light.png#only-light)

    ==Windows 10=={ .pill } Press a media key on your keyboard to see the information overlay.

    ![Windows 10 media overlay](/_static/media/media-controls-win-win10-dark.png#only-dark)
    ![Windows 10 media overlay](/_static/media/media-controls-win-win10-light.png#only-light)

    If you don't have media keys on your keyboard, try [debugging your media player](#debugging-a-media-player).

=== ":fontawesome-brands-apple:&ensp;Mac"

    Click on the icon in the menu bar that is shown in the screenshot to see whether an application reports what it is playing.

    ![macOS media controls](/_static/media/media-controls-mac-dark.png#only-dark)
    ![macOS media controls](/_static/media/media-controls-mac-light.png#only-light)

=== ":custom-linux:&ensp;Linux"

    !!! warning "TODO"

## Media player configuration

Depending on the media player you are using, you may need to install a plugin, run a helper program or enable a specific setting. Refer to the table below for instructions.

Make sure to select the correct operating system by clicking on the respective tab.

<div class="tabbed-set-table-next"></div>

=== ":fontawesome-brands-windows:&ensp;Windows"

    | Player || Instructions |
    |-|-|-|
    | ![](https://live.musicpresence.app/v3/icons/aimp/logo-128.png) | AIMP | Install the [`Windows Media Control`](https://www.aimp.ru/forum/index.php?topic=63341){ target="_blank" } plugin. Alternatively you can run the newer [`AIMP SMTC`](https://github.com/NimiGames68/aimp-smtc){ target="_blank" } helper program. Compared to the plugin, this helper program also reports the album name and track duration. |
    | ![](https://live.musicpresence.app/v3/icons/feishin/logo-128.png) | Feishin | Switch to the web backend, then go to `Settings` -> `Hotkeys` and enable `Media Session`. Note that Music Presence can only identify Feishin as mpv, when you use the mpv backend. |
    | ![](https://live.musicpresence.app/v3/icons/foobar2000/logo-128.png) | foobar2000 | Install the [`foo_mediacontrol`](https://github.com/ungive/foo_mediacontrol){ target="_blank" } plugin. Click [Releases](https://github.com/ungive/foo_mediacontrol/releases/latest){ target="_blank" } to find all downloads. Alternatively you can also enable `Windows Universal Volume Control` under advanced preferences, but foobar2000 will not report the album name or the track duration then. |
    | ![](https://live.musicpresence.app/v3/icons/itunes/logo-128.png) | iTunes | You need to run the [`iTunes-SMTC`](https://github.com/thewizrd/iTunes-SMTC){ target="_blank" } helper program alongside Music Presence. You can download it from the [Releases](https://github.com/thewizrd/iTunes-SMTC/releases/latest){ target="_blank" } or the <nobr>[Windows Store](https://apps.microsoft.com/detail/9nq3d21qt8ml){ target="_blank" } |
    | ![](https://live.musicpresence.app/v3/icons/mpc-hc/logo-128.png) | MPC-HC | Under `Player` -> `User Interface` -> `Windows Integration` enable `Control via Windows UI (SMTC)`. If you don't have this setting, make sure to use this updated fork of MPC-HC: <nobr>[clsid2/mpc-hc](https://github.com/clsid2/mpc-hc){ target="_blank" }</nobr>. |
    | ![](https://live.musicpresence.app/v3/icons/mpv/logo-128.png) | mpv | mpv must either be run with the `--media-controls=yes` command line flag or by setting `media-controls=yes` in `mpv.conf`. |
    | ![](https://live.musicpresence.app/v3/icons/musicbee/logo-128.png) | MusicBee | Install the [`mb_MediaControl`](https://github.com/HenryPDT/mb_MediaControl){ target="_blank" } plugin. Click [Releases](https://github.com/HenryPDT/mb_MediaControl/releases/latest){ target="_blank" } to find all downloads. After importing it into MusicBee, make sure the information window shows version 1.0.4 or newer. |
    | ![](https://live.musicpresence.app/v3/icons/netease-cloud-music/logo-128.png) | NetEase Cloud Music /<br> 网易云音乐 | In the application settings go to `系統` ("System") and make sure that `开启SMTC` ("Enable SMTC") is checked. This is required for the player to report what music it is playing. |
    | ![](https://live.musicpresence.app/v3/icons/vlc/logo-128.png) | VLC |  Install the [`vlc-win10smtc`](https://github.com/spmn/vlc-win10smtc){ target="_blank" } plugin. |
    | ![](https://live.musicpresence.app/v3/icons/winamp/logo-128.png) | Winamp | Install the [`gen_smtc`](https://github.com/NanMetal/gen_smtc){ target="_blank" } plugin. |
    | ![](https://live.musicpresence.app/v3/icons/windows-media-player-legacy/logo-128.png) | Windows Media Player Legacy | [`Windows-Media-Player-Discord-RPC`](https://github.com/T0biasCZe/Windows-Media-Player-Discord-RPC){ target="_blank" } is a 2-in-1 program that allows Windows Media Player to be detected by Music Presence while it's running and also provides its own Discord RPC implementation. |

=== ":fontawesome-brands-apple:&ensp;Mac"

    | Player || Instructions |
    |-|-|-|
    | ![](https://live.musicpresence.app/v3/icons/itunes/logo-128.png) | iTunes | iTunes is not supported on Mac. Use Apple Music instead. |
    | ![](https://live.musicpresence.app/v3/icons/mpv/logo-128.png) | mpv | You must install and run mpv using an `.app` bundle. mpv cannot be detected when run as a plain binary from the command line. |

=== ":custom-linux:&ensp;Linux"

    | Player || Instructions |
    |-|-|-|
    | ![](https://live.musicpresence.app/v3/icons/musicbee/logo-128.png) | MusicBee | If you run MusicBee under Wine, install the [`mb_MPRISBee`](https://github.com/UrbanCMC/mb_MPRISBee){ target="_blank" } plugin. |

## Media players with known issues

Some media players are known to not report what they are playing or are known to report inaccurate information. If you use one of these players, consider [contacting the developer](#support-message-template) of that media player, so they can improve its integration with the system.

<div class="tabbed-set-table-next"></div>

=== ":fontawesome-brands-windows:&ensp;Windows"

    | Player || Instructions |
    |-|-|-|
    | ![](https://live.musicpresence.app/v3/icons/amazon-music/logo-128.png) | <nobr class="desktop">Amazon Music</nobr> | Amazon Music does not report any album cover image and sometimes reports very inaccurate or scrambled song metadata. |
    | ![](https://live.musicpresence.app/v3/icons/qobuz/logo-128.png) | Qobuz | Qobuz does not report what it is playing anymore since a past update. You can try [downgrading](https://github.com/ungive/discord-music-presence/issues/244#issuecomment-3556269025){ target="_blank" } or [patching](https://github.com/TubaApollo/qobuz-smtc){ target="_blank" } it (this may violate Qobuz's Terms of Services, use at your own risk). |
    | ![](https://live.musicpresence.app/v3/icons/tidal/logo-128.png) | TIDAL | TIDAL does not report the album name of the playing song. If the [TIDAL API](../discord-presence/music-apis.md) is enabled for [Discord Presence](../discord-presence/intro.md), the album name can only be guessed and may sometimes be incorrect. |
    | ![](https://live.musicpresence.app/v3/icons/windows-media-player/logo-128.png) | Windows Media Player | Windows Media Player sometimes does not report any album cover image and tends to stop reporting what it is playing after playing a few songs. |

=== ":fontawesome-brands-apple:&ensp;Mac"

    | Player || Instructions |
    |-|-|-|
    | ![](https://live.musicpresence.app/v3/icons/qobuz/logo-128.png) | Qobuz | Qobuz does not report what it is playing on Mac. For compatibility with Music Presence you will need to use a third-party player like [QBZ](https://github.com/vicrodh/qbz). |

=== ":custom-linux:&ensp;Linux"

    | Player || Instructions |
    |-|-|-|
    | ![](https://live.musicpresence.app/v3/icons/strawberry/logo-128.png) | Strawberry | If you installed Strawberry via [Flatpak](https://flathub.org/apps/org.strawberrymusicplayer.strawberry){ target="_blank" }, then album covers may not show up in your Discord status. This is a [known bug](https://github.com/flathub/org.strawberrymusicplayer.strawberry/issues/133){ target="_blank" } in the Flatpak-version of Strawberry. You need to run Strawberry natively instead, until the bug is fixed. |

## Websites and browser support

On Windows and Mac, you currently need to use the desktop application for the media player or streaming service you are using, as websites are not supported yet. The following table contains a list of supported official and third-party desktop applications.

!!! info "Support for websites is coming soon"

    Click "Subscribe" in the sidebar of [this GitHub issue](https://github.com/ungive/discord-music-presence/issues/5){ target="_blank" } to receive e-mail updates. Meanwhile, you can already install and test the [browser extension](https://github.com/ungive/media-control-extension#readme){ target="_blank" } that will enable browser support later.

<div class="tabbed-set-table-next"></div>

=== ":fontawesome-brands-windows:&ensp;Windows"

    | Player || Instructions |
    |-|-|-|
    | ![](https://live.musicpresence.app/v3/icons/apple-music/logo-128.png) | <nobr class="desktop">Apple Music</nobr> | Install the Apple Music app from the [Microsoft Store](https://apps.microsoft.com/detail/9pfhdd62mxs1){ target="_blank" }. |
    | ![](https://live.musicpresence.app/v3/icons/soundcloud/logo-128.png) | SoundCloud | Install the SoundCloud app from the [Microsoft Store](https://apps.microsoft.com/detail/9n5qr3kw6cmc){ target="_blank" }. |
    | ![](https://live.musicpresence.app/v3/icons/youtube-music/logo-128.png) | <nobr class="desktop">YouTube Music</nobr> | ==Third-party=={ .pill } [Pear Desktop](https://github.com/pear-devs/pear-desktop){ target="_blank" } works well with Music Presence. |
    | <nobr>![](https://live.musicpresence.app/v3/icons/spotify/logo-128.png)&ensp;![](https://live.musicpresence.app/v3/icons/tidal/logo-128.png)&ensp;![](https://live.musicpresence.app/v3/icons/amazon-music/logo-128.png)&ensp;![](https://live.musicpresence.app/v3/icons/deezer/logo-128.png)</nobr> { colspan=2 } | For these and other streaming services, download the desktop application from the official website. |

=== ":fontawesome-brands-apple:&ensp;Mac"

    | Player || Instructions |
    |-|-|-|
    | ![](https://live.musicpresence.app/v3/icons/apple-music/logo-128.png) | <nobr class="desktop">Apple Music</nobr> | Install the Apple Music app from the [App Store](https://apps.apple.com/app/apple-music/id1108187390){ target="_blank" }. |
    | ![](https://live.musicpresence.app/v3/icons/soundcloud/logo-128.png) | SoundCloud | ==Third-party=={ .pill } [Nuage](https://github.com/lbrndnr/nuage-macos){ target="_blank" } is a third-party client for SoundCloud. |
    | ![](https://live.musicpresence.app/v3/icons/youtube-music/logo-128.png) | <nobr class="desktop">YouTube Music</nobr> | ==Third-party=={ .pill } [Pear Desktop](https://github.com/pear-devs/pear-desktop){ target="_blank" } works well with Music Presence. |
    | <nobr>![](https://live.musicpresence.app/v3/icons/spotify/logo-128.png)&ensp;![](https://live.musicpresence.app/v3/icons/tidal/logo-128.png)&ensp;![](https://live.musicpresence.app/v3/icons/amazon-music/logo-128.png)&ensp;![](https://live.musicpresence.app/v3/icons/deezer/logo-128.png)</nobr> { colspan=2 } | For these and other streaming services, download the desktop application from the official website. |

=== ":custom-linux:&ensp;Linux"

    | Player || Instructions |
    |-|-|-|
    | :custom-firefox:{ style="--md-icon-size: 2em; display: inline;" } | Firefox | Websites and streaming services can be detected when opened in Firefox or a Firefox-based browser, like LibreWolf or Zen Browser, if they are [supported](../media-players/index.md). |
    | ![](https://live.musicpresence.app/v3/icons/apple-music/logo-128.png) | <nobr class="desktop">Apple Music</nobr> | ==Third-party=={ .pill } [Sidra](https://github.com/wimpysworld/sidra){ target="_blank" } is a third-party client for Apple Music. |
    | ![](https://live.musicpresence.app/v3/icons/deezer/logo-128.png) | Deezer | ==Third-party=={ .pill } [Deezer for Linux](https://github.com/aunetx/deezer-linux){ target="_blank" } is a third-party client for Deezer. |
    | ![](https://live.musicpresence.app/v3/icons/qobuz/logo-128.png) | Qobuz | ==Third-party=={ .pill } [QBZ](https://github.com/vicrodh/qbz){ target="_blank" } is a third-party client for Qobuz. Unlike the official app for Windows and Mac, this client is fully compatible with Music Presence. |
    | ![](https://live.musicpresence.app/v3/icons/spotify/logo-128.png) | Spotify | Download Spotify from [spotify.com/download/linux](https://www.spotify.com/download/linux){ target="_blank" }. |
    | ![](https://live.musicpresence.app/v3/icons/tidal/logo-128.png) | TIDAL | ==Third-party=={ .pill } [Tidal Hi-Fi](https://github.com/Mastermindzh/tidal-hifi){ target="_blank" } and [High Tide](https://github.com/Nokse22/high-tide) are third-party clients for TIDAL. |
    | ![](https://live.musicpresence.app/v3/icons/youtube-music/logo-128.png) | <nobr class="desktop">YouTube Music</nobr> | ==Third-party=={ .pill } [Pear Desktop](https://github.com/pear-devs/pear-desktop){ target="_blank" } is a third-party client for YouTube Music. |

## Multimedia and radio players

[Discord Presence](../discord-presence/intro.md) is disabled by default for multimedia players, radio players and any other media players that may report personal information or details about your location. You have to enable these explicitly, read [Player Controls](../discord-presence/player-controls.md) to find out how.

## Adding support for a media player

If your media player is not detected, despite fulfilling the [minimum requirements](#minimum-requirements), support may not have been added yet. Follow these instructions to help:

1. Open the [Music Presence](./install.md){ target="_blank" } app
2. Play something with your media player and let it play
3. Click the <nobr>:custom-musicpresence: Music Presence</nobr> icon in your <span class="os-dependent-text" data-windows="tray menu" data-mac="menu bar" data-linux="system tray">tray menu</span>. [Where is this?](./install.md#usage){ target="_blank" }
4. Click on "Help" and then on "Submit detected media players"
5. A GitHub issue opens. Submit it and you'll receive a reply within at most a few days

If you do not have a GitHub account, you can join the [Discord server](https://go.musicpresence.app/discord-invite) instead and leave a message that contains the URL that opened in your browser.

---

## Resources

### Debugging a media player

!!! warning "TODO"

### Support message template

!!! warning "TODO"

### Information for developers

!!! warning "TODO"

---

!!! warning "TODO"
    Explain which media players need additional setup and which don't. Also explain that browser support is coming soon, but the browser extension that is needed can already be tested in terms of website compatibility.

    Contribution guide: https://github.com/music-presence/documentation#contributing

    Show the table of contents, if it's helpful.

!!! note "Content notes"
    - https://github.com/ungive/discord-music-presence/blob/master/documentation/supported-media-players.md#required-plugins-and-helper-programs
    - Mention plugins and helper programs
    - Mention that most players should work out of the box
    - Mention that some players need to be enabled explicitly for the Discord status
    - Mention that all players of interested have to be enabled explicitly for Scrobbling (add this once Scrobbling has released, not before)
    - Mention that browser support is coming soon (link to the corresponding page that mentions the browser extension)
    - Link to the supported players page
    - Explain how to add support for a media player (perhaps make a separate page for that?)
    - GitHub issue to subscribe to for e-mail notifications for browser support: https://github.com/ungive/discord-music-presence/issues/5
    - Firefox Add-on page: https://addons.mozilla.org/en-US/firefox/addon/media-control-extension/
    - Chrome Web Store page: TBD
    - Browser extension source code: https://github.com/ungive/media-control-extension/
    - Is there another way to show the Windows 10 media overlay than with media keys on the keyboard only?
    - Explain how to even know, if a media player is detected. Not everyone might know that it will show up in the Music Presence tray menu, when media is playing

<script type="module" src="/_static/scripts/page/select-and-sync-os.js"></script>
