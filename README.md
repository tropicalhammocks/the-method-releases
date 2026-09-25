# The Method — installers

This repository holds the current installers for **The Method**, a personal to-do app, one for Windows and one for Mac, and a small `latest.json` describing them. The app itself is built from a separate, private repository; nothing here is source code.

Only the current version is kept. Each release replaces these files rather than adding to them.

## Installing it on a Mac

1. In the list of files above, click the one ending in `.dmg`, then download it with the download button.
2. Open it and drag **The Method** into **Applications**. Then eject the disk image (the drive in Finder's sidebar), and always open the app from Applications. A copy opened from inside the disk image can't update itself.
3. Open **The Method** from Applications. The first time, macOS stops it with a message saying it could not verify the app. Click **Done**.
4. Open **System Settings**, then **Privacy & Security**, and scroll down. Next to the line about The Method being blocked, click **Open Anyway**, confirm with your password or Touch ID, and click **Open Anyway** once more.

That refusal is macOS being careful, not a sign of anything wrong: the app isn't signed with an Apple developer certificate. You only do this once. Afterwards it opens normally, and updates install without asking again.

On macOS 14 or earlier there is a shortcut for step 4: right-click (or Control-click) the app in Applications, choose **Open**, then **Open** again. macOS 15 took that shortcut away, so there it has to be System Settings.

One Mac build covers both Apple Silicon and Intel machines.

## Is this safe to download?

Every installer here is signed with the project's own key, and an installed copy of The Method refuses any update whose signature does not match the key built into it. That check is the point of this repository: it lets the app fetch updates from a public address without having to trust the address.

The installers are not signed with an Apple or Windows certificate, so macOS asks as described above, and Windows SmartScreen warns on first run.
