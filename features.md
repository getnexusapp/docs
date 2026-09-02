# Features

## Notes

### Writing

Notes are written and previewed in a single live-formatting editor — no separate "edit" and "preview" modes. Bold looks bold, headings look big, and links are clickable as you type, while the underlying content is stored as plain Markdown.

The formatting toolbar above the editor gives you: undo/redo, bold, italic, underline, strikethrough, headings (H1–H3), blockquote, bulleted and numbered lists, inline code, fenced code blocks with syntax highlighting, link insertion, and case transforms (UPPERCASE / lowercase / Title Case) for selected text.

Pasting code from an editor like VS Code is detected automatically (via clipboard metadata, syntax-highlighted HTML, or plain-text heuristics) and converted into a proper fenced, syntax-highlighted code block instead of landing as unformatted text.

**Auto-capitalize** fixes the first letter of a sentence, line, or a standalone lowercase "i" as you type. It can be turned off in Settings.

**Word count** can be toggled on per session from the editor header — a small floating bubble shows word count, character count, and character count excluding spaces.

### Folders and Tags

Notes can be organized into **folders** from the sidebar. **Tags** are lighter-weight and fully automatic: type `#project` anywhere in a note's body and it becomes a real tag the moment the note saves — no separate tag manager, no manually assigning tags. Delete the text and the tag is gone from that note. The sidebar lists every tag currently in use, with a live count, and clicking one filters your notes to just that tag.

### Wiki Links and Automatic Mentions

Type `[[Note Title]]` anywhere in a note and Nexus turns it into a clickable link to that note as soon as it's saved — even if the target note doesn't exist yet (it'll render as a "missing" link you can click to create it).

You don't have to use brackets at all: if you simply mention another note's exact title in ordinary prose, Nexus notices and treats it as a softer, automatic connection — visible as a dashed edge in the Graph tab, separate from the solid edges explicit `[[links]]` create.

Every note also shows a **Linked From** (backlinks) panel and a **Links to** panel for its explicit connections, plus a **Related (semantic)** panel showing notes that are similar in *meaning* even without any shared link or wording — powered by the same on-device search used by the Assistant.

### Version History

Nexus automatically snapshots a note roughly once a minute while you're actively editing it, but only when something actually changed since the last snapshot — so idle time or unchanged saves don't bloat history. Up to 250 versions are kept per note, oldest pruned first. Open **Version History** from any note's header to browse past versions and restore one; restoring first snapshots your current content too, so a restore is never a one-way trip.

### Trash

Deleting a note is a soft delete — it moves to **Trash** and stays there, fully intact (including its links, tags, and version history), until you restore it or empty the trash yourself. A brief undo toast also appears immediately after deleting, for the common case of catching a mistake right away.

### Command Palette

Press **Ctrl/Cmd + K** anywhere in the app to open the command palette — a fuzzy-search launcher for jumping to any note by title, creating a new note or folder, or switching tabs, all from the keyboard.

### Export

- **Markdown export** — every note is exported as a plain `.md` file (with a small frontmatter header for title/dates), organized into a folder structure matching your Nexus folders, and zipped into a single downloadable archive. Fully portable to any other Markdown-based tool.
- **PDF export** — export a single note as a standalone, nicely formatted PDF, including headings, lists, code blocks, blockquotes, and colored tags — generated entirely on your device.

---

## Browser

Nexus includes a real, native, multi-tab web browser — not an embedded preview pane. Because it uses native child webviews rather than an iframe, it can open sites that block iframe embedding outright (most banks, search engines, and social platforms).

- Up to **8 tabs** open at once, each with its own independent browsing session, history, and back/forward stack
- A background tab keeps running (scroll position, video playback, unsaved form input all persist) when you switch away and back — it's not reloaded
- **Bookmarks** bar for quick access to saved pages
- A **downloads** indicator and history
- A configurable **default homepage** (Settings → Browser)

Links clicked anywhere inside Nexus — in a note, in an Assistant reply, in a page that tries to open a new window — open inside Nexus's own Browser tab, never in an external system browser.

---

## Assistant

The Assistant is an AI chat panel that can ground its answers in your own notes and, optionally, whatever you currently have open in the Browser tab.

### Bring Your Own Key

Nexus has no bundled or shared AI key. You supply your own Gemini API key (see [Getting Started](getting-started.md#setting-up-the-assistant)), stored in your OS's secure credential store — never in a plain file on disk.

### Conversations

Each chat lives in its own conversation, listed in a collapsible sidebar — rename, delete, or start a new one at any time. Conversations are saved locally and persist across restarts.

### Retrieval: How Nexus Finds What's Relevant

Before sending a question to the AI, Nexus searches your notes locally to find what's actually relevant, then includes only those snippets in the request:

- **Semantic search** runs first, using a small sentence-embedding model that downloads once and then runs entirely on your device (no network call per question). It finds notes that match the *meaning* of your question, not just shared keywords.
- **Keyword search** is the fallback if semantic search finds nothing or the local model isn't ready yet.

Which notes were used to answer a question are shown as clickable **Sources** underneath the reply.

### Page Awareness

If you have pages open in the Browser tab, the Assistant can optionally read their text and use it as context — toggle this per-conversation with the "Aware of tabs" pill. Page content is always treated as untrusted reference material, never as instructions, even if a page's text tries to look like one.

### Contradiction Watching

When enabled, Nexus quietly compares the pages you have open against your notes in the background and flags likely factual conflicts — for example, noticing that an article you're reading states something that contradicts a note you wrote earlier. This runs as a two-stage check (a free, local similarity pass first, then a narrow AI call only for the closest-matching note) to avoid burning API calls on pages that have nothing to do with your notes.

### Saving Answers

Any Assistant reply can be copied to your clipboard or saved directly as a new note with one click.

---

## Knowledge Graph

The Graph tab renders your entire note collection as an interactive, force-directed node graph:

- Drag any node to reposition it; scroll to zoom; drag the background to pan
- Solid edges are explicit `[[wiki links]]`; dashed edges are automatic title mentions
- Nodes are colored by folder, with a legend in the corner
- Larger nodes indicate more connections
- Click any node to jump straight to that note

---

## Appearance

Four built-in themes — **Darkness** (near-black), **Dusk** (deep navy), **Daylight** (a proper light mode), and **Dawn** (warm charcoal with an amber accent) — switchable anytime from Settings, applied instantly across the whole app.

---

## Data Management

- **Backup** — creates a complete, consistent snapshot of your database via SQLite's own `VACUUM INTO`, saved wherever you choose.
- **Restore** — restores from a previously saved backup file. Nexus verifies the file is actually a valid SQLite database before touching anything, and keeps a safety copy of your prior database in case a restore turns out to be a mistake. Takes effect after restarting Nexus.
- **Clear All Data** — a guarded, double-confirmation action that permanently erases every note, folder, tag, link, chat message, and version — for starting fresh.

All of the above operate purely on the local database file; none of it touches a remote server, because Nexus doesn't have one.
