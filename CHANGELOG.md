# Product updates

## 0.4.0 — Templates & planning backups — 2026-10-30

- Added a full template gallery with preview cards, categories, search, sorting, details, and Light/Dark support.
- Included Meeting notes, Project brief, and Weekly plan starter layouts.
- Added Save as template, reuse, rename, and delete for local account-scoped templates, with independent nested pages and attachments.
- Version 2 workspace archives now include workspace tasks and all account calendars/events.
- Restore creates separate calendar copies and remaps links to restored pages, preserving recurrence, time zones, and all-day dates. Older version 1 archives remain readable.
- Refreshed the branded thumbnail and gallery screenshots.

Saved template libraries are local and not included in workspace archives. Backups are not encrypted. Older app versions cannot read version 2 archives. No new database migration is introduced by this release.

[Release and downloads](https://github.com/deman404/nojeon-updates/releases/tag/v0.4.0)


## 0.3.0 — Tasks, your way — 2026-10-30

- Added workspace task management in a compact table and colored Kanban board.
- Added task titles, notes, priorities, optional due dates, status changes, and confirmed deletion.
- Added title/notes search, status/due-date filters, and completion/overdue counts.
- Refined the interface with an inline header, vector icons, colored tags, and page-style task details.
- Added the Tasks database migration with workspace/account isolation and conflict checks.
- Published fresh screenshots, a task guide, installer, portable ZIP, and SHA-256 checksums.

**Upgrade:** back up MySQL and local files, close the app, install 0.3.0, and complete database setup/update. Tasks and calendars require MySQL backups; page archives do not include them. Cloud database support remains planned.

[Release and downloads](https://github.com/deman404/nojeon-updates/releases/tag/v0.3.0)


## Documentation hub — 2026-10-30

- Established a separate public home for user instructions, release announcements, and the roadmap.
- Documented the current MySQL setup, page editing, calendar, and backup behavior.
- Identified cloud database support as the next planned milestone.

This is a documentation update, not a new application release.

## 0.2.0 — existing desktop preview

- Introduced the nojeon name and original app icon.
- Added a local calendar with day, 3-day, week, and month views, colored calendars, recurring events, and linked notes.
- Includes rich block editing, nested pages, multiple workspaces, tabs, side peek, search, import/export, and workspace backups.

Requires Windows x64 and a separately configured MySQL 8+ database. Cloud database support is not included. The [Windows installer is now available](https://github.com/deman404/nojeon-updates/releases/tag/v0.2.0) in this repository. Its SHA-256 matches the original published installer.
