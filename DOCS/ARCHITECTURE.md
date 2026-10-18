# Architecture

The application is split into three layers:

- `src/main`: Electron main process, native windows, application menus, settings persistence, file dialogs, safe saving, and update orchestration.
- `src/preload`: a narrow `window.writer` API exposed through Electron context isolation.
- `src/renderer`: the desktop editor interface and TipTap structured document editing surface.

Shared TypeScript contracts live in `src/shared` so IPC requests, document data, format conversion helpers, and built-in templates stay typed on both sides.

The renderer owns editor transactions, command search, find/replace, page layout controls, and active tab state. The main process owns native dialogs, atomic recovery and version-history journals, filesystem reads and writes, PDF generation, printing, settings persistence, shell integration, menus, and updater orchestration.

Print Layout uses `tiptap-pagination-plus` for measurement-driven page boundaries without placing generated page chrome in the saved ProseMirror document. Document paper dimensions and margins update the pagination engine in pixels, while sanitized document fields populate repeating headers and footers. A companion ProseMirror decoration plugin measures manual `pageBreak` nodes against generated boundaries, so explicit breaks participate in live editing but remain clean structured nodes for save and export. Page-marker rebuilds after document shrink are visual-only transactions excluded from undo history. Web, Draft, and Outline modes disable pagination and use continuous layout.

Optional collaboration binds the active ProseMirror document directly to a Yjs `XmlFragment`. `y-websocket` provides awareness, reconnect, and transport to a user-supplied self-hosted endpoint; Yjs resolves concurrent and offline edits. Collaboration is never started automatically, sessions are scoped to one active tab, and access tokens remain in memory. `server/collaboration-server.mjs` provides an authenticated, persistent self-hosted endpoint with atomic room snapshots, payload and connection limits, heartbeat cleanup, a content-free health endpoint, and graceful shutdown.

## Extension isolation

Declarative extension data is normalized in `src/shared/extensions.ts`. Native executable commands cross a narrow IPC contract into `ExtensionService`, which re-reads the installed manifest, verifies enabled and trusted state, enforces declared document permissions, and delegates to `ExtensionRuntimeService`. The runtime validates the entry path and SHA-256 integrity before creating a disposable sandboxed `BrowserWindow` in a unique in-memory session. It exposes no Node.js or Electron API, blocks navigation and direct network access, and provides only a sender-bound permission bridge from `src/preload/extension-runtime-preload.ts`. The bridge limits files to extension-private storage, HTTPS JSON requests to declared public hosts, and bounded text clipboard operations. Source, input, output, execution time, and working-set usage are bounded, and the process is destroyed after every command. VS Code integration parses snippets only and never executes VS Code extension hosts or modules.

Background document statistics and writing analysis are isolated behind `DocumentWorkerClient` in `src/renderer/document-worker-client.ts`; the worker implementation remains in `document-worker.ts`. This keeps worker lifecycle and failure recovery outside the main editor controller and is the first boundary used for continued renderer modularization.

## Internationalization

`src/shared/i18n.ts` is the locale boundary shared by the main and renderer processes. It validates persisted locale choices, resolves the Windows language when System is selected, supplies translation resources with English fallback text, reports interface direction, and centralizes locale-aware date and number formatting.

The main process rebuilds the native application menu whenever settings change. The renderer applies `lang` and `dir` to the document root and translates marked interface controls. Interface direction is deliberately separate from editor content: paragraphs, tables, and cells retain their own automatic, LTR, or RTL attributes in the structured document model and supported export formats.
