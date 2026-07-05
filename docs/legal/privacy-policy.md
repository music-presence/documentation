---
title: Privacy Policy
icon: lucide/user-lock
hide:
    - footer
search:
    exclude: true
---

<!-- Workaround until https://github.com/zensical/backlog/issues/120 is implemented. -->
<style>
.md-content__button {
    display: none;
}
</style>

<!--

Instructions on updating this Privacy Policy:
- Make sure to document any new additions with each new version
- Make sure that links and link descriptions to sections are up-to-date
- Make sure to update the "Last updated" date at the bottom of the document

TODO:
- Document the e-mail provider that processes and sends the user their license (add section "5.9 E-Mail Providers"). Update the section link in section "4.2 Scrobbling" accordingly

-->

# Privacy Policy

Effective date: 7 July 2026

Welcome to the Music Presence Privacy Policy. This is where we describe how we handle your data, which is data that is collected when you use our Services and information that is directly linked or can be linked to you. It applies to the data that we process when you interact with websites, applications and services listed in section [2. Scope](#2-scope).

## 1. Definitions

In this Policy, the following terms have the meanings this section ascribes those terms:

"We", "us", or "our" refers to Jonas van den Berg, the author of Music Presence. For more information refer to section [7. Data Controller](#7-data-controller);

"Music Presence" or "Software" means the desktop application called "Music Presence" authored by Jonas van den Berg;

"Discord Rich Presence" or "Discord RPC" means the process of sharing information about some of your current activities on your Discord user profile in real-time. In the context of the Software this means showing some or all Media Metadata that the Software collects on your Discord profile. See section [3.1 Media Metadata](#31-media-metadata) and section [4.1 Discord Rich Presence](#41-discord-rich-presence);

"Scrobbling" means the process of recording all or some of the Media Metadata of live music playback on a computer device, waiting until a sufficient amount of it has played and logging the associated Media Metadata by uploading it (or some of it) to one or more Scrobbling services. See section [3.1 Media Metadata](#31-media-metadata) and section [4.2 Scrobbling](#42-scrobbling);

"Services" means all of the services listed in section [2. Scope](#2-scope);

Furthermore, the following sections define additional terms that are used throughout this Policy which are not defined in this section to avoid repetition or ambiguity.

## 2. Scope

This Policy covers your use of the following Services:

- The most recent version of the Music Presence desktop application (the "Software")
- Our main website at https://musicpresence.app
- This documentation website at https://docs.musicpresence.app
- Our licensing server and website at https://licensing.musicpresence.app

This Policy does not cover your use of any preview or beta versions of the Software (e.g. versions similar to `v1.2.3-beta.4`). If you are concerned about your privacy when using a preview or beta version of the Software, please contact us (see [11. Contact](#11-contact)) or wait until the next stable release of the Software.

## 3. Data We Collect

We collect data to provide the functionality of the Software and our Services and to make maintance of the Software and operation of our Services as sustainable as possible.

Each of the sections that follow outline one class of data for a specific aspect of the Software and our Services. Each section briefly touches upon the designated purpose of each class of data and links to the relevant section that further documents the use of the collected data.

### 3.1 Media Metadata

Certain data is collected by the Software from the device the Software is running on, collectively called Media Metadata. This Media Metadata includes any available information about currently playing media on the device, such as:

- The title of the media (the music or video title)
- Though uncommon, potentially the file name of the media that is playing
- The name of the person or persons that created the media (usually the artists)
- The name of the album (the album name)
- The name of the person or persons that created the album (the album artists)
- The name of the person or persons that composed the media (the composers)
- The duration of the song or video (or its length)
- The current playback state (playing, paused or stopped)
- The current playback position (how much of the media has been played)
- The exact time at which the playback position was last changed (position timestamp)
- The repeat mode of the song (whether the song or playlist is on repeat)
- The shuffle mode of the playlist
- The cover image of the media (this can be album artwork or a small thumbnail of a single frame of the media, determined by the media playback application or media source)
- A URL to a resource that provides the album artwork or a small thumbnail. When self-hosting a media server, this may contain the domain and/or IP address of your media server

This data is collected for the following purposes:

- To provide "Discord Rich Presence" functionality, see [4.1 Discord Rich Presence](#41-discord-rich-presence)
- To provide "Scrobbling" functionality, see [4.2 Scrobbling](#42-scrobbling)

By default (if at all) and without any Software configuration changes, only Media Metadata from media players is collected that are known to only or almost exclusively play music from publicly known or otherwise well-known artists. We are committed to only recording Media Metadata by default that is free of personal information about you.

Despite our efforts, it is your responsibility to ensure that none of the above Media Metadata contains personal data. We do not explicitly or willingly collect any personal data as part of Media Metadata, but due to the nature of the Software and the fact that media sources such as video players and multimedia players are supported by the Software, it can happen that some Media Metadata might e.g. include your name, the name of a relative in a personal home video or the name of someone else you are in some way related to. The Software has no control over this and has no means to differentiate personal Media Metadata from non-personal Media Metadata.

It is your responsibility to:

1. Be aware when media is being played that contains personal data in its Media Metadata.
2. Disable the application that plays media with personal data in its Media Metadata via the controls the Software offers or make sure it is already disabled.
3. To terminate the Software and make sure it is not running anymore, if any Media Metadata contains sensitive personal data.

### 3.2 Player Data

The Software collects information about all applications that are playing media on your device and that are reporting that media to your device's operating system (Player Data). This includes any of the following data:

- The application's executable file name and/or full filesystem path
- The application's [bundle identifier](https://support.apple.com/guide/deployment/get-the-bundle-id-for-a-mac-app-dep0af2cd611) (on macOS)
- The application's [app user model ID](https://learn.microsoft.com/en-us/windows/configuration/store/find-aumid) (on Windows)
- The application's [D-Bus service name](https://en.wikipedia.org/wiki/D-Bus) (on Linux)
- The application's [D-Bus media player identity](https://specifications.freedesktop.org/mpris/latest/Media_Player.html#Property:Identity) (on Linux)
- The application's display name

This data is collected for the following purposes:

- For "Discord Rich Presence" functionality, by first identifying the media player you are using and then showing its publicly known name on your Discord profile. The derived data is only shared as long as Discord Rich Presence functionality is enabled in the Software's settings. See [4.1 Discord Rich Presence](#41-discord-rich-presence)
- To improve the compatibility of the Software with existing and future desktop media players, see [4.4 Player Compatibility](#44-player-compatibility). This data does not leave your device without your explicit submission of that data

### 3.3 Scrobbling Data

The Software collects certain information you enter to use Scrobbling features of the Software (Scrobbling Data):

- The username of Scrobbling service accounts you use
- The password and/or token of Scrobbling service accounts you enter
- The types of Scrobbling services and self-hosted Scrobbling targets you use
- The internet address (domain name, IP addresses, port, protocol and/or URL path) of self-hosted Scrobbling targets you use
- The session key a Scrobbling service or self-hosted Scrobbling target provides after you connect your account which is used to authenticate with the service

This data is collected for the following purposes:

- To provide "Scrobbling" functionality, see [4.2 Scrobbling](#42-scrobbling)

### 3.4 Analytics Metrics

The Software collects certain anonymous metrics (Analytics Metrics):

- The version of the Software you use
- Your operating system (Windows, Mac or Linux) and its architecture
- Your current time zone (for vague region information) and local time
- Your app settings regarding automatic app updates, app update pop-ups, app changelog pop-ups and in-app news
- Your interaction with in-app news, e.g. whether you look at them or not, how long you look at them and which buttons or links you click
- Anonymized automatic update errors

These metrics are either sent at most once a day or for real-time events, like automatic update errors and interaction with in-app news, the relevant information is sent whenever such an event occurs.

This data is collected for the following purposes:

- For Software analytics, see [4.6 Analytics](#46-analytics)

Our websites collect anonymized visitor and usage data when you visit and interact with one of our websites, such as the following data:

- The time of your visit and which elements on the page you interact with
- Your current time zone (for vague region information) and local time
- Which browser you use and any UTM or referral URL parameters

This data is collected for the following purposes:

- For website analytics, see [4.6 Analytics](#46-analytics)

For all analytics purposes we use the privacy-friendly analytics service [Simple Analytics](https://www.simpleanalytics.com/) to collect this data. Simple Analytics will receive your IP address, but does not store it, as outlined in their own policies. Refer to section [5.8 Simple Analytics](#58-simple-analytics) for more information.

### 3.5 Abuse Prevention Data

Under specific circumstances the Software collects information to prevent abuse (Abuse Prevention Data), specifically abuse related to starting multiple Scrobbling free trials or sharing your personal Scrobbling license with other individuals.

At the time of starting a Scrobbling free trial, to ensure that you cannot start another free trial now or in the near future, we collect and store the following data ("Scrobbling Free Trial Abuse Prevention Data"):

- The types of Scrobbling services and self-hosted Scrobbling targets you use
- A hash of the username of Scrobbling service accounts you use
- Your machine identifier provided by the operating system and/or a machine hash derived from device components to recognize the same device

See [4.5 Abuse Prevention](#45-abuse-prevention) to learn how your Scrobbling service account username is hashed, how long this data is stored and why it needs to be collected to prevent abuse.

To prevent sharing of personal Scrobbling licenses with other individuals we collect the following data while you use a purchased Scrobbling license within the Software ("Scrobbling License Abuse Prevention Data"):

- A cryptographically irreversible one-way hash of the username of Scrobbling service accounts you use, the type of Scrobbling services you use and/or the internet address (domain name, IP addresses and port) of self-hosted Scrobbling targets you use

It is cryptographically infeasible for us to know which Scrobbling services and accounts you use with the Software with this data. "Cryptographically infeasible" means it would take an astronomical amount of computation time to derive the original data from the one-way hash that we collect, which is considered practically impossible. This one-way hash is created on the device the Software is running on, we never see the original data.

For more information on how this works, what cryptographic functions and key material is used, how long this data is stored and how it is used, see [4.5 Abuse Prevention](#45-abuse-prevention).

### 3.6 Donation Information

The information you enter when making a donation, e.g. your name, e-mail address and payment information is processed by the donation platform on which you enter this information. Refer to section [5.2 Donation Platforms](#55-donation-platforms) to find out which platforms we use and how your payment information is processed by these platforms. We never receive your payment information or credit card details.

On our side, we process the following data:

- Your name or nickname (the name you specified on the donation platform)
- Your e-mail address (the e-mail address you specified on the donation platform)

This data is collected for the following purposes:

- In order to recognize whether you made a donation in the past, when you contact us, e.g. when your request is about an inquiry that involves your past donation or donations

### 3.7 Payment Information

The information you enter when purchasing a Scrobbling license, e.g. your name, e-mail address and payment information is processed by our reseller [Paddle.com](https://www.paddle.com/) ("Paddle"). Refer to section [5.4.1 Paddle](#541-paddle) to find out how your payment information is processed by Paddle. We never receive your bank or credit card details.

On our side, we process the following data:

- Your name (the name you specified before or at checkout)
- Your e-mail address (the e-mail address you specified before or at checkout)

This data is collected for the following purposes:

- To provide you with a license file for your Scrobbling license, see [4.2 Scrobbling](#42-scrobbling)
- To allow you to recover a lost license file at a later time, see [4.2 Scrobbling](#42-scrobbling)

### 3.8 Website Visitor Data

When you visit any of our websites, we may collect anonymous Analytics Metrics. This is outlined in detail in section [3.4 Analytics Metrics](#34-analytics-metrics). This data is processed by [Simple Analytics](https://www.simpleanalytics.com/), see section [5.8 Simple Analytics](#58-simple-analytics) for more details.

When you visit our websites, our website hosters and other web services we use may collect data during your visit, see section [5.6 Web Services](#56-web-services) for more information. This may include, among other data, the following information (this list is not exhaustive and depends on the browser you use):

- The browser you use and the browser language
- The operating system you use
- Cookies stored in your browser
- Your device's public IP address
- The pages you visit

When you download the Software to install it on your device, you download it from [GitHub](https://github.com)'s servers and the same data collection may apply there. See [5.7 GitHub](#57-github) for more information on how GitHub processes your data when you download the Software.

When you make a donation and are directed to the donation platform from our website, from within the Software or from somewhere else, the data you enter to make that donation is processed by the respective donation platform. Refer to section [3.6 Donation Information](#36-donation-information) to find out what data is processed and section [5.5 Donation Platforms](#55-donation-platforms) to find out which donation platforms are being used.

When you make a purchase, e.g. to buy a Scrobbling license to use with the Software, the information you enter will be processed by our payment processor [Paddle.com](https://www.paddle.com/) ("Paddle"). Refer to section [3.7 Payment Information](#37-payment-information) to find out what data is being processed by us and [5.4.1 Paddle](#541-paddle) to find out how Paddle processes your data.

Avatars of people who have made a donation (small images that visually represent them) may be loaded from the donation platforms that we use when you access one of our websites. This involves a request to external servers and the above data may be sent or logged with these services as well. Refer to section [5.5 Donation Platforms](#55-donation-platforms) to find out which donation platforms are used and may receive this information.

### 3.9 Music API Data

We may also collect the following data for use with Music API Services:

- The country code of the device the Software is running on
- Music API Service credentials you enter into the Software

This data is collected for the following purposes:

- The country code of your device is sent to some or all third-party Music API Services in addition to Media Metadata in order to improve and localize search results and retrieve missing Media Metadata or repair Media Metadata. See [4.3 Music API Services](#43-music-api-services)
- Any Music API Service credentials such as "client IDs" and "client secrets" for music APIs are sent only to the respective Music API Service for authentication. See [4.3 Music API Services](#43-music-api-services)

### 3.10 Cookies

We currently do not use any cookies on our websites except functional cookies to e.g. remember preferences you set (like the site theme) for the next visit and cookies that are set by third-party providers. We do not track you with cookies.

[Paddle.com](https://www.paddle.com/) (Paddle) may set cookies when you purchase a Scrobbling license for use with the Software to e.g. remember some of the information you enter or to prevent fraud. See section [5.4.1 Paddle](#541-paddle) for more information on how Paddle processes your data, what cookies it sets and how these cookies can affect your privacy.

## 4. How We Use Your Data

This section describes how the data is used that we collect. Most, but not all, data is forwarded to third-party services and is only processed by the Software for that purpose and is not sent to or stored on our own servers. When data is sent to or stored on our servers, this is explicitly mentioned in the following sections.

### 4.1 Discord Rich Presence

The data that is collected to provide Discord Rich Presence functionality is sent to [Discord](https://discord.com/) to show a so called "Rich Presence" on the user's profile. This will display the majority of the collected data on your Discord profile. See https://docs.discord.com/developers/platform/rich-presence for more details on Discord Rich Presence.

You have the option to disable data processing by Discord by disabling Discord Rich Presence in the settings of the Software (located in the tray menu of the Software and under *Discord -> Settings* in the settings window). This will disable any data transmission to Discord.

You also have the option to customize which data is shown on your profile and how it is shown on your profile (located under *Discord -> Settings*, *Discord -> Appearance* and *Metadata* in the settings window).

To learn how Discord processes your data, see section [5.1 Discord](#51-discord).

Media Metadata may additionally be sent to Music API Services in order to retrieve more accurate and/or more complete Media Metadata for use with Discord Rich Presence. See section [4.3 Music API Services](#43-music-api-services) to learn how these Music API Services process your data and how you can control it.

Whenever necessary, we temporarily upload cover images and album artwork image data to our own servers, as Discord Rich Presence does not support uploading of raw image data, so it has to be uploaded somewhere else. The image is deleted from our servers shortly after the Discord Rich Presence disappears from your Discord profile and is never stored by us permanently. The uploaded image data may be cached on our servers temporarily.

Note that Discord may cache any uploaded cover images and album artwork images for any length of time at their own discretion. Images that are uploaded to our own servers and served by our servers are served with proper [Cache Control](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/Cache-Control) HTTP Headers to incentivize third-parties such as Discord to store these images only temporarily and for a very short time period, but Discord may choose to ignore these headers and store them for longer anyway.

You can disable uploading of cover images and album artwork in the settings of the Software (located under *Discord -> Services* in the settings window).

### 4.2 Scrobbling

The data that is collected to provide Scrobbling functionality is sent to the following Scrobbling services, depending on whether you connected your Scrobbling account in the settings of the Software (located under *Scrobbling* -> *Accounts*):

- [Last.fm](https://www.last.fm) &ndash; See section [5.2.1 Last.fm](#521-lastfm)

You have the option to disable data transmission to these Scrobbling services by logging out or deleting the respective Scrobbling account under *Scrobbling* -> *Accounts* in the settings of the Software. You also have the option to disable all media players that are enabled for Scrobbling under *Scrobbling* -> *Players* in the settings of the Software, but this will only disable data transmission for any new data. Old or outstanding data that was meant to be transmitted but was not transmitted yet may still be transmitted.

To learn how these Scrobbling services process your data, see section [5.2 Scrobbling Services](#52-scrobbling-services) and the respective subsections linked in the above list.

The Software also offers the option to connect a non-standard target server for Scrobbling ("Custom Scrobbling Target"), such as self-hosted Scrobbling servers, which are not considered central Scrobbling services. For this you usually need to enter a server address which contains information such as an internet domain, server IP, port, protocol (usually HTTPS) and/or URL path.

Any data that is collected to provide Scrobbling functionality may be sent to Custom Scrobbling Targets, should you choose to connect such a Custom Scrobbling Target under *Scrobbling* -> *Accounts* in the settings window of the Software. We make no guarantees as to how this data is processed or if it is securely encrypted during transmission, as this almost exclusively depends on the Custom Scrobbling Target's server configuration and security practices. Use Custom Scrobbling Targets at your own risk, as your use of them is not covered by this Privacy Policy.

Your name and e-mail address that you provided while purchasing a license (see [3.7 Payment Information](#37-payment-information)) are part of the Scrobbling license file that is sent to you by e-mail after you complete the purchase and are contained in a readable format in that license file. We make use of external e-mail providers in order to reliably deliver your Scrobbling license file to you, the license file and the data therein (including your name and e-mail address) are handled according to the privacy policies of those e-mail providers, see section [5.9 E-Mail Providers](#).

### 4.3 Music API Services

Media Metadata may additionally be sent to Music API Services ("API" meaning "Application Programming Interface") in order to get additional metadata that might be missing from the original Media Metadata or to repair incorrect metadata. This may include any third-party services listed under section [5.3 Music API Services](#53-music-api-services) which will process your Media Metadata according to their policies.

These Music API Services may also receive the country code of your device in order to improve and localize search results and ensure that certain music and media can be found that is only available in specific regions. You have the option to change this country code in the settings of the Software (located under *Discord* -> *Services* in the settings window), but this may impair the effectiveness of the Music API Service.

If you enter Music API credentials, such as a "client ID" and "client secret" (located under *Discord* -> *Services* in the settings window) for any of the Music API Services named in section [5.3 Music API Services](#53-music-api-services), then this data will be sent to those Music API Services for authentication. These credentials are always sent encrypted, see [6. Encryption](#6-encryption).

Generally, but not exclusively, Media Metadata is only sent to Music API Services when that Media Metadata originates from a media player application that retrieves the Media Metadata and audio stream data from the same service. In most cases this means that e.g. the Deezer API will not be contacted if you do not use Deezer or do not listen to music via Deezer.

You have the option to disable some or all Music API Services in the settings of the Software (located under *Discord -> Services* in the settings window).

To learn how these Music API Services process your data, see section [5.3 Music API Services](#53-music-api-services).

### 4.4 Player Compatibility

The Software works with a whitelist of identifiers of media player applications ("Media Player Identifier") which must be continuously expanded to support previously unsupported media players and to maintain support for existing media players that may change their Media Player Identifier with new version of the media player. This largely depends on contributions from you and the general community.

The data that is collected for Player Compatibility is sent to [GitHub](https://github.com/), but only when you actively do so via a button in the Software to "submit" detected media players or media player identifiers. This can e.g. be done via the *Help* menu in the system tray menu of the Software and will open a GitHub page in your browser where you can review the data before finally submitting it. Once you submit it, this data will go public for anyone else to see.

To learn how this data is processed by GitHub, see [5.7 GitHub](#57-github).

After you submitted this data, we process some or all of it to provide the functionality of the Software and improve compatibility with more media players.

### 4.5 Abuse Prevention

The data that is collected while you use a purchased Scrobbling license within the Software ("Scrobbling License Abuse Prevention Data") is sent to our servers and stored for a period of up to 90 days to prevent sharing of personal Scrobbling licenses with other individuals and to enforce the limitations of a purchased Scrobbling license as described in the [Scrobbling License Terms](./scrobbling-license-terms.md). This data is only used to prevent abuse and for no other purposes. It is deleted after the 90-day period.

None of this data is readable to us. All Scrobbling License Abuse Prevention Data is securely [pseudonymized](https://en.wikipedia.org/wiki/Pseudonymization) by hashing it with the [HMAC-SHA256](https://en.wikipedia.org/wiki/HMAC) cryptographic one-way hash function where at least 256 bits of the private secret in your Scrobbling license file are used as key material. This key is never persistently stored on our servers which makes it cryptographically infeasible for us to know which Scrobbling services and accounts you use. This is by design. See section [5.3 License File Contents](./scrobbling-license-terms.md#53-license-file-contents) of the [Scrobbling License Terms](./scrobbling-license-terms.md) for more information.

From a non-technical perspective this Scrobbling License Abuse Prevention Data gives us insight only into the following information:

- How many different Scrobbling accounts you use per Scrobbling target type across all devices on which you use your Scrobbling license, e.g. whether you use one or more than one account of a Scrobbling service, without us knowing which specific service you use and without us gaining knowledge about any account names

The data that is collected when you start a Scrobbling free trial within the Software ("Scrobbling Free Trial Abuse Prevention Data") is sent to our servers and stored for a period of up to 365 days to ensure that you cannot start another free trial now or in the near future and to enforce the limitations of the Scrobbling free trial as described in the [Scrobbling License Terms](./scrobbling-license-terms.md).

Unlike Scrobbling License Abuse Prevention Data, Scrobbling Free Trial Abuse Prevention Data cannot be pseudonymized in the same way because there is no private secret or other key material available during the free trial that is guaranteed to be available for the same individual across all devices on which the Software is used.

For this reason the username of Scrobbling service accounts you use that are transmitted as part of Scrobbling Free Trial Abuse Prevention Data are only hashed with the [SHA-256](https://en.wikipedia.org/wiki/SHA-256) hash function, without any key material, so that these are not transmitted or stored in plain text. We never attempt to brute force this hash to determine which specific Scrobbling service accounts are using the free trial or have used the free trial in the past.

This data is only used by our systems to automatically detect whether you have already started a free trial in the past. We only store Scrobbling License Abuse Prevention Data for a duration of at most 365 days after which it is deleted.

Scrobbling Free Trial Abuse Prevention Data and Scrobbling License Abuse Prevention Data is never linked or correlated, even if it originates from the same device.

If you do not wish for Scrobbling Free Trial Abuse Prevention Data to be collected, but you still wish to use the Scrobbling features of the Software, you may purchase a Scrobbling license and skip the free trial (to do so go to *Scrobbling* > *License* in the settings of the software and click the button to buy a license). In order to provide free trials without risk of abuse, we unfortunately cannot get around collecting this data. If you do not wish to continue using your Scrobbling license shortly after your purchase, you may be eligible for a refund depending on your country and region, see section [7.7 Refunds](./scrobbling-license-terms.md#77-refunds) of the [Scrobbling License Terms](./scrobbling-license-terms.md).

If you believe this data collection could be improved without significantly increasing the risk of abuse, please contact us. See section [11. Contact](#11-contact) for contact details.

### 4.6 Analytics

The data that is collected for Analytics is sent to [Simple Analytics](https://www.simpleanalytics.com/). To learn how this data is processed by Simple Analytics, see [5.8 Simple Analytics](#58-simple-analytics).

## 5. Third-Parties

This section lists all third-parties with which we share your data.

Note that information such as registered business addresses or company names can change over time and may become out of date. We do our best to keep these updated, but for the most up-to-date information you are advised to visit the Privacy Policy of the respective third-party and find the information you need there.

### 5.1 Discord

Discord is a social media platform to connect and chat with other people. If you reside in the European Economic Area ("EEA"), Discord Netherlands BV is the data controller of information collected by Discord. For everyone else, Discord Inc. is the data controller.

Website: https://discord.com  
Privacy Policy: https://discord.com/privacy

### 5.2 Scrobbling Services

#### 5.2.1 Last.fm

Last.fm is a social platform and online music service to keep track and gain insight into your music listening habits, get recommendations for new music to listen to and see overlaps in your music tastes with other individuals on the platform. Last.fm is operated by Paramount Skydance Corporation ("Paramount"), the street address of Paramount's headquarters is [Paramount Skydance Corporation, 1515 Broadway, New York, NY 10036, United States](https://lei.bloomberg.com/leis/view/529900B6VAJG54Y9QF02).

Website: https://www.last.fm  
Privacy Policy: https://www.last.fm/legal/privacy

### 5.3 Music API Services

#### 5.3.1 Apple

Apple Inc. ("Apple") is an American multinational technology company headquartered in Cupertino, California, in Silicon Valley, and known for consumer electronics, software and online services. Apple also provides its Apple Music music streaming platform that also offers API access to retrieve detailed information about music and its metadata. Apple offers its services under Apple, Inc., with its headquarters located at [Apple, Inc., One Apple Park Way Cupertino California 95014, USA](https://www.creditsafe.com/business-index/en-us/company/apple-inc-us22139727).

Website: https://www.apple.com  
Privacy Policy: https://www.apple.com/legal/privacy and https://www.apple.com/legal/privacy/en-ww

#### 5.3.2 Deezer

Deezer is a music streaming platform that also offers API access to retrieve detailed information about music and its metadata. Deezer offers its services under Deezer, with its headquarters located at [Deezer, 24 Rue De Calais Paris Île-De-France 75009](https://www.creditsafe.com/business-index/en-us/company/deezer-fr35187547).

Website: https://www.deezer.com  
Privacy Policy: https://www.deezer.com/legal/personal-datas

#### 5.3.3 Spotify

Spotify is a music streaming platform that also offers API access to retrieve detailed information about music and its metadata. Spotify offers its services under Spotify AB, with its headquarters located at [Spotify AB, Regeringsgatan 19, SE-111 53 Stockholm, Sweden](https://www.creditsafe.com/business-index/en-us/company/spotify-ab-se01095139).

Website: https://www.spotify.com/about-us  
Privacy Policy: https://www.spotify.com/legal/privacy-policy

#### 5.3.4 TIDAL

TIDAL is a music streaming platform that also offers API access to retrieve detailed information about music and its metadata. TIDAL offers its services under Tidal Music AS, with registered company address at [Lakkegata 53, 0187 Oslo](https://www.creditsafe.com/business-index/en-us/company/tidal-music-as-no01203356).

Website: https://tidal.com/about  
Privacy Policy: https://tidal.com/privacy

### 5.4 Payment Processors

#### 5.4.1 Paddle

Payments are processed by our reseller Paddle.com ("Paddle"). Paddle offers its services under several entities:

- [Paddle.com Market Limited with address at Judd House, 18-29 Mora Street, London, EC1V 8BT, UK](https://www.creditsafe.com/business-index/en-us/company/paddlecom-market-limited-uk08441622)
- [Paddle.com Inc. with address at 3811 Ditmars Blvd, #1071 Astoria, New York, 11105-1803, USA](https://www.creditsafe.com/business-index/en-us/company/paddlecom-inc-us153609531)
- [Paddle Payments Limited with address at The Academy, 42 Pearse Street, Dublin 2, D02 Hv59, Ireland](https://www.creditsafe.com/business-index/en-us/company/paddle-payments-limited-ie01103212)
- [Paddle.com Canada Ltd with address at 22 Adelaide Street West, Suite 3400, Toronto, Ontario, M5H 4E3, Canada](https://www.paddle.com/legal/privacy)

For more information on how Paddle processes your data, refer to the links below. We do not get access to your bank details or credit card information.

Website: https://www.paddle.com  
Privacy Policy: https://www.paddle.com/legal/privacy  
GDPR Notice: https://www.paddle.com/legal/gdpr

### 5.5 Donation Platforms

#### 5.5.1 GitHub Sponsors

GitHub Sponsors is offered by GitHub to allow developers on the platform to receive donations from people who use the software that is created and maintained by those developers. The data you enter when making a donation via GitHub Sponsors is processed by GitHub, see [5.7 GitHub](#57-github) for more details.

More information about GitHub Sponsors: https://github.com/open-source/sponsors

#### 5.5.2 Buy Me a Coffee

Buy Me a Coffee is a platform for creators to accept support from their audience and share exclusive content. The services are provided by Publisherr Inc, a Delaware company with registered address at [505 Montgomery St Fl 10 San Francisco California 94111, USA](https://www.creditsafe.com/business-index/en-us/company/publisherr-inc-us205582075).

Website: https://buymeacoffee.com/  
Privacy Policy: https://buymeacoffee.com/privacy-policy

#### 5.5.3 Ko-fi

Ko-fi is a service that allows creators to earn revenue and receive tips from their customers and supporters. The services are provided by Ko-Fi Labs Limited, which has registered offices at [Suite 501 The Nexus Building, Broadway, Letchworth Garden City, Herts, SG6 9BL, United Kingdom](https://www.creditsafe.com/business-index/en-us/company/ko-fi-labs-limited-uk16299228).

Website: https://ko-fi.com  
Privacy Policy: https://more.ko-fi.com/privacy

#### 5.5.4 Patreon

Patreon is a membership platform that helps connect fans with creators they love and allows fans to supports creators financially. The service is provided by Patreon, Inc., the street address of Patreon's headquarters is [Patreon, Inc., 600 Townsend Street Suite 500, San Francisco, CA, USA](https://www.creditsafe.com/business-index/en-us/company/patreon-inc-us150889263).

Website: https://www.patreon.com  
Privacy Policy: https://privacy.patreon.com/policies/en

### 5.6 Web Services

#### 5.6.1 GitHub

Some of our web servers that you visit in your browser and that are contacted by the Software are hosted by GitHub, specifically via GitHub Pages. For more information about GitHub and their privacy practices, see section [5.7 GitHub](#57-github).

More information about GitHub Pages: https://docs.github.com/en/pages

#### 5.6.2 Snel.com

Our servers and some of our web servers are hosted by [Snel.com B.V., Schuttevaerweg 101, 3044BA Rotterdam NL](https://www.creditsafe.com/business-index/en-us/company/snelcom-bv-nl01262967) ("Snel.com"). You can find Snel.com's Data Processing Agreement and Privacy Policy via the links below.

Website: https://www.snel.com  
Data Processing Agreement: https://www.snel.com/data-processing-agreement  
Privacy Policy: https://www.snel.com/privacy-statement

#### 5.6.3 Shields.io

Some of our websites show dynamic Shields.io "badges" with live metrics. For this your browser makes a request to Shields.io's servers. Your data is processed according to their Privacy Policy.

Website: https://shields.io  
Privacy Policy: https://shields.io/privacy

### 5.7 GitHub

GitHub refers to GitHub, Inc. ("GitHub"), the street address of GitHub's headquarters is [GitHub, Inc., 88 Colin P. Kelly Jr. Street, San Francisco, CA 94107, USA](https://www.creditsafe.com/business-index/en-us/company/github-inc-us72011324). GitHub also has headquarters in the European Economic Area ("EEA"), located at [Github B.V., Spuistraat 104A, 1012 VA, Amsterdam, Netherlands](https://www.creditsafe.com/business-index/en-us/company/github-bv-nl03765938).

Website: https://github.com  
Privacy Policy: https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement

GitHub's servers are used for the following purposes (this list is not exhaustive):

- Website hosting of https://docs.musicpresence.app
- Serving the purposes of a CDN to provide downloads of the Software
- Serving downloads of the Software for automatic updates within the Software
- Hosting of application data that the Software needs to stay up-to-date, e.g. the current list of all media player identifiers in order to be able to add support for media players without requiring a complete app update, see section [4.4 Player Compatibility](#44-player-compatibility)
- Hosting of in-app news
- Hosting of the changelog of the Software
- Managing the project and open issues and feature requests
- Serving as a contact page to submit media player identifiers
- Receiving donations via [GitHub Sponsors](https://github.com/open-source/sponsors)

When you visit our websites or you use the Software, GitHub's servers are contacted. Only very little data is sent to and processed by GitHub, GitHub's infrastructure is mostly used for hosting content that is downloaded by the device you use. Your IP address, user agent, browser language and other information is processed by GitHub when a request is made to their servers. See the below links for information on how GitHub processes your data.

### 5.8 Simple Analytics

Simple Analytics B.V. ("Simple Analytics") is a EU-based and hosted, privacy-friendly analytics service that is GDPR-compliant and does not store your IP address. Simple Analytics is a sole proprietorship, established in [(1401 ED) Bussum at Hooftlaan 4, the Netherlands](https://simpleanalytics.com/privacy-policy) with a company address at [Jacob Van Lennepstraat 78H, 1053 HM, Amsterdam, the Netherlands](https://www.creditsafe.com/business-index/en-us/company/simple-analytics-bv-nl06305057).

We use Simple Analytics for privacy-friendly Software and website analytics without tracking you. Find out more about Simple Analytics's privacy practices via the links below.

Website: https://simpleanalytics.com  
Privacy Policy: https://simpleanalytics.com/privacy-policy  
Article "We don't track people": https://dashboard.simpleanalytics.com/no-tracking  
Help page "Data Collection": https://docs.simpleanalytics.com/data-collection

## 6. Encryption

All data that is sent over the network is encrypted with the use of modern and secure transport protocols. Media Metadata that is sent to Discord for Discord Rich Presence functionality communicates with the locally running Discord client application without the use of a connection over an external network and therefore does not use encryption nor does it need to use encryption, since it does not leave the user's device.

## 7. Data Controller

Music Presence and our other Services are operated by Jonas van den Berg, the data controller ("Controller"). The Controller decides why and how your personal data is handled by us when you use the Software and our Services. Jonas van den Berg is responsible for handling your data in line with the applicable data protection rules. For data protection enquiries, please contact us at {{ contact_email }}.

## 8. Your Privacy Rights

Depending on your residence location, you may have specific legal rights regarding the data we collected about you ("Personal Data"):

- The right to access the data collected about you
- The right to request detailed information about the specific types of Personal Data we've collected over the past 12 months, including data disclosed for business purposes
- The right to rectify or update inaccurate or incomplete Personal Data under certain circumstances
- The right to erase or limit the processing of your Personal Data under specific conditions
- The right to object to the processing of your Personal Data, as allowed by applicable law
- The right to withdraw consent, where processing is based on your consent
- The right to receive your collected Personal Data in a structured, commonly used, and machine-readable format to facilitate its transfer to another company, where technically feasible

To exercise these rights, please send an email to {{ contact_email }}. To verify your identity for security, we may request extra information before addressing your data-related request. Please [contact us](#11-contact) for any feedback or concerns. Depending on your region, you have the right to complain to your local Data Protection Authority. European users can find authority contacts on the European Data Protection Board website, and UK users on the Information Commissioner’s Office website.

We aim to promptly respond to requests in compliance with legal requirements. Please note that we may retain certain data as necessary for legal obligations or for establishing, exercising, or defending legal claims.

## 9. Information For Minors

Our Services are not intended for individuals under the age of 13. We do not intentionally gather Personal Data from such individuals. If you become aware that a minor has provided us with Personal Data, please [notify us](#11-contact).

## 10. Changes to This Policy

We may update this policy to reflect changes in our information practices or legal requirements. The "last updated" date at the bottom of this section indicates when the policy was last revised. If we make material changes, we will notify you in the following ways:

- In the changelog of the Software. Make sure to leave changelog notifications enabled in the settings of the Software, for when you update to and launch a new version. You can always open the most recent version of this Privacy Policy and the changelog via the *Help* menu in the system tray menu of the Software.
- By e-mail, only for any material changes that affect you, if you have provided us your e-mail address in the past and only for material changes that are in relation to the aspect of the Software for which you have provided your e-mail address (e.g. your purchase of a Scrobbling license to use Scrobbling features of the Software). Changes that are made to other aspects of the Software for which you have not provided your e-mail address are communicated through the other listed channels.

We encourage you to periodically review this page for the latest information on our privacy practices, especially if you haven't used the Software for a while or a longer period of time has passed since you last visited one of our websites.

Last updated on 5 July 2026.

## 11. Contact

Music Presence and our other Services are operated by Jonas van den Berg. For data protection enquiries or further questions regarding this Privacy Policy contact us at {{ contact_email }}.
