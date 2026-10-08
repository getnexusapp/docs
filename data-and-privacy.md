# Data & Privacy

Nexus is designed as a local-first workspace. Your notes and core workspace data are stored on your own device rather than automatically synchronized to a Nexus cloud database.

The **AI Assistant is different**. It is an optional cloud feature that requires a free Nexus Cloud account, created by signing in with Google or GitHub. When you use it, information needed to answer your request is sent from your device to Nexus Cloud and, where applicable, forwarded to third-party AI or web-search providers.

This page explains what stays local, what can leave your device, and what Nexus Cloud stores.

## Where Things Are Stored

| Data | Where |
|---|---|
| Notes, folders, tags, links, images, version history, and Trash | Local Nexus database on your device |
| Local search indexes and embeddings | On your device |
| AI conversations | On your device (not stored by Nexus Cloud) |
| Browser bookmarks, settings, cookies, site data, and download history | Local storage on your device |
| Nexus Cloud API key (session key) | Your operating system's native secure credential storage; it is not stored in the local Nexus database |
| Account email and Google/GitHub account identifier | Nexus Cloud server |
| Hash of your API key and session records | Nexus Cloud server (only a hash of the key is stored, never the key itself) |
| Usage information (token counts and request timestamps) | Nexus Cloud server |
| Short-lived rate-limiting and sign-in records, which can include your IP address | Nexus Cloud server |

Nexus does not require an account for its core local-first workspace features. Nexus does not receive or store a password for you, and it does not store your Google or GitHub access token.

Your local notes and workspace are not automatically synchronized to Nexus Cloud.

## What Can Leave Your Device

Many Nexus features operate locally. Creating and editing notes, organizing folders and tags, using the knowledge graph, searching locally stored information, managing version history and Trash, exporting notes, and creating or restoring local backups do not require sending your workspace to Nexus Cloud.

The Nexus Browser is different from Nexus Cloud. Websites you visit communicate with those websites' own servers as part of normal web browsing. Nexus does not upload your general browsing history to Nexus Cloud merely because you browse the web.

The **AI Assistant does require a network connection and can't be used offline**.

When you send a message to the Assistant, the request may contain:

1. Your new message.
2. Up to 20 previous messages from the current AI conversation.
3. Relevant excerpts from your notes, identified through Nexus's local search, other than notes you have set to **"AI: Off"**.
4. Relevant excerpts from a note you identify by title or, in some cases, if excerpt retrieval fails or returns nothing, up to the first 20,000 characters of that note (unless it is set to "AI: Off").
5. The current date and time.
6. Text from your active browser tab, only when **"Aware of tabs"** is on.

Nexus first performs relevant retrieval locally. The request is then sent to **Nexus Cloud**, not directly from the app to a third-party AI provider.

Nexus Cloud processes the request and forwards the applicable information to a third-party AI provider to generate the response. The AI model may decide to search the web, in which case the search query it writes (which can reflect what you asked) is sent to a third-party search service, and Nexus Cloud may retrieve the text of relevant result pages.

The response is returned to your device and your conversation is saved locally.

Nexus does **not** send your entire local database or automatically upload your entire note collection as part of an Assistant request.

### Keeping a Note Private from the AI

You can mark any note **"AI: Off"** from the note's toolbar. Notes marked "AI: Off" are excluded from the excerpts and note contents the Assistant sends to Nexus Cloud, including when you mention the note by title.

This does not apply to text you type or paste into the Assistant yourself, to earlier messages in the conversation that already contain such text, or to page text from your browser. Notes marked "AI: Off" are still indexed and used by local, on-device features.

## Browser Context

Nexus can read the text of your **active browser tab** for two features:

- **"Aware of tabs"**, which lets the Assistant use that page as context.
- **"Watching for conflicts"**, which compares the page with your notes to suggest related notes or possible conflicts.

