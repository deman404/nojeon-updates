# Install nojeon 0.6.0

## Requirements

- Windows x64.
- Internet for first-time signup/login and cloud sync.
- No MySQL server, database credentials, or .NET SDK.

The installer and portable package include the .NET runtime. This is an unsigned
desktop preview using the project's .NET 11 release-candidate runtime.

## Install and sign in

1. [Download the Windows installer](https://github.com/deman404/nojeon-updates/releases/download/v0.6.0/nojeon-0.6.0-win-x64-Setup.exe).
   [Release notes](https://github.com/deman404/nojeon-updates/releases/tag/v0.6.0) and [checksums](https://github.com/deman404/nojeon-updates/releases/download/v0.6.0/SHA256SUMS.txt).
2. Close other nojeon windows and run Setup. Installation is per Windows user.
   For a portable copy, extract the ZIP from the release page and run `nojeon.exe`.
3. Create a cloud account. Passwords require 12–128 characters.
4. Open the confirmation email, confirm your address, then return to the app and log in.
5. Start working. Your local SQLite cache is created automatically.

Sign in online once on each PC before relying on offline access. Existing cached
accounts can reopen their workspace without an internet connection.

## Upgrade from 0.5.0

Before installing, use the previous local edition to export a `.notionbackup`
for each workspace. Keep the old database and local profile until you have
checked the restored content. Then install 0.6.0, create your cloud account, and
restore the archives through **Settings / Import and export**.

The old local account does not automatically become a cloud account. Workspace
archives preserve pages, files, tasks, and calendars. Old template libraries are
separate and do not migrate automatically. nojeon does not delete your old MySQL
database or legacy local files.

## Troubleshooting

| What happened | What to do |
| --- | --- |
| Confirmation email is missing | Check Spam, wait, then use **Resend confirmation email** on the login screen |
| First login fails offline | Connect once to authenticate and create the cache |
| Sync says offline | Keep working; local edits are queued and retried when connected |
| A sync conflict appears | Click the sync status and choose this PC or the cloud; the replaced version is kept in recovery |
| Local storage fails | Check disk space and access to your Windows app-data directory |
| The account is open elsewhere | Close the other nojeon window holding this account cache |
| A page link does not open | Sign in to its owning account and check Trash; portable copies do not register the Windows protocol automatically |

Email delivery is rate-limited. Repeated resend requests do not speed it up.

## Uninstall

Uninstall removes the application and shortcuts while retaining local data and
cloud data. Signing out clears saved login credentials, not cached workspace
content. Keep portable backups of important work.

[How sync works](CLOUD-SYNC.md) · [User guide](USER-GUIDE.md)
