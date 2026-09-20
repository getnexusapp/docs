# Frequently Asked Questions

### Is Nexus free?

Notes, the browser, the knowledge graph, exporting, and backups are free with no account. The AI Assistant requires a free Nexus Cloud account and is subject to a rolling usage limit.

### Is Nexus open source?

No. Nexus is closed-source, proprietary software. This documentation repository is public so users and prospective users can understand how the app works, but it does not include the application's source code.

### Do I need an internet connection to use Nexus?

No, for notes, the browser (aside from actually loading web pages), the knowledge graph, exporting, and backups. An internet connection is needed to browse the web and to use the AI Assistant.

### Do I need to create an account?

Not for notes, the browser, or the knowledge graph — those have no account system at all. You **do** need to create a free Nexus Cloud account (email and password) to use the AI Assistant.

### Where is my data stored?

Your notes, folders, tags, links, and locally saved chat history are stored locally in a SQLite database on your own device. If you use the Assistant, your Nexus Cloud account (email, hashed password and key, and usage counters) is stored on Nexus's own server. See [Data & Privacy](data-and-privacy.md) for full details.

### Does Nexus sync across devices?

Your notes workspace does not sync automatically — there's no built-in cloud sync for notes. You can manually back up your database (Settings → Data → Backup Database) and restore it on another device, or use your own file-sync tool (Dropbox, iCloud, etc.) on the backup file if you want to move data between machines yourself. Your Nexus Cloud account (for the Assistant) does work across any device where you sign in, since it's managed server-side.

### What AI model does the Assistant use?

The Assistant is powered by Nexus Cloud, a service Nexus operates, which forwards your request to a third-party AI provider using Nexus's own credentials. You don't need — and currently can't supply — your own AI provider API key; you just need a Nexus Cloud account.

### Is my account safe?

Your Nexus Cloud API key is stored in your operating system's native secure credential store (the same category of storage password managers use), not in a plain file, not in the app's local database, and not in browser storage. Your account's password is stored server-side only as a salted hash. See [Data & Privacy](data-and-privacy.md#your-nexus-cloud-api-key).

### Does the Assistant read all of my notes every time I ask something?

No. Nexus runs a local search first (semantic, falling back to keyword) to find only the notes relevant to your specific question, and sends just those snippets — not your whole note collection — along with your question to Nexus Cloud.

### What happens if I delete a note by mistake?

Deleted notes go to Trash and stay there, fully intact, until you restore them or empty the trash — there's no immediate permanent deletion. An undo toast also appears right after deleting for quick recovery.

### Can I export my notes if I stop using Nexus?

Yes. Settings → Data → Export Markdown Notes produces a zip of every note as a plain, portable `.md` file, readable by any Markdown-based tool. Individual notes can also be exported as standalone PDFs. This does not include your Nexus Cloud account information, which is separate.

### What happens if I hit the Assistant's usage limit?

You'll see a message that the limit has been reached; it clears gradually on a rolling basis as your older usage ages out, rather than resetting at a fixed time each day or month. You can keep using notes, the browser, and the knowledge graph in the meantime, since none of those depend on the Assistant.

### Which platforms does Nexus support?

Windows, macOS, and Linux, as a native desktop application.

### How do I report a bug or request a feature?

Use the [issue tracker](https://github.com/getnexusapp/releases/issues) linked from the main repository, or the "Report an Issue" link on the [Nexus organization page](https://github.com/getnexusapp).
