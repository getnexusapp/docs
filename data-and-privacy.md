# Data & Privacy

Nexus's notes, browsing history, bookmarks, and locally saved chat history are stored in a single SQLite database on your own device. That part of Nexus requires no account and does not sync anywhere by default.

The **AI Assistant is different**: it requires a free Nexus Cloud account and is powered by a server Nexus operates. This page explains both plainly.

## Where Things Are Stored

| Data | Where |
|---|---|
| Notes, folders, tags, links, locally saved chat history, version history | Local SQLite database (`nexus.db`) in your OS's standard app-data directory |
| Note search index (embeddings) | Same local database |
| Nexus Cloud API key (issued when you sign up for the first time) | Your OS's native secure credential store (Keychain / Credential Manager / Secret Service) — **not** the local database |
| Your Nexus Cloud account (email, hashed password, hashed key, usage counters) | Nexus's own server-side database (not your device) |
| Bookmarks, downloads history, browser homepage, theme, editor preferences | Local browser storage within the app |

## What Ever Leaves Your Device

Browsing pages, taking notes, using the knowledge graph, exporting to Markdown/PDF, and backing up your database are all fully offline operations.

**Using the AI Assistant is not offline.** When you send a message to the Assistant:

1. Nexus's local search first decides which of your notes are relevant to your question (this step runs entirely on-device and makes no network call).
2. Your device sends your question, those relevant note snippets, and — if you've enabled "Aware of tabs" for that conversation — the text of your currently open browser tab(s), to **Nexus's own cloud service** (not directly to a third-party AI provider).
3. Nexus's cloud service forwards that request to a third-party AI provider using API credentials that belong to Nexus, gets the reply, and sends it back to your device.
4. Nexus's cloud service also records token-usage counts and a timestamp against your account, to enforce usage limits — see "Nexus Cloud Account and Usage" below.

Your full note collection, your browsing history outside the active "Aware of tabs" toggle, and the rest of your local database are never included in a request.

## Nexus Cloud Account and Usage

To use the Assistant you need to create a Nexus Cloud account with an email address and a password. Nexus's server stores:

- Your email address;
- A hashed (not plaintext) version of your password;
- A hashed version of your Nexus Cloud API key;
- Usage records (token counts and timestamps) tied to your account, used to apply a rolling usage limit — currently based on your usage over the trailing several hours, similar to how some AI chat products apply rolling rate limits;
- If you request a password reset, a hashed reset code, its expiration, and your email address (used to deliver the code).

Nexus does not currently offer an option to use the Assistant with your own third-party AI provider key instead of a Nexus Cloud account.

## The Contradiction Watcher

The background contradiction-checking feature (see [Features](features.md#contradiction-watching)) runs both of its stages entirely on-device: the free local similarity comparison, and the follow-up check using a small local language model for the single best-matching note. Neither stage calls Nexus Cloud or any external AI provider.

## Your Nexus Cloud API Key

Your Nexus Cloud API key is stored using your operating system's native credential storage APIs, the same category of storage password managers use. It is never written to Nexus's local database, never included in exports or backups, and is used only to authenticate your device's requests to Nexus's own cloud service.

## Backups and Exports

Database backups and Markdown/PDF exports are files written to a location you choose on your own device. Nexus does not upload them anywhere. If you back up to cloud storage (Dropbox, iCloud, a NAS, etc.), that's a choice you make outside the app — Nexus has no awareness of or involvement in where you save these files. These exports do not include your Nexus Cloud account credentials.

## Third-Party AI Provider

Nexus's cloud service uses a third-party AI provider to generate Assistant responses. That provider is selected and paid for by Nexus, and receives the request from Nexus's server rather than from your device directly. You do not have a separate account with that provider through this feature, so its own end-user privacy settings do not apply to you individually — Nexus's use of the provider is governed by Nexus's own agreement with it.
