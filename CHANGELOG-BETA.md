# Changelog

All notable changes to Luria are documented in this file. The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/). Entries are grouped by date, newest first, because the project does not publish tagged releases yet.

## [2026-11-22]

### Added

- Dictionary-based typo checking for Indonesian (KBBI), German, English, French, and Spanish in the proofreader (PRs #11, #15, #17, #19, #20).
- Periodic writing reminders through local notifications in the beta build (PR #10).
- Luria Nemesis beta variant with a separate APK, PIN gate, and dedicated icon and splash artwork (PR #9).
- Automatic local Android backups to `Documents/Luria/AutoBackup.luria`, written only while the PIN is unlocked (PR #8).
- Offline `check-manuscript.py` and `validate-export.py` repository tools with test coverage (PR #7).
- End User Licence Agreement.
- CI workflows for Python tools and beta APK builds.

### Changed

- Encrypted backups now require a 6-digit PIN, and legacy unencrypted payloads are no longer accepted (PR #6).
- Extended the Python/Pyodide proofreader with smarter checks and language-specific rules (PR #7).
- Disabled and dimmed the proofreader button in official builds while keeping it available in beta (PR #18).
- Enabled R8 minification for beta release builds and simplified the beta PIN screen with the Luria Nemesis name.
- APKs now sync automatically to the Luria-Novel distribution repository after main and tag builds.
- Tightened the Bookshelf grid and Create Novel color palette, and removed unused Google AI Studio files.

### Fixed

- Stopped the proofreader from reading stdin when running under Pyodide.
- Improved umlaut suggestion ranking and made edit-distance candidate ordering deterministic.
- Reduced title-word context lookup from quadratic to linear time for long chapters.
- Ensured beta APK sync stages untracked files before checking for changes.
- Stabilized PIN and backup end-to-end tests for PIN-required payloads and parallel runs.

## [2026-11-21]

### Added

- APK verification script that checks package, version, signature, splash asset, and checksum.

### Changed

- Moved the local proofreader to Python for fully offline execution (PR #5).

### Fixed

- Android splash startup frame, artwork scaling, contrast, status-bar insets, activity lifecycle visibility, and keyboard focus (PR #3).

## [2026-11-20]

### Added

- Automated Android APK build workflow with configurable version names and version codes.
- Edge-to-edge Android display behind the status and navigation bars.
- Image compression and resizing utility for uploaded cover artwork.

### Changed

- Removed Firebase and Google Drive sync in favor of local-only storage, with stricter CSP, HSTS, and COOP headers.
- Standardized CI dependency installation and simplified the README.

### Fixed

- Service worker cleanup no longer triggers unnecessary page reloads.

## [2026-11-19]

### Added

- Google Drive backup and restore support through Firebase.
- Responsive desktop layout with sidebar navigation.

### Changed

- Migrated the canonical domain to `lurianovel.my.id`.

## [2026-11-18]

### Changed

- Exports can now be aborted, use safer blob handling, and benefit from refined service worker caching.

## [2026-11-17]

### Added

- Public-readiness work covering SEO metadata, sitemap and robots files, manifest updates, a custom 404 page, and public build checks (PR #2).

### Changed

- Improved accessibility with keyboard focus trapping in the font picker, visible tab labels for voice control, higher-contrast headers, and footer links clear of navigation.

### Fixed

- Preserved PIN vault data, prevented duplicate identities on novel import, and restored chapter revisions (PR #1).
- Restored saved chapter text on direct entry and verified backup writes.

## [2026-11-15]

### Added

- 6-digit PIN security lock with encrypted local storage.
- Chapter version history with snapshot restore.
- Preview mode toggle and PDF page settings.
- New book cover themes and scroll restoration.
- Unique origin identifiers for novels and localized bookshelf import/export.

### Changed

- Improved service worker cache management.

## [2026-11-14]

### Added

- New book cover themes and improved export styling.

### Changed

- Refreshed Luria branding and the advertised feature set.

## [2026-11-13]

### Added

- Encyclopedia module and updated bottom navigation.
- Navigation sound effects.

### Changed

- Consolidated cover generation and navigation logic, and refined splash and UI styling.
- Updated the markdown engine and UI layout.

### Fixed

- Corrected the illustration data source and rendering.

## [2026-11-12]

### Added

- Notes and note editor modules.
- Markdown rendering engine.

## [2026-10-19]

### Added

- EPUB 3 export and configurable Standard and Protected PDF options for the encyclopedia.
- Interactive text expansion in encyclopedia articles.

## [2026-10-17]

### Added

- Encyclopedia module and a Cool Slate / Deep Cobalt theme.
- French and Korean language support with complete translations.
- SEO service with dynamic titles and metadata, plus updated manifest, robots, and sitemap files.

### Changed

- Updated Angular dependencies and optimized CI installation.
- Standardized branding to "Luria Novel" across the app.

## [2026-09-03]

### Added

- Application logo in the manifest, service worker cache, and HTML meta tags.
- Version 2.1 badge in the bookshelf header.

## [2026-09-02]

### Added

- Dynamic color palettes and palette shifting for book covers.

## [2026-09-01]

### Changed

- Replaced the Blossom cover theme with Haven.

## [2026-08-31]

### Added

- Flank cover theme.

### Changed

- Removed the philosophy page and unused menu dependencies.

## [2026-08-29]

### Added

- Dark mode.
- Philosophy page.
- New cover themes and refined custom cover rendering.

### Changed

- Overhauled the README and updated logo assets.

## [2026-08-27]

### Added

- Luxury cover theme and additional cover templates.
- Image-based splash screen.

### Changed

- Updated splash artwork and aligned DOCX export dimensions.

## [2026-08-26]

### Added

- PWA manifest, offline service worker, and export progress UI.
- SEO assets, environment variables, and static routing rules.

## [2026-08-24]

### Added

- Journal module with IndexedDB persistence and DOCX export.
- Editable novel metadata.
- Copyright page support for DOCX and PDF exports.
- Custom cover image support.
- Google Drive restore support.
- Responsive desktop layout.

### Changed

- Improved mobile viewport handling and disabled browser autofill and spellcheck on form fields.

## [2026-08-23]

### Added

- Initial Luria Novel application scaffold.

### Changed

- Improved mobile viewport and safe-area handling.
