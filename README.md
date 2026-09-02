# Mood Collab

Mood Collab adds real-time Markdown collaboration to Obsidian. Teammates can
edit the same note, see each other's cursors, leave anchored comments, browse
activity, and keep closed notes synchronized on disk.

Mood Collab is a client. It requires an account on a compatible Mood Collab
server operated by your organization. The plugin does not include a hosted
service and does not connect to a default server.

## Features

- Live collaborative editing with per-user cursors and selections.
- Continuous synchronization for open and closed notes.
- Comments, replies, mentions, presence, and an activity feed.
- Remote rename and recoverable delete propagation.
- Local version snapshots and conflict-safe disk reconciliation.
- Folder-level roles for editors, commenters, and viewers.

## Install

After the plugin is accepted into the Obsidian Community directory:

1. Open **Settings** in Obsidian.
2. Select **Community plugins**, then **Browse**.
3. Search for **Mood Collab**.
4. Select **Install**, then **Enable**.

## Connect to a server

Ask your server administrator for:

- The server URL.
- Your username and password, or an invitation token.

Open **Mood Collab: log in** from the command palette. Enter the server URL and
credentials. Mood Collab accepts HTTPS servers. Plain HTTP is allowed only for
`localhost` and loopback addresses.

The server decides which remote vaults, folders, and roles your account can
access. Each local Obsidian vault connects to one remote vault.

## Network and account disclosure

Mood Collab requires an account and network access for its main features. It
connects only to the server URL entered by the user and to the Y-Sweet endpoints
returned by that server. It sends authentication requests, collaborative note
updates, presence, comments, activity, attachments, and administrative requests
initiated by authorized users.

The client contains no advertising or client-side telemetry. Server operators
control their own retention, access logs, backups, and privacy policy. Ask your
administrator how your organization's server handles data.

## Local data and credentials

The plugin reads and writes only the folders granted by the collaboration
server inside the current Obsidian vault. It stores synchronization state,
merge shadows, and local snapshots in Obsidian's plugin data and IndexedDB.

"Stay signed in on this device" is off by default. If enabled, Mood Collab
stores the username and password in the vault's local plugin data so it can log
in after Obsidian restarts. Obsidian does not provide a cross-platform secret
store for community plugins. Do not enable this option on a shared device, and
protect access to the vault's `.obsidian` folder.

The optional local automation endpoint is off by default. On desktop, users can
enable a token-protected HTTP endpoint bound to `127.0.0.1`. It never listens on
the local network.

## Mobile

The collaboration client works on desktop and mobile. The optional local
automation endpoint is desktop-only and remains disabled on mobile.

## Server compatibility

This repository contains the Obsidian client, not the collaboration server. A
compatible server must provide Mood Collab authentication, vault and scope
authorization, Y-Sweet document tokens, attachments, and administration APIs.

## Repository and updates

This public repository contains the listing metadata and signed-off release
assets used by Obsidian. The client source is maintained in a private repository
and is made available to Obsidian reviewers through the Community Directory
GitHub App.

Each release tag matches the version in `manifest.json`. After the initial
listing is approved, Obsidian checks these releases and offers updates through
Community plugins.

## Security reports

See [SECURITY.md](SECURITY.md) for private reporting instructions. Do not put
credentials, invitation tokens, note contents, or server logs in a public issue.

## License

Mood Collab is proprietary software. See [LICENSE](LICENSE). Bundled libraries
retain their own licenses as listed in
[THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
