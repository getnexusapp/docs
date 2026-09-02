# Getting Started

## Installing Nexus

Nexus is a native desktop app for Windows, macOS, and Linux. Download the installer for your platform from the [releases page](#), run it, and launch Nexus like any other application. No account, sign-up, or internet connection is required to use the core app.

## First Launch

The first time you open Nexus, you'll land on the **Notes** tab with an empty welcome screen. From here you can:

- Click **Write Your First Note** to create your first note (this also opens a short tutorial on `[[wiki links]]` and `#tags`)
- Click **Surf the Web** to jump straight into the built-in browser
- Click **Ask the Assistant** to open the AI chat (you'll need to add an API key first — see [Setting Up the Assistant](#setting-up-the-assistant) below)

## A Guided Tour

### The Rail

The narrow bar on the far left is always visible, regardless of which tab you're in. It has:

- A **Quick Capture** button (the lightning bolt) for jotting a stray thought as a note from anywhere in the app, without leaving what you're doing
- Tabs for **Notes**, **Browser**, **Assistant**, and **Graph**
- **Settings** at the bottom

### Notes

Your notes live in the left sidebar, optionally organized into folders and filtered by tag. Click any note to open it in the editor. Typing `[[Another Note's Title]]` creates a real link between notes; typing `#topic` anywhere creates a tag. See [Notes](features.md#notes) for the full picture.

### Browser

A real, tabbed web browser lives inside Nexus — not an embedded preview, but native browsing with back/forward, bookmarks, and downloads. See [Browser](features.md#browser).

### Setting Up the Assistant

The Assistant uses Google's Gemini API under a **bring-your-own-key** model — Nexus never ships or proxies a shared key.

1. Open the **Assistant** tab. If no key is set, the settings panel opens automatically.
2. Click **Open Google AI Studio** (opens inside Nexus's own browser tab) and sign in with any Google account — it's free to get started.
3. Click **Create API key**, then copy it.
4. Paste it into the **Gemini API key** field in Nexus and click **Save**.

Your key is stored in your operating system's secure credential store (Keychain on macOS, Credential Manager on Windows, Secret Service on Linux) — never in a plain file, and never sent anywhere except directly to Google when you ask a question.

### The Graph

Once you have a handful of notes, open the **Graph** tab to see how they connect — solid lines for explicit `[[links]]`, dashed lines for notes that simply mention each other's titles in plain text.

## Next Steps

- Read [Features](features.md) for a full breakdown of everything Nexus can do
- Read [Data & Privacy](data-and-privacy.md) to understand exactly what's stored where
- Check [Keyboard Shortcuts](shortcuts.md) — Nexus is built to be used mostly without touching the mouse
