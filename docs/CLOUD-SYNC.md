# Cloud + offline in nojeon 0.6.0

## Save first, sync next

Every workspace edit is saved to SQLite on your PC. A durable journal keeps
pending changes through disconnections and restarts. While the workspace is
open, nojeon checks for cloud changes roughly every four seconds.

Supabase handles cloud login and account-owned snapshots. Private Storage holds
attachments, uploaded images, covers, icons, and saved templates. Other accounts
cannot read your snapshots or files.

The bottom status bar distinguishes **Saved on this PC** from **Synced**.
An offline message means changes are kept locally and will retry when connected.
First-time signup/login and account changes need internet.

## What follows you

- Workspaces, pages, nested blocks, tables, favorites, and trash.
- Tasks, calendars, events, and links to your pages.
- Attachments, cover images, page icons, and reusable template archives.

Theme, reading width, sidebar state, autosave delay, and other appearance/display
preferences stay on the individual PC.

## Two devices and conflicts

Sign in to the same cloud account on another PC to download the workspace.
Incoming changes refresh the app after local edits are saved. In Calendar,
Templates, or Settings, finish the form/dialog and leave the view or click the
sync status when available to refresh safely.

If two devices change the account before syncing, nojeon asks which version to
keep. Click the conflict status:

- **Yes:** keep this PC's version.
- **No:** use the cloud version.
- **Cancel:** decide later.

The replaced version is saved as a local recovery copy. This preview syncs whole
account snapshots; it does not automatically merge individual page edits.

## Restore a recovery copy

Open **Settings / Storage**. Use **Open sync recovery copies** to inspect the
folders, or **Restore a sync recovery copy** to choose a snapshot.

Restore affects the entire account, including tasks, calendars, and templates.
The current version is preserved first. Restored data is saved locally and
queued for cloud sync.

Recovery snapshots share file contents under `Recovery/Blobs`. Keep the whole
Recovery folder together when making a copy; an individual snapshot folder can
depend on those shared files. Earlier self-contained recovery folders remain
readable.

## Storage and privacy

Each cloud project/account has a separate cache beneath
`%LOCALAPPDATA%/Notion/Cloud/<project-host>/<account-id>/`. Windows encryption
protects saved login tokens. Workspace content, cached files, and exported
backups are not end-to-end encrypted.

Only one app instance can hold a particular account cache at a time. Signing out
removes saved login credentials but leaves the cached content on that PC.

## Preview limits

Snapshots allow 16 MiB of structured content. Files allow up to 100 MiB, subject
to the cloud project's own upload limit. Confirmation emails are rate-limited.
Superseded cloud objects and local recovery copies are retained without automatic
garbage collection. Shared workspaces, simultaneous collaboration, OAuth,
automatic conflict merging, and end-to-end encryption are not available.

## Existing workspaces

Use the previous local edition to export each workspace as a `.notionbackup`,
then restore it in 0.6.0 after signing in. Old local accounts and template
libraries do not migrate automatically. Existing MySQL data remains untouched.

[Installation](INSTALLATION.md) · [Backups](BACKUPS.md)
