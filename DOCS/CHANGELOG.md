# Changelog

## 2.5.22

- Moved application metadata and installed update checks to `KernFerm/BubblesWordWriter`.
- Replaced raw GitHub updater responses with concise messages that do not expose request headers or internal response details.
- Added regression coverage for missing GitHub release and updater metadata.

## 2.5.20

- Added hashed-token collaboration authorization files with room-scoped editor/viewer roles and server-enforced read-only sessions.
- Extracted reusable find/replace and print-range validation from the renderer controller with direct Unicode, regular-expression, and malformed-input tests.

- Added an authenticated, persistent self-hosted Yjs collaboration server with health checks, bounded connections and payloads, heartbeat cleanup, atomic room persistence, and graceful shutdown.
- Added non-persisted collaboration access tokens and restart/persistence protocol tests.
- Added mediated executable-extension APIs for extension-private text storage, bounded clipboard text, and allowlisted public HTTPS JSON requests.
- Added forced-crash recovery, accessibility metadata, large-document performance, memory, multi-tab, and guarded Windows upgrade-preservation test workflows.
- Extracted background document worker lifecycle management from the main renderer controller and expanded production, security, and self-hosting documentation.

## 2.5.16

- Completed the installed-build GitHub Releases update flow with explicit stable/beta/developer state, localized current-version messaging, multi-release notes, download progress, and tested channel handling.
- Added automatic validation for the installer, blockmap, `latest.yml`, Authenticode status in release CI, and a generated `SHA256SUMS.txt` for manual GitHub uploads.
- Added all-pages, current-page, current-selection, and custom-range printing through the existing native printer pipeline.
- Added revision combination with pending-change preservation, deduplication, valid-range enforcement, and the existing individual accept/reject workflow.
- Added an immediate, accessible startup splash that remains visible while settings, extensions, recovery data, and the first document are initialized.
- Added an original BWW overlapping-bubble application icon and horizontal Bubbles Word Writer logo using a professional four-shade blue palette.
- Updated the About experience, browser metadata, installer branding, release metadata, and package lock for version 2.5.16.
- Kept the current patched Electron Builder release after confirming npm's proposed downgrade introduces high and critical vulnerabilities; the shipped runtime dependency audit is clean.
- Added higher-fidelity local legacy `.doc` conversion through LibreOffice when available, with a clearly reported readable-content fallback.
- Added an offline English dictionary and thesaurus with definitions, synonyms, and antonyms using the bundled Princeton WordNet database.
- Expanded page layout and Office-format round trips for gutters, mirrored margins, columns, line numbering, borders, backgrounds, vertical alignment, and paper sources.
- Added printer selection, ranges, copies, collation, duplex, color, scale, and pages-per-sheet controls while retaining the Windows system print dialog.
- Localized the startup sequence and all current static interface labels in English, Spanish, and Arabic, including right-to-left splash behavior.
- Hardened atomic document writes against partial output and completed a clean Snyk Code scan and full dependency audit with documented, expiring exceptions for mitigated upstream-only findings.
- Updated the complete TipTap editor package family to 3.32.0 and retained KaTeX 0.18.10 as the newest version supported by TipTap Mathematics 3.32.0.
- Added required third-party notices to the protected package and rebuilt the current-user NSIS installer, blockmap, updater metadata, and SHA-256 manifest.

## 1.0.42

- Added live page-based editing with automatic content reflow, document paper sizes and margins, repeating sanitized headers and footers, first/even page variants, current and total page status, manual Page Break alignment, shrink recalculation, and continuous Web/Draft/Outline views.
- Added integrity-pinned executable extensions with explicit user trust, API versioning, permission-filtered input, disposable Chromium process isolation, denied direct I/O, time and memory limits, and real Electron end-to-end coverage.
- Added persisted English, Spanish, and Arabic interface locales with translation resources, fallback behavior, localized native menus, locale-aware dates and numbers, and automatic LTR/RTL application chrome.
- Completed mixed-direction paragraph and table editing with automatic direction, table-level RTL controls, and direction preservation across DOCX, ODT, RTF, HTML, print, and PDF paths.
- Added persistent ribbon customization with group visibility, left/right ordering, validation, factory reset, and Electron end-to-end coverage.