If either setting is on, Nexus retrieves the page text by making a separate request from your device to that website, without your browser cookies. Nexus skips pages whose address looks like a one-time link (for example, links containing tokens, verification codes, or reset or unsubscribe paths). It also refuses to read pages on private or local network addresses. If both settings are off, Nexus does not retrieve page text.

Page text is included in Assistant requests and sent to Nexus Cloud **only when "Aware of tabs" is on**. If only "Watching for conflicts" is on, the page text is analyzed on your device using on-device models and is not sent to Nexus Cloud.

Your ordinary browser cookies, site data, and bookmarks remain local to the application.

## Nexus Cloud Account and Usage

The AI Assistant requires a free Nexus Cloud account. Accounts are created by signing in with **Google** or **GitHub**. The sign-in page opens in your system browser. Nexus Cloud receives only your verified email address and your account identifier from the provider.

To operate your account, Nexus Cloud may store:

- Your email address;
- Your Google or GitHub account identifier;
- A hash of your Nexus Cloud API key, and records of your sign-in sessions;
- Usage information such as token counts and request timestamps;
- Rate-limiting information, which can include your IP address for a short period;
- Limited operational information needed to operate, secure, and troubleshoot the service.

Nexus uses usage information to enforce the Assistant's rolling usage limits and per-minute rate limits.

Nexus Cloud does not function as a synchronized copy of your local Nexus workspace. Your notes, folders, local search index, and locally stored conversation history are not automatically uploaded.

Nexus currently provides the Assistant through Nexus Cloud and does not let users substitute their own third-party AI credentials.

## The Knowledge Graph and Local Processing

The Nexus knowledge graph operates as part of your local workspace.

Explicit `[[links]]` between notes, and mentions of other notes' titles that Nexus detects, can be represented in the graph. Local search indexes and embeddings are also used to find related notes.

On-device models handle local features such as note search and conflict detection. These models are downloaded once, then run on your device. They do not require an Assistant request to Nexus Cloud, and features that run entirely locally do not require a Nexus Cloud account.

## Your Nexus Cloud API Key

Your Nexus Cloud API key is stored on your device using your operating system's native secure credential storage, such as **Windows Credential Manager, macOS Keychain, or an equivalent system credential store**.

The key is not stored in the ordinary local Nexus database and is not included in exports or backups. It is used to authenticate requests from the app to Nexus Cloud.

Each sign-in creates a session key. A session stays valid until it has been unused for 90 days, you sign out, or you generate a new key. Generating a new key ends all your existing sessions. Each account can generate a new key up to three times in total.

## Third-Party Providers

Nexus and Nexus Cloud use independent third-party providers to operate particular features:

- **Google (Gemini)** for AI generation;
- **Jina AI** for web search and web-content retrieval used by the Assistant;
- **Google** and **GitHub** for sign-in;
- **Cloudflare** for hosting and infrastructure;
- **Brave Search** for non-URL searches typed in the browser address bar;
- **DuckDuckGo** for browser favicon retrieval, which receives the hostnames of sites you visit or bookmark;
- **GitHub** for update checks and downloads, which receives your IP address and ordinary request information;
- **Hugging Face** and **jsDelivr** for downloading on-device models and related runtime files, which receive your IP address and ordinary request information.

The information provided to a provider depends on the feature. These providers operate independently and have their own terms and privacy practices. Nexus Cloud uses its own service credentials when contacting AI and search providers; your Nexus Cloud API key is not given to them.

## Local Browser and External Websites

The Nexus Browser is a native browser integrated into the workspace.

When you visit an external website, that website may receive information normally associated with a web request, such as your IP address, browser information, cookies, and other technical information the site needs to operate. Nexus does not control the privacy practices of websites you visit.

Non-URL searches entered into the address bar are sent to **Brave Search**. Favicons are retrieved from **DuckDuckGo**. Cookies and site data are stored locally within the browser. Files you download are saved to your Downloads folder.

## Updates

