# Getting Started

The first time you open Nexus, you'll land on the **Notes** tab with an empty welcome screen. From here you can:

- Click **Write Your First Note** to create your first note (this also opens a short tutorial on `[[wiki links]]` and `#tags`)
- Click **Surf the Web** to jump straight into the built-in browser
- Click **Ask the Assistant** to open the AI chat (you'll need to sign up for a free Nexus Cloud account first — see [Setting Up the Assistant](#setting-up-the-assistant) below)

## A Guided Tour

### The Rail

The narrow bar on the far left is always visible, regardless of which tab you're in. It has:

- Tabs for **Notes**, **Browser**, **Assistant**, and **Graph**
- **Settings** at the bottom

### Notes

Your notes live in the left sidebar, optionally organized into folders and filtered by tag. Click any note to open it in the editor. Typing `[[Another Note's Title]]` creates a real link between notes; typing `#topic` anywhere creates a tag. See [Notes](features.md#notes) for the full picture.

### Browser

A real, tabbed web browser lives inside Nexus — not an embedded preview, but native browsing with back/forward, bookmarks, and downloads. See [Browser](features.md#browser).

### Setting Up the Assistant

The Assistant is powered by **Nexus Cloud**, a service Nexus operates — it is not a "bring your own key" feature, and there's no third-party AI provider account for you to set up yourself.

1. Open the **Assistant** tab. If you're not signed in, a sign-up/sign-in screen opens automatically.
2. Enter an email address and a password (at least 8 characters) to create a free Nexus Cloud account, or sign in if you already have one.
3. Once signed up or signed in, Nexus issues your device a Nexus Cloud API key automatically — there's nothing else to copy or paste.
4. Start asking the Assistant questions. Your usage is subject to a rolling usage limit; you can check your remaining usage and manage your account from the Account panel in the Assistant tab.

Your Nexus Cloud API key is stored in your operating system's secure credential store (Keychain on macOS, Credential Manager on Windows, Secret Service on Linux). Your account's password is never stored in plain text — only a salted hash of it is kept on Nexus's own server.

Requests you send to the Assistant go from your device to Nexus's own cloud service first, which then forwards them to a third-party AI provider on Nexus's behalf; see [Data & Privacy](data-and-privacy.md) for exactly what that involves.

### The Graph

Once you have a handful of notes, open the **Graph** tab to see how they connect — solid lines for explicit `[[links]]`, dashed lines for notes that simply mention each other's titles in plain text.

## Next Steps

- Read [Features](features.md) for a full breakdown of everything Nexus can do.
- Read [Data & Privacy](data-and-privacy.md) to understand exactly what's stored where, and what a Nexus Cloud account involves.
- Check [Keyboard Shortcuts](shortcuts.md) — Nexus is built to be used mostly without touching the mouse.
