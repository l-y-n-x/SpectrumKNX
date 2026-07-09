# Changelog

## 1.11.0

### Added

- **Update available popup & release notes**: Added an in-app "update available" popup that shows when a newer release exists, displaying release notes and a link to the GitHub release. It can also be reopened from the Settings chip. Added a new configuration option `UPDATE_CHECK` (default `true`) to allow opt-out for offline or privacy-focused installations (#149).
- **DPT name in building structure**: The building structure view now displays the descriptive DPT name (e.g. "Scaling") under the DPT number (e.g. "DPT 5.001"), with the full name visible in a tooltip (#160).

### Fixed

- **ETS project upload in HA companion mode**: Fixed the project directory permissions/symlinks in SQLite/companion mode so that ETS projects can be successfully uploaded. Also added an in-app notice when no project is loaded, pointing users to the upload flow in Settings so they can set up filtering (#159).

## 1.10.0

### Added

- **Telegram log import/export**: export the live buffer and re-import logs for offline analysis (#99).
- **Configurable web port**: the UI listen port can now be set via configuration (#147).

### Fixed

- **Header layout**: the "Spectrum KNX" brand no longer overlaps the toolbar metrics on narrow windows (#158).
- **Large imports**: clearer, actionable error when a large zip import fails because temp storage is exhausted (#157).

## 1.9.1

### Fixed

- **Branding**: browser tab title now reads "Spectrum KNX" instead of "frontend", and the favicon and in-app logo match the add-on's waveform icon (#139).

## 1.9.0

### Added

- Initial release of the **Spectrum KNX (HA Companion)** add-on: runs the Spectrum KNX analyzer UI directly on Home Assistant's own KNX telegram database (read-only) — no second bus connection and no separate database. Live telegrams are streamed from Home Assistant's websocket API (`knx/subscribe_telegrams`), with gap replay from the shared store after reconnects.