Nexus checks for updates in the background by contacting GitHub, shortly after launch and then periodically. Updates are digitally signed, and Nexus will not install an update that fails signature verification. You can also check manually in Settings.

## Backups and Exports

Nexus provides local export and backup tools.

### Markdown Export

Markdown export creates a `.zip` containing your notes as `.md` files, organized by folder, with note metadata. Images are included as attachments.

### PDF Export

PDF export creates a PDF of an individual note on your device. If a note links to a remote image, the export may try to download that image directly from its website.

### Database Backup

A Nexus backup is a local SQLite file (`.nexus`) containing your workspace data (notes, folders, tags, links, images, version history, Trash, search indexes, and AI conversations) and applicable settings such as preferences and bookmarks. It does not include your API key, your download history, or the active account selection.

Backups are created only when you choose to create them.

### Restore

When you restore a backup, Nexus checks that the selected file is a valid, undamaged Nexus database that was not made by a newer version of Nexus. The restored workspace takes effect after the app restarts. Before replacing your current workspace, Nexus keeps a safety copy of it on your device (the three most recent copies are kept).

### Automatic Pre-Update Copies

The first time you launch Nexus after an update, it saves a copy of your database on your device before applying any database changes, so you can recover if an update goes wrong. The three most recent copies are kept.

Nexus does not upload your backups, exports, or these safety copies. If you place a backup or export in another service, such as Dropbox, iCloud, Google Drive, or a NAS, that transfer is controlled by you and that provider.

## Account Deletion

You can delete your Nexus Cloud account from Settings.

When you delete an account, Nexus Cloud deletes your account record, session records, linked Google or GitHub sign-in records, usage records, and your per-account rate-limit counters, and your key stops working immediately.

Certain limited information may remain temporarily where necessary for security, abuse prevention, operational records, hosting backups, or legal requirements. This includes short-lived IP-based rate-limit counters and operational logs.

Deleting a Nexus Cloud account does **not** delete the local Nexus workspace on your device. Your notes, local conversations, browser data, and other local information remain under your control unless you delete or clear them yourself. It also does not remove Nexus from your Google or GitHub account's list of connected apps, which you can manage with those providers.

## Operational Logs and Security Information

Nexus does not use the desktop application for behavioral analytics, advertising profiles, or automatic crash-reporting telemetry.

However, Nexus Cloud and its infrastructure maintain limited operational information needed to operate and secure the service. Depending on the event, this can include:

- IP addresses;
- Request timestamps;
- Requested URLs;
- Error information;
- Limited request or search metadata;
- Rate-limit and security information.

This information is used for service operation, security, abuse prevention, troubleshooting, and enforcing usage limits.

When you use "Contact Support" in Settings, the email draft includes only your app version and operating system details, never your note content.

## What Nexus Does Not Promise

Nexus is designed to keep your core workspace local, but no software, device, network, or cloud service can guarantee absolute security.

You are responsible for protecting your device, operating-system account, your Google or GitHub account, and any exported or backed-up files.

If you use the AI Assistant, consider the information you choose to send. Applicable information is processed by Nexus Cloud and its third-party providers. For highly sensitive information, mark the note "AI: Off" and avoid typing it into the Assistant.

## Your Control

You can:

- Use the core workspace without a Nexus Cloud account;
- Keep notes and workspace data on your own device;
- Mark individual notes "AI: Off" so they are never sent to the Assistant;
- Turn off "Aware of tabs" and "Watching for conflicts";
- Choose when to create backups;
- Export notes to Markdown or PDF;
- Restore a previous database backup;
- Delete AI conversations stored locally;
- Sign out, generate a new key, or delete your Nexus Cloud account;
- Clear all local Nexus data from Settings.

**Your core Nexus workspace is local-first. The optional AI Assistant is a cloud service.**

When you use local Nexus features, your workspace remains on your device. When you use Nexus Cloud features, only the information applicable to that feature and request is transmitted, processed, or stored as described above.
