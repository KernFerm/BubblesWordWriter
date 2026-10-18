# Privacy

Bubbles Word Writer is a private, local-first desktop editor. It does not require an account or cloud storage.

## What Bubbles Word Writer Does Not Collect

Bubbles Word Writer contains no Publisher-operated telemetry, analytics, advertising, behavioral tracking, or document-content collection. The Publisher does not receive, sell, rent, monetize, or disclose your documents, settings, recovery files, templates, clipboard history, extension profile, or usage activity.

## Where Your Data Stays

Application-managed data remains on your local device by default. Documents stay wherever you choose to save them. Settings, recovery data, local version history, templates, clipboard history, and extension profile information are stored in the application's private Windows profile folder.

The uninstaller lets you choose whether to keep or remove settings, recovery data, and extension/profile data.

## Actions You Control

Bubbles Word Writer does not automatically upload your documents. It can communicate with another service only when you deliberately request or configure an action that requires it, such as:

- choosing **Check for Updates**;
- opening an external website or email link;
- saving into a OneDrive or other cloud-synchronized folder;
- using an operating-system print, share, or export destination; or
- connecting the active document to a self-hosted collaboration server whose address you entered; or
- installing or managing content obtained from an external extension source.

The optional Local Writing Assistant connects only to an Ollama service at `127.0.0.1:11434` after the user enables it and presses Run. The selected document text is processed by that locally installed model and is not sent to the Publisher or to a configurable remote AI server.

Image text recognition uses the Windows OCR runtime and locally installed recognition languages. The selected image is not uploaded by Bubbles Word Writer.

Dictation uses the Windows `System.Speech` recognizer and the computer's default microphone. Bubbles Word Writer does not record an audio file or upload microphone audio.

Live Collaboration is off until you press **Connect**. While connected, the active document's structured content, comments, cursor position, display name, and cursor color are exchanged with the Yjs-compatible WebSocket server and other participants in that room. Remote endpoints must use encrypted `wss://`; plaintext `ws://` is restricted to the local computer. The Publisher does not operate the server, receive a copy, or add telemetry to the session. The server operator controls its authentication, retention, logging, and privacy practices.

Those actions may send standard network request information or content you intentionally choose to the service involved. They do not send your documents to the Publisher as telemetry. Any third-party service is governed by its own privacy terms.
