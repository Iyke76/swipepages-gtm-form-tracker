# Changelog

## 3.0.1

Initial standalone SwipePages release prepared for public GitHub publishing.

### Included

- SwipePages-only confirmation-class-based tracking.
- `swipe_form_success` and `swipe_form_failed` dataLayer events.
- First-interaction event: `ec_form_interaction`.
- Load diagnostic event: `ec_tracker_initialized`.
- Consent detection for Google Consent Mode v2, OneTrust, and Cookiebot.
- `window.EC_FORM_CONSENT_CHECK` override hook.
- PII redaction when PII consent is denied.
- Optional SHA-256 hashing for normalized email and phone values.
- Duplicate success suppression using a 5-minute session dedupe ledger.
- SPA route-change rescanning.
- GTM Custom HTML paste-ready file and raw JavaScript file.

### Privacy hardening

- Debug logging defaults to disabled.
- Dedupe runs after PII redaction.
- Analytics-denied consent prevents event firing and storage writes.
- PII-denied consent redacts both stored and in-memory recall data.

### Fixed before public release

- Corrected heartbeat tracker version reference for the SwipePages standalone.
- Removed `<script>` wrapper from the raw `.js` file.
- Added support for both `wraning` and `warning` Tatsu class spellings.
