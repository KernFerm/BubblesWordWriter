# 🫧 Bubbles Word Writer

**Bubbles Word Writer** is a private, local-first word processor for Windows 10 and Windows 11. It combines the familiar feel of an old-school desktop word processor with modern document tools.

There is no required account, advertising, telemetry, analytics, or automatic cloud upload. Your documents remain on your computer unless you deliberately save them to a synchronized folder or connect to a collaboration server.

## ✨ What You Can Do

- Write letters, reports, notes, resumes, books, and source code
- Open several documents in closable tabs
- Format text, paragraphs, headings, lists, links, tables, and images
- Insert comments, citations, footnotes, endnotes, captions, headers, and footers
- Find and replace text, including case-sensitive and whole-word searches
- Review spelling, grammar suggestions, definitions, synonyms, and antonyms
- Use local recovery, version history, templates, and automatic saving
- Print documents or export them as PDF files
- Work in Print, Web, Draft, Outline, Reading, or Focus view
- Use optional local OCR, dictation, text-to-speech, and Ollama writing assistance
- Collaborate through a server that you or your organization controls

## 🚀 Download And Install

Download the latest installer from the official [GitHub Releases page](https://github.com/KernFerm/BubblesWordWriter/releases/latest).

1. Download `Bubbles-Word-Writer-Setup-2.5.22.exe`.
2. Open the downloaded installer.
3. Read and accept the license agreement.
4. Follow the installation prompts.
5. Open **Bubbles Word Writer** from the Start menu or desktop shortcut.

The application installs for the current Windows user in:

```text
%LOCALAPPDATA%\Programs\Bubbles Word Writer
```

The installer is intentionally unsigned. Windows may display a Microsoft Defender SmartScreen warning. Only download Bubbles Word Writer from the official repository above.

## 📝 Create Your First Document

1. Open Bubbles Word Writer.
2. Click the white page and begin typing.
3. Use the ribbon or menus to format your document.
4. Choose **File > Save**.
5. Select a folder, file name, and document format.

An asterisk (`*`) in a document tab means it contains unsaved changes. If you close a changed document, the application asks whether you want to save it.

## 🧭 Find Your Way Around

### Tabs

Each open document has its own tab. Select a tab to switch documents or use its `X` button to close it.

### Ribbon and menus

The ribbon contains the most common writing and formatting tools. The menus provide the complete command list, including document settings, references, review tools, printing, and help.

### Writing page

The white page is your document. Select text before changing its font, size, color, alignment, or other formatting.

### Status bar

The status bar shows the save state, page number, word and character counts, reading time, language, view, and zoom level.

### Views

Open the **View** menu to choose:

- **Print Layout** for editable pages with page boundaries
- **Web Layout** for continuous screen-friendly writing
- **Draft View** for a simplified writing surface
- **Outline Mode** for organizing document headings and sections
- **Reading Mode** for comfortable reading
- **Focus Mode** for distraction-reduced writing

## 💾 Open, Save, And Export

- **Save** updates the current file.
- **Save As** selects a new name, folder, or format.
- **Save Copy** creates another copy without changing the current document.
- **Save All** saves every changed tab.
- **Export PDF** creates a PDF for sharing or printing.
- **Print** provides page range, copies, collation, color, duplex, scale, and pages-per-sheet controls.

Use the native `.btw` format when you want the best preservation of Bubbles Word Writer features.

## 📁 Supported File Types

| Category | Supported file types | What Bubbles Word Writer does |
| --- | --- | --- |
| Bubbles document | `.btw` | Opens and saves the complete native document structure |
| Microsoft Word Open XML | `.docx`, `.docm`, `.dotx`, `.dotm` | Opens and saves common Word content; macros are never executed or preserved |
| Legacy Microsoft Word | `.doc` | Imports using LibreOffice when available, with a readable-text fallback |
| OpenDocument | `.odt` | Opens and saves common OpenDocument text and layout content |
| Rich Text Format | `.rtf` | Opens and saves common rich-text formatting |
| Markdown | `.md`, `.markdown`, `.mdown`, `.mkd` | Opens and saves Markdown |
| Web documents | `.html`, `.htm`, `.xhtml` | Opens and saves sanitized HTML |
| Plain text and notes | `.txt`, `.text`, `.log`, `.nfo` | Opens and saves plain text |
| Data files | `.csv`, `.tsv`, `.json`, `.jsonl`, `.xml` | Opens and saves editable data text |
| Configuration files | `.yaml`, `.yml`, `.toml`, `.ini`, `.cfg`, `.conf` | Opens and saves editable configuration text |
| Document markup | `.tex`, `.rst`, `.adoc`, `.org` | Opens and saves editable markup text |
| JavaScript and TypeScript | `.js`, `.jsx`, `.ts`, `.tsx`, `.mjs`, `.cjs` | Opens and saves editable source text |
| Web styles and components | `.css`, `.scss`, `.sass`, `.less`, `.vue`, `.svelte`, `.astro` | Opens and saves editable source text |
| Python | `.py`, `.pyw` | Opens and saves editable source text |
| Java and .NET | `.java`, `.cs`, `.fs`, `.fsx`, `.vb` | Opens and saves editable source text |
| C, C++, and Objective-C | `.c`, `.h`, `.cpp`, `.cc`, `.cxx`, `.hpp`, `.m`, `.mm` | Opens and saves editable source text |
| Go, Rust, Swift, Kotlin, and Dart | `.go`, `.rs`, `.swift`, `.kt`, `.kts`, `.dart` | Opens and saves editable source text |
| PHP, Ruby, Lua, Perl, R, and Scala | `.php`, `.rb`, `.lua`, `.pl`, `.pm`, `.r`, `.scala` | Opens and saves editable source text |
| Erlang, Elixir, and Clojure | `.erl`, `.ex`, `.exs`, `.clj`, `.cljs` | Opens and saves editable source text |
| Shell and command scripts | `.sh`, `.bash`, `.zsh`, `.fish`, `.ps1`, `.bat`, `.cmd` | Opens and saves editable script text |
| Database scripts | `.sql` | Opens and saves editable SQL text |
| PDF output | `.pdf` | Exports and prints PDF output; PDF files are not opened for editing |

Legacy `.doc` files are import-only. Complex Word and OpenDocument layouts may be simplified, so keep the original file and review converted copies before replacing anything important.

## 🖼️ Images, Tables, And Page Layout

Use **Insert > Image** to add a picture. Image Properties provides resizing, rotation, flipping, cropping, wrapping, opacity, brightness, contrast, and compression without changing the original picture file.

Table tools add or remove rows and columns, merge or split cells, repeat headers, calculate formulas, sort data, and control borders, shading, padding, alignment, and text direction.

Use **File > Page Layout** to set paper size, orientation, margins, columns, page borders, and other print settings. Headers and footers can contain title, author, date, time, and page-number fields.

## 🔎 Find And Replace

- Press `Ctrl+F` to find text.
- Press `Ctrl+H` to find and replace text.
- Choose case-sensitive, whole-word, regular-expression, or selection-only matching when needed.

The Find window stays compact and does not cover the document.

## ✅ Proofing And Review

Open **File > Settings** to select a proofing language, maintain autocorrect rules, and edit your personal dictionary.

Review tools include spelling and writing suggestions, an offline English dictionary and thesaurus, threaded comments, Track Changes, document comparison, and accessibility checks.

English, Spanish, and Arabic interface resources are included. Arabic supports a right-to-left interface, while individual paragraphs and table cells can keep their own reading direction.

## ♿ Accessibility

Bubbles Word Writer includes keyboard navigation, accessible labels, scalable controls, stronger contrast, reduced motion, editor font choices, and document accessibility checks.

The accessibility checker looks for issues such as missing image descriptions, unclear links, heading-order problems, missing table headers, and low-contrast text.

## 🛟 Recovery And Version History

Recovery information is stored locally. After an unexpected shutdown, Document Recovery lets you preview and restore unsaved work without automatically overwriting the original file.

Optional local version history and backup copies can be configured in **File > Settings**. Recovery is helpful, but it is not a replacement for saving important documents normally.

## 🔄 Updates

Choose **Help > Check for Updates** to check the official [GitHub Releases page](https://github.com/KernFerm/BubblesWordWriter/releases).

The current public release contains only the Windows installer. When automatic-update metadata is not published, the application displays a friendly message directing you to GitHub Releases. Download and run the newer installer manually; your settings and documents are preserved.

## 🔒 Privacy

- No required account or sign-in
- No advertising
- No telemetry or analytics
- No sale of user data
- No automatic document upload

Documents stay where you save them. Settings, recovery information, templates, clipboard history, and local extensions remain in the application profile on your computer.

Network access occurs only when you request an action that needs it, such as checking for updates, opening an external link, connecting to your own collaboration server, or saving into a cloud-synchronized folder.

Read the complete plain-language [Privacy Policy](PRIVACY.md).

## 🧩 Extensions And VS Code

Open **Tools > Extensions** to manage local Bubbles Word Writer extensions. Supported extensions can contribute templates, snippets, themes, and commands.

If Visual Studio Code is installed, Bubbles Word Writer detects its normal extension folders and makes compatible snippets available. VS Code executable extension code is not run inside Bubbles Word Writer.

Executable Bubbles extensions remain disabled until explicitly trusted. They run with restricted permissions, integrity checks, resource limits, and isolated access to approved capabilities.

## 🧰 Optional Local Tools

### Local writing assistant

Install Ollama separately, enable **Local AI** in Settings, and enter an installed model name. Requests are restricted to the local Ollama address at `127.0.0.1:11434`.

### OCR

Choose **Tools > Extract Text from Image** to recognize text using the Windows OCR languages installed on your computer.

### Dictation and speech

Choose **Tools > Dictation** to recognize one passage using Windows speech recognition. Review the result before inserting it. Text-to-speech can read selected text or the active document aloud.

### Collaboration

Choose **Tools > Live Collaboration** to connect to a Yjs-compatible server that you or your organization controls. Collaboration is off until you press **Connect**. The publisher does not operate a document collaboration service.

## 🧰 Troubleshooting

### The application will not open

Restart Windows and try again. If the problem continues, download a fresh installer from the official Releases page and reinstall it. Windows may warn because the installer is unsigned.

### Typing, scrolling, or moving the window feels slow

Close unusually large documents and unused tabs, then restart the application. If moving the window stutters, open **File > Settings**, turn off **Use hardware acceleration**, save the setting, and restart.

### A document will not open

Confirm that the file is supported, not damaged, and not locked by another application. Encrypted Microsoft Office and OpenDocument files are not supported.

### Formatting changed after conversion

Save your working document as `.btw` for the best preservation. Complex features from other word processors may not have an exact Bubbles Word Writer equivalent.

### Saving or exporting fails

Choose a folder where your Windows account has permission to write. Check available disk space and make sure another application is not locking the destination file.

### Check for Updates reports no compatible automatic update

This means the GitHub release contains a manual installer but not automatic-update metadata. Open the official Releases page, download the newest EXE, close Bubbles Word Writer, and run the installer.

### Recovery keeps appearing

Recover or discard the offered documents, save anything important, and close the application normally. Saved documents outside the application profile are never removed by recovery cleanup.

## 🗑️ Uninstalling

Open **Windows Settings > Apps > Installed apps**, find **Bubbles Word Writer**, and choose **Uninstall**.

The uninstaller can independently remove application settings; recovery data, version history, templates, and clipboard history; or extensions and cached profile data. These options are unchecked by default. Documents saved elsewhere are not removed.

## 👩‍💻 Developer Quick Start

Bubbles Word Writer uses Electron, TypeScript, Vite, TipTap, Vitest, Playwright, and Electron Builder.

```powershell
npm install
npm start
```

Validate and package the project:

```powershell
npm test
npm run lint
npm run security:audit
npm run prepare:protected
npm run pack:protected
npm run dist:protected
```

Developer documentation is available in [Architecture](ARCHITECTURE.md), [Security](SECURITY.md), [Contributing](CONTRIBUTING.md), and [Building](../BUILDING.md).

## ⚠️ Important Limitations

- Complex DOCX, ODT, and legacy DOC documents may not preserve every advanced layout or drawing.
- Legacy `.doc` conversion is best when LibreOffice is installed locally.
- Password encryption is supported for native `.btw` documents, not encrypted Office files.
- Collaboration requires a separately operated server.
- The installer is not digitally signed.
- Installer-only GitHub releases require manual updates.

## 📄 License And Notices

The source code is available under the [MIT License](../LICENSE). Official installers display the [End User License Agreement](../build/license.txt) before installation. Third-party notices are available in [THIRD_PARTY_NOTICES.txt](../THIRD_PARTY_NOTICES.txt).

## 👤 Author

Made by **bubblesthedev**.

Current version: **2.5.22**
