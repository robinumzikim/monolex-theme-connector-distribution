# Monolex Theme Connector

The v0.6.0 update was submitted for review on **2026-11-16** through the existing publisher account and is **Pending review**, with automatic publication after approval. It replaces the old local-companion workflow with an extension-only workflow on **Chrome 157+**. The currently published v0.4.1 still uses the old workflow until Google approves the update.

[Chrome Web Store](https://chromewebstore.google.com/detail/dpbkehcknngnainngakliekelaanccbc) · Publisher **monotologist** · Same extension ID; no reinstall or new listing is planned.

## First use of a theme

1. Install or update Theme Connector. Accept Chrome's theme-management permission request if prompted, and refresh app.monolex.ai once.
2. Log in to Monolex normally and choose a theme.
3. If that Chrome theme is missing, select **이 테마 처음 설치** in the site prompt or extension popup and confirm installation in its Chrome Web Store page. Only themes you actually use need installation.
4. During installation preparation, Chrome can briefly show default colors. Closing the store tab or selecting **설치 취소 · 이전 테마로** restores the previous theme.

## After installation

The connector follows the displayed preset in the focused app.monolex.ai tab, including previews, and automatically switches between installed themes. No local app, terminal program or per-change installation confirmation is required. The popup offers pause/resume and shows how many of the 38 themes are installed.

Themes and settings belong to each Chrome profile. Installing the extension in another profile does not install its themes there. If a theme is removed, the next use needs installation again. Managed Chrome policies may prevent changes. Chrome's native toolbar/content divider is not controlled.

The update uses `management` only for theme inventory, enable/disable transitions and installation events, and `storage` only for local settings and installation recovery. The content script is restricted to `https://app.monolex.ai/*`. It reads theme markers and focus/visibility, not page text, passwords, cookies or messages. No observations or installation inventory are sent to a developer server.

## Release validation

The submitted v0.6.0 package passed 50 unit/regression checks. In isolated Chrome 157 profiles, all 38 public theme IDs were exercised from official Google theme package bytes loaded as development fixtures, followed by 76 automatic forward/reverse transitions with all themes retained. First-use/cancel/install-event, pause/resume, focus boundaries and service-worker stop/wake were checked. This does not claim an observed end-to-end native Web Store installation UI or normal store-installed restart test.

Submitted ZIP SHA-256: `b265243b984a8e2f573bae7b6cda926e2b0485637c54c362b526bbbedb00f252`.

## Earlier versions

The older v0.4.1 store extension and optional ad hoc-signed Mac companion are documented in [the legacy guide](LEGACY-MAC.md). The Mac beta is no longer required by the v0.6.0 design. Its historical release files remain available for existing test users.

[Privacy policy](PRIVACY.md) · [Support](https://github.com/robinumzikim/monolex-theme-connector-distribution/issues)

Do not include passwords, cookies, browser profiles or private account data in public issues.
