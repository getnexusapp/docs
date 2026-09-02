# Nexus Documentation

Nexus is a desktop application that brings your notes, a real web browser, and an AI assistant into one local-first workspace. This repository is the public documentation for Nexus — it does not contain the application's source code, which is proprietary. See the [Nexus Proprietary License](https://github.com/getnexusapp/.github/blob/main/LICENSE.md) for terms of use.

**Get Nexus:** [Website](https://nexusdesktop.netlify.app/) · [Download](https://github.com/getnexusapp/releases/releases/tag/v5.0.0) · [Report an Issue](https://github.com/getnexusapp/releases/issues)

---

## Contents

- **[Getting Started](docs/getting-started.md)** — installation, first launch, and a guided tour
- **[Features](docs/features.md)** — everything Nexus does, in depth
- **[Keyboard Shortcuts](docs/shortcuts.md)** — the command palette and every shortcut
- **[Data & Privacy](docs/data-and-privacy.md)** — what's stored where, and what ever leaves your device
- **[FAQ](docs/faq.md)** — common questions
- **[Contributing to the Docs](CONTRIBUTING.md)** — how to suggest fixes or additions to these pages

---

## What is Nexus?

Nexus replaces three separate apps — a notes app, a browser, and an AI chat client — with one window where they actually talk to each other. Open a page in the built-in browser, ask the Assistant a question, and it already has context on both what you're reading and what you've written. Everything is stored locally in a SQLite database on your own machine; nothing is synced to a server Nexus operates, because there isn't one.

At a glance:

| | |
|---|---|
| **Notes** | Markdown-based, with folders, tags, `[[wiki links]]`, automatic backlinks, version history, and a knowledge graph |
| **Browser** | A real multi-tab browser built into the app — bookmarks, downloads, and per-tab isolated sessions |
| **Assistant** | An AI chat that can search your notes semantically and read your open browser tabs, using your own API key |
| **Storage** | 100% local SQLite — export to Markdown or PDF, or back up/restore the whole database anytime |

---

## Platform Support

Nexus is built on Tauri and ships as a native desktop application for Windows, macOS, and Linux.

## License

Nexus is proprietary software. This documentation is provided to help users and prospective users understand and use the application; it is not a grant of rights to the application's source code. See [Nexus End User License Agreement](https://github.com/getnexusapp/.github/blob/main/EULA.md) in the main repository for full terms.
