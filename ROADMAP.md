# Roadmap

Planned work is subject to change. No release date or cloud provider is committed yet.

## Next milestone: cloud database

The next major step is adding cloud database support. The intended outcome is easier access to hosted data, with a clear setup and migration experience.

Before release, the work needs to cover:

- Choose the hosting provider and secure application access model.
- Define account authentication, authorization, and ownership boundaries.
- Design migration from existing MySQL databases, including backups and recovery.
- Decide how attachments and calendar data are stored and transferred.
- Define behavior when the connection is unavailable and when changes conflict.
- Verify upgrade, migration, backup, and restore flows.
- Publish setup instructions, privacy information, and any hosting costs or limits.

Cloud database support does not by itself promise offline synchronization, live collaboration, shared workspaces, or external calendar integration. Those capabilities require separate scope and verification.

## Further improvements

- Calendar export and inclusion in account-level backups.
- A supported stable .NET runtime after verification.
- Code signing and a clear application update policy.
- Accessibility, keyboard navigation, and large-workspace performance improvements.

Follow the changelog and Releases page for features that have actually shipped.
