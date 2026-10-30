# How nojeon works

## Pages and writing

Create a page from the sidebar and organize related pages beneath it. Use favorites for frequent pages. Write text, headings, nested lists, tasks, quotes, and code; insert links, images, attachments, and editable tables. Type `/` in an empty block to open block commands. Drag blocks to reorder them.

Open multiple pages in tabs or use side peek to reference a second page. Search with **Ctrl+K** to find titles, content, tables, and attachment names.

Pages autosave. Watch the save status; if a write fails, restore the database connection and use Retry. Encrypted local recovery drafts help preserve unsaved changes.

## Reusable templates

Open **Templates** in the sidebar to browse the gallery. Search, filter categories, open a card, and choose **Use this template**. Save your own layout using a page menu > Save as template. See [the template guide](TEMPLATES.md).

## Tasks

Open **Tasks** in the sidebar. Use **All tasks** for the table or **Board** for status columns. Create a task with a title, notes, priority, due date, and status. Open a title to edit, click the status tag to advance it, or use the dots menu to change status or delete. Search titles/notes and filter by status and due date. See [the task guide](TASKS.md).

## Calendar

Open **Calendar** from the sidebar. Choose Day, 3 days, Week, or Month. Click or drag a time slot to create an event. Click an event to edit its details, then choose Save or press **Ctrl+Enter**. Drag an event to move it; drag its bottom edge to resize it.

Events support colored calendars, all-day entries, linked pages, and daily, weekly, or monthly recurrence. Changes to repeating events affect the whole series. Google/iCloud synchronization, invitations, notifications, and individual-occurrence exceptions are not available.

## Import, export, and backup

Use **Settings > Import / export** to import Markdown/HTML documents or folders, export a page with referenced files, or save and restore a workspace archive. Repeat workspace backups for each workspace.

**Version 2 workspace archives include the selected workspace's tasks and all account calendars/events.** Restore creates a new workspace and separate calendar copies. Older archives contain pages/files only. Saved template libraries are not included. See [the backup guide](BACKUPS.md). Workspace backup archives contain readable content and files and are not encrypted; keep them private. Markdown/HTML conversion does not preserve every complex layout exactly.

## Where data lives

Accounts, workspaces, pages, blocks, and calendar records use your configured MySQL database. Local preferences, protected connection settings, saved sessions, recovery drafts, and default imported files use `%LOCALAPPDATA%\Notion`, unless configured otherwise. Protected local settings and drafts use Windows protection for the current Windows account.

Cloud database support is planned. Do not assume that local attachments or existing databases are automatically synchronized to the cloud.

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

If saving fails, check the MySQL connection and retain recovery drafts. If a page link fails, sign into its owning account and check Trash. The installer registers Windows `notionlocal://page/...` links; the portable ZIP does not register the Windows protocol handler.
