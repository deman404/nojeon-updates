# Local calendar

Choose **Calendar** in the workspace sidebar or its collapsed rail. It opens a
full calendar workspace with a mini month, colored calendar list, date navigation,
time grid, and event details/upcoming panel. **Back to workspace** returns to notes.

## Events and calendars

- Click a timed slot or drag a range to create an event. Click the all-day row for
  an all-day event. The **+** button and `N` also start a new event.
- Click an event to edit its title, calendar, dates/times, location, meeting link,
  linked page, notes, and recurrence. Choose **Save** or press `Ctrl+Enter`.
- Drag a timed event to move it between days/times; drag its bottom edge to resize.
  Times snap to 15-minute intervals. Overlapping events use separate columns.
- Deleting an event requires confirmation. Repeating events are edited/deleted as
  a whole series, and dragging/resizing a series asks for confirmation.
- Use the calendar checkboxes to show/hide calendars. The calendar menu supports
  rename, color, and confirmed deletion of the calendar and its events. At least
  one calendar is retained.
- Link an owned active page to keep notes nearby. Opening it returns to the
  correct workspace. Event URLs support HTTP/HTTPS links opened on explicit click.

Unsaved event edits prompt before leaving or switching events. The event editor
uses an explicit Save action; drag/resize changes save after release. Workspace
page autosave is independent.

## Navigation

The view selector supports **Day**, **3 days**, **Week**, and **Month**. Weeks begin
on Monday. Use the mini month, previous/next arrows, or Today to change dates.
The selected view and display time zone are saved per account.

![Month calendar](screenshots/calendar-month.png)

| Key | Action |
| --- | --- |
| `T` | Today |
| `N` | New event |
| `D`, `W`, `M` | Day, week, month |
| `Left`, `Right` | Previous/next date range |
| `Ctrl+Enter` | Save the open event |
| `Escape` | Close the event editor, with an unsaved-changes prompt if needed |

Letter/navigation shortcuts do not intercept text input. Escape leaves an open
date/calendar selector to handle its own dismissal first.

## Dates, time zones, and recurrence

Events store UTC start/end instants and an event time-zone ID. The display zone
can change independently. Editing a title in another display zone preserves the
event's recurrence zone. All-day dates retain their original calendar dates when
the display time zone changes.

Daily, weekly, and monthly repeats preserve wall-clock time across daylight-saving
changes. Monthly repeats use the original day and clamp short months without
drifting subsequent months. Repeat-until dates are inclusive. Nonexistent spring
clock-change times are rejected for direct entry and skipped during recurrence;
ambiguous autumn entries use standard time consistently. Single events retain
their stored UTC instant, including during the repeated autumn hour.

## Persistence and setup

`AddLocalCalendars` adds account-owned `Calendars` and `CalendarEvents` tables.
Startup detects missing migrations and offers database setup/update. Developers
can also apply the schema with:

```powershell
dotnet ef database update --project notion.csproj --startup-project notion.csproj
```

Calendars belong to the signed-in account across its workspaces. Database queries
and writes enforce ownership, and revision tokens reject stale edits/deletes.
Visibility and event metadata survive restart. New accounts start with an empty
Personal calendar; demonstration events exist only in the isolated verifier.

Calendar records are account-level data, separate from workspace snapshots.
Version 0.4.0 and later write version 2 `.notionbackup` archives containing all calendars
and events for the signed-in account, plus the selected workspace’s tasks, pages,
and files. Restore creates separate calendar copies without merging or replacing
existing calendars. Page links within the restored workspace are remapped; links
to pages outside that workspace are omitted. Repeated restore creates more copies.
The published 0.3.0 installer and older version 1 archives are page/file-only; keep
using MySQL backups for calendars until upgrading to a build with version 2 support.
Google/iCloud synchronization, invitations, notifications, and single-occurrence
exceptions are not part of this local calendar version.

