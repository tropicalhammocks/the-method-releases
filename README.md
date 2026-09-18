# The Method — installers

This repository holds the current Windows installer for **The Method**, a personal to-do app, and a small `latest.json` describing it. The app itself is built from a separate, private repository; nothing here is source code.

Only the current version is kept. Each release replaces these files rather than adding to them.

## Is this safe to download?

Every installer here is signed with the project's own key, and an installed copy of The Method refuses any update whose signature does not match the key built into it. That check is the point of this repository: it lets the app fetch updates from a public address without having to trust the address.

The installer is not signed with a Windows code-signing certificate, so SmartScreen will warn on first run.
