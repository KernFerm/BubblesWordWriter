# 🎉 Bubbles Word Writer 2.5.22

Version **2.5.22** is the current Windows release of Bubbles Word Writer.

## ⬇️ Download

Download the installer from the official [GitHub Releases page](https://github.com/KernFerm/BubblesWordWriter/releases/latest):

```text
Bubbles-Word-Writer-Setup-2.5.22.exe
```

The release contains only the Windows installer. It does not contain source code, documents, settings, recovery information, credentials, or other user data.

## ✨ What Changed

- Updated the application to use the official `KernFerm/BubblesWordWriter` repository.
- Removed raw GitHub response headers and technical server output from updater messages.
- Added a clear message when a release supports manual installation but not automatic updating.
- Added an automated test covering missing GitHub release metadata.
- Updated the installer license and release documentation for version `2.5.22`.

## 🛠️ Install Or Upgrade

1. Save your open documents.
2. Download `Bubbles-Word-Writer-Setup-2.5.22.exe`.
3. Close Bubbles Word Writer.
4. Run the downloaded installer.
5. Follow the installation prompts.

Installing over an existing copy upgrades the application while preserving saved documents and normal application data.

## 🔄 About Check For Updates

The current GitHub release contains only the EXE installer. **Help > Check for Updates** can reach the correct repository, but automatic downloading requires additional updater metadata that is not included in an installer-only release.

When that metadata is unavailable, Bubbles Word Writer displays a friendly message directing the user to GitHub Releases. Download and run the latest installer manually.

## 🔐 Privacy And Security

- No telemetry or analytics were added.
- No documents or user data are included in the release.
- No account is required to use the application.
- The installer is intentionally unsigned, so Windows may display a SmartScreen warning.
- Download the installer only from `KernFerm/BubblesWordWriter`.

Installer SHA-256:

```text
B6B36BF737520B2E9DD678A004934A2C212C383B7B6153D288FD929D4647CBE1
```

## ✅ Validation

- TypeScript validation passed.
- All `123` automated unit tests passed.
- Command and interface control validation passed.
- English, Spanish, and Arabic resource validation passed.
- Protected Windows packaging completed successfully.
- The packaged updater configuration points to `KernFerm/BubblesWordWriter`.

## 🆘 Need Help?

Start with the [User Guide](README.md) and its troubleshooting section. Security concerns should follow the private reporting guidance in [SECURITY.md](SECURITY.md).
