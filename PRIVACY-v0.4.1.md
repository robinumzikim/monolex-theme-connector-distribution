# Privacy policy — Monolex Theme Connector

Effective date: 2026-11-13

Monolex Theme Connector helps match the theme displayed by Monolex with Chrome themes and an optional local Mac companion.

## Data handled locally

The Web Store extension reads only the current Monolex page's `data-theme` and `data-theme-mode` HTML attributes to identify the displayed preset. It operates only on `https://app.monolex.ai/*`. It does not read page body text, passwords, form values, messages, cookies or the account's storage. Marker changes may include a theme preview before it is saved.

With the optional Mac companion installed, the extension exchanges local status and the explicit commands status/start/reopen/pause/resume through Chrome Native Messaging. The native host is restricted to this exact extension ID. It authenticates its own local controller before forwarding controls. It does not provide arbitrary command execution or general file access.

In the dedicated Chrome profile, the Mac app's bundled extension additionally reads five computed theme color roles: primary/secondary/tertiary background and primary/secondary text. It sends those marker/color values over the app-owned local debugging pipe so the local app can generate and verify the matching Chrome theme.

## Storage and transmission

Theme observations used by the Web Store popup are kept in memory. The optional local app saves its generated theme, stable theme identity, connection metadata, timestamps and operational logs locally under `~/Library/Application Support/Monolex Theme Sync/`.

Its dedicated Chrome stores login/session information normally within that separate browser profile. The connector does not inspect those account databases. Browser profiles, authentication tokens and login sessions are not included in distributed packages.

The extension and companion do not send theme observations or local status to a developer server. They include no analytics, advertising, tracking SDK, sale of data or remote executable code. Local data is used only for the requested theme detection and connection function and is not used for credit or lending decisions.

External links open only when selected by the user. The Monolex service, Chrome Web Store and GitHub download/support pages handle their own account and web requests under their respective privacy policies. Information you choose to post in a public GitHub issue is public; please omit personal or authentication data.

## User controls and deletion

The extension popup offers explicit local connection controls. Automatic changes can be paused/resumed, and the local app can be quit. Uninstall the extension through Chrome. To remove the optional local app and its retained data, follow the removal instructions in the setup guide, including its one native messaging registration file.

## Changes and contact

Changes to these data practices will be disclosed in the extension's release information and updated here. For questions, use [this project's issue tracker](https://github.com/robinumzikim/monolex-theme-connector-distribution/issues) without posting private account information.
