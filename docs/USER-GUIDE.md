# How nojeon works

## Pages and writing

Create a page from the sidebar and organize related pages beneath it. Use favorites for frequent pages. Write text, headings, nested lists, tasks, quotes, and code; insert links, images, attachments, and editable tables. Type `/` in an empty block to open block commands. Drag blocks to reorder them.

Open multiple pages in tabs or use side peek to reference a second page. Search with **Ctrl+K** to find titles, content, tables, and attachment names.

Pages autosave to SQLite on this PC. Watch the local save status and the separate cloud sync status. Offline changes are queued for reconnect; if a local write fails, check disk space and use Retry. Encrypted recovery drafts help preserve unsaved edits.

## Page covers and icons

Choose **Add cover** above a page title for the background gallery or image uploads. Choose **Add icon** for searchable color emoji or your own logo. Click the existing icon to change/remove it. See [the artwork guide](PAGE-ARTWORK.md).

## Reusable templates

Open **Templates** in the sidebar to browse the gallery. Search, filter categories, open a card, and choose **Use this template**. Save your own layout using a page menu > Save as template. See [the template guide](TEMPLATES.md).

## Tasks

Open **Tasks** in the sidebar. Use **All tasks** for the table or **Board** for status columns. Create a task with a title, notes, priority, due date, and status. Open a title to edit, click the status tag to advance it, or use the dots menu to change status or delete. Search titles/notes and filter by status and due date. See [the task guide](TASKS.md).

## Calendar

Open **Calendar** from the sidebar. Choose Day, 3 days, Week, or Month. Click or drag a time slot to create an event. Click an event to edit its details, then choose Save or press **Ctrl+Enter**. Drag an event to move it; drag its bottom edge to resize it.

Events support colored calendars, all-day entries, linked pages, and daily, weekly, or monthly recurrence. Changes to repeating events affect the whole series. Google/iCloud synchronization, invitations, notifications, and individual-occurrence exceptions are not available.

## Import, export, and backup

Use **Settings > Import / export** to import Markdown/HTML documents or folders, export a page with referenced files, or save and restore a workspace archive. Repeat workspace backups for each workspace.

**Workspace archives include tasks and account calendars/events; version 3 also preserves page artwork.** Restore creates a new workspace and separate calendar copies. Older archives contain pages/files only. Saved template libraries are not included. See [the backup guide](BACKUPS.md). Workspace backup archives contain readable content and files and are not encrypted; keep them private. Markdown/HTML conversion does not preserve every complex layout exactly.

## Where data lives

Supabase handles cloud accounts and private workspace sync. Each PC has an account-specific SQLite cache beneath `%LOCALAPPDATA%\Notion\Cloud\<project-host>\<account-id>`. Attachments, artwork, and saved templates sync through private Storage. Saved login tokens and recovery drafts use Windows protection; workspace caches and backup archives contain readable content.

Cloud + offline is available in 0.6.0. Appearance preferences remain local. Conflicts require a version choice and keep a recovery copy. See [cloud sync and recovery](CLOUD-SYNC.md).

## Useful shortcuts

| Shortcut | Action |
| --- | --- |
| Ctrl+K | Search |
| Ctrl+B / Ctrl+I / Ctrl+U | Bold / italic / underline |
| Ctrl+Z / Ctrl+Y | Undo / redo |
| Tab / Shift+Tab in lists | Indent / outdent |
| Ctrl+Tab / Ctrl+Shift+Tab | Switch page tabs |
| Ctrl+W | Close the active tab or search view |
| T in Calendar | Today |
| N in Calendar | New event |

## Troubleshooting

If a local save fails, check disk space and retain recovery drafts. If cloud sync is offline, local edits remain queued for reconnect. If a page link fails, sign into its owning account and check Trash. The installer registers Windows `notionlocal://page/...` links; the portable ZIP does not register the Windows protocol handler.
