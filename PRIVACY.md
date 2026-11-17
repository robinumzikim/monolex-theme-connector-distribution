# Privacy policy — Monolex Theme Connector

Effective date: 2026-11-17. This policy covers the v0.7.0 update. Earlier [v0.6.0](PRIVACY-v0.6.0.md) and [v0.4.1](PRIVACY-v0.4.1.md) policies are preserved.

## Single purpose

Match the Chrome theme to the preset displayed in the focused app.monolex.ai workspace, reusing the existing signed-in page and guiding each missing theme through Chrome-confirmed first installation. No local companion is required.

## Data used locally

Only on `https://app.monolex.ai/*`, the bundled content script reads root `data-theme`/`data-theme-mode` attributes, document focus/visibility, and whether the workspace and account controls exist and are hidden. Matching open-tab URLs are inspected transiently to recognize login/workspace routes and reuse an existing tab. A ready workspace/account control is a page-UI signal; the connector does not perform or assert fresh server authentication. Unavailable/loading state is not treated as signed-out.

The connector does not read account-button labels, email addresses, page body text, form values, passwords, messages, cookies, authentication tokens or account storage. It does not use the browsing-history API. Displayed theme observations may include unsaved previews.

Chrome management returns installed-item information, immediately filtered to themes for inventory, enable/disable operations and installation events. The connector does not manage unrelated extensions. Popup counts use only the 38 known Monolex theme IDs. Inventory is not sent to a server.

## Local storage and controls

`chrome.storage.local` keeps the automatic-sync setting, last theme ID, sync state, theme IDs already offered an automatic first-install handoff, and a small installation-recovery record (theme IDs, source/store tab IDs and time). Offered IDs prevent repeated store tabs after cancellation. No page URLs, account labels, credentials or browsing history are stored.

When a focused ready workspace displays a missing known theme for the first time, the extension automatically opens its official Chrome Web Store listing once. The user completes Chrome's installation confirmation. It does not silently install or bundle-install themes. Preparing first installation temporarily disables the outgoing theme to preserve it. Completion is detected locally; cancellation restores the previous theme where possible. An explicit retry remains available. The original workspace is reactivated on completion only if the connector's store tab is still active in the focused window.

The popup open action reuses a matching existing workspace instead of opening another login tab. If no matching tab exists it opens the workspace in the same Chrome profile; Monolex controls authentication. Expired and other-profile sessions are not restored or copied. Automatic switching can be paused. Chrome controls removal of the connector and separately installed themes; uninstalling the connector removes its extension storage.

## Permissions

- `management`: theme inventory, transitions and installation events.
- `storage`: the local operational state above.
- `scripting` and exact `https://app.monolex.ai/*` host access: inject only bundled connection code into already-open matching top-level tabs after installation/update or reconnection, without forcing a page reload. Other origins are not targeted.

## Transmission and third parties

No theme observations, structural UI signals, inventory or settings are sent to a developer server. There is no analytics, advertising, tracking SDK, nativeMessaging, debugger or remote executable code. Data is not sold or transferred for unrelated uses, creditworthiness or lending.

Chrome Web Store and Monolex handle their own accounts and web requests under their policies. The first-use official store listing may open automatically as described above; support/privacy links open only after user action. Information voluntarily posted in public GitHub issues is public; omit authentication or personal data.

## Contact

Use [the support tracker](https://github.com/robinumzikim/monolex-theme-connector-distribution/issues).
