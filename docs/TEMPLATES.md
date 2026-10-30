# Reusable page templates

Open **Templates** in the sidebar to browse the full gallery page. Search by name
or description, filter by Projects/Meetings/Personal/Your templates, or sort by
name. Cards show real layout previews, category, and creator. Select a card to
open its detail page, then choose **Use this template**. The app adds a new
top-level page to your current workspace and
saves it through the normal autosave/recovery flow. The library is also available
from the collapsed sidebar.

Three starter layouts are included: **Meeting notes**, **Project brief** (with a
milestone table), and **Weekly plan**. Starter layouts cannot be renamed/deleted.

To reuse your own layout, open a page's **···** menu (on its header or sidebar row)
and choose **Save as template**. Enter a unique name. The saved template includes
that page, active nested pages, rich formatting, tables, checklists, and copies of
its image/attachment files. Trashed children are omitted. Templates preserve
checkbox states; uncheck completed items before saving if they should start empty.

Each use creates fresh page/block/file IDs and remaps links between included
pages. Editing the original page or a created copy does not change the template.
Deleting the template does not remove pages already made from it. External page
links retain their original destinations.

Open one of your templates in the gallery to **Rename** it or **Delete** it
after confirmation. Save the edited page again under a new name to create another
version of a layout. Existing pages are never replaced by applying a template.

The gallery works in Light/Dark mode and adjusts its card columns to the available
width. It contains bundled starter layouts and your own templates, not public
community listings or online downloads.

Saved templates are account-scoped local files under
`%LOCALAPPDATA%\Notion\Templates\<account-id>` (or the configured local profile).
They persist across app restarts, but are not cloud-synchronized or included in
workspace backup archives. Their archives contain readable content/files, so keep
the local profile private. Tasks and calendars are not part of a page template.

Limits: 100 custom templates per account, 1,000 pages and 20,000 blocks per template,
with the archive limits of 256 MB total, 32 MB manifest, and 100 MB per attachment.
Available in nojeon 0.4.0 and later.
