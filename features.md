## Features

### Notes That Think As You Do

- A rich-text (WYSIWYG) editor — bold looks bold, headings look like headings, and code blocks are syntax-highlighted.
- A full formatting toolbar with undo/redo, bold, italic, underline, strikethrough, headings, block quotes, bulleted lists, numbered lists, task lists, images, tables, inline code, code blocks, links, and **UPPERCASE / lowercase / Title Case** transformations.
- Insert **PNG, JPEG, GIF, and WebP** images up to 8 MB each. Images are stored inside your local database, so they travel with your backups and exports.
- Type `[[` anywhere in a note to instantly search your notes and create links. Keep typing to narrow the results with fuzzy matching — `[[rcp` can find **Recipe Ideas**.
- Insert a note link with **Enter**, **Tab**, or a click. You can also choose **New link** to create a link to a note you have not written yet.
- Type `[[Note Title]]` to create an explicit note connection, or simply mention another note by name and let Nexus detect the relationship.
- Note links appear as clickable pills directly inside the editor.
- `#tags` automatically become colored pills as you type. No separate tag manager or setup required.
- Optional **auto-capitalization** while you write.
- Optional **word-count bubble** showing words, characters, and characters excluding spaces.
- Word-level undo and redo, so you can step backward or forward through individual changes.
- **Version history** automatically preserves earlier versions of your notes. Preview an older version and restore it whenever you need to.
- Organize your workspace with **folders**.
- **Pin** important notes so they stay easy to find and stand out in the knowledge graph.
- A **command palette** (`Cmd/Ctrl+K`) for quickly jumping to notes, finding actions, and navigating your workspace without reaching for the mouse.
- A real **Trash** — deleted notes stay recoverable until you restore them, permanently delete them, or empty the Trash.
- Fast local search across your workspace using both **meaning and keywords**, so you can find ideas even when you do not remember the exact words you wrote.
- Local search indexes and embeddings are generated on your device to support semantic search and related-note features.
- Your notes and workspace are **local-first**. Your notes are stored on your device rather than automatically synchronized to a Nexus cloud database.

### A Browser That Belongs to Your Workspace

- Up to **8 tabs**, each displaying a real native web page — not an iframe — so websites that block embedding can still load.
- Switch away from a tab and come back to it exactly where you left it, including scroll position, video state, and form input where supported.
- **Back, forward, and reload** controls.
- An address bar that doubles as a search bar, using **Brave Search by default**, with the option to set your own homepage.
- A **bookmark system** with a bookmark library for saving and organizing pages.
- A **tab overview** for seeing and switching between your open pages.
- Links that request new windows open as new Nexus tabs instead.
- Only **HTTP and HTTPS** pages can be opened.
- Links clicked inside your notes or AI Assistant responses open directly in the Nexus Browser instead of your system browser.
- Browser pages can provide context to the AI Assistant when you allow it through the applicable browser settings.
- Nexus can read open-page text **locally on your device** for browser features such as conflict detection.
- The browser keeps its own cookies, site data, bookmarks, and downloaded-file information locally.

### An Assistant That Actually Knows Your World

- **Nexus Cloud AI** is the optional AI Assistant built into your workspace.
- A free **Nexus Cloud account** is required to use the Assistant.
- Ask questions about your own knowledge base and receive answers based primarily on the most relevant excerpts from your notes.
- Nexus identifies the **notes used as sources** for an answer.
- Your notes are searched using both **semantic meaning and keyword matching**.
- Ask questions using the context of pages currently open in the Nexus Browser.
- Nexus can fetch relevant page content in the background when browser context is used.
- Search the **live web** for current information when your question requires it.
- AI web-search requests can retrieve relevant information from current web pages.
- While you browse, Nexus can compare open browser pages with your notes **on-device**.
- Nexus can tell you when an open page relates to one of your notes.
- Nexus can flag possible **factual conflicts** between information in your notes and information found on an open page.
- Browser conflict detection can be switched off.
- Keep **as many separate AI conversations as you want**, with conversations stored locally on your device.
- Rename conversations whenever you want.
- Delete individual conversations whenever you want.
- Turn an AI response into a **new note with one click**.
- AI Assistant conversation history remains part of your local workspace rather than being maintained as a permanent server-side conversation database.
- The Assistant uses a rolling **5-hour usage window** rather than unlimited usage.
- Check your current usage from the app.
- Regenerate your Nexus Cloud API key when needed, subject to the applicable regeneration limit.
- Reset your Nexus Cloud password through email.
- Permanently delete your Nexus Cloud account from the app.
- Your Nexus Cloud account is separate from your local workspace — you do not need an account to use Nexus's core local-first features.

