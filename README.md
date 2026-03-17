# Corporate Privacy Shield

Corporate Privacy Shield is a static Manifest V3 browser extension for Chrome and Microsoft Edge.
It blocks selected ad and tracking domains using only the `declarativeNetRequest` API.

## Security and Privacy Design

- Uses `manifest_version: 3`.
- Uses only static rules from `rules.json`.
- No background service worker.
- No content scripts.
- No `storage`, `tabs`, or `<all_urls>` permissions.
- No JavaScript networking code (`fetch`, `XMLHttpRequest`, telemetry, analytics).

## Local Testing in Chrome

1. Open Chrome and go to `chrome://extensions`.
2. Enable **Developer mode** (top-right).
3. Click **Load unpacked**.
4. Select this folder: `internalAdblocker`.
5. Confirm the extension appears as **Corporate Privacy Shield 1.0.0**.
6. Browse to a test site that loads known tracker domains and verify requests are blocked in DevTools Network panel.

## Local Testing in Microsoft Edge

1. Open Edge and go to `edge://extensions`.
2. Enable **Developer mode** (left sidebar).
3. Click **Load unpacked**.
4. Select this folder: `internalAdblocker`.
5. Confirm the extension appears as **Corporate Privacy Shield 1.0.0**.
6. Validate blocked requests in DevTools Network panel on a tracker-heavy test page.

## Notes for IT Validation

- This package is static-only and contains no executable background logic.
- Rule updates require replacing `rules.json` and reloading the extension.
