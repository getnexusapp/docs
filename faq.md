# Frequently Asked Questions

### Is Nexus free?

Yes, it is.

### Is Nexus open source?

No. Nexus is closed-source, proprietary software. This documentation repository is public so users and prospective users can understand how the app works, but it does not include the application's source code.

### Do I need an internet connection to use Nexus?

No, for notes, the browser (aside from actually loading web pages), the knowledge graph, exporting, and backups. An internet connection is only needed to browse the web and to use the AI Assistant.

### Do I need to create an account?

No. Nexus has no account system, sign-up flow, or login of any kind.

### Where is my data stored?

Locally, in a SQLite database on your own device. See [Data & Privacy](data-and-privacy.md) for full details.

### Does Nexus sync across devices?

Not automatically — there's no built-in cloud sync. You can manually back up your database (Settings → Data → Backup Database) and restore it on another device, or use your own file-sync tool (Dropbox, iCloud, etc.) on the backup file if you want to move data between machines yourself.

### What AI model does the Assistant use?

Google's Gemini, via an API key you provide yourself. Nexus does not include or proxy any AI model or key of its own. See [Getting Started](getting-started.md#setting-up-the-assistant) for how to add one.

### Is my Gemini API key safe?

It's stored in your operating system's native secure credential store (the same category of storage password managers use), not in a plain file, not in the app's database, and not in browser storage. See [Data & Privacy](data-and-privacy.md#your-api-key).

### Does the Assistant read all of my notes every time I ask something?

No. Nexus runs a local search first (semantic, falling back to keyword) to find only the notes relevant to your specific question, and sends just those snippets — not your whole note collection — along with your question.

### What happens if I delete a note by mistake?

Deleted notes go to Trash and stay there, fully intact, until you restore them or empty the trash — there's no immediate permanent deletion. An undo toast also appears right after deleting for quick recovery.

### Can I export my notes if I stop using Nexus?

Yes. Settings → Data → Export Markdown Notes produces a zip of every note as a plain, portable `.md` file, readable by any Markdown-based tool. Individual notes can also be exported as standalone PDFs.

### Which platforms does Nexus support?

Windows, macOS, and Linux, as a native desktop application.

### How do I report a bug or request a feature?

Use the [issue tracker](https://github.com/getnexusapp/releases/issues) linked from the main repository, or the "Report an Issue" link on the [Nexus organization page](https://github.com/getnexusapp).
