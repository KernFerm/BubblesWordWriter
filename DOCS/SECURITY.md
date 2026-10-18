# Security

## Reporting a vulnerability

Use GitHub's private vulnerability reporting for `KernFerm/BubblesWordWriter` when it is enabled. Do not include exploit details, private documents, credentials, or access tokens in a public issue. Include the affected version, impact, reproduction steps using non-sensitive data, and any proposed mitigation. Security reports are reviewed before public disclosure.

Bubbles Word Writer uses Electron with context isolation, disabled renderer Node integration, renderer sandboxing, a strict preload bridge, blocked arbitrary navigation, and a restrictive Content Security Policy.

Documents are treated as data. Imported HTML is sanitized before saving or conversion, and document contents are not executed.

Privileged operations such as file access, shell integration, and update checks live in the main process behind narrow IPC methods.

Local structured logs are size-bounded and rotated. Sensitive context fields, authorization values, secret URL parameters, and operating-system account names in paths are redacted before an entry is written. Logs are never uploaded by the application.

The optional local AI bridge is disabled by default and hard-coded to the IPv4 loopback Ollama endpoint. It rejects redirects, limits prompt and response sizes, applies a two-minute timeout, and never accepts a renderer-supplied URL.

Live Collaboration is opt-in and uses the established Yjs CRDT with `y-prosemirror` and `y-websocket`. Remote endpoints must use WSS; plaintext WebSockets are restricted to loopback hosts. Endpoint URLs cannot contain embedded credentials, query parameters, or fragments. An optional access token is sent as a connection parameter, retained only in memory, and never written to settings or documents. Password-protected and read-only documents are blocked, and the active session is destroyed before switching tabs. The included self-hosted server supports a shared token or a server-owned authorization file with SHA-256 token hashes, exact or prefix room rules, editor/viewer roles, constant-time hash comparison, bounded payloads and connections, heartbeat cleanup, atomic local persistence, native TLS through `BWW_COLLAB_TLS_CERT` and `BWW_COLLAB_TLS_KEY`, and graceful shutdown. Viewers can synchronize and publish presence but server-side protocol enforcement rejects document updates. A non-loopback listener without native TLS starts only when `BWW_COLLAB_TRUST_PROXY_TLS=1` confirms trusted TLS termination. Deployments remain responsible for token rotation, account provisioning, backups, monitoring, and operating-system hardening.

Extensions use an explicit permission allowlist. Declarative commands and templates require `document:modify`; unknown permissions are discarded. Native executable commands additionally require an API-v1 runtime manifest, a SHA-256 integrity value, and a separate persisted trust decision. Each invocation runs in a new hidden, sandboxed Chromium renderer with Node.js and Electron disabled, all direct navigation and network requests denied, a dedicated in-memory session, bounded source/input/output sizes, and enforced execution-time and working-set limits. The host passes document or selection text only when `document:read` is granted. A sender-bound preload bridge mediates extension-private text storage, bounded clipboard text, and HTTPS JSON requests to exact manifest-declared public hosts; it rejects path traversal, redirects, and private-address network resolution. The sandbox is destroyed and its browser storage cleared after each invocation. Detected VS Code snippets are parsed as bounded text contributions; VS Code executable code is never loaded.

## Automated scanning

Run local dependency and source checks with:

```powershell
npm run security:audit
npm run security:audit:tooling
npm run security:snyk
npm run security:snyk:tooling
npm run security:snyk:code
```

`security:audit` and `security:snyk` are blocking checks for dependencies shipped inside the application. Their `:tooling` counterparts separately report development and packaging dependencies. The exact application and Electron versions are recorded in `package.json`; release validation rejects mismatched tags and metadata.

The local Snyk policy records one narrow, expiring risk acceptance for `deepmerge` through `sanitize-html`. The sanitizer receives only application-owned literal option objects, never parsed document objects, so the vulnerable merge path is not attacker-controlled in Bubbles Word Writer. The exception expires on January 31, 2027 and must be removed or reevaluated when the dependency publishes a fix.

Upload dependency monitoring and source findings to the authenticated Snyk account with:

```powershell
npm run security:snyk:monitor
npm run security:snyk:report
```

Snyk Code exclusions are defined in `.snyk`. Dependency folders, generated builds, installers, runtime profiles, Git metadata, and coverage output are excluded from source upload. Never commit or print `SNYK_TOKEN`; configure it as a Snyk CLI credential or GitHub Actions secret.
## Protected release builds

Production builds use `npm run dist:protected`. This pipeline minifies and mangles compiled main-process and preload JavaScript, removes comments and debugger statements, omits application source maps, and packages the app in an integrity-checked ASAR archive. Electron's `RunAsNode`, Node options environment variable, and command-line inspector fuses are disabled, and the executable only loads the embedded ASAR application.

The TypeScript source tree, tests, and build scripts are not included in the installer. Runtime dependencies remain packaged because the application requires them. These measures make inspection and modification harder, but they are not encryption and cannot guarantee that client-side code is unrecoverable. Secrets and signing credentials must never be embedded in the application.

