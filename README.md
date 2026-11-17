# Monolex Theme Connector

The **v0.7.0 update is implemented and validated; review submission has not yet been confirmed**. The currently public store version is **v0.6.0**, published on November 17, 2026. v0.7.0 improves existing-session connection and first-theme installation guidance on **Chrome 157+**.

[Chrome Web Store](https://chromewebstore.google.com/detail/dpbkehcknngnainngakliekelaanccbc) · Publisher **monotologist** · The same extension ID is retained.

## Reuse your existing Monolex session

Install/update the connector in the same Chrome profile where you use Monolex. v0.7.0 attaches to tabs already open before extension installation without a page reload. Its popup distinguishes a ready workspace, login page, loading/unavailable page and no open Monolex tab. The open button returns to the existing workspace, preferring it over a separate login tab.

This observes workspace/account-control visibility, not account text or authentication secrets. It does not perform a new server-authentication check, transfer another profile's login or restore a genuinely expired Monolex session. Monolex still controls its own login.

## First use of a theme

1. In a focused ready app.monolex.ai workspace, choose a theme.
2. If that Chrome theme is missing, v0.7.0 opens its official Web Store listing automatically once. Confirm **Add to Chrome** and any Chrome installation dialog. No theme search or separate file download is needed.
3. On completion, the connector returns to the original workspace if its store tab is still active. During preparation Chrome may briefly show default colors. Closing the store tab or selecting **설치 취소 · 이전 테마로** restores the previous theme.
4. Cancellation, page focus and worker wake do not repeatedly reopen the same theme. Use **설치 페이지 다시 열기** to retry. The no-account theme-management page also supports explicit installation.

All 38 names, palettes and official theme mappings are included in the connector. Bundled color data is not a Chrome theme installation: Chrome's first-install confirmation remains required for each desired theme, in each profile. The connector cannot silently or bulk-install themes.

## After installation

Installed themes switch automatically with the displayed preset in the focused Monolex workspace, including previews. No local app or per-change confirmation is required. The popup offers pause/resume and installed-theme counts. Brief previews are debounced before first-install handoff. Chrome policies may block changes. Removing a theme requires installation again; after an earlier offer, use explicit retry. Native toolbar-divider hiding is unsupported.

## Privacy and validation

Permissions are `management`, `storage`, `scripting` and exact app host access. Account labels, passwords, cookies, tokens, page text and account storage are not read. No observations or inventory are sent to a developer server. See [the privacy policy](PRIVACY.md).

The v0.7.0 candidate passed 57 unit/regression checks, actual Chrome 157 app-open-before-install connection tests, ready/login/loading distinction, workspace reuse, one-time store handoff, cancellation recovery, worker wake and focus restrictions. All 38 public IDs passed 76 automatic transitions with all themes retained, using official Google CRX bytes loaded as development fixtures. Real user authentication was not accessed. Native Web Store install completion and normal store-installed full-browser restart retention are not claimed as observed tests.

Prepared ZIP SHA-256: `e9d7829873ec5527de1e08b9e6a3dec00bc6918fd4c42d0e9804faff714bd4fa`.

## Earlier versions

v0.6.0 required a connector install click before opening each missing theme's listing. The older v0.4.1 local-companion workflow is preserved in [the legacy guide](LEGACY-MAC.md). That Mac beta is not required by current extension-only versions.

[Support](https://github.com/robinumzikim/monolex-theme-connector-distribution/issues). Do not post passwords, cookies, browser profiles or private account data.
