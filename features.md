# Features

## Notes That Think As You Do

- A rich-text **WYSIWYG editor** — bold looks bold, headings look like headings, and code blocks are syntax-highlighted.
- A full formatting toolbar with **undo/redo, bold, italic, underline, strikethrough, headings, block quotes, bulleted lists, numbered lists, task lists, images, tables, inline code, code blocks, links, and UPPERCASE / lowercase / Title Case transformations**.
- Insert **PNG, JPEG, GIF, and WebP** images up to 8 MB each. Images are stored inside your Nexus database so they travel with your backups.
- Paste code directly from editors such as VS Code and Nexus automatically recognizes it and turns it into a syntax-highlighted code block, using the source language when available.
- Type `[[` anywhere in a note to instantly search your notes and create links. Keep typing to narrow the results with **fuzzy matching** — `[[rcp` can find **Recipe Ideas**.
- Insert note links with **Enter, Tab, or a click**.
- Create a link to a note you have not written yet with **New link**.
- Type `[[Note Title]]` to create an explicit connection between notes, or simply mention another note by name and let Nexus detect the relationship.
- Note links appear as **clickable pills** directly inside the editor.
- `#tags` automatically become colored pills as you type. No separate tag manager or setup required.
- Tags appear in the sidebar with their counts, and clicking a tag filters your notes.
- Optional **auto-capitalization** while you write.
- Optional **word-count bubble** showing words, characters, and characters excluding spaces.
- Word-level **undo and redo**, allowing you to move backward or forward through individual changes.
- **Version history** automatically preserves earlier versions as you edit, keeping up to 20 versions per note with saves occurring approximately every 30 seconds at most.
- Preview previous versions before restoring them.
- Restoring a previous version first saves your current content as a new version, so the restore itself can be undone.
- Organize your workspace with **folders**.
- **Pin** important notes so they stay easy to find and stand out in the knowledge graph.
- Use the **Command Palette** (`Cmd/Ctrl+K`) to jump to notes or perform quick actions.
- A real **Trash** keeps deleted notes recoverable until you restore them, permanently delete them, or empty the Trash.
- Trashed notes are excluded from the Assistant's note search until they are restored.
- A short, skippable tutorial introduces links and tags the first time you create your first note.

---

## A Browser That Belongs to Your Workspace

- Open up to **8 tabs**, each displaying a real native web page rather than an iframe.
- Websites that normally block iframe embedding can therefore still load normally.
- Switch away from a tab and return to it exactly where you left it, including its scroll position, video state, and form input where supported.
- **Back, forward, and reload** controls.
- An address bar that also works as a search bar, using **Brave Search by default**.
- Set your own **homepage** from Settings.
- Save websites using the built-in **bookmark system and bookmark library**.
- Use the **tab overview** to see and switch between open pages.
- Links that request a new window open as new Nexus tabs.
- If all 8 tab slots are already occupied, new-window links load in the current tab instead.
- Only **HTTP and HTTPS** pages can be opened.
- Links clicked from your notes or the Assistant open inside the Nexus Browser instead of your system browser.
- Browser pages can provide context to the Assistant when **page awareness** is enabled.
- Nexus fetches public page content in the background when page awareness is being used.
- Pages that require you to be logged in may not be readable by the Assistant.
- While you browse, Nexus can compare an open page with your notes **on-device**.
- Nexus can identify when a browser page relates to one of your notes and flag possible factual conflicts.
- Conflict watching is **off by default** and can be enabled from the Assistant tab or Settings.
- Downloaded files are saved to your **Downloads folder**.
- A downloads panel lets you open downloaded files or show them in their folder.

---

## An Assistant That Actually Knows Your World

- **Nexus Cloud AI** is the built-in Assistant for your workspace.
- A free **Nexus Cloud account** is required to use the Assistant.
- Create your account automatically the first time you choose **Continue with Google** or **Continue with GitHub**.
- There are no Nexus Cloud passwords to manage; authentication takes place through your system browser.
- Ask questions about your own knowledge base and receive answers based primarily on the **most relevant excerpts from your notes**.
- Nexus displays the notes used as sources, allowing you to open them directly.
- Notes are searched using both **semantic meaning and keyword matching**.
- Very long notes are split into overlapping sections so relevant passages can still be found.
- Mention a note by title and Nexus can pull information directly from that note.
- Use the page currently open in the Nexus Browser as additional context when **page awareness** is enabled.
- Nexus can search the **live web** when your question requires current information.
- While you browse, Nexus can compare open pages with your notes on-device.
- Nexus can tell you when a browser page relates to something in your knowledge base.
- Nexus can flag possible **factual conflicts** between information in your notes and information found on a page.
- Keep **as many separate AI conversations as you like**, with each conversation stored locally and kept separate for your signed-in account.
- Rename or delete conversations whenever you want.
- Copy any Assistant response.
- Turn an Assistant response into a **new note with one click**.
- Assistant usage is limited by a **rolling 5-hour usage window**.
- View your current usage from the **Nexus Cloud Account** panel.
- Copy or regenerate your Nexus Cloud API key, subject to the applicable regeneration limit.
- Sign out of your Nexus Cloud account whenever you want.
- Your Nexus Cloud sign-in remains active for approximately **90 days of activity** before another sign-in may be required.
- Permanently delete your Nexus Cloud account from Settings.

---

## A Map of Everything You Know

