# Data & Privacy

Nexus is designed as a local-first workspace. Your notes and core workspace data are stored on your own device rather than automatically synchronized to a Nexus cloud database.

The **AI Assistant is different**. It is an optional cloud feature that requires a free Nexus Cloud account. When you use it, information needed to answer your request can be sent from your device to Nexus Cloud and, where applicable, forwarded to third-party AI or web-search providers.

This page explains what stays local, what can leave your device, and what Nexus Cloud stores.

## Where Things Are Stored

| Data | Where |
|---|---|
| Notes, folders, tags, links, images, version history, and Trash | Local Nexus workspace/database on your device |
| Local search indexes and embeddings | On your device |
| Locally saved AI conversations | On your device |
| Browser bookmarks, settings, cookies, site data, and related browser information | Local browser storage on your device |
| Nexus Cloud API key | Your operating system's native secure credential storage; it is not stored in the local Nexus database |
| Nexus Cloud account email | Nexus Cloud server |
| Nexus Cloud password | Nexus Cloud server as a salted password hash, not plaintext |
| Nexus Cloud API key | Nexus Cloud server as a hash used for authentication/verification |
| Cloud usage information | Nexus Cloud server, including usage/token counts and request timestamps |
| Temporary password-reset information | Nexus Cloud server for the limited period necessary to process the reset |

Nexus does not require an account for its core local-first workspace features.

Your local notes and workspace are not automatically synchronized to Nexus Cloud.

## What Can Leave Your Device

Many Nexus features operate locally. Creating and editing notes, organizing folders and tags, using the knowledge graph, searching locally stored information, managing version history and Trash, exporting notes, and creating or restoring local backups do not require sending your workspace to Nexus Cloud.

The Nexus Browser is different from Nexus Cloud. Websites you visit communicate with those websites' own servers as part of normal web browsing. Nexus does not upload your general browsing history to Nexus Cloud merely because you browse the web.

The **AI Assistant does require network communication**.

When you send a message to the Assistant, the request may contain information needed to answer it, including:

1. Your new message.
2. Up to 20 previous messages from the current AI conversation.
3. Relevant excerpts from your local notes identified through Nexus's local search.
4. The full contents of a specific note when the request identifies that note by title or otherwise requires its contents.
5. The current date and time when relevant.
6. Text from an open browser page when applicable browser context is enabled.

Nexus first performs relevant local retrieval from your workspace. The applicable request is then sent to **Nexus Cloud**, rather than directly from the Nexus application to the third-party AI provider.

Nexus Cloud processes the request and may forward the applicable information to a third-party AI provider to generate the response. If web information is required, Nexus Cloud may also use third-party web-search services and retrieve relevant page content.

The response is returned to your device, and your AI conversation is saved locally.

Nexus does **not** send your entire local database or automatically upload your entire note collection as part of an Assistant request.

## Browser Context and "Aware of Tabs"

Nexus can use the content of pages open in its built-in Browser as context for the AI Assistant.

When browser awareness is enabled for a conversation, relevant text from open browser pages may be included in an Assistant request.

You can turn off the browser-awareness setting to prevent open-tab content from being automatically included in AI requests.

Nexus may also read open-tab content locally for other browser/workspace features, including comparing information on a page with information in your notes. Turning off browser awareness does not necessarily prevent every form of local processing of open-page content; it primarily controls whether that content is automatically provided as AI context.

Your ordinary browser cookies, site data, bookmarks, and other browser storage remain local to the application.

## Nexus Cloud Account and Usage

The AI Assistant requires a free Nexus Cloud account.

To create and operate that account, Nexus Cloud may store:

- Your email address;
- A salted hash of your password rather than the plaintext password;
- A hash of your Nexus Cloud API key;
- Account-security information;
- Usage information such as token counts and request timestamps;
- Rate-limiting information;
- Temporary password-reset information, including a hashed reset code and its expiration;
- Limited operational information needed to operate, secure, and troubleshoot the service.

Nexus uses usage information to enforce the Assistant's applicable rolling usage limits.

Nexus Cloud does not function as a synchronized copy of your local Nexus workspace. Your notes, folders, local search index, and locally stored conversation history are not automatically uploaded and maintained as a cloud workspace.

Nexus currently provides the Assistant through Nexus Cloud rather than allowing users to substitute their own third-party AI provider credentials.

## The Knowledge Graph and Local Processing

The Nexus knowledge graph operates as part of your local workspace.

Explicit `[[links]]` between notes and relationships detected by Nexus can be represented in the graph. Local search indexes and embeddings can also be used to identify related information.

Where Nexus uses on-device processing or models for local features, that processing occurs on your device rather than requiring an Assistant request to Nexus Cloud.

Features that operate entirely locally do not require a Nexus Cloud account.

## Your Nexus Cloud API Key

Your Nexus Cloud API key is stored on your device using your operating system's native secure credential storage.