### A Map of Everything You Know

- A living, interactive **knowledge graph** showing how your notes connect.
- Drag and zoom freely around your graph.
- **Solid lines** represent explicit `[[links]]` between notes.
- **Dashed lines** represent relationships Nexus detected automatically.
- Nodes are sized according to how connected they are.
- Nodes are colored according to their folder.
- **Pinned notes receive a gold outline** so important information stands out.
- Click any node to open its note.
- The graph updates as your notes and relationships change.
- Connections can be discovered from the content of your workspace rather than requiring you to manually create every relationship.

### Search That Understands Meaning

- Search your entire workspace without relying solely on exact words.
- Combine **keyword matching and semantic search** to find relevant notes.
- On-device embeddings help Nexus understand relationships between ideas.
- Search indexes remain local to your device.
- Related-note features can surface connections that are not represented by explicit `[[links]]`.
- Search works alongside folders, tags, links, and the knowledge graph rather than replacing them.

### AI That Can Run on Your Device

- Some Nexus features use **on-device AI models** downloaded from public model-hosting infrastructure.
- These models can support local features such as semantic search, related-note discovery, page analysis, and conflict detection.
- Processing performed by these models can happen locally on your device.
- Downloading an on-device model is separate from sending an AI Assistant request through Nexus Cloud.
- Your local workspace does not need a Nexus Cloud account for features that operate entirely on your device.

### It Looks However You Want

- Four built-in themes: **Darkness**, **Dusk**, **Daylight**, and **Dawn**.
- A custom title bar designed to fit the Nexus interface.
- **Self-hosted fonts**, so the interface remains consistent even when you are offline.
- The interface is designed to remain usable without a cloud connection for local-first features.

### Your Workspace Stays Yours

- **Markdown export:** export your notes as `.md` files inside a `.zip`, preserving your folder structure.
- Markdown exports include a small metadata header for each note.
- Images used by notes are included as attachments in the export.
- **PDF export:** export any individual note as a PDF, generated entirely on your device.
- **Full workspace backup:** create a complete `.db` backup containing your workspace, preferences, bookmarks, and other locally stored Nexus data.
- Backups are created **only when you choose to create them**.
- **Restore:** select a backup and Nexus verifies that it is a valid SQLite database before replacing your current workspace.
- Restored data takes effect after restarting the application.
- Your local database gives you a portable backup of your workspace rather than requiring continuous cloud synchronization.
- Export your work whenever you want and keep your own independent copies.

### Built for Local-First Privacy

- Your core notes workspace does not require a cloud account.
- Notes, folders, tags, links, images, version history, Trash, search indexes, embeddings, bookmarks, browser data, and locally stored AI conversations remain on your device during ordinary local operation.
- Nexus does **not** automatically synchronize your notes and workspace to a cloud database.
- The optional AI Assistant is different: requests are processed through **Nexus Cloud** and applicable third-party AI and search providers.
- Your Nexus Cloud API key is stored using your operating system's secure credential storage, such as **Windows Credential Manager** or the **macOS Keychain**.
- Account information required for Nexus Cloud is kept separately from your local workspace.
- You can delete your Nexus Cloud account without deleting the local notes and workspace stored on your device.
- Core local functionality remains available without a Nexus Cloud account.

### One Workspace, Not a Collection of Separate Apps

- Write your notes.
- Browse the web.
- Save bookmarks.
- Connect ideas with `[[links]]`.
- Discover relationships automatically.
- Search your knowledge semantically.
- Compare web pages with what you already know.
- Ask an AI Assistant questions about your own workspace.
- Turn useful answers into notes.
- Visualize your knowledge as a graph.
- Export everything to Markdown or PDF.
- Back up the entire workspace to a SQLite database.
- Restore it when you need to.

**Nexus brings your notes, browser, knowledge graph, local intelligence, and optional cloud AI into one workspace — while keeping your core knowledge on your device.**
