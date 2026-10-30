# Page covers and icons

Open a page and choose **Add cover** above the title. Browse 12 built-in gradients,
abstract backgrounds, and patterns, or use **Upload image**. Choosing a built-in
cover saves it as a managed PNG with the page. Use **Change cover** or **Remove
cover** on the banner afterward.
Covers fill the available width and crop around the center; manual repositioning
is not included in this version.

Choose **Add icon** to browse 205 bundled color emoji, search by name, or filter
categories such as Nature, Travel, and Work & hobbies. Click an emoji to apply it
immediately. **Upload image** lets you use your own logo. Click the existing icon
to reopen the picker or remove it. Page icons also appear beside page titles in
the sidebar and in subpage lists. No internet connection is needed for the picker.

Emoji graphics are Twemoji (Twitter, Inc. and contributors), licensed CC BY 4.0.
Attribution and the full license are included with application packaging.

Supported uploads: PNG, JPEG, GIF, BMP, and ICO, up to 20 MB and 40 million pixels.
Files are copied into account-owned managed storage, so changes to the original
file do not affect the page. Image icons preserve their proportions. Remote image
URLs and animated playback are not supported.

Artwork saves through the normal page autosave/recovery flow and is preserved by
duplication, trash/restore, workspace backups, and custom page templates. Restoring
a backup into another account copies the images and remaps their ownership.
Images are kept in local managed-file storage; the database stores references.

Archives containing artwork use format version 3 so older applications cannot
silently drop covers/icons. New builds continue to read version 1 and 2 backups
and older template archives. Workspace task/calendar backup behavior is unchanged.
Markdown/HTML exports currently omit page covers/icons; use a workspace backup
for exact page artwork.

`AddPageCoversAndIcons` adds optional columns to Pages; startup database setup
applies this migration. Available in nojeon 0.5.0 and later.
