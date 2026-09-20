# Nexus Documentation

Nexus is an application that brings your notes, a real web browser, and an AI assistant into one workspace. Your notes and browsing live locally on your device; the AI Assistant is powered by a Nexus-operated cloud service that requires a free Nexus Cloud account. This repository is the public documentation for Nexus — it does not contain the application's source code, which is proprietary. See the [Nexus Proprietary License](https://github.com/getnexusapp/.github/blob/main/LICENSE.md) for terms of use.

**Get Nexus:** [Website](https://letnexusout.vercel.app/) · [Download](https://github.com/getnexusapp/releases/releases/tag/v5.4.0) · [Report an Issue](https://github.com/getnexusapp/releases/issues)

---

## Contents

- **[Getting Started](getting-started.md)** — installation, first launch, and a guided tour
- **[Features](features.md)** — everything Nexus does, in depth
- **[Keyboard Shortcuts](shortcuts.md)** — the command palette and every shortcut
- **[Data & Privacy](data-and-privacy.md)** — what's stored where, and what leaves your device
- **[FAQ](faq.md)** — common questions
- **[Contributing to the Docs](CONTRIBUTING.md)** — how to suggest fixes or additions to these pages

---

## What is Nexus?

Nexus replaces three separate apps — a notes app, a browser, and an AI chat client — with one window where they actually talk to each other. Open a page in the built-in browser, ask the Assistant a question, and it already has context on both what you're reading and what you've written.

Your notes, folders, tags, links, browsing data, and version history are stored locally in a SQLite database on your own machine — nothing about your notes workspace is synced to a server by default. The AI Assistant is the exception: it's powered by **Nexus Cloud**, a backend service Nexus operates, and requires a free Nexus Cloud account to use.

At a glance:
 
| | |
|---|---|
| **Notes** | Markdown-based, with folders, tags, `[[wiki links]]`, automatic backlinks, version history, and a knowledge graph — fully local |
| **Browser** | A real multi-tab browser built into the app — bookmarks, downloads, and per-tab isolated sessions — fully local, no account needed |
| **Assistant** | An AI chat that can search your notes semantically and read your open browser tabs, powered by your Nexus Cloud account (sign-up required, subject to usage limits) |
| **Storage** | Local SQLite for your notes workspace — export to Markdown or PDF, or back up/restore the whole database anytime |
 
---

## License

Nexus is proprietary software. This documentation is provided to help users and prospective users understand and use the application; it is not a grant of rights to the application's source code. See [Nexus End User License Agreement](https://github.com/getnexusapp/.github/blob/main/EULA.md) in the main repository for full terms.
