# Installation and setup

## Requirements

- Windows x64.
- MySQL Community Server 8 or newer, installed and running separately.
- A nojeon Windows installer or portable package from a published release.

The 0.2.0 desktop preview bundles a .NET 11 release-candidate runtime and is currently unsigned. You do not need to install the .NET SDK to use it.

## Install

1. [Download the Windows x64 installer](https://github.com/deman404/nojeon-updates/releases/download/v0.2.0/nojeon-0.2.0-win-x64-Setup.exe) and read the [release notes and installer SHA-256](https://github.com/deman404/nojeon-updates/releases/tag/v0.2.0).
2. Run the Windows Setup executable. Installation is per Windows user and does not require administrator access. The current public release provides the installer; a portable ZIP is not attached.
3. Start MySQL, then open nojeon.
4. Enter the MySQL server, port, database name, username, and password on the setup page. Use a dedicated database and an account permitted to create or update its tables. For a new database name, use at most 45 letters, numbers, or underscores.
5. Choose **Test connection**, then **Create / update database and continue**. Back up an existing database before updating its schema.
6. Create an app account, then start a page from the sidebar. This account is separate from a notion.com account. App passwords require 12–128 characters.

## Upgrade and uninstall

Back up your data and close all nojeon windows before upgrading. Run the new installer over the existing installation; database setup applies required schema updates. Uninstalling removes application files and shortcuts but retains the MySQL database and local workspace files.

## Connection problems

Check that MySQL is running, the server and port are correct, and the database account has the required permissions. Use **Database setup** on the login page to change saved connection settings. Sign out before switching databases.

The current preview does not provide a hosted cloud database or automatic cloud migration.
