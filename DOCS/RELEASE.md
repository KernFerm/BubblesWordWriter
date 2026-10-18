# 🎉 Bubbles Word Writer 2.5.22

**Release date:** October 18, 2026  
**Platform:** Windows 10 and Windows 11, 64-bit  
**Installer:** `Bubbles-Word-Writer-Setup-2.5.22.exe`

[⬇️ Download Bubbles Word Writer 2.5.22](https://github.com/KernFerm/BubblesWordWriter/releases/download/v2.5.22/Bubbles-Word-Writer-Setup-2.5.22.exe)

Version `2.5.22` is a protected Windows release of Bubbles Word Writer: a private, local-first word processor with a familiar old-school desktop workflow. It does not require an account, advertising, telemetry, analytics, or cloud storage.

## 🌟 Release Highlights

- Familiar menus, ribbon controls, document tabs, and printable pages
- Rich-text formatting, paragraph styles, lists, tables, links, and images
- Print, PDF export, headers, footers, page numbers, and page layout controls
- Comments, Track Changes, document comparison, references, and citations
- Find and replace with case, whole-word, regular-expression, and selection options
- Local recovery, version history, templates, backups, and automatic saving
- Print, Web, Draft, Outline, Reading, and Focus views
- English, Spanish, and Arabic interfaces with right-to-left support
- Local spelling, writing suggestions, dictionary, thesaurus, and autocorrect tools
- Optional local OCR, Windows dictation, text-to-speech, and Ollama assistance
- Optional self-hosted collaboration and restricted local extensions
- Editable text support for 88 document, data, configuration, and programming extensions

## 🆕 What Changed In 2.5.22

### Updater repair

- Changed the official application and updater destination to `KernFerm/BubblesWordWriter`.
- Removed the obsolete `bubblesthedev/bubbles-writer` address from the current build.
- Prevented raw GitHub response headers, authentication details, and server output from appearing in the Software Update window.
- Added a clear message when a release supports manual installation but does not provide automatic-update metadata.
- Added regression coverage for missing GitHub release information.

### Documentation

- Rebuilt the end-user guide with clearer installation, writing, privacy, recovery, troubleshooting, and uninstall instructions.
- Documented all 88 file extensions accepted by the application.
- Updated repository links, version information, installer details, and release guidance.

### Packaging

- Updated the installer license to version `2.5.22`.
- Rebuilt the protected Windows x64 application and NSIS installer.
- Verified that the packaged updater points to `KernFerm/BubblesWordWriter`.

## ✍️ Writing And Editing

Bubbles Word Writer provides everyday desktop writing tools without requiring an online service:

- Font family, size, color, highlighting, bold, italic, underline, and strikethrough
- Superscript, subscript, alignment, spacing, indentation, and text direction
- Headings, paragraph styles, bulleted lists, numbered lists, and task lists
- Tables with row, column, cell, border, shading, alignment, sorting, and formula tools
- Images with crop, rotation, flip, wrapping, opacity, brightness, contrast, and compression
- Shapes, decorative text, equations, symbols, links, captions, and page breaks
- Reusable templates and customizable keyboard shortcuts, toolbar items, and ribbon groups

## 📚 References And Review

- Table of contents
- Footnotes and endnotes
- Captions and tables of figures
- Bookmarks and cross-references
- Citations, bibliography libraries, and indexes
- Comments, replies, resolution, and reopening
- Track Changes with individual and bulk accept/reject controls
- Document comparison and revision combination
- Mail merge from XLSX, CSV, and JSON data
- Printable envelopes and label sheets

## 📁 Document Compatibility

The application opens and saves its native `.btw` format plus common Word Open XML, OpenDocument, RTF, Markdown, HTML, plain-text, data, configuration, and programming-language files.

Use `.btw` for the most complete preservation of Bubbles Word Writer features. Complex DOCX, ODT, or legacy DOC content may be simplified when the source format contains features that do not have an exact equivalent. Legacy `.doc` conversion has the best results when LibreOffice is installed locally.

See the [complete supported-file table](README.md#-supported-file-types) for all 88 accepted extensions.

## 🔒 Privacy

- No required account or sign-in
- No advertising
- No publisher-operated telemetry or analytics
- No sale or collection of document content
- No automatic cloud upload
- Documents and application data remain on the local device by default

Network access occurs only after a user requests a network feature, such as checking for updates, opening an external link, or joining a specified collaboration server.

## 🛠️ Install Or Upgrade

1. Save all open documents.
2. Close Bubbles Word Writer.
3. Download the `2.5.22` installer using the button at the top of this page.
4. Run `Bubbles-Word-Writer-Setup-2.5.22.exe`.
5. Read and accept the license agreement.
6. Complete the installation and launch the application.

Installing over an older version upgrades the application while preserving saved documents and normal application data.

The application installs for the current Windows user at:

```text
%LOCALAPPDATA%\Programs\Bubbles Word Writer
```

## 🔄 Update Behavior

The `2.5.22` GitHub release contains only the Windows EXE installer. Automatic downloading through Electron Updater requires additional metadata that is intentionally not included in an installer-only release.

When **Help > Check for Updates** cannot find compatible automatic-update metadata, the application displays a friendly message instead of technical GitHub output. Install future versions by downloading and running their newer installer.

## ✅ Release Validation

- TypeScript validation passed
- `123` automated tests passed
- `136` native menu commands validated
- `116` renderer controls validated
- `158` Command Search entries validated
- `673` static interface strings validated in English, Spanish, and Arabic
- Protected Electron build completed successfully
- Windows NSIS installer completed successfully
- Packaged updater destination verified as `KernFerm/BubblesWordWriter`

## 🔐 Installer Verification

SHA-256 for `Bubbles-Word-Writer-Setup-2.5.22.exe`:

```text
B6B36BF737520B2E9DD678A004934A2C212C383B7B6153D288FD929D4647CBE1
```

The installer is intentionally not digitally signed. Windows may display a Microsoft Defender SmartScreen warning. Download the installer only from the official `KernFerm/BubblesWordWriter` repository.

## ⚠️ Known Limitations

- Installer-only releases require manual downloading and installation.
- Complex DOCX and ODT layouts may not round-trip perfectly.
- Legacy `.doc` files are import-only and may lose formatting without LibreOffice.
- Password encryption applies to native `.btw` documents, not encrypted Office files.
- PDF is an export and print format, not an editable import format.
- Collaboration requires a separately operated Yjs-compatible server.
- The installer is unsigned.

## 🗑️ Uninstalling

Open **Windows Settings > Apps > Installed apps**, select **Bubbles Word Writer**, and choose **Uninstall**.

The uninstaller can optionally remove settings, recovery and history data, templates, clipboard history, extensions, and cached profile data. These choices are unchecked by default. Documents saved outside the application profile are never removed.

## 🆘 Help And Information

- [User Guide](README.md)
- [Privacy Policy](PRIVACY.md)
- [Security Information](SECURITY.md)
- [Complete Changelog](CHANGELOG.md)
- [GitHub Repository](https://github.com/KernFerm/BubblesWordWriter)

Made by **bubblesthedev**.