Depending on your operating system, this can include facilities such as the **Windows Credential Manager, macOS Keychain, or an equivalent system credential store**.

The API key is not stored in the ordinary local Nexus database and is not included in normal workspace exports or database backups.

The key is used to authenticate requests from your Nexus application to Nexus Cloud.

Signing in or performing certain account actions may issue or regenerate a key. Key regeneration is subject to the applicable security and usage limits.

## Third-Party Providers

Nexus Cloud may use independent third-party providers to operate particular features.

These can include:

- **Google/Gemini** for AI generation;
- **Jina AI** for applicable web-search or web-content retrieval;
- **Resend** for account-related email such as password-reset messages;
- **Cloudflare** for hosting and infrastructure;
- **DuckDuckGo** for browser favicon/icon retrieval.

The specific information provided to a third-party provider depends on the feature being used.

For example, when you use the AI Assistant, Nexus Cloud may forward the applicable Assistant request to its AI provider. When web search or page retrieval is required, applicable search queries or page requests may be sent to the relevant service.

These providers operate independently and have their own terms and privacy practices. Nexus uses its own service credentials when interacting with these providers; your Nexus Cloud API key is not given to them as their own service credential.

## Local Browser and External Websites

The Nexus Browser is a native browser integrated into the workspace.

When you visit an external website, that website may receive information normally associated with a web request, such as your IP address, browser information, cookies, and other technical information required for the site to operate.

Nexus does not control the privacy practices of websites you choose to visit.

Non-URL searches entered into the Nexus Browser's address bar may be sent to **Brave Search** when Brave Search is being used as the configured search provider.

Browser icons and favicons may be retrieved through external services such as **DuckDuckGo**.

Cookies and site data are stored locally within the Nexus Browser.

## Backups and Exports

Nexus provides local export and backup tools.

### Markdown Export

Markdown export creates a `.zip` containing your notes as `.md` files, organized according to your folder structure. The export can include note metadata and images as attachments.

### PDF Export

PDF export creates a PDF of an individual note entirely on your device.

### Database Backup

A Nexus workspace backup is a local SQLite `.db` file containing your workspace data and applicable local settings, including preferences and bookmarks.

Backups are created only when you choose to create them.

### Restore

When you restore a backup, Nexus checks that the selected file is a valid SQLite database before replacing the current workspace. The restored workspace takes effect after restarting the application.

Nexus does not upload your backups or exports as part of the normal backup/export process.

If you choose to place a backup or export in another service — such as Dropbox, iCloud, Google Drive, a NAS, or another cloud-storage provider — that transfer is controlled by you and that provider.

## Account Deletion

You can delete your Nexus Cloud account from the application.

When an account is deleted, Nexus removes the active account information and invalidates the associated Nexus Cloud API key.

Certain limited information may remain temporarily where necessary for security, abuse prevention, operational records, backups, or legal/accounting requirements.

Deleting a Nexus Cloud account does **not** delete the local Nexus workspace stored on your device.

Your notes, local conversations, browser data, and other local workspace information remain under your control unless you separately delete or clear them from the application.

## Operational Logs and Security Information

Nexus does not use the desktop application for general behavioral analytics, advertising profiles, or automatic crash-reporting telemetry.

However, Nexus Cloud and its infrastructure may maintain limited operational information needed to operate and secure the service. Depending on the event, this can include information such as:

- IP addresses;
- Request timestamps;
- Requested URLs;
- Error information;
- Limited request or search metadata;
- Rate-limit and security information.

This information is used for purposes such as service operation, security, abuse prevention, troubleshooting, and enforcing usage limits.

## What Nexus Does Not Promise

Nexus is designed to keep your core workspace local, but no software, device, network, or cloud service can guarantee absolute security.

You are responsible for protecting your device, operating-system account, Nexus Cloud credentials, and any exported or backed-up files.

If you use the AI Assistant, you should consider the information you choose to send to the service and understand that applicable information may be processed by Nexus Cloud and its third-party providers.

For highly sensitive information, use Nexus's local-first features without transmitting that information to the AI Assistant unless you understand and accept the applicable processing.

## Your Control

Nexus is built around keeping your core knowledge under your control.

You can:

- Use the core workspace without a Nexus Cloud account;
- Keep notes and workspace data on your own device;
- Choose when to create backups;
- Export notes to Markdown or PDF;
- Restore a previous database backup;
- Control whether browser-tab context is automatically supplied to the AI Assistant;
- Delete AI conversations stored locally;
- Delete your Nexus Cloud account;
- Clear local Nexus data from the application.

The key distinction is simple:

**Your core Nexus workspace is local-first. The optional AI Assistant is a cloud service.**

When you use local Nexus features, your workspace remains on your device. When you use Nexus Cloud features, only the information applicable to that feature and request is transmitted, processed, or stored as described above.
