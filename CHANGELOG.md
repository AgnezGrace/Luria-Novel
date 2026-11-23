# Changelog

All notable changes to Luria are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).
This repository does not publish release tags yet, so entries are grouped by the date the changes landed on `main`.

## [2026-11-23]

### Changed
- Proofreader is now beta-only; its button is disabled in Official builds.

## [2026-11-22]

### Added
- Beta "Luria Nemesis" Android variant with a separate APK, PIN gate, and portrait/landscape splash screens (PR #9).
- Automatic local Android backup to `Documents/Luria/AutoBackup.luria`, written only while the PIN is unlocked and restored when the library is empty (PR #8).
- Smarter offline Python proofreader plus repository checks for manuscript and export validation, with dedicated CI (PR #7).
- Beta APK build workflow for the Luria Nemesis variant (PR #9).

### Changed
- Encrypted `.luria` backups now require a 6-digit PIN (PR #6).
- Legacy unencrypted v2 backups are rejected, and PIN-less exports report `PIN_REQUIRED` (PR #6).
- APK publishing now syncs builds to the Luria-Novel repository on pushes to `main`, version tags, and manual runs (PR #6).
- Bookshelf uses a compact two-column grid on phones.
- Create Novel uses a denser color palette.
- README rewritten in English and trimmed of contributor and internal-tooling notes.

### Fixed
- Browser proofreader no longer reads stdin when running under Pyodide (PR #7).
- Playwright coverage for PIN backup/restore and offline flows was stabilized with separate tests, digit-by-digit PIN entry, and longer timeouts.

### Removed
- Abandoned Google AI Studio scaffolding, screenshots, generated assets, design notes, and unused configuration files.

## [2026-11-21]

### Added
- Release APK verification script added to the Android CI pipeline (PR #3).

### Changed
- Local proofreader rewritten in Python and executed in the browser through Pyodide (PR #5).
- Android launcher and splash assets were regenerated and refreshed.

### Fixed
- Android splash now starts on the correct frame, fits its artwork, and keeps readable contrast (PR #3).
- Android splash and status bar now respect system insets (PR #3).
- Keyboard focus and Capacitor lifecycle visibility were stabilized on Android (PR #3).

## [2026-11-20]

### Added
- Native Android project via Capacitor with an APK build workflow.
- Edge-to-edge display on Android.
- Dynamic Android versioning from tags or manual input.

### Changed
- Hardened local security with input sanitization and stricter PIN and encryption handling.
- Standardized dependency installation in CI.
- Updated the Android SDK setup in the APK workflow.

### Removed
- Firebase-backed Google Drive backup integration and related configuration.

## [2026-11-19]

### Added
- Optional Google Drive backup and restore.
- Responsive desktop layout with sidebar navigation.

### Changed
- Canonical domain moved to `lurianovel.my.id`.

## [2026-11-18]

### Changed
- Reworked the PDF/EPUB export pipeline and export manager.
- Improved service worker caching and offline behavior.

## [2026-11-17]

### Added
- Public launch readiness with static public pages, sitemap and robots files, a 404 page, security headers, and SEO metadata (PR #2).
- Public build and end-to-end checks plus more reliable offline-writing behavior (PR #2).
- Accessibility improvements including font-picker focus trapping, visible tab labels, and higher-contrast help and legal headers (PR #2).

### Changed
- Restored saved chapter text when entering a chapter directly and verified backup writes (PR #2).

### Fixed
- Preserved PIN vault saves, novel identities on import, and chapter revisions (PR #1).

## [2026-11-15]

### Added
- 6-digit PIN lock with PBKDF2-derived AES-256-GCM encryption for local data.
- Chapter version history with restore support.
- Preview mode toggle and PDF page-size settings.
- Six additional cover themes.
- Router scroll-position restoration.
- Bookshelf `.luria` import/export with localized UI.
- Unique origin identifiers for novels to distinguish imported copies.

### Changed
- Improved service worker cache management.

## [2026-11-14]

### Added
- Ten new cover themes: Zenith, Citadel, Vortex, Obelisk, Aether, Axiom, Thesis, Vector, Cortex, and Summit.

### Changed
- Improved PDF/EPUB typography with CJK-aware styling and fallback fonts.
- Refreshed Luria branding, metadata, help and legal copy, and UI styling.

## [2026-11-13]

### Added
- Encyclopedia wiki with categories, images, and automatic tables of contents.
- Chinese localization.
- Navigation sound effects.

### Changed
- Consolidated cover generation and navigation logic.
- Expanded bottom navigation with Notes and Encyclopedia tabs.
- Refined markdown rendering and UI layout.

### Fixed
- Corrected the illustration data source and rendering in EPUB exports.

## [2026-11-12]

### Added
- Notes workspace with a note editor, checklists, eight paper tints, labels, pinning, archive, and trash.
- Markdown rendering engine for chapters, notes, and exports.
- Bottom navigation for Bookshelf, Create Novel, and Settings.

### Removed
- Legacy seed-data encyclopedia pages ahead of the wiki rebuild.
- Legacy DOCX export in favor of PDF and EPUB.

## [2026-10-19]

### Added
- EPUB 3.0 book export.
- Standard and Protected PDF export modes.

## [2026-10-17]

### Added
- Initial seed-data encyclopedia with localized content and SEO-friendly pages.
- French, Korean, and German language support.

### Changed
- Upgraded to Angular 21 and optimized CI dependency installation.
- Expanded SEO metadata, sitemap, and public page metadata.

## [2026-09-03]

### Added
- Luria application logo and PWA icons.
- Version 2.1 badge in the bookshelf header.

## [2026-09-02]

### Added
- Dynamic color palettes and a palette picker for book covers.

## [2026-08-29]

### Added
- Dark mode and additional cover themes.

### Changed
- Overhauled the README with the full Luria feature set.

## [2026-08-27]

### Added
- Geometric book cover themes and refreshed splash artwork.

## [2026-08-26]

### Changed
- Reworked PWA configuration, manifest, service worker, routes, and application shell.

## [2026-08-24]

### Added
- Custom 2:3 cover image uploads with cropping.
- Copyright and colophon page options for document exports.
- DOCX export for manuscripts.

### Changed
- Refined the desktop layout and responsive behavior.

## [2026-08-23]

### Added
- Initial Luria Novel application with bookshelf, chapter editor, novel detail, IndexedDB storage, and PDF export.

### Changed
- Upgraded dependencies and the CI workflow.

### Fixed
- Improved mobile layout and viewport handling.
