# Bossa — installers

This repository holds the current installers for **Bossa**, a personal to-do app (called The Method until 30 Sep 2026), and a small `latest.json` describing them for the app's update check. The app itself is built from a separate, private repository; nothing here is source code.

The installers are in the **`bossa`** folder. Only the current version is kept, and each release replaces the files rather than adding to them. The quickest way to get them is the Download buttons on your dashboard at [bossa.day](https://bossa.day/dashboard/).

The files at the top level are **The Method**'s last version (0.76.0). They stay so that copies of The Method keep working, but they no longer receive updates. Bossa installs beside The Method rather than over it: install Bossa once, copy your list across, then uninstall The Method.

## Installing it on Windows

1. In the `bossa` folder, open `Bossa-setup.exe` and download it with the download button.
2. Run it. Windows shows a blue box, "Windows protected your PC". Click **More info**, then **Run anyway**.

That box appears because these installers aren't signed with a Windows certificate. From the public launch, the Windows app comes from the Microsoft Store, which signs it.

## Installing it on a Mac

1. In the `bossa` folder, open `Bossa.dmg` and download it with the download button.
2. Open it and drag **Bossa** into **Applications**. Then eject the disk image (the drive in Finder's sidebar), and always open the app from Applications. A copy opened from inside the disk image can't update itself.
3. Open **Bossa** from Applications. The first time, macOS stops it with a message saying it could not verify the app. Click **Done**.
4. Open **System Settings**, then **Privacy & Security**, and scroll down. Next to the line about Bossa being blocked, click **Open Anyway**, confirm with your password or Touch ID, and click **Open Anyway** once more.

That refusal is macOS being careful, not a sign of anything wrong: the app isn't yet signed with an Apple developer certificate. You only do this once. Afterwards it opens normally, and updates install without asking again.

On macOS 14 or earlier there is a shortcut for step 4: right-click (or Control-click) the app in Applications, choose **Open**, then **Open** again. macOS 15 took that shortcut away, so there it has to be System Settings.

One Mac build covers both Apple Silicon and Intel machines.

## Is this safe to download?

Every update here carries a signature made with the project's own key, and an installed copy of Bossa refuses any update whose signature doesn't match the key built into it. That check is the point of this repository: it lets the app fetch updates from a public address without having to trust the address.

The installers themselves are not yet signed with an Apple or Windows certificate, so macOS and Windows ask as described above the first time.
