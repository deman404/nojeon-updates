# Task management

Open **Tasks** in the sidebar (also available when the sidebar is collapsed).
Tasks belong to the active workspace and are saved in MySQL. Switching workspaces
shows that workspace's tasks; other accounts cannot read or modify them.

Choose **New task**, enter a title, optional notes and due date, status, and
priority, then **Save**. Statuses are **To do**, **In progress**, and **Done**;
priorities are **Low**, **Normal**, **High**, and **Urgent**. Due dates are calendar
dates interpreted using your PC's local date; completed tasks are never overdue.

- **All tasks** shows a compact table sorted by status, due date, priority, then
  newest first. Click a title to edit or a status tag to advance its state.
- **Board** groups the same tasks into three status columns. The column's **+**
  and **New task** actions create a task with that column's status.
- Each row/card has a **···** menu for opening, moving status, and deleting.
  **Move to next status** advances To do → In progress → Done → To do. Open a
  task to choose any status directly. Board drag-and-drop is not implemented.
- Search matches titles and notes. Combine it with status and due-date filters.
- Clicking a title or **Open task** opens the page-style details window;
  Cancel/close asks before discarding changed fields.
- **Delete** permanently removes a task after confirmation.
- **Refresh** reloads changes from other windows. Stale edits and deletes are
  rejected; keep any needed editor text, refresh, then reopen the task.

Tasks save explicitly rather than through page autosave. Database failures keep
editor text available for retry. Tasks do not currently have offline drafts,
reminders, recurring schedules, assignees, or calendar synchronization.

**Backup:** existing `.notionbackup` workspace archives and Markdown/HTML exports
cover pages/files, not tasks. Back up MySQL to preserve tasks. Deleting a workspace
also deletes its tasks; restore of a page archive does not restore tasks.

The `AddWorkspaceTasks` migration adds the Tasks table. Existing databases are
offered a database update through the normal startup/setup flow.
