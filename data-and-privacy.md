# Data & Privacy

Nexus is local-first: your notes, browsing history, bookmarks, and chat history are stored in a single SQLite database on your own device. Nexus does not operate a server, does not require an account, and does not sync your data anywhere by default.

## Where Things Are Stored

| Data | Where |
|---|---|
| Notes, folders, tags, links, chat history, version history | Local SQLite database (`nexus.db`) in your OS's standard app-data directory |
| Note search index (embeddings) | Same local database |
| Gemini API key | Your OS's native secure credential store (Keychain / Credential Manager / Secret Service) — **not** the database, and not `localStorage` |
| Bookmarks, downloads history, browser homepage, theme, editor preferences | Local browser storage within the app |

## What Ever Leaves Your Device

Nothing does, **unless you use the Assistant**. Browsing pages, taking notes, using the knowledge graph, exporting to Markdown/PDF, and backing up your database are all fully offline operations.

When you send a message to the Assistant, exactly the following is transmitted directly from your device to Google's Gemini API, using your own API key:

- The note snippets Nexus's local search determined were relevant to your question (not your entire note collection)
- Your question and the current conversation's message history
- If you've enabled "Aware of tabs" for that conversation, the text of your currently open browser tab(s)

Nothing else — other notes, folders, browsing history outside the active toggle, or anything else in your local database — is ever included in a request. Note search itself (deciding *which* notes are relevant) runs entirely on your device via a local embedding model; the search process itself makes no network call.

## The Contradiction Watcher

The background contradiction-checking feature (see [Features](features.md#contradiction-watching)) follows the same rule: the free, local similarity comparison never leaves your device. Only the second stage — a compact yes/no check against the single best-matching note — is sent to Gemini, and only when the feature is enabled and a plausible match has already been found locally.

## Your API Key

Your Gemini API key is stored using your operating system's native credential storage APIs, via the same mechanism as password managers and other credential-aware apps. It is never written to Nexus's database, never included in exports or backups, and never leaves your device except as the authentication header on your own direct requests to Google.

## Backups and Exports

Database backups and Markdown/PDF exports are files written to a location you choose on your own device. Nexus does not upload them anywhere. If you back up to cloud storage (Dropbox, iCloud, a NAS, etc.), that's a choice you make outside the app — Nexus has no awareness of or involvement in where you save these files.

## Third-Party AI Provider

When the Assistant is used, your data is subject to Google's own terms and privacy policy for the Gemini API, since that request goes directly from your device to Google. Nexus has no visibility into, and no involvement in, how Google processes that request beyond what you send it.
