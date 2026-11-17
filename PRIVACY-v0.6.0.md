# Privacy policy — Monolex Theme Connector

Effective date:2026-11-16. This policy covers the v0.6.0 update; the earlier v0.4.1 policy is [preserved here](PRIVACY-v0.4.1.md).

## Single purpose

Match the Chrome theme to the preset displayed in the focused app.monolex.ai tab, after each desired theme is installed once with user confirmation. No local companion is required by v0.6.0.

## Data used locally

On `https://app.monolex.ai/*`, the content script reads only root `data-theme`/`data-theme-mode` attributes plus whether the document is focused and visible. It displays an in-page first-use installation prompt. It does not read page body text, forms, passwords, messages, cookies or account storage. Displayed theme observations may include unsaved previews.

Chrome's management API returns installed-item information. The worker immediately filters this to themes for inventory, enable/disable operations and installation events. It does not manage unrelated extensions. Popup installation counts use only the38 known Monolex theme IDs. The inventory is not sent to a server.

## Local storage and controls

`chrome.storage.local` stores the automatic-sync setting, last selected theme ID, sync state and a small in-progress installation recovery record: theme IDs, source/store tab IDs and an operational timestamp. This is per-profile operational state, not browsing history or analytics. No page URLs or account credentials are stored in that record.

Missing themes are installed through the official Chrome Web Store after the user's explicit action. Preparing an installation temporarily disables the outgoing theme to preserve it. Installation completion is detected locally; cancellation attempts to restore the prior theme. Automatic changes can be paused or resumed. Removing a theme or the connector is controlled by Chrome. Uninstalling the connector removes its local extension storage; Chrome manages any separately installed themes.

## Transmission and third parties

No theme observations, installed-theme inventory or local settings are sent to a developer server. The package includes no analytics, advertising, tracking SDK, nativeMessaging, debugger or remote executable code. Data is not sold or transferred for unrelated uses, creditworthiness or lending.

Chrome Web Store and Monolex handle their own accounts and web requests under their privacy policies. Store/support/privacy links are opened only after user action. Information voluntarily posted in public GitHub issues is public; omit authentication or personal data.

## Contact

Use [the support tracker](https://github.com/robinumzikim/monolex-theme-connector-distribution/issues).
