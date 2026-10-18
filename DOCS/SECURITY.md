# Security Policy

The security and privacy of Bubbles Word Writer users are taken seriously. This policy explains which releases receive security fixes, how to report a vulnerability privately, and what reporters can expect after submitting a report.

## Supported Versions

Security fixes are provided for the latest published release.

| Version | Supported |
| --- | --- |
| 2.5.x | Yes |
| 2.4.x and earlier | No |

Users should install the newest available version before reporting a problem that may already have been corrected.

## Reporting A Vulnerability

Do not report security vulnerabilities in a public issue, discussion, pull request, or social-media post.

Use GitHub's private vulnerability reporting feature:

1. Open the [Bubbles Word Writer Security page](https://github.com/KernFerm/BubblesWordWriter/security).
2. Select **Report a vulnerability**.
3. Submit the report privately through the security advisory form.

If private vulnerability reporting is temporarily unavailable, contact the repository owner privately through the [KernFerm GitHub profile](https://github.com/KernFerm). Do not publish exploit details while trying to make contact.

## What To Include

A useful report should contain:

- The affected Bubbles Word Writer version
- The Windows version and system architecture
- A clear description of the vulnerability and its possible impact
- Exact steps needed to reproduce the problem
- Whether user interaction is required
- A minimal proof of concept using non-sensitive sample data
- Relevant screenshots or redacted diagnostic output
- Any suggested mitigation or correction

Do not submit real documents, passwords, access tokens, private collaboration room names, personal information, or other confidential data.

## Response Process

After a private report is received:

1. The report will be reviewed and its receipt acknowledged when possible.
2. The issue will be reproduced and its severity evaluated.
3. The reporter may be asked for additional non-sensitive information.
4. A correction or mitigation will be developed and tested when the issue is confirmed.
5. A security release and advisory will be prepared when appropriate.
6. Public disclosure will occur after users have had a reasonable opportunity to update.

Response and correction times depend on severity, reproducibility, affected components, and the availability of a safe fix. Submitting a report does not guarantee that it will be accepted as a vulnerability.

## Security Scope

Reports are welcome for security problems involving:

- The Windows installer or application update flow
- Document opening, conversion, saving, printing, or export
- Malicious DOCX, ODT, RTF, HTML, Markdown, image, or native `.btw` files
- Password-protected native documents
- Recovery data, settings, logs, or version history
- Electron IPC boundaries and renderer isolation
- Extension permissions, integrity checks, and sandbox escape
- Clipboard, filesystem, or network mediation for extensions
- Collaboration authentication, authorization, room isolation, or persistence
- Local AI, OCR, dictation, or text-to-speech boundaries
- Exposure of document content, credentials, or private local paths

## Generally Out Of Scope

The following are normally not treated as application vulnerabilities unless they create a separate security impact in Bubbles Word Writer:

- Microsoft Defender SmartScreen warnings caused by the intentionally unsigned installer
- Issues requiring an attacker to already have unrestricted administrator access to the computer
- Social engineering without a technical application vulnerability
- Denial of service requiring intentionally opening an extremely large trusted document
- Vulnerabilities found only in unsupported versions
- Findings in third-party services that do not affect Bubbles Word Writer
- Missing features, formatting differences, or general software bugs without a security impact
- Automated scanner output without a reproducible vulnerable path

## Safe Research Guidelines

Security research must:

- Use systems and data you own or have permission to test
- Avoid accessing, changing, or deleting another person's data
- Avoid privacy violations, service disruption, and destructive testing
- Stop testing if sensitive user information is encountered
- Allow reasonable time for investigation and correction before disclosure
- Follow applicable laws and platform terms

Good-faith research that follows these guidelines will be treated respectfully. This policy does not authorize testing against systems, accounts, or collaboration servers operated by other people.

## Privacy And Data Handling

Bubbles Word Writer does not include publisher-operated telemetry, analytics, advertising, or document-content collection. Security reports and diagnostics should therefore be prepared manually and reviewed before submission.

Local logs redact authorization values, sensitive URL parameters, and operating-system account names in paths. Reporters should still inspect every attachment and remove confidential information before sending it.

See the [Privacy Policy](PRIVACY.md) for more information about local data and optional network features.

## Application Security Measures

Current production protections include:

- Electron context isolation and renderer sandboxing
- Disabled renderer Node.js integration
- A narrow preload API and validated IPC requests
- Sanitized imported HTML and non-executable document content
- Atomic document, recovery, and history writes
- Restricted navigation and Content Security Policy controls
- Redacted, bounded, locally stored diagnostic logs
- Integrity-pinned and permission-limited executable extensions
- Disposable extension sandboxes with time, memory, input, and output limits
- HTTPS-only extension networking to explicitly approved public hosts
- Loopback-only local AI access
- Encrypted remote collaboration transport requirements
- Protected production packaging and Electron fuse hardening

These protections reduce risk but do not guarantee that the software is free of vulnerabilities.

## Dependency And Source Scanning

Maintainers can run the project's security checks with:

```powershell
npm run security:audit
npm run security:audit:tooling
npm run security:snyk
npm run security:snyk:tooling
npm run security:snyk:code
```

Dependency folders, generated builds, installers, local runtime profiles, Git metadata, and coverage output are excluded from Snyk source upload. Credentials such as `SNYK_TOKEN` must never be committed, printed, or included in reports.

## Installer Authenticity

Official installers are published through the [Bubbles Word Writer repository](https://github.com/KernFerm/BubblesWordWriter). The current installer is intentionally unsigned, so Windows may show a SmartScreen warning.

The expected SHA-256 value for version `2.5.22` is documented in [RELEASE.md](RELEASE.md). Compare the complete hash before running a downloaded installer when independent verification is required.

## Disclosure And Credit

Confirmed vulnerabilities may be documented in a GitHub security advisory or release notes after a correction is available. Reporters who want recognition may request credit in the advisory. Anonymous reporting and anonymous credit requests will also be respected where GitHub permits them.
