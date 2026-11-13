# Monolex Theme Connector

This repository contains public installation instructions, privacy information and reviewed Mac companion downloads. It does not contain account data or browser profiles.

## Chrome extension

**Monolex Theme Connector v0.4.1** was submitted to the Chrome Web Store on **2026-11-13** by publisher **monotologist**. The developer dashboard confirms **Pending review**. It is configured for free, public availability in all regions and automatic publication after approval. It is not yet available for installation.

[Chrome Web Store listing (available after approval)](https://chromewebstore.google.com/detail/dpbkehcknngnainngakliekelaanccbc) - Store ID: `dpbkehcknngnainngakliekelaanccbc`.

The extension detects the `data-theme` marker on the current `app.monolex.ai` page. Where a matching standalone Chrome theme has been verified as published, it can open that theme's Web Store page for manual installation.

## Optional Mac automatic theme connection — beta

[Download the Mac companion beta](https://github.com/robinumzikim/monolex-theme-connector-distribution/releases/download/v0.4.0-beta.1/monolex-theme-sync-mac-arm64.zip)

Requires Apple Silicon (M1 or later), macOS 14+, and installed Google Chrome. The app includes its Node runtime; no separate Node installation is required. **This beta is ad hoc signed and has not been Apple-notarized. macOS may prevent downloaded copies from opening.** Developer ID signing and notarization remain pending. This beta is intended for evaluated test use; it is not a notarized general-availability Mac installer.

1. Extract the ZIP and move **Monolex Theme Sync.app** to Applications.
2. Open the Mac app once. It registers a user-level native messaging connector restricted to this exact Chrome extension and opens its own dedicated Chrome.
3. Log in to Monolex in that dedicated Chrome and change its theme in settings. The local app reads the displayed theme marker and five color roles and updates the dedicated Chrome theme.
4. The separately installed Web Store extension can show the local app status, open its dedicated Chrome, pause/resume automatic changes, and reopen its connection window.
5. Quit by closing all dedicated Chrome windows or quitting the Mac app. Reopening preserves its dedicated profile and theme identity.

**Automatic theme changes affect the companion's dedicated Chrome profile. Ordinary Chrome windows retain their theme.** Installing the Web Store extension alone does not recolor ordinary Chrome automatically. The companion uses Chrome's development theme-loading capability, so Chrome updates may require compatibility verification.

No paid companion subscription is required by this package. Access to the Monolex service uses your own Monolex account and its applicable service plan.

## Storage, updates and removal

The app keeps its dedicated profile, generated theme and local status/log files in `~/Library/Application Support/Monolex Theme Sync/`. Replacing or moving the app keeps this data. The download does not contain anyone's login session.

The native messaging registration is one file:
`~/Library/Application Support/Google/Chrome/NativeMessagingHosts/ai.monolex.theme_sync.json`.
It permits only `chrome-extension://dpbkehcknngnainngakliekelaanccbc/` and accepts status/start/reopen/pause/resume requests. It does not provide a general shell or file-access API.

To uninstall, quit and move the Mac app to Trash, remove the Chrome extension, and optionally move the dedicated data folder and this one registration file to Trash. Other Chrome profiles and native messaging registrations are separate.

## Privacy and support

[Privacy policy](PRIVACY.md) · [Report a problem](https://github.com/robinumzikim/monolex-theme-connector-distribution/issues)

Do not include passwords, browser profiles, cookies or local connection tokens in issue reports.