- A living, interactive **knowledge graph** showing how your notes connect.
- Drag and zoom freely around the graph.
- **Solid lines** represent explicit `[[links]]` between notes.
- **Dashed lines** represent relationships Nexus discovered automatically.
- Nodes are sized according to how connected they are.
- Nodes are colored according to their folder.
- **Pinned notes receive a gold outline**.
- Click any node to open its note.
- The graph helps you see both the relationships you created yourself and connections Nexus discovered from your workspace.

---

## Search That Understands Meaning

- Search your workspace using both **keyword matching and semantic meaning**.
- Find notes even when you do not remember the exact words you originally wrote.
- Long notes are divided into overlapping sections to improve retrieval.
- Semantic search works alongside traditional keyword search.
- Related-note discovery can surface notes that were never explicitly connected with `[[links]]`.
- Search works together with your **folders, tags, links, backlinks, and knowledge graph**.
- Nexus uses the most relevant results from your notes when answering questions through the Assistant.

---

## It Looks However You Want

- Four built-in themes:
  - **Darkness**
  - **Dusk**
  - **Daylight**
  - **Dawn**
- A custom title bar designed to fit the Nexus interface.
- **Self-hosted fonts** keep the interface visually consistent even when you are offline.
- Nexus is designed around a local-first workspace, so core local functionality remains available without relying on a cloud connection.

---

## You Own What You Make

### Markdown Export

- Export your notes as `.md` files inside a `.zip`.
- Your folder structure is preserved.
- Each note includes a small metadata header.
- Images used by your notes are included as attachments.

### PDF Export

- Export any individual note as a **PDF**.
- PDFs are generated entirely on your device.
- The exported document preserves the appearance and structure of the note, including:
  - Lists
  - Tables
  - Code
  - Links
  - Tags
  - Images

### Backup

- Create a complete **`.nexus` backup** of your workspace.
- Backups include your locally stored workspace data, preferences, and bookmarks.
- Backups are created **only when you choose to create one**.

### Restore

- Restore a workspace from Settings or from the Welcome screen when there are no notes.
- Nexus verifies that the backup is a valid and healthy Nexus database before replacing your current data.
- Backups created by a **newer version of Nexus are refused**.
- Restoring takes effect after the application restarts.
- Nexus keeps a **safety copy of your current data** before replacing it.

### Clear All Data

- A clearly marked **Clear All Data** option is available in the Settings danger zone.
- It can wipe your local notes, version history, and chats when you want to start with a clean workspace.

---

## Built for Local-First Privacy

- Nexus is designed around a **local-first workspace**.
- Your core notes and workspace data are stored locally rather than automatically synchronized to a Nexus cloud database.
- Your local workspace includes your notes and the associated local features that power your writing environment.
- The optional **Nexus Cloud Assistant** is separate from your local workspace.
- When you use the Assistant, relevant information may be processed through Nexus Cloud and applicable AI or web-search services to provide the requested response.
- Browser page awareness is optional and can be disabled.
- Browser pages that require authentication may not be readable by the Assistant.
- Your Nexus Cloud account is separate from your local Nexus workspace.
- You can use Nexus's core local features without creating a Nexus Cloud account.

---

## Safe Updates

- Nexus checks for new versions in the background shortly after launch and periodically afterward.
- You can also manually check for updates from Settings.
- Updates are **digitally signed and verified** before installation.
- Updates that fail verification are refused.
- Unsaved edits are saved before an update is installed.
- Before database changes are performed after an update, Nexus creates a safety copy of the database in an **`upgrade-backups`** folder.
- Nexus keeps the most recent upgrade backups so that a problematic update can be recovered from.
- Only **one copy of Nexus** can run at a time.
- Launching Nexus again brings the existing window to the front instead of starting a second instance.

---

## Settings & Support

- **Appearance** — choose your Nexus theme.
- **Nexus Cloud Account** — manage your Assistant account, usage, key, and sign-in.
- **Assistant conflict watching** — enable or disable browser-to-note conflict detection.
- **Browser homepage** — choose your default homepage.
- **Auto-capitalization** — control automatic capitalization while writing.
- **Update controls** — manage update behavior and check for new versions.
- **Data tools** — export, backup, restore, and clear your workspace.
- **Account deletion** — permanently delete your Nexus Cloud account.
- **Contact Support** — opens a pre-filled email containing only your Nexus version and system information.
- Support emails do **not** include your note content.
- Access the **Terms of Service** and **Privacy Policy** directly from the Support section.

---

# One Workspace, Not a Collection of Separate Apps

- **Write** your notes in a powerful rich-text editor.
- **Connect** ideas with `[[links]]` and tags.
- **Discover** relationships automatically.
- **Search** your knowledge using keywords and meaning.
- **Browse** the web without leaving your workspace.
- **Bookmark** useful pages.
- **Compare** what you find online with what you already know.
- **Ask** an AI Assistant questions about your own knowledge.
- **Use** current web information when you need it.
- **Turn** useful AI answers into notes.
- **Visualize** your knowledge as an interactive graph.
- **Track** earlier versions of your writing.
- **Restore** deleted notes from Trash.
- **Export** your work to Markdown or PDF.
- **Back up** your entire workspace as `.nexus` file.
- **Restore** your workspace when you need it.

**Nexus brings your notes, browser, knowledge graph, search, and optional cloud AI together in one workspace — giving you a place to write, think, research, connect ideas, and keep control of your work.**
