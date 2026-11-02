# Workspace backups in nojeon 0.6.0

Open **Settings > Import / export > Save workspace backup**. Save the
`.notionbackup` file somewhere private. Page edits are saved before the archive
is created; finish and save task/calendar edits first.

A version 2 backup includes the selected workspace's pages, hierarchy, formatting,
tables, trash, managed files, and tasks, plus **all calendars and events for the
signed-in account**. Calendars belong to the account, not to individual workspaces.
Repeat the backup for each workspace whose pages and tasks you want to preserve.

## Restore

Choose **Restore workspace backup**, review the page/file/task/calendar/event
counts, and enter a new workspace name. Restore creates a new workspace and
separate, uniquely named calendar copies. Existing workspaces and calendars remain
unchanged; repeated restores add further copies.

Tasks keep their notes, priorities, status, and due dates. Calendars keep colors,
visibility, event details, time zones, recurrence, and all-day dates. IDs are
recreated for the destination account, and links to included pages are remapped.
Event page links outside the selected workspace are omitted; ordinary text links
outside the archive retain their original destination.

The archive is validated before import. Workspace pages, tasks, calendars, and
events are imported in one transaction. A failed restore rolls back database
changes and cleans up newly copied attachment files.

## Compatibility and limits

- Version 1 archives from older releases still restore pages/files, without tasks
  or calendars. Data absent from an old archive cannot be recovered from it.
- Older applications cannot read version 2 archives. Upgrade to 0.4.0 or later.
- Archives are **not encrypted**. They exclude passwords, database credentials,
  and saved sessions, but their content and attached files are readable.
- Saved template libraries sync between devices in 0.6.0 but are **not included** in workspace backup archives.
- Markdown/HTML exports remain page/file-only.
- Limits: 256 MB uncompressed archive, 32 MB manifest, 100 MB per attached file,
  20,000 tasks, 1,000 calendars, and 20,000 events per archive.

For a full offline recovery copy, close nojeon and preserve the complete account
cache under `%LOCALAPPDATA%\Notion\Cloud`, including the SQLite database, assets,
templates, and Recovery folder. Recovery snapshots can depend on shared files in
`Recovery/Blobs`; keep the whole folder together. Sync is not a replacement for
independent portable backups.

When migrating from 0.5.0, export each workspace in the old local edition, then
restore it after signing into the cloud edition. Old local accounts and saved
template libraries do not migrate automatically. The existing MySQL database
and legacy profile are left untouched.

## Page artwork

Archives containing covers/icons use version 3. Image files are included and restored with the destination account's ownership. Upgrade to nojeon 0.5.0 or later before restoring version 3; older version 1/2 archives remain readable. Markdown/HTML exports currently omit page covers/icons.