- Added real Print, Web, Draft, and Outline views. Outline Mode supports stable section collapse, heading promotion/demotion, and undoable whole-section movement with per-tab state isolation.
- Added an Electron regression covering heading creation, collapse, section reordering, heading demotion, and transitions across all editable document views.
- Removed full-document traversal, Track Changes diffing, repeated title updates, and redundant main-process dirty-state IPC from the per-keystroke path; revisions now flush after typing becomes idle and at save, copy, snapshot, comparison, review, recovery, tab-switch, and updater-restart boundaries.
- Stopped rebuilding unchanged tabs, recent files, extension menus, document properties, page layout, and other application chrome when an idle typing update only needs statistics and outline analysis.
- Added a real 1,500-paragraph Electron performance regression that verifies responsive typing and correctly batched Track Changes revisions.
- Made Copy Diagnostics obtain real runtime information directly instead of relying on previously rendered About-dialog content or exposing an unfinished fallback.
- Reworked PDF and print headers and footers as repeating paged-media margin boxes with real page counters plus first-page and even-page variants, including CSS-safe handling of user-authored metadata.
- Added accessibility release checks for editor semantics, accessible control names, keyboard focus visibility, modal focus containment, reduced motion, and interface scaling.
- Hardened updater state transitions and added controlled coverage for stable/beta/developer channels, no-update and available-update states, progress, verified completion, network failure, corrupted artifact rejection, and restart/install gating.
- Added personal, organization, and project dictionaries with native spellchecker integration, migration, and bounded `.dic`, `.txt`, and `.json` import/export.
- Added an enforced declarative-extension permission allowlist and blocked document-changing contributions without explicit `document:modify` access.
- Added document-comparison detection for unique moved passages and formatting-only changes, individual formatting restoration, and native DOCX moved-revision round trips.
- Added opt-in, self-hostable Yjs collaboration with structured live updates, synchronized comments, participant presence, named cursors, local collaborative undo, automatic reconnect, and conflict-free offline merging, backed by real two-process Electron tests.
- Added image-aware DOCX and ODT round trips, document layout and header/footer preservation, equations, editable drawing shapes with floating placement and layers, right-to-left paragraphs, and customizable shortcuts and quick tools.
- Completed the interactive updater flow with separate automatic-check and automatic-download preferences, release details, byte progress, manual download, install-on-close, and recovery-aware restart controls.
- Fixed a main-process startup crash caused by an invalid generated filename regular expression and added compiled JavaScript syntax validation to every production build.
- Reduced window-composition cost with contained document painting, lighter shadows, and an automatic low-paint mode while the native window is moving or resizing; added an early-start hardware-acceleration preference and documented the graphics-driver fallback.
- Added XLSX mail merge sources alongside CSV and JSON with bounded local worksheet parsing.
- Added scheduled installed-build update checks, GitHub Releases publishing metadata, release validation, and a tag-driven Windows release workflow.
- Added native `.btw` password encryption using scrypt and AES-256-GCM; encrypted documents are excluded from plaintext recovery and local version-history caches.
- Added DOCX comment parts and ranges, Bubbles comment reply/resolution round trips, and custom paragraph style import/export.
- Added visible inline Track Changes decorations for insertions, deletions, and formatting revisions.
- Added an opt-in, loopback-only Ollama writing assistant for selected text or the current document.
- Added offline image-to-text recognition through the Windows OCR runtime with review, copy, and insert actions.
- Added start/stop offline Windows dictation with language selection, confidence reporting, and review before insertion.
- Added table formulas, custom cell borders, and repeat-on-print header rows.
- Added first-page and odd/even header and footer variants with DOCX import and export support.
- Added printable #10 envelope documents and configurable address label sheets.
- Added a Playwright Electron smoke suite covering editing, Find layout, table actions, tab closing, and process shutdown.
- Added native DOCX tracked-insertion/deletion round trips plus table splitting, AutoFit, distribution, and alignment tools.
- Added editable decorative text with gradients, outlines, shadows, curvature, rotation, and transparency.
- Added marked index entries, generated alphabetical indexes, and linked tables of figures, tables, and equations.
- Moved live document statistics and grammar/style analysis into a bounded background worker for smoother large-document editing.
- Moved crash recovery to a validated, size-bounded atomic disk journal with a backup copy and legacy browser-storage migration; recovery now supports timestamped previews, selective restore, discard, and keep-for-later choices without overwriting source files.
- Completed version-history controls with preview, text comparison, restore, duplicate, delete, protected-document exclusion, and per-document retention limits.
- Migrated version snapshots from browser storage to a validated, bounded atomic disk journal with backup recovery and automatic legacy-history migration.
- Added controlled Wait/Reload handling for unresponsive editor windows and made crash-close behavior bypass stale unsaved-change prompts safely.
- Replaced prompt-only mail merge with record-range preview, separate-tab output, and combined page-separated output for one bulk Print Preview or print job.
- Added tracked formatting revisions for common character and paragraph commands, including visible labels and individual formatting rollback.
- Added persistent accessibility preferences for reduced motion, stronger contrast, larger controls, and 80-150% interface scaling.
- Added bounded, local citation-library import and export for CSL JSON, BibTeX, and RIS with duplicate detection.
- Removed the confusing green ruler sliders; page margins and paragraph indents remain available in their dedicated dialogs.
- Validated the unpacked application and current-user NSIS installer, including blockmap and SHA-512 updater metadata.

## 0.1.0

- Established the initial Electron, TypeScript, Vite, TipTap, and electron-builder foundation for BubblesTheDev Writer.
- Added startup scripts, Electron launch wrapper, current dependency versions, and installer script approvals.
- Added real command search, find/replace, editable document properties, recent documents, settings UI, format-aware saving, close confirmation, and local recovery snapshots.
- Added PDF export, document printing, page layout metadata/controls, expanded document statistics, and optional backup copies.
- Added per-user Windows installation under Local AppData, an application registry key, desktop and Start menu shortcuts, and clean uninstall of app-owned data.
- Added an original application icon, tab close buttons, reliable window exit handling, responsive typing updates, and a compact Find toolbar.
- Added automated validation for every visible native-menu and renderer command.
- Reworked the README into an end-user installation, usage, privacy, file-support, troubleshooting, uninstall, and developer guide.
- Added npm audit and Snyk dependency/source scanning, continuous monitoring uploads, CI security checks, and explicit source-upload exclusions.
- Patched vulnerable transitive `undici` and `fast-uri` versions identified by Snyk.
- Added independent uninstall checkboxes for removing settings, recovery/history data, and extensions/profile caches while preserving all optional data by default.
